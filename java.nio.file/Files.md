# Files

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Files

```
class Files
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.file.Files](../java/nio/file/Files.md) |

This class consists exclusively of static methods that operate on files, directories, or other types of files.

In most cases, the methods defined here will delegate to the associated file system provider to perform the file operations.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [copy](../java/nio/file/Files.md))`(`in:` ` [InputStream](../java/io/InputStream.md)!`, `target:` ` [Path](../java/nio/file/Path.md)!`, `vararg` `options:` ` [CopyOption](../java/nio/file/CopyOption.md)!`)` Copies all bytes from an input stream to a file. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [copy](../java/nio/file/Files.md))`(`source:` ` [Path](../java/nio/file/Path.md)!`, `out:` ` [OutputStream](../java/io/OutputStream.md)!`)` Copies all bytes from a file to an output stream. |
| static [Path](../java/nio/file/Path.md)! | [copy](../java/nio/file/Files.md))`(`source:` ` [Path](../java/nio/file/Path.md)!`, `target:` ` [Path](../java/nio/file/Path.md)!`, `vararg` `options:` ` [CopyOption](../java/nio/file/CopyOption.md)!`)` Copy a file to a target file. |
| --- | --- |
| static [Path](../java/nio/file/Path.md)! | [createDirectories](../java/nio/file/Files.md))`(`dir:` ` [Path](../java/nio/file/Path.md)!`, `vararg` `attrs:` ` [FileAttribute](../java/nio/file/attribute/FileAttribute.md)<*>!`)` Creates a directory by creating all nonexistent parent directories first. |
| static [Path](../java/nio/file/Path.md)! | [createDirectory](../java/nio/file/Files.md))`(`dir:` ` [Path](../java/nio/file/Path.md)!`, `vararg` `attrs:` ` [FileAttribute](../java/nio/file/attribute/FileAttribute.md)<*>!`)` Creates a new directory. |
| static [Path](../java/nio/file/Path.md)! | [createFile](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `vararg` `attrs:` ` [FileAttribute](../java/nio/file/attribute/FileAttribute.md)<*>!`)` Creates a new and empty file, failing if the file already exists. |
| --- | --- |
| static [Path](../java/nio/file/Path.md)! | [createLink](../java/nio/file/Files.md))`(`link:` ` [Path](../java/nio/file/Path.md)!`, `existing:` ` [Path](../java/nio/file/Path.md)!`)` Creates a new link (directory entry) for an existing file*(optional operation)*. |
| static [Path](../java/nio/file/Path.md)! | [createSymbolicLink](../java/nio/file/Files.md))`(`link:` ` [Path](../java/nio/file/Path.md)!`, `target:` ` [Path](../java/nio/file/Path.md)!`, `vararg` `attrs:` ` [FileAttribute](../java/nio/file/attribute/FileAttribute.md)<*>!`)` Creates a symbolic link to a target*(optional operation)*. |
| static [Path](../java/nio/file/Path.md)! | [createTempDirectory](../java/nio/file/Files.md))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `attrs:` ` [FileAttribute](../java/nio/file/attribute/FileAttribute.md)<*>!`)` Creates a new directory in the default temporary-file directory, using the given prefix to generate its name. |
| --- | --- |
| static [Path](../java/nio/file/Path.md)! | [createTempDirectory](../java/nio/file/Files.md))`(`dir:` ` [Path](../java/nio/file/Path.md)!`, `prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `attrs:` ` [FileAttribute](../java/nio/file/attribute/FileAttribute.md)<*>!`)` Creates a new directory in the specified directory, using the given prefix to generate its name. |
| static [Path](../java/nio/file/Path.md)! | [createTempFile](../java/nio/file/Files.md))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `suffix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `attrs:` ` [FileAttribute](../java/nio/file/attribute/FileAttribute.md)<*>!`)` Creates an empty file in the default temporary-file directory, using the given prefix and suffix to generate its name. |
| static [Path](../java/nio/file/Path.md)! | [createTempFile](../java/nio/file/Files.md))`(`dir:` ` [Path](../java/nio/file/Path.md)!`, `prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `suffix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `attrs:` ` [FileAttribute](../java/nio/file/attribute/FileAttribute.md)<*>!`)` Creates a new empty file in the specified directory, using the given prefix and suffix strings to generate its name. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [delete](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`)` Deletes a file. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [deleteIfExists](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`)` Deletes a file if it exists. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [exists](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `vararg` `options:` ` [LinkOption](../java/nio/file/LinkOption.md)!`)` Tests whether a file exists. |
| --- | --- |
| static [Stream](../java/util/stream/Stream.md)\< [Path](../java/nio/file/Path.md)!\>! | [find](../java/nio/file/Files.md))`(`start:` ` [Path](../java/nio/file/Path.md)!`, `maxDepth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `matcher:` ` [BiPredicate](../java/util/function/BiPredicate.md)< [Path](../java/nio/file/Path.md)!,` ` [BasicFileAttributes](../java/nio/file/attribute/BasicFileAttributes.md)!>!`, `vararg` `options:` ` [FileVisitOption](../java/nio/file/FileVisitOption.md)!`)` Return a`Stream`that is lazily populated with`Path`by searching for files in a file tree rooted at a given starting file. |
| static [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAttribute](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `attribute:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `options:` ` [LinkOption](../java/nio/file/LinkOption.md)!`)` Reads the value of a file attribute. |
| staticV | [getFileAttributeView](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `type:` ` [Class](../java/lang/Class.md)<V>!`, `vararg` `options:` ` [LinkOption](../java/nio/file/LinkOption.md)!`)` Returns a file attribute view of a given type. |
| --- | --- |
| static [FileStore](../java/nio/file/FileStore.md)! | [getFileStore](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`)` Returns the [FileStore](../java/nio/file/FileStore.md) representing the file store where a file is located. |
| static [FileTime](../java/nio/file/attribute/FileTime.md)! | [getLastModifiedTime](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `vararg` `options:` ` [LinkOption](../java/nio/file/LinkOption.md)!`)` Returns a file's last modified time. |
| static [UserPrincipal](../java/nio/file/attribute/UserPrincipal.md)! | [getOwner](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `vararg` `options:` ` [LinkOption](../java/nio/file/LinkOption.md)!`)` Returns the owner of a file. |
| --- | --- |
| static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [PosixFilePermission](../java/nio/file/attribute/PosixFilePermission.md)!\>! | [getPosixFilePermissions](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `vararg` `options:` ` [LinkOption](../java/nio/file/LinkOption.md)!`)` Returns a file's POSIX file permissions. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDirectory](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `vararg` `options:` ` [LinkOption](../java/nio/file/LinkOption.md)!`)` Tests whether a file is a directory. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExecutable](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`)` Tests whether a file is executable. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHidden](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`)` Tells whether or not a file is considered*hidden*. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadable](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`)` Tests whether a file is readable. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRegularFile](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `vararg` `options:` ` [LinkOption](../java/nio/file/LinkOption.md)!`)` Tests whether a file is a regular file with opaque content. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSameFile](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `path2:` ` [Path](../java/nio/file/Path.md)!`)` Tests if two paths locate the same file. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSymbolicLink](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`)` Tests whether a file is a symbolic link. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWritable](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`)` Tests whether a file is writable. |
| --- | --- |
| static [Stream](../java/util/stream/Stream.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [lines](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`)` Read all lines from a file as a`Stream`. |
| static [Stream](../java/util/stream/Stream.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [lines](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `cs:` ` [Charset](../java/nio/charset/Charset.md)!`)` Read all lines from a file as a`Stream`. |
| static [Stream](../java/util/stream/Stream.md)\< [Path](../java/nio/file/Path.md)!\>! | [list](../java/nio/file/Files.md))`(`dir:` ` [Path](../java/nio/file/Path.md)!`)` Return a lazily populated`Stream`, the elements of which are the entries in the directory. |
| --- | --- |
| static [Path](../java/nio/file/Path.md)! | [move](../java/nio/file/Files.md))`(`source:` ` [Path](../java/nio/file/Path.md)!`, `target:` ` [Path](../java/nio/file/Path.md)!`, `vararg` `options:` ` [CopyOption](../java/nio/file/CopyOption.md)!`)` Move or rename a file to a target file. |
| static [BufferedReader](../java/io/BufferedReader.md)! | [newBufferedReader](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`)` Opens a file for reading, returning a`BufferedReader`to read text from the file in an efficient manner. |
| static [BufferedReader](../java/io/BufferedReader.md)! | [newBufferedReader](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `cs:` ` [Charset](../java/nio/charset/Charset.md)!`)` Opens a file for reading, returning a`BufferedReader`that may be used to read text from the file in an efficient manner. |
| --- | --- |
| static [BufferedWriter](../java/io/BufferedWriter.md)! | [newBufferedWriter](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `cs:` ` [Charset](../java/nio/charset/Charset.md)!`, `vararg` `options:` ` [OpenOption](../java/nio/file/OpenOption.md)!`)` Opens or creates a file for writing, returning a`BufferedWriter`that may be used to write text to the file in an efficient manner. |
| static [BufferedWriter](../java/io/BufferedWriter.md)! | [newBufferedWriter](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `vararg` `options:` ` [OpenOption](../java/nio/file/OpenOption.md)!`)` Opens or creates a file for writing, returning a`BufferedWriter`to write text to the file in an efficient manner. |
| static [SeekableByteChannel](../java/nio/channels/SeekableByteChannel.md)! | [newByteChannel](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `vararg` `options:` ` [OpenOption](../java/nio/file/OpenOption.md)!`)` Opens or creates a file, returning a seekable byte channel to access the file. |
| --- | --- |
| static [SeekableByteChannel](../java/nio/channels/SeekableByteChannel.md)! | [newByteChannel](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `options:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<out` ` [OpenOption](../java/nio/file/OpenOption.md)!>!`, `vararg` `attrs:` ` [FileAttribute](../java/nio/file/attribute/FileAttribute.md)<*>!`)` Opens or creates a file, returning a seekable byte channel to access the file. |
| static [DirectoryStream](../java/nio/file/DirectoryStream.md)\< [Path](../java/nio/file/Path.md)!\>! | [newDirectoryStream](../java/nio/file/Files.md))`(`dir:` ` [Path](../java/nio/file/Path.md)!`)` Opens a directory, returning a [DirectoryStream](../java/nio/file/DirectoryStream.md) to iterate over all entries in the directory. |
| static [DirectoryStream](../java/nio/file/DirectoryStream.md)\< [Path](../java/nio/file/Path.md)!\>! | [newDirectoryStream](../java/nio/file/Files.md))`(`dir:` ` [Path](../java/nio/file/Path.md)!`, `glob:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Opens a directory, returning a [DirectoryStream](../java/nio/file/DirectoryStream.md) to iterate over the entries in the directory. |
| --- | --- |
| static [DirectoryStream](../java/nio/file/DirectoryStream.md)\< [Path](../java/nio/file/Path.md)!\>! | [newDirectoryStream](../java/nio/file/Files.md))`(`dir:` ` [Path](../java/nio/file/Path.md)!`, `filter:` ` [DirectoryStream.Filter](../java/nio/file/DirectoryStream.Filter.md)<in` ` [Path](../java/nio/file/Path.md)!>!`)` Opens a directory, returning a [DirectoryStream](../java/nio/file/DirectoryStream.md) to iterate over the entries in the directory. |
| static [InputStream](../java/io/InputStream.md)! | [newInputStream](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `vararg` `options:` ` [OpenOption](../java/nio/file/OpenOption.md)!`)` Opens a file, returning an input stream to read from the file. |
| static [OutputStream](../java/io/OutputStream.md)! | [newOutputStream](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `vararg` `options:` ` [OpenOption](../java/nio/file/OpenOption.md)!`)` Opens or creates a file, returning an output stream that may be used to write bytes to the file. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [notExists](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `vararg` `options:` ` [LinkOption](../java/nio/file/LinkOption.md)!`)` Tests whether the file located by this path does not exist. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [probeContentType](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`)` Probes the content type of a file. |
| static [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readAllBytes](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`)` Reads all the bytes from a file. |
| --- | --- |
| static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [readAllLines](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`)` Read all lines from a file. |
| static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [readAllLines](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `cs:` ` [Charset](../java/nio/charset/Charset.md)!`)` Read all lines from a file. |
| staticA | [readAttributes](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `type:` ` [Class](../java/lang/Class.md)<A>!`, `vararg` `options:` ` [LinkOption](../java/nio/file/LinkOption.md)!`)` Reads a file's attributes as a bulk operation. |
| --- | --- |
| static [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [readAttributes](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `attributes:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `options:` ` [LinkOption](../java/nio/file/LinkOption.md)!`)` Reads a set of file attributes as a bulk operation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [readString](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`)` Reads all content from a file into a string, decoding from bytes to characters using the [UTF-8](../java/nio/charset/StandardCharsets.md) [charset](../java/nio/charset/Charset.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [readString](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `cs:` ` [Charset](../java/nio/charset/Charset.md)!`)` Reads all characters from a file into a string, decoding from bytes to characters using the specified [charset](../java/nio/charset/Charset.md). |
| --- | --- |
| static [Path](../java/nio/file/Path.md)! | [readSymbolicLink](../java/nio/file/Files.md))`(`link:` ` [Path](../java/nio/file/Path.md)!`)` Reads the target of a symbolic link*(optional operation)*. |
| static [Path](../java/nio/file/Path.md)! | [setAttribute](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `attribute:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `vararg` `options:` ` [LinkOption](../java/nio/file/LinkOption.md)!`)` Sets the value of a file attribute. |
| static [Path](../java/nio/file/Path.md)! | [setLastModifiedTime](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `time:` ` [FileTime](../java/nio/file/attribute/FileTime.md)!`)` Updates a file's last modified time attribute. |
| --- | --- |
| static [Path](../java/nio/file/Path.md)! | [setOwner](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `owner:` ` [UserPrincipal](../java/nio/file/attribute/UserPrincipal.md)!`)` Updates the file owner. |
| static [Path](../java/nio/file/Path.md)! | [setPosixFilePermissions](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `perms:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [PosixFilePermission](../java/nio/file/attribute/PosixFilePermission.md)!>!`)` Sets a file's POSIX permissions. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [size](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`)` Returns the size of a file (in bytes). |
| --- | --- |
| static [Stream](../java/util/stream/Stream.md)\< [Path](../java/nio/file/Path.md)!\>! | [walk](../java/nio/file/Files.md))`(`start:` ` [Path](../java/nio/file/Path.md)!`, `maxDepth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `vararg` `options:` ` [FileVisitOption](../java/nio/file/FileVisitOption.md)!`)` Return a`Stream`that is lazily populated with`Path`by walking the file tree rooted at a given starting file. |
| static [Stream](../java/util/stream/Stream.md)\< [Path](../java/nio/file/Path.md)!\>! | [walk](../java/nio/file/Files.md))`(`start:` ` [Path](../java/nio/file/Path.md)!`, `vararg` `options:` ` [FileVisitOption](../java/nio/file/FileVisitOption.md)!`)` Return a`Stream`that is lazily populated with`Path`by walking the file tree rooted at a given starting file. |
| static [Path](../java/nio/file/Path.md)! | [walkFileTree](../java/nio/file/Files.md))`(`start:` ` [Path](../java/nio/file/Path.md)!`, `visitor:` ` [FileVisitor](../java/nio/file/FileVisitor.md)<in` ` [Path](../java/nio/file/Path.md)!>!`)` Walks a file tree. |
| --- | --- |
| static [Path](../java/nio/file/Path.md)! | [walkFileTree](../java/nio/file/Files.md))`(`start:` ` [Path](../java/nio/file/Path.md)!`, `options:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [FileVisitOption](../java/nio/file/FileVisitOption.md)!>!`, `maxDepth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `visitor:` ` [FileVisitor](../java/nio/file/FileVisitor.md)<in` ` [Path](../java/nio/file/Path.md)!>!`)` Walks a file tree. |
| static [Path](../java/nio/file/Path.md)! | [write](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `bytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `vararg` `options:` ` [OpenOption](../java/nio/file/OpenOption.md)!`)` Writes bytes to a file. |
| static [Path](../java/nio/file/Path.md)! | [write](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `lines:` ` [MutableIterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>!`, `cs:` ` [Charset](../java/nio/charset/Charset.md)!`, `vararg` `options:` ` [OpenOption](../java/nio/file/OpenOption.md)!`)` Write lines of text to a file. |
| --- | --- |
| static [Path](../java/nio/file/Path.md)! | [write](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `lines:` ` [MutableIterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>!`, `vararg` `options:` ` [OpenOption](../java/nio/file/OpenOption.md)!`)` Write lines of text to a file. |
| static [Path](../java/nio/file/Path.md)! | [writeString](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `cs:` ` [Charset](../java/nio/charset/Charset.md)!`, `vararg` `options:` ` [OpenOption](../java/nio/file/OpenOption.md)!`)` Write a [CharSequence](../java/lang/CharSequence.md) to a file. |
| static [Path](../java/nio/file/Path.md)! | [writeString](../java/nio/file/Files.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`, `csq:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `vararg` `options:` ` [OpenOption](../java/nio/file/OpenOption.md)!`)` Write a [CharSequence](../java/lang/CharSequence.md) to a file. |
| --- | --- |

## Public methods

### copy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun copy(
    in: InputStream!, 
    target: Path!, 
    vararg options: CopyOption!
): Long
```

Copies all bytes from an input stream to a file. On return, the input stream will be at end of stream.

By default, the copy fails if the target file already exists or is a symbolic link. If the [REPLACE_EXISTING](../java/nio/file/StandardCopyOption.md) option is specified, and the target file already exists, then it is replaced if it is not a non-empty directory. If the target file exists and is a symbolic link, then the symbolic link is replaced. In this release, the`REPLACE_EXISTING`option is the only option required to be supported by this method. Additional options may be supported in future releases.

If an I/O error occurs reading from the input stream or writing to the file, then it may do so after the target file has been created and after some bytes have been read or written. Consequently the input stream may not be at end of stream and may be in an inconsistent state. It is strongly recommended that the input stream be promptly closed if an I/O error occurs.

This method may block indefinitely reading from the input stream (or writing to the file). The behavior for the case that the input stream is*asynchronously closed*or the thread interrupted during the copy is highly input stream and file system provider specific and therefore not specified.

**Usage example**: Suppose we want to capture a web page and save it to a file: 

```kotlin
Path path = ...
      URI u = URI.create("http://java.sun.com/");
      try (InputStream in = u.toURL().openStream()) {
          Files.copy(in, path);
      }
  
```

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| `in` | [InputStream](../java/io/InputStream.md)!:the input stream to read from |
| `target` | [Path](../java/nio/file/Path.md)!:the path to the file |
| `options` | [CopyOption](../java/nio/file/CopyOption.md)!:options specifying how the copy should be done |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the number of bytes read or written |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when reading or writing |
| `java.nio.file.FileAlreadyExistsException` | if the target file exists but cannot be replaced because the`REPLACE_EXISTING`option is not specified*(optional specific exception)* |
| `java.nio.file.DirectoryNotEmptyException` | the`REPLACE_EXISTING`option is specified but the file cannot be replaced because it is a non-empty directory*(optional specific exception)*\* |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if`options`contains a copy option that is not supported |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access to the file. Where the`REPLACE_EXISTING`option is specified, the security manager's [checkDelete](../java/lang/SecurityManager.md))method is invoked to check that an existing file can be deleted. |

### copy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun copy(
    source: Path!, 
    out: OutputStream!
): Long
```

Copies all bytes from a file to an output stream.

If an I/O error occurs reading from the file or writing to the output stream, then it may do so after some bytes have been read or written. Consequently the output stream may be in an inconsistent state. It is strongly recommended that the output stream be promptly closed if an I/O error occurs.

This method may block indefinitely writing to the output stream (or reading from the file). The behavior for the case that the output stream is*asynchronously closed*or the thread interrupted during the copy is highly output stream and file system provider specific and therefore not specified.

Note that if the given output stream is [java.io.Flushable](../java/io/Flushable.md) then its [flush](../java/io/Flushable.md))method may need to invoked after this method completes so as to flush any buffered output.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------|
| `source` | [Path](../java/nio/file/Path.md)!:the path to the file |
| `out` | [OutputStream](../java/io/OutputStream.md)!:the output stream to write to |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the number of bytes read or written |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs when reading or writing |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the file. |

### copy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun copy(
    source: Path!, 
    target: Path!, 
    vararg options: CopyOption!
): Path!
```

