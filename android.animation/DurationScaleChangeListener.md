# ValueAnimator.DurationScaleChangeListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DurationScaleChangeListener

Kotlin| [Java](../android/animation/ValueAnimator.DurationScaleChangeListener.md) 
| --- | --- |

```
interface DurationScaleChangeListener
```

| [android.animation.ValueAnimator.DurationScaleChangeListener](../android/animation/ValueAnimator.DurationScaleChangeListener.md) |

Listener interface for the system-wide scaling factor for Animator-based animations.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onChanged](../android/animation/ValueAnimator.DurationScaleChangeListener.md))`(`scale:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Called when the duration scale changes. |

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
