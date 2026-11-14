# BlurMaskFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BlurMaskFilter

Kotlin| [Java](https://developer.android.com/reference/android/graphics/BlurMaskFilter "View this page in Java") 

```
open class BlurMaskFilter : MaskFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.graphics.MaskFilter](https://developer.android.com/reference/kotlin/android/graphics/MaskFilter) ||
| | ↳ | [android.graphics.BlurMaskFilter](https://developer.android.com/reference/kotlin/android/graphics/BlurMaskFilter#) |

This takes a mask, and blurs its edge by the specified radius. Whether or or not to include the original mask, and whether the blur goes outside, inside, or straddles, the original mask's border, is controlled by the Blur enum.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------|
| | [Blur](https://developer.android.com/reference/kotlin/android/graphics/BlurMaskFilter.Blur) <br /> |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BlurMaskFilter](https://developer.android.com/reference/kotlin/android/graphics/BlurMaskFilter#BlurMaskFilter(kotlin.Float,%20android.graphics.BlurMaskFilter.Blur))`(`radius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `style:` ` [BlurMaskFilter.Blur](https://developer.android.com/reference/kotlin/android/graphics/BlurMaskFilter.Blur)!`)` Create a blur maskfilter. |

| Inherited functions ||
|---|---|
| From class [MaskFilter](https://developer.android.com/reference/kotlin/android/graphics/MaskFilter) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/graphics/MaskFilter#finalize())`()` <br /> | ||

## Public constructors

### BlurMaskFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BlurMaskFilter(
    radius: Float, 
    style: BlurMaskFilter.Blur!)
```

Create a blur maskfilter.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `radius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The radius to extend the blur from the original mask. Must be \> 0. |
| `style` | [BlurMaskFilter.Blur](https://developer.android.com/reference/kotlin/android/graphics/BlurMaskFilter.Blur)!:The Blur to use |

| Return ||
|---|-------------------------|
| | The new blur maskfilter |
