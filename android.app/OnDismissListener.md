# SearchManager.OnDismissListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDismissListener

Kotlin| [Java](../android/app/SearchManager.OnDismissListener.md) 
| --- | --- |

```
interface OnDismissListener
```

| [android.app.SearchManager.OnDismissListener](../android/app/SearchManager.OnDismissListener.md) |

See [SearchManager.setOnDismissListener](SearchManager.md))for configuring your activity to monitor search UI state.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDismiss](../android/app/SearchManager.OnDismissListener.md))`()` This method will be called when the search UI is dismissed. |

## Public methods

### onDismiss

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDismiss(): Unit
```

This method will be called when the search UI is dismissed. To make use of it, you must implement this method in your activity, and call [SearchManager.setOnDismissListener](SearchManager.md))to register it.
