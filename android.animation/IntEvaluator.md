# IntEvaluator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IntEvaluator

Kotlin| [Java](../android/animation/IntEvaluator.md) 
| --- | --- |

```
open class IntEvaluator : TypeEvaluator<Int!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.animation.IntEvaluator](../android/animation/IntEvaluator.md) |

This evaluator can be used to perform type interpolation between`int`values.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------|---|
| [IntEvaluator](../android/animation/IntEvaluator.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | [evaluate](../android/animation/IntEvaluator.md))`(`fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `startValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!`, `endValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!`)` This function returns the result of linearly interpolating the start and end values, with`fraction`representing the proportion between the start and end values. |

## Public constructors

### IntEvaluator

```
IntEvaluator()
```

## Public methods

### evaluate

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun evaluate(
    fraction: Float, 
    startValue: Int!, 
    endValue: Int!
): Int!
```

This function returns the result of linearly interpolating the start and end values, with`fraction`representing the proportion between the start and end values. The calculation is a simple parametric calculation:`result = x0 + t * (x1 - x0)`, where`x0`is`startValue`,`x1`is`endValue`, and`t`is`fraction`.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------|
| `fraction` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The fraction from the starting to the ending values |
| `startValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!:The start value; should be of type`int`or`Integer` |
| `endValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!:The end value; should be of type`int`or`Integer` |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | A linear interpolation between the start and end values, given the`fraction`parameter. |
