# CipherOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CipherOutputStream

```
open class CipherOutputStream : FilterOutputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.io.OutputStream](../java.io/OutputStream.md) |||
| | ↳ | [java.io.FilterOutputStream](../java.io/FilterOutputStream.md) ||
| | | ↳ | [javax.crypto.CipherOutputStream](CipherOutputStream.md) |
| --- | --- | --- | --- |

A CipherOutputStream is composed of an OutputStream and a Cipher so that write() methods first process the data before writing them out to the underlying OutputStream. The cipher must be fully initialized before being used by a CipherOutputStream.

For example, if the cipher is initialized for encryption, the CipherOutputStream will attempt to encrypt data before writing out the encrypted data.

This class adheres strictly to the semantics, especially the failure semantics, of its ancestor classes java.io.OutputStream and java.io.FilterOutputStream. This class has exactly those methods specified in its ancestor classes, and overrides them all. Moreover, this class catches all exceptions that are not thrown by its ancestor classes.

It is crucial for a programmer using this class not to use methods that are not defined or overriden in this class (such as a new method or constructor that is later added to one of the super classes), because the design and implementation of those methods are unlikely to have considered security impact with regard to CipherOutputStream.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CipherOutputStream](CipherOutputStream.md))`(`os:` ` [OutputStream](../java.io/OutputStream.md)!`, `c:` ` [Cipher](Cipher.md)!`)` Constructs a CipherOutputStream from an OutputStream and a Cipher. |

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CipherOutputStream](CipherOutputStream.md))`(`os:` ` [OutputStream](../java.io/OutputStream.md)!`)` Constructs a CipherOutputStream from an OutputStream without specifying a Cipher. |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](CipherOutputStream.md))`()` Closes this output stream and releases any system resources associated with this stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](CipherOutputStream.md))`()` Flushes this output stream by forcing any buffered output bytes that have already been processed by the encapsulated cipher object to be written out. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](CipherOutputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Writes`b.length`bytes from the specified byte array to this output stream. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](CipherOutputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes`len`bytes from the specified byte array starting at offset`off`to this output stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](CipherOutputStream.md))`(`b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes the specified byte to this output stream. |

| Inherited functions ||
|---|---|
| From class [OutputStream](../java.io/OutputStream.md) |--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [OutputStream](../java.io/OutputStream.md)! | [nullOutputStream](../java.io/OutputStream.md))`()` <br /> Returns a new`OutputStream`which discards all bytes. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`write(int)`,`write(byte[])`, and`write(byte[], int, int)`methods do nothing. After the stream has been closed, these methods all throw`IOException`. The`flush()`method does nothing. <br /> | ||

| Inherited properties ||
|---|---|
| From class [FilterOutputStream](../java.io/FilterOutputStream.md) |--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [OutputStream](../java.io/OutputStream.md)! | [out](../java.io/FilterOutputStream.md) <br /> The underlying output stream to be filtered. <br /> | ||

## Public constructors

### CipherOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CipherOutputStream(
    os: OutputStream!, 
    c: Cipher!)
```

Constructs a CipherOutputStream from an OutputStream and a Cipher. 
Note: if the specified output stream or cipher is null, a NullPointerException may be thrown later when they are used.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------|
| `os` | [OutputStream](../java.io/OutputStream.md)!:the OutputStream object |
| `c` | [Cipher](Cipher.md)!:an initialized Cipher object |

## Protected constructors

### CipherOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected CipherOutputStream(os: OutputStream!)
```

Constructs a CipherOutputStream from an OutputStream without specifying a Cipher. This has the effect of constructing a CipherOutputStream using a NullCipher. 
Note: if the specified output stream is null, a NullPointerException may be thrown later when it is used.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------|
| `os` | [OutputStream](../java.io/OutputStream.md)!:the OutputStream object |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes this output stream and releases any system resources associated with this stream.

This method invokes the`doFinal`method of the encapsulated cipher object, which causes any bytes buffered by the encapsulated cipher to be processed. The result is written out by calling the`flush`method of this output stream.

This method resets the encapsulated cipher object to its initial state and calls the`close`method of the underlying output stream.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs. |
| `java.io.IOException` | if an I/O error occurs. |
| --- | --- |

### flush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun flush(): Unit
```

Flushes this output stream by forcing any buffered output bytes that have already been processed by the encapsulated cipher object to be written out.

Any bytes buffered by the encapsulated cipher and waiting to be processed by it will not be written out. For example, if the encapsulated cipher is a block cipher, and the total number of bytes written using one of the`write`methods is less than the cipher's block size, no bytes will be written out.

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |
| `java.io.IOException` | if an I/O error occurs. |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(b: ByteArray!): Unit
```

Writes`b.length`bytes from the specified byte array to this output stream.

The`write`method of`CipherOutputStream`calls the`write`method of three arguments with the three arguments`b`,`0`, and`b.length`.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data. |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |
| `java.lang.NullPointerException` | if`b`is null. |
| `java.io.IOException` | if an I/O error occurs. |
| --- | --- |

**See Also**

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Writes`len`bytes from the specified byte array starting at offset`off`to this output stream.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset in the data. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to write. |
| --- | --- |

| Exceptions ||
|-----------------------|-------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs. In particular, an`IOException`is thrown if the output stream is closed. |
| `java.io.IOException` | if an I/O error occurs. |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(b: Int): Unit
```

Writes the specified byte to this output stream.

| Parameters ||
|-----|---------------------------------------------------------------------------------------|
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the`byte`. |

| Exceptions ||
|-----------------------|-----------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs. In particular, an`IOException`may be thrown if the output stream has been closed. |
| `java.io.IOException` | if an I/O error occurs. |
