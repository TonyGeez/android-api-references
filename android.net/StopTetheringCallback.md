# TetheringManager.StopTetheringCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StopTetheringCallback

Kotlin| [Java](../android/net/TetheringManager.StopTetheringCallback.md) 
| --- | --- |

```
interface StopTetheringCallback
```

| [android.net.TetheringManager.StopTetheringCallback](../android/net/TetheringManager.StopTetheringCallback.md) |

Callback for use with [stopTethering](TetheringManager.md))to find out whether stop tethering succeeded.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStopTetheringFailed](../android/net/TetheringManager.StopTetheringCallback.md))`(`error:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when starting tethering failed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStopTetheringSucceeded](../android/net/TetheringManager.StopTetheringCallback.md))`()` Called when tethering has been successfully stopped. |

## Public methods

### onStopTetheringFailed

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onStopTetheringFailed(error: Int): Unit
```

Called when starting tethering failed.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The error that caused the failure. Value is [android.net.TetheringManager#TETHER_ERROR_NO_ERROR](TetheringManager.md), or [android.net.TetheringManager#TETHER_ERROR_UNKNOWN_REQUEST](TetheringManager.md) |

### onStopTetheringSucceeded

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onStopTetheringSucceeded(): Unit
```

Called when tethering has been successfully stopped.
