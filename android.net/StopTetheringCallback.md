# TetheringManager.StopTetheringCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StopTetheringCallback

Kotlin| [Java](https://developer.android.com/reference/android/net/TetheringManager.StopTetheringCallback "View this page in Java") 

```
interface StopTetheringCallback
```

| [android.net.TetheringManager.StopTetheringCallback](https://developer.android.com/reference/kotlin/android/net/TetheringManager.StopTetheringCallback#) |

Callback for use with [stopTethering](https://developer.android.com/reference/kotlin/android/net/TetheringManager#stopTethering(android.net.TetheringManager.TetheringRequest,%20java.util.concurrent.Executor,%20android.net.TetheringManager.StopTetheringCallback))to find out whether stop tethering succeeded.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStopTetheringFailed](https://developer.android.com/reference/kotlin/android/net/TetheringManager.StopTetheringCallback#onStopTetheringFailed(kotlin.Int))`(`error:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when starting tethering failed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStopTetheringSucceeded](https://developer.android.com/reference/kotlin/android/net/TetheringManager.StopTetheringCallback#onStopTetheringSucceeded())`()` Called when tethering has been successfully stopped. |

## Public methods

### onStopTetheringFailed

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onStopTetheringFailed(error: Int): Unit
```

Called when starting tethering failed.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The error that caused the failure. Value is [android.net.TetheringManager#TETHER_ERROR_NO_ERROR](https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_NO_ERROR:kotlin.Int), or [android.net.TetheringManager#TETHER_ERROR_UNKNOWN_REQUEST](https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_UNKNOWN_REQUEST:kotlin.Int) |

### onStopTetheringSucceeded

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onStopTetheringSucceeded(): Unit
```

Called when tethering has been successfully stopped.
