# MessageDigestSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MessageDigestSpi

```
abstract class MessageDigestSpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.MessageDigestSpi](MessageDigestSpi.md) |

| Known Direct Subclasses [MessageDigest](MessageDigest.md) |---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------| | [MessageDigest](MessageDigest.md) | This MessageDigest class provides applications the functionality of a message digest algorithm, such as SHA-1 or SHA-256. | |
| --- | --- | --- | --- | --- | --- | --- |

This class defines the*Service Provider Interface* (**SPI** ) for the`MessageDigest`class, which provides the functionality of a message digest algorithm, such as MD5 or SHA. Message digests are secure one-way hash functions that take arbitrary-sized data and output a fixed-length hash value.

All the abstract methods in this class must be implemented by a cryptographic service provider who wishes to supply the implementation of a particular message digest algorithm.

Implementations are free to implement the Cloneable interface.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------|---|
| [MessageDigestSpi](MessageDigestSpi.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [clone](MessageDigestSpi.md))`()` Returns a clone if the implementation is cloneable. |

| Protected methods ||
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [engineDigest](MessageDigestSpi.md))`()` Completes the hash computation by performing final operations such as padding. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [engineDigest](MessageDigestSpi.md))`(`buf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Completes the hash computation by performing final operations such as padding. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [engineGetDigestLength](MessageDigestSpi.md))`()` Returns the digest length in bytes. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineReset](MessageDigestSpi.md))`()` Resets the digest for further use. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineUpdate](MessageDigestSpi.md))`(`input:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Updates the digest using the specified byte. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineUpdate](MessageDigestSpi.md))`(`input:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Updates the digest using the specified array of bytes, starting at the specified offset. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineUpdate](MessageDigestSpi.md))`(`input:` ` [ByteBuffer](../java.nio/ByteBuffer.md)!`)` Update the digest using the specified ByteBuffer. |

## Public constructors

### MessageDigestSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MessageDigestSpi()
```

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any!
```

Returns a clone if the implementation is cloneable.

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | a clone if the implementation is cloneable. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |
| `java.lang.CloneNotSupportedException` | if this is called on an implementation that does not support`Cloneable`. |

## Protected methods

### engineDigest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineDigest(): ByteArray!
```

Completes the hash computation by performing final operations such as padding. Once`engineDigest`has been called, the engine should be reset (see [engineReset](MessageDigestSpi.md))). Resetting is the responsibility of the engine implementor.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the array of bytes for the resulting hash value. |

### engineDigest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineDigest(
    buf: ByteArray!, 
    offset: Int, 
    len: Int
): Int
```

Completes the hash computation by performing final operations such as padding. Once`engineDigest`has been called, the engine should be reset (see [engineReset](MessageDigestSpi.md))). Resetting is the responsibility of the engine implementor. This method should be abstract, but we leave it concrete for binary compatibility. Knowledgeable providers should override this method.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `buf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the output buffer in which to store the digest |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):offset to start from in the output buffer |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of bytes within buf allotted for the digest. Both this default implementation and the SUN provider do not return partial digests. The presence of this parameter is solely for consistency in our API's. If the value of this parameter is less than the actual digest length, the method will throw a DigestException. This parameter is ignored if its value is greater than or equal to the actual digest length. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the length of the digest stored in the output buffer. |

| Exceptions ||
|---------------------------------|---------------------|
| `java.security.DigestException` | if an error occurs. |

### engineGetDigestLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineGetDigestLength(): Int
```

Returns the digest length in bytes.

This concrete method has been added to this previously-defined abstract class. (For backwards compatibility, it cannot be abstract.)

The default behavior is to return 0.

This method may be overridden by a provider to return the digest length.

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the digest length in bytes. |

### engineReset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineReset(): Unit
```

Resets the digest for further use. 

### engineUpdate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineUpdate(input: Byte): Unit
```

Updates the digest using the specified byte.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `input` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the byte to use for the update. |

### engineUpdate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineUpdate(
    input: ByteArray!, 
    offset: Int, 
    len: Int
): Unit
```

Updates the digest using the specified array of bytes, starting at the specified offset.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `input` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the array of bytes to use for the update. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset to start from in the array of bytes. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to use, starting at`offset`. |
| --- | --- |

### engineUpdate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineUpdate(input: ByteBuffer!): Unit
```

Update the digest using the specified ByteBuffer. The digest is updated using the`input.remaining()`bytes starting at`input.position()`. Upon return, the buffer's position will be equal to its limit; its limit will not have changed.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------|
| `input` | [ByteBuffer](../java.nio/ByteBuffer.md)!:the ByteBuffer |
