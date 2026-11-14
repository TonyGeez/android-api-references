# RectEvaluator

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RectEvaluator

Kotlin| [Java](../android/animation/RectEvaluator.md) 
| --- | --- |

```
open class RectEvaluator : TypeEvaluator<Rect!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.animation.RectEvaluator](../android/animation/RectEvaluator.md) |

This evaluator can be used to perform type interpolation between`Rect`values.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RectEvaluator](../android/animation/RectEvaluator.md))`()` Construct a RectEvaluator that returns a new Rect on every evaluate call. |
| [RectEvaluator](../android/animation/RectEvaluator.md))`(`reuseRect:` ` [Rect](../android/graphics/Rect.md)!`)` Constructs a RectEvaluator that modifies and returns`reuseRect`in [evaluate(float,android.graphics.Rect,android.graphics.Rect)](../android/animation/RectEvaluator.md))calls. |

| Public methods ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Rect](../android/graphics/Rect.md)! | [evaluate](../android/animation/RectEvaluator.md))`(`fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `startValue:` ` [Rect](../android/graphics/Rect.md)!`, `endValue:` ` [Rect](../android/graphics/Rect.md)!`)` This function returns the result of linearly interpolating the start and end Rect values, with`fraction`representing the proportion between the start and end values. |

## Public constructors

### RectEvaluator

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RectEvaluator()
```

Construct a RectEvaluator that returns a new Rect on every evaluate call. To avoid creating an object for each evaluate call, [RectEvaluator.RectEvaluator(android.graphics.Rect)](../android/animation/RectEvaluator.md))should be used whenever possible. 

### RectEvaluator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RectEvaluator(reuseRect: Rect!)
```

Constructs a RectEvaluator that modifies and returns`reuseRect`in [evaluate(float,android.graphics.Rect,android.graphics.Rect)](../android/animation/RectEvaluator.md))calls. The value returned from [evaluate(float,android.graphics.Rect,android.graphics.Rect)](../android/animation/RectEvaluator.md))should not be cached because it will change over time as the object is reused on each call.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `reuseRect` | [Rect](../android/graphics/Rect.md)!:A Rect to be modified and returned by evaluate. |

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

If [RectEvaluator(android.graphics.Rect)](../android/animation/RectEvaluator.md))was used to construct this RectEvaluator, the object returned will be the`reuseRect`passed into the constructor.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------|
| `fraction` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The fraction from the starting to the ending values |
| `startValue` | [Rect](../android/graphics/Rect.md)!:The start Rect |
| `endValue` | [Rect](../android/graphics/Rect.md)!:The end Rect |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Rect](../android/graphics/Rect.md)! | A linear interpolation between the start and end values, given the`fraction`parameter. |
