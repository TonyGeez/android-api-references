# BaseInterpolator

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BaseInterpolator

Kotlin| [Java](BaseInterpolator.md) 
| --- | --- |

```
abstract class BaseInterpolator : Interpolator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.animation.BaseInterpolator](BaseInterpolator.md) |

| Known Direct Subclasses [AccelerateDecelerateInterpolator](AccelerateDecelerateInterpolator.md), [AccelerateInterpolator](AccelerateInterpolator.md), [AnticipateInterpolator](AnticipateInterpolator.md), [AnticipateOvershootInterpolator](AnticipateOvershootInterpolator.md), [BounceInterpolator](BounceInterpolator.md), [CycleInterpolator](CycleInterpolator.md), [DecelerateInterpolator](DecelerateInterpolator.md), [LinearInterpolator](LinearInterpolator.md), [OvershootInterpolator](OvershootInterpolator.md), [PathInterpolator](PathInterpolator.md) |--------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------| | [AccelerateDecelerateInterpolator](AccelerateDecelerateInterpolator.md) | An interpolator where the rate of change starts and ends slowly but accelerates through the middle. | | [AccelerateInterpolator](AccelerateInterpolator.md) | An interpolator where the rate of change starts out slowly and and then accelerates. | | [AnticipateInterpolator](AnticipateInterpolator.md) | An interpolator where the change starts backward then flings forward. | | [AnticipateOvershootInterpolator](AnticipateOvershootInterpolator.md) | An interpolator where the change starts backward then flings forward and overshoots the target value and finally goes back to the final value. | | [BounceInterpolator](BounceInterpolator.md) | An interpolator where the change bounces at the end. | | [CycleInterpolator](CycleInterpolator.md) | Repeats the animation for a specified number of cycles. | | [DecelerateInterpolator](DecelerateInterpolator.md) | An interpolator where the rate of change starts out quickly and and then decelerates. | | [LinearInterpolator](LinearInterpolator.md) | An interpolator where the rate of change is constant | | [OvershootInterpolator](OvershootInterpolator.md) | An interpolator where the change flings forward and overshoots the last value then comes back. | | [PathInterpolator](PathInterpolator.md) | An interpolator that can traverse a Path that extends from`Point``(0, 0)`to`(1, 1)`. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An abstract class which is extended by default interpolators.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BaseInterpolator](BaseInterpolator.md))`()` <br /> |

## Public constructors

### BaseInterpolator

```
BaseInterpolator()
```
