# ViewTreeObserver.OnGlobalFocusChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnGlobalFocusChangeListener

Kotlin| [Java](../android/view/ViewTreeObserver.OnGlobalFocusChangeListener.md) 
| --- | --- |

```
interface OnGlobalFocusChangeListener
```

| [android.view.ViewTreeObserver.OnGlobalFocusChangeListener](../android/view/ViewTreeObserver.OnGlobalFocusChangeListener.md) |

| Known Direct Subclasses [WebView](../android/webkit/WebView.md) |----------------------------------------------------------------------------------------|---------------------------------| | [WebView](../android/webkit/WebView.md) | A View that displays web pages. | |
| --- | --- | --- | --- | --- | --- | --- |

Interface definition for a callback to be invoked when the focus state within the view tree changes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGlobalFocusChanged](../android/view/ViewTreeObserver.OnGlobalFocusChangeListener.md))`(`oldFocus:` ` [View](../android/view/View.md)!`, `newFocus:` ` [View](../android/view/View.md)!`)` Callback method to be invoked when the focus changes in the view tree. |

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
| `oldFocus` | [View](../android/view/View.md)!:The previously focused view, if any. |
| `newFocus` | [View](../android/view/View.md)!:The newly focused View, if any. |
