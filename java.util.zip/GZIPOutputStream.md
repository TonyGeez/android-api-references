# GZIPOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GZIPOutputStream

```
open class GZIPOutputStream : DeflaterOutputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [java.io.OutputStream](../java/io/OutputStream.md) ||||
| | ↳ | [java.io.FilterOutputStream](../java/io/FilterOutputStream.md) |||
| | | ↳ | [java.util.zip.DeflaterOutputStream](../java/util/zip/DeflaterOutputStream.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.util.zip.GZIPOutputStream](../java/util/zip/GZIPOutputStream.md) |

This class implements a stream filter for writing compressed data in the GZIP file format.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GZIPOutputStream](../java/util/zip/GZIPOutputStream.md))`(`out:` ` [OutputStream](../java/io/OutputStream.md)!`)` Creates a new output stream with a default buffer size. |
| [GZIPOutputStream](../java/util/zip/GZIPOutputStream.md))`(`out:` ` [OutputStream](../java/io/OutputStream.md)!`, `syncFlush:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new output stream with a default buffer size and the specified flush mode. |
| [GZIPOutputStream](../java/util/zip/GZIPOutputStream.md))`(`out:` ` [OutputStream](../java/io/OutputStream.md)!`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new output stream with the specified buffer size. |
| [GZIPOutputStream](../java/util/zip/GZIPOutputStream.md))`(`out:` ` [OutputStream](../java/io/OutputStream.md)!`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `syncFlush:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new output stream with the specified buffer size and flush mode. |

| Public methods ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finish](../java/util/zip/GZIPOutputStream.md))`()` Finishes writing compressed data to the output stream without closing the underlying stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../java/util/zip/GZIPOutputStream.md))`(`buf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes array of bytes to the compressed output stream. |

| Inherited functions ||
|---|---|
| From class [DeflaterOutputStream](../java/util/zip/DeflaterOutputStream.md) |------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/util/zip/DeflaterOutputStream.md))`()` Writes remaining compressed data to the output stream and closes the underlying stream. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deflate](../java/util/zip/DeflaterOutputStream.md))`()` Writes next block of compressed data to the output stream. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](../java/util/zip/DeflaterOutputStream.md))`()` Flushes the compressed output stream. If [syncFlush](../java/util/zip/DeflaterOutputStream.md)) is `true` when this compressed output stream is constructed, this method first flushes the underlying `compressor` with the flush mode [Deflater.SYNC_FLUSH](../java/util/zip/Deflater.md) to force all pending data to be flushed out to the output stream and then flushes the output stream. Otherwise this method only flushes the output stream without flushing the `compressor`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../java/util/zip/DeflaterOutputStream.md))`(`b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a byte to the compressed output stream. This method will block until the byte can be written. <br /> | ||
| From class [OutputStream](../java/io/OutputStream.md) |--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [OutputStream](../java/io/OutputStream.md)! | [nullOutputStream](../java/io/OutputStream.md))`()` Returns a new `OutputStream` which discards all bytes. The returned stream is initially open. The stream is closed by calling the `close()` method. Subsequent calls to `close()` have no effect. While the stream is open, the `write(int)`, `write(byte[])`, and `write(byte[], int, int)` methods do nothing. After the stream has been closed, these methods all throw `IOException`. The `flush()` method does nothing. <br /> | ||
| From class [FilterOutputStream](../java/io/FilterOutputStream.md) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../java/io/FilterOutputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Writes `b.length` bytes to this output stream. The `write` method of `FilterOutputStream` calls its `write` method of three arguments with the arguments `b`, `0`, and `b.length`. Note that this method does not call the one-argument `write` method of its underlying output stream with the single argument `b`. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- |

| Properties ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [CRC32](../java/util/zip/CRC32.md)! | [crc](../java/util/zip/GZIPOutputStream.md) CRC-32 of uncompressed data. |

