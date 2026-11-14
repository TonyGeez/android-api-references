# BlurMaskFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BlurMaskFilter

Kotlin| [Java](BlurMaskFilter.md) 
| --- | --- |

```
open class BlurMaskFilter : MaskFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.MaskFilter](MaskFilter.md) ||
| | ↳ | [android.graphics.BlurMaskFilter](BlurMaskFilter.md) |

This takes a mask, and blurs its edge by the specified radius. Whether or or not to include the original mask, and whether the blur goes outside, inside, or straddles, the original mask's border, is controlled by the Blur enum.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------|
| | [Blur](../android/graphics/BlurMaskFilter.Blur.md) <br /> |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BlurMaskFilter](BlurMaskFilter.md))`(`radius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `style:` ` [BlurMaskFilter.Blur](../android/graphics/BlurMaskFilter.Blur.md)!`)` Create a blur maskfilter. |

| Inherited functions ||
|---|---|
| From class [MaskFilter](MaskFilter.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](MaskFilter.md))`()` <br /> | ||

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
| `style` | [BlurMaskFilter.Blur](../android/graphics/BlurMaskFilter.Blur.md)!:The Blur to use |

| Return ||
|---|-------------------------|
| | The new blur maskfilter |
