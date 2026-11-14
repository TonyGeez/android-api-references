# ValueAnimator.DurationScaleChangeListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DurationScaleChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/animation/ValueAnimator.DurationScaleChangeListener "View this page in Java") 

```
interface DurationScaleChangeListener
```

| [android.animation.ValueAnimator.DurationScaleChangeListener](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator.DurationScaleChangeListener#) |

Listener interface for the system-wide scaling factor for Animator-based animations.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onChanged](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator.DurationScaleChangeListener#onChanged(kotlin.Float))`(`scale:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Called when the duration scale changes. |

## Public methods

### onChanged

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onChanged(scale: Float): Unit
```

Called when the duration scale changes.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------|
| `scale` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the duration scale Value is 0.0f or greater |
