# ViewTreeObserver.OnWindowAttachListener

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnWindowAttachListener

Kotlin| [Java](https://developer.android.com/reference/android/view/ViewTreeObserver.OnWindowAttachListener "View this page in Java") 
| --- | --- |

```
interface OnWindowAttachListener
```

| [android.view.ViewTreeObserver.OnWindowAttachListener](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnWindowAttachListener#) |

Interface definition for a callback to be invoked when the view hierarchy is attached to and detached from its window.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onWindowAttached](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnWindowAttachListener#onWindowAttached())`()` Callback method to be invoked when the view hierarchy is attached to a window |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onWindowDetached](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnWindowAttachListener#onWindowDetached())`()` Callback method to be invoked when the view hierarchy is detached from a window |

## Public methods

### onWindowAttached

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onWindowAttached(): Unit
```

Callback method to be invoked when the view hierarchy is attached to a window 

### onWindowDetached

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onWindowDetached(): Unit
```

Callback method to be invoked when the view hierarchy is detached from a window
