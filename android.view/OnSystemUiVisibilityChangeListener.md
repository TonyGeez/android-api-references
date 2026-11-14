# View.OnSystemUiVisibilityChangeListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnSystemUiVisibilityChangeListener

Kotlin| [Java](../android/view/View.OnSystemUiVisibilityChangeListener.md) 
| --- | --- |

```
interface OnSystemUiVisibilityChangeListener
```

| [android.view.View.OnSystemUiVisibilityChangeListener](../android/view/View.OnSystemUiVisibilityChangeListener.md) |

| **This interface was deprecated in API level 30.**
|
| Use [WindowInsets.isVisible(int)](../android/view/WindowInsets.md))to find out about system bar visibilities by setting a [OnApplyWindowInsetsListener](../android/view/View.OnApplyWindowInsetsListener.md) on this view.

Interface definition for a callback to be invoked when the status bar changes visibility. This reports**global**changes to the system UI state, not what the application is requesting.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSystemUiVisibilityChange](../android/view/View.OnSystemUiVisibilityChangeListener.md))`(`visibility:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the status bar changes visibility because of a call to [View.setSystemUiVisibility(int)](../android/view/View.md)). |

## Public methods

### onSystemUiVisibilityChange

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSystemUiVisibilityChange(visibility: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the status bar changes visibility because of a call to [View.setSystemUiVisibility(int)](../android/view/View.md)).

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `visibility` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Bitwise-or of flags [SYSTEM_UI_FLAG_LOW_PROFILE](../android/view/View.md), [SYSTEM_UI_FLAG_HIDE_NAVIGATION](../android/view/View.md), and [SYSTEM_UI_FLAG_FULLSCREEN](../android/view/View.md). This tells you the**global**state of these UI visibility flags, not what your app is currently applying. |
