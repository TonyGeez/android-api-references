# ColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ColorFilter

Kotlin | [Java](../android/graphics/ColorFilter.md) 
| --- | --- |

```
open class ColorFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.ColorFilter](../android/graphics/ColorFilter.md) |

| Known Direct Subclasses [BlendModeColorFilter](../android/graphics/BlendModeColorFilter.md), [ColorMatrixColorFilter](../android/graphics/ColorMatrixColorFilter.md), [LightingColorFilter](../android/graphics/LightingColorFilter.md), [PorterDuffColorFilter](../android/graphics/PorterDuffColorFilter.md), [RuntimeColorFilter](../android/graphics/RuntimeColorFilter.md) |------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BlendModeColorFilter](../android/graphics/BlendModeColorFilter.md) | A color filter that can be used to tint the source pixels using a single color and a specific [BlendMode](../android/graphics/BlendMode.md). | | [ColorMatrixColorFilter](../android/graphics/ColorMatrixColorFilter.md) | A color filter that transforms colors through a 4x5 color matrix. | | [LightingColorFilter](../android/graphics/LightingColorFilter.md) | A color filter that can be used to simulate simple lighting effects. | | [PorterDuffColorFilter](../android/graphics/PorterDuffColorFilter.md) | A color filter that can be used to tint the source pixels using a single color and a specific [Porter-Duff composite mode](../android/graphics/PorterDuff.md). | | [RuntimeColorFilter](../android/graphics/RuntimeColorFilter.md) | A [RuntimeColorFilter](../android/graphics/RuntimeColorFilter.md) calculates a per-pixel color based on the output of a user \* defined Android Graphics Shading Language (AGSL) function. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A color filter can be used with a [Paint](../android/graphics/Paint.md) to modify the color of each pixel drawn with that paint. This is an abstract class that should never be used directly.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------|---|
| [ColorFilter](../android/graphics/ColorFilter.md))`()` <br /> |

## Public constructors

### ColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ColorFilter()
```

**Deprecated:** *Use subclass constructors directly instead.*
