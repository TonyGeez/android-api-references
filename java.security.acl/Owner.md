# Owner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Owner

```
interface Owner
```

| [java.security.acl.Owner](../java/security/acl/Owner.md) |

| Known Direct Subclasses [Acl](../java/security/acl/Acl.md) |-----------------------------------------------------------------------------|------------------------------------------------------| | [Acl](../java/security/acl/Acl.md) | Interface representing an Access Control List (ACL). | |
| --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 33.**
|
| This class is deprecated and subject to removal in a future version of Java SE. It has been replaced by`java.security.Policy`and related classes since 1.2.

Interface for managing owners of Access Control Lists (ACLs) or ACL configurations. (Note that the Acl interface in the`java.security.acl`package extends this Owner interface.) The initial owner Principal should be specified as an argument to the constructor of the class implementing this interface.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addOwner](../java/security/acl/Owner.md))`(`caller:` ` [Principal](../java/security/Principal.md)!`, `owner:` ` [Principal](../java/security/Principal.md)!`)` Adds an owner. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [deleteOwner](../java/security/acl/Owner.md))`(`caller:` ` [Principal](../java/security/Principal.md)!`, `owner:` ` [Principal](../java/security/Principal.md)!`)` Deletes an owner. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOwner](../java/security/acl/Owner.md))`(`owner:` ` [Principal](../java/security/Principal.md)!`)` Returns true if the given principal is an owner of the ACL. |
| --- | --- |

## Public methods

### addOwner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addOwner(
    caller: Principal!, 
    owner: Principal!
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Adds an owner. Only owners can modify ACL contents. The caller principal must be an owner of the ACL in order to invoke this method. That is, only an owner can add another owner. The initial owner is configured at ACL construction time.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `caller` | [Principal](../java/security/Principal.md)!:the principal invoking this method. It must be an owner of the ACL. |
| `owner` | [Principal](../java/security/Principal.md)!:the owner that should be added to the list of owners. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if successful, false if owner is already an owner. |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------|
| `java.security.acl.NotOwnerException` | if the caller principal is not an owner of the ACL. |

### deleteOwner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun deleteOwner(
    caller: Principal!, 
    owner: Principal!
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Deletes an owner. If this is the last owner in the ACL, an exception is raised.

The caller principal must be an owner of the ACL in order to invoke this method.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `caller` | [Principal](../java/security/Principal.md)!:the principal invoking this method. It must be an owner of the ACL. |
| `owner` | [Principal](../java/security/Principal.md)!:the owner to be removed from the list of owners. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the owner is removed, false if the owner is not part of the list of owners. |

| Exceptions ||
|----------------------------------------|--------------------------------------------------------------------------------------|
| `java.security.acl.NotOwnerException` | if the caller principal is not an owner of the ACL. |
| `java.security.acl.LastOwnerException` | if there is only one owner left, so that deleteOwner would leave the ACL owner-less. |

### isOwner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isOwner(owner: Principal!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if the given principal is an owner of the ACL.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `owner` | [Principal](../java/security/Principal.md)!:the principal to be checked to determine whether or not it is an owner. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the passed principal is in the list of owners, false if not. |
