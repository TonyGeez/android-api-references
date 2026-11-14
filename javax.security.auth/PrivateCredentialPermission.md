# PrivateCredentialPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrivateCredentialPermission

```
class PrivateCredentialPermission : Permission
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.security.Permission](../java.security/Permission.md) ||
| | ↳ | [javax.security.auth.PrivateCredentialPermission](PrivateCredentialPermission.md) |

Legacy security code; do not use.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PrivateCredentialPermission](PrivateCredentialPermission.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `actions:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getActions](PrivateCredentialPermission.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCredentialClass](PrivateCredentialPermission.md))`()` <br /> |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>! | [getPrincipals](PrivateCredentialPermission.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](PrivateCredentialPermission.md))`(`p:` ` [Permission](../java.security/Permission.md)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Permission](../java.security/Permission.md) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkGuard](../java.security/Permission.md))`(`object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../java.security/Permission.md))`()` <br /> | | [PermissionCollection](../java.security/PermissionCollection.md)! | [newPermissionCollection](../java.security/Permission.md))`()` <br /> | ||

## Public constructors

### PrivateCredentialPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PrivateCredentialPermission(
    name: String!, 
    actions: String!)
```

## Public methods

### getActions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActions(): String!
```  

### getCredentialClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCredentialClass(): String!
```  

### getPrincipals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrincipals(): Array<Array<String!>!>!
```  

### implies

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun implies(p: Permission!): Boolean
```
