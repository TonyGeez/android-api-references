# StrictMode.OnThreadViolationListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnThreadViolationListener

Kotlin| [Java](../android/os/StrictMode.OnThreadViolationListener.md) 
| --- | --- |

```
interface OnThreadViolationListener
```

| [android.os.StrictMode.OnThreadViolationListener](../android/os/StrictMode.OnThreadViolationListener.md) |

When # [ThreadPolicy.Builder#penaltyListener](../android/os/StrictMode.ThreadPolicy.Builder.md))is enabled, the listener is called on the provided executor when a Thread violation occurs.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onThreadViolation](../android/os/StrictMode.OnThreadViolationListener.md))`(`v:` ` [Violation](../android/os/strictmode/Violation.md)!`)` Called on a thread policy violation. |

## Public methods

### onThreadViolation

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onThreadViolation(v: Violation!): Unit
```

Called on a thread policy violation.
