# TetheringManager.StartTetheringCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StartTetheringCallback

Kotlin| [Java](https://developer.android.com/reference/android/net/TetheringManager.StartTetheringCallback "View this page in Java") 
| --- | --- |

```
interface StartTetheringCallback
```

| [android.net.TetheringManager.StartTetheringCallback](https://developer.android.com/reference/kotlin/android/net/TetheringManager.StartTetheringCallback#) |

Callback for use with [startTethering](https://developer.android.com/reference/kotlin/android/net/TetheringManager#startTethering(android.net.TetheringManager.TetheringRequest,%20java.util.concurrent.Executor,%20android.net.TetheringManager.StartTetheringCallback))to find out whether tethering succeeded.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTetheringFailed](https://developer.android.com/reference/kotlin/android/net/TetheringManager.StartTetheringCallback#onTetheringFailed(kotlin.Int))`(`error:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when starting tethering failed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTetheringStarted](https://developer.android.com/reference/kotlin/android/net/TetheringManager.StartTetheringCallback#onTetheringStarted())`()` Called when tethering has been successfully started. |

## Public methods

### onTetheringFailed

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTetheringFailed(error: Int): Unit
```

Called when starting tethering failed.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The error that caused the failure. Value is [android.net.TetheringManager#TETHER_ERROR_SERVICE_UNAVAIL](https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_SERVICE_UNAVAIL:kotlin.Int), [android.net.TetheringManager#TETHER_ERROR_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_UNSUPPORTED:kotlin.Int), [android.net.TetheringManager#TETHER_ERROR_INTERNAL_ERROR](https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_INTERNAL_ERROR:kotlin.Int), [android.net.TetheringManager#TETHER_ERROR_NO_CHANGE_TETHERING_PERMISSION](https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_NO_CHANGE_TETHERING_PERMISSION:kotlin.Int), [android.net.TetheringManager#TETHER_ERROR_UNKNOWN_TYPE](https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_UNKNOWN_TYPE:kotlin.Int), or [android.net.TetheringManager#TETHER_ERROR_DUPLICATE_REQUEST](https://developer.android.com/reference/kotlin/android/net/TetheringManager#TETHER_ERROR_DUPLICATE_REQUEST:kotlin.Int) |

### onTetheringStarted

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTetheringStarted(): Unit
```

Called when tethering has been successfully started.
