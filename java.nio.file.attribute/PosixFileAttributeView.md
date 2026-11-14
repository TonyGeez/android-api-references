# PosixFileAttributeView

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PosixFileAttributeView

```
interface PosixFileAttributeView : BasicFileAttributeView, FileOwnerAttributeView
```

| [java.nio.file.attribute.PosixFileAttributeView](../java/nio/file/attribute/PosixFileAttributeView.md) |

A file attribute view that provides a view of the file attributes commonly associated with files on file systems used by operating systems that implement the Portable Operating System Interface (POSIX) family of standards.

Operating systems that implement the [POSIX](http://www.opengroup.org) family of standards commonly use file systems that have a file*owner* ,*group-owner* , and related*access permissions*. This file attribute view provides read and write access to these attributes.

The [readAttributes](../java/nio/file/attribute/PosixFileAttributeView.md))method is used to read the file's attributes. The file [owner](../java/nio/file/attribute/PosixFileAttributes.md))is represented by a [UserPrincipal](../java/nio/file/attribute/UserPrincipal.md) that is the identity of the file owner for the purposes of access control. The [group-owner](../java/nio/file/attribute/PosixFileAttributes.md)), represented by a [GroupPrincipal](../java/nio/file/attribute/GroupPrincipal.md), is the identity of the group owner, where a group is an identity created for administrative purposes so as to determine the access rights for the members of the group.

The [permissions](../java/nio/file/attribute/PosixFileAttributes.md))attribute is a set of access permissions. This file attribute view provides access to the nine permission defined by the [PosixFilePermission](../java/nio/file/attribute/PosixFilePermission.md) class. These nine permission bits determine the*read* ,*write* , and*execute*access for the file owner, group, and others (others meaning identities other than the owner and members of the group). Some operating systems and file systems may provide additional permission bits but access to these other bits is not defined by this class in this release.

**Usage Example:**Suppose we need to print out the owner and access permissions of a file: 

```kotlin
Path file = ...
      PosixFileAttributes attrs = Files.getFileAttributeView(file, PosixFileAttributeView.class)
          .readAttributes();
      System.out.format("%s %s%n",
          attrs.owner().getName(),
          PosixFilePermissions.toString(attrs.permissions()));
  
```

## Dynamic Access

Where dynamic access to file attributes is required, the attributes supported by this attribute view are as defined by [BasicFileAttributeView](../java/nio/file/attribute/BasicFileAttributeView.md) and [FileOwnerAttributeView](../java/nio/file/attribute/FileOwnerAttributeView.md), and in addition, the following attributes are supported:

| Name | Type |
| --- | --- |
| "permissions" | [Set](../java/util/Set.md)\< [PosixFilePermission](../java/nio/file/attribute/PosixFilePermission.md)\> |
| "group" | [GroupPrincipal](../java/nio/file/attribute/GroupPrincipal.md) |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

The [getAttribute](../java/nio/file/Files.md))method may be used to read any of these attributes, or any of the attributes defined by [BasicFileAttributeView](../java/nio/file/attribute/BasicFileAttributeView.md) as if by invoking the [readAttributes()](../java/nio/file/attribute/PosixFileAttributeView.md))method.

The [setAttribute](../java/nio/file/Files.md))method may be used to update the file's last modified time, last access time or create time attributes as defined by [BasicFileAttributeView](../java/nio/file/attribute/BasicFileAttributeView.md). It may also be used to update the permissions, owner, or group-owner as if by invoking the [setPermissions](../java/nio/file/attribute/PosixFileAttributeView.md)), [setOwner](../java/nio/file/attribute/FileOwnerAttributeView.md)), and [setGroup](../java/nio/file/attribute/PosixFileAttributeView.md))methods respectively.

## Setting Initial Permissions

Implementations supporting this attribute view may also support setting the initial permissions when creating a file or directory. The initial permissions are provided to the [createFile](../java/nio/file/Files.md))or [createDirectory](../java/nio/file/Files.md))methods as a [FileAttribute](../java/nio/file/attribute/FileAttribute.md) with [name](../java/nio/file/attribute/FileAttribute.md))`"posix:permissions"`and a [value](../java/nio/file/attribute/FileAttribute.md))that is the set of permissions. The following example uses the [asFileAttribute](../java/nio/file/attribute/PosixFilePermissions.md))method to construct a`FileAttribute`when creating a file: 

```kotlin
Path path = ...
      Set<PosixFilePermission> perms =
          EnumSet.of(OWNER_READ, OWNER_WRITE, OWNER_EXECUTE, GROUP_READ);
      Files.createFile(path, PosixFilePermissions.asFileAttribute(perms));
  
```

