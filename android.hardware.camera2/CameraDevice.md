Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CameraDevice

```
abstract class CameraDevice : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.CameraDevice](CameraDevice.md) |

The CameraDevice class is a representation of a single camera connected to an Android device, allowing for fine-grain control of image capture and post-processing at high frame rates.

Your application must declare the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` permission in its manifest in order to access camera devices.

A given camera device may provide support at one of several levels defined in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`. If a device supports `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LEGACY:kotlin.Int` level, the camera device is running in backward compatibility mode and has minimum camera2 API support. If a device supports the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` level, then Camera2 exposes a feature set that is roughly equivalent to the older `https://developer.android.com/reference/kotlin/android/hardware/Camera.html#` API, although with a cleaner and more efficient interface. If a device supports the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_EXTERNAL:kotlin.Int` level, then the device is a removable camera that provides similar but slightly less features as the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` level. Devices that implement the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_3:kotlin.Int` level of support provide substantially improved capabilities over the older camera API. If your application requires a full-level device for proper operation, declare the "android.hardware.camera.level.full" feature in your manifest.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup` CameraDeviceSetup is a limited representation of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#` that can be used to query device specific information which would otherwise need a CameraDevice instance. |
| abstract | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.StateCallback` A callback objects for receiving updates about the state of a camera device. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#AUDIO_RESTRICTION_NONE:kotlin.Int` No vibration or sound muting for this camera device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#AUDIO_RESTRICTION_VIBRATION:kotlin.Int` Mute vibration from ringtones, alarms or notifications while this camera device is in use. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#AUDIO_RESTRICTION_VIBRATION_SOUND:kotlin.Int` Mute vibration and sound from ringtones, alarms or notifications while this camera device is in use. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_MANUAL:kotlin.Int` A basic template for direct application control of capture parameters. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_PREVIEW:kotlin.Int` Create a request suitable for a camera preview window. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_RECORD:kotlin.Int` Create a request suitable for video recording. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_STILL_CAPTURE:kotlin.Int` Create a request suitable for still image capture. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_VIDEO_SNAPSHOT:kotlin.Int` Create a request suitable for still image capture while recording video. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_ZERO_SHUTTER_LAG:kotlin.Int` Create a request suitable for zero shutter lag still capture. |
| --- | --- |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#close()()` Close the connection to this camera device as quickly as possible. |
| abstract [CaptureRequest.Builder](../android/hardware/camera2/CaptureRequest.Builder.md) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createCaptureRequest(kotlin.Int)(templateType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder` for new capture requests, initialized with template for a target use case. |
| open [CaptureRequest.Builder](../android/hardware/camera2/CaptureRequest.Builder.md) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createCaptureRequest(kotlin.Int,%20kotlin.collections.MutableSet)(templateType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, physicalCameraIdSet: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Create a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder` for new capture requests, initialized with template for a target use case. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)(config: https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration!)` Create a new `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession` using a `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration` helper object that aggregates all supported parameters. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createCaptureSession(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)(outputs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/view/Surface.html#!>, callback: https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?)` Create a new camera capture session by providing the target output set of Surfaces to the camera device. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createCaptureSessionByOutputConfigurations(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)(outputConfigurations: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration!>!, callback: https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?)` Create a new camera capture session by providing the target output set of Surfaces and its corresponding surface configuration to the camera device. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createConstrainedHighSpeedCaptureSession(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)(outputs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/view/Surface.html#!>, callback: https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?)` Create a new constrained high speed capture session. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createExtensionSession(android.hardware.camera2.params.ExtensionSessionConfiguration)(extensionConfiguration: https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ExtensionSessionConfiguration)` Initialize a specific device-specific extension augmented camera capture session. |
| abstract [CaptureRequest.Builder](../android/hardware/camera2/CaptureRequest.Builder.md) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createReprocessCaptureRequest(android.hardware.camera2.TotalCaptureResult)(inputResult: https://developer.android.com/reference/kotlin/android/hardware/camera2/TotalCaptureResult)` Create a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder` for a new reprocess `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest` from a `https://developer.android.com/reference/kotlin/android/hardware/camera2/TotalCaptureResult`. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createReprocessableCaptureSession(android.hardware.camera2.params.InputConfiguration,%20kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)(inputConfig: https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration, outputs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/view/Surface.html#!>, callback: https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?)` Create a new reprocessable camera capture session by providing the desired reprocessing input Surface configuration and the target output set of Surfaces to the camera device. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createReprocessableCaptureSessionByConfigurations(android.hardware.camera2.params.InputConfiguration,%20kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)(inputConfig: https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration, outputs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration!>, callback: https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?)` Create a new reprocessable camera capture session by providing the desired reprocessing input configuration and output `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration` to the camera device. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#getCameraAudioRestriction()()` Get currently applied global camera audio restriction mode. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#getId()()` Get the ID of this camera device. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#isSessionConfigurationSupported(android.hardware.camera2.params.SessionConfiguration)(sessionConfig: https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration)` Checks whether a particular `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration` is supported by the camera device. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#setCameraAudioRestriction(kotlin.Int)(mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set audio restriction mode when this CameraDevice is being used. |
| --- | --- |

## Constants

### AUDIO_RESTRICTION_NONE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_RESTRICTION_NONE: Int
```

No vibration or sound muting for this camera device. This is the default mode for all camera devices.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#setCameraAudioRestriction(kotlin.Int)`

### AUDIO_RESTRICTION_VIBRATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_RESTRICTION_VIBRATION: Int
```

Mute vibration from ringtones, alarms or notifications while this camera device is in use.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#setCameraAudioRestriction(kotlin.Int)`

### AUDIO_RESTRICTION_VIBRATION_SOUND

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_RESTRICTION_VIBRATION_SOUND: Int
```

Mute vibration and sound from ringtones, alarms or notifications while this camera device is in use.

As of API level 37, this option will also turn off any lights on the device if they are bright enough to interfere with camera photos or recordings.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#setCameraAudioRestriction(kotlin.Int)`

### TEMPLATE_MANUAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEMPLATE_MANUAL: Int
```

A basic template for direct application control of capture parameters. All automatic control is disabled (auto-exposure, auto-white balance, auto-focus), and post-processing parameters are set to preview quality. The manual capture parameters (exposure, sensitivity, and so on) are set to reasonable defaults, but should be overridden by the application depending on the intended use case. This template is guaranteed to be supported on camera devices that support the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_MANUAL_SENSOR:kotlin.Int` capability.

 Value: 6

**See Also**

### TEMPLATE_PREVIEW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEMPLATE_PREVIEW: Int
```

Create a request suitable for a camera preview window. Specifically, this means that high frame rate is given priority over the highest-quality post-processing. These requests would normally be used with the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)` method. This template is guaranteed to be supported on all camera devices.

 Value: 1

**See Also**

### TEMPLATE_RECORD

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEMPLATE_RECORD: Int
```

Create a request suitable for video recording. Specifically, this means that a stable frame rate is used, and post-processing is set for recording quality. These requests would commonly be used with the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)` method. This template is guaranteed to be supported on all camera devices except `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_DEPTH_OUTPUT:kotlin.Int` devices that are not `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_BACKWARD_COMPATIBLE:kotlin.Int`.

 Value: 3

**See Also**

### TEMPLATE_STILL_CAPTURE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEMPLATE_STILL_CAPTURE: Int
```

Create a request suitable for still image capture. Specifically, this means prioritizing image quality over frame rate. These requests would commonly be used with the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#capture(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)` method. This template is guaranteed to be supported on all camera devices except `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_DEPTH_OUTPUT:kotlin.Int` devices that are not `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_BACKWARD_COMPATIBLE:kotlin.Int`.

 Value: 2

**See Also**

### TEMPLATE_VIDEO_SNAPSHOT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEMPLATE_VIDEO_SNAPSHOT: Int
```

Create a request suitable for still image capture while recording video. Specifically, this means maximizing image quality without disrupting the ongoing recording. These requests would commonly be used with the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#capture(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)` method while a request based on `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_RECORD:kotlin.Int` is is in use with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`. This template is guaranteed to be supported on all camera devices except legacy devices (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` `== ``https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LEGACY:kotlin.Int`) and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_DEPTH_OUTPUT:kotlin.Int` devices that are not `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_BACKWARD_COMPATIBLE:kotlin.Int`.

 Value: 4

**See Also**

### TEMPLATE_ZERO_SHUTTER_LAG

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TEMPLATE_ZERO_SHUTTER_LAG: Int
```

Create a request suitable for zero shutter lag still capture. This means means maximizing image quality without compromising preview frame rate. AE/AWB/AF should be on auto mode. This is intended for application-operated ZSL. For device-operated ZSL, use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ENABLE_ZSL:android.hardware.camera2.CaptureRequest.Key` if available. This template is guaranteed to be supported on camera devices that support the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_PRIVATE_REPROCESSING:kotlin.Int` capability or the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_YUV_REPROCESSING:kotlin.Int` capability.

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ENABLE_ZSL:android.hardware.camera2.CaptureRequest.Key`

## Public methods

### close

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun close(): Unit
```

Close the connection to this camera device as quickly as possible.

Immediately after this call, all calls to the camera device or active session interface will throw a `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`, except for calls to close(). Once the device has fully shut down, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.StateCallback#onClosed(android.hardware.camera2.CameraDevice)` callback will be called, and the camera is free to be re-opened.

