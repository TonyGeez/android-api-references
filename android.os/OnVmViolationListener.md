# StrictMode.OnVmViolationListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnVmViolationListener

Kotlin| [Java](../android/os/StrictMode.OnVmViolationListener.md) 
| --- | --- |

```
interface OnVmViolationListener
```

| [android.os.StrictMode.OnVmViolationListener](../android/os/StrictMode.OnVmViolationListener.md) |

When # [VmPolicy.Builder#penaltyListener](../android/os/StrictMode.VmPolicy.Builder.md))is enabled, the listener is called on the provided executor when a VM violation occurs.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onVmViolation](../android/os/StrictMode.OnVmViolationListener.md))`(`v:` ` [Violation](../android.os.strictmode/Violation.md)!`)` Called on a VM policy violation. |

## Public methods

### onVmViolation

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onVmViolation(v: Violation!): Unit
```

Called on a VM policy violation.