When the access permissions are set at file creation time then the actual value of the permissions may differ that the value of the attribute object. The reasons for this are implementation specific. On UNIX systems, for example, a process has a*umask* that impacts the permission bits of newly created files. Where an implementation supports the setting of the access permissions, and the underlying file system supports access permissions, then it is required that the value of the actual access permissions will be equal or less than the value of the attribute provided to the [createFile](../java/nio/file/Files.md))or [createDirectory](../java/nio/file/Files.md))methods. In other words, the file may be more secure than requested.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](../java/nio/file/attribute/PosixFileAttributeView.md))`()` Returns the name of the attribute view. |
| abstract [PosixFileAttributes](../java/nio/file/attribute/PosixFileAttributes.md)! | [readAttributes](../java/nio/file/attribute/PosixFileAttributeView.md))`()` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroup](../java/nio/file/attribute/PosixFileAttributeView.md))`(`group:` ` [GroupPrincipal](../java/nio/file/attribute/GroupPrincipal.md)!`)` Updates the file group-owner. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPermissions](../java/nio/file/attribute/PosixFileAttributeView.md))`(`perms:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [PosixFilePermission](../java/nio/file/attribute/PosixFilePermission.md)!>!`)` Updates the file permissions. |

| Inherited functions ||
|---|---|
| From class [FileOwnerAttributeView](../java/nio/file/attribute/FileOwnerAttributeView.md) |--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [UserPrincipal](../java/nio/file/attribute/UserPrincipal.md)! | [getOwner](../java/nio/file/attribute/FileOwnerAttributeView.md))`()` <br /> Read the file owner. It is implementation specific if the file owner can be a [group](../java/nio/file/attribute/GroupPrincipal.md). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOwner](../java/nio/file/attribute/FileOwnerAttributeView.md))`(`owner:` ` [UserPrincipal](../java/nio/file/attribute/UserPrincipal.md)!`)` <br /> Updates the file owner. It is implementation specific if the file owner can be a [group](../java/nio/file/attribute/GroupPrincipal.md). To ensure consistent and correct behavior across platforms it is recommended that this method should only be used to set the file owner to a user principal that is not a group. <br /> | ||
| From class [BasicFileAttributeView](../java/nio/file/attribute/BasicFileAttributeView.md) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimes](../java/nio/file/attribute/BasicFileAttributeView.md))`(`lastModifiedTime:` ` [FileTime](../java/nio/file/attribute/FileTime.md)!`, `lastAccessTime:` ` [FileTime](../java/nio/file/attribute/FileTime.md)!`, `createTime:` ` [FileTime](../java/nio/file/attribute/FileTime.md)!`)` <br /> Updates any or all of the file's last modified time, last access time, and create time attributes. This method updates the file's timestamp attributes. The values are converted to the epoch and precision supported by the file system. Converting from finer to coarser granularities result in precision loss. The behavior of this method when attempting to set a timestamp that is not supported or to a value that is outside the range supported by the underlying file store is not defined. It may or not fail by throwing an`IOException`. If any of the`lastModifiedTime`,`lastAccessTime`, or`createTime`parameters has the value`null`then the corresponding timestamp is not changed. An implementation may require to read the existing values of the file attributes when only some, but not all, of the timestamp attributes are updated. Consequently, this method may not be an atomic operation with respect to other file system operations. Reading and re-writing existing values may also result in precision loss. If all of the`lastModifiedTime`,`lastAccessTime`and`createTime`parameters are`null`then this method has no effect. **Usage Example:**Suppose we want to change a file's last access time. ```kotlin Path path = ... FileTime time = ... Files.getFileAttributeView(path, BasicFileAttributeView.class).setTimes(null, time, null); ``` <br /> | ||

## Public methods

### name

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun name(): String!
```

Returns the name of the attribute view. Attribute views of this type have the name`"posix"`.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the attribute view |

### readAttributes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readAttributes(): PosixFileAttributes!
```

| Return ||
|--------------------------------------------------------------------------------------------------------------------|---------------------|
| [PosixFileAttributes](../java/nio/file/attribute/PosixFileAttributes.md)! | the file attributes |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, and it denies [RuntimePermission](../java/lang/RuntimePermission.md)`("accessUserInformation")`or its [checkRead](../java/lang/SecurityManager.md))method denies read access to the file. |

### setGroup

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setGroup(group: GroupPrincipal!): Unit
```

Updates the file group-owner.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| `group` | [GroupPrincipal](../java/nio/file/attribute/GroupPrincipal.md)!:the new file group-owner |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, it denies [RuntimePermission](../java/lang/RuntimePermission.md)`("accessUserInformation")`or its [checkWrite](../java/lang/SecurityManager.md))method denies write access to the file. |

### setPermissions

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setPermissions(perms: MutableSet<PosixFilePermission!>!): Unit
```

Updates the file permissions.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `perms` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [PosixFilePermission](../java/nio/file/attribute/PosixFilePermission.md)!\>!:the new set of permissions |

| Exceptions ||
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the sets contains elements that are not of type`PosixFilePermission` |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, and it denies [RuntimePermission](../java/lang/RuntimePermission.md)`("accessUserInformation")`or its [checkWrite](../java/lang/SecurityManager.md))method denies write access to the file. |
| --- | --- |
