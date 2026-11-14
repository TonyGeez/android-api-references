# MessageDigest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MessageDigest

```
abstract class MessageDigest : MessageDigestSpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.security.MessageDigestSpi](MessageDigestSpi.md) ||
| | ↳ | [java.security.MessageDigest](MessageDigest.md) |

This MessageDigest class provides applications the functionality of a message digest algorithm, such as SHA-1 or SHA-256. Message digests are secure one-way hash functions that take arbitrary-sized data and output a fixed-length hash value.

A MessageDigest object starts out initialized. The data is processed through it using the [update](MessageDigest.md))methods. At any point [reset](MessageDigest.md))can be called to reset the digest. Once all the data to be updated has been updated, one of the [digest](MessageDigest.md))methods should be called to complete the hash computation.

The`digest`method can be called once for a given number of updates. After`digest`has been called, the MessageDigest object is reset to its initialized state.

Implementations are free to implement the Cloneable interface. Client applications can test cloneability by attempting cloning and catching the CloneNotSupportedException: 

```kotlin
<code>MessageDigest md = MessageDigest.getInstance("SHA-256");
 
  try {
      md.update(toChapter1);
      MessageDigest tc1 = md.clone();
      byte[] toChapter1Digest = tc1.digest();
      md.update(toChapter2);
      ...etc.
  } catch (CloneNotSupportedException cnse) {
      throw new DigestException("couldn't make digest of partial content");
  }
  </code>
```

Note that if a given implementation is not cloneable, it is still possible to compute intermediate digests by instantiating several instances, if the number of digests is known in advance.

Note that this class is abstract and extends from`MessageDigestSpi`for historical reasons. Application developers should only take notice of the methods defined in this`MessageDigest`class; all the methods in the superclass are intended for cryptographic service providers who wish to supply their own implementations of message digest algorithms.

Android provides the following`MessageDigest`algorithms:

| Algorithm | Supported API Levels |
|-----------|----------------------|
| MD5 | 1+ |
| SHA-1 | 1+ |
| SHA-224 | 1-8,22+ |
| --- | --- |
| SHA-256 | 1+ |
| SHA-384 | 1+ |
| SHA-512 | 1+ |
| --- | --- |

These algorithms are described in the [MessageDigest section](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#messagedigest-algorithms) of the Java Cryptography Architecture Standard Algorithm Name Documentation.

## Summary

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MessageDigest](MessageDigest.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Creates a message digest with the specified algorithm name. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](MessageDigest.md))`()` Returns a clone if the implementation is cloneable. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [digest](MessageDigest.md))`()` Completes the hash computation by performing final operations such as padding. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [digest](MessageDigest.md))`(`input:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Performs a final update on the digest using the specified array of bytes, then completes the digest computation. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [digest](MessageDigest.md))`(`buf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Completes the hash computation by performing final operations such as padding. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getAlgorithm](MessageDigest.md))`()` Returns a string that identifies the algorithm, independent of implementation details. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDigestLength](MessageDigest.md))`()` Returns the length of the digest in bytes, or 0 if this operation is not supported by the provider and the implementation is not cloneable. |
| --- | --- |
| openstatic [MessageDigest](MessageDigest.md) | [getInstance](MessageDigest.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns a MessageDigest object that implements the specified digest algorithm. |
| openstatic [MessageDigest](MessageDigest.md) | [getInstance](MessageDigest.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns a MessageDigest object that implements the specified digest algorithm. |
| openstatic [MessageDigest](MessageDigest.md) | [getInstance](MessageDigest.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `provider:` ` [Provider](Provider.md)`)` Returns a MessageDigest object that implements the specified digest algorithm. |
| --- | --- |
| [Provider](Provider.md) | [getProvider](MessageDigest.md))`()` Returns the provider of this message digest object. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEqual](MessageDigest.md))`(`digesta:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`, `digestb:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`)` Compares two digests for equality. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](MessageDigest.md))`()` Resets the digest for further use. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](MessageDigest.md))`()` Returns a string representation of this message digest object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](MessageDigest.md))`(`input:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Updates the digest using the specified byte. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](MessageDigest.md))`(`input:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Updates the digest using the specified array of bytes. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](MessageDigest.md))`(`input:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Updates the digest using the specified array of bytes, starting at the specified offset. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](MessageDigest.md))`(`input:` ` [ByteBuffer](../java.nio/ByteBuffer.md)`)` Update the digest using the specified ByteBuffer. |

