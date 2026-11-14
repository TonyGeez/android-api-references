# UserPrincipalLookupService

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UserPrincipalLookupService

```
abstract class UserPrincipalLookupService
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.file.attribute.UserPrincipalLookupService](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipalLookupService#) |

An object to lookup user and group principals by name. A [UserPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal) represents an identity that may be used to determine access rights to objects in a file system. A [GroupPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/GroupPrincipal) represents a*group identity* . A`UserPrincipalLookupService`defines methods to lookup identities by name or group name (which are typically user or account names). Whether names and group names are case sensitive or not depends on the implementation. The exact definition of a group is implementation specific but typically a group represents an identity created for administrative purposes so as to determine the access rights for the members of the group. In particular it is implementation specific if the*namespace* for names and groups is the same or is distinct. To ensure consistent and correct behavior across platforms it is recommended that this API be used as if the namespaces are distinct. In other words, the [lookupPrincipalByName](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipalLookupService#lookupPrincipalByName(kotlin.String))should be used to lookup users, and [lookupPrincipalByGroupName](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipalLookupService#lookupPrincipalByGroupName(kotlin.String))should be used to lookup groups.

## Summary

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UserPrincipalLookupService](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipalLookupService#UserPrincipalLookupService())`()` Initializes a new instance of this class. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [GroupPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/GroupPrincipal)! | [lookupPrincipalByGroupName](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipalLookupService#lookupPrincipalByGroupName(kotlin.String))`(`group:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Lookup a group principal by group name. |
| abstract [UserPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal)! | [lookupPrincipalByName](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipalLookupService#lookupPrincipalByName(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Lookup a user principal by name. |

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

Where an implementation does not support any notion of group then this method always throws [UserPrincipalNotFoundException](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipalNotFoundException). Where the namespace for user accounts and groups is the same, then this method is identical to invoking [lookupPrincipalByName](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipalLookupService#lookupPrincipalByName(kotlin.String)).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------|
| `group` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string representation of the group to lookup |

| Return ||
|----------------------------------------------------------------------------------------------------------|-------------------|
| [GroupPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/GroupPrincipal)! | a group principal |

| Exceptions ||
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.file.attribute.UserPrincipalNotFoundException` | the principal does not exist or is not a group |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, it checks [RuntimePermission](https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#)`("lookupUserInformation")` |
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
| [UserPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal)! | a user principal |

| Exceptions ||
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.file.attribute.UserPrincipalNotFoundException` | the principal does not exist |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, it checks [RuntimePermission](https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#)`("lookupUserInformation")` |
| --- | --- |
