# DosFileAttributes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DosFileAttributes

```
interface DosFileAttributes : BasicFileAttributes
```

| [java.nio.file.attribute.DosFileAttributes](../java/nio/file/attribute/DosFileAttributes.md) |

File attributes associated with a file in a file system that supports legacy "DOS" attributes.

**Usage Example:** 

```kotlin
Path file = ...
     DosFileAttributes attrs = Files.readAttributes(file, DosFileAttributes.class);
  
```

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isArchive](../java/nio/file/attribute/DosFileAttributes.md))`()` Returns the value of the archive attribute. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHidden](../java/nio/file/attribute/DosFileAttributes.md))`()` Returns the value of the hidden attribute. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadOnly](../java/nio/file/attribute/DosFileAttributes.md))`()` Returns the value of the read-only attribute. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSystem](../java/nio/file/attribute/DosFileAttributes.md))`()` Returns the value of the system attribute. |

| Inherited functions ||
|---|---|
| From class [BasicFileAttributes](../java/nio/file/attribute/BasicFileAttributes.md) |----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [FileTime](../java/nio/file/attribute/FileTime.md)! | [creationTime](../java/nio/file/attribute/BasicFileAttributes.md))`()` <br /> Returns the creation time. The creation time is the time that the file was created. If the file system implementation does not support a time stamp to indicate the time when the file was created then this method returns an implementation specific default value, typically the [last-modified-time](../java/nio/file/attribute/BasicFileAttributes.md))or a`FileTime`representing the epoch (1970-01-01T00:00:00Z). <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [fileKey](../java/nio/file/attribute/BasicFileAttributes.md))`()` <br /> Returns an object that uniquely identifies the given file, or`null`if a file key is not available. On some platforms or file systems it is possible to use an identifier, or a combination of identifiers to uniquely identify a file. Such identifiers are important for operations such as file tree traversal in file systems that support [symbolic links](../java/nio/file/_package.md) or file systems that allow a file to be an entry in more than one directory. On UNIX file systems, for example, the*device ID* and*inode*are commonly used for such purposes. The file key returned by this method can only be guaranteed to be unique if the file system and files remain static. Whether a file system re-uses identifiers after a file is deleted is implementation dependent and therefore unspecified. File keys returned by this method can be compared for equality and are suitable for use in collections. If the file system and files remain static, and two files are the [same](../java/nio/file/Files.md))with non-`null`file keys, then their file keys are equal. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDirectory](../java/nio/file/attribute/BasicFileAttributes.md))`()` <br /> Tells whether the file is a directory. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOther](../java/nio/file/attribute/BasicFileAttributes.md))`()` <br /> Tells whether the file is something other than a regular file, directory, or symbolic link. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRegularFile](../java/nio/file/attribute/BasicFileAttributes.md))`()` <br /> Tells whether the file is a regular file with opaque content. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSymbolicLink](../java/nio/file/attribute/BasicFileAttributes.md))`()` <br /> Tells whether the file is a symbolic link. <br /> | | [FileTime](../java/nio/file/attribute/FileTime.md)! | [lastAccessTime](../java/nio/file/attribute/BasicFileAttributes.md))`()` <br /> Returns the time of last access. If the file system implementation does not support a time stamp to indicate the time of last access then this method returns an implementation specific default value, typically the [last-modified-time](../java/nio/file/attribute/BasicFileAttributes.md))or a`FileTime`representing the epoch (1970-01-01T00:00:00Z). <br /> | | [FileTime](../java/nio/file/attribute/FileTime.md)! | [lastModifiedTime](../java/nio/file/attribute/BasicFileAttributes.md))`()` <br /> Returns the time of last modification. If the file system implementation does not support a time stamp to indicate the time of last modification then this method returns an implementation specific default value, typically a`FileTime`representing the epoch (1970-01-01T00:00:00Z). <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [size](../java/nio/file/attribute/BasicFileAttributes.md))`()` <br /> Returns the size of the file (in bytes). The size may differ from the actual size on the file system due to compression, support for sparse files, or other reasons. The size of files that are not [regular](../java/nio/file/attribute/BasicFileAttributes.md))files is implementation specific and therefore unspecified. <br /> | ||

## Public methods

### isArchive

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isArchive(): Boolean
```

Returns the value of the archive attribute.

This attribute is typically used by backup programs.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the value of the archive attribute |

### isHidden

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isHidden(): Boolean
```

Returns the value of the hidden attribute.

This attribute is often used to indicate if the file is visible to users.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the value of the hidden attribute |

### isReadOnly

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isReadOnly(): Boolean
```

Returns the value of the read-only attribute.

This attribute is often used as a simple access control mechanism to prevent files from being deleted or updated. Whether the file system or platform does any enforcement to prevent*read-only*files from being updated is implementation specific.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the value of the read-only attribute |

### isSystem

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSystem(): Boolean
```

Returns the value of the system attribute.

This attribute is often used to indicate that the file is a component of the operating system.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the value of the system attribute |
