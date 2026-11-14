# SearchManager.OnCancelListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnCancelListener

Kotlin| [Java](../android/app/SearchManager.OnCancelListener.md) 
| --- | --- |

```
interface OnCancelListener
```

| [android.app.SearchManager.OnCancelListener](../android/app/SearchManager.OnCancelListener.md) |

See [SearchManager.setOnCancelListener](../android/app/SearchManager.md))for configuring your activity to monitor search UI state.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCancel](../android/app/SearchManager.OnCancelListener.md))`()` This method will be called when the search UI is canceled. |

## Public methods

### onCancel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCancel(): Unit
```

This method will be called when the search UI is canceled. To make use if it, you must implement this method in your activity, and call [SearchManager.setOnCancelListener](../android/app/SearchManager.md))to register it.
