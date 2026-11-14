# SSLPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLPermission

```
class SSLPermission : BasicPermission
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.security.Permission](../java.security/Permission.md) |||
| | ↳ | [java.security.BasicPermission](../java.security/BasicPermission.md) ||
| | | ↳ | [javax.net.ssl.SSLPermission](SSLPermission.md) |
| --- | --- | --- | --- |

Legacy security code; do not use.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SSLPermission](SSLPermission.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [SSLPermission](SSLPermission.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `actions:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Permission](../java.security/Permission.md) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkGuard](../java.security/Permission.md))`(`object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../java.security/Permission.md))`()` <br /> | | [PermissionCollection](../java.security/PermissionCollection.md)! | [newPermissionCollection](../java.security/Permission.md))`()` <br /> | ||
| From class [BasicPermission](../java.security/BasicPermission.md) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getActions](../java.security/BasicPermission.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](../java.security/BasicPermission.md))`(`p:` ` [Permission](../java.security/Permission.md)!`)` <br /> | ||

## Public constructors

### SSLPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SSLPermission(name: String!)
```  

### SSLPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SSLPermission(
    name: String!, 
    actions: String!)
```
