# SocketPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SocketPermission

```
class SocketPermission : Permission, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.security.Permission](https://developer.android.com/reference/kotlin/java/security/Permission.html#) ||
| | ↳ | [java.net.SocketPermission](https://developer.android.com/reference/kotlin/java/net/SocketPermission#) |

Legacy security code; do not use.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SocketPermission](https://developer.android.com/reference/kotlin/java/net/SocketPermission#SocketPermission(kotlin.String,%20kotlin.String))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `action:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getActions](https://developer.android.com/reference/kotlin/java/net/SocketPermission#getActions())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](https://developer.android.com/reference/kotlin/java/net/SocketPermission#implies(java.security.Permission))`(`p:` ` [Permission](https://developer.android.com/reference/kotlin/java/security/Permission.html#)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Permission](https://developer.android.com/reference/kotlin/java/security/Permission.html#) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkGuard](https://developer.android.com/reference/kotlin/java/security/Permission.html#checkGuard(kotlin.Any))`(`object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/java/security/Permission.html#getName())`()` <br /> | | [PermissionCollection](https://developer.android.com/reference/kotlin/java/security/PermissionCollection.html#)! | [newPermissionCollection](https://developer.android.com/reference/kotlin/java/security/Permission.html#newPermissionCollection())`()` <br /> | ||

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
