Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnticipateOvershootInterpolator

Kotlin | [Java](AnticipateOvershootInterpolator.md)
| --- | --- |

```
open class AnticipateOvershootInterpolator : BaseInterpolator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.view.animation.BaseInterpolator](BaseInterpolator.md) ||
| | ↳ | [android.view.animation.AnticipateOvershootInterpolator](AnticipateOvershootInterpolator.md) |

An interpolator where the change starts backward then flings forward and overshoots the target value and finally goes back to the final value.

## Summary

| Public constructors ||
|---|---|
| AnticipateOvershootInterpolator <br /> |
| AnticipateOvershootInterpolator <br /> |
| AnticipateOvershootInterpolator <br /> |
| AnticipateOvershootInterpolator <br /> |

| Public methods ||
|---|---|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getInterpolation Maps a value representing the elapsed fraction of an animation to a value that represents the interpolated fraction. |

## Public constructors

### AnticipateOvershootInterpolator

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AnticipateOvershootInterpolator()
```

### AnticipateOvershootInterpolator

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AnticipateOvershootInterpolator(
    context: Context!, 
    attrs: AttributeSet!)
```

### AnticipateOvershootInterpolator

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AnticipateOvershootInterpolator(tension: Float)
```

| Parameters ||
|---|---|
| `tension` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Amount of anticipation/overshoot. When tension equals 0.0f, there is no anticipation/overshoot and the interpolator becomes a simple acceleration/deceleration interpolator. |

### AnticipateOvershootInterpolator

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AnticipateOvershootInterpolator(
    tension: Float, 
    extraTension: Float)
```

| Parameters ||
|---|---|
| `tension` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Amount of anticipation/overshoot. When tension equals 0.0f, there is no anticipation/overshoot and the interpolator becomes a simple acceleration/deceleration interpolator. |
| `extraTension` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Amount by which to multiply the tension. For instance, to get the same overshoot as an OvershootInterpolator with a tension of 2.0f, you would use an extraTension of 1.5f. |

## Public methods

### getInterpolation

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInterpolation(t: Float): Float
```

Maps a value representing the elapsed fraction of an animation to a value that represents the interpolated fraction. This interpolated value is then multiplied by the change in value of an animation to derive the animated value at the current elapsed animation time.

| Parameters ||
|---|---|
| `input` | A value between 0 and 1.0 indicating our current point in the animation where 0 represents the start and 1.0 represents the end |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | The interpolation value. This value can be more than 1.0 for interpolators which overshoot their targets, or less than 0 for interpolators that undershoot their targets. |
