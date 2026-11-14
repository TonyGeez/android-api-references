Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrintWriter

```
open class PrintWriter : Writer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.io.Writer](Writer.md) ||
| | ↳ | [java.io.PrintWriter](PrintWriter.md) |

Prints formatted representations of objects to a text-output stream. This class implements all of the `print` methods found in PrintStream. It does not contain methods for writing raw bytes, for which a program should use unencoded byte streams.

Unlike the PrintStream class, if automatic flushing is enabled it will be done only when one of the `println`, `printf`, or `format` methods is invoked, rather than whenever a newline character happens to be output. These methods use the platform's own notion of line separator rather than the newline character.

Methods in this class never throw I/O exceptions, although some of its constructors may. The client may inquire as to whether any errors have occurred by invoking checkError.

This class always replaces malformed and unmappable character sequences with the charset's default replacement string. The [java.nio.charset.CharsetEncoder](../java.nio.charset/CharsetEncoder.md) class should be used when more control over the encoding process is required.

## Summary

| Public constructors ||
|---|---|
| PrintWriter Creates a new PrintWriter, without automatic line flushing, with the specified file. |
| PrintWriter Creates a new PrintWriter, without automatic line flushing, with the specified file and charset. |
| PrintWriter Creates a new PrintWriter, without automatic line flushing, with the specified file and charset. |
| PrintWriter Creates a new PrintWriter, without automatic line flushing, from an existing OutputStream. |
| PrintWriter Creates a new PrintWriter from an existing OutputStream. |
| PrintWriter Creates a new PrintWriter from an existing OutputStream. |
| PrintWriter Creates a new PrintWriter, without automatic line flushing. |
| PrintWriter Creates a new PrintWriter. |
| PrintWriter Creates a new PrintWriter, without automatic line flushing, with the specified file name. |
| PrintWriter Creates a new PrintWriter, without automatic line flushing, with the specified file name and charset. |
| PrintWriter Creates a new PrintWriter, without automatic line flushing, with the specified file name and charset. |

| Public methods ||
|---|---|
| open [PrintWriter](PrintWriter.md) | append Appends the specified character to this writer. |
| open [PrintWriter](PrintWriter.md) | append Appends the specified character sequence to this writer. |
| open [PrintWriter](PrintWriter.md) | append Appends a subsequence of the specified character sequence to this writer. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | checkError Flushes the stream if it's not closed and checks its error state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | close Closes the stream and releases any system resources associated with it. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | flush Flushes the stream. |
| --- | --- |
| open [PrintWriter](PrintWriter.md) | format Writes a formatted string to this writer using the specified format string and arguments. |
| open [PrintWriter](PrintWriter.md) | format Writes a formatted string to this writer using the specified format string and arguments. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | print Prints a boolean value. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | print Prints a character. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | print Prints an array of characters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | print Prints a double-precision floating-point number. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | print Prints a floating-point number. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | print Prints an integer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | print Prints an object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | print Prints a string. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | print Prints a long integer. |
| open [PrintWriter](PrintWriter.md) | printf A convenience method to write a formatted string to this writer using the specified format string and arguments. |
| --- | --- |
| open [PrintWriter](PrintWriter.md) | printf A convenience method to write a formatted string to this writer using the specified format string and arguments. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | println Terminates the current line by writing the line separator string. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | println Prints a boolean value and then terminates the line. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | println Prints a character and then terminates the line. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | println Prints an array of characters and then terminates the line. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | println Prints a double-precision floating-point number and then terminates the line. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | println Prints a floating-point number and then terminates the line. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | println Prints an integer and then terminates the line. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | println Prints an Object and then terminates the line. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | println Prints a String and then terminates the line. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | println Prints a long integer and then terminates the line. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | write Writes an array of characters. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | write Writes A Portion of an array of characters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | write Writes a single character. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | write Writes a string. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | write Writes a portion of a string. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | clearError Clears the error state of this stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setError Indicates that an error has occurred. |

| Inherited functions ||
|---|---|
| From class Writer |---|---| | `https://developer.android.com/reference/kotlin/java/io/Writer!` | nullWriter Returns a new `Writer` which discards all characters. The returned stream is initially open. The stream is closed by calling the `close()` method. Subsequent calls to `close()` have no effect. While the stream is open, the `append(char)`, `append(CharSequence)`, `append(CharSequence, int, int)`, `flush()`, `write(int)`, `write(char[])`, and `write(char[], int, int)` methods do nothing. After the stream has been closed, these methods all throw `IOException`. The `https://developer.android.com/reference/kotlin/java/io/Writer#lock:kotlin.Any` used to synchronize operations on the returned `Writer` is not specified. <br /> | ||

