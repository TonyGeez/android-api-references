# StrictMode.OnThreadViolationListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnThreadViolationListener

Kotlin| [Java](https://developer.android.com/reference/android/os/StrictMode.OnThreadViolationListener "View this page in Java") 

```
interface OnThreadViolationListener
```

| [android.os.StrictMode.OnThreadViolationListener](https://developer.android.com/reference/kotlin/android/os/StrictMode.OnThreadViolationListener#) |

When # [ThreadPolicy.Builder#penaltyListener](https://developer.android.com/reference/kotlin/android/os/StrictMode.ThreadPolicy.Builder#penaltyListener(java.util.concurrent.Executor,%20android.os.StrictMode.OnThreadViolationListener))is enabled, the listener is called on the provided executor when a Thread violation occurs.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onThreadViolation](https://developer.android.com/reference/kotlin/android/os/StrictMode.OnThreadViolationListener#onThreadViolation(android.os.strictmode.Violation))`(`v:` ` [Violation](https://developer.android.com/reference/kotlin/android/os/strictmode/Violation)!`)` Called on a thread policy violation. |

## Public methods

### onThreadViolation

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onThreadViolation(v: Violation!): Unit
```

Called on a thread policy violation.
