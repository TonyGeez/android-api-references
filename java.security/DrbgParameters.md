# DrbgParameters

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DrbgParameters

```
open class DrbgParameters
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.DrbgParameters](../java/security/DrbgParameters.md) |

This class specifies the parameters used by a DRBG (Deterministic Random Bit Generator).

According to [NIST Special Publication 800-90A Revision 1, Recommendation for Random Number Generation Using Deterministic Random Bit Generators](http://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-90Ar1.pdf) (800-90Ar1),
A DRBG is based on a DRBG mechanism as specified in this Recommendation and includes a source of randomness. A DRBG mechanism uses an algorithm (i.e., a DRBG algorithm) that produces a sequence of bits from an initial value that is determined by a seed that is determined from the output of the randomness source."

The 800-90Ar1 specification allows for a variety of DRBG implementation choices, such as:

- an entropy source,
- a DRBG mechanism (for example, Hash_DRBG),
- a DRBG algorithm (for example, SHA-256 for Hash_DRBG and AES-256 for CTR_DRBG. Please note that it is not the algorithm used in java.security.SecureRandom#getInstance, which we will call a *SecureRandom algorithm* below),
- optional features, including prediction resistance and reseeding supports,
- highest security strength.

These choices are set in each implementation and are not directly managed by the `SecureRandom` API. Check your DRBG provider's documentation to find an appropriate implementation for the situation.

On the other hand, the 800-90Ar1 specification does have some configurable options, such as:

- required security strength,
- if prediction resistance is required,
- personalization string and additional input.

A DRBG instance can be instantiated with parameters from an [DrbgParameters.Instantiation](../java/security/DrbgParameters.Instantiation.md) object and other information (for example, the nonce, which is not managed by this API). This maps to the `Instantiate_function` defined in NIST SP 800-90Ar1.

A DRBG instance can be reseeded with parameters from a [DrbgParameters.Reseed](../java/security/DrbgParameters.Reseed.md) object. This maps to the `Reseed_function` defined in NIST SP 800-90Ar1. Calling [SecureRandom.reseed()](../java/security/SecureRandom.md)) is equivalent to calling [SecureRandom.reseed(SecureRandomParameters)](../java/security/SecureRandom.md)) with the effective instantiated prediction resistance flag (as returned by [SecureRandom.getParameters()](../java/security/SecureRandom.md))) with no additional input.

A DRBG instance generates data with additional parameters from a [DrbgParameters.NextBytes](../java/security/DrbgParameters.NextBytes.md) object. This maps to the `Generate_function` defined in NIST SP 800-90Ar1. Calling java.security.SecureRandom#nextBytes(byte\[\]) is equivalent to calling [SecureRandom.nextBytes(byte[], SecureRandomParameters)](https://developer.android.com/reference/kotlin/java/security/SecureRandom#nextBytes(kotlin.ByteArray,%20java.security.SecureRandomParameters)) with the effective instantiated strength and prediction resistance flag (as returned by [SecureRandom.getParameters()](../java/security/SecureRandom.md))) with no additional input.

A DRBG should be implemented as a subclass of [SecureRandomSpi](../java/security/SecureRandomSpi.md). It is recommended that the implementation contain the 1-arg [constructor](../java/security/SecureRandomSpi.md)) that takes a `DrbgParameters.Instantiation` argument. If implemented this way, this implementation can be chosen by any `SecureRandom.getInstance()` method. If it is chosen by a `SecureRandom.getInstance()` with a [SecureRandomParameters](../java/security/SecureRandomParameters.md) parameter, the parameter is passed into this constructor. If it is chosen by a `SecureRandom.getInstance()` without a `SecureRandomParameters` parameter, the constructor is called with a `null` argument and the implementation should choose its own parameters. Its [SecureRandom.getParameters()](../java/security/SecureRandom.md)) must always return a non-null effective `DrbgParameters.Instantiation` object that reflects how the DRBG is actually instantiated. A caller can use this information to determine whether a `SecureRandom` object is a DRBG and what features it supports. Please note that the returned value does not necessarily equal to the `DrbgParameters.Instantiation` object passed into the `SecureRandom.getInstance()` call. For example, the requested capability can be [DrbgParameters.Capability.NONE](../java/security/DrbgParameters.Capability.md) but the effective value can be [DrbgParameters.Capability.RESEED_ONLY](../java/security/DrbgParameters.Capability.md) if the implementation supports reseeding. The implementation must implement the [SecureRandomSpi.engineNextBytes(byte[], SecureRandomParameters)](https://developer.android.com/reference/kotlin/java/security/SecureRandomSpi#engineNextBytes(kotlin.ByteArray,%20java.security.SecureRandomParameters)) method which takes a `DrbgParameters.NextBytes` parameter. Unless the result of [SecureRandom.getParameters()](../java/security/SecureRandom.md)) has its [capability](../java/security/DrbgParameters.Instantiation.md)) being [NONE](../java/security/DrbgParameters.Capability.md), it must implement [SecureRandomSpi.engineReseed(SecureRandomParameters)](../java/security/SecureRandomSpi.md)) which takes a `DrbgParameters.Reseed` parameter.

On the other hand, if a DRBG implementation does not contain a constructor that has an `DrbgParameters.Instantiation` argument (not recommended), it can only be chosen by a `SecureRandom.getInstance()` without a `SecureRandomParameters` parameter, but will not be chosen if a `getInstance` method with a `SecureRandomParameters` parameter is called. If implemented this way, its [SecureRandom.getParameters()](../java/security/SecureRandom.md)) must return `null`, and it does not need to implement either [SecureRandomSpi.engineNextBytes(byte[], SecureRandomParameters)](https://developer.android.com/reference/kotlin/java/security/SecureRandomSpi#engineNextBytes(kotlin.ByteArray,%20java.security.SecureRandomParameters)) or [SecureRandomSpi.engineReseed(SecureRandomParameters)](../java/security/SecureRandomSpi.md)).

A DRBG might reseed itself automatically if the seed period is bigger than the maximum seed life defined by the DRBG mechanism.

A DRBG implementation should support serialization and deserialization by retaining the configuration and effective parameters, but the internal state must not be serialized and the deserialized object must be reinstantiated.

Examples: 

```kotlin
SecureRandom drbg;
  byte[] buffer = new byte[32];
 
  // Any DRBG is OK
  drbg = SecureRandom.getInstance("DRBG");
  drbg.nextBytes(buffer);
 
  SecureRandomParameters params = drbg.getParameters();
  if (params instanceof DrbgParameters.Instantiation) {
      DrbgParameters.Instantiation ins = (DrbgParameters.Instantiation) params;
      if (ins.getCapability().supportsReseeding()) {
          drbg.reseed();
      }
  }
 
  // The following call requests a weak DRBG instance. It is only
  // guaranteed to support 112 bits of security strength.
  drbg = SecureRandom.getInstance("DRBG",
          DrbgParameters.instantiation(112, NONE, null));
 
  // Both the next two calls will likely fail, because drbg could be
  // instantiated with a smaller strength with no prediction resistance
  // support.
  drbg.nextBytes(buffer,
          DrbgParameters.nextBytes(256, false, "more".getBytes()));
  drbg.nextBytes(buffer,
          DrbgParameters.nextBytes(112, true, "more".getBytes()));
 
  // The following call requests a strong DRBG instance, with a
  // personalization string. If it successfully returns an instance,
  // that instance is guaranteed to support 256 bits of security strength
  // with prediction resistance available.
  drbg = SecureRandom.getInstance("DRBG", DrbgParameters.instantiation(
          256, PR_AND_RESEED, "hello".getBytes()));
 
  // Prediction resistance is not requested in this single call,
  // but an additional input is used.
  drbg.nextBytes(buffer,
          DrbgParameters.nextBytes(-1, false, "more".getBytes()));
 
  // Same for this call.
  drbg.reseed(DrbgParameters.reseed(false, "extra".getBytes()));
