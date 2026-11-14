# BufferedWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BufferedWriter

```
open class BufferedWriter : Writer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.io.Writer](https://developer.android.com/reference/kotlin/java/io/Writer) ||
| | ↳ | [java.io.BufferedWriter](https://developer.android.com/reference/kotlin/java/io/BufferedWriter#) |

Writes text to a character-output stream, buffering characters so as to provide for the efficient writing of single characters, arrays, and strings.

The buffer size may be specified, or the default size may be accepted. The default is large enough for most purposes.

A newLine() method is provided, which uses the platform's own notion of line separator as defined by the system property`line.separator`. Not all platforms use the newline character ('\\n') to terminate lines. Calling this method to terminate each output line is therefore preferred to writing a newline character directly.

In general, a Writer sends its output immediately to the underlying character or byte stream. Unless prompt output is required, it is advisable to wrap a BufferedWriter around any Writer whose write() operations may be costly, such as FileWriters and OutputStreamWriters. For example, 

```kotlin
PrintWriter out
    = new PrintWriter(new BufferedWriter(new FileWriter("foo.out")));
  
```
will buffer the PrintWriter's output to the file. Without buffering, each invocation of a print() method would cause characters to be converted into bytes that would then be written immediately to the file, which can be very inefficient.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BufferedWriter](https://developer.android.com/reference/kotlin/java/io/BufferedWriter#BufferedWriter(java.io.Writer))`(`out:` ` [Writer](https://developer.android.com/reference/kotlin/java/io/Writer)!`)` Creates a buffered character-output stream that uses a default-sized output buffer. |
| [BufferedWriter](https://developer.android.com/reference/kotlin/java/io/BufferedWriter#BufferedWriter(java.io.Writer,%20kotlin.Int))`(`out:` ` [Writer](https://developer.android.com/reference/kotlin/java/io/Writer)!`, `sz:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new buffered character-output stream that uses an output buffer of the given size. |

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/io/BufferedWriter#close())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](https://developer.android.com/reference/kotlin/java/io/BufferedWriter#flush())`()` Flushes the stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [newLine](https://developer.android.com/reference/kotlin/java/io/BufferedWriter#newLine())`()` Writes a line separator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/BufferedWriter#write(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a portion of an array of characters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/BufferedWriter#write(kotlin.Int))`(`c:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a single character. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/BufferedWriter#write(kotlin.String,%20kotlin.Int,%20kotlin.Int))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a portion of a String. |

| Inherited functions ||
|---|---|
| From class [Writer](https://developer.android.com/reference/kotlin/java/io/Writer) |------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Writer](https://developer.android.com/reference/kotlin/java/io/Writer) | [append](https://developer.android.com/reference/kotlin/java/io/Writer#append(kotlin.Char))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` <br /> Appends the specified character to this writer. An invocation of this method of the form`out.append(c)`behaves in exactly the same way as the invocation ```kotlin out.write(c) ``` <br /> | | [Writer](https://developer.android.com/reference/kotlin/java/io/Writer) | [append](https://developer.android.com/reference/kotlin/java/io/Writer#append(kotlin.CharSequence))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` <br /> Appends the specified character sequence to this writer. An invocation of this method of the form`out.append(csq)`behaves in exactly the same way as the invocation ```kotlin out.write(csq.toString()) ``` Depending on the specification of`toString`for the character sequence`csq`, the entire sequence may not be appended. For instance, invoking the`toString`method of a character buffer will return a subsequence whose content depends upon the buffer's position and limit. <br /> | | [Writer](https://developer.android.com/reference/kotlin/java/io/Writer) | [append](https://developer.android.com/reference/kotlin/java/io/Writer#append(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Appends a subsequence of the specified character sequence to this writer.`Appendable`. An invocation of this method of the form`out.append(csq, start, end)`when`csq`is not`null`behaves in exactly the same way as the invocation ```kotlin <code>out.write(csq.subSequence(start, end).toString()) </code> ``` <br /> | | [Writer](https://developer.android.com/reference/kotlin/java/io/Writer)! | [nullWriter](https://developer.android.com/reference/kotlin/java/io/Writer#nullWriter())`()` <br /> Returns a new`Writer`which discards all characters. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`append(char)`,`append(CharSequence)`,`append(CharSequence, int, int)`,`flush()`,`write(int)`,`write(char[])`, and`write(char[], int, int)`methods do nothing. After the stream has been closed, these methods all throw`IOException`. The [object](https://developer.android.com/reference/kotlin/java/io/Writer#lock:kotlin.Any) used to synchronize operations on the returned`Writer`is not specified. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/Writer#write(kotlin.CharArray))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` <br /> Writes an array of characters. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/Writer#write(kotlin.String))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Writes a string. <br /> | ||

| Inherited properties ||
|---|---|
| From class [Writer](https://developer.android.com/reference/kotlin/java/io/Writer) |-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [lock](https://developer.android.com/reference/kotlin/java/io/Writer#lock:kotlin.Any) <br /> The object used to synchronize operations on this stream. For efficiency, a character-stream object may use an object other than itself to protect critical sections. A subclass should therefore use the object in this field rather than`this`or a synchronized method. <br /> | ||

## Public constructors

### BufferedWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BufferedWriter(out: Writer!)
```

Creates a buffered character-output stream that uses a default-sized output buffer.

| Parameters ||
|-------|-----------------------------------------------------------------------------------|
| `out` | [Writer](https://developer.android.com/reference/kotlin/java/io/Writer)!:A Writer |

### BufferedWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BufferedWriter(
    out: Writer!, 
    sz: Int)
```

Creates a new buffered character-output stream that uses an output buffer of the given size.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------|
| `out` | [Writer](https://developer.android.com/reference/kotlin/java/io/Writer)!:A Writer |
| `sz` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Output-buffer size, a positive integer |

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
| `java.io.IOException` | If an I/O error occurs |

### flush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun flush(): Unit
```

Flushes the stream.

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |
| `java.io.IOException` | If an I/O error occurs |

### newLine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newLine(): Unit
```

Writes a line separator. The line separator string is defined by the system property`line.separator`, and is not necessarily a single newline ('\\n') character.

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(
    cbuf: CharArray!, 
    off: Int, 
    len: Int
): Unit
```

Writes a portion of an array of characters.

Ordinarily this method stores characters from the given array into this stream's buffer, flushing the buffer to the underlying stream as needed. If the requested length is at least as large as the buffer, however, then this method will flush the buffer and write the characters directly to the underlying stream. Thus redundant`BufferedWriter`s will not copy data unnecessarily.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------|
| `cbuf` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:A character array |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset from which to start reading characters |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of characters to write |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`off`is negative, or`len`is negative, or`off + len`is negative or greater than the length of the given array |
| `java.io.IOException` | If an I/O error occurs |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(c: Int): Unit
```

Writes a single character.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------|
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):int specifying a character to be written |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |
| `java.io.IOException` | If an I/O error occurs |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(
    s: String!, 
    off: Int, 
    len: Int
): Unit
```

Writes a portion of a String.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------|
| `str` | A String |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset from which to start reading characters |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of characters to be written |
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:String to be written |

| Exceptions ||
|---------------------------------------|---------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`off`is negative, or`off + len`is greater than the length of the given string |
| `java.io.IOException` | If an I/O error occurs |
