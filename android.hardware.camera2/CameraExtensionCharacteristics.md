Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CameraExtensionCharacteristics

```
class CameraExtensionCharacteristics
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.CameraExtensionCharacteristics](CameraExtensionCharacteristics.md) |

Allows clients to query availability and supported resolutions of camera extensions.

Camera extensions give camera clients access to device-specific algorithms and sequences that can improve the overall image quality of snapshots in various cases such as low light, selfies, portraits, and scenes that can benefit from enhanced dynamic range. Often such sophisticated processing sequences will rely on multiple camera frames as input and will produce a single output.

Camera extensions are not guaranteed to be present on all devices so camera clients must query for their availability via getSupportedExtensions.

In order to use any available camera extension, camera clients must create a corresponding CameraExtensionSession via createExtensionSession

Camera clients must be aware that device-specific camera extensions may support only a subset of the available camera resolutions. Starting from API level 37.1, extensions may also choose to not advertise any supported capture resolutions for still capture requests, effectively not supporting still capture functionality. Clients must first query getExtensionSupportedSizes for supported single high-quality request output sizes and getExtensionSupportedSizes for supported repeating request output sizes.

The extension characteristics for a given device are expected to remain static under normal operating conditions.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_AUTOMATIC:kotlin.Int` Device-specific extension implementation for automatic selection of particular extension such as HDR or NIGHT depending on the current lighting and environment conditions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_BEAUTY:kotlin.Int` Device-specific extension implementation which tends to smooth the skin and apply other cosmetic effects to people's faces. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_BOKEH:kotlin.Int` Device-specific extension implementation which can blur certain regions of the final image thereby "enhancing" focus for all remaining non-blurred parts. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_FACE_RETOUCH:kotlin.Int` Device-specific extension implementation which tends to smooth the skin and apply other cosmetic effects to people's faces. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_HDR:kotlin.Int` Device-specific extension implementation for enhancing the dynamic range of the final image. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_NIGHT:kotlin.Int` Device-specific extension implementation that aims to suppress noise and improve the overall image quality under low light conditions. |
| --- | --- |

| Public methods ||
|---|---|
| T | get Gets an extension specific camera characteristics field value. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!\> | getAvailableCaptureRequestKeys Returns the set of keys supported by a CaptureRequest submitted in a CameraExtensionSession with a given extension type. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [CaptureResult.Key](../android/hardware/camera2/CaptureResult.Key.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!\> | getAvailableCaptureResultKeys Returns the set of keys supported by a CaptureResult passed as an argument to onCaptureResultAvailable. |
| --- | --- |
| [Range](../android.util/Range.md)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\>? | getEstimatedCaptureLatencyRangeMillis Returns the estimated capture latency range in milliseconds for the target capture resolution during the calls to capture. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Size](../android.util/Size.md)!\> | getExtensionSupportedSizes Check whether a given extension is available and return the supported output surface resolutions that can be used for high-quality capture requests via capture. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Size](../android.util/Size.md)!\> | getExtensionSupportedSizes Get a list of sizes compatible with `klass` to use as an output for the repeating request setRepeatingRequest. |
| --- | --- |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [CameraCharacteristics.Key](../android/hardware/camera2/CameraCharacteristics.Key.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!\> | getKeys Returns the CameraCharacteristics keys that have extension-specific values. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Size](../android.util/Size.md)!\> | getPostviewSupportedSizes Get a list of the postview sizes supported for a still capture, using its capture size `captureSize`, to use as an output for the postview request. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | getSupportedExtensions Return a list of supported device-specific extensions for a given camera device. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isCaptureProcessProgressAvailable Retrieve support for capture progress callbacks via onCaptureProcessProgressed. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isExtensionSupported Checks if a given camera extension is available for a specific camera device. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isPostviewAvailable Checks for postview support of still capture. |
| --- | --- |

## Constants

### EXTENSION_AUTOMATIC

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTENSION_AUTOMATIC: Int
```

Device-specific extension implementation for automatic selection of particular extension such as HDR or NIGHT depending on the current lighting and environment conditions.

 Value: 0

### EXTENSION_BEAUTY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTENSION_BEAUTY: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_FACE_RETOUCH:kotlin.Int` instead.*

Device-specific extension implementation which tends to smooth the skin and apply other cosmetic effects to people's faces.

 Value: 1

### EXTENSION_BOKEH

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTENSION_BOKEH: Int
```

Device-specific extension implementation which can blur certain regions of the final image thereby "enhancing" focus for all remaining non-blurred parts.

 Value: 2

### EXTENSION_FACE_RETOUCH

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTENSION_FACE_RETOUCH: Int
```

Device-specific extension implementation which tends to smooth the skin and apply other cosmetic effects to people's faces.

 Value: 1

### EXTENSION_HDR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTENSION_HDR: Int
```

Device-specific extension implementation for enhancing the dynamic range of the final image.

 Value: 3

### EXTENSION_NIGHT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTENSION_NIGHT: Int
```

Device-specific extension implementation that aims to suppress noise and improve the overall image quality under low light conditions.

 Value: 4

