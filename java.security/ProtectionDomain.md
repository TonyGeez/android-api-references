# ProtectionDomain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProtectionDomain

```
open class ProtectionDomain
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.ProtectionDomain](ProtectionDomain.md) |

Legacy security code; do not use.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ProtectionDomain](ProtectionDomain.md))`(`codesource:` ` [CodeSource](CodeSource.md)!`, `permissions:` ` [PermissionCollection](PermissionCollection.md)!`)` <br /> |
| [ProtectionDomain](ProtectionDomain.md))`(`codesource:` ` [CodeSource](CodeSource.md)!`, `permissions:` ` [PermissionCollection](PermissionCollection.md)!`, `classloader:` ` [ClassLoader](../java.lang/ClassLoader.md)!`, `principals:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](Principal.md)!>!`)` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ClassLoader](../java.lang/ClassLoader.md)! | [getClassLoader](ProtectionDomain.md))`()` <br /> |
| [CodeSource](CodeSource.md)! | [getCodeSource](ProtectionDomain.md))`()` <br /> |
| [PermissionCollection](PermissionCollection.md)! | [getPermissions](ProtectionDomain.md))`()` <br /> |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Principal](Principal.md)!\>! | [getPrincipals](ProtectionDomain.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](ProtectionDomain.md))`(`permission:` ` [Permission](Permission.md)!`)` <br /> |

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
