# DosFileAttributeView

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DosFileAttributeView

```
interface DosFileAttributeView : BasicFileAttributeView
```

| [java.nio.file.attribute.DosFileAttributeView](../java/nio/file/attribute/DosFileAttributeView.md) |

A file attribute view that provides a view of the legacy "DOS" file attributes. These attributes are supported by file systems such as the File Allocation Table (FAT) format commonly used in*consumer devices*.

A`DosFileAttributeView`is a [BasicFileAttributeView](../java/nio/file/attribute/BasicFileAttributeView.md) that additionally supports access to the set of DOS attribute flags that are used to indicate if the file is read-only, hidden, a system file, or archived.

Where dynamic access to file attributes is required, the attributes supported by this attribute view are as defined by`BasicFileAttributeView`, and in addition, the following attributes are supported:

| Name | Type |
| --- | --- |
| readonly | [Boolean](../java/lang/Boolean.md) |
| hidden | [Boolean](../java/lang/Boolean.md) |
| system | [Boolean](../java/lang/Boolean.md) |
| --- | --- |
| archive | [Boolean](../java/lang/Boolean.md) |
|----------|-----------------------------------------------------------------------------------|

The [getAttribute](../java/nio/file/Files.md))method may be used to read any of these attributes, or any of the attributes defined by [BasicFileAttributeView](../java/nio/file/attribute/BasicFileAttributeView.md) as if by invoking the [readAttributes()](../java/nio/file/attribute/DosFileAttributeView.md))method.

The [setAttribute](../java/nio/file/Files.md))method may be used to update the file's last modified time, last access time or create time attributes as defined by [BasicFileAttributeView](../java/nio/file/attribute/BasicFileAttributeView.md). It may also be used to update the DOS attributes as if by invoking the [setReadOnly](../java/nio/file/attribute/DosFileAttributeView.md)), [setHidden](../java/nio/file/attribute/DosFileAttributeView.md)), [setSystem](../java/nio/file/attribute/DosFileAttributeView.md)), and [setArchive](../java/nio/file/attribute/DosFileAttributeView.md))methods respectively.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](../java/nio/file/attribute/DosFileAttributeView.md))`()` Returns the name of the attribute view. |
| abstract [DosFileAttributes](../java/nio/file/attribute/DosFileAttributes.md)! | [readAttributes](../java/nio/file/attribute/DosFileAttributeView.md))`()` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setArchive](../java/nio/file/attribute/DosFileAttributeView.md))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Updates the value of the archive attribute. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHidden](../java/nio/file/attribute/DosFileAttributeView.md))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Updates the value of the hidden attribute. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReadOnly](../java/nio/file/attribute/DosFileAttributeView.md))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Updates the value of the read-only attribute. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSystem](../java/nio/file/attribute/DosFileAttributeView.md))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Updates the value of the system attribute. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [BasicFileAttributeView](../java/nio/file/attribute/BasicFileAttributeView.md) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimes](../java/nio/file/attribute/BasicFileAttributeView.md))`(`lastModifiedTime:` ` [FileTime](../java/nio/file/attribute/FileTime.md)!`, `lastAccessTime:` ` [FileTime](../java/nio/file/attribute/FileTime.md)!`, `createTime:` ` [FileTime](../java/nio/file/attribute/FileTime.md)!`)` <br /> Updates any or all of the file's last modified time, last access time, and create time attributes. This method updates the file's timestamp attributes. The values are converted to the epoch and precision supported by the file system. Converting from finer to coarser granularities result in precision loss. The behavior of this method when attempting to set a timestamp that is not supported or to a value that is outside the range supported by the underlying file store is not defined. It may or not fail by throwing an`IOException`. If any of the`lastModifiedTime`,`lastAccessTime`, or`createTime`parameters has the value`null`then the corresponding timestamp is not changed. An implementation may require to read the existing values of the file attributes when only some, but not all, of the timestamp attributes are updated. Consequently, this method may not be an atomic operation with respect to other file system operations. Reading and re-writing existing values may also result in precision loss. If all of the`lastModifiedTime`,`lastAccessTime`and`createTime`parameters are`null`then this method has no effect. **Usage Example:**Suppose we want to change a file's last access time. ```kotlin Path path = ... FileTime time = ... Files.getFileAttributeView(path, BasicFileAttributeView.class).setTimes(null, time, null); ``` <br /> | ||

## Public methods

### name

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun name(): String!
```

Returns the name of the attribute view. Attribute views of this type have the name`"dos"`.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the attribute view |

### readAttributes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readAttributes(): DosFileAttributes!
```

| Return ||
|----------------------------------------------------------------------------------------------------------------|---------------------|
| [DosFileAttributes](../java/nio/file/attribute/DosFileAttributes.md)! | the file attributes |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, its [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the file |

### setArchive

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setArchive(value: Boolean): Unit
```

Updates the value of the archive attribute.

It is implementation specific if the attribute can be updated as an atomic operation with respect to other file system operations. An implementation may, for example, require to read the existing value of the DOS attribute in order to update this attribute.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value of the attribute |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default, and a security manager is installed, its [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access to the file |

### setHidden

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setHidden(value: Boolean): Unit
```

Updates the value of the hidden attribute.

It is implementation specific if the attribute can be updated as an atomic operation with respect to other file system operations. An implementation may, for example, require to read the existing value of the DOS attribute in order to update this attribute.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value of the attribute |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default, and a security manager is installed, its [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access to the file |

### setReadOnly

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setReadOnly(value: Boolean): Unit
```

Updates the value of the read-only attribute.

It is implementation specific if the attribute can be updated as an atomic operation with respect to other file system operations. An implementation may, for example, require to read the existing value of the DOS attribute in order to update this attribute.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value of the attribute |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default, and a security manager is installed, its [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access to the file |

### setSystem

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSystem(value: Boolean): Unit
```

Updates the value of the system attribute.

It is implementation specific if the attribute can be updated as an atomic operation with respect to other file system operations. An implementation may, for example, require to read the existing value of the DOS attribute in order to update this attribute.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value of the attribute |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default, and a security manager is installed, its [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access to the file |
