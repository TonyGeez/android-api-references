# CRC32

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CRC32

```
open class CRC32 : Checksum
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.zip.CRC32](../java/util/zip/CRC32.md) |

A class that can be used to compute the CRC-32 of a data stream.

Passing a`null`argument to a method in this class will cause a [NullPointerException](../java/lang/NullPointerException.md) to be thrown.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------|---|
| [CRC32](../java/util/zip/CRC32.md))`()` Creates a new CRC32 object. |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getValue](../java/util/zip/CRC32.md))`()` Returns CRC-32 value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](../java/util/zip/CRC32.md))`()` Resets CRC-32 to initial value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](../java/util/zip/CRC32.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Updates the CRC-32 checksum with the specified array of bytes. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](../java/util/zip/CRC32.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Updates the CRC-32 checksum with the specified array of bytes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](../java/util/zip/CRC32.md))`(`b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Updates the CRC-32 checksum with the specified byte (the low eight bits of the argument b). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](../java/util/zip/CRC32.md))`(`buffer:` ` [ByteBuffer](../java/nio/ByteBuffer.md)!`)` Updates the CRC-32 checksum with the bytes from the specified buffer. |
| --- | --- |

## Public constructors

### CRC32

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CRC32()
```

Creates a new CRC32 object.

## Public methods

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValue(): Long
```

Returns CRC-32 value.

| Return ||
|------------------------------------------------------------------------------|----------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the current checksum value |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Resets CRC-32 to initial value. 

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun update(b: ByteArray!): Unit
```

Updates the CRC-32 checksum with the specified array of bytes.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the array of bytes to update the checksum with |

| Exceptions ||
|----------------------------------|---------------|
| `java.lang.NullPointerException` | if`b`is`null` |

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun update(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Updates the CRC-32 checksum with the specified array of bytes.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the byte array to update the checksum with |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset of the data |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to use for the update |
| --- | --- |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------|
| `java.lang.ArrayIndexOutOfBoundsException` | if`off`is negative, or`len`is negative, or`off+len`is negative or greater than the length of the array`b`. |

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun update(b: Int): Unit
```

Updates the CRC-32 checksum with the specified byte (the low eight bits of the argument b).

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------|
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the byte to update the checksum with |

### update

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun update(buffer: ByteBuffer!): Unit
```

Updates the CRC-32 checksum with the bytes from the specified buffer. The checksum is updated with the remaining bytes in the buffer, starting at the buffer's position. Upon return, the buffer's position will be updated to its limit; its limit will not have been changed.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `buffer` | [ByteBuffer](../java/nio/ByteBuffer.md)!:the ByteBuffer to update the checksum with |

| Exceptions ||
|----------------------------------|--------------------|
| `java.lang.NullPointerException` | if`buffer`is`null` |
