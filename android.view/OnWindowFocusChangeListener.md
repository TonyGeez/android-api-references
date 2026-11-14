# ViewTreeObserver.OnWindowFocusChangeListener

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnWindowFocusChangeListener

Kotlin| [Java](../android/view/ViewTreeObserver.OnWindowFocusChangeListener.md) 
| --- | --- |

```
interface OnWindowFocusChangeListener
```

| [android.view.ViewTreeObserver.OnWindowFocusChangeListener](../android/view/ViewTreeObserver.OnWindowFocusChangeListener.md) |

Interface definition for a callback to be invoked when the view hierarchy's window focus state changes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onWindowFocusChanged](../android/view/ViewTreeObserver.OnWindowFocusChangeListener.md))`(`hasFocus:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Callback method to be invoked when the window focus changes in the view tree. |

## Public methods

### onWindowFocusChanged

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onWindowFocusChanged(hasFocus: Boolean): Unit
```

Callback method to be invoked when the window focus changes in the view tree.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `hasFocus` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Set to true if the window is gaining focus, false if it is losing focus. |