Copy a file to a target file.

This method copies a file to the target file with the`options`parameter specifying how the copy is performed. By default, the copy fails if the target file already exists or is a symbolic link, except if the source and target are the [same](../java/nio/file/Files.md))file, in which case the method completes without copying the file. File attributes are not required to be copied to the target file. If symbolic links are supported, and the file is a symbolic link, then the final target of the link is copied. If the file is a directory then it creates an empty directory in the target location (entries in the directory are not copied). This method can be used with the #walkFileTree method to copy a directory and all entries in the directory, or an entire*file-tree*where required.

The`options`parameter may include any of the following:

| Option | Description |
| --- | --- |
| [REPLACE_EXISTING](../java/nio/file/StandardCopyOption.md) | If the target file exists, then the target file is replaced if it is not a non-empty directory. If the target file exists and is a symbolic link, then the symbolic link itself, not the target of the link, is replaced. |
| [COPY_ATTRIBUTES](../java/nio/file/StandardCopyOption.md) | Attempts to copy the file attributes associated with this file to the target file. The exact file attributes that are copied is platform and file system dependent and therefore unspecified. Minimally, the [last-modified-time](../java/nio/file/attribute/BasicFileAttributes.md))is copied to the target file if supported by both the source and target file stores. Copying of file timestamps may result in precision loss. |
| [NOFOLLOW_LINKS](../java/nio/file/LinkOption.md) | Symbolic links are not followed. If the file is a symbolic link, then the symbolic link itself, not the target of the link, is copied. It is implementation specific if file attributes can be copied to the new link. In other words, the`COPY_ATTRIBUTES`option may be ignored when copying a symbolic link. |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

An implementation of this interface may support additional implementation specific options.

Copying a file is not an atomic operation. If an [IOException](../java/io/IOException.md) is thrown, then it is possible that the target file is incomplete or some of its file attributes have not been copied from the source file. When the`REPLACE_EXISTING`option is specified and the target file exists, then the target file is replaced. The check for the existence of the file and the creation of the new file may not be atomic with respect to other file system activities.

**Usage Example:**Suppose we want to copy a file into a directory, giving it the same file name as the source file: 

```kotlin
Path source = ...
      Path newdir = ...
      Files.copy(source, newdir.resolve(source.getFileName());
  
```

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Path](../java/nio/file/Path.md)!:the path to the file to copy |
| `target` | [Path](../java/nio/file/Path.md)!:the path to the target file (may be associated with a different provider to the source path) |
| `options` | [CopyOption](../java/nio/file/CopyOption.md)!:options specifying how the copy should be done |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Path](../java/nio/file/Path.md)! | the path to the target file |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the array contains a copy option that is not supported |
| `java.nio.file.FileAlreadyExistsException` | if the target file exists but cannot be replaced because the`REPLACE_EXISTING`option is not specified*(optional specific exception)* |
| `java.nio.file.DirectoryNotEmptyException` | the`REPLACE_EXISTING`option is specified but the file cannot be replaced because it is a non-empty directory*(optional specific exception)* |
| --- | --- |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the source file, the [checkWrite](../java/lang/SecurityManager.md))is invoked to check write access to the target file. If a symbolic link is copied the security manager is invoked to check [LinkPermission](../java/nio/file/LinkPermission.md)`("symbolic")`. |

### createDirectories

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createDirectories(
    dir: Path!, 
    vararg attrs: FileAttribute<*>!
): Path!
```

Creates a directory by creating all nonexistent parent directories first. Unlike the [createDirectory](../java/nio/file/Files.md))method, an exception is not thrown if the directory could not be created because it already exists.

The`attrs`parameter is optional [file-attributes](../java/nio/file/attribute/FileAttribute.md) to set atomically when creating the nonexistent directories. Each file attribute is identified by its [name](../java/nio/file/attribute/FileAttribute.md)). If more than one attribute of the same name is included in the array then all but the last occurrence is ignored.

If this method fails, then it may do so after creating some, but not all, of the parent directories.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dir` | [Path](../java/nio/file/Path.md)!:the directory to create |
| `attrs` | [FileAttribute](../java/nio/file/attribute/FileAttribute.md)\<\*\>!:an optional list of file attributes to set atomically when creating the directory |

| Return ||
|----------------------------------------------------------------------------|---------------|
| [Path](../java/nio/file/Path.md)! | the directory |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the array contains an attribute that cannot be set atomically when creating the directory |
| `java.nio.file.FileAlreadyExistsException` | if`dir`exists but is not a directory*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| --- | --- |
| `java.lang.SecurityException` | in the case of the default provider, and a security manager is installed, the [checkWrite](../java/lang/SecurityManager.md))method is invoked prior to attempting to create a directory and its [checkRead](../java/lang/SecurityManager.md))is invoked for each parent directory that is checked. If`dir`is not an absolute path then its [toAbsolutePath](../java/nio/file/Path.md))may need to be invoked to get its absolute path. This may invoke the security manager's [checkPropertyAccess](../java/lang/SecurityManager.md))method to check access to the system property`user.dir` |

### createDirectory

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createDirectory(
    dir: Path!, 
    vararg attrs: FileAttribute<*>!
): Path!
```

Creates a new directory. The check for the existence of the file and the creation of the directory if it does not exist are a single operation that is atomic with respect to all other filesystem activities that might affect the directory. The [createDirectories](../java/nio/file/Files.md))method should be used where it is required to create all nonexistent parent directories first.

The`attrs`parameter is optional [file-attributes](../java/nio/file/attribute/FileAttribute.md) to set atomically when creating the directory. Each attribute is identified by its [name](../java/nio/file/attribute/FileAttribute.md)). If more than one attribute of the same name is included in the array then all but the last occurrence is ignored.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dir` | [Path](../java/nio/file/Path.md)!:the directory to create |
| `attrs` | [FileAttribute](../java/nio/file/attribute/FileAttribute.md)\<\*\>!:an optional list of file attributes to set atomically when creating the directory |

| Return ||
|----------------------------------------------------------------------------|---------------|
| [Path](../java/nio/file/Path.md)! | the directory |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the array contains an attribute that cannot be set atomically when creating the directory |
| `java.nio.file.FileAlreadyExistsException` | if a directory could not otherwise be created because a file of that name already exists*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs or the parent directory does not exist |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access to the new directory. |

### createFile

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createFile(
    path: Path!, 
    vararg attrs: FileAttribute<*>!
): Path!
```

Creates a new and empty file, failing if the file already exists. The check for the existence of the file and the creation of the new file if it does not exist are a single operation that is atomic with respect to all other filesystem activities that might affect the directory.

The`attrs`parameter is optional [file-attributes](../java/nio/file/attribute/FileAttribute.md) to set atomically when creating the file. Each attribute is identified by its [name](../java/nio/file/attribute/FileAttribute.md)). If more than one attribute of the same name is included in the array then all but the last occurrence is ignored.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file to create |
| `attrs` | [FileAttribute](../java/nio/file/attribute/FileAttribute.md)\<\*\>!:an optional list of file attributes to set atomically when creating the file |

| Return ||
|----------------------------------------------------------------------------|----------|
| [Path](../java/nio/file/Path.md)! | the file |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the array contains an attribute that cannot be set atomically when creating the file |
| `java.nio.file.FileAlreadyExistsException` | if a file of that name already exists*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs or the parent directory does not exist |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access to the new file. |

### createLink

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createLink(
    link: Path!, 
    existing: Path!
): Path!
```

Creates a new link (directory entry) for an existing file*(optional operation)*.

The`link`parameter locates the directory entry to create. The`existing`parameter is the path to an existing file. This method creates a new directory entry for the file so that it can be accessed using`link`as the path. On some file systems this is known as creating a "hard link". Whether the file attributes are maintained for the file or for each directory entry is file system specific and therefore not specified. Typically, a file system requires that all links (directory entries) for a file be on the same file system. Furthermore, on some platforms, the Java virtual machine may require to be started with implementation specific privileges to create hard links or to create links to directories.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------|
| `link` | [Path](../java/nio/file/Path.md)!:the link (directory entry) to create |
| `existing` | [Path](../java/nio/file/Path.md)!:a path to an existing file |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Path](../java/nio/file/Path.md)! | the path to the link (directory entry) |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the implementation does not support adding an existing file to a directory |
| `java.nio.file.FileAlreadyExistsException` | if the entry could not otherwise be created because a file of that name already exists*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, it denies [LinkPermission](../java/nio/file/LinkPermission.md)`("hard")`or its [checkWrite](../java/lang/SecurityManager.md))method denies write access to either the link or the existing file. |

