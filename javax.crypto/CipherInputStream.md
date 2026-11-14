# CipherInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CipherInputStream

```
open class CipherInputStream : FilterInputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.io.InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) |||
| | ↳ | [java.io.FilterInputStream](https://developer.android.com/reference/kotlin/java/io/FilterInputStream.html#) ||
| | | ↳ | [javax.crypto.CipherInputStream](https://developer.android.com/reference/kotlin/javax/crypto/CipherInputStream#) |
| --- | --- | --- | --- |

A CipherInputStream is composed of an InputStream and a Cipher so that read() methods return data that are read in from the underlying InputStream but have been additionally processed by the Cipher. The Cipher must be fully initialized before being used by a CipherInputStream.

For example, if the Cipher is initialized for decryption, the CipherInputStream will attempt to read in data and decrypt them, before returning the decrypted data.

This class adheres strictly to the semantics, especially the failure semantics, of its ancestor classes java.io.FilterInputStream and java.io.InputStream. This class has exactly those methods specified in its ancestor classes, and overrides them all. Moreover, this class catches all exceptions that are not thrown by its ancestor classes. In particular, the`skip`method skips, and the`available`method counts only data that have been processed by the encapsulated Cipher.

It is crucial for a programmer using this class not to use methods that are not defined or overriden in this class (such as a new method or constructor that is later added to one of the super classes), because the design and implementation of those methods are unlikely to have considered security impact with regard to CipherInputStream.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CipherInputStream](https://developer.android.com/reference/kotlin/javax/crypto/CipherInputStream#CipherInputStream(java.io.InputStream,%20javax.crypto.Cipher))`(`is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `c:` ` [Cipher](https://developer.android.com/reference/kotlin/javax/crypto/Cipher)!`)` Constructs a CipherInputStream from an InputStream and a Cipher. |

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CipherInputStream](https://developer.android.com/reference/kotlin/javax/crypto/CipherInputStream#CipherInputStream(java.io.InputStream))`(`is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` Constructs a CipherInputStream from an InputStream without specifying a Cipher. |

| Public methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [available](https://developer.android.com/reference/kotlin/javax/crypto/CipherInputStream#available())`()` Returns the number of bytes that can be read from this input stream without blocking. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/javax/crypto/CipherInputStream#close())`()` Closes this input stream and releases any system resources associated with the stream. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [markSupported](https://developer.android.com/reference/kotlin/javax/crypto/CipherInputStream#markSupported())`()` Tests if this input stream supports the`mark`and`reset`methods, which it does not. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/javax/crypto/CipherInputStream#read())`()` Reads the next byte of data from this input stream. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/javax/crypto/CipherInputStream#read(kotlin.ByteArray))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Reads up to`b.length`bytes of data from this input stream into an array of bytes. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/javax/crypto/CipherInputStream#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads up to`len`bytes of data from this input stream into an array of bytes. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [skip](https://developer.android.com/reference/kotlin/javax/crypto/CipherInputStream#skip(kotlin.Long))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Skips`n`bytes of input from the bytes that can be read from this input stream without blocking. |

| Inherited functions ||
|---|---|
| From class [FilterInputStream](https://developer.android.com/reference/kotlin/java/io/FilterInputStream.html#) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mark](https://developer.android.com/reference/kotlin/java/io/FilterInputStream.html#mark(kotlin.Int))`(`readlimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Marks the current position in this input stream. A subsequent call to the`reset`method repositions this stream at the last marked position so that subsequent reads re-read the same bytes. The`readlimit`argument tells this input stream to allow that many bytes to be read before the mark position gets invalidated. This method simply performs`in.mark(readlimit)`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/java/io/FilterInputStream.html#reset())`()` <br /> Repositions this stream to the position at the time the`mark`method was last called on this input stream. This method simply performs`in.reset()`. Stream marks are intended to be used in situations where you need to read ahead a little to see what's in the stream. Often this is most easily done by invoking some general parser. If the stream is of the type handled by the parse, it just chugs along happily. If the stream is not of that type, the parser should toss an exception when it fails. If this happens within readlimit bytes, it allows the outer code to reset the stream and try another parser. <br /> | ||
| From class [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) |------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | [nullInputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#nullInputStream())`()` <br /> Returns a new`InputStream`that reads no bytes. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`available()`,`read()`,`read(byte[])`,`read(byte[], int, int)`,`readAllBytes()`,`readNBytes(byte[], int, int)`,`readNBytes(int)`,`skip(long)`,`skipNBytes(long)`, and`transferTo()`methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw`IOException`. The`markSupported()`method returns`false`. The`mark()`method does nothing, and the`reset()`method throws`IOException`. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readAllBytes](https://developer.android.com/reference/kotlin/java/io/InputStream.html#readAllBytes())`()` <br /> Reads all remaining bytes from the input stream. This method blocks until all remaining bytes have been read and end of stream is detected, or an exception is thrown. This method does not close the input stream. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read all bytes into a byte array. It is not intended for reading input streams with large amounts of data. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readNBytes](https://developer.android.com/reference/kotlin/java/io/InputStream.html#readNBytes(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Reads the requested number of bytes from the input stream into the given byte array. This method blocks until`len`bytes of input data have been read, end of stream is detected, or an exception is thrown. The number of bytes actually read, possibly zero, is returned. This method does not close the input stream. In the case where end of stream is reached before`len`bytes have been read, then the actual number of bytes read will be returned. When this stream reaches end of stream, further invocations of this method will return zero. If`len`is zero, then no bytes are read and`0`is returned; otherwise, there is an attempt to read up to`len`bytes. The first byte read is stored into element`b[off]`, the next one in to`b[off+1]`, and so on. The number of bytes read is, at most, equal to`len`. Let*k* be the number of bytes actually read; these bytes will be stored in elements`b[off]`through`b[off+`*k* `-1]`, leaving elements`b[off+`*k* `]`through`b[off+len-1]`unaffected. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes of`b`have been updated with data from the input stream. Consequently the input stream and`b`may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readNBytes](https://developer.android.com/reference/kotlin/java/io/InputStream.html#readNBytes(kotlin.Int))`(`len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Reads up to a specified number of bytes from the input stream. This method blocks until the requested number of bytes has been read, end of stream is detected, or an exception is thrown. This method does not close the input stream. The length of the returned array equals the number of bytes read from the stream. If`len`is zero, then no bytes are read and an empty byte array is returned. Otherwise, up to`len`bytes are read from the stream. Fewer than`len`bytes may be read if end of stream is encountered. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read the specified number of bytes into a byte array. The total amount of memory allocated by this method is proportional to the number of bytes read from the stream which is bounded by`len`. Therefore, the method may be safely called with very large values of`len`provided sufficient memory is available. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [skipNBytes](https://developer.android.com/reference/kotlin/java/io/InputStream.html#skipNBytes(kotlin.Long))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Skips over and discards exactly`n`bytes of data from this input stream. If`n`is zero, then no bytes are skipped. If`n`is negative, then no bytes are skipped. Subclasses may handle the negative value differently. This method blocks until the requested number of bytes has been skipped, end of file is reached, or an exception is thrown. If end of stream is reached before the stream is at the desired position, then an`EOFException`is thrown. If an I/O error occurs, then the input stream may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [transferTo](https://developer.android.com/reference/kotlin/java/io/InputStream.html#transferTo(java.io.OutputStream))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`)` <br /> Reads all bytes from this input stream and writes the bytes to the given output stream in the order that they are read. On return, this input stream will be at end of stream. This method does not close either stream. This method may block indefinitely reading from the input stream, or writing to the output stream. The behavior for the case where the input and/or output stream is*asynchronously closed*, or the thread interrupted during the transfer, is highly input and output stream specific, and therefore not specified. If an I/O error occurs reading from the input stream or writing to the output stream, then it may do so after some bytes have been read or written. Consequently the input stream may not be at end of stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs. <br /> | ||

| Inherited properties ||
|---|---|
| From class [FilterInputStream](https://developer.android.com/reference/kotlin/java/io/FilterInputStream.html#) |------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------| | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | [in](https://developer.android.com/reference/kotlin/java/io/FilterInputStream.html#in:java.io.InputStream) <br /> The input stream to be filtered. <br /> | ||

## Public constructors

### CipherInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CipherInputStream(
    is: InputStream!, 
    c: Cipher!)
```

Constructs a CipherInputStream from an InputStream and a Cipher. 
Note: if the specified input stream or cipher is null, a NullPointerException may be thrown later when they are used.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------|
| `is` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:the to-be-processed input stream |
| `c` | [Cipher](https://developer.android.com/reference/kotlin/javax/crypto/Cipher)!:an initialized Cipher object |

## Protected constructors

### CipherInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected CipherInputStream(is: InputStream!)
```

Constructs a CipherInputStream from an InputStream without specifying a Cipher. This has the effect of constructing a CipherInputStream using a NullCipher. 
Note: if the specified input stream is null, a NullPointerException may be thrown later when it is used.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------|
| `is` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:the to-be-processed input stream |

## Public methods

### available

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun available(): Int
```

Returns the number of bytes that can be read from this input stream without blocking. The`available`method of`InputStream`returns`0`. This method**should**be overridden by subclasses.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bytes that can be read from this input stream without blocking. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |
| `java.io.IOException` | if an I/O error occurs. |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes this input stream and releases any system resources associated with the stream.

The`close`method of`CipherInputStream`calls the`close`method of its underlying input stream.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs. |
| `java.io.IOException` | if an I/O error occurs. |
| --- | --- |

### markSupported

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun markSupported(): Boolean
```

Tests if this input stream supports the`mark`and`reset`methods, which it does not.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `false`, since this class does not support the`mark`and`reset`methods. |

**See Also**

- [java.io.InputStream#mark(int)](https://developer.android.com/reference/kotlin/java/io/InputStream.html#mark(kotlin.Int))
- [java.io.InputStream#reset()](https://developer.android.com/reference/kotlin/java/io/InputStream.html#reset()) 

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(): Int
```

Reads the next byte of data from this input stream. The value byte is returned as an`int`in the range`0`to`255`. If no byte is available because the end of the stream has been reached, the value`-1`is returned. This method blocks until input data is available, the end of the stream is detected, or an exception is thrown.

<br />

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the next byte of data, or`-1`if the end of the stream is reached. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |
| `java.io.IOException` | if an I/O error occurs. |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(b: ByteArray!): Int
```

Reads up to`b.length`bytes of data from this input stream into an array of bytes.

The`read`method of`InputStream`calls the`read`method of three arguments with the arguments`b`,`0`, and`b.length`.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer into which the data is read. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the total number of bytes read into the buffer, or`-1`is there is no more data because the end of the stream has been reached. |

| Exceptions ||
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | If the first byte cannot be read for any reason other than the end of the file, if the input stream has been closed, or if some other I/O error occurs. |
| `java.lang.NullPointerException` | if`b`is`null`. |
| `java.io.IOException` | if an I/O error occurs. |
| --- | --- |

**See Also**

- [java.io.InputStream#read(byte[], int, int)](https://developer.android.com/reference/kotlin/java/io/InputStream.html#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)) 

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Int
```

Reads up to`len`bytes of data from this input stream into an array of bytes. This method blocks until some input is available. If the first argument is`null,`up to`len`bytes are read and discarded.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer into which the data is read. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset in the destination array`buf` |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of bytes read. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the total number of bytes read into the buffer, or`-1`if there is no more data because the end of the stream has been reached. |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | If the first byte cannot be read for any reason other than end of file, or if the input stream has been closed, or if some other I/O error occurs. |
| `java.lang.NullPointerException` | If`b`is`null`. |
| `java.lang.IndexOutOfBoundsException` | If`off`is negative,`len`is negative, or`len`is greater than`b.length - off` |
| --- | --- |
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- [java.io.InputStream#read()](https://developer.android.com/reference/kotlin/java/io/InputStream.html#read()) 

### skip

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun skip(n: Long): Long
```

Skips`n`bytes of input from the bytes that can be read from this input stream without blocking.

Fewer bytes than requested might be skipped. The actual number of bytes skipped is equal to`n`or the result of a call to #available(), whichever is smaller. If`n`is less than zero, no bytes are skipped.

The actual number of bytes skipped is returned.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of bytes to be skipped. |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the actual number of bytes skipped. |

| Exceptions ||
|-----------------------|--------------------------------------|
| `java.io.IOException` | if`in.skip(n)`throws an IOException. |
| `java.io.IOException` | if an I/O error occurs. |
