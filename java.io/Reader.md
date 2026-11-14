Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Reader

```
abstract class Reader : Closeable, Readable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.io.Reader](../java/io/Reader.md) |

| Known Direct Subclasses [BufferedReader](../java/io/BufferedReader.md), [CharArrayReader](../java/io/CharArrayReader.md), [FilterReader](../java/io/FilterReader.md), [InputStreamReader](../java/io/InputStreamReader.md), [PipedReader](../java/io/PipedReader.md), [StringReader](../java/io/StringReader.md) |---|---| | [BufferedReader](../java/io/BufferedReader.md) | Reads text from a character-input stream, buffering characters so as to provide for the efficient reading of characters, arrays, and lines. | | [CharArrayReader](../java/io/CharArrayReader.md) | This class implements a character buffer that can be used as a character-input stream. | | [FilterReader](../java/io/FilterReader.md) | Abstract class for reading filtered character streams. | | [InputStreamReader](../java/io/InputStreamReader.md) | An InputStreamReader is a bridge from byte streams to character streams: It reads bytes and decodes them into characters using a specified `https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#`. | | [PipedReader](../java/io/PipedReader.md) | Piped character-input streams. | | [StringReader](../java/io/StringReader.md) | A character stream whose source is a string. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [FileReader](../java/io/FileReader.md), [LineNumberReader](../java/io/LineNumberReader.md), [PushbackReader](../java/io/PushbackReader.md) |---|---| | [FileReader](../java/io/FileReader.md) | Reads text from character files using a default buffer size. | | [LineNumberReader](../java/io/LineNumberReader.md) | A buffered character-input stream that keeps track of line numbers. | | [PushbackReader](../java/io/PushbackReader.md) | A character-stream reader that allows characters to be pushed back into the stream. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Abstract class for reading character streams. The only methods that a subclass must implement are read(char\[\], int, int) and close(). Most subclasses, however, will override some of the methods defined here in order to provide higher efficiency, additional functionality, or both.

## Summary

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/Reader#Reader()()` Creates a new character-stream reader whose critical sections will synchronize on the reader itself. |
| `https://developer.android.com/reference/kotlin/java/io/Reader#Reader(kotlin.Any)(lock: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Creates a new character-stream reader whose critical sections will synchronize on the given object. |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/Reader#close()()` Closes the stream and releases any system resources associated with it. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/Reader#mark(kotlin.Int)(readAheadLimit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Marks the present position in the stream. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/io/Reader#markSupported()()` Tells whether this stream supports the mark() operation. |
| --- | --- |
| open static [Reader](../java/io/Reader.md)! | `https://developer.android.com/reference/kotlin/java/io/Reader#nullReader()()` Returns a new `Reader` that reads no characters. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/Reader#read()()` Reads a single character. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/Reader#read(kotlin.CharArray)(cbuf: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!)` Reads characters into an array. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/Reader#read(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)(cbuf: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, off: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Reads characters into a portion of an array. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/Reader#read(java.nio.CharBuffer)(target: https://developer.android.com/reference/kotlin/java/nio/CharBuffer.html#!)` Attempts to read characters into the specified character buffer. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/io/Reader#ready()()` Tells whether this stream is ready to be read. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/Reader#reset()()` Resets the stream. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/io/Reader#skip(kotlin.Long)(n: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Skips characters. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/io/Reader#transferTo(java.io.Writer)(out: https://developer.android.com/reference/kotlin/java/io/Writer!)` Reads all characters from this reader and writes the characters to the given writer in the order that they are read. |
| --- | --- |

| Properties ||
|---|---|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/java/io/Reader#lock:kotlin.Any` The object used to synchronize operations on this stream. |

## Protected constructors

### Reader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected Reader()
```

Creates a new character-stream reader whose critical sections will synchronize on the reader itself.

### Reader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected Reader(lock: Any!)
```

Creates a new character-stream reader whose critical sections will synchronize on the given object.

| Parameters ||
|---|---|
| `lock` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The Object to synchronize on. |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun close(): Unit
```

Closes the stream and releases any system resources associated with it. Once the stream has been closed, further read(), ready(), mark(), reset(), or skip() invocations will throw an IOException. Closing a previously closed stream has no effect.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | If an I/O error occurs |

### mark

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun mark(readAheadLimit: Int): Unit
```

Marks the present position in the stream. Subsequent calls to reset() will attempt to reposition the stream to this point. Not all character-input streams support the mark() operation.

| Parameters ||
|---|---|
| `readAheadLimit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Limit on the number of characters that may be read while still preserving the mark. After reading this many characters, attempting to reset the stream may fail. |

| Exceptions ||
|---|---|
| `java.io.IOException` | If the stream does not support mark(), or if some other I/O error occurs |

### markSupported

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun markSupported(): Boolean
```