### createSymbolicLink

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createSymbolicLink(
    link: Path!, 
    target: Path!, 
    vararg attrs: FileAttribute<*>!
): Path!
```

Creates a symbolic link to a target*(optional operation)*.

The`target`parameter is the target of the link. It may be an [absolute](../java/nio/file/Path.md))or relative path and may not exist. When the target is a relative path then file system operations on the resulting link are relative to the path of the link.

The`attrs`parameter is optional [attributes](../java/nio/file/attribute/FileAttribute.md) to set atomically when creating the link. Each attribute is identified by its [name](../java/nio/file/attribute/FileAttribute.md)). If more than one attribute of the same name is included in the array then all but the last occurrence is ignored.

Where symbolic links are supported, but the underlying [FileStore](../java/nio/file/FileStore.md) does not support symbolic links, then this may fail with an [IOException](../java/io/IOException.md). Additionally, some operating systems may require that the Java virtual machine be started with implementation specific privileges to create symbolic links, in which case this method may throw`IOException`.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `link` | [Path](../java/nio/file/Path.md)!:the path of the symbolic link to create |
| `target` | [Path](../java/nio/file/Path.md)!:the target of the symbolic link |
| `attrs` | [FileAttribute](../java/nio/file/attribute/FileAttribute.md)\<\*\>!:the array of attributes to set atomically when creating the symbolic link |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-------------------------------|
| [Path](../java/nio/file/Path.md)! | the path to the symbolic link |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the implementation does not support symbolic links or the array contains an attribute that cannot be set atomically when creating the symbolic link |
| `java.nio.file.FileAlreadyExistsException` | if a file with the name already exists*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, it denies [LinkPermission](../java/nio/file/LinkPermission.md)`("symbolic")`or its [checkWrite](../java/lang/SecurityManager.md))method denies write access to the path of the symbolic link. |

### createTempDirectory

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createTempDirectory(
    prefix: String!, 
    vararg attrs: FileAttribute<*>!
): Path!
```

Creates a new directory in the default temporary-file directory, using the given prefix to generate its name. The resulting`Path`is associated with the default`FileSystem`.

This method works in exactly the manner specified by[createTempDirectory(java.nio.file.Path,java.lang.String,java.nio.file.attribute.FileAttribute[])](https://developer.android.com/reference/kotlin/java/nio/file/Files#createTempDirectory(java.nio.file.Path,%20kotlin.String,%20java.nio.file.attribute.FileAttribute))method for the case that the`dir`parameter is the temporary-file directory.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the prefix string to be used in generating the directory's name; may be`null` |
| `attrs` | [FileAttribute](../java/nio/file/attribute/FileAttribute.md)\<\*\>!:an optional list of file attributes to set atomically when creating the directory |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Path](../java/nio/file/Path.md)! | the path to the newly created directory that did not exist before this method was invoked |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the prefix cannot be used to generate a candidate directory name |
| `java.lang.UnsupportedOperationException` | if the array contains an attribute that cannot be set atomically when creating the directory |
| `java.io.IOException` | if an I/O error occurs or the temporary-file directory does not exist |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access when creating the directory. |

### createTempDirectory

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createTempDirectory(
    dir: Path!, 
    prefix: String!, 
    vararg attrs: FileAttribute<*>!
): Path!
```

Creates a new directory in the specified directory, using the given prefix to generate its name. The resulting`Path`is associated with the same`FileSystem`as the given directory.

The details as to how the name of the directory is constructed is implementation dependent and therefore not specified. Where possible the`prefix`is used to construct candidate names.

As with the`createTempFile`methods, this method is only part of a temporary-file facility. A [shutdown-hook](../java/lang/Runtime.md)), or the [java.io.File#deleteOnExit](../java/io/File.md))mechanism may be used to delete the directory automatically.

The`attrs`parameter is optional [file-attributes](../java/nio/file/attribute/FileAttribute.md) to set atomically when creating the directory. Each attribute is identified by its [name](../java/nio/file/attribute/FileAttribute.md)). If more than one attribute of the same name is included in the array then all but the last occurrence is ignored.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dir` | [Path](../java/nio/file/Path.md)!:the path to directory in which to create the directory |
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the prefix string to be used in generating the directory's name; may be`null` |
| `attrs` | [FileAttribute](../java/nio/file/attribute/FileAttribute.md)\<\*\>!:an optional list of file attributes to set atomically when creating the directory |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Path](../java/nio/file/Path.md)! | the path to the newly created directory that did not exist before this method was invoked |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the prefix cannot be used to generate a candidate directory name |
| `java.lang.UnsupportedOperationException` | if the array contains an attribute that cannot be set atomically when creating the directory |
| `java.io.IOException` | if an I/O error occurs or`dir`does not exist |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access when creating the directory. |

### createTempFile

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createTempFile(
    prefix: String!, 
    suffix: String!, 
    vararg attrs: FileAttribute<*>!
): Path!
```

Creates an empty file in the default temporary-file directory, using the given prefix and suffix to generate its name. The resulting`Path`is associated with the default`FileSystem`.

This method works in exactly the manner specified by the[createTempFile(java.nio.file.Path,java.lang.String,java.lang.String,java.nio.file.attribute.FileAttribute[])](https://developer.android.com/reference/kotlin/java/nio/file/Files#createTempFile(java.nio.file.Path,%20kotlin.String,%20kotlin.String,%20java.nio.file.attribute.FileAttribute))method for the case that the`dir`parameter is the temporary-file directory.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the prefix string to be used in generating the file's name; may be`null` |
| `suffix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the suffix string to be used in generating the file's name; may be`null`, in which case "`.tmp`" is used |
| `attrs` | [FileAttribute](../java/nio/file/attribute/FileAttribute.md)\<\*\>!:an optional list of file attributes to set atomically when creating the file |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Path](../java/nio/file/Path.md)! | the path to the newly created file that did not exist before this method was invoked |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the prefix or suffix parameters cannot be used to generate a candidate file name |
| `java.lang.UnsupportedOperationException` | if the array contains an attribute that cannot be set atomically when creating the directory |
| `java.io.IOException` | if an I/O error occurs or the temporary-file directory does not exist |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access to the file. |

### createTempFile

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createTempFile(
    dir: Path!, 
    prefix: String!, 
    suffix: String!, 
    vararg attrs: FileAttribute<*>!
): Path!
```

Creates a new empty file in the specified directory, using the given prefix and suffix strings to generate its name. The resulting`Path`is associated with the same`FileSystem`as the given directory.

The details as to how the name of the file is constructed is implementation dependent and therefore not specified. Where possible the`prefix`and`suffix`are used to construct candidate names in the same manner as the [java.io.File#createTempFile(String,String,File)](../java/io/File.md))method.

As with the`File.createTempFile`methods, this method is only part of a temporary-file facility. Where used as a*work files* , the resulting file may be opened using the [DELETE_ON_CLOSE](../java/nio/file/StandardOpenOption.md) option so that the file is deleted when the appropriate`close`method is invoked. Alternatively, a [shutdown-hook](../java/lang/Runtime.md)), or the [java.io.File#deleteOnExit](../java/io/File.md))mechanism may be used to delete the file automatically.

The`attrs`parameter is optional [file-attributes](../java/nio/file/attribute/FileAttribute.md) to set atomically when creating the file. Each attribute is identified by its [name](../java/nio/file/attribute/FileAttribute.md)). If more than one attribute of the same name is included in the array then all but the last occurrence is ignored. When no file attributes are specified, then the resulting file may have more restrictive access permissions to files created by the [java.io.File#createTempFile(String,String,File)](../java/io/File.md))method.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dir` | [Path](../java/nio/file/Path.md)!:the path to directory in which to create the file |
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the prefix string to be used in generating the file's name; may be`null` |
| `suffix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the suffix string to be used in generating the file's name; may be`null`, in which case "`.tmp`" is used |
| --- | --- |
| `attrs` | [FileAttribute](../java/nio/file/attribute/FileAttribute.md)\<\*\>!:an optional list of file attributes to set atomically when creating the file |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Path](../java/nio/file/Path.md)! | the path to the newly created file that did not exist before this method was invoked |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the prefix or suffix parameters cannot be used to generate a candidate file name |
| `java.lang.UnsupportedOperationException` | if the array contains an attribute that cannot be set atomically when creating the directory |
| `java.io.IOException` | if an I/O error occurs or`dir`does not exist |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access to the file. |

### delete

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun delete(path: Path!): Unit
```

Deletes a file.

An implementation may require to examine the file to determine if the file is a directory. Consequently this method may not be atomic with respect to other file system operations. If the file is a symbolic link then the symbolic link itself, not the final target of the link, is deleted.

If the file is a directory then the directory must be empty. In some implementations a directory has entries for special files or links that are created when the directory is created. In such implementations a directory is considered empty when only the special entries exist. This method can be used with the #walkFileTree method to delete a directory and all entries in the directory, or an entire*file-tree*where required.

On some operating systems it may not be possible to remove a file when it is open and in use by this Java virtual machine or other programs.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file to delete |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.file.NoSuchFileException` | if the file does not exist*(optional specific exception)* |
| `java.nio.file.DirectoryNotEmptyException` | if the file is a directory and could not otherwise be deleted because the directory is not empty*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [SecurityManager.checkDelete(String)](../java/lang/SecurityManager.md))method is invoked to check delete access to the file |

### deleteIfExists

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun deleteIfExists(path: Path!): Boolean
```

Deletes a file if it exists.

As with the [delete(Path)](../java/nio/file/Files.md))method, an implementation may need to examine the file to determine if the file is a directory. Consequently this method may not be atomic with respect to other file system operations. If the file is a symbolic link, then the symbolic link itself, not the final target of the link, is deleted.

If the file is a directory then the directory must be empty. In some implementations a directory has entries for special files or links that are created when the directory is created. In such implementations a directory is considered empty when only the special entries exist.

On some operating systems it may not be possible to remove a file when it is open and in use by this Java virtual machine or other programs.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file to delete |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the file was deleted by this method;`false`if the file could not be deleted because it did not exist |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.file.DirectoryNotEmptyException` | if the file is a directory and could not otherwise be deleted because the directory is not empty*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [SecurityManager.checkDelete(String)](../java/lang/SecurityManager.md))method is invoked to check delete access to the file. |
| --- | --- |

### exists

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun exists(
    path: Path!, 
    vararg options: LinkOption!
): Boolean
```

Tests whether a file exists.

The`options`parameter may be used to indicate how symbolic links are handled for the case that the file is a symbolic link. By default, symbolic links are followed. If the option [NOFOLLOW_LINKS](../java/nio/file/LinkOption.md) is present then symbolic links are not followed.

