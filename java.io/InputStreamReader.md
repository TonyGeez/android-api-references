Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputStreamReader

```
open class InputStreamReader : Reader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.io.Reader](../java/io/Reader.md) ||
| | ↳ | [java.io.InputStreamReader](../java/io/InputStreamReader.md) |

| Known Direct Subclasses [FileReader](../java/io/FileReader.md) |---|---| | [FileReader](../java/io/FileReader.md) | Reads text from character files using a default buffer size. | |
| --- | --- | --- | --- | --- | --- | --- |

An InputStreamReader is a bridge from byte streams to character streams: It reads bytes and decodes them into characters using a specified `https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#`. The charset that it uses may be specified by name or may be given explicitly, or the platform's `https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset()` may be accepted.

Each invocation of one of an InputStreamReader's read() methods may cause one or more bytes to be read from the underlying byte-input stream. To enable the efficient conversion of bytes to characters, more bytes may be read ahead from the underlying stream than are necessary to satisfy the current read operation.

For top efficiency, consider wrapping an InputStreamReader within a BufferedReader. For example:

```kotlin
BufferedReader in
    = new BufferedReader(new InputStreamReader(anInputStream));
  
```

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/InputStreamReader#InputStreamReader(java.io.InputStream)(in: https://developer.android.com/reference/kotlin/java/io/InputStream!)` Creates an InputStreamReader that uses the `https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset()`. |
| `https://developer.android.com/reference/kotlin/java/io/InputStreamReader#InputStreamReader(java.io.InputStream,%20kotlin.String)(in: https://developer.android.com/reference/kotlin/java/io/InputStream!, charsetName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Creates an InputStreamReader that uses the named charset. |
| `https://developer.android.com/reference/kotlin/java/io/InputStreamReader#InputStreamReader(java.io.InputStream,%20java.nio.charset.Charset)(in: https://developer.android.com/reference/kotlin/java/io/InputStream!, cs: https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#!)` Creates an InputStreamReader that uses the given charset. |
| `https://developer.android.com/reference/kotlin/java/io/InputStreamReader#InputStreamReader(java.io.InputStream,%20java.nio.charset.CharsetDecoder)(in: https://developer.android.com/reference/kotlin/java/io/InputStream!, dec: https://developer.android.com/reference/kotlin/java/nio/charset/CharsetDecoder.html#!)` Creates an InputStreamReader that uses the given charset decoder. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/InputStreamReader#close()()` Closes the stream and releases any system resources associated with it. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/io/InputStreamReader#getEncoding()()` Returns the name of the character encoding being used by this stream. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/InputStreamReader#read()()` Reads a single character. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/InputStreamReader#read(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)(cbuf: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, off: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Reads characters into a portion of an array. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/InputStreamReader#read(java.nio.CharBuffer)(target: https://developer.android.com/reference/kotlin/java/nio/CharBuffer.html#!)` Attempts to read characters into the specified character buffer. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/io/InputStreamReader#ready()()` Tells whether this stream is ready to be read. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/io/Reader` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/io/Reader#mark(kotlin.Int)(readAheadLimit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Marks the present position in the stream. Subsequent calls to reset() will attempt to reposition the stream to this point. Not all character-input streams support the mark() operation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/io/Reader#markSupported()()` Tells whether this stream supports the mark() operation. The default implementation always returns false. Subclasses should override this method. <br /> | | `https://developer.android.com/reference/kotlin/java/io/Reader!` | `https://developer.android.com/reference/kotlin/java/io/Reader#nullReader()()` Returns a new `Reader` that reads no characters. The returned stream is initially open. The stream is closed by calling the `close()` method. Subsequent calls to `close()` have no effect. While the stream is open, the `read()`, `read(char[])`, `read(char[], int, int)`, `read(Charbuffer)`, `ready()`, `skip(long)`, and `transferTo()` methods all behave as if end of stream has been reached. After the stream has been closed, these methods all throw `IOException`. The `markSupported()` method returns `false`. The `mark()` and `reset()` methods throw an `IOException`. The `https://developer.android.com/reference/kotlin/java/io/Reader#lock:kotlin.Any` used to synchronize operations on the returned `Reader` is not specified. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/io/Reader#read(kotlin.CharArray)(cbuf: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!)` Reads characters into an array. This method will block until some input is available, an I/O error occurs, or the end of the stream is reached. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/io/Reader#reset()()` Resets the stream. If the stream has been marked, then attempt to reposition it at the mark. If the stream has not been marked, then attempt to reset it in some way appropriate to the particular stream, for example by repositioning it to its starting point. Not all character-input streams support the reset() operation, and some support reset() without supporting mark(). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/io/Reader#skip(kotlin.Long)(n: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Skips characters. This method will block until some characters are available, an I/O error occurs, or the end of the stream is reached. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/io/Reader#transferTo(java.io.Writer)(out: https://developer.android.com/reference/kotlin/java/io/Writer!)` Reads all characters from this reader and writes the characters to the given writer in the order that they are read. On return, this reader will be at end of the stream. This method does not close either reader or writer. This method may block indefinitely reading from the reader, or writing to the writer. The behavior for the case where the reader and/or writer is *asynchronously closed*, or the thread interrupted during the transfer, is highly reader and writer specific, and therefore not specified. If an I/O error occurs reading from the reader or writing to the writer, then it may do so after some characters have been read or written. Consequently the reader may not be at end of the stream and one, or both, streams may be in an inconsistent state. It is strongly recommended that both streams be promptly closed if an I/O error occurs. <br /> | ||

