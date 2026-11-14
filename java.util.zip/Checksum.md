# Checksum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Checksum

```
interface Checksum
```

| [java.util.zip.Checksum](https://developer.android.com/reference/kotlin/java/util/zip/Checksum#) |

| Known Direct Subclasses [Adler32](https://developer.android.com/reference/kotlin/java/util/zip/Adler32), [CRC32](https://developer.android.com/reference/kotlin/java/util/zip/CRC32), [CRC32C](https://developer.android.com/reference/kotlin/java/util/zip/CRC32C) |---------------------------------------------------------------------------------|-----------------------------------------------------------------------------| | [Adler32](https://developer.android.com/reference/kotlin/java/util/zip/Adler32) | A class that can be used to compute the Adler-32 checksum of a data stream. | | [CRC32](https://developer.android.com/reference/kotlin/java/util/zip/CRC32) | A class that can be used to compute the CRC-32 of a data stream. | | [CRC32C](https://developer.android.com/reference/kotlin/java/util/zip/CRC32C) | A class that can be used to compute the CRC-32C of a data stream. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An interface representing a data checksum.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getValue](https://developer.android.com/reference/kotlin/java/util/zip/Checksum#getValue())`()` Returns the current checksum value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/java/util/zip/Checksum#reset())`()` Resets the checksum to its initial value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](https://developer.android.com/reference/kotlin/java/util/zip/Checksum#update(kotlin.ByteArray))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Updates the current checksum with the specified array of bytes. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](https://developer.android.com/reference/kotlin/java/util/zip/Checksum#update(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Updates the current checksum with the specified array of bytes. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](https://developer.android.com/reference/kotlin/java/util/zip/Checksum#update(kotlin.Int))`(`b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Updates the current checksum with the specified byte. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](https://developer.android.com/reference/kotlin/java/util/zip/Checksum#update(java.nio.ByteBuffer))`(`buffer:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`)` Updates the current checksum with the bytes from the specified buffer. |
| --- | --- |

## Public methods

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getValue(): Long
```

Returns the current checksum value.

| Return ||
|------------------------------------------------------------------------------|----------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the current checksum value |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun reset(): Unit
```

Resets the checksum to its initial value. 

### update

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun update(b: ByteArray!): Unit
```

Updates the current checksum with the specified array of bytes.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the array of bytes to update the checksum with |

| Exceptions ||
|----------------------------------|---------------|
| `java.lang.NullPointerException` | if`b`is`null` |

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun update(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Updates the current checksum with the specified array of bytes.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the byte array to update the checksum with |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset of the data |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to use for the update |
| --- | --- |

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun update(b: Int): Unit
```

Updates the current checksum with the specified byte.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------|
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the byte to update the checksum with |

### update

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun update(buffer: ByteBuffer!): Unit
```

Updates the current checksum with the bytes from the specified buffer. The checksum is updated with the remaining bytes in the buffer, starting at the buffer's position. Upon return, the buffer's position will be updated to its limit; its limit will not have been changed.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `buffer` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:the ByteBuffer to update the checksum with |

| Exceptions ||
|----------------------------------|--------------------|
| `java.lang.NullPointerException` | if`buffer`is`null` |
