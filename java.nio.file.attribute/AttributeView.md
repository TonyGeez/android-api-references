# AttributeView

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AttributeView

```
interface AttributeView
```

| [java.nio.file.attribute.AttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AttributeView#) |

| Known Direct Subclasses [FileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttributeView), [FileStoreAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileStoreAttributeView) |-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [FileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttributeView) | An attribute view that is a read-only or updatable view of non-opaque values associated with a file in a filesystem. | | [FileStoreAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileStoreAttributeView) | An attribute view that is a read-only or updatable view of the attributes of a [java.nio.file.FileStore](https://developer.android.com/reference/kotlin/java/nio/file/FileStore.html#). | |

| Known Indirect Subclasses [AclFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclFileAttributeView), [BasicFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributeView), [DosFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/DosFileAttributeView), [FileOwnerAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileOwnerAttributeView), [PosixFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributeView), [PosixFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributeView), [UserDefinedFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserDefinedFileAttributeView) |-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AclFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclFileAttributeView) | A file attribute view that supports reading or updating a file's Access Control Lists (ACL) or file owner attributes. | | [BasicFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributeView) | A file attribute view that provides a view of a*basic set*of file attributes common to many file systems. | | [DosFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/DosFileAttributeView) | A file attribute view that provides a view of the legacy "DOS" file attributes. | | [FileOwnerAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileOwnerAttributeView) | A file attribute view that supports reading or updating the owner of a file. | | [PosixFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributeView) | A file attribute view that provides a view of the file attributes commonly associated with files on file systems used by operating systems that implement the Portable Operating System Interface (POSIX) family of standards. | | [PosixFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributeView) | A file attribute view that provides a view of the file attributes commonly associated with files on file systems used by operating systems that implement the Portable Operating System Interface (POSIX) family of standards. | | [UserDefinedFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserDefinedFileAttributeView) | A file attribute view that provides a view of a file's user-defined attributes, sometimes known as*extended attributes*. | |

An object that provides a read-only or updatable*view*of non-opaque values associated with an object in a filesystem. This interface is extended or implemented by specific attribute views that define the attributes supported by the view. A specific attribute view will typically define type-safe methods to read or update the attributes that it supports.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AttributeView#name())`()` Returns the name of the attribute view. |

## Public methods

### name

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun name(): String!
```

Returns the name of the attribute view.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the attribute view |
