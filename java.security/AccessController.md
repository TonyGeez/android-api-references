# AccessController

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessController

```
class AccessController
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.AccessController](../java/security/AccessController.md) |

Android doesn't support [SecurityManager](../java/lang/SecurityManager.md). Do not use this class.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkPermission](../java/security/AccessController.md))`(`perm:` ` [Permission](../java/security/Permission.md)!`)` <br /> |
| staticT | [doPrivileged](../java/security/AccessController.md))`(`action:` ` [PrivilegedAction](../java/security/PrivilegedAction.md)<T>!`)` Calls`action.run()`. |
| staticT | [doPrivileged](../java/security/AccessController.md))`(`action:` ` [PrivilegedAction](../java/security/PrivilegedAction.md)<T>!`, `context:` ` [AccessControlContext](../java/security/AccessControlContext.md)!`)` Calls`action.run()`. |
| --- | --- |
| staticT | [doPrivileged](../java/security/AccessController.md))`(`action:` ` [PrivilegedExceptionAction](../java/security/PrivilegedExceptionAction.md)<T>!`)` Calls`action.run()`. |
| staticT | [doPrivileged](../java/security/AccessController.md))`(`action:` ` [PrivilegedExceptionAction](../java/security/PrivilegedExceptionAction.md)<T>!`, `context:` ` [AccessControlContext](../java/security/AccessControlContext.md)!`)` Calls`action.run()`. |
| staticT | [doPrivilegedWithCombiner](../java/security/AccessController.md))`(`action:` ` [PrivilegedAction](../java/security/PrivilegedAction.md)<T>!`)` Calls`action.run()`. |
| --- | --- |
| staticT | [doPrivilegedWithCombiner](../java/security/AccessController.md))`(`action:` ` [PrivilegedExceptionAction](../java/security/PrivilegedExceptionAction.md)<T>!`)` Calls`action.run()`. |
| static [AccessControlContext](../java/security/AccessControlContext.md)! | [getContext](../java/security/AccessController.md))`()` <br /> |

## Public methods

### checkPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun checkPermission(perm: Permission!): Unit
```  

### doPrivileged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> doPrivileged(action: PrivilegedAction<T>!): T
```

Calls`action.run()`. 

### doPrivileged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> doPrivileged(
    action: PrivilegedAction<T>!, 
    context: AccessControlContext!
): T
```

Calls`action.run()`. 

### doPrivileged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> doPrivileged(action: PrivilegedExceptionAction<T>!): T
```

Calls`action.run()`. 

### doPrivileged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> doPrivileged(
    action: PrivilegedExceptionAction<T>!, 
    context: AccessControlContext!
): T
```

Calls`action.run()`. 

### doPrivilegedWithCombiner

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> doPrivilegedWithCombiner(action: PrivilegedAction<T>!): T
```

Calls`action.run()`. 

### doPrivilegedWithCombiner

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> doPrivilegedWithCombiner(action: PrivilegedExceptionAction<T>!): T
```

Calls`action.run()`. 

### getContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getContext(): AccessControlContext!
```
