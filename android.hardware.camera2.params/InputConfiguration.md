Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputConfiguration

Kotlin | [Java](../android/hardware/camera2/params/InputConfiguration.md)
| --- | --- |

```
class InputConfiguration
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.params.InputConfiguration](../android/hardware/camera2/params/InputConfiguration.md) |

Immutable class to store an input configuration that is used to create a reprocessable capture session.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration#InputConfiguration(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create an input configuration with the width, height, and user-defined format. |
| `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration#InputConfiguration(kotlin.collections.MutableCollection,%20kotlin.Int)(multiResolutionInputs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MultiResolutionStreamInfo!>, format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create an input configuration with the format and a list of multi-resolution input stream info. |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Check if this InputConfiguration is equal to another InputConfiguration. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration#getFormat()()` Get the format of this input configuration. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration#getHeight()()` Get the height of this input configuration. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration#getWidth()()` Get the width of this input configuration. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration#hashCode()()` Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration#isMultiResolution()()` Whether this input configuration is of multi-resolution. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration#toString()()` Return this `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration#` as a string representation. |

## Public constructors

### InputConfiguration

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
InputConfiguration(
    width: Int, 
    height: Int, 
    format: Int)
```

Create an input configuration with the width, height, and user-defined format.

Images of a user-defined format are accessible by applications. Use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key` to query supported input formats

| Parameters ||
|---|---|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Width of the input buffers. |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Height of the input buffers. |
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Format of the input buffers. One of ImageFormat or PixelFormat constants. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#`
- `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key`

### InputConfiguration

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
InputConfiguration(
    multiResolutionInputs: MutableCollection<MultiResolutionStreamInfo!>, 
    format: Int)
```

Create an input configuration with the format and a list of multi-resolution input stream info.

Use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SCALER_MULTI_RESOLUTION_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key` to query supported multi-resolution input formats.

To do reprocessing with variable resolution input, the application calls `https://developer.android.com/reference/kotlin/android/media/ImageWriter.html#queueInputImage(android.media.Image)` using an image from an `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader.html#`. See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createReprocessCaptureRequest(android.hardware.camera2.TotalCaptureResult)` for more details on camera reprocessing.

| Parameters ||
|---|---|
| `multiResolutionInputs` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [MultiResolutionStreamInfo](../android/hardware/camera2/params/MultiResolutionStreamInfo.md)!\>: A group of multi-resolution input info for the specified format. This value cannot be `null`. |
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Format of the input buffers. One of ImageFormat or PixelFormat constants. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGBX_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RGB_565:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YV12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P010:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P210:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV21:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUY2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_JPEG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_422_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_444_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGB_888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#FLEX_RGBA_8888:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW10:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW14:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_POINT_CLOUD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC_ULTRAHDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG_R:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#`
- `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SCALER_MULTI_RESOLUTION_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key`

## Public methods

### equals

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Check if this InputConfiguration is equal to another InputConfiguration.

Two input configurations are equal if and only if they have the same widths, heights, and formats.

| Parameters ||
|---|---|
| `obj` | the object to compare this instance with. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the objects were equal, `false` otherwise. |

### getFormat

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFormat(): Int
```

Get the format of this input configuration.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | format of this input configuration. |

### getHeight

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHeight(): Int
```

Get the height of this input configuration.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | height of this input configuration. |

### getWidth

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getWidth(): Int
```

Get the width of this input configuration.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | width of this input configuration. |

### hashCode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isMultiResolution

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isMultiResolution(): Boolean
```

Whether this input configuration is of multi-resolution.

An multi-resolution InputConfiguration means that the reprocessing session created from it allows input images of different sizes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | this input configuration is multi-resolution or not. |

### toString

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Return this `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration#` as a string representation.

`"InputConfiguration(w:%d, h:%d, format:%d, isMultiResolution:%d)"`, where `%d` represents the width, height, format, and multi-resolution flag respectively.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | string representation of `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration#` |
