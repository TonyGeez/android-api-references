# Writer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Writer

```
abstract class Writer : Appendable, Closeable, Flushable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.io.Writer](../java/io/Writer.md) |

| Known Direct Subclasses [BufferedWriter](../java/io/BufferedWriter.md), [CharArrayWriter](../java/io/CharArrayWriter.md), [FilterWriter](../java/io/FilterWriter.md), [OutputStreamWriter](../java/io/OutputStreamWriter.md), [PipedWriter](../java/io/PipedWriter.md), [PrintWriter](../java/io/PrintWriter.md), [StringWriter](../java/io/StringWriter.md) |-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------| | [BufferedWriter](../java/io/BufferedWriter.md) | Writes text to a character-output stream, buffering characters so as to provide for the efficient writing of single characters, arrays, and strings. | | [CharArrayWriter](../java/io/CharArrayWriter.md) | This class implements a character buffer that can be used as an Writer. | | [FilterWriter](../java/io/FilterWriter.md) | Abstract class for writing filtered character streams. | | [OutputStreamWriter](../java/io/OutputStreamWriter.md) | An OutputStreamWriter is a bridge from character streams to byte streams: Characters written to it are encoded into bytes using a specified . | | [PipedWriter](../java/io/PipedWriter.md) | Piped character-output streams. | | [PrintWriter](../java/io/PrintWriter.md) | Prints formatted representations of objects to a text-output stream. | | [StringWriter](../java/io/StringWriter.md) | A character stream that collects its output in a string buffer, which can then be used to construct a string. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [FileWriter](../java/io/FileWriter.md) |---------------------------------------------------------------------------------|-------------------------------------------------------------| | [FileWriter](../java/io/FileWriter.md) | Writes text to character files using a default buffer size. | |
| --- | --- | --- | --- | --- | --- | --- |

Abstract class for writing to character streams. The only methods that a subclass must implement are write(char\[\], int, int), flush(), and close(). Most subclasses, however, will override some of the methods defined here in order to provide higher efficiency, additional functionality, or both.

## Summary

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Writer](../java/io/Writer.md))`()` Creates a new character-stream writer whose critical sections will synchronize on the writer itself. |
| [Writer](../java/io/Writer.md))`(`lock:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Creates a new character-stream writer whose critical sections will synchronize on the given object. |

| Public methods ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Writer](../java/io/Writer.md) | [append](../java/io/Writer.md))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Appends the specified character to this writer. |
| open [Writer](../java/io/Writer.md) | [append](../java/io/Writer.md))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Appends the specified character sequence to this writer. |
| open [Writer](../java/io/Writer.md) | [append](../java/io/Writer.md))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Appends a subsequence of the specified character sequence to this writer. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/io/Writer.md))`()` Closes the stream, flushing it first. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](../java/io/Writer.md))`()` Flushes the stream. |
| open static [Writer](../java/io/Writer.md)! | [nullWriter](../java/io/Writer.md))`()` Returns a new `Writer` which discards all characters. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../java/io/Writer.md))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` Writes an array of characters. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../java/io/Writer.md))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a portion of an array of characters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../java/io/Writer.md))`(`c:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a single character. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../java/io/Writer.md))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Writes a string. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../java/io/Writer.md))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a portion of a string. |

| Properties ||
|-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [lock](../java/io/Writer.md) The object used to synchronize operations on this stream. |

## Protected constructors

### Writer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Writer()
```

Creates a new character-stream writer whose critical sections will synchronize on the writer itself. 

### Writer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Writer(lock: Any!)
```

Creates a new character-stream writer whose critical sections will synchronize on the given object.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------|
| `lock` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: Object to synchronize on |

## Public methods

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun append(c: Char): Writer
```

Appends the specified character to this writer.

An invocation of this method of the form `out.append(c)` behaves in exactly the same way as the invocation 

```kotlin
out.write(c) 
```

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------|
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): The 16-bit character to append |

| Return ||
|--------------------------------------------------------------------------|-------------|
| [Writer](../java/io/Writer.md) | This writer |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun append(csq: CharSequence?): Writer
```

Appends the specified character sequence to this writer.

An invocation of this method of the form `out.append(csq)` behaves in exactly the same way as the invocation 

