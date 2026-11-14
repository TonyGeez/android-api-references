Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JarOutputStream

```
open class JarOutputStream : ZipOutputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [java.io.OutputStream](../java.io/OutputStream.md) |||||
| | ↳ | [java.io.FilterOutputStream](../java.io/FilterOutputStream.md) ||||
| | | ↳ | [java.util.zip.DeflaterOutputStream](../java.util.zip/DeflaterOutputStream.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.util.zip.ZipOutputStream](../java.util.zip/ZipOutputStream.md) ||
| | | | | ↳ | [java.util.jar.JarOutputStream](JarOutputStream.md) |

The `JarOutputStream` class is used to write the contents of a JAR file to any output stream. It extends the class `java.util.zip.ZipOutputStream` with support for writing an optional `Manifest` entry. The `Manifest` can be used to specify meta-information about the JAR file and its entries.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#CENATT:kotlin.Int` Central directory (CEN) header internal file attributes field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#CENATX:kotlin.Int` Central directory (CEN) header external file attributes field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#CENCOM:kotlin.Int` Central directory (CEN) header comment length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#CENCRC:kotlin.Int` Central directory (CEN) header uncompressed file crc-32 value field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#CENDSK:kotlin.Int` Central directory (CEN) header disk number start field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#CENEXT:kotlin.Int` Central directory (CEN) header extra field length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#CENFLG:kotlin.Int` Central directory (CEN) header encrypt, decrypt flags field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#CENHDR:kotlin.Int` Central directory (CEN) header size in bytes (including signature). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#CENHOW:kotlin.Int` Central directory (CEN) header compression method field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#CENLEN:kotlin.Int` Central directory (CEN) header uncompressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#CENNAM:kotlin.Int` Central directory (CEN) header filename length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#CENOFF:kotlin.Int` Central directory (CEN) header LOC header offset field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#CENSIG:kotlin.Long` Central directory (CEN) header signature. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#CENSIZ:kotlin.Int` Central directory (CEN) header compressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#CENTIM:kotlin.Int` Central directory (CEN) header modification time field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#CENVEM:kotlin.Int` Central directory (CEN) header version made by field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#CENVER:kotlin.Int` Central directory (CEN) header version needed to extract field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#DEFLATED:kotlin.Int` Compression method for compressed (DEFLATED) entries. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#ENDCOM:kotlin.Int` End of central directory (END) header zip file comment length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#ENDHDR:kotlin.Int` End of central directory (END) header size in bytes (including signature). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#ENDOFF:kotlin.Int` End of central directory (END) header offset for the first CEN header field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#ENDSIG:kotlin.Long` End of central directory (END) header signature. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#ENDSIZ:kotlin.Int` End of central directory (END) header central directory size in bytes field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#ENDSUB:kotlin.Int` End of central directory (END) header number of entries on this disk field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#ENDTOT:kotlin.Int` End of central directory (END) header total number of entries field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#EXTCRC:kotlin.Int` Extra local (EXT) header uncompressed file crc-32 value field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#EXTHDR:kotlin.Int` Extra local (EXT) header size in bytes (including signature). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#EXTLEN:kotlin.Int` Extra local (EXT) header uncompressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#EXTSIG:kotlin.Long` Extra local (EXT) header signature. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#EXTSIZ:kotlin.Int` Extra local (EXT) header compressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#LOCCRC:kotlin.Int` Local file (LOC) header uncompressed file crc-32 value field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#LOCEXT:kotlin.Int` Local file (LOC) header extra field length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#LOCFLG:kotlin.Int` Local file (LOC) header general purpose bit flag field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#LOCHDR:kotlin.Int` Local file (LOC) header size in bytes (including signature). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#LOCHOW:kotlin.Int` Local file (LOC) header compression method field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#LOCLEN:kotlin.Int` Local file (LOC) header uncompressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#LOCNAM:kotlin.Int` Local file (LOC) header filename length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#LOCSIG:kotlin.Long` Local file (LOC) header signature. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#LOCSIZ:kotlin.Int` Local file (LOC) header compressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#LOCTIM:kotlin.Int` Local file (LOC) header modification time field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#LOCVER:kotlin.Int` Local file (LOC) header version needed to extract field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#STORED:kotlin.Int` Compression method for uncompressed (STORED) entries. <br /> | ||

