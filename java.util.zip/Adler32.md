# Adler32

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Adler32

```
open class Adler32 : Checksum
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.zip.Adler32](https://developer.android.com/reference/kotlin/java/util/zip/Adler32#) |

A class that can be used to compute the Adler-32 checksum of a data stream. An Adler-32 checksum is almost as reliable as a CRC-32 but can be computed much faster.

Passing a`null`argument to a method in this class will cause a [NullPointerException](https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#) to be thrown.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------|---|
| [Adler32](https://developer.android.com/reference/kotlin/java/util/zip/Adler32#Adler32())`()` Creates a new Adler32 object. |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getValue](https://developer.android.com/reference/kotlin/java/util/zip/Adler32#getValue())`()` Returns the checksum value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/java/util/zip/Adler32#reset())`()` Resets the checksum to initial value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](https://developer.android.com/reference/kotlin/java/util/zip/Adler32#update(kotlin.ByteArray))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Updates the checksum with the specified array of bytes. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](https://developer.android.com/reference/kotlin/java/util/zip/Adler32#update(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Updates the checksum with the specified array of bytes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](https://developer.android.com/reference/kotlin/java/util/zip/Adler32#update(kotlin.Int))`(`b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Updates the checksum with the specified byte (the low eight bits of the argument b). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](https://developer.android.com/reference/kotlin/java/util/zip/Adler32#update(java.nio.ByteBuffer))`(`buffer:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`)` Updates the checksum with the bytes from the specified buffer. |
| --- | --- |

## Public constructors

### Adler32

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Adler32()
```

Creates a new Adler32 object.

## Public methods

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValue(): Long
```

Returns the checksum value.

| Return ||
|------------------------------------------------------------------------------|----------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the current checksum value |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Resets the checksum to initial value. 

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun update(b: ByteArray!): Unit
```

Updates the checksum with the specified array of bytes.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the byte array to update the checksum with |

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

Updates the checksum with the specified array of bytes.

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

Updates the checksum with the specified byte (the low eight bits of the argument b).

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------|
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the byte to update the checksum with |

### update

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun update(buffer: ByteBuffer!): Unit
```

Updates the checksum with the bytes from the specified buffer. The checksum is updated with the remaining bytes in the buffer, starting at the buffer's position. Upon return, the buffer's position will be updated to its limit; its limit will not have been changed.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `buffer` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:the ByteBuffer to update the checksum with |

| Exceptions ||
|----------------------------------|--------------------|
| `java.lang.NullPointerException` | if`buffer`is`null` |
