# DashPathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DashPathEffect

Kotlin| [Java](https://developer.android.com/reference/android/graphics/DashPathEffect "View this page in Java") 

```
open class DashPathEffect : PathEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.graphics.PathEffect](https://developer.android.com/reference/kotlin/android/graphics/PathEffect) ||
| | ↳ | [android.graphics.DashPathEffect](https://developer.android.com/reference/kotlin/android/graphics/DashPathEffect#) |

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DashPathEffect](https://developer.android.com/reference/kotlin/android/graphics/DashPathEffect#DashPathEffect(kotlin.FloatArray,%20kotlin.Float))`(`intervals:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `phase:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` The intervals array must contain an even number of entries (\>=2), with the even indices specifying the "on" intervals, and the odd indices specifying the "off" intervals. |

| Inherited functions ||
|---|---|
| From class [PathEffect](https://developer.android.com/reference/kotlin/android/graphics/PathEffect) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/graphics/PathEffect#finalize())`()` <br /> | ||

## Public constructors

### DashPathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DashPathEffect(
    intervals: FloatArray!, 
    phase: Float)
```

The intervals array must contain an even number of entries (\>=2), with the even indices specifying the "on" intervals, and the odd indices specifying the "off" intervals. phase is an offset into the intervals array (mod the sum of all of the intervals). The intervals array controls the length of the dashes. The paint's strokeWidth controls the thickness of the dashes. Note: this patheffect only affects drawing with the paint's style is set to STROKE or FILL_AND_STROKE. It is ignored if the drawing is done with style == FILL.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| `intervals` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:array of ON and OFF distances |
| `phase` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):offset into the intervals array |
