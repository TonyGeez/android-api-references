# PathDashPathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PathDashPathEffect

Kotlin | [Java](https://developer.android.com/reference/android/graphics/PathDashPathEffect "View this page in Java") 
| --- | --- |

```
open class PathDashPathEffect : PathEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.PathEffect](https://developer.android.com/reference/kotlin/android/graphics/PathEffect) ||
| | ↳ | [android.graphics.PathDashPathEffect](https://developer.android.com/reference/kotlin/android/graphics/PathDashPathEffect#) |

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------|
| | [Style](https://developer.android.com/reference/kotlin/android/graphics/PathDashPathEffect.Style) <br /> |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PathDashPathEffect](https://developer.android.com/reference/kotlin/android/graphics/PathDashPathEffect#PathDashPathEffect(android.graphics.Path,%20kotlin.Float,%20kotlin.Float,%20android.graphics.PathDashPathEffect.Style))`(`shape:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path)!`, `advance:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `phase:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `style:` ` [PathDashPathEffect.Style](https://developer.android.com/reference/kotlin/android/graphics/PathDashPathEffect.Style)!`)` Dash the drawn path by stamping it with the specified shape. |

| Inherited functions ||
|---|---|
| From class [PathEffect](https://developer.android.com/reference/kotlin/android/graphics/PathEffect) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/graphics/PathEffect#finalize())`()` <br /> | ||

## Public constructors

### PathDashPathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PathDashPathEffect(
    shape: Path!, 
    advance: Float, 
    phase: Float, 
    style: PathDashPathEffect.Style!)
```

Dash the drawn path by stamping it with the specified shape. This only applies to drawings when the paint's style is STROKE or STROKE_AND_FILL. If the paint's style is FILL, then this effect is ignored. The paint's strokeWidth does not affect the results.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `shape` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path)!: The path to stamp along |
| `advance` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): spacing between each stamp of shape |
| `phase` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): amount to offset before the first shape is stamped |
| --- | --- |
| `style` | [PathDashPathEffect.Style](https://developer.android.com/reference/kotlin/android/graphics/PathDashPathEffect.Style)!: how to transform the shape at each position as it is stamped |
