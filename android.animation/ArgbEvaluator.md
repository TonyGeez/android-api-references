# ArgbEvaluator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ArgbEvaluator

Kotlin| [Java](../android/animation/ArgbEvaluator.md) 
| --- | --- |

```
open class ArgbEvaluator : TypeEvaluator<Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.animation.ArgbEvaluator](../android/animation/ArgbEvaluator.md) |

This evaluator can be used to perform type interpolation between integer values that represent ARGB colors.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------|---|
| [ArgbEvaluator](../android/animation/ArgbEvaluator.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [evaluate](../android/animation/ArgbEvaluator.md))`(`fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `startValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `endValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` This function returns the calculated in-between value for a color given integers that represent the start and end values in the four bytes of the 32-bit int. |

## Public constructors

### ArgbEvaluator

```
ArgbEvaluator()
```

## Public methods

### evaluate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun evaluate(
    fraction: Float, 
    startValue: Any!, 
    endValue: Any!
): Any!
```

This function returns the calculated in-between value for a color given integers that represent the start and end values in the four bytes of the 32-bit int. Each channel is separately linearly interpolated and the resulting calculated values are recombined into the return value.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fraction` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The fraction from the starting to the ending values |
| `startValue` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:A 32-bit int value representing colors in the separate bytes of the parameter |
| `endValue` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:A 32-bit int value representing colors in the separate bytes of the parameter |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | A value that is calculated to be the linearly interpolated result, derived by separating the start and end values into separate color channels and interpolating each one separately, recombining the resulting values in the same way. |
