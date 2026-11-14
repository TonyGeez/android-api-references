# FilterWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FilterWriter

```
abstract class FilterWriter : Writer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.io.Writer](https://developer.android.com/reference/kotlin/java/io/Writer) ||
| | ↳ | [java.io.FilterWriter](https://developer.android.com/reference/kotlin/java/io/FilterWriter#) |

Abstract class for writing filtered character streams. The abstract class`FilterWriter`itself provides default methods that pass all requests to the contained stream. Subclasses of`FilterWriter`should override some of these methods and may also provide additional methods and fields.

## Summary

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FilterWriter](https://developer.android.com/reference/kotlin/java/io/FilterWriter#FilterWriter(java.io.Writer))`(`out:` ` [Writer](https://developer.android.com/reference/kotlin/java/io/Writer)!`)` Create a new filtered writer. |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/io/FilterWriter#close())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](https://developer.android.com/reference/kotlin/java/io/FilterWriter#flush())`()` Flushes the stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/FilterWriter#write(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a portion of an array of characters. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/FilterWriter#write(kotlin.Int))`(`c:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a single character. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/FilterWriter#write(kotlin.String,%20kotlin.Int,%20kotlin.Int))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a portion of a string. |

| Inherited functions ||
|---|---|
| From class [Writer](https://developer.android.com/reference/kotlin/java/io/Writer) |------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Writer](https://developer.android.com/reference/kotlin/java/io/Writer) | [append](https://developer.android.com/reference/kotlin/java/io/Writer#append(kotlin.Char))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` <br /> Appends the specified character to this writer. An invocation of this method of the form`out.append(c)`behaves in exactly the same way as the invocation ```kotlin out.write(c) ``` <br /> | | [Writer](https://developer.android.com/reference/kotlin/java/io/Writer) | [append](https://developer.android.com/reference/kotlin/java/io/Writer#append(kotlin.CharSequence))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` <br /> Appends the specified character sequence to this writer. An invocation of this method of the form`out.append(csq)`behaves in exactly the same way as the invocation ```kotlin out.write(csq.toString()) ``` Depending on the specification of`toString`for the character sequence`csq`, the entire sequence may not be appended. For instance, invoking the`toString`method of a character buffer will return a subsequence whose content depends upon the buffer's position and limit. <br /> | | [Writer](https://developer.android.com/reference/kotlin/java/io/Writer) | [append](https://developer.android.com/reference/kotlin/java/io/Writer#append(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Appends a subsequence of the specified character sequence to this writer.`Appendable`. An invocation of this method of the form`out.append(csq, start, end)`when`csq`is not`null`behaves in exactly the same way as the invocation ```kotlin <code>out.write(csq.subSequence(start, end).toString()) </code> ``` <br /> | | [Writer](https://developer.android.com/reference/kotlin/java/io/Writer)! | [nullWriter](https://developer.android.com/reference/kotlin/java/io/Writer#nullWriter())`()` <br /> Returns a new`Writer`which discards all characters. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`append(char)`,`append(CharSequence)`,`append(CharSequence, int, int)`,`flush()`,`write(int)`,`write(char[])`, and`write(char[], int, int)`methods do nothing. After the stream has been closed, these methods all throw`IOException`. The [object](https://developer.android.com/reference/kotlin/java/io/Writer#lock:kotlin.Any) used to synchronize operations on the returned`Writer`is not specified. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/Writer#write(kotlin.CharArray))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` <br /> Writes an array of characters. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/Writer#write(kotlin.String))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Writes a string. <br /> | ||

| Properties ||
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Writer](https://developer.android.com/reference/kotlin/java/io/Writer)! | [out](https://developer.android.com/reference/kotlin/java/io/FilterWriter#out:java.io.Writer) The underlying character-output stream. |

| Inherited properties ||
|---|---|
| From class [Writer](https://developer.android.com/reference/kotlin/java/io/Writer) |-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [lock](https://developer.android.com/reference/kotlin/java/io/Writer#lock:kotlin.Any) <br /> The object used to synchronize operations on this stream. For efficiency, a character-stream object may use an object other than itself to protect critical sections. A subclass should therefore use the object in this field rather than`this`or a synchronized method. <br /> | ||

## Protected constructors

### FilterWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected FilterWriter(out: Writer!)
```

Create a new filtered writer.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------|
| `out` | [Writer](https://developer.android.com/reference/kotlin/java/io/Writer)!:a Writer object to provide the underlying stream. |

| Exceptions ||
|----------------------------------|-----------------|
| `java.lang.NullPointerException` | if`out`is`null` |

## Public methods

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
| `java.io.IOException` | If an I/O error occurs |

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
|--------|-----------------------------------------------------------------------------------------------------------------------------|
| `cbuf` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:Buffer of characters to be written |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset from which to start reading characters |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of characters to be written |
| --- | --- |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the values of the`off`and`len`parameters cause the corresponding method of the underlying`Writer`to throw an`IndexOutOfBoundsException` |
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
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:String to be written |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset from which to start reading characters |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Number of characters to be written |
| --- | --- |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the values of the`off`and`len`parameters cause the corresponding method of the underlying`Writer`to throw an`IndexOutOfBoundsException` |
| `java.io.IOException` | If an I/O error occurs |

## Properties

### out

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var out: Writer!
```

The underlying character-output stream.
