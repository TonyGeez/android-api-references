# BufferedReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BufferedReader

```
open class BufferedReader : Reader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.io.Reader](https://developer.android.com/reference/kotlin/java/io/Reader) ||
| | ↳ | [java.io.BufferedReader](https://developer.android.com/reference/kotlin/java/io/BufferedReader#) |

| Known Direct Subclasses [LineNumberReader](https://developer.android.com/reference/kotlin/java/io/LineNumberReader) |---------------------------------------------------------------------------------------------|---------------------------------------------------------------------| | [LineNumberReader](https://developer.android.com/reference/kotlin/java/io/LineNumberReader) | A buffered character-input stream that keeps track of line numbers. | |
| --- | --- | --- | --- | --- | --- | --- |

Reads text from a character-input stream, buffering characters so as to provide for the efficient reading of characters, arrays, and lines.

The buffer size may be specified, or the default size may be used. The default is large enough for most purposes.

In general, each read request made of a Reader causes a corresponding read request to be made of the underlying character or byte stream. It is therefore advisable to wrap a BufferedReader around any Reader whose read() operations may be costly, such as FileReaders and InputStreamReaders. For example, 

```kotlin
BufferedReader in
    = new BufferedReader(new FileReader("foo.in"));
  
```
will buffer the input from the specified file. Without buffering, each invocation of read() or readLine() could cause bytes to be read from the file, converted into characters, and then returned, which can be very inefficient.

Programs that use DataInputStreams for textual input can be localized by replacing each DataInputStream with an appropriate BufferedReader.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BufferedReader](https://developer.android.com/reference/kotlin/java/io/BufferedReader#BufferedReader(java.io.Reader))`(`in:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader)!`)` Creates a buffering character-input stream that uses a default-sized input buffer. |
| [BufferedReader](https://developer.android.com/reference/kotlin/java/io/BufferedReader#BufferedReader(java.io.Reader,%20kotlin.Int))`(`in:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader)!`, `sz:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a buffering character-input stream that uses an input buffer of the specified size. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/io/BufferedReader#close())`()` <br /> |
| open [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [lines](https://developer.android.com/reference/kotlin/java/io/BufferedReader#lines())`()` Returns a`Stream`, the elements of which are lines read from this`BufferedReader`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mark](https://developer.android.com/reference/kotlin/java/io/BufferedReader#mark(kotlin.Int))`(`readAheadLimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Marks the present position in the stream. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [markSupported](https://developer.android.com/reference/kotlin/java/io/BufferedReader#markSupported())`()` Tells whether this stream supports the mark() operation, which it does. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/BufferedReader#read())`()` Reads a single character. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/BufferedReader#read(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads characters into a portion of an array. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [readLine](https://developer.android.com/reference/kotlin/java/io/BufferedReader#readLine())`()` Reads a line of text. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [ready](https://developer.android.com/reference/kotlin/java/io/BufferedReader#ready())`()` Tells whether this stream is ready to be read. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/java/io/BufferedReader#reset())`()` Resets the stream to the most recent mark. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [skip](https://developer.android.com/reference/kotlin/java/io/BufferedReader#skip(kotlin.Long))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Skips characters. |

| Inherited functions ||
|---|---|
| From class [Reader](https://developer.android.com/reference/kotlin/java/io/Reader) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader)! | [nullReader](https://developer.android.com/reference/kotlin/java/io/Reader#nullReader())`()` <br /> Returns a new`Reader`that reads no characters. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`read()`,`read(char[])`,`read(char[], int, int)`,`read(Charbuffer)`,`ready()`,`skip(long)`, and`transferTo()`methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw`IOException`. The`markSupported()`method returns`false`. The`mark()`and`reset()`methods throw an`IOException`. The [object](https://developer.android.com/reference/kotlin/java/io/Reader#lock:kotlin.Any) used to synchronize operations on the returned`Reader`is not specified. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/Reader#read(kotlin.CharArray))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` <br /> Reads characters into an array. This method will block until some input is available, an I/O error occurs, or the end of the stream is reached. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/Reader#read(java.nio.CharBuffer))`(`target:` ` [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer.html#)!`)` <br /> Attempts to read characters into the specified character buffer. The buffer is used as a repository of characters as-is: the only changes made are the results of a put operation. No flipping or rewinding of the buffer is performed. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [transferTo](https://developer.android.com/reference/kotlin/java/io/Reader#transferTo(java.io.Writer))`(`out:` ` [Writer](https://developer.android.com/reference/kotlin/java/io/Writer)!`)` <br /> Reads all characters from this reader and writes the characters to the given writer in the order that they are read. On return, this reader will be at end of the stream. This method does not close either reader or writer. This method may block indefinitely reading from the reader, or writing to the writer. The behavior for the case where the reader and/or writer is*asynchronously closed*, or the thread interrupted during the transfer, is highly reader and writer specific, and therefore not specified. If an I/O error occurs reading from the reader or writing to the writer, then it may do so after some characters have been read or written. Consequently the reader may not be at end of the stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs. <br /> | ||

| Inherited properties ||
|---|---|
| From class [Reader](https://developer.android.com/reference/kotlin/java/io/Reader) |-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [lock](https://developer.android.com/reference/kotlin/java/io/Reader#lock:kotlin.Any) <br /> The object used to synchronize operations on this stream. For efficiency, a character-stream object may use an object other than itself to protect critical sections. A subclass should therefore use the object in this field rather than`this`or a synchronized method. <br /> | ||

## Public constructors

### BufferedReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BufferedReader(in: Reader!)
```

Creates a buffering character-input stream that uses a default-sized input buffer.

| Parameters ||
|------|-----------------------------------------------------------------------------------|
| `in` | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader)!:A Reader |

### BufferedReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BufferedReader(
    in: Reader!, 
    sz: Int)
```

Creates a buffering character-input stream that uses an input buffer of the specified size.

| Parameters ||
|------|----------------------------------------------------------------------------------------------|
| `in` | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader)!:A Reader |
| `sz` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Input-buffer size |

| Exceptions ||
|--------------------------------------|-------------|
| `java.lang.IllegalArgumentException` | If`sz <= 0` |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

### lines

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun lines(): Stream<String!>!
```

Returns a`Stream`, the elements of which are lines read from this`BufferedReader`. The [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#) is lazily populated, i.e., read only occurs during the [terminal stream operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary.html#StreamOps).

The reader must not be operated on during the execution of the terminal stream operation. Otherwise, the result of the terminal stream operation is undefined.

After execution of the terminal stream operation there are no guarantees that the reader will be at a specific position from which to read the next character or line.

If an [IOException](https://developer.android.com/reference/kotlin/java/io/IOException) is thrown when accessing the underlying`BufferedReader`, it is wrapped in an [UncheckedIOException](https://developer.android.com/reference/kotlin/java/io/UncheckedIOException) which will be thrown from the`Stream`method that caused the read to take place. This method will return a Stream if invoked on a BufferedReader that is closed. Any operation on that stream that requires reading from the BufferedReader after it is closed, will cause an UncheckedIOException to be thrown.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | a`Stream<String>`providing the lines of text described by this`BufferedReader` |

### mark

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mark(readAheadLimit: Int): Unit
```

Marks the present position in the stream. Subsequent calls to reset() will attempt to reposition the stream to this point.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `readAheadLimit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Limit on the number of characters that may be read while still preserving the mark. An attempt to reset the stream after reading characters up to this limit or beyond may fail. A limit value larger than the size of the input buffer will cause a new buffer to be allocated whose size is no smaller than limit. Therefore large values should be used with care. |

| Exceptions ||
|--------------------------------------|------------------------|
| `java.lang.IllegalArgumentException` | If`readAheadLimit < 0` |
| `java.io.IOException` | If an I/O error occurs |

### markSupported

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun markSupported(): Boolean
```

Tells whether this stream supports the mark() operation, which it does.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if and only if this stream supports the mark operation. |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(): Int
```

Reads a single character.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The character read, as an integer in the range 0 to 65535 (0x00-0xffff), or -1 if the end of the stream has been reached |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(
    cbuf: CharArray!, 
    off: Int, 
    len: Int
): Int
```

Reads characters into a portion of an array.

This method implements the general contract of the corresponding [read](https://developer.android.com/reference/kotlin/java/io/Reader#read(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))method of the [Reader](https://developer.android.com/reference/kotlin/java/io/Reader) class. As an additional convenience, it attempts to read as many characters as possible by repeatedly invoking the`read`method of the underlying stream. This iterated`read`continues until one of the following conditions becomes true:

- The specified number of characters have been read,
- The`read`method of the underlying stream returns`-1`, indicating end-of-file, or
- The`ready`method of the underlying stream returns`false`, indicating that further input requests would block.

If the first`read`on the underlying stream returns`-1`to indicate end-of-file then this method returns`-1`. Otherwise this method returns the number of characters actually read.

Subclasses of this class are encouraged, but not required, to attempt to read as many characters as possible in the same fashion.

Ordinarily this method takes characters from this stream's character buffer, filling it from the underlying stream as necessary. If, however, the buffer is empty, the mark is not valid, and the requested length is at least as large as the buffer, then this method will read characters directly from the underlying stream into the given array. Thus redundant`BufferedReader`s will not copy data unnecessarily.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------|
| `cbuf` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:Destination buffer |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset at which to start storing characters |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Maximum number of characters to read |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of characters read, or -1 if the end of the stream has been reached |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------|
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.IndexOutOfBoundsException` | If`off`is negative, or`len`is negative, or`len`is greater than`cbuf.length - off` |

### readLine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun readLine(): String!
```

Reads a line of text. A line is considered to be terminated by any one of a line feed ('\\n'), a carriage return ('\\r'), a carriage return followed immediately by a line feed, or by reaching the end-of-file (EOF).

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | A String containing the contents of the line, not including any line-termination characters, or null if the end of the stream has been reached without reading any characters |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

**See Also**

### ready

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun ready(): Boolean
```

Tells whether this stream is ready to be read. A buffered character stream is ready if the buffer is not empty, or if the underlying character stream is ready.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the next read() is guaranteed not to block for input, false otherwise. Note that returning false does not guarantee that the next read will block. |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Resets the stream to the most recent mark.

| Exceptions ||
|-----------------------|--------------------------------------------------------------------------|
| `java.io.IOException` | If the stream has never been marked, or if the mark has been invalidated |

### skip

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun skip(n: Long): Long
```

Skips characters.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The number of characters to skip |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of characters actually skipped |

| Exceptions ||
|--------------------------------------|------------------------|
| `java.lang.IllegalArgumentException` | If`n`is negative. |
| `java.io.IOException` | If an I/O error occurs |
