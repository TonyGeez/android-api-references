# CheckedInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CheckedInputStream

```
open class CheckedInputStream : FilterInputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.io.InputStream](../java.io/InputStream.md) |||
| | ↳ | [java.io.FilterInputStream](../java.io/FilterInputStream.md) ||
| | | ↳ | [java.util.zip.CheckedInputStream](CheckedInputStream.md) |
| --- | --- | --- | --- |

An input stream that also maintains a checksum of the data being read. The checksum can then be used to verify the integrity of the input data.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CheckedInputStream](CheckedInputStream.md))`(`in:` ` [InputStream](../java.io/InputStream.md)!`, `cksum:` ` [Checksum](Checksum.md)!`)` Creates an input stream using the specified Checksum. |

| Public methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Checksum](Checksum.md)! | [getChecksum](CheckedInputStream.md))`()` Returns the Checksum for this input stream. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](CheckedInputStream.md))`()` Reads a byte. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](CheckedInputStream.md))`(`buf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads into an array of bytes. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [skip](CheckedInputStream.md))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Skips specified number of bytes of input. |

| Inherited functions ||
|---|---|
| From class [FilterInputStream](../java.io/FilterInputStream.md) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [available](../java.io/FilterInputStream.md))`()` <br /> Returns an estimate of the number of bytes that can be read (or skipped over) from this input stream without blocking by the next caller of a method for this input stream. The next caller might be the same thread or another thread. A single read or skip of this many bytes will not block, but may read or skip fewer bytes. This method returns the result of [in](../java.io/FilterInputStream.md).available(). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java.io/FilterInputStream.md))`()` <br /> Closes this input stream and releases any system resources associated with the stream. This method simply performs`in.close()`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mark](../java.io/FilterInputStream.md))`(`readlimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Marks the current position in this input stream. A subsequent call to the`reset`method repositions this stream at the last marked position so that subsequent reads re-read the same bytes. The`readlimit`argument tells this input stream to allow that many bytes to be read before the mark position gets invalidated. This method simply performs`in.mark(readlimit)`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [markSupported](../java.io/FilterInputStream.md))`()` <br /> Tests if this input stream supports the`mark`and`reset`methods. This method simply performs`in.markSupported()`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](../java.io/FilterInputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Reads up to`b.length`bytes of data from this input stream into an array of bytes. This method blocks until some input is available. This method simply performs the call`read(b, 0, b.length)`and returns the result. It is important that it does*not* do`in.read(b)`instead; certain subclasses of`FilterInputStream`depend on the implementation strategy actually used. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](../java.io/FilterInputStream.md))`()` <br /> Repositions this stream to the position at the time the`mark`method was last called on this input stream. This method simply performs`in.reset()`. Stream marks are intended to be used in situations where you need to read ahead a little to see what's in the stream. Often this is most easily done by invoking some general parser. If the stream is of the type handled by the parse, it just chugs along happily. If the stream is not of that type, the parser should toss an exception when it fails. If this happens within readlimit bytes, it allows the outer code to reset the stream and try another parser. <br /> | ||
| From class [InputStream](../java.io/InputStream.md) |------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InputStream](../java.io/InputStream.md)! | [nullInputStream](../java.io/InputStream.md))`()` <br /> Returns a new`InputStream`that reads no bytes. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`available()`,`read()`,`read(byte[])`,`read(byte[], int, int)`,`readAllBytes()`,`readNBytes(byte[], int, int)`,`readNBytes(int)`,`skip(long)`,`skipNBytes(long)`, and`transferTo()`methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw`IOException`. The`markSupported()`method returns`false`. The`mark()`method does nothing, and the`reset()`method throws`IOException`. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readAllBytes](../java.io/InputStream.md))`()` <br /> Reads all remaining bytes from the input stream. This method blocks until all remaining bytes have been read and end of stream is detected, or an exception is thrown. This method does not close the input stream. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read all bytes into a byte array. It is not intended for reading input streams with large amounts of data. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readNBytes](../java.io/InputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Reads the requested number of bytes from the input stream into the given byte array. This method blocks until`len`bytes of input data have been read, end of stream is detected, or an exception is thrown. The number of bytes actually read, possibly zero, is returned. This method does not close the input stream. In the case where end of stream is reached before`len`bytes have been read, then the actual number of bytes read will be returned. When this stream reaches end of stream, further invocations of this method will return zero. If`len`is zero, then no bytes are read and`0`is returned; otherwise, there is an attempt to read up to`len`bytes. The first byte read is stored into element`b[off]`, the next one in to`b[off+1]`, and so on. The number of bytes read is, at most, equal to`len`. Let*k* be the number of bytes actually read; these bytes will be stored in elements`b[off]`through`b[off+`*k* `-1]`, leaving elements`b[off+`*k* `]`through`b[off+len-1]`unaffected. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes of`b`have been updated with data from the input stream. Consequently the input stream and`b`may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readNBytes](../java.io/InputStream.md))`(`len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Reads up to a specified number of bytes from the input stream. This method blocks until the requested number of bytes has been read, end of stream is detected, or an exception is thrown. This method does not close the input stream. The length of the returned array equals the number of bytes read from the stream. If`len`is zero, then no bytes are read and an empty byte array is returned. Otherwise, up to`len`bytes are read from the stream. Fewer than`len`bytes may be read if end of stream is encountered. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read the specified number of bytes into a byte array. The total amount of memory allocated by this method is proportional to the number of bytes read from the stream which is bounded by`len`. Therefore, the method may be safely called with very large values of`len`provided sufficient memory is available. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [skipNBytes](../java.io/InputStream.md))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Skips over and discards exactly`n`bytes of data from this input stream. If`n`is zero, then no bytes are skipped. If`n`is negative, then no bytes are skipped. Subclasses may handle the negative value differently. This method blocks until the requested number of bytes has been skipped, end of file is reached, or an exception is thrown. If end of stream is reached before the stream is at the desired position, then an`EOFException`is thrown. If an I/O error occurs, then the input stream may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [transferTo](../java.io/InputStream.md))`(`out:` ` [OutputStream](../java.io/OutputStream.md)!`)` <br /> Reads all bytes from this input stream and writes the bytes to the given output stream in the order that they are read. On return, this input stream will be at end of stream. This method does not close either stream. This method may block indefinitely reading from the input stream, or writing to the output stream. The behavior for the case where the input and/or output stream is*asynchronously closed*, or the thread interrupted during the transfer, is highly input and output stream specific, and therefore not specified. If an I/O error occurs reading from the input stream or writing to the output stream, then it may do so after some bytes have been read or written. Consequently the input stream may not be at end of stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs. <br /> | ||

| Inherited properties ||
|---|---|
| From class [FilterInputStream](../java.io/FilterInputStream.md) |------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------| | [InputStream](../java.io/InputStream.md)! | [in](../java.io/FilterInputStream.md) <br /> The input stream to be filtered. <br /> | ||

## Public constructors

### CheckedInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CheckedInputStream(
    in: InputStream!, 
    cksum: Checksum!)
```

Creates an input stream using the specified Checksum.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------|
| `in` | [InputStream](../java.io/InputStream.md)!:the input stream |
| `cksum` | [Checksum](Checksum.md)!:the Checksum |

## Public methods

### getChecksum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChecksum(): Checksum!
```

Returns the Checksum for this input stream.

| Return ||
|------------------------------------------------------------------------------------|--------------------|
| [Checksum](Checksum.md)! | the Checksum value |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(): Int
```

Reads a byte. Will block if no input is available.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the byte read, or -1 if the end of the stream is reached. |

| Exceptions ||
|-----------------------|------------------------------|
| `java.io.IOException` | if an I/O error has occurred |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(
    buf: ByteArray!, 
    off: Int, 
    len: Int
): Int
```

Reads into an array of bytes. If`len`is not zero, the method blocks until some input is available; otherwise, no bytes are read and`0`is returned.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------|
| `b` | the buffer into which the data is read. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset in the destination array`b` |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of bytes read |
| --- | --- |
| `buf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer into which the data is read |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the actual number of bytes read, or -1 if the end of the stream is reached. |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error has occurred |
| `java.lang.NullPointerException` | If`buf`is`null`. |
| `java.lang.IndexOutOfBoundsException` | If`off`is negative,`len`is negative, or`len`is greater than`buf.length - off` |
| --- | --- |

### skip

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun skip(n: Long): Long
```

Skips specified number of bytes of input.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of bytes to skip |

| Return ||
|------------------------------------------------------------------------------|------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the actual number of bytes skipped |

| Exceptions ||
|-----------------------|------------------------------|
| `java.io.IOException` | if an I/O error has occurred |
