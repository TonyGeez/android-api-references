# View.OnLongClickListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnLongClickListener

Kotlin | [Java](../android/view/View.OnLongClickListener.md) 
| --- | --- |

```
interface OnLongClickListener
```

| [android.view.View.OnLongClickListener](../android/view/View.OnLongClickListener.md) |

| Known Direct Subclasses [ZoomButton](../android.widget/ZoomButton.md) |----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------| | [ZoomButton](../android.widget/ZoomButton.md) | This widget provides a simple utility for turning a continued long-press event into a series of clicks at some set frequency. | |
| --- | --- | --- | --- | --- | --- | --- |

Interface definition for a callback to be invoked when a view has been clicked and held.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLongClick](../android/view/View.OnLongClickListener.md))`(`v:` ` [View](View.md)!`)` Called when a view has been clicked and held. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onLongClickUseDefaultHapticFeedback](../android/view/View.OnLongClickListener.md))`(`v:` ` [View](View.md)`)` Returns whether the default [HapticFeedbackConstants.LONG_PRESS](HapticFeedbackConstants.md) haptic feedback is performed when this listener has consumed the long click. |

## Public methods

### onLongClick

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onLongClick(v: View!): Boolean
```

Called when a view has been clicked and held.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------|
| `v` | [View](View.md)!: The view that was clicked and held. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the callback consumed the long click, false otherwise. |

### onLongClickUseDefaultHapticFeedback

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onLongClickUseDefaultHapticFeedback(v: View): Boolean
```

Returns whether the default [HapticFeedbackConstants.LONG_PRESS](HapticFeedbackConstants.md) haptic feedback is performed when this listener has consumed the long click. This method is called immediately after [onLongClick](../android/view/View.OnLongClickListener.md)) has returned true.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------------------|
| `v` | [View](View.md): The view that was clicked and held. This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true to perform the default [HapticFeedbackConstants.LONG_PRESS](HapticFeedbackConstants.md) haptic feedback, or false if the handler manages all haptics itself. |
