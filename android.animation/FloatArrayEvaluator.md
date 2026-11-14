# FloatArrayEvaluator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FloatArrayEvaluator

Kotlin| [Java](https://developer.android.com/reference/android/animation/FloatArrayEvaluator "View this page in Java") 

```
open class FloatArrayEvaluator : TypeEvaluator<FloatArray!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.animation.FloatArrayEvaluator](https://developer.android.com/reference/kotlin/android/animation/FloatArrayEvaluator#) |

This evaluator can be used to perform type interpolation between`float[]`values. Each index into the array is treated as a separate value to interpolate. For example, evaluating`{100, 200}`and`{300, 400}`will interpolate the value at the first index between 100 and 300 and the value at the second index value between 200 and 400.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FloatArrayEvaluator](https://developer.android.com/reference/kotlin/android/animation/FloatArrayEvaluator#FloatArrayEvaluator())`()` Create a FloatArrayEvaluator that does not reuse the animated value. |
| [FloatArrayEvaluator](https://developer.android.com/reference/kotlin/android/animation/FloatArrayEvaluator#FloatArrayEvaluator(kotlin.FloatArray))`(`reuseArray:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Create a FloatArrayEvaluator that reuses`reuseArray`for every evaluate() call. |

| Public methods ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | [evaluate](https://developer.android.com/reference/kotlin/android/animation/FloatArrayEvaluator#evaluate(kotlin.Float,%20kotlin.FloatArray,%20kotlin.FloatArray))`(`fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `startValue:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `endValue:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Interpolates the value at each index by the fraction. |

## Public constructors

### FloatArrayEvaluator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FloatArrayEvaluator()
```

Create a FloatArrayEvaluator that does not reuse the animated value. Care must be taken when using this option because on every evaluation a new`float[]`will be allocated. 
**See Also**

- [#FloatArrayEvaluator(float[])](https://developer.android.com/reference/kotlin/android/animation/FloatArrayEvaluator#FloatArrayEvaluator(kotlin.FloatArray)) 

### FloatArrayEvaluator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FloatArrayEvaluator(reuseArray: FloatArray!)
```

Create a FloatArrayEvaluator that reuses`reuseArray`for every evaluate() call. Caution must be taken to ensure that the value returned from [android.animation.ValueAnimator#getAnimatedValue()](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#getAnimatedValue())is not cached, modified, or used across threads. The value will be modified on each`evaluate()`call.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `reuseArray` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The array to modify and return from`evaluate`. |

## Public methods

### evaluate

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun evaluate(
    fraction: Float, 
    startValue: FloatArray!, 
    endValue: FloatArray!
): FloatArray!
```

Interpolates the value at each index by the fraction. If[FloatArrayEvaluator(float[])](https://developer.android.com/reference/kotlin/android/animation/FloatArrayEvaluator#FloatArrayEvaluator(kotlin.FloatArray))was used to construct this object,`reuseArray`will be returned, otherwise a new`float[]`will be returned.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------|
| `fraction` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The fraction from the starting to the ending values |
| `startValue` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The start value. |
| `endValue` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The end value. |

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | A`float[]`where each element is an interpolation between the same index in startValue and endValue. |
