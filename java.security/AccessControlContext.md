# AccessControlContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessControlContext

```
class AccessControlContext
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.AccessControlContext](AccessControlContext.md) |

Android doesn't support [SecurityManager](../java.lang/SecurityManager.md). Do not use this class.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AccessControlContext](AccessControlContext.md))`(`acc:` ` [AccessControlContext](AccessControlContext.md)!`, `combiner:` ` [DomainCombiner](DomainCombiner.md)!`)` <br /> |
| [AccessControlContext](AccessControlContext.md))`(`context:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ProtectionDomain](ProtectionDomain.md)!>!`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkPermission](AccessControlContext.md))`(`perm:` ` [Permission](Permission.md)!`)` <br /> |
| [DomainCombiner](DomainCombiner.md)! | [getDomainCombiner](AccessControlContext.md))`()` <br /> |

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
