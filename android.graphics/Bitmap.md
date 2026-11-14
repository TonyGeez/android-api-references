Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Bitmap

```
class Bitmap : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.Bitmap](Bitmap.md) |

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
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Bitmap](Bitmap.md) | asShared Return an immutable bitmap backed by shared memory which can be efficiently passed between processes via Parcelable. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | compress Write a compressed version of the bitmap to the specified outputstream. |
| [Bitmap](Bitmap.md)! | copy Tries to make a new bitmap based on the dimensions of this bitmap, setting the new bitmap's config to the one specified, and then copying this bitmap's pixels into the new bitmap. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copyPixelsFromBuffer Copy the pixels from the buffer, beginning at the current position, overwriting the bitmap's pixels. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copyPixelsToBuffer Copy the bitmap's pixels into the specified buffer (allocated by the caller). |
| static [Bitmap](Bitmap.md) | createBitmap Returns a bitmap from the source bitmap. |
| --- | --- |
| static [Bitmap](Bitmap.md) | createBitmap Returns a bitmap from the specified subset of the source bitmap. |
| static [Bitmap](Bitmap.md) | createBitmap Returns a bitmap from subset of the source bitmap, transformed by the optional matrix. |
| static [Bitmap](Bitmap.md) | createBitmap Creates a Bitmap from the given Picture source of recorded drawing commands. |
| --- | --- |
| static [Bitmap](Bitmap.md) | createBitmap Creates a Bitmap from the given Picture source of recorded drawing commands. |
| static [Bitmap](Bitmap.md) | createBitmap Returns a mutable bitmap with the specified width and height. |
| static [Bitmap](Bitmap.md) | createBitmap Returns a mutable bitmap with the specified width and height. |
| --- | --- |
| static [Bitmap](Bitmap.md) | createBitmap Returns a mutable bitmap with the specified width and height. |
| static [Bitmap](Bitmap.md) | createBitmap Returns a immutable bitmap with the specified width and height, with each pixel value set to the corresponding value in the colors array. |
| static [Bitmap](Bitmap.md) | createBitmap Returns a immutable bitmap with the specified width and height, with each pixel value set to the corresponding value in the colors array. |
| --- | --- |
| static [Bitmap](Bitmap.md) | createBitmap Returns a mutable bitmap with the specified width and height. |
| static [Bitmap](Bitmap.md) | createBitmap Returns a mutable bitmap with the specified width and height. |
| static [Bitmap](Bitmap.md) | createBitmap Returns a mutable bitmap with the specified width and height. |
| --- | --- |
| static [Bitmap](Bitmap.md) | createBitmap Returns a immutable bitmap with the specified width and height, with each pixel value set to the corresponding value in the colors array. |
| static [Bitmap](Bitmap.md) | createBitmap Returns a immutable bitmap with the specified width and height, with each pixel value set to the corresponding value in the colors array. |
| static [Bitmap](Bitmap.md) | createScaledBitmap Creates a new bitmap, scaled from an existing bitmap, when possible. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents No special parcel contents. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | eraseColor Fills the bitmap's pixels with the specified Color. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | eraseColor Fills the bitmap's pixels with the specified `ColorLong`. |
| --- | --- |
| [Bitmap](Bitmap.md) | extractAlpha Returns a new bitmap that captures the alpha values of the original. |
| [Bitmap](Bitmap.md) | extractAlpha Returns a new bitmap that captures the alpha values of the original. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getAllocationByteCount Returns the size of the allocated memory used to store this bitmap's pixels. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getByteCount Returns the minimum number of bytes that can be used to store this bitmap's pixels. |
| [Color](Color.md) | getColor Returns the Color at the specified location. |
| [ColorSpace](ColorSpace.md)? | getColorSpace Returns the color space associated with this bitmap. |
| --- | --- |
| [Bitmap.Config](../android/graphics/Bitmap.Config.md)? | getConfig If the bitmap's internal config is in one of the public formats, return that config, otherwise return null. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDensity Returns the density for this bitmap. |
| [Gainmap](Gainmap.md)? | getGainmap Returns the gainmap or null if the bitmap doesn't contain a gainmap |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getGenerationId Returns the generation ID of this bitmap. |
| [HardwareBuffer](../android.hardware/HardwareBuffer.md) | getHardwareBuffer <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getHeight Returns the bitmap's height |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | getNinePatchChunk Returns an optional array of private data, used by the UI system for some bitmaps. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPixel Returns the Color at the specified location. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getPixels Returns in pixels\[\] a copy of the data in the bitmap. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getRowBytes Return the number of bytes between rows in the bitmap's pixels. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getScaledHeight Convenience for calling getScaledHeight with the target density of the given Canvas. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getScaledHeight Convenience for calling getScaledHeight with the target density of the given `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getScaledHeight Convenience method that returns the height of this bitmap divided by the density scale factor. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getScaledWidth Convenience for calling getScaledWidth with the target density of the given Canvas. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getScaledWidth Convenience for calling getScaledWidth with the target density of the given `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getScaledWidth Convenience method that returns the width of this bitmap divided by the density scale factor. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getWidth Returns the bitmap's width |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasAlpha Returns true if the bitmap's config supports per-pixel alpha, and if the pixels may contain non-opaque alpha values. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasGainmap Returns whether or not this Bitmap contains a Gainmap. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasMipMap Indicates whether the renderer responsible for drawing this bitmap should attempt to use mipmaps when this bitmap is drawn scaled down. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isMutable Returns true if the bitmap is marked as mutable (i.e. can be drawn into) |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isPremultiplied Indicates whether pixels stored in this bitmaps are stored pre-multiplied. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isRecycled Returns true if this bitmap has been recycled. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | prepareToDraw Builds caches associated with the bitmap that are used for drawing it. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | reconfigure Modifies the bitmap to have a specified width, height, and `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config`, without affecting the underlying allocation backing the bitmap. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | recycle Immediately releases the pixel data associated with this Bitmap. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | sameAs Given another bitmap, return true if it has the same dimensions, config, and pixel data as this bitmap. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setColorSpace Modifies the bitmap to have the specified ColorSpace, without affecting the underlying allocation backing the bitmap. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setConfig Convenience method for calling reconfigure with the current height and width. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setDensity Specifies the density for this bitmap. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setGainmap Sets a gainmap on this bitmap, or removes the gainmap if null |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setHasAlpha Tell the bitmap if all of the pixels are known to be opaque (false) or if some of the pixels may contain non-opaque alpha values (true). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setHasMipMap Set a hint for the renderer responsible for drawing this bitmap indicating that it should attempt to use mipmaps when this bitmap is drawn scaled down. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setHeight Convenience method for calling reconfigure with the current width and config. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPixel Write the specified Color into the bitmap (assuming it is mutable) at the x,y coordinate. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPixels Replace pixels in the bitmap with the colors in the array. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPremultiplied Sets whether the bitmap should treat its data as pre-multiplied. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setWidth Convenience method for calling reconfigure with the current height and config. |
| static [Bitmap](Bitmap.md)? | wrapHardwareBuffer Create a hardware bitmap backed by a `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Write the bitmap and its pixels to the parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Bitmap](Bitmap.md)!\> | `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### DENSITY_NONE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DENSITY_NONE: Int
```

