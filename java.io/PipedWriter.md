# PipedWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PipedWriter

```
open class PipedWriter : Writer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.io.Writer](https://developer.android.com/reference/kotlin/java/io/Writer) ||
| | ↳ | [java.io.PipedWriter](https://developer.android.com/reference/kotlin/java/io/PipedWriter#) |

Piped character-output streams.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PipedWriter](https://developer.android.com/reference/kotlin/java/io/PipedWriter#PipedWriter())`()` Creates a piped writer that is not yet connected to a piped reader. |
| [PipedWriter](https://developer.android.com/reference/kotlin/java/io/PipedWriter#PipedWriter(java.io.PipedReader))`(`snk:` ` [PipedReader](https://developer.android.com/reference/kotlin/java/io/PipedReader)!`)` Creates a piped writer connected to the specified piped reader. |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/io/PipedWriter#close())`()` Closes this piped output stream and releases any system resources associated with this stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/java/io/PipedWriter#connect(java.io.PipedReader))`(`snk:` ` [PipedReader](https://developer.android.com/reference/kotlin/java/io/PipedReader)!`)` Connects this piped writer to a receiver. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](https://developer.android.com/reference/kotlin/java/io/PipedWriter#flush())`()` Flushes this output stream and forces any buffered output characters to be written out. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/PipedWriter#write(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes`len`characters from the specified character array starting at offset`off`to this piped output stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/PipedWriter#write(kotlin.Int))`(`c:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes the specified`char`to the piped output stream. |

| Inherited functions ||
|---|---|
| From class [Writer](https://developer.android.com/reference/kotlin/java/io/Writer) |------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Writer](https://developer.android.com/reference/kotlin/java/io/Writer) | [append](https://developer.android.com/reference/kotlin/java/io/Writer#append(kotlin.Char))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` <br /> Appends the specified character to this writer. An invocation of this method of the form`out.append(c)`behaves in exactly the same way as the invocation ```kotlin out.write(c) ``` <br /> | | [Writer](https://developer.android.com/reference/kotlin/java/io/Writer) | [append](https://developer.android.com/reference/kotlin/java/io/Writer#append(kotlin.CharSequence))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` <br /> Appends the specified character sequence to this writer. An invocation of this method of the form`out.append(csq)`behaves in exactly the same way as the invocation ```kotlin out.write(csq.toString()) ``` Depending on the specification of`toString`for the character sequence`csq`, the entire sequence may not be appended. For instance, invoking the`toString`method of a character buffer will return a subsequence whose content depends upon the buffer's position and limit. <br /> | | [Writer](https://developer.android.com/reference/kotlin/java/io/Writer) | [append](https://developer.android.com/reference/kotlin/java/io/Writer#append(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int))`(`csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Appends a subsequence of the specified character sequence to this writer.`Appendable`. An invocation of this method of the form`out.append(csq, start, end)`when`csq`is not`null`behaves in exactly the same way as the invocation ```kotlin <code>out.write(csq.subSequence(start, end).toString()) </code> ``` <br /> | | [Writer](https://developer.android.com/reference/kotlin/java/io/Writer)! | [nullWriter](https://developer.android.com/reference/kotlin/java/io/Writer#nullWriter())`()` <br /> Returns a new`Writer`which discards all characters. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`append(char)`,`append(CharSequence)`,`append(CharSequence, int, int)`,`flush()`,`write(int)`,`write(char[])`, and`write(char[], int, int)`methods do nothing. After the stream has been closed, these methods all throw`IOException`. The [object](https://developer.android.com/reference/kotlin/java/io/Writer#lock:kotlin.Any) used to synchronize operations on the returned`Writer`is not specified. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/Writer#write(kotlin.CharArray))`(`cbuf:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` <br /> Writes an array of characters. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/Writer#write(kotlin.String))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Writes a string. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/Writer#write(kotlin.String,%20kotlin.Int,%20kotlin.Int))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Writes a portion of a string. <br /> | ||

| Inherited properties ||
|---|---|
| From class [Writer](https://developer.android.com/reference/kotlin/java/io/Writer) |-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [lock](https://developer.android.com/reference/kotlin/java/io/Writer#lock:kotlin.Any) <br /> The object used to synchronize operations on this stream. For efficiency, a character-stream object may use an object other than itself to protect critical sections. A subclass should therefore use the object in this field rather than`this`or a synchronized method. <br /> | ||

## Public constructors

### PipedWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PipedWriter()
```

Creates a piped writer that is not yet connected to a piped reader. It must be connected to a piped reader, either by the receiver or the sender, before being used. 
**See Also**

- [java.io.PipedReader#connect(java.io.PipedWriter)](https://developer.android.com/reference/kotlin/java/io/PipedReader#connect(java.io.PipedWriter))
- [java.io.PipedWriter#connect(java.io.PipedReader)](https://developer.android.com/reference/kotlin/java/io/PipedWriter#connect(java.io.PipedReader)) 

### PipedWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PipedWriter(snk: PipedReader!)
```

Creates a piped writer connected to the specified piped reader. Data characters written to this stream will then be available as input from`snk`.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------|
| `snk` | [PipedReader](https://developer.android.com/reference/kotlin/java/io/PipedReader)!:The piped reader to connect to. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes this piped output stream and releases any system resources associated with this stream. This stream may no longer be used for writing characters.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | If an I/O error occurs |
| `java.io.IOException` | if an I/O error occurs. |
| --- | --- |

### connect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun connect(snk: PipedReader!): Unit
```

Connects this piped writer to a receiver. If this object is already connected to some other piped reader, an`IOException`is thrown.

If`snk`is an unconnected piped reader and`src`is an unconnected piped writer, they may be connected by either the call: 

```kotlin
src.connect(snk)
```
or the call: 

```kotlin
snk.connect(src)
```
The two calls have the same effect.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------|
| `snk` | [PipedReader](https://developer.android.com/reference/kotlin/java/io/PipedReader)!:the piped reader to connect to. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### flush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun flush(): Unit
```

Flushes this output stream and forces any buffered output characters to be written out. This will notify any readers that characters are waiting in the pipe.

| Exceptions ||
|-----------------------|------------------------------------------------|
| `java.io.IOException` | If an I/O error occurs |
| `java.io.IOException` | if the pipe is closed, or an I/O error occurs. |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(
    cbuf: CharArray!, 
    off: Int, 
    len: Int
): Unit
```

Writes`len`characters from the specified character array starting at offset`off`to this piped output stream. This method blocks until all the characters are written to the output stream. If a thread was reading data characters from the connected piped input stream, but the thread is no longer alive, then an`IOException`is thrown.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------|
| `cbuf` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the data. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset in the data. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of characters to write. |
| --- | --- |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If`off`is negative, or`len`is negative, or`off + len`is negative or greater than the length of the given array |
| `java.io.IOException` | if the pipe is [`broken`](https://developer.android.com/reference/kotlin/java/io/PipedOutputStream#BROKEN), [unconnected](https://developer.android.com/reference/kotlin/java/io/PipedWriter#connect(java.io.PipedReader)), closed or an I/O error occurs. |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(c: Int): Unit
```

Writes the specified`char`to the piped output stream. If a thread was reading data characters from the connected piped input stream, but the thread is no longer alive, then an`IOException`is thrown.

Implements the`write`method of`Writer`.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------|
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the`char`to be written. |

| Exceptions ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | If an I/O error occurs |
| `java.io.IOException` | if the pipe is [`broken`](https://developer.android.com/reference/kotlin/java/io/PipedOutputStream#BROKEN), [unconnected](https://developer.android.com/reference/kotlin/java/io/PipedWriter#connect(java.io.PipedReader)), closed or an I/O error occurs. |
