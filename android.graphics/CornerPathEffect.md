# CornerPathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CornerPathEffect

Kotlin| [Java](CornerPathEffect.md) 
| --- | --- |

```
open class CornerPathEffect : PathEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.PathEffect](PathEffect.md) ||
| | ↳ | [android.graphics.CornerPathEffect](CornerPathEffect.md) |

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CornerPathEffect](CornerPathEffect.md))`(`radius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Transforms geometries that are drawn (either STROKE or FILL styles) by replacing any sharp angles between line segments into rounded angles of the specified radius. |

| Inherited functions ||
|---|---|
| From class [PathEffect](PathEffect.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](PathEffect.md))`()` <br /> | ||

## Public constructors

### CornerPathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CornerPathEffect(radius: Float)
```

Transforms geometries that are drawn (either STROKE or FILL styles) by replacing any sharp angles between line segments into rounded angles of the specified radius.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `radius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Amount to round sharp angles between line segments. |
