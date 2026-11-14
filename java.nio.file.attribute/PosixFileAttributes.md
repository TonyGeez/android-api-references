# PosixFileAttributes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PosixFileAttributes

```
interface PosixFileAttributes : BasicFileAttributes
```

| [java.nio.file.attribute.PosixFileAttributes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributes#) |

File attributes associated with files on file systems used by operating systems that implement the Portable Operating System Interface (POSIX) family of standards.

The POSIX attributes of a file are retrieved using a [PosixFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributeView) by invoking its [readAttributes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributeView#readAttributes())method.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [GroupPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/GroupPrincipal)! | [group](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributes#group())`()` Returns the group owner of the file. |
| abstract [UserPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal)! | [owner](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributes#owner())`()` Returns the owner of the file. |
| abstract [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [PosixFilePermission](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission)!\>! | [permissions](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributes#permissions())`()` Returns the permissions of the file. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [BasicFileAttributes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes) |----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [FileTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime)! | [creationTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#creationTime())`()` <br /> Returns the creation time. The creation time is the time that the file was created. If the file system implementation does not support a time stamp to indicate the time when the file was created then this method returns an implementation specific default value, typically the [last-modified-time](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#lastModifiedTime())or a`FileTime`representing the epoch (1970-01-01T00:00:00Z). <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [fileKey](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#fileKey())`()` <br /> Returns an object that uniquely identifies the given file, or`null`if a file key is not available. On some platforms or file systems it is possible to use an identifier, or a combination of identifiers to uniquely identify a file. Such identifiers are important for operations such as file tree traversal in file systems that support [symbolic links](https://developer.android.com/reference/kotlin/java/nio/file/package-summary.html#links) or file systems that allow a file to be an entry in more than one directory. On UNIX file systems, for example, the*device ID* and*inode*are commonly used for such purposes. The file key returned by this method can only be guaranteed to be unique if the file system and files remain static. Whether a file system re-uses identifiers after a file is deleted is implementation dependent and therefore unspecified. File keys returned by this method can be compared for equality and are suitable for use in collections. If the file system and files remain static, and two files are the [same](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#isSameFile(java.nio.file.Path,%20java.nio.file.Path))with non-`null`file keys, then their file keys are equal. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDirectory](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#isDirectory())`()` <br /> Tells whether the file is a directory. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOther](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#isOther())`()` <br /> Tells whether the file is something other than a regular file, directory, or symbolic link. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRegularFile](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#isRegularFile())`()` <br /> Tells whether the file is a regular file with opaque content. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSymbolicLink](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#isSymbolicLink())`()` <br /> Tells whether the file is a symbolic link. <br /> | | [FileTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime)! | [lastAccessTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#lastAccessTime())`()` <br /> Returns the time of last access. If the file system implementation does not support a time stamp to indicate the time of last access then this method returns an implementation specific default value, typically the [last-modified-time](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#lastModifiedTime())or a`FileTime`representing the epoch (1970-01-01T00:00:00Z). <br /> | | [FileTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime)! | [lastModifiedTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#lastModifiedTime())`()` <br /> Returns the time of last modification. If the file system implementation does not support a time stamp to indicate the time of last modification then this method returns an implementation specific default value, typically a`FileTime`representing the epoch (1970-01-01T00:00:00Z). <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [size](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#size())`()` <br /> Returns the size of the file (in bytes). The size may differ from the actual size on the file system due to compression, support for sparse files, or other reasons. The size of files that are not [regular](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes#isRegularFile())files is implementation specific and therefore unspecified. <br /> | ||

## Public methods

### group

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun group(): GroupPrincipal!
```

Returns the group owner of the file.

| Return ||
|----------------------------------------------------------------------------------------------------------|----------------------|
| [GroupPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/GroupPrincipal)! | the file group owner |

**See Also**

- [java.nio.file.attribute.PosixFileAttributeView#setGroup](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributeView#setGroup(java.nio.file.attribute.GroupPrincipal)) 

### owner

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun owner(): UserPrincipal!
```

Returns the owner of the file.

| Return ||
|--------------------------------------------------------------------------------------------------------|----------------|
| [UserPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal)! | the file owner |

**See Also**

- [java.nio.file.attribute.PosixFileAttributeView#setOwner](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileOwnerAttributeView#setOwner(java.nio.file.attribute.UserPrincipal)) 

### permissions

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun permissions(): MutableSet<PosixFilePermission!>!
```

Returns the permissions of the file. The file permissions are returned as a set of [PosixFilePermission](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission) elements. The returned set is a copy of the file permissions and is modifiable. This allows the result to be modified and passed to the [setPermissions](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributeView#setPermissions(kotlin.collections.MutableSet))method to update the file's permissions.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [PosixFilePermission](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission)!>! | the file permissions |

**See Also**

- [java.nio.file.attribute.PosixFileAttributeView#setPermissions](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributeView#setPermissions(kotlin.collections.MutableSet))
