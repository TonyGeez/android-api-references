# ZipOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ZipOutputStream

```
open class ZipOutputStream : DeflaterOutputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [java.io.OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#) ||||
| | ↳ | [java.io.FilterOutputStream](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#) |||
| | | ↳ | [java.util.zip.DeflaterOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream) ||
| | | | ↳ | [java.util.zip.ZipOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#) |

| Known Direct Subclasses [JarOutputStream](https://developer.android.com/reference/kotlin/java/util/jar/JarOutputStream.html#) |-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------| | [JarOutputStream](https://developer.android.com/reference/kotlin/java/util/jar/JarOutputStream.html#) | The`JarOutputStream`class is used to write the contents of a JAR file to any output stream. | |

This class implements an output stream filter for writing files in the ZIP file format. Includes support for both compressed and uncompressed entries.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENATT](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#CENATT:kotlin.Int) Central directory (CEN) header internal file attributes field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENATX](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#CENATX:kotlin.Int) Central directory (CEN) header external file attributes field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENCOM](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#CENCOM:kotlin.Int) Central directory (CEN) header comment length field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENCRC](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#CENCRC:kotlin.Int) Central directory (CEN) header uncompressed file crc-32 value field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENDSK](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#CENDSK:kotlin.Int) Central directory (CEN) header disk number start field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENEXT](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#CENEXT:kotlin.Int) Central directory (CEN) header extra field length field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENFLG](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#CENFLG:kotlin.Int) Central directory (CEN) header encrypt, decrypt flags field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENHDR](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#CENHDR:kotlin.Int) Central directory (CEN) header size in bytes (including signature). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENHOW](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#CENHOW:kotlin.Int) Central directory (CEN) header compression method field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENLEN](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#CENLEN:kotlin.Int) Central directory (CEN) header uncompressed size field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENNAM](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#CENNAM:kotlin.Int) Central directory (CEN) header filename length field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENOFF](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#CENOFF:kotlin.Int) Central directory (CEN) header LOC header offset field offset. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [CENSIG](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#CENSIG:kotlin.Long) Central directory (CEN) header signature. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENSIZ](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#CENSIZ:kotlin.Int) Central directory (CEN) header compressed size field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENTIM](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#CENTIM:kotlin.Int) Central directory (CEN) header modification time field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENVEM](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#CENVEM:kotlin.Int) Central directory (CEN) header version made by field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENVER](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#CENVER:kotlin.Int) Central directory (CEN) header version needed to extract field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEFLATED](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#DEFLATED:kotlin.Int) Compression method for compressed (DEFLATED) entries. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDCOM](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#ENDCOM:kotlin.Int) End of central directory (END) header zip file comment length field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDHDR](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#ENDHDR:kotlin.Int) End of central directory (END) header size in bytes (including signature). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDOFF](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#ENDOFF:kotlin.Int) End of central directory (END) header offset for the first CEN header field offset. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ENDSIG](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#ENDSIG:kotlin.Long) End of central directory (END) header signature. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDSIZ](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#ENDSIZ:kotlin.Int) End of central directory (END) header central directory size in bytes field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDSUB](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#ENDSUB:kotlin.Int) End of central directory (END) header number of entries on this disk field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDTOT](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#ENDTOT:kotlin.Int) End of central directory (END) header total number of entries field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXTCRC](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#EXTCRC:kotlin.Int) Extra local (EXT) header uncompressed file crc-32 value field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXTHDR](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#EXTHDR:kotlin.Int) Extra local (EXT) header size in bytes (including signature). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXTLEN](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#EXTLEN:kotlin.Int) Extra local (EXT) header uncompressed size field offset. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [EXTSIG](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#EXTSIG:kotlin.Long) Extra local (EXT) header signature. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXTSIZ](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#EXTSIZ:kotlin.Int) Extra local (EXT) header compressed size field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCCRC](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#LOCCRC:kotlin.Int) Local file (LOC) header uncompressed file crc-32 value field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCEXT](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#LOCEXT:kotlin.Int) Local file (LOC) header extra field length field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCFLG](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#LOCFLG:kotlin.Int) Local file (LOC) header general purpose bit flag field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCHDR](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#LOCHDR:kotlin.Int) Local file (LOC) header size in bytes (including signature). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCHOW](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#LOCHOW:kotlin.Int) Local file (LOC) header compression method field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCLEN](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#LOCLEN:kotlin.Int) Local file (LOC) header uncompressed size field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCNAM](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#LOCNAM:kotlin.Int) Local file (LOC) header filename length field offset. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [LOCSIG](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#LOCSIG:kotlin.Long) Local file (LOC) header signature. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCSIZ](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#LOCSIZ:kotlin.Int) Local file (LOC) header compressed size field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCTIM](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#LOCTIM:kotlin.Int) Local file (LOC) header modification time field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCVER](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#LOCVER:kotlin.Int) Local file (LOC) header version needed to extract field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STORED](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#STORED:kotlin.Int) Compression method for uncompressed (STORED) entries. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ZipOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#ZipOutputStream(java.io.OutputStream))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`)` Creates a new ZIP output stream. |
| [ZipOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#ZipOutputStream(java.io.OutputStream,%20java.nio.charset.Charset))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`, `charset:` ` [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!`)` Creates a new ZIP output stream. |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#close())`()` Closes the ZIP output stream as well as the stream being filtered. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [closeEntry](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#closeEntry())`()` Closes the current ZIP entry and positions the stream for writing the next entry. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finish](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#finish())`()` Finishes writing the contents of the ZIP output stream without closing the underlying stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putNextEntry](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#putNextEntry(java.util.zip.ZipEntry))`(`e:` ` [ZipEntry](https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry)!`)` Begins writing a new ZIP file entry and positions the stream to the start of the entry data. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setComment](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#setComment(kotlin.String))`(`comment:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the ZIP file comment. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLevel](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#setLevel(kotlin.Int))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the compression level for subsequent entries which are DEFLATED. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMethod](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#setMethod(kotlin.Int))`(`method:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the default compression method for subsequent entries. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/util/zip/ZipOutputStream#write(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes an array of bytes to the current ZIP entry data. |

| Inherited functions ||
|---|---|
| From class [DeflaterOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream) |------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deflate](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#deflate())`()` <br /> Writes next block of compressed data to the output stream. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#flush())`()` <br /> Flushes the compressed output stream. If [syncFlush](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#DeflaterOutputStream(java.io.OutputStream,%20java.util.zip.Deflater,%20kotlin.Int,%20kotlin.Boolean))is`true`when this compressed output stream is constructed, this method first flushes the underlying`compressor`with the flush mode [Deflater.SYNC_FLUSH](https://developer.android.com/reference/kotlin/java/util/zip/Deflater#SYNC_FLUSH:kotlin.Int) to force all pending data to be flushed out to the output stream and then flushes the output stream. Otherwise this method only flushes the output stream without flushing the`compressor`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#write(kotlin.Int))`(`b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Writes a byte to the compressed output stream. This method will block until the byte can be written. <br /> | ||
| From class [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#) |--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | [nullOutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#nullOutputStream())`()` <br /> Returns a new`OutputStream`which discards all bytes. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`write(int)`,`write(byte[])`, and`write(byte[], int, int)`methods do nothing. After the stream has been closed, these methods all throw`IOException`. The`flush()`method does nothing. <br /> | ||
| From class [FilterOutputStream](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#) |------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#write(kotlin.ByteArray))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Writes`b.length`bytes to this output stream. The`write`method of`FilterOutputStream`calls its`write`method of three arguments with the arguments`b`,`0`, and`b.length`. Note that this method does not call the one-argument`write`method of its underlying output stream with the single argument`b`. <br /> | ||

| Inherited properties ||
|---|---|
| From class [DeflaterOutputStream](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream) |------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [buf](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#buf:kotlin.ByteArray) <br /> Output buffer for writing compressed data. <br /> | | [Deflater](https://developer.android.com/reference/kotlin/java/util/zip/Deflater)! | [def](https://developer.android.com/reference/kotlin/java/util/zip/DeflaterOutputStream#def:java.util.zip.Deflater) <br /> Compressor for this stream. <br /> | ||
| From class [FilterOutputStream](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#) |--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | [out](https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#out:java.io.OutputStream) <br /> The underlying output stream to be filtered. <br /> | ||

## Constants

### CENATT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENATT: Int
```

Central directory (CEN) header internal file attributes field offset. 

 Value: 36

### CENATX

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENATX: Int
```

Central directory (CEN) header external file attributes field offset. 

 Value: 38

### CENCOM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENCOM: Int
```

Central directory (CEN) header comment length field offset. 

 Value: 32

### CENCRC

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENCRC: Int
```

Central directory (CEN) header uncompressed file crc-32 value field offset. 

 Value: 16

### CENDSK

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENDSK: Int
```

Central directory (CEN) header disk number start field offset. 

 Value: 34

### CENEXT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENEXT: Int
```

Central directory (CEN) header extra field length field offset. 

 Value: 30

### CENFLG

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENFLG: Int
```

Central directory (CEN) header encrypt, decrypt flags field offset. 

 Value: 8

### CENHDR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENHDR: Int
```

Central directory (CEN) header size in bytes (including signature). 

 Value: 46

### CENHOW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENHOW: Int
```

Central directory (CEN) header compression method field offset. 

 Value: 10

### CENLEN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENLEN: Int
```

Central directory (CEN) header uncompressed size field offset. 

 Value: 24

### CENNAM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENNAM: Int
```

Central directory (CEN) header filename length field offset. 

 Value: 28

### CENOFF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENOFF: Int
```

Central directory (CEN) header LOC header offset field offset. 

 Value: 42

### CENSIG

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENSIG: Long
```

Central directory (CEN) header signature. 

 Value: 33639248L

### CENSIZ

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENSIZ: Int
```

Central directory (CEN) header compressed size field offset. 

 Value: 20

### CENTIM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENTIM: Int
```

Central directory (CEN) header modification time field offset. 

 Value: 12

### CENVEM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENVEM: Int
```

Central directory (CEN) header version made by field offset. 

 Value: 4

### CENVER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CENVER: Int
```

Central directory (CEN) header version needed to extract field offset. 

 Value: 6

### DEFLATED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFLATED: Int
```

Compression method for compressed (DEFLATED) entries. 

 Value: 8

### ENDCOM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENDCOM: Int
```

End of central directory (END) header zip file comment length field offset. 

 Value: 20

### ENDHDR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENDHDR: Int
```

End of central directory (END) header size in bytes (including signature). 

 Value: 22

### ENDOFF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENDOFF: Int
```

End of central directory (END) header offset for the first CEN header field offset. 

 Value: 16

### ENDSIG

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENDSIG: Long
```

End of central directory (END) header signature. 

 Value: 101010256L

### ENDSIZ

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENDSIZ: Int
```

End of central directory (END) header central directory size in bytes field offset. 

 Value: 12

### ENDSUB

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENDSUB: Int
```

End of central directory (END) header number of entries on this disk field offset. 

 Value: 8

### ENDTOT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENDTOT: Int
```

End of central directory (END) header total number of entries field offset. 

 Value: 10

### EXTCRC

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTCRC: Int
```

Extra local (EXT) header uncompressed file crc-32 value field offset. 

 Value: 4

### EXTHDR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTHDR: Int
```

Extra local (EXT) header size in bytes (including signature). 

 Value: 16

### EXTLEN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTLEN: Int
```

Extra local (EXT) header uncompressed size field offset. 

 Value: 12

### EXTSIG

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTSIG: Long
```

Extra local (EXT) header signature. 

 Value: 134695760L

### EXTSIZ

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTSIZ: Int
```

Extra local (EXT) header compressed size field offset. 

 Value: 8

### LOCCRC

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCCRC: Int
```

Local file (LOC) header uncompressed file crc-32 value field offset. 

 Value: 14

### LOCEXT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCEXT: Int
```

Local file (LOC) header extra field length field offset. 

 Value: 28

### LOCFLG

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCFLG: Int
```

Local file (LOC) header general purpose bit flag field offset. 

 Value: 6

### LOCHDR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCHDR: Int
```

Local file (LOC) header size in bytes (including signature). 

 Value: 30

### LOCHOW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCHOW: Int
```

Local file (LOC) header compression method field offset. 

 Value: 8

### LOCLEN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCLEN: Int
```

Local file (LOC) header uncompressed size field offset. 

 Value: 22

### LOCNAM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCNAM: Int
```

Local file (LOC) header filename length field offset. 

 Value: 26

### LOCSIG

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCSIG: Long
```

Local file (LOC) header signature. 

 Value: 67324752L

### LOCSIZ

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCSIZ: Int
```

Local file (LOC) header compressed size field offset. 

 Value: 18

### LOCTIM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCTIM: Int
```

Local file (LOC) header modification time field offset. 

 Value: 10

### LOCVER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCVER: Int
```

Local file (LOC) header version needed to extract field offset. 

 Value: 4

### STORED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STORED: Int
```

Compression method for uncompressed (STORED) entries. 

 Value: 0

## Public constructors

### ZipOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ZipOutputStream(out: OutputStream!)
```

Creates a new ZIP output stream.

The UTF-8 [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) is used to encode the entry names and comments.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!:the actual output stream |

### ZipOutputStream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ZipOutputStream(
    out: OutputStream!, 
    charset: Charset!)
```

Creates a new ZIP output stream.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!:the actual output stream |
| `charset` | [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!:the [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) to be used to encode the entry names and comments |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes the ZIP output stream as well as the stream being filtered.

| Exceptions ||
|------------------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error has occurred |
| `java.util.zip.ZipException` | if a ZIP file error has occurred |

### closeEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun closeEntry(): Unit
```

Closes the current ZIP entry and positions the stream for writing the next entry.

| Exceptions ||
|------------------------------|------------------------------------|
| `java.util.zip.ZipException` | if a ZIP format error has occurred |
| `java.io.IOException` | if an I/O error has occurred |

### finish

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun finish(): Unit
```

Finishes writing the contents of the ZIP output stream without closing the underlying stream. Use this method when applying multiple filters in succession to the same output stream.

| Exceptions ||
|------------------------------|----------------------------------|
| `java.io.IOException` | if an I/O exception has occurred |
| `java.util.zip.ZipException` | if a ZIP file error has occurred |

### putNextEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putNextEntry(e: ZipEntry!): Unit
```

Begins writing a new ZIP file entry and positions the stream to the start of the entry data. Closes the current entry if still active.

The default compression method will be used if no compression method was specified for the entry. When writing a compressed (DEFLATED) entry, and the compressed size has not been explicitly set with the [ZipEntry.setCompressedSize(long)](https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry#setCompressedSize(kotlin.Long))method, then the compressed size will be set to the actual compressed size after deflation.

The current time will be used if the entry has no set modification time.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------|
| `e` | [ZipEntry](https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry)!:the ZIP entry to be written |

| Exceptions ||
|------------------------------|------------------------------------|
| `java.util.zip.ZipException` | if a ZIP format error has occurred |
| `java.io.IOException` | if an I/O error has occurred |

### setComment

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setComment(comment: String!): Unit
```

Sets the ZIP file comment.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------|
| `comment` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the comment string |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the length of the specified ZIP file comment is greater than 0xFFFF bytes |

### setLevel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLevel(level: Int): Unit
```

Sets the compression level for subsequent entries which are DEFLATED. The default setting is DEFAULT_COMPRESSION.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------|
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the compression level (0-9) |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalArgumentException` | if the compression level is invalid |

### setMethod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMethod(method: Int): Unit
```

Sets the default compression method for subsequent entries. This default will be used whenever the compression method is not specified for an individual ZIP file entry, and is initially set to DEFLATED.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------|
| `method` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the default compression method |

| Exceptions ||
|--------------------------------------|------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the specified compression method is invalid |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Writes an array of bytes to the current ZIP entry data. This method will block until all the bytes are written.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data to be written |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset in the data |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes that are written |

| Exceptions ||
|------------------------------|----------------------------------|
| `java.io.IOException` | if an I/O error has occurred |
| `java.util.zip.ZipException` | if a ZIP file error has occurred |
