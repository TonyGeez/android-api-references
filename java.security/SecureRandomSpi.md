# SecureRandomSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SecureRandomSpi

```
abstract class SecureRandomSpi : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.SecureRandomSpi](../java/security/SecureRandomSpi.md) |

This class defines the*Service Provider Interface* (**SPI** ) for the [SecureRandom](../java/security/SecureRandom.md) class.

All the abstract methods in this class must be implemented by each service provider who wishes to supply the implementation of a cryptographically strong pseudo-random number generator.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SecureRandomSpi](../java/security/SecureRandomSpi.md))`()` Constructor without a parameter. |

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SecureRandomSpi](../java/security/SecureRandomSpi.md))`(`params:` ` [SecureRandomParameters](../java/security/SecureRandomParameters.md)!`)` Constructor with a parameter. |

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/security/SecureRandomSpi.md))`()` Returns a Human-readable string representation of this`SecureRandom`. |

| Protected methods ||
|--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [engineGenerateSeed](../java/security/SecureRandomSpi.md))`(`numBytes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the given number of seed bytes. |
| open [SecureRandomParameters](../java/security/SecureRandomParameters.md)! | [engineGetParameters](../java/security/SecureRandomSpi.md))`()` Returns the effective [SecureRandomParameters](../java/security/SecureRandomParameters.md) for this`SecureRandom`instance. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineNextBytes](../java/security/SecureRandomSpi.md))`(`bytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Generates a user-specified number of random bytes. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineNextBytes](../java/security/SecureRandomSpi.md))`(`bytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `params:` ` [SecureRandomParameters](../java/security/SecureRandomParameters.md)!`)` Generates a user-specified number of random bytes with additional parameters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineReseed](../java/security/SecureRandomSpi.md))`(`params:` ` [SecureRandomParameters](../java/security/SecureRandomParameters.md)!`)` Reseeds this random object with entropy input read from its entropy source with additional parameters. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineSetSeed](../java/security/SecureRandomSpi.md))`(`seed:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Reseeds this random object with the given seed. |
| --- | --- |

## Public constructors

### SecureRandomSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SecureRandomSpi()
```

Constructor without a parameter.

## Protected constructors

### SecureRandomSpi

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected SecureRandomSpi(params: SecureRandomParameters!)
```

Constructor with a parameter.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [SecureRandomParameters](../java/security/SecureRandomParameters.md)!:the [SecureRandomParameters](../java/security/SecureRandomParameters.md) object. This argument can be`null`. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`params`is unrecognizable or unsupported by this`SecureRandom` |

## Public methods

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a Human-readable string representation of this`SecureRandom`.

| Return ||
|----------------------------------------------------------------------------------|---------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the string representation |

## Protected methods

### engineGenerateSeed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGenerateSeed(numBytes: Int): ByteArray!
```

Returns the given number of seed bytes. This call may be used to seed other random number generators.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------|
| `numBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of seed bytes to generate. |

| Return ||
|------------------------------------------------------------------------------------------|-----------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the seed bytes. |

### engineGetParameters

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineGetParameters(): SecureRandomParameters!
```

Returns the effective [SecureRandomParameters](../java/security/SecureRandomParameters.md) for this`SecureRandom`instance.

| Return ||
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SecureRandomParameters](../java/security/SecureRandomParameters.md)! | the effective [SecureRandomParameters](../java/security/SecureRandomParameters.md) parameters, or`null`if no parameters were used. |

### engineNextBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineNextBytes(bytes: ByteArray!): Unit
```

Generates a user-specified number of random bytes.

Some random number generators can only generate a limited amount of random bytes per invocation. If the size of`bytes`is greater than this limit, the implementation should invoke its generation process multiple times to completely fill the buffer before returning from this method.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the array to be filled in with random bytes. |

### engineNextBytes

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineNextBytes(
    bytes: ByteArray!, 
    params: SecureRandomParameters!
): Unit
```

Generates a user-specified number of random bytes with additional parameters.

Some random number generators can only generate a limited amount of random bytes per invocation. If the size of`bytes`is greater than this limit, the implementation should invoke its generation process multiple times to completely fill the buffer before returning from this method.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the array to be filled in with random bytes |
| `params` | [SecureRandomParameters](../java/security/SecureRandomParameters.md)!:additional parameters |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the implementation has not overridden this method |
| `java.lang.IllegalArgumentException` | if`params`is`null`, illegal or unsupported by this`SecureRandom` |

### engineReseed

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineReseed(params: SecureRandomParameters!): Unit
```

Reseeds this random object with entropy input read from its entropy source with additional parameters.

If this method is called by [SecureRandom.reseed()](../java/security/SecureRandom.md)),`params`will be`null`.

Do not override this method if the implementation does not support reseeding.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [SecureRandomParameters](../java/security/SecureRandomParameters.md)!:extra parameters, can be`null`. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the implementation has not overridden this method |
| `java.lang.IllegalArgumentException` | if`params`is illegal or unsupported by this`SecureRandom` |

### engineSetSeed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineSetSeed(seed: ByteArray!): Unit
```

Reseeds this random object with the given seed. The seed supplements, rather than replaces, the existing seed. Thus, repeated calls are guaranteed never to reduce randomness.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------|
| `seed` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the seed. |
