Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JarEntry

```
open class JarEntry : ZipEntry
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.zip.ZipEntry](../java/util/zip/ZipEntry.md) ||
| | ↳ | [java.util.jar.JarEntry](../java/util/jar/JarEntry.md) |

This class is used to represent a JAR file entry.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#CENATT:kotlin.Int` Central directory (CEN) header internal file attributes field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#CENATX:kotlin.Int` Central directory (CEN) header external file attributes field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#CENCOM:kotlin.Int` Central directory (CEN) header comment length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#CENCRC:kotlin.Int` Central directory (CEN) header uncompressed file crc-32 value field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#CENDSK:kotlin.Int` Central directory (CEN) header disk number start field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#CENEXT:kotlin.Int` Central directory (CEN) header extra field length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#CENFLG:kotlin.Int` Central directory (CEN) header encrypt, decrypt flags field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#CENHDR:kotlin.Int` Central directory (CEN) header size in bytes (including signature). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#CENHOW:kotlin.Int` Central directory (CEN) header compression method field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#CENLEN:kotlin.Int` Central directory (CEN) header uncompressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#CENNAM:kotlin.Int` Central directory (CEN) header filename length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#CENOFF:kotlin.Int` Central directory (CEN) header LOC header offset field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#CENSIG:kotlin.Long` Central directory (CEN) header signature. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#CENSIZ:kotlin.Int` Central directory (CEN) header compressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#CENTIM:kotlin.Int` Central directory (CEN) header modification time field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#CENVEM:kotlin.Int` Central directory (CEN) header version made by field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#CENVER:kotlin.Int` Central directory (CEN) header version needed to extract field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#DEFLATED:kotlin.Int` Compression method for compressed (deflated) entries. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#ENDCOM:kotlin.Int` End of central directory (END) header zip file comment length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#ENDHDR:kotlin.Int` End of central directory (END) header size in bytes (including signature). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#ENDOFF:kotlin.Int` End of central directory (END) header offset for the first CEN header field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#ENDSIG:kotlin.Long` End of central directory (END) header signature. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#ENDSIZ:kotlin.Int` End of central directory (END) header central directory size in bytes field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#ENDSUB:kotlin.Int` End of central directory (END) header number of entries on this disk field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#ENDTOT:kotlin.Int` End of central directory (END) header total number of entries field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#EXTCRC:kotlin.Int` Extra local (EXT) header uncompressed file crc-32 value field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#EXTHDR:kotlin.Int` Extra local (EXT) header size in bytes (including signature). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#EXTLEN:kotlin.Int` Extra local (EXT) header uncompressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#EXTSIG:kotlin.Long` Extra local (EXT) header signature. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#EXTSIZ:kotlin.Int` Extra local (EXT) header compressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#LOCCRC:kotlin.Int` Local file (LOC) header uncompressed file crc-32 value field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#LOCEXT:kotlin.Int` Local file (LOC) header extra field length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#LOCFLG:kotlin.Int` Local file (LOC) header general purpose bit flag field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#LOCHDR:kotlin.Int` Local file (LOC) header size in bytes (including signature). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#LOCHOW:kotlin.Int` Local file (LOC) header compression method field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#LOCLEN:kotlin.Int` Local file (LOC) header uncompressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#LOCNAM:kotlin.Int` Local file (LOC) header filename length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#LOCSIG:kotlin.Long` Local file (LOC) header signature. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#LOCSIZ:kotlin.Int` Local file (LOC) header compressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#LOCTIM:kotlin.Int` Local file (LOC) header modification time field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#LOCVER:kotlin.Int` Local file (LOC) header version needed to extract field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#STORED:kotlin.Int` Compression method for uncompressed entries. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/jar/JarEntry#JarEntry(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Creates a new `JarEntry` for the specified JAR file entry name. |
| `https://developer.android.com/reference/kotlin/java/util/jar/JarEntry#JarEntry(java.util.jar.JarEntry)(je: https://developer.android.com/reference/kotlin/java/util/jar/JarEntry#!)` Creates a new `JarEntry` with fields taken from the specified `JarEntry` object. |
| `https://developer.android.com/reference/kotlin/java/util/jar/JarEntry#JarEntry(java.util.zip.ZipEntry)(ze: https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#!)` Creates a new `JarEntry` with fields taken from the specified `ZipEntry` object. |

