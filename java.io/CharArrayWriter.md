# CharArrayWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CharArrayWriter

```
open class CharArrayWriter : Writer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.io.Writer](Writer.md) ||
| | ↳ | [java.io.CharArrayWriter](CharArrayWriter.md) |

This class implements a character buffer that can be used as an Writer. The buffer automatically grows when data is written to the stream. The data can be retrieved using toCharArray() and toString().

Note: Invoking close() on this class has no effect, and methods of this class can be called after the stream has closed without generating an IOException.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CharArrayWriter](CharArrayWriter.md))`()` Creates a new CharArrayWriter. |
| [CharArrayWriter](CharArrayWriter.md))`(`initialSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new CharArrayWriter with the specified initial size. |

| Public methods ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [CharArrayWriter](CharArrayWriter.md) | [append](CharArrayWriter.md))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Appends the specified character to this writer. |
| open [CharArrayWriter](CharArrayWriter.md) | [append](CharArrayWriter.md))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Appends the specified character sequence to this writer. |
| open [CharArrayWriter](CharArrayWriter.md) | [append](CharArrayWriter.md))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Appends a subsequence of the specified character sequence to this writer. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](CharArrayWriter.md))`()` Close the stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](CharArrayWriter.md))`()` Flush the stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](CharArrayWriter.md))`()` Resets the buffer so that you can use it again without throwing away the already allocated buffer. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](CharArrayWriter.md))`()` Returns the current size of the buffer. |
| open [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [toCharArray](CharArrayWriter.md))`()` Returns a copy of the input data. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](CharArrayWriter.md))`()` Converts input data to a string. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](CharArrayWriter.md))`(`c:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes characters to the buffer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](CharArrayWriter.md))`(`c:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a character to the buffer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](CharArrayWriter.md))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Write a portion of a string to the buffer. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeTo](CharArrayWriter.md))`(`out:` ` [Writer](Writer.md)!`)` Writes the contents of the buffer to another character stream. |

| Inherited functions ||
|---|---|
| From class [Writer](Writer.md) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Writer](Writer.md)! | [nullWriter](Writer.md))`()` <br /> Returns a new`Writer`which discards all characters. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`append(char)`,`append(CharSequence)`,`append(CharSequence, int, int)`,`flush()`,`write(int)`,`write(char[])`, and`write(char[], int, int)`methods do nothing. After the stream has been closed, these methods all throw`IOException`. The [object](Writer.md) used to synchronize operations on the returned`Writer`is not specified. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](Writer.md))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` <br /> Writes an array of characters. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](Writer.md))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Writes a string. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [buf](CharArrayWriter.md) The buffer where data is stored. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [count](CharArrayWriter.md) The number of chars in the buffer. |

| Inherited properties ||
|---|---|
| From class [Writer](Writer.md) |-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [lock](Writer.md) <br /> The object used to synchronize operations on this stream. For efficiency, a character-stream object may use an object other than itself to protect critical sections. A subclass should therefore use the object in this field rather than`this`or a synchronized method. <br /> | ||

## Public constructors

### CharArrayWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CharArrayWriter()
```

Creates a new CharArrayWriter. 

### CharArrayWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CharArrayWriter(initialSize: Int)
```

Creates a new CharArrayWriter with the specified initial size.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------|
| `initialSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an int specifying the initial buffer size. |

| Exceptions ||
|--------------------------------------|----------------------------|
| `java.lang.IllegalArgumentException` | if initialSize is negative |

## Public methods

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun append(c: Char): CharArrayWriter
```

Appends the specified character to this writer.

An invocation of this method of the form`out.append(c)`behaves in exactly the same way as the invocation 

```kotlin
out.write(c) 
```

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------|
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The 16-bit character to append |

| Return ||
|--------------------------------------------------------------------------------------------|-------------|
| [CharArrayWriter](CharArrayWriter.md) | This writer |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun append(csq: CharSequence?): CharArrayWriter
```

Appends the specified character sequence to this writer.

An invocation of this method of the form`out.append(csq)`behaves in exactly the same way as the invocation 

```kotlin
out.write(csq.toString()) 
```

Depending on the specification of`toString`for the character sequence`csq`, the entire sequence may not be appended. For instance, invoking the`toString`method of a character buffer will return a subsequence whose content depends upon the buffer's position and limit.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `csq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:The character sequence to append. If`csq`is`null`, then the four characters`"null"`are appended to this writer. |

| Return ||
|--------------------------------------------------------------------------------------------|-------------|
| [CharArrayWriter](CharArrayWriter.md) | This writer |

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
): CharArrayWriter
```

Appends a subsequence of the specified character sequence to this writer.

An invocation of this method of the form`out.append(csq, start, end)`when`csq`is not`null`, behaves in exactly the same way as the invocation 

```kotlin
out.write(csq.subSequence(start, end).toString()) 
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `csq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:The character sequence from which a subsequence will be appended. If`csq`is`null`, then characters will be appended as if`csq`contained the four characters`"null"`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the first character in the subsequence |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the character following the last character in the subsequence |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------|-------------|
| [CharArrayWriter](CharArrayWriter.md) | This writer |

| Exceptions ||
|---------------------------------------|------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`start`or`end`are negative,`start`is greater than`end`, or`end`is greater than`csq.length()` |
| `java.io.IOException` | If an I/O error occurs |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Close the stream. This method does not release the buffer, since its contents might still be required. Note: Invoking this method in this class will have no effect.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | If an I/O error occurs |

### flush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun flush(): Unit
```

Flush the stream.

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Resets the buffer so that you can use it again without throwing away the already allocated buffer. 

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun size(): Int
```

Returns the current size of the buffer.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an int representing the current size of the buffer. |

### toCharArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toCharArray(): CharArray!
```

Returns a copy of the input data.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------|
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | an array of chars copied from the input data. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Converts input data to a string.

| Return ||
|----------------------------------------------------------------------------------|-------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the string. |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(
    c: CharArray!, 
    off: Int, 
    len: Int
): Unit
```

Writes characters to the buffer.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------|
| `cbuf` | Array of characters |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset in the data |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of chars that are written |
| --- | --- |
| `c` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the data to be written |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`off`is negative, or`len`is negative, or`off + len`is negative or greater than the length of the given array |
| `java.io.IOException` | If an I/O error occurs |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(c: Int): Unit
```

Writes a character to the buffer.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------|
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):int specifying a character to be written |

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

Write a portion of a string to the buffer.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:String to be written from |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset from which to start reading characters |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of characters to be written |
| --- | --- |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`off`is negative, or`len`is negative, or`off + len`is negative or greater than the length of the given string |
| `java.io.IOException` | If an I/O error occurs |

### writeTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeTo(out: Writer!): Unit
```

Writes the contents of the buffer to another character stream.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------|
| `out` | [Writer](Writer.md)!:the output stream to write to |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | If an I/O error occurs. |

## Properties

### buf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var buf: CharArray!
```

The buffer where data is stored. 

### count

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var count: Int
```

The number of chars in the buffer.
