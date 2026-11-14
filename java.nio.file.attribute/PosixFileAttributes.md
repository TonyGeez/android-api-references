# PosixFileAttributes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PosixFileAttributes

```
interface PosixFileAttributes : BasicFileAttributes
```

| [java.nio.file.attribute.PosixFileAttributes](PosixFileAttributes.md) |

File attributes associated with files on file systems used by operating systems that implement the Portable Operating System Interface (POSIX) family of standards.

The POSIX attributes of a file are retrieved using a [PosixFileAttributeView](PosixFileAttributeView.md) by invoking its [readAttributes](PosixFileAttributeView.md))method.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [GroupPrincipal](GroupPrincipal.md)! | [group](PosixFileAttributes.md))`()` Returns the group owner of the file. |
| abstract [UserPrincipal](UserPrincipal.md)! | [owner](PosixFileAttributes.md))`()` Returns the owner of the file. |
| abstract [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [PosixFilePermission](PosixFilePermission.md)!\>! | [permissions](PosixFileAttributes.md))`()` Returns the permissions of the file. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [BasicFileAttributes](BasicFileAttributes.md) |----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [FileTime](FileTime.md)! | [creationTime](BasicFileAttributes.md))`()` <br /> Returns the creation time. The creation time is the time that the file was created. If the file system implementation does not support a time stamp to indicate the time when the file was created then this method returns an implementation specific default value, typically the [last-modified-time](BasicFileAttributes.md))or a`FileTime`representing the epoch (1970-01-01T00:00:00Z). <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [fileKey](BasicFileAttributes.md))`()` <br /> Returns an object that uniquely identifies the given file, or`null`if a file key is not available. On some platforms or file systems it is possible to use an identifier, or a combination of identifiers to uniquely identify a file. Such identifiers are important for operations such as file tree traversal in file systems that support [symbolic links](../java.nio.file/_package.md) or file systems that allow a file to be an entry in more than one directory. On UNIX file systems, for example, the*device ID* and*inode*are commonly used for such purposes. The file key returned by this method can only be guaranteed to be unique if the file system and files remain static. Whether a file system re-uses identifiers after a file is deleted is implementation dependent and therefore unspecified. File keys returned by this method can be compared for equality and are suitable for use in collections. If the file system and files remain static, and two files are the [same](../java.nio.file/Files.md))with non-`null`file keys, then their file keys are equal. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDirectory](BasicFileAttributes.md))`()` <br /> Tells whether the file is a directory. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOther](BasicFileAttributes.md))`()` <br /> Tells whether the file is something other than a regular file, directory, or symbolic link. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRegularFile](BasicFileAttributes.md))`()` <br /> Tells whether the file is a regular file with opaque content. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSymbolicLink](BasicFileAttributes.md))`()` <br /> Tells whether the file is a symbolic link. <br /> | | [FileTime](FileTime.md)! | [lastAccessTime](BasicFileAttributes.md))`()` <br /> Returns the time of last access. If the file system implementation does not support a time stamp to indicate the time of last access then this method returns an implementation specific default value, typically the [last-modified-time](BasicFileAttributes.md))or a`FileTime`representing the epoch (1970-01-01T00:00:00Z). <br /> | | [FileTime](FileTime.md)! | [lastModifiedTime](BasicFileAttributes.md))`()` <br /> Returns the time of last modification. If the file system implementation does not support a time stamp to indicate the time of last modification then this method returns an implementation specific default value, typically a`FileTime`representing the epoch (1970-01-01T00:00:00Z). <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [size](BasicFileAttributes.md))`()` <br /> Returns the size of the file (in bytes). The size may differ from the actual size on the file system due to compression, support for sparse files, or other reasons. The size of files that are not [regular](BasicFileAttributes.md))files is implementation specific and therefore unspecified. <br /> | ||

## Public methods

### group

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun group(): GroupPrincipal!
```

Returns the group owner of the file.

| Return ||
|----------------------------------------------------------------------------------------------------------|----------------------|
| [GroupPrincipal](GroupPrincipal.md)! | the file group owner |

**See Also**

- [java.nio.file.attribute.PosixFileAttributeView#setGroup](PosixFileAttributeView.md)) 

### owner

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun owner(): UserPrincipal!
```

Returns the owner of the file.

| Return ||
|--------------------------------------------------------------------------------------------------------|----------------|
| [UserPrincipal](UserPrincipal.md)! | the file owner |

**See Also**

- [java.nio.file.attribute.PosixFileAttributeView#setOwner](FileOwnerAttributeView.md)) 

### permissions

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun permissions(): MutableSet<PosixFilePermission!>!
```

Returns the permissions of the file. The file permissions are returned as a set of [PosixFilePermission](PosixFilePermission.md) elements. The returned set is a copy of the file permissions and is modifiable. This allows the result to be modified and passed to the [setPermissions](PosixFileAttributeView.md))method to update the file's permissions.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [PosixFilePermission](PosixFilePermission.md)!>! | the file permissions |

**See Also**

- [java.nio.file.attribute.PosixFileAttributeView#setPermissions](PosixFileAttributeView.md))
