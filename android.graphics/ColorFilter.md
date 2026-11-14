# ColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ColorFilter

Kotlin | [Java](https://developer.android.com/reference/android/graphics/ColorFilter "View this page in Java") 

```
open class ColorFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.graphics.ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter#) |

| Known Direct Subclasses [BlendModeColorFilter](https://developer.android.com/reference/kotlin/android/graphics/BlendModeColorFilter), [ColorMatrixColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorMatrixColorFilter), [LightingColorFilter](https://developer.android.com/reference/kotlin/android/graphics/LightingColorFilter), [PorterDuffColorFilter](https://developer.android.com/reference/kotlin/android/graphics/PorterDuffColorFilter), [RuntimeColorFilter](https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter) |------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BlendModeColorFilter](https://developer.android.com/reference/kotlin/android/graphics/BlendModeColorFilter) | A color filter that can be used to tint the source pixels using a single color and a specific [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode). | | [ColorMatrixColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorMatrixColorFilter) | A color filter that transforms colors through a 4x5 color matrix. | | [LightingColorFilter](https://developer.android.com/reference/kotlin/android/graphics/LightingColorFilter) | A color filter that can be used to simulate simple lighting effects. | | [PorterDuffColorFilter](https://developer.android.com/reference/kotlin/android/graphics/PorterDuffColorFilter) | A color filter that can be used to tint the source pixels using a single color and a specific [Porter-Duff composite mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff). | | [RuntimeColorFilter](https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter) | A [RuntimeColorFilter](https://developer.android.com/reference/kotlin/android/graphics/RuntimeColorFilter) calculates a per-pixel color based on the output of a user \* defined Android Graphics Shading Language (AGSL) function. | |

A color filter can be used with a [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint) to modify the color of each pixel drawn with that paint. This is an abstract class that should never be used directly.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------|---|
| [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter#ColorFilter())`()` <br /> |

## Public constructors

### ColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ColorFilter()
```

**Deprecated:** *Use subclass constructors directly instead.*
