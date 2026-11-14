# TetheringManager.StartTetheringCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StartTetheringCallback

Kotlin| [Java](../android/net/TetheringManager.StartTetheringCallback.md) 
| --- | --- |

```
interface StartTetheringCallback
```

| [android.net.TetheringManager.StartTetheringCallback](../android/net/TetheringManager.StartTetheringCallback.md) |

Callback for use with [startTethering](../android/net/TetheringManager.md))to find out whether tethering succeeded.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTetheringFailed](../android/net/TetheringManager.StartTetheringCallback.md))`(`error:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when starting tethering failed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTetheringStarted](../android/net/TetheringManager.StartTetheringCallback.md))`()` Called when tethering has been successfully started. |

## Public methods

### onTetheringFailed

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTetheringFailed(error: Int): Unit
```

Called when starting tethering failed.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The error that caused the failure. Value is [android.net.TetheringManager#TETHER_ERROR_SERVICE_UNAVAIL](../android/net/TetheringManager.md), [android.net.TetheringManager#TETHER_ERROR_UNSUPPORTED](../android/net/TetheringManager.md), [android.net.TetheringManager#TETHER_ERROR_INTERNAL_ERROR](../android/net/TetheringManager.md), [android.net.TetheringManager#TETHER_ERROR_NO_CHANGE_TETHERING_PERMISSION](../android/net/TetheringManager.md), [android.net.TetheringManager#TETHER_ERROR_UNKNOWN_TYPE](../android/net/TetheringManager.md), or [android.net.TetheringManager#TETHER_ERROR_DUPLICATE_REQUEST](../android/net/TetheringManager.md) |

### onTetheringStarted

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTetheringStarted(): Unit
```

Called when tethering has been successfully started.