Indicates that the bitmap was created for an unknown pixel density.

 Value: 0

**See Also**

- getDensity
- setDensity

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
| Bitmap | This value cannot be `null`. |

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
| `format` | [Bitmap.CompressFormat](../android/graphics/Bitmap.CompressFormat.md): The format of the compressed image. This value cannot be `null`. |
| `quality` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Hint to the compressor, 0-100. The value is interpreted differently depending on the `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.CompressFormat`. |
| `stream` | [OutputStream](../java.io/OutputStream.md): The outputstream to write the compressed data. This value cannot be `null`. |
| --- | --- |

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
| `config` | [Bitmap.Config](../android/graphics/Bitmap.Config.md): The desired config for the resulting bitmap. This value cannot be `null`. |
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
| `src` | [Buffer](../java.nio/Buffer.md): This value cannot be `null`. |

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

The content of the bitmap is copied into the buffer as-is. This means that if this bitmap stores its pixels pre-multiplied (see isPremultiplied, the values in the buffer will also be pre-multiplied. The pixels remain in the color space of the bitmap.

After this method returns, the current position of the buffer is updated: the position is incremented by the number of elements written in the buffer.

| Parameters ||
|---|---|
| `dst` | [Buffer](../java.nio/Buffer.md): This value cannot be `null`. |

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
| `src` | [Bitmap](Bitmap.md): This value cannot be `null`. |

| Return ||
|---|---|
| Bitmap | This value cannot be `null`. |

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
| `source` | [Bitmap](Bitmap.md): The bitmap we are subsetting. This value cannot be `null`. |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The x coordinate of the first pixel in source |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The y coordinate of the first pixel in source |
| --- | --- |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of pixels in each row |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of rows |

| Return ||
|---|---|
| Bitmap | A copy of a subset of the source bitmap or the source bitmap itself. This value cannot be `null`. |

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

Returns a bitmap from subset of the source bitmap, transformed by the optional matrix. The new bitmap may be the same object as source, or a copy may have been made. It is initialized with the same density and color space as the original bitmap. If the source bitmap is immutable and the requested subset is the same as the source bitmap itself, then the source bitmap is returned and no new bitmap is created. The returned bitmap will always be mutable except in the following scenarios: (1) In situations where the source bitmap is returned and the source bitmap is immutable (2) The source bitmap is a hardware bitmap. That is getConfig is equivalent to `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config`

| Parameters ||
|---|---|
| `source` | [Bitmap](Bitmap.md): The bitmap we are subsetting. This value cannot be `null`. |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The x coordinate of the first pixel in source |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The y coordinate of the first pixel in source |
| --- | --- |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of pixels in each row |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of rows |
| `m` | [Matrix](Matrix.md)?: Optional matrix to be applied to the pixels. This value may be `null`. |
| --- | --- |
| `filter` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the source should be filtered. Only applies if the matrix contains more than just translation. |

| Return ||
|---|---|
| Bitmap | A bitmap that represents the specified subset of source. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the x, y, width, height values are outside of the dimensions of the source bitmap, or width is \<= 0, or height is \<= 0, or if the source bitmap has already been recycled |

### createBitmap

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createBitmap(source: Picture): Bitmap
```

Creates a Bitmap from the given Picture source of recorded drawing commands. Equivalent to calling createBitmap with width and height the same as the Picture's width and height and a Config.HARDWARE config.

| Parameters ||
|---|---|
| `source` | [Picture](Picture.md): The recorded Picture of drawing commands that will be drawn into the returned Bitmap. This value cannot be `null`. |

| Return ||
|---|---|
| Bitmap | An immutable bitmap with a HARDWARE config whose contents are created from the recorded drawing commands in the Picture source. This value cannot be `null`. |

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

Creates a Bitmap from the given Picture source of recorded drawing commands. The bitmap will be immutable with the given width and height. If the width and height are not the same as the Picture's width \& height, the Picture will be scaled to fit the given width and height.

| Parameters ||
|---|---|
| `source` | [Picture](Picture.md): The recorded Picture of drawing commands that will be drawn into the returned Bitmap. This value cannot be `null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the bitmap to create. The picture's width will be scaled to match if necessary. |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the bitmap to create. The picture's height will be scaled to match if necessary. |
| --- | --- |
| `config` | [Bitmap.Config](../android/graphics/Bitmap.Config.md): The `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` of the created bitmap. This value cannot be `null`. |

| Return ||
|---|---|
| Bitmap | An immutable bitmap with a configuration specified by the config parameter. This value cannot be `null`. |

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
| `display` | [DisplayMetrics](../android.util/DisplayMetrics.md)?: Display metrics for the display this bitmap will be drawn on. This value may be `null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the bitmap |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the bitmap |
| --- | --- |
| `config` | [Bitmap.Config](../android/graphics/Bitmap.Config.md): The bitmap config to create. This value cannot be `null`. |

| Return ||
|---|---|
| Bitmap | This value cannot be `null`. |

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
| `display` | [DisplayMetrics](../android.util/DisplayMetrics.md)?: Display metrics for the display this bitmap will be drawn on. This value may be `null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the bitmap |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the bitmap |
| --- | --- |
| `config` | [Bitmap.Config](../android/graphics/Bitmap.Config.md): The bitmap config to create. This value cannot be `null`. |
| `hasAlpha` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If the bitmap is ARGB_8888, RGBA_16F, or RGBA_1010102 this flag can be used to mark the bitmap as opaque. Doing so will clear the bitmap in black instead of transparent. |

| Return ||
|---|---|
| Bitmap | This value cannot be `null`. |

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
| `display` | [DisplayMetrics](../android.util/DisplayMetrics.md)?: Display metrics for the display this bitmap will be drawn on. This value may be `null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the bitmap |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the bitmap |
| --- | --- |
| `config` | [Bitmap.Config](../android/graphics/Bitmap.Config.md): The bitmap config to create. This value cannot be `null`. |
| `hasAlpha` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If the bitmap is ARGB_8888, RGBA_16F, or RGBA_1010102 this flag can be used to mark the bitmap as opaque. Doing so will clear the bitmap in black instead of transparent. |
| `colorSpace` | [ColorSpace](ColorSpace.md): The color space of the bitmap. If the config is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` and `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` or `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` is provided then the corresponding extended range variant is assumed. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| Bitmap | This value cannot be `null`. |

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
| `display` | [DisplayMetrics](../android.util/DisplayMetrics.md)?: Display metrics for the display this bitmap will be drawn on. This value may be `null`. |
| `colors` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): Array of sRGB Color used to initialize the pixels. This array must be at least as large as width \* height. This value cannot be `null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the bitmap |
| --- | --- |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the bitmap |
| `config` | [Bitmap.Config](../android/graphics/Bitmap.Config.md): The bitmap config to create. If the config does not support per-pixel alpha (e.g. RGB_565), then the alpha bytes in the colors\[\] will be ignored (assumed to be FF). This value cannot be `null`. |

| Return ||
|---|---|
| Bitmap | This value cannot be `null`. |

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
| `display` | [DisplayMetrics](../android.util/DisplayMetrics.md): Display metrics for the display this bitmap will be drawn on. This value cannot be `null`. |
| `colors` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): Array of sRGB Color used to initialize the pixels. This value cannot be `null`. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of values to skip before the first color in the array of colors. |
| --- | --- |
| `stride` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of colors in the array between rows (must be \>= width or \<= -width). |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the bitmap |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the bitmap |
| --- | --- |
| `config` | [Bitmap.Config](../android/graphics/Bitmap.Config.md): The bitmap config to create. If the config does not support per-pixel alpha (e.g. RGB_565), then the alpha bytes in the colors\[\] will be ignored (assumed to be FF). This value cannot be `null`. |

| Return ||
|---|---|
| Bitmap | This value cannot be `null`. |

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

Returns a mutable bitmap with the specified width and height. Its initial density is as per getDensity. The newly created bitmap is in the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` color space.