| Inherited properties ||
|---|---|
| From class [DeflaterOutputStream](../java/util/zip/DeflaterOutputStream.md) |------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [buf](../java/util/zip/DeflaterOutputStream.md) Output buffer for writing compressed data. <br /> | | [Deflater](../java/util/zip/Deflater.md)! | [def](../java/util/zip/DeflaterOutputStream.md) Compressor for this stream. <br /> | ||
| From class [FilterOutputStream](../java/io/FilterOutputStream.md) |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [OutputStream](../java/io/OutputStream.md)! | [out](../java/io/FilterOutputStream.md) The underlying output stream to be filtered. <br /> | ||

## Public constructors

### GZIPOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GZIPOutputStream(out: OutputStream!)
```

Creates a new output stream with a default buffer size.

The new output stream instance is created as if by invoking the 2-argument constructor GZIPOutputStream(out, false).

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](../java/io/OutputStream.md)!: the output stream |

| Exceptions ||
|-----------------------|-------------------------------|
| `java.io.IOException` | If an I/O error has occurred. |

### GZIPOutputStream

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GZIPOutputStream(
    out: OutputStream!, 
    syncFlush: Boolean)
```

Creates a new output stream with a default buffer size and the specified flush mode.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](../java/io/OutputStream.md)!: the output stream |
| `syncFlush` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if `true` invocation of the inherited java.util.zip.DeflaterOutputStream#flush() method of this instance flushes the compressor with flush mode [Deflater.SYNC_FLUSH](../java/util/zip/Deflater.md) before flushing the output stream, otherwise only flushes the output stream |

| Exceptions ||
|-----------------------|-------------------------------|
| `java.io.IOException` | If an I/O error has occurred. |

### GZIPOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GZIPOutputStream(
    out: OutputStream!, 
    size: Int)
```

Creates a new output stream with the specified buffer size.

The new output stream instance is created as if by invoking the 3-argument constructor GZIPOutputStream(out, size, false). Android-note: Android limits the number of UnbufferedIO operations that can be performed, so consider using buffered inputs with this class. More information can be found in the [UnbufferedIO](../android/os/StrictMode.ThreadPolicy.Builder.md)) and [StrictMode](../android/os/StrictMode.md) documentation.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](../java/io/OutputStream.md)!: the output stream |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the output buffer size |

| Exceptions ||
|--------------------------------------|-------------------------------|
| `java.io.IOException` | If an I/O error has occurred. |
| `java.lang.IllegalArgumentException` | if `size <= 0` |

### GZIPOutputStream

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GZIPOutputStream(
    out: OutputStream!, 
    size: Int, 
    syncFlush: Boolean)
```

Creates a new output stream with the specified buffer size and flush mode.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](../java/io/OutputStream.md)!: the output stream |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the output buffer size |
| `syncFlush` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if `true` invocation of the inherited java.util.zip.DeflaterOutputStream#flush() method of this instance flushes the compressor with flush mode [Deflater.SYNC_FLUSH](../java/util/zip/Deflater.md) before flushing the output stream, otherwise only flushes the output stream |
| --- | --- |

| Exceptions ||
|--------------------------------------|-------------------------------|
| `java.io.IOException` | If an I/O error has occurred. |
| `java.lang.IllegalArgumentException` | if `size <= 0` |

## Public methods

### finish

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun finish(): Unit
```

Finishes writing compressed data to the output stream without closing the underlying stream. Use this method when applying multiple filters in succession to the same output stream.

| Exceptions ||
|-----------------------|------------------------------|
| `java.io.IOException` | if an I/O error has occurred |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(
    buf: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Writes array of bytes to the compressed output stream. This method will block until all the bytes are written.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------|
| `b` | the data to be written |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start offset of the data |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the length of the data |
| --- | --- |
| `buf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the data to be written |

| Exceptions ||
|-----------------------|-------------------------------|
| `java.io.IOException` | If an I/O error has occurred. |

## Properties

### crc

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var crc: CRC32!
```

CRC-32 of uncompressed data.
