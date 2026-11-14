# Principal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Principal

```
interface Principal
```

| [java.security.Principal](https://developer.android.com/reference/kotlin/java/security/Principal#) |

| Known Direct Subclasses [Group](https://developer.android.com/reference/kotlin/java/security/acl/Group), [Identity](https://developer.android.com/reference/kotlin/java/security/Identity), [UserPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal.html#), [X500Principal](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#) |--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Group](https://developer.android.com/reference/kotlin/java/security/acl/Group) | This interface is used to represent a group of principals. | | [Identity](https://developer.android.com/reference/kotlin/java/security/Identity) | This class represents identities: real-world objects such as people, companies or organizations whose identities can be authenticated using their public keys. | | [UserPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal.html#) | A`Principal`representing an identity used to determine access rights to objects in a file system. | | [X500Principal](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#) | This class represents an X. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [GroupPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/GroupPrincipal.html#), [IdentityScope](https://developer.android.com/reference/kotlin/java/security/IdentityScope), [Signer](https://developer.android.com/reference/kotlin/java/security/Signer) |---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [GroupPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/GroupPrincipal.html#) | A`UserPrincipal`representing a*group identity*, used to determine access rights to objects in a file system. | | [IdentityScope](https://developer.android.com/reference/kotlin/java/security/IdentityScope) | This class represents a scope for identities. | | [Signer](https://developer.android.com/reference/kotlin/java/security/Signer) | This class is used to represent an Identity that can also digitally sign data. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This interface represents the abstract notion of a principal, which can be used to represent any entity, such as an individual, a corporation, and a login id.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/java/security/Principal#getName())`()` Returns the name of this principal. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](https://developer.android.com/reference/kotlin/java/security/Principal#implies(javax.security.auth.Subject))`(`subject:` ` [Subject](https://developer.android.com/reference/kotlin/javax/security/auth/Subject.html#)!`)` Returns true if the specified subject is implied by this principal. |

## Public methods

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getName(): String!
```

Returns the name of this principal.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of this principal. |

### implies

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun implies(subject: Subject!): Boolean
```

Returns true if the specified subject is implied by this principal.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------|
| `subject` | [Subject](https://developer.android.com/reference/kotlin/javax/security/auth/Subject.html#)!:the`Subject` |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if`subject`is non-null and is implied by this principal, or false otherwise. |
