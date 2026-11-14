# GZIPOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GZIPOutputStream

```
open class GZIPOutputStream : DeflaterOutputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [java.io.OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#) ||||
| | ↳ | [java.io.FilterOutputStream](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#) |||
| | | ↳ | [java.util.zip.DeflaterOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.util.zip.GZIPOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/GZIPOutputStream#) |

This class implements a stream filter for writing compressed data in the GZIP file format.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GZIPOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/GZIPOutputStream#GZIPOutputStream(java.io.OutputStream))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`)` Creates a new output stream with a default buffer size. |
| [GZIPOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/GZIPOutputStream#GZIPOutputStream(java.io.OutputStream,%20kotlin.Boolean))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`, `syncFlush:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new output stream with a default buffer size and the specified flush mode. |
| [GZIPOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/GZIPOutputStream#GZIPOutputStream(java.io.OutputStream,%20kotlin.Int))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new output stream with the specified buffer size. |
| [GZIPOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/GZIPOutputStream#GZIPOutputStream(java.io.OutputStream,%20kotlin.Int,%20kotlin.Boolean))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `syncFlush:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new output stream with the specified buffer size and flush mode. |

| Public methods ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finish](https://developer.android.com/reference/kotlin/java/util/zip/GZIPOutputStream#finish())`()` Finishes writing compressed data to the output stream without closing the underlying stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/util/zip/GZIPOutputStream#write(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`buf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes array of bytes to the compressed output stream. |

| Inherited functions ||
|---|---|
| From class [DeflaterOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream) |------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#close())`()` Writes remaining compressed data to the output stream and closes the underlying stream. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deflate](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#deflate())`()` Writes next block of compressed data to the output stream. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#flush())`()` Flushes the compressed output stream. If [syncFlush](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#DeflaterOutputStream(java.io.OutputStream,%20java.util.zip.Deflater,%20kotlin.Int,%20kotlin.Boolean)) is `true` when this compressed output stream is constructed, this method first flushes the underlying `compressor` with the flush mode [Deflater.SYNC_FLUSH](https://developer.android.com/reference/kotlin/java/util/zip/Deflater#SYNC_FLUSH:kotlin.Int) to force all pending data to be flushed out to the output stream and then flushes the output stream. Otherwise this method only flushes the output stream without flushing the `compressor`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#write(kotlin.Int))`(`b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a byte to the compressed output stream. This method will block until the byte can be written. <br /> | ||
| From class [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#) |--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | [nullOutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#nullOutputStream())`()` Returns a new `OutputStream` which discards all bytes. The returned stream is initially open. The stream is closed by calling the `close()` method. Subsequent calls to `close()` have no effect. While the stream is open, the `write(int)`, `write(byte[])`, and `write(byte[], int, int)` methods do nothing. After the stream has been closed, these methods all throw `IOException`. The `flush()` method does nothing. <br /> | ||
| From class [FilterOutputStream](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#write(kotlin.ByteArray))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Writes `b.length` bytes to this output stream. The `write` method of `FilterOutputStream` calls its `write` method of three arguments with the arguments `b`, `0`, and `b.length`. Note that this method does not call the one-argument `write` method of its underlying output stream with the single argument `b`. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- |

| Properties ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [CRC32](https://developer.android.com/reference/kotlin/java/util/zip/CRC32)! | [crc](https://developer.android.com/reference/kotlin/java/util/zip/GZIPOutputStream#crc:java.util.zip.CRC32) CRC-32 of uncompressed data. |

| Inherited properties ||
|---|---|
| From class [DeflaterOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream) |------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [buf](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#buf:kotlin.ByteArray) Output buffer for writing compressed data. <br /> | | [Deflater](https://developer.android.com/reference/kotlin/java/util/zip/Deflater)! | [def](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#def:java.util.zip.Deflater) Compressor for this stream. <br /> | ||
| From class [FilterOutputStream](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#) |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | [out](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#out:java.io.OutputStream) The underlying output stream to be filtered. <br /> | ||

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
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!: the output stream |

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
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!: the output stream |
| `syncFlush` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if `true` invocation of the inherited java.util.zip.DeflaterOutputStream#flush() method of this instance flushes the compressor with flush mode [Deflater.SYNC_FLUSH](https://developer.android.com/reference/kotlin/java/util/zip/Deflater#SYNC_FLUSH:kotlin.Int) before flushing the output stream, otherwise only flushes the output stream |

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

The new output stream instance is created as if by invoking the 3-argument constructor GZIPOutputStream(out, size, false). Android-note: Android limits the number of UnbufferedIO operations that can be performed, so consider using buffered inputs with this class. More information can be found in the [UnbufferedIO](https://developer.android.com/reference/android/os/StrictMode.ThreadPolicy.Builder#detectUnbufferedIo()) and [StrictMode](https://developer.android.com/reference/android/os/StrictMode) documentation.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!: the output stream |
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
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!: the output stream |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the output buffer size |
| `syncFlush` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if `true` invocation of the inherited java.util.zip.DeflaterOutputStream#flush() method of this instance flushes the compressor with flush mode [Deflater.SYNC_FLUSH](https://developer.android.com/reference/kotlin/java/util/zip/Deflater#SYNC_FLUSH:kotlin.Int) before flushing the output stream, otherwise only flushes the output stream |
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