| Properties ||
|---|---|
| [Writer](Writer.md)! | `https://developer.android.com/reference/kotlin/java/io/PrintWriter#out:java.io.Writer` The underlying character-output stream of this `PrintWriter`. |

| Inherited properties ||
|---|---|
| From class Writer |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | `https://developer.android.com/reference/kotlin/java/io/Writer#lock:kotlin.Any` The object used to synchronize operations on this stream. For efficiency, a character-stream object may use an object other than itself to protect critical sections. A subclass should therefore use the object in this field rather than `this` or a synchronized method. <br /> | ||

## Public constructors

### PrintWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PrintWriter(file: File)
```

Creates a new PrintWriter, without automatic line flushing, with the specified file. This convenience constructor creates the necessary intermediate OutputStreamWriter, which will encode characters using the [default charset](../java.nio.charset/Charset.md)) for this instance of the Java virtual machine.

| Parameters ||
|---|---|
| `file` | [File](File.md): The file to use as the destination of this writer. If the file exists then it will be truncated to zero size; otherwise, a new file will be created. The output will be written to the file and is buffered. |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | If the given file object does not denote an existing, writable regular file and a new regular file of that name cannot be created, or if some other error occurs while opening or creating the file |
| `java.lang.SecurityException` | If a security manager is present and java.lang.SecurityManager#checkWrite denies write access to the file |

### PrintWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PrintWriter(
    file: File, 
    csn: String)
```

Creates a new PrintWriter, without automatic line flushing, with the specified file and charset. This convenience constructor creates the necessary intermediate OutputStreamWriter, which will encode characters using the provided charset.

| Parameters ||
|---|---|
| `file` | [File](File.md): The file to use as the destination of this writer. If the file exists then it will be truncated to zero size; otherwise, a new file will be created. The output will be written to the file and is buffered. |
| `csn` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of a supported [charset](../java.nio.charset/Charset.md) |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | If the given file object does not denote an existing, writable regular file and a new regular file of that name cannot be created, or if some other error occurs while opening or creating the file |
| `java.io.UnsupportedEncodingException` | If the named charset is not supported |
| `java.lang.SecurityException` | If a security manager is present and java.lang.SecurityManager#checkWrite denies write access to the file |
| --- | --- |

### PrintWriter

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PrintWriter(
    file: File, 
    charset: Charset)
```

Creates a new PrintWriter, without automatic line flushing, with the specified file and charset. This convenience constructor creates the necessary intermediate OutputStreamWriter, which will encode characters using the provided charset.

| Parameters ||
|---|---|
| `file` | [File](File.md): The file to use as the destination of this writer. If the file exists then it will be truncated to zero size; otherwise, a new file will be created. The output will be written to the file and is buffered. |
| `charset` | [Charset](../java.nio.charset/Charset.md): A [charset](../java.nio.charset/Charset.md) |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs while opening or creating the file |
| `java.lang.SecurityException` | If a security manager is present and java.lang.SecurityManager#checkWrite denies write access to the file |

### PrintWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PrintWriter(out: OutputStream)
```

Creates a new PrintWriter, without automatic line flushing, from an existing OutputStream. This convenience constructor creates the necessary intermediate OutputStreamWriter, which will convert characters into bytes using the default character encoding.

| Parameters ||
|---|---|
| `out` | [OutputStream](OutputStream.md): An output stream |

**See Also**

- OutputStreamWriter

### PrintWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PrintWriter(
    out: OutputStream, 
    autoFlush: Boolean)
```

Creates a new PrintWriter from an existing OutputStream. This convenience constructor creates the necessary intermediate OutputStreamWriter, which will convert characters into bytes using the default character encoding.

| Parameters ||
|---|---|
| `out` | [OutputStream](OutputStream.md): An output stream |
| `autoFlush` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): A boolean; if true, the `println`, `printf`, or `format` methods will flush the output buffer |

**See Also**

- OutputStreamWriter

### PrintWriter

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PrintWriter(
    out: OutputStream, 
    autoFlush: Boolean, 
    charset: Charset)
```

