# SocketPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SocketPermission

```
class SocketPermission : Permission, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.security.Permission](../java.security/Permission.md) ||
| | ↳ | [java.net.SocketPermission](SocketPermission.md) |

Legacy security code; do not use.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SocketPermission](SocketPermission.md))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `action:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getActions](SocketPermission.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](SocketPermission.md))`(`p:` ` [Permission](../java.security/Permission.md)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Permission](../java.security/Permission.md) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkGuard](../java.security/Permission.md))`(`object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../java.security/Permission.md))`()` <br /> | | [PermissionCollection](../java.security/PermissionCollection.md)! | [newPermissionCollection](../java.security/Permission.md))`()` <br /> | ||

## Public constructors

### SocketPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SocketPermission(
    host: String!, 
    action: String!)
```

## Public methods

### getActions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActions(): String!
```  

### implies

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun implies(p: Permission!): Boolean
```