| Parameters ||
|---|---|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the bitmap |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the bitmap |
| `config` | [Bitmap.Config](../android/graphics/Bitmap.Config.md): The bitmap config to create. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| Bitmap | This value cannot be `null`. |

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

Returns a mutable bitmap with the specified width and height. Its initial density is as per getDensity. The newly created bitmap is in the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` color space.

| Parameters ||
|---|---|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the bitmap |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the bitmap |
| `config` | [Bitmap.Config](../android/graphics/Bitmap.Config.md): The bitmap config to create. This value cannot be `null`. |
| --- | --- |
| `hasAlpha` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If the bitmap is ARGB_8888, RGBA_16F, or RGBA_1010102 this flag can be used to mark the bitmap as opaque. Doing so will clear the bitmap in black instead of transparent. |

| Return ||
|---|---|
| Bitmap | This value cannot be `null`. |

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

Returns a mutable bitmap with the specified width and height. Its initial density is as per getDensity.

| Parameters ||
|---|---|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the bitmap |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the bitmap |
| `config` | [Bitmap.Config](../android/graphics/Bitmap.Config.md): The bitmap config to create. This value cannot be `null`. |
| --- | --- |
| `hasAlpha` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If the bitmap is ARGB_8888, RGBA_16F, or RGBA_1010102 this flag can be used to mark the bitmap as opaque. Doing so will clear the bitmap in black instead of transparent. |
| `colorSpace` | [ColorSpace](ColorSpace.md): The color space of the bitmap. If the config is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` and `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` or `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` is provided then the corresponding extended range variant is assumed. This value cannot be `null`. |

