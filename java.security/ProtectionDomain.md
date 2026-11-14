# ProtectionDomain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProtectionDomain

```
open class ProtectionDomain
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.ProtectionDomain](../java/security/ProtectionDomain.md) |

Legacy security code; do not use.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ProtectionDomain](../java/security/ProtectionDomain.md))`(`codesource:` ` [CodeSource](../java/security/CodeSource.md)!`, `permissions:` ` [PermissionCollection](../java/security/PermissionCollection.md)!`)` <br /> |
| [ProtectionDomain](../java/security/ProtectionDomain.md))`(`codesource:` ` [CodeSource](../java/security/CodeSource.md)!`, `permissions:` ` [PermissionCollection](../java/security/PermissionCollection.md)!`, `classloader:` ` [ClassLoader](../java/lang/ClassLoader.md)!`, `principals:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](../java/security/Principal.md)!>!`)` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ClassLoader](../java/lang/ClassLoader.md)! | [getClassLoader](../java/security/ProtectionDomain.md))`()` <br /> |
| [CodeSource](../java/security/CodeSource.md)! | [getCodeSource](../java/security/ProtectionDomain.md))`()` <br /> |
| [PermissionCollection](../java/security/PermissionCollection.md)! | [getPermissions](../java/security/ProtectionDomain.md))`()` <br /> |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Principal](../java/security/Principal.md)!\>! | [getPrincipals](../java/security/ProtectionDomain.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](../java/security/ProtectionDomain.md))`(`permission:` ` [Permission](../java/security/Permission.md)!`)` <br /> |

## Public constructors

### ProtectionDomain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ProtectionDomain(
    codesource: CodeSource!, 
    permissions: PermissionCollection!)
```  

### ProtectionDomain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ProtectionDomain(
    codesource: CodeSource!, 
    permissions: PermissionCollection!, 
    classloader: ClassLoader!, 
    principals: Array<Principal!>!)
```

## Public methods

### getClassLoader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClassLoader(): ClassLoader!
```  

### getCodeSource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCodeSource(): CodeSource!
```  

### getPermissions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPermissions(): PermissionCollection!
```  

### getPrincipals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrincipals(): Array<Principal!>!
```  

### implies

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun implies(permission: Permission!): Boolean
```
