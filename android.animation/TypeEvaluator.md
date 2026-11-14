# TypeEvaluator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TypeEvaluator

Kotlin| [Java](https://developer.android.com/reference/android/animation/TypeEvaluator "View this page in Java") 

```
interface TypeEvaluator<T : Any!>
```

| [android.animation.TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator#) |

| Known Direct Subclasses [ArgbEvaluator](https://developer.android.com/reference/kotlin/android/animation/ArgbEvaluator), [FloatArrayEvaluator](https://developer.android.com/reference/kotlin/android/animation/FloatArrayEvaluator), [FloatEvaluator](https://developer.android.com/reference/kotlin/android/animation/FloatEvaluator), [IntArrayEvaluator](https://developer.android.com/reference/kotlin/android/animation/IntArrayEvaluator), [IntEvaluator](https://developer.android.com/reference/kotlin/android/animation/IntEvaluator), [PointFEvaluator](https://developer.android.com/reference/kotlin/android/animation/PointFEvaluator), [RectEvaluator](https://developer.android.com/reference/kotlin/android/animation/RectEvaluator) |-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------| | [ArgbEvaluator](https://developer.android.com/reference/kotlin/android/animation/ArgbEvaluator) | This evaluator can be used to perform type interpolation between integer values that represent ARGB colors. | | [FloatArrayEvaluator](https://developer.android.com/reference/kotlin/android/animation/FloatArrayEvaluator) | This evaluator can be used to perform type interpolation between`float[]`values. | | [FloatEvaluator](https://developer.android.com/reference/kotlin/android/animation/FloatEvaluator) | This evaluator can be used to perform type interpolation between`float`values. | | [IntArrayEvaluator](https://developer.android.com/reference/kotlin/android/animation/IntArrayEvaluator) | This evaluator can be used to perform type interpolation between`int[]`values. | | [IntEvaluator](https://developer.android.com/reference/kotlin/android/animation/IntEvaluator) | This evaluator can be used to perform type interpolation between`int`values. | | [PointFEvaluator](https://developer.android.com/reference/kotlin/android/animation/PointFEvaluator) | This evaluator can be used to perform type interpolation between`PointF`values. | | [RectEvaluator](https://developer.android.com/reference/kotlin/android/animation/RectEvaluator) | This evaluator can be used to perform type interpolation between`Rect`values. | |

Interface for use with the [ValueAnimator.setEvaluator(TypeEvaluator)](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#setEvaluator(android.animation.TypeEvaluator))function. Evaluators allow developers to create animations on arbitrary property types, by allowing them to supply custom evaluators for types that are not automatically understood and used by the animation system.

## Summary

| Public methods ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractT | [evaluate](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator#evaluate(kotlin.Float,%20android.animation.TypeEvaluator.T,%20android.animation.TypeEvaluator.T))`(`fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `startValue:` `T`, `endValue:` `T`)` This function returns the result of linearly interpolating the start and end values, with`fraction`representing the proportion between the start and end values. |

## Public methods

### evaluate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun evaluate(
    fraction: Float, 
    startValue: T, 
    endValue: T
): T
```

This function returns the result of linearly interpolating the start and end values, with`fraction`representing the proportion between the start and end values. The calculation is a simple parametric calculation:`result = x0 + t * (x1 - x0)`, where`x0`is`startValue`,`x1`is`endValue`, and`t`is`fraction`.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------|
| `fraction` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The fraction from the starting to the ending values |
| `startValue` | T:The start value. |
| `endValue` | T:The end value. |

| Return ||
|---|----------------------------------------------------------------------------------------|
| T | A linear interpolation between the start and end values, given the`fraction`parameter. |