Note that the result of this method is immediately outdated. If this method indicates the file exists then there is no guarantee that a subsequent access will succeed. Care should be taken when using this method in security sensitive applications.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file to test |
| `options` | [LinkOption](../java/nio/file/LinkOption.md)!:options indicating how symbolic links are handled . |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the file exists;`false`if the file does not exist or its existence cannot be determined. |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | In the case of the default provider, the [java.lang.SecurityManager#checkRead(java.lang.String)](../java/lang/SecurityManager.md))is invoked to check read access to the file. |

**See Also**

- [#notExists](../java/nio/file/Files.md)) 

### find

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun find(
    start: Path!, 
    maxDepth: Int, 
    matcher: BiPredicate<Path!, BasicFileAttributes!>!, 
    vararg options: FileVisitOption!
): Stream<Path!>!
```

Return a`Stream`that is lazily populated with`Path`by searching for files in a file tree rooted at a given starting file.

This method walks the file tree in exactly the manner specified by the #walk method. For each file encountered, the given [BiPredicate](../java/util/function/BiPredicate.md) is invoked with its [Path](../java/nio/file/Path.md) and [BasicFileAttributes](../java/nio/file/attribute/BasicFileAttributes.md). The`Path`object is obtained as if by [resolving](../java/nio/file/Path.md))the relative path against`start`and is only included in the returned [Stream](../java/util/stream/Stream.md) if the`BiPredicate`returns true. Compare to calling [filter](../java/util/stream/Stream.md))on the`Stream`returned by`walk`method, this method may be more efficient by avoiding redundant retrieval of the`BasicFileAttributes`.

The returned stream contains references to one or more open directories. The directories are closed by closing the stream.

If an [IOException](../java/io/IOException.md) is thrown when accessing the directory after returned from this method, it is wrapped in an [UncheckedIOException](../java/io/UncheckedIOException.md) which will be thrown from the method that caused the access to take place.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `start` | [Path](../java/nio/file/Path.md)!:the starting file |
| `maxDepth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of directory levels to search |
| `matcher` | [BiPredicate](../java/util/function/BiPredicate.md)\< [Path](../java/nio/file/Path.md)!, [BasicFileAttributes](../java/nio/file/attribute/BasicFileAttributes.md)!\>!:the function used to decide whether a file should be included in the returned stream |
| --- | --- |
| `options` | [FileVisitOption](../java/nio/file/FileVisitOption.md)!:options to configure the traversal |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Stream](../java/util/stream/Stream.md)< [Path](../java/nio/file/Path.md)!>! | the [Stream](../java/util/stream/Stream.md) of [Path](../java/nio/file/Path.md) |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the`maxDepth`parameter is negative |
| `java.lang.SecurityException` | If the security manager denies access to the starting file. In the case of the default provider, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the directory. |
| `java.io.IOException` | if an I/O error is thrown when accessing the starting file. |
| --- | --- |

**See Also**

- [#walk(Path, int, FileVisitOption...)](../java/nio/file/Files.md)) 

### getAttribute

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getAttribute(
    path: Path!, 
    attribute: String!, 
    vararg options: LinkOption!
): Any!
```

Reads the value of a file attribute.

The`attribute`parameter identifies the attribute to be read and takes the form:
\[*view-name* **:** \]*attribute-name* where square brackets \[...\] delineate an optional component and the character`':'`stands for itself.

*view-name* is the [name](../java/nio/file/attribute/AttributeView.md))of a [FileAttributeView](../java/nio/file/attribute/FileAttributeView.md) that identifies a set of file attributes. If not specified then it defaults to`"basic"`, the name of the file attribute view that identifies the basic set of file attributes common to many file systems.*attribute-name*is the name of the attribute.

The`options`array may be used to indicate how symbolic links are handled for the case that the file is a symbolic link. By default, symbolic links are followed and the file attribute of the final target of the link is read. If the option [NOFOLLOW_LINKS](../java/nio/file/LinkOption.md) is present then symbolic links are not followed.

**Usage Example:** Suppose we require the user ID of the file owner on a system that supports a "`unix`" view: 

```kotlin
Path path = ...
     int uid = (Integer)Files.getAttribute(path, "unix:uid");
  
```

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |
| `attribute` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the attribute to read |
| `options` | [LinkOption](../java/nio/file/LinkOption.md)!:options indicating how symbolic links are handled |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------|---------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the attribute value |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the attribute view is not available |
| `java.lang.IllegalArgumentException` | if the attribute name is not specified or is not recognized |
| `java.io.IOException` | if an I/O error occurs |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, its [checkRead](../java/lang/SecurityManager.md))method denies read access to the file. If this method is invoked to read security sensitive attributes then the security manager may be invoked to check for additional permissions. |

### getFileAttributeView

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <V : FileAttributeView!> getFileAttributeView(
    path: Path!, 
    type: Class<V>!, 
    vararg options: LinkOption!
): V
```

Returns a file attribute view of a given type.

A file attribute view provides a read-only or updatable view of a set of file attributes. This method is intended to be used where the file attribute view defines type-safe methods to read or update the file attributes. The`type`parameter is the type of the attribute view required and the method returns an instance of that type if supported. The [BasicFileAttributeView](../java/nio/file/attribute/BasicFileAttributeView.md) type supports access to the basic attributes of a file. Invoking this method to select a file attribute view of that type will always return an instance of that class.

The`options`array may be used to indicate how symbolic links are handled by the resulting file attribute view for the case that the file is a symbolic link. By default, symbolic links are followed. If the option [NOFOLLOW_LINKS](../java/nio/file/LinkOption.md) is present then symbolic links are not followed. This option is ignored by implementations that do not support symbolic links.

**Usage Example:**Suppose we want read or set a file's ACL, if supported: 

```kotlin
Path path = ...
      AclFileAttributeView view = Files.getFileAttributeView(path, AclFileAttributeView.class);
      if (view != null) {
          List<AclEntry> acl = view.getAcl();
          :
      }
  
```

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `<V>` | The`FileAttributeView`type |
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |
| `type` | [Class](../java/lang/Class.md)\<V\>!:the`Class`object corresponding to the file attribute view |
| --- | --- |
| `options` | [LinkOption](../java/nio/file/LinkOption.md)!:options indicating how symbolic links are handled |

| Return ||
|---|--------------------------------------------------------------------------------------------------|
| V | a file attribute view of the specified type, or`null`if the attribute view type is not available |

### getFileStore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getFileStore(path: Path!): FileStore!
```

Returns the [FileStore](../java/nio/file/FileStore.md) representing the file store where a file is located.

Once a reference to the`FileStore`is obtained it is implementation specific if operations on the returned`FileStore`, or [FileStoreAttributeView](../java/nio/file/attribute/FileStoreAttributeView.md) objects obtained from it, continue to depend on the existence of the file. In particular the behavior is not defined for the case that the file is deleted or moved to a different file store.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |

| Return ||
|--------------------------------------------------------------------------------------|-----------------------------------------|
| [FileStore](../java/nio/file/FileStore.md)! | the file store where the file is stored |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the file, and in addition it checks [RuntimePermission](../java/lang/RuntimePermission.md)`("getFileStoreAttributes")` |

### getLastModifiedTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getLastModifiedTime(
    path: Path!, 
    vararg options: LinkOption!
): FileTime!
```

Returns a file's last modified time.

The`options`array may be used to indicate how symbolic links are handled for the case that the file is a symbolic link. By default, symbolic links are followed and the file attribute of the final target of the link is read. If the option [NOFOLLOW_LINKS](../java/nio/file/LinkOption.md) is present then symbolic links are not followed.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |
| `options` | [LinkOption](../java/nio/file/LinkOption.md)!:options indicating how symbolic links are handled |

| Return ||
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [FileTime](../java/nio/file/attribute/FileTime.md)! | a`FileTime`representing the time the file was last modified, or an implementation specific default when a time stamp to indicate the time of last modification is not supported by the file system |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, its [checkRead](../java/lang/SecurityManager.md))method denies read access to the file. |

**See Also**

- [java.nio.file.attribute.BasicFileAttributes#lastModifiedTime](../java/nio/file/attribute/BasicFileAttributes.md)) 

### getOwner

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getOwner(
    path: Path!, 
    vararg options: LinkOption!
): UserPrincipal!
```

Returns the owner of a file.

The`path`parameter is associated with a file system that supports [FileOwnerAttributeView](../java/nio/file/attribute/FileOwnerAttributeView.md). This file attribute view provides access to a file attribute that is the owner of the file.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:The path to the file |
| `options` | [LinkOption](../java/nio/file/LinkOption.md)!:options indicating how symbolic links are handled |

| Return ||
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [UserPrincipal](../java/nio/file/attribute/UserPrincipal.md)! | A user principal representing the owner of the file |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the associated file system does not support the`FileOwnerAttributeView` |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, it denies [RuntimePermission](../java/lang/RuntimePermission.md)`("accessUserInformation")`or its [checkRead](../java/lang/SecurityManager.md))method denies read access to the file. |
| --- | --- |

### getPosixFilePermissions

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getPosixFilePermissions(
    path: Path!, 
    vararg options: LinkOption!
): MutableSet<PosixFilePermission!>!
```

Returns a file's POSIX file permissions.

The`path`parameter is associated with a`FileSystem`that supports the [PosixFileAttributeView](../java/nio/file/attribute/PosixFileAttributeView.md). This attribute view provides access to file attributes commonly associated with files on file systems used by operating systems that implement the Portable Operating System Interface (POSIX) family of standards.

The`options`array may be used to indicate how symbolic links are handled for the case that the file is a symbolic link. By default, symbolic links are followed and the file attribute of the final target of the link is read. If the option [NOFOLLOW_LINKS](../java/nio/file/LinkOption.md) is present then symbolic links are not followed.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |
| `options` | [LinkOption](../java/nio/file/LinkOption.md)!:options indicating how symbolic links are handled |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [PosixFilePermission](../java/nio/file/attribute/PosixFilePermission.md)!>! | the file permissions |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the associated file system does not support the`PosixFileAttributeView` |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, and it denies [RuntimePermission](../java/lang/RuntimePermission.md)`("accessUserInformation")`or its [checkRead](../java/lang/SecurityManager.md))method denies read access to the file. |
| --- | --- |

### isDirectory

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isDirectory(
    path: Path!, 
    vararg options: LinkOption!
): Boolean
```

Tests whether a file is a directory.

The`options`array may be used to indicate how symbolic links are handled for the case that the file is a symbolic link. By default, symbolic links are followed and the file attribute of the final target of the link is read. If the option [NOFOLLOW_LINKS](../java/nio/file/LinkOption.md) is present then symbolic links are not followed.

Where it is required to distinguish an I/O exception from the case that the file is not a directory then the file attributes can be read with the [readAttributes](../java/nio/file/Files.md))method and the file type tested with the [java.nio.file.attribute.BasicFileAttributes#isDirectory](../java/nio/file/attribute/BasicFileAttributes.md))method.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file to test |
| `options` | [LinkOption](../java/nio/file/LinkOption.md)!:options indicating how symbolic links are handled |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the file is a directory;`false`if the file does not exist, is not a directory, or it cannot be determined if the file is a directory or not. |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, its [checkRead](../java/lang/SecurityManager.md))method denies read access to the file. |

### isExecutable

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isExecutable(path: Path!): Boolean
```

Tests whether a file is executable. This method checks that a file exists and that this Java virtual machine has appropriate privileges to java.lang.Runtime#exec the file. The semantics may differ when checking access to a directory. For example, on UNIX systems, checking for execute access checks that the Java virtual machine has permission to search the directory in order to access file or subdirectories.

Depending on the implementation, this method may require to read file permissions, access control lists, or other file attributes in order to check the effective access to the file. Consequently, this method may not be atomic with respect to other file system operations.

Note that the result of this method is immediately outdated, there is no guarantee that a subsequent attempt to execute the file will succeed (or even that it will access the same file). Care should be taken when using this method in security sensitive applications.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file to check |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the file exists and is executable;`false`if the file does not exist, execute access would be denied because the Java virtual machine has insufficient privileges, or access cannot be determined |

| Exceptions ||
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkExec](../java/lang/SecurityManager.md))is invoked to check execute access to the file. |

### isHidden

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isHidden(path: Path!): Boolean
```

Tells whether or not a file is considered*hidden* . The exact definition of hidden is platform or provider dependent. On UNIX for example a file is considered to be hidden if its name begins with a period character ('.'). On Windows a file is considered hidden if it isn't a directory and the DOS [hidden](../java/nio/file/attribute/DosFileAttributes.md))attribute is set.

Depending on the implementation this method may require to access the file system to determine if the file is considered hidden.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file to test |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the file is considered hidden |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the file. |

### isReadable

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isReadable(path: Path!): Boolean
```

Tests whether a file is readable. This method checks that a file exists and that this Java virtual machine has appropriate privileges that would allow it open the file for reading. Depending on the implementation, this method may require to read file permissions, access control lists, or other file attributes in order to check the effective access to the file. Consequently, this method may not be atomic with respect to other file system operations.

Note that the result of this method is immediately outdated, there is no guarantee that a subsequent attempt to open the file for reading will succeed (or even that it will access the same file). Care should be taken when using this method in security sensitive applications.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file to check |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the file exists and is readable;`false`if the file does not exist, read access would be denied because the Java virtual machine has insufficient privileges, or access cannot be determined |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))is invoked to check read access to the file. |

### isRegularFile

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isRegularFile(
    path: Path!, 
    vararg options: LinkOption!
): Boolean
```

Tests whether a file is a regular file with opaque content.

The`options`array may be used to indicate how symbolic links are handled for the case that the file is a symbolic link. By default, symbolic links are followed and the file attribute of the final target of the link is read. If the option [NOFOLLOW_LINKS](../java/nio/file/LinkOption.md) is present then symbolic links are not followed.

Where it is required to distinguish an I/O exception from the case that the file is not a regular file then the file attributes can be read with the [readAttributes](../java/nio/file/Files.md))method and the file type tested with the [java.nio.file.attribute.BasicFileAttributes#isRegularFile](../java/nio/file/attribute/BasicFileAttributes.md))method.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |
| `options` | [LinkOption](../java/nio/file/LinkOption.md)!:options indicating how symbolic links are handled |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the file is a regular file;`false`if the file does not exist, is not a regular file, or it cannot be determined if the file is a regular file or not. |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, its [checkRead](../java/lang/SecurityManager.md))method denies read access to the file. |

### isSameFile

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isSameFile(
    path: Path!, 
    path2: Path!
): Boolean
```

Tests if two paths locate the same file.

If both`Path`objects are [equal](../java/nio/file/Files.md) then this method returns`true`without checking if the file exists. If the two`Path`objects are associated with different providers then this method returns`false`. Otherwise, this method checks if both`Path`objects locate the same file, and depending on the implementation, may require to open or access both files.

If the file system and files remain static, then this method implements an equivalence relation for non-null`Paths`.

- It is*reflexive* : for`Path``f`,`isSameFile(f,f)`should return`true`.
- It is*symmetric* : for two`Paths``f`and`g`,`isSameFile(f,g)`will equal`isSameFile(g,f)`.
- It is*transitive* : for three`Paths``f`,`g`, and`h`, if`isSameFile(f,g)`returns`true`and`isSameFile(g,h)`returns`true`, then`isSameFile(f,h)`will return`true`.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:one path to the file |
| `path2` | [Path](../java/nio/file/Path.md)!:the other path |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, the two paths locate the same file |

| Exceptions ||
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to both files. |

**See Also**

- [java.nio.file.attribute.BasicFileAttributes#fileKey](../java/nio/file/attribute/BasicFileAttributes.md)) 

### isSymbolicLink

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isSymbolicLink(path: Path!): Boolean
```

Tests whether a file is a symbolic link.

Where it is required to distinguish an I/O exception from the case that the file is not a symbolic link then the file attributes can be read with the [readAttributes](../java/nio/file/Files.md))method and the file type tested with the [java.nio.file.attribute.BasicFileAttributes#isSymbolicLink](../java/nio/file/attribute/BasicFileAttributes.md))method.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:The path to the file |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the file is a symbolic link;`false`if the file does not exist, is not a symbolic link, or it cannot be determined if the file is a symbolic link or not. |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, its [checkRead](../java/lang/SecurityManager.md))method denies read access to the file. |

### isWritable

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isWritable(path: Path!): Boolean
```

Tests whether a file is writable. This method checks that a file exists and that this Java virtual machine has appropriate privileges that would allow it open the file for writing. Depending on the implementation, this method may require to read file permissions, access control lists, or other file attributes in order to check the effective access to the file. Consequently, this method may not be atomic with respect to other file system operations.

Note that result of this method is immediately outdated, there is no guarantee that a subsequent attempt to open the file for writing will succeed (or even that it will access the same file). Care should be taken when using this method in security sensitive applications.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file to check |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the file exists and is writable;`false`if the file does not exist, write access would be denied because the Java virtual machine has insufficient privileges, or access cannot be determined |

| Exceptions ||
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkWrite](../java/lang/SecurityManager.md))is invoked to check write access to the file. |

### lines

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun lines(path: Path!): Stream<String!>!
```

Read all lines from a file as a`Stream`. Bytes from the file are decoded into characters using the [UTF-8](../java/nio/charset/StandardCharsets.md) [charset](../java/nio/charset/Charset.md).

The returned stream contains a reference to an open file. The file is closed by closing the stream.

The file contents should not be modified during the execution of the terminal stream operation. Otherwise, the result of the terminal stream operation is undefined.

This method works as if invoking it were equivalent to evaluating the expression: 

```kotlin
<code>Files.lines(path, StandardCharsets.UTF_8)
  </code>
```

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Stream](../java/util/stream/Stream.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the lines from the file as a`Stream` |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs opening the file |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the file. |

### lines

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun lines(
    path: Path!, 
    cs: Charset!
): Stream<String!>!
```

Read all lines from a file as a`Stream`. Unlike [readAllLines](../java/nio/file/Files.md)), this method does not read all lines into a`List`, but instead populates lazily as the stream is consumed.

Bytes from the file are decoded into characters using the specified charset and the same line terminators as specified by`readAllLines`are supported.

The returned stream contains a reference to an open file. The file is closed by closing the stream.

The file contents should not be modified during the execution of the terminal stream operation. Otherwise, the result of the terminal stream operation is undefined.

