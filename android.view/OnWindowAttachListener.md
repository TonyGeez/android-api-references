# ViewTreeObserver.OnWindowAttachListener

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnWindowAttachListener

Kotlin| [Java](../android/view/ViewTreeObserver.OnWindowAttachListener.md) 
| --- | --- |

```
interface OnWindowAttachListener
```

| [android.view.ViewTreeObserver.OnWindowAttachListener](../android/view/ViewTreeObserver.OnWindowAttachListener.md) |

Interface definition for a callback to be invoked when the view hierarchy is attached to and detached from its window.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onWindowAttached](../android/view/ViewTreeObserver.OnWindowAttachListener.md))`()` Callback method to be invoked when the view hierarchy is attached to a window |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onWindowDetached](../android/view/ViewTreeObserver.OnWindowAttachListener.md))`()` Callback method to be invoked when the view hierarchy is detached from a window |

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