Immediately after this call, besides the final `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.StateCallback#onClosed(android.hardware.camera2.CameraDevice)` calls, no further callbacks from the device or the active session will occur, and any remaining submitted capture requests will be discarded, as if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#abortCaptures()` had been called, except that no success or failure callbacks will be invoked.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |

### createCaptureRequest

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun createCaptureRequest(templateType: Int): CaptureRequest.Builder
```

Create a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder` for new capture requests, initialized with template for a target use case. The settings are chosen to be the best options for the specific camera device, so it is not recommended to reuse the same request for a different camera device; create a builder specific for that device and template and override the settings as desired, instead.

| Parameters ||
|---|---|
| `templateType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An enumeration selecting the use case for this request. Not all template types are supported on every device. See the documentation for each template type for details. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_PREVIEW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_STILL_CAPTURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_RECORD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_VIDEO_SNAPSHOT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_ZERO_SHUTTER_LAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_MANUAL:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder` | a builder for a capture request, initialized with default settings for that template, and no output streams. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalArgumentException` | if the templateType is not supported by this device. |
| `java.lang.IllegalStateException` | if the camera device has been closed |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if this is not a primary client of a camera opened in shared mode |

### createCaptureRequest

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createCaptureRequest(
    templateType: Int, 
    physicalCameraIdSet: MutableSet<String!>!
): CaptureRequest.Builder
```

Create a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder` for new capture requests, initialized with template for a target use case. This methods allows clients to pass physical camera ids which can be used to customize the request for a specific physical camera. The settings are chosen to be the best options for the specific logical camera device. If additional physical camera ids are passed, then they will also use the same settings template. Clients can further modify individual camera settings by calling `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder#setPhysicalCameraKey(android.hardware.camera2.CaptureRequest.Key,%20android.hardware.camera2.CaptureRequest.Builder.setPhysicalCameraKey.T,%20kotlin.String)`.

Individual physical camera settings will only be honored for camera session that was initialized with corresponding physical camera id output configuration `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#setPhysicalCameraId(kotlin.String)` and the same output targets are also attached in the request by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder#addTarget(android.view.Surface)`.

The output is undefined for any logical camera streams in case valid physical camera settings are attached.

| Parameters ||
|---|---|
| `templateType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An enumeration selecting the use case for this request. Not all template types are supported on every device. See the documentation for each template type for details. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_PREVIEW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_STILL_CAPTURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_RECORD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_VIDEO_SNAPSHOT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_ZERO_SHUTTER_LAG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_MANUAL:kotlin.Int` |
| `physicalCameraIdSet` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: A set of physical camera ids that can be used to customize the request for a specific physical camera. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder` | a builder for a capture request, initialized with default settings for that template, and no output streams. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalArgumentException` | if the templateType is not supported by this device, or one of the physical id arguments matches with logical camera id. |
| `java.lang.IllegalStateException` | if the camera device has been closed |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if this is not a primary client of a camera opened in shared mode |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_PREVIEW:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_RECORD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_STILL_CAPTURE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_VIDEO_SNAPSHOT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#TEMPLATE_MANUAL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder#setPhysicalCameraKey(android.hardware.camera2.CaptureRequest.Key,%20android.hardware.camera2.CaptureRequest.Builder.setPhysicalCameraKey.T,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder#getPhysicalCameraKey(android.hardware.camera2.CaptureRequest.Key,%20kotlin.String)`

### createCaptureSession

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createCaptureSession(config: SessionConfiguration!): Unit
```

Create a new `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession` using a `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration` helper object that aggregates all supported parameters.

The active capture session determines the set of potential output Surfaces for the camera device for each capture request. A given request may use all or only some of the outputs. Once the CameraCaptureSession is created, requests can be submitted with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#capture(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#captureBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`, or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`.

Surfaces suitable for inclusion as a camera output can be created for various use cases and targets:

- For drawing to a `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#`: Once the SurfaceView's Surface is `https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.Callback.html#surfaceCreated(android.view.SurfaceHolder)`, set the size of the Surface with `https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.html#setFixedSize(kotlin.Int,%20kotlin.Int)` to be one of the sizes returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(java.lang.Class)` and then obtain the Surface by calling `https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.html#getSurface()`. If the size is not set by the application, it will be rounded to the nearest supported size less than 1080p, by the camera device.
- For accessing through an OpenGL texture via a `https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#`: Set the size of the SurfaceTexture with `https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#setDefaultBufferSize(kotlin.Int,%20kotlin.Int)` to be one of the sizes returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(java.lang.Class)` before creating a Surface from the SurfaceTexture with `https://developer.android.com/reference/kotlin/android/view/Surface.html#Surface(android.graphics.SurfaceTexture)`. If the size is not set by the application, it will be set to be the smallest supported size less than 1080p, by the camera device.
- For recording with `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#`: Call `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#createInputSurface()` after configuring the media codec to use one of the sizes returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(java.lang.Class)`
- For recording with `https://developer.android.com/reference/kotlin/android/media/MediaRecorder.html#`: Call `https://developer.android.com/reference/kotlin/android/media/MediaRecorder.html#getSurface()` after configuring the media recorder to use one of the sizes returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(java.lang.Class)`, or configuring it to use one of the supported `https://developer.android.com/reference/kotlin/android/media/CamcorderProfile.html#`.
- For access to RAW, uncompressed YUV, or compressed JPEG data in the application: Create an `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#` object with one of the supported output formats given by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputFormats()`, setting its size to one of the corresponding supported sizes by passing the chosen output format into `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(kotlin.Int)`. Then obtain a `https://developer.android.com/reference/kotlin/android/view/Surface.html#` from it with `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#getSurface()`. If the ImageReader size is not set to a supported size, it will be rounded to a supported size less than 1080p by the camera device.

The camera device will query each Surface's size and formats upon this call, so they must be set to a valid setting at this time.

It can take several hundred milliseconds for the session's configuration to complete, since camera hardware may need to be powered on or reconfigured. Once the configuration is complete and the session is ready to actually capture data, the provided `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback`'s `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback#onConfigured(android.hardware.camera2.CameraCaptureSession)` callback will be called.

If a prior CameraCaptureSession already exists when this method is called, the previous session will no longer be able to accept new capture requests and will be closed. Any in-progress capture requests made on the prior session will be completed before it's closed. `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback#onConfigured(android.hardware.camera2.CameraCaptureSession)` for the new session may be invoked before `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback#onClosed(android.hardware.camera2.CameraCaptureSession)` is invoked for the prior session. Once the new session is `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback#onConfigured(android.hardware.camera2.CameraCaptureSession)`, it is able to start capturing its own requests. To minimize the transition time, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#abortCaptures()` call can be used to discard the remaining requests for the prior capture session before a new one is created. Note that once the new session is created, the old one can no longer have its captures aborted.

Using larger resolution outputs, or more outputs, can result in slower output rate from the device.

Configuring a session with an empty or null list will close the current session, if any. This can be used to release the current session's target surfaces for another use.

This function throws an `IllegalArgumentException` if called with a SessionConfiguration lacking state callbacks or valid output surfaces. The only exceptions are deferred SurfaceView or SurfaceTexture outputs. See `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#OutputConfiguration(android.util.Size,%20java.lang.Class)` for details.

### Regular capture

While any of the sizes from android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes can be used when a single output stream is configured, a given camera device may not be able to support all combination of sizes, formats, and targets when multiple outputs are configured at once. The tables below list the maximum guaranteed resolutions for combinations of streams and targets, given the capabilities of the camera device. These are valid for when the `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setInputConfiguration(android.hardware.camera2.params.InputConfiguration)` is not set and therefore no reprocessing is active.

If an application tries to create a session using a set of targets that exceed the limits described in the below tables, one of three possibilities may occur. First, the session may be successfully created and work normally. Second, the session may be successfully created, but the camera device won't meet the frame rate guarantees as described in android.hardware.camera2.params.StreamConfigurationMap#getOutputMinFrameDuration. Or third, if the output set cannot be used at all, session creation will fail entirely, with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.StateCallback#onConfigureFailed(android.hardware.camera2.CameraCaptureSession)` being invoked.

For the type column, `PRIV` refers to any target whose available sizes are found using `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(java.lang.Class)` with no direct application-visible format, `YUV` refers to a target Surface using the `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` format, `JPEG` refers to the `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` format, and `RAW` refers to the `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` format.

For the maximum size column, `PREVIEW` refers to the best size match to the device's screen resolution, or to 1080p (`1920x1080`), whichever is smaller. `RECORD` refers to the camera device's maximum supported recording resolution, as determined by `https://developer.android.com/reference/kotlin/android/media/CamcorderProfile.html#`. And `MAXIMUM` refers to the camera device's maximum output resolution for that format or target from android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes.

To use these tables, determine the number and the formats/targets of outputs needed, and find the row(s) of the table with those targets. The sizes indicate the maximum set of sizes that can be used; it is guaranteed that for those targets, the listed sizes and anything smaller from the list given by android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes can be successfully used to create a session. For example, if a row indicates that a 8 megapixel (MP) YUV_420_888 output can be used together with a 2 MP `PRIV` output, then a session can be created with targets `[8 MP YUV, 2 MP PRIV]` or targets `[2 MP YUV, 2 MP PRIV]`; but a session with targets `[8 MP YUV, 4 MP PRIV]`, targets `[4 MP YUV, 4 MP PRIV]`, or targets `[8 MP PRIV, 2 MP YUV]` would not be guaranteed to work, unless some other row of the table lists such a combination.

