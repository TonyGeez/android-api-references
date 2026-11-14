# Base64InputStream

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Base64InputStream

Kotlin| [Java](Base64InputStream.md) 
| --- | --- |

```
open class Base64InputStream : FilterInputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.io.InputStream](../java.io/InputStream.md) |||
| | ↳ | [java.io.FilterInputStream](../java.io/FilterInputStream.md) ||
| | | ↳ | [android.util.Base64InputStream](Base64InputStream.md) |
| --- | --- | --- | --- |

An InputStream that does Base64 decoding on the data read through it.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Base64InputStream](Base64InputStream.md))`(`in:` ` [InputStream](../java.io/InputStream.md)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` An InputStream that performs Base64 decoding on the data read from the wrapped stream. |

| Public methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [available](Base64InputStream.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](Base64InputStream.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mark](Base64InputStream.md))`(`readlimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [markSupported](Base64InputStream.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](Base64InputStream.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](Base64InputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](Base64InputStream.md))`()` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [skip](Base64InputStream.md))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [InputStream](../java.io/InputStream.md) |------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InputStream](../java.io/InputStream.md)! | [nullInputStream](../java.io/InputStream.md))`()` <br /> Returns a new`InputStream`that reads no bytes. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`available()`,`read()`,`read(byte[])`,`read(byte[], int, int)`,`readAllBytes()`,`readNBytes(byte[], int, int)`,`readNBytes(int)`,`skip(long)`,`skipNBytes(long)`, and`transferTo()`methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw`IOException`. The`markSupported()`method returns`false`. The`mark()`method does nothing, and the`reset()`method throws`IOException`. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readAllBytes](../java.io/InputStream.md))`()` <br /> Reads all remaining bytes from the input stream. This method blocks until all remaining bytes have been read and end of stream is detected, or an exception is thrown. This method does not close the input stream. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read all bytes into a byte array. It is not intended for reading input streams with large amounts of data. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readNBytes](../java.io/InputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Reads the requested number of bytes from the input stream into the given byte array. This method blocks until`len`bytes of input data have been read, end of stream is detected, or an exception is thrown. The number of bytes actually read, possibly zero, is returned. This method does not close the input stream. In the case where end of stream is reached before`len`bytes have been read, then the actual number of bytes read will be returned. When this stream reaches end of stream, further invocations of this method will return zero. If`len`is zero, then no bytes are read and`0`is returned; otherwise, there is an attempt to read up to`len`bytes. The first byte read is stored into element`b[off]`, the next one in to`b[off+1]`, and so on. The number of bytes read is, at most, equal to`len`. Let*k* be the number of bytes actually read; these bytes will be stored in elements`b[off]`through`b[off+`*k* `-1]`, leaving elements`b[off+`*k* `]`through`b[off+len-1]`unaffected. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes of`b`have been updated with data from the input stream. Consequently the input stream and`b`may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readNBytes](../java.io/InputStream.md))`(`len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Reads up to a specified number of bytes from the input stream. This method blocks until the requested number of bytes has been read, end of stream is detected, or an exception is thrown. This method does not close the input stream. The length of the returned array equals the number of bytes read from the stream. If`len`is zero, then no bytes are read and an empty byte array is returned. Otherwise, up to`len`bytes are read from the stream. Fewer than`len`bytes may be read if end of stream is encountered. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read the specified number of bytes into a byte array. The total amount of memory allocated by this method is proportional to the number of bytes read from the stream which is bounded by`len`. Therefore, the method may be safely called with very large values of`len`provided sufficient memory is available. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [skipNBytes](../java.io/InputStream.md))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Skips over and discards exactly`n`bytes of data from this input stream. If`n`is zero, then no bytes are skipped. If`n`is negative, then no bytes are skipped. Subclasses may handle the negative value differently. This method blocks until the requested number of bytes has been skipped, end of file is reached, or an exception is thrown. If end of stream is reached before the stream is at the desired position, then an`EOFException`is thrown. If an I/O error occurs, then the input stream may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [transferTo](../java.io/InputStream.md))`(`out:` ` [OutputStream](../java.io/OutputStream.md)!`)` <br /> Reads all bytes from this input stream and writes the bytes to the given output stream in the order that they are read. On return, this input stream will be at end of stream. This method does not close either stream. This method may block indefinitely reading from the input stream, or writing to the output stream. The behavior for the case where the input and/or output stream is*asynchronously closed*, or the thread interrupted during the transfer, is highly input and output stream specific, and therefore not specified. If an I/O error occurs reading from the input stream or writing to the output stream, then it may do so after some bytes have been read or written. Consequently the input stream may not be at end of stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs. <br /> | ||
| From class [FilterInputStream](../java.io/FilterInputStream.md) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](../java.io/FilterInputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Reads up to`b.length`bytes of data from this input stream into an array of bytes. This method blocks until some input is available. This method simply performs the call`read(b, 0, b.length)`and returns the result. It is important that it does*not* do`in.read(b)`instead; certain subclasses of`FilterInputStream`depend on the implementation strategy actually used. <br /> | ||

| Inherited properties ||
|---|---|
| From class [FilterInputStream](../java.io/FilterInputStream.md) |------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------| | [InputStream](../java.io/InputStream.md)! | [in](../java.io/FilterInputStream.md) <br /> The input stream to be filtered. <br /> | ||

## Public constructors

### Base64InputStream

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Base64InputStream(
    in: InputStream!, 
    flags: Int)
```

An InputStream that performs Base64 decoding on the data read from the wrapped stream.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `in` | [InputStream](../java.io/InputStream.md)!:the InputStream to read the source data from |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):bit flags for controlling the decoder; see the constants in [Base64](Base64.md) |

## Public methods

### available

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun available(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an estimate of the number of bytes that can be read (or skipped over) from this input stream without blocking. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### close

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs. |

### mark

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mark(readlimit: Int): Unit
```

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `readlimit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum limit of bytes that can be read before the mark position becomes invalid. |

### markSupported

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun markSupported(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this stream type supports the`mark`and`reset`method;`false`otherwise. |

### read

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the next byte of data, or`-1`if the end of the stream is reached. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### read

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Int
```

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer into which the data is read. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset in the destination array`b` |
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

### reset

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------------------------------------------|
| `java.io.IOException` | if this stream has not been marked or if the mark has been invalidated. |

### skip

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun skip(n: Long): Long
```

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of bytes to be skipped. |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the actual number of bytes skipped. |

| Exceptions ||
|-----------------------|--------------------------------------|
| `java.io.IOException` | if`in.skip(n)`throws an IOException. |
