# ColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ColorFilter

Kotlin | [Java](ColorFilter.md) 
| --- | --- |

```
open class ColorFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.ColorFilter](ColorFilter.md) |

| Known Direct Subclasses [BlendModeColorFilter](BlendModeColorFilter.md), [ColorMatrixColorFilter](ColorMatrixColorFilter.md), [LightingColorFilter](LightingColorFilter.md), [PorterDuffColorFilter](PorterDuffColorFilter.md), [RuntimeColorFilter](RuntimeColorFilter.md) |------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BlendModeColorFilter](BlendModeColorFilter.md) | A color filter that can be used to tint the source pixels using a single color and a specific [BlendMode](BlendMode.md). | | [ColorMatrixColorFilter](ColorMatrixColorFilter.md) | A color filter that transforms colors through a 4x5 color matrix. | | [LightingColorFilter](LightingColorFilter.md) | A color filter that can be used to simulate simple lighting effects. | | [PorterDuffColorFilter](PorterDuffColorFilter.md) | A color filter that can be used to tint the source pixels using a single color and a specific [Porter-Duff composite mode](PorterDuff.md). | | [RuntimeColorFilter](RuntimeColorFilter.md) | A [RuntimeColorFilter](RuntimeColorFilter.md) calculates a per-pixel color based on the output of a user \* defined Android Graphics Shading Language (AGSL) function. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A color filter can be used with a [Paint](Paint.md) to modify the color of each pixel drawn with that paint. This is an abstract class that should never be used directly.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------|---|
| [ColorFilter](ColorFilter.md))`()` <br /> |

## Public constructors

### ColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ColorFilter()
```

**Deprecated:** *Use subclass constructors directly instead.*