##### LEGACY-level guaranteed configurations

Legacy devices (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` `== ``https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LEGACY:kotlin.Int`) support at least the following stream combinations:

| Target 1 || Target 2 || Target 3 || Sample use case(s) |
| --- | --- | --- | --- | --- | --- | --- |
| Type | Max size | Type | Max size | Type | Max size | Sample use case(s) |
|---|---|---|---|---|---|---|
| `PRIV` | `MAXIMUM` | || || Simple preview, GPU video processing, or no-preview video recording. |
| `JPEG` | `MAXIMUM` | || || No-viewfinder still image capture. |
| `YUV ` | `MAXIMUM` | || || In-application video/image processing. |
| --- | --- | --- | --- | --- | --- | --- |
| `PRIV` | `PREVIEW` | `JPEG` | `MAXIMUM` | || Standard still imaging. |
| `YUV ` | `PREVIEW` | `JPEG` | `MAXIMUM` | || In-app processing plus still capture. |
| `PRIV` | `PREVIEW` | `PRIV` | `PREVIEW` | || Standard recording. |
| --- | --- | --- | --- | --- | --- | --- |
| `PRIV` | `PREVIEW` | `YUV ` | `PREVIEW` | || Preview plus in-app processing. |
| `PRIV` | `PREVIEW` | `YUV ` | `PREVIEW` | `JPEG` | `MAXIMUM` | Still capture plus in-app processing. |

<br />

<br />

##### LIMITED-level additional guaranteed configurations

Limited-level (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` `== ``https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int`) devices support at least the following stream combinations in addition to those for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LEGACY:kotlin.Int` devices:

| Target 1 || Target 2 || Target 3 || Sample use case(s) |
| --- | --- | --- | --- | --- | --- | --- |
| Type | Max size | Type | Max size | Type | Max size | Sample use case(s) |
|---|---|---|---|---|---|---|
| `PRIV` | `PREVIEW` | `PRIV` | `RECORD ` | || High-resolution video recording with preview. |
| `PRIV` | `PREVIEW` | `YUV ` | `RECORD ` | || High-resolution in-app video processing with preview. |
| `YUV ` | `PREVIEW` | `YUV ` | `RECORD ` | || Two-input in-app video processing. |
| --- | --- | --- | --- | --- | --- | --- |
| `PRIV` | `PREVIEW` | `PRIV` | `RECORD ` | `JPEG` | `RECORD ` | High-resolution recording with video snapshot. |
| `PRIV` | `PREVIEW` | `YUV ` | `RECORD ` | `JPEG` | `RECORD ` | High-resolution in-app processing with video snapshot. |
| `YUV ` | `PREVIEW` | `YUV ` | `PREVIEW` | `JPEG` | `MAXIMUM` | Two-input in-app processing with still capture. |
| --- | --- | --- | --- | --- | --- | --- |

<br />

<br />

##### FULL-level additional guaranteed configurations

FULL-level (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` `== ``https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int`) devices support at least the following stream combinations in addition to those for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices:

| Target 1 || Target 2 || Target 3 || Sample use case(s) |
| --- | --- | --- | --- | --- | --- | --- |
| Type | Max size | Type | Max size | Type | Max size | Sample use case(s) |
|---|---|---|---|---|---|---|
| `PRIV` | `PREVIEW` | `PRIV` | `MAXIMUM` | || Maximum-resolution GPU processing with preview. |
| `PRIV` | `PREVIEW` | `YUV ` | `MAXIMUM` | || Maximum-resolution in-app processing with preview. |
| `YUV ` | `PREVIEW` | `YUV ` | `MAXIMUM` | || Maximum-resolution two-input in-app processing. |
| --- | --- | --- | --- | --- | --- | --- |
| `PRIV` | `PREVIEW` | `PRIV` | `PREVIEW` | `JPEG` | `MAXIMUM` | Video recording with maximum-size video snapshot |
| `YUV ` | `640x480` | `PRIV` | `PREVIEW` | `YUV ` | `MAXIMUM` | Standard video recording plus maximum-resolution in-app processing. |
| `YUV ` | `640x480` | `YUV ` | `PREVIEW` | `YUV ` | `MAXIMUM` | Preview plus two-input maximum-resolution in-app processing. |
| --- | --- | --- | --- | --- | --- | --- |

<br />

<br />

##### RAW-capability additional guaranteed configurations

RAW-capability (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` includes `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_RAW:kotlin.Int`) devices additionally support at least the following stream combinations on both `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices:

| Target 1 || Target 2 || Target 3 || Sample use case(s) |
| --- | --- | --- | --- | --- | --- | --- |
| Type | Max size | Type | Max size | Type | Max size | Sample use case(s) |
|---|---|---|---|---|---|---|
| `RAW ` | `MAXIMUM` | || || No-preview DNG capture. |
| `PRIV` | `PREVIEW` | `RAW ` | `MAXIMUM` | || Standard DNG capture. |
| `YUV ` | `PREVIEW` | `RAW ` | `MAXIMUM` | || In-app processing plus DNG capture. |
| --- | --- | --- | --- | --- | --- | --- |
| `PRIV` | `PREVIEW` | `PRIV` | `PREVIEW` | `RAW ` | `MAXIMUM` | Video recording with DNG capture. |
| `PRIV` | `PREVIEW` | `YUV ` | `PREVIEW` | `RAW ` | `MAXIMUM` | Preview with in-app processing and DNG capture. |
| `YUV ` | `PREVIEW` | `YUV ` | `PREVIEW` | `RAW ` | `MAXIMUM` | Two-input in-app processing plus DNG capture. |
| --- | --- | --- | --- | --- | --- | --- |
| `PRIV` | `PREVIEW` | `JPEG` | `MAXIMUM` | `RAW ` | `MAXIMUM` | Still capture with simultaneous JPEG and DNG. |
| `YUV ` | `PREVIEW` | `JPEG` | `MAXIMUM` | `RAW ` | `MAXIMUM` | In-app processing with simultaneous JPEG and DNG. |

<br />

<br />

##### BURST-capability additional guaranteed configurations

BURST-capability (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` includes `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_BURST_CAPTURE:kotlin.Int`) devices support at least the below stream combinations in addition to those for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices. Note that all FULL-level devices support the BURST capability, and the below list is a strict subset of the list for FULL-level devices, so this table is only relevant for LIMITED-level devices that support the BURST_CAPTURE capability.

| Target 1 || Target 2 || Sample use case(s) |
| --- | --- | --- | --- | --- |
| Type | Max size | Type | Max size | Sample use case(s) |
|---|---|---|---|---|
| `PRIV` | `PREVIEW` | `PRIV` | `MAXIMUM` | Maximum-resolution GPU processing with preview. |
| `PRIV` | `PREVIEW` | `YUV ` | `MAXIMUM` | Maximum-resolution in-app processing with preview. |
| `YUV ` | `PREVIEW` | `YUV ` | `MAXIMUM` | Maximum-resolution two-input in-app processing. |
| --- | --- | --- | --- | --- |

<br />

<br />

##### LEVEL-3 additional guaranteed configurations

LEVEL-3 (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` `== ``https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_3:kotlin.Int`) support at least the following stream combinations in addition to the combinations for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` and for RAW capability (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` includes `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_RAW:kotlin.Int`):

| Target 1 || Target 2 || Target 3 || Target 4 || Sample use case(s) |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Type | Max size | Type | Max size | Type | Max size | Type | Max size | Sample use case(s) |
|---|---|---|---|---|---|---|---|---|
| `PRIV` | `PREVIEW` | `PRIV` | `640x480` | `YUV` | `MAXIMUM` | `RAW` | `MAXIMUM` | In-app viewfinder analysis with dynamic selection of output format. |
| `PRIV` | `PREVIEW` | `PRIV` | `640x480` | `JPEG` | `MAXIMUM` | `RAW` | `MAXIMUM` | In-app viewfinder analysis with dynamic selection of output format. |

<br />

<br />

##### Concurrent stream guaranteed configurations

BACKWARD_COMPATIBLE devices capable of streaming concurrently with other devices as described by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getConcurrentCameraIds()` have the following guaranteed streams (when streaming concurrently with other devices)

Note: The sizes mentioned for these concurrent streams are the maximum sizes guaranteed to be supported. Sizes smaller than these, obtained by android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes for a particular format, are supported as well.

| Target 1 || Target 2 || Sample use case(s) |
| --- | --- | --- | --- | --- |
| Type | Max size | Type | Max size | Sample use case(s) |
|---|---|---|---|---|
| `YUV` | `s1440p` | || In-app video / image processing. |
| `PRIV` | `s1440p` | || In-app viewfinder analysis. |
| `JPEG` | `s1440p` | || No viewfinder still image capture. |
| --- | --- | --- | --- | --- |
| `YUV / PRIV` | `s720p` | `JPEG` | `s1440p` | Standard still imaging. |
| `YUV / PRIV` | `s720p` | `YUV / PRIV ` | `s1440p` | In-app video / processing with preview. |

<br />

<br />

Devices which are not backwards-compatible, support a mandatory single stream of size sVGA with image format `DEPTH16` during concurrent operation.

For guaranteed concurrent stream configurations:

sVGA refers to the camera device's maximum resolution for that format from android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes or VGA resolution (640X480) whichever is lower.

s720p refers to the camera device's maximum resolution for that format from android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes or 720p(1280X720) whichever is lower.

s1440p refers to the camera device's maximum resolution for that format from android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes or 1440p(1920X1440) whichever is lower.

MONOCHROME-capability (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` includes `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_MONOCHROME:kotlin.Int`) devices supporting `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int` support substituting `YUV` streams with `Y8` in all guaranteed stream combinations for the device's hardware level and capabilities.

