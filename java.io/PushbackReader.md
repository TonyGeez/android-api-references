# PushbackReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PushbackReader

```
open class PushbackReader : FilterReader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.io.Reader](Reader.md) |||
| | ↳ | [java.io.FilterReader](FilterReader.md) ||
| | | ↳ | [java.io.PushbackReader](PushbackReader.md) |
| --- | --- | --- | --- |

A character-stream reader that allows characters to be pushed back into the stream.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PushbackReader](PushbackReader.md))`(`in:` ` [Reader](Reader.md)!`)` Creates a new pushback reader with a one-character pushback buffer. |
| [PushbackReader](PushbackReader.md))`(`in:` ` [Reader](Reader.md)!`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new pushback reader with a pushback buffer of the given size. |

| Public methods ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](PushbackReader.md))`()` Closes the stream and releases any system resources associated with it. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mark](PushbackReader.md))`(`readAheadLimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Marks the present position in the stream. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [markSupported](PushbackReader.md))`()` Tells whether this stream supports the mark() operation, which it does not. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](PushbackReader.md))`()` Reads a single character. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](PushbackReader.md))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads characters into a portion of an array. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [ready](PushbackReader.md))`()` Tells whether this stream is ready to be read. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](PushbackReader.md))`()` Resets the stream. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [skip](PushbackReader.md))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Skips characters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unread](PushbackReader.md))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` Pushes back an array of characters by copying it to the front of the pushback buffer. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unread](PushbackReader.md))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Pushes back a portion of an array of characters by copying it to the front of the pushback buffer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unread](PushbackReader.md))`(`c:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Pushes back a single character by copying it to the front of the pushback buffer. |

| Inherited functions ||
|---|---|
| From class [Reader](Reader.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Reader](Reader.md)! | [nullReader](Reader.md))`()` <br /> Returns a new`Reader`that reads no characters. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`read()`,`read(char[])`,`read(char[], int, int)`,`read(Charbuffer)`,`ready()`,`skip(long)`, and`transferTo()`methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw`IOException`. The`markSupported()`method returns`false`. The`mark()`and`reset()`methods throw an`IOException`. The [object](Reader.md) used to synchronize operations on the returned`Reader`is not specified. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](Reader.md))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` <br /> Reads characters into an array. This method will block until some input is available, an I/O error occurs, or the end of the stream is reached. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](Reader.md))`(`target:` ` [CharBuffer](../java.nio/CharBuffer.md)!`)` <br /> Attempts to read characters into the specified character buffer. The buffer is used as a repository of characters as-is: the only changes made are the results of a put operation. No flipping or rewinding of the buffer is performed. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [transferTo](Reader.md))`(`out:` ` [Writer](Writer.md)!`)` <br /> Reads all characters from this reader and writes the characters to the given writer in the order that they are read. On return, this reader will be at end of the stream. This method does not close either reader or writer. This method may block indefinitely reading from the reader, or writing to the writer. The behavior for the case where the reader and/or writer is*asynchronously closed*, or the thread interrupted during the transfer, is highly reader and writer specific, and therefore not specified. If an I/O error occurs reading from the reader or writing to the writer, then it may do so after some characters have been read or written. Consequently the reader may not be at end of the stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs. <br /> | ||

| Inherited properties ||
|---|---|
| From class [FilterReader](FilterReader.md) |--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------| | [Reader](Reader.md)! | [in](FilterReader.md) <br /> The underlying character-input stream. <br /> | ||
| From class [Reader](Reader.md) |-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [lock](Reader.md) <br /> The object used to synchronize operations on this stream. For efficiency, a character-stream object may use an object other than itself to protect critical sections. A subclass should therefore use the object in this field rather than`this`or a synchronized method. <br /> | ||

## Public constructors

### PushbackReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PushbackReader(in: Reader!)
```

Creates a new pushback reader with a one-character pushback buffer.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------|
| `in` | [Reader](Reader.md)!:The reader from which characters will be read |

### PushbackReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PushbackReader(
    in: Reader!, 
    size: Int)
```