| Return ||
|---|---|
| Bitmap | This value cannot be `null`. |

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

Returns a immutable bitmap with the specified width and height, with each pixel value set to the corresponding value in the colors array. Its initial density is as per getDensity. The newly created bitmap is in the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` color space.

| Parameters ||
|---|---|
| `colors` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): Array of sRGB Color used to initialize the pixels. This array must be at least as large as width \* height. This value cannot be `null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the bitmap |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the bitmap |
| --- | --- |
| `config` | [Bitmap.Config](../android/graphics/Bitmap.Config.md)!: The bitmap config to create. If the config does not support per-pixel alpha (e.g. RGB_565), then the alpha bytes in the colors\[\] will be ignored (assumed to be FF) |

| Return ||
|---|---|
| Bitmap | This value cannot be `null`. |

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

Returns a immutable bitmap with the specified width and height, with each pixel value set to the corresponding value in the colors array. Its initial density is as per getDensity. The newly created bitmap is in the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` color space.

| Parameters ||
|---|---|
| `colors` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): Array of sRGB Color used to initialize the pixels. This value cannot be `null`. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of values to skip before the first color in the array of colors. |
| `stride` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of colors in the array between rows (must be \>= width or \<= -width). |
| --- | --- |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the bitmap |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the bitmap |
| `config` | [Bitmap.Config](../android/graphics/Bitmap.Config.md): The bitmap config to create. If the config does not support per-pixel alpha (e.g. RGB_565), then the alpha bytes in the colors\[\] will be ignored (assumed to be FF). This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| Bitmap | This value cannot be `null`. |

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
| `src` | [Bitmap](Bitmap.md): The source bitmap. This value cannot be `null`. |
| `dstWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new bitmap's desired width. |
| `dstHeight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new bitmap's desired height. |
| --- | --- |
| `filter` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether or not bilinear filtering should be used when scaling the bitmap. If this is true then bilinear filtering will be used when scaling which has better image quality at the cost of worse performance. If this is false then nearest-neighbor scaling is used instead which will have worse image quality but is faster. Recommended default is to set filter to 'true' as the cost of bilinear filtering is typically minimal and the improved image quality is significant. |

| Return ||
|---|---|
| Bitmap | The new scaled bitmap or the source bitmap if no scaling is required. This value cannot be `null`. |

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

Fills the bitmap's pixels with the specified Color.

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
| `color` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The color to fill as packed by the Color class. |

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
| Bitmap | new bitmap containing the alpha channel of the original bitmap. This value cannot be `null`. |

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
| `paint` | [Paint](Paint.md)?: Optional paint used to modify the alpha values in the resulting bitmap. Pass null for default behavior. |
| `offsetXY` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: Optional array that returns the X (index 0) and Y (index 1) offset needed to position the returned bitmap so that it visually lines up with the original. |

| Return ||
|---|---|
| Bitmap | new bitmap containing the (optionally modified by paint) alpha channel of the original bitmap. This may be drawn with Canvas.drawBitmap(), where the color(s) will be taken from the paint that is passed to the draw call. |

### getAllocationByteCount

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAllocationByteCount(): Int
```