| Public constructors ||
|---|---|
| JarOutputStream Creates a new `JarOutputStream` with no manifest. |
| JarOutputStream Creates a new `JarOutputStream` with the specified `Manifest`. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | putNextEntry Begins writing a new JAR file entry and positions the stream to the start of the entry data. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | close Closes the ZIP output stream as well as the stream being filtered. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | closeEntry Closes the current ZIP entry and positions the stream for writing the next entry. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | finish Finishes writing the contents of the ZIP output stream without closing the underlying stream. Use this method when applying multiple filters in succession to the same output stream. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setComment Sets the ZIP file comment. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setLevel Sets the compression level for subsequent entries which are DEFLATED. The default setting is DEFAULT_COMPRESSION. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setMethod Sets the default compression method for subsequent entries. This default will be used whenever the compression method is not specified for an individual ZIP file entry, and is initially set to DEFLATED. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | write Writes an array of bytes to the current ZIP entry data. This method will block until all the bytes are written. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | deflate Writes next block of compressed data to the output stream. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | flush Flushes the compressed output stream. If DeflaterOutputStream is `true` when this compressed output stream is constructed, this method first flushes the underlying `compressor` with the flush mode `https://developer.android.com/reference/kotlin/java/util/zip/Deflater.html#SYNC_FLUSH:kotlin.Int` to force all pending data to be flushed out to the output stream and then flushes the output stream. Otherwise this method only flushes the output stream without flushing the `compressor`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | write Writes a byte to the compressed output stream. This method will block until the byte can be written. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/io/OutputStream.html#` |---|---| | `https://developer.android.com/reference/kotlin/java/io/OutputStream.html#!` | nullOutputStream Returns a new `OutputStream` which discards all bytes. The returned stream is initially open. The stream is closed by calling the `close()` method. Subsequent calls to `close()` have no effect. While the stream is open, the `write(int)`, `write(byte[])`, and `write(byte[], int, int)` methods do nothing. After the stream has been closed, these methods all throw `IOException`. The `flush()` method does nothing. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- |
| From class `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | write Writes `b.length` bytes to this output stream. The `write` method of `FilterOutputStream` calls its `write` method of three arguments with the arguments `b`, `0`, and `b.length`. Note that this method does not call the one-argument `write` method of its underlying output stream with the single argument `b`. <br /> | ||

| Inherited properties ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | `https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream.html#buf:kotlin.ByteArray` Output buffer for writing compressed data. <br /> | | `https://developer.android.com/reference/kotlin/java/util/zip/Deflater.html#!` | `https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream.html#def:java.util.zip.Deflater` Compressor for this stream. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#` |---|---| | `https://developer.android.com/reference/kotlin/java/io/OutputStream.html#!` | `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#out:java.io.OutputStream` The underlying output stream to be filtered. <br /> | ||

## Public constructors

### JarOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
JarOutputStream(out: OutputStream!)
```

Creates a new `JarOutputStream` with no manifest.

| Parameters ||
|---|---|
| `out` | [OutputStream](../java.io/OutputStream.md)!: the actual output stream |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error has occurred |

### JarOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
JarOutputStream(
    out: OutputStream!, 
    man: Manifest!)
```

Creates a new `JarOutputStream` with the specified `Manifest`. The manifest is written as the first entry to the output stream.

| Parameters ||
|---|---|
| `out` | [OutputStream](../java.io/OutputStream.md)!: the actual output stream |
| `man` | [Manifest](Manifest.md)!: the optional `Manifest` |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error has occurred |

## Public methods

### putNextEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun putNextEntry(ze: ZipEntry!): Unit
```

Begins writing a new JAR file entry and positions the stream to the start of the entry data. This method will also close any previous entry. The default compression method will be used if no compression method was specified for the entry. The current time will be used if the entry has no set modification time.

| Parameters ||
|---|---|
| `e` | the ZIP entry to be written |
| `ze` | [ZipEntry](../java.util.zip/ZipEntry.md)!: the ZIP/JAR entry to be written |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error has occurred |
| `java.util.zip.ZipException` | if a ZIP error has occurred |
