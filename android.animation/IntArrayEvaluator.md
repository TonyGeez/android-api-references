# IntArrayEvaluator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IntArrayEvaluator

Kotlin| [Java](../android/animation/IntArrayEvaluator.md) 
| --- | --- |

```
open class IntArrayEvaluator : TypeEvaluator<IntArray!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.animation.IntArrayEvaluator](../android/animation/IntArrayEvaluator.md) |

This evaluator can be used to perform type interpolation between`int[]`values. Each index into the array is treated as a separate value to interpolate. For example, evaluating`{100, 200}`and`{300, 400}`will interpolate the value at the first index between 100 and 300 and the value at the second index value between 200 and 400.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IntArrayEvaluator](../android/animation/IntArrayEvaluator.md))`()` Create an IntArrayEvaluator that does not reuse the animated value. |
| [IntArrayEvaluator](../android/animation/IntArrayEvaluator.md))`(`reuseArray:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Create an IntArrayEvaluator that reuses`reuseArray`for every evaluate() call. |

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [evaluate](../android/animation/IntArrayEvaluator.md))`(`fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `startValue:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `endValue:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Interpolates the value at each index by the fraction. |

## Public constructors

### IntArrayEvaluator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IntArrayEvaluator()
```

Create an IntArrayEvaluator that does not reuse the animated value. Care must be taken when using this option because on every evaluation a new`int[]`will be allocated. 
**See Also**

- [#IntArrayEvaluator(int[])](https://developer.android.com/reference/kotlin/android/animation/IntArrayEvaluator#IntArrayEvaluator(kotlin.IntArray)) 

### IntArrayEvaluator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IntArrayEvaluator(reuseArray: IntArray!)
```

Create an IntArrayEvaluator that reuses`reuseArray`for every evaluate() call. Caution must be taken to ensure that the value returned from [android.animation.ValueAnimator#getAnimatedValue()](../android/animation/ValueAnimator.md))is not cached, modified, or used across threads. The value will be modified on each`evaluate()`call.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `reuseArray` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The array to modify and return from`evaluate`. |

## Public methods

### evaluate

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun evaluate(
    fraction: Float, 
    startValue: IntArray!, 
    endValue: IntArray!
): IntArray!
```

Interpolates the value at each index by the fraction. If[IntArrayEvaluator(int[])](https://developer.android.com/reference/kotlin/android/animation/IntArrayEvaluator#IntArrayEvaluator(kotlin.IntArray))was used to construct this object,`reuseArray`will be returned, otherwise a new`int[]`will be returned.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------|
| `fraction` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The fraction from the starting to the ending values |
| `startValue` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The start value. |
| `endValue` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The end value. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | An`int[]`where each element is an interpolation between the same index in startValue and endValue. |