Creates a new PrintWriter from an existing OutputStream. This convenience constructor creates the necessary intermediate OutputStreamWriter, which will convert characters into bytes using the specified charset.

| Parameters ||
|---|---|
| `out` | [OutputStream](OutputStream.md): An output stream |
| `autoFlush` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): A boolean; if true, the `println`, `printf`, or `format` methods will flush the output buffer |
| `charset` | [Charset](../java.nio.charset/Charset.md): A [charset](../java.nio.charset/Charset.md) |
| --- | --- |

### PrintWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PrintWriter(out: Writer)
```

Creates a new PrintWriter, without automatic line flushing.

| Parameters ||
|---|---|
| `out` | [Writer](Writer.md): A character-output stream |

### PrintWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PrintWriter(
    out: Writer, 
    autoFlush: Boolean)
```

Creates a new PrintWriter.

| Parameters ||
|---|---|
| `out` | [Writer](Writer.md): A character-output stream |
| `autoFlush` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): A boolean; if true, the println, printf, or format methods will flush the output buffer |

### PrintWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PrintWriter(fileName: String)
```

Creates a new PrintWriter, without automatic line flushing, with the specified file name. This convenience constructor creates the necessary intermediate OutputStreamWriter, which will encode characters using the [default charset](../java.nio.charset/Charset.md)) for this instance of the Java virtual machine.

| Parameters ||
|---|---|
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the file to use as the destination of this writer. If the file exists then it will be truncated to zero size; otherwise, a new file will be created. The output will be written to the file and is buffered. |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | If the given string does not denote an existing, writable regular file and a new regular file of that name cannot be created, or if some other error occurs while opening or creating the file |
| `java.lang.SecurityException` | If a security manager is present and java.lang.SecurityManager#checkWrite denies write access to the file |

### PrintWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PrintWriter(
    fileName: String, 
    csn: String)
```

Creates a new PrintWriter, without automatic line flushing, with the specified file name and charset. This convenience constructor creates the necessary intermediate OutputStreamWriter, which will encode characters using the provided charset.

| Parameters ||
|---|---|
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the file to use as the destination of this writer. If the file exists then it will be truncated to zero size; otherwise, a new file will be created. The output will be written to the file and is buffered. |
| `csn` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of a supported [charset](../java.nio.charset/Charset.md) |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | If the given string does not denote an existing, writable regular file and a new regular file of that name cannot be created, or if some other error occurs while opening or creating the file |
| `java.io.UnsupportedEncodingException` | If the named charset is not supported |
| `java.lang.SecurityException` | If a security manager is present and java.lang.SecurityManager#checkWrite denies write access to the file |
| --- | --- |

### PrintWriter

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PrintWriter(
    fileName: String, 
    charset: Charset)
```

Creates a new PrintWriter, without automatic line flushing, with the specified file name and charset. This convenience constructor creates the necessary intermediate OutputStreamWriter, which will encode characters using the provided charset.

| Parameters ||
|---|---|
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the file to use as the destination of this writer. If the file exists then it will be truncated to zero size; otherwise, a new file will be created. The output will be written to the file and is buffered. |
| `charset` | [Charset](../java.nio.charset/Charset.md): A [charset](../java.nio.charset/Charset.md) |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs while opening or creating the file |
| `java.lang.SecurityException` | If a security manager is present and java.lang.SecurityManager#checkWrite denies write access to the file |

## Public methods

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun append(c: Char): PrintWriter
```

Appends the specified character to this writer.

An invocation of this method of the form `out.append(c)` behaves in exactly the same way as the invocation

```kotlin
<code>out.write(c)
  </code>
```

| Parameters ||
|---|---|
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): The 16-bit character to append |

| Return ||
|---|---|
| PrintWriter | This writer |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun append(csq: CharSequence?): PrintWriter
```

Appends the specified character sequence to this writer.

An invocation of this method of the form `out.append(csq)` behaves in exactly the same way as the invocation

```kotlin
<code>out.write(csq.toString())
  </code>
```

Depending on the specification of `toString` for the character sequence `csq`, the entire sequence may not be appended. For instance, invoking the `toString` method of a character buffer will return a subsequence whose content depends upon the buffer's position and limit.

| Parameters ||
|---|---|
| `csq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: The character sequence to append. If `csq` is `null`, then the four characters `"null"` are appended to this writer. |

