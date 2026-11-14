# SequenceInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SequenceInputStream

```
open class SequenceInputStream : InputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.io.InputStream](InputStream.md) ||
| | ↳ | [java.io.SequenceInputStream](SequenceInputStream.md) |

A`SequenceInputStream`represents the logical concatenation of other input streams. It starts out with an ordered collection of input streams and reads from the first one until end of file is reached, whereupon it reads from the second one, and so on, until end of file is reached on the last of the contained input streams.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SequenceInputStream](SequenceInputStream.md))`(`s1:` ` [InputStream](InputStream.md)!`, `s2:` ` [InputStream](InputStream.md)!`)` Initializes a newly created`SequenceInputStream`by remembering the two arguments, which will be read in order, first`s1`and then`s2`, to provide the bytes to be read from this`SequenceInputStream`. |
| [SequenceInputStream](SequenceInputStream.md))`(`e:` ` [Enumeration](../java.util/Enumeration.md)<out` ` [InputStream](InputStream.md)!>!`)` Initializes a newly created`SequenceInputStream`by remembering the argument, which must be an`Enumeration`that produces objects whose run-time type is`InputStream`. |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [available](SequenceInputStream.md))`()` Returns an estimate of the number of bytes that can be read (or skipped over) from the current underlying input stream without blocking by the next invocation of a method for the current underlying input stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](SequenceInputStream.md))`()` Closes this input stream and releases any system resources associated with the stream. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](SequenceInputStream.md))`()` Reads the next byte of data from this input stream. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](SequenceInputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads up to`len`bytes of data from this input stream into an array of bytes. |

| Inherited functions ||
|---|---|
| From class [InputStream](InputStream.md) |------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mark](InputStream.md))`(`readlimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Marks the current position in this input stream. A subsequent call to the`reset`method repositions this stream at the last marked position so that subsequent reads re-read the same bytes. The`readlimit`arguments tells this input stream to allow that many bytes to be read before the mark position gets invalidated. The general contract of`mark`is that, if the method`markSupported`returns`true`, the stream somehow remembers all the bytes read after the call to`mark`and stands ready to supply those same bytes again if and whenever the method`reset`is called. However, the stream is not required to remember any data at all if more than`readlimit`bytes are read from the stream before`reset`is called. Marking a closed stream should not have any effect on the stream. The`mark`method of`InputStream`does nothing. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [markSupported](InputStream.md))`()` <br /> Tests if this input stream supports the`mark`and`reset`methods. Whether or not`mark`and`reset`are supported is an invariant property of a particular input stream instance. The`markSupported`method of`InputStream`returns`false`. <br /> | | [InputStream](InputStream.md)! | [nullInputStream](InputStream.md))`()` <br /> Returns a new`InputStream`that reads no bytes. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`available()`,`read()`,`read(byte[])`,`read(byte[], int, int)`,`readAllBytes()`,`readNBytes(byte[], int, int)`,`readNBytes(int)`,`skip(long)`,`skipNBytes(long)`, and`transferTo()`methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw`IOException`. The`markSupported()`method returns`false`. The`mark()`method does nothing, and the`reset()`method throws`IOException`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](InputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Reads some number of bytes from the input stream and stores them into the buffer array`b`. The number of bytes actually read is returned as an integer. This method blocks until input data is available, end of file is detected, or an exception is thrown. If the length of`b`is zero, then no bytes are read and`0`is returned; otherwise, there is an attempt to read at least one byte. If no byte is available because the stream is at the end of the file, the value`-1`is returned; otherwise, at least one byte is read and stored into`b`. The first byte read is stored into element`b[0]`, the next one into`b[1]`, and so on. The number of bytes read is, at most, equal to the length of`b`. Let*k* be the number of bytes actually read; these bytes will be stored in elements`b[0]`through`b[`*k* `-1]`, leaving elements`b[`*k* `]`through`b[b.length-1]`unaffected. The`read(b)`method for class`InputStream`has the same effect as: ```kotlin <code>read(b, 0, b.length) </code> ``` <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readAllBytes](InputStream.md))`()` <br /> Reads all remaining bytes from the input stream. This method blocks until all remaining bytes have been read and end of stream is detected, or an exception is thrown. This method does not close the input stream. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read all bytes into a byte array. It is not intended for reading input streams with large amounts of data. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readNBytes](InputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Reads the requested number of bytes from the input stream into the given byte array. This method blocks until`len`bytes of input data have been read, end of stream is detected, or an exception is thrown. The number of bytes actually read, possibly zero, is returned. This method does not close the input stream. In the case where end of stream is reached before`len`bytes have been read, then the actual number of bytes read will be returned. When this stream reaches end of stream, further invocations of this method will return zero. If`len`is zero, then no bytes are read and`0`is returned; otherwise, there is an attempt to read up to`len`bytes. The first byte read is stored into element`b[off]`, the next one in to`b[off+1]`, and so on. The number of bytes read is, at most, equal to`len`. Let*k* be the number of bytes actually read; these bytes will be stored in elements`b[off]`through`b[off+`*k* `-1]`, leaving elements`b[off+`*k* `]`through`b[off+len-1]`unaffected. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes of`b`have been updated with data from the input stream. Consequently the input stream and`b`may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readNBytes](InputStream.md))`(`len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Reads up to a specified number of bytes from the input stream. This method blocks until the requested number of bytes has been read, end of stream is detected, or an exception is thrown. This method does not close the input stream. The length of the returned array equals the number of bytes read from the stream. If`len`is zero, then no bytes are read and an empty byte array is returned. Otherwise, up to`len`bytes are read from the stream. Fewer than`len`bytes may be read if end of stream is encountered. When this stream reaches end of stream, further invocations of this method will return an empty byte array. Note that this method is intended for simple cases where it is convenient to read the specified number of bytes into a byte array. The total amount of memory allocated by this method is proportional to the number of bytes read from the stream which is bounded by`len`. Therefore, the method may be safely called with very large values of`len`provided sufficient memory is available. The behavior for the case where the input stream is*asynchronously closed*, or the thread interrupted during the read, is highly input stream specific, and therefore not specified. If an I/O error occurs reading from the input stream, then it may do so after some, but not all, bytes have been read. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](InputStream.md))`()` <br /> Repositions this stream to the position at the time the`mark`method was last called on this input stream. The general contract of`reset`is: - If the method`markSupported`returns`true`, then: - If the method`mark`has not been called since the stream was created, or the number of bytes read from the stream since`mark`was last called is larger than the argument to`mark`at that last call, then an`IOException`might be thrown. - If such an`IOException`is not thrown, then the stream is reset to a state such that all the bytes read since the most recent call to`mark`(or since the start of the file, if`mark`has not been called) will be resupplied to subsequent callers of the`read`method, followed by any bytes that otherwise would have been the next input data as of the time of the call to`reset`. - If the method`markSupported`returns`false`, then: - The call to`reset`may throw an`IOException`. - If an`IOException`is not thrown, then the stream is reset to a fixed state that depends on the particular type of the input stream and how it was created. The bytes that will be supplied to subsequent callers of the`read`method depend on the particular type of the input stream. The method`reset`for class`InputStream`does nothing except throw an`IOException`. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [skip](InputStream.md))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Skips over and discards`n`bytes of data from this input stream. The`skip`method may, for a variety of reasons, end up skipping over some smaller number of bytes, possibly`0`. This may result from any of a number of conditions; reaching end of file before`n`bytes have been skipped is only one possibility. The actual number of bytes skipped is returned. If`n`is negative, the`skip`method for class`InputStream`always returns 0, and no bytes are skipped. Subclasses may handle the negative value differently. The`skip`method implementation of this class creates a byte array and then repeatedly reads into it until`n`bytes have been read or the end of the stream has been reached. Subclasses are encouraged to provide a more efficient implementation of this method. For instance, the implementation may depend on the ability to seek. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [skipNBytes](InputStream.md))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Skips over and discards exactly`n`bytes of data from this input stream. If`n`is zero, then no bytes are skipped. If`n`is negative, then no bytes are skipped. Subclasses may handle the negative value differently. This method blocks until the requested number of bytes has been skipped, end of file is reached, or an exception is thrown. If end of stream is reached before the stream is at the desired position, then an`EOFException`is thrown. If an I/O error occurs, then the input stream may be in an inconsistent state. It is strongly recommended that the stream be promptly closed if an I/O error occurs. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [transferTo](InputStream.md))`(`out:` ` [OutputStream](OutputStream.md)!`)` <br /> Reads all bytes from this input stream and writes the bytes to the given output stream in the order that they are read. On return, this input stream will be at end of stream. This method does not close either stream. This method may block indefinitely reading from the input stream, or writing to the output stream. The behavior for the case where the input and/or output stream is*asynchronously closed*, or the thread interrupted during the transfer, is highly input and output stream specific, and therefore not specified. If an I/O error occurs reading from the input stream or writing to the output stream, then it may do so after some bytes have been read or written. Consequently the input stream may not be at end of stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs. <br /> | ||

## Public constructors

### SequenceInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SequenceInputStream(
    s1: InputStream!, 
    s2: InputStream!)
```

Initializes a newly created`SequenceInputStream`by remembering the two arguments, which will be read in order, first`s1`and then`s2`, to provide the bytes to be read from this`SequenceInputStream`.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------|
| `s1` | [InputStream](InputStream.md)!:the first input stream to read. |
| `s2` | [InputStream](InputStream.md)!:the second input stream to read. |

### SequenceInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SequenceInputStream(e: Enumeration<out InputStream!>!)
```

Initializes a newly created`SequenceInputStream`by remembering the argument, which must be an`Enumeration`that produces objects whose run-time type is`InputStream`. The input streams that are produced by the enumeration will be read, in order, to provide the bytes to be read from this`SequenceInputStream`. After each input stream from the enumeration is exhausted, it is closed by calling its`close`method.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [Enumeration](../java.util/Enumeration.md)\<out [InputStream](InputStream.md)!\>!:an enumeration of input streams. |

**See Also**

- [java.util.Enumeration](../java.util/Enumeration.md)

## Public methods

### available

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun available(): Int
```

Returns an estimate of the number of bytes that can be read (or skipped over) from the current underlying input stream without blocking by the next invocation of a method for the current underlying input stream. The next invocation might be the same thread or another thread. A single read or skip of this many bytes will not block, but may read or skip fewer bytes.

This method simply calls`available`of the current underlying input stream and returns the result.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an estimate of the number of bytes that can be read (or skipped over) from the current underlying input stream without blocking or`0`if this input stream has been closed by invoking its #close() method |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |
| `java.io.IOException` | if an I/O error occurs. |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes this input stream and releases any system resources associated with the stream. A closed`SequenceInputStream`cannot perform input operations and cannot be reopened.

If this stream was created from an enumeration, all remaining elements are requested from the enumeration and closed before the`close`method returns.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs. |
| `java.io.IOException` | if an I/O error occurs. |
| --- | --- |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(): Int
```

Reads the next byte of data from this input stream. The byte is returned as an`int`in the range`0`to`255`. If no byte is available because the end of the stream has been reached, the value`-1`is returned. This method blocks until input data is available, the end of the stream is detected, or an exception is thrown.

This method tries to read one character from the current substream. If it reaches the end of the stream, it calls the`close`method of the current substream and begins reading from the next substream.

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
open fun read(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Int
```

Reads up to`len`bytes of data from this input stream into an array of bytes. If`len`is not zero, the method blocks until at least 1 byte of input is available; otherwise, no bytes are read and`0`is returned.

The`read`method of`SequenceInputStream`tries to read the data from the current substream. If it fails to read any characters because the substream has reached the end of the stream, it calls the`close`method of the current substream and begins reading from the next substream.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer into which the data is read. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset in array`b`at which the data is written. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of bytes read. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | int the number of bytes read. |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | If the first byte cannot be read for any reason other than end of file, or if the input stream has been closed, or if some other I/O error occurs. |
| `java.lang.NullPointerException` | If`b`is`null`. |
| `java.lang.IndexOutOfBoundsException` | If`off`is negative,`len`is negative, or`len`is greater than`b.length - off` |
| --- | --- |
| `java.lang.NullPointerException` | If`b`is`null`. |
| `java.lang.IndexOutOfBoundsException` | If`off`is negative,`len`is negative, or`len`is greater than`b.length - off` |
| `java.io.IOException` | if an I/O error occurs. |
| --- | --- |
