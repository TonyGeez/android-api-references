Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JarFile

```
open class JarFile : ZipFile
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.zip.ZipFile](../java.util.zip/ZipFile.md) ||
| | ↳ | [java.util.jar.JarFile](JarFile.md) |

The `JarFile` class is used to read the contents of a jar file from any file that can be opened with `java.io.RandomAccessFile`. It extends the class `java.util.zip.ZipFile` with support for reading an optional `Manifest` entry. The `Manifest` can be used to specify meta-information about the jar file and its entries.

Unless otherwise noted, passing a null argument to a constructor or method in this class will cause a `https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#` to be thrown. If the verify flag is on when opening a signed jar file, the content of the file is verified against its signature embedded inside the file. Please note that the verification process does not include validating the signer's certificate. A caller should inspect the return value of getCodeSigners to further determine if the signature can be trusted.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/jar/JarFile#MANIFEST_NAME:kotlin.String` The JAR manifest file name. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#CENATT:kotlin.Int` Central directory (CEN) header internal file attributes field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#CENATX:kotlin.Int` Central directory (CEN) header external file attributes field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#CENCOM:kotlin.Int` Central directory (CEN) header comment length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#CENCRC:kotlin.Int` Central directory (CEN) header uncompressed file crc-32 value field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#CENDSK:kotlin.Int` Central directory (CEN) header disk number start field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#CENEXT:kotlin.Int` Central directory (CEN) header extra field length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#CENFLG:kotlin.Int` Central directory (CEN) header encrypt, decrypt flags field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#CENHDR:kotlin.Int` Central directory (CEN) header size in bytes (including signature). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#CENHOW:kotlin.Int` Central directory (CEN) header compression method field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#CENLEN:kotlin.Int` Central directory (CEN) header uncompressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#CENNAM:kotlin.Int` Central directory (CEN) header filename length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#CENOFF:kotlin.Int` Central directory (CEN) header LOC header offset field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#CENSIG:kotlin.Long` Central directory (CEN) header signature. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#CENSIZ:kotlin.Int` Central directory (CEN) header compressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#CENTIM:kotlin.Int` Central directory (CEN) header modification time field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#CENVEM:kotlin.Int` Central directory (CEN) header version made by field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#CENVER:kotlin.Int` Central directory (CEN) header version needed to extract field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#ENDCOM:kotlin.Int` End of central directory (END) header zip file comment length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#ENDHDR:kotlin.Int` End of central directory (END) header size in bytes (including signature). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#ENDOFF:kotlin.Int` End of central directory (END) header offset for the first CEN header field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#ENDSIG:kotlin.Long` End of central directory (END) header signature. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#ENDSIZ:kotlin.Int` End of central directory (END) header central directory size in bytes field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#ENDSUB:kotlin.Int` End of central directory (END) header number of entries on this disk field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#ENDTOT:kotlin.Int` End of central directory (END) header total number of entries field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#EXTCRC:kotlin.Int` Extra local (EXT) header uncompressed file crc-32 value field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#EXTHDR:kotlin.Int` Extra local (EXT) header size in bytes (including signature). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#EXTLEN:kotlin.Int` Extra local (EXT) header uncompressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#EXTSIG:kotlin.Long` Extra local (EXT) header signature. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#EXTSIZ:kotlin.Int` Extra local (EXT) header compressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#LOCCRC:kotlin.Int` Local file (LOC) header uncompressed file crc-32 value field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#LOCEXT:kotlin.Int` Local file (LOC) header extra field length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#LOCFLG:kotlin.Int` Local file (LOC) header general purpose bit flag field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#LOCHDR:kotlin.Int` Local file (LOC) header size in bytes (including signature). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#LOCHOW:kotlin.Int` Local file (LOC) header compression method field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#LOCLEN:kotlin.Int` Local file (LOC) header uncompressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#LOCNAM:kotlin.Int` Local file (LOC) header filename length field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#LOCSIG:kotlin.Long` Local file (LOC) header signature. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#LOCSIZ:kotlin.Int` Local file (LOC) header compressed size field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#LOCTIM:kotlin.Int` Local file (LOC) header modification time field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#LOCVER:kotlin.Int` Local file (LOC) header version needed to extract field offset. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#OPEN_DELETE:kotlin.Int` Mode flag to open a zip file and mark it for deletion. The file will be deleted some time between the moment that it is opened and the moment that it is closed, but its contents will remain accessible via the `ZipFile` object until either the close method is invoked or the virtual machine exits. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#OPEN_READ:kotlin.Int` Mode flag to open a zip file for reading. <br /> | ||

| Public constructors ||
|---|---|
| JarFile Creates a new `JarFile` to read from the specified `File` object. |
| JarFile Creates a new `JarFile` to read from the specified `File` object. |
| JarFile Creates a new `JarFile` to read from the specified `File` object in the specified mode. |
| JarFile Creates a new `JarFile` to read from the specified file `name`. |
| JarFile Creates a new `JarFile` to read from the specified file `name`. |

