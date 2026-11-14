# WebChromeClient.CustomViewCallback

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CustomViewCallback

Kotlin| [Java](../android/webkit/WebChromeClient.CustomViewCallback.md) 
| --- | --- |

```
interface CustomViewCallback
```

| [android.webkit.WebChromeClient.CustomViewCallback](../android/webkit/WebChromeClient.CustomViewCallback.md) |

A callback interface used by the host application to notify the current page that its custom view has been dismissed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCustomViewHidden](../android/webkit/WebChromeClient.CustomViewCallback.md))`()` Invoked when the host application dismisses the custom view. |

## Public methods

### onCustomViewHidden

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCustomViewHidden(): Unit
```

Invoked when the host application dismisses the custom view.
