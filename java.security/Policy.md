# Policy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Policy

```
abstract class Policy
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.Policy](https://developer.android.com/reference/kotlin/java/security/Policy#) |

Android doesn't support [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#). Do not use this class.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------|
| abstract | [Parameters](https://developer.android.com/reference/kotlin/java/security/Policy.Parameters) <br /> |

| Public constructors ||
|---------------------------------------------------------------------------------------------------|---|
| [Policy](https://developer.android.com/reference/kotlin/java/security/Policy#Policy())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Policy](https://developer.android.com/reference/kotlin/java/security/Policy#)! | [getInstance](https://developer.android.com/reference/kotlin/java/security/Policy#getInstance(kotlin.String,%20java.security.Policy.Parameters))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `params:` ` [Policy.Parameters](https://developer.android.com/reference/kotlin/java/security/Policy.Parameters)!`)` <br /> |
| openstatic [Policy](https://developer.android.com/reference/kotlin/java/security/Policy#)! | [getInstance](https://developer.android.com/reference/kotlin/java/security/Policy#getInstance(kotlin.String,%20java.security.Policy.Parameters,%20kotlin.String))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `params:` ` [Policy.Parameters](https://developer.android.com/reference/kotlin/java/security/Policy.Parameters)!`, `provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| openstatic [Policy](https://developer.android.com/reference/kotlin/java/security/Policy#)! | [getInstance](https://developer.android.com/reference/kotlin/java/security/Policy#getInstance(kotlin.String,%20java.security.Policy.Parameters,%20java.security.Provider))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `params:` ` [Policy.Parameters](https://developer.android.com/reference/kotlin/java/security/Policy.Parameters)!`, `provider:` ` [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)!`)` <br /> |
| open [Policy.Parameters](https://developer.android.com/reference/kotlin/java/security/Policy.Parameters)! | [getParameters](https://developer.android.com/reference/kotlin/java/security/Policy#getParameters())`()` <br /> |
| open [PermissionCollection](https://developer.android.com/reference/kotlin/java/security/PermissionCollection)! | [getPermissions](https://developer.android.com/reference/kotlin/java/security/Policy#getPermissions(java.security.CodeSource))`(`codesource:` ` [CodeSource](https://developer.android.com/reference/kotlin/java/security/CodeSource)!`)` <br /> |
| open [PermissionCollection](https://developer.android.com/reference/kotlin/java/security/PermissionCollection)! | [getPermissions](https://developer.android.com/reference/kotlin/java/security/Policy#getPermissions(java.security.ProtectionDomain))`(`domain:` ` [ProtectionDomain](https://developer.android.com/reference/kotlin/java/security/ProtectionDomain)!`)` <br /> |
| openstatic [Policy](https://developer.android.com/reference/kotlin/java/security/Policy#)! | [getPolicy](https://developer.android.com/reference/kotlin/java/security/Policy#getPolicy())`()` <br /> |
| open [Provider](https://developer.android.com/reference/kotlin/java/security/Provider)! | [getProvider](https://developer.android.com/reference/kotlin/java/security/Policy#getProvider())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](https://developer.android.com/reference/kotlin/java/security/Policy#getType())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](https://developer.android.com/reference/kotlin/java/security/Policy#implies(java.security.ProtectionDomain,%20java.security.Permission))`(`domain:` ` [ProtectionDomain](https://developer.android.com/reference/kotlin/java/security/ProtectionDomain)!`, `permission:` ` [Permission](https://developer.android.com/reference/kotlin/java/security/Permission)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [refresh](https://developer.android.com/reference/kotlin/java/security/Policy#refresh())`()` <br /> |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPolicy](https://developer.android.com/reference/kotlin/java/security/Policy#setPolicy(java.security.Policy))`(`p:` ` [Policy](https://developer.android.com/reference/kotlin/java/security/Policy#)!`)` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [PermissionCollection](https://developer.android.com/reference/kotlin/java/security/PermissionCollection)! | [UNSUPPORTED_EMPTY_COLLECTION](https://developer.android.com/reference/kotlin/java/security/Policy#UNSUPPORTED_EMPTY_COLLECTION:java.security.PermissionCollection) <br /> |

## Public constructors

### Policy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Policy()
```

## Public methods

### getInstance

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    type: String!, 
    params: Policy.Parameters!
): Policy!
```  

### getInstance

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    type: String!, 
    params: Policy.Parameters!, 
    provider: String!
): Policy!
```  

### getInstance

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    type: String!, 
    params: Policy.Parameters!, 
    provider: Provider!
): Policy!
```  

### getParameters

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParameters(): Policy.Parameters!
```  

### getPermissions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPermissions(codesource: CodeSource!): PermissionCollection!
```  

### getPermissions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPermissions(domain: ProtectionDomain!): PermissionCollection!
```  

### getPolicy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getPolicy(): Policy!
```  

### getProvider

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProvider(): Provider!
```  

### getType

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(): String!
```  

### implies

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun implies(
    domain: ProtectionDomain!, 
    permission: Permission!
): Boolean
```  

### refresh

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun refresh(): Unit
```  

### setPolicy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setPolicy(p: Policy!): Unit
```

## Properties

### UNSUPPORTED_EMPTY_COLLECTION

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNSUPPORTED_EMPTY_COLLECTION: PermissionCollection!
```
