Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ColorSpaceProfiles

Kotlin | [Java](../android/hardware/camera2/params/ColorSpaceProfiles.md)
| --- | --- |

```
class ColorSpaceProfiles
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.params.ColorSpaceProfiles](../android/hardware/camera2/params/ColorSpaceProfiles.md) |

Immutable class with information about supported color space profiles.

An instance of this class can be queried by retrieving the value of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#REQUEST_AVAILABLE_COLOR_SPACE_PROFILES:android.hardware.camera2.CameraCharacteristics.Key`.

All camera devices supporting the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_COLOR_SPACE_PROFILES:kotlin.Int` capability must advertise the supported color space profiles in `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceProfiles#getSupportedColorSpaces(kotlin.Int)`

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceProfiles#UNSPECIFIED:kotlin.Int` <br /> |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceProfiles#ColorSpaceProfiles(kotlin.LongArray)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)` Create a new immutable ColorSpaceProfiles instance. |

| Public methods ||
|---|---|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [ColorSpace.Named](../android/graphics/ColorSpace.Named.md)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceProfiles#getSupportedColorSpaces(kotlin.Int)(imageFormat: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return a list of color spaces that are compatible with an ImageFormat. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [ColorSpace.Named](../android/graphics/ColorSpace.Named.md)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceProfiles#getSupportedColorSpacesForDynamicRange(kotlin.Int,%20kotlin.Long)(imageFormat: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dynamicRangeProfile: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Return a list of color spaces that are compatible with an ImageFormat and a dynamic range profile. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceProfiles#getSupportedDynamicRangeProfiles(android.graphics.ColorSpace.Named,%20kotlin.Int)(colorSpace: https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named.html#, imageFormat: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return a list of dynamic range profiles that are compatible with a color space and ImageFormat. |
| --- | --- |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceProfiles#getSupportedImageFormatsForColorSpace(android.graphics.ColorSpace.Named)(colorSpace: https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named.html#)` Return a list of image formats that are compatible with a color space. |

## Constants

### UNSPECIFIED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNSPECIFIED: Int
```

 Value: -1

## Public constructors

### ColorSpaceProfiles

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ColorSpaceProfiles(elements: LongArray)
```

Create a new immutable ColorSpaceProfiles instance.

This constructor takes over the array; do not write to the array afterwards.

Do note that the constructor is available for testing purposes only! Camera clients must always retrieve the value of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#REQUEST_AVAILABLE_COLOR_SPACE_PROFILES:android.hardware.camera2.CameraCharacteristics.Key`. for a given camera id in order to retrieve the device capabilities.

| Parameters ||
|---|---|
| `elements` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): An array of elements describing the map. It contains three elements per entry which describe the supported color space profile value in the first element, a compatible image format in the second, and in the third element a bitmap of compatible dynamic range profiles (see `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#STANDARD:kotlin.Long` and others for the individual bitmap components). This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the `elements` array length is invalid, not divisible by 3 or contains invalid element values |
| `java.lang.NullPointerException` | if `elements` is `null` |

## Public methods

### getSupportedColorSpaces

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSupportedColorSpaces(imageFormat: Int): MutableSet<ColorSpace.Named!>
```

Return a list of color spaces that are compatible with an ImageFormat. If ImageFormat.UNKNOWN is provided, this function will return a set of all unique color spaces supported by the device, regardless of image format. Color spaces which are compatible with ImageFormat.PRIVATE are able to be used with SurfaceView, SurfaceTexture, MediaCodec and MediaRecorder.

| Parameters ||
|---|---|
| `imageFormat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBX_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RGB_565:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YV12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P010:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P210:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV21:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUY2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_JPEG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_422_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_444_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW10:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW14:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_POINT_CLOUD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC_ULTRAHDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG_R:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named.html#!>` | set of color spaces. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setColorSpace(android.graphics.ColorSpace.Named)`
- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named.html#`

### getSupportedColorSpacesForDynamicRange

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSupportedColorSpacesForDynamicRange(
    imageFormat: Int, 
    dynamicRangeProfile: Long
): MutableSet<ColorSpace.Named!>
```

Return a list of color spaces that are compatible with an ImageFormat and a dynamic range profile. If ImageFormat.UNKNOWN is provided, this function will return a set of all unique color spaces compatible with the given dynamic range profile, regardless of image format.

| Parameters ||
|---|---|
| `imageFormat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBX_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RGB_565:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YV12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P010:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P210:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV21:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUY2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_JPEG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_422_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_444_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW10:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW14:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_POINT_CLOUD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC_ULTRAHDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG_R:kotlin.Int` |
| `dynamicRangeProfile` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#STANDARD:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#HLG10:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#HDR10:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#HDR10_PLUS:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_REF:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_REF_PO:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_OEM:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_OEM_PO:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_REF:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_REF_PO:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_OEM:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_OEM_PO:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#STANDARD_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#HLG10_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#HDR10_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#HDR10_PLUS_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_REF_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_REF_PO_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_OEM_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_OEM_PO_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_REF_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_REF_PO_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_OEM_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_OEM_PO_SMPTE_2094_50:kotlin.Long` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named.html#!>` | set of color spaces. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setColorSpace(android.graphics.ColorSpace.Named)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#setDynamicRangeProfile(kotlin.Long)`
- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named.html#`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles`

### getSupportedDynamicRangeProfiles

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSupportedDynamicRangeProfiles(
    colorSpace: ColorSpace.Named, 
    imageFormat: Int
): MutableSet<Long!>
```

Return a list of dynamic range profiles that are compatible with a color space and ImageFormat. If ImageFormat.UNKNOWN is provided, this function will return a set of all unique dynamic range profiles supported by the device given a color space, regardless of image format.

| Parameters ||
|---|---|
| `colorSpace` | [ColorSpace.Named](../android/graphics/ColorSpace.Named.md): This value cannot be `null`. |
| `imageFormat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBX_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RGB_565:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YV12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P010:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P210:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV21:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUY2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_JPEG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_422_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_444_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW10:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW14:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_POINT_CLOUD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC_ULTRAHDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG_R:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html!>` | set of dynamic range profiles. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#setDynamicRangeProfile(kotlin.Long)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setColorSpace(android.graphics.ColorSpace.Named)`
- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named.html#`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles`

### getSupportedImageFormatsForColorSpace

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSupportedImageFormatsForColorSpace(colorSpace: ColorSpace.Named): MutableSet<Int!>
```

Return a list of image formats that are compatible with a color space. Color spaces which are compatible with ImageFormat.PRIVATE are able to be used with SurfaceView, SurfaceTexture, MediaCodec and MediaRecorder.

| Parameters ||
|---|---|
| `colorSpace` | [ColorSpace.Named](../android/graphics/ColorSpace.Named.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | set of image formats. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setColorSpace(android.graphics.ColorSpace.Named)`
- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named.html#`
