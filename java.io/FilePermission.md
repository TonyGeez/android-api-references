# FilePermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FilePermission

```
class FilePermission : Permission, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.security.Permission](https://developer.android.com/reference/kotlin/java/security/Permission.html#) ||
| | ↳ | [java.io.FilePermission](https://developer.android.com/reference/kotlin/java/io/FilePermission#) |

Legacy security code; do not use.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FilePermission](https://developer.android.com/reference/kotlin/java/io/FilePermission#FilePermission(kotlin.String,%20kotlin.String))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `actions:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getActions](https://developer.android.com/reference/kotlin/java/io/FilePermission#getActions())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](https://developer.android.com/reference/kotlin/java/io/FilePermission#implies(java.security.Permission))`(`p:` ` [Permission](https://developer.android.com/reference/kotlin/java/security/Permission.html#)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Permission](https://developer.android.com/reference/kotlin/java/security/Permission.html#) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkGuard](https://developer.android.com/reference/kotlin/java/security/Permission.html#checkGuard(kotlin.Any))`(`object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/java/security/Permission.html#getName())`()` <br /> | | [PermissionCollection](https://developer.android.com/reference/kotlin/java/security/PermissionCollection.html#)! | [newPermissionCollection](https://developer.android.com/reference/kotlin/java/security/Permission.html#newPermissionCollection())`()` <br /> | ||

## Public constructors

### FilePermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FilePermission(
    path: String!, 
    actions: String!)
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
