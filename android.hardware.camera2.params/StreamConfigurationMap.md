Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StreamConfigurationMap

```
class StreamConfigurationMap
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.hardware.camera2.params.StreamConfigurationMap](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#) |

Immutable class to store the available stream `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key` to set up `https://developer.android.com/reference/kotlin/android/view/Surface.html#` for creating a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.html#` with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)`.

This is the authoritative list for all output formats (and sizes respectively for that format) that are supported by a camera device.

This also contains the minimum frame durations and stall durations for each format/size combination that can be used to calculate effective frame rate when submitting multiple captures.

An instance of this object is available from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#` using the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key` key and the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#get(android.hardware.camera2.CameraCharacteristics.Key)` method.

```kotlin
<code><code>CameraCharacteristics characteristics = cameraManager.getCameraCharacteristics(cameraId); StreamConfigurationMap configs = characteristics.get( CameraCharacteristics.SCALER_STREAM_CONFIGURATION_MAP); </code></code>
```

## Summary

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Check if this `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#` is equal to another `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#`. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!\>! | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighResolutionOutputSizes(kotlin.Int)(format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get a list of supported high resolution sizes, which cannot operate at full BURST_CAPTURE rate. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Range](https://developer.android.com/reference/kotlin/android/util/Range.html#)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!\>! | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoFpsRanges()()` Get a list of supported high speed video recording FPS ranges. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Range](https://developer.android.com/reference/kotlin/android/util/Range.html#)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!\>! | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoFpsRangesFor(android.util.Size)(size: https://developer.android.com/reference/kotlin/android/util/Size.html#!)` Get the frame per second ranges (fpsMin, fpsMax) for input high speed video size. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!\>! | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoSizes()()` Get a list of supported high speed video recording sizes. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!\>! | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoSizesFor(android.util.Range)(fpsRange: https://developer.android.com/reference/kotlin/android/util/Range.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>!)` Get the supported video sizes for an input high speed FPS range. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()()` Get the image `format` input formats in this stream configuration. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!\>! | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputSizes(kotlin.Int)(format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the supported input sizes for this input format. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputFormats()()` Get the image `format` output formats in this stream configuration. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputMinFrameDuration(kotlin.Int,%20android.util.Size)(format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, size: https://developer.android.com/reference/kotlin/android/util/Size.html#!)` Get the minimum `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` for the format/size combination (in nanoseconds). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputMinFrameDuration(java.lang.Class,%20android.util.Size)(klass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>!, size: https://developer.android.com/reference/kotlin/android/util/Size.html#!)` Get the minimum `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` for the class/size combination (in nanoseconds). |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!\>! | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(kotlin.Int)(format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get a list of sizes compatible with the requested image `format`. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!\>! | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(java.lang.Class)(klass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>!)` Get a list of sizes compatible with `klass` to use as an output. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputStallDuration(kotlin.Int,%20android.util.Size)(format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, size: https://developer.android.com/reference/kotlin/android/util/Size.html#!)` Get the stall duration for the format/size combination (in nanoseconds). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputStallDuration(java.lang.Class,%20android.util.Size)(klass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>!, size: https://developer.android.com/reference/kotlin/android/util/Size.html#!)` Get the stall duration for the class/size combination (in nanoseconds). |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getValidOutputFormatsForInput(kotlin.Int)(inputFormat: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the image `format` output formats for a reprocessing input format. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#hashCode()()` Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#isOutputSupportedFor(android.view.Surface)(surface: https://developer.android.com/reference/kotlin/android/view/Surface.html#!)` Determine whether or not the `surface` in its current state is suitable to be included in a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)` as an output. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#isOutputSupportedFor(kotlin.Int)(format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determine whether or not output surfaces with a particular user-defined format can be passed `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)`. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#isOutputSupportedFor(java.lang.Class)(klass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>!)` Determine whether or not output streams can be configured with a particular class as a consumer. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#toString()()` Return this `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#` as a string representation. |

## Public methods

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Check if this `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#` is equal to another `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#`.

Two vectors are only equal if and only if each of the respective elements is equal.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the objects were equal, `false` otherwise |

### getHighResolutionOutputSizes

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHighResolutionOutputSizes(format: Int): Array<Size!>!
```

Get a list of supported high resolution sizes, which cannot operate at full BURST_CAPTURE rate.

This includes all output sizes that cannot meet the 20 fps frame rate requirements for the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_BURST_CAPTURE:kotlin.Int` capability. This does not include the stall duration, so for example, a JPEG or RAW16 output resolution with a large stall duration but a minimum frame duration that's above 20 fps will still be listed in the regular #getOutputSizes list. All the sizes on this list that are less than 24 megapixels are still guaranteed to operate at a rate of at least 10 fps, not including stall duration. Sizes on this list that are at least 24 megapixels are allowed to operate at less than 10 fps.

For a device that does not support the BURST_CAPTURE capability, this list will be `null`, since resolutions in the #getOutputSizes list are already not guaranteed to meet \>= 20 fps rate requirements. For a device that does support the BURST_CAPTURE capability, this list may be empty, if all supported resolutions meet the 20 fps requirement.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/util/Size.html#!>!` | an array of supported slower high-resolution sizes, or `null` if the BURST_CAPTURE capability is not supported |

### getHighSpeedVideoFpsRanges

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHighSpeedVideoFpsRanges(): Array<Range<Int!>!>!
```

Get a list of supported high speed video recording FPS ranges.

When `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_CONSTRAINED_HIGH_SPEED_VIDEO:kotlin.Int` is supported in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`, this method will list the supported high speed video FPS range configurations. Application can then use `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoSizesFor(android.util.Range)` to query available sizes for one of returned FPS range.

To enable high speed video recording, application must create a constrained create high speed capture session via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createConstrainedHighSpeedCaptureSession(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)`, and submit a CaptureRequest list created by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraConstrainedHighSpeedCaptureSession.html#createHighSpeedRequestList(android.hardware.camera2.CaptureRequest)` to this session. The application must select the video size from this method and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key` from `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoFpsRangesFor(android.util.Size)` to configure the constrained high speed session and generate the high speed request list. For example, if the application intends to do high speed recording, it can select one FPS range reported by this method, query the video sizes corresponding to this FPS range by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoSizesFor(android.util.Range)` and use one of reported sizes to create a high speed capture session. Note that for the use case of multiple output streams, application must select one unique size from this method to use (e.g., preview and recording streams must have the same size). Otherwise, the high speed session creation will fail. Once the high speed capture session is created, the application can set the FPS range in the recording request lists via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraConstrainedHighSpeedCaptureSession.html#createHighSpeedRequestList(android.hardware.camera2.CaptureRequest)`.

The FPS ranges reported by this method will have below characteristics:
- The fpsMin and fpsMax will be a multiple 30fps.
- The fpsMin will be no less than 30fps, the fpsMax will be no less than 120fps.
- At least one range will be a fixed FPS range where fpsMin == fpsMax.
- For each fixed FPS range, there will be one corresponding variable FPS range \[30, fps_max\] or \[60, fps_max\]. These kinds of FPS ranges are suitable for preview-only use cases where the application doesn't want the camera device always produce higher frame rate than the display refresh rate. Both 30fps and 60fps preview rate will not be supported for the same recording rate.
- This function returns an empty array if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_CONSTRAINED_HIGH_SPEED_VIDEO:kotlin.Int` is not supported.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/util/Range.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>!>!` | an array of supported high speed video recording FPS ranges The upper bound of returned ranges is guaranteed to be larger or equal to 120. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoSizesFor(android.util.Range)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_CONSTRAINED_HIGH_SPEED_VIDEO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createConstrainedHighSpeedCaptureSession(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraConstrainedHighSpeedCaptureSession.html#createHighSpeedRequestList(android.hardware.camera2.CaptureRequest)`

### getHighSpeedVideoFpsRangesFor

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHighSpeedVideoFpsRangesFor(size: Size!): Array<Range<Int!>!>!
```

Get the frame per second ranges (fpsMin, fpsMax) for input high speed video size.

See `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoFpsRanges()` for how to enable high speed recording.

The `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key` reported in this method must not be used to setup capture requests that are submitted to unconstrained capture sessions, or it will result in `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

See `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoFpsRanges()` for the characteristics of the returned FPS ranges.

| Parameters ||
|---|---|
| `size` | [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!: one of the sizes returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoSizes()` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/util/Range.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>!>!` | an array of supported high speed video recording FPS ranges The upper bound of returned ranges is guaranteed to be greater than or equal to 120. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if input size does not exist in the return value of getHighSpeedVideoSizes |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoSizes()`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoFpsRanges()`

### getHighSpeedVideoSizes

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHighSpeedVideoSizes(): Array<Size!>!
```

Get a list of supported high speed video recording sizes.

When `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_CONSTRAINED_HIGH_SPEED_VIDEO:kotlin.Int` is supported in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`, this method will list the supported high speed video size configurations. All the sizes listed will be a subset of the sizes reported by #getOutputSizes for processed non-stalling formats (typically `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int`, etc.)

To enable high speed video recording, application must create a constrained create high speed capture session via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createConstrainedHighSpeedCaptureSession(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)`, and submit a CaptureRequest list created by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraConstrainedHighSpeedCaptureSession.html#createHighSpeedRequestList(android.hardware.camera2.CaptureRequest)` to this session. The application must select the video size from this method and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key` from `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoFpsRangesFor(android.util.Size)` to configure the constrained high speed session and generate the high speed request list. For example, if the application intends to do high speed recording, it can select the maximum size reported by this method to create high speed capture session. Note that for the use case of multiple output streams, application must select one unique size from this method to use (e.g., preview and recording streams must have the same size). Otherwise, the high speed session creation will fail. Once the size is selected, application can get the supported FPS ranges by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoFpsRangesFor(android.util.Size)`, and use these FPS ranges to setup the recording request lists via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraConstrainedHighSpeedCaptureSession.html#createHighSpeedRequestList(android.hardware.camera2.CaptureRequest)`.

This function returns an empty array if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_CONSTRAINED_HIGH_SPEED_VIDEO:kotlin.Int` is not supported.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/util/Size.html#!>!` | an array of supported high speed video recording sizes |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoFpsRangesFor(android.util.Size)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_CONSTRAINED_HIGH_SPEED_VIDEO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createConstrainedHighSpeedCaptureSession(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraConstrainedHighSpeedCaptureSession.html#createHighSpeedRequestList(android.hardware.camera2.CaptureRequest)`

### getHighSpeedVideoSizesFor

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHighSpeedVideoSizesFor(fpsRange: Range<Int!>!): Array<Size!>!
```

Get the supported video sizes for an input high speed FPS range.

See `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoSizes()` for how to enable high speed recording.

| Parameters ||
|---|---|
| `fpsRange` | [Range](https://developer.android.com/reference/kotlin/android/util/Range.html#)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!: one of the FPS range returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoFpsRanges()` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/util/Size.html#!>!` | An array of video sizes to create high speed capture sessions for high speed streaming use cases. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if input FPS range does not exist in the return value of getHighSpeedVideoFpsRanges |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoFpsRanges()`

### getInputFormats

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInputFormats(): IntArray!
```

Get the image `format` input formats in this stream configuration.

All image formats returned by this function will be defined in either `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or in `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#` (and there is no possibility of collision).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` | an array of integer format |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#`
- `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#`

### getInputSizes

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInputSizes(format: Int): Array<Size!>!
```

Get the supported input sizes for this input format.

The format must have come from `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()`; otherwise `null` is returned.

| Parameters ||
|---|---|
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a format from `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/util/Size.html#!>!` | a non-empty array of sizes, or `null` if the format was not available. |

### getOutputFormats

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOutputFormats(): IntArray!
```

Get the image `format` output formats in this stream configuration.

All image formats returned by this function will be defined in either `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or in `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#` (and there is no possibility of collision).

Formats listed in this array are guaranteed to return true if queried with `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#isOutputSupportedFor(kotlin.Int)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` | an array of integer format |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#`
- `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#`

### getOutputMinFrameDuration

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOutputMinFrameDuration(
    format: Int, 
    size: Size!
): Long
```

Get the minimum `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` for the format/size combination (in nanoseconds).

`format` should be one of the ones returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputFormats()`.

`size` should be one of the ones returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(kotlin.Int)`.

This corresponds to the minimum frame duration (maximum frame rate) possible when only that stream is configured in a session, with all processing (typically in `android.*.mode`) set to either `OFF` or `FAST`.

When multiple streams are used in a session, the minimum frame duration will be `max(individual stream min durations)`. See #getOutputStallDuration for details of timing for formats that may cause frame rate slowdown when they are targeted by a capture request.

For camera `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key`, up until Android 11, for devices that do not support manual sensor control (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_MANUAL_SENSOR:kotlin.Int`), this function may return 0. From Android 12 onwards, this function always returns a positive value.

For `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SCALER_STREAM_CONFIGURATION_MAP_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key` stream configuration map, this function always returns a positive value for OSes newer than Android 17.

The minimum frame duration of a stream (of a particular format, size) is the same regardless of whether the stream is input or output.

| Parameters ||
|---|---|
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an image format from `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#` |
| `size` | [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!: an output-compatible size |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | a minimum frame duration `>` 0 in nanoseconds, or 0 if the minimum frame duration is not available. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `format` or `size` was not supported |
| `java.lang.NullPointerException` | if `size` was `null` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputStallDuration(kotlin.Int,%20android.util.Size)`
- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#`
- `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#`

### getOutputMinFrameDuration

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> getOutputMinFrameDuration(
    klass: Class<T>!, 
    size: Size!
): Long
```

Get the minimum `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` for the class/size combination (in nanoseconds).

This assumes that the `klass` is set up to use `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int`. For user-defined formats, use `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputMinFrameDuration(kotlin.Int,%20android.util.Size)`.

`klass` should be one of the ones which is supported by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#isOutputSupportedFor(java.lang.Class)`.

`size` should be one of the ones returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(kotlin.Int)`.

This corresponds to the minimum frame duration (maximum frame rate) possible when only that stream is configured in a session, with all processing (typically in `android.*.mode`) set to either `OFF` or `FAST`.

When multiple streams are used in a session, the minimum frame duration will be `max(individual stream min durations)`. See #getOutputStallDuration for details of timing for formats that may cause frame rate slowdown when they are targeted by a capture request.

For devices that do not support manual sensor control (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_MANUAL_SENSOR:kotlin.Int`), this function may return 0.

The minimum frame duration of a stream (of a particular format, size) is the same regardless of whether the stream is input or output.

| Parameters ||
|---|---|
| `klass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>!: a class which is supported by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#isOutputSupportedFor(java.lang.Class)` and has a non-empty array returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(java.lang.Class)` |
| `size` | [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!: an output-compatible size |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | a minimum frame duration `>` 0 in nanoseconds, or 0 if the minimum frame duration is not available. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `klass` or `size` was not supported |
| `java.lang.NullPointerException` | if `size` or `klass` was `null` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#`
- `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#`

### getOutputSizes

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOutputSizes(format: Int): Array<Size!>!
```

Get a list of sizes compatible with the requested image `format`.

The `format` should be a supported format (one of the formats returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputFormats()`).
As of API level 23, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighResolutionOutputSizes(kotlin.Int)` method can be used on devices that support the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_BURST_CAPTURE:kotlin.Int` capability to get a list of high-resolution output sizes that cannot operate at the preferred 20fps rate. This means that for some supported formats, this method will return an empty list, if all the supported resolutions operate at below 20fps. For devices that do not support the BURST_CAPTURE capability, all output resolutions are listed through this method.

| Parameters ||
|---|---|
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an image format from `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/util/Size.html#!>!` | an array of supported sizes, or `null` if the `format` is not a supported output |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#`
- `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputFormats()`

### getOutputSizes

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> getOutputSizes(klass: Class<T>!): Array<Size!>!
```

Get a list of sizes compatible with `klass` to use as an output.

Some of the supported classes may support additional formats beyond `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int`; this function only returns sizes for `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int`. For example, `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#` supports `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int`, this method will only return the sizes for `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` for `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#` class.

If a well-defined format such as `NV21` is required, use `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(kotlin.Int)` instead.

The `klass` should be a supported output, that querying `isOutputSupportedFor(Class)` should return `true`.

| Parameters ||
|---|---|
| `klass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>!: a non-`null` `https://developer.android.com/reference/kotlin/java/lang/Class.html#` object reference |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/util/Size.html#!>!` | an array of supported sizes for `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` format, or `null` iff the `klass` is not a supported output. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `klass` was `null` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#isOutputSupportedFor(java.lang.Class)`

### getOutputStallDuration

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOutputStallDuration(
    format: Int, 
    size: Size!
): Long
```

Get the stall duration for the format/size combination (in nanoseconds).

`format` should be one of the ones returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputFormats()`.

`size` should be one of the ones returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(kotlin.Int)`.

A stall duration is how much extra time would get added to the normal minimum frame duration for a repeating request that has streams with non-zero stall.

For example, consider JPEG captures which have the following characteristics:

- JPEG streams act like processed YUV streams in requests for which they are not included; in requests in which they are directly referenced, they act as JPEG streams. This is because supporting a JPEG stream requires the underlying YUV data to always be ready for use by a JPEG encoder, but the encoder will only be used (and impact frame duration) on requests that actually reference a JPEG stream.
- The JPEG processor can run concurrently to the rest of the camera pipeline, but cannot process more than 1 capture at a time.

In other words, using a repeating YUV request would result in a steady frame rate (let's say it's 30 FPS). If a single JPEG request is submitted periodically, the frame rate will stay at 30 FPS (as long as we wait for the previous JPEG to return each time). If we try to submit a repeating YUV + JPEG request, then the frame rate will drop from 30 FPS.

In general, submitting a new request with a non-0 stall time stream will *not* cause a frame rate drop unless there are still outstanding buffers for that stream from previous requests.

Submitting a repeating request with streams (call this `S`) is the same as setting the minimum frame duration from the normal minimum frame duration corresponding to `S`, added with the maximum stall duration for `S`.

If interleaving requests with and without a stall duration, a request will stall by the maximum of the remaining times for each can-stall stream with outstanding buffers.

This means that a stalling request will not have an exposure start until the stall has completed.

This should correspond to the stall duration when only that stream is active, with all processing (typically in `android.*.mode`) set to `FAST` or `OFF`. Setting any of the processing modes to `HIGH_QUALITY` effectively results in an indeterminate stall duration for all streams in a request (the regular stall calculation rules are ignored).

The following formats may always have a stall duration:

- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_PRIVATE:kotlin.Int`

<br />

The following formats will never have a stall duration:

- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int`

<br />

All other formats may or may not have an allowed stall duration on a per-capability basis; refer to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` for more details.

<br />

See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` for more information about calculating the max frame rate (absent stalls).

| Parameters ||
|---|---|
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an image format from `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#` |
| `size` | [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!: an output-compatible size |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | a stall duration `>=` 0 in nanoseconds |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `format` or `size` was not supported |
| `java.lang.NullPointerException` | if `size` was `null` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#`
- `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#`

### getOutputStallDuration

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> getOutputStallDuration(
    klass: Class<T>!, 
    size: Size!
): Long
```

Get the stall duration for the class/size combination (in nanoseconds).

This assumes that the `klass` is set up to use `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int`. For user-defined formats, use `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputMinFrameDuration(kotlin.Int,%20android.util.Size)`.

`klass` should be one of the ones with a non-empty array returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(java.lang.Class)`.

`size` should be one of the ones returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(java.lang.Class)`.

See `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputStallDuration(kotlin.Int,%20android.util.Size)` for a definition of a *stall duration*.

| Parameters ||
|---|---|
| `klass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>!: a class which is supported by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#isOutputSupportedFor(java.lang.Class)` and has a non-empty array returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(java.lang.Class)` |
| `size` | [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!: an output-compatible size |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | a minimum frame duration `>=` 0 in nanoseconds |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `klass` or `size` was not supported |
| `java.lang.NullPointerException` | if `size` or `klass` was `null` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#`
- `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#`

### getValidOutputFormatsForInput

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getValidOutputFormatsForInput(inputFormat: Int): IntArray!
```

Get the image `format` output formats for a reprocessing input format.

When submitting a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#` with an input Surface of a given format, the only allowed target outputs of the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#` are the ones with a format listed in the return value of this method. Including any other output Surface as a target will throw an IllegalArgumentException. If no output format is supported given the input format, an empty int\[\] will be returned.

All image formats returned by this function will be defined in either `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or in `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#` (and there is no possibility of collision).

Formats listed in this array are guaranteed to return true if queried with `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#isOutputSupportedFor(kotlin.Int)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` | an array of integer format |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#`
- `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#`

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### isOutputSupportedFor

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isOutputSupportedFor(surface: Surface!): Boolean
```

Determine whether or not the `surface` in its current state is suitable to be included in a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)` as an output.

Not all surfaces are usable with the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#`, and not all configurations of that `surface` are compatible. Some classes that provide the `surface` are compatible with the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#` in general (see `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#isOutputSupportedFor(java.lang.Class)`, but it is the caller's responsibility to put the `surface` into a state that will be compatible with the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#`.

Reasons for a `surface` being specifically incompatible might be:

- Using a format that's not listed by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputFormats()`
- Using a format/size combination that's not listed by #getOutputSizes
- The `surface` itself is not in a state where it can service a new producer.

 <br />

Surfaces from flexible sources will return true even if the exact size of the Surface does not match a camera-supported size, as long as the format (or class) is supported and the camera device supports a size that is equal to or less than 1080p in that format. If such as Surface is used to create a capture session, it will have its size rounded to the nearest supported size, below or equal to 1080p. Flexible sources include SurfaceView, SurfaceTexture, and ImageReader.

This is not an exhaustive list; see the particular class's documentation for further possible reasons of incompatibility.

| Parameters ||
|---|---|
| `surface` | [Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#)!: a non-`null` `https://developer.android.com/reference/kotlin/android/view/Surface.html#` object reference |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this is supported, `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the Surface endpoint is no longer valid |
| `java.lang.NullPointerException` | if `surface` was `null` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#isOutputSupportedFor(java.lang.Class)`

### isOutputSupportedFor

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isOutputSupportedFor(format: Int): Boolean
```

Determine whether or not output surfaces with a particular user-defined format can be passed `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)`.

This method determines that the output `format` is supported by the camera device; each output `surface` target may or may not itself support that `format`. Refer to the class which provides the surface for additional documentation.

Formats for which this returns `true` are guaranteed to exist in the result returned by #getOutputSizes.

| Parameters ||
|---|---|
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an image format from either `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` iff using a `surface` with this `format` will be supported with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the image format was not a defined named constant from either `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#`
- `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)`

### isOutputSupportedFor

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> isOutputSupportedFor(klass: Class<T>!): Boolean
```

Determine whether or not output streams can be configured with a particular class as a consumer.

The following list is generally usable for outputs:

- `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#` - Recommended for image processing or streaming to external resources (such as a file or network)
- `https://developer.android.com/reference/kotlin/android/media/MediaRecorder.html#` - Recommended for recording video (simple to use)
- `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#` - Recommended for recording video (more complicated to use, with more flexibility)
- `https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.html#` - Recommended for low-power camera preview with `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#`
- `https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#` - Recommended for OpenGL-accelerated preview processing or compositing with `https://developer.android.com/reference/kotlin/android/view/TextureView.html#`

<br />

Generally speaking this means that creating a `https://developer.android.com/reference/kotlin/android/view/Surface.html#` from that class *may* provide a producer endpoint that is suitable to be used with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)`.

Since not all of the above classes support output of all format and size combinations, the particular combination should be queried with `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#isOutputSupportedFor(android.view.Surface)`.

| Parameters ||
|---|---|
| `klass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>!: a non-`null` `https://developer.android.com/reference/kotlin/java/lang/Class.html#` object reference |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this class is supported as an output, `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `klass` was `null` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#isOutputSupportedFor(android.view.Surface)`

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Return this `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#` as a string representation.

`"StreamConfigurationMap(Outputs([w:%d, h:%d, format:%s(%d), min_duration:%d, stall:%d], ... [w:%d, h:%d, format:%s(%d), min_duration:%d, stall:%d]), Inputs([w:%d, h:%d, format:%s(%d)], ... [w:%d, h:%d, format:%s(%d)]), ValidOutputFormatsForInput( [in:%d, out:%d, ... %d], ... [in:%d, out:%d, ... %d]), HighSpeedVideoConfigurations( [w:%d, h:%d, min_fps:%d, max_fps:%d], ... [w:%d, h:%d, min_fps:%d, max_fps:%d]))"`.

`Outputs([w:%d, h:%d, format:%s(%d), min_duration:%d, stall:%d], ... [w:%d, h:%d, format:%s(%d), min_duration:%d, stall:%d])`, where `[w:%d, h:%d, format:%s(%d), min_duration:%d, stall:%d]` represents an output configuration's width, height, format, minimal frame duration in nanoseconds, and stall duration in nanoseconds.

`Inputs([w:%d, h:%d, format:%s(%d)], ... [w:%d, h:%d, format:%s(%d)])`, where `[w:%d, h:%d, format:%s(%d)]` represents an input configuration's width, height, and format.

`ValidOutputFormatsForInput([in:%s(%d), out:%s(%d), ... %s(%d)], ... [in:%s(%d), out:%s(%d), ... %s(%d)])`, where `[in:%s(%d), out:%s(%d), ... %s(%d)]` represents an input format and its valid output formats.

`HighSpeedVideoConfigurations([w:%d, h:%d, min_fps:%d, max_fps:%d], ... [w:%d, h:%d, min_fps:%d, max_fps:%d])`, where `[w:%d, h:%d, min_fps:%d, max_fps:%d]` represents a high speed video output configuration's width, height, minimal frame rate, and maximal frame rate.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | string representation of `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#` |
