# PowerManager.WakeLockStateListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WakeLockStateListener

Kotlin| [Java](https://developer.android.com/reference/android/os/PowerManager.WakeLockStateListener "View this page in Java") 

```
interface WakeLockStateListener
```

| [android.os.PowerManager.WakeLockStateListener](https://developer.android.com/reference/kotlin/android/os/PowerManager.WakeLockStateListener#) |

A listener interface to get notified when the wakelock is enabled/disabled.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStateChanged](https://developer.android.com/reference/kotlin/android/os/PowerManager.WakeLockStateListener#onStateChanged(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Frameworks could disable the wakelock because either device's power allowlist has changed, or the app's wakelock has exceeded its quota, or the app goes into cached state. |

## Public methods

### onStateChanged

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStateChanged(enabled: Boolean): Unit
```

Frameworks could disable the wakelock because either device's power allowlist has changed, or the app's wakelock has exceeded its quota, or the app goes into cached state.

This callback is called whenever the wakelock's state has changed.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true is enabled, false is disabled. |
