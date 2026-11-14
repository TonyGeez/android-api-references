# WebChromeClient.CustomViewCallback

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CustomViewCallback

Kotlin| [Java](https://developer.android.com/reference/android/webkit/WebChromeClient.CustomViewCallback "View this page in Java") 
| --- | --- |

```
interface CustomViewCallback
```

| [android.webkit.WebChromeClient.CustomViewCallback](https://developer.android.com/reference/kotlin/android/webkit/WebChromeClient.CustomViewCallback#) |

A callback interface used by the host application to notify the current page that its custom view has been dismissed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCustomViewHidden](https://developer.android.com/reference/kotlin/android/webkit/WebChromeClient.CustomViewCallback#onCustomViewHidden())`()` Invoked when the host application dismisses the custom view. |

## Public methods

### onCustomViewHidden

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCustomViewHidden(): Unit
```

Invoked when the host application dismisses the custom view.