```

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Capability](../java/security/DrbgParameters.Capability.md) The reseedable and prediction resistance capabilities of a DRBG. |
| | [Instantiation](../java/security/DrbgParameters.Instantiation.md) DRBG parameters for instantiation. |
| | [NextBytes](../java/security/DrbgParameters.NextBytes.md) DRBG parameters for random bits generation. |
| --- | --- |
| | [Reseed](../java/security/DrbgParameters.Reseed.md) DRBG parameters for reseed. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open static [DrbgParameters.Instantiation](../java/security/DrbgParameters.Instantiation.md)! | [instantiation](../java/security/DrbgParameters.md))`(`strength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `capability:` ` [DrbgParameters.Capability](../java/security/DrbgParameters.Capability.md)!`, `personalizationString:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Generates a [DrbgParameters.Instantiation](../java/security/DrbgParameters.Instantiation.md) object. |
| open static [DrbgParameters.NextBytes](../java/security/DrbgParameters.NextBytes.md)! | [nextBytes](../java/security/DrbgParameters.md))`(`strength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `predictionResistance:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `additionalInput:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Generates a [NextBytes](../java/security/DrbgParameters.NextBytes.md) object. |
| open static [DrbgParameters.Reseed](../java/security/DrbgParameters.Reseed.md)! | [reseed](../java/security/DrbgParameters.md))`(`predictionResistance:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `additionalInput:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Generates a [Reseed](../java/security/DrbgParameters.Reseed.md) object. |
| --- | --- |

## Public methods

### instantiation

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun instantiation(
    strength: Int, 
    capability: DrbgParameters.Capability!, 
    personalizationString: ByteArray!
): DrbgParameters.Instantiation!
```

