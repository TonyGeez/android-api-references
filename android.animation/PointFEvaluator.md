# PointFEvaluator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PointFEvaluator

Kotlin| [Java](PointFEvaluator.md) 
| --- | --- |

```
open class PointFEvaluator : TypeEvaluator<PointF!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.animation.PointFEvaluator](PointFEvaluator.md) |

This evaluator can be used to perform type interpolation between`PointF`values.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PointFEvaluator](PointFEvaluator.md))`()` Construct a PointFEvaluator that returns a new PointF on every evaluate call. |
| [PointFEvaluator](PointFEvaluator.md))`(`reuse:` ` [PointF](../android.graphics/PointF.md)!`)` Constructs a PointFEvaluator that modifies and returns`reuse`in [evaluate(float,android.graphics.PointF,android.graphics.PointF)](PointFEvaluator.md))calls. |

| Public methods ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [PointF](../android.graphics/PointF.md)! | [evaluate](PointFEvaluator.md))`(`fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `startValue:` ` [PointF](../android.graphics/PointF.md)!`, `endValue:` ` [PointF](../android.graphics/PointF.md)!`)` This function returns the result of linearly interpolating the start and end PointF values, with`fraction`representing the proportion between the start and end values. |

## Public constructors

### PointFEvaluator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PointFEvaluator()
```

Construct a PointFEvaluator that returns a new PointF on every evaluate call. To avoid creating an object for each evaluate call, [PointFEvaluator.PointFEvaluator(android.graphics.PointF)](PointFEvaluator.md))should be used whenever possible. 

### PointFEvaluator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PointFEvaluator(reuse: PointF!)
```

Constructs a PointFEvaluator that modifies and returns`reuse`in [evaluate(float,android.graphics.PointF,android.graphics.PointF)](PointFEvaluator.md))calls. The value returned from [evaluate(float,android.graphics.PointF,android.graphics.PointF)](PointFEvaluator.md))should not be cached because it will change over time as the object is reused on each call.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `reuse` | [PointF](../android.graphics/PointF.md)!:A PointF to be modified and returned by evaluate. |

## Public methods

### evaluate

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun evaluate(
    fraction: Float, 
    startValue: PointF!, 
    endValue: PointF!
): PointF!
```

This function returns the result of linearly interpolating the start and end PointF values, with`fraction`representing the proportion between the start and end values. The calculation is a simple parametric calculation on each of the separate components in the PointF objects (x, y).

If [PointFEvaluator(android.graphics.PointF)](PointFEvaluator.md))was used to construct this PointFEvaluator, the object returned will be the`reuse`passed into the constructor.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------|
| `fraction` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The fraction from the starting to the ending values |
| `startValue` | [PointF](../android.graphics/PointF.md)!:The start PointF |
| `endValue` | [PointF](../android.graphics/PointF.md)!:The end PointF |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [PointF](../android.graphics/PointF.md)! | A linear interpolation between the start and end values, given the`fraction`parameter. |
