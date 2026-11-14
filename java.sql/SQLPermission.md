# SQLPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLPermission

```
class SQLPermission : BasicPermission
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.security.Permission](https://developer.android.com/reference/kotlin/java/security/Permission.html#) |||
| | ↳ | [java.security.BasicPermission](https://developer.android.com/reference/kotlin/java/security/BasicPermission.html#) ||
| | | ↳ | [java.sql.SQLPermission](https://developer.android.com/reference/kotlin/java/sql/SQLPermission#) |
| --- | --- | --- | --- |

Legacy security code; do not use.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLPermission](https://developer.android.com/reference/kotlin/java/sql/SQLPermission#SQLPermission(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [SQLPermission](https://developer.android.com/reference/kotlin/java/sql/SQLPermission#SQLPermission(kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `actions:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Permission](https://developer.android.com/reference/kotlin/java/security/Permission.html#) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkGuard](https://developer.android.com/reference/kotlin/java/security/Permission.html#checkGuard(kotlin.Any))`(`object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/java/security/Permission.html#getName())`()` <br /> | | [PermissionCollection](https://developer.android.com/reference/kotlin/java/security/PermissionCollection.html#)! | [newPermissionCollection](https://developer.android.com/reference/kotlin/java/security/Permission.html#newPermissionCollection())`()` <br /> | ||
| From class [BasicPermission](https://developer.android.com/reference/kotlin/java/security/BasicPermission.html#) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getActions](https://developer.android.com/reference/kotlin/java/security/BasicPermission.html#getActions())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](https://developer.android.com/reference/kotlin/java/security/BasicPermission.html#implies(java.security.Permission))`(`p:` ` [Permission](https://developer.android.com/reference/kotlin/java/security/Permission.html#)!`)` <br /> | ||

## Public constructors

### SQLPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLPermission(name: String!)
```  

### SQLPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLPermission(
    name: String!, 
    actions: String!)
```
