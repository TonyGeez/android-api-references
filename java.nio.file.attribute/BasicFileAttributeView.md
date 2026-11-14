# BasicFileAttributeView

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BasicFileAttributeView

```
interface BasicFileAttributeView : FileAttributeView
```

| [java.nio.file.attribute.BasicFileAttributeView](BasicFileAttributeView.md) |

| Known Direct Subclasses [DosFileAttributeView](DosFileAttributeView.md), [PosixFileAttributeView](PosixFileAttributeView.md) |-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DosFileAttributeView](DosFileAttributeView.md) | A file attribute view that provides a view of the legacy "DOS" file attributes. | | [PosixFileAttributeView](PosixFileAttributeView.md) | A file attribute view that provides a view of the file attributes commonly associated with files on file systems used by operating systems that implement the Portable Operating System Interface (POSIX) family of standards. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A file attribute view that provides a view of a*basic set* of file attributes common to many file systems. The basic set of file attributes consist of*mandatory* and*optional* file attributes as defined by the [BasicFileAttributes](BasicFileAttributes.md) interface.

The file attributes are retrieved from the file system as a*bulk operation* by invoking the [readAttributes](BasicFileAttributeView.md))method. This class also defines the [setTimes](BasicFileAttributeView.md))method to update the file's time attributes.

Where dynamic access to file attributes is required, the attributes supported by this attribute view have the following names and types:

| Name | Type |
| --- | --- |
| "lastModifiedTime" | [FileTime](FileTime.md) |
| "lastAccessTime" | [FileTime](FileTime.md) |
| "creationTime" | [FileTime](FileTime.md) |
| --- | --- |
| "size" | [Long](../java.lang/Long.md) |
| "isRegularFile" | [Boolean](../java.lang/Boolean.md) |
| "isDirectory" | [Boolean](../java.lang/Boolean.md) |
| --- | --- |
| "isSymbolicLink" | [Boolean](../java.lang/Boolean.md) |
| "isOther" | [Boolean](../java.lang/Boolean.md) |
| "fileKey" | [Object](../java.lang/Object.md) |
|--------------------|---------------------------------------------------------------------------------------------|

The [getAttribute](../java.nio.file/Files.md))method may be used to read any of these attributes as if by invoking the [readAttributes()](BasicFileAttributeView.md))method.

The [setAttribute](../java.nio.file/Files.md))method may be used to update the file's last modified time, last access time or create time attributes as if by invoking the [setTimes](BasicFileAttributeView.md))method.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](BasicFileAttributeView.md))`()` Returns the name of the attribute view. |
| abstract [BasicFileAttributes](BasicFileAttributes.md)! | [readAttributes](BasicFileAttributeView.md))`()` Reads the basic file attributes as a bulk operation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimes](BasicFileAttributeView.md))`(`lastModifiedTime:` ` [FileTime](FileTime.md)!`, `lastAccessTime:` ` [FileTime](FileTime.md)!`, `createTime:` ` [FileTime](FileTime.md)!`)` Updates any or all of the file's last modified time, last access time, and create time attributes. |
| --- | --- |

## Public methods

### name

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun name(): String!
```

Returns the name of the attribute view. Attribute views of this type have the name`"basic"`.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the attribute view |

### readAttributes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readAttributes(): BasicFileAttributes!
```

Reads the basic file attributes as a bulk operation.

It is implementation specific if all file attributes are read as an atomic operation with respect to other file system operations.

| Return ||
|--------------------------------------------------------------------------------------------------------------------|---------------------|
| [BasicFileAttributes](BasicFileAttributes.md)! | the file attributes |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, its [checkRead](../java.lang/SecurityManager.md))method is invoked to check read access to the file |

### setTimes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTimes(
    lastModifiedTime: FileTime!, 
    lastAccessTime: FileTime!, 
    createTime: FileTime!
): Unit
```

Updates any or all of the file's last modified time, last access time, and create time attributes.

This method updates the file's timestamp attributes. The values are converted to the epoch and precision supported by the file system. Converting from finer to coarser granularities result in precision loss. The behavior of this method when attempting to set a timestamp that is not supported or to a value that is outside the range supported by the underlying file store is not defined. It may or not fail by throwing an`IOException`.

If any of the`lastModifiedTime`,`lastAccessTime`, or`createTime`parameters has the value`null`then the corresponding timestamp is not changed. An implementation may require to read the existing values of the file attributes when only some, but not all, of the timestamp attributes are updated. Consequently, this method may not be an atomic operation with respect to other file system operations. Reading and re-writing existing values may also result in precision loss. If all of the`lastModifiedTime`,`lastAccessTime`and`createTime`parameters are`null`then this method has no effect.

**Usage Example:**Suppose we want to change a file's last access time. 

```kotlin
Path path = ...
     FileTime time = ...
     Files.getFileAttributeView(path, BasicFileAttributeView.class).setTimes(null, time, null);
  
```

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `lastModifiedTime` | [FileTime](FileTime.md)!:the new last modified time, or`null`to not change the value |
| `lastAccessTime` | [FileTime](FileTime.md)!:the last access time, or`null`to not change the value |
| `createTime` | [FileTime](FileTime.md)!:the file's create time, or`null`to not change the value |
| --- | --- |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, its [checkWrite](../java.lang/SecurityManager.md))method is invoked to check write access to the file |

**See Also**

- [java.nio.file.Files#setLastModifiedTime](../java.nio.file/Files.md))
