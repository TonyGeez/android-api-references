# UserPrincipalLookupService

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UserPrincipalLookupService

```
abstract class UserPrincipalLookupService
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.file.attribute.UserPrincipalLookupService](UserPrincipalLookupService.md) |

An object to lookup user and group principals by name. A [UserPrincipal](UserPrincipal.md) represents an identity that may be used to determine access rights to objects in a file system. A [GroupPrincipal](GroupPrincipal.md) represents a*group identity* . A`UserPrincipalLookupService`defines methods to lookup identities by name or group name (which are typically user or account names). Whether names and group names are case sensitive or not depends on the implementation. The exact definition of a group is implementation specific but typically a group represents an identity created for administrative purposes so as to determine the access rights for the members of the group. In particular it is implementation specific if the*namespace* for names and groups is the same or is distinct. To ensure consistent and correct behavior across platforms it is recommended that this API be used as if the namespaces are distinct. In other words, the [lookupPrincipalByName](UserPrincipalLookupService.md))should be used to lookup users, and [lookupPrincipalByGroupName](UserPrincipalLookupService.md))should be used to lookup groups.

## Summary

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UserPrincipalLookupService](UserPrincipalLookupService.md))`()` Initializes a new instance of this class. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [GroupPrincipal](GroupPrincipal.md)! | [lookupPrincipalByGroupName](UserPrincipalLookupService.md))`(`group:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Lookup a group principal by group name. |
| abstract [UserPrincipal](UserPrincipal.md)! | [lookupPrincipalByName](UserPrincipalLookupService.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Lookup a user principal by name. |

## Protected constructors

### UserPrincipalLookupService

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected UserPrincipalLookupService()
```

Initializes a new instance of this class.

## Public methods

### lookupPrincipalByGroupName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun lookupPrincipalByGroupName(group: String!): GroupPrincipal!
```

Lookup a group principal by group name.

Where an implementation does not support any notion of group then this method always throws [UserPrincipalNotFoundException](UserPrincipalNotFoundException.md). Where the namespace for user accounts and groups is the same, then this method is identical to invoking [lookupPrincipalByName](UserPrincipalLookupService.md)).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------|
| `group` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string representation of the group to lookup |

| Return ||
|----------------------------------------------------------------------------------------------------------|-------------------|
| [GroupPrincipal](GroupPrincipal.md)! | a group principal |

| Exceptions ||
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.file.attribute.UserPrincipalNotFoundException` | the principal does not exist or is not a group |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, it checks [RuntimePermission](../java.lang/RuntimePermission.md)`("lookupUserInformation")` |
| --- | --- |

### lookupPrincipalByName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun lookupPrincipalByName(name: String!): UserPrincipal!
```

Lookup a user principal by name.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string representation of the user principal to lookup |

| Return ||
|--------------------------------------------------------------------------------------------------------|------------------|
| [UserPrincipal](UserPrincipal.md)! | a user principal |

| Exceptions ||
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.file.attribute.UserPrincipalNotFoundException` | the principal does not exist |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, it checks [RuntimePermission](../java.lang/RuntimePermission.md)`("lookupUserInformation")` |
| --- | --- |
