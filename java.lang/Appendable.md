Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Appendable

```
interface Appendable
```

| [java.lang.Appendable](https://developer.android.com/reference/kotlin/java/lang/Appendable#) |

| Known Direct Subclasses [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer.html#), [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#), [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream.html#), [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder.html#), [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer), [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder), [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#) |---|---| | [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer.html#) | A char buffer. | | [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#) | This is the interface for text whose content and markup can be changed (as opposed to immutable text like Strings). | | [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream.html#) | A `PrintStream` adds functionality to another output stream, namely the ability to print representations of various data values conveniently. | | [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder.html#) | This is the class for text whose content and markup can both be changed. | | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer) | A thread-safe, mutable sequence of characters. | | [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder) | A mutable sequence of characters. | | [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#) | Abstract class for writing to character streams. | |

| Known Indirect Subclasses [BufferedWriter](https://developer.android.com/reference/kotlin/java/io/BufferedWriter.html#), [CharArrayWriter](https://developer.android.com/reference/kotlin/java/io/CharArrayWriter.html#), [FileWriter](https://developer.android.com/reference/kotlin/java/io/FileWriter.html#), [FilterWriter](https://developer.android.com/reference/kotlin/java/io/FilterWriter.html#), [OutputStreamWriter](https://developer.android.com/reference/kotlin/java/io/OutputStreamWriter.html#), [PipedWriter](https://developer.android.com/reference/kotlin/java/io/PipedWriter.html#), [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#), [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder.html#), [StringWriter](https://developer.android.com/reference/kotlin/java/io/StringWriter.html#) |---|---| | [BufferedWriter](https://developer.android.com/reference/kotlin/java/io/BufferedWriter.html#) | Writes text to a character-output stream, buffering characters so as to provide for the efficient writing of single characters, arrays, and strings. | | [CharArrayWriter](https://developer.android.com/reference/kotlin/java/io/CharArrayWriter.html#) | This class implements a character buffer that can be used as an Writer. | | [FileWriter](https://developer.android.com/reference/kotlin/java/io/FileWriter.html#) | Writes text to character files using a default buffer size. | | [FilterWriter](https://developer.android.com/reference/kotlin/java/io/FilterWriter.html#) | Abstract class for writing filtered character streams. | | [OutputStreamWriter](https://developer.android.com/reference/kotlin/java/io/OutputStreamWriter.html#) | An OutputStreamWriter is a bridge from character streams to byte streams: Characters written to it are encoded into bytes using a specified `https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#`. | | [PipedWriter](https://developer.android.com/reference/kotlin/java/io/PipedWriter.html#) | Piped character-output streams. | | [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#) | Prints formatted representations of objects to a text-output stream. | | [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder.html#) | This is the class for text whose content and markup can both be changed. | | [StringWriter](https://developer.android.com/reference/kotlin/java/io/StringWriter.html#) | A character stream that collects its output in a string buffer, which can then be used to construct a string. | |

An object to which `char` sequences and values can be appended. The `Appendable` interface must be implemented by any class whose instances are intended to receive formatted output from a `https://developer.android.com/reference/kotlin/java/util/Formatter.html#`.

The characters to be appended should be valid Unicode characters as described in [Unicode Character Representation](https://developer.android.com/reference/kotlin/java/lang/Character#unicode). Note that supplementary characters may be composed of multiple 16-bit `char` values.

Appendables are not necessarily safe for multithreaded access. Thread safety is the responsibility of classes that extend and implement this interface.

Since this interface may be implemented by existing classes with different styles of error handling there is no guarantee that errors will be propagated to the invoker.

## Summary

| Public methods ||
|---|---|
| abstract [Appendable](https://developer.android.com/reference/kotlin/java/lang/Appendable#) | `https://developer.android.com/reference/kotlin/java/lang/Appendable#append(kotlin.Char)(c: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Appends the specified character to this `Appendable`. |
| abstract [Appendable](https://developer.android.com/reference/kotlin/java/lang/Appendable#) | `https://developer.android.com/reference/kotlin/java/lang/Appendable#append(kotlin.CharSequence)(csq: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)` Appends the specified character sequence to this `Appendable`. |
| abstract [Appendable](https://developer.android.com/reference/kotlin/java/lang/Appendable#) | `https://developer.android.com/reference/kotlin/java/lang/Appendable#append(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int)(csq: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Appends a subsequence of the specified character sequence to this `Appendable`. |

## Public methods

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun append(c: Char): Appendable
```

Appends the specified character to this `Appendable`.

| Parameters ||
|---|---|
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): The character to append |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Appendable#` | A reference to this `Appendable` |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun append(csq: CharSequence?): Appendable
```

Appends the specified character sequence to this `Appendable`.

Depending on which class implements the character sequence `csq`, the entire sequence may not be appended. For instance, if `csq` is a `https://developer.android.com/reference/kotlin/java/nio/CharBuffer.html#` then the subsequence to append is defined by the buffer's position and limit.

| Parameters ||
|---|---|
| `csq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: The character sequence to append. If `csq` is `null`, then the four characters `"null"` are appended to this Appendable. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Appendable#` | A reference to this `Appendable` |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun append(
    csq: CharSequence?, 
    start: Int, 
    end: Int
): Appendable
```

Appends a subsequence of the specified character sequence to this `Appendable`.

An invocation of this method of the form `out.append(csq, start, end)` when `csq` is not `null`, behaves in exactly the same way as the invocation

```kotlin
out.append(csq.subSequence(start, end)) 
```

| Parameters ||
|---|---|
| `csq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: The character sequence from which a subsequence will be appended. If `csq` is `null`, then characters will be appended as if `csq` contained the four characters `"null"`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the first character in the subsequence |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the character following the last character in the subsequence |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Appendable#` | A reference to this `Appendable` |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.IndexOutOfBoundsException` | If `start` or `end` are negative, `start` is greater than `end`, or `end` is greater than `csq.length()` |
