Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BitmapShader

Kotlin | [Java](BitmapShader.md)
| --- | --- |

```
open class BitmapShader : Shader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.Shader](Shader.md) ||
| | ↳ | [android.graphics.BitmapShader](BitmapShader.md) |

Shader used to draw a bitmap as a texture. The bitmap can be repeated or mirrored by setting the tiling mode.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#FILTER_MODE_DEFAULT:kotlin.Int` This FilterMode value will respect the value of the Paint#isFilterBitmap flag while the shader is attached to the Paint. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#FILTER_MODE_LINEAR:kotlin.Int` This FilterMode value will cause the shader to interpolate the output of the shader from a 2x2 grid of pixels nearest to the sample point (i.e. bilinear interpolation). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#FILTER_MODE_NEAREST:kotlin.Int` This FilterMode value will cause the shader to sample from the nearest pixel to the requested sample point. |
| --- | --- |

| Public constructors ||
|---|---|
| BitmapShader Call this to create a new shader that will draw with a bitmap. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getFilterMode Returns the filter mode used when sampling from this shader |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMaxAnisotropy Returns the current max anisotropic filtering value configured by setFilterMode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setFilterMode Set the filter mode to be used when sampling from this shader. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setMaxAnisotropy Enables and configures the max anisotropy sampling value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOverrideGainmap Draws the BitmapShader with a copy of the given gainmap instead of the gainmap on the Bitmap the shader was constructed from |

| Inherited functions ||
|---|---|
| From class Shader |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getLocalMatrix Return true if the shader has a non-identity local matrix. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setLocalMatrix Set the shader's local matrix. Passing null will reset the shader's matrix to identity. If the matrix has scale value as 0, the drawing result is undefined. <br /> | ||

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

- setFilterMode

### FILTER_MODE_LINEAR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FILTER_MODE_LINEAR: Int
```

This FilterMode value will cause the shader to interpolate the output of the shader from a 2x2 grid of pixels nearest to the sample point (i.e. bilinear interpolation).

This value will override the effect of Paint#isFilterBitmap.

 Value: 2

**See Also**

- setFilterMode

### FILTER_MODE_NEAREST

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FILTER_MODE_NEAREST: Int
```

This FilterMode value will cause the shader to sample from the nearest pixel to the requested sample point.

This value will override the effect of Paint#isFilterBitmap.

 Value: 1

**See Also**

- setFilterMode

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
| `bitmap` | [Bitmap](Bitmap.md): The bitmap to use inside the shader. This value cannot be `null`. |
| `tileX` | [Shader.TileMode](../android/graphics/Shader.TileMode.md): The tiling mode for x to draw the bitmap in. This value cannot be `null`. |
| `tileY` | [Shader.TileMode](../android/graphics/Shader.TileMode.md): The tiling mode for y to draw the bitmap in. This value cannot be `null`. |
| --- | --- |

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

Returns the current max anisotropic filtering value configured by setFilterMode. If setFilterMode is invoked this returns zero.

### setFilterMode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFilterMode(mode: Int): Unit
```

Set the filter mode to be used when sampling from this shader. If this is configured then the anisotropic filtering value specified in any previous call to setMaxAnisotropy is ignored.

| Parameters ||
|---|---|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#FILTER_MODE_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#FILTER_MODE_NEAREST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/BitmapShader#FILTER_MODE_LINEAR:kotlin.Int` |

### setMaxAnisotropy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMaxAnisotropy(maxAnisotropy: Int): Unit
```

Enables and configures the max anisotropy sampling value. If this value is configured, setFilterMode is ignored. Anisotropic filtering can enhance visual quality by removing aliasing effects of images that are at oblique viewing angles. This value is typically consumed as a power of 2 and anisotropic values of the next power of 2 typically provide twice the quality improvement as the previous value. For example, a sampling value of 4 would provide twice the improvement of a sampling value of 2. It is important to note that higher sampling values reach diminishing returns as the improvements between 8 and 16 can be slight.

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
| `overrideGainmap` | [Gainmap](Gainmap.md)?: The gainmap to draw instead, null to use any gainmap on the Bitmap |
