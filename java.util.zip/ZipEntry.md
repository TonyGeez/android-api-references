# ZipEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ZipEntry

```
open class ZipEntry : Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.zip.ZipEntry](../java/util/zip/ZipEntry.md) |

| Known Direct Subclasses [JarEntry](../java/util/jar/JarEntry.md) |-----------------------------------------------------------------------------------------|---------------------------------------------------| | [JarEntry](../java/util/jar/JarEntry.md) | This class is used to represent a JAR file entry. | |
| --- | --- | --- | --- | --- | --- | --- |

This class is used to represent a ZIP file entry.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENATT](../java/util/zip/ZipEntry.md) Central directory (CEN) header internal file attributes field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENATX](../java/util/zip/ZipEntry.md) Central directory (CEN) header external file attributes field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENCOM](../java/util/zip/ZipEntry.md) Central directory (CEN) header comment length field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENCRC](../java/util/zip/ZipEntry.md) Central directory (CEN) header uncompressed file crc-32 value field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENDSK](../java/util/zip/ZipEntry.md) Central directory (CEN) header disk number start field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENEXT](../java/util/zip/ZipEntry.md) Central directory (CEN) header extra field length field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENFLG](../java/util/zip/ZipEntry.md) Central directory (CEN) header encrypt, decrypt flags field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENHDR](../java/util/zip/ZipEntry.md) Central directory (CEN) header size in bytes (including signature). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENHOW](../java/util/zip/ZipEntry.md) Central directory (CEN) header compression method field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENLEN](../java/util/zip/ZipEntry.md) Central directory (CEN) header uncompressed size field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENNAM](../java/util/zip/ZipEntry.md) Central directory (CEN) header filename length field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENOFF](../java/util/zip/ZipEntry.md) Central directory (CEN) header LOC header offset field offset. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [CENSIG](../java/util/zip/ZipEntry.md) Central directory (CEN) header signature. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENSIZ](../java/util/zip/ZipEntry.md) Central directory (CEN) header compressed size field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENTIM](../java/util/zip/ZipEntry.md) Central directory (CEN) header modification time field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENVEM](../java/util/zip/ZipEntry.md) Central directory (CEN) header version made by field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CENVER](../java/util/zip/ZipEntry.md) Central directory (CEN) header version needed to extract field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEFLATED](../java/util/zip/ZipEntry.md) Compression method for compressed (deflated) entries. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDCOM](../java/util/zip/ZipEntry.md) End of central directory (END) header zip file comment length field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDHDR](../java/util/zip/ZipEntry.md) End of central directory (END) header size in bytes (including signature). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDOFF](../java/util/zip/ZipEntry.md) End of central directory (END) header offset for the first CEN header field offset. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ENDSIG](../java/util/zip/ZipEntry.md) End of central directory (END) header signature. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDSIZ](../java/util/zip/ZipEntry.md) End of central directory (END) header central directory size in bytes field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDSUB](../java/util/zip/ZipEntry.md) End of central directory (END) header number of entries on this disk field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENDTOT](../java/util/zip/ZipEntry.md) End of central directory (END) header total number of entries field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXTCRC](../java/util/zip/ZipEntry.md) Extra local (EXT) header uncompressed file crc-32 value field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXTHDR](../java/util/zip/ZipEntry.md) Extra local (EXT) header size in bytes (including signature). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXTLEN](../java/util/zip/ZipEntry.md) Extra local (EXT) header uncompressed size field offset. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [EXTSIG](../java/util/zip/ZipEntry.md) Extra local (EXT) header signature. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXTSIZ](../java/util/zip/ZipEntry.md) Extra local (EXT) header compressed size field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCCRC](../java/util/zip/ZipEntry.md) Local file (LOC) header uncompressed file crc-32 value field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCEXT](../java/util/zip/ZipEntry.md) Local file (LOC) header extra field length field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCFLG](../java/util/zip/ZipEntry.md) Local file (LOC) header general purpose bit flag field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCHDR](../java/util/zip/ZipEntry.md) Local file (LOC) header size in bytes (including signature). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCHOW](../java/util/zip/ZipEntry.md) Local file (LOC) header compression method field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCLEN](../java/util/zip/ZipEntry.md) Local file (LOC) header uncompressed size field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCNAM](../java/util/zip/ZipEntry.md) Local file (LOC) header filename length field offset. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [LOCSIG](../java/util/zip/ZipEntry.md) Local file (LOC) header signature. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCSIZ](../java/util/zip/ZipEntry.md) Local file (LOC) header compressed size field offset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCTIM](../java/util/zip/ZipEntry.md) Local file (LOC) header modification time field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCVER](../java/util/zip/ZipEntry.md) Local file (LOC) header version needed to extract field offset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STORED](../java/util/zip/ZipEntry.md) Compression method for uncompressed entries. |
| --- | --- |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ZipEntry](../java/util/zip/ZipEntry.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new zip entry with the specified name. |
| [ZipEntry](../java/util/zip/ZipEntry.md))`(`e:` ` [ZipEntry](../java/util/zip/ZipEntry.md)!`)` Creates a new zip entry with fields taken from the specified zip entry. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../java/util/zip/ZipEntry.md))`()` Returns a copy of this entry. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getComment](../java/util/zip/ZipEntry.md))`()` Returns the comment string for the entry. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCompressedSize](../java/util/zip/ZipEntry.md))`()` Returns the size of the compressed entry data. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCrc](../java/util/zip/ZipEntry.md))`()` Returns the CRC-32 checksum of the uncompressed entry data. |
| open [FileTime](../java/nio/file/attribute/FileTime.md)! | [getCreationTime](../java/util/zip/ZipEntry.md))`()` Returns the creation time of the entry. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getExtra](../java/util/zip/ZipEntry.md))`()` Returns the extra field data for the entry. |
| --- | --- |
| open [FileTime](../java/nio/file/attribute/FileTime.md)! | [getLastAccessTime](../java/util/zip/ZipEntry.md))`()` Returns the last access time of the entry. |
| open [FileTime](../java/nio/file/attribute/FileTime.md)! | [getLastModifiedTime](../java/util/zip/ZipEntry.md))`()` Returns the last modification time of the entry. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMethod](../java/util/zip/ZipEntry.md))`()` Returns the compression method of the entry. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../java/util/zip/ZipEntry.md))`()` Returns the name of the entry. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getSize](../java/util/zip/ZipEntry.md))`()` Returns the uncompressed size of the entry data. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTime](../java/util/zip/ZipEntry.md))`()` Returns the last modification time of the entry. |
| --- | --- |
| open [LocalDateTime](../java/time/LocalDateTime.md)! | [getTimeLocal](../java/util/zip/ZipEntry.md))`()` Returns the last modification time of the entry in local date-time. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/util/zip/ZipEntry.md))`()` Returns the hash code value for this entry. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDirectory](../java/util/zip/ZipEntry.md))`()` Returns true if this is a directory entry. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setComment](../java/util/zip/ZipEntry.md))`(`comment:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the optional comment string for the entry. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCompressedSize](../java/util/zip/ZipEntry.md))`(`csize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the size of the compressed entry data. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCrc](../java/util/zip/ZipEntry.md))`(`crc:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the CRC-32 checksum of the uncompressed entry data. |
| --- | --- |
| open [ZipEntry](../java/util/zip/ZipEntry.md)! | [setCreationTime](../java/util/zip/ZipEntry.md))`(`time:` ` [FileTime](../java/nio/file/attribute/FileTime.md)!`)` Sets the creation time of the entry. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExtra](../java/util/zip/ZipEntry.md))`(`extra:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Sets the optional extra field data for the entry. |
| open [ZipEntry](../java/util/zip/ZipEntry.md)! | [setLastAccessTime](../java/util/zip/ZipEntry.md))`(`time:` ` [FileTime](../java/nio/file/attribute/FileTime.md)!`)` Sets the last access time of the entry. |
| --- | --- |
| open [ZipEntry](../java/util/zip/ZipEntry.md)! | [setLastModifiedTime](../java/util/zip/ZipEntry.md))`(`time:` ` [FileTime](../java/nio/file/attribute/FileTime.md)!`)` Sets the last modification time of the entry. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMethod](../java/util/zip/ZipEntry.md))`(`method:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the compression method for the entry. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSize](../java/util/zip/ZipEntry.md))`(`size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the uncompressed size of the entry data. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTime](../java/util/zip/ZipEntry.md))`(`time:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the last modification time of the entry. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimeLocal](../java/util/zip/ZipEntry.md))`(`time:` ` [LocalDateTime](../java/time/LocalDateTime.md)!`)` Sets the last modification time of the entry in local date-time. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/util/zip/ZipEntry.md))`()` Returns a string representation of the ZIP entry. |
| --- | --- |

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

Compression method for compressed (deflated) entries. 

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

Compression method for uncompressed entries. 

 Value: 0

## Public constructors

### ZipEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ZipEntry(name: String!)
```

Creates a new zip entry with the specified name.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entry name |

| Exceptions ||
|--------------------------------------|-----------------------------------------------|
| `java.lang.NullPointerException` | if the entry name is null |
| `java.lang.IllegalArgumentException` | if the entry name is longer than 0xFFFF bytes |

### ZipEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ZipEntry(e: ZipEntry!)
```

Creates a new zip entry with fields taken from the specified zip entry.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------|
| `e` | [ZipEntry](../java/util/zip/ZipEntry.md)!:A zip Entry object |

| Exceptions ||
|----------------------------------|-----------------------------|
| `java.lang.NullPointerException` | if the entry object is null |

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Returns a copy of this entry.

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### getComment

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getComment(): String!
```

Returns the comment string for the entry.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the comment string for the entry, or null if none |

**See Also**

- [#setComment(String)](../java/util/zip/ZipEntry.md)) 

### getCompressedSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCompressedSize(): Long
```

Returns the size of the compressed entry data.

In the case of a stored entry, the compressed size will be the same as the uncompressed size of the entry.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the size of the compressed entry data, or -1 if not known |

**See Also**

- [#setCompressedSize(long)](../java/util/zip/ZipEntry.md)) 

### getCrc

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCrc(): Long
```

Returns the CRC-32 checksum of the uncompressed entry data.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the CRC-32 checksum of the uncompressed entry data, or -1 if not known |

**See Also**

- [#setCrc(long)](../java/util/zip/ZipEntry.md)) 

### getCreationTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCreationTime(): FileTime!
```

Returns the creation time of the entry.

The creation time is from the extended timestamp fields of entry's`optional extra data`when read from a ZIP file or ZIP file formatted stream.

| Return ||
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [FileTime](../java/nio/file/attribute/FileTime.md)! | the creation time of the entry, null if not specified |

**See Also**

- [#setCreationTime(FileTime)](../java/util/zip/ZipEntry.md)) 

### getExtra

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExtra(): ByteArray!
```

Returns the extra field data for the entry.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the extra field data for the entry, or null if none |

**See Also**

- [#setExtra(byte[])](https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry#setExtra(kotlin.ByteArray)) 

### getLastAccessTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLastAccessTime(): FileTime!
```

Returns the last access time of the entry.

The last access time is from the extended timestamp fields of entry's`optional extra data`when read from a ZIP file or ZIP file formatted stream.

| Return ||
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [FileTime](../java/nio/file/attribute/FileTime.md)! | The last access time of the entry, null if not specified |

**See Also**

- [#setLastAccessTime(FileTime)](../java/util/zip/ZipEntry.md)) 

### getLastModifiedTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLastModifiedTime(): FileTime!
```

Returns the last modification time of the entry.

If the entry is read from a ZIP file or ZIP file formatted input stream, this is the last modification time from the zip file entry's`optional extra data`if the extended timestamp fields are present. Otherwise the last modification time is read from the entry's`date and time fields`, the [default TimeZone](../java/util/TimeZone.md))is used to convert the standard MS-DOS formatted date and time to the epoch time.

| Return ||
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [FileTime](../java/nio/file/attribute/FileTime.md)! | The last modification time of the entry, null if not specified |

**See Also**

- [#setLastModifiedTime(FileTime)](../java/util/zip/ZipEntry.md)) 

### getMethod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMethod(): Int
```

Returns the compression method of the entry.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the compression method of the entry, or -1 if not specified |

**See Also**

- [#setMethod(int)](../java/util/zip/ZipEntry.md)) 

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getName(): String!
```

Returns the name of the entry.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the entry |

### getSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSize(): Long
```

Returns the uncompressed size of the entry data.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the uncompressed size of the entry data, or -1 if not known |

**See Also**

- [#setSize(long)](../java/util/zip/ZipEntry.md)) 

### getTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTime(): Long
```

Returns the last modification time of the entry.

If the entry is read from a ZIP file or ZIP file formatted input stream, this is the last modification time from the`date and time fields`of the zip file entry. The [default TimeZone](../java/util/TimeZone.md))is used to convert the standard MS-DOS formatted date and time to the epoch time.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The last modification time of the entry in milliseconds since the epoch, or -1 if not specified |

**See Also**

- [#setTime(long)](../java/util/zip/ZipEntry.md))
- [#setLastModifiedTime(FileTime)](../java/util/zip/ZipEntry.md)) 

### getTimeLocal

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimeLocal(): LocalDateTime!
```

Returns the last modification time of the entry in local date-time.

If the entry is read from a ZIP file or ZIP file formatted input stream, this is the last modification time from the zip file entry's`optional extra data`if the extended timestamp fields are present. Otherwise, the last modification time is read from entry's standard MS-DOS formatted`date and time fields`.

The [system default TimeZone](../java/time/ZoneId.md))is used to convert the UTC time to local date-time.

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [LocalDateTime](../java/time/LocalDateTime.md)! | The last modification time of the entry in local date-time |

**See Also**

- [#setTimeLocal(LocalDateTime)](../java/util/zip/ZipEntry.md)) 

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns the hash code value for this entry.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isDirectory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isDirectory(): Boolean
```

Returns true if this is a directory entry. A directory entry is defined to be one whose name ends with a '/'.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this is a directory entry |

### setComment

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setComment(comment: String!): Unit
```

Sets the optional comment string for the entry.

ZIP entry comments have maximum length of 0xffff. If the length of the specified comment string is greater than 0xFFFF bytes after encoding, only the first 0xFFFF bytes are output to the ZIP file entry.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------|
| `comment` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the comment string |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry#getComment()> 

### setCompressedSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCompressedSize(csize: Long): Unit
```

Sets the size of the compressed entry data.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------|
| `csize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the compressed size to set |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry#getCompressedSize()> 

### setCrc

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCrc(crc: Long): Unit
```

Sets the CRC-32 checksum of the uncompressed entry data.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------|
| `crc` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the CRC-32 value |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the specified CRC-32 value is less than 0 or greater than 0xFFFFFFFF |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry#getCrc()> 

### setCreationTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCreationTime(time: FileTime!): ZipEntry!
```

Sets the creation time of the entry.

If set, the creation time will be stored into the extended timestamp fields of entry's`optional extra data`, when output to a ZIP file or ZIP file formatted stream.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------|
| `time` | [FileTime](../java/nio/file/attribute/FileTime.md)!:The creation time of the entry |

| Return ||
|-------------------------------------------------------------------------------------|----------------|
| [ZipEntry](../java/util/zip/ZipEntry.md)! | This zip entry |

| Exceptions ||
|----------------------------------|---------------------|
| `java.lang.NullPointerException` | if the`time`is null |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry#getCreationTime()> 

### setExtra

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setExtra(extra: ByteArray!): Unit
```

Sets the optional extra field data for the entry.

Invoking this method may change this entry's last modification time, last access time and creation time, if the`extra`field data includes the extensible timestamp fields, such as`NTFS tag 0x0001`or`Info-ZIP Extended Timestamp`, as specified in [Info-ZIP Application Note 970311](http://www.info-zip.org/doc/appnote-19970311-iz.zip).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `extra` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:The extra field data bytes |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the length of the specified extra field data is greater than 0xFFFF bytes |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry#getExtra()> 

### setLastAccessTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLastAccessTime(time: FileTime!): ZipEntry!
```

Sets the last access time of the entry.

If set, the last access time will be stored into the extended timestamp fields of entry's`optional extra data`, when output to a ZIP file or ZIP file formatted stream.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------|
| `time` | [FileTime](../java/nio/file/attribute/FileTime.md)!:The last access time of the entry |

| Return ||
|-------------------------------------------------------------------------------------|----------------|
| [ZipEntry](../java/util/zip/ZipEntry.md)! | This zip entry |

| Exceptions ||
|----------------------------------|---------------------|
| `java.lang.NullPointerException` | if the`time`is null |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry#getLastAccessTime()> 

### setLastModifiedTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLastModifiedTime(time: FileTime!): ZipEntry!
```

Sets the last modification time of the entry.

When output to a ZIP file or ZIP file formatted output stream the last modification time set by this method will be stored into zip file entry's`date and time fields`in`standard MS-DOS date and time format`), and the extended timestamp fields in`optional extra data`in UTC time.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `time` | [FileTime](../java/nio/file/attribute/FileTime.md)!:The last modification time of the entry |

| Return ||
|-------------------------------------------------------------------------------------|----------------|
| [ZipEntry](../java/util/zip/ZipEntry.md)! | This zip entry |

| Exceptions ||
|----------------------------------|---------------------|
| `java.lang.NullPointerException` | if the`time`is null |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry#getLastModifiedTime()> 

### setMethod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMethod(method: Int): Unit
```

Sets the compression method for the entry.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------|
| `method` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the compression method, either STORED or DEFLATED |

| Exceptions ||
|--------------------------------------|------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the specified compression method is invalid |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry#getMethod()> 

### setSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSize(size: Long): Unit
```

Sets the uncompressed size of the entry data.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------|
| `size` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the uncompressed size in bytes |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the specified size is less than 0, is greater than 0xFFFFFFFF when [ZIP64 format](../java/util/zip/_package.md) is not supported, or is less than 0 when ZIP64 is supported |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry#getSize()> 

### setTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTime(time: Long): Unit
```

Sets the last modification time of the entry.

If the entry is output to a ZIP file or ZIP file formatted output stream the last modification time set by this method will be stored into the`date and time fields`of the zip file entry and encoded in standard`MS-DOS date and time format`. The [default TimeZone](../java/util/TimeZone.md))is used to convert the epoch time to the MS-DOS data and time.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `time` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The last modification time of the entry in milliseconds since the epoch |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry#getTime()>
- <https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry#getLastModifiedTime()> 

### setTimeLocal

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTimeLocal(time: LocalDateTime!): Unit
```

Sets the last modification time of the entry in local date-time.

If the entry is output to a ZIP file or ZIP file formatted output stream the last modification time set by this method will be stored into the`date and time fields`of the zip file entry and encoded in standard`MS-DOS date and time format`. If the date-time set is out of the range of the standard`MS-DOS date and time format`, the time will also be stored into zip file entry's extended timestamp fields in`optional extra data`in UTC time. The [system default TimeZone](../java/time/ZoneId.md))is used to convert the local date-time to UTC time.

`LocalDateTime`uses a precision of nanoseconds, whereas this class uses a precision of milliseconds. The conversion will truncate any excess precision information as though the amount in nanoseconds was subject to integer division by one million.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `time` | [LocalDateTime](../java/time/LocalDateTime.md)!:The last modification time of the entry in local date-time |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry#getTimeLocal()> 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of the ZIP entry.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
