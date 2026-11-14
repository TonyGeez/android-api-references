# View.OnSystemUiVisibilityChangeListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnSystemUiVisibilityChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/view/View.OnSystemUiVisibilityChangeListener "View this page in Java") 

```
interface OnSystemUiVisibilityChangeListener
```

| [android.view.View.OnSystemUiVisibilityChangeListener](https://developer.android.com/reference/kotlin/android/view/View.OnSystemUiVisibilityChangeListener#) |

| **This interface was deprecated in API level 30.**
|
| Use [WindowInsets.isVisible(int)](https://developer.android.com/reference/kotlin/android/view/WindowInsets#isVisible(kotlin.Int))to find out about system bar visibilities by setting a [OnApplyWindowInsetsListener](https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener) on this view.

Interface definition for a callback to be invoked when the status bar changes visibility. This reports**global**changes to the system UI state, not what the application is requesting.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSystemUiVisibilityChange](https://developer.android.com/reference/kotlin/android/view/View.OnSystemUiVisibilityChangeListener#onSystemUiVisibilityChange(kotlin.Int))`(`visibility:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the status bar changes visibility because of a call to [View.setSystemUiVisibility(int)](https://developer.android.com/reference/kotlin/android/view/View#setSystemUiVisibility(kotlin.Int)). |

## Public methods

### onSystemUiVisibilityChange

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSystemUiVisibilityChange(visibility: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the status bar changes visibility because of a call to [View.setSystemUiVisibility(int)](https://developer.android.com/reference/kotlin/android/view/View#setSystemUiVisibility(kotlin.Int)).

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `visibility` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Bitwise-or of flags [SYSTEM_UI_FLAG_LOW_PROFILE](https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_LOW_PROFILE:kotlin.Int), [SYSTEM_UI_FLAG_HIDE_NAVIGATION](https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int), and [SYSTEM_UI_FLAG_FULLSCREEN](https://developer.android.com/reference/kotlin/android/view/View#SYSTEM_UI_FLAG_FULLSCREEN:kotlin.Int). This tells you the**global**state of these UI visibility flags, not what your app is currently applying. |
