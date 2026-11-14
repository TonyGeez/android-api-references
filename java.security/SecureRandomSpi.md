# SecureRandomSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SecureRandomSpi

```
abstract class SecureRandomSpi : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.SecureRandomSpi](https://developer.android.com/reference/kotlin/java/security/SecureRandomSpi#) |

This class defines the*Service Provider Interface* (**SPI** ) for the [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom) class.

All the abstract methods in this class must be implemented by each service provider who wishes to supply the implementation of a cryptographically strong pseudo-random number generator.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SecureRandomSpi](https://developer.android.com/reference/kotlin/java/security/SecureRandomSpi#SecureRandomSpi())`()` Constructor without a parameter. |

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SecureRandomSpi](https://developer.android.com/reference/kotlin/java/security/SecureRandomSpi#SecureRandomSpi(java.security.SecureRandomParameters))`(`params:` ` [SecureRandomParameters](https://developer.android.com/reference/kotlin/java/security/SecureRandomParameters)!`)` Constructor with a parameter. |

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/security/SecureRandomSpi#toString())`()` Returns a Human-readable string representation of this`SecureRandom`. |

| Protected methods ||
|--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [engineGenerateSeed](https://developer.android.com/reference/kotlin/java/security/SecureRandomSpi#engineGenerateSeed(kotlin.Int))`(`numBytes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the given number of seed bytes. |
| open [SecureRandomParameters](https://developer.android.com/reference/kotlin/java/security/SecureRandomParameters)! | [engineGetParameters](https://developer.android.com/reference/kotlin/java/security/SecureRandomSpi#engineGetParameters())`()` Returns the effective [SecureRandomParameters](https://developer.android.com/reference/kotlin/java/security/SecureRandomParameters) for this`SecureRandom`instance. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineNextBytes](https://developer.android.com/reference/kotlin/java/security/SecureRandomSpi#engineNextBytes(kotlin.ByteArray))`(`bytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Generates a user-specified number of random bytes. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineNextBytes](https://developer.android.com/reference/kotlin/java/security/SecureRandomSpi#engineNextBytes(kotlin.ByteArray,%20java.security.SecureRandomParameters))`(`bytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `params:` ` [SecureRandomParameters](https://developer.android.com/reference/kotlin/java/security/SecureRandomParameters)!`)` Generates a user-specified number of random bytes with additional parameters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineReseed](https://developer.android.com/reference/kotlin/java/security/SecureRandomSpi#engineReseed(java.security.SecureRandomParameters))`(`params:` ` [SecureRandomParameters](https://developer.android.com/reference/kotlin/java/security/SecureRandomParameters)!`)` Reseeds this random object with entropy input read from its entropy source with additional parameters. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineSetSeed](https://developer.android.com/reference/kotlin/java/security/SecureRandomSpi#engineSetSeed(kotlin.ByteArray))`(`seed:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Reseeds this random object with the given seed. |
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
| `params` | [SecureRandomParameters](https://developer.android.com/reference/kotlin/java/security/SecureRandomParameters)!:the [SecureRandomParameters](https://developer.android.com/reference/kotlin/java/security/SecureRandomParameters) object. This argument can be`null`. |

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

Returns the effective [SecureRandomParameters](https://developer.android.com/reference/kotlin/java/security/SecureRandomParameters) for this`SecureRandom`instance.

| Return ||
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SecureRandomParameters](https://developer.android.com/reference/kotlin/java/security/SecureRandomParameters)! | the effective [SecureRandomParameters](https://developer.android.com/reference/kotlin/java/security/SecureRandomParameters) parameters, or`null`if no parameters were used. |

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
| `params` | [SecureRandomParameters](https://developer.android.com/reference/kotlin/java/security/SecureRandomParameters)!:additional parameters |

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

If this method is called by [SecureRandom.reseed()](https://developer.android.com/reference/kotlin/java/security/SecureRandom#reseed()),`params`will be`null`.

Do not override this method if the implementation does not support reseeding.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [SecureRandomParameters](https://developer.android.com/reference/kotlin/java/security/SecureRandomParameters)!:extra parameters, can be`null`. |

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
