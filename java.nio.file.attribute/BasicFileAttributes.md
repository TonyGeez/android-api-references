# BasicFileAttributes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BasicFileAttributes

```
interface BasicFileAttributes
```

| [java.nio.file.attribute.BasicFileAttributes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#) |

| Known Direct Subclasses [DosFileAttributes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/DosFileAttributes), [PosixFileAttributes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributes) |-------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DosFileAttributes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/DosFileAttributes) | File attributes associated with a file in a file system that supports legacy "DOS" attributes. | | [PosixFileAttributes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributes) | File attributes associated with files on file systems used by operating systems that implement the Portable Operating System Interface (POSIX) family of standards. | |

Basic attributes associated with a file in a file system.

Basic file attributes are attributes that are common to many file systems and consist of mandatory and optional file attributes as defined by this interface.

**Usage Example:** 

```kotlin
Path file = ...
     BasicFileAttributes attrs = Files.readAttributes(file, BasicFileAttributes.class);
  
```

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [FileTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime)! | [creationTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#creationTime())`()` Returns the creation time. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [fileKey](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#fileKey())`()` Returns an object that uniquely identifies the given file, or`null`if a file key is not available. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDirectory](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#isDirectory())`()` Tells whether the file is a directory. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOther](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#isOther())`()` Tells whether the file is something other than a regular file, directory, or symbolic link. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRegularFile](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#isRegularFile())`()` Tells whether the file is a regular file with opaque content. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSymbolicLink](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#isSymbolicLink())`()` Tells whether the file is a symbolic link. |
| abstract [FileTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime)! | [lastAccessTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#lastAccessTime())`()` Returns the time of last access. |
| abstract [FileTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime)! | [lastModifiedTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#lastModifiedTime())`()` Returns the time of last modification. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [size](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#size())`()` Returns the size of the file (in bytes). |

## Public methods

### creationTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun creationTime(): FileTime!
```

Returns the creation time. The creation time is the time that the file was created.

If the file system implementation does not support a time stamp to indicate the time when the file was created then this method returns an implementation specific default value, typically the [last-modified-time](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#lastModifiedTime())or a`FileTime`representing the epoch (1970-01-01T00:00:00Z).

| Return ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [FileTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime)! | a`FileTime`representing the time the file was created |

### fileKey

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun fileKey(): Any!
```

Returns an object that uniquely identifies the given file, or`null`if a file key is not available. On some platforms or file systems it is possible to use an identifier, or a combination of identifiers to uniquely identify a file. Such identifiers are important for operations such as file tree traversal in file systems that support [symbolic links](https://developer.android.com/reference/kotlin/java/nio/file/package-summary.html#links) or file systems that allow a file to be an entry in more than one directory. On UNIX file systems, for example, the*device ID* and*inode*are commonly used for such purposes.

The file key returned by this method can only be guaranteed to be unique if the file system and files remain static. Whether a file system re-uses identifiers after a file is deleted is implementation dependent and therefore unspecified.

File keys returned by this method can be compared for equality and are suitable for use in collections. If the file system and files remain static, and two files are the [same](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#isSameFile(java.nio.file.Path,%20java.nio.file.Path))with non-`null`file keys, then their file keys are equal.

| Return ||
|-----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | an object that uniquely identifies the given file, or`null` |

**See Also**

### isDirectory

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isDirectory(): Boolean
```

Tells whether the file is a directory.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the file is a directory |

### isOther

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isOther(): Boolean
```

Tells whether the file is something other than a regular file, directory, or symbolic link.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the file something other than a regular file, directory or symbolic link |

### isRegularFile

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isRegularFile(): Boolean
```

Tells whether the file is a regular file with opaque content.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the file is a regular file with opaque content |

### isSymbolicLink

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSymbolicLink(): Boolean
```

Tells whether the file is a symbolic link.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the file is a symbolic link |

### lastAccessTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun lastAccessTime(): FileTime!
```

Returns the time of last access.

If the file system implementation does not support a time stamp to indicate the time of last access then this method returns an implementation specific default value, typically the [last-modified-time](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#lastModifiedTime())or a`FileTime`representing the epoch (1970-01-01T00:00:00Z).

| Return ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| [FileTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime)! | a`FileTime`representing the time of last access |

### lastModifiedTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun lastModifiedTime(): FileTime!
```

Returns the time of last modification.

If the file system implementation does not support a time stamp to indicate the time of last modification then this method returns an implementation specific default value, typically a`FileTime`representing the epoch (1970-01-01T00:00:00Z).

| Return ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [FileTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime)! | a`FileTime`representing the time the file was last modified |

### size

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun size(): Long
```

Returns the size of the file (in bytes). The size may differ from the actual size on the file system due to compression, support for sparse files, or other reasons. The size of files that are not [regular](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#isRegularFile())files is implementation specific and therefore unspecified.

| Return ||
|------------------------------------------------------------------------------|-------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the file size, in bytes |
