# WindowInsetsAnimation

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WindowInsetsAnimation

Kotlin| [Java](WindowInsetsAnimation.md) 
| --- | --- |

```
class WindowInsetsAnimation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.WindowInsetsAnimation](WindowInsetsAnimation.md) |

Class representing an animation of a set of windows that cause insets.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Bounds](../android/view/WindowInsetsAnimation.Bounds.md) Class representing the range of an [WindowInsetsAnimation](WindowInsetsAnimation.md) |
| abstract | [Callback](../android/view/WindowInsetsAnimation.Callback.md) Interface that allows the application to listen to animation events for windows that cause insets. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WindowInsetsAnimation](WindowInsetsAnimation.md))`(`typeMask:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `interpolator:` ` [Interpolator](../android.view.animation/Interpolator.md)?`, `durationMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Creates a new [WindowInsetsAnimation](WindowInsetsAnimation.md) object. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getAlpha](WindowInsetsAnimation.md))`()` Retrieves the translucency of the windows that are animating. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDurationMillis](WindowInsetsAnimation.md))`()` <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFraction](WindowInsetsAnimation.md))`()` Returns the raw fractional progress of this animation between start state of the animation and the end state of the animation. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getInterpolatedFraction](WindowInsetsAnimation.md))`()` Returns the interpolated fractional progress of this animation between start state of the animation and the end state of the animation. |
| [Interpolator](../android.view.animation/Interpolator.md)? | [getInterpolator](WindowInsetsAnimation.md))`()` Retrieves the interpolator used for this animation, or`null`if this animation doesn't follow an interpolation curved. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTypeMask](WindowInsetsAnimation.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAlpha](WindowInsetsAnimation.md))`(`alpha:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the translucency of the windows that are animating. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFraction](WindowInsetsAnimation.md))`(`fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set fraction of the progress if [WindowInsets.Type](../android/view/WindowInsets.Type.md) animation is controlled by the app. |

## Public constructors

### WindowInsetsAnimation

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WindowInsetsAnimation(
    typeMask: Int, 
    interpolator: Interpolator?, 
    durationMillis: Long)
```

Creates a new [WindowInsetsAnimation](WindowInsetsAnimation.md) object.

This should only be used for testing, as usually the system creates this object for the application to listen to with [Callback](../android/view/WindowInsetsAnimation.Callback.md).

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `typeMask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The bitmask of [WindowInsets.Type](../android/view/WindowInsets.Type.md) s that are animating. Value is either`0`or a combination of android.view.WindowInsets.Type.STATUS_BARS, android.view.WindowInsets.Type.NAVIGATION_BARS, android.view.WindowInsets.Type.CAPTION_BAR, android.view.WindowInsets.Type.IME, android.view.WindowInsets.Type.SYSTEM_GESTURES, android.view.WindowInsets.Type.MANDATORY_SYSTEM_GESTURES, android.view.WindowInsets.Type.TAPPABLE_ELEMENT, android.view.WindowInsets.Type.DISPLAY_CUTOUT, and android.view.WindowInsets.Type.SYSTEM_OVERLAYS |
| `interpolator` | [Interpolator](../android.view.animation/Interpolator.md)?:The interpolator of the animation. This value may be`null`. |
| `durationMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The duration of the animation in [java.util.concurrent.TimeUnit#MILLISECONDS](../java.util.concurrent/TimeUnit.md). |
| --- | --- |

## Public methods

### getAlpha

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAlpha(): Float
```

Retrieves the translucency of the windows that are animating.

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | Alpha of windows that cause insets of type [WindowInsets.Type](../android/view/WindowInsets.Type.md). Value is between 0.0f and 1.0f inclusive |

### getDurationMillis

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDurationMillis(): Long
```

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | duration of animation in [java.util.concurrent.TimeUnit#MILLISECONDS](../java.util.concurrent/TimeUnit.md), or -1 if the animation doesn't have a fixed duration. |

### getFraction

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFraction(): Float
```