| Return ||
|---|---|
| PrintWriter | This writer |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun append(
    csq: CharSequence?, 
    start: Int, 
    end: Int
): PrintWriter
```

Appends a subsequence of the specified character sequence to this writer.

An invocation of this method of the form `out.append(csq, start, end)` when `csq` is not `null`, behaves in exactly the same way as the invocation

```kotlin
<code>out.write(csq.subSequence(start, end).toString())
  </code>
```

| Parameters ||
|---|---|
| `csq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: The character sequence from which a subsequence will be appended. If `csq` is `null`, then characters will be appended as if `csq` contained the four characters `"null"`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the first character in the subsequence |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the character following the last character in the subsequence |
| --- | --- |

| Return ||
|---|---|
| PrintWriter | This writer |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.IndexOutOfBoundsException` | If `start` or `end` are negative, `start` is greater than `end`, or `end` is greater than `csq.length()` |

### checkError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkError(): Boolean
```

Flushes the stream if it's not closed and checks its error state.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the print stream has encountered an error, either on the underlying output stream or during a format conversion. |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun close(): Unit
```

Closes the stream and releases any system resources associated with it. Closing a previously closed stream has no effect.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | If an I/O error occurs |

**See Also**

- checkError

### flush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun flush(): Unit
```

Flushes the stream.

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |

**See Also**

- checkError

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun format(
    format: String, 
    vararg args: Any!
): PrintWriter
```

Writes a formatted string to this writer using the specified format string and arguments. If automatic flushing is enabled, calls to this method will flush the output buffer.

The locale always used is the one returned by getDefault, regardless of any previous invocations of other formatting methods on this object.

| Parameters ||
|---|---|
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A format string as described in [Format string syntax](../java.util/Formatter.md). |
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: Arguments referenced by the format specifiers in the format string. If there are more arguments than format specifiers, the extra arguments are ignored. The number of arguments is variable and may be zero. The maximum number of arguments is limited by the maximum dimension of a Java array as defined by The Java™ Virtual Machine Specification. The behaviour on a `null` argument depends on the [conversion](../java.util/Formatter.md). |

| Return ||
|---|---|
| PrintWriter | This writer |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | If the `format` is `null` |
| `java.util.IllegalFormatException` | If a format string contains an illegal syntax, a format specifier that is incompatible with the given arguments, insufficient arguments given the format string, or other illegal conditions. For specification of all possible formatting errors, see the [Details](../java.util/Formatter.md) section of the Formatter class specification. |

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun format(
    l: Locale?, 
    format: String, 
    vararg args: Any!
): PrintWriter
```

Writes a formatted string to this writer using the specified format string and arguments. If automatic flushing is enabled, calls to this method will flush the output buffer.

| Parameters ||
|---|---|
| `l` | [Locale](../java.util/Locale.md)?: The [locale](../java.util/Locale.md) to apply during formatting. If `l` is `null` then no localization is applied. |
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A format string as described in [Format string syntax](../java.util/Formatter.md). |
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: Arguments referenced by the format specifiers in the format string. If there are more arguments than format specifiers, the extra arguments are ignored. The number of arguments is variable and may be zero. The maximum number of arguments is limited by the maximum dimension of a Java array as defined by The Java™ Virtual Machine Specification. The behaviour on a `null` argument depends on the [conversion](../java.util/Formatter.md). |
| --- | --- |

| Return ||
|---|---|
| PrintWriter | This writer |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | If the `format` is `null` |
| `java.util.IllegalFormatException` | If a format string contains an illegal syntax, a format specifier that is incompatible with the given arguments, insufficient arguments given the format string, or other illegal conditions. For specification of all possible formatting errors, see the [Details](../java.util/Formatter.md) section of the formatter class specification. |

### print

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun print(b: Boolean): Unit
```

Prints a boolean value. The string produced by valueOf is translated into bytes according to the platform's default character encoding, and these bytes are written in exactly the manner of the write method.

| Parameters ||
|---|---|
| `b` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The `boolean` to be printed |

### print

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun print(c: Char): Unit
```

Prints a character. The character is translated into one or more bytes according to the platform's default character encoding, and these bytes are written in exactly the manner of the write method.

