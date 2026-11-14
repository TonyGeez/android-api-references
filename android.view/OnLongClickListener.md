# View.OnLongClickListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnLongClickListener

Kotlin | [Java](https://developer.android.com/reference/android/view/View.OnLongClickListener "View this page in Java") 

```
interface OnLongClickListener
```

| [android.view.View.OnLongClickListener](https://developer.android.com/reference/kotlin/android/view/View.OnLongClickListener#) |

| Known Direct Subclasses [ZoomButton](https://developer.android.com/reference/kotlin/android/widget/ZoomButton.html#) |----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------| | [ZoomButton](https://developer.android.com/reference/kotlin/android/widget/ZoomButton.html#) | This widget provides a simple utility for turning a continued long-press event into a series of clicks at some set frequency. | |

Interface definition for a callback to be invoked when a view has been clicked and held.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLongClick](https://developer.android.com/reference/kotlin/android/view/View.OnLongClickListener#onLongClick(android.view.View))`(`v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`)` Called when a view has been clicked and held. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLongClickUseDefaultHapticFeedback](https://developer.android.com/reference/kotlin/android/view/View.OnLongClickListener#onLongClickUseDefaultHapticFeedback(android.view.View))`(`v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)`)` Returns whether the default [HapticFeedbackConstants.LONG_PRESS](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#LONG_PRESS:kotlin.Int) haptic feedback is performed when this listener has consumed the long click. |

## Public methods

### onLongClick

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onLongClick(v: View!): Boolean
```

Called when a view has been clicked and held.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------|
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: The view that was clicked and held. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the callback consumed the long click, false otherwise. |

### onLongClickUseDefaultHapticFeedback

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onLongClickUseDefaultHapticFeedback(v: View): Boolean
```

Returns whether the default [HapticFeedbackConstants.LONG_PRESS](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#LONG_PRESS:kotlin.Int) haptic feedback is performed when this listener has consumed the long click. This method is called immediately after [onLongClick](https://developer.android.com/reference/kotlin/android/view/View.OnLongClickListener#onLongClick(android.view.View)) has returned true.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------------------|
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View): The view that was clicked and held. This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true to perform the default [HapticFeedbackConstants.LONG_PRESS](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#LONG_PRESS:kotlin.Int) haptic feedback, or false if the handler manages all haptics itself. |