Returns the raw fractional progress of this animation between start state of the animation and the end state of the animation. Note that this progress is the global progress of the animation, whereas [Callback.onProgress](../android/view/WindowInsetsAnimation.Callback.md))will only dispatch the insets that may be inset with android.view.WindowInsets#inset by parents of views in the hierarchy. Progress per insets animation is global for the entire animation. One animation animates all things together (in, out, ...). If they don't animate together, we'd have multiple animations.

Note: In case the application is controlling the animation, the valued returned here will be the same as the application passed into [WindowInsetsAnimationController.setInsetsAndAlpha(Insets, float, float)](WindowInsetsAnimationController.md)).

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The current progress of this animation. Value is between 0.0f and 1.0f inclusive |

### getInterpolatedFraction

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInterpolatedFraction(): Float
```

Returns the interpolated fractional progress of this animation between start state of the animation and the end state of the animation. Note that this progress is the global progress of the animation, whereas [Callback.onProgress](../android/view/WindowInsetsAnimation.Callback.md))will only dispatch the insets that may be inset with android.view.WindowInsets#inset by parents of views in the hierarchy. Progress per insets animation is global for the entire animation. One animation animates all things together (in, out, ...). If they don't animate together, we'd have multiple animations.

Note: In case the application is controlling the animation, the valued returned here will be the same as the application passed into [WindowInsetsAnimationController.setInsetsAndAlpha(Insets, float, float)](WindowInsetsAnimationController.md)), interpolated with the interpolator passed into [WindowInsetsController.controlWindowInsetsAnimation](WindowInsetsController.md)).

Note: For system-initiated animations, this will always return a valid value between 0 and 1.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The current interpolated progress of this animation. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation#getFraction()> 

### getInterpolator

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInterpolator(): Interpolator?
```

Retrieves the interpolator used for this animation, or`null`if this animation doesn't follow an interpolation curved. For system-initiated animations, this will never return`null`.

| Return ||
|-----------------------------------------------------------------------------------------------------|-------------------------------------------|
| [Interpolator](../android.view.animation/Interpolator.md)? | The interpolator used for this animation. |

### getTypeMask

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTypeMask(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The bitmask of [WindowInsets.Type](../android/view/WindowInsets.Type.md) s that are animating. Value is either`0`or a combination of android.view.WindowInsets.Type.STATUS_BARS, android.view.WindowInsets.Type.NAVIGATION_BARS, android.view.WindowInsets.Type.CAPTION_BAR, android.view.WindowInsets.Type.IME, android.view.WindowInsets.Type.SYSTEM_GESTURES, android.view.WindowInsets.Type.MANDATORY_SYSTEM_GESTURES, android.view.WindowInsets.Type.TAPPABLE_ELEMENT, android.view.WindowInsets.Type.DISPLAY_CUTOUT, and android.view.WindowInsets.Type.SYSTEM_OVERLAYS |

### setAlpha

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setAlpha(alpha: Float): Unit
```

Sets the translucency of the windows that are animating.

Note: This should only be used for testing, as the system fills in the alpha for the application or the alpha that was passed into [WindowInsetsAnimationController.setInsetsAndAlpha(Insets, float, float)](WindowInsetsAnimationController.md))is being used.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Alpha of windows that cause insets of type [WindowInsets.Type](../android/view/WindowInsets.Type.md). Value is between 0.0f and 1.0f inclusive |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation#getAlpha()> 

### setFraction

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setFraction(fraction: Float): Unit
```

Set fraction of the progress if [WindowInsets.Type](../android/view/WindowInsets.Type.md) animation is controlled by the app.

Note: This should only be used for testing, as the system fills in the fraction for the application or the fraction that was passed into [WindowInsetsAnimationController.setInsetsAndAlpha(Insets, float, float)](WindowInsetsAnimationController.md))is being used.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fraction` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):fractional progress between 0 and 1 where 0 represents hidden and zero progress and 1 represent fully shown final state. Value is between 0.0f and 1.0f inclusive |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation#getFraction()>
