# Principal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Principal

```
interface Principal
```

| [java.security.Principal](../java/security/Principal.md) |

| Known Direct Subclasses [Group](../java/security/acl/Group.md), [Identity](../java/security/Identity.md), [UserPrincipal](../java/nio/file/attribute/UserPrincipal.md), [X500Principal](../javax/security/auth/x500/X500Principal.md) |--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Group](../java/security/acl/Group.md) | This interface is used to represent a group of principals. | | [Identity](../java/security/Identity.md) | This class represents identities: real-world objects such as people, companies or organizations whose identities can be authenticated using their public keys. | | [UserPrincipal](../java/nio/file/attribute/UserPrincipal.md) | A`Principal`representing an identity used to determine access rights to objects in a file system. | | [X500Principal](../javax/security/auth/x500/X500Principal.md) | This class represents an X. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [GroupPrincipal](../java/nio/file/attribute/GroupPrincipal.md), [IdentityScope](../java/security/IdentityScope.md), [Signer](../java/security/Signer.md) |---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [GroupPrincipal](../java/nio/file/attribute/GroupPrincipal.md) | A`UserPrincipal`representing a*group identity*, used to determine access rights to objects in a file system. | | [IdentityScope](../java/security/IdentityScope.md) | This class represents a scope for identities. | | [Signer](../java/security/Signer.md) | This class is used to represent an Identity that can also digitally sign data. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This interface represents the abstract notion of a principal, which can be used to represent any entity, such as an individual, a corporation, and a login id.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../java/security/Principal.md))`()` Returns the name of this principal. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](../java/security/Principal.md))`(`subject:` ` [Subject](../javax/security/auth/Subject.md)!`)` Returns true if the specified subject is implied by this principal. |

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
| `subject` | [Subject](../javax/security/auth/Subject.md)!:the`Subject` |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if`subject`is non-null and is implied by this principal, or false otherwise. |
