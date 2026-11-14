# DeflaterOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeflaterOutputStream

```
open class DeflaterOutputStream : FilterOutputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.io.OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#) |||
| | ↳ | [java.io.FilterOutputStream](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#) ||
| | | ↳ | [java.util.zip.DeflaterOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#) |
| --- | --- | --- | --- |

| Known Direct Subclasses [GZIPOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/GZIPOutputStream), [ZipOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream) |---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------| | [GZIPOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/GZIPOutputStream) | This class implements a stream filter for writing compressed data in the GZIP file format. | | [ZipOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream) | This class implements an output stream filter for writing files in the ZIP file format. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [JarOutputStream](https://developer.android.com/reference/kotlin/java/util/jar/JarOutputStream.html#) |-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------| | [JarOutputStream](https://developer.android.com/reference/kotlin/java/util/jar/JarOutputStream.html#) | The`JarOutputStream`class is used to write the contents of a JAR file to any output stream. | |
| --- | --- | --- | --- | --- | --- | --- |

This class implements an output stream filter for compressing data in the "deflate" compression format. It is also used as the basis for other types of compression filters, such as GZIPOutputStream.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DeflaterOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#DeflaterOutputStream(java.io.OutputStream))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`)` Creates a new output stream with a default compressor and buffer size. |
| [DeflaterOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#DeflaterOutputStream(java.io.OutputStream,%20kotlin.Boolean))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`, `syncFlush:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new output stream with a default compressor, a default buffer size and the specified flush mode. |
| [DeflaterOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#DeflaterOutputStream(java.io.OutputStream,%20java.util.zip.Deflater))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`, `def:` ` [Deflater](https://developer.android.com/reference/kotlin/java/util/zip/Deflater)!`)` Creates a new output stream with the specified compressor and a default buffer size. |
| [DeflaterOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#DeflaterOutputStream(java.io.OutputStream,%20java.util.zip.Deflater,%20kotlin.Boolean))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`, `def:` ` [Deflater](https://developer.android.com/reference/kotlin/java/util/zip/Deflater)!`, `syncFlush:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new output stream with the specified compressor, flush mode and a default buffer size. |
| [DeflaterOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#DeflaterOutputStream(java.io.OutputStream,%20java.util.zip.Deflater,%20kotlin.Int))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`, `def:` ` [Deflater](https://developer.android.com/reference/kotlin/java/util/zip/Deflater)!`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new output stream with the specified compressor and buffer size. |
| [DeflaterOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#DeflaterOutputStream(java.io.OutputStream,%20java.util.zip.Deflater,%20kotlin.Int,%20kotlin.Boolean))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`, `def:` ` [Deflater](https://developer.android.com/reference/kotlin/java/util/zip/Deflater)!`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `syncFlush:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new output stream with the specified compressor, buffer size and flush mode. |

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#close())`()` Writes remaining compressed data to the output stream and closes the underlying stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finish](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#finish())`()` Finishes writing compressed data to the output stream without closing the underlying stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#flush())`()` Flushes the compressed output stream. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#write(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes an array of bytes to the compressed output stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#write(kotlin.Int))`(`b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a byte to the compressed output stream. |

| Protected methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deflate](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#deflate())`()` Writes next block of compressed data to the output stream. |

| Inherited functions ||
|---|---|
| From class [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#) |--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | [nullOutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#nullOutputStream())`()` <br /> Returns a new`OutputStream`which discards all bytes. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`write(int)`,`write(byte[])`, and`write(byte[], int, int)`methods do nothing. After the stream has been closed, these methods all throw`IOException`. The`flush()`method does nothing. <br /> | ||
| From class [FilterOutputStream](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#) |------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#write(kotlin.ByteArray))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Writes`b.length`bytes to this output stream. The`write`method of`FilterOutputStream`calls its`write`method of three arguments with the arguments`b`,`0`, and`b.length`. Note that this method does not call the one-argument`write`method of its underlying output stream with the single argument`b`. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [buf](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#buf:kotlin.ByteArray) Output buffer for writing compressed data. |
| [Deflater](https://developer.android.com/reference/kotlin/java/util/zip/Deflater)! | [def](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#def:java.util.zip.Deflater) Compressor for this stream. |

| Inherited properties ||
|---|---|
| From class [FilterOutputStream](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#) |--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | [out](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#out:java.io.OutputStream) <br /> The underlying output stream to be filtered. <br /> | ||

## Public constructors

### DeflaterOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DeflaterOutputStream(out: OutputStream!)
```

Creates a new output stream with a default compressor and buffer size.

The new output stream instance is created as if by invoking the 2-argument constructor DeflaterOutputStream(out, false).

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!:the output stream |

### DeflaterOutputStream

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DeflaterOutputStream(
    out: OutputStream!, 
    syncFlush: Boolean)
```

Creates a new output stream with a default compressor, a default buffer size and the specified flush mode.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!:the output stream |
| `syncFlush` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`the #flush() method of this instance flushes the compressor with flush mode [Deflater.SYNC_FLUSH](https://developer.android.com/reference/kotlin/java/util/zip/Deflater#SYNC_FLUSH:kotlin.Int) before flushing the output stream, otherwise only flushes the output stream |

### DeflaterOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DeflaterOutputStream(
    out: OutputStream!, 
    def: Deflater!)
```

Creates a new output stream with the specified compressor and a default buffer size.

The new output stream instance is created as if by invoking the 3-argument constructor DeflaterOutputStream(out, def, false).

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!:the output stream |
| `def` | [Deflater](https://developer.android.com/reference/kotlin/java/util/zip/Deflater)!:the compressor ("deflater") |

### DeflaterOutputStream

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DeflaterOutputStream(
    out: OutputStream!, 
    def: Deflater!, 
    syncFlush: Boolean)
```

Creates a new output stream with the specified compressor, flush mode and a default buffer size.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!:the output stream |
| `def` | [Deflater](https://developer.android.com/reference/kotlin/java/util/zip/Deflater)!:the compressor ("deflater") |
| `syncFlush` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`the #flush() method of this instance flushes the compressor with flush mode [Deflater.SYNC_FLUSH](https://developer.android.com/reference/kotlin/java/util/zip/Deflater#SYNC_FLUSH:kotlin.Int) before flushing the output stream, otherwise only flushes the output stream |
| --- | --- |

### DeflaterOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DeflaterOutputStream(
    out: OutputStream!, 
    def: Deflater!, 
    size: Int)
```

Creates a new output stream with the specified compressor and buffer size.

The new output stream instance is created as if by invoking the 4-argument constructor DeflaterOutputStream(out, def, size, false).

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!:the output stream |
| `def` | [Deflater](https://developer.android.com/reference/kotlin/java/util/zip/Deflater)!:the compressor ("deflater") |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the output buffer size |
| --- | --- |

| Exceptions ||
|--------------------------------------|---------------|
| `java.lang.IllegalArgumentException` | if`size <= 0` |

### DeflaterOutputStream

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DeflaterOutputStream(
    out: OutputStream!, 
    def: Deflater!, 
    size: Int, 
    syncFlush: Boolean)
```

Creates a new output stream with the specified compressor, buffer size and flush mode.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!:the output stream |
| `def` | [Deflater](https://developer.android.com/reference/kotlin/java/util/zip/Deflater)!:the compressor ("deflater") |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the output buffer size |
| --- | --- |
| `syncFlush` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`the #flush() method of this instance flushes the compressor with flush mode [Deflater.SYNC_FLUSH](https://developer.android.com/reference/kotlin/java/util/zip/Deflater#SYNC_FLUSH:kotlin.Int) before flushing the output stream, otherwise only flushes the output stream |

| Exceptions ||
|--------------------------------------|---------------|
| `java.lang.IllegalArgumentException` | if`size <= 0` |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Writes remaining compressed data to the output stream and closes the underlying stream.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error has occurred |

### finish

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun finish(): Unit
```

Finishes writing compressed data to the output stream without closing the underlying stream. Use this method when applying multiple filters in succession to the same output stream.

| Exceptions ||
|-----------------------|------------------------------|
| `java.io.IOException` | if an I/O error has occurred |

### flush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun flush(): Unit
```

Flushes the compressed output stream. If [syncFlush](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#DeflaterOutputStream(java.io.OutputStream,%20java.util.zip.Deflater,%20kotlin.Int,%20kotlin.Boolean))is`true`when this compressed output stream is constructed, this method first flushes the underlying`compressor`with the flush mode [Deflater.SYNC_FLUSH](https://developer.android.com/reference/kotlin/java/util/zip/Deflater#SYNC_FLUSH:kotlin.Int) to force all pending data to be flushed out to the output stream and then flushes the output stream. Otherwise this method only flushes the output stream without flushing the`compressor`.

| Exceptions ||
|-----------------------|------------------------------|
| `java.io.IOException` | if an I/O error has occurred |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Writes an array of bytes to the compressed output stream. This method will block until all the bytes are written.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data to be written |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset of the data |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the length of the data |
| --- | --- |

| Exceptions ||
|-----------------------|------------------------------|
| `java.io.IOException` | if an I/O error has occurred |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(b: Int): Unit
```

Writes a byte to the compressed output stream. This method will block until the byte can be written.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------|
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the byte to be written |

| Exceptions ||
|-----------------------|------------------------------|
| `java.io.IOException` | if an I/O error has occurred |

## Protected methods

### deflate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun deflate(): Unit
```

Writes next block of compressed data to the output stream.

| Exceptions ||
|-----------------------|------------------------------|
| `java.io.IOException` | if an I/O error has occurred |

## Properties

### buf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var buf: ByteArray!
```

Output buffer for writing compressed data. 

### def

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var def: Deflater!
```

Compressor for this stream.
