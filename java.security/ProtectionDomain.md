# ProtectionDomain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProtectionDomain

```
open class ProtectionDomain
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.ProtectionDomain](https://developer.android.com/reference/kotlin/java/security/ProtectionDomain#) |

Legacy security code; do not use.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ProtectionDomain](https://developer.android.com/reference/kotlin/java/security/ProtectionDomain#ProtectionDomain(java.security.CodeSource,%20java.security.PermissionCollection))`(`codesource:` ` [CodeSource](https://developer.android.com/reference/kotlin/java/security/CodeSource)!`, `permissions:` ` [PermissionCollection](https://developer.android.com/reference/kotlin/java/security/PermissionCollection)!`)` <br /> |
| [ProtectionDomain](https://developer.android.com/reference/kotlin/java/security/ProtectionDomain#ProtectionDomain(java.security.CodeSource,%20java.security.PermissionCollection,%20java.lang.ClassLoader,%20kotlin.Array))`(`codesource:` ` [CodeSource](https://developer.android.com/reference/kotlin/java/security/CodeSource)!`, `permissions:` ` [PermissionCollection](https://developer.android.com/reference/kotlin/java/security/PermissionCollection)!`, `classloader:` ` [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#)!`, `principals:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Principal](https://developer.android.com/reference/kotlin/java/security/Principal)!>!`)` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#)! | [getClassLoader](https://developer.android.com/reference/kotlin/java/security/ProtectionDomain#getClassLoader())`()` <br /> |
| [CodeSource](https://developer.android.com/reference/kotlin/java/security/CodeSource)! | [getCodeSource](https://developer.android.com/reference/kotlin/java/security/ProtectionDomain#getCodeSource())`()` <br /> |
| [PermissionCollection](https://developer.android.com/reference/kotlin/java/security/PermissionCollection)! | [getPermissions](https://developer.android.com/reference/kotlin/java/security/ProtectionDomain#getPermissions())`()` <br /> |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Principal](https://developer.android.com/reference/kotlin/java/security/Principal)!\>! | [getPrincipals](https://developer.android.com/reference/kotlin/java/security/ProtectionDomain#getPrincipals())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](https://developer.android.com/reference/kotlin/java/security/ProtectionDomain#implies(java.security.Permission))`(`permission:` ` [Permission](https://developer.android.com/reference/kotlin/java/security/Permission)!`)` <br /> |

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