After this method returns, then any subsequent I/O exception that occurs while reading from the file or when a malformed or unmappable byte sequence is read, is wrapped in an [UncheckedIOException](../java/io/UncheckedIOException.md) that will be thrown from the [java.util.stream.Stream](../java/util/stream/Stream.md) method that caused the read to take place. In case an`IOException`is thrown when closing the file, it is also wrapped as an`UncheckedIOException`.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |
| `cs` | [Charset](../java/nio/charset/Charset.md)!:the charset to use for decoding |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Stream](../java/util/stream/Stream.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the lines from the file as a`Stream` |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs opening the file |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the file. |

**See Also**

- [#readAllLines(Path, Charset)](../java/nio/file/Files.md))
- [#newBufferedReader(Path, Charset)](../java/nio/file/Files.md))
- [java.io.BufferedReader#lines()](../java/io/BufferedReader.md)) 

### list

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun list(dir: Path!): Stream<Path!>!
```

Return a lazily populated`Stream`, the elements of which are the entries in the directory. The listing is not recursive.

The elements of the stream are [Path](../java/nio/file/Path.md) objects that are obtained as if by [resolving](../java/nio/file/Path.md))the name of the directory entry against`dir`. Some file systems maintain special links to the directory itself and the directory's parent directory. Entries representing these links are not included.

The stream is*weakly consistent*. It is thread safe but does not freeze the directory while iterating, so it may (or may not) reflect updates to the directory that occur after returning from this method.

The returned stream contains a reference to an open directory. The directory is closed by closing the stream.

Operating on a closed stream behaves as if the end of stream has been reached. Due to read-ahead, one or more elements may be returned after the stream has been closed.

If an [IOException](../java/io/IOException.md) is thrown when accessing the directory after this method has returned, it is wrapped in an [UncheckedIOException](../java/io/UncheckedIOException.md) which will be thrown from the method that caused the access to take place.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `dir` | [Path](../java/nio/file/Path.md)!:The path to the directory |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [Stream](../java/util/stream/Stream.md)< [Path](../java/nio/file/Path.md)!>! | The`Stream`describing the content of the directory |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.file.NotDirectoryException` | if the file could not otherwise be opened because it is not a directory*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs when opening the directory |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the directory. |
| --- | --- |

**See Also**

- [#newDirectoryStream(Path)](../java/nio/file/Files.md)) 

### move

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun move(
    source: Path!, 
    target: Path!, 
    vararg options: CopyOption!
): Path!
```

Move or rename a file to a target file.

By default, this method attempts to move the file to the target file, failing if the target file exists except if the source and target are the [same](../java/nio/file/Files.md))file, in which case this method has no effect. If the file is a symbolic link then the symbolic link itself, not the target of the link, is moved. This method may be invoked to move an empty directory. In some implementations a directory has entries for special files or links that are created when the directory is created. In such implementations a directory is considered empty when only the special entries exist. When invoked to move a directory that is not empty then the directory is moved if it does not require moving the entries in the directory. For example, renaming a directory on the same [FileStore](../java/nio/file/FileStore.md) will usually not require moving the entries in the directory. When moving a directory requires that its entries be moved then this method fails (by throwing an`IOException`). To move a*file tree*may involve copying rather than moving directories and this can be done using the #copy method in conjunction with the #walkFileTree utility method.

The`options`parameter may include any of the following:

| Option | Description |
| --- | --- |
| [REPLACE_EXISTING](../java/nio/file/StandardCopyOption.md) | If the target file exists, then the target file is replaced if it is not a non-empty directory. If the target file exists and is a symbolic link, then the symbolic link itself, not the target of the link, is replaced. |
| [ATOMIC_MOVE](../java/nio/file/StandardCopyOption.md) | The move is performed as an atomic file system operation and all other options are ignored. If the target file exists then it is implementation specific if the existing file is replaced or this method fails by throwing an [IOException](../java/io/IOException.md). If the move cannot be performed as an atomic file system operation then [AtomicMoveNotSupportedException](../java/nio/file/AtomicMoveNotSupportedException.md) is thrown. This can arise, for example, when the target location is on a different`FileStore`and would require that the file be copied, or target location is associated with a different provider to this object. |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

An implementation of this interface may support additional implementation specific options.

Moving a file will copy the [last-modified-time](../java/nio/file/attribute/BasicFileAttributes.md))to the target file if supported by both source and target file stores. Copying of file timestamps may result in precision loss. An implementation may also attempt to copy other file attributes but is not required to fail if the file attributes cannot be copied. When the move is performed as a non-atomic operation, and an`IOException`is thrown, then the state of the files is not defined. The original file and the target file may both exist, the target file may be incomplete or some of its file attributes may not been copied from the original file.

**Usage Examples:**Suppose we want to rename a file to "newname", keeping the file in the same directory: 

```kotlin
Path source = ...
      Files.move(source, source.resolveSibling("newname"));
  
```
Alternatively, suppose we want to move a file to new directory, keeping the same file name, and replacing any existing file of that name in the directory: 

```kotlin
Path source = ...
      Path newdir = ...
      Files.move(source, newdir.resolve(source.getFileName()), REPLACE_EXISTING);
  
```

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Path](../java/nio/file/Path.md)!:the path to the file to move |
| `target` | [Path](../java/nio/file/Path.md)!:the path to the target file (may be associated with a different provider to the source path) |
| `options` | [CopyOption](../java/nio/file/CopyOption.md)!:options specifying how the move should be done |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Path](../java/nio/file/Path.md)! | the path to the target file |

| Exceptions ||
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the array contains a copy option that is not supported |
| `java.nio.file.FileAlreadyExistsException` | if the target file exists but cannot be replaced because the`REPLACE_EXISTING`option is not specified*(optional specific exception)* |
| `java.nio.file.DirectoryNotEmptyException` | the`REPLACE_EXISTING`option is specified but the file cannot be replaced because it is a non-empty directory, or the source is a non-empty directory containing entries that would be required to be moved*(optional specific exceptions)* |
| --- | --- |
| `java.nio.file.AtomicMoveNotSupportedException` | if the options array contains the`ATOMIC_MOVE`option but the file cannot be moved as an atomic file system operation. |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access to both the source and target file. |
| --- | --- |

### newBufferedReader

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newBufferedReader(path: Path!): BufferedReader!
```

Opens a file for reading, returning a`BufferedReader`to read text from the file in an efficient manner. Bytes from the file are decoded into characters using the [UTF-8](../java/nio/charset/StandardCharsets.md) [charset](../java/nio/charset/Charset.md).

This method works as if invoking it were equivalent to evaluating the expression: 

```kotlin
<code>Files.newBufferedReader(path, StandardCharsets.UTF_8)
  </code>
```

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [BufferedReader](../java/io/BufferedReader.md)! | a new buffered reader, with default buffer size, to read text from the file |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs opening the file |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the file. |

### newBufferedReader

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newBufferedReader(
    path: Path!, 
    cs: Charset!
): BufferedReader!
```

Opens a file for reading, returning a`BufferedReader`that may be used to read text from the file in an efficient manner. Bytes from the file are decoded into characters using the specified charset. Reading commences at the beginning of the file.

The`Reader`methods that read from the file throw`IOException`if a malformed or unmappable byte sequence is read.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |
| `cs` | [Charset](../java/nio/charset/Charset.md)!:the charset to use for decoding |

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [BufferedReader](../java/io/BufferedReader.md)! | a new buffered reader, with default buffer size, to read text from the file |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs opening the file |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the file. |

**See Also**

### newBufferedWriter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newBufferedWriter(
    path: Path!, 
    cs: Charset!, 
    vararg options: OpenOption!
): BufferedWriter!
```

Opens or creates a file for writing, returning a`BufferedWriter`that may be used to write text to the file in an efficient manner. The`options`parameter specifies how the file is created or opened. If no options are present then this method works as if the [CREATE](../java/nio/file/StandardOpenOption.md), [TRUNCATE_EXISTING](../java/nio/file/StandardOpenOption.md), and [WRITE](../java/nio/file/StandardOpenOption.md) options are present. In other words, it opens the file for writing, creating the file if it doesn't exist, or initially truncating an existing [regular-file](../java/nio/file/Files.md))to a size of`0`if it exists.

The`Writer`methods to write text throw`IOException`if the text cannot be encoded using the specified charset.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |
| `cs` | [Charset](../java/nio/charset/Charset.md)!:the charset to use for encoding |
| `options` | [OpenOption](../java/nio/file/OpenOption.md)!:options specifying how the file is opened |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [BufferedWriter](../java/io/BufferedWriter.md)! | a new buffered writer, with default buffer size, to write text to the file |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`options`contains an invalid combination of options |
| `java.io.IOException` | if an I/O error occurs opening or creating the file |
| `java.lang.UnsupportedOperationException` | if an unsupported option is specified |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access to the file. The [checkDelete](../java/lang/SecurityManager.md))method is invoked to check delete access if the file is opened with the`DELETE_ON_CLOSE`option. |

**See Also**

- [#write(Path,Iterable,Charset,OpenOption[])](https://developer.android.com/reference/kotlin/java/nio/file/Files#write(java.nio.file.Path,%20kotlin.collections.MutableIterable,%20java.nio.charset.Charset,%20java.nio.file.OpenOption)) 

### newBufferedWriter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newBufferedWriter(
    path: Path!, 
    vararg options: OpenOption!
): BufferedWriter!
```

Opens or creates a file for writing, returning a`BufferedWriter`to write text to the file in an efficient manner. The text is encoded into bytes for writing using the [UTF-8](../java/nio/charset/StandardCharsets.md) [charset](../java/nio/charset/Charset.md).

This method works as if invoking it were equivalent to evaluating the expression: 

```kotlin
<code>Files.newBufferedWriter(path, StandardCharsets.UTF_8, options)
  </code>
```

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |
| `options` | [OpenOption](../java/nio/file/OpenOption.md)!:options specifying how the file is opened |

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [BufferedWriter](../java/io/BufferedWriter.md)! | a new buffered writer, with default buffer size, to write text to the file |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`options`contains an invalid combination of options |
| `java.io.IOException` | if an I/O error occurs opening or creating the file |
| `java.lang.UnsupportedOperationException` | if an unsupported option is specified |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access to the file. The [checkDelete](../java/lang/SecurityManager.md))method is invoked to check delete access if the file is opened with the`DELETE_ON_CLOSE`option. |

### newByteChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newByteChannel(
    path: Path!, 
    vararg options: OpenOption!
): SeekableByteChannel!
```

Opens or creates a file, returning a seekable byte channel to access the file.

This method opens or creates a file in exactly the manner specified by the [newByteChannel](../java/nio/file/Files.md))method.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file to open or create |
| `options` | [OpenOption](../java/nio/file/OpenOption.md)!:options specifying how the file is opened |

| Return ||
|--------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [SeekableByteChannel](../java/nio/channels/SeekableByteChannel.md)! | a new seekable byte channel |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the set contains an invalid combination of options |
| `java.lang.UnsupportedOperationException` | if an unsupported open option is specified |
| `java.nio.file.FileAlreadyExistsException` | if a file of that name already exists and the [CREATE_NEW](../java/nio/file/StandardOpenOption.md) option is specified*(optional specific exception)* |
| --- | --- |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the path if the file is opened for reading. The [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access to the path if the file is opened for writing. The [checkDelete](../java/lang/SecurityManager.md))method is invoked to check delete access if the file is opened with the`DELETE_ON_CLOSE`option. |

**See Also**

- [java.nio.channels.FileChannel#open(Path,OpenOption[])](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.html#open(java.nio.file.Path,%20java.nio.file.OpenOption)) 

### newByteChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newByteChannel(
    path: Path!, 
    options: MutableSet<out OpenOption!>!, 
    vararg attrs: FileAttribute<*>!
): SeekableByteChannel!
```

Opens or creates a file, returning a seekable byte channel to access the file.

The`options`parameter determines how the file is opened. The [READ](../java/nio/file/StandardOpenOption.md) and [WRITE](../java/nio/file/StandardOpenOption.md) options determine if the file should be opened for reading and/or writing. If neither option (or the [APPEND](../java/nio/file/StandardOpenOption.md) option) is present then the file is opened for reading. By default reading or writing commence at the beginning of the file.

In the addition to`READ`and`WRITE`, the following options may be present:

| Option | Description |
| --- | --- |
| [APPEND](../java/nio/file/StandardOpenOption.md) | If this option is present then the file is opened for writing and each invocation of the channel's`write`method first advances the position to the end of the file and then writes the requested data. Whether the advancement of the position and the writing of the data are done in a single atomic operation is system-dependent and therefore unspecified. This option may not be used in conjunction with the`READ`or`TRUNCATE_EXISTING`options. |
| [TRUNCATE_EXISTING](../java/nio/file/StandardOpenOption.md) | If this option is present then the existing file is truncated to a size of 0 bytes. This option is ignored when the file is opened only for reading. |
| [CREATE_NEW](../java/nio/file/StandardOpenOption.md) | If this option is present then a new file is created, failing if the file already exists or is a symbolic link. When creating a file the check for the existence of the file and the creation of the file if it does not exist is atomic with respect to other file system operations. This option is ignored when the file is opened only for reading. |
| --- | --- |
| [CREATE](../java/nio/file/StandardOpenOption.md) | If this option is present then an existing file is opened if it exists, otherwise a new file is created. This option is ignored if the`CREATE_NEW`option is also present or the file is opened only for reading. |
| [DELETE_ON_CLOSE](../java/nio/file/StandardOpenOption.md) | When this option is present then the implementation makes a*best effort* attempt to delete the file when closed by the java.nio.channels.SeekableByteChannel#close method. If the`close`method is not invoked then a*best effort*attempt is made to delete the file when the Java virtual machine terminates. |
| [SPARSE](../java/nio/file/StandardOpenOption.md) | When creating a new file this option is a*hint*that the new file will be sparse. This option is ignored when not creating a new file. |
| --- | --- |
| [SYNC](../java/nio/file/StandardOpenOption.md) | Requires that every update to the file's content or metadata be written synchronously to the underlying storage device. (see [Synchronized I/O file integrity](../java/nio/file/_package.md)). |
| [DSYNC](../java/nio/file/StandardOpenOption.md) | Requires that every update to the file's content be written synchronously to the underlying storage device. (see [Synchronized I/O file integrity](../java/nio/file/_package.md)). |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

An implementation may also support additional implementation specific options.

The`attrs`parameter is optional [file-attributes](../java/nio/file/attribute/FileAttribute.md) to set atomically when a new file is created.

In the case of the default provider, the returned seekable byte channel is a [java.nio.channels.FileChannel](../java/nio/channels/FileChannel.md).

**Usage Examples:** 

```kotlin
<code>Path path = ...
 
      // open file for reading
      ReadableByteChannel rbc = Files.newByteChannel(path, EnumSet.of(READ)));
 
      // open file for writing to the end of an existing file, creating
      // the file if it doesn't already exist
      WritableByteChannel wbc = Files.newByteChannel(path, EnumSet.of(CREATE,APPEND));
 
      // create file with initial permissions, opening it for both reading and writing
      FileAttribute&lt;Set&lt;PosixFilePermission&gt;&gt; perms = ...
      SeekableByteChannel sbc =
          Files.newByteChannel(path, EnumSet.of(CREATE_NEW,READ,WRITE), perms);
  </code>
```

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file to open or create |
| `options` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<out [OpenOption](../java/nio/file/OpenOption.md)!\>!:options specifying how the file is opened |
| `attrs` | [FileAttribute](../java/nio/file/attribute/FileAttribute.md)\<\*\>!:an optional list of file attributes to set atomically when creating the file |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [SeekableByteChannel](../java/nio/channels/SeekableByteChannel.md)! | a new seekable byte channel |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the set contains an invalid combination of options |
| `java.lang.UnsupportedOperationException` | if an unsupported open option is specified or the array contains attributes that cannot be set atomically when creating the file |
| `java.nio.file.FileAlreadyExistsException` | if a file of that name already exists and the [CREATE_NEW](../java/nio/file/StandardOpenOption.md) option is specified*(optional specific exception)* |
| --- | --- |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the path if the file is opened for reading. The [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access to the path if the file is opened for writing. The [checkDelete](../java/lang/SecurityManager.md))method is invoked to check delete access if the file is opened with the`DELETE_ON_CLOSE`option. |

**See Also**

- [java.nio.channels.FileChannel#open(Path,Set,FileAttribute[])](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.html#open(java.nio.file.Path,%20kotlin.collections.MutableSet,%20java.nio.file.attribute.FileAttribute)) 

### newDirectoryStream

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newDirectoryStream(dir: Path!): DirectoryStream<Path!>!
```

Opens a directory, returning a [DirectoryStream](../java/nio/file/DirectoryStream.md) to iterate over all entries in the directory. The elements returned by the directory stream's [iterator](../java/nio/file/DirectoryStream.md))are of type`Path`, each one representing an entry in the directory. The`Path`objects are obtained as if by [resolving](../java/nio/file/Path.md))the name of the directory entry against`dir`.

When not using the try-with-resources construct, then directory stream's`close`method should be invoked after iteration is completed so as to free any resources held for the open directory.

When an implementation supports operations on entries in the directory that execute in a race-free manner then the returned directory stream is a [SecureDirectoryStream](../java/nio/file/SecureDirectoryStream.md).

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `dir` | [Path](../java/nio/file/Path.md)!:the path to the directory |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [DirectoryStream](../java/nio/file/DirectoryStream.md)< [Path](../java/nio/file/Path.md)!>! | a new and open`DirectoryStream`object |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.file.NotDirectoryException` | if the file could not otherwise be opened because it is not a directory*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the directory. |
| --- | --- |

### newDirectoryStream

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newDirectoryStream(
    dir: Path!, 
    glob: String!
): DirectoryStream<Path!>!
```

Opens a directory, returning a [DirectoryStream](../java/nio/file/DirectoryStream.md) to iterate over the entries in the directory. The elements returned by the directory stream's [iterator](../java/nio/file/DirectoryStream.md))are of type`Path`, each one representing an entry in the directory. The`Path`objects are obtained as if by [resolving](../java/nio/file/Path.md))the name of the directory entry against`dir`. The entries returned by the iterator are filtered by matching the`String`representation of their file names against the given*globbing*pattern.

For example, suppose we want to iterate over the files ending with ".java" in a directory: 

```kotlin
Path dir = ...
      try (DirectoryStream<Path> stream = Files.newDirectoryStream(dir, "*.java")) {
          :
      }
  
```

The globbing pattern is specified by the [getPathMatcher](../java/nio/file/FileSystem.md))method.

When not using the try-with-resources construct, then directory stream's`close`method should be invoked after iteration is completed so as to free any resources held for the open directory.

When an implementation supports operations on entries in the directory that execute in a race-free manner then the returned directory stream is a [SecureDirectoryStream](../java/nio/file/SecureDirectoryStream.md).

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------|
| `dir` | [Path](../java/nio/file/Path.md)!:the path to the directory |
| `glob` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the glob pattern |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [DirectoryStream](../java/nio/file/DirectoryStream.md)< [Path](../java/nio/file/Path.md)!>! | a new and open`DirectoryStream`object |

| Exceptions ||
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.regex.PatternSyntaxException` | if the pattern is invalid |
| `java.nio.file.NotDirectoryException` | if the file could not otherwise be opened because it is not a directory*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the directory. |

### newDirectoryStream

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newDirectoryStream(
    dir: Path!, 
    filter: DirectoryStream.Filter<in Path!>!
): DirectoryStream<Path!>!
```

Opens a directory, returning a [DirectoryStream](../java/nio/file/DirectoryStream.md) to iterate over the entries in the directory. The elements returned by the directory stream's [iterator](../java/nio/file/DirectoryStream.md))are of type`Path`, each one representing an entry in the directory. The`Path`objects are obtained as if by [resolving](../java/nio/file/Path.md))the name of the directory entry against`dir`. The entries returned by the iterator are filtered by the given [filter](../java/nio/file/DirectoryStream.Filter.md).

When not using the try-with-resources construct, then directory stream's`close`method should be invoked after iteration is completed so as to free any resources held for the open directory.

Where the filter terminates due to an uncaught error or runtime exception then it is propagated to the [hasNext](../java/util/Iterator.md))or [next](../java/util/Iterator.md))method. Where an`IOException`is thrown, it results in the`hasNext`or`next`method throwing a [DirectoryIteratorException](../java/nio/file/DirectoryIteratorException.md) with the`IOException`as the cause.

