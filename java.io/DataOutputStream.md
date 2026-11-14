Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DataOutputStream

```
open class DataOutputStream : FilterOutputStream, DataOutput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [java.io.OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream) |||
| | ↳ | [java.io.FilterOutputStream](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream) ||
| | | ↳ | [java.io.DataOutputStream](https://developer.android.com/reference/kotlin/java/io/DataOutputStream#) |

A data output stream lets an application write primitive Java data types to an output stream in a portable way. An application can then use a data input stream to read the data back in.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/DataOutputStream#DataOutputStream(java.io.OutputStream)(out: https://developer.android.com/reference/kotlin/java/io/OutputStream!)` Creates a new data output stream to write data to the specified underlying output stream. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/DataOutputStream#flush()()` Flushes this data output stream. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/DataOutputStream#size()()` Returns the current value of the counter `written`, the number of bytes written to this data output stream so far. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/DataOutputStream#write(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, off: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Writes `len` bytes from the specified byte array starting at offset `off` to the underlying output stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/DataOutputStream#write(kotlin.Int)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Writes the specified byte (the low eight bits of the argument `b`) to the underlying output stream. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/DataOutputStream#writeBoolean(kotlin.Boolean)(v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Writes a `boolean` to the underlying output stream as a 1-byte value. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/DataOutputStream#writeByte(kotlin.Int)(v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Writes out a `byte` to the underlying output stream as a 1-byte value. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/DataOutputStream#writeBytes(kotlin.String)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Writes out the string to the underlying output stream as a sequence of bytes. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/DataOutputStream#writeChar(kotlin.Int)(v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Writes a `char` to the underlying output stream as a 2-byte value, high byte first. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/DataOutputStream#writeChars(kotlin.String)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Writes a string to the underlying output stream as a sequence of characters. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/DataOutputStream#writeDouble(kotlin.Double)(v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Converts the double argument to a `long` using the `doubleToLongBits` method in class `Double`, and then writes that `long` value to the underlying output stream as an 8-byte quantity, high byte first. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/DataOutputStream#writeFloat(kotlin.Float)(v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Converts the float argument to an `int` using the `floatToIntBits` method in class `Float`, and then writes that `int` value to the underlying output stream as a 4-byte quantity, high byte first. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/DataOutputStream#writeInt(kotlin.Int)(v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Writes an `int` to the underlying output stream as four bytes, high byte first. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/DataOutputStream#writeLong(kotlin.Long)(v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Writes a `long` to the underlying output stream as eight bytes, high byte first. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/DataOutputStream#writeShort(kotlin.Int)(v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Writes a `short` to the underlying output stream as two bytes, high byte first. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/DataOutputStream#writeUTF(kotlin.String)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Writes a string to the underlying output stream using [modified UTF-8](https://developer.android.com/reference/kotlin/java/io/DataInput#modified-utf-8) encoding in a machine-independent manner. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream#close()()` Closes this output stream and releases any system resources associated with the stream. When not already closed, the `close` method of `FilterOutputStream` calls its `flush` method, and then calls the `close` method of its underlying output stream. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream#write(kotlin.ByteArray)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Writes `b.length` bytes to this output stream. The `write` method of `FilterOutputStream` calls its `write` method of three arguments with the arguments `b`, `0`, and `b.length`. Note that this method does not call the one-argument `write` method of its underlying output stream with the single argument `b`. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/io/OutputStream` |---|---| | `https://developer.android.com/reference/kotlin/java/io/OutputStream!` | `https://developer.android.com/reference/kotlin/java/io/OutputStream#nullOutputStream()()` Returns a new `OutputStream` which discards all bytes. The returned stream is initially open. The stream is closed by calling the `close()` method. Subsequent calls to `close()` have no effect. While the stream is open, the `write(int)`, `write(byte[])`, and `write(byte[], int, int)` methods do nothing. After the stream has been closed, these methods all throw `IOException`. The `flush()` method does nothing. <br /> | ||

| Properties ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/DataOutputStream#written:kotlin.Int` The number of bytes written to the data output stream so far. |

| Inherited properties ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream` |---|---| | `https://developer.android.com/reference/kotlin/java/io/OutputStream!` | `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream#out:java.io.OutputStream` The underlying output stream to be filtered. <br /> | ||

## Public constructors

### DataOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DataOutputStream(out: OutputStream!)
```

Creates a new data output stream to write data to the specified underlying output stream. The counter `written` is set to zero.

| Parameters ||
|---|---|
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream)!: the underlying output stream, to be saved for later use. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream#out:java.io.OutputStream`

## Public methods

