# PaintFlagsDrawFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PaintFlagsDrawFilter

Kotlin| [Java](../android/graphics/PaintFlagsDrawFilter.md) 
| --- | --- |

```
open class PaintFlagsDrawFilter : DrawFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.DrawFilter](../android/graphics/DrawFilter.md) ||
| | ↳ | [android.graphics.PaintFlagsDrawFilter](../android/graphics/PaintFlagsDrawFilter.md) |

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PaintFlagsDrawFilter](../android/graphics/PaintFlagsDrawFilter.md))`(`clearBits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `setBits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Subclass of DrawFilter that affects every paint by first clearing the specified clearBits in the paint's flags, and then setting the specified setBits in the paint's flags. |

| Inherited functions ||
|---|---|
| From class [DrawFilter](../android/graphics/DrawFilter.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/graphics/DrawFilter.md))`()` <br /> | ||

## Public constructors

### PaintFlagsDrawFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PaintFlagsDrawFilter(
    clearBits: Int, 
    setBits: Int)
```

Subclass of DrawFilter that affects every paint by first clearing the specified clearBits in the paint's flags, and then setting the specified setBits in the paint's flags.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------|
| `clearBits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):These bits will be cleared in the paint's flags |
| `setBits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):These bits will be set in the paint's flags |
