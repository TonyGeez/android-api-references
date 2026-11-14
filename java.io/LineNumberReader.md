# LineNumberReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LineNumberReader

```
open class LineNumberReader : BufferedReader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.io.Reader](https://developer.android.com/reference/kotlin/java/io/Reader) |||
| | ↳ | [java.io.BufferedReader](https://developer.android.com/reference/kotlin/java/io/BufferedReader) ||
| | | ↳ | [java.io.LineNumberReader](https://developer.android.com/reference/kotlin/java/io/LineNumberReader#) |
| --- | --- | --- | --- |

A buffered character-input stream that keeps track of line numbers. This class defines methods [setLineNumber(int)](https://developer.android.com/reference/kotlin/java/io/LineNumberReader#setLineNumber(kotlin.Int))and [getLineNumber()](https://developer.android.com/reference/kotlin/java/io/LineNumberReader#getLineNumber())for setting and getting the current line number respectively.

By default, line numbering begins at 0. This number increments at every [line terminator](https://developer.android.com/reference/kotlin/java/io/LineNumberReader#lt) as the data is read, and can be changed with a call to`setLineNumber(int)`. Note however, that`setLineNumber(int)`does not actually change the current position in the stream; it only changes the value that will be returned by`getLineNumber()`.

A line is considered to be terminated by any one of a line feed ('\\n'), a carriage return ('\\r'), or a carriage return followed immediately by a linefeed.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LineNumberReader](https://developer.android.com/reference/kotlin/java/io/LineNumberReader#LineNumberReader(java.io.Reader))`(`in:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader)!`)` Create a new line-numbering reader, using the default input-buffer size. |
| [LineNumberReader](https://developer.android.com/reference/kotlin/java/io/LineNumberReader#LineNumberReader(java.io.Reader,%20kotlin.Int))`(`in:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader)!`, `sz:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new line-numbering reader, reading characters into a buffer of the given size. |

| Public methods ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineNumber](https://developer.android.com/reference/kotlin/java/io/LineNumberReader#getLineNumber())`()` Get the current line number. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mark](https://developer.android.com/reference/kotlin/java/io/LineNumberReader#mark(kotlin.Int))`(`readAheadLimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Mark the present position in the stream. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/LineNumberReader#read())`()` Read a single character. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/LineNumberReader#read(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Read characters into a portion of an array. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [readLine](https://developer.android.com/reference/kotlin/java/io/LineNumberReader#readLine())`()` Read a line of text. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/java/io/LineNumberReader#reset())`()` Reset the stream to the most recent mark. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLineNumber](https://developer.android.com/reference/kotlin/java/io/LineNumberReader#setLineNumber(kotlin.Int))`(`lineNumber:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the current line number. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [skip](https://developer.android.com/reference/kotlin/java/io/LineNumberReader#skip(kotlin.Long))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Skip characters. |

| Inherited functions ||
|---|---|
| From class [BufferedReader](https://developer.android.com/reference/kotlin/java/io/BufferedReader) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/io/BufferedReader#close())`()` <br /> | | [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [lines](https://developer.android.com/reference/kotlin/java/io/BufferedReader#lines())`()` <br /> Returns a`Stream`, the elements of which are lines read from this`BufferedReader`. The [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#) is lazily populated, i.e., read only occurs during the [terminal stream operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary.html#StreamOps). The reader must not be operated on during the execution of the terminal stream operation. Otherwise, the result of the terminal stream operation is undefined. After execution of the terminal stream operation there are no guarantees that the reader will be at a specific position from which to read the next character or line. If an [IOException](https://developer.android.com/reference/kotlin/java/io/IOException) is thrown when accessing the underlying`BufferedReader`, it is wrapped in an [UncheckedIOException](https://developer.android.com/reference/kotlin/java/io/UncheckedIOException) which will be thrown from the`Stream`method that caused the read to take place. This method will return a Stream if invoked on a BufferedReader that is closed. Any operation on that stream that requires reading from the BufferedReader after it is closed, will cause an UncheckedIOException to be thrown. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [markSupported](https://developer.android.com/reference/kotlin/java/io/BufferedReader#markSupported())`()` <br /> Tells whether this stream supports the mark() operation, which it does. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [ready](https://developer.android.com/reference/kotlin/java/io/BufferedReader#ready())`()` <br /> Tells whether this stream is ready to be read. A buffered character stream is ready if the buffer is not empty, or if the underlying character stream is ready. <br /> | ||
| From class [Reader](https://developer.android.com/reference/kotlin/java/io/Reader) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader)! | [nullReader](https://developer.android.com/reference/kotlin/java/io/Reader#nullReader())`()` <br /> Returns a new`Reader`that reads no characters. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`read()`,`read(char[])`,`read(char[], int, int)`,`read(Charbuffer)`,`ready()`,`skip(long)`, and`transferTo()`methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw`IOException`. The`markSupported()`method returns`false`. The`mark()`and`reset()`methods throw an`IOException`. The [object](https://developer.android.com/reference/kotlin/java/io/Reader#lock:kotlin.Any) used to synchronize operations on the returned`Reader`is not specified. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/Reader#read(kotlin.CharArray))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` <br /> Reads characters into an array. This method will block until some input is available, an I/O error occurs, or the end of the stream is reached. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/Reader#read(java.nio.CharBuffer))`(`target:` ` [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer.html#)!`)` <br /> Attempts to read characters into the specified character buffer. The buffer is used as a repository of characters as-is: the only changes made are the results of a put operation. No flipping or rewinding of the buffer is performed. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [transferTo](https://developer.android.com/reference/kotlin/java/io/Reader#transferTo(java.io.Writer))`(`out:` ` [Writer](https://developer.android.com/reference/kotlin/java/io/Writer)!`)` <br /> Reads all characters from this reader and writes the characters to the given writer in the order that they are read. On return, this reader will be at end of the stream. This method does not close either reader or writer. This method may block indefinitely reading from the reader, or writing to the writer. The behavior for the case where the reader and/or writer is*asynchronously closed*, or the thread interrupted during the transfer, is highly reader and writer specific, and therefore not specified. If an I/O error occurs reading from the reader or writing to the writer, then it may do so after some characters have been read or written. Consequently the reader may not be at end of the stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs. <br /> | ||

| Inherited properties ||
|---|---|
| From class [Reader](https://developer.android.com/reference/kotlin/java/io/Reader) |-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [lock](https://developer.android.com/reference/kotlin/java/io/Reader#lock:kotlin.Any) <br /> The object used to synchronize operations on this stream. For efficiency, a character-stream object may use an object other than itself to protect critical sections. A subclass should therefore use the object in this field rather than`this`or a synchronized method. <br /> | ||

## Public constructors

### LineNumberReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LineNumberReader(in: Reader!)
```

Create a new line-numbering reader, using the default input-buffer size.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------|
| `in` | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader)!:A Reader object to provide the underlying stream |

### LineNumberReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LineNumberReader(
    in: Reader!, 
    sz: Int)
```

Create a new line-numbering reader, reading characters into a buffer of the given size.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------|
| `in` | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader)!:A Reader object to provide the underlying stream |
| `sz` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):An int specifying the size of the buffer |

## Public methods

### getLineNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLineNumber(): Int
```

Get the current line number.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The current line number |

**See Also**

- [#setLineNumber](https://developer.android.com/reference/kotlin/java/io/LineNumberReader#setLineNumber(kotlin.Int)) 

### mark

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mark(readAheadLimit: Int): Unit
```

Mark the present position in the stream. Subsequent calls to reset() will attempt to reposition the stream to this point, and will also reset the line number appropriately.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `readAheadLimit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Limit on the number of characters that may be read while still preserving the mark. After reading this many characters, attempting to reset the stream may fail. |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(): Int
```

Read a single character. [Line terminators](https://developer.android.com/reference/kotlin/java/io/LineNumberReader#lt) are compressed into single newline ('\\n') characters. Whenever a line terminator is read the current line number is incremented.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The character read, or -1 if the end of the stream has been reached |

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

Read characters into a portion of an array. Whenever a [line terminator](https://developer.android.com/reference/kotlin/java/io/LineNumberReader#lt) is read the current line number is incremented.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------|
| `cbuf` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:Destination buffer |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset at which to start storing characters |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Maximum number of characters to read |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of bytes read, or -1 if the end of the stream has already been reached |

| Exceptions ||
|---------------------------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.IndexOutOfBoundsException` | |

### readLine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun readLine(): String!
```

Read a line of text. Whenever a [line terminator](https://developer.android.com/reference/kotlin/java/io/LineNumberReader#lt) is read the current line number is incremented.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | A String containing the contents of the line, not including any [line termination characters](https://developer.android.com/reference/kotlin/java/io/LineNumberReader#lt), or`null`if the end of the stream has been reached |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Reset the stream to the most recent mark.

| Exceptions ||
|-----------------------|------------------------------------------------------------------------|
| `java.io.IOException` | If the stream has not been marked, or if the mark has been invalidated |

### setLineNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLineNumber(lineNumber: Int): Unit
```

Set the current line number.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------|
| `lineNumber` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):An int specifying the line number |

**See Also**

- [#getLineNumber](https://developer.android.com/reference/kotlin/java/io/LineNumberReader#getLineNumber()) 

### skip

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun skip(n: Long): Long
```

Skip characters.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The number of characters to skip |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of characters actually skipped |

| Exceptions ||
|--------------------------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.IllegalArgumentException` | If`n`is negative |
