# SecurityPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SecurityPermission

```
class SecurityPermission : BasicPermission
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.security.Permission](Permission.md) |||
| | ↳ | [java.security.BasicPermission](BasicPermission.md) ||
| | | ↳ | [java.security.SecurityPermission](SecurityPermission.md) |
| --- | --- | --- | --- |

Legacy security code; do not use.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SecurityPermission](SecurityPermission.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [SecurityPermission](SecurityPermission.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `actions:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Permission](Permission.md) |------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkGuard](Permission.md))`(`object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](Permission.md))`()` <br /> | | [PermissionCollection](PermissionCollection.md)! | [newPermissionCollection](Permission.md))`()` <br /> | ||
| From class [BasicPermission](BasicPermission.md) |------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getActions](BasicPermission.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](BasicPermission.md))`(`p:` ` [Permission](Permission.md)!`)` <br /> | ||

## Public constructors

### SecurityPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SecurityPermission(name: String!)
```  

### SecurityPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SecurityPermission(
    name: String!, 
    actions: String!)
```
