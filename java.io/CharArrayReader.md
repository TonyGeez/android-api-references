# CharArrayReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CharArrayReader

```
open class CharArrayReader : Reader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.io.Reader](Reader.md) ||
| | ↳ | [java.io.CharArrayReader](CharArrayReader.md) |

This class implements a character buffer that can be used as a character-input stream.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CharArrayReader](CharArrayReader.md))`(`buf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` Creates a CharArrayReader from the specified array of chars. |
| [CharArrayReader](CharArrayReader.md))`(`buf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a CharArrayReader from the specified array of chars. |

| Public methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](CharArrayReader.md))`()` Closes the stream and releases any system resources associated with it. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mark](CharArrayReader.md))`(`readAheadLimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Marks the present position in the stream. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [markSupported](CharArrayReader.md))`()` Tells whether this stream supports the mark() operation, which it does. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](CharArrayReader.md))`()` Reads a single character. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](CharArrayReader.md))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads characters into a portion of an array. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](CharArrayReader.md))`(`target:` ` [CharBuffer](../java.nio/CharBuffer.md)!`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [ready](CharArrayReader.md))`()` Tells whether this stream is ready to be read. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](CharArrayReader.md))`()` Resets the stream to the most recent mark, or to the beginning if it has never been marked. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [skip](CharArrayReader.md))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Skips characters. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Reader](Reader.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Reader](Reader.md)! | [nullReader](Reader.md))`()` <br /> Returns a new`Reader`that reads no characters. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`read()`,`read(char[])`,`read(char[], int, int)`,`read(Charbuffer)`,`ready()`,`skip(long)`, and`transferTo()`methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw`IOException`. The`markSupported()`method returns`false`. The`mark()`and`reset()`methods throw an`IOException`. The [object](Reader.md) used to synchronize operations on the returned`Reader`is not specified. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](Reader.md))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` <br /> Reads characters into an array. This method will block until some input is available, an I/O error occurs, or the end of the stream is reached. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [transferTo](Reader.md))`(`out:` ` [Writer](Writer.md)!`)` <br /> Reads all characters from this reader and writes the characters to the given writer in the order that they are read. On return, this reader will be at end of the stream. This method does not close either reader or writer. This method may block indefinitely reading from the reader, or writing to the writer. The behavior for the case where the reader and/or writer is*asynchronously closed*, or the thread interrupted during the transfer, is highly reader and writer specific, and therefore not specified. If an I/O error occurs reading from the reader or writing to the writer, then it may do so after some characters have been read or written. Consequently the reader may not be at end of the stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [buf](CharArrayReader.md) The character buffer. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [count](CharArrayReader.md) The index of the end of this buffer. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [markedPos](CharArrayReader.md) The position of mark in buffer. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [pos](CharArrayReader.md) The current buffer position. |

| Inherited properties ||
|---|---|
| From class [Reader](Reader.md) |-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [lock](Reader.md) <br /> The object used to synchronize operations on this stream. For efficiency, a character-stream object may use an object other than itself to protect critical sections. A subclass should therefore use the object in this field rather than`this`or a synchronized method. <br /> | ||

## Public constructors

### CharArrayReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CharArrayReader(buf: CharArray!)
```

Creates a CharArrayReader from the specified array of chars.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------|
| `buf` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:Input buffer (not copied) |

### CharArrayReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CharArrayReader(
    buf: CharArray!, 
    offset: Int, 
    length: Int)
```

Creates a CharArrayReader from the specified array of chars.

The resulting reader will start reading at the given`offset`. The total number of`char`values that can be read from this reader will be either`length`or`buf.length-offset`, whichever is smaller.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `buf` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:Input buffer (not copied) |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset of the first char to read |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of chars to read |
| --- | --- |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If`offset`is negative or greater than`buf.length`, or if`length`is negative, or if the sum of these two values is negative. |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes the stream and releases any system resources associated with it. Once the stream has been closed, further read(), ready(), mark(), reset(), or skip() invocations will throw an IOException. Closing a previously closed stream has no effect. This method will block while there is another thread blocking on the reader.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

### mark

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mark(readAheadLimit: Int): Unit
```

Marks the present position in the stream. Subsequent calls to reset() will reposition the stream to this point.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `readAheadLimit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Limit on the number of characters that may be read while still preserving the mark. Because the stream's input comes from a character array, there is no actual limit; hence this argument is ignored. |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### markSupported

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun markSupported(): Boolean
```

Tells whether this stream supports the mark() operation, which it does.

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
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The character read, as an integer in the range 0 to 65535 (`0x00-0xffff`), or -1 if the end of the stream has been reached |

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

If`len`is zero, then no characters are read and`0`is returned; otherwise, there is an attempt to read at least one character. If no character is available because the stream is at its end, the value`-1`is returned; otherwise, at least one character is read and stored into`cbuf`.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------|
| `cbuf` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:Destination buffer |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset at which to start storing characters |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Maximum number of characters to read |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of characters read, or -1 if the end of the stream has been reached |

| Exceptions ||
|---------------------------------------|---|
| `java.lang.IndexOutOfBoundsException` | |
| `java.io.IOException` | |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun read(target: CharBuffer!): Int
```

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------|
| `cb` | the buffer to read characters into |
| `target` | [CharBuffer](../java.nio/CharBuffer.md)!:the buffer to read characters into |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of characters added to the buffer, or -1 if this source of characters is at its end |

| Exceptions ||
|------------------------------------|---------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.NullPointerException` | if target is null |
| `java.nio.ReadOnlyBufferException` | if target is a read only buffer |
| --- | --- |

### ready

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun ready(): Boolean
```

Tells whether this stream is ready to be read. Character-array readers are always ready to be read.

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

Resets the stream to the most recent mark, or to the beginning if it has never been marked.

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### skip

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun skip(n: Long): Long
```

Skips characters. If the stream is already at its end before this method is invoked, then no characters are skipped and zero is returned.

The`n`parameter may be negative, even though the`skip`method of the [Reader](Reader.md) superclass throws an exception in this case. If`n`is negative, then this method does nothing and returns`0`.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The number of characters to skip |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of characters actually skipped |

| Exceptions ||
|-----------------------|---|
| `java.io.IOException` | |

## Properties

### buf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var buf: CharArray!
```

The character buffer. 

### count

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var count: Int
```

The index of the end of this buffer. There is not valid data at or beyond this index. 

### markedPos

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var markedPos: Int
```

The position of mark in buffer. 

### pos

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var pos: Int
```

The current buffer position.
