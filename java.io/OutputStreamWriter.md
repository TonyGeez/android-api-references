# OutputStreamWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OutputStreamWriter

```
open class OutputStreamWriter : Writer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.io.Writer](../java/io/Writer.md) ||
| | ↳ | [java.io.OutputStreamWriter](../java/io/OutputStreamWriter.md) |

| Known Direct Subclasses [FileWriter](../java/io/FileWriter.md) |---------------------------------------------------------------------------------|-------------------------------------------------------------| | [FileWriter](../java/io/FileWriter.md) | Writes text to character files using a default buffer size. | |
| --- | --- | --- | --- | --- | --- | --- |

An OutputStreamWriter is a bridge from character streams to byte streams: Characters written to it are encoded into bytes using a specified . The charset that it uses may be specified by name or may be given explicitly, or the platform's default charset may be accepted.

Each invocation of a write() method causes the encoding converter to be invoked on the given character(s). The resulting bytes are accumulated in a buffer before being written to the underlying output stream. Note that the characters passed to the write() methods are not buffered.

For top efficiency, consider wrapping an OutputStreamWriter within a BufferedWriter so as to avoid frequent converter invocations. For example: 

```kotlin
Writer out
    = new BufferedWriter(new OutputStreamWriter(System.out));
  
```

A*surrogate pair* is a character represented by a sequence of two`char`values: A*high* surrogate in the range '\\uD800' to '\\uDBFF' followed by a*low*surrogate in the range '\\uDC00' to '\\uDFFF'.

A*malformed surrogate element*is a high surrogate that is not followed by a low surrogate or a low surrogate that is not preceded by a high surrogate.

This class always replaces malformed surrogate elements and unmappable character sequences with the charset's default*substitution sequence* . The [java.nio.charset.CharsetEncoder](../java/nio/charset/CharsetEncoder.md) class should be used when more control over the encoding process is required.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [OutputStreamWriter](../java/io/OutputStreamWriter.md))`(`out:` ` [OutputStream](../java/io/OutputStream.md)!`)` Creates an OutputStreamWriter that uses the default character encoding. |
| [OutputStreamWriter](../java/io/OutputStreamWriter.md))`(`out:` ` [OutputStream](../java/io/OutputStream.md)!`, `charsetName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates an OutputStreamWriter that uses the named charset. |
| [OutputStreamWriter](../java/io/OutputStreamWriter.md))`(`out:` ` [OutputStream](../java/io/OutputStream.md)!`, `cs:` ` [Charset](../java/nio/charset/Charset.md)!`)` Creates an OutputStreamWriter that uses the given charset. |
| [OutputStreamWriter](../java/io/OutputStreamWriter.md))`(`out:` ` [OutputStream](../java/io/OutputStream.md)!`, `enc:` ` [CharsetEncoder](../java/nio/charset/CharsetEncoder.md)!`)` Creates an OutputStreamWriter that uses the given charset encoder. |

| Public methods ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Writer](../java/io/Writer.md) | [append](../java/io/OutputStreamWriter.md))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` <br /> |
| open [Writer](../java/io/Writer.md) | [append](../java/io/OutputStreamWriter.md))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/io/OutputStreamWriter.md))`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](../java/io/OutputStreamWriter.md))`()` Flushes the stream. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEncoding](../java/io/OutputStreamWriter.md))`()` Returns the name of the character encoding being used by this stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../java/io/OutputStreamWriter.md))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a portion of an array of characters. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../java/io/OutputStreamWriter.md))`(`c:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a single character. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../java/io/OutputStreamWriter.md))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a portion of a string. |

| Inherited functions ||
|---|---|
| From class [Writer](../java/io/Writer.md) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Writer](../java/io/Writer.md) | [append](../java/io/Writer.md))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` <br /> Appends the specified character to this writer. An invocation of this method of the form`out.append(c)`behaves in exactly the same way as the invocation ```kotlin out.write(c) ``` <br /> | | [Writer](../java/io/Writer.md)! | [nullWriter](../java/io/Writer.md))`()` <br /> Returns a new`Writer`which discards all characters. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`append(char)`,`append(CharSequence)`,`append(CharSequence, int, int)`,`flush()`,`write(int)`,`write(char[])`, and`write(char[], int, int)`methods do nothing. After the stream has been closed, these methods all throw`IOException`. The [object](../java/io/Writer.md) used to synchronize operations on the returned`Writer`is not specified. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../java/io/Writer.md))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` <br /> Writes an array of characters. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../java/io/Writer.md))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Writes a string. <br /> | ||

| Inherited properties ||
|---|---|
| From class [Writer](../java/io/Writer.md) |-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [lock](../java/io/Writer.md) <br /> The object used to synchronize operations on this stream. For efficiency, a character-stream object may use an object other than itself to protect critical sections. A subclass should therefore use the object in this field rather than`this`or a synchronized method. <br /> | ||

## Public constructors

### OutputStreamWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OutputStreamWriter(out: OutputStream!)
```

