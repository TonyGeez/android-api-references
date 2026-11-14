# StringWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StringWriter

```
open class StringWriter : Writer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.io.Writer](Writer.md) ||
| | ↳ | [java.io.StringWriter](StringWriter.md) |

A character stream that collects its output in a string buffer, which can then be used to construct a string.

Closing a`StringWriter`has no effect. The methods in this class can be called after the stream has been closed without generating an`IOException`.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StringWriter](StringWriter.md))`()` Create a new string writer using the default initial string-buffer size. |
| [StringWriter](StringWriter.md))`(`initialSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new string writer using the specified initial string-buffer size. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [StringWriter](StringWriter.md) | [append](StringWriter.md))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Appends the specified character to this writer. |
| open [StringWriter](StringWriter.md) | [append](StringWriter.md))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Appends the specified character sequence to this writer. |
| open [StringWriter](StringWriter.md) | [append](StringWriter.md))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Appends a subsequence of the specified character sequence to this writer. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](StringWriter.md))`()` Closing a`StringWriter`has no effect. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](StringWriter.md))`()` Flush the stream. |
| open [StringBuffer](../java.lang/StringBuffer.md)! | [getBuffer](StringWriter.md))`()` Return the string buffer itself. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](StringWriter.md))`()` Return the buffer's current value as a string. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](StringWriter.md))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Write a portion of an array of characters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](StringWriter.md))`(`c:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Write a single character. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](StringWriter.md))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Write a string. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](StringWriter.md))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Write a portion of a string. |

| Inherited functions ||
|---|---|
| From class [Writer](Writer.md) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Writer](Writer.md)! | [nullWriter](Writer.md))`()` <br /> Returns a new`Writer`which discards all characters. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`append(char)`,`append(CharSequence)`,`append(CharSequence, int, int)`,`flush()`,`write(int)`,`write(char[])`, and`write(char[], int, int)`methods do nothing. After the stream has been closed, these methods all throw`IOException`. The [object](Writer.md) used to synchronize operations on the returned`Writer`is not specified. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](Writer.md))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` <br /> Writes an array of characters. <br /> | ||

| Inherited properties ||
|---|---|
| From class [Writer](Writer.md) |-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [lock](Writer.md) <br /> The object used to synchronize operations on this stream. For efficiency, a character-stream object may use an object other than itself to protect critical sections. A subclass should therefore use the object in this field rather than`this`or a synchronized method. <br /> | ||

## Public constructors

### StringWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StringWriter()
```

Create a new string writer using the default initial string-buffer size. 

### StringWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StringWriter(initialSize: Int)
```

Create a new string writer using the specified initial string-buffer size.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `initialSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of`char`values that will fit into this buffer before it is automatically expanded |

| Exceptions ||
|--------------------------------------|----------------------------|
| `java.lang.IllegalArgumentException` | If`initialSize`is negative |

## Public methods

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun append(c: Char): StringWriter
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
|--------------------------------------------------------------------------------------|-------------|
| [StringWriter](StringWriter.md) | This writer |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun append(csq: CharSequence?): StringWriter
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
|--------------------------------------------------------------------------------------|-------------|
| [StringWriter](StringWriter.md) | This writer |

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
): StringWriter
```

Appends a subsequence of the specified character sequence to this writer.

An invocation of this method of the form`out.append(csq, start, end)`when`csq`is not`null`, behaves in exactly the same way as the invocation 

```kotlin
<code>out.write(csq.subSequence(start, end).toString())
  </code>
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `csq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:The character sequence from which a subsequence will be appended. If`csq`is`null`, then characters will be appended as if`csq`contained the four characters`"null"`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the first character in the subsequence |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the character following the last character in the subsequence |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------|-------------|
| [StringWriter](StringWriter.md) | This writer |

| Exceptions ||
|---------------------------------------|------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`start`or`end`are negative,`start`is greater than`end`, or`end`is greater than`csq.length()` |
| `java.io.IOException` | If an I/O error occurs |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closing a`StringWriter`has no effect. The methods in this class can be called after the stream has been closed without generating an`IOException`.

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

### getBuffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBuffer(): StringBuffer!
```

Return the string buffer itself.

| Return ||
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| [StringBuffer](../java.lang/StringBuffer.md)! | StringBuffer holding the current buffer value. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Return the buffer's current value as a string.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(
    cbuf: CharArray!, 
    off: Int, 
    len: Int
): Unit
```

Write a portion of an array of characters.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------|
| `cbuf` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:Array of characters |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset from which to start writing characters |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of characters to write |
| --- | --- |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`off`is negative, or`len`is negative, or`off + len`is negative or greater than the length of the given array |
| `java.io.IOException` | If an I/O error occurs |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(c: Int): Unit
```

Write a single character.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------|
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):int specifying a character to be written |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(str: String!): Unit
```

Write a string.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:String to be written |

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

Write a portion of a string.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:String to be written |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset from which to start writing characters |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of characters to write |
| --- | --- |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`off`is negative, or`len`is negative, or`off + len`is negative or greater than the length of the given string |
| `java.io.IOException` | If an I/O error occurs |
