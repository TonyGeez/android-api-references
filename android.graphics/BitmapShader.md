Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BitmapShader

Kotlin | [Java](https://developer.android.com/reference/android/graphics/BitmapShader "View this page in Java")

```
open class BitmapShader : Shader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.graphics.Shader](https://developer.android.com/reference/kotlin/android/graphics/Shader) ||
| | ↳ | [android.graphics.BitmapShader](https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#) |

Shader used to draw a bitmap as a texture. The bitmap can be repeated or mirrored by setting the tiling mode.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#FILTER_MODE_DEFAULT:kotlin.Int` This FilterMode value will respect the value of the Paint#isFilterBitmap flag while the shader is attached to the Paint. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#FILTER_MODE_LINEAR:kotlin.Int` This FilterMode value will cause the shader to interpolate the output of the shader from a 2x2 grid of pixels nearest to the sample point (i.e. bilinear interpolation). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#FILTER_MODE_NEAREST:kotlin.Int` This FilterMode value will cause the shader to sample from the nearest pixel to the requested sample point. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#BitmapShader(android.graphics.Bitmap,%20android.graphics.Shader.TileMode,%20android.graphics.Shader.TileMode)(bitmap: https://developer.android.com/reference/kotlin/android/graphics/Bitmap, tileX: https://developer.android.com/reference/kotlin/android/graphics/Shader.TileMode, tileY: https://developer.android.com/reference/kotlin/android/graphics/Shader.TileMode)` Call this to create a new shader that will draw with a bitmap. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#getFilterMode()()` Returns the filter mode used when sampling from this shader |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#getMaxAnisotropy()()` Returns the current max anisotropic filtering value configured by `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#setFilterMode(kotlin.Int)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#setFilterMode(kotlin.Int)(mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the filter mode to be used when sampling from this shader. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#setMaxAnisotropy(kotlin.Int)(maxAnisotropy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Enables and configures the max anisotropy sampling value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#setOverrideGainmap(android.graphics.Gainmap)(overrideGainmap: https://developer.android.com/reference/kotlin/android/graphics/Gainmap?)` Draws the BitmapShader with a copy of the given gainmap instead of the gainmap on the Bitmap the shader was constructed from |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/graphics/Shader` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/Shader#getLocalMatrix(android.graphics.Matrix)(localM: https://developer.android.com/reference/kotlin/android/graphics/Matrix)` Return true if the shader has a non-identity local matrix. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/Shader#setLocalMatrix(android.graphics.Matrix)(localM: https://developer.android.com/reference/kotlin/android/graphics/Matrix?)` Set the shader's local matrix. Passing null will reset the shader's matrix to identity. If the matrix has scale value as 0, the drawing result is undefined. <br /> | ||

## Constants

### FILTER_MODE_DEFAULT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FILTER_MODE_DEFAULT: Int
```

This FilterMode value will respect the value of the Paint#isFilterBitmap flag while the shader is attached to the Paint.

The exception to this rule is when a Shader is attached as input to a RuntimeShader. In that case this mode will default to FILTER_MODE_NEAREST.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#setFilterMode(kotlin.Int)`

### FILTER_MODE_LINEAR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FILTER_MODE_LINEAR: Int
```

This FilterMode value will cause the shader to interpolate the output of the shader from a 2x2 grid of pixels nearest to the sample point (i.e. bilinear interpolation).

This value will override the effect of Paint#isFilterBitmap.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#setFilterMode(kotlin.Int)`

### FILTER_MODE_NEAREST

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FILTER_MODE_NEAREST: Int
```

This FilterMode value will cause the shader to sample from the nearest pixel to the requested sample point.

This value will override the effect of Paint#isFilterBitmap.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#setFilterMode(kotlin.Int)`

## Public constructors

### BitmapShader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BitmapShader(
    bitmap: Bitmap, 
    tileX: Shader.TileMode, 
    tileY: Shader.TileMode)
```

Call this to create a new shader that will draw with a bitmap.

| Parameters ||
|---|---|
| `bitmap` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap): The bitmap to use inside the shader. This value cannot be `null`. |
| `tileX` | [Shader.TileMode](https://developer.android.com/reference/kotlin/android/graphics/Shader.TileMode): The tiling mode for x to draw the bitmap in. This value cannot be `null`. |
| `tileY` | [Shader.TileMode](https://developer.android.com/reference/kotlin/android/graphics/Shader.TileMode): The tiling mode for y to draw the bitmap in. This value cannot be `null`. |

## Public methods

### getFilterMode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFilterMode(): Int
```

Returns the filter mode used when sampling from this shader

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#FILTER_MODE_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#FILTER_MODE_NEAREST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#FILTER_MODE_LINEAR:kotlin.Int` |

### getMaxAnisotropy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMaxAnisotropy(): Int
```

Returns the current max anisotropic filtering value configured by `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#setFilterMode(kotlin.Int)`. If `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#setFilterMode(kotlin.Int)` is invoked this returns zero.

### setFilterMode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFilterMode(mode: Int): Unit
```

Set the filter mode to be used when sampling from this shader. If this is configured then the anisotropic filtering value specified in any previous call to `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#setMaxAnisotropy(kotlin.Int)` is ignored.

| Parameters ||
|---|---|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#FILTER_MODE_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#FILTER_MODE_NEAREST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#FILTER_MODE_LINEAR:kotlin.Int` |

### setMaxAnisotropy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMaxAnisotropy(maxAnisotropy: Int): Unit
```

Enables and configures the max anisotropy sampling value. If this value is configured, `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#setFilterMode(kotlin.Int)` is ignored. Anisotropic filtering can enhance visual quality by removing aliasing effects of images that are at oblique viewing angles. This value is typically consumed as a power of 2 and anisotropic values of the next power of 2 typically provide twice the quality improvement as the previous value. For example, a sampling value of 4 would provide twice the improvement of a sampling value of 2. It is important to note that higher sampling values reach diminishing returns as the improvements between 8 and 16 can be slight.

| Parameters ||
|---|---|
| `maxAnisotropy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The Anisotropy value to use for filtering. Must be greater than 0. Value is 1 or greater |

### setOverrideGainmap

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOverrideGainmap(overrideGainmap: Gainmap?): Unit
```

Draws the BitmapShader with a copy of the given gainmap instead of the gainmap on the Bitmap the shader was constructed from

| Parameters ||
|---|---|
| `overrideGainmap` | [Gainmap](https://developer.android.com/reference/kotlin/android/graphics/Gainmap)?: The gainmap to draw instead, null to use any gainmap on the Bitmap |