Returns the size of the allocated memory used to store this bitmap's pixels.

This can be larger than the result of getByteCount if a bitmap is reused to decode other bitmaps of smaller size, or by manual reconfiguration. See reconfigure, setWidth, setHeight, setConfig, and `https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options#inBitmap:android.graphics.Bitmap`. If a bitmap is not modified in this way, this value will be the same as that returned by getByteCount.

This value will not change over the lifetime of a Bitmap.
**See Also**

- reconfigure

### getByteCount

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getByteCount(): Int
```

Returns the minimum number of bytes that can be used to store this bitmap's pixels.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int`, the result of this method can no longer be used to determine memory usage of a bitmap. See getAllocationByteCount.

### getColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getColor(
    x: Int, 
    y: Int
): Color
```

Returns the Color at the specified location. Throws an exception if x or y are out of bounds (negative or \>= to the width or height respectively).

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The x coordinate (0...width-1) of the pixel to return |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The y coordinate (0...height-1) of the pixel to return |

| Return ||
|---|---|
| Color | The Color at the specified coordinate. This value cannot be `null`. |

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

- setDensity
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
| `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#` | `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#` which is internally used by hardware bitmap Note: the HardwareBuffer does \*not\* have an associated ColorSpace. To render this object the same as its rendered with this Bitmap, you should also call getColorSpace. <br /> Must not be modified while a wrapped Bitmap is accessing it. Doing so will result in undefined behavior. <br /> . This value cannot be `null`. |

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