| Parameters ||
|---|---|
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): The `char` to be printed |

### print

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun print(s: CharArray!): Unit
```

Prints an array of characters. The characters are converted into bytes according to the platform's default character encoding, and these bytes are written in exactly the manner of the write method.

| Parameters ||
|---|---|
| `s` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: The array of chars to be printed |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | If `s` is `null` |

### print

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun print(d: Double): Unit
```

Prints a double-precision floating-point number. The string produced by valueOf is translated into bytes according to the platform's default character encoding, and these bytes are written in exactly the manner of the write method.

| Parameters ||
|---|---|
| `d` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The `double` to be printed |

**See Also**

- toString

### print

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun print(f: Float): Unit
```

Prints a floating-point number. The string produced by valueOf is translated into bytes according to the platform's default character encoding, and these bytes are written in exactly the manner of the write method.

| Parameters ||
|---|---|
| `f` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The `float` to be printed |

**See Also**

- toString

### print

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun print(i: Int): Unit
```

Prints an integer. The string produced by valueOf is translated into bytes according to the platform's default character encoding, and these bytes are written in exactly the manner of the write method.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `int` to be printed |

**See Also**

- toString

### print

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun print(obj: Any?): Unit
```

Prints an object. The string produced by the valueOf method is translated into bytes according to the platform's default character encoding, and these bytes are written in exactly the manner of the write method.

| Parameters ||
|---|---|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: The `Object` to be printed |

**See Also**

- toString

### print

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun print(s: String?): Unit
```

Prints a string. If the argument is `null` then the string `"null"` is printed. Otherwise, the string's characters are converted into bytes according to the platform's default character encoding, and these bytes are written in exactly the manner of the write method.

| Parameters ||
|---|---|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The `String` to be printed |

### print

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun print(l: Long): Unit
```

Prints a long integer. The string produced by valueOf is translated into bytes according to the platform's default character encoding, and these bytes are written in exactly the manner of the write method.

| Parameters ||
|---|---|
| `l` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The `long` to be printed |

**See Also**

- toString

### printf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun printf(
    format: String, 
    vararg args: Any!
): PrintWriter
```

A convenience method to write a formatted string to this writer using the specified format string and arguments. If automatic flushing is enabled, calls to this method will flush the output buffer.

An invocation of this method of the form `out.printf(format, args)` behaves in exactly the same way as the invocation

```kotlin
<code>out.format(format, args)
  </code>
```

| Parameters ||
|---|---|
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A format string as described in [Format string syntax](../java.util/Formatter.md). |
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: Arguments referenced by the format specifiers in the format string. If there are more arguments than format specifiers, the extra arguments are ignored. The number of arguments is variable and may be zero. The maximum number of arguments is limited by the maximum dimension of a Java array as defined by The Java™ Virtual Machine Specification. The behaviour on a `null` argument depends on the [conversion](../java.util/Formatter.md). |

| Return ||
|---|---|
| PrintWriter | This writer |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | If the `format` is `null` |
| `java.util.IllegalFormatException` | If a format string contains an illegal syntax, a format specifier that is incompatible with the given arguments, insufficient arguments given the format string, or other illegal conditions. For specification of all possible formatting errors, see the [Details](../java.util/Formatter.md) section of the formatter class specification. |

### printf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun printf(
    l: Locale?, 
    format: String, 
    vararg args: Any!
): PrintWriter
```

A convenience method to write a formatted string to this writer using the specified format string and arguments. If automatic flushing is enabled, calls to this method will flush the output buffer.

An invocation of this method of the form `out.printf(l, format, args)` behaves in exactly the same way as the invocation

```kotlin
<code>out.format(l, format, args)
  </code>
```

| Parameters ||
|---|---|
| `l` | [Locale](../java.util/Locale.md)?: The [locale](../java.util/Locale.md) to apply during formatting. If `l` is `null` then no localization is applied. |
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A format string as described in [Format string syntax](../java.util/Formatter.md). |
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: Arguments referenced by the format specifiers in the format string. If there are more arguments than format specifiers, the extra arguments are ignored. The number of arguments is variable and may be zero. The maximum number of arguments is limited by the maximum dimension of a Java array as defined by The Java™ Virtual Machine Specification. The behaviour on a `null` argument depends on the [conversion](../java.util/Formatter.md). |
| --- | --- |

| Return ||
|---|---|
| PrintWriter | This writer |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | If the `format` is `null` |
| `java.util.IllegalFormatException` | If a format string contains an illegal syntax, a format specifier that is incompatible with the given arguments, insufficient arguments given the format string, or other illegal conditions. For specification of all possible formatting errors, see the [Details](../java.util/Formatter.md) section of the formatter class specification. |

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun println(): Unit
```

