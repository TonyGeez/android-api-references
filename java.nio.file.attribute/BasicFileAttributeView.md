# BasicFileAttributeView

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BasicFileAttributeView

```
interface BasicFileAttributeView : FileAttributeView
```

| [java.nio.file.attribute.BasicFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributeView#) |

| Known Direct Subclasses [DosFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/DosFileAttributeView), [PosixFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributeView) |-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DosFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/DosFileAttributeView) | A file attribute view that provides a view of the legacy "DOS" file attributes. | | [PosixFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributeView) | A file attribute view that provides a view of the file attributes commonly associated with files on file systems used by operating systems that implement the Portable Operating System Interface (POSIX) family of standards. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A file attribute view that provides a view of a*basic set* of file attributes common to many file systems. The basic set of file attributes consist of*mandatory* and*optional* file attributes as defined by the [BasicFileAttributes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes) interface.

The file attributes are retrieved from the file system as a*bulk operation* by invoking the [readAttributes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributeView#readAttributes())method. This class also defines the [setTimes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributeView#setTimes(java.nio.file.attribute.FileTime,%20java.nio.file.attribute.FileTime,%20java.nio.file.attribute.FileTime))method to update the file's time attributes.

Where dynamic access to file attributes is required, the attributes supported by this attribute view have the following names and types:

| Name | Type |
| --- | --- |
| "lastModifiedTime" | [FileTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime) |
| "lastAccessTime" | [FileTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime) |
| "creationTime" | [FileTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime) |
| --- | --- |
| "size" | [Long](https://developer.android.com/reference/kotlin/java/lang/Long.html#) |
| "isRegularFile" | [Boolean](https://developer.android.com/reference/kotlin/java/lang/Boolean.html#) |
| "isDirectory" | [Boolean](https://developer.android.com/reference/kotlin/java/lang/Boolean.html#) |
| --- | --- |
| "isSymbolicLink" | [Boolean](https://developer.android.com/reference/kotlin/java/lang/Boolean.html#) |
| "isOther" | [Boolean](https://developer.android.com/reference/kotlin/java/lang/Boolean.html#) |
| "fileKey" | [Object](https://developer.android.com/reference/kotlin/java/lang/Object.html#) |
|--------------------|---------------------------------------------------------------------------------------------|

The [getAttribute](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#getAttribute(java.nio.file.Path,%20kotlin.String,%20java.nio.file.LinkOption))method may be used to read any of these attributes as if by invoking the [readAttributes()](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributeView#readAttributes())method.

The [setAttribute](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#setAttribute(java.nio.file.Path,%20kotlin.String,%20kotlin.Any,%20java.nio.file.LinkOption))method may be used to update the file's last modified time, last access time or create time attributes as if by invoking the [setTimes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributeView#setTimes(java.nio.file.attribute.FileTime,%20java.nio.file.attribute.FileTime,%20java.nio.file.attribute.FileTime))method.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributeView#name())`()` Returns the name of the attribute view. |
| abstract [BasicFileAttributes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes)! | [readAttributes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributeView#readAttributes())`()` Reads the basic file attributes as a bulk operation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributeView#setTimes(java.nio.file.attribute.FileTime,%20java.nio.file.attribute.FileTime,%20java.nio.file.attribute.FileTime))`(`lastModifiedTime:` ` [FileTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime)!`, `lastAccessTime:` ` [FileTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime)!`, `createTime:` ` [FileTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime)!`)` Updates any or all of the file's last modified time, last access time, and create time attributes. |
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
| [BasicFileAttributes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes)! | the file attributes |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, its [checkRead](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String))method is invoked to check read access to the file |

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
| `lastModifiedTime` | [FileTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime)!:the new last modified time, or`null`to not change the value |
| `lastAccessTime` | [FileTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime)!:the last access time, or`null`to not change the value |
| `createTime` | [FileTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime)!:the file's create time, or`null`to not change the value |
| --- | --- |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, its [checkWrite](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String))method is invoked to check write access to the file |

**See Also**

- [java.nio.file.Files#setLastModifiedTime](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#setLastModifiedTime(java.nio.file.Path,%20java.nio.file.attribute.FileTime))
