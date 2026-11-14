# FileAttributeView

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileAttributeView

```
interface FileAttributeView : AttributeView
```

| [java.nio.file.attribute.FileAttributeView](../java/nio/file/attribute/FileAttributeView.md) |

| Known Direct Subclasses [BasicFileAttributeView](../java/nio/file/attribute/BasicFileAttributeView.md), [FileOwnerAttributeView](../java/nio/file/attribute/FileOwnerAttributeView.md), [UserDefinedFileAttributeView](../java/nio/file/attribute/UserDefinedFileAttributeView.md) |-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------| | [BasicFileAttributeView](../java/nio/file/attribute/BasicFileAttributeView.md) | A file attribute view that provides a view of a*basic set*of file attributes common to many file systems. | | [FileOwnerAttributeView](../java/nio/file/attribute/FileOwnerAttributeView.md) | A file attribute view that supports reading or updating the owner of a file. | | [UserDefinedFileAttributeView](../java/nio/file/attribute/UserDefinedFileAttributeView.md) | A file attribute view that provides a view of a file's user-defined attributes, sometimes known as*extended attributes*. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AclFileAttributeView](../java/nio/file/attribute/AclFileAttributeView.md), [DosFileAttributeView](../java/nio/file/attribute/DosFileAttributeView.md), [PosixFileAttributeView](../java/nio/file/attribute/PosixFileAttributeView.md) [PosixFileAttributeView](../java/nio/file/attribute/PosixFileAttributeView.md) |-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AclFileAttributeView](../java/nio/file/attribute/AclFileAttributeView.md) | A file attribute view that supports reading or updating a file's Access Control Lists (ACL) or file owner attributes. | | [DosFileAttributeView](../java/nio/file/attribute/DosFileAttributeView.md) | A file attribute view that provides a view of the legacy "DOS" file attributes. | | [PosixFileAttributeView](../java/nio/file/attribute/PosixFileAttributeView.md) | A file attribute view that provides a view of the file attributes commonly associated with files on file systems used by operating systems that implement the Portable Operating System Interface (POSIX) family of standards. | | [PosixFileAttributeView](../java/nio/file/attribute/PosixFileAttributeView.md) | A file attribute view that provides a view of the file attributes commonly associated with files on file systems used by operating systems that implement the Portable Operating System Interface (POSIX) family of standards. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An attribute view that is a read-only or updatable view of non-opaque values associated with a file in a filesystem. This interface is extended or implemented by specific file attribute views that define methods to read and/or update the attributes of a file.

## Summary

| Inherited functions ||
|---|---|
| From class [AttributeView](../java/nio/file/attribute/AttributeView.md) |-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](../java/nio/file/attribute/AttributeView.md))`()` <br /> Returns the name of the attribute view. <br /> | ||