Terminates the current line by writing the line separator string. The line separator string is defined by the system property `line.separator`, and is not necessarily a single newline character (`'\n'`).

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun println(x: Boolean): Unit
```

Prints a boolean value and then terminates the line. This method behaves as though it invokes print and then println.

| Parameters ||
|---|---|
| `x` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the `boolean` value to be printed |

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun println(x: Char): Unit
```

Prints a character and then terminates the line. This method behaves as though it invokes print and then println.

| Parameters ||
|---|---|
| `x` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the `char` value to be printed |

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun println(x: CharArray!): Unit
```

Prints an array of characters and then terminates the line. This method behaves as though it invokes print and then println.

| Parameters ||
|---|---|
| `x` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: the array of `char` values to be printed |

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun println(x: Double): Unit
```

Prints a double-precision floating-point number and then terminates the line. This method behaves as though it invokes print and then println.

| Parameters ||
|---|---|
| `x` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the `double` value to be printed |

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun println(x: Float): Unit
```

Prints a floating-point number and then terminates the line. This method behaves as though it invokes print and then println.

| Parameters ||
|---|---|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the `float` value to be printed |

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun println(x: Int): Unit
```

Prints an integer and then terminates the line. This method behaves as though it invokes print and then println.

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the `int` value to be printed |

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun println(x: Any?): Unit
```

Prints an Object and then terminates the line. This method calls at first String.valueOf(x) to get the printed object's string value, then behaves as though it invokes print and then println.

| Parameters ||
|---|---|
| `x` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: The `Object` to be printed. |

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun println(x: String?): Unit
```

Prints a String and then terminates the line. This method behaves as though it invokes print and then println.

| Parameters ||
|---|---|
| `x` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: the `String` value to be printed |

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun println(x: Long): Unit
```

Prints a long integer and then terminates the line. This method behaves as though it invokes print and then println.

| Parameters ||
|---|---|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the `long` value to be printed |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun write(buf: CharArray!): Unit
```

Writes an array of characters. This method cannot be inherited from the Writer class because it must suppress I/O exceptions.

| Parameters ||
|---|---|
| `cbuf` | Array of characters to be written |
| `buf` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: Array of characters to be written |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun write(
    buf: CharArray!, 
    off: Int, 
    len: Int
): Unit
```

Writes A Portion of an array of characters.

| Parameters ||
|---|---|
| `cbuf` | Array of characters |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Offset from which to start writing characters |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of characters to write |
| --- | --- |
| `buf` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: Array of characters |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.IndexOutOfBoundsException` | If the values of the `off` and `len` parameters cause the corresponding method of the underlying `Writer` to throw an `IndexOutOfBoundsException` |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun write(c: Int): Unit
```

Writes a single character.

| Parameters ||
|---|---|
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): int specifying a character to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun write(s: String): Unit
```

Writes a string. This method cannot be inherited from the Writer class because it must suppress I/O exceptions.

| Parameters ||
|---|---|
| `str` | String to be written |
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): String to be written |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun write(
    s: String, 
    off: Int, 
    len: Int
): Unit
```

Writes a portion of a string.

| Parameters ||
|---|---|
| `str` | A String |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Offset from which to start writing characters |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of characters to write |
| --- | --- |
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A String |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.IndexOutOfBoundsException` | If the values of the `off` and `len` parameters cause the corresponding method of the underlying `Writer` to throw an `IndexOutOfBoundsException` |

## Protected methods

### clearError

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun clearError(): Unit
```

Clears the error state of this stream.

This method will cause subsequent invocations of checkError to return `false` until another write operation fails and invokes setError.

### setError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun setError(): Unit
```

Indicates that an error has occurred.

This method will cause subsequent invocations of checkError to return `true` until clearError is invoked.

## Properties

### out

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var out: Writer!
```

The underlying character-output stream of this `PrintWriter`.
