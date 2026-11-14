# UserPrincipal

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UserPrincipal

```
interface UserPrincipal : Principal
```

| [java.nio.file.attribute.UserPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal#) |

| Known Direct Subclasses [GroupPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/GroupPrincipal) |---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [GroupPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/GroupPrincipal) | A`UserPrincipal`representing a*group identity*, used to determine access rights to objects in a file system. | |

A`Principal`representing an identity used to determine access rights to objects in a file system.

On many platforms and file systems an entity requires appropriate access rights or permissions in order to access objects in a file system. The access rights are generally performed by checking the identity of the entity. For example, on implementations that use Access Control Lists (ACLs) to enforce privilege separation then a file in the file system may have an associated ACL that determines the access rights of identities specified in the ACL.

A`UserPrincipal`object is an abstract representation of an identity. It has a [name](https://developer.android.com/reference/kotlin/java/security/Principal.html#getName())that is typically the username or account name that it represents. User principal objects may be obtained using a [UserPrincipalLookupService](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipalLookupService), or returned by [FileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttributeView) implementations that provide access to identity related attributes. For example, the [AclFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclFileAttributeView) and [PosixFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributeView) provide access to a file's [owner](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributes#owner()).

## Summary

| Inherited functions ||
|---|---|
| From class [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/java/security/Principal.html#getName())`()` <br /> Returns the name of this principal. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](https://developer.android.com/reference/kotlin/java/security/Principal.html#implies(javax.security.auth.Subject))`(`subject:` ` [Subject](https://developer.android.com/reference/kotlin/javax/security/auth/Subject.html#)!`)` <br /> Returns true if the specified subject is implied by this principal. <br /> | ||
