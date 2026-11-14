Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RecommendedStreamConfigurationMap

Kotlin | [Java](https://developer.android.com/reference/android/hardware/camera2/params/RecommendedStreamConfigurationMap "View this page in Java")

```
class RecommendedStreamConfigurationMap
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.hardware.camera2.params.RecommendedStreamConfigurationMap](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#) |

Immutable class to store the recommended stream configurations to set up `https://developer.android.com/reference/kotlin/android/view/Surface.html#` for creating a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.html#` with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)`.

The recommended list does not replace or deprecate the exhaustive complete list found in `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap`. It is a suggestion about available power and performance efficient stream configurations for a specific use case. Per definition it is only a subset of `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap` and can be considered by developers for optimization purposes.

This also duplicates the minimum frame durations and stall durations from the `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap` for each format/size combination that can be used to calculate effective frame rate when submitting multiple captures.

An instance of this object is available by invoking `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#getRecommendedStreamConfigurationMap(kotlin.Int)` and passing a respective usecase id. For more information about supported use case constants see `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_PREVIEW:kotlin.Int`.

```kotlin
<code><code>CameraCharacteristics characteristics = cameraManager.getCameraCharacteristics(cameraId); RecommendedStreamConfigurationMap configs = characteristics.getRecommendedStreamConfigurationMap( RecommendedStreamConfigurationMap.USECASE_PREVIEW); </code></code>
```

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_10BIT_OUTPUT:kotlin.Int` If supported, the recommended 10-bit output stream configurations must include a subset of the advertised `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P010:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` outputs that are optimized for power and performance when registered along with a supported 10-bit dynamic range profile. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_LOW_LATENCY_SNAPSHOT:kotlin.Int` The recommended stream configuration map for use case low latency snapshot must contain subset of configurations with end-to-end latency that does not exceed 200 ms. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_PREVIEW:kotlin.Int` The recommended stream configuration map for use case preview must contain a subset of efficient, non-stalling configurations that must include both `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` output formats. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_RAW:kotlin.Int` In case the device supports `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_RAW:kotlin.Int`, the recommended stream configuration map for use case RAW must contain a subset of efficient configurations that include the `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` and other RAW output formats. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_RECORD:kotlin.Int` The recommended stream configuration map for recording must contain a subset of efficient video configurations that include `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` output format for at least all supported `https://developer.android.com/reference/kotlin/android/media/CamcorderProfile.html#`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_SNAPSHOT:kotlin.Int` The recommended stream configuration map for use case snapshot must contain a subset of efficient still capture configurations that must include `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` output format and at least one configuration with size approximately equal to the sensor pixel array size `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_VIDEO_SNAPSHOT:kotlin.Int` The recommended stream configuration map for use case video snapshot must only contain a subset of efficient liveshot configurations that include `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` output format. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_ZSL:kotlin.Int` In case the device supports `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_YUV_REPROCESSING:kotlin.Int` and/or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_PRIVATE_REPROCESSING:kotlin.Int`, the recommended stream configuration map for use case ZSL must contain a subset of efficient configurations that include the suggested input and output format mappings. |

| Public methods ||
|---|---|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!\>? | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#getHighResolutionOutputSizes(kotlin.Int)(format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get a list of supported high resolution sizes, which cannot operate at full BURST_CAPTURE rate. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Range](https://developer.android.com/reference/kotlin/android/util/Range.html#)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!\>? | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#getHighSpeedVideoFpsRanges()()` Get a list of supported high speed video recording FPS ranges. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Range](https://developer.android.com/reference/kotlin/android/util/Range.html#)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!\>? | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#getHighSpeedVideoFpsRangesFor(android.util.Size)(size: https://developer.android.com/reference/kotlin/android/util/Size.html#)` Get the frame per second ranges (fpsMin, fpsMax) for input high speed video size. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!\>? | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#getHighSpeedVideoSizes()()` Get a list of supported high speed video recording sizes. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!\>? | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#getHighSpeedVideoSizesFor(android.util.Range)(fpsRange: https://developer.android.com/reference/kotlin/android/util/Range.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>)` Get the supported video sizes for an input high speed FPS range. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#getInputFormats()()` Get the image `format` input formats in this stream configuration. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!\>? | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#getInputSizes(kotlin.Int)(format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the supported input sizes for this input format. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#getOutputFormats()()` Get the image `format` output formats in this stream configuration. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#getOutputMinFrameDuration(kotlin.Int,%20android.util.Size)(format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, size: https://developer.android.com/reference/kotlin/android/util/Size.html#)` Get the minimum `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` for the format/size combination (in nanoseconds). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#getOutputMinFrameDuration(java.lang.Class,%20android.util.Size)(klass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>, size: https://developer.android.com/reference/kotlin/android/util/Size.html#)` Get the minimum `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` for the class/size combination (in nanoseconds). |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!\>? | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#getOutputSizes(kotlin.Int)(format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get a list of sizes compatible with the requested image `format`. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!\>? | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#getOutputSizes(java.lang.Class)(klass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>)` Get a list of sizes compatible with `klass` to use as an output. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#getOutputStallDuration(kotlin.Int,%20android.util.Size)(format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, size: https://developer.android.com/reference/kotlin/android/util/Size.html#)` Get the stall duration for the format/size combination (in nanoseconds). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#getOutputStallDuration(java.lang.Class,%20android.util.Size)(klass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>, size: https://developer.android.com/reference/kotlin/android/util/Size.html#)` Get the stall duration for the class/size combination (in nanoseconds). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#getRecommendedUseCase()()` Get the use case value for the recommended stream configurations. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#getValidOutputFormatsForInput(kotlin.Int)(inputFormat: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the image `format` output formats for a reprocessing input format. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#isOutputSupportedFor(android.view.Surface)(surface: https://developer.android.com/reference/kotlin/android/view/Surface.html#)` Determine whether or not the `surface` in its current state is suitable to be included in a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)` as an output. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#isOutputSupportedFor(kotlin.Int)(format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determine whether or not output surfaces with a particular user-defined format can be passed `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)`. |

## Constants

### USECASE_10BIT_OUTPUT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USECASE_10BIT_OUTPUT: Int
```

If supported, the recommended 10-bit output stream configurations must include a subset of the advertised `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P010:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` outputs that are optimized for power and performance when registered along with a supported 10-bit dynamic range profile. See `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#setDynamicRangeProfile(kotlin.Long)` for details.

 Value: 8

### USECASE_LOW_LATENCY_SNAPSHOT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USECASE_LOW_LATENCY_SNAPSHOT: Int
```

The recommended stream configuration map for use case low latency snapshot must contain subset of configurations with end-to-end latency that does not exceed 200 ms. under standard operating conditions (reasonable light levels, not loaded system). The expected output format will be primarily `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` however other image formats can be present as well. Even if available for the camera device, high speed and input configurations will be absent. This suggested configuration map may be absent on some devices that can not support any low latency requests.

 Value: 6

### USECASE_PREVIEW

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USECASE_PREVIEW: Int
```

The recommended stream configuration map for use case preview must contain a subset of efficient, non-stalling configurations that must include both `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` output formats. Even if available for the camera device, high speed or input configurations will be absent.

 Value: 0

### USECASE_RAW

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USECASE_RAW: Int
```

In case the device supports `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_RAW:kotlin.Int`, the recommended stream configuration map for use case RAW must contain a subset of efficient configurations that include the `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` and other RAW output formats. Even if available for the camera device, high speed and input configurations will be absent.

 Value: 5

### USECASE_RECORD

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USECASE_RECORD: Int
```

The recommended stream configuration map for recording must contain a subset of efficient video configurations that include `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` output format for at least all supported `https://developer.android.com/reference/kotlin/android/media/CamcorderProfile.html#`. High speed configurations if supported will be available as well. Even if available for the camera device, input configurations will be absent.

 Value: 1

### USECASE_SNAPSHOT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USECASE_SNAPSHOT: Int
```

The recommended stream configuration map for use case snapshot must contain a subset of efficient still capture configurations that must include `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` output format and at least one configuration with size approximately equal to the sensor pixel array size `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`. Even if available for the camera device, high speed or input configurations will be absent.

 Value: 3

### USECASE_VIDEO_SNAPSHOT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USECASE_VIDEO_SNAPSHOT: Int
```

The recommended stream configuration map for use case video snapshot must only contain a subset of efficient liveshot configurations that include `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` output format. The sizes will match at least the maximum resolution of usecase record and will not cause any preview glitches. Even if available for the camera device, high speed or input configurations will be absent.

 Value: 2

### USECASE_ZSL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USECASE_ZSL: Int
```

In case the device supports `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_YUV_REPROCESSING:kotlin.Int` and/or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_PRIVATE_REPROCESSING:kotlin.Int`, the recommended stream configuration map for use case ZSL must contain a subset of efficient configurations that include the suggested input and output format mappings. Even if available for the camera device, high speed configurations will be absent.

 Value: 4

## Public methods

### getHighResolutionOutputSizes

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHighResolutionOutputSizes(format: Int): MutableSet<Size!>?
```

Get a list of supported high resolution sizes, which cannot operate at full BURST_CAPTURE rate.

For further information refer to `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighResolutionOutputSizes(kotlin.Int)`.

| Parameters ||
|---|---|
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBX_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RGB_565:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YV12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P010:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P210:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV21:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUY2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_JPEG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_422_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_444_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW10:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW14:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_POINT_CLOUD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC_ULTRAHDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG_R:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/util/Size.html#!>?` | a non-modifiable set of supported slower high-resolution sizes, or `null` if the BURST_CAPTURE capability is not supported |

### getHighSpeedVideoFpsRanges

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHighSpeedVideoFpsRanges(): MutableSet<Range<Int!>!>?
```

Get a list of supported high speed video recording FPS ranges.

For further information refer to `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoFpsRanges()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/util/Range.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>!>?` | a non-modifiable set of supported high speed video recording FPS ranges The upper bound of returned ranges is guaranteed to be larger or equal to 120. This value may be `null`. |

### getHighSpeedVideoFpsRangesFor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHighSpeedVideoFpsRangesFor(size: Size): MutableSet<Range<Int!>!>?
```

Get the frame per second ranges (fpsMin, fpsMax) for input high speed video size.

For further information refer to `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoFpsRangesFor(android.util.Size)`.

| Parameters ||
|---|---|
| `size` | [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#): one of the sizes returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#getHighSpeedVideoSizes()` This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/util/Range.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>!>?` | a non-modifiable set of supported high speed video recording FPS ranges The upper bound of returned ranges is guaranteed to be greater than or equal to 120. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if input size does not exist in the return value of getHighSpeedVideoSizes |

### getHighSpeedVideoSizes

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHighSpeedVideoSizes(): MutableSet<Size!>?
```

Get a list of supported high speed video recording sizes.

For more information refer to `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoSizes()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/util/Size.html#!>?` | a non-modifiable set of supported high speed video recording sizes. This value may be `null`. |

### getHighSpeedVideoSizesFor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHighSpeedVideoSizesFor(fpsRange: Range<Int!>): MutableSet<Size!>?
```

Get the supported video sizes for an input high speed FPS range.

For further information refer to `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoSizesFor(android.util.Range)`.

| Parameters ||
|---|---|
| `fpsRange` | [Range](https://developer.android.com/reference/kotlin/android/util/Range.html#)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>: one of the FPS ranges returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#getHighSpeedVideoFpsRanges()` This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/util/Size.html#!>?` | A non-modifiable set of video sizes to create high speed capture sessions for high speed streaming use cases. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if input FPS range does not exist in the return value of getHighSpeedVideoFpsRanges |

### getInputFormats

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInputFormats(): MutableSet<Int!>?
```

Get the image `format` input formats in this stream configuration.

All image formats returned by this function will be defined in either `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or in `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#` (and there is no possibility of collision).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>?` | a non-modifiable set of Integer formats. This value may be `null`. |

### getInputSizes

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInputSizes(format: Int): MutableSet<Size!>?
```

Get the supported input sizes for this input format.

The format must have come from `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#getInputFormats()`; otherwise `null` is returned.

| Parameters ||
|---|---|
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a format from `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#getInputFormats()` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBX_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RGB_565:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YV12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P010:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P210:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV21:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUY2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_JPEG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_422_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_444_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW10:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW14:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_POINT_CLOUD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC_ULTRAHDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG_R:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/util/Size.html#!>?` | a non-modifiable set of sizes, or `null` if the format was not available. |

### getOutputFormats

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOutputFormats(): MutableSet<Int!>
```

Get the image `format` output formats in this stream configuration.

For more information refer to `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputFormats()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | a non-modifiable set of Integer formats. This value cannot be `null`. |

### getOutputMinFrameDuration

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOutputMinFrameDuration(
    format: Int, 
    size: Size
): Long
```

Get the minimum `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` for the format/size combination (in nanoseconds).

For further information refer to android.hardware.camera2.params.StreamConfigurationMap#getOutputMinFrameDuration.

| Parameters ||
|---|---|
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an image format from `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBX_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RGB_565:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YV12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P010:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P210:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV21:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUY2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_JPEG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_422_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_444_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW10:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW14:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_POINT_CLOUD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC_ULTRAHDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG_R:kotlin.Int` |
| `size` | [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#): an output-compatible size. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | a minimum frame duration `>` 0 in nanoseconds, or 0 if the minimum frame duration is not available. Value is 0 or greater |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `format` or `size` was not supported |

### getOutputMinFrameDuration

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> getOutputMinFrameDuration(
    klass: Class<T>, 
    size: Size
): Long
```

Get the minimum `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` for the class/size combination (in nanoseconds).

For more information refer to `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputMinFrameDuration(java.lang.Class,%20android.util.Size)`.

| Parameters ||
|---|---|
| `klass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>: a class which has a non-empty array returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#getOutputSizes(java.lang.Class)` This value cannot be `null`. |
| `size` | [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#): an output-compatible size. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | a minimum frame duration `>` 0 in nanoseconds, or 0 if the minimum frame duration is not available. Value is 0 or greater |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `klass` or `size` was not supported |

### getOutputSizes

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOutputSizes(format: Int): MutableSet<Size!>?
```

Get a list of sizes compatible with the requested image `format`.

For more information refer to android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes.

| Parameters ||
|---|---|
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an image format from `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBX_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RGB_565:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YV12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P010:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P210:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV21:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUY2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_JPEG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_422_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_444_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW10:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW14:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_POINT_CLOUD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC_ULTRAHDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG_R:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/util/Size.html#!>?` | a non-modifiable set of supported sizes, or `null` if the `format` is not a supported output |

### getOutputSizes

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> getOutputSizes(klass: Class<T>): MutableSet<Size!>?
```

Get a list of sizes compatible with `klass` to use as an output.

For further information refer to `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(java.lang.Class)`.

| Parameters ||
|---|---|
| `klass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>: a `https://developer.android.com/reference/kotlin/java/lang/Class.html#` object reference. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/util/Size.html#!>?` | a non-modifiable set of supported sizes for `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` format, or `null` if the `klass` is not a supported output. |

### getOutputStallDuration

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOutputStallDuration(
    format: Int, 
    size: Size
): Long
```

Get the stall duration for the format/size combination (in nanoseconds).

For further information refer to android.hardware.camera2.params.StreamConfigurationMap#getOutputStallDuration.

| Parameters ||
|---|---|
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an image format from `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBX_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RGB_565:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YV12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P010:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P210:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV21:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUY2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_JPEG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_422_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_444_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW10:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW14:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_POINT_CLOUD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC_ULTRAHDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG_R:kotlin.Int` |
| `size` | [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#): an output-compatible size. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | a stall duration `>=` 0 in nanoseconds. Value is 0 or greater |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `format` or `size` was not supported |

### getOutputStallDuration

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> getOutputStallDuration(
    klass: Class<T>, 
    size: Size
): Long
```

Get the stall duration for the class/size combination (in nanoseconds).

For more information refer to `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputStallDuration(java.lang.Class,%20android.util.Size)`.

| Parameters ||
|---|---|
| `klass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>: a class which has a non-empty array returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#getOutputSizes(java.lang.Class)`. This value cannot be `null`. |
| `size` | [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#): an output-compatible size. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | a minimum frame duration `>` 0 in nanoseconds, or 0 if the stall duration is not available. Value is 0 or greater |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `klass` or `size` was not supported |

### getRecommendedUseCase

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRecommendedUseCase(): Int
```

Get the use case value for the recommended stream configurations.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Use case id. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_PREVIEW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_RECORD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_VIDEO_SNAPSHOT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_SNAPSHOT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_ZSL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_RAW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_LOW_LATENCY_SNAPSHOT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_10BIT_OUTPUT:kotlin.Int` |

### getValidOutputFormatsForInput

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getValidOutputFormatsForInput(inputFormat: Int): MutableSet<Int!>?
```

Get the image `format` output formats for a reprocessing input format.

For more information refer to `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getValidOutputFormatsForInput(kotlin.Int)`.

| Parameters ||
|---|---|
| `inputFormat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBX_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RGB_565:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YV12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P010:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P210:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV21:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUY2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_JPEG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_422_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_444_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW10:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW14:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_POINT_CLOUD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC_ULTRAHDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG_R:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>?` | a non-modifiable set of Integer formats. This value may be `null`. |

### isOutputSupportedFor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isOutputSupportedFor(surface: Surface): Boolean
```

Determine whether or not the `surface` in its current state is suitable to be included in a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)` as an output.

For more information refer to android.hardware.camera2.params.StreamConfigurationMap#isOutputSupportedFor.

| Parameters ||
|---|---|
| `surface` | [Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#): a `https://developer.android.com/reference/kotlin/android/view/Surface.html#` object reference. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this is supported, `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the Surface endpoint is no longer valid |

### isOutputSupportedFor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isOutputSupportedFor(format: Int): Boolean
```

Determine whether or not output surfaces with a particular user-defined format can be passed `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)`.

For further information refer to android.hardware.camera2.params.StreamConfigurationMap#isOutputSupportedFor.

| Parameters ||
|---|---|
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an image format from either `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBX_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RGB_565:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YV12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P010:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P210:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV21:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUY2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_JPEG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_422_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_444_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW10:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW14:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_POINT_CLOUD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC_ULTRAHDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG_R:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if using a `surface` with this `format` will be supported with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the image format was not a defined named constant from either `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#` |