When an implementation supports operations on entries in the directory that execute in a race-free manner then the returned directory stream is a [SecureDirectoryStream](../java/nio/file/SecureDirectoryStream.md).

**Usage Example:**Suppose we want to iterate over the files in a directory that are larger than 8K. 

```kotlin
DirectoryStream.Filter<Path> filter = new DirectoryStream.Filter<Path>() {
          public boolean accept(Path file) throws IOException {
              return (Files.size(file) > 8192L);
          }
      };
      Path dir = ...
      try (DirectoryStream<Path> stream = Files.newDirectoryStream(dir, filter)) {
          :
      }
  
```

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dir` | [Path](../java/nio/file/Path.md)!:the path to the directory |
| `filter` | [DirectoryStream.Filter](../java/nio/file/DirectoryStream.Filter.md)\<in [Path](../java/nio/file/Path.md)!\>!:the directory stream filter |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [DirectoryStream](../java/nio/file/DirectoryStream.md)< [Path](../java/nio/file/Path.md)!>! | a new and open`DirectoryStream`object |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.file.NotDirectoryException` | if the file could not otherwise be opened because it is not a directory*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the directory. |
| --- | --- |

### newInputStream

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newInputStream(
    path: Path!, 
    vararg options: OpenOption!
): InputStream!
```

Opens a file, returning an input stream to read from the file. The stream will not be buffered, and is not required to support the [mark](../java/io/InputStream.md))or [reset](../java/io/InputStream.md))methods. The stream will be safe for access by multiple concurrent threads. Reading commences at the beginning of the file. Whether the returned stream is*asynchronously closeable* and/or*interruptible*is highly file system provider specific and therefore not specified.

The`options`parameter determines how the file is opened. If no options are present then it is equivalent to opening the file with the [READ](../java/nio/file/StandardOpenOption.md) option. In addition to the`READ`option, an implementation may also support additional implementation specific options.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file to open |
| `options` | [OpenOption](../java/nio/file/OpenOption.md)!:options specifying how the file is opened |

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [InputStream](../java/io/InputStream.md)! | a new input stream |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if an invalid combination of options is specified |
| `java.lang.UnsupportedOperationException` | if an unsupported option is specified |
| `java.io.IOException` | if an I/O error occurs |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the file. |

### newOutputStream

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newOutputStream(
    path: Path!, 
    vararg options: OpenOption!
): OutputStream!
```

Opens or creates a file, returning an output stream that may be used to write bytes to the file. The resulting stream will not be buffered. The stream will be safe for access by multiple concurrent threads. Whether the returned stream is*asynchronously closeable* and/or*interruptible*is highly file system provider specific and therefore not specified.

This method opens or creates a file in exactly the manner specified by the [newByteChannel](../java/nio/file/Files.md))method with the exception that the [READ](../java/nio/file/StandardOpenOption.md) option may not be present in the array of options. If no options are present then this method works as if the [CREATE](../java/nio/file/StandardOpenOption.md), [TRUNCATE_EXISTING](../java/nio/file/StandardOpenOption.md), and [WRITE](../java/nio/file/StandardOpenOption.md) options are present. In other words, it opens the file for writing, creating the file if it doesn't exist, or initially truncating an existing [regular-file](../java/nio/file/Files.md))to a size of`0`if it exists.

**Usage Examples:** 

```kotlin
Path path = ...
 
      // truncate and overwrite an existing file, or create the file if
      // it doesn't initially exist
      OutputStream out = Files.newOutputStream(path);
 
      // append to an existing file, fail if the file does not exist
      out = Files.newOutputStream(path, APPEND);
 
      // append to an existing file, create file if it doesn't initially exist
      out = Files.newOutputStream(path, CREATE, APPEND);
 
      // always create new file, failing if it already exists
      out = Files.newOutputStream(path, CREATE_NEW);
  
```

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file to open or create |
| `options` | [OpenOption](../java/nio/file/OpenOption.md)!:options specifying how the file is opened |

| Return ||
|--------------------------------------------------------------------------------------------|---------------------|
| [OutputStream](../java/io/OutputStream.md)! | a new output stream |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`options`contains an invalid combination of options |
| `java.lang.UnsupportedOperationException` | if an unsupported option is specified |
| `java.io.IOException` | if an I/O error occurs |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access to the file. The [checkDelete](../java/lang/SecurityManager.md))method is invoked to check delete access if the file is opened with the`DELETE_ON_CLOSE`option. |

### notExists

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun notExists(
    path: Path!, 
    vararg options: LinkOption!
): Boolean
```

Tests whether the file located by this path does not exist. This method is intended for cases where it is required to take action when it can be confirmed that a file does not exist.

The`options`parameter may be used to indicate how symbolic links are handled for the case that the file is a symbolic link. By default, symbolic links are followed. If the option [NOFOLLOW_LINKS](../java/nio/file/LinkOption.md) is present then symbolic links are not followed.

Note that this method is not the complement of the [exists](../java/nio/file/Files.md))method. Where it is not possible to determine if a file exists or not then both methods return`false`. As with the`exists`method, the result of this method is immediately outdated. If this method indicates the file does exist then there is no guarantee that a subsequent attempt to create the file will succeed. Care should be taken when using this method in security sensitive applications.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file to test |
| `options` | [LinkOption](../java/nio/file/LinkOption.md)!:options indicating how symbolic links are handled |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the file does not exist;`false`if the file exists or its existence cannot be determined |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | In the case of the default provider, the [java.lang.SecurityManager#checkRead(java.lang.String)](../java/lang/SecurityManager.md))is invoked to check read access to the file. |

### probeContentType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun probeContentType(path: Path!): String!
```

Probes the content type of a file.

This method uses the installed [FileTypeDetector](../java/nio/file/spi/FileTypeDetector.md) implementations to probe the given file to determine its content type. Each file type detector's [probeContentType](../java/nio/file/spi/FileTypeDetector.md))is invoked, in turn, to probe the file type. If the file is recognized then the content type is returned. If the file is not recognized by any of the installed file type detectors then a system-default file type detector is invoked to guess the content type.

A given invocation of the Java virtual machine maintains a system-wide list of file type detectors. Installed file type detectors are loaded using the service-provider loading facility defined by the [ServiceLoader](../java/util/ServiceLoader.md) class. Installed file type detectors are loaded using the system class loader. If the system class loader cannot be found then the platform class loader is used. File type detectors are typically installed by placing them in a JAR file on the application class path, the JAR file contains a provider-configuration file named`java.nio.file.spi.FileTypeDetector`in the resource directory`META-INF/services`, and the file lists one or more fully-qualified names of concrete subclass of`FileTypeDetector `that have a zero argument constructor. If the process of locating or instantiating the installed file type detectors fails then an unspecified error is thrown. The ordering that installed providers are located is implementation specific.

