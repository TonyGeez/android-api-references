# MacSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MacSpi

```
abstract class MacSpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [javax.crypto.MacSpi](https://developer.android.com/reference/kotlin/javax/crypto/MacSpi#) |

This class defines the*Service Provider Interface* (**SPI** ) for the`Mac`class. All the abstract methods in this class must be implemented by each cryptographic service provider who wishes to supply the implementation of a particular MAC algorithm.

Implementations are free to implement the Cloneable interface.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------|---|
| [MacSpi](https://developer.android.com/reference/kotlin/javax/crypto/MacSpi#MacSpi())`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [clone](https://developer.android.com/reference/kotlin/javax/crypto/MacSpi#clone())`()` Returns a clone if the implementation is cloneable. |

| Protected methods ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [engineDoFinal](https://developer.android.com/reference/kotlin/javax/crypto/MacSpi#engineDoFinal())`()` Completes the MAC computation and resets the MAC for further use, maintaining the secret key that the MAC was initialized with. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [engineGetMacLength](https://developer.android.com/reference/kotlin/javax/crypto/MacSpi#engineGetMacLength())`()` Returns the length of the MAC in bytes. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](https://developer.android.com/reference/kotlin/javax/crypto/MacSpi#engineInit(java.security.Key,%20java.security.spec.AlgorithmParameterSpec))`(`key:` ` [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!`, `params:` ` [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)!`)` Initializes the MAC with the given (secret) key and algorithm parameters. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineReset](https://developer.android.com/reference/kotlin/javax/crypto/MacSpi#engineReset())`()` Resets the MAC for further use, maintaining the secret key that the MAC was initialized with. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineUpdate](https://developer.android.com/reference/kotlin/javax/crypto/MacSpi#engineUpdate(kotlin.Byte))`(`input:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Processes the given byte. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineUpdate](https://developer.android.com/reference/kotlin/javax/crypto/MacSpi#engineUpdate(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`input:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Processes the first`len`bytes in`input`, starting at`offset`inclusive. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineUpdate](https://developer.android.com/reference/kotlin/javax/crypto/MacSpi#engineUpdate(java.nio.ByteBuffer))`(`input:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`)` Processes`input.remaining()`bytes in the ByteBuffer`input`, starting at`input.position()`. |

## Public constructors

### MacSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MacSpi()
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

### engineDoFinal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineDoFinal(): ByteArray!
```

Completes the MAC computation and resets the MAC for further use, maintaining the secret key that the MAC was initialized with.

| Return ||
|------------------------------------------------------------------------------------------|-----------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the MAC result. |

### engineGetMacLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGetMacLength(): Int
```

Returns the length of the MAC in bytes.

| Return ||
|----------------------------------------------------------------------------|--------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the MAC length in bytes. |

### engineInit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInit(
    key: Key!, 
    params: AlgorithmParameterSpec!
): Unit
```

Initializes the MAC with the given (secret) key and algorithm parameters.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!:the (secret) key. |
| `params` | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)!:the algorithm parameters. |

| Exceptions ||
|----------------------------------------------------|-------------------------------------------------------------------|
| `java.security.InvalidKeyException` | if the given key is inappropriate for initializing this MAC. |
| `java.security.InvalidAlgorithmParameterException` | if the given algorithm parameters are inappropriate for this MAC. |

### engineReset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineReset(): Unit
```

Resets the MAC for further use, maintaining the secret key that the MAC was initialized with. 

### engineUpdate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineUpdate(input: Byte): Unit
```

Processes the given byte.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `input` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the input byte to be processed. |

### engineUpdate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineUpdate(
    input: ByteArray!, 
    offset: Int, 
    len: Int
): Unit
```

Processes the first`len`bytes in`input`, starting at`offset`inclusive.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `input` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the input buffer. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset in`input`where the input starts. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to process. |

### engineUpdate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineUpdate(input: ByteBuffer!): Unit
```

Processes`input.remaining()`bytes in the ByteBuffer`input`, starting at`input.position()`. Upon return, the buffer's position will be equal to its limit; its limit will not have changed.

Subclasses should consider overriding this method if they can process ByteBuffers more efficiently than byte arrays.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------|
| `input` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:the ByteBuffer |
