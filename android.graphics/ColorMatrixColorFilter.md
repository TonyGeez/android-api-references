# ColorMatrixColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ColorMatrixColorFilter

Kotlin| [Java](https://developer.android.com/reference/android/graphics/ColorMatrixColorFilter "View this page in Java") 
| --- | --- |

```
open class ColorMatrixColorFilter : ColorFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter) ||
| | ↳ | [android.graphics.ColorMatrixColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorMatrixColorFilter#) |

A color filter that transforms colors through a 4x5 color matrix. This filter can be used to change the saturation of pixels, convert from YUV to RGB, etc.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ColorMatrixColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorMatrixColorFilter#ColorMatrixColorFilter(android.graphics.ColorMatrix))`(`matrix:` ` [ColorMatrix](https://developer.android.com/reference/kotlin/android/graphics/ColorMatrix)`)` Create a color filter that transforms colors through a 4x5 color matrix. |
| [ColorMatrixColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorMatrixColorFilter#ColorMatrixColorFilter(kotlin.FloatArray))`(`array:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`)` Create a color filter that transforms colors through a 4x5 color matrix. |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getColorMatrix](https://developer.android.com/reference/kotlin/android/graphics/ColorMatrixColorFilter#getColorMatrix(android.graphics.ColorMatrix))`(`colorMatrix:` ` [ColorMatrix](https://developer.android.com/reference/kotlin/android/graphics/ColorMatrix)!`)` Copies the ColorMatrix from the filter into the passed ColorMatrix. |

## Public constructors

### ColorMatrixColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ColorMatrixColorFilter(matrix: ColorMatrix)
```

Create a color filter that transforms colors through a 4x5 color matrix.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `matrix` | [ColorMatrix](https://developer.android.com/reference/kotlin/android/graphics/ColorMatrix):4x5 matrix used to transform colors. It is copied into the filter, so changes made to the matrix after the filter is constructed will not be reflected in the filter. This value cannot be`null`. |

### ColorMatrixColorFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ColorMatrixColorFilter(array: FloatArray)
```

Create a color filter that transforms colors through a 4x5 color matrix.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `array` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html):Array of floats used to transform colors, treated as a 4x5 matrix. The first 20 entries of the array are copied into the filter. See ColorMatrix. This value cannot be`null`. |

## Public methods

### getColorMatrix

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColorMatrix(colorMatrix: ColorMatrix!): Unit
```

Copies the ColorMatrix from the filter into the passed ColorMatrix.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `colorMatrix` | [ColorMatrix](https://developer.android.com/reference/kotlin/android/graphics/ColorMatrix)!:Set to the current value of the filter's ColorMatrix. |
