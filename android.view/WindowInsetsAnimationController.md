# WindowInsetsAnimationController

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WindowInsetsAnimationController

Kotlin| [Java](https://developer.android.com/reference/android/view/WindowInsetsAnimationController "View this page in Java") 
| --- | --- |

```
interface WindowInsetsAnimationController
```

| [android.view.WindowInsetsAnimationController](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#) |

Controller for app-driven animation of system windows.

`WindowInsetsAnimationController`lets apps animate system windows such as the [IME](https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#). The animation is synchronized, such that changes the system windows and the app's current frame are rendered at the same time.

Control is obtained through [WindowInsetsController.controlWindowInsetsAnimation](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#controlWindowInsetsAnimation(kotlin.Int,%20kotlin.Long,%20android.view.animation.Interpolator,%20android.os.CancellationSignal,%20android.view.WindowInsetsAnimationControlListener)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finish](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#finish(kotlin.Boolean))`(`shown:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Finishes the animation, and leaves the windows shown or hidden. |
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getCurrentAlpha](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#getCurrentAlpha())`()` Current alpha value of the window. |
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getCurrentFraction](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#getCurrentFraction())`()` Returns the progress as previously set by`fraction`in [setInsetsAndAlpha](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#setInsetsAndAlpha(android.graphics.Insets,%20kotlin.Float,%20kotlin.Float)) |
| --- | --- |
| abstract [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | [getCurrentInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#getCurrentInsets())`()` Retrieves the current insets. |
| abstract [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | [getHiddenStateInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#getHiddenStateInsets())`()` Retrieves the [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) when the windows this animation is controlling are fully hidden. |
| abstract [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | [getShownStateInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#getShownStateInsets())`()` Retrieves the [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) when the windows this animation is controlling are fully shown. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTypes](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#getTypes())`()` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCancelled](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#isCancelled())`()` Returns whether this instance has been cancelled by the system, or by invoking the [android.os.CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#) passed into [WindowInsetsController.controlWindowInsetsAnimation](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#controlWindowInsetsAnimation(kotlin.Int,%20kotlin.Long,%20android.view.animation.Interpolator,%20android.os.CancellationSignal,%20android.view.WindowInsetsAnimationControlListener)). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFinished](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#isFinished())`()` Returns whether this instance has been finished by a call to [finish](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#finish(kotlin.Boolean)). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReady](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#isReady())`()` Returns whether this instance is ready to be used to control window insets. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInsetsAndAlpha](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#setInsetsAndAlpha(android.graphics.Insets,%20kotlin.Float,%20kotlin.Float))`(`insets:` ` [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#)?`, `alpha:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Modifies the insets for the frame being drawn by indirectly moving the windows around in the system that are causing window insets. |

## Public methods

### finish

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun finish(shown: Boolean): Unit
```

Finishes the animation, and leaves the windows shown or hidden.

After invoking [finish](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#finish(kotlin.Boolean)), this instance is no longer [ready](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#isReady()).

Note: Finishing an animation implicitly [sets insets and alpha](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#setInsetsAndAlpha(android.graphics.Insets,%20kotlin.Float,%20kotlin.Float))according to the requested end state without any further animation.

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

Returns the progress as previously set by`fraction`in [setInsetsAndAlpha](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#setInsetsAndAlpha(android.graphics.Insets,%20kotlin.Float,%20kotlin.Float))

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the progress of the animation, where`0`is fully hidden and`1`is fully shown. Note: this value represents raw overall progress of the animation i.e. the combined progress of insets and alpha. Value is between 0.0f and 1.0f inclusive |

### getCurrentInsets

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCurrentInsets(): Insets
```

Retrieves the current insets.

Note that these insets are always relative to the window, which is the same as being relative to [View.getRootView](https://developer.android.com/reference/kotlin/android/view/View#getRootView())

| Return ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | The current insets on the currently showing frame. These insets will change as the animation progresses to reflect the current insets provided by the controlled window. This value cannot be`null`. |

### getHiddenStateInsets

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getHiddenStateInsets(): Insets
```

Retrieves the [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) when the windows this animation is controlling are fully hidden.

Note that these insets are always relative to the window, which is the same as being relative to [View.getRootView](https://developer.android.com/reference/kotlin/android/view/View#getRootView())

If there are any animation listeners registered, this value is the same as [Bounds.getLowerBound()](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Bounds#getLowerBound())that is being be passed into the root view of the hierarchy.

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | Insets when the windows this animation is controlling are fully hidden. This value cannot be`null`. |

**See Also**

- [android.view.WindowInsetsAnimation.Bounds#getLowerBound()](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Bounds#getLowerBound()) 

### getShownStateInsets

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getShownStateInsets(): Insets
```

Retrieves the [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) when the windows this animation is controlling are fully shown.

Note that these insets are always relative to the window, which is the same as being relative to [View.getRootView](https://developer.android.com/reference/kotlin/android/view/View#getRootView())

If there are any animation listeners registered, this value is the same as [Bounds.getUpperBound()](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Bounds#getUpperBound())that is being passed into the root view of hierarchy.

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | Insets when the windows this animation is controlling are fully shown. This value cannot be`null`. |

**See Also**

- [android.view.WindowInsetsAnimation.Bounds#getUpperBound()](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Bounds#getUpperBound()) 

### getTypes

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTypes(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The [WindowInsets.Type](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type) s this object is currently controlling. Value is either`0`or a combination of android.view.WindowInsets.Type.STATUS_BARS, android.view.WindowInsets.Type.NAVIGATION_BARS, android.view.WindowInsets.Type.CAPTION_BAR, android.view.WindowInsets.Type.IME, android.view.WindowInsets.Type.SYSTEM_GESTURES, android.view.WindowInsets.Type.MANDATORY_SYSTEM_GESTURES, android.view.WindowInsets.Type.TAPPABLE_ELEMENT, android.view.WindowInsets.Type.DISPLAY_CUTOUT, and android.view.WindowInsets.Type.SYSTEM_OVERLAYS |

### isCancelled

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isCancelled(): Boolean
```

Returns whether this instance has been cancelled by the system, or by invoking the [android.os.CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#) passed into [WindowInsetsController.controlWindowInsetsAnimation](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#controlWindowInsetsAnimation(kotlin.Int,%20kotlin.Long,%20android.view.animation.Interpolator,%20android.os.CancellationSignal,%20android.view.WindowInsetsAnimationControlListener)).

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the instance is cancelled,`false`otherwise. |

**See Also**

- [android.view.WindowInsetsAnimationControlListener#onCancelled](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationControlListener#onCancelled(android.view.WindowInsetsAnimationController)) 

### isFinished

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isFinished(): Boolean
```

Returns whether this instance has been finished by a call to [finish](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#finish(kotlin.Boolean)).

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the instance is finished,`false`otherwise. |

**See Also**

- [android.view.WindowInsetsAnimationControlListener#onFinished](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationControlListener#onFinished(android.view.WindowInsetsAnimationController)) 

### isReady

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isReady(): Boolean
```

Returns whether this instance is ready to be used to control window insets.

Instances are ready when passed in [WindowInsetsAnimationControlListener.onReady](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationControlListener#onReady(android.view.WindowInsetsAnimationController,%20kotlin.Int))and stop being ready when it is either [finished](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#isFinished())or [cancelled](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#isCancelled()).

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

Note that these insets are always relative to the window, which is the same as being relative to [View.getRootView](https://developer.android.com/reference/kotlin/android/view/View#getRootView())

Also note that this will**not** inform the view system of a full inset change via [View.dispatchApplyWindowInsets](https://developer.android.com/reference/kotlin/android/view/View#dispatchApplyWindowInsets(android.view.WindowInsets))in order to avoid a full layout pass during the animation. If you'd like to animate views during a window inset animation, register a [WindowInsetsAnimation.Callback](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback) by calling [View.setWindowInsetsAnimationCallback(WindowInsetsAnimation.Callback)](https://developer.android.com/reference/kotlin/android/view/View#setWindowInsetsAnimationCallback(android.view.WindowInsetsAnimation.Callback))that will be notified about any insets change via [WindowInsetsAnimation.Callback.onProgress](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback#onProgress(android.view.WindowInsets,%20kotlin.collections.MutableList))during the animation.

[View.dispatchApplyWindowInsets](https://developer.android.com/reference/kotlin/android/view/View#dispatchApplyWindowInsets(android.view.WindowInsets))will instead be called once the animation has finished, i.e. once [finish](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#finish(kotlin.Boolean))has been called. Note: If there are no insets, alpha animation is still applied.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `insets` | [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#)?:The new insets to apply. Based on the requested insets, the system will calculate the positions of the windows in the system causing insets such that the resulting insets of that configuration will match the passed in parameter. Note that these insets are being clamped to the range from [getHiddenStateInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#getHiddenStateInsets())to [getShownStateInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#getShownStateInsets()). If you intend on changing alpha only, pass null or [getCurrentInsets()](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#getCurrentInsets()). |
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The new alpha to apply to the inset side. Value is between 0.0f and 1.0f inclusive |
| `fraction` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):instantaneous animation progress. This value is dispatched to [WindowInsetsAnimation.Callback](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback). Value is between 0.0f and 1.0f inclusive |
| --- | --- |

**See Also**

- [android.view.WindowInsetsAnimation.Callback](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback)
- [android.view.View#setWindowInsetsAnimationCallback(WindowInsetsAnimation.Callback)](https://developer.android.com/reference/kotlin/android/view/View#setWindowInsetsAnimationCallback(android.view.WindowInsetsAnimation.Callback))