## Public methods

### get

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> get(
    extension: Int, 
    key: CameraCharacteristics.Key<T>
): T
```

Gets an extension specific camera characteristics field value.

An extension can have a reduced set of camera capabilities (such as limited zoom ratio range, available video stabilization modes, etc). This API enables applications to query for an extension's specific camera characteristics. Applications are recommended to prioritize obtaining camera characteristics using this API when using an extension. A `null` result indicates that the extension specific characteristic is not defined or available.

| Parameters ||
|---|---|
| `extension` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The extension type. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_AUTOMATIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_FACE_RETOUCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_BOKEH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_HDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_NIGHT:kotlin.Int` |
| `key` | [CameraCharacteristics.Key](../android/hardware/camera2/CameraCharacteristics.Key.md)\<T\>: The characteristics field to read. This value cannot be `null`. |

| Return ||
|---|---|
| `T` | The value of that key, or `null` if the field is not set. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the key is not valid or extension type is not a supported device-specific extension. |

### getAvailableCaptureRequestKeys

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAvailableCaptureRequestKeys(extension: Int): MutableSet<CaptureRequest.Key<Any!>!>
```

Returns the set of keys supported by a CaptureRequest submitted in a CameraExtensionSession with a given extension type.

The set returned is not modifiable, so any attempts to modify it will throw a `UnsupportedOperationException`.

Devices launching on Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int` or newer versions are required to support `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_NIGHT:kotlin.Int`.

| Parameters ||
|---|---|
| `extension` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the extension type. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_AUTOMATIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_FACE_RETOUCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_BOKEH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_HDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_NIGHT:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Key<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>!>` | non-modifiable set of capture keys supported by camera extension session initialized with the given extension type. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | in case of unsupported extension. |

### getAvailableCaptureResultKeys

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAvailableCaptureResultKeys(extension: Int): MutableSet<CaptureResult.Key<Any!>!>
```

Returns the set of keys supported by a CaptureResult passed as an argument to onCaptureResultAvailable.

The set returned is not modifiable, so any attempts to modify it will throw a `UnsupportedOperationException`.

In case the set is empty, then the extension is not able to support any capture results and the onCaptureResultAvailable callback will not be fired.

Devices launching on Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int` or newer versions are required to support `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AF_MODE:android.hardware.camera2.CaptureResult.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureResult.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureResult.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AF_STATE:android.hardware.camera2.CaptureResult.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureResult.Key` for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_NIGHT:kotlin.Int`.

| Parameters ||
|---|---|
| `extension` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the extension type. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_AUTOMATIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_FACE_RETOUCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_BOKEH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_HDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_NIGHT:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult.Key<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>!>` | non-modifiable set of capture result keys supported by camera extension session initialized with the given extension type. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | in case of unsupported extension. |

### getEstimatedCaptureLatencyRangeMillis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEstimatedCaptureLatencyRangeMillis(
    extension: Int, 
    captureOutputSize: Size, 
    format: Int
): Range<Long!>?
```

Returns the estimated capture latency range in milliseconds for the target capture resolution during the calls to capture. This includes the time spent processing the multi-frame capture request along with any additional time for encoding of the processed buffer if necessary.

| Parameters ||
|---|---|
| `extension` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the extension type. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_AUTOMATIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_FACE_RETOUCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_BOKEH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_HDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_NIGHT:kotlin.Int` |
| `captureOutputSize` | [Size](../android.util/Size.md): size of the capture output surface. If it is not in the supported output sizes, maximum capture output size is used for the estimation. This value cannot be `null`. |
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): device-specific extension output format |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Range.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html!>?` | the range of estimated minimal and maximal capture latency in milliseconds or null if no capture latency info can be provided |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | in case of format different from `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG_R:kotlin.Int` `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P010:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_JPEG:kotlin.Int`; or unsupported extension. |

### getExtensionSupportedSizes

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExtensionSupportedSizes(
    extension: Int, 
    format: Int
): MutableList<Size!>
```

Check whether a given extension is available and return the supported output surface resolutions that can be used for high-quality capture requests via capture.

Note that device-specific extensions are allowed to support only a subset of the camera resolutions advertised by android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes.

Device-specific extensions currently support at most three multi-frame capture surface formats. ImageFormat.JPEG, ImageFormat.YUV_420_888, ImageFormat.JPEG_R, ImageFormat.YCBCR_P010 or ImageFormat.DEPTH_JPEG may or may not be supported. Starting from API level 37.1, extensions that do not advertise any supported capture resolutions do not support still capture functionality.

| Parameters ||
|---|---|
| `extension` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the extension type. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_AUTOMATIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_FACE_RETOUCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_BOKEH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_HDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_NIGHT:kotlin.Int` |
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): device-specific extension output format |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/util/Size.html#!>` | non-modifiable list of available sizes or an empty list if the format is not supported. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | in case of format different from ImageFormat.JPEG, ImageFormat.YUV_420_888, ImageFormat.JPEG_R, ImageFormat.DEPTH_JPEG, ImageFormat.YCBCR_P010; or unsupported extension. |