| Public methods ||
|---|---|
| open [Attributes](../java/util/jar/Attributes.md)! | `https://developer.android.com/reference/kotlin/java/util/jar/JarEntry#getAttributes()()` Returns the `Manifest` `Attributes` for this entry, or `null` if none. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Certificate](../java/security/cert/Certificate.md)!\>! | `https://developer.android.com/reference/kotlin/java/util/jar/JarEntry#getCertificates()()` Returns the `Certificate` objects for this entry, or `null` if none. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CodeSigner](../java/security/CodeSigner.md)!\>! | `https://developer.android.com/reference/kotlin/java/util/jar/JarEntry#getCodeSigners()()` Returns the `CodeSigner` objects for this entry, or `null` if none. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/util/jar/JarEntry#getRealName()()` This method returns the same name that `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#getName()` returns. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#clone()()` Returns a copy of this entry. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#getComment()()` Returns the comment string for the entry. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#getCompressedSize()()` Returns the size of the compressed entry data. In the case of a stored entry, the compressed size will be the same as the uncompressed size of the entry. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#getCrc()()` Returns the CRC-32 checksum of the uncompressed entry data. <br /> | | `https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime.html#!` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#getCreationTime()()` Returns the creation time of the entry. The creation time is from the extended timestamp fields of entry's `optional extra data` when read from a ZIP file or ZIP file formatted stream. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#getExtra()()` Returns the extra field data for the entry. <br /> | | `https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime.html#!` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#getLastAccessTime()()` Returns the last access time of the entry. The last access time is from the extended timestamp fields of entry's `optional extra data` when read from a ZIP file or ZIP file formatted stream. <br /> | | `https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime.html#!` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#getLastModifiedTime()()` Returns the last modification time of the entry. If the entry is read from a ZIP file or ZIP file formatted input stream, this is the last modification time from the zip file entry's `optional extra data` if the extended timestamp fields are present. Otherwise the last modification time is read from the entry's `date and time fields`, the `https://developer.android.com/reference/kotlin/java/util/TimeZone.html#getDefault()` is used to convert the standard MS-DOS formatted date and time to the epoch time. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#getMethod()()` Returns the compression method of the entry. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#getName()()` Returns the name of the entry. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#getSize()()` Returns the uncompressed size of the entry data. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#getTime()()` Returns the last modification time of the entry. If the entry is read from a ZIP file or ZIP file formatted input stream, this is the last modification time from the `date and time fields` of the zip file entry. The `https://developer.android.com/reference/kotlin/java/util/TimeZone.html#getDefault()` is used to convert the standard MS-DOS formatted date and time to the epoch time. <br /> | | `https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#!` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#getTimeLocal()()` Returns the last modification time of the entry in local date-time. If the entry is read from a ZIP file or ZIP file formatted input stream, this is the last modification time from the zip file entry's `optional extra data` if the extended timestamp fields are present. Otherwise, the last modification time is read from entry's standard MS-DOS formatted `date and time fields`. The `https://developer.android.com/reference/kotlin/java/time/ZoneId.html#systemDefault()` is used to convert the UTC time to local date-time. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#hashCode()()` Returns the hash code value for this entry. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#isDirectory()()` Returns true if this is a directory entry. A directory entry is defined to be one whose name ends with a '/'. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#setComment(kotlin.String)(comment: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Sets the optional comment string for the entry. ZIP entry comments have maximum length of 0xffff. If the length of the specified comment string is greater than 0xFFFF bytes after encoding, only the first 0xFFFF bytes are output to the ZIP file entry. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#setCompressedSize(kotlin.Long)(csize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the size of the compressed entry data. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#setCrc(kotlin.Long)(crc: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the CRC-32 checksum of the uncompressed entry data. <br /> | | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#!` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#setCreationTime(java.nio.file.attribute.FileTime)(time: https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime.html#!)` Sets the creation time of the entry. If set, the creation time will be stored into the extended timestamp fields of entry's `optional extra data`, when output to a ZIP file or ZIP file formatted stream. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#setExtra(kotlin.ByteArray)(extra: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Sets the optional extra field data for the entry. Invoking this method may change this entry's last modification time, last access time and creation time, if the `extra` field data includes the extensible timestamp fields, such as `NTFS tag 0x0001` or `Info-ZIP Extended Timestamp`, as specified in [Info-ZIP Application Note 970311](http://www.info-zip.org/doc/appnote-19970311-iz.zip). <br /> | | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#!` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#setLastAccessTime(java.nio.file.attribute.FileTime)(time: https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime.html#!)` Sets the last access time of the entry. If set, the last access time will be stored into the extended timestamp fields of entry's `optional extra data`, when output to a ZIP file or ZIP file formatted stream. <br /> | | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#!` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#setLastModifiedTime(java.nio.file.attribute.FileTime)(time: https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime.html#!)` Sets the last modification time of the entry. When output to a ZIP file or ZIP file formatted output stream the last modification time set by this method will be stored into zip file entry's `date and time fields` in `standard MS-DOS date and time format`), and the extended timestamp fields in `optional extra data` in UTC time. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#setMethod(kotlin.Int)(method: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the compression method for the entry. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#setSize(kotlin.Long)(size: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the uncompressed size of the entry data. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#setTime(kotlin.Long)(time: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the last modification time of the entry. If the entry is output to a ZIP file or ZIP file formatted output stream the last modification time set by this method will be stored into the `date and time fields` of the zip file entry and encoded in standard `MS-DOS date and time format`. The `https://developer.android.com/reference/kotlin/java/util/TimeZone.html#getDefault()` is used to convert the epoch time to the MS-DOS data and time. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#setTimeLocal(java.time.LocalDateTime)(time: https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#!)` Sets the last modification time of the entry in local date-time. If the entry is output to a ZIP file or ZIP file formatted output stream the last modification time set by this method will be stored into the `date and time fields` of the zip file entry and encoded in standard `MS-DOS date and time format`. If the date-time set is out of the range of the standard `MS-DOS date and time format`, the time will also be stored into zip file entry's extended timestamp fields in `optional extra data` in UTC time. The `https://developer.android.com/reference/kotlin/java/time/ZoneId.html#systemDefault()` is used to convert the local date-time to UTC time. `LocalDateTime` uses a precision of nanoseconds, whereas this class uses a precision of milliseconds. The conversion will truncate any excess precision information as though the amount in nanoseconds was subject to integer division by one million. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#toString()()` Returns a string representation of the ZIP entry. <br /> | ||

