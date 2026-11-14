# AclFileAttributeView

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AclFileAttributeView

```
interface AclFileAttributeView : FileOwnerAttributeView
```

| [java.nio.file.attribute.AclFileAttributeView](AclFileAttributeView.md) |

A file attribute view that supports reading or updating a file's Access Control Lists (ACL) or file owner attributes.

ACLs are used to specify access rights to file system objects. An ACL is an ordered list of [access-control-entries](AclEntry.md), each specifying a [UserPrincipal](UserPrincipal.md) and the level of access for that user principal. This file attribute view defines the [getAcl](AclFileAttributeView.md)), and [setAcl](AclFileAttributeView.md))methods to read and write ACLs based on the ACL model specified in [*RFC 3530: Network File System (NFS) version 4 Protocol*](http://www.ietf.org/rfc/rfc3530.txt). This file attribute view is intended for file system implementations that support the NFSv4 ACL model or have a*well-defined*mapping between the NFSv4 ACL model and the ACL model used by the file system. The details of such mapping are implementation dependent and are therefore unspecified.

This class also extends`FileOwnerAttributeView`so as to define methods to get and set the file owner.

When a file system provides access to a set of [file-systems](../java.nio.file/FileStore.md) that are not homogeneous then only some of the file systems may support ACLs. The java.nio.file.FileStore#supportsFileAttributeView method can be used to test if a file system supports ACLs.

## Interoperability

RFC 3530 allows for special user identities to be used on platforms that support the POSIX defined access permissions. The special user identities are "`OWNER@`", "`GROUP@`", and "`EVERYONE@`". When both the`AclFileAttributeView`and the [PosixFileAttributeView](PosixFileAttributeView.md) are supported then these special user identities may be included in ACL [entries](AclEntry.md) that are read or written. The file system's [UserPrincipalLookupService](UserPrincipalLookupService.md) may be used to obtain a [UserPrincipal](UserPrincipal.md) to represent these special identities by invoking the [lookupPrincipalByName](UserPrincipalLookupService.md))method.

**Usage Example:**Suppose we wish to add an entry to an existing ACL to grant "joe" access: 

```kotlin
// lookup "joe"
      UserPrincipal joe = file.getFileSystem().getUserPrincipalLookupService()
          .lookupPrincipalByName("joe");
 
      // get view
      AclFileAttributeView view = Files.getFileAttributeView(file, AclFileAttributeView.class);
 
      // create ACE to give "joe" read access
      AclEntry entry = AclEntry.newBuilder()
          .setType(AclEntryType.ALLOW)
          .setPrincipal(joe)
          .setPermissions(AclEntryPermission.READ_DATA, AclEntryPermission.READ_ATTRIBUTES)
          .build();
 
      // read ACL, insert ACE, re-write ACL
      List<AclEntry> acl = view.getAcl();
      acl.add(0, entry);   // insert before any DENY entries
      view.setAcl(acl);
  
```

## Dynamic Access

Where dynamic access to file attributes is required, the attributes supported by this attribute view are as follows:

| Name | Type |
| --- | --- |
| "acl" | [List](../java.util/List.md)\< [AclEntry](AclEntry.md)\> |
| "owner" | [UserPrincipal](UserPrincipal.md) |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

The [getAttribute](../java.nio.file/Files.md))method may be used to read the ACL or owner attributes as if by invoking the [getAcl](AclFileAttributeView.md))or [getOwner](FileOwnerAttributeView.md))methods.

The [setAttribute](../java.nio.file/Files.md))method may be used to update the ACL or owner attributes as if by invoking the [setAcl](AclFileAttributeView.md))or [setOwner](FileOwnerAttributeView.md))methods.

## Setting the ACL when creating a file

Implementations supporting this attribute view may also support setting the initial ACL when creating a file or directory. The initial ACL may be provided to methods such as [createFile](../java.nio.file/Files.md))or [createDirectory](../java.nio.file/Files.md))as an [FileAttribute](FileAttribute.md) with [name](FileAttribute.md))`"acl:acl"`and a [value](FileAttribute.md))that is the list of`AclEntry`objects.

Where an implementation supports an ACL model that differs from the NFSv4 defined ACL model then setting the initial ACL when creating the file must translate the ACL to the model supported by the file system. Methods that create a file should reject (by throwing [IOException](../java.io/IOException.md)) any attempt to create a file that would be less secure as a result of the translation.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AclEntry](AclEntry.md)!\>! | [getAcl](AclFileAttributeView.md))`()` Reads the access control list. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](AclFileAttributeView.md))`()` Returns the name of the attribute view. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAcl](AclFileAttributeView.md))`(`acl:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AclEntry](AclEntry.md)!>!`)` Updates (replace) the access control list. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [FileOwnerAttributeView](FileOwnerAttributeView.md) |--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [UserPrincipal](UserPrincipal.md)! | [getOwner](FileOwnerAttributeView.md))`()` <br /> Read the file owner. It is implementation specific if the file owner can be a [group](GroupPrincipal.md). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOwner](FileOwnerAttributeView.md))`(`owner:` ` [UserPrincipal](UserPrincipal.md)!`)` <br /> Updates the file owner. It is implementation specific if the file owner can be a [group](GroupPrincipal.md). To ensure consistent and correct behavior across platforms it is recommended that this method should only be used to set the file owner to a user principal that is not a group. <br /> | ||

## Public methods

### getAcl

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAcl(): MutableList<AclEntry!>!
```

Reads the access control list.

When the file system uses an ACL model that differs from the NFSv4 defined ACL model, then this method returns an ACL that is the translation of the ACL to the NFSv4 ACL model.

The returned list is modifiable so as to facilitate changes to the existing ACL. The [setAcl](AclFileAttributeView.md))method is used to update the file's ACL attribute.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AclEntry](AclEntry.md)!>! | an ordered list of [entries](AclEntry.md) representing the ACL |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, and it denies [RuntimePermission](../java.lang/RuntimePermission.md)`("accessUserInformation")`or its [checkRead](../java.lang/SecurityManager.md))method denies read access to the file. |

### name

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun name(): String!
```

Returns the name of the attribute view. Attribute views of this type have the name`"acl"`.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the attribute view |

### setAcl

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAcl(acl: MutableList<AclEntry!>!): Unit
```

Updates (replace) the access control list.

Where the file system supports Access Control Lists, and it uses an ACL model that differs from the NFSv4 defined ACL model, then this method must translate the ACL to the model supported by the file system. This method should reject (by throwing [IOException](../java.io/IOException.md)) any attempt to write an ACL that would appear to make the file more secure than would be the case if the ACL were updated. Where an implementation does not support a mapping of [AclEntryType.AUDIT](AclEntryType.md) or [java.nio.file.attribute.AclEntryType#ALARM](AclEntryType.md) entries, then this method ignores these entries when writing the ACL.

If an ACL entry contains a [user-principal](AclEntry.md))that is not associated with the same provider as this attribute view then [ProviderMismatchException](../java.nio.file/ProviderMismatchException.md) is thrown. Additional validation, if any, is implementation dependent.

If the file system supports other security related file attributes (such as a file [access-permissions](PosixFileAttributes.md))for example), the updating the access control list may also cause these security related attributes to be updated.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `acl` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AclEntry](AclEntry.md)!\>!:the new access control list |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs or the ACL is invalid |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, it denies [RuntimePermission](../java.lang/RuntimePermission.md)`("accessUserInformation")`or its [checkWrite](../java.lang/SecurityManager.md))method denies write access to the file. |
