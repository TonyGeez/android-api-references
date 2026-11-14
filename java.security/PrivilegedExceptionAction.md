# PrivilegedExceptionAction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrivilegedExceptionAction

```
interface PrivilegedExceptionAction<T : Any!>
```

| [java.security.PrivilegedExceptionAction](https://developer.android.com/reference/kotlin/java/security/PrivilegedExceptionAction#) |

Android doesn't support [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#). Do not use this class.

## Summary

| Public methods ||
|-----------|----------------------------------------------------------------------------------------------------------------|
| abstractT | [run](https://developer.android.com/reference/kotlin/java/security/PrivilegedExceptionAction#run())`()` <br /> |

## Public methods

### run

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun run(): T
```
