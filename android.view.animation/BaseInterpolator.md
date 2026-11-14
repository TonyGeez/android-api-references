# BaseInterpolator

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BaseInterpolator

Kotlin| [Java](https://developer.android.com/reference/android/view/animation/BaseInterpolator "View this page in Java") 

```
abstract class BaseInterpolator : Interpolator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.animation.BaseInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/BaseInterpolator#) |

| Known Direct Subclasses [AccelerateDecelerateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AccelerateDecelerateInterpolator), [AccelerateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AccelerateInterpolator), [AnticipateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AnticipateInterpolator), [AnticipateOvershootInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AnticipateOvershootInterpolator), [BounceInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/BounceInterpolator), [CycleInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/CycleInterpolator), [DecelerateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/DecelerateInterpolator), [LinearInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/LinearInterpolator), [OvershootInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/OvershootInterpolator), [PathInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/PathInterpolator) |--------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------| | [AccelerateDecelerateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AccelerateDecelerateInterpolator) | An interpolator where the rate of change starts and ends slowly but accelerates through the middle. | | [AccelerateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AccelerateInterpolator) | An interpolator where the rate of change starts out slowly and and then accelerates. | | [AnticipateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AnticipateInterpolator) | An interpolator where the change starts backward then flings forward. | | [AnticipateOvershootInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AnticipateOvershootInterpolator) | An interpolator where the change starts backward then flings forward and overshoots the target value and finally goes back to the final value. | | [BounceInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/BounceInterpolator) | An interpolator where the change bounces at the end. | | [CycleInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/CycleInterpolator) | Repeats the animation for a specified number of cycles. | | [DecelerateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/DecelerateInterpolator) | An interpolator where the rate of change starts out quickly and and then decelerates. | | [LinearInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/LinearInterpolator) | An interpolator where the rate of change is constant | | [OvershootInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/OvershootInterpolator) | An interpolator where the change flings forward and overshoots the last value then comes back. | | [PathInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/PathInterpolator) | An interpolator that can traverse a Path that extends from`Point``(0, 0)`to`(1, 1)`. | |

An abstract class which is extended by default interpolators.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BaseInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/BaseInterpolator#BaseInterpolator())`()` <br /> |

## Public constructors

### BaseInterpolator

```
BaseInterpolator()
```