Creates a new pushback reader with a pushback buffer of the given size.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------|
| `in` | [Reader](Reader.md)!:The reader from which characters will be read |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The size of the pushback buffer |

| Exceptions ||
|--------------------------------------|---------------|
| `java.lang.IllegalArgumentException` | if`size <= 0` |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes the stream and releases any system resources associated with it. Once the stream has been closed, further read(), unread(), ready(), or skip() invocations will throw an IOException. Closing a previously closed stream has no effect. This method will block while there is another thread blocking on the reader.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |
| `java.io.IOException` | If an I/O error occurs |
| --- | --- |

### mark

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mark(readAheadLimit: Int): Unit
```

Marks the present position in the stream. The`mark`for class`PushbackReader`always throws an exception.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `readAheadLimit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Limit on the number of characters that may be read while still preserving the mark. After reading this many characters, attempting to reset the stream may fail. |

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.io.IOException` | Always, since mark is not supported |

### markSupported

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun markSupported(): Boolean
```

Tells whether this stream supports the mark() operation, which it does not.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if and only if this stream supports the mark operation. |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(): Int
```

Reads a single character.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The character read, or -1 if the end of the stream has been reached |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(
    cbuf: CharArray!, 
    off: Int, 
    len: Int
): Int
```

Reads characters into a portion of an array.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------|
| `cbuf` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:Destination buffer |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset at which to start writing characters |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Maximum number of characters to read |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of characters read, or -1 if the end of the stream has been reached |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------|
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.IndexOutOfBoundsException` | If`off`is negative, or`len`is negative, or`len`is greater than`cbuf.length - off` |

### ready

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun ready(): Boolean
```

Tells whether this stream is ready to be read.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the next read() is guaranteed not to block for input, false otherwise. Note that returning false does not guarantee that the next read will block. |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Resets the stream. The`reset`method of`PushbackReader`always throws an exception.

| Exceptions ||
|-----------------------|--------------------------------------|
| `java.io.IOException` | Always, since reset is not supported |

### skip

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun skip(n: Long): Long
```

Skips characters. This method will block until some characters are available, an I/O error occurs, or the end of the stream is reached.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The number of characters to skip |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of characters actually skipped |

| Exceptions ||
|--------------------------------------|------------------------|
| `java.lang.IllegalArgumentException` | If`n`is negative. |
| `java.io.IOException` | If an I/O error occurs |

### unread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unread(cbuf: CharArray!): Unit
```

Pushes back an array of characters by copying it to the front of the pushback buffer. After this method returns, the next character to be read will have the value`cbuf[0]`, the character after that will have the value`cbuf[1]`, and so forth.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------|
| `cbuf` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:Character array to push back |

| Exceptions ||
|-----------------------|-----------------------------------------------------------------------------------------|
| `java.io.IOException` | If there is insufficient room in the pushback buffer, or if some other I/O error occurs |

### unread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unread(
    cbuf: CharArray!, 
    off: Int, 
    len: Int
): Unit
```

Pushes back a portion of an array of characters by copying it to the front of the pushback buffer. After this method returns, the next character to be read will have the value`cbuf[off]`, the character after that will have the value`cbuf[off+1]`, and so forth.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------|
| `cbuf` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:Character array |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset of first character to push back |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of characters to push back |
| --- | --- |

| Exceptions ||
|-----------------------|-----------------------------------------------------------------------------------------|
| `java.io.IOException` | If there is insufficient room in the pushback buffer, or if some other I/O error occurs |

### unread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unread(c: Int): Unit
```

Pushes back a single character by copying it to the front of the pushback buffer. After this method returns, the next character to be read will have the value`(char)c`.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The int value representing a character to be pushed back |

| Exceptions ||
|-----------------------|-------------------------------------------------------------------|
| `java.io.IOException` | If the pushback buffer is full, or if some other I/O error occurs |
