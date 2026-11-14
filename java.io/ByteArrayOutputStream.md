# ByteArrayOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ByteArrayOutputStream

```
open class ByteArrayOutputStream : OutputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.io.OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream) ||
| | ↳ | [java.io.ByteArrayOutputStream](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#) |

This class implements an output stream in which the data is written into a byte array. The buffer automatically grows as data is written to it. The data can be retrieved using`toByteArray()`and`toString()`.

Closing a`ByteArrayOutputStream`has no effect. The methods in this class can be called after the stream has been closed without generating an`IOException`.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ByteArrayOutputStream](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#ByteArrayOutputStream())`()` Creates a new`ByteArrayOutputStream`. |
| [ByteArrayOutputStream](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#ByteArrayOutputStream(kotlin.Int))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new`ByteArrayOutputStream`, with a buffer capacity of the specified size, in bytes. |

| Public methods ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#close())`()` Closing a`ByteArrayOutputStream`has no effect. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#reset())`()` Resets the`count`field of this`ByteArrayOutputStream`to zero, so that all currently accumulated output in the output stream is discarded. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#size())`()` Returns the current size of the buffer. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [toByteArray](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#toByteArray())`()` Creates a newly allocated byte array. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#toString())`()` Converts the buffer's contents into a string decoding bytes using the platform's default character set. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#toString(kotlin.Int))`(`hibyte:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a newly allocated string. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#toString(kotlin.String))`(`charsetName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Converts the buffer's contents into a string by decoding the bytes using the named [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#toString(java.nio.charset.Charset))`(`charset:` ` [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)`)` Converts the buffer's contents into a string by decoding the bytes using the specified [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#write(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes`len`bytes from the specified byte array starting at offset`off`to this`ByteArrayOutputStream`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#write(kotlin.Int))`(`b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes the specified byte to this`ByteArrayOutputStream`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeBytes](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#writeBytes(kotlin.ByteArray))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Writes the complete contents of the specified byte array to this`ByteArrayOutputStream`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeTo](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#writeTo(java.io.OutputStream))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream)`)` Writes the complete contents of this`ByteArrayOutputStream`to the specified output stream argument, as if by calling the output stream's write method using`out.write(buf, 0, count)`. |

| Inherited functions ||
|---|---|
| From class [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream) |--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](https://developer.android.com/reference/kotlin/java/io/OutputStream#flush())`()` <br /> Flushes this output stream and forces any buffered output bytes to be written out. The general contract of`flush`is that calling it is an indication that, if any bytes previously written have been buffered by the implementation of the output stream, such bytes should immediately be written to their intended destination. If the intended destination of this stream is an abstraction provided by the underlying operating system, for example a file, then flushing the stream guarantees only that bytes previously written to the stream are passed to the operating system for writing; it does not guarantee that they are actually written to a physical device such as a disk drive. The`flush`method of`OutputStream`does nothing. <br /> | | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream)! | [nullOutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream#nullOutputStream())`()` <br /> Returns a new`OutputStream`which discards all bytes. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`write(int)`,`write(byte[])`, and`write(byte[], int, int)`methods do nothing. After the stream has been closed, these methods all throw`IOException`. The`flush()`method does nothing. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/OutputStream#write(kotlin.ByteArray))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Writes`b.length`bytes from the specified byte array to this output stream. The general contract for`write(b)`is that it should have exactly the same effect as the call`write(b, 0, b.length)`. <br /> | ||

| Properties ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [buf](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#buf:kotlin.ByteArray) The buffer where data is stored. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [count](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#count:kotlin.Int) The number of valid bytes in the buffer. |

## Public constructors

### ByteArrayOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ByteArrayOutputStream()
```

Creates a new`ByteArrayOutputStream`. The buffer capacity is initially 32 bytes, though its size increases if necessary. 

### ByteArrayOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ByteArrayOutputStream(size: Int)
```

Creates a new`ByteArrayOutputStream`, with a buffer capacity of the specified size, in bytes.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------|
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial size. |

| Exceptions ||
|--------------------------------------|----------------------|
| `java.lang.IllegalArgumentException` | if size is negative. |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closing a`ByteArrayOutputStream`has no effect. The methods in this class can be called after the stream has been closed without generating an`IOException`.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs. |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Resets the`count`field of this`ByteArrayOutputStream`to zero, so that all currently accumulated output in the output stream is discarded. The output stream can be used again, reusing the already allocated buffer space. 
**See Also**

- [java.io.ByteArrayInputStream#count](https://developer.android.com/reference/kotlin/java/io/ByteArrayInputStream#count:kotlin.Int) 

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun size(): Int
```

Returns the current size of the buffer.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value of the`count`field, which is the number of valid bytes in this output stream. |

**See Also**

- [java.io.ByteArrayOutputStream#count](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#count:kotlin.Int) 

### toByteArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toByteArray(): ByteArray
```

Creates a newly allocated byte array. Its size is the current size of this output stream and the valid contents of the buffer have been copied into it.

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | the current contents of this output stream, as a byte array. |

**See Also**

- [java.io.ByteArrayOutputStream#size()](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#size()) 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Converts the buffer's contents into a string decoding bytes using the platform's default character set. The length of the new`String`is a function of the character set, and hence may not be equal to the size of the buffer.

This method always replaces malformed-input and unmappable-character sequences with the default replacement string for the platform's default character set. The [java.nio.charset.CharsetDecoder](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetDecoder.html#) class should be used when more control over the decoding process is required.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | String decoded from the buffer's contents. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(hibyte: Int): String
```

**Deprecated:** *This method does not properly convert bytes into characters. As of JDK 1.1, the preferred way to do this is via the [toString(java.lang.String)](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#toString(kotlin.String))or [toString(java.nio.charset.Charset)](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#toString(java.nio.charset.Charset))method, which takes an encoding-name or charset argument, or the`toString()`method, which uses the platform's default character encoding.*

Creates a newly allocated string. Its size is the current size of the output stream and the valid contents of the buffer have been copied into it. Each character*c* in the resulting string is constructed from the corresponding element*b*in the byte array such that: 

```kotlin
<code>c == (char)(((hibyte &amp; 0xff) &lt;&lt; 8) | (b &amp; 0xff))
  </code>
```

<br />

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `hibyte` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the high byte of each resulting Unicode character. |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the current contents of the output stream, as a string. |

**See Also**

- [java.io.ByteArrayOutputStream#size()](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#size())
- [java.io.ByteArrayOutputStream#toString(String)](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#toString(kotlin.String))
- [java.io.ByteArrayOutputStream#toString()](https://developer.android.com/reference/kotlin/java/io/ByteArrayOutputStream#toString()) 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(charsetName: String): String
```

Converts the buffer's contents into a string by decoding the bytes using the named [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#).

This method is equivalent to`toString(charset)`that takes a [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#).

An invocation of this method of the form 

```kotlin
<code>ByteArrayOutputStream b = ...
       b.toString("UTF-8")
       </code>
```
behaves in exactly the same way as the expression 

```kotlin
<code>ByteArrayOutputStream b = ...
       b.toString(StandardCharsets.UTF_8)
       </code>
```

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `charsetName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of a supported [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) |

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | String decoded from the buffer's contents. |

| Exceptions ||
|----------------------------------------|---------------------------------------|
| `java.io.UnsupportedEncodingException` | If the named charset is not supported |

### toString

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(charset: Charset): String
```

Converts the buffer's contents into a string by decoding the bytes using the specified [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#). The length of the new`String`is a function of the charset, and hence may not be equal to the length of the byte array.

This method always replaces malformed-input and unmappable-character sequences with the charset's default replacement string. The class should be used when more control over the decoding process is required.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `charset` | [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#):the [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) to be used to decode the`bytes` |

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | String decoded from the buffer's contents. |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(
    b: ByteArray, 
    off: Int, 
    len: Int
): Unit
```

Writes`len`bytes from the specified byte array starting at offset`off`to this`ByteArrayOutputStream`.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the data. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset in the data. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to write. |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs. In particular, an`IOException`is thrown if the output stream is closed. |
| `java.lang.NullPointerException` | if`b`is`null`. |
| `java.lang.IndexOutOfBoundsException` | if`off`is negative,`len`is negative, or`len`is greater than`b.length - off` |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(b: Int): Unit
```

Writes the specified byte to this`ByteArrayOutputStream`.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------|
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the byte to be written. |

| Exceptions ||
|-----------------------|-----------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs. In particular, an`IOException`may be thrown if the output stream has been closed. |

### writeBytes

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeBytes(b: ByteArray!): Unit
```

Writes the complete contents of the specified byte array to this`ByteArrayOutputStream`.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data. |

| Exceptions ||
|----------------------------------|----------------|
| `java.lang.NullPointerException` | if`b`is`null`. |

### writeTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeTo(out: OutputStream): Unit
```

Writes the complete contents of this`ByteArrayOutputStream`to the specified output stream argument, as if by calling the output stream's write method using`out.write(buf, 0, count)`.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream):the output stream to which to write the data. |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | if`out`is`null`. |
| `java.io.IOException` | if an I/O error occurs. |

## Properties

### buf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var buf: ByteArray
```

The buffer where data is stored. 

### count

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var count: Int
```

The number of valid bytes in the buffer.
