Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Gainmap

Kotlin | [Java](Gainmap.md)
| --- | --- |

```
class Gainmap : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.Gainmap](Gainmap.md) |

Gainmap represents a mechanism for augmenting an SDR image to produce an HDR one with variable display adjustment capability. It is a combination of a set of metadata describing how to apply the gainmap, as well as either a 1 (such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` or 3 (such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config` with the alpha channel ignored) channel Bitmap that represents the gainmap data itself.

When rendering to an `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#COLOR_MODE_HDR:kotlin.Int` activity, the hardware accelerated `https://developer.android.com/reference/kotlin/android/graphics/Canvas` will automatically apply the gainmap when sufficient HDR headroom is available.

### Gainmap Structure

The logical whole of a gainmap'd image consists of a base Bitmap that represents the original image as would be displayed without gainmap support in addition to a gainmap with a second enhancement image. In the case of a JPEG, the base image would be the typical 8-bit SDR image that the format is commonly associated with. The gainmap image is embedded alongside the base image, often at a lower resolution (such as 1/4th), along with some metadata to describe how to apply the gainmap. The gainmap image itself is then a greyscale image representing the transformation to apply onto the base image to reconstruct an HDR rendition of it.

As such these "gainmap images" consist of 3 parts - a base `https://developer.android.com/reference/kotlin/android/graphics/Bitmap` with a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getGainmap()` that returns an instance of this class which in turn contains the enhancement layer represented as another Bitmap, accessible via `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#getGainmapContents()`

### Applying a gainmap manually

When doing custom rendering such as to an OpenGL ES or Vulkan context, the gainmap is not automatically applied. In such situations, the following steps are appropriate to render the gainmap in combination with the base image.

Suppose our display has HDR to SDR ratio of H, and we wish to display an image with gainmap on this display. Let B be the pixel value from the base image in a color space that has the primaries of the base image and a linear transfer function. Let G be the pixel value from the gainmap. Let D be the output pixel in the same color space as B. The value of D is computed as follows:

First, let W be a weight parameter determining how much the gainmap will be applied.

```kotlin
W = clamp((log(H)                      - log(minDisplayRatioForHdrTransition)) /
              (log(displayRatioForFullHdr) - log(minDisplayRatioForHdrTransition), 0, 1)
```
Next, let L be the gainmap value in log space. We compute this from the value G that was sampled from the texture as follows:

```kotlin
L = mix(log(ratioMin), log(ratioMax), pow(G, gamma))
```
Finally, apply the gainmap to compute D, the displayed pixel. If the base image is SDR then compute:

```kotlin
D = (B + epsilonSdr) * exp(L * W) - epsilonHdr
```

In the above math, log() is a natural logarithm and exp() is natural exponentiation. The base for these functions cancels out and does not affect the result, so other bases may be used if preferred.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#GAINMAP_DIRECTION_HDR_TO_SDR:kotlin.Int` The gainmap will be applied as if the base image were HDR, and fully applying the gainmap results in an SDR image. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#GAINMAP_DIRECTION_SDR_TO_HDR:kotlin.Int` The gainmap will be applied as if the base image were SDR, and fully applying the gainmap results in an HDR image. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#Gainmap(android.graphics.Bitmap)(gainmapContents: https://developer.android.com/reference/kotlin/android/graphics/Bitmap)` Creates a gainmap from a given Bitmap. |
| `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#Gainmap(android.graphics.Gainmap,%20android.graphics.Bitmap)(gainmap: https://developer.android.com/reference/kotlin/android/graphics/Gainmap#, gainmapContents: https://developer.android.com/reference/kotlin/android/graphics/Bitmap)` Creates a new gainmap using the provided gainmap as the metadata source and the provided bitmap as the replacement for the gainmapContents |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#describeContents()()` No special parcel contents. |
| [ColorSpace](ColorSpace.md)? | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#getAlternativeImagePrimaries()()` Gets the colorspace that the gainmap math should be applied in. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#getDisplayRatioForFullHdr()()` Gets the hdr/sdr ratio at which point applying the gainmap results in an HDR rendition |
| --- | --- |
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#getEpsilonHdr()()` Gets the hdr epsilon. |
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#getEpsilonSdr()()` Gets the sdr epsilon. |
| [Bitmap](Bitmap.md) | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#getGainmapContents()()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#getGainmapDirection()()` Gets the direction that the gainmap math should be applied in. |
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#getGamma()()` Gets the gainmap gamma. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#getMinDisplayRatioForHdrTransition()()` Gets the hdr/sdr ratio below which applying the gainmap results in an SDR rendition. |
| --- | --- |
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#getRatioMax()()` Gets the gainmap ratio max. |
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#getRatioMin()()` Gets the gainmap ratio max. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#setAlternativeImagePrimaries(android.graphics.ColorSpace)(colorSpace: https://developer.android.com/reference/kotlin/android/graphics/ColorSpace?)` Sets the colorspace that the gainmap math should be applied in. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#setDisplayRatioForFullHdr(kotlin.Float)(max: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the hdr/sdr ratio at which point applying the gainmap results in an HDR rendition. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#setEpsilonHdr(kotlin.Float,%20kotlin.Float,%20kotlin.Float)(r: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, g: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the hdr epsilon which is used to avoid numerical instability. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#setEpsilonSdr(kotlin.Float,%20kotlin.Float,%20kotlin.Float)(r: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, g: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the sdr epsilon which is used to avoid numerical instability. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#setGainmapContents(android.graphics.Bitmap)(bitmap: https://developer.android.com/reference/kotlin/android/graphics/Bitmap)` Sets the image data of the gainmap. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#setGainmapDirection(kotlin.Int)(direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the direction that the gainmap math should be applied in. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#setGamma(kotlin.Float,%20kotlin.Float,%20kotlin.Float)(r: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, g: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the gainmap gamma. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#setMinDisplayRatioForHdrTransition(kotlin.Float)(min: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the hdr/sdr ratio below which applying the gainmap results in an SDR rendition. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#setRatioMax(kotlin.Float,%20kotlin.Float,%20kotlin.Float)(r: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, g: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the gainmap ratio max. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#setRatioMin(kotlin.Float,%20kotlin.Float,%20kotlin.Float)(r: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, g: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the gainmap ratio min. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Write the gainmap to the parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Gainmap](Gainmap.md)!\> | `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### GAINMAP_DIRECTION_HDR_TO_SDR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GAINMAP_DIRECTION_HDR_TO_SDR: Int
```

The gainmap will be applied as if the base image were HDR, and fully applying the gainmap results in an SDR image.

 Value: 1

### GAINMAP_DIRECTION_SDR_TO_HDR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GAINMAP_DIRECTION_SDR_TO_HDR: Int
```

The gainmap will be applied as if the base image were SDR, and fully applying the gainmap results in an HDR image.

 Value: 0

## Public constructors

### Gainmap

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Gainmap(gainmapContents: Bitmap)
```

Creates a gainmap from a given Bitmap. The caller is responsible for setting the various fields to the desired values. The defaults are as follows:

- Ratio min is 1f, 1f, 1f
- Ratio max is 2f, 2f, 2f
- Gamma is 1f, 1f, 1f
- Epsilon SDR is 0f, 0f, 0f
- Epsilon HDR is 0f, 0f, 0f
- Display ratio SDR is 1f
- Display ratio HDR is 2f

It is strongly recommended that at least the ratio max and display ratio HDR are adjusted to better suit the given gainmap contents.

<br />

| Parameters ||
|---|---|
| `gainmapContents` | [Bitmap](Bitmap.md): This value cannot be `null`. |

### Gainmap

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Gainmap(
    gainmap: Gainmap, 
    gainmapContents: Bitmap)
```

Creates a new gainmap using the provided gainmap as the metadata source and the provided bitmap as the replacement for the gainmapContents

| Parameters ||
|---|---|
| `gainmap` | [Gainmap](Gainmap.md): This value cannot be `null`. |
| `gainmapContents` | [Bitmap](Bitmap.md): This value cannot be `null`. |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

No special parcel contents.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getAlternativeImagePrimaries

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAlternativeImagePrimaries(): ColorSpace?
```

Gets the colorspace that the gainmap math should be applied in. Only the primaries are what is relevant for applying the gainmap. The transfer and range characteritics are ignored. If the returned ColorSpace is null, then applying the gainmap will be done using the color gamut of the base image.

### getDisplayRatioForFullHdr

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplayRatioForFullHdr(): Float
```

Gets the hdr/sdr ratio at which point applying the gainmap results in an HDR rendition

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | This value cannot be `null`. |

### getEpsilonHdr

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEpsilonHdr(): FloatArray
```

Gets the hdr epsilon. For single-plane gainmaps, all 3 components should be the same. The components are in r, g, b order.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html` | This value cannot be `null`. |

### getEpsilonSdr

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEpsilonSdr(): FloatArray
```

Gets the sdr epsilon. For single-plane gainmaps, all 3 components should be the same. The components are in r, g, b order.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html` | This value cannot be `null`. |

### getGainmapContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getGainmapContents(): Bitmap
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap` | Returns the image data of the gainmap represented as a Bitmap. This is represented as a Bitmap for broad API compatibility, however certain aspects of the Bitmap are ignored such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getColorSpace()` or `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getGainmap()` as they are not relevant to the gainmap's enhancement layer. This value cannot be `null`. |

### getGainmapDirection

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getGainmapDirection(): Int
```

Gets the direction that the gainmap math should be applied in.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#GAINMAP_DIRECTION_SDR_TO_HDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#GAINMAP_DIRECTION_HDR_TO_SDR:kotlin.Int` |

### getGamma

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getGamma(): FloatArray
```

Gets the gainmap gamma. For single-plane gainmaps, all 3 components should be the same. The components are in r, g, b order.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html` | This value cannot be `null`. |

### getMinDisplayRatioForHdrTransition

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMinDisplayRatioForHdrTransition(): Float
```

Gets the hdr/sdr ratio below which applying the gainmap results in an SDR rendition.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | This value cannot be `null`. |

### getRatioMax

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRatioMax(): FloatArray
```

Gets the gainmap ratio max. For single-plane gainmaps, all 3 components should be the same. The components are in r, g, b order.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html` | This value cannot be `null`. |

### getRatioMin

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRatioMin(): FloatArray
```

Gets the gainmap ratio max. For single-plane gainmaps, all 3 components should be the same. The components are in r, g, b order.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html` | This value cannot be `null`. |

### setAlternativeImagePrimaries

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setAlternativeImagePrimaries(colorSpace: ColorSpace?): Unit
```

Sets the colorspace that the gainmap math should be applied in. Only the primaries are what is relevant for applying the gainmap. The transfer and range characteritics are ignored. If the supplied ColorSpace is null, then applying the gainmap will be done using the color gamut of the base image.

| Parameters ||
|---|---|
| `colorSpace` | [ColorSpace](ColorSpace.md)?: This value may be `null`. |

### setDisplayRatioForFullHdr

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setDisplayRatioForFullHdr(max: Float): Unit
```

Sets the hdr/sdr ratio at which point applying the gainmap results in an HDR rendition.

| Parameters ||
|---|---|
| `max` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The hdr/sdr ratio at which point applying the gainmap results in an HDR rendition. Must be \>= 1.0f. Value is 1.0f or greater |

### setEpsilonHdr

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setEpsilonHdr(
    r: Float, 
    g: Float, 
    b: Float
): Unit
```

Sets the hdr epsilon which is used to avoid numerical instability. For single-plane gainmaps, r, g, and b should be the same.

### setEpsilonSdr

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setEpsilonSdr(
    r: Float, 
    g: Float, 
    b: Float
): Unit
```

Sets the sdr epsilon which is used to avoid numerical instability. For single-plane gainmaps, r, g, and b should be the same.

### setGainmapContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setGainmapContents(bitmap: Bitmap): Unit
```

Sets the image data of the gainmap. This is the 1 or 3 channel enhancement layer to apply to the base image. This is represented as a Bitmap for broad API compatibility, however certain aspects of the Bitmap are ignored such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getColorSpace()` or `https://developer.android.com/reference/kotlin/android/graphics/Bitmap#getGainmap()` as they are not relevant to the gainmap's enhancement layer.

| Parameters ||
|---|---|
| `bitmap` | [Bitmap](Bitmap.md): The non-null bitmap to set as the gainmap's contents |

### setGainmapDirection

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setGainmapDirection(direction: Int): Unit
```

Sets the direction that the gainmap math should be applied in.

| Parameters ||
|---|---|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#GAINMAP_DIRECTION_SDR_TO_HDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/Gainmap#GAINMAP_DIRECTION_HDR_TO_SDR:kotlin.Int` |

### setGamma

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setGamma(
    r: Float, 
    g: Float, 
    b: Float
): Unit
```

Sets the gainmap gamma. For single-plane gainmaps, r, g, and b should be the same.

### setMinDisplayRatioForHdrTransition

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setMinDisplayRatioForHdrTransition(min: Float): Unit
```

Sets the hdr/sdr ratio below which applying the gainmap results in an SDR rendition.

| Parameters ||
|---|---|
| `min` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The minimum hdr/sdr ratio at which point applying the gainmap results in an SDR rendition. Must be \>= 1.0f. Value is 1.0f or greater |

### setRatioMax

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRatioMax(
    r: Float, 
    g: Float, 
    b: Float
): Unit
```

Sets the gainmap ratio max. For single-plane gainmaps, r, g, and b should be the same.

### setRatioMin

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRatioMin(
    r: Float, 
    g: Float, 
    b: Float
): Unit
```

Sets the gainmap ratio min. For single-plane gainmaps, r, g, and b should be the same.

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Write the gainmap to the parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): Parcel object to write the gainmap data into. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<Gainmap!>
```
