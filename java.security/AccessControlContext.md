# AccessControlContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessControlContext

```
class AccessControlContext
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.AccessControlContext](../java/security/AccessControlContext.md) |

Android doesn't support [SecurityManager](../java/lang/SecurityManager.md). Do not use this class.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AccessControlContext](../java/security/AccessControlContext.md))`(`acc:` ` [AccessControlContext](../java/security/AccessControlContext.md)!`, `combiner:` ` [DomainCombiner](../java/security/DomainCombiner.md)!`)` <br /> |
| [AccessControlContext](../java/security/AccessControlContext.md))`(`context:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ProtectionDomain](../java/security/ProtectionDomain.md)!>!`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkPermission](../java/security/AccessControlContext.md))`(`perm:` ` [Permission](../java/security/Permission.md)!`)` <br /> |
| [DomainCombiner](../java/security/DomainCombiner.md)! | [getDomainCombiner](../java/security/AccessControlContext.md))`()` <br /> |

## Public constructors

### AccessControlContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AccessControlContext(
    acc: AccessControlContext!, 
    combiner: DomainCombiner!)
```  

### AccessControlContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AccessControlContext(context: Array<ProtectionDomain!>!)
```

## Public methods

### checkPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun checkPermission(perm: Permission!): Unit
```  

### getDomainCombiner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDomainCombiner(): DomainCombiner!
```
