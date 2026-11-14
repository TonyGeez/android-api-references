# FileWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileWriter

```
open class FileWriter : OutputStreamWriter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.io.Writer](Writer.md) |||
| | ↳ | [java.io.OutputStreamWriter](OutputStreamWriter.md) ||
| | | ↳ | [java.io.FileWriter](FileWriter.md) |
| --- | --- | --- | --- |

Writes text to character files using a default buffer size. Encoding from characters to bytes uses either a specified [charset](../java.nio.charset/Charset.md) or the platform's [default charset](../java.nio.charset/Charset.md)).

Whether or not a file is available or may be created depends upon the underlying platform. Some platforms, in particular, allow a file to be opened for writing by only one`FileWriter`(or other file-writing object) at a time. In such situations the constructors in this class will fail if the file involved is already open.

The`FileWriter`is meant for writing streams of characters. For writing streams of raw bytes, consider using a`FileOutputStream`.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileWriter](FileWriter.md))`(`file:` ` [File](File.md)!`)` Constructs a`FileWriter`given the`File`to write, using the platform's [default charset](../java.nio.charset/Charset.md)) |
| [FileWriter](FileWriter.md))`(`file:` ` [File](File.md)!`, `append:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Constructs a`FileWriter`given the`File`to write and a boolean indicating whether to append the data written, using the platform's [default charset](../java.nio.charset/Charset.md)). |
| [FileWriter](FileWriter.md))`(`file:` ` [File](File.md)!`, `charset:` ` [Charset](../java.nio.charset/Charset.md)!`)` Constructs a`FileWriter`given the`File`to write and [charset](../java.nio.charset/Charset.md). |
| [FileWriter](FileWriter.md))`(`file:` ` [File](File.md)!`, `charset:` ` [Charset](../java.nio.charset/Charset.md)!`, `append:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Constructs a`FileWriter`given the`File`to write, [charset](../java.nio.charset/Charset.md) and a boolean indicating whether to append the data written. |
| [FileWriter](FileWriter.md))`(`fd:` ` [FileDescriptor](FileDescriptor.md)!`)` Constructs a`FileWriter`given a file descriptor, using the platform's [default charset](../java.nio.charset/Charset.md)). |
| [FileWriter](FileWriter.md))`(`fileName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`FileWriter`given a file name, using the platform's [default charset](../java.nio.charset/Charset.md)) |
| [FileWriter](FileWriter.md))`(`fileName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `append:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Constructs a`FileWriter`given a file name and a boolean indicating whether to append the data written, using the platform's [default charset](../java.nio.charset/Charset.md)). |
| [FileWriter](FileWriter.md))`(`fileName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `charset:` ` [Charset](../java.nio.charset/Charset.md)!`)` Constructs a`FileWriter`given a file name and [charset](../java.nio.charset/Charset.md). |
| [FileWriter](FileWriter.md))`(`fileName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `charset:` ` [Charset](../java.nio.charset/Charset.md)!`, `append:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Constructs a`FileWriter`given a file name, [charset](../java.nio.charset/Charset.md) and a boolean indicating whether to append the data written. |

| Inherited functions ||
|---|---|
| From class [OutputStreamWriter](OutputStreamWriter.md) |-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Writer](Writer.md) | [append](OutputStreamWriter.md))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` <br /> | | [Writer](Writer.md) | [append](OutputStreamWriter.md))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](OutputStreamWriter.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](OutputStreamWriter.md))`()` <br /> Flushes the stream. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEncoding](OutputStreamWriter.md))`()` <br /> Returns the name of the character encoding being used by this stream. If the encoding has an historical name then that name is returned; otherwise the encoding's canonical name is returned. If this instance was created with the [OutputStreamWriter(java.io.OutputStream,java.lang.String)](OutputStreamWriter.md))constructor then the returned name, being unique for the encoding, may differ from the name passed to the constructor. This method may return`null`if the stream has been closed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](OutputStreamWriter.md))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Writes a portion of an array of characters. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](OutputStreamWriter.md))`(`c:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Writes a single character. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](OutputStreamWriter.md))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Writes a portion of a string. <br /> | ||
| From class [Writer](Writer.md) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Writer](Writer.md) | [append](Writer.md))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` <br /> Appends the specified character to this writer. An invocation of this method of the form`out.append(c)`behaves in exactly the same way as the invocation ```kotlin out.write(c) ``` <br /> | | [Writer](Writer.md)! | [nullWriter](Writer.md))`()` <br /> Returns a new`Writer`which discards all characters. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`append(char)`,`append(CharSequence)`,`append(CharSequence, int, int)`,`flush()`,`write(int)`,`write(char[])`, and`write(char[], int, int)`methods do nothing. After the stream has been closed, these methods all throw`IOException`. The [object](Writer.md) used to synchronize operations on the returned`Writer`is not specified. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](Writer.md))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` <br /> Writes an array of characters. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](Writer.md))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Writes a string. <br /> | ||

| Inherited properties ||
|---|---|
| From class [Writer](Writer.md) |-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [lock](Writer.md) <br /> The object used to synchronize operations on this stream. For efficiency, a character-stream object may use an object other than itself to protect critical sections. A subclass should therefore use the object in this field rather than`this`or a synchronized method. <br /> | ||

## Public constructors

### FileWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileWriter(file: File!)
```

Constructs a`FileWriter`given the`File`to write, using the platform's [default charset](../java.nio.charset/Charset.md))

| Parameters ||
|--------|-----------------------------------------------------------------------------------------|
| `file` | [File](File.md)!:the`File`to write. |

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

Constructs a`FileWriter`given the`File`to write and a boolean indicating whether to append the data written, using the platform's [default charset](../java.nio.charset/Charset.md)).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](File.md)!:the`File`to write |
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

Constructs a`FileWriter`given the`File`to write and [charset](../java.nio.charset/Charset.md).

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](File.md)!:the`File`to write |
| `charset` | [Charset](../java.nio.charset/Charset.md)!:the [charset](../java.nio.charset/Charset.md) |

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

Constructs a`FileWriter`given the`File`to write, [charset](../java.nio.charset/Charset.md) and a boolean indicating whether to append the data written.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](File.md)!:the`File`to write |
| `charset` | [Charset](../java.nio.charset/Charset.md)!:the [charset](../java.nio.charset/Charset.md) |
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

Constructs a`FileWriter`given a file descriptor, using the platform's [default charset](../java.nio.charset/Charset.md)).

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](FileDescriptor.md)!:the`FileDescriptor`to write. |

### FileWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileWriter(fileName: String!)
```

Constructs a`FileWriter`given a file name, using the platform's [default charset](../java.nio.charset/Charset.md))

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

Constructs a`FileWriter`given a file name and a boolean indicating whether to append the data written, using the platform's [default charset](../java.nio.charset/Charset.md)).

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

Constructs a`FileWriter`given a file name and [charset](../java.nio.charset/Charset.md).

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the file to write |
| `charset` | [Charset](../java.nio.charset/Charset.md)!:the [charset](../java.nio.charset/Charset.md) |

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

Constructs a`FileWriter`given a file name, [charset](../java.nio.charset/Charset.md) and a boolean indicating whether to append the data written.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the file to write |
| `charset` | [Charset](../java.nio.charset/Charset.md)!:the [charset](../java.nio.charset/Charset.md) |
| `append` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):a boolean. If`true`, the writer will write the data to the end of the file rather than the beginning. |
| --- | --- |

| Exceptions ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if the named file exists but is a directory rather than a regular file, does not exist but cannot be created, or cannot be opened for any other reason |
