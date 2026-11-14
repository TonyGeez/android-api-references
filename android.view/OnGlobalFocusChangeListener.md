# ViewTreeObserver.OnGlobalFocusChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnGlobalFocusChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/view/ViewTreeObserver.OnGlobalFocusChangeListener "View this page in Java") 

```
interface OnGlobalFocusChangeListener
```

| [android.view.ViewTreeObserver.OnGlobalFocusChangeListener](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnGlobalFocusChangeListener#) |

| Known Direct Subclasses [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView.html#) |----------------------------------------------------------------------------------------|---------------------------------| | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView.html#) | A View that displays web pages. | |

Interface definition for a callback to be invoked when the focus state within the view tree changes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGlobalFocusChanged](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnGlobalFocusChangeListener#onGlobalFocusChanged(android.view.View,%20android.view.View))`(`oldFocus:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`, `newFocus:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`)` Callback method to be invoked when the focus changes in the view tree. |

## Public methods

### onGlobalFocusChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGlobalFocusChanged(
    oldFocus: View!, 
    newFocus: View!
): Unit
```

Callback method to be invoked when the focus changes in the view tree. When the view tree transitions from touch mode to non-touch mode, oldFocus is null. When the view tree transitions from non-touch mode to touch mode, newFocus is null. When focus changes in non-touch mode (without transition from or to touch mode) either oldFocus or newFocus can be null.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------|
| `oldFocus` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:The previously focused view, if any. |
| `newFocus` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:The newly focused View, if any. |