### getExtensionSupportedSizes

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> getExtensionSupportedSizes(
    extension: Int, 
    klass: Class<T>
): MutableList<Size!>
```

Get a list of sizes compatible with `klass` to use as an output for the repeating request setRepeatingRequest.

Note that device-specific extensions are allowed to support only a subset of the camera output surfaces and resolutions. The `https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#` class is guaranteed at least one size for backward compatible cameras whereas other output classes are not guaranteed to be supported.

Starting with Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#` classes are also guaranteed to be supported and include the same resolutions as `https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#`. Clients must set the desired SurfaceView resolution by calling setFixedSize.

| Parameters ||
|---|---|
| `extension` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the extension type. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_AUTOMATIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_FACE_RETOUCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_BOKEH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_HDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_NIGHT:kotlin.Int` |
| `klass` | [Class](../java.lang/Class.md)\<T\>: a non-`null` `https://developer.android.com/reference/kotlin/java/lang/Class.html#` object reference |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/util/Size.html#!>` | non-modifiable list of available sizes or an empty list if the Surface output is not supported. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | in case of unsupported extension. |
| `java.lang.NullPointerException` | if `klass` was `null` |

### getKeys

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKeys(extension: Int): MutableSet<CameraCharacteristics.Key<Any!>!>
```

Returns the CameraCharacteristics keys that have extension-specific values.

An application can query the value from the key using get API.

| Parameters ||
|---|---|
| `extension` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The extension type. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_AUTOMATIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_FACE_RETOUCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_BOKEH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_HDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_NIGHT:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>!>` | An unmodifiable set of keys that are extension specific. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | in case the extension type is not a supported device-specific extension |

### getPostviewSupportedSizes

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPostviewSupportedSizes(
    extension: Int, 
    captureSize: Size, 
    format: Int
): MutableList<Size!>
```

Get a list of the postview sizes supported for a still capture, using its capture size `captureSize`, to use as an output for the postview request.

Available postview sizes will always be either equal to or less than the still capture size. When choosing the most applicable postview size for a usecase, it should be noted that lower resolution postviews will generally be available more quickly than larger resolution postviews. For example, when choosing a size for an optimized postview that will be displayed as a placeholder while the final image is processed, the resolution closest to the preview size may be most suitable.

Note that device-specific extensions are allowed to support only a subset of the camera resolutions advertised by android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes.

| Parameters ||
|---|---|
| `extension` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the extension type. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_AUTOMATIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_FACE_RETOUCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_BOKEH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_HDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_NIGHT:kotlin.Int` |
| `captureSize` | [Size](../android.util/Size.md): size of the still capture for which the postview is requested. This value cannot be `null`. |
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): device-specific extension output format of the postview |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/util/Size.html#!>` | non-modifiable list of available sizes or an empty list if the format and size is not supported. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | in case of unsupported extension or if postview feature is not supported by extension. |

### getSupportedExtensions

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSupportedExtensions(): MutableList<Int!>
```

Return a list of supported device-specific extensions for a given camera device.

Do note that starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int` applications can use #isExtensionSupported(java.lang.String,int) to query for public and device specific extension modes. The latter will not be included in the list here.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | non-modifiable list of available extensions. This value cannot be `null`. |

### isCaptureProcessProgressAvailable

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isCaptureProcessProgressAvailable(extension: Int): Boolean
```

Retrieve support for capture progress callbacks via onCaptureProcessProgressed.

| Parameters ||
|---|---|
| `extension` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the extension type. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_AUTOMATIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_FACE_RETOUCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_BOKEH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_HDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_NIGHT:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` in case progress callbacks are supported, `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | in case of an unsupported extension. |

### isExtensionSupported

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isExtensionSupported(extensionType: Int): Boolean
```

Checks if a given camera extension is available for a specific camera device.

An extension may not be available on all devices. Even if a device supports extensions in general, a specific extension might not be implemented for a particular camera ID.

In contrast to getSupportedExtensions this method can also be used to query the available device specific extension modes.

| Parameters ||
|---|---|
| `extensionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The camera extension to query for. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_AUTOMATIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_FACE_RETOUCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_BOKEH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_HDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_NIGHT:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the specified extension is supported for the given camera device, `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_AUTOMATIC:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_BOKEH:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_FACE_RETOUCH:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_HDR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_NIGHT:kotlin.Int`

### isPostviewAvailable

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isPostviewAvailable(extension: Int): Boolean
```

Checks for postview support of still capture.

A postview is a preview version of the still capture that is available before the final image. For example, it can be used as a temporary placeholder for the requested capture while the final image is being processed. The supported sizes for a still capture's postview can be retrieved using getPostviewSupportedSizes.

Starting with Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`, the formats of the still capture and postview are not required to be equivalent upon capture request.

| Parameters ||
|---|---|
| `extension` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the extension type. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_AUTOMATIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_FACE_RETOUCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_BOKEH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_HDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_NIGHT:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` in case postview is supported, `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | in case the extension type is not a supported device-specific extension |
