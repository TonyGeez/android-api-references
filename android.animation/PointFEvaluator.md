# PointFEvaluator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PointFEvaluator

Kotlin| [Java](https://developer.android.com/reference/android/animation/PointFEvaluator "View this page in Java") 

```
open class PointFEvaluator : TypeEvaluator<PointF!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.animation.PointFEvaluator](https://developer.android.com/reference/kotlin/android/animation/PointFEvaluator#) |

This evaluator can be used to perform type interpolation between`PointF`values.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PointFEvaluator](https://developer.android.com/reference/kotlin/android/animation/PointFEvaluator#PointFEvaluator())`()` Construct a PointFEvaluator that returns a new PointF on every evaluate call. |
| [PointFEvaluator](https://developer.android.com/reference/kotlin/android/animation/PointFEvaluator#PointFEvaluator(android.graphics.PointF))`(`reuse:` ` [PointF](https://developer.android.com/reference/kotlin/android/graphics/PointF.html#)!`)` Constructs a PointFEvaluator that modifies and returns`reuse`in [evaluate(float,android.graphics.PointF,android.graphics.PointF)](https://developer.android.com/reference/kotlin/android/animation/PointFEvaluator#evaluate(kotlin.Float,%20android.graphics.PointF,%20android.graphics.PointF))calls. |

| Public methods ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [PointF](https://developer.android.com/reference/kotlin/android/graphics/PointF.html#)! | [evaluate](https://developer.android.com/reference/kotlin/android/animation/PointFEvaluator#evaluate(kotlin.Float,%20android.graphics.PointF,%20android.graphics.PointF))`(`fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `startValue:` ` [PointF](https://developer.android.com/reference/kotlin/android/graphics/PointF.html#)!`, `endValue:` ` [PointF](https://developer.android.com/reference/kotlin/android/graphics/PointF.html#)!`)` This function returns the result of linearly interpolating the start and end PointF values, with`fraction`representing the proportion between the start and end values. |

## Public constructors

### PointFEvaluator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PointFEvaluator()
```

Construct a PointFEvaluator that returns a new PointF on every evaluate call. To avoid creating an object for each evaluate call, [PointFEvaluator.PointFEvaluator(android.graphics.PointF)](https://developer.android.com/reference/kotlin/android/animation/PointFEvaluator#PointFEvaluator(android.graphics.PointF))should be used whenever possible. 

### PointFEvaluator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PointFEvaluator(reuse: PointF!)
```

Constructs a PointFEvaluator that modifies and returns`reuse`in [evaluate(float,android.graphics.PointF,android.graphics.PointF)](https://developer.android.com/reference/kotlin/android/animation/PointFEvaluator#evaluate(kotlin.Float,%20android.graphics.PointF,%20android.graphics.PointF))calls. The value returned from [evaluate(float,android.graphics.PointF,android.graphics.PointF)](https://developer.android.com/reference/kotlin/android/animation/PointFEvaluator#evaluate(kotlin.Float,%20android.graphics.PointF,%20android.graphics.PointF))should not be cached because it will change over time as the object is reused on each call.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `reuse` | [PointF](https://developer.android.com/reference/kotlin/android/graphics/PointF.html#)!:A PointF to be modified and returned by evaluate. |

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

If [PointFEvaluator(android.graphics.PointF)](https://developer.android.com/reference/kotlin/android/animation/PointFEvaluator#PointFEvaluator(android.graphics.PointF))was used to construct this PointFEvaluator, the object returned will be the`reuse`passed into the constructor.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------|
| `fraction` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The fraction from the starting to the ending values |
| `startValue` | [PointF](https://developer.android.com/reference/kotlin/android/graphics/PointF.html#)!:The start PointF |
| `endValue` | [PointF](https://developer.android.com/reference/kotlin/android/graphics/PointF.html#)!:The end PointF |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [PointF](https://developer.android.com/reference/kotlin/android/graphics/PointF.html#)! | A linear interpolation between the start and end values, given the`fraction`parameter. |
