# PipedReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PipedReader

```
open class PipedReader : Reader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.io.Reader](https://developer.android.com/reference/kotlin/java/io/Reader) ||
| | ↳ | [java.io.PipedReader](https://developer.android.com/reference/kotlin/java/io/PipedReader#) |

Piped character-input streams.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PipedReader](https://developer.android.com/reference/kotlin/java/io/PipedReader#PipedReader())`()` Creates a`PipedReader`so that it is not yet [connected](https://developer.android.com/reference/kotlin/java/io/PipedReader#connect(java.io.PipedWriter)). |
| [PipedReader](https://developer.android.com/reference/kotlin/java/io/PipedReader#PipedReader(kotlin.Int))`(`pipeSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a`PipedReader`so that it is not yet [connected](https://developer.android.com/reference/kotlin/java/io/PipedReader#connect(java.io.PipedWriter))and uses the specified pipe size for the pipe's buffer. |
| [PipedReader](https://developer.android.com/reference/kotlin/java/io/PipedReader#PipedReader(java.io.PipedWriter))`(`src:` ` [PipedWriter](https://developer.android.com/reference/kotlin/java/io/PipedWriter)!`)` Creates a`PipedReader`so that it is connected to the piped writer`src`. |
| [PipedReader](https://developer.android.com/reference/kotlin/java/io/PipedReader#PipedReader(java.io.PipedWriter,%20kotlin.Int))`(`src:` ` [PipedWriter](https://developer.android.com/reference/kotlin/java/io/PipedWriter)!`, `pipeSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a`PipedReader`so that it is connected to the piped writer`src`and uses the specified pipe size for the pipe's buffer. |

| Public methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/io/PipedReader#close())`()` Closes this piped stream and releases any system resources associated with the stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/java/io/PipedReader#connect(java.io.PipedWriter))`(`src:` ` [PipedWriter](https://developer.android.com/reference/kotlin/java/io/PipedWriter)!`)` Causes this piped reader to be connected to the piped writer`src`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/PipedReader#read())`()` Reads the next character of data from this piped stream. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/PipedReader#read(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads up to`len`characters of data from this piped stream into an array of characters. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [ready](https://developer.android.com/reference/kotlin/java/io/PipedReader#ready())`()` Tell whether this stream is ready to be read. |

| Inherited functions ||
|---|---|
| From class [Reader](https://developer.android.com/reference/kotlin/java/io/Reader) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mark](https://developer.android.com/reference/kotlin/java/io/Reader#mark(kotlin.Int))`(`readAheadLimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Marks the present position in the stream. Subsequent calls to reset() will attempt to reposition the stream to this point. Not all character-input streams support the mark() operation. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [markSupported](https://developer.android.com/reference/kotlin/java/io/Reader#markSupported())`()` <br /> Tells whether this stream supports the mark() operation. The default implementation always returns false. Subclasses should override this method. <br /> | | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader)! | [nullReader](https://developer.android.com/reference/kotlin/java/io/Reader#nullReader())`()` <br /> Returns a new`Reader`that reads no characters. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`read()`,`read(char[])`,`read(char[], int, int)`,`read(Charbuffer)`,`ready()`,`skip(long)`, and`transferTo()`methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw`IOException`. The`markSupported()`method returns`false`. The`mark()`and`reset()`methods throw an`IOException`. The [object](https://developer.android.com/reference/kotlin/java/io/Reader#lock:kotlin.Any) used to synchronize operations on the returned`Reader`is not specified. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/Reader#read(kotlin.CharArray))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` <br /> Reads characters into an array. This method will block until some input is available, an I/O error occurs, or the end of the stream is reached. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/Reader#read(java.nio.CharBuffer))`(`target:` ` [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer.html#)!`)` <br /> Attempts to read characters into the specified character buffer. The buffer is used as a repository of characters as-is: the only changes made are the results of a put operation. No flipping or rewinding of the buffer is performed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/java/io/Reader#reset())`()` <br /> Resets the stream. If the stream has been marked, then attempt to reposition it at the mark. If the stream has not been marked, then attempt to reset it in some way appropriate to the particular stream, for example by repositioning it to its starting point. Not all character-input streams support the reset() operation, and some support reset() without supporting mark(). <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [skip](https://developer.android.com/reference/kotlin/java/io/Reader#skip(kotlin.Long))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Skips characters. This method will block until some characters are available, an I/O error occurs, or the end of the stream is reached. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [transferTo](https://developer.android.com/reference/kotlin/java/io/Reader#transferTo(java.io.Writer))`(`out:` ` [Writer](https://developer.android.com/reference/kotlin/java/io/Writer)!`)` <br /> Reads all characters from this reader and writes the characters to the given writer in the order that they are read. On return, this reader will be at end of the stream. This method does not close either reader or writer. This method may block indefinitely reading from the reader, or writing to the writer. The behavior for the case where the reader and/or writer is*asynchronously closed*, or the thread interrupted during the transfer, is highly reader and writer specific, and therefore not specified. If an I/O error occurs reading from the reader or writing to the writer, then it may do so after some characters have been read or written. Consequently the reader may not be at end of the stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs. <br /> | ||

| Inherited properties ||
|---|---|
| From class [Reader](https://developer.android.com/reference/kotlin/java/io/Reader) |-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [lock](https://developer.android.com/reference/kotlin/java/io/Reader#lock:kotlin.Any) <br /> The object used to synchronize operations on this stream. For efficiency, a character-stream object may use an object other than itself to protect critical sections. A subclass should therefore use the object in this field rather than`this`or a synchronized method. <br /> | ||

## Public constructors

### PipedReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PipedReader()
```

Creates a`PipedReader`so that it is not yet [connected](https://developer.android.com/reference/kotlin/java/io/PipedReader#connect(java.io.PipedWriter)). It must be [connected](https://developer.android.com/reference/kotlin/java/io/PipedWriter#connect(java.io.PipedReader))to a`PipedWriter`before being used. 

### PipedReader

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PipedReader(pipeSize: Int)
```

Creates a`PipedReader`so that it is not yet [connected](https://developer.android.com/reference/kotlin/java/io/PipedReader#connect(java.io.PipedWriter))and uses the specified pipe size for the pipe's buffer. It must be [connected](https://developer.android.com/reference/kotlin/java/io/PipedWriter#connect(java.io.PipedReader))to a`PipedWriter`before being used.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------|
| `pipeSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the size of the pipe's buffer. |

| Exceptions ||
|--------------------------------------|--------------------|
| `java.lang.IllegalArgumentException` | if`pipeSize <= 0`. |

### PipedReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PipedReader(src: PipedWriter!)
```

Creates a`PipedReader`so that it is connected to the piped writer`src`. Data written to`src`will then be available as input from this stream.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------|
| `src` | [PipedWriter](https://developer.android.com/reference/kotlin/java/io/PipedWriter)!:the stream to connect to. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### PipedReader

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PipedReader(
    src: PipedWriter!, 
    pipeSize: Int)
```

Creates a`PipedReader`so that it is connected to the piped writer`src`and uses the specified pipe size for the pipe's buffer. Data written to`src`will then be available as input from this stream.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------|
| `src` | [PipedWriter](https://developer.android.com/reference/kotlin/java/io/PipedWriter)!:the stream to connect to. |
| `pipeSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the size of the pipe's buffer. |

| Exceptions ||
|--------------------------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |
| `java.lang.IllegalArgumentException` | if`pipeSize <= 0`. |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes this piped stream and releases any system resources associated with the stream.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |
| `java.io.IOException` | if an I/O error occurs. |
| --- | --- |

### connect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun connect(src: PipedWriter!): Unit
```

Causes this piped reader to be connected to the piped writer`src`. If this object is already connected to some other piped writer, an`IOException`is thrown.

If`src`is an unconnected piped writer and`snk`is an unconnected piped reader, they may be connected by either the call: 

```kotlin
<code>snk.connect(src)</code>
```

or the call: 

```kotlin
<code>src.connect(snk)</code>
```

The two calls have the same effect.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------|
| `src` | [PipedWriter](https://developer.android.com/reference/kotlin/java/io/PipedWriter)!:The piped writer to connect to. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(): Int
```

Reads the next character of data from this piped stream. If no character is available because the end of the stream has been reached, the value`-1`is returned. This method blocks until input data is available, the end of the stream is detected, or an exception is thrown.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the next character of data, or`-1`if the end of the stream is reached. |

| Exceptions ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if the pipe is [`broken`](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#BROKEN), [unconnected](https://developer.android.com/reference/kotlin/java/io/PipedReader#connect(java.io.PipedWriter)), closed, or an I/O error occurs. |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(
    cbuf: CharArray!, 
    off: Int, 
    len: Int
): Int
```

Reads up to`len`characters of data from this piped stream into an array of characters. Less than`len`characters will be read if the end of the data stream is reached or if`len`exceeds the pipe's buffer size. This method blocks until at least one character of input is available.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------|
| `cbuf` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the buffer into which the data is read. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset of the data. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of characters read. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the total number of characters read into the buffer, or`-1`if there is no more data because the end of the stream has been reached. |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if the pipe is [`broken`](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#BROKEN), [unconnected](https://developer.android.com/reference/kotlin/java/io/PipedReader#connect(java.io.PipedWriter)), closed, or an I/O error occurs. |
| `java.lang.IndexOutOfBoundsException` | If`off`is negative, or`len`is negative, or`len`is greater than`cbuf.length - off` |

### ready

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun ready(): Boolean
```

Tell whether this stream is ready to be read. A piped character stream is ready if the circular buffer is not empty.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the next read() is guaranteed not to block for input, false otherwise. Note that returning false does not guarantee that the next read will block. |

| Exceptions ||
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if the pipe is [`broken`](https://developer.android.com/reference/kotlin/java/io/PipedInputStream#BROKEN), [unconnected](https://developer.android.com/reference/kotlin/java/io/PipedReader#connect(java.io.PipedWriter)), or closed. |
