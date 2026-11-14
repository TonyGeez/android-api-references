# TimeInterpolator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TimeInterpolator

Kotlin| [Java](https://developer.android.com/reference/android/animation/TimeInterpolator "View this page in Java") 

```
interface TimeInterpolator
```

| [android.animation.TimeInterpolator](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator#) |

| Known Direct Subclasses [Interpolator](https://developer.android.com/reference/kotlin/android/view/animation/Interpolator.html#) |----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------| | [Interpolator](https://developer.android.com/reference/kotlin/android/view/animation/Interpolator.html#) | An interpolator defines the rate of change of an animation. | |

| Known Indirect Subclasses [AccelerateDecelerateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AccelerateDecelerateInterpolator.html#), [AccelerateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AccelerateInterpolator.html#), [AnticipateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AnticipateInterpolator.html#), [AnticipateOvershootInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AnticipateOvershootInterpolator.html#), [BaseInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/BaseInterpolator.html#), [BounceInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/BounceInterpolator.html#), [CycleInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/CycleInterpolator.html#), [DecelerateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/DecelerateInterpolator.html#), [LinearInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/LinearInterpolator.html#), [OvershootInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/OvershootInterpolator.html#), [PathInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/PathInterpolator.html#) |--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------| | [AccelerateDecelerateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AccelerateDecelerateInterpolator.html#) | An interpolator where the rate of change starts and ends slowly but accelerates through the middle. | | [AccelerateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AccelerateInterpolator.html#) | An interpolator where the rate of change starts out slowly and and then accelerates. | | [AnticipateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AnticipateInterpolator.html#) | An interpolator where the change starts backward then flings forward. | | [AnticipateOvershootInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AnticipateOvershootInterpolator.html#) | An interpolator where the change starts backward then flings forward and overshoots the target value and finally goes back to the final value. | | [BaseInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/BaseInterpolator.html#) | An abstract class which is extended by default interpolators. | | [BounceInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/BounceInterpolator.html#) | An interpolator where the change bounces at the end. | | [CycleInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/CycleInterpolator.html#) | Repeats the animation for a specified number of cycles. | | [DecelerateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/DecelerateInterpolator.html#) | An interpolator where the rate of change starts out quickly and and then decelerates. | | [LinearInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/LinearInterpolator.html#) | An interpolator where the rate of change is constant | | [OvershootInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/OvershootInterpolator.html#) | An interpolator where the change flings forward and overshoots the last value then comes back. | | [PathInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/PathInterpolator.html#) | An interpolator that can traverse a Path that extends from`Point``(0, 0)`to`(1, 1)`. | |

A time interpolator defines the rate of change of an animation. This allows animations to have non-linear motion, such as acceleration and deceleration.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getInterpolation](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator#getInterpolation(kotlin.Float))`(`input:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Maps a value representing the elapsed fraction of an animation to a value that represents the interpolated fraction. |

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