Returns the Color at the specified location. Throws an exception if x or y are out of bounds (negative or \>= to the width or height respectively). The returned color is a non-premultiplied ARGB value in the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` color space.

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The x coordinate (0...width-1) of the pixel to return |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The y coordinate (0...height-1) of the pixel to return |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The argb Color at the specified coordinate |

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

Returns in pixels\[\] a copy of the data in the bitmap. Each value is a packed int representing a Color. The stride parameter allows the caller to allow for gaps in the returned pixels array between rows. For normal packed results, just pass width for the stride value. The returned colors are non-premultiplied ARGB values in the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` color space.

| Parameters ||
|---|---|
| `pixels` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): The array to receive the bitmap's colors. This value cannot be `null`. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The first index to write into pixels\[\] |
| `stride` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of entries in pixels\[\] to skip between rows (must be \>= bitmap's width). Can be negative. |
| --- | --- |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The x coordinate of the first pixel to read from the bitmap |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The y coordinate of the first pixel to read from the bitmap |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of pixels to read from each row |
| --- | --- |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of rows to read |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if the pixels array is too small to receive the specified number of pixels. |
| `java.lang.IllegalArgumentException` | if x, y, width, height exceed the bounds of the bitmap, or if abs(stride) \< width. |
| `java.lang.IllegalStateException` | if the bitmap's config is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` |
| --- | --- |

### getRowBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRowBytes(): Int
```

Return the number of bytes between rows in the bitmap's pixels. Note that this refers to the pixels as stored natively by the bitmap. If you call getPixels() or setPixels(), then the pixels are uniformly treated as 32bit values, packed according to the Color class.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int`, this method should not be used to calculate the memory usage of the bitmap. Instead, see getAllocationByteCount.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | number of bytes between rows of the native bitmap pixels. |

### getScaledHeight

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScaledHeight(canvas: Canvas): Int
```

Convenience for calling getScaledHeight with the target density of the given Canvas.

| Parameters ||
|---|---|
| `canvas` | [Canvas](Canvas.md): This value cannot be `null`. |

### getScaledHeight

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScaledHeight(metrics: DisplayMetrics): Int
```

Convenience for calling getScaledHeight with the target density of the given `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`.

| Parameters ||
|---|---|
| `metrics` | [DisplayMetrics](../android.util/DisplayMetrics.md): This value cannot be `null`. |

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

Convenience for calling getScaledWidth with the target density of the given Canvas.

| Parameters ||
|---|---|
| `canvas` | [Canvas](Canvas.md): This value cannot be `null`. |

### getScaledWidth

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScaledWidth(metrics: DisplayMetrics): Int
```

Convenience for calling getScaledWidth with the target density of the given `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`.

| Parameters ||
|---|---|
| `metrics` | [DisplayMetrics](../android.util/DisplayMetrics.md): This value cannot be `null`. |

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

- setHasMipMap

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

This method always returns false if getConfig is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config`.

The return value is undefined if getConfig is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config`.

This method only returns true if hasAlpha returns true. A bitmap with no alpha channel can be used both as a pre-multiplied and as a non pre-multiplied bitmap.

Only pre-multiplied bitmaps may be drawn by the view system or Canvas. If a non-pre-multiplied bitmap with an alpha channel is drawn to a Canvas, a RuntimeException will be thrown.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the underlying pixels have been pre-multiplied, false otherwise |

**See Also**

- setPremultiplied
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

The result of getByteCount will reflect the new configuration, while getAllocationByteCount will reflect that of the initial configuration.

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
| `config` | [Bitmap.Config](../android/graphics/Bitmap.Config.md): This value cannot be `null`. |

**See Also**

- setWidth
- setHeight
- setConfig

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
| `other` | [Bitmap](Bitmap.md)?: This value may be `null`. |

### setColorSpace

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setColorSpace(colorSpace: ColorSpace): Unit
```

Modifies the bitmap to have the specified ColorSpace, without affecting the underlying allocation backing the bitmap.

This affects how the framework will interpret the color at each pixel. A bitmap with `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` never has a color space, since a color space does not affect the alpha channel. Other `Config`s must always have a non-null `ColorSpace`.

| Parameters ||
|---|---|
| `colorSpace` | [ColorSpace](ColorSpace.md): to assign to the bitmap. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the `Config` (returned by getConfig) is `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config`. |

### setConfig

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setConfig(config: Bitmap.Config): Unit
```

Convenience method for calling reconfigure with the current height and width.

WARNING: this method should not be used on bitmaps currently used by the view system, see reconfigure for more details.

| Parameters ||
|---|---|
| `config` | [Bitmap.Config](../android/graphics/Bitmap.Config.md): This value cannot be `null`. |

**See Also**

- reconfigure
- setWidth
- setHeight

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

- getDensity
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
| `gainmap` | [Gainmap](Gainmap.md)?: This value may be `null`. |

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

- hasMipMap

### setHeight

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setHeight(height: Int): Unit
```

Convenience method for calling reconfigure with the current width and config.

WARNING: this method should not be used on bitmaps currently used by the view system, see reconfigure for more details.
**See Also**

- reconfigure
- setWidth
- setConfig

### setPixel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPixel(
    x: Int, 
    y: Int, 
    color: Int
): Unit
```

Write the specified Color into the bitmap (assuming it is mutable) at the x,y coordinate. The color must be a non-premultiplied ARGB value in the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` color space.

