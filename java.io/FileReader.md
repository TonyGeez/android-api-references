# FileReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileReader

```
open class FileReader : InputStreamReader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [java.io.Reader](https://developer.android.com/reference/kotlin/java/io/Reader) |||
| | ↳ | [java.io.InputStreamReader](https://developer.android.com/reference/kotlin/java/io/InputStreamReader) ||
| | | ↳ | [java.io.FileReader](https://developer.android.com/reference/kotlin/java/io/FileReader#) |

Reads text from character files using a default buffer size. Decoding from bytes to characters uses either a specified [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) or the platform's [default charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset()).

The`FileReader`is meant for reading streams of characters. For reading streams of raw bytes, consider using a`FileInputStream`.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileReader](https://developer.android.com/reference/kotlin/java/io/FileReader#FileReader(java.io.File))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File)!`)` Creates a new`FileReader`, given the`File`to read, using the platform's [default charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset()). |
| [FileReader](https://developer.android.com/reference/kotlin/java/io/FileReader#FileReader(java.io.File,%20java.nio.charset.Charset))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File)!`, `charset:` ` [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!`)` Creates a new`FileReader`, given the`File`to read and the [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#). |
| [FileReader](https://developer.android.com/reference/kotlin/java/io/FileReader#FileReader(java.io.FileDescriptor))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor)!`)` Creates a new`FileReader`, given the`FileDescriptor`to read, using the platform's [default charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset()). |
| [FileReader](https://developer.android.com/reference/kotlin/java/io/FileReader#FileReader(kotlin.String))`(`fileName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new`FileReader`, given the name of the file to read, using the platform's [default charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset()). |
| [FileReader](https://developer.android.com/reference/kotlin/java/io/FileReader#FileReader(kotlin.String,%20java.nio.charset.Charset))`(`fileName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `charset:` ` [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!`)` Creates a new`FileReader`, given the name of the file to read and the [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#). |

| Inherited functions ||
|---|---|
| From class [InputStreamReader](https://developer.android.com/reference/kotlin/java/io/InputStreamReader) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/io/InputStreamReader#close())`()` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEncoding](https://developer.android.com/reference/kotlin/java/io/InputStreamReader#getEncoding())`()` <br /> Returns the name of the character encoding being used by this stream. If the encoding has an historical name then that name is returned; otherwise the encoding's canonical name is returned. If this instance was created with the [InputStreamReader(java.io.InputStream,java.lang.String)](https://developer.android.com/reference/kotlin/java/io/InputStreamReader#InputStreamReader(java.io.InputStream,%20kotlin.String))constructor then the returned name, being unique for the encoding, may differ from the name passed to the constructor. This method will return`null`if the stream has been closed. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/InputStreamReader#read())`()` <br /> Reads a single character. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/InputStreamReader#read(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Reads characters into a portion of an array. This method will block until some input is available, an I/O error occurs, or the end of the stream is reached. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/InputStreamReader#read(java.nio.CharBuffer))`(`target:` ` [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer.html#)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [ready](https://developer.android.com/reference/kotlin/java/io/InputStreamReader#ready())`()` <br /> Tells whether this stream is ready to be read. An InputStreamReader is ready if its input buffer is not empty, or if bytes are available to be read from the underlying byte stream. <br /> | ||
| From class [Reader](https://developer.android.com/reference/kotlin/java/io/Reader) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mark](https://developer.android.com/reference/kotlin/java/io/Reader#mark(kotlin.Int))`(`readAheadLimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Marks the present position in the stream. Subsequent calls to reset() will attempt to reposition the stream to this point. Not all character-input streams support the mark() operation. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [markSupported](https://developer.android.com/reference/kotlin/java/io/Reader#markSupported())`()` <br /> Tells whether this stream supports the mark() operation. The default implementation always returns false. Subclasses should override this method. <br /> | | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader)! | [nullReader](https://developer.android.com/reference/kotlin/java/io/Reader#nullReader())`()` <br /> Returns a new`Reader`that reads no characters. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`read()`,`read(char[])`,`read(char[], int, int)`,`read(Charbuffer)`,`ready()`,`skip(long)`, and`transferTo()`methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw`IOException`. The`markSupported()`method returns`false`. The`mark()`and`reset()`methods throw an`IOException`. The [object](https://developer.android.com/reference/kotlin/java/io/Reader#lock:kotlin.Any) used to synchronize operations on the returned`Reader`is not specified. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/Reader#read(kotlin.CharArray))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` <br /> Reads characters into an array. This method will block until some input is available, an I/O error occurs, or the end of the stream is reached. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/java/io/Reader#reset())`()` <br /> Resets the stream. If the stream has been marked, then attempt to reposition it at the mark. If the stream has not been marked, then attempt to reset it in some way appropriate to the particular stream, for example by repositioning it to its starting point. Not all character-input streams support the reset() operation, and some support reset() without supporting mark(). <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [skip](https://developer.android.com/reference/kotlin/java/io/Reader#skip(kotlin.Long))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Skips characters. This method will block until some characters are available, an I/O error occurs, or the end of the stream is reached. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [transferTo](https://developer.android.com/reference/kotlin/java/io/Reader#transferTo(java.io.Writer))`(`out:` ` [Writer](https://developer.android.com/reference/kotlin/java/io/Writer)!`)` <br /> Reads all characters from this reader and writes the characters to the given writer in the order that they are read. On return, this reader will be at end of the stream. This method does not close either reader or writer. This method may block indefinitely reading from the reader, or writing to the writer. The behavior for the case where the reader and/or writer is*asynchronously closed*, or the thread interrupted during the transfer, is highly reader and writer specific, and therefore not specified. If an I/O error occurs reading from the reader or writing to the writer, then it may do so after some characters have been read or written. Consequently the reader may not be at end of the stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs. <br /> | ||

| Inherited properties ||
|---|---|
| From class [Reader](https://developer.android.com/reference/kotlin/java/io/Reader) |-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [lock](https://developer.android.com/reference/kotlin/java/io/Reader#lock:kotlin.Any) <br /> The object used to synchronize operations on this stream. For efficiency, a character-stream object may use an object other than itself to protect critical sections. A subclass should therefore use the object in this field rather than`this`or a synchronized method. <br /> | ||

## Public constructors

### FileReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileReader(file: File!)
```

Creates a new`FileReader`, given the`File`to read, using the platform's [default charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset()).

| Parameters ||
|--------|---------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File)!:the`File`to read |

| Exceptions ||
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | if the file does not exist, is a directory rather than a regular file, or for some other reason cannot be opened for reading. |

### FileReader

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileReader(
    file: File!, 
    charset: Charset!)
```

Creates a new`FileReader`, given the`File`to read and the [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#).

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File)!:the`File`to read |
| `charset` | [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!:the [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) |

| Exceptions ||
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if the file does not exist, is a directory rather than a regular file, or for some other reason cannot be opened for reading. |

### FileReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileReader(fd: FileDescriptor!)
```

Creates a new`FileReader`, given the`FileDescriptor`to read, using the platform's [default charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset()).

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor)!:the`FileDescriptor`to read |

### FileReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileReader(fileName: String!)
```

Creates a new`FileReader`, given the name of the file to read, using the platform's [default charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset()).

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------|
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the file to read |

| Exceptions ||
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | if the named file does not exist, is a directory rather than a regular file, or for some other reason cannot be opened for reading. |

### FileReader

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileReader(
    fileName: String!, 
    charset: Charset!)
```

Creates a new`FileReader`, given the name of the file to read and the [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#).

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the file to read |
| `charset` | [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!:the [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) |

| Exceptions ||
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if the named file does not exist, is a directory rather than a regular file, or for some other reason cannot be opened for reading. |
