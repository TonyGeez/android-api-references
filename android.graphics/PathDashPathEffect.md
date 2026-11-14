# PathDashPathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PathDashPathEffect

Kotlin | [Java](PathDashPathEffect.md) 
| --- | --- |

```
open class PathDashPathEffect : PathEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.PathEffect](PathEffect.md) ||
| | ↳ | [android.graphics.PathDashPathEffect](PathDashPathEffect.md) |

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------|
| | [Style](../android/graphics/PathDashPathEffect.Style.md) <br /> |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PathDashPathEffect](PathDashPathEffect.md))`(`shape:` ` [Path](Path.md)!`, `advance:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `phase:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `style:` ` [PathDashPathEffect.Style](../android/graphics/PathDashPathEffect.Style.md)!`)` Dash the drawn path by stamping it with the specified shape. |

| Inherited functions ||
|---|---|
| From class [PathEffect](PathEffect.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](PathEffect.md))`()` <br /> | ||

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
| `shape` | [Path](Path.md)!: The path to stamp along |
| `advance` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): spacing between each stamp of shape |
| `phase` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): amount to offset before the first shape is stamped |
| --- | --- |
| `style` | [PathDashPathEffect.Style](../android/graphics/PathDashPathEffect.Style.md)!: how to transform the shape at each position as it is stamped |
