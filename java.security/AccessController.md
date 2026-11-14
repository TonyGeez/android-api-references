# AccessController

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessController

```
class AccessController
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.AccessController](https://developer.android.com/reference/kotlin/java/security/AccessController#) |

Android doesn't support [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#). Do not use this class.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkPermission](https://developer.android.com/reference/kotlin/java/security/AccessController#checkPermission(java.security.Permission))`(`perm:` ` [Permission](https://developer.android.com/reference/kotlin/java/security/Permission)!`)` <br /> |
| staticT | [doPrivileged](https://developer.android.com/reference/kotlin/java/security/AccessController#doPrivileged(java.security.PrivilegedAction))`(`action:` ` [PrivilegedAction](https://developer.android.com/reference/kotlin/java/security/PrivilegedAction)<T>!`)` Calls`action.run()`. |
| staticT | [doPrivileged](https://developer.android.com/reference/kotlin/java/security/AccessController#doPrivileged(java.security.PrivilegedAction,%20java.security.AccessControlContext))`(`action:` ` [PrivilegedAction](https://developer.android.com/reference/kotlin/java/security/PrivilegedAction)<T>!`, `context:` ` [AccessControlContext](https://developer.android.com/reference/kotlin/java/security/AccessControlContext)!`)` Calls`action.run()`. |
| --- | --- |
| staticT | [doPrivileged](https://developer.android.com/reference/kotlin/java/security/AccessController#doPrivileged(java.security.PrivilegedExceptionAction))`(`action:` ` [PrivilegedExceptionAction](https://developer.android.com/reference/kotlin/java/security/PrivilegedExceptionAction)<T>!`)` Calls`action.run()`. |
| staticT | [doPrivileged](https://developer.android.com/reference/kotlin/java/security/AccessController#doPrivileged(java.security.PrivilegedExceptionAction,%20java.security.AccessControlContext))`(`action:` ` [PrivilegedExceptionAction](https://developer.android.com/reference/kotlin/java/security/PrivilegedExceptionAction)<T>!`, `context:` ` [AccessControlContext](https://developer.android.com/reference/kotlin/java/security/AccessControlContext)!`)` Calls`action.run()`. |
| staticT | [doPrivilegedWithCombiner](https://developer.android.com/reference/kotlin/java/security/AccessController#doPrivilegedWithCombiner(java.security.PrivilegedAction))`(`action:` ` [PrivilegedAction](https://developer.android.com/reference/kotlin/java/security/PrivilegedAction)<T>!`)` Calls`action.run()`. |
| --- | --- |
| staticT | [doPrivilegedWithCombiner](https://developer.android.com/reference/kotlin/java/security/AccessController#doPrivilegedWithCombiner(java.security.PrivilegedExceptionAction))`(`action:` ` [PrivilegedExceptionAction](https://developer.android.com/reference/kotlin/java/security/PrivilegedExceptionAction)<T>!`)` Calls`action.run()`. |
| static [AccessControlContext](https://developer.android.com/reference/kotlin/java/security/AccessControlContext)! | [getContext](https://developer.android.com/reference/kotlin/java/security/AccessController#getContext())`()` <br /> |

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
