# FileOwnerAttributeView

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileOwnerAttributeView

```
interface FileOwnerAttributeView : FileAttributeView
```

| [java.nio.file.attribute.FileOwnerAttributeView](FileOwnerAttributeView.md) |

| Known Direct Subclasses [AclFileAttributeView](AclFileAttributeView.md), [PosixFileAttributeView](PosixFileAttributeView.md) |-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AclFileAttributeView](AclFileAttributeView.md) | A file attribute view that supports reading or updating a file's Access Control Lists (ACL) or file owner attributes. | | [PosixFileAttributeView](PosixFileAttributeView.md) | A file attribute view that provides a view of the file attributes commonly associated with files on file systems used by operating systems that implement the Portable Operating System Interface (POSIX) family of standards. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A file attribute view that supports reading or updating the owner of a file. This file attribute view is intended for file system implementations that support a file attribute that represents an identity that is the owner of the file. Often the owner of a file is the identity of the entity that created the file.

The [getOwner](FileOwnerAttributeView.md))or [setOwner](FileOwnerAttributeView.md))methods may be used to read or update the owner of the file.

The [getAttribute](../java.nio.file/Files.md))and [setAttribute](../java.nio.file/Files.md))methods may also be used to read or update the owner. In that case, the owner attribute is identified by the name`"owner"`, and the value of the attribute is a [UserPrincipal](UserPrincipal.md).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [UserPrincipal](UserPrincipal.md)! | [getOwner](FileOwnerAttributeView.md))`()` Read the file owner. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](FileOwnerAttributeView.md))`()` Returns the name of the attribute view. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOwner](FileOwnerAttributeView.md))`(`owner:` ` [UserPrincipal](UserPrincipal.md)!`)` Updates the file owner. |
| --- | --- |

## Public methods

### getOwner

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getOwner(): UserPrincipal!
```

Read the file owner.

It is implementation specific if the file owner can be a [group](GroupPrincipal.md).

| Return ||
|--------------------------------------------------------------------------------------------------------|----------------|
| [UserPrincipal](UserPrincipal.md)! | the file owner |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, and it denies [RuntimePermission](../java.lang/RuntimePermission.md)`("accessUserInformation")`or its [checkRead](../java.lang/SecurityManager.md))method denies read access to the file. |

### name

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun name(): String!
```

Returns the name of the attribute view. Attribute views of this type have the name`"owner"`.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the attribute view |

### setOwner

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setOwner(owner: UserPrincipal!): Unit
```

Updates the file owner.

It is implementation specific if the file owner can be a [group](GroupPrincipal.md). To ensure consistent and correct behavior across platforms it is recommended that this method should only be used to set the file owner to a user principal that is not a group.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `owner` | [UserPrincipal](UserPrincipal.md)!:the new file owner |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs, or the`owner`parameter is a group and this implementation does not support setting the owner to a group |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, and it denies [RuntimePermission](../java.lang/RuntimePermission.md)`("accessUserInformation")`or its [checkWrite](../java.lang/SecurityManager.md))method denies write access to the file. |
