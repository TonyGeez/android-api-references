# AccessControlContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessControlContext

```
class AccessControlContext
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.AccessControlContext](https://developer.android.com/reference/kotlin/java/security/AccessControlContext#) |

Android doesn't support [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#). Do not use this class.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AccessControlContext](https://developer.android.com/reference/kotlin/java/security/AccessControlContext#AccessControlContext(java.security.AccessControlContext,%20java.security.DomainCombiner))`(`acc:` ` [AccessControlContext](https://developer.android.com/reference/kotlin/java/security/AccessControlContext#)!`, `combiner:` ` [DomainCombiner](https://developer.android.com/reference/kotlin/java/security/DomainCombiner)!`)` <br /> |
| [AccessControlContext](https://developer.android.com/reference/kotlin/java/security/AccessControlContext#AccessControlContext(kotlin.Array))`(`context:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ProtectionDomain](https://developer.android.com/reference/kotlin/java/security/ProtectionDomain)!>!`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkPermission](https://developer.android.com/reference/kotlin/java/security/AccessControlContext#checkPermission(java.security.Permission))`(`perm:` ` [Permission](https://developer.android.com/reference/kotlin/java/security/Permission)!`)` <br /> |
| [DomainCombiner](https://developer.android.com/reference/kotlin/java/security/DomainCombiner)! | [getDomainCombiner](https://developer.android.com/reference/kotlin/java/security/AccessControlContext#getDomainCombiner())`()` <br /> |

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
