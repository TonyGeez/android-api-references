# Permissions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Permissions

```
class Permissions : PermissionCollection, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.security.PermissionCollection](../java/security/PermissionCollection.md) ||
| | ↳ | [java.security.Permissions](../java/security/Permissions.md) |

Android doesn't support [SecurityManager](../java/lang/SecurityManager.md). Do not use this class.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------|---|
| [Permissions](../java/security/Permissions.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [add](../java/security/Permissions.md))`(`permission:` ` [Permission](../java/security/Permission.md)!`)` <br /> |
| [Enumeration](../java/util/Enumeration.md)\< [Permission](../java/security/Permission.md)!\>! | [elements](../java/security/Permissions.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](../java/security/Permissions.md))`(`permission:` ` [Permission](../java/security/Permission.md)!`)` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [PermissionCollection](../java/security/PermissionCollection.md) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadOnly](../java/security/PermissionCollection.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReadOnly](../java/security/PermissionCollection.md))`()` <br /> | ||

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
| `permission` | [Permission](../java/security/Permission.md)!:the Permission object to add. |

### elements

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun elements(): Enumeration<Permission!>!
```

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| [Enumeration](../java/util/Enumeration.md)< [Permission](../java/security/Permission.md)!>! | an enumeration of all the Permissions. |

### implies

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun implies(permission: Permission!): Boolean
```

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------|
| `permission` | [Permission](../java/security/Permission.md)!:the Permission object to compare. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if "permission" is implied by the permissions in the collection, false if not. |