The return value of this method is the string form of the value of a Multipurpose Internet Mail Extension (MIME) content type as defined by [*RFC 2045: Multipurpose Internet Mail Extensions (MIME) Part One: Format of Internet Message Bodies*](http://www.ietf.org/rfc/rfc2045.txt). The string is guaranteed to be parsable according to the grammar in the RFC.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file to probe |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The content type of the file, or`null`if the content type cannot be determined |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | If a security manager is installed and it denies an unspecified permission required by a file type detector implementation. |

### readAllBytes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun readAllBytes(path: Path!): ByteArray!
```

Reads all the bytes from a file. The method ensures that the file is closed when all bytes have been read or an I/O error, or other runtime exception, is thrown.

Note that this method is intended for simple cases where it is convenient to read all bytes into a byte array. It is not intended for reading in large files.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | a byte array containing the bytes read from the file |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs reading from the stream |
| `java.lang.OutOfMemoryError` | if an array of the required size cannot be allocated, for example the file is larger that`2GB` |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the file. |
| --- | --- |

### readAllLines

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun readAllLines(path: Path!): MutableList<String!>!
```

Read all lines from a file. Bytes from the file are decoded into characters using the [UTF-8](../java/nio/charset/StandardCharsets.md) [charset](../java/nio/charset/Charset.md).

This method works as if invoking it were equivalent to evaluating the expression: 

```kotlin
<code>Files.readAllLines(path, StandardCharsets.UTF_8)
  </code>
```

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the lines from the file as a`List`; whether the`List`is modifiable or not is implementation dependent and therefore not specified |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs reading from the file or a malformed or unmappable byte sequence is read |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the file. |

### readAllLines

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun readAllLines(
    path: Path!, 
    cs: Charset!
): MutableList<String!>!
```

Read all lines from a file. This method ensures that the file is closed when all bytes have been read or an I/O error, or other runtime exception, is thrown. Bytes from the file are decoded into characters using the specified charset.

This method recognizes the following as line terminators:

- `\u000D`followed by`\u000A`, CARRIAGE RETURN followed by LINE FEED
- `\u000A`, LINE FEED
- `\u000D`, CARRIAGE RETURN

Additional Unicode line terminators may be recognized in future releases.

Note that this method is intended for simple cases where it is convenient to read all lines in a single operation. It is not intended for reading in large files.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |
| `cs` | [Charset](../java/nio/charset/Charset.md)!:the charset to use for decoding |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the lines from the file as a`List`; whether the`List`is modifiable or not is implementation dependent and therefore not specified |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs reading from the file or a malformed or unmappable byte sequence is read |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the file. |

**See Also**

### readAttributes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <A : BasicFileAttributes!> readAttributes(
    path: Path!, 
    type: Class<A>!, 
    vararg options: LinkOption!
): A
```

Reads a file's attributes as a bulk operation.

The`type`parameter is the type of the attributes required and this method returns an instance of that type if supported. All implementations support a basic set of file attributes and so invoking this method with a`type`parameter of`BasicFileAttributes.class`will not throw`UnsupportedOperationException`.

The`options`array may be used to indicate how symbolic links are handled for the case that the file is a symbolic link. By default, symbolic links are followed and the file attribute of the final target of the link is read. If the option [NOFOLLOW_LINKS](../java/nio/file/LinkOption.md) is present then symbolic links are not followed.

It is implementation specific if all file attributes are read as an atomic operation with respect to other file system operations.

**Usage Example:**Suppose we want to read a file's attributes in bulk: 

```kotlin
Path path = ...
     BasicFileAttributes attrs = Files.readAttributes(path, BasicFileAttributes.class);
  
```
Alternatively, suppose we want to read file's POSIX attributes without following symbolic links: 

```kotlin
PosixFileAttributes attrs =
         Files.readAttributes(path, PosixFileAttributes.class, NOFOLLOW_LINKS);
  
```

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------|
| `<A>` | The`BasicFileAttributes`type |
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |
| `type` | [Class](../java/lang/Class.md)\<A\>!:the`Class`of the file attributes required to read |
| --- | --- |
| `options` | [LinkOption](../java/nio/file/LinkOption.md)!:options indicating how symbolic links are handled |

| Return ||
|---|---------------------|
| A | the file attributes |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if an attributes of the given type are not supported |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, its [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the file. If this method is invoked to read security sensitive attributes then the security manager may be invoke to check for additional permissions. |
| --- | --- |

### readAttributes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun readAttributes(
    path: Path!, 
    attributes: String!, 
    vararg options: LinkOption!
): MutableMap<String!, Any!>!
```

Reads a set of file attributes as a bulk operation.

The`attributes`parameter identifies the attributes to be read and takes the form:
\[*view-name* **:** \]*attribute-list* where square brackets \[...\] delineate an optional component and the character`':'`stands for itself.

*view-name* is the [name](../java/nio/file/attribute/AttributeView.md))of a [FileAttributeView](../java/nio/file/attribute/FileAttributeView.md) that identifies a set of file attributes. If not specified then it defaults to`"basic"`, the name of the file attribute view that identifies the basic set of file attributes common to many file systems.

The*attribute-list* component is a comma separated list of one or more names of attributes to read. If the list contains the value`"*"`then all attributes are read. Attributes that are not supported are ignored and will not be present in the returned map. It is implementation specific if all attributes are read as an atomic operation with respect to other file system operations.

The following examples demonstrate possible values for the`attributes`parameter:

| Example | Description |
| --- | --- |
| `"*"` | Read all [basic-file-attributes](../java/nio/file/attribute/BasicFileAttributes.md). |
| `"size,lastModifiedTime,lastAccessTime"` | Reads the file size, last modified time, and last access time attributes. |
| `"posix:*"` | Read all [POSIX-file-attributes](../java/nio/file/attribute/PosixFileAttributes.md). |
| --- | --- |
| `"posix:permissions,owner,size"` | Reads the POSIX file permissions, owner, and file size. |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|

The`options`array may be used to indicate how symbolic links are handled for the case that the file is a symbolic link. By default, symbolic links are followed and the file attribute of the final target of the link is read. If the option [NOFOLLOW_LINKS](../java/nio/file/LinkOption.md) is present then symbolic links are not followed.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |
| `attributes` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the attributes to read |
| `options` | [LinkOption](../java/nio/file/LinkOption.md)!:options indicating how symbolic links are handled |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | a map of the attributes returned; The map's keys are the attribute names, its values are the attribute values |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the attribute view is not available |
| `java.lang.IllegalArgumentException` | if no attributes are specified or an unrecognized attribute is specified |
| `java.io.IOException` | if an I/O error occurs |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, its [checkRead](../java/lang/SecurityManager.md))method denies read access to the file. If this method is invoked to read security sensitive attributes then the security manager may be invoke to check for additional permissions. |

### readString

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun readString(path: Path!): String!
```

Reads all content from a file into a string, decoding from bytes to characters using the [UTF-8](../java/nio/charset/StandardCharsets.md) [charset](../java/nio/charset/Charset.md). The method ensures that the file is closed when all content have been read or an I/O error, or other runtime exception, is thrown.

This method is equivalent to:`readString(path, StandardCharsets.UTF_8) `

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a String containing the content read from the file |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs reading from the file or a malformed or unmappable byte sequence is read |
| `java.lang.OutOfMemoryError` | if the file is extremely large, for example larger than`2GB` |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the file. |
| --- | --- |

### readString

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun readString(
    path: Path!, 
    cs: Charset!
): String!
```

Reads all characters from a file into a string, decoding from bytes to characters using the specified [charset](../java/nio/charset/Charset.md). The method ensures that the file is closed when all content have been read or an I/O error, or other runtime exception, is thrown.

This method reads all content including the line separators in the middle and/or at the end. The resulting string will contain line separators as they appear in the file.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |
| `cs` | [Charset](../java/nio/charset/Charset.md)!:the charset to use for decoding |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a String containing the content read from the file |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs reading from the file or a malformed or unmappable byte sequence is read |
| `java.lang.OutOfMemoryError` | if the file is extremely large, for example larger than`2GB` |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the file. |
| --- | --- |

### readSymbolicLink

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun readSymbolicLink(link: Path!): Path!
```

Reads the target of a symbolic link*(optional operation)*.

If the file system supports [symbolic links](../java/nio/file/_package.md) then this method is used to read the target of the link, failing if the file is not a symbolic link. The target of the link need not exist. The returned`Path`object will be associated with the same file system as`link`.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------|
| `link` | [Path](../java/nio/file/Path.md)!:the path to the symbolic link |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------|
| [Path](../java/nio/file/Path.md)! | a`Path`object representing the target of the link |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the implementation does not support symbolic links |
| `java.nio.file.NotLinkException` | if the target could otherwise not be read because the file is not a symbolic link*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, it checks that`FilePermission`has been granted with the "`readlink`" action to read the link. |

### setAttribute

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setAttribute(
    path: Path!, 
    attribute: String!, 
    value: Any!, 
    vararg options: LinkOption!
): Path!
```

Sets the value of a file attribute.

The`attribute`parameter identifies the attribute to be set and takes the form:
\[*view-name* **:** \]*attribute-name* where square brackets \[...\] delineate an optional component and the character`':'`stands for itself.

*view-name* is the [name](../java/nio/file/attribute/AttributeView.md))of a [FileAttributeView](../java/nio/file/attribute/FileAttributeView.md) that identifies a set of file attributes. If not specified then it defaults to`"basic"`, the name of the file attribute view that identifies the basic set of file attributes common to many file systems.*attribute-name*is the name of the attribute within the set.

The`options`array may be used to indicate how symbolic links are handled for the case that the file is a symbolic link. By default, symbolic links are followed and the file attribute of the final target of the link is set. If the option [NOFOLLOW_LINKS](../java/nio/file/LinkOption.md) is present then symbolic links are not followed.

**Usage Example:**Suppose we want to set the DOS "hidden" attribute: 

```kotlin
Path path = ...
     Files.setAttribute(path, "dos:hidden", true);
  
```

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |
| `attribute` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the attribute to set |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the attribute value |
| --- | --- |
| `options` | [LinkOption](../java/nio/file/LinkOption.md)!:options indicating how symbolic links are handled |

| Return ||
|----------------------------------------------------------------------------|----------------|
| [Path](../java/nio/file/Path.md)! | the given path |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the attribute view is not available |
| `java.lang.IllegalArgumentException` | if the attribute name is not specified, or is not recognized, or the attribute value is of the correct type but has an inappropriate value |
| `java.lang.ClassCastException` | if the attribute value is not of the expected type or is a collection containing elements that are not of the expected type |
| --- | --- |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, its [checkWrite](../java/lang/SecurityManager.md))method denies write access to the file. If this method is invoked to set security sensitive attributes then the security manager may be invoked to check for additional permissions. |

### setLastModifiedTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setLastModifiedTime(
    path: Path!, 
    time: FileTime!
): Path!
```

Updates a file's last modified time attribute. The file time is converted to the epoch and precision supported by the file system. Converting from finer to coarser granularities result in precision loss. The behavior of this method when attempting to set the last modified time when it is not supported by the file system or is outside the range supported by the underlying file store is not defined. It may or not fail by throwing an`IOException`.

**Usage Example:**Suppose we want to set the last modified time to the current time: 

```kotlin
Path path = ...
     FileTime now = FileTime.fromMillis(System.currentTimeMillis());
     Files.setLastModifiedTime(path, now);
  
```

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |
| `time` | [FileTime](../java/nio/file/attribute/FileTime.md)!:the new last modified time |

| Return ||
|----------------------------------------------------------------------------|----------------|
| [Path](../java/nio/file/Path.md)! | the given path |

| Exceptions ||
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, its [checkWrite](../java/lang/SecurityManager.md))method denies write access to the file. |

**See Also**

- [java.nio.file.attribute.BasicFileAttributeView#setTimes](../java/nio/file/attribute/BasicFileAttributeView.md)) 

### setOwner

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setOwner(
    path: Path!, 
    owner: UserPrincipal!
): Path!
```

Updates the file owner.

The`path`parameter is associated with a file system that supports [FileOwnerAttributeView](../java/nio/file/attribute/FileOwnerAttributeView.md). This file attribute view provides access to a file attribute that is the owner of the file.

**Usage Example:**Suppose we want to make "joe" the owner of a file: 

```kotlin
Path path = ...
      UserPrincipalLookupService lookupService =
          provider(path).getUserPrincipalLookupService();
      UserPrincipal joe = lookupService.lookupPrincipalByName("joe");
      Files.setOwner(path, joe);
  
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:The path to the file |
| `owner` | [UserPrincipal](../java/nio/file/attribute/UserPrincipal.md)!:The new file owner |

| Return ||
|----------------------------------------------------------------------------|----------------|
| [Path](../java/nio/file/Path.md)! | The given path |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the associated file system does not support the`FileOwnerAttributeView` |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, it denies [RuntimePermission](../java/lang/RuntimePermission.md)`("accessUserInformation")`or its [checkWrite](../java/lang/SecurityManager.md))method denies write access to the file. |
| --- | --- |

**See Also**

- [java.nio.file.FileSystem#getUserPrincipalLookupService](../java/nio/file/FileSystem.md))
- [java.nio.file.attribute.UserPrincipalLookupService](../java/nio/file/attribute/UserPrincipalLookupService.md) 

### setPosixFilePermissions

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setPosixFilePermissions(
    path: Path!, 
    perms: MutableSet<PosixFilePermission!>!
): Path!
```

Sets a file's POSIX permissions.

The`path`parameter is associated with a`FileSystem`that supports the [PosixFileAttributeView](../java/nio/file/attribute/PosixFileAttributeView.md). This attribute view provides access to file attributes commonly associated with files on file systems used by operating systems that implement the Portable Operating System Interface (POSIX) family of standards.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:The path to the file |
| `perms` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [PosixFilePermission](../java/nio/file/attribute/PosixFilePermission.md)!\>!:The new set of permissions |

| Return ||
|----------------------------------------------------------------------------|----------------|
| [Path](../java/nio/file/Path.md)! | The given path |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the associated file system does not support the`PosixFileAttributeView` |
| `java.lang.ClassCastException` | if the sets contains elements that are not of type`PosixFilePermission` |
| `java.io.IOException` | if an I/O error occurs |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, it denies [RuntimePermission](../java/lang/RuntimePermission.md)`("accessUserInformation")`or its [checkWrite](../java/lang/SecurityManager.md))method denies write access to the file. |

### size

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun size(path: Path!): Long
```

Returns the size of a file (in bytes). The size may differ from the actual size on the file system due to compression, support for sparse files, or other reasons. The size of files that are not [regular](../java/nio/file/Files.md))files is implementation specific and therefore unspecified.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |

| Return ||
|------------------------------------------------------------------------------|-------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the file size, in bytes |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, its [checkRead](../java/lang/SecurityManager.md))method denies read access to the file. |

**See Also**

- [java.nio.file.attribute.BasicFileAttributes#size](../java/nio/file/attribute/BasicFileAttributes.md)) 

### walk

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun walk(
    start: Path!, 
    maxDepth: Int, 
    vararg options: FileVisitOption!
): Stream<Path!>!
```

Return a`Stream`that is lazily populated with`Path`by walking the file tree rooted at a given starting file. The file tree is traversed*depth-first* , the elements in the stream are [Path](../java/nio/file/Path.md) objects that are obtained as if by [resolving](../java/nio/file/Path.md))the relative path against`start`.

The`stream`walks the file tree as elements are consumed. The`Stream`returned is guaranteed to have at least one element, the starting file itself. For each file visited, the stream attempts to read its [BasicFileAttributes](../java/nio/file/attribute/BasicFileAttributes.md). If the file is a directory and can be opened successfully, entries in the directory, and their*descendants* will follow the directory in the stream as they are encountered. When all entries have been visited, then the directory is closed. The file tree walk then continues at the next*sibling*of the directory.

The stream is*weakly consistent*. It does not freeze the file tree while iterating, so it may (or may not) reflect updates to the file tree that occur after returned from this method.

By default, symbolic links are not automatically followed by this method. If the`options`parameter contains the [FOLLOW_LINKS](../java/nio/file/FileVisitOption.md) option then symbolic links are followed. When following links, and the attributes of the target cannot be read, then this method attempts to get the`BasicFileAttributes`of the link.

If the`options`parameter contains the [FOLLOW_LINKS](../java/nio/file/FileVisitOption.md) option then the stream keeps track of directories visited so that cycles can be detected. A cycle arises when there is an entry in a directory that is an ancestor of the directory. Cycle detection is done by recording the [file-key](../java/nio/file/attribute/BasicFileAttributes.md))of directories, or if file keys are not available, by invoking the [isSameFile](../java/nio/file/Files.md))method to test if a directory is the same file as an ancestor. When a cycle is detected it is treated as an I/O error with an instance of [FileSystemLoopException](../java/nio/file/FileSystemLoopException.md).

The`maxDepth`parameter is the maximum number of levels of directories to visit. A value of`0`means that only the starting file is visited, unless denied by the security manager. A value of [MAX_VALUE](../java/lang/Integer.md) may be used to indicate that all levels should be visited.

When a security manager is installed and it denies access to a file (or directory), then it is ignored and not included in the stream.

The returned stream contains references to one or more open directories. The directories are closed by closing the stream.

If an [IOException](../java/io/IOException.md) is thrown when accessing the directory after this method has returned, it is wrapped in an [UncheckedIOException](../java/io/UncheckedIOException.md) which will be thrown from the method that caused the access to take place.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `start` | [Path](../java/nio/file/Path.md)!:the starting file |
| `maxDepth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of directory levels to visit |
| `options` | [FileVisitOption](../java/nio/file/FileVisitOption.md)!:options to configure the traversal |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Stream](../java/util/stream/Stream.md)< [Path](../java/nio/file/Path.md)!>! | the [Stream](../java/util/stream/Stream.md) of [Path](../java/nio/file/Path.md) |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the`maxDepth`parameter is negative |
| `java.lang.SecurityException` | If the security manager denies access to the starting file. In the case of the default provider, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the directory. |
| `java.io.IOException` | if an I/O error is thrown when accessing the starting file. |
| --- | --- |

