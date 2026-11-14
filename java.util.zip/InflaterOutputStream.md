# InflaterOutputStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InflaterOutputStream

```
open class InflaterOutputStream : FilterOutputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.io.OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#) |||
| | ↳ | [java.io.FilterOutputStream](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#) ||
| | | ↳ | [java.util.zip.InflaterOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/InflaterOutputStream#) |
| --- | --- | --- | --- |

Implements an output stream filter for uncompressing data stored in the "deflate" compression format.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InflaterOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/InflaterOutputStream#InflaterOutputStream(java.io.OutputStream))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`)` Creates a new output stream with a default decompressor and buffer size. |
| [InflaterOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/InflaterOutputStream#InflaterOutputStream(java.io.OutputStream,%20java.util.zip.Inflater))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`, `infl:` ` [Inflater](https://developer.android.com/reference/kotlin/java/util/zip/Inflater)!`)` Creates a new output stream with the specified decompressor and a default buffer size. |
| [InflaterOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/InflaterOutputStream#InflaterOutputStream(java.io.OutputStream,%20java.util.zip.Inflater,%20kotlin.Int))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`, `infl:` ` [Inflater](https://developer.android.com/reference/kotlin/java/util/zip/Inflater)!`, `bufLen:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new output stream with the specified decompressor and buffer size. |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/util/zip/InflaterOutputStream#close())`()` Writes any remaining uncompressed data to the output stream and closes the underlying output stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finish](https://developer.android.com/reference/kotlin/java/util/zip/InflaterOutputStream#finish())`()` Finishes writing uncompressed data to the output stream without closing the underlying stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](https://developer.android.com/reference/kotlin/java/util/zip/InflaterOutputStream#flush())`()` Flushes this output stream, forcing any pending buffered output bytes to be written. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/util/zip/InflaterOutputStream#write(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes an array of bytes to the uncompressed output stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/util/zip/InflaterOutputStream#write(kotlin.Int))`(`b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a byte to the uncompressed output stream. |

| Inherited functions ||
|---|---|
| From class [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#) |--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | [nullOutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#nullOutputStream())`()` <br /> Returns a new`OutputStream`which discards all bytes. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`write(int)`,`write(byte[])`, and`write(byte[], int, int)`methods do nothing. After the stream has been closed, these methods all throw`IOException`. The`flush()`method does nothing. <br /> | ||
| From class [FilterOutputStream](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#) |------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#write(kotlin.ByteArray))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Writes`b.length`bytes to this output stream. The`write`method of`FilterOutputStream`calls its`write`method of three arguments with the arguments`b`,`0`, and`b.length`. Note that this method does not call the one-argument`write`method of its underlying output stream with the single argument`b`. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [buf](https://developer.android.com/reference/kotlin/java/util/zip/InflaterOutputStream#buf:kotlin.ByteArray) Output buffer for writing uncompressed data. |
| [Inflater](https://developer.android.com/reference/kotlin/java/util/zip/Inflater)! | [inf](https://developer.android.com/reference/kotlin/java/util/zip/InflaterOutputStream#inf:java.util.zip.Inflater) Decompressor for this stream. |

| Inherited properties ||
|---|---|
| From class [FilterOutputStream](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#) |--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | [out](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#out:java.io.OutputStream) <br /> The underlying output stream to be filtered. <br /> | ||

## Public constructors

### InflaterOutputStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InflaterOutputStream(out: OutputStream!)
```

Creates a new output stream with a default decompressor and buffer size.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!:output stream to write the uncompressed data to |

| Exceptions ||
|----------------------------------|----------------|
| `java.lang.NullPointerException` | if`out`is null |

### InflaterOutputStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InflaterOutputStream(
    out: OutputStream!, 
    infl: Inflater!)
```

Creates a new output stream with the specified decompressor and a default buffer size.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!:output stream to write the uncompressed data to |
| `infl` | [Inflater](https://developer.android.com/reference/kotlin/java/util/zip/Inflater)!:decompressor ("inflater") for this stream |

| Exceptions ||
|----------------------------------|------------------------|
| `java.lang.NullPointerException` | if`out`or`infl`is null |

### InflaterOutputStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InflaterOutputStream(
    out: OutputStream!, 
    infl: Inflater!, 
    bufLen: Int)
```

Creates a new output stream with the specified decompressor and buffer size.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!:output stream to write the uncompressed data to |
| `infl` | [Inflater](https://developer.android.com/reference/kotlin/java/util/zip/Inflater)!:decompressor ("inflater") for this stream |
| `bufLen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):decompression buffer size |
| --- | --- |

| Exceptions ||
|--------------------------------------|------------------------|
| `java.lang.IllegalArgumentException` | if`bufLen <= 0` |
| `java.lang.NullPointerException` | if`out`or`infl`is null |

## Public methods

### close

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Writes any remaining uncompressed data to the output stream and closes the underlying output stream.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

### finish

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun finish(): Unit
```

Finishes writing uncompressed data to the output stream without closing the underlying stream. Use this method when applying multiple filters in succession to the same output stream.

| Exceptions ||
|-----------------------|---------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs or this stream is already closed |

### flush

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun flush(): Unit
```

Flushes this output stream, forcing any pending buffered output bytes to be written.

| Exceptions ||
|-----------------------|---------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs or this stream is already closed |

### write

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Writes an array of bytes to the uncompressed output stream.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:buffer containing compressed data to decompress and write to the output stream |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):starting offset of the compressed data within`b` |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of bytes to decompress from`b` |
| --- | --- |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs or this stream is already closed |
| `java.lang.IndexOutOfBoundsException` | if`off < 0`, or if`len < 0`, or if`len > b.length - off` |
| `java.lang.NullPointerException` | if`b`is null |
| --- | --- |
| `java.util.zip.ZipException` | if a compression (ZIP) format error occurs |

### write

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(b: Int): Unit
```

Writes a byte to the uncompressed output stream.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a single byte of compressed data to decompress and write to the output stream |

| Exceptions ||
|------------------------------|---------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs or this stream is already closed |
| `java.util.zip.ZipException` | if a compression (ZIP) format error occurs |

## Properties

### buf

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected val buf: ByteArray!
```

Output buffer for writing uncompressed data. 

### inf

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected val inf: Inflater!
```

Decompressor for this stream.
