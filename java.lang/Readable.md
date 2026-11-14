# Readable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Readable

```
interface Readable
```

| [java.lang.Readable](../java/lang/Readable.md) |

| Known Direct Subclasses [CharBuffer](../java/nio/CharBuffer.md), [Reader](../java/io/Reader.md) |----------------------------------------------------------------------------------------|-----------------------------------------------| | [CharBuffer](../java/nio/CharBuffer.md) | A char buffer. | | [Reader](../java/io/Reader.md) | Abstract class for reading character streams. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [BufferedReader](../java/io/BufferedReader.md), [CharArrayReader](../java/io/CharArrayReader.md), [FileReader](../java/io/FileReader.md), [FilterReader](../java/io/FilterReader.md), [InputStreamReader](../java/io/InputStreamReader.md), [LineNumberReader](../java/io/LineNumberReader.md), [PipedReader](../java/io/PipedReader.md), [PushbackReader](../java/io/PushbackReader.md), [StringReader](../java/io/StringReader.md) |-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------| | [BufferedReader](../java/io/BufferedReader.md) | Reads text from a character-input stream, buffering characters so as to provide for the efficient reading of characters, arrays, and lines. | | [CharArrayReader](../java/io/CharArrayReader.md) | This class implements a character buffer that can be used as a character-input stream. | | [FileReader](../java/io/FileReader.md) | Reads text from character files using a default buffer size. | | [FilterReader](../java/io/FilterReader.md) | Abstract class for reading filtered character streams. | | [InputStreamReader](../java/io/InputStreamReader.md) | An InputStreamReader is a bridge from byte streams to character streams: It reads bytes and decodes them into characters using a specified . | | [LineNumberReader](../java/io/LineNumberReader.md) | A buffered character-input stream that keeps track of line numbers. | | [PipedReader](../java/io/PipedReader.md) | Piped character-input streams. | | [PushbackReader](../java/io/PushbackReader.md) | A character-stream reader that allows characters to be pushed back into the stream. | | [StringReader](../java/io/StringReader.md) | A character stream whose source is a string. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A`Readable`is a source of characters. Characters from a`Readable`are made available to callers of the read method via a [CharBuffer](../java/nio/CharBuffer.md).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](../java/lang/Readable.md))`(`cb:` ` [CharBuffer](../java/nio/CharBuffer.md)!`)` Attempts to read characters into the specified character buffer. |

## Public methods

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun read(cb: CharBuffer!): Int
```

Attempts to read characters into the specified character buffer. The buffer is used as a repository of characters as-is: the only changes made are the results of a put operation. No flipping or rewinding of the buffer is performed.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------|
| `cb` | [CharBuffer](../java/nio/CharBuffer.md)!:the buffer to read characters into |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of`char`values added to the buffer, or -1 if this source of characters is at its end |

| Exceptions ||
|------------------------------------|-----------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.NullPointerException` | if cb is null |
| `java.nio.ReadOnlyBufferException` | if cb is a read only buffer |
| --- | --- |
