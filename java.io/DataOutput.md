# DataOutput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DataOutput

```
interface DataOutput
```

| [java.io.DataOutput](https://developer.android.com/reference/kotlin/java/io/DataOutput#) |

| Known Direct Subclasses [DataOutputStream](https://developer.android.com/reference/kotlin/java/io/DataOutputStream), [ObjectOutput](https://developer.android.com/reference/kotlin/java/io/ObjectOutput), [RandomAccessFile](https://developer.android.com/reference/kotlin/java/io/RandomAccessFile) |---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------| | [DataOutputStream](https://developer.android.com/reference/kotlin/java/io/DataOutputStream) | A data output stream lets an application write primitive Java data types to an output stream in a portable way. | | [ObjectOutput](https://developer.android.com/reference/kotlin/java/io/ObjectOutput) | ObjectOutput extends the DataOutput interface to include writing of objects. | | [RandomAccessFile](https://developer.android.com/reference/kotlin/java/io/RandomAccessFile) | Instances of this class support both reading and writing to a random access file. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ObjectOutputStream](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream) |-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------| | [ObjectOutputStream](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream) | An ObjectOutputStream writes primitive data types and graphs of Java objects to an OutputStream. | |
| --- | --- | --- | --- | --- | --- | --- |

The`DataOutput`interface provides for converting data from any of the Java primitive types to a series of bytes and writing these bytes to a binary stream. There is also a facility for converting a`String`into [modified UTF-8](https://developer.android.com/reference/kotlin/java/io/DataInput#modified-utf-8) format and writing the resulting series of bytes.

For all the methods in this interface that write bytes, it is generally true that if a byte cannot be written for any reason, an`IOException`is thrown.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/DataOutput#write(kotlin.ByteArray))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Writes to the output stream all the bytes in array`b`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/DataOutput#write(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes`len`bytes from array`b`, in order, to the output stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/DataOutput#write(kotlin.Int))`(`b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes to the output stream the eight low-order bits of the argument`b`. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeBoolean](https://developer.android.com/reference/kotlin/java/io/DataOutput#writeBoolean(kotlin.Boolean))`(`v:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Writes a`boolean`value to this output stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeByte](https://developer.android.com/reference/kotlin/java/io/DataOutput#writeByte(kotlin.Int))`(`v:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes to the output stream the eight low- order bits of the argument`v`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeBytes](https://developer.android.com/reference/kotlin/java/io/DataOutput#writeBytes(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Writes a string to the output stream. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeChar](https://developer.android.com/reference/kotlin/java/io/DataOutput#writeChar(kotlin.Int))`(`v:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a`char`value, which is comprised of two bytes, to the output stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeChars](https://developer.android.com/reference/kotlin/java/io/DataOutput#writeChars(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Writes every character in the string`s`, to the output stream, in order, two bytes per character. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeDouble](https://developer.android.com/reference/kotlin/java/io/DataOutput#writeDouble(kotlin.Double))`(`v:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Writes a`double`value, which is comprised of eight bytes, to the output stream. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeFloat](https://developer.android.com/reference/kotlin/java/io/DataOutput#writeFloat(kotlin.Float))`(`v:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Writes a`float`value, which is comprised of four bytes, to the output stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeInt](https://developer.android.com/reference/kotlin/java/io/DataOutput#writeInt(kotlin.Int))`(`v:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes an`int`value, which is comprised of four bytes, to the output stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeLong](https://developer.android.com/reference/kotlin/java/io/DataOutput#writeLong(kotlin.Long))`(`v:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Writes a`long`value, which is comprised of eight bytes, to the output stream. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeShort](https://developer.android.com/reference/kotlin/java/io/DataOutput#writeShort(kotlin.Int))`(`v:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes two bytes to the output stream to represent the value of the argument. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeUTF](https://developer.android.com/reference/kotlin/java/io/DataOutput#writeUTF(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Writes two bytes of length information to the output stream, followed by the [modified UTF-8](https://developer.android.com/reference/kotlin/java/io/DataInput#modified-utf-8) representation of every character in the string`s`. |

## Public methods

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun write(b: ByteArray!): Unit
```

Writes to the output stream all the bytes in array`b`. If`b`is`null`, a`NullPointerException`is thrown. If`b.length`is zero, then no bytes are written. Otherwise, the byte`b[0]`is written first, then`b[1]`, and so on; the last byte written is`b[b.length-1]`.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun write(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Writes`len`bytes from array`b`, in order, to the output stream. If`b`is`null`, a`NullPointerException`is thrown. If`off`is negative, or`len`is negative, or`off+len`is greater than the length of the array`b`, then an`IndexOutOfBoundsException`is thrown. If`len`is zero, then no bytes are written. Otherwise, the byte`b[off]`is written first, then`b[off+1]`, and so on; the last byte written is`b[off+len-1]`.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset in the data. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to write. |
| --- | --- |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun write(b: Int): Unit
```

Writes to the output stream the eight low-order bits of the argument`b`. The 24 high-order bits of`b`are ignored.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------|
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the byte to be written. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### writeBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeBoolean(v: Boolean): Unit
```

Writes a`boolean`value to this output stream. If the argument`v`is`true`, the value`(byte)1`is written; if`v`is`false`, the value`(byte)0`is written. The byte written by this method may be read by the`readBoolean`method of interface`DataInput`, which will then return a`boolean`equal to`v`.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------|
| `v` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the boolean to be written. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### writeByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeByte(v: Int): Unit
```

Writes to the output stream the eight low- order bits of the argument`v`. The 24 high-order bits of`v`are ignored. (This means that`writeByte`does exactly the same thing as`write`for an integer argument.) The byte written by this method may be read by the`readByte`method of interface`DataInput`, which will then return a`byte`equal to`(byte)v`.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------|
| `v` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the byte value to be written. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### writeBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeBytes(s: String!): Unit
```

Writes a string to the output stream. For every character in the string`s`, taken in order, one byte is written to the output stream. If`s`is`null`, a`NullPointerException`is thrown.

If`s.length`is zero, then no bytes are written. Otherwise, the character`s[0]`is written first, then`s[1]`, and so on; the last character written is`s[s.length-1]`. For each character, one byte is written, the low-order byte, in exactly the manner of the`writeByte`method . The high-order eight bits of each character in the string are ignored.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string of bytes to be written. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### writeChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeChar(v: Int): Unit
```

Writes a`char`value, which is comprised of two bytes, to the output stream. The byte values to be written, in the order shown, are: 

```kotlin
<code>(byte)(0xff &amp; (v &gt;&gt; 8))
  (byte)(0xff &amp; v)
  </code>
```

<br />

The bytes written by this method may be read by the`readChar`method of interface`DataInput`, which will then return a`char`equal to`(char)v`.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------|
| `v` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the`char`value to be written. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### writeChars

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeChars(s: String!): Unit
```

Writes every character in the string`s`, to the output stream, in order, two bytes per character. If`s`is`null`, a`NullPointerException`is thrown. If`s.length`is zero, then no characters are written. Otherwise, the character`s[0]`is written first, then`s[1]`, and so on; the last character written is`s[s.length-1]`. For each character, two bytes are actually written, high-order byte first, in exactly the manner of the`writeChar`method.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string value to be written. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### writeDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeDouble(v: Double): Unit
```

Writes a`double`value, which is comprised of eight bytes, to the output stream. It does this as if it first converts this`double`value to a`long`in exactly the manner of the`Double.doubleToLongBits`method and then writes the`long`value in exactly the manner of the`writeLong`method. The bytes written by this method may be read by the`readDouble`method of interface`DataInput`, which will then return a`double`equal to`v`.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------|
| `v` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the`double`value to be written. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### writeFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeFloat(v: Float): Unit
```

Writes a`float`value, which is comprised of four bytes, to the output stream. It does this as if it first converts this`float`value to an`int`in exactly the manner of the`Float.floatToIntBits`method and then writes the`int`value in exactly the manner of the`writeInt`method. The bytes written by this method may be read by the`readFloat`method of interface`DataInput`, which will then return a`float`equal to`v`.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------|
| `v` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the`float`value to be written. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### writeInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeInt(v: Int): Unit
```

Writes an`int`value, which is comprised of four bytes, to the output stream. The byte values to be written, in the order shown, are: 

```kotlin
<code>(byte)(0xff &amp; (v &gt;&gt; 24))
  (byte)(0xff &amp; (v &gt;&gt; 16))
  (byte)(0xff &amp; (v &gt;&gt;  8))
  (byte)(0xff &amp; v)
  </code>
```

<br />

The bytes written by this method may be read by the`readInt`method of interface`DataInput`, which will then return an`int`equal to`v`.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------|
| `v` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the`int`value to be written. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### writeLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeLong(v: Long): Unit
```

Writes a`long`value, which is comprised of eight bytes, to the output stream. The byte values to be written, in the order shown, are: 

```kotlin
<code>(byte)(0xff &amp; (v &gt;&gt; 56))
  (byte)(0xff &amp; (v &gt;&gt; 48))
  (byte)(0xff &amp; (v &gt;&gt; 40))
  (byte)(0xff &amp; (v &gt;&gt; 32))
  (byte)(0xff &amp; (v &gt;&gt; 24))
  (byte)(0xff &amp; (v &gt;&gt; 16))
  (byte)(0xff &amp; (v &gt;&gt;  8))
  (byte)(0xff &amp; v)
  </code>
```

<br />

The bytes written by this method may be read by the`readLong`method of interface`DataInput`, which will then return a`long`equal to`v`.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------|
| `v` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the`long`value to be written. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### writeShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeShort(v: Int): Unit
```

Writes two bytes to the output stream to represent the value of the argument. The byte values to be written, in the order shown, are: 

```kotlin
<code>(byte)(0xff &amp; (v &gt;&gt; 8))
  (byte)(0xff &amp; v)
  </code>
```

<br />

The bytes written by this method may be read by the`readShort`method of interface`DataInput`, which will then return a`short`equal to`(short)v`.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------|
| `v` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the`short`value to be written. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### writeUTF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeUTF(s: String!): Unit
```

Writes two bytes of length information to the output stream, followed by the [modified UTF-8](https://developer.android.com/reference/kotlin/java/io/DataInput#modified-utf-8) representation of every character in the string`s`. If`s`is`null`, a`NullPointerException`is thrown. Each character in the string`s`is converted to a group of one, two, or three bytes, depending on the value of the character.

If a character`c`is in the range`\u0001`through`\u007f`, it is represented by one byte: 

```kotlin
(byte)c 
```

If a character`c`is`\u0000`or is in the range`\u0080`through`\u07ff`, then it is represented by two bytes, to be written in the order shown: 

```kotlin
<code>(byte)(0xc0 | (0x1f &amp; (c &gt;&gt; 6)))
  (byte)(0x80 | (0x3f &amp; c))
  </code>
```

If a character`c`is in the range`\u0800`through`uffff`, then it is represented by three bytes, to be written in the order shown: 

```kotlin
<code>(byte)(0xe0 | (0x0f &amp; (c &gt;&gt; 12)))
  (byte)(0x80 | (0x3f &amp; (c &gt;&gt;  6)))
  (byte)(0x80 | (0x3f &amp; c))
  </code>
```

First, the total number of bytes needed to represent all the characters of`s`is calculated. If this number is larger than`65535`, then a`UTFDataFormatException`is thrown. Otherwise, this length is written to the output stream in exactly the manner of the`writeShort`method; after this, the one-, two-, or three-byte representation of each character in the string`s`is written.

The bytes written by this method may be read by the`readUTF`method of interface`DataInput`, which will then return a`String`equal to`s`.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string value to be written. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |
