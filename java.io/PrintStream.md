# PrintStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrintStream

```
open class PrintStream : FilterOutputStream, Appendable, Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [java.io.OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream) |||
| | ↳ | [java.io.FilterOutputStream](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream) ||
| | | ↳ | [java.io.PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#) |

A`PrintStream`adds functionality to another output stream, namely the ability to print representations of various data values conveniently. Two other features are provided as well. Unlike other output streams, a`PrintStream`never throws an`IOException`; instead, exceptional situations merely set an internal flag that can be tested via the`checkError`method. Optionally, a`PrintStream`can be created so as to flush automatically; this means that the`flush`method of the underlying output stream is automatically invoked after a byte array is written, one of the`println`methods is invoked, or a newline character or byte (`'\n'`) is written.

All characters printed by a`PrintStream`are converted into bytes using the given encoding or charset, or the platform's default character encoding if not specified. The [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter) class should be used in situations that require writing characters rather than bytes.

This class always replaces malformed and unmappable character sequences with the charset's default replacement string. The [java.nio.charset.CharsetEncoder](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder.html#) class should be used when more control over the encoding process is required.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#PrintStream(java.io.File))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File)!`)` Creates a new print stream, without automatic line flushing, with the specified file. |
| [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#PrintStream(java.io.File,%20kotlin.String))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File)!`, `csn:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new print stream, without automatic line flushing, with the specified file and charset. |
| [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#PrintStream(java.io.File,%20java.nio.charset.Charset))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File)!`, `charset:` ` [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!`)` Creates a new print stream, without automatic line flushing, with the specified file and charset. |
| [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#PrintStream(java.io.OutputStream))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream)!`)` Creates a new print stream, without automatic line flushing, with the specified OutputStream. |
| [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#PrintStream(java.io.OutputStream,%20kotlin.Boolean))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream)!`, `autoFlush:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new print stream, with the specified OutputStream and line flushing. |
| [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#PrintStream(java.io.OutputStream,%20kotlin.Boolean,%20kotlin.String))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream)!`, `autoFlush:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `encoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new print stream, with the specified OutputStream, line flushing, and character encoding. |
| [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#PrintStream(java.io.OutputStream,%20kotlin.Boolean,%20java.nio.charset.Charset))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream)!`, `autoFlush:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `charset:` ` [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!`)` Creates a new print stream, with the specified OutputStream, line flushing and charset. |
| [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#PrintStream(kotlin.String))`(`fileName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new print stream, without automatic line flushing, with the specified file name. |
| [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#PrintStream(kotlin.String,%20kotlin.String))`(`fileName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `csn:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new print stream, without automatic line flushing, with the specified file name and charset. |
| [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#PrintStream(kotlin.String,%20java.nio.charset.Charset))`(`fileName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `charset:` ` [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!`)` Creates a new print stream, without automatic line flushing, with the specified file name and charset. |

| Public methods ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#) | [append](https://developer.android.com/reference/kotlin/java/io/PrintStream#append(kotlin.Char))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Appends the specified character to this output stream. |
| open [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#) | [append](https://developer.android.com/reference/kotlin/java/io/PrintStream#append(kotlin.CharSequence))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Appends the specified character sequence to this output stream. |
| open [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#) | [append](https://developer.android.com/reference/kotlin/java/io/PrintStream#append(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Appends a subsequence of the specified character sequence to this output stream. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [checkError](https://developer.android.com/reference/kotlin/java/io/PrintStream#checkError())`()` Flushes the stream and checks its error state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/io/PrintStream#close())`()` Closes the stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](https://developer.android.com/reference/kotlin/java/io/PrintStream#flush())`()` Flushes the stream. |
| open [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#)! | [format](https://developer.android.com/reference/kotlin/java/io/PrintStream#format(kotlin.String,%20kotlin.Any))`(`format:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Writes a formatted string to this output stream using the specified format string and arguments. |
| open [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#)! | [format](https://developer.android.com/reference/kotlin/java/io/PrintStream#format(java.util.Locale,%20kotlin.String,%20kotlin.Any))`(`l:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`, `format:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Writes a formatted string to this output stream using the specified format string and arguments. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [print](https://developer.android.com/reference/kotlin/java/io/PrintStream#print(kotlin.Boolean))`(`b:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Prints a boolean value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [print](https://developer.android.com/reference/kotlin/java/io/PrintStream#print(kotlin.Char))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Prints a character. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [print](https://developer.android.com/reference/kotlin/java/io/PrintStream#print(kotlin.CharArray))`(`s:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` Prints an array of characters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [print](https://developer.android.com/reference/kotlin/java/io/PrintStream#print(kotlin.Double))`(`d:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Prints a double-precision floating-point number. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [print](https://developer.android.com/reference/kotlin/java/io/PrintStream#print(kotlin.Float))`(`f:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Prints a floating-point number. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [print](https://developer.android.com/reference/kotlin/java/io/PrintStream#print(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Prints an integer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [print](https://developer.android.com/reference/kotlin/java/io/PrintStream#print(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Prints an object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [print](https://developer.android.com/reference/kotlin/java/io/PrintStream#print(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Prints a string. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [print](https://developer.android.com/reference/kotlin/java/io/PrintStream#print(kotlin.Long))`(`l:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Prints a long integer. |
| open [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#)! | [printf](https://developer.android.com/reference/kotlin/java/io/PrintStream#printf(kotlin.String,%20kotlin.Any))`(`format:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` A convenience method to write a formatted string to this output stream using the specified format string and arguments. |
| open [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#)! | [printf](https://developer.android.com/reference/kotlin/java/io/PrintStream#printf(java.util.Locale,%20kotlin.String,%20kotlin.Any))`(`l:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`, `format:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` A convenience method to write a formatted string to this output stream using the specified format string and arguments. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [println](https://developer.android.com/reference/kotlin/java/io/PrintStream#println())`()` Terminates the current line by writing the line separator string. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [println](https://developer.android.com/reference/kotlin/java/io/PrintStream#println(kotlin.Boolean))`(`x:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Prints a boolean and then terminate the line. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [println](https://developer.android.com/reference/kotlin/java/io/PrintStream#println(kotlin.Char))`(`x:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Prints a character and then terminate the line. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [println](https://developer.android.com/reference/kotlin/java/io/PrintStream#println(kotlin.CharArray))`(`x:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` Prints an array of characters and then terminate the line. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [println](https://developer.android.com/reference/kotlin/java/io/PrintStream#println(kotlin.Double))`(`x:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Prints a double and then terminate the line. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [println](https://developer.android.com/reference/kotlin/java/io/PrintStream#println(kotlin.Float))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Prints a float and then terminate the line. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [println](https://developer.android.com/reference/kotlin/java/io/PrintStream#println(kotlin.Int))`(`x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Prints an integer and then terminate the line. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [println](https://developer.android.com/reference/kotlin/java/io/PrintStream#println(kotlin.Any))`(`x:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Prints an Object and then terminate the line. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [println](https://developer.android.com/reference/kotlin/java/io/PrintStream#println(kotlin.String))`(`x:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Prints a String and then terminate the line. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [println](https://developer.android.com/reference/kotlin/java/io/PrintStream#println(kotlin.Long))`(`x:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Prints a long and then terminate the line. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/PrintStream#write(kotlin.ByteArray))`(`buf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Writes all bytes from the specified byte array to this stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/PrintStream#write(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`buf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes`len`bytes from the specified byte array starting at offset`off`to this stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/PrintStream#write(kotlin.Int))`(`b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes the specified byte to this stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeBytes](https://developer.android.com/reference/kotlin/java/io/PrintStream#writeBytes(kotlin.ByteArray))`(`buf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Writes all bytes from the specified byte array to this stream. |

| Protected methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearError](https://developer.android.com/reference/kotlin/java/io/PrintStream#clearError())`()` Clears the internal error state of this stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setError](https://developer.android.com/reference/kotlin/java/io/PrintStream#setError())`()` Sets the error state of the stream to`true`. |

| Inherited functions ||
|---|---|
| From class [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream) |--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream)! | [nullOutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream#nullOutputStream())`()` <br /> Returns a new`OutputStream`which discards all bytes. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`write(int)`,`write(byte[])`, and`write(byte[], int, int)`methods do nothing. After the stream has been closed, these methods all throw`IOException`. The`flush()`method does nothing. <br /> | ||

| Inherited properties ||
|---|---|
| From class [FilterOutputStream](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream) |--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream)! | [out](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream#out:java.io.OutputStream) <br /> The underlying output stream to be filtered. <br /> | ||

## Public constructors

### PrintStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PrintStream(file: File!)
```

Creates a new print stream, without automatic line flushing, with the specified file. This convenience constructor creates the necessary intermediate [OutputStreamWriter](https://developer.android.com/reference/kotlin/java/io/OutputStreamWriter), which will encode characters using the [default charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset())for this instance of the Java virtual machine.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File)!:The file to use as the destination of this print stream. If the file exists, then it will be truncated to zero size; otherwise, a new file will be created. The output will be written to the file and is buffered. |

| Exceptions ||
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | If the given file object does not denote an existing, writable regular file and a new regular file of that name cannot be created, or if some other error occurs while opening or creating the file |
| `java.lang.SecurityException` | If a security manager is present and java.lang.SecurityManager#checkWrite denies write access to the file |

### PrintStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PrintStream(
    file: File!, 
    csn: String!)
```

Creates a new print stream, without automatic line flushing, with the specified file and charset. This convenience constructor creates the necessary intermediate [OutputStreamWriter](https://developer.android.com/reference/kotlin/java/io/OutputStreamWriter), which will encode characters using the provided charset.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File)!:The file to use as the destination of this print stream. If the file exists, then it will be truncated to zero size; otherwise, a new file will be created. The output will be written to the file and is buffered. |
| `csn` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of a supported [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) |

| Exceptions ||
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | If the given file object does not denote an existing, writable regular file and a new regular file of that name cannot be created, or if some other error occurs while opening or creating the file |
| `java.lang.SecurityException` | If a security manager is present and java.lang.SecurityManager#checkWrite denies write access to the file |
| `java.io.UnsupportedEncodingException` | If the named charset is not supported |

### PrintStream

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PrintStream(
    file: File!, 
    charset: Charset!)
```

Creates a new print stream, without automatic line flushing, with the specified file and charset. This convenience constructor creates the necessary intermediate [OutputStreamWriter](https://developer.android.com/reference/kotlin/java/io/OutputStreamWriter), which will encode characters using the provided charset.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File)!:The file to use as the destination of this print stream. If the file exists, then it will be truncated to zero size; otherwise, a new file will be created. The output will be written to the file and is buffered. |
| `charset` | [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!:A [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs while opening or creating the file |
| `java.lang.SecurityException` | If a security manager is present and java.lang.SecurityManager#checkWrite denies write access to the file |

### PrintStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PrintStream(out: OutputStream!)
```

Creates a new print stream, without automatic line flushing, with the specified OutputStream. Characters written to the stream are converted to bytes using the platform's default character encoding.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream)!:The output stream to which values and objects will be printed |

**See Also**

- [java.io.PrintWriter#PrintWriter(java.io.OutputStream)](https://developer.android.com/reference/kotlin/java/io/PrintWriter#PrintWriter(java.io.OutputStream)) 

### PrintStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PrintStream(
    out: OutputStream!, 
    autoFlush: Boolean)
```

Creates a new print stream, with the specified OutputStream and line flushing. Characters written to the stream are converted to bytes using the platform's default character encoding.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream)!:The output stream to which values and objects will be printed |
| `autoFlush` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the output buffer will be flushed whenever a byte array is written, one of the`println`methods is invoked, or a newline character or byte (`'\n'`) is written |

**See Also**

- [java.io.PrintWriter#PrintWriter(java.io.OutputStream, boolean)](https://developer.android.com/reference/kotlin/java/io/PrintWriter#PrintWriter(java.io.OutputStream,%20kotlin.Boolean)) 

### PrintStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PrintStream(
    out: OutputStream!, 
    autoFlush: Boolean, 
    encoding: String!)
```

Creates a new print stream, with the specified OutputStream, line flushing, and character encoding.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream)!:The output stream to which values and objects will be printed |
| `autoFlush` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the output buffer will be flushed whenever a byte array is written, one of the`println`methods is invoked, or a newline character or byte (`'\n'`) is written |
| `encoding` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of a supported [character encoding](https://developer.android.com/reference/kotlin/java/lang/package-summary.html#charenc) |

| Exceptions ||
|----------------------------------------|----------------------------------------|
| `java.io.UnsupportedEncodingException` | If the named encoding is not supported |

### PrintStream

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PrintStream(
    out: OutputStream!, 
    autoFlush: Boolean, 
    charset: Charset!)
```

Creates a new print stream, with the specified OutputStream, line flushing and charset. This convenience constructor creates the necessary intermediate [OutputStreamWriter](https://developer.android.com/reference/kotlin/java/io/OutputStreamWriter), which will encode characters using the provided charset.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream)!:The output stream to which values and objects will be printed |
| `autoFlush` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the output buffer will be flushed whenever a byte array is written, one of the`println`methods is invoked, or a newline character or byte (`'\n'`) is written |
| `charset` | [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!:A [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) |

### PrintStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PrintStream(fileName: String!)
```

Creates a new print stream, without automatic line flushing, with the specified file name. This convenience constructor creates the necessary intermediate [OutputStreamWriter](https://developer.android.com/reference/kotlin/java/io/OutputStreamWriter), which will encode characters using the [default charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset())for this instance of the Java virtual machine.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the file to use as the destination of this print stream. If the file exists, then it will be truncated to zero size; otherwise, a new file will be created. The output will be written to the file and is buffered. |

| Exceptions ||
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | If the given file object does not denote an existing, writable regular file and a new regular file of that name cannot be created, or if some other error occurs while opening or creating the file |
| `java.lang.SecurityException` | If a security manager is present and java.lang.SecurityManager#checkWrite denies write access to the file |

### PrintStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PrintStream(
    fileName: String!, 
    csn: String!)
```

Creates a new print stream, without automatic line flushing, with the specified file name and charset. This convenience constructor creates the necessary intermediate [OutputStreamWriter](https://developer.android.com/reference/kotlin/java/io/OutputStreamWriter), which will encode characters using the provided charset.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the file to use as the destination of this print stream. If the file exists, then it will be truncated to zero size; otherwise, a new file will be created. The output will be written to the file and is buffered. |
| `csn` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of a supported [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) |

| Exceptions ||
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | If the given file object does not denote an existing, writable regular file and a new regular file of that name cannot be created, or if some other error occurs while opening or creating the file |
| `java.lang.SecurityException` | If a security manager is present and java.lang.SecurityManager#checkWrite denies write access to the file |
| `java.io.UnsupportedEncodingException` | If the named charset is not supported |

### PrintStream

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PrintStream(
    fileName: String!, 
    charset: Charset!)
```

Creates a new print stream, without automatic line flushing, with the specified file name and charset. This convenience constructor creates the necessary intermediate [OutputStreamWriter](https://developer.android.com/reference/kotlin/java/io/OutputStreamWriter), which will encode characters using the provided charset.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the file to use as the destination of this print stream. If the file exists, then it will be truncated to zero size; otherwise, a new file will be created. The output will be written to the file and is buffered. |
| `charset` | [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!:A [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs while opening or creating the file |
| `java.lang.SecurityException` | If a security manager is present and java.lang.SecurityManager#checkWrite denies write access to the file |

## Public methods

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun append(c: Char): PrintStream
```

Appends the specified character to this output stream.

An invocation of this method of the form`out.append(c)`behaves in exactly the same way as the invocation 

```kotlin
<code>out.print(c)
  </code>
```

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------|
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The 16-bit character to append |

| Return ||
|------------------------------------------------------------------------------------|--------------------|
| [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#) | This output stream |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun append(csq: CharSequence?): PrintStream
```

Appends the specified character sequence to this output stream.

An invocation of this method of the form`out.append(csq)`behaves in exactly the same way as the invocation 

```kotlin
<code>out.print(csq.toString())
  </code>
```

Depending on the specification of`toString`for the character sequence`csq`, the entire sequence may not be appended. For instance, invoking then`toString`method of a character buffer will return a subsequence whose content depends upon the buffer's position and limit.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `csq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:The character sequence to append. If`csq`is`null`, then the four characters`"null"`are appended to this output stream. |

| Return ||
|------------------------------------------------------------------------------------|--------------------|
| [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#) | This output stream |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun append(
    csq: CharSequence?, 
    start: Int, 
    end: Int
): PrintStream
```

Appends a subsequence of the specified character sequence to this output stream.

An invocation of this method of the form`out.append(csq, start, end)`when`csq`is not`null`, behaves in exactly the same way as the invocation 

```kotlin
<code>out.print(csq.subSequence(start, end).toString())
  </code>
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `csq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:The character sequence from which a subsequence will be appended. If`csq`is`null`, then characters will be appended as if`csq`contained the four characters`"null"`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the first character in the subsequence |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the character following the last character in the subsequence |

| Return ||
|------------------------------------------------------------------------------------|--------------------|
| [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#) | This output stream |

| Exceptions ||
|---------------------------------------|------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`start`or`end`are negative,`start`is greater than`end`, or`end`is greater than`csq.length()` |
| `java.io.IOException` | If an I/O error occurs |

### checkError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun checkError(): Boolean
```

Flushes the stream and checks its error state. The internal error state is set to`true`when the underlying output stream throws an`IOException`other than`InterruptedIOException`, and when the`setError`method is invoked. If an operation on the underlying output stream throws an`InterruptedIOException`, then the`PrintStream`converts the exception back into an interrupt by doing: 

```kotlin
<code>Thread.currentThread().interrupt();
  </code>
```
or the equivalent.

<br />

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if and only if this stream has encountered an`IOException`other than`InterruptedIOException`, or the`setError`method has been invoked |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes the stream. This is done by flushing the stream and then closing the underlying output stream.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

**See Also**

### flush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun flush(): Unit
```

Flushes the stream. This is done by writing any buffered output bytes to the underlying output stream and then flushing that stream.

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- [java.io.OutputStream#flush()](https://developer.android.com/reference/kotlin/java/io/OutputStream#flush()) 

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun format(
    format: String!, 
    vararg args: Any!
): PrintStream!
```

Writes a formatted string to this output stream using the specified format string and arguments.

The locale always used is the one returned by [java.util.Locale#getDefault(Locale.Category)](https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault(java.util.Locale.Category))with [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) category specified, regardless of any previous invocations of other formatting methods on this object.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A format string as described in [Format string syntax](https://developer.android.com/reference/kotlin/java/util/Formatter.html#syntax) |
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:Arguments referenced by the format specifiers in the format string. If there are more arguments than format specifiers, the extra arguments are ignored. The number of arguments is variable and may be zero. The maximum number of arguments is limited by the maximum dimension of a Java array as defined by The Java Virtual Machine Specification. The behaviour on a`null`argument depends on the [conversion](https://developer.android.com/reference/kotlin/java/util/Formatter.html#syntax). |

| Return ||
|-------------------------------------------------------------------------------------|--------------------|
| [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#)! | This output stream |

| Exceptions ||
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.IllegalFormatException` | If a format string contains an illegal syntax, a format specifier that is incompatible with the given arguments, insufficient arguments given the format string, or other illegal conditions. For specification of all possible formatting errors, see the [Details](https://developer.android.com/reference/kotlin/java/util/Formatter.html#detail) section of the formatter class specification. |
| `java.lang.NullPointerException` | If the`format`is`null` |

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun format(
    l: Locale!, 
    format: String!, 
    vararg args: Any!
): PrintStream!
```

Writes a formatted string to this output stream using the specified format string and arguments.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `l` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:The [locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) to apply during formatting. If`l`is`null`then no localization is applied. |
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A format string as described in [Format string syntax](https://developer.android.com/reference/kotlin/java/util/Formatter.html#syntax) |
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:Arguments referenced by the format specifiers in the format string. If there are more arguments than format specifiers, the extra arguments are ignored. The number of arguments is variable and may be zero. The maximum number of arguments is limited by the maximum dimension of a Java array as defined by The Java Virtual Machine Specification. The behaviour on a`null`argument depends on the [conversion](https://developer.android.com/reference/kotlin/java/util/Formatter.html#syntax). |

| Return ||
|-------------------------------------------------------------------------------------|--------------------|
| [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#)! | This output stream |

| Exceptions ||
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.IllegalFormatException` | If a format string contains an illegal syntax, a format specifier that is incompatible with the given arguments, insufficient arguments given the format string, or other illegal conditions. For specification of all possible formatting errors, see the [Details](https://developer.android.com/reference/kotlin/java/util/Formatter.html#detail) section of the formatter class specification. |
| `java.lang.NullPointerException` | If the`format`is`null` |

### print

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun print(b: Boolean): Unit
```

Prints a boolean value. The string produced by [java.lang.String#valueOf(boolean)](https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Boolean))is translated into bytes according to the platform's default character encoding, and these bytes are written in exactly the manner of the #write(int) method.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------|
| `b` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):The`boolean`to be printed |

### print

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun print(c: Char): Unit
```

Prints a character. The character is translated into one or more bytes according to the character encoding given to the constructor, or the platform's default character encoding if none specified. These bytes are written in exactly the manner of the #write(int) method.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------|
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The`char`to be printed |

### print

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun print(s: CharArray!): Unit
```

Prints an array of characters. The characters are converted into bytes according to the character encoding given to the constructor, or the platform's default character encoding if none specified. These bytes are written in exactly the manner of the #write(int) method.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------|
| `s` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:The array of chars to be printed |

| Exceptions ||
|----------------------------------|---------------|
| `java.lang.NullPointerException` | If`s`is`null` |

### print

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun print(d: Double): Unit
```

Prints a double-precision floating-point number. The string produced by [java.lang.String#valueOf(double)](https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Double))is translated into bytes according to the platform's default character encoding, and these bytes are written in exactly the manner of the #write(int) method.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------|
| `d` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):The`double`to be printed |

**See Also**

- [java.lang.Double#toString(double)](https://developer.android.com/reference/kotlin/java/lang/Double.html#toString(kotlin.Double)) 

### print

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun print(f: Float): Unit
```

Prints a floating-point number. The string produced by [java.lang.String#valueOf(float)](https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Float))is translated into bytes according to the platform's default character encoding, and these bytes are written in exactly the manner of the #write(int) method.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------|
| `f` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The`float`to be printed |

**See Also**

- [java.lang.Float#toString(float)](https://developer.android.com/reference/kotlin/java/lang/Float.html#toString(kotlin.Float)) 

### print

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun print(i: Int): Unit
```

Prints an integer. The string produced by [java.lang.String#valueOf(int)](https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Int))is translated into bytes according to the platform's default character encoding, and these bytes are written in exactly the manner of the #write(int) method.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The`int`to be printed |

**See Also**

- [java.lang.Integer#toString(int)](https://developer.android.com/reference/kotlin/java/lang/Integer.html#toString(kotlin.Int)) 

### print

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun print(obj: Any!): Unit
```

Prints an object. The string produced by the [java.lang.String#valueOf(Object)](https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Any))method is translated into bytes according to the platform's default character encoding, and these bytes are written in exactly the manner of the #write(int) method.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The`Object`to be printed |

**See Also**

- [java.lang.Object#toString()](https://developer.android.com/reference/kotlin/java/lang/Object.html#toString()) 

### print

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun print(s: String!): Unit
```

Prints a string. If the argument is`null`then the string`"null"`is printed. Otherwise, the string's characters are converted into bytes according to the character encoding given to the constructor, or the platform's default character encoding if none specified. These bytes are written in exactly the manner of the #write(int) method.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The`String`to be printed |

### print

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun print(l: Long): Unit
```

Prints a long integer. The string produced by [java.lang.String#valueOf(long)](https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Long))is translated into bytes according to the platform's default character encoding, and these bytes are written in exactly the manner of the #write(int) method.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------|
| `l` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The`long`to be printed |

**See Also**

- [java.lang.Long#toString(long)](https://developer.android.com/reference/kotlin/java/lang/Long.html#toString(kotlin.Long)) 

### printf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun printf(
    format: String!, 
    vararg args: Any!
): PrintStream!
```

A convenience method to write a formatted string to this output stream using the specified format string and arguments.

An invocation of this method of the form`out.printf(format, args)`behaves in exactly the same way as the invocation 

```kotlin
<code>out.format(format, args)
  </code>
```

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A format string as described in [Format string syntax](https://developer.android.com/reference/kotlin/java/util/Formatter.html#syntax) |
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:Arguments referenced by the format specifiers in the format string. If there are more arguments than format specifiers, the extra arguments are ignored. The number of arguments is variable and may be zero. The maximum number of arguments is limited by the maximum dimension of a Java array as defined by The Java Virtual Machine Specification. The behaviour on a`null`argument depends on the [conversion](https://developer.android.com/reference/kotlin/java/util/Formatter.html#syntax). |

| Return ||
|-------------------------------------------------------------------------------------|--------------------|
| [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#)! | This output stream |

| Exceptions ||
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.IllegalFormatException` | If a format string contains an illegal syntax, a format specifier that is incompatible with the given arguments, insufficient arguments given the format string, or other illegal conditions. For specification of all possible formatting errors, see the [Details](https://developer.android.com/reference/kotlin/java/util/Formatter.html#detail) section of the formatter class specification. |
| `java.lang.NullPointerException` | If the`format`is`null` |

### printf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun printf(
    l: Locale!, 
    format: String!, 
    vararg args: Any!
): PrintStream!
```

A convenience method to write a formatted string to this output stream using the specified format string and arguments.

An invocation of this method of the form`out.printf(l, format, args)`behaves in exactly the same way as the invocation 

```kotlin
<code>out.format(l, format, args)
  </code>
```

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `l` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:The [locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) to apply during formatting. If`l`is`null`then no localization is applied. |
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A format string as described in [Format string syntax](https://developer.android.com/reference/kotlin/java/util/Formatter.html#syntax) |
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:Arguments referenced by the format specifiers in the format string. If there are more arguments than format specifiers, the extra arguments are ignored. The number of arguments is variable and may be zero. The maximum number of arguments is limited by the maximum dimension of a Java array as defined by The Java Virtual Machine Specification. The behaviour on a`null`argument depends on the [conversion](https://developer.android.com/reference/kotlin/java/util/Formatter.html#syntax). |

| Return ||
|-------------------------------------------------------------------------------------|--------------------|
| [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream#)! | This output stream |

| Exceptions ||
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.IllegalFormatException` | If a format string contains an illegal syntax, a format specifier that is incompatible with the given arguments, insufficient arguments given the format string, or other illegal conditions. For specification of all possible formatting errors, see the [Details](https://developer.android.com/reference/kotlin/java/util/Formatter.html#detail) section of the formatter class specification. |
| `java.lang.NullPointerException` | If the`format`is`null` |

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun println(): Unit
```

Terminates the current line by writing the line separator string. The line separator string is defined by the system property`line.separator`, and is not necessarily a single newline character (`'\n'`). 

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun println(x: Boolean): Unit
```

Prints a boolean and then terminate the line. This method behaves as though it invokes [print(boolean)](https://developer.android.com/reference/kotlin/java/io/PrintStream#print(kotlin.Boolean))and then [println()](https://developer.android.com/reference/kotlin/java/io/PrintStream#println()).

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------|
| `x` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):The`boolean`to be printed |

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun println(x: Char): Unit
```

Prints a character and then terminate the line. This method behaves as though it invokes [print(char)](https://developer.android.com/reference/kotlin/java/io/PrintStream#print(kotlin.Char))and then [println()](https://developer.android.com/reference/kotlin/java/io/PrintStream#println()).

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------|
| `x` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The`char`to be printed. |

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun println(x: CharArray!): Unit
```

Prints an array of characters and then terminate the line. This method behaves as though it invokes[print(char[])](https://developer.android.com/reference/kotlin/java/io/PrintStream#print(kotlin.CharArray))and then [println()](https://developer.android.com/reference/kotlin/java/io/PrintStream#println()).

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------|
| `x` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:an array of chars to print. |

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun println(x: Double): Unit
```

Prints a double and then terminate the line. This method behaves as though it invokes [print(double)](https://developer.android.com/reference/kotlin/java/io/PrintStream#print(kotlin.Double))and then [println()](https://developer.android.com/reference/kotlin/java/io/PrintStream#println()).

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------|
| `x` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):The`double`to be printed. |

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun println(x: Float): Unit
```

Prints a float and then terminate the line. This method behaves as though it invokes [print(float)](https://developer.android.com/reference/kotlin/java/io/PrintStream#print(kotlin.Float))and then [println()](https://developer.android.com/reference/kotlin/java/io/PrintStream#println()).

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The`float`to be printed. |

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun println(x: Int): Unit
```

Prints an integer and then terminate the line. This method behaves as though it invokes [print(int)](https://developer.android.com/reference/kotlin/java/io/PrintStream#print(kotlin.Int))and then [println()](https://developer.android.com/reference/kotlin/java/io/PrintStream#println()).

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The`int`to be printed. |

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun println(x: Any!): Unit
```

Prints an Object and then terminate the line. This method calls at first String.valueOf(x) to get the printed object's string value, then behaves as though it invokes [print(java.lang.String)](https://developer.android.com/reference/kotlin/java/io/PrintStream#print(kotlin.String))and then [println()](https://developer.android.com/reference/kotlin/java/io/PrintStream#println()).

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `x` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The`Object`to be printed. |

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun println(x: String!): Unit
```

Prints a String and then terminate the line. This method behaves as though it invokes [print(java.lang.String)](https://developer.android.com/reference/kotlin/java/io/PrintStream#print(kotlin.String))and then [println()](https://developer.android.com/reference/kotlin/java/io/PrintStream#println()).

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------|
| `x` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The`String`to be printed. |

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun println(x: Long): Unit
```

Prints a long and then terminate the line. This method behaves as though it invokes [print(long)](https://developer.android.com/reference/kotlin/java/io/PrintStream#print(kotlin.Long))and then [println()](https://developer.android.com/reference/kotlin/java/io/PrintStream#println()).

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a The`long`to be printed. |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(buf: ByteArray!): Unit
```

Writes all bytes from the specified byte array to this stream. If automatic flushing is enabled then the`flush`method will be invoked on the underlying output stream.

Note that the bytes will be written as given; to write characters that will be translated according to the platform's default character encoding, use the`print(char[])`or`println(char[])`methods.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `b` | the data to be written. |
| `buf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:A byte array |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | If an I/O error occurs. |

**See Also**

- [#writeBytes(byte[])](https://developer.android.com/reference/kotlin/java/io/PrintStream#writeBytes(kotlin.ByteArray)) 

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(
    buf: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Writes`len`bytes from the specified byte array starting at offset`off`to this stream. If automatic flushing is enabled then the`flush`method will be invoked on the underlying output stream.

Note that the bytes will be written as given; to write characters that will be translated according to the platform's default character encoding, use the`print(char)`or`println(char)`methods.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------|
| `b` | the data. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset from which to start taking bytes |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of bytes to write |
| `buf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:A byte array |

| Exceptions ||
|-----------------------|-------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs. In particular, an`IOException`is thrown if the output stream is closed. |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(b: Int): Unit
```

Writes the specified byte to this stream. If the byte is a newline and automatic flushing is enabled then the`flush`method will be invoked on the underlying output stream.

Note that the byte is written as given; to write a character that will be translated according to the platform's default character encoding, use the`print(char)`or`println(char)`methods.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------|
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The byte to be written |

| Exceptions ||
|-----------------------|-----------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs. In particular, an`IOException`may be thrown if the output stream has been closed. |

**See Also**

- [#print(char)](https://developer.android.com/reference/kotlin/java/io/PrintStream#print(kotlin.Char))
- [#println(char)](https://developer.android.com/reference/kotlin/java/io/PrintStream#println(kotlin.Char)) 

### writeBytes

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeBytes(buf: ByteArray!): Unit
```

Writes all bytes from the specified byte array to this stream. If automatic flushing is enabled then the`flush`method will be invoked.

Note that the bytes will be written as given; to write characters that will be translated according to the platform's default character encoding, use the`print(char[])`or`println(char[])`methods.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `buf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:A byte array |

## Protected methods

### clearError

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun clearError(): Unit
```

Clears the internal error state of this stream.

This method will cause subsequent invocations of [checkError()](https://developer.android.com/reference/kotlin/java/io/PrintStream#checkError())to return`false`until another write operation fails and invokes [setError()](https://developer.android.com/reference/kotlin/java/io/PrintStream#setError()). 

### setError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun setError(): Unit
```

Sets the error state of the stream to`true`.

This method will cause subsequent invocations of [checkError()](https://developer.android.com/reference/kotlin/java/io/PrintStream#checkError())to return`true`until [clearError()](https://developer.android.com/reference/kotlin/java/io/PrintStream#clearError())is invoked.
