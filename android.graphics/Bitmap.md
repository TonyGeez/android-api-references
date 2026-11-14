Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Bitmap

```
class Bitmap : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.graphics.Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#) |

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.CompressFormat` Specifies the known formats a bitmap can be compressed into |
| | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` Possible bitmap configurations. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#DENSITY_NONE:kotlin.Int` Indicates that the bitmap was created for an unknown pixel density. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#asShared()()` Return an immutable bitmap backed by shared memory which can be efficiently passed between processes via Parcelable. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#compress(android.graphics.Bitmap.CompressFormat,%20kotlin.Int,%20java.io.OutputStream)(format: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.CompressFormat, quality: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, stream: https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)` Write a compressed version of the bitmap to the specified outputstream. |
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#)! | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#copy(android.graphics.Bitmap.Config,%20kotlin.Boolean)(config: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config, isMutable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Tries to make a new bitmap based on the dimensions of this bitmap, setting the new bitmap's config to the one specified, and then copying this bitmap's pixels into the new bitmap. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#copyPixelsFromBuffer(java.nio.Buffer)(src: https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)` Copy the pixels from the buffer, beginning at the current position, overwriting the bitmap's pixels. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#copyPixelsToBuffer(java.nio.Buffer)(dst: https://developer.android.com/reference/kotlin/java/nio/Buffer.html#)` Copy the bitmap's pixels into the specified buffer (allocated by the caller). |
| static [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#createBitmap(android.graphics.Bitmap)(src: https://developer.android.com/reference/kotlin/android/graphics/Bitmap#)` Returns a bitmap from the source bitmap. |
| static [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#createBitmap(android.graphics.Bitmap,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(source: https://developer.android.com/reference/kotlin/android/graphics/Bitmap#, x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a bitmap from the specified subset of the source bitmap. |
| static [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#createBitmap(android.graphics.Bitmap,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Matrix,%20kotlin.Boolean)(source: https://developer.android.com/reference/kotlin/android/graphics/Bitmap#, x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, m: https://developer.android.com/reference/kotlin/android/graphics/Matrix?, filter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns a bitmap from subset of the source bitmap, transformed by the optional matrix. |
| static [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#createBitmap(android.graphics.Picture)(source: https://developer.android.com/reference/kotlin/android/graphics/Picture)` Creates a Bitmap from the given `https://developer.android.com/reference/kotlin/android/graphics/Picture` source of recorded drawing commands. |
| static [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#createBitmap(android.graphics.Picture,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config)(source: https://developer.android.com/reference/kotlin/android/graphics/Picture, width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, config: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config)` Creates a Bitmap from the given `https://developer.android.com/reference/kotlin/android/graphics/Picture` source of recorded drawing commands. |
| static [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#createBitmap(android.util.DisplayMetrics,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config)(display: https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#?, width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, config: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config)` Returns a mutable bitmap with the specified width and height. |
| static [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#createBitmap(android.util.DisplayMetrics,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config,%20kotlin.Boolean)(display: https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#?, width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, config: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config, hasAlpha: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns a mutable bitmap with the specified width and height. |
| static [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#createBitmap(android.util.DisplayMetrics,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config,%20kotlin.Boolean,%20android.graphics.ColorSpace)(display: https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#?, width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, config: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config, hasAlpha: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, colorSpace: https://developer.android.com/reference/kotlin/android/graphics/ColorSpace)` Returns a mutable bitmap with the specified width and height. |
| static [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#createBitmap(android.util.DisplayMetrics,%20kotlin.IntArray,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config)(display: https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#?, colors: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html, width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, config: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config)` Returns a immutable bitmap with the specified width and height, with each pixel value set to the corresponding value in the colors array. |
| static [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#createBitmap(android.util.DisplayMetrics,%20kotlin.IntArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config)(display: https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#, colors: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, stride: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, config: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config)` Returns a immutable bitmap with the specified width and height, with each pixel value set to the corresponding value in the colors array. |
| static [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#createBitmap(kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config)(width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, config: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config)` Returns a mutable bitmap with the specified width and height. |
| static [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#createBitmap(kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config,%20kotlin.Boolean)(width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, config: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config, hasAlpha: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns a mutable bitmap with the specified width and height. |
| static [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#createBitmap(kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config,%20kotlin.Boolean,%20android.graphics.ColorSpace)(width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, config: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config, hasAlpha: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, colorSpace: https://developer.android.com/reference/kotlin/android/graphics/ColorSpace)` Returns a mutable bitmap with the specified width and height. |
| static [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#createBitmap(kotlin.IntArray,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config)(colors: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html, width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, config: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config!)` Returns a immutable bitmap with the specified width and height, with each pixel value set to the corresponding value in the colors array. |
| static [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#createBitmap(kotlin.IntArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config)(colors: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, stride: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, config: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config)` Returns a immutable bitmap with the specified width and height, with each pixel value set to the corresponding value in the colors array. |
| static [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#createScaledBitmap(android.graphics.Bitmap,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean)(src: https://developer.android.com/reference/kotlin/android/graphics/Bitmap#, dstWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dstHeight: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, filter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Creates a new bitmap, scaled from an existing bitmap, when possible. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#describeContents()()` No special parcel contents. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#eraseColor(kotlin.Int)(c: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Fills the bitmap's pixels with the specified `https://developer.android.com/reference/kotlin/android/graphics/Color`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#eraseColor(kotlin.Long)(color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Fills the bitmap's pixels with the specified `ColorLong`. |
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#extractAlpha()()` Returns a new bitmap that captures the alpha values of the original. |
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#extractAlpha(android.graphics.Paint,%20kotlin.IntArray)(paint: https://developer.android.com/reference/kotlin/android/graphics/Paint?, offsetXY: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!)` Returns a new bitmap that captures the alpha values of the original. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getAllocationByteCount()()` Returns the size of the allocated memory used to store this bitmap's pixels. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getByteCount()()` Returns the minimum number of bytes that can be used to store this bitmap's pixels. |
| [Color](https://developer.android.com/reference/kotlin/android/graphics/Color) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getColor(kotlin.Int,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the `https://developer.android.com/reference/kotlin/android/graphics/Color` at the specified location. |
| [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace)? | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getColorSpace()()` Returns the color space associated with this bitmap. |
| [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config)? | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getConfig()()` If the bitmap's internal config is in one of the public formats, return that config, otherwise return null. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getDensity()()` Returns the density for this bitmap. |
| [Gainmap](https://developer.android.com/reference/kotlin/android/graphics/Gainmap)? | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getGainmap()()` Returns the gainmap or null if the bitmap doesn't contain a gainmap |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getGenerationId()()` Returns the generation ID of this bitmap. |
| [HardwareBuffer](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getHardwareBuffer()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getHeight()()` Returns the bitmap's height |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getNinePatchChunk()()` Returns an optional array of private data, used by the UI system for some bitmaps. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getPixel(kotlin.Int,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the `https://developer.android.com/reference/kotlin/android/graphics/Color` at the specified location. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getPixels(kotlin.IntArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(pixels: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, stride: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns in pixels\[\] a copy of the data in the bitmap. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getRowBytes()()` Return the number of bytes between rows in the bitmap's pixels. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getScaledHeight(android.graphics.Canvas)(canvas: https://developer.android.com/reference/kotlin/android/graphics/Canvas)` Convenience for calling `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getScaledHeight(kotlin.Int)` with the target density of the given `https://developer.android.com/reference/kotlin/android/graphics/Canvas`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getScaledHeight(android.util.DisplayMetrics)(metrics: https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#)` Convenience for calling `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getScaledHeight(kotlin.Int)` with the target density of the given `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getScaledHeight(kotlin.Int)(targetDensity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Convenience method that returns the height of this bitmap divided by the density scale factor. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getScaledWidth(android.graphics.Canvas)(canvas: https://developer.android.com/reference/kotlin/android/graphics/Canvas)` Convenience for calling `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getScaledWidth(kotlin.Int)` with the target density of the given `https://developer.android.com/reference/kotlin/android/graphics/Canvas`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getScaledWidth(android.util.DisplayMetrics)(metrics: https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#)` Convenience for calling `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getScaledWidth(kotlin.Int)` with the target density of the given `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getScaledWidth(kotlin.Int)(targetDensity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Convenience method that returns the width of this bitmap divided by the density scale factor. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getWidth()()` Returns the bitmap's width |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#hasAlpha()()` Returns true if the bitmap's config supports per-pixel alpha, and if the pixels may contain non-opaque alpha values. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#hasGainmap()()` Returns whether or not this Bitmap contains a Gainmap. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#hasMipMap()()` Indicates whether the renderer responsible for drawing this bitmap should attempt to use mipmaps when this bitmap is drawn scaled down. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#isMutable()()` Returns true if the bitmap is marked as mutable (i.e. can be drawn into) |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#isPremultiplied()()` Indicates whether pixels stored in this bitmaps are stored pre-multiplied. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#isRecycled()()` Returns true if this bitmap has been recycled. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#prepareToDraw()()` Builds caches associated with the bitmap that are used for drawing it. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#reconfigure(kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config)(width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, config: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config)` Modifies the bitmap to have a specified width, height, and `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config`, without affecting the underlying allocation backing the bitmap. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#recycle()()` Immediately releases the pixel data associated with this Bitmap. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#sameAs(android.graphics.Bitmap)(other: https://developer.android.com/reference/kotlin/android/graphics/Bitmap#?)` Given another bitmap, return true if it has the same dimensions, config, and pixel data as this bitmap. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setColorSpace(android.graphics.ColorSpace)(colorSpace: https://developer.android.com/reference/kotlin/android/graphics/ColorSpace)` Modifies the bitmap to have the specified `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace`, without affecting the underlying allocation backing the bitmap. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setConfig(android.graphics.Bitmap.Config)(config: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config)` Convenience method for calling `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#reconfigure(kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config)` with the current height and width. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setDensity(kotlin.Int)(density: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specifies the density for this bitmap. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setGainmap(android.graphics.Gainmap)(gainmap: https://developer.android.com/reference/kotlin/android/graphics/Gainmap?)` Sets a gainmap on this bitmap, or removes the gainmap if null |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setHasAlpha(kotlin.Boolean)(hasAlpha: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Tell the bitmap if all of the pixels are known to be opaque (false) or if some of the pixels may contain non-opaque alpha values (true). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setHasMipMap(kotlin.Boolean)(hasMipMap: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set a hint for the renderer responsible for drawing this bitmap indicating that it should attempt to use mipmaps when this bitmap is drawn scaled down. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setHeight(kotlin.Int)(height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Convenience method for calling `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#reconfigure(kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config)` with the current width and config. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setPixel(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Write the specified `https://developer.android.com/reference/kotlin/android/graphics/Color` into the bitmap (assuming it is mutable) at the x,y coordinate. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setPixels(kotlin.IntArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(pixels: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, stride: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Replace pixels in the bitmap with the colors in the array. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setPremultiplied(kotlin.Boolean)(premultiplied: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the bitmap should treat its data as pre-multiplied. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setWidth(kotlin.Int)(width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Convenience method for calling `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#reconfigure(kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config)` with the current height and config. |
| static [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#)? | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#wrapHardwareBuffer(android.hardware.HardwareBuffer,%20android.graphics.ColorSpace)(hardwareBuffer: https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#, colorSpace: https://developer.android.com/reference/kotlin/android/graphics/ColorSpace?)` Create a hardware bitmap backed by a `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#writeToParcel(android.os.Parcel,%20kotlin.Int)(p: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Write the bitmap and its pixels to the parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#)!\> | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### DENSITY_NONE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DENSITY_NONE: Int
```

Indicates that the bitmap was created for an unknown pixel density.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getDensity()`
- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setDensity(kotlin.Int)`

## Public methods

### asShared

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun asShared(): Bitmap
```

Return an immutable bitmap backed by shared memory which can be efficiently passed between processes via Parcelable.

If this bitmap already meets these criteria it will return itself.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#` | This value cannot be `null`. |

### compress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compress(
    format: Bitmap.CompressFormat, 
    quality: Int, 
    stream: OutputStream
): Boolean
```

Write a compressed version of the bitmap to the specified outputstream. If this returns true, the bitmap can be reconstructed by passing a corresponding inputstream to BitmapFactory.decodeStream(). Note: not all Formats support all bitmap configs directly, so it is possible that the returned bitmap from BitmapFactory could be in a different bitdepth, and/or may have lost per-pixel alpha (e.g. JPEG only supports opaque pixels). 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `format` | [Bitmap.CompressFormat](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.CompressFormat): The format of the compressed image. This value cannot be `null`. |
| `quality` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Hint to the compressor, 0-100. The value is interpreted differently depending on the `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.CompressFormat`. |
| `stream` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#): The outputstream to write the compressed data. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if successfully compressed to the specified stream. |

### copy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun copy(
    config: Bitmap.Config, 
    isMutable: Boolean
): Bitmap!
```

Tries to make a new bitmap based on the dimensions of this bitmap, setting the new bitmap's config to the one specified, and then copying this bitmap's pixels into the new bitmap. If the conversion is not supported, or the allocator fails, then this returns NULL. The returned bitmap has the same density and color space as the original, except in the following cases. When copying to `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config`, the color space is dropped. When copying to or from `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config`, EXTENDED or non-EXTENDED variants may be adjusted as appropriate.

| Parameters ||
|---|---|
| `config` | [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config): The desired config for the resulting bitmap. This value cannot be `null`. |
| `isMutable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the resulting bitmap should be mutable (i.e. its pixels can be modified) |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#!` | the new bitmap, or null if the copy could not be made. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if config is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` and isMutable is true |

### copyPixelsFromBuffer

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun copyPixelsFromBuffer(src: Buffer): Unit
```

Copy the pixels from the buffer, beginning at the current position, overwriting the bitmap's pixels. The data in the buffer is not changed in any way (unlike setPixels(), which converts from unpremultipled 32bit to whatever the bitmap's native format is. The pixels in the source buffer are assumed to be in the bitmap's color space.

The data in the buffer must be packed according to the Bitmap's `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config`. See `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` for the packing formulas for each configuration.

After this method returns, the current position of the buffer is updated: the position is incremented by the number of elements read from the buffer. If you need to read the bitmap from the buffer again you must first rewind the buffer.

| Parameters ||
|---|---|
| `src` | [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#): This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the bitmap's config is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` |

### copyPixelsToBuffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun copyPixelsToBuffer(dst: Buffer): Unit
```

Copy the bitmap's pixels into the specified buffer (allocated by the caller). An exception is thrown if the buffer is not large enough to hold all of the pixels (taking into account the number of bytes per pixel) or if the Buffer subclass is not one of the support types (ByteBuffer, ShortBuffer, IntBuffer).

The data copied into the buffer is packed according to the Bitmap's `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config`. See `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` for the packing formulas for each configuration.

The content of the bitmap is copied into the buffer as-is. This means that if this bitmap stores its pixels pre-multiplied (see `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#isPremultiplied()`, the values in the buffer will also be pre-multiplied. The pixels remain in the color space of the bitmap.

After this method returns, the current position of the buffer is updated: the position is incremented by the number of elements written in the buffer.

| Parameters ||
|---|---|
| `dst` | [Buffer](https://developer.android.com/reference/kotlin/java/nio/Buffer.html#): This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the bitmap's config is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` |

### createBitmap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBitmap(src: Bitmap): Bitmap
```

Returns a bitmap from the source bitmap. The new bitmap may be the same object as source, or a copy may have been made. It is initialized with the same density and color space as the original bitmap.

| Parameters ||
|---|---|
| `src` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#` | This value cannot be `null`. |

### createBitmap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBitmap(
    source: Bitmap, 
    x: Int, 
    y: Int, 
    width: Int, 
    height: Int
): Bitmap
```

Returns a bitmap from the specified subset of the source bitmap. The new bitmap may be the same object as source, or a copy may have been made. It is initialized with the same density and color space as the original bitmap.

| Parameters ||
|---|---|
| `source` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#): The bitmap we are subsetting. This value cannot be `null`. |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The x coordinate of the first pixel in source |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The y coordinate of the first pixel in source |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of pixels in each row |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of rows |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#` | A copy of a subset of the source bitmap or the source bitmap itself. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the x, y, width, height values are outside of the dimensions of the source bitmap, or width is \<= 0, or height is \<= 0 |

### createBitmap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBitmap(
    source: Bitmap, 
    x: Int, 
    y: Int, 
    width: Int, 
    height: Int, 
    m: Matrix?, 
    filter: Boolean
): Bitmap
```

Returns a bitmap from subset of the source bitmap, transformed by the optional matrix. The new bitmap may be the same object as source, or a copy may have been made. It is initialized with the same density and color space as the original bitmap. If the source bitmap is immutable and the requested subset is the same as the source bitmap itself, then the source bitmap is returned and no new bitmap is created. The returned bitmap will always be mutable except in the following scenarios: (1) In situations where the source bitmap is returned and the source bitmap is immutable (2) The source bitmap is a hardware bitmap. That is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getConfig()` is equivalent to `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config`

| Parameters ||
|---|---|
| `source` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#): The bitmap we are subsetting. This value cannot be `null`. |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The x coordinate of the first pixel in source |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The y coordinate of the first pixel in source |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of pixels in each row |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of rows |
| `m` | [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix)?: Optional matrix to be applied to the pixels. This value may be `null`. |
| `filter` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the source should be filtered. Only applies if the matrix contains more than just translation. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#` | A bitmap that represents the specified subset of source. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the x, y, width, height values are outside of the dimensions of the source bitmap, or width is \<= 0, or height is \<= 0, or if the source bitmap has already been recycled |

### createBitmap

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBitmap(source: Picture): Bitmap
```

Creates a Bitmap from the given `https://developer.android.com/reference/kotlin/android/graphics/Picture` source of recorded drawing commands. Equivalent to calling `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#createBitmap(android.graphics.Picture,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config)` with width and height the same as the Picture's width and height and a Config.HARDWARE config.

| Parameters ||
|---|---|
| `source` | [Picture](https://developer.android.com/reference/kotlin/android/graphics/Picture): The recorded `https://developer.android.com/reference/kotlin/android/graphics/Picture` of drawing commands that will be drawn into the returned Bitmap. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#` | An immutable bitmap with a HARDWARE config whose contents are created from the recorded drawing commands in the Picture source. This value cannot be `null`. |

### createBitmap

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBitmap(
    source: Picture, 
    width: Int, 
    height: Int, 
    config: Bitmap.Config
): Bitmap
```

Creates a Bitmap from the given `https://developer.android.com/reference/kotlin/android/graphics/Picture` source of recorded drawing commands. The bitmap will be immutable with the given width and height. If the width and height are not the same as the Picture's width \& height, the Picture will be scaled to fit the given width and height.

| Parameters ||
|---|---|
| `source` | [Picture](https://developer.android.com/reference/kotlin/android/graphics/Picture): The recorded `https://developer.android.com/reference/kotlin/android/graphics/Picture` of drawing commands that will be drawn into the returned Bitmap. This value cannot be `null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the bitmap to create. The picture's width will be scaled to match if necessary. |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the bitmap to create. The picture's height will be scaled to match if necessary. |
| `config` | [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config): The `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` of the created bitmap. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#` | An immutable bitmap with a configuration specified by the config parameter. This value cannot be `null`. |

### createBitmap

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBitmap(
    display: DisplayMetrics?, 
    width: Int, 
    height: Int, 
    config: Bitmap.Config
): Bitmap
```

Returns a mutable bitmap with the specified width and height. Its initial density is determined from the given `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`. The newly created bitmap is in the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` color space.

| Parameters ||
|---|---|
| `display` | [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#)?: Display metrics for the display this bitmap will be drawn on. This value may be `null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the bitmap |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the bitmap |
| `config` | [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config): The bitmap config to create. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the width or height are \<= 0, or if Config is Config.HARDWARE, because hardware bitmaps are always immutable |

### createBitmap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBitmap(
    display: DisplayMetrics?, 
    width: Int, 
    height: Int, 
    config: Bitmap.Config, 
    hasAlpha: Boolean
): Bitmap
```

Returns a mutable bitmap with the specified width and height. Its initial density is determined from the given `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`. The newly created bitmap is in the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` color space.

| Parameters ||
|---|---|
| `display` | [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#)?: Display metrics for the display this bitmap will be drawn on. This value may be `null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the bitmap |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the bitmap |
| `config` | [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config): The bitmap config to create. This value cannot be `null`. |
| `hasAlpha` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If the bitmap is ARGB_8888, RGBA_16F, or RGBA_1010102 this flag can be used to mark the bitmap as opaque. Doing so will clear the bitmap in black instead of transparent. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the width or height are \<= 0, or if Config is Config.HARDWARE, because hardware bitmaps are always immutable |

### createBitmap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBitmap(
    display: DisplayMetrics?, 
    width: Int, 
    height: Int, 
    config: Bitmap.Config, 
    hasAlpha: Boolean, 
    colorSpace: ColorSpace
): Bitmap
```

Returns a mutable bitmap with the specified width and height. Its initial density is determined from the given `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`. The newly created bitmap is in the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` color space.

| Parameters ||
|---|---|
| `display` | [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#)?: Display metrics for the display this bitmap will be drawn on. This value may be `null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the bitmap |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the bitmap |
| `config` | [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config): The bitmap config to create. This value cannot be `null`. |
| `hasAlpha` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If the bitmap is ARGB_8888, RGBA_16F, or RGBA_1010102 this flag can be used to mark the bitmap as opaque. Doing so will clear the bitmap in black instead of transparent. |
| `colorSpace` | [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace): The color space of the bitmap. If the config is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` and `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` or `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` is provided then the corresponding extended range variant is assumed. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the width or height are \<= 0, if Config is Config.HARDWARE (because hardware bitmaps are always immutable), if the specified color space is not `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model`, if the specified color space's transfer function is not an `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Rgb.TransferParameters`, or if the color space is null |

### createBitmap

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBitmap(
    display: DisplayMetrics?, 
    colors: IntArray, 
    width: Int, 
    height: Int, 
    config: Bitmap.Config
): Bitmap
```

Returns a immutable bitmap with the specified width and height, with each pixel value set to the corresponding value in the colors array. Its initial density is determined from the given `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`. The newly created bitmap is in the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` color space.

| Parameters ||
|---|---|
| `display` | [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#)?: Display metrics for the display this bitmap will be drawn on. This value may be `null`. |
| `colors` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): Array of sRGB `https://developer.android.com/reference/kotlin/android/graphics/Color` used to initialize the pixels. This array must be at least as large as width \* height. This value cannot be `null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the bitmap |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the bitmap |
| `config` | [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config): The bitmap config to create. If the config does not support per-pixel alpha (e.g. RGB_565), then the alpha bytes in the colors\[\] will be ignored (assumed to be FF). This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the width or height are \<= 0, or if the color array's length is less than the number of pixels. |

### createBitmap

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBitmap(
    display: DisplayMetrics, 
    colors: IntArray, 
    offset: Int, 
    stride: Int, 
    width: Int, 
    height: Int, 
    config: Bitmap.Config
): Bitmap
```

Returns a immutable bitmap with the specified width and height, with each pixel value set to the corresponding value in the colors array. Its initial density is determined from the given `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`. The newly created bitmap is in the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` color space.

| Parameters ||
|---|---|
| `display` | [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#): Display metrics for the display this bitmap will be drawn on. This value cannot be `null`. |
| `colors` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): Array of sRGB `https://developer.android.com/reference/kotlin/android/graphics/Color` used to initialize the pixels. This value cannot be `null`. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of values to skip before the first color in the array of colors. |
| `stride` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of colors in the array between rows (must be \>= width or \<= -width). |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the bitmap |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the bitmap |
| `config` | [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config): The bitmap config to create. If the config does not support per-pixel alpha (e.g. RGB_565), then the alpha bytes in the colors\[\] will be ignored (assumed to be FF). This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the width or height are \<= 0, or if the color array's length is less than the number of pixels. |

### createBitmap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBitmap(
    width: Int, 
    height: Int, 
    config: Bitmap.Config
): Bitmap
```

Returns a mutable bitmap with the specified width and height. Its initial density is as per `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getDensity()`. The newly created bitmap is in the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` color space.

| Parameters ||
|---|---|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the bitmap |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the bitmap |
| `config` | [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config): The bitmap config to create. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the width or height are \<= 0, or if Config is Config.HARDWARE, because hardware bitmaps are always immutable |

### createBitmap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBitmap(
    width: Int, 
    height: Int, 
    config: Bitmap.Config, 
    hasAlpha: Boolean
): Bitmap
```

Returns a mutable bitmap with the specified width and height. Its initial density is as per `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getDensity()`. The newly created bitmap is in the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` color space.

| Parameters ||
|---|---|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the bitmap |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the bitmap |
| `config` | [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config): The bitmap config to create. This value cannot be `null`. |
| `hasAlpha` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If the bitmap is ARGB_8888, RGBA_16F, or RGBA_1010102 this flag can be used to mark the bitmap as opaque. Doing so will clear the bitmap in black instead of transparent. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the width or height are \<= 0, or if Config is Config.HARDWARE, because hardware bitmaps are always immutable |

### createBitmap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBitmap(
    width: Int, 
    height: Int, 
    config: Bitmap.Config, 
    hasAlpha: Boolean, 
    colorSpace: ColorSpace
): Bitmap
```

Returns a mutable bitmap with the specified width and height. Its initial density is as per `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getDensity()`.

| Parameters ||
|---|---|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the bitmap |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the bitmap |
| `config` | [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config): The bitmap config to create. This value cannot be `null`. |
| `hasAlpha` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If the bitmap is ARGB_8888, RGBA_16F, or RGBA_1010102 this flag can be used to mark the bitmap as opaque. Doing so will clear the bitmap in black instead of transparent. |
| `colorSpace` | [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace): The color space of the bitmap. If the config is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` and `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` or `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` is provided then the corresponding extended range variant is assumed. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the width or height are \<= 0, if Config is Config.HARDWARE (because hardware bitmaps are always immutable), if the specified color space is not `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model`, if the specified color space's transfer function is not an `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Rgb.TransferParameters`, or if the color space is null |

### createBitmap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBitmap(
    colors: IntArray, 
    width: Int, 
    height: Int, 
    config: Bitmap.Config!
): Bitmap
```

Returns a immutable bitmap with the specified width and height, with each pixel value set to the corresponding value in the colors array. Its initial density is as per `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getDensity()`. The newly created bitmap is in the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` color space.

| Parameters ||
|---|---|
| `colors` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): Array of sRGB `https://developer.android.com/reference/kotlin/android/graphics/Color` used to initialize the pixels. This array must be at least as large as width \* height. This value cannot be `null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the bitmap |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the bitmap |
| `config` | [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config)!: The bitmap config to create. If the config does not support per-pixel alpha (e.g. RGB_565), then the alpha bytes in the colors\[\] will be ignored (assumed to be FF) |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the width or height are \<= 0, or if the color array's length is less than the number of pixels. |

### createBitmap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBitmap(
    colors: IntArray, 
    offset: Int, 
    stride: Int, 
    width: Int, 
    height: Int, 
    config: Bitmap.Config
): Bitmap
```

Returns a immutable bitmap with the specified width and height, with each pixel value set to the corresponding value in the colors array. Its initial density is as per `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getDensity()`. The newly created bitmap is in the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` color space.

| Parameters ||
|---|---|
| `colors` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): Array of sRGB `https://developer.android.com/reference/kotlin/android/graphics/Color` used to initialize the pixels. This value cannot be `null`. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of values to skip before the first color in the array of colors. |
| `stride` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of colors in the array between rows (must be \>= width or \<= -width). |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the bitmap |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the bitmap |
| `config` | [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config): The bitmap config to create. If the config does not support per-pixel alpha (e.g. RGB_565), then the alpha bytes in the colors\[\] will be ignored (assumed to be FF). This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the width or height are \<= 0, or if the color array's length is less than the number of pixels. |

### createScaledBitmap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createScaledBitmap(
    src: Bitmap, 
    dstWidth: Int, 
    dstHeight: Int, 
    filter: Boolean
): Bitmap
```

Creates a new bitmap, scaled from an existing bitmap, when possible. If the specified width and height are the same as the current width and height of the source bitmap, the source bitmap is returned and no new bitmap is created.

| Parameters ||
|---|---|
| `src` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#): The source bitmap. This value cannot be `null`. |
| `dstWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new bitmap's desired width. |
| `dstHeight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new bitmap's desired height. |
| `filter` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether or not bilinear filtering should be used when scaling the bitmap. If this is true then bilinear filtering will be used when scaling which has better image quality at the cost of worse performance. If this is false then nearest-neighbor scaling is used instead which will have worse image quality but is faster. Recommended default is to set filter to 'true' as the cost of bilinear filtering is typically minimal and the improved image quality is significant. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#` | The new scaled bitmap or the source bitmap if no scaling is required. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if width is \<= 0, or height is \<= 0 |

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

No special parcel contents.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### eraseColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun eraseColor(c: Int): Unit
```

Fills the bitmap's pixels with the specified `https://developer.android.com/reference/kotlin/android/graphics/Color`.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the bitmap is not mutable. |

### eraseColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun eraseColor(color: Long): Unit
```

Fills the bitmap's pixels with the specified `ColorLong`.

| Parameters ||
|---|---|
| `color` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The color to fill as packed by the `https://developer.android.com/reference/kotlin/android/graphics/Color` class. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the color space encoded in the `ColorLong` is invalid or unknown. |
| `java.lang.IllegalStateException` | if the bitmap is not mutable. |

### extractAlpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun extractAlpha(): Bitmap
```

Returns a new bitmap that captures the alpha values of the original. This may be drawn with Canvas.drawBitmap(), where the color(s) will be taken from the paint that is passed to the draw call.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#` | new bitmap containing the alpha channel of the original bitmap. This value cannot be `null`. |

### extractAlpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun extractAlpha(
    paint: Paint?, 
    offsetXY: IntArray!
): Bitmap
```

Returns a new bitmap that captures the alpha values of the original. These values may be affected by the optional Paint parameter, which can contain its own alpha, and may also contain a MaskFilter which could change the actual dimensions of the resulting bitmap (e.g. a blur maskfilter might enlarge the resulting bitmap). If offsetXY is not null, it returns the amount to offset the returned bitmap so that it will logically align with the original. For example, if the paint contains a blur of radius 2, then offsetXY\[\] would contains -2, -2, so that drawing the alpha bitmap offset by (-2, -2) and then drawing the original would result in the blur visually aligning with the original.

The initial density of the returned bitmap is the same as the original's.

| Parameters ||
|---|---|
| `paint` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)?: Optional paint used to modify the alpha values in the resulting bitmap. Pass null for default behavior. |
| `offsetXY` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: Optional array that returns the X (index 0) and Y (index 1) offset needed to position the returned bitmap so that it visually lines up with the original. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#` | new bitmap containing the (optionally modified by paint) alpha channel of the original bitmap. This may be drawn with Canvas.drawBitmap(), where the color(s) will be taken from the paint that is passed to the draw call. |

### getAllocationByteCount

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAllocationByteCount(): Int
```

Returns the size of the allocated memory used to store this bitmap's pixels.

This can be larger than the result of `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getByteCount()` if a bitmap is reused to decode other bitmaps of smaller size, or by manual reconfiguration. See `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#reconfigure(kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config)`, `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setWidth(kotlin.Int)`, `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setHeight(kotlin.Int)`, `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setConfig(android.graphics.Bitmap.Config)`, and `https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options#inBitmap:android.graphics.Bitmap`. If a bitmap is not modified in this way, this value will be the same as that returned by `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getByteCount()`.

This value will not change over the lifetime of a Bitmap.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#reconfigure(kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config)`

### getByteCount

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getByteCount(): Int
```

Returns the minimum number of bytes that can be used to store this bitmap's pixels.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int`, the result of this method can no longer be used to determine memory usage of a bitmap. See `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getAllocationByteCount()`.

### getColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getColor(
    x: Int, 
    y: Int
): Color
```

Returns the `https://developer.android.com/reference/kotlin/android/graphics/Color` at the specified location. Throws an exception if x or y are out of bounds (negative or \>= to the width or height respectively).

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The x coordinate (0...width-1) of the pixel to return |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The y coordinate (0...height-1) of the pixel to return |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Color` | The `https://developer.android.com/reference/kotlin/android/graphics/Color` at the specified coordinate. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if x, y exceed the bitmap's bounds |
| `java.lang.IllegalStateException` | if the bitmap's config is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` |

### getColorSpace

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getColorSpace(): ColorSpace?
```

Returns the color space associated with this bitmap. If the color space is unknown, this method returns null.

### getConfig

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConfig(): Bitmap.Config?
```

If the bitmap's internal config is in one of the public formats, return that config, otherwise return null.

### getDensity

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDensity(): Int
```

Returns the density for this bitmap.

The default density is the same density as the current display, unless the current application does not support different screen densities in which case it is `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#DENSITY_DEFAULT:kotlin.Int`. Note that compatibility mode is determined by the application that was initially loaded into a process -- applications that share the same process should all have the same compatibility, or ensure they explicitly set the density of their bitmaps appropriately.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A scaling factor of the default density or `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#DENSITY_NONE:kotlin.Int` if the scaling factor is unknown. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setDensity(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#DENSITY_DEFAULT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#densityDpi:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#DENSITY_NONE:kotlin.Int`

### getGainmap

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getGainmap(): Gainmap?
```

Returns the gainmap or null if the bitmap doesn't contain a gainmap

### getGenerationId

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getGenerationId(): Int
```

Returns the generation ID of this bitmap. The generation ID changes whenever the bitmap is modified. This can be used as an efficient way to check if a bitmap has changed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The current generation ID for this bitmap. |

### getHardwareBuffer

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHardwareBuffer(): HardwareBuffer
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#` | `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#` which is internally used by hardware bitmap Note: the HardwareBuffer does \*not\* have an associated `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace`. To render this object the same as its rendered with this Bitmap, you should also call `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getColorSpace()`. <br /> Must not be modified while a wrapped Bitmap is accessing it. Doing so will result in undefined behavior. <br /> . This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the bitmap's config is not `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` or if the bitmap has been recycled. |

### getHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHeight(): Int
```

Returns the bitmap's height

### getNinePatchChunk

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNinePatchChunk(): ByteArray?
```

Returns an optional array of private data, used by the UI system for some bitmaps. Not intended to be called by applications.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | This value may be `null`. |

### getPixel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPixel(
    x: Int, 
    y: Int
): Int
```

Returns the `https://developer.android.com/reference/kotlin/android/graphics/Color` at the specified location. Throws an exception if x or y are out of bounds (negative or \>= to the width or height respectively). The returned color is a non-premultiplied ARGB value in the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` color space.

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The x coordinate (0...width-1) of the pixel to return |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The y coordinate (0...height-1) of the pixel to return |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The argb `https://developer.android.com/reference/kotlin/android/graphics/Color` at the specified coordinate |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if x, y exceed the bitmap's bounds |
| `java.lang.IllegalStateException` | if the bitmap's config is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` |

### getPixels

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPixels(
    pixels: IntArray, 
    offset: Int, 
    stride: Int, 
    x: Int, 
    y: Int, 
    width: Int, 
    height: Int
): Unit
```

Returns in pixels\[\] a copy of the data in the bitmap. Each value is a packed int representing a `https://developer.android.com/reference/kotlin/android/graphics/Color`. The stride parameter allows the caller to allow for gaps in the returned pixels array between rows. For normal packed results, just pass width for the stride value. The returned colors are non-premultiplied ARGB values in the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` color space.

| Parameters ||
|---|---|
| `pixels` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): The array to receive the bitmap's colors. This value cannot be `null`. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The first index to write into pixels\[\] |
| `stride` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of entries in pixels\[\] to skip between rows (must be \>= bitmap's width). Can be negative. |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The x coordinate of the first pixel to read from the bitmap |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The y coordinate of the first pixel to read from the bitmap |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of pixels to read from each row |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of rows to read |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if the pixels array is too small to receive the specified number of pixels. |
| `java.lang.IllegalArgumentException` | if x, y, width, height exceed the bounds of the bitmap, or if abs(stride) \< width. |
| `java.lang.IllegalStateException` | if the bitmap's config is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` |

### getRowBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRowBytes(): Int
```

Return the number of bytes between rows in the bitmap's pixels. Note that this refers to the pixels as stored natively by the bitmap. If you call getPixels() or setPixels(), then the pixels are uniformly treated as 32bit values, packed according to the Color class.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int`, this method should not be used to calculate the memory usage of the bitmap. Instead, see `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getAllocationByteCount()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | number of bytes between rows of the native bitmap pixels. |

### getScaledHeight

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScaledHeight(canvas: Canvas): Int
```

Convenience for calling `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getScaledHeight(kotlin.Int)` with the target density of the given `https://developer.android.com/reference/kotlin/android/graphics/Canvas`.

| Parameters ||
|---|---|
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas): This value cannot be `null`. |

### getScaledHeight

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScaledHeight(metrics: DisplayMetrics): Int
```

Convenience for calling `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getScaledHeight(kotlin.Int)` with the target density of the given `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`.

| Parameters ||
|---|---|
| `metrics` | [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#): This value cannot be `null`. |

### getScaledHeight

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScaledHeight(targetDensity: Int): Int
```

Convenience method that returns the height of this bitmap divided by the density scale factor. Returns the bitmap's height multiplied by the ratio of the target density to the bitmap's source density

| Parameters ||
|---|---|
| `targetDensity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The density of the target canvas of the bitmap. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The scaled height of this bitmap, according to the density scale factor. |

### getScaledWidth

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScaledWidth(canvas: Canvas): Int
```

Convenience for calling `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getScaledWidth(kotlin.Int)` with the target density of the given `https://developer.android.com/reference/kotlin/android/graphics/Canvas`.

| Parameters ||
|---|---|
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas): This value cannot be `null`. |

### getScaledWidth

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScaledWidth(metrics: DisplayMetrics): Int
```

Convenience for calling `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getScaledWidth(kotlin.Int)` with the target density of the given `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`.

| Parameters ||
|---|---|
| `metrics` | [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#): This value cannot be `null`. |

### getScaledWidth

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScaledWidth(targetDensity: Int): Int
```

Convenience method that returns the width of this bitmap divided by the density scale factor. Returns the bitmap's width multiplied by the ratio of the target density to the bitmap's source density

| Parameters ||
|---|---|
| `targetDensity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The density of the target canvas of the bitmap. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The scaled width of this bitmap, according to the density scale factor. |

### getWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getWidth(): Int
```

Returns the bitmap's width

### hasAlpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasAlpha(): Boolean
```

Returns true if the bitmap's config supports per-pixel alpha, and if the pixels may contain non-opaque alpha values. For some configs, this is always false (e.g. RGB_565), since they do not support per-pixel alpha. However, for configs that do, the bitmap may be flagged to be known that all of its pixels are opaque. In this case hasAlpha() will also return false. If a config such as ARGB_8888 is not so flagged, it will return true by default.

### hasGainmap

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasGainmap(): Boolean
```

Returns whether or not this Bitmap contains a Gainmap.

### hasMipMap

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasMipMap(): Boolean
```

Indicates whether the renderer responsible for drawing this bitmap should attempt to use mipmaps when this bitmap is drawn scaled down. If you know that you are going to draw this bitmap at less than 50% of its original size, you may be able to obtain a higher quality This property is only a suggestion that can be ignored by the renderer. It is not guaranteed to have any effect.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the renderer should attempt to use mipmaps, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setHasMipMap(kotlin.Boolean)`

### isMutable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isMutable(): Boolean
```

Returns true if the bitmap is marked as mutable (i.e. can be drawn into)

### isPremultiplied

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isPremultiplied(): Boolean
```

Indicates whether pixels stored in this bitmaps are stored pre-multiplied. When a pixel is pre-multiplied, the RGB components have been multiplied by the alpha component. For instance, if the original color is a 50% translucent red `(128, 255, 0, 0)`, the pre-multiplied form is `(128, 128, 0, 0)`.

This method always returns false if `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getConfig()` is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config`.

The return value is undefined if `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getConfig()` is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config`.

This method only returns true if `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#hasAlpha()` returns true. A bitmap with no alpha channel can be used both as a pre-multiplied and as a non pre-multiplied bitmap.

Only pre-multiplied bitmaps may be drawn by the view system or `https://developer.android.com/reference/kotlin/android/graphics/Canvas`. If a non-pre-multiplied bitmap with an alpha channel is drawn to a Canvas, a RuntimeException will be thrown.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the underlying pixels have been pre-multiplied, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setPremultiplied(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options#inPremultiplied:kotlin.Boolean`

### isRecycled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isRecycled(): Boolean
```

Returns true if this bitmap has been recycled. If so, then it is an error to try to access its pixels, and the bitmap will not draw.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the bitmap has been recycled |

### prepareToDraw

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun prepareToDraw(): Unit
```

Builds caches associated with the bitmap that are used for drawing it.

Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int`, this call initiates an asynchronous upload to the GPU on RenderThread, if the Bitmap is not already uploaded. With Hardware Acceleration, Bitmaps must be uploaded to the GPU in order to be rendered. This is done by default the first time a Bitmap is drawn, but the process can take several milliseconds, depending on the size of the Bitmap. Each time a Bitmap is modified and drawn again, it must be re-uploaded.

Calling this method in advance can save time in the first frame it's used. For example, it is recommended to call this on an image decoding worker thread when a decoded Bitmap is about to be displayed. It is recommended to make any pre-draw modifications to the Bitmap before calling this method, so the cached, uploaded copy may be reused without re-uploading.
In `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int` and below, for purgeable bitmaps, this call would attempt to ensure that the pixels have been decoded.

### reconfigure

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun reconfigure(
    width: Int, 
    height: Int, 
    config: Bitmap.Config
): Unit
```

Modifies the bitmap to have a specified width, height, and `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config`, without affecting the underlying allocation backing the bitmap. Bitmap pixel data is not re-initialized for the new configuration.

This method can be used to avoid allocating a new bitmap, instead reusing an existing bitmap's allocation for a new configuration of equal or lesser size. If the Bitmap's allocation isn't large enough to support the new configuration, an IllegalArgumentException will be thrown and the bitmap will not be modified.

The result of `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getByteCount()` will reflect the new configuration, while `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getAllocationByteCount()` will reflect that of the initial configuration.

Note: This may change this result of hasAlpha(). When converting to 565, the new bitmap will always be considered opaque. When converting from 565, the new bitmap will be considered non-opaque, and will respect the value set by setPremultiplied().

WARNING: This method should NOT be called on a bitmap currently in use by the view system, Canvas, or the AndroidBitmap NDK API. It does not make guarantees about how the underlying pixel buffer is remapped to the new config, just that the allocation is reused. Additionally, the view system does not account for bitmap properties being modifying during use, e.g. while attached to drawables.

In order to safely ensure that a Bitmap is no longer in use by the View system it is necessary to wait for a draw pass to occur after invalidate()'ing any view that had previously drawn the Bitmap in the last draw pass due to hardware acceleration's caching of draw commands. As an example, here is how this can be done for an ImageView:

```kotlin
ImageView myImageView = ...;
       final Bitmap myBitmap = ...;
       myImageView.setImageDrawable(null);
       myImageView.post(new Runnable() {
           public void run() {
               // myBitmap is now no longer in use by the ImageView
               // and can be safely reconfigured.
               myBitmap.reconfigure(...);
           }
       });
  
```

<br />

| Parameters ||
|---|---|
| `config` | [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config): This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setWidth(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setHeight(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setConfig(android.graphics.Bitmap.Config)`

### recycle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun recycle(): Unit
```

Immediately releases the pixel data associated with this Bitmap.

Call this method to release a Bitmap that is certainly no longer needed, such as with a Bitmap that was created as an intermediate buffer in a transformation. Calling this method will release the pixel memory immediately, rather than wait for a future Garbage Collection.

Avoid calling this method on Bitmaps that were used in a View or that may be referenced elsewhere, as it may be unsafe.

After calling this method, any subsequent attempt to access the bitmap's pixel data (e.g., using `getPixels()` or `setPixels()`) will throw an exception, and the bitmap will draw nothing. This operation cannot be reversed.

### sameAs

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sameAs(other: Bitmap?): Boolean
```

Given another bitmap, return true if it has the same dimensions, config, and pixel data as this bitmap. If any of those differ, return false. If other is null, return false. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `other` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap#)?: This value may be `null`. |

### setColorSpace

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setColorSpace(colorSpace: ColorSpace): Unit
```

Modifies the bitmap to have the specified `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace`, without affecting the underlying allocation backing the bitmap.

This affects how the framework will interpret the color at each pixel. A bitmap with `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` never has a color space, since a color space does not affect the alpha channel. Other `Config`s must always have a non-null `ColorSpace`.

| Parameters ||
|---|---|
| `colorSpace` | [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace): to assign to the bitmap. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the `Config` (returned by `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getConfig()`) is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config`. |

### setConfig

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setConfig(config: Bitmap.Config): Unit
```

Convenience method for calling `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#reconfigure(kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config)` with the current height and width.

WARNING: this method should not be used on bitmaps currently used by the view system, see `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#reconfigure(kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config)` for more details.

| Parameters ||
|---|---|
| `config` | [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config): This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#reconfigure(kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config)`
- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setWidth(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setHeight(kotlin.Int)`

### setDensity

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setDensity(density: Int): Unit
```

Specifies the density for this bitmap. When the bitmap is drawn to a Canvas that also has a density, it will be scaled appropriately.

| Parameters ||
|---|---|
| `density` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The density scaling factor to use with this bitmap or `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#DENSITY_NONE:kotlin.Int` if the density is unknown. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getDensity()`
- `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#DENSITY_DEFAULT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#densityDpi:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#DENSITY_NONE:kotlin.Int`

### setGainmap

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setGainmap(gainmap: Gainmap?): Unit
```

Sets a gainmap on this bitmap, or removes the gainmap if null

| Parameters ||
|---|---|
| `gainmap` | [Gainmap](https://developer.android.com/reference/kotlin/android/graphics/Gainmap)?: This value may be `null`. |

### setHasAlpha

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setHasAlpha(hasAlpha: Boolean): Unit
```

Tell the bitmap if all of the pixels are known to be opaque (false) or if some of the pixels may contain non-opaque alpha values (true). Note, for some configs (e.g. RGB_565) this call is ignored, since it does not support per-pixel alpha values. This is meant as a drawing hint, as in some cases a bitmap that is known to be opaque can take a faster drawing case than one that may have non-opaque per-pixel alpha values.

### setHasMipMap

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setHasMipMap(hasMipMap: Boolean): Unit
```

Set a hint for the renderer responsible for drawing this bitmap indicating that it should attempt to use mipmaps when this bitmap is drawn scaled down. If you know that you are going to draw this bitmap at less than 50% of its original size, you may be able to obtain a higher quality by turning this property on. Note that if the renderer respects this hint it might have to allocate extra memory to hold the mipmap levels for this bitmap. This property is only a suggestion that can be ignored by the renderer. It is not guaranteed to have any effect.

| Parameters ||
|---|---|
| `hasMipMap` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): indicates whether the renderer should attempt to use mipmaps |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#hasMipMap()`

### setHeight

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setHeight(height: Int): Unit
```

Convenience method for calling `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#reconfigure(kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config)` with the current width and config.

WARNING: this method should not be used on bitmaps currently used by the view system, see `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#reconfigure(kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config)` for more details.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#reconfigure(kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config)`
- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setWidth(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setConfig(android.graphics.Bitmap.Config)`

### setPixel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPixel(
    x: Int, 
    y: Int, 
    color: Int
): Unit
```

Write the specified `https://developer.android.com/reference/kotlin/android/graphics/Color` into the bitmap (assuming it is mutable) at the x,y coordinate. The color must be a non-premultiplied ARGB value in the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` color space.

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The x coordinate of the pixel to replace (0...width-1) |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The y coordinate of the pixel to replace (0...height-1) |
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The ARGB color to write into the bitmap |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if x, y are outside of the bitmap's bounds. |
| `java.lang.IllegalStateException` | if the bitmap is not mutable |

### setPixels

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPixels(
    pixels: IntArray, 
    offset: Int, 
    stride: Int, 
    x: Int, 
    y: Int, 
    width: Int, 
    height: Int
): Unit
```

Replace pixels in the bitmap with the colors in the array. Each element in the array is a packed int representing a non-premultiplied ARGB `https://developer.android.com/reference/kotlin/android/graphics/Color` in the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` color space.

| Parameters ||
|---|---|
| `pixels` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): The colors to write to the bitmap. This value cannot be `null`. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the first color to read from pixels\[\] |
| `stride` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of colors in pixels\[\] to skip between rows. Normally this value will be the same as the width of the bitmap, but it can be larger (or negative). |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The x coordinate of the first pixel to write to in the bitmap. |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The y coordinate of the first pixel to write to in the bitmap. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of colors to copy from pixels\[\] per row |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of rows to write to the bitmap |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if the pixels array is too small to receive the specified number of pixels. |
| `java.lang.IllegalArgumentException` | if x, y, width, height are outside of the bitmap's bounds. |
| `java.lang.IllegalStateException` | if the bitmap is not mutable |

### setPremultiplied

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPremultiplied(premultiplied: Boolean): Unit
```

Sets whether the bitmap should treat its data as pre-multiplied.

Bitmaps are always treated as pre-multiplied by the view system and `https://developer.android.com/reference/kotlin/android/graphics/Canvas` for performance reasons. Storing un-pre-multiplied data in a Bitmap (through `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setPixel(kotlin.Int,%20kotlin.Int,%20kotlin.Int)`, `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setPixels(kotlin.IntArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`, or `https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options#inPremultiplied:kotlin.Boolean`) can lead to incorrect blending if drawn by the framework.

This method will not affect the behavior of a bitmap without an alpha channel, or if `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#hasAlpha()` returns false.

Calling #createBitmap or `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#createScaledBitmap(android.graphics.Bitmap,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean)` with a source Bitmap whose colors are not pre-multiplied may result in a RuntimeException, since those functions require drawing the source, which is not supported for un-pre-multiplied Bitmaps.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#isPremultiplied()`
- `https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options#inPremultiplied:kotlin.Boolean`

### setWidth

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setWidth(width: Int): Unit
```

Convenience method for calling `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#reconfigure(kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config)` with the current height and config.

WARNING: this method should not be used on bitmaps currently used by the view system, see `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#reconfigure(kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config)` for more details.
**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#reconfigure(kotlin.Int,%20kotlin.Int,%20android.graphics.Bitmap.Config)`
- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setHeight(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#setConfig(android.graphics.Bitmap.Config)`

### wrapHardwareBuffer

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun wrapHardwareBuffer(
    hardwareBuffer: HardwareBuffer, 
    colorSpace: ColorSpace?
): Bitmap?
```

Create a hardware bitmap backed by a `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#`.

The passed HardwareBuffer's usage flags must contain `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_SAMPLED_IMAGE:kotlin.Long`.

The bitmap will keep a reference to the buffer so that callers can safely close the HardwareBuffer without affecting the Bitmap. However the HardwareBuffer must not be modified while a wrapped Bitmap is accessing it. Doing so will result in undefined behavior.

| Parameters ||
|---|---|
| `hardwareBuffer` | [HardwareBuffer](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#): The HardwareBuffer to wrap. This value cannot be `null`. |
| `colorSpace` | [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace)?: The color space of the bitmap. Must be a `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Rgb` colorspace. If null, SRGB is assumed. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#?` | A bitmap wrapping the buffer, or null if there was a problem creating the bitmap. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the HardwareBuffer has an invalid usage, or an invalid colorspace is given. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    p: Parcel, 
    flags: Int
): Unit
```

Write the bitmap and its pixels to the parcel. The bitmap can be rebuilt from the parcel by calling CREATOR.createFromParcel(). If this bitmap is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config`, it may be unparceled with a different pixel format (e.g. 565, 8888), but the content will be preserved to the best quality permitted by the final pixel format

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |
| `p` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): Parcel object to write the bitmap data into. This value cannot be `null`. |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<Bitmap!>
```