Clients can access the above mandatory stream combination tables via `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination`.

Devices capable of outputting HEIC formats (`https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputFormats()` contains `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#HEIC:kotlin.Int`) will support substituting `JPEG` streams with `HEIC` in all guaranteed stream combinations for the device's hardware level and capabilities. Calling createCaptureSession with both JPEG and HEIC outputs is not supported.

##### LEGACY-level additional guaranteed combinations with multi-resolution outputs

Devices capable of multi-resolution output for a particular format ( `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MultiResolutionStreamConfigurationMap#getOutputInfo(kotlin.Int)` returns a non-empty list) support using `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader` for MAXIMUM resolution streams of that format for all mandatory stream combinations. For example, if a LIMITED camera device supports multi-resolution output streams for both `JPEG` and `PRIVATE`, in addition to the stream configurations in the LIMITED and Legacy table above, the camera device supports the following guaranteed stream combinations (`MULTI_RES` in the Max size column refers to a `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader` created based on the variable max resolutions supported):

| Target 1 || Target 2 || Target 3 || Sample use case(s) |
| --- | --- | --- | --- | --- | --- | --- |
| Type | Max size | Type | Max size | Type | Max size | Sample use case(s) |
|---|---|---|---|---|---|---|
| `PRIV` | `MULTI_RES` | || || Simple preview, GPU video processing, or no-preview video recording. |
| `JPEG` | `MULTI_RES` | || || No-viewfinder still image capture. |
| `PRIV` | `PREVIEW` | `JPEG` | `MULTI_RES` | || Standard still imaging. |
| --- | --- | --- | --- | --- | --- | --- |
| `PRIV` | `PREVIEW` | `YUV ` | `PREVIEW` | `JPEG` | `MULTI_RES` | Still capture plus in-app processing. |

<br />

<br />

##### LIMITED-level additional guaranteed configurations with multi-resolution outputs

| Target 1 || Target 2 || Target 3 || Sample use case(s) |
| --- | --- | --- | --- | --- | --- | --- |
| Type | Max size | Type | Max size | Type | Max size | Sample use case(s) |
|---|---|---|---|---|---|---|
| `YUV ` | `PREVIEW` | `YUV ` | `PREVIEW` | `JPEG` | `MULTI_RES` | Two-input in-app processing with still capture. |

<br />

The same logic applies to other hardware levels and capabilities.

<br />

##### Additional guaranteed combinations for ULTRA_HIGH_RESOLUTION sensors

Devices with the ULTRA_HIGH_RESOLUTION_SENSOR capability have some additional guarantees which clients can take advantage of:

| Target 1 ||| Target 2 ||| Target 3 ||| Sample use case(s) |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Type | SC Map | Max size | Type | SC Map | Max size | Type | SC Map | Max size | Sample use case(s) |
|---|---|---|---|---|---|---|---|---|---|
| `YUV / JPEG / RAW` | `MAX_RES` | `MAX` | `PRIV / YUV` | `DEFAULT` | `PREVIEW` | ||| Ultra high res still image capture with preview |
| `YUV / JPEG / RAW` | `MAX_RES` | `MAX` | `PRIV` | `DEFAULT` | `PREVIEW` | `PRIV / YUV` | `DEFAULT` | `RECORD` | Ultra high res still capture with preview + app based RECORD size analysis |
| `YUV / JPEG / RAW` | `MAX_RES` | `MAX` | `PRIV` | `DEFAULT` | `PREVIEW` | `JPEG / YUV / RAW` | `DEFAULT` | `MAX` | Ultra high res still image capture with preview + default sensor pixel mode analysis stream |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

<br />

<br />

Here, SC Map, refers to the `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap`, the target stream sizes must be chosen from. `DEFAULT` refers to the default sensor pixel mode `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap` and `MAX_RES` refers to the maximum resolution `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap`. For `MAX_RES` streams, `MAX` in the `Max size` column refers to the maximum size from android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes and `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighResolutionOutputSizes(kotlin.Int)`. Note: The same capture request must not mix targets from `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap`s corresponding to different sensor pixel modes.

##### 10-bit output additional guaranteed configurations

10-bit output capable `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_DYNAMIC_RANGE_TEN_BIT:kotlin.Int` devices support at least the following stream combinations:

| Target 1 || Target 2 || Target 3 || Sample use case(s) |
| --- | --- | --- | --- | --- | --- | --- |
| Type | Max size | Type | Max size | Type | Max size | Sample use case(s) |
|---|---|---|---|---|---|---|
| `PRIV` | `MAXIMUM` | |||| Simple preview, GPU video processing, or no-preview video recording. |
| `YUV` | `MAXIMUM` | |||| In-application video/image processing. |
| `PRIV` | `PREVIEW` | `JPEG` | `MAXIMUM ` | || Standard still imaging. |
| --- | --- | --- | --- | --- | --- | --- |
| `PRIV` | `PREVIEW` | `YUV ` | `MAXIMUM ` | || Maximum-resolution in-app processing with preview. |
| `YUV` | `PREVIEW` | `YUV` | `MAXIMUM ` | || Maximum-resolution two-input in-app processing. |
| `PRIV` | `PREVIEW` | `PRIV` | `RECORD ` | || High-resolution video recording with preview. |
| --- | --- | --- | --- | --- | --- | --- |
| `PRIV` | `PREVIEW` | `PRIV` | `RECORD ` | `YUV` | `RECORD ` | High-resolution recording with in-app snapshot. |
| `PRIV` | `PREVIEW` | `PRIV ` | `RECORD ` | `JPEG` | `RECORD ` | High-resolution recording with video snapshot. |

<br />

<br />

Here PRIV can be either 8 or 10-bit `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` pixel format. YUV can be either `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P010:kotlin.Int`. For the maximum size column, PREVIEW refers to the best size match to the device's screen resolution, or to 1080p (1920x1080), whichever is smaller. RECORD refers to the camera device's maximum supported recording resolution, as determined by `https://developer.android.com/reference/kotlin/android/media/CamcorderProfile.html#`. MAXIMUM refers to the camera device's maximum output resolution for that format or target from `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(kotlin.Int)`. Do note that invalid combinations such as having a camera surface configured to use pixel format `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` with a 10-bit profile will cause a capture session initialization failure.

`https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG_R:kotlin.Int` may also be supported if advertised by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap`. When initializing a capture session that includes a Jpeg/R camera output clients must consider the following items w.r.t. the 10-bit mandatory stream combination table:

- To generate the compressed Jpeg/R image a single `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P010:kotlin.Int` output will be used internally by the camera device.
- On camera devices that are able to support concurrent 10 and 8-bit capture requests see `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#getProfileCaptureRequestConstraints(kotlin.Long)` an extra `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` will also be configured internally to help speed up the encoding process.

Jpeg/R camera outputs will typically be able to support the MAXIMUM device resolution. Clients can also call `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(kotlin.Int)` for a complete list supported sizes. Camera clients that register a Jpeg/R output within a stream combination that doesn't fit in the mandatory stream table above can call `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#isSessionConfigurationSupported(android.hardware.camera2.params.SessionConfiguration)` to ensure that this particular configuration is supported.

<br />

##### STREAM_USE_CASE capability additional guaranteed configurations