## Public constructors

### JarEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
JarEntry(name: String!)
```

Creates a new `JarEntry` for the specified JAR file entry name.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the JAR file entry name |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the entry name is longer than 0xFFFF bytes. |
| `java.lang.NullPointerException` | if the entry name is `null` |

### JarEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
JarEntry(je: JarEntry!)
```

Creates a new `JarEntry` with fields taken from the specified `JarEntry` object.

| Parameters ||
|---|---|
| `je` | [JarEntry](../java/util/jar/JarEntry.md)!: the `JarEntry` to copy |

### JarEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
JarEntry(ze: ZipEntry!)
```

Creates a new `JarEntry` with fields taken from the specified `ZipEntry` object.

| Parameters ||
|---|---|
| `ze` | [ZipEntry](../java/util/zip/ZipEntry.md)!: the `ZipEntry` object to create the `JarEntry` from |

## Public methods

### getAttributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAttributes(): Attributes!
```

Returns the `Manifest` `Attributes` for this entry, or `null` if none.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/jar/Attributes!` | the `Manifest` `Attributes` for this entry, or `null` if none |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error has occurred |

### getCertificates

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCertificates(): Array<Certificate!>!
```

Returns the `Certificate` objects for this entry, or `null` if none. This method can only be called once the `JarEntry` has been completely verified by reading from the entry input stream until the end of the stream has been reached. Otherwise, this method will return `null`.

The returned certificate array comprises all the signer certificates that were used to verify this entry. Each signer certificate is followed by its supporting certificate chain (which may be empty). Each signer certificate and its supporting certificate chain are ordered bottom-to-top (i.e., with the signer certificate first and the (root) certificate authority last).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/security/cert/Certificate.html#!>!` | the `Certificate` objects for this entry, or `null` if none. |

### getCodeSigners

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCodeSigners(): Array<CodeSigner!>!
```

Returns the `CodeSigner` objects for this entry, or `null` if none. This method can only be called once the `JarEntry` has been completely verified by reading from the entry input stream until the end of the stream has been reached. Otherwise, this method will return `null`.

The returned array comprises all the code signers that have signed this entry.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/security/CodeSigner.html#!>!` | the `CodeSigner` objects for this entry, or `null` if none. |

### getRealName

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRealName(): String!
```

This method returns the same name that `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#getName()` returns.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the real name of the JarEntry |