| Public methods ||
|---|---|
| open [Enumeration](../java.util/Enumeration.md)\< [JarEntry](JarEntry.md)!\>! | entries Returns an enumeration of the zip file entries. |
| open [ZipEntry](../java.util.zip/ZipEntry.md)! | getEntry Returns the `ZipEntry` for the given entry name or `null` if not found. |
| open [InputStream](../java.io/InputStream.md)! | getInputStream Returns an input stream for reading the contents of the specified zip file entry. |
| --- | --- |
| open [JarEntry](JarEntry.md)! | getJarEntry Returns the `JarEntry` for the given entry name or `null` if not found. |
| open [Manifest](Manifest.md)! | getManifest Returns the jar file manifest, or `null` if none. |
| open [Stream](../java.util.stream/Stream.md)\< [JarEntry](JarEntry.md)!\>! | stream Returns an ordered `Stream` over the ZIP file entries. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/zip/ZipFile.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | close Closes the ZIP file. Closing this ZIP file will close all of the input streams previously returned by invocations of the getInputStream method. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getComment Returns the zip file comment, or null if none. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getName Returns the path name of the ZIP file. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | size Returns the number of entries in the ZIP file. <br /> | ||

## Constants

### MANIFEST_NAME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MANIFEST_NAME: String
```

The JAR manifest file name.

 Value: "META-INF/MANIFEST.MF"

## Public constructors

### JarFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
JarFile(file: File!)
```

Creates a new `JarFile` to read from the specified `File` object. The `JarFile` will be verified if it is signed.

| Parameters ||
|---|---|
| `file` | [File](../java.io/File.md)!: the jar file to be opened for reading |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error has occurred |
| `java.lang.SecurityException` | if access to the file is denied by the SecurityManager |

### JarFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
JarFile(
    file: File!, 
    verify: Boolean)
```

Creates a new `JarFile` to read from the specified `File` object.

| Parameters ||
|---|---|
| `file` | [File](../java.io/File.md)!: the jar file to be opened for reading |
| `verify` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether or not to verify the jar file if it is signed. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error has occurred |
| `java.lang.SecurityException` | if access to the file is denied by the SecurityManager. |

### JarFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
JarFile(
    file: File!, 
    verify: Boolean, 
    mode: Int)
```

Creates a new `JarFile` to read from the specified `File` object in the specified mode. The mode argument must be either OPEN_READ or OPEN_READ | OPEN_DELETE.
| --- | --- |

| Parameters ||
|---|---|
| `file` | [File](../java.io/File.md)!: the jar file to be opened for reading |
| `verify` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether or not to verify the jar file if it is signed. |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the mode in which the file is to be opened |
| --- | --- |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error has occurred |
| `java.lang.IllegalArgumentException` | if the mode argument is invalid |
| `java.lang.SecurityException` | if access to the file is denied by the SecurityManager |
| --- | --- |

### JarFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
JarFile(name: String!)
```

Creates a new `JarFile` to read from the specified file `name`. The `JarFile` will be verified if it is signed.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the jar file to be opened for reading |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error has occurred |
| `java.lang.SecurityException` | if access to the file is denied by the SecurityManager |

### JarFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
JarFile(
    name: String!, 
    verify: Boolean)
```

Creates a new `JarFile` to read from the specified file `name`.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the jar file to be opened for reading |
| `verify` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether or not to verify the jar file if it is signed. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error has occurred |
| `java.lang.SecurityException` | if access to the file is denied by the SecurityManager |

## Public methods

### entries

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun entries(): Enumeration<JarEntry!>!
```

Returns an enumeration of the zip file entries.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Enumeration.html#<https://developer.android.com/reference/kotlin/java/util/jar/JarEntry!>!` | an enumeration of the ZIP file entries |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the zip file has been closed |

### getEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEntry(name: String!): ZipEntry!
```

Returns the `ZipEntry` for the given entry name or `null` if not found.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the jar file entry name |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#!` | the `ZipEntry` for the given entry name or `null` if not found |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | may be thrown if the jar file has been closed |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/zip/ZipEntry.html#`

### getInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInputStream(ze: ZipEntry!): InputStream!
```

Returns an input stream for reading the contents of the specified zip file entry.

| Parameters ||
|---|---|
| `entry` | the zip file entry |
| `ze` | [ZipEntry](../java.util.zip/ZipEntry.md)!: the zip file entry |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/InputStream.html#!` | an input stream for reading the contents of the specified zip file entry |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error has occurred |
| `java.lang.IllegalStateException` | may be thrown if the jar file has been closed |
| `java.util.zip.ZipException` | if a zip file format error has occurred |
| --- | --- |
| `java.lang.SecurityException` | if any of the jar file entries are incorrectly signed. |

### getJarEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getJarEntry(name: String!): JarEntry!
```

Returns the `JarEntry` for the given entry name or `null` if not found.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the jar file entry name |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/jar/JarEntry!` | the `JarEntry` for the given entry name or `null` if not found. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | may be thrown if the jar file has been closed |

**See Also**

- JarEntry

### getManifest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getManifest(): Manifest!
```

Returns the jar file manifest, or `null` if none.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/jar/Manifest!` | the jar file manifest, or `null` if none |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error has occurred |
| `java.lang.IllegalStateException` | may be thrown if the jar file has been closed |

### stream

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun stream(): Stream<JarEntry!>!
```

Returns an ordered `Stream` over the ZIP file entries. Entries appear in the `Stream` in the order they appear in the central directory of the ZIP file.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#<https://developer.android.com/reference/kotlin/java/util/jar/JarEntry!>!` | an ordered `Stream` of entries in this ZIP file |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the zip file has been closed |
