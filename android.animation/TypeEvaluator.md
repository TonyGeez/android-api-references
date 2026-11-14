# TypeEvaluator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TypeEvaluator

Kotlin| [Java](../android/animation/TypeEvaluator.md) 
| --- | --- |

```
interface TypeEvaluator<T : Any!>
```

| [android.animation.TypeEvaluator](../android/animation/TypeEvaluator.md) |

| Known Direct Subclasses [ArgbEvaluator](../android/animation/ArgbEvaluator.md), [FloatArrayEvaluator](../android/animation/FloatArrayEvaluator.md), [FloatEvaluator](../android/animation/FloatEvaluator.md), [IntArrayEvaluator](../android/animation/IntArrayEvaluator.md), [IntEvaluator](../android/animation/IntEvaluator.md), [PointFEvaluator](../android/animation/PointFEvaluator.md), [RectEvaluator](../android/animation/RectEvaluator.md) |-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------| | [ArgbEvaluator](../android/animation/ArgbEvaluator.md) | This evaluator can be used to perform type interpolation between integer values that represent ARGB colors. | | [FloatArrayEvaluator](../android/animation/FloatArrayEvaluator.md) | This evaluator can be used to perform type interpolation between`float[]`values. | | [FloatEvaluator](../android/animation/FloatEvaluator.md) | This evaluator can be used to perform type interpolation between`float`values. | | [IntArrayEvaluator](../android/animation/IntArrayEvaluator.md) | This evaluator can be used to perform type interpolation between`int[]`values. | | [IntEvaluator](../android/animation/IntEvaluator.md) | This evaluator can be used to perform type interpolation between`int`values. | | [PointFEvaluator](../android/animation/PointFEvaluator.md) | This evaluator can be used to perform type interpolation between`PointF`values. | | [RectEvaluator](../android/animation/RectEvaluator.md) | This evaluator can be used to perform type interpolation between`Rect`values. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface for use with the [ValueAnimator.setEvaluator(TypeEvaluator)](../android/animation/ValueAnimator.md))function. Evaluators allow developers to create animations on arbitrary property types, by allowing them to supply custom evaluators for types that are not automatically understood and used by the animation system.

## Summary

| Public methods ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractT | [evaluate](../android/animation/TypeEvaluator.md))`(`fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `startValue:` `T`, `endValue:` `T`)` This function returns the result of linearly interpolating the start and end values, with`fraction`representing the proportion between the start and end values. |

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
| --- | --- |

| Return ||
|---|----------------------------------------------------------------------------------------|
| T | A linear interpolation between the start and end values, given the`fraction`parameter. |
