# FileWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileWriter

```
open class FileWriter : OutputStreamWriter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.io.Writer](https://developer.android.com/reference/kotlin/java/io/Writer) |||
| | ↳ | [java.io.OutputStreamWriter](https://developer.android.com/reference/kotlin/java/io/OutputStreamWriter) ||
| | | ↳ | [java.io.FileWriter](https://developer.android.com/reference/kotlin/java/io/FileWriter#) |
| --- | --- | --- | --- |

Writes text to character files using a default buffer size. Encoding from characters to bytes uses either a specified [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) or the platform's [default charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset()).

Whether or not a file is available or may be created depends upon the underlying platform. Some platforms, in particular, allow a file to be opened for writing by only one`FileWriter`(or other file-writing object) at a time. In such situations the constructors in this class will fail if the file involved is already open.

The`FileWriter`is meant for writing streams of characters. For writing streams of raw bytes, consider using a`FileOutputStream`.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileWriter](https://developer.android.com/reference/kotlin/java/io/FileWriter#FileWriter(java.io.File))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File)!`)` Constructs a`FileWriter`given the`File`to write, using the platform's [default charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset()) |
| [FileWriter](https://developer.android.com/reference/kotlin/java/io/FileWriter#FileWriter(java.io.File,%20kotlin.Boolean))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File)!`, `append:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Constructs a`FileWriter`given the`File`to write and a boolean indicating whether to append the data written, using the platform's [default charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset()). |
| [FileWriter](https://developer.android.com/reference/kotlin/java/io/FileWriter#FileWriter(java.io.File,%20java.nio.charset.Charset))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File)!`, `charset:` ` [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!`)` Constructs a`FileWriter`given the`File`to write and [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#). |
| [FileWriter](https://developer.android.com/reference/kotlin/java/io/FileWriter#FileWriter(java.io.File,%20java.nio.charset.Charset,%20kotlin.Boolean))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File)!`, `charset:` ` [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!`, `append:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Constructs a`FileWriter`given the`File`to write, [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) and a boolean indicating whether to append the data written. |
| [FileWriter](https://developer.android.com/reference/kotlin/java/io/FileWriter#FileWriter(java.io.FileDescriptor))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor)!`)` Constructs a`FileWriter`given a file descriptor, using the platform's [default charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset()). |
| [FileWriter](https://developer.android.com/reference/kotlin/java/io/FileWriter#FileWriter(kotlin.String))`(`fileName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`FileWriter`given a file name, using the platform's [default charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset()) |
| [FileWriter](https://developer.android.com/reference/kotlin/java/io/FileWriter#FileWriter(kotlin.String,%20kotlin.Boolean))`(`fileName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `append:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Constructs a`FileWriter`given a file name and a boolean indicating whether to append the data written, using the platform's [default charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset()). |
| [FileWriter](https://developer.android.com/reference/kotlin/java/io/FileWriter#FileWriter(kotlin.String,%20java.nio.charset.Charset))`(`fileName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `charset:` ` [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!`)` Constructs a`FileWriter`given a file name and [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#). |
| [FileWriter](https://developer.android.com/reference/kotlin/java/io/FileWriter#FileWriter(kotlin.String,%20java.nio.charset.Charset,%20kotlin.Boolean))`(`fileName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `charset:` ` [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!`, `append:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Constructs a`FileWriter`given a file name, [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) and a boolean indicating whether to append the data written. |

| Inherited functions ||
|---|---|
| From class [OutputStreamWriter](https://developer.android.com/reference/kotlin/java/io/OutputStreamWriter) |-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Writer](https://developer.android.com/reference/kotlin/java/io/Writer) | [append](https://developer.android.com/reference/kotlin/java/io/OutputStreamWriter#append(kotlin.CharSequence))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` <br /> | | [Writer](https://developer.android.com/reference/kotlin/java/io/Writer) | [append](https://developer.android.com/reference/kotlin/java/io/OutputStreamWriter#append(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/io/OutputStreamWriter#close())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](https://developer.android.com/reference/kotlin/java/io/OutputStreamWriter#flush())`()` <br /> Flushes the stream. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEncoding](https://developer.android.com/reference/kotlin/java/io/OutputStreamWriter#getEncoding())`()` <br /> Returns the name of the character encoding being used by this stream. If the encoding has an historical name then that name is returned; otherwise the encoding's canonical name is returned. If this instance was created with the [OutputStreamWriter(java.io.OutputStream,java.lang.String)](https://developer.android.com/reference/kotlin/java/io/OutputStreamWriter#OutputStreamWriter(java.io.OutputStream,%20kotlin.String))constructor then the returned name, being unique for the encoding, may differ from the name passed to the constructor. This method may return`null`if the stream has been closed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/OutputStreamWriter#write(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Writes a portion of an array of characters. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/OutputStreamWriter#write(kotlin.Int))`(`c:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Writes a single character. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/OutputStreamWriter#write(kotlin.String,%20kotlin.Int,%20kotlin.Int))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Writes a portion of a string. <br /> | ||
| From class [Writer](https://developer.android.com/reference/kotlin/java/io/Writer) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Writer](https://developer.android.com/reference/kotlin/java/io/Writer) | [append](https://developer.android.com/reference/kotlin/java/io/Writer#append(kotlin.Char))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` <br /> Appends the specified character to this writer. An invocation of this method of the form`out.append(c)`behaves in exactly the same way as the invocation ```kotlin out.write(c) ``` <br /> | | [Writer](https://developer.android.com/reference/kotlin/java/io/Writer)! | [nullWriter](https://developer.android.com/reference/kotlin/java/io/Writer#nullWriter())`()` <br /> Returns a new`Writer`which discards all characters. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`append(char)`,`append(CharSequence)`,`append(CharSequence, int, int)`,`flush()`,`write(int)`,`write(char[])`, and`write(char[], int, int)`methods do nothing. After the stream has been closed, these methods all throw`IOException`. The [object](https://developer.android.com/reference/kotlin/java/io/Writer#lock:kotlin.Any) used to synchronize operations on the returned`Writer`is not specified. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/Writer#write(kotlin.CharArray))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` <br /> Writes an array of characters. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/Writer#write(kotlin.String))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Writes a string. <br /> | ||

| Inherited properties ||
|---|---|
| From class [Writer](https://developer.android.com/reference/kotlin/java/io/Writer) |-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [lock](https://developer.android.com/reference/kotlin/java/io/Writer#lock:kotlin.Any) <br /> The object used to synchronize operations on this stream. For efficiency, a character-stream object may use an object other than itself to protect critical sections. A subclass should therefore use the object in this field rather than`this`or a synchronized method. <br /> | ||

## Public constructors

### FileWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileWriter(file: File!)
```

Constructs a`FileWriter`given the`File`to write, using the platform's [default charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset())

| Parameters ||
|--------|-----------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File)!:the`File`to write. |

| Exceptions ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if the file exists but is a directory rather than a regular file, does not exist but cannot be created, or cannot be opened for any other reason |

### FileWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileWriter(
    file: File!, 
    append: Boolean)
```

Constructs a`FileWriter`given the`File`to write and a boolean indicating whether to append the data written, using the platform's [default charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset()).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File)!:the`File`to write |
| `append` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`, then bytes will be written to the end of the file rather than the beginning |

| Exceptions ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if the file exists but is a directory rather than a regular file, does not exist but cannot be created, or cannot be opened for any other reason |

### FileWriter

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileWriter(
    file: File!, 
    charset: Charset!)
```

Constructs a`FileWriter`given the`File`to write and [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#).

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File)!:the`File`to write |
| `charset` | [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!:the [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) |

| Exceptions ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if the file exists but is a directory rather than a regular file, does not exist but cannot be created, or cannot be opened for any other reason |

### FileWriter

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileWriter(
    file: File!, 
    charset: Charset!, 
    append: Boolean)
```

Constructs a`FileWriter`given the`File`to write, [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) and a boolean indicating whether to append the data written.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File)!:the`File`to write |
| `charset` | [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!:the [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) |
| `append` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):a boolean. If`true`, the writer will write the data to the end of the file rather than the beginning. |
| --- | --- |

| Exceptions ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if the file exists but is a directory rather than a regular file, does not exist but cannot be created, or cannot be opened for any other reason |

### FileWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileWriter(fd: FileDescriptor!)
```

Constructs a`FileWriter`given a file descriptor, using the platform's [default charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset()).

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor)!:the`FileDescriptor`to write. |

### FileWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileWriter(fileName: String!)
```

Constructs a`FileWriter`given a file name, using the platform's [default charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset())

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:String The system-dependent filename. |

| Exceptions ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if the named file exists but is a directory rather than a regular file, does not exist but cannot be created, or cannot be opened for any other reason |

### FileWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileWriter(
    fileName: String!, 
    append: Boolean)
```

Constructs a`FileWriter`given a file name and a boolean indicating whether to append the data written, using the platform's [default charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset()).

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:String The system-dependent filename. |
| `append` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):boolean if`true`, then data will be written to the end of the file rather than the beginning. |

| Exceptions ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if the named file exists but is a directory rather than a regular file, does not exist but cannot be created, or cannot be opened for any other reason |

### FileWriter

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileWriter(
    fileName: String!, 
    charset: Charset!)
```

Constructs a`FileWriter`given a file name and [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#).

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the file to write |
| `charset` | [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!:the [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) |

| Exceptions ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if the named file exists but is a directory rather than a regular file, does not exist but cannot be created, or cannot be opened for any other reason |

### FileWriter

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileWriter(
    fileName: String!, 
    charset: Charset!, 
    append: Boolean)
```

Constructs a`FileWriter`given a file name, [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) and a boolean indicating whether to append the data written.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the file to write |
| `charset` | [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!:the [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) |
| `append` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):a boolean. If`true`, the writer will write the data to the end of the file rather than the beginning. |
| --- | --- |

| Exceptions ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if the named file exists but is a directory rather than a regular file, does not exist but cannot be created, or cannot be opened for any other reason |
