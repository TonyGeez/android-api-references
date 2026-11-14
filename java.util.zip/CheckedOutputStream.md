# CheckedOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CheckedOutputStream

```
open class CheckedOutputStream : FilterOutputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.io.OutputStream](../java.io/OutputStream.md) |||
| | ↳ | [java.io.FilterOutputStream](../java.io/FilterOutputStream.md) ||
| | | ↳ | [java.util.zip.CheckedOutputStream](CheckedOutputStream.md) |
| --- | --- | --- | --- |

An output stream that also maintains a checksum of the data being written. The checksum can then be used to verify the integrity of the output data.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CheckedOutputStream](CheckedOutputStream.md))`(`out:` ` [OutputStream](../java.io/OutputStream.md)!`, `cksum:` ` [Checksum](Checksum.md)!`)` Creates an output stream with the specified Checksum. |

| Public methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Checksum](Checksum.md)! | [getChecksum](CheckedOutputStream.md))`()` Returns the Checksum for this output stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](CheckedOutputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes an array of bytes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](CheckedOutputStream.md))`(`b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a byte. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [FilterOutputStream](../java.io/FilterOutputStream.md) |------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java.io/FilterOutputStream.md))`()` <br /> Closes this output stream and releases any system resources associated with the stream. When not already closed, the`close`method of`FilterOutputStream`calls its`flush`method, and then calls the`close`method of its underlying output stream. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](../java.io/FilterOutputStream.md))`()` <br /> Flushes this output stream and forces any buffered output bytes to be written out to the stream. The`flush`method of`FilterOutputStream`calls the`flush`method of its underlying output stream. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../java.io/FilterOutputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Writes`b.length`bytes to this output stream. The`write`method of`FilterOutputStream`calls its`write`method of three arguments with the arguments`b`,`0`, and`b.length`. Note that this method does not call the one-argument`write`method of its underlying output stream with the single argument`b`. <br /> | ||
| From class [OutputStream](../java.io/OutputStream.md) |--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [OutputStream](../java.io/OutputStream.md)! | [nullOutputStream](../java.io/OutputStream.md))`()` <br /> Returns a new`OutputStream`which discards all bytes. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`write(int)`,`write(byte[])`, and`write(byte[], int, int)`methods do nothing. After the stream has been closed, these methods all throw`IOException`. The`flush()`method does nothing. <br /> | ||

| Inherited properties ||
|---|---|
| From class [FilterOutputStream](../java.io/FilterOutputStream.md) |--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [OutputStream](../java.io/OutputStream.md)! | [out](../java.io/FilterOutputStream.md) <br /> The underlying output stream to be filtered. <br /> | ||

## Public constructors

### CheckedOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CheckedOutputStream(
    out: OutputStream!, 
    cksum: Checksum!)
```

Creates an output stream with the specified Checksum.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](../java.io/OutputStream.md)!:the output stream |
| `cksum` | [Checksum](Checksum.md)!:the checksum |

## Public methods

### getChecksum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChecksum(): Checksum!
```

Returns the Checksum for this output stream.

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [Checksum](Checksum.md)! | the Checksum |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Writes an array of bytes. Will block until the bytes are actually written.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data to be written |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset of the data |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to be written |
| --- | --- |

| Exceptions ||
|-----------------------|------------------------------|
| `java.io.IOException` | if an I/O error has occurred |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(b: Int): Unit
```

Writes a byte. Will block until the byte is actually written.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------|
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the byte to be written |

| Exceptions ||
|-----------------------|------------------------------|
| `java.io.IOException` | if an I/O error has occurred |
