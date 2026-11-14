# FloatEvaluator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FloatEvaluator

Kotlin| [Java](FloatEvaluator.md) 
| --- | --- |

```
open class FloatEvaluator : TypeEvaluator<Number!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.animation.FloatEvaluator](FloatEvaluator.md) |

This evaluator can be used to perform type interpolation between`float`values.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------|---|
| [FloatEvaluator](FloatEvaluator.md))`()` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [evaluate](FloatEvaluator.md))`(`fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `startValue:` ` [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)!`, `endValue:` ` [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)!`)` This function returns the result of linearly interpolating the start and end values, with`fraction`representing the proportion between the start and end values. |

## Public constructors

### FloatEvaluator

```
FloatEvaluator()
```

## Public methods

### evaluate

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun evaluate(
    fraction: Float, 
    startValue: Number!, 
    endValue: Number!
): Float!
```

This function returns the result of linearly interpolating the start and end values, with`fraction`representing the proportion between the start and end values. The calculation is a simple parametric calculation:`result = x0 + t * (x1 - x0)`, where`x0`is`startValue`,`x1`is`endValue`, and`t`is`fraction`.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `fraction` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The fraction from the starting to the ending values |
| `startValue` | [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)!:The start value; should be of type`float`or`Float` |
| `endValue` | [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)!:The end value; should be of type`float`or`Float` |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | A linear interpolation between the start and end values, given the`fraction`parameter. |
