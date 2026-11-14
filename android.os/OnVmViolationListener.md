# StrictMode.OnVmViolationListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnVmViolationListener

Kotlin| [Java](https://developer.android.com/reference/android/os/StrictMode.OnVmViolationListener "View this page in Java") 
| --- | --- |

```
interface OnVmViolationListener
```

| [android.os.StrictMode.OnVmViolationListener](https://developer.android.com/reference/kotlin/android/os/StrictMode.OnVmViolationListener#) |

When # [VmPolicy.Builder#penaltyListener](https://developer.android.com/reference/kotlin/android/os/StrictMode.VmPolicy.Builder#penaltyListener(java.util.concurrent.Executor,%20android.os.StrictMode.OnVmViolationListener))is enabled, the listener is called on the provided executor when a VM violation occurs.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onVmViolation](https://developer.android.com/reference/kotlin/android/os/StrictMode.OnVmViolationListener#onVmViolation(android.os.strictmode.Violation))`(`v:` ` [Violation](https://developer.android.com/reference/kotlin/android/os/strictmode/Violation)!`)` Called on a VM policy violation. |

## Public methods

### onVmViolation

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onVmViolation(v: Violation!): Unit
```

Called on a VM policy violation.
