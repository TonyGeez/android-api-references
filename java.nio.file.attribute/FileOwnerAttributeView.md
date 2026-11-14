# FileOwnerAttributeView

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileOwnerAttributeView

```
interface FileOwnerAttributeView : FileAttributeView
```

| [java.nio.file.attribute.FileOwnerAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileOwnerAttributeView#) |

| Known Direct Subclasses [AclFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclFileAttributeView), [PosixFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributeView) |-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AclFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclFileAttributeView) | A file attribute view that supports reading or updating a file's Access Control Lists (ACL) or file owner attributes. | | [PosixFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributeView) | A file attribute view that provides a view of the file attributes commonly associated with files on file systems used by operating systems that implement the Portable Operating System Interface (POSIX) family of standards. | |

A file attribute view that supports reading or updating the owner of a file. This file attribute view is intended for file system implementations that support a file attribute that represents an identity that is the owner of the file. Often the owner of a file is the identity of the entity that created the file.

The [getOwner](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileOwnerAttributeView#getOwner())or [setOwner](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileOwnerAttributeView#setOwner(java.nio.file.attribute.UserPrincipal))methods may be used to read or update the owner of the file.

The [getAttribute](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#getAttribute(java.nio.file.Path,%20kotlin.String,%20java.nio.file.LinkOption))and [setAttribute](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#setAttribute(java.nio.file.Path,%20kotlin.String,%20kotlin.Any,%20java.nio.file.LinkOption))methods may also be used to read or update the owner. In that case, the owner attribute is identified by the name`"owner"`, and the value of the attribute is a [UserPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [UserPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal)! | [getOwner](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileOwnerAttributeView#getOwner())`()` Read the file owner. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileOwnerAttributeView#name())`()` Returns the name of the attribute view. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOwner](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileOwnerAttributeView#setOwner(java.nio.file.attribute.UserPrincipal))`(`owner:` ` [UserPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal)!`)` Updates the file owner. |

## Public methods

### getOwner

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getOwner(): UserPrincipal!
```

Read the file owner.

It is implementation specific if the file owner can be a [group](https://developer.android.com/reference/kotlin/java/nio/file/attribute/GroupPrincipal).

| Return ||
|--------------------------------------------------------------------------------------------------------|----------------|
| [UserPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal)! | the file owner |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, and it denies [RuntimePermission](https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#)`("accessUserInformation")`or its [checkRead](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String))method denies read access to the file. |

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

It is implementation specific if the file owner can be a [group](https://developer.android.com/reference/kotlin/java/nio/file/attribute/GroupPrincipal). To ensure consistent and correct behavior across platforms it is recommended that this method should only be used to set the file owner to a user principal that is not a group.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `owner` | [UserPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal)!:the new file owner |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs, or the`owner`parameter is a group and this implementation does not support setting the owner to a group |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, and it denies [RuntimePermission](https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#)`("accessUserInformation")`or its [checkWrite](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String))method denies write access to the file. |
