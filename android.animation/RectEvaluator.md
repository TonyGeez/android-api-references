# RectEvaluator

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RectEvaluator

Kotlin| [Java](https://developer.android.com/reference/android/animation/RectEvaluator "View this page in Java") 
| --- | --- |

```
open class RectEvaluator : TypeEvaluator<Rect!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.animation.RectEvaluator](https://developer.android.com/reference/kotlin/android/animation/RectEvaluator#) |

This evaluator can be used to perform type interpolation between`Rect`values.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RectEvaluator](https://developer.android.com/reference/kotlin/android/animation/RectEvaluator#RectEvaluator())`()` Construct a RectEvaluator that returns a new Rect on every evaluate call. |
| [RectEvaluator](https://developer.android.com/reference/kotlin/android/animation/RectEvaluator#RectEvaluator(android.graphics.Rect))`(`reuseRect:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!`)` Constructs a RectEvaluator that modifies and returns`reuseRect`in [evaluate(float,android.graphics.Rect,android.graphics.Rect)](https://developer.android.com/reference/kotlin/android/animation/RectEvaluator#evaluate(kotlin.Float,%20android.graphics.Rect,%20android.graphics.Rect))calls. |

| Public methods ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)! | [evaluate](https://developer.android.com/reference/kotlin/android/animation/RectEvaluator#evaluate(kotlin.Float,%20android.graphics.Rect,%20android.graphics.Rect))`(`fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `startValue:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!`, `endValue:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!`)` This function returns the result of linearly interpolating the start and end Rect values, with`fraction`representing the proportion between the start and end values. |

## Public constructors

### RectEvaluator

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RectEvaluator()
```

Construct a RectEvaluator that returns a new Rect on every evaluate call. To avoid creating an object for each evaluate call, [RectEvaluator.RectEvaluator(android.graphics.Rect)](https://developer.android.com/reference/kotlin/android/animation/RectEvaluator#RectEvaluator(android.graphics.Rect))should be used whenever possible. 

### RectEvaluator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RectEvaluator(reuseRect: Rect!)
```

Constructs a RectEvaluator that modifies and returns`reuseRect`in [evaluate(float,android.graphics.Rect,android.graphics.Rect)](https://developer.android.com/reference/kotlin/android/animation/RectEvaluator#evaluate(kotlin.Float,%20android.graphics.Rect,%20android.graphics.Rect))calls. The value returned from [evaluate(float,android.graphics.Rect,android.graphics.Rect)](https://developer.android.com/reference/kotlin/android/animation/RectEvaluator#evaluate(kotlin.Float,%20android.graphics.Rect,%20android.graphics.Rect))should not be cached because it will change over time as the object is reused on each call.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `reuseRect` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!:A Rect to be modified and returned by evaluate. |

## Public methods

### evaluate

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun evaluate(
    fraction: Float, 
    startValue: Rect!, 
    endValue: Rect!
): Rect!
```

This function returns the result of linearly interpolating the start and end Rect values, with`fraction`representing the proportion between the start and end values. The calculation is a simple parametric calculation on each of the separate components in the Rect objects (left, top, right, and bottom).

If [RectEvaluator(android.graphics.Rect)](https://developer.android.com/reference/kotlin/android/animation/RectEvaluator#RectEvaluator(android.graphics.Rect))was used to construct this RectEvaluator, the object returned will be the`reuseRect`passed into the constructor.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------|
| `fraction` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The fraction from the starting to the ending values |
| `startValue` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!:The start Rect |
| `endValue` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!:The end Rect |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)! | A linear interpolation between the start and end values, given the`fraction`parameter. |
