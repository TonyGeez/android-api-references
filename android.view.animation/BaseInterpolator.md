# BaseInterpolator

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BaseInterpolator

Kotlin| [Java](../android/view/animation/BaseInterpolator.md) 
| --- | --- |

```
abstract class BaseInterpolator : Interpolator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.animation.BaseInterpolator](../android/view/animation/BaseInterpolator.md) |

| Known Direct Subclasses [AccelerateDecelerateInterpolator](../android/view/animation/AccelerateDecelerateInterpolator.md), [AccelerateInterpolator](../android/view/animation/AccelerateInterpolator.md), [AnticipateInterpolator](../android/view/animation/AnticipateInterpolator.md), [AnticipateOvershootInterpolator](../android/view/animation/AnticipateOvershootInterpolator.md), [BounceInterpolator](../android/view/animation/BounceInterpolator.md), [CycleInterpolator](../android/view/animation/CycleInterpolator.md), [DecelerateInterpolator](../android/view/animation/DecelerateInterpolator.md), [LinearInterpolator](../android/view/animation/LinearInterpolator.md), [OvershootInterpolator](../android/view/animation/OvershootInterpolator.md), [PathInterpolator](../android/view/animation/PathInterpolator.md) |--------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------| | [AccelerateDecelerateInterpolator](../android/view/animation/AccelerateDecelerateInterpolator.md) | An interpolator where the rate of change starts and ends slowly but accelerates through the middle. | | [AccelerateInterpolator](../android/view/animation/AccelerateInterpolator.md) | An interpolator where the rate of change starts out slowly and and then accelerates. | | [AnticipateInterpolator](../android/view/animation/AnticipateInterpolator.md) | An interpolator where the change starts backward then flings forward. | | [AnticipateOvershootInterpolator](../android/view/animation/AnticipateOvershootInterpolator.md) | An interpolator where the change starts backward then flings forward and overshoots the target value and finally goes back to the final value. | | [BounceInterpolator](../android/view/animation/BounceInterpolator.md) | An interpolator where the change bounces at the end. | | [CycleInterpolator](../android/view/animation/CycleInterpolator.md) | Repeats the animation for a specified number of cycles. | | [DecelerateInterpolator](../android/view/animation/DecelerateInterpolator.md) | An interpolator where the rate of change starts out quickly and and then decelerates. | | [LinearInterpolator](../android/view/animation/LinearInterpolator.md) | An interpolator where the rate of change is constant | | [OvershootInterpolator](../android/view/animation/OvershootInterpolator.md) | An interpolator where the change flings forward and overshoots the last value then comes back. | | [PathInterpolator](../android/view/animation/PathInterpolator.md) | An interpolator that can traverse a Path that extends from`Point``(0, 0)`to`(1, 1)`. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An abstract class which is extended by default interpolators.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BaseInterpolator](../android/view/animation/BaseInterpolator.md))`()` <br /> |

## Public constructors

### BaseInterpolator

```
BaseInterpolator()
```
