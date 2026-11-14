# Permissions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Permissions

```
class Permissions : PermissionCollection, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.security.PermissionCollection](https://developer.android.com/reference/kotlin/java/security/PermissionCollection) ||
| | ↳ | [java.security.Permissions](https://developer.android.com/reference/kotlin/java/security/Permissions#) |

Android doesn't support [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#). Do not use this class.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------|---|
| [Permissions](https://developer.android.com/reference/kotlin/java/security/Permissions#Permissions())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [add](https://developer.android.com/reference/kotlin/java/security/Permissions#add(java.security.Permission))`(`permission:` ` [Permission](https://developer.android.com/reference/kotlin/java/security/Permission)!`)` <br /> |
| [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration.html#)\< [Permission](https://developer.android.com/reference/kotlin/java/security/Permission)!\>! | [elements](https://developer.android.com/reference/kotlin/java/security/Permissions#elements())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](https://developer.android.com/reference/kotlin/java/security/Permissions#implies(java.security.Permission))`(`permission:` ` [Permission](https://developer.android.com/reference/kotlin/java/security/Permission)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [PermissionCollection](https://developer.android.com/reference/kotlin/java/security/PermissionCollection) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadOnly](https://developer.android.com/reference/kotlin/java/security/PermissionCollection#isReadOnly())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReadOnly](https://developer.android.com/reference/kotlin/java/security/PermissionCollection#setReadOnly())`()` <br /> | ||

## Public constructors

### Permissions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Permissions()
```

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun add(permission: Permission!): Unit
```

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------|
| `permission` | [Permission](https://developer.android.com/reference/kotlin/java/security/Permission)!:the Permission object to add. |

### elements

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun elements(): Enumeration<Permission!>!
```

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration.html#)< [Permission](https://developer.android.com/reference/kotlin/java/security/Permission)!>! | an enumeration of all the Permissions. |

### implies

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun implies(permission: Permission!): Boolean
```

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------|
| `permission` | [Permission](https://developer.android.com/reference/kotlin/java/security/Permission)!:the Permission object to compare. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if "permission" is implied by the permissions in the collection, false if not. |
