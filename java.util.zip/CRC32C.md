# CRC32C

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CRC32C

```
class CRC32C : Checksum
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.zip.CRC32C](CRC32C.md) |

A class that can be used to compute the CRC-32C of a data stream.

CRC-32C is defined in [RFC 3720](http://www.ietf.org/rfc/rfc3720.txt): Internet Small Computer Systems Interface (iSCSI).

Passing a`null`argument to a method in this class will cause a [NullPointerException](../java.lang/NullPointerException.md) to be thrown.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------|---|
| [CRC32C](CRC32C.md))`()` Creates a new CRC32C object. |

| Public methods ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getValue](CRC32C.md))`()` Returns CRC-32C value. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](CRC32C.md))`()` Resets CRC-32C to initial value. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](CRC32C.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Updates the CRC-32C checksum with the specified array of bytes. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](CRC32C.md))`(`b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Updates the CRC-32C checksum with the specified byte (the low eight bits of the argument b). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](CRC32C.md))`(`buffer:` ` [ByteBuffer](../java.nio/ByteBuffer.md)!`)` Updates the CRC-32C checksum with the bytes from the specified buffer. |

| Inherited functions ||
|---|---|
| From class [Checksum](Checksum.md) |------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](Checksum.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Updates the current checksum with the specified array of bytes. <br /> | ||

## Public constructors

### CRC32C

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CRC32C()
```

Creates a new CRC32C object.

## Public methods

### getValue

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getValue(): Long
```

Returns CRC-32C value.

| Return ||
|------------------------------------------------------------------------------|----------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the current checksum value |

### reset

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun reset(): Unit
```

Resets CRC-32C to initial value. 

### update

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun update(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Updates the CRC-32C checksum with the specified array of bytes.

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

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun update(b: Int): Unit
```

Updates the CRC-32C checksum with the specified byte (the low eight bits of the argument b).

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------|
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the byte to update the checksum with |

### update

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun update(buffer: ByteBuffer!): Unit
```

Updates the CRC-32C checksum with the bytes from the specified buffer. The checksum is updated with the remaining bytes in the buffer, starting at the buffer's position. Upon return, the buffer's position will be updated to its limit; its limit will not have been changed.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `buffer` | [ByteBuffer](../java.nio/ByteBuffer.md)!:the ByteBuffer to update the checksum with |

| Exceptions ||
|----------------------------------|--------------------|
| `java.lang.NullPointerException` | if`buffer`is`null` |
