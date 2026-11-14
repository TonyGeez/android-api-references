# Policy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Policy

```
abstract class Policy
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.Policy](../java/security/Policy.md) |

Android doesn't support [SecurityManager](../java/lang/SecurityManager.md). Do not use this class.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------|
| abstract | [Parameters](../java/security/Policy.Parameters.md) <br /> |

| Public constructors ||
|---------------------------------------------------------------------------------------------------|---|
| [Policy](../java/security/Policy.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Policy](../java/security/Policy.md)! | [getInstance](../java/security/Policy.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `params:` ` [Policy.Parameters](../java/security/Policy.Parameters.md)!`)` <br /> |
| openstatic [Policy](../java/security/Policy.md)! | [getInstance](../java/security/Policy.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `params:` ` [Policy.Parameters](../java/security/Policy.Parameters.md)!`, `provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| openstatic [Policy](../java/security/Policy.md)! | [getInstance](../java/security/Policy.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `params:` ` [Policy.Parameters](../java/security/Policy.Parameters.md)!`, `provider:` ` [Provider](../java/security/Provider.md)!`)` <br /> |
| --- | --- |
| open [Policy.Parameters](../java/security/Policy.Parameters.md)! | [getParameters](../java/security/Policy.md))`()` <br /> |
| open [PermissionCollection](../java/security/PermissionCollection.md)! | [getPermissions](../java/security/Policy.md))`(`codesource:` ` [CodeSource](../java/security/CodeSource.md)!`)` <br /> |
| open [PermissionCollection](../java/security/PermissionCollection.md)! | [getPermissions](../java/security/Policy.md))`(`domain:` ` [ProtectionDomain](../java/security/ProtectionDomain.md)!`)` <br /> |
| --- | --- |
| openstatic [Policy](../java/security/Policy.md)! | [getPolicy](../java/security/Policy.md))`()` <br /> |
| open [Provider](../java/security/Provider.md)! | [getProvider](../java/security/Policy.md))`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](../java/security/Policy.md))`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](../java/security/Policy.md))`(`domain:` ` [ProtectionDomain](../java/security/ProtectionDomain.md)!`, `permission:` ` [Permission](../java/security/Permission.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [refresh](../java/security/Policy.md))`()` <br /> |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPolicy](../java/security/Policy.md))`(`p:` ` [Policy](../java/security/Policy.md)!`)` <br /> |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [PermissionCollection](../java/security/PermissionCollection.md)! | [UNSUPPORTED_EMPTY_COLLECTION](../java/security/Policy.md) <br /> |

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
