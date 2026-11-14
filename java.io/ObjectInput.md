# ObjectInput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ObjectInput

```
interface ObjectInput : AutoCloseable, DataInput
```

| [java.io.ObjectInput](https://developer.android.com/reference/kotlin/java/io/ObjectInput#) |

| Known Direct Subclasses [ObjectInputStream](https://developer.android.com/reference/kotlin/java/io/ObjectInputStream) |-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [ObjectInputStream](https://developer.android.com/reference/kotlin/java/io/ObjectInputStream) | An ObjectInputStream deserializes primitive data and objects previously written using an ObjectOutputStream. | |

ObjectInput extends the DataInput interface to include the reading of objects. DataInput includes methods for the input of primitive types, ObjectInput extends that interface to include objects, arrays, and Strings.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [available](https://developer.android.com/reference/kotlin/java/io/ObjectInput#available())`()` Returns the number of bytes that can be read without blocking. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/io/ObjectInput#close())`()` Closes the input stream. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/ObjectInput#read())`()` Reads a byte of data. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/ObjectInput#read(kotlin.ByteArray))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Reads into an array of bytes. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/io/ObjectInput#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads into an array of bytes. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [readObject](https://developer.android.com/reference/kotlin/java/io/ObjectInput#readObject())`()` Read and return an object. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [skip](https://developer.android.com/reference/kotlin/java/io/ObjectInput#skip(kotlin.Long))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Skips n bytes of input. |

| Inherited functions ||
|---|---|
| From class [DataInput](https://developer.android.com/reference/kotlin/java/io/DataInput) |------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [readBoolean](https://developer.android.com/reference/kotlin/java/io/DataInput#readBoolean())`()` <br /> Reads one input byte and returns`true`if that byte is nonzero,`false`if that byte is zero. This method is suitable for reading the byte written by the`writeBoolean`method of interface`DataOutput`. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [readByte](https://developer.android.com/reference/kotlin/java/io/DataInput#readByte())`()` <br /> Reads and returns one input byte. The byte is treated as a signed value in the range`-128`through`127`, inclusive. This method is suitable for reading the byte written by the`writeByte`method of interface`DataOutput`. <br /> | | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [readChar](https://developer.android.com/reference/kotlin/java/io/DataInput#readChar())`()` <br /> Reads two input bytes and returns a`char`value. Let`a`be the first byte read and`b`be the second byte. The value returned is: ```kotlin <code>(char)((a &lt;&lt; 8) | (b &amp; 0xff)) </code> ``` This method is suitable for reading bytes written by the`writeChar`method of interface`DataOutput`. <br /> <br /> | | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [readDouble](https://developer.android.com/reference/kotlin/java/io/DataInput#readDouble())`()` <br /> Reads eight input bytes and returns a`double`value. It does this by first constructing a`long`value in exactly the manner of the`readLong`method, then converting this`long`value to a`double`in exactly the manner of the method`Double.longBitsToDouble`. This method is suitable for reading bytes written by the`writeDouble`method of interface`DataOutput`. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [readFloat](https://developer.android.com/reference/kotlin/java/io/DataInput#readFloat())`()` <br /> Reads four input bytes and returns a`float`value. It does this by first constructing an`int`value in exactly the manner of the`readInt`method, then converting this`int`value to a`float`in exactly the manner of the method`Float.intBitsToFloat`. This method is suitable for reading bytes written by the`writeFloat`method of interface`DataOutput`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readFully](https://developer.android.com/reference/kotlin/java/io/DataInput#readFully(kotlin.ByteArray))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Reads some bytes from an input stream and stores them into the buffer array`b`. The number of bytes read is equal to the length of`b`. This method blocks until one of the following conditions occurs: - `b.length`bytes of input data are available, in which case a normal return is made. - End of file is detected, in which case an`EOFException`is thrown. - An I/O error occurs, in which case an`IOException`other than`EOFException`is thrown. If`b`is`null`, a`NullPointerException`is thrown. If`b.length`is zero, then no bytes are read. Otherwise, the first byte read is stored into element`b[0]`, the next one into`b[1]`, and so on. If an exception is thrown from this method, then it may be that some but not all bytes of`b`have been updated with data from the input stream. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readFully](https://developer.android.com/reference/kotlin/java/io/DataInput#readFully(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Reads`len`bytes from an input stream. This method blocks until one of the following conditions occurs: - `len`bytes of input data are available, in which case a normal return is made. - End of file is detected, in which case an`EOFException`is thrown. - An I/O error occurs, in which case an`IOException`other than`EOFException`is thrown. If`b`is`null`, a`NullPointerException`is thrown. If`off`is negative, or`len`is negative, or`off+len`is greater than the length of the array`b`, then an`IndexOutOfBoundsException`is thrown. If`len`is zero, then no bytes are read. Otherwise, the first byte read is stored into element`b[off]`, the next one into`b[off+1]`, and so on. The number of bytes read is, at most, equal to`len`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readInt](https://developer.android.com/reference/kotlin/java/io/DataInput#readInt())`()` <br /> Reads four input bytes and returns an`int`value. Let`a-d`be the first through fourth bytes read. The value returned is: ```kotlin <code>(((a &amp; 0xff) &lt;&lt; 24) | ((b &amp; 0xff) &lt;&lt; 16) | ((c &amp; 0xff) &lt;&lt; 8) | (d &amp; 0xff)) </code> ``` This method is suitable for reading bytes written by the`writeInt`method of interface`DataOutput`. <br /> <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [readLine](https://developer.android.com/reference/kotlin/java/io/DataInput#readLine())`()` <br /> Reads the next line of text from the input stream. It reads successive bytes, converting each byte separately into a character, until it encounters a line terminator or end of file; the characters read are then returned as a`String`. Note that because this method processes bytes, it does not support input of the full Unicode character set. If end of file is encountered before even one byte can be read, then`null`is returned. Otherwise, each byte that is read is converted to type`char`by zero-extension. If the character`'\n'`is encountered, it is discarded and reading ceases. If the character`'\r'`is encountered, it is discarded and, if the following byte converts to the character`'\n'`, then that is discarded also; reading then ceases. If end of file is encountered before either of the characters`'\n'`and`'\r'`is encountered, reading ceases. Once reading has ceased, a`String`is returned that contains all the characters read and not discarded, taken in order. Note that every character in this string will have a value less than`\u005Cu0100`, that is,`(char)256`. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [readLong](https://developer.android.com/reference/kotlin/java/io/DataInput#readLong())`()` <br /> Reads eight input bytes and returns a`long`value. Let`a-h`be the first through eighth bytes read. The value returned is: ```kotlin <code>(((long)(a &amp; 0xff) &lt;&lt; 56) | ((long)(b &amp; 0xff) &lt;&lt; 48) | ((long)(c &amp; 0xff) &lt;&lt; 40) | ((long)(d &amp; 0xff) &lt;&lt; 32) | ((long)(e &amp; 0xff) &lt;&lt; 24) | ((long)(f &amp; 0xff) &lt;&lt; 16) | ((long)(g &amp; 0xff) &lt;&lt; 8) | ((long)(h &amp; 0xff))) </code> ``` <br /> This method is suitable for reading bytes written by the`writeLong`method of interface`DataOutput`. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [readShort](https://developer.android.com/reference/kotlin/java/io/DataInput#readShort())`()` <br /> Reads two input bytes and returns a`short`value. Let`a`be the first byte read and`b`be the second byte. The value returned is: ```kotlin <code>(short)((a &lt;&lt; 8) | (b &amp; 0xff)) </code> ``` This method is suitable for reading the bytes written by the`writeShort`method of interface`DataOutput`. <br /> <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [readUTF](https://developer.android.com/reference/kotlin/java/io/DataInput#readUTF())`()` <br /> Reads in a string that has been encoded using a [modified UTF-8](https://developer.android.com/reference/kotlin/java/io/DataInput#modified-utf-8) format. The general contract of`readUTF`is that it reads a representation of a Unicode character string encoded in modified UTF-8 format; this string of characters is then returned as a`String`. First, two bytes are read and used to construct an unsigned 16-bit integer in exactly the manner of the`readUnsignedShort`method . This integer value is called the*UTF length*and specifies the number of additional bytes to be read. These bytes are then converted to characters by considering them in groups. The length of each group is computed from the value of the first byte of the group. The byte following a group, if any, is the first byte of the next group. If the first byte of a group matches the bit pattern`0xxxxxxx`(where`x`means "may be`0`or`1`"), then the group consists of just that byte. The byte is zero-extended to form a character. If the first byte of a group matches the bit pattern`110xxxxx`, then the group consists of that byte`a`and a second byte`b`. If there is no byte`b`(because byte`a`was the last of the bytes to be read), or if byte`b`does not match the bit pattern`10xxxxxx`, then a`UTFDataFormatException`is thrown. Otherwise, the group is converted to the character: ```kotlin <code>(char)(((a &amp; 0x1F) &lt;&lt; 6) | (b &amp; 0x3F)) </code> ``` If the first byte of a group matches the bit pattern`1110xxxx`, then the group consists of that byte`a`and two more bytes`b`and`c`. If there is no byte`c`(because byte`a`was one of the last two of the bytes to be read), or either byte`b`or byte`c`does not match the bit pattern`10xxxxxx`, then a`UTFDataFormatException`is thrown. Otherwise, the group is converted to the character: ```kotlin <code>(char)(((a &amp; 0x0F) &lt;&lt; 12) | ((b &amp; 0x3F) &lt;&lt; 6) | (c &amp; 0x3F)) </code> ``` If the first byte of a group matches the pattern`1111xxxx`or the pattern`10xxxxxx`, then a`UTFDataFormatException`is thrown. If end of file is encountered at any time during this entire process, then an`EOFException`is thrown. After every group has been converted to a character by this process, the characters are gathered, in the same order in which their corresponding groups were read from the input stream, to form a`String`, which is returned. The`writeUTF`method of interface`DataOutput`may be used to write data that is suitable for reading by this method. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readUnsignedByte](https://developer.android.com/reference/kotlin/java/io/DataInput#readUnsignedByte())`()` <br /> Reads one input byte, zero-extends it to type`int`, and returns the result, which is therefore in the range`0`through`255`. This method is suitable for reading the byte written by the`writeByte`method of interface`DataOutput`if the argument to`writeByte`was intended to be a value in the range`0`through`255`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readUnsignedShort](https://developer.android.com/reference/kotlin/java/io/DataInput#readUnsignedShort())`()` <br /> Reads two input bytes and returns an`int`value in the range`0`through`65535`. Let`a`be the first byte read and`b`be the second byte. The value returned is: ```kotlin <code>(((a &amp; 0xff) &lt;&lt; 8) | (b &amp; 0xff)) </code> ``` This method is suitable for reading the bytes written by the`writeShort`method of interface`DataOutput`if the argument to`writeShort`was intended to be a value in the range`0`through`65535`. <br /> <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [skipBytes](https://developer.android.com/reference/kotlin/java/io/DataInput#skipBytes(kotlin.Int))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Makes an attempt to skip over`n`bytes of data from the input stream, discarding the skipped bytes. However, it may skip over some smaller number of bytes, possibly zero. This may result from any of a number of conditions; reaching end of file before`n`bytes have been skipped is only one possibility. This method never throws an`EOFException`. The actual number of bytes skipped is returned. <br /> | ||

## Public methods

### available

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun available(): Int
```

Returns the number of bytes that can be read without blocking.

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of available bytes. |

| Exceptions ||
|-----------------------|-------------------------------|
| `java.io.IOException` | If an I/O error has occurred. |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

Closes the input stream. Must be called to release any resources associated with the stream.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | If an I/O error has occurred. |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun read(): Int
```

Reads a byte of data. This method will block if no input is available.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the byte read, or -1 if the end of the stream is reached. |

| Exceptions ||
|-----------------------|-------------------------------|
| `java.io.IOException` | If an I/O error has occurred. |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun read(b: ByteArray!): Int
```

Reads into an array of bytes. This method will block until some input is available.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer into which the data is read |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the actual number of bytes read, -1 is returned when the end of the stream is reached. |

| Exceptions ||
|-----------------------|-------------------------------|
| `java.io.IOException` | If an I/O error has occurred. |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun read(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Int
```

Reads into an array of bytes. This method will block until some input is available.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer into which the data is read |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset of the data |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of bytes read |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the actual number of bytes read, -1 is returned when the end of the stream is reached. |

| Exceptions ||
|-----------------------|-------------------------------|
| `java.io.IOException` | If an I/O error has occurred. |

### readObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readObject(): Any!
```

Read and return an object. The class that implements this interface defines where the object is "read" from.

| Return ||
|-----------------------------------------------------------------------------|---------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the object read from the stream |

| Exceptions ||
|------------------------------------|------------------------------------------------------------|
| `java.lang.ClassNotFoundException` | If the class of a serialized object cannot be found. |
| `java.io.IOException` | If any of the usual Input/Output related exceptions occur. |

### skip

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun skip(n: Long): Long
```

Skips n bytes of input.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of bytes to be skipped |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the actual number of bytes skipped. |

| Exceptions ||
|-----------------------|-------------------------------|
| `java.io.IOException` | If an I/O error has occurred. |
