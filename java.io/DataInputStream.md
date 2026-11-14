# DataInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DataInputStream

```
open class DataInputStream : FilterInputStream, DataInput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [java.io.InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream) |||
| | ↳ | [java.io.FilterInputStream](https://developer.android.com/reference/kotlin/java/io/FilterInputStream) ||
| | | ↳ | [java.io.DataInputStream](https://developer.android.com/reference/kotlin/java/io/DataInputStream#) |

A data input stream lets an application read primitive Java data types from an underlying input stream in a machine-independent way. An application uses a data output stream to write data that can later be read by a data input stream.

DataInputStream is not necessarily safe for multithreaded access. Thread safety is optional and is the responsibility of users of methods in this class.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DataInputStream](https://developer.android.com/reference/kotlin/java/io/DataInputStream#DataInputStream(java.io.InputStream))`(`in:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream)!`)` Creates a DataInputStream that uses the specified underlying InputStream. |

| Public methods ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/DataInputStream#read(kotlin.ByteArray))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Reads some number of bytes from the contained input stream and stores them into the buffer array`b`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/DataInputStream#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads up to`len`bytes of data from the contained input stream into an array of bytes. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [readBoolean](https://developer.android.com/reference/kotlin/java/io/DataInputStream#readBoolean())`()` See the general contract of the`readBoolean`method of`DataInput`. |
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [readByte](https://developer.android.com/reference/kotlin/java/io/DataInputStream#readByte())`()` See the general contract of the`readByte`method of`DataInput`. |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [readChar](https://developer.android.com/reference/kotlin/java/io/DataInputStream#readChar())`()` See the general contract of the`readChar`method of`DataInput`. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [readDouble](https://developer.android.com/reference/kotlin/java/io/DataInputStream#readDouble())`()` See the general contract of the`readDouble`method of`DataInput`. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [readFloat](https://developer.android.com/reference/kotlin/java/io/DataInputStream#readFloat())`()` See the general contract of the`readFloat`method of`DataInput`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readFully](https://developer.android.com/reference/kotlin/java/io/DataInputStream#readFully(kotlin.ByteArray))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` See the general contract of the`readFully`method of`DataInput`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readFully](https://developer.android.com/reference/kotlin/java/io/DataInputStream#readFully(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` See the general contract of the`readFully`method of`DataInput`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readInt](https://developer.android.com/reference/kotlin/java/io/DataInputStream#readInt())`()` See the general contract of the`readInt`method of`DataInput`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [readLine](https://developer.android.com/reference/kotlin/java/io/DataInputStream#readLine())`()` See the general contract of the`readLine`method of`DataInput`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [readLong](https://developer.android.com/reference/kotlin/java/io/DataInputStream#readLong())`()` See the general contract of the`readLong`method of`DataInput`. |
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [readShort](https://developer.android.com/reference/kotlin/java/io/DataInputStream#readShort())`()` See the general contract of the`readShort`method of`DataInput`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [readUTF](https://developer.android.com/reference/kotlin/java/io/DataInputStream#readUTF())`()` See the general contract of the`readUTF`method of`DataInput`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [readUTF](https://developer.android.com/reference/kotlin/java/io/DataInputStream#readUTF(java.io.DataInput))`(`in:` ` [DataInput](https://developer.android.com/reference/kotlin/java/io/DataInput)!`)` Reads from the stream`in`a representation of a Unicode character string encoded in [modified UTF-8](https://developer.android.com/reference/kotlin/java/io/DataInput#modified-utf-8) format; this string of characters is then returned as a`String`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readUnsignedByte](https://developer.android.com/reference/kotlin/java/io/DataInputStream#readUnsignedByte())`()` See the general contract of the`readUnsignedByte`method of`DataInput`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readUnsignedShort](https://developer.android.com/reference/kotlin/java/io/DataInputStream#readUnsignedShort())`()` See the general contract of the`readUnsignedShort`method of`DataInput`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [skipBytes](https://developer.android.com/reference/kotlin/java/io/DataInputStream#skipBytes(kotlin.Int))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` See the general contract of the`skipBytes`method of`DataInput`. |

| Inherited functions ||
|---|---|
| From class [FilterInputStream](https://developer.android.com/reference/kotlin/java/io/FilterInputStream) |------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [available](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#available())`()` <br /> Returns an estimate of the number of bytes that can be read (or skipped over) from this input stream without blocking by the next caller of a method for this input stream. The next caller might be the same thread or another thread. A single read or skip of this many bytes will not block, but may read or skip fewer bytes. This method returns the result of [in](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream).available(). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#close())`()` <br /> Closes this input stream and releases any system resources associated with the stream. This method simply performs`in.close()`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mark](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#mark(kotlin.Int))`(`readlimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Marks the current position in this input stream. A subsequent call to the`reset`method repositions this stream at the last marked position so that subsequent reads re-read the same bytes. The`readlimit`argument tells this input stream to allow that many bytes to be read before the mark position gets invalidated. This method simply performs`in.mark(readlimit)`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [markSupported](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#markSupported())`()` <br /> Tests if this input stream supports the`mark`and`reset`methods. This method simply performs`in.markSupported()`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#read())`()` <br /> Reads the next byte of data from this input stream. The value byte is returned as an`int`in the range`0`to`255`. If no byte is available because the end of the stream has been reached, the value`-1`is returned. This method blocks until input data is available, the end of the stream is detected, or an exception is thrown. This method simply performs`in.read()`and returns the result. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#reset())`()` <br /> Repositions this stream to the position at the time the`mark`method was last called on this input stream. This method simply performs`in.reset()`. Stream marks are intended to be used in situations where you need to read ahead a little to see what's in the stream. Often this is most easily done by invoking some general parser. If the stream is of the type handled by the parse, it just chugs along happily. If the stream is not of that type, the parser should toss an exception when it fails. If this happens within readlimit bytes, it allows the outer code to reset the stream and try another parser. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [skip](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#skip(kotlin.Long))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Skips over and discards`n`bytes of data from the input stream. The`skip`method may, for a variety of reasons, end up skipping over some smaller number of bytes, possibly`0`. The actual number of bytes skipped is returned. This method simply performs`in.skip(n)`. <br /> | ||
| From class [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream) |------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream)! | [nullInputStream](https://developer.android.com/reference/kotlin/java/io/InputStream#nullInputStream())`()` <br /> Returns a new`InputStream`that reads no bytes. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`available()`,`read()`,`read(byte[])`,`read(byte[], int, int)`,`readAllBytes()`,`readNBytes(byte[], int, int)`,`readNBytes(int)`,`skip(long)`,`skipNBytes(long)`, and`transferTo()`methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw`IOException`. The`markSupported()`method returns`false`. The`mark()`method does nothing, and the`reset()`method throws`IOException`. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readAllBytes](https://developer.android.com/reference/kotlin/java/io/InputStream#readAllBytes())`()` <br /> Reads all remaining bytes from the input stream. This method blocks until all remaining bytes have been read and end of stream is detected, or an exception is thrown. This method does not close the input stream. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read all bytes into a byte array. It is not intended for reading input streams with large amounts of data. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readNBytes](https://developer.android.com/reference/kotlin/java/io/InputStream#readNBytes(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Reads the requested number of bytes from the input stream into the given byte array. This method blocks until`len`bytes of input data have been read, end of stream is detected, or an exception is thrown. The number of bytes actually read, possibly zero, is returned. This method does not close the input stream. In the case where end of stream is reached before`len`bytes have been read, then the actual number of bytes read will be returned. When this stream reaches end of stream, further invocations of this method will return zero. If`len`is zero, then no bytes are read and`0`is returned; otherwise, there is an attempt to read up to`len`bytes. The first byte read is stored into element`b[off]`, the next one in to`b[off+1]`, and so on. The number of bytes read is, at most, equal to`len`. Let*k* be the number of bytes actually read; these bytes will be stored in elements`b[off]`through`b[off+`*k* `-1]`, leaving elements`b[off+`*k* `]`through`b[off+len-1]`unaffected. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes of`b`have been updated with data from the input stream. Consequently the input stream and`b`may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readNBytes](https://developer.android.com/reference/kotlin/java/io/InputStream#readNBytes(kotlin.Int))`(`len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Reads up to a specified number of bytes from the input stream. This method blocks until the requested number of bytes has been read, end of stream is detected, or an exception is thrown. This method does not close the input stream. The length of the returned array equals the number of bytes read from the stream. If`len`is zero, then no bytes are read and an empty byte array is returned. Otherwise, up to`len`bytes are read from the stream. Fewer than`len`bytes may be read if end of stream is encountered. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read the specified number of bytes into a byte array. The total amount of memory allocated by this method is proportional to the number of bytes read from the stream which is bounded by`len`. Therefore, the method may be safely called with very large values of`len`provided sufficient memory is available. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [skipNBytes](https://developer.android.com/reference/kotlin/java/io/InputStream#skipNBytes(kotlin.Long))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Skips over and discards exactly`n`bytes of data from this input stream. If`n`is zero, then no bytes are skipped. If`n`is negative, then no bytes are skipped. Subclasses may handle the negative value differently. This method blocks until the requested number of bytes has been skipped, end of file is reached, or an exception is thrown. If end of stream is reached before the stream is at the desired position, then an`EOFException`is thrown. If an I/O error occurs, then the input stream may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [transferTo](https://developer.android.com/reference/kotlin/java/io/InputStream#transferTo(java.io.OutputStream))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream)!`)` <br /> Reads all bytes from this input stream and writes the bytes to the given output stream in the order that they are read. On return, this input stream will be at end of stream. This method does not close either stream. This method may block indefinitely reading from the input stream, or writing to the output stream. The behavior for the case where the input and/or output stream is*asynchronously closed*, or the thread interrupted during the transfer, is highly input and output stream specific, and therefore not specified. If an I/O error occurs reading from the input stream or writing to the output stream, then it may do so after some bytes have been read or written. Consequently the input stream may not be at end of stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs. <br /> | ||

| Inherited properties ||
|---|---|
| From class [FilterInputStream](https://developer.android.com/reference/kotlin/java/io/FilterInputStream) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------| | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream)! | [in](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream) <br /> The input stream to be filtered. <br /> | ||

## Public constructors

### DataInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DataInputStream(in: InputStream!)
```

Creates a DataInputStream that uses the specified underlying InputStream.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------|
| `in` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream)!:the specified input stream |

## Public methods

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun read(b: ByteArray!): Int
```

Reads some number of bytes from the contained input stream and stores them into the buffer array`b`. The number of bytes actually read is returned as an integer. This method blocks until input data is available, end of file is detected, or an exception is thrown.

If`b`is null, a`NullPointerException`is thrown. If the length of`b`is zero, then no bytes are read and`0`is returned; otherwise, there is an attempt to read at least one byte. If no byte is available because the stream is at end of file, the value`-1`is returned; otherwise, at least one byte is read and stored into`b`.

The first byte read is stored into element`b[0]`, the next one into`b[1]`, and so on. The number of bytes read is, at most, equal to the length of`b`. Let`k`be the number of bytes actually read; these bytes will be stored in elements`b[0]`through`b[k-1]`, leaving elements`b[k]`through`b[b.length-1]`unaffected.

The`read(b)`method has the same effect as: 

```kotlin
read(b, 0, b.length)
  
```

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer into which the data is read. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the total number of bytes read into the buffer, or`-1`if there is no more data because the end of the stream has been reached. |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | If the first byte cannot be read for any reason other than the end of the file, if the input stream has been closed, or if some other I/O error occurs. |
| `java.lang.NullPointerException` | if`b`is`null`. |
| `java.io.IOException` | if the first byte cannot be read for any reason other than end of file, the stream has been closed and the underlying input stream does not support reading after close, or another I/O error occurs. |

**See Also**

- [java.io.FilterInputStream#in](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream)
- [java.io.InputStream#read(byte[], int, int)](https://developer.android.com/reference/kotlin/java/io/InputStream#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)) 

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun read(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Int
```

Reads up to`len`bytes of data from the contained input stream into an array of bytes. An attempt is made to read as many as`len`bytes, but a smaller number may be read, possibly zero. The number of bytes actually read is returned as an integer.

This method blocks until input data is available, end of file is detected, or an exception is thrown.

If`len`is zero, then no bytes are read and`0`is returned; otherwise, there is an attempt to read at least one byte. If no byte is available because the stream is at end of file, the value`-1`is returned; otherwise, at least one byte is read and stored into`b`.

The first byte read is stored into element`b[off]`, the next one into`b[off+1]`, and so on. The number of bytes read is, at most, equal to`len`. Let*k* be the number of bytes actually read; these bytes will be stored in elements`b[off]`through`b[off+`*k* `-1]`, leaving elements`b[off+`*k* `]`through`b[off+len-1]`unaffected.

In every case, elements`b[0]`through`b[off]`and elements`b[off+len]`through`b[b.length-1]`are unaffected.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer into which the data is read. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset in the destination array`b` |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of bytes read. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the total number of bytes read into the buffer, or`-1`if there is no more data because the end of the stream has been reached. |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | If the first byte cannot be read for any reason other than end of file, or if the input stream has been closed, or if some other I/O error occurs. |
| `java.lang.NullPointerException` | If`b`is`null`. |
| `java.lang.IndexOutOfBoundsException` | If`off`is negative,`len`is negative, or`len`is greater than`b.length - off` |
| `java.lang.NullPointerException` | If`b`is`null`. |
| `java.lang.IndexOutOfBoundsException` | If`off`is negative,`len`is negative, or`len`is greater than`b.length - off` |
| `java.io.IOException` | if the first byte cannot be read for any reason other than end of file, the stream has been closed and the underlying input stream does not support reading after close, or another I/O error occurs. |

**See Also**

- [java.io.FilterInputStream#in](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream)
- [java.io.InputStream#read(byte[], int, int)](https://developer.android.com/reference/kotlin/java/io/InputStream#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)) 

### readBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readBoolean(): Boolean
```

See the general contract of the`readBoolean`method of`DataInput`.

Bytes for this operation are read from the contained input stream.

| Return ||
|------------------------------------------------------------------------------------|-------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the`boolean`value read. |

| Exceptions ||
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| `java.io.EOFException` | if this input stream has reached the end. |
| `java.io.IOException` | the stream has been closed and the contained input stream does not support reading after close, or another I/O error occurs. |

**See Also**

- [java.io.FilterInputStream#in](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream) 

### readByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readByte(): Byte
```

See the general contract of the`readByte`method of`DataInput`.

Bytes for this operation are read from the contained input stream.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | the next byte of this input stream as a signed 8-bit`byte`. |

| Exceptions ||
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| `java.io.EOFException` | if this input stream has reached the end. |
| `java.io.IOException` | the stream has been closed and the contained input stream does not support reading after close, or another I/O error occurs. |

**See Also**

- [java.io.FilterInputStream#in](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream) 

### readChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readChar(): Char
```

See the general contract of the`readChar`method of`DataInput`.

Bytes for this operation are read from the contained input stream.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the next two bytes of this input stream, interpreted as a`char`. |

| Exceptions ||
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| `java.io.EOFException` | if this input stream reaches the end before reading two bytes. |
| `java.io.IOException` | the stream has been closed and the contained input stream does not support reading after close, or another I/O error occurs. |

**See Also**

- [java.io.FilterInputStream#in](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream) 

### readDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readDouble(): Double
```

See the general contract of the`readDouble`method of`DataInput`.

Bytes for this operation are read from the contained input stream.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the next eight bytes of this input stream, interpreted as a`double`. |

| Exceptions ||
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| `java.io.EOFException` | if this input stream reaches the end before reading eight bytes. |
| `java.io.IOException` | the stream has been closed and the contained input stream does not support reading after close, or another I/O error occurs. |

**See Also**

- [java.io.DataInputStream#readLong()](https://developer.android.com/reference/kotlin/java/io/DataInputStream#readLong())
- [java.lang.Double#longBitsToDouble(long)](https://developer.android.com/reference/kotlin/java/lang/Double.html#longBitsToDouble(kotlin.Long)) 

### readFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readFloat(): Float
```

See the general contract of the`readFloat`method of`DataInput`.

Bytes for this operation are read from the contained input stream.

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the next four bytes of this input stream, interpreted as a`float`. |

| Exceptions ||
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| `java.io.EOFException` | if this input stream reaches the end before reading four bytes. |
| `java.io.IOException` | the stream has been closed and the contained input stream does not support reading after close, or another I/O error occurs. |

**See Also**

- [java.io.DataInputStream#readInt()](https://developer.android.com/reference/kotlin/java/io/DataInputStream#readInt())
- [java.lang.Float#intBitsToFloat(int)](https://developer.android.com/reference/kotlin/java/lang/Float.html#intBitsToFloat(kotlin.Int)) 

### readFully

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readFully(b: ByteArray!): Unit
```

See the general contract of the`readFully`method of`DataInput`.

Bytes for this operation are read from the contained input stream.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer into which the data is read. |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`b`is`null`. |
| `java.io.EOFException` | if this input stream reaches the end before reading all the bytes. |
| `java.io.IOException` | the stream has been closed and the contained input stream does not support reading after close, or another I/O error occurs. |

**See Also**

- [java.io.FilterInputStream#in](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream) 

### readFully

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readFully(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

See the general contract of the`readFully`method of`DataInput`.

Bytes for this operation are read from the contained input stream.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer into which the data is read. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset in the data array`b`. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to read. |

| Exceptions ||
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`b`is`null`. |
| `java.lang.IndexOutOfBoundsException` | if`off`is negative,`len`is negative, or`len`is greater than`b.length - off`. |
| `java.io.EOFException` | if this stream reaches the end before reading all the bytes. |
| `java.io.IOException` | if an I/O error occurs. |
| `java.lang.NullPointerException` | if`b`is`null`. |
| `java.lang.IndexOutOfBoundsException` | if`off`is negative,`len`is negative, or`len`is greater than`b.length - off`. |
| `java.io.EOFException` | if this input stream reaches the end before reading all the bytes. |
| `java.io.IOException` | the stream has been closed and the contained input stream does not support reading after close, or another I/O error occurs. |

**See Also**

- [java.io.FilterInputStream#in](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream) 

### readInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readInt(): Int
```

See the general contract of the`readInt`method of`DataInput`.

Bytes for this operation are read from the contained input stream.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the next four bytes of this input stream, interpreted as an`int`. |

| Exceptions ||
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| `java.io.EOFException` | if this input stream reaches the end before reading four bytes. |
| `java.io.IOException` | the stream has been closed and the contained input stream does not support reading after close, or another I/O error occurs. |

**See Also**

- [java.io.FilterInputStream#in](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream) 

### readLine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readLine(): String!
```

**Deprecated:** *This method does not properly convert bytes to characters. As of JDK 1.1, the preferred way to read lines of text is via the`BufferedReader.readLine()`method. Programs that use the`DataInputStream`class to read lines can be converted to use the`BufferedReader`class by replacing code of the form:* 

```kotlin
DataInputStream d = new DataInputStream(in);
  
```
*with:
```kotlin
BufferedReader d
= new BufferedReader(new InputStreamReader(in));

```*

<br />

See the general contract of the`readLine`method of`DataInput`.

Bytes for this operation are read from the contained input stream.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the next line of text from this input stream. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- [java.io.BufferedReader#readLine()](https://developer.android.com/reference/kotlin/java/io/BufferedReader#readLine())
- [java.io.FilterInputStream#in](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream) 

### readLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readLong(): Long
```

See the general contract of the`readLong`method of`DataInput`.

Bytes for this operation are read from the contained input stream.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the next eight bytes of this input stream, interpreted as a`long`. |

| Exceptions ||
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| `java.io.EOFException` | if this input stream reaches the end before reading eight bytes. |
| `java.io.IOException` | the stream has been closed and the contained input stream does not support reading after close, or another I/O error occurs. |

**See Also**

- [java.io.FilterInputStream#in](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream) 

### readShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readShort(): Short
```

See the general contract of the`readShort`method of`DataInput`.

Bytes for this operation are read from the contained input stream.

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the next two bytes of this input stream, interpreted as a signed 16-bit number. |

| Exceptions ||
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| `java.io.EOFException` | if this input stream reaches the end before reading two bytes. |
| `java.io.IOException` | the stream has been closed and the contained input stream does not support reading after close, or another I/O error occurs. |

**See Also**

- [java.io.FilterInputStream#in](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream) 

### readUTF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readUTF(): String!
```

See the general contract of the`readUTF`method of`DataInput`.

Bytes for this operation are read from the contained input stream.

| Return ||
|-----------------------------------------------------------------------------------|-------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a Unicode string. |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| `java.io.EOFException` | if this input stream reaches the end before reading all the bytes. |
| `java.io.IOException` | the stream has been closed and the contained input stream does not support reading after close, or another I/O error occurs. |
| `java.io.UTFDataFormatException` | if the bytes do not represent a valid modified UTF-8 encoding of a string. |

**See Also**

- [java.io.DataInputStream#readUTF(java.io.DataInput)](https://developer.android.com/reference/kotlin/java/io/DataInputStream#readUTF(java.io.DataInput)) 

### readUTF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun readUTF(in: DataInput!): String!
```

Reads from the stream`in`a representation of a Unicode character string encoded in [modified UTF-8](https://developer.android.com/reference/kotlin/java/io/DataInput#modified-utf-8) format; this string of characters is then returned as a`String`. The details of the modified UTF-8 representation are exactly the same as for the`readUTF`method of`DataInput`.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------|
| `in` | [DataInput](https://developer.android.com/reference/kotlin/java/io/DataInput)!:a data input stream. |

| Return ||
|-----------------------------------------------------------------------------------|-------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a Unicode string. |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| `java.io.EOFException` | if the input stream reaches the end before all the bytes. |
| `java.io.IOException` | the stream has been closed and the contained input stream does not support reading after close, or another I/O error occurs. |
| `java.io.UTFDataFormatException` | if the bytes do not represent a valid modified UTF-8 encoding of a Unicode string. |

**See Also**

- [java.io.DataInputStream#readUnsignedShort()](https://developer.android.com/reference/kotlin/java/io/DataInputStream#readUnsignedShort()) 

### readUnsignedByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readUnsignedByte(): Int
```

See the general contract of the`readUnsignedByte`method of`DataInput`.

Bytes for this operation are read from the contained input stream.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the next byte of this input stream, interpreted as an unsigned 8-bit number. |

| Exceptions ||
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| `java.io.EOFException` | if this input stream has reached the end. |
| `java.io.IOException` | the stream has been closed and the contained input stream does not support reading after close, or another I/O error occurs. |

**See Also**

- [java.io.FilterInputStream#in](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream) 

### readUnsignedShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readUnsignedShort(): Int
```

See the general contract of the`readUnsignedShort`method of`DataInput`.

Bytes for this operation are read from the contained input stream.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the next two bytes of this input stream, interpreted as an unsigned 16-bit integer. |

| Exceptions ||
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| `java.io.EOFException` | if this input stream reaches the end before reading two bytes. |
| `java.io.IOException` | the stream has been closed and the contained input stream does not support reading after close, or another I/O error occurs. |

**See Also**

- [java.io.FilterInputStream#in](https://developer.android.com/reference/kotlin/java/io/FilterInputStream#in:java.io.InputStream) 

### skipBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun skipBytes(n: Int): Int
```

See the general contract of the`skipBytes`method of`DataInput`.

Bytes for this operation are read from the contained input stream.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to be skipped. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the actual number of bytes skipped. |

| Exceptions ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if the contained input stream does not support seek, or the stream has been closed and the contained input stream does not support reading after close, or another I/O error occurs. |
