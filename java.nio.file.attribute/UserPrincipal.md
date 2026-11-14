# UserPrincipal

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UserPrincipal

```
interface UserPrincipal : Principal
```

| [java.nio.file.attribute.UserPrincipal](../java/nio/file/attribute/UserPrincipal.md) |

| Known Direct Subclasses [GroupPrincipal](../java/nio/file/attribute/GroupPrincipal.md) |---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [GroupPrincipal](../java/nio/file/attribute/GroupPrincipal.md) | A`UserPrincipal`representing a*group identity*, used to determine access rights to objects in a file system. | |
| --- | --- | --- | --- | --- | --- | --- |

A`Principal`representing an identity used to determine access rights to objects in a file system.

On many platforms and file systems an entity requires appropriate access rights or permissions in order to access objects in a file system. The access rights are generally performed by checking the identity of the entity. For example, on implementations that use Access Control Lists (ACLs) to enforce privilege separation then a file in the file system may have an associated ACL that determines the access rights of identities specified in the ACL.

A`UserPrincipal`object is an abstract representation of an identity. It has a [name](../java/security/Principal.md))that is typically the username or account name that it represents. User principal objects may be obtained using a [UserPrincipalLookupService](../java/nio/file/attribute/UserPrincipalLookupService.md), or returned by [FileAttributeView](../java/nio/file/attribute/FileAttributeView.md) implementations that provide access to identity related attributes. For example, the [AclFileAttributeView](../java/nio/file/attribute/AclFileAttributeView.md) and [PosixFileAttributeView](../java/nio/file/attribute/PosixFileAttributeView.md) provide access to a file's [owner](../java/nio/file/attribute/PosixFileAttributes.md)).

## Summary

| Inherited functions ||
|---|---|
| From class [Principal](../java/security/Principal.md) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../java/security/Principal.md))`()` <br /> Returns the name of this principal. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](../java/security/Principal.md))`(`subject:` ` [Subject](../javax/security/auth/Subject.md)!`)` <br /> Returns true if the specified subject is implied by this principal. <br /> | ||
