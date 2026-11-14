# AttributeView

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AttributeView

```
interface AttributeView
```

| [java.nio.file.attribute.AttributeView](AttributeView.md) |

| Known Direct Subclasses [FileAttributeView](FileAttributeView.md), [FileStoreAttributeView](FileStoreAttributeView.md) |-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [FileAttributeView](FileAttributeView.md) | An attribute view that is a read-only or updatable view of non-opaque values associated with a file in a filesystem. | | [FileStoreAttributeView](FileStoreAttributeView.md) | An attribute view that is a read-only or updatable view of the attributes of a [java.nio.file.FileStore](../java.nio.file/FileStore.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AclFileAttributeView](AclFileAttributeView.md), [BasicFileAttributeView](BasicFileAttributeView.md), [DosFileAttributeView](DosFileAttributeView.md), [FileOwnerAttributeView](FileOwnerAttributeView.md), [PosixFileAttributeView](PosixFileAttributeView.md), [PosixFileAttributeView](PosixFileAttributeView.md), [UserDefinedFileAttributeView](UserDefinedFileAttributeView.md) |-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AclFileAttributeView](AclFileAttributeView.md) | A file attribute view that supports reading or updating a file's Access Control Lists (ACL) or file owner attributes. | | [BasicFileAttributeView](BasicFileAttributeView.md) | A file attribute view that provides a view of a*basic set*of file attributes common to many file systems. | | [DosFileAttributeView](DosFileAttributeView.md) | A file attribute view that provides a view of the legacy "DOS" file attributes. | | [FileOwnerAttributeView](FileOwnerAttributeView.md) | A file attribute view that supports reading or updating the owner of a file. | | [PosixFileAttributeView](PosixFileAttributeView.md) | A file attribute view that provides a view of the file attributes commonly associated with files on file systems used by operating systems that implement the Portable Operating System Interface (POSIX) family of standards. | | [PosixFileAttributeView](PosixFileAttributeView.md) | A file attribute view that provides a view of the file attributes commonly associated with files on file systems used by operating systems that implement the Portable Operating System Interface (POSIX) family of standards. | | [UserDefinedFileAttributeView](UserDefinedFileAttributeView.md) | A file attribute view that provides a view of a file's user-defined attributes, sometimes known as*extended attributes*. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An object that provides a read-only or updatable*view*of non-opaque values associated with an object in a filesystem. This interface is extended or implemented by specific attribute views that define the attributes supported by the view. A specific attribute view will typically define type-safe methods to read or update the attributes that it supports.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](AttributeView.md))`()` Returns the name of the attribute view. |

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
