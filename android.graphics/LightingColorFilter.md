# LightingColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LightingColorFilter

Kotlin| [Java](../android/graphics/LightingColorFilter.md) 
| --- | --- |

```
open class LightingColorFilter : ColorFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.ColorFilter](../android/graphics/ColorFilter.md) ||
| | ↳ | [android.graphics.LightingColorFilter](../android/graphics/LightingColorFilter.md) |

A color filter that can be used to simulate simple lighting effects. A`LightingColorFilter`is defined by two parameters, one used to multiply the source color (called`colorMultiply`) and one used to add to the source color (called`colorAdd`). The alpha channel is left untouched by this color filter. Given a source color RGB, the resulting R'G'B' color is computed thusly: 

```kotlin
R' = R * colorMultiply.R + colorAdd.R
  G' = G * colorMultiply.G + colorAdd.G
  B' = B * colorMultiply.B + colorAdd.B
  
```
The result is pinned to the`[0..255]`range for each channel.

<br />

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LightingColorFilter](../android/graphics/LightingColorFilter.md))`(`mul:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `add:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a colorfilter that multiplies the RGB channels by one color, and then adds a second color. |

| Public methods ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColorAdd](../android/graphics/LightingColorFilter.md))`()` Returns the RGB color that will be added to the source color when the color filter is applied. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColorMultiply](../android/graphics/LightingColorFilter.md))`()` Returns the RGB color used to multiply the source color when the color filter is applied. |

## Public constructors

### LightingColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LightingColorFilter(
    mul: Int, 
    add: Int)
```

Create a colorfilter that multiplies the RGB channels by one color, and then adds a second color. The alpha components of the mul and add arguments are ignored.

## Public methods

### getColorAdd

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColorAdd(): Int
```

Returns the RGB color that will be added to the source color when the color filter is applied. 

### getColorMultiply

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColorMultiply(): Int
```

Returns the RGB color used to multiply the source color when the color filter is applied.
