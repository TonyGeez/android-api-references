# TimeInterpolator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TimeInterpolator

Kotlin| [Java](../android/animation/TimeInterpolator.md) 
| --- | --- |

```
interface TimeInterpolator
```

| [android.animation.TimeInterpolator](../android/animation/TimeInterpolator.md) |

| Known Direct Subclasses [Interpolator](../android/view/animation/Interpolator.md) |----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------| | [Interpolator](../android/view/animation/Interpolator.md) | An interpolator defines the rate of change of an animation. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AccelerateDecelerateInterpolator](../android/view/animation/AccelerateDecelerateInterpolator.md), [AccelerateInterpolator](../android/view/animation/AccelerateInterpolator.md), [AnticipateInterpolator](../android/view/animation/AnticipateInterpolator.md), [AnticipateOvershootInterpolator](../android/view/animation/AnticipateOvershootInterpolator.md), [BaseInterpolator](../android/view/animation/BaseInterpolator.md), [BounceInterpolator](../android/view/animation/BounceInterpolator.md), [CycleInterpolator](../android/view/animation/CycleInterpolator.md), [DecelerateInterpolator](../android/view/animation/DecelerateInterpolator.md), [LinearInterpolator](../android/view/animation/LinearInterpolator.md), [OvershootInterpolator](../android/view/animation/OvershootInterpolator.md), [PathInterpolator](../android/view/animation/PathInterpolator.md) |--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------| | [AccelerateDecelerateInterpolator](../android/view/animation/AccelerateDecelerateInterpolator.md) | An interpolator where the rate of change starts and ends slowly but accelerates through the middle. | | [AccelerateInterpolator](../android/view/animation/AccelerateInterpolator.md) | An interpolator where the rate of change starts out slowly and and then accelerates. | | [AnticipateInterpolator](../android/view/animation/AnticipateInterpolator.md) | An interpolator where the change starts backward then flings forward. | | [AnticipateOvershootInterpolator](../android/view/animation/AnticipateOvershootInterpolator.md) | An interpolator where the change starts backward then flings forward and overshoots the target value and finally goes back to the final value. | | [BaseInterpolator](../android/view/animation/BaseInterpolator.md) | An abstract class which is extended by default interpolators. | | [BounceInterpolator](../android/view/animation/BounceInterpolator.md) | An interpolator where the change bounces at the end. | | [CycleInterpolator](../android/view/animation/CycleInterpolator.md) | Repeats the animation for a specified number of cycles. | | [DecelerateInterpolator](../android/view/animation/DecelerateInterpolator.md) | An interpolator where the rate of change starts out quickly and and then decelerates. | | [LinearInterpolator](../android/view/animation/LinearInterpolator.md) | An interpolator where the rate of change is constant | | [OvershootInterpolator](../android/view/animation/OvershootInterpolator.md) | An interpolator where the change flings forward and overshoots the last value then comes back. | | [PathInterpolator](../android/view/animation/PathInterpolator.md) | An interpolator that can traverse a Path that extends from`Point``(0, 0)`to`(1, 1)`. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A time interpolator defines the rate of change of an animation. This allows animations to have non-linear motion, such as acceleration and deceleration.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getInterpolation](../android/animation/TimeInterpolator.md))`(`input:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Maps a value representing the elapsed fraction of an animation to a value that represents the interpolated fraction. |

## Public methods

### getInterpolation

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getInterpolation(input: Float): Float
```

Maps a value representing the elapsed fraction of an animation to a value that represents the interpolated fraction. This interpolated value is then multiplied by the change in value of an animation to derive the animated value at the current elapsed animation time.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `input` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):A value between 0 and 1.0 indicating our current point in the animation where 0 represents the start and 1.0 represents the end |

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The interpolation value. This value can be more than 1.0 for interpolators which overshoot their targets, or less than 0 for interpolators that undershoot their targets. |
