# ReflectPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReflectPermission

```
class ReflectPermission : BasicPermission
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [java.security.Permission](https://developer.android.com/reference/kotlin/java/security/Permission.html#) |||
| | ↳ | [java.security.BasicPermission](https://developer.android.com/reference/kotlin/java/security/BasicPermission.html#) ||
| | | ↳ | [java.lang.reflect.ReflectPermission](https://developer.android.com/reference/kotlin/java/lang/reflect/ReflectPermission#) |

Legacy security code; do not use.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ReflectPermission](https://developer.android.com/reference/kotlin/java/lang/reflect/ReflectPermission#ReflectPermission(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [ReflectPermission](https://developer.android.com/reference/kotlin/java/lang/reflect/ReflectPermission#ReflectPermission(kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `actions:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Permission](https://developer.android.com/reference/kotlin/java/security/Permission.html#) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkGuard](https://developer.android.com/reference/kotlin/java/security/Permission.html#checkGuard(kotlin.Any))`(`object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/java/security/Permission.html#getName())`()` <br /> | | [PermissionCollection](https://developer.android.com/reference/kotlin/java/security/PermissionCollection.html#)! | [newPermissionCollection](https://developer.android.com/reference/kotlin/java/security/Permission.html#newPermissionCollection())`()` <br /> | ||
| From class [BasicPermission](https://developer.android.com/reference/kotlin/java/security/BasicPermission.html#) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getActions](https://developer.android.com/reference/kotlin/java/security/BasicPermission.html#getActions())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](https://developer.android.com/reference/kotlin/java/security/BasicPermission.html#implies(java.security.Permission))`(`p:` ` [Permission](https://developer.android.com/reference/kotlin/java/security/Permission.html#)!`)` <br /> | ||

## Public constructors

### ReflectPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ReflectPermission(name: String!)
```  

### ReflectPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ReflectPermission(
    name: String!, 
    actions: String!)
```