```kotlin
out.write(csq.toString()) 
```

Depending on the specification of `toString` for the character sequence `csq`, the entire sequence may not be appended. For instance, invoking the `toString` method of a character buffer will return a subsequence whose content depends upon the buffer's position and limit.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `csq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: The character sequence to append. If `csq` is `null`, then the four characters `"null"` are appended to this writer. |

| Return ||
|--------------------------------------------------------------------------|-------------|
| [Writer](../java/io/Writer.md) | This writer |

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
): Writer
```

Appends a subsequence of the specified character sequence to this writer. `Appendable`.

An invocation of this method of the form `out.append(csq, start, end)` when `csq` is not `null` behaves in exactly the same way as the invocation 

```kotlin
<code>out.write(csq.subSequence(start, end).toString())
  </code>
```

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `csq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: The character sequence from which a subsequence will be appended. If `csq` is `null`, then characters will be appended as if `csq` contained the four characters `"null"`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the first character in the subsequence |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the character following the last character in the subsequence |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------|-------------|
| [Writer](../java/io/Writer.md) | This writer |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If `start` or `end` are negative, `start` is greater than `end`, or `end` is greater than `csq.length()` |
| `java.io.IOException` | If an I/O error occurs |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

Closes the stream, flushing it first. Once the stream has been closed, further write() or flush() invocations will cause an IOException to be thrown. Closing a previously closed stream has no effect.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | If an I/O error occurs |

### flush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun flush(): Unit
```

Flushes the stream. If the stream has saved any characters from the various write() methods in a buffer, write them immediately to their intended destination. Then, if that destination is another character or byte stream, flush it. Thus one flush() invocation will flush all the buffers in a chain of Writers and OutputStreams.

If the intended destination of this stream is an abstraction provided by the underlying operating system, for example a file, then flushing the stream guarantees only that bytes previously written to the stream are passed to the operating system for writing; it does not guarantee that they are actually written to a physical device such as a disk drive.

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### nullWriter

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun nullWriter(): Writer!
```

Returns a new `Writer` which discards all characters. The returned stream is initially open. The stream is closed by calling the `close()` method. Subsequent calls to `close()` have no effect.

While the stream is open, the `append(char)`, `append(CharSequence)`, `append(CharSequence, int, int)`, `flush()`, `write(int)`, `write(char[])`, and `write(char[], int, int)` methods do nothing. After the stream has been closed, these methods all throw `IOException`.

The [object](../java/io/Writer.md) used to synchronize operations on the returned `Writer` is not specified.

| Return ||
|---------------------------------------------------------------------------|------------------------------------------|
| [Writer](../java/io/Writer.md)! | a `Writer` which discards all characters |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(cbuf: CharArray!): Unit
```

Writes an array of characters.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------|
| `cbuf` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: Array of characters to be written |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun write(
    cbuf: CharArray!, 
    off: Int, 
    len: Int
): Unit
```

Writes a portion of an array of characters.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------|
| `cbuf` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: Array of characters |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Offset from which to start writing characters |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of characters to write |
| --- | --- |

| Exceptions ||
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | Implementations should throw this exception if `off` is negative, or `len` is negative, or `off + len` is negative or greater than the length of the given array |
| `java.io.IOException` | If an I/O error occurs |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(c: Int): Unit
```

Writes a single character. The character to be written is contained in the 16 low-order bits of the given integer value; the 16 high-order bits are ignored.

Subclasses that intend to support efficient single-character output should override this method.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------|
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): int specifying a character to be written |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(str: String!): Unit
```

Writes a string.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: String to be written |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(
    str: String!, 
    off: Int, 
    len: Int
): Unit
```

Writes a portion of a string.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A String |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Offset from which to start writing characters |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of characters to write |
| --- | --- |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | Implementations should throw this exception if `off` is negative, or `len` is negative, or `off + len` is negative or greater than the length of the given string |
| `java.io.IOException` | If an I/O error occurs |

## Properties

### lock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var lock: Any!
```

The object used to synchronize operations on this stream. For efficiency, a character-stream object may use an object other than itself to protect critical sections. A subclass should therefore use the object in this field rather than `this` or a synchronized method.