### flush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun flush(): Unit
```

Flushes this data output stream. This forces any buffered output bytes to be written out to the stream.

The `flush` method of `DataOutputStream` calls the `flush` method of its underlying output stream.

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream#out:java.io.OutputStream`
- `https://developer.android.com/reference/kotlin/java/io/OutputStream#flush()`

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun size(): Int
```

Returns the current value of the counter `written`, the number of bytes written to this data output stream so far. If the counter overflows, it will be wrapped to Integer.MAX_VALUE.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value of the `written` field. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/DataOutputStream#written:kotlin.Int`

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun write(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Writes `len` bytes from the specified byte array starting at offset `off` to the underlying output stream. If no exception is thrown, the counter `written` is incremented by `len`.

| Parameters ||
|---|---|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the data. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start offset in the data. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of bytes to write. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream#out:java.io.OutputStream`

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun write(b: Int): Unit
```

Writes the specified byte (the low eight bits of the argument `b`) to the underlying output stream. If no exception is thrown, the counter `written` is incremented by `1`.

Implements the `write` method of `OutputStream`.

| Parameters ||
|---|---|
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the `byte` to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream#out:java.io.OutputStream`

### writeBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeBoolean(v: Boolean): Unit
```

Writes a `boolean` to the underlying output stream as a 1-byte value. The value `true` is written out as the value `(byte)1`; the value `false` is written out as the value `(byte)0`. If no exception is thrown, the counter `written` is incremented by `1`.

| Parameters ||
|---|---|
| `v` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): a `boolean` value to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream#out:java.io.OutputStream`

### writeByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeByte(v: Int): Unit
```

Writes out a `byte` to the underlying output stream as a 1-byte value. If no exception is thrown, the counter `written` is incremented by `1`.

| Parameters ||
|---|---|
| `v` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a `byte` value to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream#out:java.io.OutputStream`

### writeBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeBytes(s: String!): Unit
```

Writes out the string to the underlying output stream as a sequence of bytes. Each character in the string is written out, in sequence, by discarding its high eight bits. If no exception is thrown, the counter `written` is incremented by the length of `s`.

| Parameters ||
|---|---|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a string of bytes to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream#out:java.io.OutputStream`

### writeChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeChar(v: Int): Unit
```

Writes a `char` to the underlying output stream as a 2-byte value, high byte first. If no exception is thrown, the counter `written` is incremented by `2`.

| Parameters ||
|---|---|
| `v` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a `char` value to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream#out:java.io.OutputStream`

### writeChars

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeChars(s: String!): Unit
```

Writes a string to the underlying output stream as a sequence of characters. Each character is written to the data output stream as if by the `writeChar` method. If no exception is thrown, the counter `written` is incremented by twice the length of `s`.

| Parameters ||
|---|---|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a `String` value to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/DataOutputStream#writeChar(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream#out:java.io.OutputStream`

### writeDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeDouble(v: Double): Unit
```

Converts the double argument to a `long` using the `doubleToLongBits` method in class `Double`, and then writes that `long` value to the underlying output stream as an 8-byte quantity, high byte first. If no exception is thrown, the counter `written` is incremented by `8`.

| Parameters ||
|---|---|
| `v` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): a `double` value to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream#out:java.io.OutputStream`
- `https://developer.android.com/reference/kotlin/java/lang/Double.html#doubleToLongBits(kotlin.Double)`

### writeFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeFloat(v: Float): Unit
```

Converts the float argument to an `int` using the `floatToIntBits` method in class `Float`, and then writes that `int` value to the underlying output stream as a 4-byte quantity, high byte first. If no exception is thrown, the counter `written` is incremented by `4`.

| Parameters ||
|---|---|
| `v` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): a `float` value to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream#out:java.io.OutputStream`
- `https://developer.android.com/reference/kotlin/java/lang/Float.html#floatToIntBits(kotlin.Float)`

### writeInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeInt(v: Int): Unit
```

Writes an `int` to the underlying output stream as four bytes, high byte first. If no exception is thrown, the counter `written` is incremented by `4`.

| Parameters ||
|---|---|
| `v` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an `int` to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream#out:java.io.OutputStream`

### writeLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeLong(v: Long): Unit
```

Writes a `long` to the underlying output stream as eight bytes, high byte first. In no exception is thrown, the counter `written` is incremented by `8`.

| Parameters ||
|---|---|
| `v` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): a `long` to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream#out:java.io.OutputStream`

### writeShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeShort(v: Int): Unit
```

Writes a `short` to the underlying output stream as two bytes, high byte first. If no exception is thrown, the counter `written` is incremented by `2`.

| Parameters ||
|---|---|
| `v` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a `short` to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream#out:java.io.OutputStream`

### writeUTF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeUTF(str: String!): Unit
```

Writes a string to the underlying output stream using [modified UTF-8](https://developer.android.com/reference/kotlin/java/io/DataInput#modified-utf-8) encoding in a machine-independent manner.

First, two bytes are written to the output stream as if by the `writeShort` method giving the number of bytes to follow. This value is the number of bytes actually written out, not the length of the string. Following the length, each character of the string is output, in sequence, using the modified UTF-8 encoding for the character. If no exception is thrown, the counter `written` is incremented by the total number of bytes written to the output stream. This will be at least two plus the length of `str`, and at most two plus thrice the length of `str`.

| Parameters ||
|---|---|
| `s` | the string value to be written. |
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a string to be written. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

## Properties

### written

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var written: Int
```

The number of bytes written to the data output stream so far. If this counter overflows, it will be wrapped to Integer.MAX_VALUE.
