# ZipFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ZipFile

```
open class ZipFile : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.zip.ZipFile](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#) |

| Known Direct Subclasses [JarFile](https://developer.android.com/reference/kotlin/java/util/jar/JarFile.html#) |---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------| | [JarFile](https://developer.android.com/reference/kotlin/java/util/jar/JarFile.html#) | The`JarFile`class is used to read the contents of a jar file from any file that can be opened with`java.io.RandomAccessFile`. | |
| --- | --- | --- | --- | --- | --- | --- |

This class is used to read entries from a zip file.

Unless otherwise noted, passing a`null`argument to a constructor or method in this class will cause a [NullPointerException](https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#) to be thrown.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENATT](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#CENATT:kotlin.Int) Central directory (CEN) header internal file attributes field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENATX](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#CENATX:kotlin.Int) Central directory (CEN) header external file attributes field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENCOM](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#CENCOM:kotlin.Int) Central directory (CEN) header comment length field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENCRC](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#CENCRC:kotlin.Int) Central directory (CEN) header uncompressed file crc-32 value field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENDSK](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#CENDSK:kotlin.Int) Central directory (CEN) header disk number start field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENEXT](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#CENEXT:kotlin.Int) Central directory (CEN) header extra field length field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENFLG](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#CENFLG:kotlin.Int) Central directory (CEN) header encrypt, decrypt flags field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENHDR](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#CENHDR:kotlin.Int) Central directory (CEN) header size in bytes (including signature). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENHOW](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#CENHOW:kotlin.Int) Central directory (CEN) header compression method field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENLEN](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#CENLEN:kotlin.Int) Central directory (CEN) header uncompressed size field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENNAM](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#CENNAM:kotlin.Int) Central directory (CEN) header filename length field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENOFF](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#CENOFF:kotlin.Int) Central directory (CEN) header LOC header offset field offset. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [CENSIG](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#CENSIG:kotlin.Long) Central directory (CEN) header signature. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENSIZ](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#CENSIZ:kotlin.Int) Central directory (CEN) header compressed size field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENTIM](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#CENTIM:kotlin.Int) Central directory (CEN) header modification time field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENVEM](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#CENVEM:kotlin.Int) Central directory (CEN) header version made by field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENVER](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#CENVER:kotlin.Int) Central directory (CEN) header version needed to extract field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDCOM](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#ENDCOM:kotlin.Int) End of central directory (END) header zip file comment length field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDHDR](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#ENDHDR:kotlin.Int) End of central directory (END) header size in bytes (including signature). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDOFF](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#ENDOFF:kotlin.Int) End of central directory (END) header offset for the first CEN header field offset. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ENDSIG](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#ENDSIG:kotlin.Long) End of central directory (END) header signature. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDSIZ](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#ENDSIZ:kotlin.Int) End of central directory (END) header central directory size in bytes field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDSUB](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#ENDSUB:kotlin.Int) End of central directory (END) header number of entries on this disk field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDTOT](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#ENDTOT:kotlin.Int) End of central directory (END) header total number of entries field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXTCRC](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#EXTCRC:kotlin.Int) Extra local (EXT) header uncompressed file crc-32 value field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXTHDR](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#EXTHDR:kotlin.Int) Extra local (EXT) header size in bytes (including signature). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXTLEN](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#EXTLEN:kotlin.Int) Extra local (EXT) header uncompressed size field offset. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [EXTSIG](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#EXTSIG:kotlin.Long) Extra local (EXT) header signature. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXTSIZ](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#EXTSIZ:kotlin.Int) Extra local (EXT) header compressed size field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCCRC](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#LOCCRC:kotlin.Int) Local file (LOC) header uncompressed file crc-32 value field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCEXT](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#LOCEXT:kotlin.Int) Local file (LOC) header extra field length field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCFLG](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#LOCFLG:kotlin.Int) Local file (LOC) header general purpose bit flag field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCHDR](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#LOCHDR:kotlin.Int) Local file (LOC) header size in bytes (including signature). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCHOW](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#LOCHOW:kotlin.Int) Local file (LOC) header compression method field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCLEN](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#LOCLEN:kotlin.Int) Local file (LOC) header uncompressed size field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCNAM](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#LOCNAM:kotlin.Int) Local file (LOC) header filename length field offset. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [LOCSIG](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#LOCSIG:kotlin.Long) Local file (LOC) header signature. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCSIZ](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#LOCSIZ:kotlin.Int) Local file (LOC) header compressed size field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCTIM](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#LOCTIM:kotlin.Int) Local file (LOC) header modification time field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCVER](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#LOCVER:kotlin.Int) Local file (LOC) header version needed to extract field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OPEN_DELETE](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#OPEN_DELETE:kotlin.Int) Mode flag to open a zip file and mark it for deletion. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OPEN_READ](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#OPEN_READ:kotlin.Int) Mode flag to open a zip file for reading. |
| --- | --- |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ZipFile](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#ZipFile(java.io.File))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`)` Opens a ZIP file for reading given the specified File object. |
| [ZipFile](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#ZipFile(java.io.File,%20kotlin.Int))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`, `mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Opens a new`ZipFile`to read from the specified`File`object in the specified mode. |
| [ZipFile](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#ZipFile(java.io.File,%20kotlin.Int,%20java.nio.charset.Charset))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`, `mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `charset:` ` [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!`)` Opens a new`ZipFile`to read from the specified`File`object in the specified mode. |
| [ZipFile](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#ZipFile(java.io.File,%20java.nio.charset.Charset))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`, `charset:` ` [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!`)` Opens a ZIP file for reading given the specified File object. |
| [ZipFile](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#ZipFile(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Opens a zip file for reading. |
| [ZipFile](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#ZipFile(kotlin.String,%20java.nio.charset.Charset))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `charset:` ` [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!`)` Opens a zip file for reading. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#close())`()` Closes the ZIP file. |
| open [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration.html#)\<out [ZipEntry](https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry)!\>! | [entries](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#entries())`()` Returns an enumeration of the ZIP file entries. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getComment](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#getComment())`()` Returns the zip file comment, or null if none. |
| --- | --- |
| open [ZipEntry](https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry)! | [getEntry](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#getEntry(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the zip file entry for the specified name, or null if not found. |
| open [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | [getInputStream](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#getInputStream(java.util.zip.ZipEntry))`(`entry:` ` [ZipEntry](https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry)!`)` Returns an input stream for reading the contents of the specified zip file entry. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#getName())`()` Returns the path name of the ZIP file. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#size())`()` Returns the number of entries in the ZIP file. |
| open [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#)\<out [ZipEntry](https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry)!\>! | [stream](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#stream())`()` Returns an ordered`Stream`over the ZIP file entries. |

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

### OPEN_DELETE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPEN_DELETE: Int
```

Mode flag to open a zip file and mark it for deletion. The file will be deleted some time between the moment that it is opened and the moment that it is closed, but its contents will remain accessible via the`ZipFile`object until either the close method is invoked or the virtual machine exits. 

 Value: 4

### OPEN_READ

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPEN_READ: Int
```

Mode flag to open a zip file for reading. 

 Value: 1

## Public constructors

### ZipFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ZipFile(file: File!)
```

Opens a ZIP file for reading given the specified File object.

The UTF-8 [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) is used to decode the entry names and comments.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!:the ZIP file to be opened for reading |

| Exceptions ||
|------------------------------|------------------------------------|
| `java.util.zip.ZipException` | if a ZIP format error has occurred |
| `java.io.IOException` | if an I/O error has occurred |

### ZipFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ZipFile(
    file: File!, 
    mode: Int)
```

Opens a new`ZipFile`to read from the specified`File`object in the specified mode. The mode argument must be either`OPEN_READ`or`OPEN_READ | OPEN_DELETE`.
| --- | --- |

First, if there is a security manager, its`checkRead`method is called with the`name`argument as its argument to ensure the read is allowed.

The UTF-8 [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) is used to decode the entry names and comments

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!:the ZIP file to be opened for reading |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the mode in which the file is to be opened |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.zip.ZipException` | if a ZIP format error has occurred |
| `java.io.IOException` | if an I/O error has occurred |
| `java.lang.SecurityException` | if a security manager exists and its`checkRead`method doesn't allow read access to the file, or its`checkDelete`method doesn't allow deleting the file when the`OPEN_DELETE`flag is set. |
| --- | --- |
| `java.lang.IllegalArgumentException` | if the`mode`argument is invalid |

**See Also**

- [java.lang.SecurityManager#checkRead(java.lang.String)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String)) 

### ZipFile

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ZipFile(
    file: File!, 
    mode: Int, 
    charset: Charset!)
```

Opens a new`ZipFile`to read from the specified`File`object in the specified mode. The mode argument must be either`OPEN_READ`or`OPEN_READ | OPEN_DELETE`.
| --- | --- |

First, if there is a security manager, its`checkRead`method is called with the`name`argument as its argument to ensure the read is allowed.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!:the ZIP file to be opened for reading |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the mode in which the file is to be opened |
| `charset` | [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!:the [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) to be used to decode the ZIP entry name and comment that are not encoded by using UTF-8 encoding (indicated by entry's general purpose flag). |
| --- | --- |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.zip.ZipException` | if a ZIP format error has occurred |
| `java.io.IOException` | if an I/O error has occurred |
| `java.lang.SecurityException` | if a security manager exists and its`checkRead`method doesn't allow read access to the file,or its`checkDelete`method doesn't allow deleting the file when the`OPEN_DELETE`flag is set |
| --- | --- |
| `java.lang.IllegalArgumentException` | if the`mode`argument is invalid |

**See Also**

- [java.lang.SecurityManager#checkRead(java.lang.String)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String)) 

### ZipFile

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ZipFile(
    file: File!, 
    charset: Charset!)
```

Opens a ZIP file for reading given the specified File object.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!:the ZIP file to be opened for reading |
| `charset` | [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!:The [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) to be used to decode the ZIP entry name and comment (ignored if the [language encoding bit](https://developer.android.com/reference/kotlin/java/util/zip/package-summary#lang_encoding) of the ZIP entry's general purpose bit flag is set). |

| Exceptions ||
|------------------------------|------------------------------------|
| `java.util.zip.ZipException` | if a ZIP format error has occurred |
| `java.io.IOException` | if an I/O error has occurred |

### ZipFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ZipFile(name: String!)
```

Opens a zip file for reading.

First, if there is a security manager, its`checkRead`method is called with the`name`argument as its argument to ensure the read is allowed.

The UTF-8 [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) is used to decode the entry names and comments.

If the app targets Android U or above, zip file entry names containing ".." or starting with "/" passed here will throw a [ZipException](https://developer.android.com/reference/kotlin/java/util/zip/ZipException). For more details, see [dalvik.system.ZipPathValidator](https://developer.android.com/reference/kotlin/dalvik/system/ZipPathValidator.html#).

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the zip file |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.zip.ZipException` | if (1) a ZIP format error has occurred or (2)`targetSdkVersion >= BUILD.VERSION_CODES.UPSIDE_DOWN_CAKE`and (the`name`argument contains ".." or starts with "/"). |
| `java.io.IOException` | if an I/O error has occurred |
| `java.lang.SecurityException` | if a security manager exists and its`checkRead`method doesn't allow read access to the file. |
| --- | --- |

**See Also**

- [java.lang.SecurityManager#checkRead(java.lang.String)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String)) 

### ZipFile

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ZipFile(
    name: String!, 
    charset: Charset!)
```

Opens a zip file for reading.

First, if there is a security manager, its`checkRead`method is called with the`name`argument as its argument to ensure the read is allowed.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the zip file |
| `charset` | [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!:the [charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) to be used to decode the ZIP entry name and comment that are not encoded by using UTF-8 encoding (indicated by entry's general purpose flag). |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------------------|
| `java.util.zip.ZipException` | if a ZIP format error has occurred |
| `java.io.IOException` | if an I/O error has occurred |
| `java.lang.SecurityException` | if a security manager exists and its`checkRead`method doesn't allow read access to the file |
| --- | --- |

**See Also**

- [java.lang.SecurityManager#checkRead(java.lang.String)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String))

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Closes the ZIP file.

Closing this ZIP file will close all of the input streams previously returned by invocations of the [getInputStream](https://developer.android.com/reference/kotlin/java/util/zip/ZipFile#getInputStream(java.util.zip.ZipEntry))method.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error has occurred |

### entries

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun entries(): Enumeration<out ZipEntry!>!
```

Returns an enumeration of the ZIP file entries.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration.html#)<out` ` [ZipEntry](https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry)!>! | an enumeration of the ZIP file entries |

| Exceptions ||
|-----------------------------------|---------------------------------|
| `java.lang.IllegalStateException` | if the zip file has been closed |

### getComment

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getComment(): String!
```

Returns the zip file comment, or null if none.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the comment string for the zip file, or null if none |

| Exceptions ||
|-----------------------------------|---------------------------------|
| `java.lang.IllegalStateException` | if the zip file has been closed |

### getEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEntry(name: String!): ZipEntry!
```

Returns the zip file entry for the specified name, or null if not found.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the entry |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [ZipEntry](https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry)! | the zip file entry, or null if not found |

| Exceptions ||
|-----------------------------------|---------------------------------|
| `java.lang.IllegalStateException` | if the zip file has been closed |

### getInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInputStream(entry: ZipEntry!): InputStream!
```

Returns an input stream for reading the contents of the specified zip file entry.

Closing this ZIP file will, in turn, close all input streams that have been returned by invocations of this method.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------|
| `entry` | [ZipEntry](https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry)!:the zip file entry |

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | the input stream for reading the contents of the specified zip file entry. |

| Exceptions ||
|-----------------------------------|------------------------------------|
| `java.util.zip.ZipException` | if a ZIP format error has occurred |
| `java.io.IOException` | if an I/O error has occurred |
| `java.lang.IllegalStateException` | if the zip file has been closed |
| --- | --- |

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getName(): String!
```

Returns the path name of the ZIP file.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the path name of the ZIP file |

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun size(): Int
```

Returns the number of entries in the ZIP file.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of entries in the ZIP file |

| Exceptions ||
|-----------------------------------|---------------------------------|
| `java.lang.IllegalStateException` | if the zip file has been closed |

### stream

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stream(): Stream<out ZipEntry!>!
```

Returns an ordered`Stream`over the ZIP file entries. Entries appear in the`Stream`in the order they appear in the central directory of the ZIP file.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#)<out` ` [ZipEntry](https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry)!>! | an ordered`Stream`of entries in this ZIP file |

| Exceptions ||
|-----------------------------------|---------------------------------|
| `java.lang.IllegalStateException` | if the zip file has been closed |