| Parameters ||
|---|---|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The x coordinate of the pixel to replace (0...width-1) |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The y coordinate of the pixel to replace (0...height-1) |
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The ARGB color to write into the bitmap |
| --- | --- |

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

Replace pixels in the bitmap with the colors in the array. Each element in the array is a packed int representing a non-premultiplied ARGB Color in the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` color space.

| Parameters ||
|---|---|
| `pixels` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): The colors to write to the bitmap. This value cannot be `null`. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the first color to read from pixels\[\] |
| `stride` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of colors in pixels\[\] to skip between rows. Normally this value will be the same as the width of the bitmap, but it can be larger (or negative). |
| --- | --- |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The x coordinate of the first pixel to write to in the bitmap. |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The y coordinate of the first pixel to write to in the bitmap. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of colors to copy from pixels\[\] per row |
| --- | --- |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of rows to write to the bitmap |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if the pixels array is too small to receive the specified number of pixels. |
| `java.lang.IllegalArgumentException` | if x, y, width, height are outside of the bitmap's bounds. |
| `java.lang.IllegalStateException` | if the bitmap is not mutable |
| --- | --- |

### setPremultiplied

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPremultiplied(premultiplied: Boolean): Unit
```

Sets whether the bitmap should treat its data as pre-multiplied.

Bitmaps are always treated as pre-multiplied by the view system and Canvas for performance reasons. Storing un-pre-multiplied data in a Bitmap (through setPixel, setPixels, or `https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options#inPremultiplied:kotlin.Boolean`) can lead to incorrect blending if drawn by the framework.

This method will not affect the behavior of a bitmap without an alpha channel, or if hasAlpha returns false.

Calling #createBitmap or createScaledBitmap with a source Bitmap whose colors are not pre-multiplied may result in a RuntimeException, since those functions require drawing the source, which is not supported for un-pre-multiplied Bitmaps.
**See Also**

- isPremultiplied
- `https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options#inPremultiplied:kotlin.Boolean`

### setWidth

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setWidth(width: Int): Unit
```

Convenience method for calling reconfigure with the current height and config.

WARNING: this method should not be used on bitmaps currently used by the view system, see reconfigure for more details.
**See Also**

- reconfigure
- setHeight
- setConfig

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
| `hardwareBuffer` | [HardwareBuffer](../android.hardware/HardwareBuffer.md): The HardwareBuffer to wrap. This value cannot be `null`. |
| `colorSpace` | [ColorSpace](ColorSpace.md)?: The color space of the bitmap. Must be a `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Rgb` colorspace. If null, SRGB is assumed. |

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
| `p` | [Parcel](../android.os/Parcel.md): Parcel object to write the bitmap data into. This value cannot be `null`. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<Bitmap!>
```