| Inherited functions ||
|---|---|
| From class [MessageDigestSpi](MessageDigestSpi.md) |------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [engineDigest](MessageDigestSpi.md))`()` <br /> Completes the hash computation by performing final operations such as padding. Once`engineDigest`has been called, the engine should be reset (see [engineReset](MessageDigestSpi.md))). Resetting is the responsibility of the engine implementor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [engineDigest](MessageDigestSpi.md))`(`buf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Completes the hash computation by performing final operations such as padding. Once`engineDigest`has been called, the engine should be reset (see [engineReset](MessageDigestSpi.md))). Resetting is the responsibility of the engine implementor. This method should be abstract, but we leave it concrete for binary compatibility. Knowledgeable providers should override this method. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [engineGetDigestLength](MessageDigestSpi.md))`()` <br /> Returns the digest length in bytes. This concrete method has been added to this previously-defined abstract class. (For backwards compatibility, it cannot be abstract.) The default behavior is to return 0. This method may be overridden by a provider to return the digest length. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineReset](MessageDigestSpi.md))`()` <br /> Resets the digest for further use. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineUpdate](MessageDigestSpi.md))`(`input:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` <br /> Updates the digest using the specified byte. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineUpdate](MessageDigestSpi.md))`(`input:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Updates the digest using the specified array of bytes, starting at the specified offset. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineUpdate](MessageDigestSpi.md))`(`input:` ` [ByteBuffer](../java.nio/ByteBuffer.md)!`)` <br /> Update the digest using the specified ByteBuffer. The digest is updated using the`input.remaining()`bytes starting at`input.position()`. Upon return, the buffer's position will be equal to its limit; its limit will not have changed. <br /> | ||

## Protected constructors

### MessageDigest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected MessageDigest(algorithm: String)
```

Creates a message digest with the specified algorithm name.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the standard name of the digest algorithm. See the MessageDigest section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#messagedigest-algorithms) for information about standard algorithm names. |

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Returns a clone if the implementation is cloneable.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a clone if the implementation is cloneable. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |
| `java.lang.CloneNotSupportedException` | if this is called on an implementation that does not support`Cloneable`. |

### digest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun digest(): ByteArray
```

Completes the hash computation by performing final operations such as padding. The digest is reset after this call is made.

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | the array of bytes for the resulting hash value. |

### digest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun digest(input: ByteArray): ByteArray
```

Performs a final update on the digest using the specified array of bytes, then completes the digest computation. That is, this method first calls [update(input)](MessageDigest.md)), passing the*input* array to the`update`method, then calls [digest()](MessageDigest.md)).

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `input` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the input to be updated before the digest is completed. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | the array of bytes for the resulting hash value. |

### digest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun digest(
    buf: ByteArray, 
    offset: Int, 
    len: Int
): Int
```

Completes the hash computation by performing final operations such as padding. The digest is reset after this call is made.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `buf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):output buffer for the computed digest |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):offset into the output buffer to begin storing the digest |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of bytes within buf allotted for the digest |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bytes placed into`buf` |

| Exceptions ||
|---------------------------------|---------------------|
| `java.security.DigestException` | if an error occurs. |

### getAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAlgorithm(): String
```

Returns a string that identifies the algorithm, independent of implementation details. The name should be a standard Java Security name (such as "SHA-256"). See the MessageDigest section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#messagedigest-algorithms) for information about standard algorithm names.

| Return ||
|----------------------------------------------------------------------------------|---------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the name of the algorithm |

### getDigestLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDigestLength(): Int
```