Devices with the STREAM_USE_CASE capability (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` includes `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_STREAM_USE_CASE:kotlin.Int`) support below additional stream combinations:

| Target 1 ||| Target 2 ||| Target 3 ||| Sample use case(s) |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Type | Max size | Usecase | Type | Max size | Usecase | Type | Max size | Usecase | Sample use case(s) |
|---|---|---|---|---|---|---|---|---|---|
| `YUV / PRIV` | `PREVIEW` | `PREVIEW` | ||| ||| Simple preview or in-app image processing |
| `YUV / PRIV` | `RECORD` | `VIDEO_RECORD` | ||| ||| Simple video recording or in-app video processing |
| `YUV / JPEG` | `MAXIMUM` | `STILL_CAPTURE` | ||| ||| Simple JPEG or YUV still image capture |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `YUV / PRIV` | `s1440p` | `PREVIEW_VIDEO_STILL` | ||| ||| Multi-purpose stream for preview, video and still image capture |
| `YUV / PRIV` | `s1440p` | `VIDEO_CALL` | ||| ||| Simple video call |
| `PRIV` | `PREVIEW` | `PREVIEW` | `YUV / JPEG` | `MAXIMUM` | `STILL_CAPTURE` | ||| Preview with JPEG or YUV still image capture |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `PRIV` | `PREVIEW` | `PREVIEW` | `YUV / PRIV` | `RECORD` | `VIDEO_RECORD` | ||| Preview with video recording or in-app video processing |
| `PRIV` | `PREVIEW` | `PREVIEW` | `YUV` | `PREVIEW` | `PREVIEW` | ||| Preview with in-application image processing |
| `PRIV` | `PREVIEW` | `PREVIEW` | `YUV / PRIV` | `s1440p` | `VIDEO_CALL` | ||| Preview with video call |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `YUV / PRIV` | `s1440p` | `PREVIEW_VIDEO_STILL` | `YUV / JPEG` | `MAXIMUM` | `STILL_CAPTURE` | ||| MultI-purpose stream with JPEG or YUV still capture |
| `YUV` | `PREVIEW` | `STILL_CAPTURE` | `JPEG` | `MAXIMUM` | `STILL_CAPTURE` | ||| YUV and JPEG concurrent still image capture (for testing) |
| `PRIV` | `PREVIEW` | `PREVIEW` | `YUV / PRIV` | `RECORD` | `VIDEO_RECORD` | `JPEG` | `RECORD` | `STILL_CAPTURE` | Preview, video record and JPEG video snapshot |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `PRIV` | `PREVIEW` | `PREVIEW` | `YUV` | `PREVIEW` | `PREVIEW` | `JPEG` | `MAXIMUM` | `STILL_CAPTURE` | Preview, in-application image processing, and JPEG still image capture |

<br />

<br />

##### STREAM_USE_CASE_CROPPED_RAW capability additional guaranteed configurations

Devices that include the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_CROPPED_RAW:kotlin.Int` stream use-case in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_STREAM_USE_CASES:android.hardware.camera2.CameraCharacteristics.Key`, support the additional stream combinations below:

| Target 1 ||| Target 2 ||| Target 3 ||| Sample use case(s) |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Type | Max size | Usecase | Type | Max size | Usecase | Type | Max size | Usecase | Sample use case(s) |
|---|---|---|---|---|---|---|---|---|---|
| `RAW` | `MAXIMUM` | `CROPPED_RAW` | ||| ||| Cropped RAW still capture without preview |
| `PRIV / YUV` | `PREVIEW` | `PREVIEW` | `RAW` | `MAXIMUM` | `CROPPED_RAW` | ||| Preview with cropped RAW still capture |
| `PRIV / YUV` | `PREVIEW` | `PREVIEW` | `YUV / JPEG` | `MAXIMUM` | `STILL_CAPTURE` | `RAW` | `MAXIMUM` | `CROPPED_RAW` | Preview with YUV / JPEG and cropped RAW still capture |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `PRIV / YUV` | `PREVIEW` | `PREVIEW` | `PRIV / YUV` | `PREVIEW` | `VIDEO_RECORD / PREVIEW` | `RAW` | `MAXIMUM` | `CROPPED_RAW` | Video recording with preview and cropped RAW still capture |

<br />

<br />

##### Preview stabilization guaranteed stream configurations

For devices where `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_VIDEO_STABILIZATION_MODES:android.hardware.camera2.CameraCharacteristics.Key` includes `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_VIDEO_STABILIZATION_MODE_PREVIEW_STABILIZATION:kotlin.Int`, the following stream combinations are guaranteed, for CaptureRequests where `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_VIDEO_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key` is set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_VIDEO_STABILIZATION_MODE_PREVIEW_STABILIZATION:kotlin.Int`

| Target 1 || Target 2 || Sample use case(s) |
| --- | --- | --- | --- | --- |
| Type | Max size | Type | Max size | Sample use case(s) |
|---|---|---|---|---|
| `PRIV / YUV` | `s1440p` | || Stabilized preview, GPU video processing, or no-preview stabilized video recording. |
| `PRIV / YUV` | `s1440p` | `JPEG / YUV` | `MAXIMUM ` | Standard still imaging with stabilized preview. |
| `PRIV / YUV` | `PREVIEW` | `PRIV / YUV` | `s1440p ` | High-resolution recording with stabilized preview and recording stream. |
| --- | --- | --- | --- | --- |

<br />

<br />

For the maximum size column, PREVIEW refers to the best size match to the device's screen resolution, or to 1080p (1920x1080), whichever is smaller. RECORD refers to the camera device's maximum supported recording resolution, as determined by `https://developer.android.com/reference/kotlin/android/media/CamcorderProfile.html#`. MAXIMUM refers to the camera device's maximum output resolution for that format or target from `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(kotlin.Int)`.

Since the capabilities of camera devices vary greatly, a given camera device may support target combinations with sizes outside of these guarantees, but this can only be tested for by calling `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#isSessionConfigurationSupported(android.hardware.camera2.params.SessionConfiguration)` or attempting to create a session with such targets.

Exception on 176x144 (QCIF) resolution: Camera devices usually have a fixed capability for downscaling from larger resolution to smaller, and the QCIF resolution sometimes is not fully supported due to this limitation on devices with high-resolution image sensors. Therefore, trying to configure a QCIF resolution stream together with any other stream larger than 1920x1080 resolution (either width or height) might not be supported, and capture session creation will fail if it is not.

### Reprocessing

If a camera device supports YUV reprocessing (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_YUV_REPROCESSING:kotlin.Int`) or PRIVATE reprocessing (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_PRIVATE_REPROCESSING:kotlin.Int`), the application can also create a reprocessable capture session to submit reprocess capture requests in addition to regular capture requests, by setting an `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setInputConfiguration(android.hardware.camera2.params.InputConfiguration)` for the session. A reprocess capture request takes the next available buffer from the session's input Surface, and sends it through the camera device's processing pipeline again, to produce buffers for the request's target output Surfaces. No new image data is captured for a reprocess request. However the input buffer provided by the application must be captured previously by the same camera device in the same session directly (e.g. for Zero-Shutter-Lag use case) or indirectly (e.g. combining multiple output images).

The active reprocessable capture session determines an input `https://developer.android.com/reference/kotlin/android/view/Surface.html#` and the set of potential output Surfaces for the camera devices for each capture request. The application can use #createCaptureRequest to create regular capture requests to capture new images from the camera device, and use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createReprocessCaptureRequest(android.hardware.camera2.TotalCaptureResult)` to create reprocess capture requests to process buffers from the input `https://developer.android.com/reference/kotlin/android/view/Surface.html#`. Some combinations of output Surfaces in a session may not be used in a request simultaneously. The guaranteed combinations of output Surfaces that can be used in a request simultaneously are listed in the tables under #createCaptureSession. All the output Surfaces in one capture request will come from the same source, either from a new capture by the camera device, or from the input Surface depending on if the request is a reprocess capture request.

Input formats and sizes supported by the camera device can be queried via `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputSizes(kotlin.Int)`. For each supported input format, the camera device supports a set of output formats and sizes for reprocessing that can be queried via `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getValidOutputFormatsForInput(kotlin.Int)` and android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes. While output Surfaces with formats that aren't valid reprocess output targets for the input configuration can be part of a session, they cannot be used as targets for a reprocessing request.

Since the application cannot access `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` images directly, an output Surface created by android.media.ImageReader#newInstance with `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` as the format will be considered as intended to be used for reprocessing input and thus the `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#` size must match one of the supported input sizes for `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` format. Otherwise, creating a reprocessable capture session will fail.

Starting from API level 30, recreating a reprocessable capture session will flush all the queued but not yet processed buffers from the input surface.

The configurations in the tables below are guaranteed for creating a reprocessable capture session if the camera device supports YUV reprocessing or PRIVATE reprocessing. However, not all output targets used to create a reprocessable session may be used in a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest` simultaneously. For devices that support only 1 output target in a reprocess `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest`, submitting a reprocess `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest` with multiple output targets will result in a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureFailure`. For devices that support multiple output targets in a reprocess `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest`, the guaranteed output targets that can be included in a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest` simultaneously are listed in the tables under #createCaptureSession. For example, with a FULL-capability (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` `== ` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int`) device that supports PRIVATE reprocessing, an application can create a reprocessable capture session with 1 input, (`PRIV`, `MAXIMUM`), and 3 outputs, (`PRIV`, `MAXIMUM`), (`PRIV`, `PREVIEW`), and (`YUV`, `MAXIMUM`). However, it's not guaranteed that an application can submit a regular or reprocess capture with (`PRIV`, `MAXIMUM`) and (`YUV`, `MAXIMUM`) outputs based on the table listed under #createCaptureSession. In other words, use the tables below to determine the guaranteed stream configurations for creating a reprocessable capture session, and use the tables under #createCaptureSession to determine the guaranteed output targets that can be submitted in a regular or reprocess `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest` simultaneously.

Reprocessing with 10-bit output targets on 10-bit capable `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_DYNAMIC_RANGE_TEN_BIT:kotlin.Int` devices is not supported. Trying to initialize a repreocessable capture session with one ore more output configurations set `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#setDynamicRangeProfile(kotlin.Long)` to use a 10-bit dynamic range profile `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles` will trigger `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

LIMITED-level (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` `== ``https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int`) devices support at least the following stream combinations for creating a reprocessable capture session in addition to those listed earlier for regular captures for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices:

| LIMITED-level additional guaranteed configurations for creating a reprocessable capture session (`PRIV` input is guaranteed only if PRIVATE reprocessing is supported. `YUV` input is guaranteed only if YUV reprocessing is supported) |||||||||||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Input || Target 1 || Target 2 || Target 3 || Target 4 || Sample use case(s) |
| Type | Max size | Type | Max size | Type | Max size | Type | Max size | Type | Max size | Sample use case(s) |
|---|---|---|---|---|---|---|---|---|---|---|
| `PRIV`/`YUV` | `MAXIMUM` | Same as input | `MAXIMUM` | `JPEG` | `MAXIMUM` | | | | | No-viewfinder still image reprocessing. |
| `PRIV`/`YUV` | `MAXIMUM` | Same as input | `MAXIMUM` | `PRIV` | `PREVIEW` | `JPEG` | `MAXIMUM` | | | ZSL(Zero-Shutter-Lag) still imaging. |
| `PRIV`/`YUV` | `MAXIMUM` | Same as input | `MAXIMUM` | `YUV` | `PREVIEW` | `JPEG` | `MAXIMUM` | | | ZSL still and in-app processing imaging. |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `PRIV`/`YUV` | `MAXIMUM` | Same as input | `MAXIMUM` | `YUV` | `PREVIEW` | `YUV` | `PREVIEW` | `JPEG` | `MAXIMUM` | ZSL in-app processing with still capture. |

<br />

<br />

FULL-level (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` `== ``https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int`) devices support at least the following stream combinations for creating a reprocessable capture session in addition to those for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices:

| FULL-level additional guaranteed configurations for creating a reprocessable capture session (`PRIV` input is guaranteed only if PRIVATE reprocessing is supported. `YUV` input is guaranteed only if YUV reprocessing is supported) |||||||||||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Input || Target 1 || Target 2 || Target 3 || Target 4 || Sample use case(s) |
| Type | Max size | Type | Max size | Type | Max size | Type | Max size | Type | Max size | Sample use case(s) |
|---|---|---|---|---|---|---|---|---|---|---|
| `YUV` | `MAXIMUM` | `YUV` | `MAXIMUM` | `PRIV` | `PREVIEW` | | | | | Maximum-resolution multi-frame image fusion in-app processing with regular preview. |
| `YUV` | `MAXIMUM` | `YUV` | `MAXIMUM` | `YUV` | `PREVIEW` | | | | | Maximum-resolution multi-frame image fusion two-input in-app processing. |
| `PRIV`/`YUV` | `MAXIMUM` | Same as input | `MAXIMUM` | `PRIV` | `PREVIEW` | `YUV` | `RECORD` | | | High-resolution ZSL in-app video processing with regular preview. |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `PRIV` | `MAXIMUM` | `PRIV` | `MAXIMUM` | `PRIV` | `PREVIEW` | `YUV` | `MAXIMUM` | | | Maximum-resolution ZSL in-app processing with regular preview. |
| `PRIV` | `MAXIMUM` | `PRIV` | `MAXIMUM` | `YUV` | `PREVIEW` | `YUV` | `MAXIMUM` | | | Maximum-resolution two-input ZSL in-app processing. |
| `PRIV`/`YUV` | `MAXIMUM` | Same as input | `MAXIMUM` | `PRIV` | `PREVIEW` | `YUV` | `PREVIEW` | `JPEG` | `MAXIMUM` | ZSL still capture and in-app processing. |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

<br />

<br />

RAW-capability (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` includes `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_RAW:kotlin.Int`) devices additionally support at least the following stream combinations for creating a reprocessable capture session on both `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices

| RAW-capability additional guaranteed configurations for creating a reprocessable capture session (`PRIV` input is guaranteed only if PRIVATE reprocessing is supported. `YUV` input is guaranteed only if YUV reprocessing is supported) |||||||||||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Input || Target 1 || Target 2 || Target 3 || Target 4 || Sample use case(s) |
| Type | Max size | Type | Max size | Type | Max size | Type | Max size | Type | Max size | Sample use case(s) |
|---|---|---|---|---|---|---|---|---|---|---|
| `PRIV`/`YUV` | `MAXIMUM` | Same as input | `MAXIMUM` | `YUV` | `PREVIEW` | `RAW` | `MAXIMUM` | | | Mutually exclusive ZSL in-app processing and DNG capture. |
| `PRIV`/`YUV` | `MAXIMUM` | Same as input | `MAXIMUM` | `PRIV` | `PREVIEW` | `YUV` | `PREVIEW` | `RAW` | `MAXIMUM` | Mutually exclusive ZSL in-app processing and preview with DNG capture. |
| `PRIV`/`YUV` | `MAXIMUM` | Same as input | `MAXIMUM` | `YUV` | `PREVIEW` | `YUV` | `PREVIEW` | `RAW` | `MAXIMUM` | Mutually exclusive ZSL two-input in-app processing and DNG capture. |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `PRIV`/`YUV` | `MAXIMUM` | Same as input | `MAXIMUM` | `PRIV` | `PREVIEW` | `JPEG` | `MAXIMUM` | `RAW` | `MAXIMUM` | Mutually exclusive ZSL still capture and preview with DNG capture. |
| `PRIV`/`YUV` | `MAXIMUM` | Same as input | `MAXIMUM` | `YUV` | `PREVIEW` | `JPEG` | `MAXIMUM` | `RAW` | `MAXIMUM` | Mutually exclusive ZSL in-app processing with still capture and DNG capture. |

<br />

<br />

LEVEL-3 (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` `== ``https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_3:kotlin.Int`) devices support at least the following stream combinations for creating a reprocessable capture session in addition to those for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices. Note that while the second configuration allows for configuring `MAXIMUM` `YUV` and `JPEG` outputs at the same time, that configuration is not listed for regular capture sessions, and therefore simultaneous output to both targets is not allowed.

| LEVEL-3 additional guaranteed configurations for creating a reprocessable capture session (`PRIV` input is guaranteed only if PRIVATE reprocessing is supported. `YUV` input is always guaranteed. |||||||||||||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Input || Target 1 || Target 2 || Target 3 || Target 4 || Target 5 || Sample use case(s) |
| Type | Max size | Type | Max size | Type | Max size | Type | Max size | Type | Max size | Type | Max size | Sample use case(s) |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| `YUV` | `MAXIMUM` | `YUV` | `MAXIMUM` | `PRIV` | `PREVIEW` | `PRIV` | `640x480` | `RAW` | `MAXIMUM` | | | In-app viewfinder analysis with ZSL and RAW. |
| `PRIV`/`YUV` | `MAXIMUM` | Same as input | `MAXIMUM` | `PRIV` | `PREVIEW` | `PRIV` | `640x480` | `RAW` | `MAXIMUM` | `JPEG` | `MAXIMUM` | In-app viewfinder analysis with ZSL, RAW, and JPEG reprocessing output. |

<br />

<br />

If a camera device supports multi-resolution `YUV` input and multi-resolution `YUV` output or supports multi-resolution `PRIVATE` input and multi-resolution `PRIVATE` output, the additional mandatory stream combinations for LIMITED and FULL devices are listed below (`MULTI_RES` in the Max size column refers to a `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader` for output, and a multi-resolution `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration` for input):

| LIMITED-level additional guaranteed configurations for creating a reprocessable capture session with multi-resolution input and multi-resolution outputs (`PRIV` input is guaranteed only if PRIVATE reprocessing is supported. `YUV` input is guaranteed only if YUV reprocessing is supported) |||||||||||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Input || Target 1 || Target 2 || Target 3 || Target 4 || Sample use case(s) |
| Type | Max size | Type | Max size | Type | Max size | Type | Max size | Type | Max size | Sample use case(s) |
|---|---|---|---|---|---|---|---|---|---|---|
| `PRIV`/`YUV` | `MULTI_RES` | Same as input | `MULTI_RES` | `JPEG` | `MULTI_RES` | | | | | No-viewfinder still image reprocessing. |
| `PRIV`/`YUV` | `MULTI_RES` | Same as input | `MULTI_RES` | `PRIV` | `PREVIEW` | `JPEG` | `MULTI_RES` | | | ZSL(Zero-Shutter-Lag) still imaging. |
| `PRIV`/`YUV` | `MULTI_RES` | Same as input | `MULTI_RES` | `YUV` | `PREVIEW` | `JPEG` | `MULTI_RES` | | | ZSL still and in-app processing imaging. |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `PRIV`/`YUV` | `MULTI_RES` | Same as input | `MULTI_RES` | `YUV` | `PREVIEW` | `YUV` | `PREVIEW` | `JPEG` | `MULTI_RES` | ZSL in-app processing with still capture. |

<br />

| FULL-level additional guaranteed configurations for creating a reprocessable capture session with multi-resolution input and multi-resolution outputs (`PRIV` input is guaranteed only if PRIVATE reprocessing is supported. `YUV` input is guaranteed only if YUV reprocessing is supported) |||||||||||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Input || Target 1 || Target 2 || Target 3 || Target 4 || Sample use case(s) |
| Type | Max size | Type | Max size | Type | Max size | Type | Max size | Type | Max size | Sample use case(s) |
|---|---|---|---|---|---|---|---|---|---|---|
| `PRIV` | `MULTI_RES` | `PRIV` | `MULTI_RES` | `PRIV` | `PREVIEW` | `YUV` | `MULTI_RES` | | | Maximum-resolution ZSL in-app processing with regular preview. |
| `PRIV` | `MULTI_RES` | `PRIV` | `MULTI_RES` | `YUV` | `PREVIEW` | `YUV` | `MULTI_RES` | | | Maximum-resolution two-input ZSL in-app processing. |
| `PRIV`/`YUV` | `MULTI_RES` | Same as input | `MULTI_RES` | `PRIV` | `PREVIEW` | `YUV` | `PREVIEW` | `JPEG` | `MULTI_RES` | ZSL still capture and in-app processing. |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

<br />

Devices with the ULTRA_HIGH_RESOLUTION_SENSOR capability have some additional guarantees which clients can take advantage of :

| Additional guaranteed combinations for ULTRA_HIGH_RESOLUTION sensors (YUV / PRIV inputs are guaranteed only if YUV / PRIVATE reprocessing are supported) |||||||||||||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Input ||| Target 1 ||| Target 2 ||| Target 3 ||| Sample use case(s) |
| Type | SC Map | Max size | Type | SC Map | Max size | Type | SC Map | Max size | Type | SC Map | Max size | Sample use case(s) |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| `RAW` | `MAX_RES` | `MAX` | `RAW` | `MAX_RES` | `MAX` | `PRIV / YUV` | `DEFAULT` | `PREVIEW` | ||| RAW remosaic reprocessing with separate preview |
| `RAW` | `MAX_RES` | `MAX` | `RAW` | `MAX_RES` | `MAX` | `PRIV / YUV` | `DEFAULT` | `PREVIEW` | `JPEG / YUV` | `MAX_RES` | `MAX` | Ultra high res RAW -\> JPEG / YUV with seperate preview |
| `YUV / PRIV` | `MAX_RES` | `MAX` | `YUV / PRIV` | `MAX_RES` | `MAX` | `YUV / PRIV` | `DEFAULT` | `PREVIEW` | `JPEG ` | `MAX_RES` | `MAX` | Ultra high res PRIV / YUV -\> YUV / JPEG reprocessing with seperate preview |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

<br />

No additional mandatory stream combinations for RAW capability and LEVEL-3 hardware level.

<br />

### Constrained high-speed recording

The application can use a `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#SESSION_REGULAR:kotlin.Int` for high speed capture if the desired high speed FPS ranges are advertised by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_TARGET_FPS_RANGES:android.hardware.camera2.CameraCharacteristics.Key`, in which case all API semantics associated with normal capture sessions applies.

A `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#SESSION_HIGH_SPEED:kotlin.Int` can be use for high speed video recording (\>=120fps) when the camera device supports high speed video capability (i.e., `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` contains `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_CONSTRAINED_HIGH_SPEED_VIDEO:kotlin.Int`). A constrained high-speed capture session has special limitations compared with a normal capture session:

- In addition to the output target Surface requirements specified above for regular captures, a high speed capture session will only support up to 2 output Surfaces, though the application might choose to configure just one Surface (e.g., preview only). All Surfaces must be either video encoder surfaces (acquired by `https://developer.android.com/reference/kotlin/android/media/MediaRecorder.html#getSurface()` or `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#createInputSurface()`) or preview surfaces (obtained from `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#`, `https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#` via `https://developer.android.com/reference/kotlin/android/view/Surface.html#Surface(android.graphics.SurfaceTexture)`). The Surface sizes must be one of the sizes reported by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoSizes()`. When multiple Surfaces are configured, their size must be same.
- An active high speed capture session only accepts request lists created via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraConstrainedHighSpeedCaptureSession#createHighSpeedRequestList(android.hardware.camera2.CaptureRequest)`, and the request list can only be submitted to this session via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#captureBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`, or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`.
- The FPS ranges being requested to this session must be selected from `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoFpsRangesFor(android.util.Size)`. The application can still use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key` to control the desired FPS range. Switching to an FPS range that has different `https://developer.android.com/reference/kotlin/android/util/Range.html#getUpper()` may trigger some camera device reconfigurations, which may introduce extra latency. It is recommended that the application avoids unnecessary maximum target FPS changes as much as possible during high speed streaming.
- For the request lists submitted to this session, the camera device will override the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key`, auto-exposure (AE), auto-white balance (AWB) and auto-focus (AF) to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_AUTO:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_AUTO:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_CONTINUOUS_VIDEO:kotlin.Int`, respectively. All post-processing block mode controls will be overridden to be FAST. Therefore, no manual control of capture and post-processing parameters is possible. Beside these, only a subset of controls will work, see `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_CONSTRAINED_HIGH_SPEED_VIDEO:kotlin.Int` for more details.

| Parameters ||
|---|---|
| `config` | [SessionConfiguration](../android.hardware.camera2.params/SessionConfiguration.md)!: A session configuration (see `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration`). |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | In case the camera device is no longer connected or has encountered a fatal error. |
| `java.lang.IllegalArgumentException` | In case the session configuration is invalid; or the output configurations are empty; or the session configuration executor is invalid; or the output dynamic range combination is invalid/unsupported; or the session type is not shared when camera has been opened in shared mode. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createCaptureSession(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createCaptureSessionByOutputConfigurations(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createReprocessableCaptureSession(android.hardware.camera2.params.InputConfiguration,%20kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createConstrainedHighSpeedCaptureSession(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#setDynamicRangeProfile(kotlin.Long)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles`

### createCaptureSession

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun createCaptureSession(
    outputs: MutableList<Surface!>, 
    callback: CameraCaptureSession.StateCallback, 
    handler: Handler?
): Unit
```

**Deprecated:** *Please use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)` for the full set of configuration options available.*

Create a new camera capture session by providing the target output set of Surfaces to the camera device.

| Parameters ||
|---|---|
| `outputs` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Surface](../android.view/Surface.md)!\>: The new set of Surfaces that should be made available as targets for captured image data. This value cannot be `null`. |
| `callback` | [CameraCaptureSession.StateCallback](../android/hardware/camera2/CameraCaptureSession.StateCallback.md): The callback to notify about the status of the new capture session. This value cannot be `null`. |
| `handler` | [Handler](../android.os/Handler.md)?: The handler on which the callback should be invoked, or `null` to use the current thread's `https://developer.android.com/reference/kotlin/android/os/Looper.html#`. |
| --- | --- |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalArgumentException` | if the set of output Surfaces do not meet the requirements, the callback is null, or the handler is null but the current thread has no looper. |
| `java.lang.IllegalStateException` | if the camera device has been closed |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputFormats()`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(java.lang.Class)`

### createCaptureSessionByOutputConfigurations

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun createCaptureSessionByOutputConfigurations(
    outputConfigurations: MutableList<OutputConfiguration!>!, 
    callback: CameraCaptureSession.StateCallback!, 
    handler: Handler?
): Unit
```

**Deprecated:** *Please use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)` for the full set of configuration options available.*

Create a new camera capture session by providing the target output set of Surfaces and its corresponding surface configuration to the camera device.

| Parameters ||
|---|---|
| `handler` | [Handler](../android.os/Handler.md)?: This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration`

### createConstrainedHighSpeedCaptureSession

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun createConstrainedHighSpeedCaptureSession(
    outputs: MutableList<Surface!>, 
    callback: CameraCaptureSession.StateCallback, 
    handler: Handler?
): Unit
```

**Deprecated:** *Please use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)` for the full set of configuration options available.*

Create a new constrained high speed capture session.

| Parameters ||
|---|---|
| `outputs` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Surface](../android.view/Surface.md)!\>: The new set of Surfaces that should be made available as targets for captured high speed image data. This value cannot be `null`. |
| `callback` | [CameraCaptureSession.StateCallback](../android/hardware/camera2/CameraCaptureSession.StateCallback.md): The callback to notify about the status of the new capture session. This value cannot be `null`. |
| `handler` | [Handler](../android.os/Handler.md)?: The handler on which the callback should be invoked, or `null` to use the current thread's `https://developer.android.com/reference/kotlin/android/os/Looper.html#`. |
| --- | --- |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalArgumentException` | if the set of output Surfaces do not meet the requirements, the callback is null, or the handler is null but the current thread has no looper, or the camera device doesn't support high speed video capability. |
| `java.lang.IllegalStateException` | if the camera device has been closed |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoSizes()`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoFpsRangesFor(android.util.Size)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_CONSTRAINED_HIGH_SPEED_VIDEO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#captureBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingBurst(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraConstrainedHighSpeedCaptureSession#createHighSpeedRequestList(android.hardware.camera2.CaptureRequest)`

### createExtensionSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createExtensionSession(extensionConfiguration: ExtensionSessionConfiguration): Unit
```

Initialize a specific device-specific extension augmented camera capture session.

Extension sessions can be used to enable device-specific operation modes like `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_NIGHT:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_HDR:kotlin.Int`. These modes are less flexible than the full camera API, but enable access to more sophisticated processing algorithms that can capture multi-frame bursts to generate single output images. To query for available extensions on this device call `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#getSupportedExtensions()`.

This method will also trigger the setup of the internal processing pipeline for extension augmented preview and multi-frame still capture.

If a prior CameraCaptureSession already exists when this method is called, the previous session will no longer be able to accept new capture requests and will be closed. Any in-progress capture requests made on the prior session will be completed before it's closed.

The CameraExtensionSession will be active until the client either calls CameraExtensionSession.close() or creates a new camera capture session. In both cases all internal resources will be released, continuous repeating requests stopped and any pending multi-frame capture requests flushed.

Note that the CameraExtensionSession currently supports multi-frame capture surface formats including ImageFormat.JPEG and ImageFormat.YUV_420_888, which may or may not be supported depending on the extension. Starting from API level 37.1, if an extension does not support still capture functionality, no multi-frame capture formats will be supported. Clients must query the multi-frame capture format support using `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#getExtensionSupportedSizes(kotlin.Int,%20kotlin.Int)`. For repeating requests CameraExtensionSession supports only `https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#` as output. Clients can query the supported resolution for the repeating request output using `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#getExtensionSupportedSizes(kotlin.Int,%20java.lang.Class)`.

At the very minimum the initialization expects either one valid output surface for repeating or one valid output for high-quality single requests registered in the outputs argument of the extension configuration argument. At the maximum the initialization will accept two valid output surfaces, one for repeating and the other for single requests. Additional unsupported surfaces passed to ExtensionSessionConfiguration will cause an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` to be thrown.

| Parameters ||
|---|---|
| `extensionConfiguration` | [ExtensionSessionConfiguration](../android.hardware.camera2.params/ExtensionSessionConfiguration.md): extension configuration. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If both the preview and still capture surfaces are not set or invalid, or if any of the registered surfaces do not meet the device-specific extension requirements such as dimensions and/or (output format)/(surface type), or if the extension is not supported, or if any of the output configurations select a dynamic range different from `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#STANDARD:kotlin.Long`, or if any of the output configurations sets a stream use case different from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_DEFAULT:kotlin.Int`. |
| `java.lang.UnsupportedOperationException` | if the camera has been opened in shared mode |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#getSupportedExtensions()`

### createReprocessCaptureRequest

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun createReprocessCaptureRequest(inputResult: TotalCaptureResult): CaptureRequest.Builder
```

Create a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder` for a new reprocess `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest` from a `https://developer.android.com/reference/kotlin/android/hardware/camera2/TotalCaptureResult`.

Each reprocess `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest` processes one buffer from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession`'s input `https://developer.android.com/reference/kotlin/android/view/Surface.html#` to all output `https://developer.android.com/reference/kotlin/android/view/Surface.html#` included in the reprocess capture request. The reprocess input images must be generated from one or multiple output images captured from the same camera device. The application can provide input images to camera device via `https://developer.android.com/reference/kotlin/android/media/ImageWriter.html#queueInputImage(android.media.Image)`. The application must use the capture result of one of those output images to create a reprocess capture request so that the camera device can use the information to achieve optimal reprocess image quality. For camera devices that support only 1 output `https://developer.android.com/reference/kotlin/android/view/Surface.html#`, submitting a reprocess `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest` with multiple output targets will result in a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureFailure`. From Android 14 onward, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key` will be set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_STILL_CAPTURE:kotlin.Int` by default. Prior to Android 14, apps will need to explicitly set this key themselves.

| Parameters ||
|---|---|
| `inputResult` | [TotalCaptureResult](TotalCaptureResult.md): The capture result of the output image or one of the output images used to generate the reprocess input image for this capture request. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalArgumentException` | if inputResult is null. |
| `java.lang.IllegalStateException` | if the camera device has been closed |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the camera has been opened in shared mode |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/TotalCaptureResult`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)`
- `https://developer.android.com/reference/kotlin/android/media/ImageWriter.html#`

### createReprocessableCaptureSession

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun createReprocessableCaptureSession(
    inputConfig: InputConfiguration, 
    outputs: MutableList<Surface!>, 
    callback: CameraCaptureSession.StateCallback, 
    handler: Handler?
): Unit
```

**Deprecated:** *Please use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)` for the full set of configuration options available.*

Create a new reprocessable camera capture session by providing the desired reprocessing input Surface configuration and the target output set of Surfaces to the camera device.

| Parameters ||
|---|---|
| `inputConfig` | [InputConfiguration](../android.hardware.camera2.params/InputConfiguration.md): The configuration for the input `https://developer.android.com/reference/kotlin/android/view/Surface.html#` This value cannot be `null`. |
| `outputs` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Surface](../android.view/Surface.md)!\>: The new set of Surfaces that should be made available as targets for captured image data. This value cannot be `null`. |
| `callback` | [CameraCaptureSession.StateCallback](../android/hardware/camera2/CameraCaptureSession.StateCallback.md): The callback to notify about the status of the new capture session. This value cannot be `null`. |
| --- | --- |
| `handler` | [Handler](../android.os/Handler.md)?: The handler on which the callback should be invoked, or `null` to use the current thread's `https://developer.android.com/reference/kotlin/android/os/Looper.html#`. |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalArgumentException` | if the input configuration is null or not supported, the set of output Surfaces do not meet the requirements, the callback is null, or the handler is null but the current thread has no looper. |
| `java.lang.IllegalStateException` | if the camera device has been closed |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputSizes(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getValidOutputFormatsForInput(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputSizes(java.lang.Class)`
- `https://developer.android.com/reference/kotlin/android/media/ImageWriter.html#`
- `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#`

### createReprocessableCaptureSessionByConfigurations

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun createReprocessableCaptureSessionByConfigurations(
    inputConfig: InputConfiguration, 
    outputs: MutableList<OutputConfiguration!>, 
    callback: CameraCaptureSession.StateCallback, 
    handler: Handler?
): Unit
```

**Deprecated:** *Please use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)` for the full set of configuration options available.*

Create a new reprocessable camera capture session by providing the desired reprocessing input configuration and output `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration` to the camera device.

| Parameters ||
|---|---|
| `inputConfig` | [InputConfiguration](../android.hardware.camera2.params/InputConfiguration.md): This value cannot be `null`. |
| `outputs` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [OutputConfiguration](../android.hardware.camera2.params/OutputConfiguration.md)!\>: This value cannot be `null`. |
| `callback` | [CameraCaptureSession.StateCallback](../android/hardware/camera2/CameraCaptureSession.StateCallback.md): This value cannot be `null`. |
| --- | --- |
| `handler` | [Handler](../android.os/Handler.md)?: This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createReprocessableCaptureSession(android.hardware.camera2.params.InputConfiguration,%20kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration`

### getCameraAudioRestriction

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCameraAudioRestriction(): Int
```

Get currently applied global camera audio restriction mode.

Application can use this method to retrieve the system-wide camera audio restriction settings described in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#setCameraAudioRestriction(kotlin.Int)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The current system-wide mute mode setting in effect. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#AUDIO_RESTRICTION_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#AUDIO_RESTRICTION_VIBRATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#AUDIO_RESTRICTION_VIBRATION_SOUND:kotlin.Int` |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalStateException` | if the camera device has been closed |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#setCameraAudioRestriction(kotlin.Int)`

### getId

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getId(): String
```

Get the ID of this camera device.

This matches the ID given to android.hardware.camera2.CameraManager#openCamera to instantiate this this camera device.

This ID can be used to query the camera device's `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics` with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraCharacteristics(kotlin.String)`.

This method can be called even if the device has been closed or has encountered a serious error.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the ID for this camera device. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraCharacteristics(kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList()`

### isSessionConfigurationSupported

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isSessionConfigurationSupported(sessionConfig: SessionConfiguration): Boolean
```

Checks whether a particular `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration` is supported by the camera device.

This method performs a runtime check of a given `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration`. The result confirms whether or not the passed session configuration can be successfully used to create a camera capture session using `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)`.

The method can be called at any point before, during and after active capture session. It must not impact normal camera behavior in any way and must complete significantly faster than creating a regular or constrained capture session.

Although this method is faster than creating a new capture session, it is not intended to be used for exploring the entire space of supported stream combinations. The available mandatory stream combinations `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination` are better suited for this purpose.

If this function returns `true` for a particular stream combination, the camera device supports concurrent captures on all of the streams in the same CaptureRequest, with two exceptions below where concurrent captures are not supported:

- Supported stream combinations with exclusive dynamic range profiles as specified by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#getProfileCaptureRequestConstraints(kotlin.Long)`.
- Supported combinations of 'default' mode and 'max resolution' mode streams for devices with ULTRA_HIGH_RESOLUTION_SENSOR capability.

For other cases where concurrent captures of a stream combination are not supported, this function returns `false`.

**NOTE:**

- For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int` and above, this method will automatically delegate to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup#isSessionConfigurationSupported(android.hardware.camera2.params.SessionConfiguration)` whenever possible. This means that the output of this method will consider parameters set through `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setSessionParameters(android.hardware.camera2.CaptureRequest)` as well.
- Session Parameters will be ignored for apps targeting \<= `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, or if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#isCameraDeviceSetupSupported(kotlin.String)` returns false for the camera id associated with this `CameraDevice`.

| Parameters ||
|---|---|
| `sessionConfig` | [SessionConfiguration](../android.hardware.camera2.params/SessionConfiguration.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the given session configuration is supported by the camera device `false` otherwise. |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalArgumentException` | if the session configuration is invalid, including, if it contains certain non-supported features queryable via CameraCharacteristics. |
| `java.lang.IllegalStateException` | if the camera device has been closed |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the query operation is not supported by the camera device |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#isCameraDeviceSetupSupported(kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup#isSessionConfigurationSupported(android.hardware.camera2.params.SessionConfiguration)`

### setCameraAudioRestriction

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCameraAudioRestriction(mode: Int): Unit
```

Set audio restriction mode when this CameraDevice is being used.

Some camera hardware (e.g. devices with optical image stabilization support) are sensitive to device vibration and video recordings can be ruined by unexpected sounds. Applications can use this method to suppress vibration or sounds coming from ringtones, alarms or notifications. Other vibration or sounds (e.g. media playback or accessibility) will not be muted.

The mute mode is a system-wide setting. When multiple CameraDevice objects are setting different modes, the system will pick a the mode that's union of all modes set by CameraDevice. Applications can also use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#getCameraAudioRestriction()` to query current system-wide camera mute mode in effect.

The mute settings from this CameraDevice will be automatically removed when the CameraDevice is closed or the application is disconnected from the camera.

| Parameters ||
|---|---|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An enumeration selecting the audio restriction mode for this camera device. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#AUDIO_RESTRICTION_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#AUDIO_RESTRICTION_VIBRATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#AUDIO_RESTRICTION_VIBRATION_SOUND:kotlin.Int` |

| Exceptions ||
|---|---|
| `android.hardware.camera2.CameraAccessException` | if the camera device is no longer connected or has encountered a fatal error |
| `java.lang.IllegalArgumentException` | if the mode is not supported |
| `java.lang.IllegalStateException` | if the camera device has been closed |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#getCameraAudioRestriction()`
