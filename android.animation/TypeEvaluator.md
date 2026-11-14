# TypeEvaluator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TypeEvaluator

Kotlin| [Java](TypeEvaluator.md) 
| --- | --- |

```
interface TypeEvaluator<T : Any!>
```

| [android.animation.TypeEvaluator](TypeEvaluator.md) |

| Known Direct Subclasses [ArgbEvaluator](ArgbEvaluator.md), [FloatArrayEvaluator](FloatArrayEvaluator.md), [FloatEvaluator](FloatEvaluator.md), [IntArrayEvaluator](IntArrayEvaluator.md), [IntEvaluator](IntEvaluator.md), [PointFEvaluator](PointFEvaluator.md), [RectEvaluator](RectEvaluator.md) |-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------| | [ArgbEvaluator](ArgbEvaluator.md) | This evaluator can be used to perform type interpolation between integer values that represent ARGB colors. | | [FloatArrayEvaluator](FloatArrayEvaluator.md) | This evaluator can be used to perform type interpolation between`float[]`values. | | [FloatEvaluator](FloatEvaluator.md) | This evaluator can be used to perform type interpolation between`float`values. | | [IntArrayEvaluator](IntArrayEvaluator.md) | This evaluator can be used to perform type interpolation between`int[]`values. | | [IntEvaluator](IntEvaluator.md) | This evaluator can be used to perform type interpolation between`int`values. | | [PointFEvaluator](PointFEvaluator.md) | This evaluator can be used to perform type interpolation between`PointF`values. | | [RectEvaluator](RectEvaluator.md) | This evaluator can be used to perform type interpolation between`Rect`values. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface for use with the [ValueAnimator.setEvaluator(TypeEvaluator)](ValueAnimator.md))function. Evaluators allow developers to create animations on arbitrary property types, by allowing them to supply custom evaluators for types that are not automatically understood and used by the animation system.

## Summary

| Public methods ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractT | [evaluate](TypeEvaluator.md))`(`fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `startValue:` `T`, `endValue:` `T`)` This function returns the result of linearly interpolating the start and end values, with`fraction`representing the proportion between the start and end values. |

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
