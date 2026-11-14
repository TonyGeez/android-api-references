# Readable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Readable

```
interface Readable
```

| [java.lang.Readable](https://developer.android.com/reference/kotlin/java/lang/Readable#) |

| Known Direct Subclasses [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer.html#), [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#) |----------------------------------------------------------------------------------------|-----------------------------------------------| | [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer.html#) | A char buffer. | | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#) | Abstract class for reading character streams. | |

| Known Indirect Subclasses [BufferedReader](https://developer.android.com/reference/kotlin/java/io/BufferedReader.html#), [CharArrayReader](https://developer.android.com/reference/kotlin/java/io/CharArrayReader.html#), [FileReader](https://developer.android.com/reference/kotlin/java/io/FileReader.html#), [FilterReader](https://developer.android.com/reference/kotlin/java/io/FilterReader.html#), [InputStreamReader](https://developer.android.com/reference/kotlin/java/io/InputStreamReader.html#), [LineNumberReader](https://developer.android.com/reference/kotlin/java/io/LineNumberReader.html#), [PipedReader](https://developer.android.com/reference/kotlin/java/io/PipedReader.html#), [PushbackReader](https://developer.android.com/reference/kotlin/java/io/PushbackReader.html#), [StringReader](https://developer.android.com/reference/kotlin/java/io/StringReader.html#) |-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------| | [BufferedReader](https://developer.android.com/reference/kotlin/java/io/BufferedReader.html#) | Reads text from a character-input stream, buffering characters so as to provide for the efficient reading of characters, arrays, and lines. | | [CharArrayReader](https://developer.android.com/reference/kotlin/java/io/CharArrayReader.html#) | This class implements a character buffer that can be used as a character-input stream. | | [FileReader](https://developer.android.com/reference/kotlin/java/io/FileReader.html#) | Reads text from character files using a default buffer size. | | [FilterReader](https://developer.android.com/reference/kotlin/java/io/FilterReader.html#) | Abstract class for reading filtered character streams. | | [InputStreamReader](https://developer.android.com/reference/kotlin/java/io/InputStreamReader.html#) | An InputStreamReader is a bridge from byte streams to character streams: It reads bytes and decodes them into characters using a specified . | | [LineNumberReader](https://developer.android.com/reference/kotlin/java/io/LineNumberReader.html#) | A buffered character-input stream that keeps track of line numbers. | | [PipedReader](https://developer.android.com/reference/kotlin/java/io/PipedReader.html#) | Piped character-input streams. | | [PushbackReader](https://developer.android.com/reference/kotlin/java/io/PushbackReader.html#) | A character-stream reader that allows characters to be pushed back into the stream. | | [StringReader](https://developer.android.com/reference/kotlin/java/io/StringReader.html#) | A character stream whose source is a string. | |

A`Readable`is a source of characters. Characters from a`Readable`are made available to callers of the read method via a [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer.html#).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/lang/Readable#read(java.nio.CharBuffer))`(`cb:` ` [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer.html#)!`)` Attempts to read characters into the specified character buffer. |

## Public methods

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun read(cb: CharBuffer!): Int
```

Attempts to read characters into the specified character buffer. The buffer is used as a repository of characters as-is: the only changes made are the results of a put operation. No flipping or rewinding of the buffer is performed.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------|
| `cb` | [CharBuffer](https://developer.android.com/reference/kotlin/java/nio/CharBuffer.html#)!:the buffer to read characters into |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of`char`values added to the buffer, or -1 if this source of characters is at its end |

| Exceptions ||
|------------------------------------|-----------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.NullPointerException` | if cb is null |
| `java.nio.ReadOnlyBufferException` | if cb is a read only buffer |