Creates an OutputStreamWriter that uses the default character encoding.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](../java/io/OutputStream.md)!:An OutputStream |

### OutputStreamWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OutputStreamWriter(
    out: OutputStream!, 
    charsetName: String!)
```

Creates an OutputStreamWriter that uses the named charset.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](../java/io/OutputStream.md)!:An OutputStream |
| `charsetName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of a supported [charset](../java/nio/charset/Charset.md) |

| Exceptions ||
|----------------------------------------|----------------------------------------|
| `java.io.UnsupportedEncodingException` | If the named encoding is not supported |

### OutputStreamWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OutputStreamWriter(
    out: OutputStream!, 
    cs: Charset!)
```

Creates an OutputStreamWriter that uses the given charset.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](../java/io/OutputStream.md)!:An OutputStream |
| `cs` | [Charset](../java/nio/charset/Charset.md)!:A charset |

### OutputStreamWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OutputStreamWriter(
    out: OutputStream!, 
    enc: CharsetEncoder!)
```

Creates an OutputStreamWriter that uses the given charset encoder.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](../java/io/OutputStream.md)!:An OutputStream |
| `enc` | [CharsetEncoder](../java/nio/charset/CharsetEncoder.md)!:A charset encoder |

## Public methods

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun append(csq: CharSequence?): Writer
```

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `csq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:The character sequence to append. If`csq`is`null`, then the four characters`"null"`are appended to this writer. |

| Return ||
|-------------------------------------------------------------------------|-------------|
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

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `csq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:The character sequence from which a subsequence will be appended. If`csq`is`null`, then characters will be appended as if`csq`contained the four characters`"null"`. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the first character in the subsequence |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the character following the last character in the subsequence |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------|-------------|
| [Writer](../java/io/Writer.md) | This writer |

| Exceptions ||
|---------------------------------------|------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`start`or`end`are negative,`start`is greater than`end`, or`end`is greater than`csq.length()` |
| `java.io.IOException` | If an I/O error occurs |

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

### getEncoding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEncoding(): String!
```

Returns the name of the character encoding being used by this stream.

If the encoding has an historical name then that name is returned; otherwise the encoding's canonical name is returned.

If this instance was created with the [OutputStreamWriter(java.io.OutputStream,java.lang.String)](../java/io/OutputStreamWriter.md))constructor then the returned name, being unique for the encoding, may differ from the name passed to the constructor. This method may return`null`if the stream has been closed.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The historical name of this encoding, or possibly`null`if the stream has been closed |

**See Also**

- [java.nio.charset.Charset](../java/nio/charset/Charset.md) 

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

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------|
| `cbuf` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:Buffer of characters |
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

Writes a single character.

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

Writes a portion of a string.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A String |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset from which to start writing characters |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of characters to write |
| --- | --- |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`off`is negative, or`len`is negative, or`off + len`is negative or greater than the length of the given string |
| `java.io.IOException` | If an I/O error occurs |
