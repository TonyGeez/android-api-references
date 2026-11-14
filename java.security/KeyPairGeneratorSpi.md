# KeyPairGeneratorSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyPairGeneratorSpi

```
abstract class KeyPairGeneratorSpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.KeyPairGeneratorSpi](https://developer.android.com/reference/kotlin/java/security/KeyPairGeneratorSpi#) |

| Known Direct Subclasses [KeyPairGenerator](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator) |---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------| | [KeyPairGenerator](https://developer.android.com/reference/kotlin/java/security/KeyPairGenerator) | The KeyPairGenerator class is used to generate pairs of public and private keys. | |

This class defines the*Service Provider Interface* (**SPI** ) for the`KeyPairGenerator`class, which is used to generate pairs of public and private keys.

All the abstract methods in this class must be implemented by each cryptographic service provider who wishes to supply the implementation of a key pair generator for a particular algorithm.

In case the client does not explicitly initialize the KeyPairGenerator (via a call to an`initialize`method), each provider must supply (and document) a default initialization. For example, the*Sun*provider uses a default modulus size (keysize) of 1024 bits.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------|---|
| [KeyPairGeneratorSpi](https://developer.android.com/reference/kotlin/java/security/KeyPairGeneratorSpi#KeyPairGeneratorSpi())`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [KeyPair](https://developer.android.com/reference/kotlin/java/security/KeyPair)! | [generateKeyPair](https://developer.android.com/reference/kotlin/java/security/KeyPairGeneratorSpi#generateKeyPair())`()` Generates a key pair. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [initialize](https://developer.android.com/reference/kotlin/java/security/KeyPairGeneratorSpi#initialize(kotlin.Int,%20java.security.SecureRandom))`(`keysize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `random:` ` [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom)!`)` Initializes the key pair generator for a certain keysize, using the default parameter set. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [initialize](https://developer.android.com/reference/kotlin/java/security/KeyPairGeneratorSpi#initialize(java.security.spec.AlgorithmParameterSpec,%20java.security.SecureRandom))`(`params:` ` [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)!`, `random:` ` [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom)!`)` Initializes the key pair generator using the specified parameter set and user-provided source of randomness. |

## Public constructors

### KeyPairGeneratorSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyPairGeneratorSpi()
```

## Public methods

### generateKeyPair

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun generateKeyPair(): KeyPair!
```

Generates a key pair. Unless an initialization method is called using a KeyPairGenerator interface, algorithm-specific defaults will be used. This will generate a new key pair every time it is called.

| Return ||
|----------------------------------------------------------------------------------|------------------------------|
| [KeyPair](https://developer.android.com/reference/kotlin/java/security/KeyPair)! | the newly generated`KeyPair` |

### initialize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun initialize(
    keysize: Int, 
    random: SecureRandom!
): Unit
```

Initializes the key pair generator for a certain keysize, using the default parameter set.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keysize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the keysize. This is an algorithm-specific metric, such as modulus length, specified in number of bits. |
| `random` | [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom)!:the source of randomness for this generator. |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------|
| `java.security.InvalidParameterException` | if the`keysize`is not supported by this KeyPairGeneratorSpi object. |

### initialize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun initialize(
    params: AlgorithmParameterSpec!, 
    random: SecureRandom!
): Unit
```

Initializes the key pair generator using the specified parameter set and user-provided source of randomness.

This concrete method has been added to this previously-defined abstract class. (For backwards compatibility, it cannot be abstract.) It may be overridden by a provider to initialize the key pair generator. Such an override is expected to throw an InvalidAlgorithmParameterException if a parameter is inappropriate for this key pair generator. If this method is not overridden, it always throws an UnsupportedOperationException.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec)!:the parameter set used to generate the keys. |
| `random` | [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom)!:the source of randomness for this generator. |

| Exceptions ||
|----------------------------------------------------|------------------------------------------------------------------------|
| `java.security.InvalidAlgorithmParameterException` | if the given parameters are inappropriate for this key pair generator. |