Returns the length of the digest in bytes, or 0 if this operation is not supported by the provider and the implementation is not cloneable.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the digest length in bytes, or 0 if this operation is not supported by the provider and the implementation is not cloneable. |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(algorithm: String): MessageDigest
```

Returns a MessageDigest object that implements the specified digest algorithm.

This method traverses the list of registered security Providers, starting with the most preferred Provider. A new MessageDigest object encapsulating the MessageDigestSpi implementation from the first Provider that supports the specified algorithm is returned.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](Security.md))method.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the algorithm requested. See the MessageDigest section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#messagedigest-algorithms) for information about standard algorithm names. |

| Return ||
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [MessageDigest](MessageDigest.md) | a`MessageDigest`object that implements the specified algorithm |

| Exceptions ||
|------------------------------------------|---------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if no`Provider`supports a`MessageDigestSpi`implementation for the specified algorithm |
| `java.lang.NullPointerException` | if`algorithm`is`null` |

**See Also**

- [java.security.Provider](Provider.md) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    algorithm: String, 
    provider: String
): MessageDigest
```

Returns a MessageDigest object that implements the specified digest algorithm.

A new MessageDigest object encapsulating the MessageDigestSpi implementation from the specified provider is returned. The specified provider must be registered in the security provider list.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](Security.md))method.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the algorithm requested. See the MessageDigest section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#messagedigest-algorithms) for information about standard algorithm names. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the provider. |

| Return ||
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [MessageDigest](MessageDigest.md) | a`MessageDigest`object that implements the specified algorithm |

| Exceptions ||
|------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the provider name is`null`or empty |
| `java.security.NoSuchAlgorithmException` | if a`MessageDigestSpi`implementation for the specified algorithm is not available from the specified provider |
| `java.security.NoSuchProviderException` | if the specified provider is not registered in the security provider list |
| --- | --- |
| `java.lang.NullPointerException` | if`algorithm`is`null` |

**See Also**

- [java.security.Provider](Provider.md) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    algorithm: String, 
    provider: Provider
): MessageDigest
```

Returns a MessageDigest object that implements the specified digest algorithm.

A new MessageDigest object encapsulating the MessageDigestSpi implementation from the specified Provider object is returned. Note that the specified Provider object does not have to be registered in the provider list.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the algorithm requested. See the MessageDigest section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#messagedigest-algorithms) for information about standard algorithm names. |
| `provider` | [Provider](Provider.md):the provider. |

| Return ||
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [MessageDigest](MessageDigest.md) | a`MessageDigest`object that implements the specified algorithm |

| Exceptions ||
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the specified provider is`null` |
| `java.security.NoSuchAlgorithmException` | if a`MessageDigestSpi`implementation for the specified algorithm is not available from the specified`Provider`object |
| `java.lang.NullPointerException` | if`algorithm`is`null` |
| --- | --- |

**See Also**

- [java.security.Provider](Provider.md) 

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProvider(): Provider
```

Returns the provider of this message digest object.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------|
| [Provider](Provider.md) | the provider of this message digest object |

### isEqual

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isEqual(
    digesta: ByteArray?, 
    digestb: ByteArray?
): Boolean
```

Compares two digests for equality. Two digests are equal if they have the same length and all bytes at corresponding positions are equal.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------|
| `digesta` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:one of the digests to compare. |
| `digestb` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:the other digest to compare. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the digests are equal, false otherwise. |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Resets the digest for further use. 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of this message digest object.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun update(input: Byte): Unit
```

Updates the digest using the specified byte.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `input` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the byte with which to update the digest. |

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun update(input: ByteArray): Unit
```

Updates the digest using the specified array of bytes.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------|
| `input` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the array of bytes. |

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun update(
    input: ByteArray, 
    offset: Int, 
    len: Int
): Unit
```

Updates the digest using the specified array of bytes, starting at the specified offset.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------|
| `input` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the array of bytes. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset to start from in the array of bytes. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to use, starting at`offset`. |
| --- | --- |

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun update(input: ByteBuffer): Unit
```

Update the digest using the specified ByteBuffer. The digest is updated using the`input.remaining()`bytes starting at`input.position()`. Upon return, the buffer's position will be equal to its limit; its limit will not have changed.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------|
| `input` | [ByteBuffer](../java.nio/ByteBuffer.md):the ByteBuffer |
