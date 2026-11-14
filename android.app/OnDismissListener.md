# SearchManager.OnDismissListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDismissListener

Kotlin| [Java](https://developer.android.com/reference/android/app/SearchManager.OnDismissListener "View this page in Java") 

```
interface OnDismissListener
```

| [android.app.SearchManager.OnDismissListener](https://developer.android.com/reference/kotlin/android/app/SearchManager.OnDismissListener#) |

See [SearchManager.setOnDismissListener](https://developer.android.com/reference/kotlin/android/app/SearchManager#setOnDismissListener(android.app.SearchManager.OnDismissListener))for configuring your activity to monitor search UI state.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDismiss](https://developer.android.com/reference/kotlin/android/app/SearchManager.OnDismissListener#onDismiss())`()` This method will be called when the search UI is dismissed. |

## Public methods

### onDismiss

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDismiss(): Unit
```

This method will be called when the search UI is dismissed. To make use of it, you must implement this method in your activity, and call [SearchManager.setOnDismissListener](https://developer.android.com/reference/kotlin/android/app/SearchManager#setOnDismissListener(android.app.SearchManager.OnDismissListener))to register it.