| Inherited properties ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/io/Reader` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | `https://developer.android.com/reference/kotlin/java/io/Reader#lock:kotlin.Any` The object used to synchronize operations on this stream. For efficiency, a character-stream object may use an object other than itself to protect critical sections. A subclass should therefore use the object in this field rather than `this` or a synchronized method. <br /> | ||

## Public constructors

### InputStreamReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
InputStreamReader(in: InputStream!)
```

Creates an InputStreamReader that uses the `https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset()`.

| Parameters ||
|---|---|
| `in` | [InputStream](../java/io/InputStream.md)!: An InputStream |

**See Also**

- `https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset()`

### InputStreamReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
InputStreamReader(
    in: InputStream!, 
    charsetName: String!)
```

Creates an InputStreamReader that uses the named charset.

| Parameters ||
|---|---|
| `in` | [InputStream](../java/io/InputStream.md)!: An InputStream |
| `charsetName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of a supported `https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#` |

| Exceptions ||
|---|---|
| `java.io.UnsupportedEncodingException` | If the named charset is not supported |

### InputStreamReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
InputStreamReader(
    in: InputStream!, 
    cs: Charset!)
```

Creates an InputStreamReader that uses the given charset.

| Parameters ||
|---|---|
| `in` | [InputStream](../java/io/InputStream.md)!: An InputStream |
| `cs` | [Charset](../java/nio/charset/Charset.md)!: A charset |

### InputStreamReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
InputStreamReader(
    in: InputStream!, 
    dec: CharsetDecoder!)
```

Creates an InputStreamReader that uses the given charset decoder.

| Parameters ||
|---|---|
| `in` | [InputStream](../java/io/InputStream.md)!: An InputStream |
| `dec` | [CharsetDecoder](../java/nio/charset/CharsetDecoder.md)!: A charset decoder |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun close(): Unit
```

Closes the stream and releases any system resources associated with it. Once the stream has been closed, further read(), ready(), mark(), reset(), or skip() invocations will throw an IOException. Closing a previously closed stream has no effect.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | If an I/O error occurs |

### getEncoding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEncoding(): String!
```

Returns the name of the character encoding being used by this stream.

If the encoding has an historical name then that name is returned; otherwise the encoding's canonical name is returned.

If this instance was created with the `https://developer.android.com/reference/kotlin/java/io/InputStreamReader#InputStreamReader(java.io.InputStream,%20kotlin.String)` constructor then the returned name, being unique for the encoding, may differ from the name passed to the constructor. This method will return `null` if the stream has been closed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The historical name of this encoding, or `null` if the stream has been closed |

**See Also**

- `https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#`

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun read(): Int
```

Reads a single character.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The character read, or -1 if the end of the stream has been reached |

| Exceptions ||
|---|---|
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

Tells whether this stream is ready to be read. An InputStreamReader is ready if its input buffer is not empty, or if bytes are available to be read from the underlying byte stream.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the next read() is guaranteed not to block for input, false otherwise. Note that returning false does not guarantee that the next read will block. |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs |
