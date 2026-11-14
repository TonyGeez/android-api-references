# WindowInsetsAnimationController

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WindowInsetsAnimationController

Kotlin| [Java](WindowInsetsAnimationController.md) 
| --- | --- |

```
interface WindowInsetsAnimationController
```

| [android.view.WindowInsetsAnimationController](WindowInsetsAnimationController.md) |

Controller for app-driven animation of system windows.

`WindowInsetsAnimationController`lets apps animate system windows such as the [IME](../android.inputmethodservice/InputMethodService.md). The animation is synchronized, such that changes the system windows and the app's current frame are rendered at the same time.

Control is obtained through [WindowInsetsController.controlWindowInsetsAnimation](WindowInsetsController.md)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finish](WindowInsetsAnimationController.md))`(`shown:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Finishes the animation, and leaves the windows shown or hidden. |
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getCurrentAlpha](WindowInsetsAnimationController.md))`()` Current alpha value of the window. |
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getCurrentFraction](WindowInsetsAnimationController.md))`()` Returns the progress as previously set by`fraction`in [setInsetsAndAlpha](WindowInsetsAnimationController.md)) |
| --- | --- |
| abstract [Insets](../android.graphics/Insets.md) | [getCurrentInsets](WindowInsetsAnimationController.md))`()` Retrieves the current insets. |
| abstract [Insets](../android.graphics/Insets.md) | [getHiddenStateInsets](WindowInsetsAnimationController.md))`()` Retrieves the [Insets](../android.graphics/Insets.md) when the windows this animation is controlling are fully hidden. |
| abstract [Insets](../android.graphics/Insets.md) | [getShownStateInsets](WindowInsetsAnimationController.md))`()` Retrieves the [Insets](../android.graphics/Insets.md) when the windows this animation is controlling are fully shown. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTypes](WindowInsetsAnimationController.md))`()` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCancelled](WindowInsetsAnimationController.md))`()` Returns whether this instance has been cancelled by the system, or by invoking the [android.os.CancellationSignal](../android.os/CancellationSignal.md) passed into [WindowInsetsController.controlWindowInsetsAnimation](WindowInsetsController.md)). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFinished](WindowInsetsAnimationController.md))`()` Returns whether this instance has been finished by a call to [finish](WindowInsetsAnimationController.md)). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReady](WindowInsetsAnimationController.md))`()` Returns whether this instance is ready to be used to control window insets. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInsetsAndAlpha](WindowInsetsAnimationController.md))`(`insets:` ` [Insets](../android.graphics/Insets.md)?`, `alpha:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Modifies the insets for the frame being drawn by indirectly moving the windows around in the system that are causing window insets. |

## Public methods

### finish

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun finish(shown: Boolean): Unit
```

Finishes the animation, and leaves the windows shown or hidden.

After invoking [finish](WindowInsetsAnimationController.md)), this instance is no longer [ready](WindowInsetsAnimationController.md)).

Note: Finishing an animation implicitly [sets insets and alpha](WindowInsetsAnimationController.md))according to the requested end state without any further animation.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `shown` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`, the windows will be shown after finishing the animation. Otherwise they will be hidden. |

### getCurrentAlpha

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCurrentAlpha(): Float
```

Current alpha value of the window.

| Return ||
|--------------------------------------------------------------------------------|------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | float value between 0 and 1. |

### getCurrentFraction

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCurrentFraction(): Float
```

Returns the progress as previously set by`fraction`in [setInsetsAndAlpha](WindowInsetsAnimationController.md))

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the progress of the animation, where`0`is fully hidden and`1`is fully shown. Note: this value represents raw overall progress of the animation i.e. the combined progress of insets and alpha. Value is between 0.0f and 1.0f inclusive |

### getCurrentInsets

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCurrentInsets(): Insets
```

Retrieves the current insets.

Note that these insets are always relative to the window, which is the same as being relative to [View.getRootView](View.md))

| Return ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Insets](../android.graphics/Insets.md) | The current insets on the currently showing frame. These insets will change as the animation progresses to reflect the current insets provided by the controlled window. This value cannot be`null`. |

### getHiddenStateInsets

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getHiddenStateInsets(): Insets
```

Retrieves the [Insets](../android.graphics/Insets.md) when the windows this animation is controlling are fully hidden.

Note that these insets are always relative to the window, which is the same as being relative to [View.getRootView](View.md))

If there are any animation listeners registered, this value is the same as [Bounds.getLowerBound()](../android/view/WindowInsetsAnimation.Bounds.md))that is being be passed into the root view of the hierarchy.

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Insets](../android.graphics/Insets.md) | Insets when the windows this animation is controlling are fully hidden. This value cannot be`null`. |

**See Also**

- [android.view.WindowInsetsAnimation.Bounds#getLowerBound()](../android/view/WindowInsetsAnimation.Bounds.md)) 

### getShownStateInsets

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getShownStateInsets(): Insets
```

Retrieves the [Insets](../android.graphics/Insets.md) when the windows this animation is controlling are fully shown.

Note that these insets are always relative to the window, which is the same as being relative to [View.getRootView](View.md))

If there are any animation listeners registered, this value is the same as [Bounds.getUpperBound()](../android/view/WindowInsetsAnimation.Bounds.md))that is being passed into the root view of hierarchy.

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Insets](../android.graphics/Insets.md) | Insets when the windows this animation is controlling are fully shown. This value cannot be`null`. |

**See Also**

- [android.view.WindowInsetsAnimation.Bounds#getUpperBound()](../android/view/WindowInsetsAnimation.Bounds.md)) 

### getTypes

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTypes(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The [WindowInsets.Type](../android/view/WindowInsets.Type.md) s this object is currently controlling. Value is either`0`or a combination of android.view.WindowInsets.Type.STATUS_BARS, android.view.WindowInsets.Type.NAVIGATION_BARS, android.view.WindowInsets.Type.CAPTION_BAR, android.view.WindowInsets.Type.IME, android.view.WindowInsets.Type.SYSTEM_GESTURES, android.view.WindowInsets.Type.MANDATORY_SYSTEM_GESTURES, android.view.WindowInsets.Type.TAPPABLE_ELEMENT, android.view.WindowInsets.Type.DISPLAY_CUTOUT, and android.view.WindowInsets.Type.SYSTEM_OVERLAYS |

### isCancelled

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isCancelled(): Boolean
```

Returns whether this instance has been cancelled by the system, or by invoking the [android.os.CancellationSignal](../android.os/CancellationSignal.md) passed into [WindowInsetsController.controlWindowInsetsAnimation](WindowInsetsController.md)).

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the instance is cancelled,`false`otherwise. |

**See Also**

- [android.view.WindowInsetsAnimationControlListener#onCancelled](WindowInsetsAnimationControlListener.md)) 

### isFinished

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isFinished(): Boolean
```

Returns whether this instance has been finished by a call to [finish](WindowInsetsAnimationController.md)).

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the instance is finished,`false`otherwise. |

**See Also**

- [android.view.WindowInsetsAnimationControlListener#onFinished](WindowInsetsAnimationControlListener.md)) 

### isReady

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isReady(): Boolean
```

Returns whether this instance is ready to be used to control window insets.

Instances are ready when passed in [WindowInsetsAnimationControlListener.onReady](WindowInsetsAnimationControlListener.md))and stop being ready when it is either [finished](WindowInsetsAnimationController.md))or [cancelled](WindowInsetsAnimationController.md)).

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the instance is ready,`false`otherwise. |

### setInsetsAndAlpha

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setInsetsAndAlpha(
    insets: Insets?, 
    alpha: Float, 
    fraction: Float
): Unit
```

Modifies the insets for the frame being drawn by indirectly moving the windows around in the system that are causing window insets.

Note that these insets are always relative to the window, which is the same as being relative to [View.getRootView](View.md))

Also note that this will**not** inform the view system of a full inset change via [View.dispatchApplyWindowInsets](View.md))in order to avoid a full layout pass during the animation. If you'd like to animate views during a window inset animation, register a [WindowInsetsAnimation.Callback](../android/view/WindowInsetsAnimation.Callback.md) by calling [View.setWindowInsetsAnimationCallback(WindowInsetsAnimation.Callback)](View.md))that will be notified about any insets change via [WindowInsetsAnimation.Callback.onProgress](../android/view/WindowInsetsAnimation.Callback.md))during the animation.

[View.dispatchApplyWindowInsets](View.md))will instead be called once the animation has finished, i.e. once [finish](WindowInsetsAnimationController.md))has been called. Note: If there are no insets, alpha animation is still applied.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `insets` | [Insets](../android.graphics/Insets.md)?:The new insets to apply. Based on the requested insets, the system will calculate the positions of the windows in the system causing insets such that the resulting insets of that configuration will match the passed in parameter. Note that these insets are being clamped to the range from [getHiddenStateInsets](WindowInsetsAnimationController.md))to [getShownStateInsets](WindowInsetsAnimationController.md)). If you intend on changing alpha only, pass null or [getCurrentInsets()](WindowInsetsAnimationController.md)). |
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The new alpha to apply to the inset side. Value is between 0.0f and 1.0f inclusive |
| `fraction` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):instantaneous animation progress. This value is dispatched to [WindowInsetsAnimation.Callback](../android/view/WindowInsetsAnimation.Callback.md). Value is between 0.0f and 1.0f inclusive |
| --- | --- |

**See Also**

- [android.view.WindowInsetsAnimation.Callback](../android/view/WindowInsetsAnimation.Callback.md)
- [android.view.View#setWindowInsetsAnimationCallback(WindowInsetsAnimation.Callback)](View.md))
