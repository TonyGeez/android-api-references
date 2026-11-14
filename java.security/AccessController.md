# AccessController

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessController

```
class AccessController
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.AccessController](AccessController.md) |

Android doesn't support [SecurityManager](../java.lang/SecurityManager.md). Do not use this class.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkPermission](AccessController.md))`(`perm:` ` [Permission](Permission.md)!`)` <br /> |
| staticT | [doPrivileged](AccessController.md))`(`action:` ` [PrivilegedAction](PrivilegedAction.md)<T>!`)` Calls`action.run()`. |
| staticT | [doPrivileged](AccessController.md))`(`action:` ` [PrivilegedAction](PrivilegedAction.md)<T>!`, `context:` ` [AccessControlContext](AccessControlContext.md)!`)` Calls`action.run()`. |
| --- | --- |
| staticT | [doPrivileged](AccessController.md))`(`action:` ` [PrivilegedExceptionAction](PrivilegedExceptionAction.md)<T>!`)` Calls`action.run()`. |
| staticT | [doPrivileged](AccessController.md))`(`action:` ` [PrivilegedExceptionAction](PrivilegedExceptionAction.md)<T>!`, `context:` ` [AccessControlContext](AccessControlContext.md)!`)` Calls`action.run()`. |
| staticT | [doPrivilegedWithCombiner](AccessController.md))`(`action:` ` [PrivilegedAction](PrivilegedAction.md)<T>!`)` Calls`action.run()`. |
| --- | --- |
| staticT | [doPrivilegedWithCombiner](AccessController.md))`(`action:` ` [PrivilegedExceptionAction](PrivilegedExceptionAction.md)<T>!`)` Calls`action.run()`. |
| static [AccessControlContext](AccessControlContext.md)! | [getContext](AccessController.md))`()` <br /> |

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
