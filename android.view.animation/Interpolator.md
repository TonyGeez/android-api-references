# Interpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Interpolator

Kotlin| [Java](../android/view/animation/Interpolator.md) 
| --- | --- |

```
interface Interpolator : TimeInterpolator
```

| [android.view.animation.Interpolator](../android/view/animation/Interpolator.md) |

| Known Direct Subclasses [BaseInterpolator](../android/view/animation/BaseInterpolator.md) |------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------| | [BaseInterpolator](../android/view/animation/BaseInterpolator.md) | An abstract class which is extended by default interpolators. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AccelerateDecelerateInterpolator](../android/view/animation/AccelerateDecelerateInterpolator.md), [AccelerateInterpolator](../android/view/animation/AccelerateInterpolator.md), [AnticipateInterpolator](../android/view/animation/AnticipateInterpolator.md), [AnticipateOvershootInterpolator](../android/view/animation/AnticipateOvershootInterpolator.md), [BounceInterpolator](../android/view/animation/BounceInterpolator.md), [CycleInterpolator](../android/view/animation/CycleInterpolator.md), [DecelerateInterpolator](../android/view/animation/DecelerateInterpolator.md), [LinearInterpolator](../android/view/animation/LinearInterpolator.md), [OvershootInterpolator](../android/view/animation/OvershootInterpolator.md), [PathInterpolator](../android/view/animation/PathInterpolator.md) |--------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------| | [AccelerateDecelerateInterpolator](../android/view/animation/AccelerateDecelerateInterpolator.md) | An interpolator where the rate of change starts and ends slowly but accelerates through the middle. | | [AccelerateInterpolator](../android/view/animation/AccelerateInterpolator.md) | An interpolator where the rate of change starts out slowly and and then accelerates. | | [AnticipateInterpolator](../android/view/animation/AnticipateInterpolator.md) | An interpolator where the change starts backward then flings forward. | | [AnticipateOvershootInterpolator](../android/view/animation/AnticipateOvershootInterpolator.md) | An interpolator where the change starts backward then flings forward and overshoots the target value and finally goes back to the final value. | | [BounceInterpolator](../android/view/animation/BounceInterpolator.md) | An interpolator where the change bounces at the end. | | [CycleInterpolator](../android/view/animation/CycleInterpolator.md) | Repeats the animation for a specified number of cycles. | | [DecelerateInterpolator](../android/view/animation/DecelerateInterpolator.md) | An interpolator where the rate of change starts out quickly and and then decelerates. | | [LinearInterpolator](../android/view/animation/LinearInterpolator.md) | An interpolator where the rate of change is constant | | [OvershootInterpolator](../android/view/animation/OvershootInterpolator.md) | An interpolator where the change flings forward and overshoots the last value then comes back. | | [PathInterpolator](../android/view/animation/PathInterpolator.md) | An interpolator that can traverse a Path that extends from`Point``(0, 0)`to`(1, 1)`. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An interpolator defines the rate of change of an animation. This allows the basic animation effects (alpha, scale, translate, rotate) to be accelerated, decelerated, repeated, etc.

## Summary

| Inherited functions ||
|---|---|
| From class [TimeInterpolator](../android/animation/TimeInterpolator.md) |--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getInterpolation](../android/animation/TimeInterpolator.md))`(`input:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Maps a value representing the elapsed fraction of an animation to a value that represents the interpolated fraction. This interpolated value is then multiplied by the change in value of an animation to derive the animated value at the current elapsed animation time. <br /> | ||
