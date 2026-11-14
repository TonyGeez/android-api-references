# AclFileAttributeView

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AclFileAttributeView

```
interface AclFileAttributeView : FileOwnerAttributeView
```

| [java.nio.file.attribute.AclFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclFileAttributeView#) |

A file attribute view that supports reading or updating a file's Access Control Lists (ACL) or file owner attributes.

ACLs are used to specify access rights to file system objects. An ACL is an ordered list of [access-control-entries](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntry), each specifying a [UserPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal) and the level of access for that user principal. This file attribute view defines the [getAcl](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclFileAttributeView#getAcl()), and [setAcl](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclFileAttributeView#setAcl(kotlin.collections.MutableList))methods to read and write ACLs based on the ACL model specified in [*RFC 3530: Network File System (NFS) version 4 Protocol*](http://www.ietf.org/rfc/rfc3530.txt). This file attribute view is intended for file system implementations that support the NFSv4 ACL model or have a*well-defined*mapping between the NFSv4 ACL model and the ACL model used by the file system. The details of such mapping are implementation dependent and are therefore unspecified.

This class also extends`FileOwnerAttributeView`so as to define methods to get and set the file owner.

When a file system provides access to a set of [file-systems](https://developer.android.com/reference/kotlin/java/nio/file/FileStore.html#) that are not homogeneous then only some of the file systems may support ACLs. The java.nio.file.FileStore#supportsFileAttributeView method can be used to test if a file system supports ACLs.

## Interoperability

RFC 3530 allows for special user identities to be used on platforms that support the POSIX defined access permissions. The special user identities are "`OWNER@`", "`GROUP@`", and "`EVERYONE@`". When both the`AclFileAttributeView`and the [PosixFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributeView) are supported then these special user identities may be included in ACL [entries](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntry) that are read or written. The file system's [UserPrincipalLookupService](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipalLookupService) may be used to obtain a [UserPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal) to represent these special identities by invoking the [lookupPrincipalByName](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipalLookupService#lookupPrincipalByName(kotlin.String))method.

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
| "acl" | [List](https://developer.android.com/reference/kotlin/java/util/List.html#)\< [AclEntry](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntry)\> |
| "owner" | [UserPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal) |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

The [getAttribute](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#getAttribute(java.nio.file.Path,%20kotlin.String,%20java.nio.file.LinkOption))method may be used to read the ACL or owner attributes as if by invoking the [getAcl](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclFileAttributeView#getAcl())or [getOwner](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileOwnerAttributeView#getOwner())methods.

The [setAttribute](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#setAttribute(java.nio.file.Path,%20kotlin.String,%20kotlin.Any,%20java.nio.file.LinkOption))method may be used to update the ACL or owner attributes as if by invoking the [setAcl](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclFileAttributeView#setAcl(kotlin.collections.MutableList))or [setOwner](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileOwnerAttributeView#setOwner(java.nio.file.attribute.UserPrincipal))methods.

## Setting the ACL when creating a file

Implementations supporting this attribute view may also support setting the initial ACL when creating a file or directory. The initial ACL may be provided to methods such as [createFile](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#createFile(java.nio.file.Path,%20java.nio.file.attribute.FileAttribute))or [createDirectory](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#createDirectory(java.nio.file.Path,%20java.nio.file.attribute.FileAttribute))as an [FileAttribute](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute) with [name](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute#name())`"acl:acl"`and a [value](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute#value())that is the list of`AclEntry`objects.

Where an implementation supports an ACL model that differs from the NFSv4 defined ACL model then setting the initial ACL when creating the file must translate the ACL to the model supported by the file system. Methods that create a file should reject (by throwing [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#)) any attempt to create a file that would be less secure as a result of the translation.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AclEntry](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntry)!\>! | [getAcl](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclFileAttributeView#getAcl())`()` Reads the access control list. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclFileAttributeView#name())`()` Returns the name of the attribute view. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAcl](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclFileAttributeView#setAcl(kotlin.collections.MutableList))`(`acl:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AclEntry](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntry)!>!`)` Updates (replace) the access control list. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [FileOwnerAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileOwnerAttributeView) |--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [UserPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal)! | [getOwner](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileOwnerAttributeView#getOwner())`()` <br /> Read the file owner. It is implementation specific if the file owner can be a [group](https://developer.android.com/reference/kotlin/java/nio/file/attribute/GroupPrincipal). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOwner](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileOwnerAttributeView#setOwner(java.nio.file.attribute.UserPrincipal))`(`owner:` ` [UserPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal)!`)` <br /> Updates the file owner. It is implementation specific if the file owner can be a [group](https://developer.android.com/reference/kotlin/java/nio/file/attribute/GroupPrincipal). To ensure consistent and correct behavior across platforms it is recommended that this method should only be used to set the file owner to a user principal that is not a group. <br /> | ||

## Public methods

### getAcl

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAcl(): MutableList<AclEntry!>!
```

Reads the access control list.

When the file system uses an ACL model that differs from the NFSv4 defined ACL model, then this method returns an ACL that is the translation of the ACL to the NFSv4 ACL model.

The returned list is modifiable so as to facilitate changes to the existing ACL. The [setAcl](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclFileAttributeView#setAcl(kotlin.collections.MutableList))method is used to update the file's ACL attribute.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AclEntry](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntry)!>! | an ordered list of [entries](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntry) representing the ACL |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, and it denies [RuntimePermission](https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#)`("accessUserInformation")`or its [checkRead](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String))method denies read access to the file. |

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

Where the file system supports Access Control Lists, and it uses an ACL model that differs from the NFSv4 defined ACL model, then this method must translate the ACL to the model supported by the file system. This method should reject (by throwing [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#)) any attempt to write an ACL that would appear to make the file more secure than would be the case if the ACL were updated. Where an implementation does not support a mapping of [AclEntryType.AUDIT](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryType) or [java.nio.file.attribute.AclEntryType#ALARM](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryType) entries, then this method ignores these entries when writing the ACL.

If an ACL entry contains a [user-principal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntry#principal())that is not associated with the same provider as this attribute view then [ProviderMismatchException](https://developer.android.com/reference/kotlin/java/nio/file/ProviderMismatchException.html#) is thrown. Additional validation, if any, is implementation dependent.

If the file system supports other security related file attributes (such as a file [access-permissions](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributes#permissions())for example), the updating the access control list may also cause these security related attributes to be updated.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `acl` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AclEntry](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntry)!\>!:the new access control list |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs or the ACL is invalid |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, it denies [RuntimePermission](https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#)`("accessUserInformation")`or its [checkWrite](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String))method denies write access to the file. |