Tells whether this stream supports the mark() operation. The default implementation always returns false. Subclasses should override this method.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this stream supports the mark operation. |

### nullReader

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun nullReader(): Reader!
```

Returns a new `Reader` that reads no characters. The returned stream is initially open. The stream is closed by calling the `close()` method. Subsequent calls to `close()` have no effect.

While the stream is open, the `read()`, `read(char[])`, `read(char[], int, int)`, `read(Charbuffer)`, `ready()`, `skip(long)`, and `transferTo()` methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw `IOException`.

The `markSupported()` method returns `false`. The `mark()` and `reset()` methods throw an `IOException`.

The `https://developer.android.com/reference/kotlin/java/io/Reader#lock:kotlin.Any` used to synchronize operations on the returned `Reader` is not specified.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/Reader#!` | a `Reader` which reads no characters |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun read(): Int
```

Reads a single character. This method will block until a character is available, an I/O error occurs, or the end of the stream is reached.

Subclasses that intend to support efficient single-character input should override this method.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The character read, as an integer in the range 0 to 65535 (`0x00-0xffff`), or -1 if the end of the stream has been reached |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun read(cbuf: CharArray!): Int
```

Reads characters into an array. This method will block until some input is available, an I/O error occurs, or the end of the stream is reached.

| Parameters ||
|---|---|
| `cbuf` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: Destination buffer |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of characters read, or -1 if the end of the stream has been reached |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun read(
    cbuf: CharArray!, 
    off: Int, 
    len: Int
): Int
```

Reads characters into a portion of an array. This method will block until some input is available, an I/O error occurs, or the end of the stream is reached.

| Parameters ||
|---|---|
| `cbuf` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: Destination buffer |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Offset at which to start storing characters |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Maximum number of characters to read |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of characters read, or -1 if the end of the stream has been reached |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.IndexOutOfBoundsException` | If `off` is negative, or `len` is negative, or `len` is greater than `cbuf.length - off` |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun read(target: CharBuffer!): Int
```

Attempts to read characters into the specified character buffer. The buffer is used as a repository of characters as-is: the only changes made are the results of a put operation. No flipping or rewinding of the buffer is performed.

| Parameters ||
|---|---|
| `cb` | the buffer to read characters into |
| `target` | [CharBuffer](../java/nio/CharBuffer.md)!: the buffer to read characters into |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of characters added to the buffer, or -1 if this source of characters is at its end |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.NullPointerException` | if target is null |
| `java.nio.ReadOnlyBufferException` | if target is a read only buffer |
| --- | --- |

### ready

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun ready(): Boolean
```

Tells whether this stream is ready to be read.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the next read() is guaranteed not to block for input, false otherwise. Note that returning false does not guarantee that the next read will block. |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reset(): Unit
```

Resets the stream. If the stream has been marked, then attempt to reposition it at the mark. If the stream has not been marked, then attempt to reset it in some way appropriate to the particular stream, for example by repositioning it to its starting point. Not all character-input streams support the reset() operation, and some support reset() without supporting mark().

| Exceptions ||
|---|---|
| `java.io.IOException` | If the stream has not been marked, or if the mark has been invalidated, or if the stream does not support reset(), or if some other I/O error occurs |

### skip

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun skip(n: Long): Long
```

Skips characters. This method will block until some characters are available, an I/O error occurs, or the end of the stream is reached.

| Parameters ||
|---|---|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The number of characters to skip |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The number of characters actually skipped |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.IllegalArgumentException` | If `n` is negative. |

### transferTo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun transferTo(out: Writer!): Long
```

Reads all characters from this reader and writes the characters to the given writer in the order that they are read. On return, this reader will be at end of the stream. This method does not close either reader or writer.

This method may block indefinitely reading from the reader, or writing to the writer. The behavior for the case where the reader and/or writer is *asynchronously closed*, or the thread interrupted during the transfer, is highly reader and writer specific, and therefore not specified.

If an I/O error occurs reading from the reader or writing to the writer, then it may do so after some characters have been read or written. Consequently the reader may not be at end of the stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs.

| Parameters ||
|---|---|
| `out` | [Writer](../java/io/Writer.md)!: the writer, non-null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the number of characters transferred |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs when reading or writing |
| `java.lang.NullPointerException` | if `out` is `null` |

## Properties

### lock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var lock: Any!
```

The object used to synchronize operations on this stream. For efficiency, a character-stream object may use an object other than itself to protect critical sections. A subclass should therefore use the object in this field rather than `this` or a synchronized method.