### walk

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun walk(
    start: Path!, 
    vararg options: FileVisitOption!
): Stream<Path!>!
```

Return a`Stream`that is lazily populated with`Path`by walking the file tree rooted at a given starting file. The file tree is traversed*depth-first* , the elements in the stream are [Path](../java/nio/file/Path.md) objects that are obtained as if by [resolving](../java/nio/file/Path.md))the relative path against`start`.

This method works as if invoking it were equivalent to evaluating the expression: 

```kotlin
walk(start, Integer.MAX_VALUE, options)
  
```
In other words, it visits all levels of the file tree.

The returned stream contains references to one or more open directories. The directories are closed by closing the stream.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------|
| `start` | [Path](../java/nio/file/Path.md)!:the starting file |
| `options` | [FileVisitOption](../java/nio/file/FileVisitOption.md)!:options to configure the traversal |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Stream](../java/util/stream/Stream.md)< [Path](../java/nio/file/Path.md)!>! | the [Stream](../java/util/stream/Stream.md) of [Path](../java/nio/file/Path.md) |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If the security manager denies access to the starting file. In the case of the default provider, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the directory. |
| `java.io.IOException` | if an I/O error is thrown when accessing the starting file. |

**See Also**

- [#walk(Path, int, FileVisitOption...)](../java/nio/file/Files.md)) 

### walkFileTree

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun walkFileTree(
    start: Path!, 
    visitor: FileVisitor<in Path!>!
): Path!
```

Walks a file tree.

This method works as if invoking it were equivalent to evaluating the expression: 

```kotlin
walkFileTree(start, EnumSet.noneOf(FileVisitOption.class), Integer.MAX_VALUE, visitor)
  
```
In other words, it does not follow symbolic links, and visits all levels of the file tree.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `start` | [Path](../java/nio/file/Path.md)!:the starting file |
| `visitor` | [FileVisitor](../java/nio/file/FileVisitor.md)\<in [Path](../java/nio/file/Path.md)!\>!:the file visitor to invoke for each file |

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Path](../java/nio/file/Path.md)! | the starting file |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If the security manager denies access to the starting file. In the case of the default provider, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the directory. |
| `java.io.IOException` | if an I/O error is thrown by a visitor method |

### walkFileTree

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun walkFileTree(
    start: Path!, 
    options: MutableSet<FileVisitOption!>!, 
    maxDepth: Int, 
    visitor: FileVisitor<in Path!>!
): Path!
```

Walks a file tree.

This method walks a file tree rooted at a given starting file. The file tree traversal is*depth-first* with the given [FileVisitor](../java/nio/file/FileVisitor.md) invoked for each file encountered. File tree traversal completes when all accessible files in the tree have been visited, or a visit method returns a result of [TERMINATE](../java/nio/file/FileVisitResult.md). Where a visit method terminates due an`IOException`, an uncaught error, or runtime exception, then the traversal is terminated and the error or exception is propagated to the caller of this method.

For each file encountered this method attempts to read its . If the file is not a directory then the [visitFile](../java/nio/file/FileVisitor.md))method is invoked with the file attributes. If the file attributes cannot be read, due to an I/O exception, then the [visitFileFailed](../java/nio/file/FileVisitor.md))method is invoked with the I/O exception.

Where the file is a directory, and the directory could not be opened, then the`visitFileFailed`method is invoked with the I/O exception, after which, the file tree walk continues, by default, at the next*sibling*of the directory.

Where the directory is opened successfully, then the entries in the directory, and their*descendants* are visited. When all entries have been visited, or an I/O error occurs during iteration of the directory, then the directory is closed and the visitor's [postVisitDirectory](../java/nio/file/FileVisitor.md))method is invoked. The file tree walk then continues, by default, at the next*sibling*of the directory.

By default, symbolic links are not automatically followed by this method. If the`options`parameter contains the [FOLLOW_LINKS](../java/nio/file/FileVisitOption.md) option then symbolic links are followed. When following links, and the attributes of the target cannot be read, then this method attempts to get the`BasicFileAttributes`of the link. If they can be read then the`visitFile`method is invoked with the attributes of the link (otherwise the`visitFileFailed`method is invoked as specified above).

If the`options`parameter contains the [FOLLOW_LINKS](../java/nio/file/FileVisitOption.md) option then this method keeps track of directories visited so that cycles can be detected. A cycle arises when there is an entry in a directory that is an ancestor of the directory. Cycle detection is done by recording the [file-key](../java/nio/file/attribute/BasicFileAttributes.md))of directories, or if file keys are not available, by invoking the [isSameFile](../java/nio/file/Files.md))method to test if a directory is the same file as an ancestor. When a cycle is detected it is treated as an I/O error, and the [visitFileFailed](../java/nio/file/FileVisitor.md))method is invoked with an instance of [FileSystemLoopException](../java/nio/file/FileSystemLoopException.md).

The`maxDepth`parameter is the maximum number of levels of directories to visit. A value of`0`means that only the starting file is visited, unless denied by the security manager. A value of [MAX_VALUE](../java/lang/Integer.md) may be used to indicate that all levels should be visited. The`visitFile`method is invoked for all files, including directories, encountered at`maxDepth`, unless the basic file attributes cannot be read, in which case the`visitFileFailed`method is invoked.

If a visitor returns a result of`null`then`NullPointerException`is thrown.

When a security manager is installed and it denies access to a file (or directory), then it is ignored and the visitor is not invoked for that file (or directory).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `start` | [Path](../java/nio/file/Path.md)!:the starting file |
| `options` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [FileVisitOption](../java/nio/file/FileVisitOption.md)!\>!:options to configure the traversal |
| `maxDepth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of directory levels to visit |
| --- | --- |
| `visitor` | [FileVisitor](../java/nio/file/FileVisitor.md)\<in [Path](../java/nio/file/Path.md)!\>!:the file visitor to invoke for each file |

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Path](../java/nio/file/Path.md)! | the starting file |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the`maxDepth`parameter is negative |
| `java.lang.SecurityException` | If the security manager denies access to the starting file. In the case of the default provider, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the directory. |
| `java.io.IOException` | if an I/O error is thrown by a visitor method |
| --- | --- |

### write

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun write(
    path: Path!, 
    bytes: ByteArray!, 
    vararg options: OpenOption!
): Path!
```

Writes bytes to a file. The`options`parameter specifies how the file is created or opened. If no options are present then this method works as if the [CREATE](../java/nio/file/StandardOpenOption.md), [TRUNCATE_EXISTING](../java/nio/file/StandardOpenOption.md), and [WRITE](../java/nio/file/StandardOpenOption.md) options are present. In other words, it opens the file for writing, creating the file if it doesn't exist, or initially truncating an existing [regular-file](../java/nio/file/Files.md))to a size of`0`. All bytes in the byte array are written to the file. The method ensures that the file is closed when all bytes have been written (or an I/O error or other runtime exception is thrown). If an I/O error occurs then it may do so after the file has been created or truncated, or after some bytes have been written to the file.

**Usage example**: By default the method creates a new file or overwrites an existing file. Suppose you instead want to append bytes to an existing file: 

```kotlin
Path path = ...
      byte[] bytes = ...
      Files.write(path, bytes, StandardOpenOption.APPEND);
  
```

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the byte array with the bytes to write |
| `options` | [OpenOption](../java/nio/file/OpenOption.md)!:options specifying how the file is opened |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|----------|
| [Path](../java/nio/file/Path.md)! | the path |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`options`contains an invalid combination of options |
| `java.io.IOException` | if an I/O error occurs writing to or creating the file |
| `java.lang.UnsupportedOperationException` | if an unsupported option is specified |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access to the file. The [checkDelete](../java/lang/SecurityManager.md))method is invoked to check delete access if the file is opened with the`DELETE_ON_CLOSE`option. |

### write

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun write(
    path: Path!, 
    lines: MutableIterable<CharSequence!>!, 
    cs: Charset!, 
    vararg options: OpenOption!
): Path!
```

Write lines of text to a file. Each line is a char sequence and is written to the file in sequence with each line terminated by the platform's line separator, as defined by the system property`line.separator`. Characters are encoded into bytes using the specified charset.

The`options`parameter specifies how the file is created or opened. If no options are present then this method works as if the [CREATE](../java/nio/file/StandardOpenOption.md), [TRUNCATE_EXISTING](../java/nio/file/StandardOpenOption.md), and [WRITE](../java/nio/file/StandardOpenOption.md) options are present. In other words, it opens the file for writing, creating the file if it doesn't exist, or initially truncating an existing [regular-file](../java/nio/file/Files.md))to a size of`0`. The method ensures that the file is closed when all lines have been written (or an I/O error or other runtime exception is thrown). If an I/O error occurs then it may do so after the file has been created or truncated, or after some bytes have been written to the file.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |
| `lines` | [MutableIterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\>!:an object to iterate over the char sequences |
| `cs` | [Charset](../java/nio/charset/Charset.md)!:the charset to use for encoding |
| --- | --- |
| `options` | [OpenOption](../java/nio/file/OpenOption.md)!:options specifying how the file is opened |

| Return ||
|----------------------------------------------------------------------------|----------|
| [Path](../java/nio/file/Path.md)! | the path |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`options`contains an invalid combination of options |
| `java.io.IOException` | if an I/O error occurs writing to or creating the file, or the text cannot be encoded using the specified charset |
| `java.lang.UnsupportedOperationException` | if an unsupported option is specified |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access to the file. The [checkDelete](../java/lang/SecurityManager.md))method is invoked to check delete access if the file is opened with the`DELETE_ON_CLOSE`option. |

### write

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun write(
    path: Path!, 
    lines: MutableIterable<CharSequence!>!, 
    vararg options: OpenOption!
): Path!
```

Write lines of text to a file. Characters are encoded into bytes using the [UTF-8](../java/nio/charset/StandardCharsets.md) [charset](../java/nio/charset/Charset.md).

This method works as if invoking it were equivalent to evaluating the expression: 

```kotlin
<code>Files.write(path, lines, StandardCharsets.UTF_8, options);
  </code>
```

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |
| `lines` | [MutableIterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\>!:an object to iterate over the char sequences |
| `options` | [OpenOption](../java/nio/file/OpenOption.md)!:options specifying how the file is opened |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|----------|
| [Path](../java/nio/file/Path.md)! | the path |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`options`contains an invalid combination of options |
| `java.io.IOException` | if an I/O error occurs writing to or creating the file, or the text cannot be encoded as`UTF-8` |
| `java.lang.UnsupportedOperationException` | if an unsupported option is specified |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access to the file. The [checkDelete](../java/lang/SecurityManager.md))method is invoked to check delete access if the file is opened with the`DELETE_ON_CLOSE`option. |

### writeString

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun writeString(
    path: Path!, 
    csq: CharSequence!, 
    cs: Charset!, 
    vararg options: OpenOption!
): Path!
```

Write a [CharSequence](../java/lang/CharSequence.md) to a file. Characters are encoded into bytes using the specified [charset](../java/nio/charset/Charset.md).

All characters are written as they are, including the line separators in the char sequence. No extra characters are added.

The`options`parameter specifies how the file is created or opened. If no options are present then this method works as if the [CREATE](../java/nio/file/StandardOpenOption.md), [TRUNCATE_EXISTING](../java/nio/file/StandardOpenOption.md), and [WRITE](../java/nio/file/StandardOpenOption.md) options are present. In other words, it opens the file for writing, creating the file if it doesn't exist, or initially truncating an existing [regular-file](../java/nio/file/Files.md))to a size of`0`.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |
| `csq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the CharSequence to be written |
| `cs` | [Charset](../java/nio/charset/Charset.md)!:the charset to use for encoding |
| --- | --- |
| `options` | [OpenOption](../java/nio/file/OpenOption.md)!:options specifying how the file is opened |

| Return ||
|----------------------------------------------------------------------------|----------|
| [Path](../java/nio/file/Path.md)! | the path |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`options`contains an invalid combination of options |
| `java.io.IOException` | if an I/O error occurs writing to or creating the file, or the text cannot be encoded using the specified charset |
| `java.lang.UnsupportedOperationException` | if an unsupported option is specified |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access to the file. The [checkDelete](../java/lang/SecurityManager.md))method is invoked to check delete access if the file is opened with the`DELETE_ON_CLOSE`option. |

### writeString

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun writeString(
    path: Path!, 
    csq: CharSequence!, 
    vararg options: OpenOption!
): Path!
```

Write a [CharSequence](../java/lang/CharSequence.md) to a file. Characters are encoded into bytes using the [UTF-8](../java/nio/charset/StandardCharsets.md) [charset](../java/nio/charset/Charset.md).

This method is equivalent to:`writeString(path, test, StandardCharsets.UTF_8, options) `

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to the file |
| `csq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the CharSequence to be written |
| `options` | [OpenOption](../java/nio/file/OpenOption.md)!:options specifying how the file is opened |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|----------|
| [Path](../java/nio/file/Path.md)! | the path |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`options`contains an invalid combination of options |
| `java.io.IOException` | if an I/O error occurs writing to or creating the file, or the text cannot be encoded using the specified charset |
| `java.lang.UnsupportedOperationException` | if an unsupported option is specified |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access to the file. The [checkDelete](../java/lang/SecurityManager.md))method is invoked to check delete access if the file is opened with the`DELETE_ON_CLOSE`option. |