Generates a [DrbgParameters.Instantiation](../java/security/DrbgParameters.Instantiation.md) object.

| Parameters ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `strength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): security strength in bits, -1 for default strength if used in `getInstance`. |
| `capability` | [DrbgParameters.Capability](../java/security/DrbgParameters.Capability.md)!: capability |
| `personalizationString` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: personalization string as a byte array, can be `null`. The content of this byte array will be copied. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [DrbgParameters.Instantiation](../java/security/DrbgParameters.Instantiation.md)! | a new `Instantiation` object |

| Exceptions ||
|--------------------------------------|-------------------------------|
| `java.lang.NullPointerException` | if `capability` is `null` |
| `java.lang.IllegalArgumentException` | if `strength` is less than -1 |

### nextBytes

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun nextBytes(
    strength: Int, 
    predictionResistance: Boolean, 
    additionalInput: ByteArray!
): DrbgParameters.NextBytes!
```

Generates a [NextBytes](../java/security/DrbgParameters.NextBytes.md) object.

| Parameters ||
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `strength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): requested security strength in bits. If set to -1, the effective strength will be used. |
| `predictionResistance` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): prediction resistance requested |
| `additionalInput` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: additional input, can be `null`. The content of this byte array will be copied. |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------------------------------|--------------------------|
| [DrbgParameters.NextBytes](../java/security/DrbgParameters.NextBytes.md)! | a new `NextBytes` object |

| Exceptions ||
|--------------------------------------|-------------------------------|
| `java.lang.IllegalArgumentException` | if `strength` is less than -1 |

### reseed

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun reseed(
    predictionResistance: Boolean, 
    additionalInput: ByteArray!
): DrbgParameters.Reseed!
```

Generates a [Reseed](../java/security/DrbgParameters.Reseed.md) object.

| Parameters ||
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predictionResistance` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): prediction resistance requested |
| `additionalInput` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: additional input, can be `null`. The content of this byte array will be copied. |

| Return ||
|--------------------------------------------------------------------------------------------------------------|-----------------------|
| [DrbgParameters.Reseed](../java/security/DrbgParameters.Reseed.md)! | a new `Reseed` object |
