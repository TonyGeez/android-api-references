# PipedInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PipedInputStream

```
open class PipedInputStream : InputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.io.InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream) ||
| | ↳ | [java.io.PipedInputStream](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#) |

A piped input stream should be connected to a piped output stream; the piped input stream then provides whatever data bytes are written to the piped output stream. Typically, data is read from a`PipedInputStream`object by one thread and data is written to the corresponding`PipedOutputStream`by some other thread. Attempting to use both objects from a single thread is not recommended, as it may deadlock the thread. The piped input stream contains a buffer, decoupling read operations from write operations, within limits. A pipe is said to be*broken*if a thread that was providing data bytes to the connected piped output stream is no longer alive.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PIPE_SIZE](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#PIPE_SIZE:kotlin.Int) The default size of the pipe's circular input buffer. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PipedInputStream](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#PipedInputStream())`()` Creates a`PipedInputStream`so that it is not yet [connected](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#connect(java.io.PipedOutputStream)). |
| [PipedInputStream](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#PipedInputStream(kotlin.Int))`(`pipeSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a`PipedInputStream`so that it is not yet [connected](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#connect(java.io.PipedOutputStream))and uses the specified pipe size for the pipe's buffer. |
| [PipedInputStream](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#PipedInputStream(java.io.PipedOutputStream))`(`src:` ` [PipedOutputStream](https://developer.android.com/reference/kotlin/java/io/PipedOutputStream)!`)` Creates a`PipedInputStream`so that it is connected to the piped output stream`src`. |
| [PipedInputStream](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#PipedInputStream(java.io.PipedOutputStream,%20kotlin.Int))`(`src:` ` [PipedOutputStream](https://developer.android.com/reference/kotlin/java/io/PipedOutputStream)!`, `pipeSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a`PipedInputStream`so that it is connected to the piped output stream`src`and uses the specified pipe size for the pipe's buffer. |

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [available](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#available())`()` Returns the number of bytes that can be read from this input stream without blocking. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#close())`()` Closes this piped input stream and releases any system resources associated with the stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#connect(java.io.PipedOutputStream))`(`src:` ` [PipedOutputStream](https://developer.android.com/reference/kotlin/java/io/PipedOutputStream)!`)` Causes this piped input stream to be connected to the piped output stream`src`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#read())`()` Reads the next byte of data from this piped input stream. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads up to`len`bytes of data from this piped input stream into an array of bytes. |

| Protected methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [receive](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#receive(kotlin.Int))`(`b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Receives a byte of data. |

| Inherited functions ||
|---|---|
| From class [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream) |------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mark](https://developer.android.com/reference/kotlin/java/io/InputStream#mark(kotlin.Int))`(`readlimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Marks the current position in this input stream. A subsequent call to the`reset`method repositions this stream at the last marked position so that subsequent reads re-read the same bytes. The`readlimit`arguments tells this input stream to allow that many bytes to be read before the mark position gets invalidated. The general contract of`mark`is that, if the method`markSupported`returns`true`, the stream somehow remembers all the bytes read after the call to`mark`and stands ready to supply those same bytes again if and whenever the method`reset`is called. However, the stream is not required to remember any data at all if more than`readlimit`bytes are read from the stream before`reset`is called. Marking a closed stream should not have any effect on the stream. The`mark`method of`InputStream`does nothing. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [markSupported](https://developer.android.com/reference/kotlin/java/io/InputStream#markSupported())`()` <br /> Tests if this input stream supports the`mark`and`reset`methods. Whether or not`mark`and`reset`are supported is an invariant property of a particular input stream instance. The`markSupported`method of`InputStream`returns`false`. <br /> | | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream)! | [nullInputStream](https://developer.android.com/reference/kotlin/java/io/InputStream#nullInputStream())`()` <br /> Returns a new`InputStream`that reads no bytes. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`available()`,`read()`,`read(byte[])`,`read(byte[], int, int)`,`readAllBytes()`,`readNBytes(byte[], int, int)`,`readNBytes(int)`,`skip(long)`,`skipNBytes(long)`, and`transferTo()`methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw`IOException`. The`markSupported()`method returns`false`. The`mark()`method does nothing, and the`reset()`method throws`IOException`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/InputStream#read(kotlin.ByteArray))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Reads some number of bytes from the input stream and stores them into the buffer array`b`. The number of bytes actually read is returned as an integer. This method blocks until input data is available, end of file is detected, or an exception is thrown. If the length of`b`is zero, then no bytes are read and`0`is returned; otherwise, there is an attempt to read at least one byte. If no byte is available because the stream is at the end of the file, the value`-1`is returned; otherwise, at least one byte is read and stored into`b`. The first byte read is stored into element`b[0]`, the next one into`b[1]`, and so on. The number of bytes read is, at most, equal to the length of`b`. Let*k* be the number of bytes actually read; these bytes will be stored in elements`b[0]`through`b[`*k* `-1]`, leaving elements`b[`*k* `]`through`b[b.length-1]`unaffected. The`read(b)`method for class`InputStream`has the same effect as: ```kotlin <code>read(b, 0, b.length) </code> ``` <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readAllBytes](https://developer.android.com/reference/kotlin/java/io/InputStream#readAllBytes())`()` <br /> Reads all remaining bytes from the input stream. This method blocks until all remaining bytes have been read and end of stream is detected, or an exception is thrown. This method does not close the input stream. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read all bytes into a byte array. It is not intended for reading input streams with large amounts of data. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readNBytes](https://developer.android.com/reference/kotlin/java/io/InputStream#readNBytes(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Reads the requested number of bytes from the input stream into the given byte array. This method blocks until`len`bytes of input data have been read, end of stream is detected, or an exception is thrown. The number of bytes actually read, possibly zero, is returned. This method does not close the input stream. In the case where end of stream is reached before`len`bytes have been read, then the actual number of bytes read will be returned. When this stream reaches end of stream, further invocations of this method will return zero. If`len`is zero, then no bytes are read and`0`is returned; otherwise, there is an attempt to read up to`len`bytes. The first byte read is stored into element`b[off]`, the next one in to`b[off+1]`, and so on. The number of bytes read is, at most, equal to`len`. Let*k* be the number of bytes actually read; these bytes will be stored in elements`b[off]`through`b[off+`*k* `-1]`, leaving elements`b[off+`*k* `]`through`b[off+len-1]`unaffected. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes of`b`have been updated with data from the input stream. Consequently the input stream and`b`may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readNBytes](https://developer.android.com/reference/kotlin/java/io/InputStream#readNBytes(kotlin.Int))`(`len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Reads up to a specified number of bytes from the input stream. This method blocks until the requested number of bytes has been read, end of stream is detected, or an exception is thrown. This method does not close the input stream. The length of the returned array equals the number of bytes read from the stream. If`len`is zero, then no bytes are read and an empty byte array is returned. Otherwise, up to`len`bytes are read from the stream. Fewer than`len`bytes may be read if end of stream is encountered. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read the specified number of bytes into a byte array. The total amount of memory allocated by this method is proportional to the number of bytes read from the stream which is bounded by`len`. Therefore, the method may be safely called with very large values of`len`provided sufficient memory is available. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/java/io/InputStream#reset())`()` <br /> Repositions this stream to the position at the time the`mark`method was last called on this input stream. The general contract of`reset`is: - If the method`markSupported`returns`true`, then: - If the method`mark`has not been called since the stream was created, or the number of bytes read from the stream since`mark`was last called is larger than the argument to`mark`at that last call, then an`IOException`might be thrown. - If such an`IOException`is not thrown, then the stream is reset to a state such that all the bytes read since the most recent call to`mark`(or since the start of the file, if`mark`has not been called) will be resupplied to subsequent callers of the`read`method, followed by any bytes that otherwise would have been the next input data as of the time of the call to`reset`. - If the method`markSupported`returns`false`, then: - The call to`reset`may throw an`IOException`. - If an`IOException`is not thrown, then the stream is reset to a fixed state that depends on the particular type of the input stream and how it was created. The bytes that will be supplied to subsequent callers of the`read`method depend on the particular type of the input stream. The method`reset`for class`InputStream`does nothing except throw an`IOException`. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [skip](https://developer.android.com/reference/kotlin/java/io/InputStream#skip(kotlin.Long))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Skips over and discards`n`bytes of data from this input stream. The`skip`method may, for a variety of reasons, end up skipping over some smaller number of bytes, possibly`0`. This may result from any of a number of conditions; reaching end of file before`n`bytes have been skipped is only one possibility. The actual number of bytes skipped is returned. If`n`is negative, the`skip`method for class`InputStream`always returns 0, and no bytes are skipped. Subclasses may handle the negative value differently. The`skip`method implementation of this class creates a byte array and then repeatedly reads into it until`n`bytes have been read or the end of the stream has been reached. Subclasses are encouraged to provide a more efficient implementation of this method. For instance, the implementation may depend on the ability to seek. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [skipNBytes](https://developer.android.com/reference/kotlin/java/io/InputStream#skipNBytes(kotlin.Long))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Skips over and discards exactly`n`bytes of data from this input stream. If`n`is zero, then no bytes are skipped. If`n`is negative, then no bytes are skipped. Subclasses may handle the negative value differently. This method blocks until the requested number of bytes has been skipped, end of file is reached, or an exception is thrown. If end of stream is reached before the stream is at the desired position, then an`EOFException`is thrown. If an I/O error occurs, then the input stream may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [transferTo](https://developer.android.com/reference/kotlin/java/io/InputStream#transferTo(java.io.OutputStream))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream)!`)` <br /> Reads all bytes from this input stream and writes the bytes to the given output stream in the order that they are read. On return, this input stream will be at end of stream. This method does not close either stream. This method may block indefinitely reading from the input stream, or writing to the output stream. The behavior for the case where the input and/or output stream is*asynchronously closed*, or the thread interrupted during the transfer, is highly input and output stream specific, and therefore not specified. If an I/O error occurs reading from the input stream or writing to the output stream, then it may do so after some bytes have been read or written. Consequently the input stream may not be at end of stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [buffer](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#buffer:kotlin.ByteArray) The circular buffer into which incoming data is placed. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [in](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#in:kotlin.Int) The index of the position in the circular buffer at which the next byte of data will be stored when received from the connected piped output stream. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [out](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#out:kotlin.Int) The index of the position in the circular buffer at which the next byte of data will be read by this piped input stream. |
| --- | --- |

## Constants

### PIPE_SIZE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected static val PIPE_SIZE: Int
```

The default size of the pipe's circular input buffer. 

 Value: 1024

## Public constructors

### PipedInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PipedInputStream()
```

Creates a`PipedInputStream`so that it is not yet [connected](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#connect(java.io.PipedOutputStream)). It must be [connected](https://developer.android.com/reference/kotlin/java/io/PipedOutputStream#connect(java.io.PipedInputStream))to a`PipedOutputStream`before being used. 

### PipedInputStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PipedInputStream(pipeSize: Int)
```

Creates a`PipedInputStream`so that it is not yet [connected](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#connect(java.io.PipedOutputStream))and uses the specified pipe size for the pipe's buffer. It must be [connected](https://developer.android.com/reference/kotlin/java/io/PipedOutputStream#connect(java.io.PipedInputStream))to a`PipedOutputStream`before being used.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------|
| `pipeSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the size of the pipe's buffer. |

| Exceptions ||
|--------------------------------------|--------------------|
| `java.lang.IllegalArgumentException` | if`pipeSize <= 0`. |

### PipedInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PipedInputStream(src: PipedOutputStream!)
```

Creates a`PipedInputStream`so that it is connected to the piped output stream`src`. Data bytes written to`src`will then be available as input from this stream.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------|
| `src` | [PipedOutputStream](https://developer.android.com/reference/kotlin/java/io/PipedOutputStream)!:the stream to connect to. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### PipedInputStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PipedInputStream(
    src: PipedOutputStream!, 
    pipeSize: Int)
```

Creates a`PipedInputStream`so that it is connected to the piped output stream`src`and uses the specified pipe size for the pipe's buffer. Data bytes written to`src`will then be available as input from this stream.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------|
| `src` | [PipedOutputStream](https://developer.android.com/reference/kotlin/java/io/PipedOutputStream)!:the stream to connect to. |
| `pipeSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the size of the pipe's buffer. |

| Exceptions ||
|--------------------------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |
| `java.lang.IllegalArgumentException` | if`pipeSize <= 0`. |

## Public methods

### available

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun available(): Int
```

Returns the number of bytes that can be read from this input stream without blocking.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bytes that can be read from this input stream without blocking, or`0`if this input stream has been closed by invoking its #close() method, or if the pipe is [unconnected](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#connect(java.io.PipedOutputStream)), or [`broken`](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#BROKEN). |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |
| `java.io.IOException` | if an I/O error occurs. |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes this piped input stream and releases any system resources associated with the stream.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs. |
| `java.io.IOException` | if an I/O error occurs. |
| --- | --- |

### connect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun connect(src: PipedOutputStream!): Unit
```

Causes this piped input stream to be connected to the piped output stream`src`. If this object is already connected to some other piped output stream, an`IOException`is thrown.

If`src`is an unconnected piped output stream and`snk`is an unconnected piped input stream, they may be connected by either the call: 

```kotlin
<code>snk.connect(src)</code>
```

or the call: 

```kotlin
<code>src.connect(snk)</code>
```

The two calls have the same effect.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [PipedOutputStream](https://developer.android.com/reference/kotlin/java/io/PipedOutputStream)!:The piped output stream to connect to. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(): Int
```

Reads the next byte of data from this piped input stream. The value byte is returned as an`int`in the range`0`to`255`. This method blocks until input data is available, the end of the stream is detected, or an exception is thrown.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the next byte of data, or`-1`if the end of the stream is reached. |

| Exceptions ||
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs. |
| `java.io.IOException` | if the pipe is [unconnected](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#connect(java.io.PipedOutputStream)), [`broken`](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#BROKEN), closed, or if an I/O error occurs. |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Int
```

Reads up to`len`bytes of data from this piped input stream into an array of bytes. Less than`len`bytes will be read if the end of the data stream is reached or if`len`exceeds the pipe's buffer size. If`len `is zero, then no bytes are read and 0 is returned; otherwise, the method blocks until at least 1 byte of input is available, end of the stream has been detected, or an exception is thrown.

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
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | If the first byte cannot be read for any reason other than end of file, or if the input stream has been closed, or if some other I/O error occurs. |
| `java.lang.NullPointerException` | If`b`is`null`. |
| `java.lang.IndexOutOfBoundsException` | If`off`is negative,`len`is negative, or`len`is greater than`b.length - off` |
| --- | --- |
| `java.lang.NullPointerException` | If`b`is`null`. |
| `java.lang.IndexOutOfBoundsException` | If`off`is negative,`len`is negative, or`len`is greater than`b.length - off` |
| `java.io.IOException` | if the pipe is [`broken`](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#BROKEN), [unconnected](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#connect(java.io.PipedOutputStream)), closed, or if an I/O error occurs. |
| --- | --- |

## Protected methods

### receive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun receive(b: Int): Unit
```

Receives a byte of data. This method will block if no input is available.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------|
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the byte being received |

| Exceptions ||
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | If the pipe is [`broken`](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#BROKEN), [unconnected](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#connect(java.io.PipedOutputStream)), closed, or if an I/O error occurs. |

## Properties

### buffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var buffer: ByteArray!
```

The circular buffer into which incoming data is placed. 

### in

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var in: Int
```

The index of the position in the circular buffer at which the next byte of data will be stored when received from the connected piped output stream.`in<0`implies the buffer is empty,`in==out`implies the buffer is full 

### out

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var out: Int
```

The index of the position in the circular buffer at which the next byte of data will be read by this piped input stream.
