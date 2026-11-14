# CornerPathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CornerPathEffect

Kotlin| [Java](https://developer.android.com/reference/android/graphics/CornerPathEffect "View this page in Java") 

```
open class CornerPathEffect : PathEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.graphics.PathEffect](https://developer.android.com/reference/kotlin/android/graphics/PathEffect) ||
| | ↳ | [android.graphics.CornerPathEffect](https://developer.android.com/reference/kotlin/android/graphics/CornerPathEffect#) |

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CornerPathEffect](https://developer.android.com/reference/kotlin/android/graphics/CornerPathEffect#CornerPathEffect(kotlin.Float))`(`radius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Transforms geometries that are drawn (either STROKE or FILL styles) by replacing any sharp angles between line segments into rounded angles of the specified radius. |

| Inherited functions ||
|---|---|
| From class [PathEffect](https://developer.android.com/reference/kotlin/android/graphics/PathEffect) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/graphics/PathEffect#finalize())`()` <br /> | ||

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
