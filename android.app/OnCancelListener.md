# SearchManager.OnCancelListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnCancelListener

Kotlin| [Java](https://developer.android.com/reference/android/app/SearchManager.OnCancelListener "View this page in Java") 

```
interface OnCancelListener
```

| [android.app.SearchManager.OnCancelListener](https://developer.android.com/reference/kotlin/android/app/SearchManager.OnCancelListener#) |

See [SearchManager.setOnCancelListener](https://developer.android.com/reference/kotlin/android/app/SearchManager#setOnCancelListener(android.app.SearchManager.OnCancelListener))for configuring your activity to monitor search UI state.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCancel](https://developer.android.com/reference/kotlin/android/app/SearchManager.OnCancelListener#onCancel())`()` This method will be called when the search UI is canceled. |

## Public methods

### onCancel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCancel(): Unit
```

This method will be called when the search UI is canceled. To make use if it, you must implement this method in your activity, and call [SearchManager.setOnCancelListener](https://developer.android.com/reference/kotlin/android/app/SearchManager#setOnCancelListener(android.app.SearchManager.OnCancelListener))to register it.
