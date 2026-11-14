Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CaptureRequest

```
class CaptureRequest : CameraMetadata<CaptureRequest.Key<*>!>, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.hardware.camera2.CameraMetadata](../android/hardware/camera2/CameraMetadata.md)\< [android.hardware.camera2.CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [\*](../android/hardware/camera2/CaptureRequest.md)\>\> ||
| | ↳ | [android.hardware.camera2.CaptureRequest](../android/hardware/camera2/CaptureRequest.md) |

An immutable package of settings and outputs needed to capture a single image from the camera device.

Contains the configuration for the capture hardware (sensor, lens, flash), the processing pipeline, the control algorithms, and the output buffers. Also contains the list of target Surfaces to send image data to for this capture.

CaptureRequests can be created by using a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder` instance, obtained by calling android.hardware.camera2.CameraDevice#createCaptureRequest or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup#createCaptureRequest(kotlin.Int)`

CaptureRequests are given to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#capture(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#setRepeatingRequest(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler)` to capture images from a camera.

Each request can specify a different subset of target Surfaces for the camera to send the captured data to. All the surfaces used in a request must be part of the surface list given to the last call to android.hardware.camera2.CameraDevice#createCaptureSession, when the request is submitted to the session.

For example, a request meant for repeating preview might only include the Surface for the preview SurfaceView or SurfaceTexture, while a high-resolution still capture would also include a Surface from a ImageReader configured for high-resolution JPEG images.

A reprocess capture request allows a previously-captured image from the camera device to be sent back to the device for further processing. It can be created with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createReprocessCaptureRequest(android.hardware.camera2.TotalCaptureResult)`, and used with a reprocessable capture session created with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createReprocessableCaptureSession(android.hardware.camera2.params.InputConfiguration,%20kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)`.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder` A builder for capture requests. |
| | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Key` A `Key` is used to do capture request field lookups with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#get(android.hardware.camera2.CaptureRequest.Key)` or to set fields with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder#set(android.hardware.camera2.CaptureRequest.Key,%20android.hardware.camera2.CaptureRequest.Builder.set.T)`. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_FRONT:kotlin.Int` The camera device faces the front of the vehicle body frame. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_LEFT:kotlin.Int` The camera device faces the left side of the vehicle body frame. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_OTHER:kotlin.Int` The camera device faces the outside of the vehicle body frame but not exactly one of the exterior sides defined by this enum. Applications should determine the exact facing direction from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_REAR:kotlin.Int` The camera device faces the rear of the vehicle body frame. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_RIGHT:kotlin.Int` The camera device faces the right side of the vehicle body frame. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_OTHER:kotlin.Int` The camera device faces the inside of the vehicle body frame but not exactly one of seats described by this enum. Applications should determine the exact facing direction from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_1_CENTER:kotlin.Int` The camera device faces the center seat of the first row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_1_LEFT:kotlin.Int` The camera device faces the left side seat of the first row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_1_RIGHT:kotlin.Int` The camera device faces the right seat of the first row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_2_CENTER:kotlin.Int` The camera device faces the center seat of the second row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_2_LEFT:kotlin.Int` The camera device faces the left side seat of the second row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_2_RIGHT:kotlin.Int` The camera device faces the right side seat of the second row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_3_CENTER:kotlin.Int` The camera device faces the center seat of the third row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_3_LEFT:kotlin.Int` The camera device faces the left side seat of the third row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_3_RIGHT:kotlin.Int` The camera device faces the right seat of the third row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_FRONT:kotlin.Int` The camera device exists outside of the vehicle body frame and on its front side. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_LEFT:kotlin.Int` The camera device exists outside and on left side of the vehicle body frame. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_OTHER:kotlin.Int` The camera exists outside of the vehicle body frame but not exactly on one of the exterior locations this enum defines. The applications should determine the exact location from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_REAR:kotlin.Int` The camera device exists outside of the vehicle body frame and on its rear side. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_RIGHT:kotlin.Int` The camera device exists outside and on right side of the vehicle body frame. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_FRONT:kotlin.Int` The camera device exists outside of the extra vehicle's body frame and on its front side. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_LEFT:kotlin.Int` The camera device exists outside and on left side of the extra vehicle body. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_OTHER:kotlin.Int` The camera device exists on an extra vehicle, such as the trailer, but not exactly on one of front, rear, left, or right side. Applications should determine the exact location from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_REAR:kotlin.Int` The camera device exists outside of the extra vehicle's body frame and on its rear side. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_RIGHT:kotlin.Int` The camera device exists outside and on right side of the extra vehicle body. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_INTERIOR:kotlin.Int` The camera device exists inside of the vehicle cabin. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_ABERRATION_MODE_FAST:kotlin.Int` Aberration correction will not slow down capture rate relative to sensor raw output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_ABERRATION_MODE_HIGH_QUALITY:kotlin.Int` Aberration correction operates at improved quality but the capture rate might be reduced (relative to sensor raw output rate) <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_ABERRATION_MODE_OFF:kotlin.Int` No aberration correction is applied. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_MODE_CCT:kotlin.Int` Use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_COLOR_TEMPERATURE:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_COLOR_TINT:android.hardware.camera2.CaptureRequest.Key` to adjust the white balance based on correlated color temperature. If AWB is enabled with `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key` != OFF ``, then CCT is ignored. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_MODE_FAST:kotlin.Int` Color correction processing must not slow down capture rate relative to sensor raw output. Advanced white balance adjustments above and beyond the specified white balance pipeline may be applied. If AWB is enabled with `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key` != OFF ``, then the camera device uses the last frame's AWB values (or defaults if AWB has never been run). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_MODE_HIGH_QUALITY:kotlin.Int` Color correction processing operates at improved quality but the capture rate might be reduced (relative to sensor raw output rate) Advanced white balance adjustments above and beyond the specified white balance pipeline may be applied. If AWB is enabled with `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key` != OFF ``, then the camera device uses the last frame's AWB values (or defaults if AWB has never been run). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_MODE_TRANSFORM_MATRIX:kotlin.Int` Use the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` matrix and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` to do color conversion. All advanced white balance adjustments (not specified by our white balance pipeline) must be disabled. If AWB is enabled with `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key` != OFF ``, then TRANSFORM_MATRIX is ignored. The camera device will override this value to either FAST or HIGH_QUALITY. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_ANTIBANDING_MODE_50HZ:kotlin.Int` The camera device will adjust exposure duration to avoid banding problems with 50Hz illumination sources. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_ANTIBANDING_MODE_60HZ:kotlin.Int` The camera device will adjust exposure duration to avoid banding problems with 60Hz illumination sources. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_ANTIBANDING_MODE_AUTO:kotlin.Int` The camera device will automatically adapt its antibanding routine to the current illumination condition. This is the default mode if AUTO is available on given camera device. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_ANTIBANDING_MODE_OFF:kotlin.Int` The camera device will not adjust exposure duration to avoid banding problems. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_OFF:kotlin.Int` The camera device's autoexposure routine is disabled. The application-selected `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` are used by the camera device, along with android.flash.\* fields, if there's a flash unit for this camera device. Note that auto-white balance (AWB) and auto-focus (AF) behavior is device dependent when AE is in OFF mode. To have consistent behavior across different devices, it is recommended to either set AWB and AF to OFF mode or lock AWB and AF before setting AE to OFF. See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_LOCK:android.hardware.camera2.CaptureRequest.Key`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key` for more details. LEGACY devices do not support the OFF mode and will override attempts to use this value to ON. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON:kotlin.Int` The camera device's autoexposure routine is active, with no flash control. The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` are ignored. The application has control over the various android.flash.\* fields. If the device supports manual flash strength control, i.e., if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_SINGLE_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_TORCH_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` are greater than 1, then the auto-exposure (AE) precapture metering sequence should be triggered for the configured flash mode and strength to avoid the image being incorrectly exposed at different `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_STRENGTH_LEVEL:android.hardware.camera2.CaptureRequest.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_ALWAYS_FLASH:kotlin.Int` Like ON, except that the camera device also controls the camera's flash unit, always firing it for still captures. The flash may be fired during a precapture sequence (triggered by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key`) and will always be fired for captures for which the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key` field is set to STILL_CAPTURE. It's important to wait for the precapture sequence to complete (i.e., `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key` reaches FLASH_REQUIRED, CONVERGED, or LOCKED) Dbefore submitting a STILL_CAPTURE request. Otherwise, in low-light conditions, the image captures with flash fired won't have correct exposures. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_AUTO_FLASH:kotlin.Int` Like ON, except that the camera device also controls the camera's flash unit, firing it in low-light conditions. The flash may be fired during a precapture sequence (triggered by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key`) and may be fired for captures for which the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key` field is set to STILL_CAPTURE. It's important to wait for the precapture sequence to complete (i.e., `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key` reaches FLASH_REQUIRED, CONVERGED, or LOCKED) before submitting a STILL_CAPTURE request. Otherwise, in low-light conditions, the image captures with flash fired won't have correct exposures. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_AUTO_FLASH_REDEYE:kotlin.Int` Like ON_AUTO_FLASH, but with automatic red eye reduction. If deemed necessary by the camera device, a red eye reduction flash will fire during the precapture sequence. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_EXTERNAL_FLASH:kotlin.Int` An external flash has been turned on. It informs the camera device that an external flash has been turned on, and that metering (and continuous focus if active) should be quickly recalculated to account for the external flash. Otherwise, this mode acts like ON. When the external flash is turned off, AE mode should be changed to one of the other available AE modes. If the camera device supports AE external flash mode, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key` must be FLASH_REQUIRED after the camera device finishes AE scan and it's too dark without flash. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_LOW_LIGHT_BOOST_BRIGHTNESS_PRIORITY:kotlin.Int` Like 'ON' but applies additional brightness boost in low light scenes. When the scene lighting conditions are within the range defined by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_LOW_LIGHT_BOOST_INFO_LUMINANCE_RANGE:android.hardware.camera2.CameraCharacteristics.Key` this mode will apply additional brightness boost. This mode will automatically adjust the intensity of low light boost applied according to the scene lighting conditions. A darker scene will receive more boost while a brighter scene will receive less boost. This mode can ignore the set target frame rate to allow more light to be captured which can result in choppier motion. The frame rate can extend to lower than the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_TARGET_FPS_RANGES:android.hardware.camera2.CameraCharacteristics.Key` but will not go below 10 FPS. This mode can also increase the sensor sensitivity gain which can result in increased luma and chroma noise. The sensor sensitivity gain can extend to higher values beyond `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_SENSITIVITY_RANGE:android.hardware.camera2.CameraCharacteristics.Key`. This mode may also apply additional processing to recover details in dark and bright areas of the image,and noise reduction at high sensitivity gain settings to manage the trade-off between light sensitivity and capture noise. This mode is restricted to two output surfaces. One output surface type can either be SurfaceView or TextureView. Another output surface type can either be MediaCodec or MediaRecorder. This mode cannot be used with a target FPS range higher than 30 FPS. If the session configuration is not supported, the AE mode reported in the CaptureResult will be 'ON' instead of 'ON_LOW_LIGHT_BOOST_BRIGHTNESS_PRIORITY'. When this AE mode is enabled, the CaptureResult field `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_LOW_LIGHT_BOOST_STATE:android.hardware.camera2.CaptureResult.Key` will indicate when low light boost is 'ACTIVE' or 'INACTIVE'. By default `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_LOW_LIGHT_BOOST_STATE:android.hardware.camera2.CaptureResult.Key` will be 'INACTIVE'. The low light boost is 'ACTIVE' once the scene lighting condition is less than the upper bound lux value defined by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_LOW_LIGHT_BOOST_INFO_LUMINANCE_RANGE:android.hardware.camera2.CameraCharacteristics.Key`. This mode will be 'INACTIVE' once the scene lighting condition is greater than the upper bound lux value defined by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_LOW_LIGHT_BOOST_INFO_LUMINANCE_RANGE:android.hardware.camera2.CameraCharacteristics.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRECAPTURE_TRIGGER_CANCEL:kotlin.Int` The camera device will cancel any currently active or completed precapture metering sequence, the auto-exposure routine will return to its initial state. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRECAPTURE_TRIGGER_IDLE:kotlin.Int` The trigger is idle. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRECAPTURE_TRIGGER_START:kotlin.Int` The precapture metering sequence will be started by the camera device. The exact effect of the precapture trigger depends on the current AE mode and state. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRIORITY_MODE_OFF:kotlin.Int` Disable AE priority mode. This is the default value. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRIORITY_MODE_SENSOR_EXPOSURE_TIME_PRIORITY:kotlin.Int` The camera device's auto-exposure routine is active and prioritizes the application-selected exposure time (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`). The application has control over `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key` while the application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` are ignored. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRIORITY_MODE_SENSOR_SENSITIVITY_PRIORITY:kotlin.Int` The camera device's auto-exposure routine is active and prioritizes the application-selected ISO (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`). The application has control over `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key` while the application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` are ignored. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_STATE_CONVERGED:kotlin.Int` AE has a good set of control values for the current scene. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_STATE_FLASH_REQUIRED:kotlin.Int` AE has a good set of control values, but flash needs to be fired for good quality still capture. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_STATE_INACTIVE:kotlin.Int` AE is off or recently reset. When a camera device is opened, it starts in this state. This is a transient state, the camera device may skip reporting this state in capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_STATE_LOCKED:kotlin.Int` AE has been locked. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_STATE_PRECAPTURE:kotlin.Int` AE has been asked to do a precapture sequence and is currently executing it. Precapture can be triggered through setting `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key` to START. Currently active and completed (if it causes camera device internal AE lock) precapture metering sequence can be canceled through setting `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key` to CANCEL. Once PRECAPTURE completes, AE will transition to CONVERGED or FLASH_REQUIRED as appropriate. This is a transient state, the camera device may skip reporting this state in capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_STATE_SEARCHING:kotlin.Int` AE doesn't yet have a good set of control values for the current scene. This is a transient state, the camera device may skip reporting this state in capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_AUTO:kotlin.Int` Basic automatic focus mode. In this mode, the lens does not move unless the autofocus trigger action is called. When that trigger is activated, AF will transition to ACTIVE_SCAN, then to the outcome of the scan (FOCUSED or NOT_FOCUSED). Always supported if lens is not fixed focus. Use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key` to determine if lens is fixed-focus. Triggering AF_CANCEL resets the lens position to default, and sets the AF state to INACTIVE. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_CONTINUOUS_PICTURE:kotlin.Int` In this mode, the AF algorithm modifies the lens position continually to attempt to provide a constantly-in-focus image stream. The focusing behavior should be suitable for still image capture; typically this means focusing as fast as possible. When the AF trigger is not involved, the AF algorithm should start in INACTIVE state, and then transition into PASSIVE_SCAN and PASSIVE_FOCUSED states as appropriate as it attempts to maintain focus. When the AF trigger is activated, the algorithm should finish its PASSIVE_SCAN if active, and then transition into AF_FOCUSED or AF_NOT_FOCUSED as appropriate, and lock the lens position until a cancel AF trigger is received. When the AF cancel trigger is activated, the algorithm should transition back to INACTIVE and then act as if it has just been started. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_CONTINUOUS_VIDEO:kotlin.Int` In this mode, the AF algorithm modifies the lens position continually to attempt to provide a constantly-in-focus image stream. The focusing behavior should be suitable for good quality video recording; typically this means slower focus movement and no overshoots. When the AF trigger is not involved, the AF algorithm should start in INACTIVE state, and then transition into PASSIVE_SCAN and PASSIVE_FOCUSED states as appropriate. When the AF trigger is activated, the algorithm should immediately transition into AF_FOCUSED or AF_NOT_FOCUSED as appropriate, and lock the lens position until a cancel AF trigger is received. Once cancel is received, the algorithm should transition back to INACTIVE and resume passive scan. Note that this behavior is not identical to CONTINUOUS_PICTURE, since an ongoing PASSIVE_SCAN must immediately be canceled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_EDOF:kotlin.Int` Extended depth of field (digital focus) mode. The camera device will produce images with an extended depth of field automatically; no special focusing operations need to be done before taking a picture. AF triggers are ignored, and the AF state will always be INACTIVE. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_MACRO:kotlin.Int` Close-up focusing mode. In this mode, the lens does not move unless the autofocus trigger action is called. When that trigger is activated, AF will transition to ACTIVE_SCAN, then to the outcome of the scan (FOCUSED or NOT_FOCUSED). This mode is optimized for focusing on objects very close to the camera. When that trigger is activated, AF will transition to ACTIVE_SCAN, then to the outcome of the scan (FOCUSED or NOT_FOCUSED). Triggering cancel AF resets the lens position to default, and sets the AF state to INACTIVE. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_OFF:kotlin.Int` The auto-focus routine does not control the lens; `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key` is controlled by the application. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_SCENE_CHANGE_DETECTED:kotlin.Int` Scene change is detected within the AF region(s). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_SCENE_CHANGE_NOT_DETECTED:kotlin.Int` Scene change is not detected within the AF region(s). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_STATE_ACTIVE_SCAN:kotlin.Int` AF is performing an AF scan because it was triggered by AF trigger. Only used by AUTO or MACRO AF modes. This is a transient state, the camera device may skip reporting this state in capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_STATE_FOCUSED_LOCKED:kotlin.Int` AF believes it is focused correctly and has locked focus. This state is reached only after an explicit START AF trigger has been sent (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`), when good focus has been obtained. The lens will remain stationary until the AF mode (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`) is changed or a new AF trigger is sent to the camera device (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_STATE_INACTIVE:kotlin.Int` AF is off or has not yet tried to scan/been asked to scan. When a camera device is opened, it starts in this state. This is a transient state, the camera device may skip reporting this state in capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_STATE_NOT_FOCUSED_LOCKED:kotlin.Int` AF has failed to focus successfully and has locked focus. This state is reached only after an explicit START AF trigger has been sent (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`), when good focus cannot be obtained. The lens will remain stationary until the AF mode (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`) is changed or a new AF trigger is sent to the camera device (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_STATE_PASSIVE_FOCUSED:kotlin.Int` AF currently believes it is in focus, but may restart scanning at any time. Only used by CONTINUOUS_\* AF modes. This is a transient state, the camera device may skip reporting this state in capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_STATE_PASSIVE_SCAN:kotlin.Int` AF is currently performing an AF scan initiated the camera device in a continuous autofocus mode. Only used by CONTINUOUS_\* AF modes. This is a transient state, the camera device may skip reporting this state in capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_STATE_PASSIVE_UNFOCUSED:kotlin.Int` AF finished a passive scan without finding focus, and may restart scanning at any time. Only used by CONTINUOUS_\* AF modes. This is a transient state, the camera device may skip reporting this state in capture result. LEGACY camera devices do not support this state. When a passive scan has finished, it will always go to PASSIVE_FOCUSED. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_TRIGGER_CANCEL:kotlin.Int` Autofocus will return to its initial state, and cancel any currently active trigger. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_TRIGGER_IDLE:kotlin.Int` The trigger is idle. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_TRIGGER_START:kotlin.Int` Autofocus will trigger now. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AUTOFRAMING_OFF:kotlin.Int` Disable autoframing. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AUTOFRAMING_ON:kotlin.Int` Enable autoframing to keep people in the frame's field of view. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AUTOFRAMING_STATE_CONVERGED:kotlin.Int` Auto-framing has reached a stable state (frame/fov is not being adjusted). The state may transition back to FRAMING if the scene changes. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AUTOFRAMING_STATE_FRAMING:kotlin.Int` Auto-framing is in process - either zooming in, zooming out or pan is taking place. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AUTOFRAMING_STATE_INACTIVE:kotlin.Int` Auto-framing is inactive. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_AUTO:kotlin.Int` The camera device's auto-white balance routine is active. The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_CLOUDY_DAYLIGHT:kotlin.Int` The camera device's auto-white balance routine is disabled; the camera device uses cloudy daylight light as the assumed scene illumination for white balance. The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_DAYLIGHT:kotlin.Int` The camera device's auto-white balance routine is disabled; the camera device uses daylight light as the assumed scene illumination for white balance. While the exact white balance transforms are up to the camera device, they will approximately match the CIE standard illuminant D65. The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_FLUORESCENT:kotlin.Int` The camera device's auto-white balance routine is disabled; the camera device uses fluorescent light as the assumed scene illumination for white balance. While the exact white balance transforms are up to the camera device, they will approximately match the CIE standard illuminant F2. The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_INCANDESCENT:kotlin.Int` The camera device's auto-white balance routine is disabled; the camera device uses incandescent light as the assumed scene illumination for white balance. While the exact white balance transforms are up to the camera device, they will approximately match the CIE standard illuminant A. The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_OFF:kotlin.Int` The camera device's auto-white balance routine is disabled. The application-selected color transform matrix (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key`) and gains (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key`) are used by the camera device for manual white balance control. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_SHADE:kotlin.Int` The camera device's auto-white balance routine is disabled; the camera device uses shade light as the assumed scene illumination for white balance. The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_TWILIGHT:kotlin.Int` The camera device's auto-white balance routine is disabled; the camera device uses twilight light as the assumed scene illumination for white balance. The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_WARM_FLUORESCENT:kotlin.Int` The camera device's auto-white balance routine is disabled; the camera device uses warm fluorescent light as the assumed scene illumination for white balance. While the exact white balance transforms are up to the camera device, they will approximately match the CIE standard illuminant F4. The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_STATE_CONVERGED:kotlin.Int` AWB has a good set of control values for the current scene. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_STATE_INACTIVE:kotlin.Int` AWB is not in auto mode, or has not yet started metering. When a camera device is opened, it starts in this state. This is a transient state, the camera device may skip reporting this state in capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_STATE_LOCKED:kotlin.Int` AWB has been locked. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_STATE_SEARCHING:kotlin.Int` AWB doesn't yet have a good set of control values for the current scene. This is a transient state, the camera device may skip reporting this state in capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_CUSTOM:kotlin.Int` The goal of this request doesn't fall into the other categories. The camera device will default to preview-like behavior. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_MANUAL:kotlin.Int` This request is for manual capture use case where the applications want to directly control the capture parameters. For example, the application may wish to manually control `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`, etc. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_MOTION_TRACKING:kotlin.Int` This request is for a motion tracking use case, where the application will use camera and inertial sensor data to locate and track objects in the world. The camera device auto-exposure routine will limit the exposure time of the camera to no more than 20 milliseconds, to minimize motion blur. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_PREVIEW:kotlin.Int` This request is for a preview-like use case. The precapture trigger may be used to start off a metering w/flash sequence. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_STILL_CAPTURE:kotlin.Int` This request is for a still capture-type use case. If the flash unit is under automatic control, it may fire as needed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_VIDEO_RECORD:kotlin.Int` This request is for a video recording use case. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_VIDEO_SNAPSHOT:kotlin.Int` This request is for a video snapshot (still image while recording video) use case. The camera device should take the highest-quality image possible (given the other settings) without disrupting the frame rate of video recording. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_ZERO_SHUTTER_LAG:kotlin.Int` This request is for a ZSL usecase; the application will stream full-resolution images and reprocess one or several later for a final capture. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_AQUA:kotlin.Int` An "aqua" effect where a blue hue is added to the image. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_BLACKBOARD:kotlin.Int` A "blackboard" effect where the image is typically displayed as regions of black, with white or grey details. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_MONO:kotlin.Int` A "monocolor" effect where the image is mapped into a single color. This will typically be grayscale. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_NEGATIVE:kotlin.Int` A "photo-negative" effect where the image's colors are inverted. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_OFF:kotlin.Int` No color effect will be applied. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_POSTERIZE:kotlin.Int` A "posterization" effect where the image uses discrete regions of tone rather than a continuous gradient of tones. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_SEPIA:kotlin.Int` A "sepia" effect where the image is mapped into warm gray, red, and brown tones. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_SOLARIZE:kotlin.Int` A "solarisation" effect (Sabattier effect) where the image is wholly or partially reversed in tone. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_WHITEBOARD:kotlin.Int` A "whiteboard" effect where the image is typically displayed as regions of white, with black or grey details. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EXTENDED_SCENE_MODE_BOKEH_CONTINUOUS:kotlin.Int` Bokeh effect must not slow down capture rate relative to sensor raw output, and the effect is applied to all processed streams no larger than the maximum streaming dimension. This mode should be used if performance and power are a priority, such as video recording. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EXTENDED_SCENE_MODE_BOKEH_STILL_CAPTURE:kotlin.Int` High quality bokeh mode is enabled for all non-raw streams (including YUV, JPEG, and IMPLEMENTATION_DEFINED) when capture intent is STILL_CAPTURE. Due to the extra image processing, this mode may introduce additional stall to non-raw streams. This mode should be used in high quality still capture use case. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EXTENDED_SCENE_MODE_DISABLED:kotlin.Int` Extended scene mode is disabled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_LOW_LIGHT_BOOST_STATE_ACTIVE:kotlin.Int` The AE mode 'ON_LOW_LIGHT_BOOST_BRIGHTNESS_PRIORITY' is enabled and applied. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_LOW_LIGHT_BOOST_STATE_INACTIVE:kotlin.Int` The AE mode 'ON_LOW_LIGHT_BOOST_BRIGHTNESS_PRIORITY' is enabled but not applied. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_AUTO:kotlin.Int` Use settings for each individual 3A routine. Manual control of capture parameters is disabled. All controls in android.control.\* besides sceneMode take effect. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_OFF:kotlin.Int` Full application control of pipeline. All control by the device's metering and focusing (3A) routines is disabled, and no other settings in android.control.\* have any effect, except that `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key` may be used by the camera device to select post-processing values for processing blocks that do not allow for manual control, or are not exposed by the camera API. However, the camera device's 3A routines may continue to collect statistics and update their internal state so that when control is switched to AUTO mode, good control values can be immediately applied. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_OFF_KEEP_STATE:kotlin.Int` Same as OFF mode, except that this capture will not be used by camera device background auto-exposure, auto-white balance and auto-focus algorithms (3A) to update their statistics. Specifically, the 3A routines are locked to the last values set from a request with AUTO, OFF, or USE_SCENE_MODE, and any statistics or state updates collected from manual captures with OFF_KEEP_STATE will be discarded by the camera device. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_USE_EXTENDED_SCENE_MODE:kotlin.Int` Use a specific extended scene mode. When extended scene mode is on, the camera device may override certain control parameters, such as targetFpsRange, AE, AWB, and AF modes, to achieve best power and quality tradeoffs. Only the mandatory stream combinations of LIMITED hardware level are guaranteed. This setting can only be used if extended scene mode is supported (i.e. android.control.availableExtendedSceneModes contains some modes other than DISABLED). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_USE_SCENE_MODE:kotlin.Int` Use a specific scene mode. Enabling this disables control.aeMode, control.awbMode and control.afMode controls; the camera device will ignore those settings while USE_SCENE_MODE is active (except for FACE_PRIORITY scene mode). Other control entries are still active. This setting can only be used if scene mode is supported (i.e. `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_SCENE_MODES:android.hardware.camera2.CameraCharacteristics.Key` contain some modes other than DISABLED). For extended scene modes such as BOKEH, please use USE_EXTENDED_SCENE_MODE instead. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_ACTION:kotlin.Int` Optimized for photos of quickly moving objects. Similar to SPORTS. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_BARCODE:kotlin.Int` Optimized for accurately capturing a photo of barcode for use by camera applications that wish to read the barcode value. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_BEACH:kotlin.Int` Optimized for bright, outdoor beach settings. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_CANDLELIGHT:kotlin.Int` Optimized for dim settings where the main light source is a candle. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_DISABLED:kotlin.Int` Indicates that no scene modes are set for a given capture request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_FACE_PRIORITY:kotlin.Int` If face detection support exists, use face detection data for auto-focus, auto-white balance, and auto-exposure routines. If face detection statistics are disabled (i.e. `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_FACE_DETECT_MODE:android.hardware.camera2.CaptureRequest.Key` is set to OFF), this should still operate correctly (but will not return face detection statistics to the framework). Unlike the other scene modes, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key` remain active when FACE_PRIORITY is set. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_FIREWORKS:kotlin.Int` Optimized for nighttime photos of fireworks. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_HDR:kotlin.Int` Turn on a device-specific high dynamic range (HDR) mode. In this scene mode, the camera device captures images that keep a larger range of scene illumination levels visible in the final image. For example, when taking a picture of a object in front of a bright window, both the object and the scene through the window may be visible when using HDR mode, while in normal AUTO mode, one or the other may be poorly exposed. As a tradeoff, HDR mode generally takes much longer to capture a single image, has no user control, and may have other artifacts depending on the HDR method used. Therefore, HDR captures operate at a much slower rate than regular captures. In this mode, on LIMITED or FULL devices, when a request is made with a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key` of STILL_CAPTURE, the camera device will capture an image using a high dynamic range capture technique. On LEGACY devices, captures that target a JPEG-format output will be captured with HDR, and the capture intent is not relevant. The HDR capture may involve the device capturing a burst of images internally and combining them into one, or it may involve the device using specialized high dynamic range capture hardware. In all cases, a single image is produced in response to a capture request submitted while in HDR mode. Since substantial post-processing is generally needed to produce an HDR image, only YUV, PRIVATE, and JPEG outputs are supported for LIMITED/FULL device HDR captures, and only JPEG outputs are supported for LEGACY HDR captures. Using a RAW output for HDR capture is not supported. Some devices may also support always-on HDR, which applies HDR processing at full frame rate. For these devices, intents other than STILL_CAPTURE will also produce an HDR output with no frame rate impact compared to normal operation, though the quality may be lower than for STILL_CAPTURE intents. If SCENE_MODE_HDR is used with unsupported output types or capture intents, the images captured will be as if the SCENE_MODE was not enabled at all. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_HIGH_SPEED_VIDEO:kotlin.Int` This is deprecated, please use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createConstrainedHighSpeedCaptureSession(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraConstrainedHighSpeedCaptureSession#createHighSpeedRequestList(android.hardware.camera2.CaptureRequest)` for high speed video recording. Optimized for high speed video recording (frame rate \>=60fps) use case. The supported high speed video sizes and fps ranges are specified in android.control.availableHighSpeedVideoConfigurations. To get desired output frame rates, the application is only allowed to select video size and fps range combinations listed in this static metadata. The fps range can be control via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key`. In this mode, the camera device will override aeMode, awbMode, and afMode to ON, ON, and CONTINUOUS_VIDEO, respectively. All post-processing block mode controls will be overridden to be FAST. Therefore, no manual control of capture and post-processing parameters is possible. All other controls operate the same as when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` == AUTO. This means that all other android.control.\* fields continue to work, such as - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_EXPOSURE_COMPENSATION:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_LOCK:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_LOCK:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EFFECT_MODE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_REGIONS:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` Outside of android.control.\*, the following controls will work: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_MODE:android.hardware.camera2.CaptureRequest.Key` (automatic flash for still capture will not work since aeMode is ON) - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_OPTICAL_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key` (if it is supported) - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_FACE_DETECT_MODE:android.hardware.camera2.CaptureRequest.Key` For high speed recording use case, the actual maximum supported frame rate may be lower than what camera can output, depending on the destination Surfaces for the image data. For example, if the destination surface is from video encoder, the application need check if the video encoder is capable of supporting the high frame rate for a given video size, or it will end up with lower recording frame rate. If the destination surface is from preview window, the preview frame rate will be bounded by the screen refresh rate. The camera device will only support up to 2 output high speed streams (processed non-stalling format defined in android.request.maxNumOutputStreams) in this mode. This control will be effective only if all of below conditions are true: - The application created no more than maxNumHighSpeedStreams processed non-stalling format output streams, where maxNumHighSpeedStreams is calculated as min(2, android.request.maxNumOutputStreams\[Processed (but not-stalling)\]). - The stream sizes are selected from the sizes reported by android.control.availableHighSpeedVideoConfigurations. - No processed non-stalling or raw streams are configured. When above conditions are NOT satisfied, the controls of this mode and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key` will be ignored by the camera device, the camera device will fall back to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` `==` AUTO, and the returned capture result metadata will give the fps range chosen by the camera device. Switching into or out of this mode may trigger some camera ISP/sensor reconfigurations, which may introduce extra latency. It is recommended that the application avoids unnecessary scene mode switch as much as possible. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_LANDSCAPE:kotlin.Int` Optimized for photos of distant macroscopic objects. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_NIGHT:kotlin.Int` Optimized for low-light settings. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_NIGHT_PORTRAIT:kotlin.Int` Optimized for still photos of people in low-light settings. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_PARTY:kotlin.Int` Optimized for dim, indoor settings with multiple moving people. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_PORTRAIT:kotlin.Int` Optimized for still photos of people. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_SNOW:kotlin.Int` Optimized for bright, outdoor settings containing snow. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_SPORTS:kotlin.Int` Optimized for photos of quickly moving people. Similar to ACTION. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_STEADYPHOTO:kotlin.Int` Optimized to avoid blurry photos due to small amounts of device motion (for example: due to hand shake). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_SUNSET:kotlin.Int` Optimized for scenes of the setting sun. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_THEATRE:kotlin.Int` Optimized for dim, indoor settings where flash must remain off. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SETTINGS_OVERRIDE_OFF:kotlin.Int` No keys are applied sooner than the other keys when applying CaptureRequest settings to the camera device. This is the default value. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SETTINGS_OVERRIDE_ZOOM:kotlin.Int` Zoom related keys are applied sooner than the other keys in the CaptureRequest. The zoom related keys are: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_REGIONS:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureRequest.Key` Even though `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_REGIONS:android.hardware.camera2.CaptureRequest.Key`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureRequest.Key` are not directly zoom related, applications typically scale these regions together with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` to have a consistent mapping within the current field of view. In this aspect, they are related to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_VIDEO_STABILIZATION_MODE_OFF:kotlin.Int` Video stabilization is disabled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_VIDEO_STABILIZATION_MODE_ON:kotlin.Int` Video stabilization is enabled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_VIDEO_STABILIZATION_MODE_PREVIEW_STABILIZATION:kotlin.Int` Preview stabilization, where the preview in addition to all other non-RAW streams are stabilized with the same quality of stabilization, is enabled. This mode aims to give clients a 'what you see is what you get' effect. In this mode, the FoV reduction will be a maximum of 20 % both horizontally and vertically (10% from left, right, top, bottom) for the given zoom ratio / crop region. The resultant FoV will also be the same across all processed streams (that have the same aspect ratio). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_ZOOM_METHOD_AUTO:kotlin.Int` The camera device automatically detects whether the application does zoom with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`, and in turn decides which metadata tag reflects the effective zoom level. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_ZOOM_METHOD_ZOOM_RATIO:kotlin.Int` The application intends to control zoom via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`, and the effective zoom level is reflected by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` in capture results. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#DISTORTION_CORRECTION_MODE_FAST:kotlin.Int` Lens distortion correction is applied without reducing frame rate relative to sensor output. It may be the same as OFF if distortion correction would reduce frame rate relative to sensor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#DISTORTION_CORRECTION_MODE_HIGH_QUALITY:kotlin.Int` High-quality distortion correction is applied, at the cost of possibly reduced frame rate relative to sensor output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#DISTORTION_CORRECTION_MODE_OFF:kotlin.Int` No distortion correction is applied. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EDGE_MODE_FAST:kotlin.Int` Apply edge enhancement at a quality level that does not slow down frame rate relative to sensor output. It may be the same as OFF if edge enhancement will slow down frame rate relative to sensor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EDGE_MODE_HIGH_QUALITY:kotlin.Int` Apply high-quality edge enhancement, at a cost of possibly reduced output frame rate. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EDGE_MODE_OFF:kotlin.Int` No edge enhancement is applied. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EDGE_MODE_ZERO_SHUTTER_LAG:kotlin.Int` Edge enhancement is applied at different levels for different output streams, based on resolution. Streams at maximum recording resolution (see android.hardware.camera2.CameraDevice#createCaptureSession) or below have edge enhancement applied, while higher-resolution streams have no edge enhancement applied. The level of edge enhancement for low-resolution streams is tuned so that frame rate is not impacted, and the quality is equal to or better than FAST (since it is only applied to lower-resolution outputs, quality may improve from FAST). This mode is intended to be used by applications operating in a zero-shutter-lag mode with YUV or PRIVATE reprocessing, where the application continuously captures high-resolution intermediate buffers into a circular buffer, from which a final image is produced via reprocessing when a user takes a picture. For such a use case, the high-resolution buffers must not have edge enhancement applied to maximize efficiency of preview and to avoid double-applying enhancement when reprocessed, while low-resolution buffers (used for recording or preview, generally) need edge enhancement applied for reasonable preview quality. This mode is guaranteed to be supported by devices that support either the YUV_REPROCESSING or PRIVATE_REPROCESSING capabilities (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` lists either of those capabilities) and it will be the default mode for CAMERA3_TEMPLATE_ZERO_SHUTTER_LAG template. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EXTENSION_NIGHT_MODE_INDICATOR_OFF:kotlin.Int` The camera has detected lighting conditions that are sufficiently bright. Night Mode Camera Extensions is available but may not be able to optimize the camera settings to take a higher quality photo. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EXTENSION_NIGHT_MODE_INDICATOR_ON:kotlin.Int` The camera has detected low-light conditions. It is recommended to use Night Mode Camera Extension to optimize the camera settings to take a high-quality photo in the dark. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EXTENSION_NIGHT_MODE_INDICATOR_UNKNOWN:kotlin.Int` The camera can't accurately assess the scene's lighting to determine if a Night Mode Camera Extension capture would improve the photo. This can happen when the current camera configuration doesn't support night mode indicator detection, such as when the auto exposure mode is ON_AUTO_FLASH, ON_ALWAYS_FLASH, ON_AUTO_FLASH_REDEYE, or ON_EXTERNAL_FLASH. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_MODE_OFF:kotlin.Int` Do not fire the flash for this capture. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_MODE_SINGLE:kotlin.Int` If the flash is available and charged, fire flash for this capture. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_MODE_TORCH:kotlin.Int` Transition flash to continuously on. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_STATE_CHARGING:kotlin.Int` Flash is charging and cannot be fired. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_STATE_FIRED:kotlin.Int` Flash fired for this capture. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_STATE_PARTIAL:kotlin.Int` Flash partially illuminated this frame. This is usually due to the next or previous frame having the flash fire, and the flash spilling into this capture due to hardware limitations. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_STATE_READY:kotlin.Int` Flash is ready to fire. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_STATE_UNAVAILABLE:kotlin.Int` No flash on camera. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#HOT_PIXEL_MODE_FAST:kotlin.Int` Hot pixel correction is applied, without reducing frame rate relative to sensor raw output. The hotpixel map may be returned in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_HOT_PIXEL_MAP:android.hardware.camera2.CaptureResult.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#HOT_PIXEL_MODE_HIGH_QUALITY:kotlin.Int` High-quality hot pixel correction is applied, at a cost of possibly reduced frame rate relative to sensor raw output. The hotpixel map may be returned in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_HOT_PIXEL_MAP:android.hardware.camera2.CaptureResult.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#HOT_PIXEL_MODE_OFF:kotlin.Int` No hot pixel correction is applied. The frame rate must not be reduced relative to sensor raw output for this option. The hotpixel map may be returned in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_HOT_PIXEL_MAP:android.hardware.camera2.CaptureResult.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_DEVICE_TYPE_BUILT_IN:kotlin.Int` This camera device is physically a part of this Android device, and the data produced is always within the device's control before it reaches the application requesting it. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_DEVICE_TYPE_EXTERNAL:kotlin.Int` This camera device is not permanently connected to this Android device. It may be connected by a wired connection, such as a USB webcam, or it might be connected wirelessly, such as via WiFi or other communication mechanism. The provenance of the image data from the external camera cannot be guaranteed, since it is produced by hardware that is not controlled by this Android device. Note that an `EXTERNAL` `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_DEVICE_TYPE:android.hardware.camera2.CameraCharacteristics.Key` `` does not mean the `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` `` must be `EXTERNAL`. A basic USB webcam would likely have an `EXTERNAL` hardware level, but more sophisticated remote camera systems may have more capabilities than that, and be listed with a `LIMITED` or better hardware level. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_DEVICE_TYPE_UNKNOWN:kotlin.Int` This camera device has an unknown classification. This value will be used when new device classifications need to be added in future Android versions, so that applications targeting older SDK levels do not have to handle unknown enumeration values. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_DEVICE_TYPE_VIRTUAL:kotlin.Int` This camera device produces purely virtual images, though they may be based on the output of a real hardware camera in some cases. For example, a virtual reality headset may have a virtual camera as the front-facing camera, producing a virtual avatar to represent the user, which is animated based on sensors on the headset. The image data should not be assumed to be real. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_3:kotlin.Int` This camera device is capable of YUV reprocessing and RAW data capture, in addition to FULL-level capabilities. The stream configurations listed in the `LEVEL_3`, `RAW`, `FULL`, `LEGACY` and `LIMITED` [tables](../android/hardware/camera2/CameraDevice.md) in the documentation are guaranteed to be supported. The following additional capabilities are guaranteed to be supported: - `YUV_REPROCESSING` capability (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` contains `YUV_REPROCESSING`) - `RAW` capability (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` contains `RAW`) <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_EXTERNAL:kotlin.Int` This camera device is backed by an external camera connected to this Android device. The device has capability identical to a LIMITED level device, with the following exceptions: - The device may not report lens/sensor related information such as - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_HYPERFOCAL_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PHYSICAL_SIZE:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_WHITE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_BLACK_LEVEL_PATTERN:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_ROLLING_SHUTTER_SKEW:android.hardware.camera2.CaptureResult.Key` - The device will report 0 for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_ORIENTATION:android.hardware.camera2.CameraCharacteristics.Key` - The device has less guarantee on stable framerate, as the framerate partly depends on the external camera being used. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` This camera device is capable of supporting advanced imaging applications. The stream configurations listed in the `FULL`, `LEGACY` and `LIMITED` [tables](../android/hardware/camera2/CameraDevice.md) in the documentation are guaranteed to be supported. A `FULL` device will support below capabilities: - `BURST_CAPTURE` capability (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` contains `BURST_CAPTURE`) - Per frame control (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SYNC_MAX_LATENCY:android.hardware.camera2.CameraCharacteristics.Key` `==` PER_FRAME_CONTROL) - Manual sensor control (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` contains `MANUAL_SENSOR`) - Manual post-processing control (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` contains `MANUAL_POST_PROCESSING`) - The required exposure time range defined in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_EXPOSURE_TIME_RANGE:android.hardware.camera2.CameraCharacteristics.Key` - The required maxFrameDuration defined in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_MAX_FRAME_DURATION:android.hardware.camera2.CameraCharacteristics.Key` Note: Pre-API level 23, FULL devices also supported arbitrary cropping region (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_CROPPING_TYPE:android.hardware.camera2.CameraCharacteristics.Key` `== FREEFORM`); this requirement was relaxed in API level 23, and `FULL` devices may only support `CENTERED` cropping. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LEGACY:kotlin.Int` This camera device is running in backward compatibility mode. Only the stream configurations listed in the `LEGACY` [table](../android/hardware/camera2/CameraDevice.md) in the documentation are supported. A `LEGACY` device does not support per-frame control, manual sensor control, manual post-processing, arbitrary cropping regions, and has relaxed performance constraints. No additional capabilities beyond `BACKWARD_COMPATIBLE` will ever be listed by a `LEGACY` device in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`. In addition, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key` is not functional on `LEGACY` devices. Instead, every request that includes a JPEG-format output target is treated as triggering a still capture, internally executing a precapture trigger. This may fire the flash for flash power metering during precapture, and then fire the flash for the final capture, if a flash is available on the device and the AE mode is set to enable the flash. Devices that initially shipped with Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` or newer will not include any LEGACY-level devices. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` This camera device does not have enough capabilities to qualify as a `FULL` device or better. Only the stream configurations listed in the `LEGACY` and `LIMITED` [tables](../android/hardware/camera2/CameraDevice.md) in the documentation are guaranteed to be supported. All `LIMITED` devices support the `BACKWARDS_COMPATIBLE` capability, indicating basic support for color image capture. The only exception is that the device may alternatively support only the `DEPTH_OUTPUT` capability, if it can only output depth measurements and not color images. `LIMITED` devices and above require the use of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key` to lock exposure metering (and calculate flash power, for cameras with flash) before capturing a high-quality still image. A `LIMITED` device that only lists the `BACKWARDS_COMPATIBLE` capability is only required to support full-automatic operation and post-processing (`OFF` is not supported for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`, or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`) Additional capabilities may optionally be supported by a `LIMITED`-level device, and can be checked for in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_FACING_BACK:kotlin.Int` The camera device faces the opposite direction as the device's screen. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_FACING_EXTERNAL:kotlin.Int` The camera device is an external camera, and has no fixed facing relative to the device's screen. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_FACING_FRONT:kotlin.Int` The camera device faces the same direction as the device's screen. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_INFO_FOCUS_DISTANCE_CALIBRATION_APPROXIMATE:kotlin.Int` The lens focus distance is measured in diopters. However, setting the lens to the same focus distance on separate occasions may result in a different real focus distance, depending on factors such as the orientation of the device, the age of the focusing mechanism, and the device temperature. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_INFO_FOCUS_DISTANCE_CALIBRATION_CALIBRATED:kotlin.Int` The lens focus distance is measured in diopters, and is calibrated. The lens mechanism is calibrated so that setting the same focus distance is repeatable on multiple occasions with good accuracy, and the focus distance corresponds to the real physical distance to the plane of best focus. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_INFO_FOCUS_DISTANCE_CALIBRATION_UNCALIBRATED:kotlin.Int` The lens focus distance is not accurate, and the units used for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key` do not correspond to any physical units. Setting the lens to the same focus distance on separate occasions may result in a different real focus distance, depending on factors such as the orientation of the device, the age of the focusing mechanism, and the device temperature. The focus distance value will still be in the range of ``[0, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key`]``, where 0 represents the farthest focus. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_OPTICAL_STABILIZATION_MODE_OFF:kotlin.Int` Optical stabilization is unavailable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_OPTICAL_STABILIZATION_MODE_ON:kotlin.Int` Optical stabilization is enabled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_POSE_REFERENCE_AUTOMOTIVE:kotlin.Int` The value of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` is relative to the origin of the automotive sensor coordinate system, which is at the center of the rear axle. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_POSE_REFERENCE_GYROSCOPE:kotlin.Int` The value of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` is relative to the position of the primary gyroscope of this Android device. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_POSE_REFERENCE_PRIMARY_CAMERA:kotlin.Int` The value of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` is relative to the optical center of the largest camera device facing the same direction as this camera. This is the default value for API levels before Android P. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_POSE_REFERENCE_UNDEFINED:kotlin.Int` The camera device cannot represent the values of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key` accurately enough. One such example is a camera device on the cover of a foldable phone: in order to measure the pose translation and rotation, some kind of hinge position sensor would be needed. The value of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` must be all zeros, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key` must be values matching its default facing. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_STATE_MOVING:kotlin.Int` One or several of the lens parameters (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FILTER_DENSITY:android.hardware.camera2.CaptureRequest.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_APERTURE:android.hardware.camera2.CaptureRequest.Key`) is currently changing. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_STATE_STATIONARY:kotlin.Int` The lens parameters (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FILTER_DENSITY:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_APERTURE:android.hardware.camera2.CaptureRequest.Key`) are not changing. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LOGICAL_MULTI_CAMERA_SENSOR_SYNC_TYPE_APPROXIMATE:kotlin.Int` A software mechanism is used to synchronize between the physical cameras. As a result, the timestamp of an image from a physical stream is only an approximation of the image sensor start-of-exposure time. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LOGICAL_MULTI_CAMERA_SENSOR_SYNC_TYPE_CALIBRATED:kotlin.Int` The camera device supports frame timestamp synchronization at the hardware level, and the timestamp of a physical stream image accurately reflects its start-of-exposure time. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_FAST:kotlin.Int` Noise reduction is applied without reducing frame rate relative to sensor output. It may be the same as OFF if noise reduction will reduce frame rate relative to sensor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_HIGH_QUALITY:kotlin.Int` High-quality noise reduction is applied, at the cost of possibly reduced frame rate relative to sensor output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_MINIMAL:kotlin.Int` MINIMAL noise reduction is applied without reducing frame rate relative to sensor output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_OFF:kotlin.Int` No noise reduction is applied. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_ZERO_SHUTTER_LAG:kotlin.Int` Noise reduction is applied at different levels for different output streams, based on resolution. Streams at maximum recording resolution (see android.hardware.camera2.CameraDevice#createCaptureSession) or below have noise reduction applied, while higher-resolution streams have MINIMAL (if supported) or no noise reduction applied (if MINIMAL is not supported.) The degree of noise reduction for low-resolution streams is tuned so that frame rate is not impacted, and the quality is equal to or better than FAST (since it is only applied to lower-resolution outputs, quality may improve from FAST). This mode is intended to be used by applications operating in a zero-shutter-lag mode with YUV or PRIVATE reprocessing, where the application continuously captures high-resolution intermediate buffers into a circular buffer, from which a final image is produced via reprocessing when a user takes a picture. For such a use case, the high-resolution buffers must not have noise reduction applied to maximize efficiency of preview and to avoid over-applying noise filtering when reprocessing, while low-resolution buffers (used for recording or preview, generally) need noise reduction applied for reasonable preview quality. This mode is guaranteed to be supported by devices that support either the YUV_REPROCESSING or PRIVATE_REPROCESSING capabilities (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` lists either of those capabilities) and it will be the default mode for CAMERA3_TEMPLATE_ZERO_SHUTTER_LAG template. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_BACKWARD_COMPATIBLE:kotlin.Int` The minimal set of capabilities that every camera device (regardless of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`) supports. This capability is listed by all normal devices, and indicates that the camera device has a feature set that's comparable to the baseline requirements for the older android.hardware.Camera API. Devices with the DEPTH_OUTPUT capability might not list this capability, indicating that they support only depth measurement, not standard color output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_BURST_CAPTURE:kotlin.Int` The camera device supports capturing high-resolution images at \>= 20 frames per second, in at least the uncompressed YUV format, when post-processing settings are set to FAST. Additionally, all image resolutions less than 24 megapixels can be captured at \>= 10 frames per second. Here, 'high resolution' means at least 8 megapixels, or the maximum resolution of the device, whichever is smaller. More specifically, this means that a size matching the camera device's active array size is listed as a supported size for the `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` format in either android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes or `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighResolutionOutputSizes(kotlin.Int)`, with a minimum frame duration for that format and size of either \<= 1/20 s, or \<= 1/10 s if the image size is less than 24 megapixels, respectively; and the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_TARGET_FPS_RANGES:android.hardware.camera2.CameraCharacteristics.Key` entry lists at least one FPS range where the minimum FPS is \>= 1 / minimumFrameDuration for the maximum-size YUV_420_888 format. If that maximum size is listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighResolutionOutputSizes(kotlin.Int)`, then the list of resolutions for YUV_420_888 from android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes contains at least one resolution \>= 8 megapixels, with a minimum frame duration of \<= 1/20 s. If the device supports the `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW10:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW12:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW14:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int`, then those can also be captured at the same rate as the maximum-size YUV_420_888 resolution is. If the device supports the PRIVATE_REPROCESSING capability, then the same guarantees as for the YUV_420_888 format also apply to the `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` format. In addition, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SYNC_MAX_LATENCY:android.hardware.camera2.CameraCharacteristics.Key` field is guaranteed to have a value between 0 and 4, inclusive. `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_LOCK_AVAILABLE:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AWB_LOCK_AVAILABLE:android.hardware.camera2.CameraCharacteristics.Key` are also guaranteed to be `true` so burst capture with these two locks ON yields consistent image output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_COLOR_SPACE_PROFILES:kotlin.Int` The device supports querying the possible combinations of color spaces, image formats, and dynamic range profiles supported by the camera and requesting a particular color space for a session via `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setColorSpace(android.graphics.ColorSpace.Named)`. Cameras that enable this capability may or may not also implement dynamic range profiles. If they don't, `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceProfiles#getSupportedDynamicRangeProfiles(android.graphics.ColorSpace.Named,%20kotlin.Int)` will return only `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#STANDARD:kotlin.Long` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceProfiles#getSupportedColorSpacesForDynamicRange(kotlin.Int,%20kotlin.Long)` will assume support of the `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#STANDARD:kotlin.Long` profile in all combinations of color spaces and image formats. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_CONSTRAINED_HIGH_SPEED_VIDEO:kotlin.Int` The device supports constrained high speed video recording (frame rate \>=120fps) use case. The camera device will support high speed capture session created by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createConstrainedHighSpeedCaptureSession(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)`, which only accepts high speed request lists created by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraConstrainedHighSpeedCaptureSession#createHighSpeedRequestList(android.hardware.camera2.CaptureRequest)`. A camera device can still support high speed video streaming by advertising the high speed FPS ranges in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_TARGET_FPS_RANGES:android.hardware.camera2.CameraCharacteristics.Key`. For this case, all normal capture request per frame control and synchronization requirements will apply to the high speed fps ranges, the same as all other fps ranges. This capability describes the capability of a specialized operating mode with many limitations (see below), which is only targeted at high speed video recording. The supported high speed video sizes and fps ranges are specified in `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoFpsRanges()`. To get desired output frame rates, the application is only allowed to select video size and FPS range combinations provided by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoSizes()`. The fps range can be controlled via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key`. In this capability, the camera device will override aeMode, awbMode, and afMode to ON, AUTO, and CONTINUOUS_VIDEO, respectively. All post-processing block mode controls will be overridden to be FAST. Therefore, no manual control of capture and post-processing parameters is possible. All other controls operate the same as when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` == AUTO. This means that all other android.control.\* fields continue to work, such as - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_EXPOSURE_COMPENSATION:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_LOCK:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_LOCK:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EFFECT_MODE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_REGIONS:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` Outside of android.control.\*, the following controls will work: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_MODE:android.hardware.camera2.CaptureRequest.Key` (TORCH mode only, automatic flash for still capture will not work since aeMode is ON) - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_OPTICAL_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key` (if it is supported) - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_FACE_DETECT_MODE:android.hardware.camera2.CaptureRequest.Key` (if it is supported) For high speed recording use case, the actual maximum supported frame rate may be lower than what camera can output, depending on the destination Surfaces for the image data. For example, if the destination surface is from video encoder, the application need check if the video encoder is capable of supporting the high frame rate for a given video size, or it will end up with lower recording frame rate. If the destination surface is from preview window, the actual preview frame rate will be bounded by the screen refresh rate. The camera device will only support up to 2 high speed simultaneous output surfaces (preview and recording surfaces) in this mode. Above controls will be effective only if all of below conditions are true: - The application creates a camera capture session with no more than 2 surfaces via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createConstrainedHighSpeedCaptureSession(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)`. The targeted surfaces must be preview surface (either from `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#` or `https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#`) or recording surface(either from `https://developer.android.com/reference/kotlin/android/media/MediaRecorder.html#getSurface()` or `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#createInputSurface()`). - The stream sizes are selected from the sizes reported by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoSizes()`. - The FPS ranges are selected from `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoFpsRanges()`. When above conditions are NOT satisfied, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createConstrainedHighSpeedCaptureSession(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)` will fail. Switching to a FPS range that has different maximum FPS may trigger some camera device reconfigurations, which may introduce extra latency. It is recommended that the application avoids unnecessary maximum target FPS changes as much as possible during high speed streaming. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_DEPTH_OUTPUT:kotlin.Int` The camera device can produce depth measurements from its field of view. This capability requires the camera device to support the following: - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH16:kotlin.Int` is supported as an output format. - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_POINT_CLOUD:kotlin.Int` is optionally supported as an output format. - This camera device, and all camera devices with the same `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key`, will list the following calibration metadata entries in both `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult`: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key` - The `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#DEPTH_DEPTH_IS_EXCLUSIVE:android.hardware.camera2.CameraCharacteristics.Key` entry is listed by this device. - As of Android P, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key` entry is listed by this device. - A LIMITED camera with only the DEPTH_OUTPUT capability does not have to support normal YUV_420_888, Y8, JPEG, and PRIV-format outputs. It only has to support the DEPTH16 format. Generally, depth output operates at a slower frame rate than standard color capture, so the DEPTH16 and DEPTH_POINT_CLOUD formats will commonly have a stall duration that should be accounted for (see android.hardware.camera2.params.StreamConfigurationMap#getOutputStallDuration). On a device that supports both depth and color-based output, to enable smooth preview, using a repeating burst is recommended, where a depth-output target is only included once every N frames, where N is the ratio between preview output rate and depth output rate, including depth stall time. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_DYNAMIC_RANGE_TEN_BIT:kotlin.Int` The device supports one or more 10-bit camera outputs according to the dynamic range profiles specified in `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#getSupportedProfiles()`. They can be configured as part of the capture session initialization via `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#setDynamicRangeProfile(kotlin.Long)`. Cameras that enable this capability must also support the following: - Profile `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#HLG10:kotlin.Long` - All mandatory stream combinations for this specific capability as per [documentation](../android/hardware/camera2/CameraDevice.md) - In case the device is not able to capture some combination of supported standard 8-bit and/or 10-bit dynamic range profiles within the same capture request, then those constraints must be listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#getProfileCaptureRequestConstraints(kotlin.Long)` - Recommended dynamic range profile listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_RECOMMENDED_TEN_BIT_DYNAMIC_RANGE_PROFILE:android.hardware.camera2.CameraCharacteristics.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_LOGICAL_MULTI_CAMERA:kotlin.Int` The camera device is a logical camera backed by two or more physical cameras. In API level 28, the physical cameras must also be exposed to the application via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList()`. Starting from API level 29: - Some or all physical cameras may not be independently exposed to the application, in which case the physical camera IDs will not be available in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList()`. But the application can still query the physical cameras' characteristics by calling `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraCharacteristics(kotlin.String)`. - If a physical camera is hidden from camera ID list, the mandatory stream combinations for that physical camera must be supported through the logical camera using physical streams. One exception is that in API level 30, a physical camera may become unavailable via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.AvailabilityCallback#onPhysicalCameraUnavailable(kotlin.String,%20kotlin.String)` callback. Combinations of logical and physical streams, or physical streams from different physical cameras are not guaranteed. However, if the camera device supports `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#isSessionConfigurationSupported(android.hardware.camera2.params.SessionConfiguration)`, application must be able to query whether a stream combination involving physical streams is supported by calling `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#isSessionConfigurationSupported(android.hardware.camera2.params.SessionConfiguration)`. Camera application shouldn't assume that there are at most 1 rear camera and 1 front camera in the system. For an application that switches between front and back cameras, the recommendation is to switch between the first rear camera and the first front camera in the list of supported camera devices. This capability requires the camera device to support the following: - The IDs of underlying physical cameras are returned via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getPhysicalCameraIds()`. - This camera device must list static metadata `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LOGICAL_MULTI_CAMERA_SENSOR_SYNC_TYPE:android.hardware.camera2.CameraCharacteristics.Key` in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics`. - The underlying physical cameras' static metadata must list the following entries, so that the application can correlate pixels from the physical streams: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key` - The SENSOR_INFO_TIMESTAMP_SOURCE of the logical device and physical devices must be the same. - The logical camera must be LIMITED or higher device. A logical camera device's dynamic metadata may contain `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#LOGICAL_MULTI_CAMERA_ACTIVE_PHYSICAL_ID:android.hardware.camera2.CaptureResult.Key` to notify the application of the current active physical camera Id. An active physical camera is the physical camera from which the logical camera's main image data outputs (YUV or RAW) and metadata come from. In addition, this serves as an indication which physical camera is used to output to a RAW stream, or in case only physical cameras support RAW, which physical RAW stream the application should request. Logical camera's static metadata tags below describe the default active physical camera. An active physical camera is default if it's used when application directly uses requests built from a template. All templates will default to the same active physical camera. - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_SENSITIVITY_RANGE:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_EXPOSURE_TIME_RANGE:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_MAX_FRAME_DURATION:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PHYSICAL_SIZE:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_WHITE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_LENS_SHADING_APPLIED:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT2:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_CALIBRATION_TRANSFORM1:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_CALIBRATION_TRANSFORM2:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_COLOR_TRANSFORM1:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_COLOR_TRANSFORM2:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_FORWARD_MATRIX1:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_FORWARD_MATRIX2:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_BLACK_LEVEL_PATTERN:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_MAX_ANALOG_SENSITIVITY:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_OPTICAL_BLACK_REGIONS:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_AVAILABLE_TEST_PATTERN_MODES:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_HYPERFOCAL_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_FOCUS_DISTANCE_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key` The field of view of non-RAW physical streams must not be smaller than that of the non-RAW logical streams, or the maximum field-of-view of the physical camera, whichever is smaller. The application should check the physical capture result metadata and physical camera characteristics for how the physical streams are cropped or zoomed. See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key` on how field-of-view is calculated. Typically the physical stream of active physical camera has the same field-of-view as the logical streams. However, the same may not be true for physical streams from non-active physical cameras. For example, if the logical camera has a wide-ultrawide configuration where the wide lens is the default, when the crop region is set to the logical camera's active array size, (and the zoom ratio set to 1.0 starting from Android 11), a physical stream for the ultrawide camera may prefer outputting images with larger field-of-view than that of the wide camera for better stereo matching margin or more robust motion tracking. At the same time, the physical non-RAW streams' field of view must not be smaller than the requested crop region and zoom ratio, as long as it's within the physical lens' capability. For example, for a logical camera with wide-tele lens configuration where the wide lens is the default, if the logical camera's crop region is set to maximum size, and zoom ratio set to 1.0, the physical stream for the tele lens will be configured to its maximum size crop region (no zoom). *Deprecated:* Prior to Android 11, the field of view of all non-RAW physical streams cannot be larger than that of non-RAW logical streams. If the logical camera has a wide-ultrawide lens configuration where the wide lens is the default, when the logical camera's crop region is set to maximum size, the FOV of the physical streams for the ultrawide lens will be the same as the logical stream, by making the crop region smaller than its active array size to compensate for the smaller focal length. For a logical camera, typically the underlying physical cameras have different RAW capabilities (such as resolution or CFA pattern). There are two ways for the application to capture RAW images from the logical camera: - If the logical camera has RAW capability, the application can create and use RAW streams in the same way as before. In case a RAW stream is configured, to maintain backward compatibility, the camera device makes sure the default active physical camera remains active and does not switch to other physical cameras. (One exception is that, if the logical camera consists of identical image sensors and advertises multiple focalLength due to different lenses, the camera device may generate RAW images from different physical cameras based on the focalLength being set by the application.) This backward-compatible approach usually results in loss of optical zoom, to telephoto lens or to ultrawide lens. - Alternatively, if supported by the device, `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader` can be used to capture RAW images from one of the underlying physical cameras ( depending on current zoom level). Because different physical cameras may have different RAW characteristics, the application needs to use the characteristics and result metadata of the active physical camera for the relevant RAW metadata. The capture request and result metadata tags required for backward compatible camera functionalities will be solely based on the logical camera capability. On the other hand, the use of manual capture controls (sensor or post-processing) with a logical camera may result in unexpected behavior when the HAL decides to switch between physical cameras with different characteristics under the hood. For example, when the application manually sets exposure time and sensitivity while zooming in, the brightness of the camera images may suddenly change because HAL switches from one physical camera to the other. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_MANUAL_POST_PROCESSING:kotlin.Int` The camera device post-processing stages can be manually controlled. The camera device supports basic manual control of the image post-processing stages. This means the following controls are guaranteed to be supported: - Manual tonemap control - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_CURVE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#TONEMAP_MAX_CURVE_POINTS:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_GAMMA:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_PRESET_CURVE:android.hardware.camera2.CaptureRequest.Key` - Manual white balance control - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` - Manual lens shading map control - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SHADING_MODE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_LENS_SHADING_MAP_MODE:android.hardware.camera2.CaptureRequest.Key` - android.statistics.lensShadingMap - android.lens.info.shadingMapSize - Manual aberration correction control (if aberration correction is supported) - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_ABERRATION_MODE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#COLOR_CORRECTION_AVAILABLE_ABERRATION_MODES:android.hardware.camera2.CameraCharacteristics.Key` - Auto white balance lock - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_LOCK:android.hardware.camera2.CaptureRequest.Key` If auto white balance is enabled, then the camera device will accurately report the values applied by AWB in the result. A given camera device may also support additional post-processing controls, but this capability only covers the above list of controls. For camera devices with LOGICAL_MULTI_CAMERA capability, when underlying active physical camera switches, tonemap, white balance, and shading map may change even if awb is locked. However, the overall post-processing experience for users will be consistent. Refer to LOGICAL_MULTI_CAMERA capability for details. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_MANUAL_SENSOR:kotlin.Int` The camera device can be manually controlled (3A algorithms such as auto-exposure, and auto-focus can be bypassed). The camera device supports basic manual control of the sensor image acquisition related stages. This means the following controls are guaranteed to be supported: - Manual frame duration control - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_MAX_FRAME_DURATION:android.hardware.camera2.CameraCharacteristics.Key` - Manual exposure control - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_EXPOSURE_TIME_RANGE:android.hardware.camera2.CameraCharacteristics.Key` - Manual sensitivity control - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_SENSITIVITY_RANGE:android.hardware.camera2.CameraCharacteristics.Key` - Manual lens control (if the lens is adjustable) - android.lens.\* - Manual flash control (if a flash unit is present) - android.flash.\* - Manual black level locking - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#BLACK_LEVEL_LOCK:android.hardware.camera2.CaptureRequest.Key` - Auto exposure lock - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_LOCK:android.hardware.camera2.CaptureRequest.Key` If any of the above 3A algorithms are enabled, then the camera device will accurately report the values applied by 3A in the result. A given camera device may also support additional manual sensor controls, but this capability only covers the above list of controls. If this is supported, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key` will additionally return a min frame duration that is greater than zero for each supported size-format combination. For camera devices with LOGICAL_MULTI_CAMERA capability, when the underlying active physical camera switches, exposureTime, sensitivity, and lens properties may change even if AE/AF is locked. However, the overall auto exposure and auto focus experience for users will be consistent. Refer to LOGICAL_MULTI_CAMERA capability for details. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_MONOCHROME:kotlin.Int` The camera device is a monochrome camera that doesn't contain a color filter array, and for YUV_420_888 stream, the pixel values on U and V planes are all 128. A MONOCHROME camera must support the guaranteed stream combinations required for its device level and capabilities. Additionally, if the monochrome camera device supports Y8 format, all mandatory stream combination requirements related to `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` apply to `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int` as well. There are no mandatory stream combination requirements with regard to `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int` for Bayer camera devices. Starting from Android Q, the SENSOR_INFO_COLOR_FILTER_ARRANGEMENT of a MONOCHROME camera will be either MONO or NIR. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_MOTION_TRACKING:kotlin.Int` The camera device supports the MOTION_TRACKING value for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key`, which limits maximum exposure time to 20 ms. This limits the motion blur of capture images, resulting in better image tracking results for use cases such as image stabilization or augmented reality. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_OFFLINE_PROCESSING:kotlin.Int` The camera device supports the OFFLINE_PROCESSING use case. With OFFLINE_PROCESSING capability, the application can switch an ongoing capture session to offline mode by calling the CameraCaptureSession#switchToOffline method and specify streams to be kept in offline mode. The camera will then stop currently active repeating requests, prepare for some requests to go into offline mode, and return an offline session object. After the switchToOffline call returns, the original capture session is in closed state as if the CameraCaptureSession#close method has been called. In the offline mode, all inflight requests will continue to be processed in the background, and the application can immediately close the camera or create a new capture session without losing those requests' output images and capture results. While the camera device is processing offline requests, it might not be able to support all stream configurations it can support without offline requests. When that happens, the createCaptureSession method call will fail. The following stream configurations are guaranteed to work without hitting the resource busy exception: - One ongoing offline session: target one output surface of YUV or JPEG format, any resolution. - The active camera capture session: 1. One preview surface (SurfaceView or SurfaceTexture) up to 1920 width 2. One YUV ImageReader surface up to 1920 width 3. One Jpeg ImageReader, any resolution: the camera device is allowed to slow down JPEG output speed by 50% if there is any ongoing offline session. 4. If the device supports PRIVATE_REPROCESSING, one pair of ImageWriter/ImageReader surfaces of private format, with the same resolution that is larger or equal to the JPEG ImageReader resolution above. - Alternatively, the active camera session above can be replaced by an legacy `https://developer.android.com/reference/kotlin/android/hardware/Camera.html#` with the following parameter settings: 1. Preview size up to 1920 width 2. Preview callback size up to 1920 width 3. Video size up to 1920 width 4. Picture size, any resolution: the camera device is allowed to slow down JPEG output speed by 50% if there is any ongoing offline session. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_PRIVATE_REPROCESSING:kotlin.Int` The camera device supports the Zero Shutter Lag reprocessing use case. - One input stream is supported, that is, `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_MAX_NUM_INPUT_STREAMS:android.hardware.camera2.CameraCharacteristics.Key` == 1 ``. - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` is supported as an output/input format, that is, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` is included in the lists of formats returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputFormats()`. - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getValidOutputFormatsForInput(kotlin.Int)` returns non-empty int\[\] for each supported input format returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()`. - Each size returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputSizes(kotlin.Int)` is also included in android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes - Using `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` does not cause a frame rate drop relative to the sensor's maximum capture rate (at that resolution). - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` will be reprocessable into both `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` formats. - For a MONOCHROME camera supporting Y8 format, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` will be reprocessable into `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int`. - The maximum available resolution for PRIVATE streams (both input/output) will match the maximum available resolution of JPEG streams. - Static metadata `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REPROCESS_MAX_CAPTURE_STALL:android.hardware.camera2.CameraCharacteristics.Key`. - Only below controls are effective for reprocessing requests and will be present in capture results, other controls in reprocess requests will be ignored by the camera device. - android.jpeg.\* - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#NOISE_REDUCTION_MODE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#EDGE_MODE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#NOISE_REDUCTION_AVAILABLE_NOISE_REDUCTION_MODES:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#EDGE_AVAILABLE_EDGE_MODES:android.hardware.camera2.CameraCharacteristics.Key` will both list ZERO_SHUTTER_LAG as a supported mode. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_RAW:kotlin.Int` The camera device supports outputting RAW buffers and metadata for interpreting them. Devices supporting the RAW capability allow both for saving DNG files, and for direct application processing of raw sensor images. - RAW_SENSOR is supported as an output format. - The maximum available resolution for RAW_SENSOR streams will match either the value in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PIXEL_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`. - All DNG-related optional metadata entries are provided by the camera device. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_READ_SENSOR_SETTINGS:kotlin.Int` The camera device supports accurately reporting the sensor settings for many of the sensor controls while the built-in 3A algorithm is running. This allows reporting of sensor settings even when these settings cannot be manually changed. The values reported for the following controls are guaranteed to be available in the CaptureResult, including when 3A is enabled: - Exposure control - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key` - Sensitivity control - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key` - Lens controls (if the lens is adjustable) - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_APERTURE:android.hardware.camera2.CaptureRequest.Key` This capability is a subset of the MANUAL_SENSOR control capability, and will always be included if the MANUAL_SENSOR capability is available. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_REMOSAIC_REPROCESSING:kotlin.Int` The device supports reprocessing from the `RAW_SENSOR` format with a bayer pattern given by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_BINNING_FACTOR:android.hardware.camera2.CameraCharacteristics.Key` (m x n group of pixels with the same color filter) to a remosaiced regular bayer pattern. This capability will only be present for devices with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR:kotlin.Int` capability. When `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR:kotlin.Int` devices do not advertise this capability, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` images will already have a regular bayer pattern. If a `RAW_SENSOR` stream is requested along with another non-RAW stream in a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#` (if multiple streams are supported when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` is set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`), the `RAW_SENSOR` stream will have a regular bayer pattern. This capability requires the camera device to support the following : - The `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap` mentioned below refers to the one, described by `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key` ``. - One input stream is supported, that is, `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_MAX_NUM_INPUT_STREAMS:android.hardware.camera2.CameraCharacteristics.Key` == 1 ``. - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` is supported as an output/input format, that is, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` is included in the lists of formats returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputFormats()`. - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getValidOutputFormatsForInput(kotlin.Int)` returns non-empty int\[\] for each supported input format returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()`. - Each size returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputSizes(kotlin.Int)` is also included in android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes - Using `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` does not cause a frame rate drop relative to the sensor's maximum capture rate (at that resolution). - No CaptureRequest controls will be applicable when a request has an input target with `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` format. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_SECURE_IMAGE_DATA:kotlin.Int` The camera device is capable of writing image data into a region of memory inaccessible to Android userspace or the Android kernel, and only accessible to trusted execution environments (TEE). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_STREAM_USE_CASE:kotlin.Int` The camera device supports selecting a per-stream use case via `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#setStreamUseCase(kotlin.Long)` so that the device can optimize camera pipeline parameters such as tuning, sensor mode, or ISP settings for a specific user scenario. Some sample usages of this capability are: - Distinguish high quality YUV captures from a regular YUV stream where the image quality may not be as good as the JPEG stream, or - Use one stream to serve multiple purposes: viewfinder, video recording and still capture. This is common with applications that wish to apply edits equally to preview, saved images, and saved videos. This capability requires the camera device to support the following stream use cases: - DEFAULT for backward compatibility where the application doesn't set a stream use case - PREVIEW for live viewfinder and in-app image analysis - STILL_CAPTURE for still photo capture - VIDEO_RECORD for recording video clips - PREVIEW_VIDEO_STILL for one single stream used for viewfinder, video recording, and still capture. - VIDEO_CALL for long running video calls `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_STREAM_USE_CASES:android.hardware.camera2.CameraCharacteristics.Key` lists all of the supported stream use cases. Refer to the [guideline](../android/hardware/camera2/CameraDevice.md) for the mandatory stream combinations involving stream use cases, which can also be queried via `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_SYSTEM_CAMERA:kotlin.Int` The camera device is only accessible by Android's system components and privileged applications. Processes need to have the android.permission.SYSTEM_CAMERA in addition to android.permission.CAMERA in order to connect to this camera device. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR:kotlin.Int` This camera device is capable of producing ultra high resolution images in addition to the image sizes described in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key`. It can operate in 'default' mode and 'max resolution' mode. It generally does this by binning pixels in 'default' mode and not binning them in 'max resolution' mode. `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key` `` describes the streams supported in 'default' mode. The stream configurations supported in 'max resolution' mode are described by `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key` ``. The maximum resolution mode pixel array size of a camera device (`` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PIXEL_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` ``) with this capability, will be at least 24 megapixels. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_YUV_REPROCESSING:kotlin.Int` The camera device supports the YUV_420_888 reprocessing use case, similar as PRIVATE_REPROCESSING, This capability requires the camera device to support the following: - One input stream is supported, that is, `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_MAX_NUM_INPUT_STREAMS:android.hardware.camera2.CameraCharacteristics.Key` == 1 ``. - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` is supported as an output/input format, that is, YUV_420_888 is included in the lists of formats returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputFormats()`. - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getValidOutputFormatsForInput(kotlin.Int)` returns non-empty int\[\] for each supported input format returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()`. - Each size returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputSizes(kotlin.Int)` is also included in android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes - Using `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` does not cause a frame rate drop relative to the sensor's maximum capture rate (at that resolution). - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` will be reprocessable into both `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` formats. - The maximum available resolution for `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` streams (both input/output) will match the maximum available resolution of `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` streams. - For a MONOCHROME camera with Y8 format support, all the requirements mentioned above for YUV_420_888 apply for Y8 format as well. - Static metadata `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REPROCESS_MAX_CAPTURE_STALL:android.hardware.camera2.CameraCharacteristics.Key`. - Only the below controls are effective for reprocessing requests and will be present in capture results. The reprocess requests are from the original capture results that are associated with the intermediate `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` output buffers. All other controls in the reprocess requests will be ignored by the camera device. - android.jpeg.\* - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#NOISE_REDUCTION_MODE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#EDGE_MODE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#REPROCESS_EFFECTIVE_EXPOSURE_FACTOR:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#NOISE_REDUCTION_AVAILABLE_NOISE_REDUCTION_MODES:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#EDGE_AVAILABLE_EDGE_MODES:android.hardware.camera2.CameraCharacteristics.Key` will both list ZERO_SHUTTER_LAG as a supported mode. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_CROPPED_RAW:kotlin.Int` Cropped RAW stream when the client chooses to crop the field of view. Certain types of image sensors can run in binned modes in order to improve signal to noise ratio while capturing frames. However, at certain zoom levels and / or when other scene conditions are deemed fit, the camera sub-system may choose to un-bin and remosaic the sensor's output. This results in a RAW frame which is cropped in field of view and yet has the same number of pixels as full field of view RAW, thereby improving image detail. The resultant field of view of the RAW stream will be greater than or equal to croppable non-RAW streams. The effective crop region for this RAW stream will be reflected in the CaptureResult key `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SCALER_RAW_CROP_REGION:android.hardware.camera2.CaptureResult.Key`. If this stream use case is set on a non-RAW stream, i.e. not one of : - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW10:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW14:kotlin.Int` session configuration is not guaranteed to succeed. This stream use case may not be supported on some devices. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_DEFAULT:kotlin.Int` Default stream use case. This use case is the same as when the application doesn't set any use case for the stream. The camera device uses the properties of the output target, such as format, dataSpace, or surface class type, to optimize the image processing pipeline. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_PREVIEW:kotlin.Int` Live stream shown to the user. Optimized for performance and usability as a viewfinder, but not necessarily for image quality. The output is not meant to be persisted as saved images or video. No stall if android.control.\* are set to FAST. There may be stall if they are set to HIGH_QUALITY. This use case has the same behavior as the default SurfaceView and SurfaceTexture targets. Additionally, this use case can be used for in-app image analysis. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_PREVIEW_VIDEO_STILL:kotlin.Int` One single stream used for combined purposes of preview, video, and still capture. For such multi-purpose streams, the camera device aims to make the best tradeoff between the individual use cases. For example, the STILL_CAPTURE use case by itself may have stalls for achieving best image quality. But if combined with PREVIEW and VIDEO_RECORD, the camera device needs to trade off the additional image processing for speed so that preview and video recording aren't slowed down. Similarly, VIDEO_RECORD may produce frames with a substantial lag, but PREVIEW_VIDEO_STILL must have minimal output delay. This means that to enable video stabilization with this use case, the device must support and the app must select the PREVIEW_STABILIZATION mode for video stabilization. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_STILL_CAPTURE:kotlin.Int` Still photo capture. Optimized for high-quality high-resolution capture, and not expected to maintain preview-like frame rates. The stream may have stalls regardless of whether android.control.\* is HIGH_QUALITY. This use case has the same behavior as the default JPEG and RAW related formats. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_VIDEO_CALL:kotlin.Int` Long-running video call optimized for both power efficiency and video quality. The camera sensor may run in a lower-resolution mode to reduce power consumption at the cost of some image and digital zoom quality. Unlike VIDEO_RECORD, VIDEO_CALL outputs are expected to work in dark conditions, so are usually accompanied with variable frame rate settings to allow sufficient exposure time in low light. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_VIDEO_RECORD:kotlin.Int` Recording video clips. Optimized for high-quality video capture, including high-quality image stabilization if supported by the device and enabled by the application. As a result, may produce output frames with a substantial lag from real time, to allow for highest-quality stabilization or other processing. As such, such an output is not suitable for drawing to screen directly, and is expected to be persisted to disk or similar for later playback or processing. Only streams that set the VIDEO_RECORD use case are guaranteed to have video stabilization applied when the video stabilization control is set to ON, as opposed to PREVIEW_STABILIZATION. This use case has the same behavior as the default MediaRecorder and MediaCodec targets. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_CROPPING_TYPE_CENTER_ONLY:kotlin.Int` The camera device only supports centered crop regions. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_CROPPING_TYPE_FREEFORM:kotlin.Int` The camera device supports arbitrarily chosen crop regions. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_180:kotlin.Int` Processed images are rotated by 180 degrees. Since the aspect ratio does not change, no cropping is performed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_270:kotlin.Int` Processed images are rotated by 270 degrees clockwise, and then cropped to the original aspect ratio. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_90:kotlin.Int` Processed images are rotated by 90 degrees clockwise, and then cropped to the original aspect ratio. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_AUTO:kotlin.Int` The camera API automatically selects the best concrete value for rotate-and-crop based on the application's support for resizability and the current multi-window mode. If the application does not support resizing but the display mode for its main Activity is not in a typical orientation, the camera API will set `ROTATE_AND_CROP_90` or some other supported rotation value, depending on device configuration, to ensure preview and captured images are correctly shown to the user. Otherwise, `ROTATE_AND_CROP_NONE` will be selected. When a value other than NONE is selected, several metadata fields will also be parsed differently to ensure that coordinates are correctly handled for features like drawing face detection boxes or passing in tap-to-focus coordinates. The camera API will convert positions in the active array coordinate system to/from the cropped-and-rotated coordinate system to make the operation transparent for applications. No coordinate mapping will be done when the application selects a non-AUTO mode. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_NONE:kotlin.Int` No rotate and crop is applied. Processed outputs are in the sensor orientation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_BGGR:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_GBRG:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_GRBG:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_MONO:kotlin.Int` Sensor doesn't have any Bayer color filter. Such sensor captures visible light in monochrome. The exact weighting and wavelengths captured is not specified, but generally only includes the visible frequencies. This value implies a MONOCHROME camera. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_NIR:kotlin.Int` Sensor has a near infrared filter capturing light with wavelength between roughly 750nm and 1400nm, and the same filter covers the whole sensor array. This value implies a MONOCHROME camera. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_RGB:kotlin.Int` Sensor is not Bayer; output has 3 16-bit values for each pixel, instead of just 1 16-bit value per pixel. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_RGGB:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_TIMESTAMP_SOURCE_REALTIME:kotlin.Int` Timestamps from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_TIMESTAMP:android.hardware.camera2.CaptureResult.Key` are in the same timebase as `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtimeNanos()`, and they can be compared to other timestamps using that base. When buffers from a REALTIME device are passed directly to a video encoder from the camera, automatic compensation is done to account for differing timebases of the audio and camera subsystems. If the application is receiving buffers and then later sending them to a video encoder or other application where they are compared with audio subsystem timestamps or similar, this compensation is not present. In those cases, applications need to adjust the timestamps themselves. Since `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtimeNanos()` and `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()` only diverge while the device is asleep, an offset between the two sources can be measured once per active session and applied to timestamps for sufficient accuracy for A/V sync. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_TIMESTAMP_SOURCE_UNKNOWN:kotlin.Int` Timestamps from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_TIMESTAMP:android.hardware.camera2.CaptureResult.Key` are in nanoseconds and monotonic, but can not be compared to timestamps from other subsystems (e.g. accelerometer, gyro etc.), or other instances of the same or different camera devices in the same system with accuracy. However, the timestamps are roughly in the same timebase as `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()`. The accuracy is sufficient for tasks like A/V synchronization for video recording, at least, and the timestamps can be directly used together with timestamps from the audio subsystem for that task. Timestamps between streams and results for a single camera instance are comparable, and the timestamps for all buffers and the result metadata generated by a single capture are identical. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_DEFAULT:kotlin.Int` This is the default sensor pixel mode. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int` In this mode, sensors typically do not bin pixels, as a result can offer larger image sizes. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_READOUT_TIMESTAMP_HARDWARE:kotlin.Int` This camera device supports the onReadoutStarted callback as well as outputting readout timestamps. The readout timestamp is generated by the camera hardware and it has the same accuracy and timing characteristics of the start-of-exposure time. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_READOUT_TIMESTAMP_NOT_SUPPORTED:kotlin.Int` This camera device doesn't support readout timestamp and onReadoutStarted callback. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_CLOUDY_WEATHER:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_COOL_WHITE_FLUORESCENT:kotlin.Int` W 3900 - 4500K <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_D50:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_D55:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_D65:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_D75:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_DAYLIGHT:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_DAYLIGHT_FLUORESCENT:kotlin.Int` D 5700 - 7100K <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_DAY_WHITE_FLUORESCENT:kotlin.Int` N 4600 - 5400K <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_FINE_WEATHER:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_FLASH:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_FLUORESCENT:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_ISO_STUDIO_TUNGSTEN:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_SHADE:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_STANDARD_A:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_STANDARD_B:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_STANDARD_C:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_TUNGSTEN:kotlin.Int` Incandescent light <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_WHITE_FLUORESCENT:kotlin.Int` WW 3200 - 3700K <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_COLOR_BARS:kotlin.Int` All pixel data is replaced with an 8-bar color pattern. The vertical bars (left-to-right) are as follows: - 100% white - yellow - cyan - green - magenta - red - blue - black In general the image would look like the following: ```kotlin <code>W Y C G M R B K W Y C G M R B K W Y C G M R B K W Y C G M R B K W Y C G M R B K . . . . . . . . . . . . . . . . . . . . . . . . (B = Blue, K = Black) </code> ``` Each bar should take up 1/8 of the sensor pixel array width. When this is not possible, the bar size should be rounded down to the nearest integer and the pattern can repeat on the right side. Each bar's height must always take up the full sensor pixel array height. Each pixel in this test pattern must be set to either 0% intensity or 100% intensity. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_COLOR_BARS_FADE_TO_GRAY:kotlin.Int` The test pattern is similar to COLOR_BARS, except that each bar should start at its specified color at the top, and fade to gray at the bottom. Furthermore each bar is further subdivided into a left and right half. The left half should have a smooth gradient, and the right half should have a quantized gradient. In particular, the right half's should consist of blocks of the same color for 1/16th active sensor pixel array width. The least significant bits in the quantized gradient should be copied from the most significant bits of the smooth gradient. The height of each bar should always be a multiple of 128. When this is not the case, the pattern should repeat at the bottom of the image. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_CUSTOM1:kotlin.Int` The first custom test pattern. All custom patterns that are available only on this camera device are at least this numeric value. All of the custom test patterns will be static (that is the raw image must not vary from frame to frame). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_OFF:kotlin.Int` No test pattern mode is used, and the camera device returns captures from the image sensor. This is the default if the key is not set. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_PN9:kotlin.Int` All pixel data is replaced by a pseudo-random sequence generated from a PN9 512-bit sequence (typically implemented in hardware with a linear feedback shift register). The generator should be reset at the beginning of each frame, and thus each subsequent raw frame with this test pattern should be exactly the same as the last. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_SOLID_COLOR:kotlin.Int` Each pixel in `[R, G_even, G_odd, B]` is replaced by its respective color channel provided in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_TEST_PATTERN_DATA:android.hardware.camera2.CaptureRequest.Key`. For example: ```kotlin <code><code><a docref="android.hardware.camera2.CaptureRequest$SENSOR_TEST_PATTERN_DATA">android.sensor.testPatternData</a></code> = [0, 0xFFFFFFFF, 0xFFFFFFFF, 0] </code> ``` All green pixels are 100% green. All red/blue pixels are black. ```kotlin <code><code><a docref="android.hardware.camera2.CaptureRequest$SENSOR_TEST_PATTERN_DATA">android.sensor.testPatternData</a></code> = [0xFFFFFFFF, 0, 0xFFFFFFFF, 0] </code> ``` All red pixels are 100% red. Only the odd green pixels are 100% green. All blue pixels are 100% black. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SHADING_MODE_FAST:kotlin.Int` Apply lens shading corrections, without slowing frame rate relative to sensor raw output <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SHADING_MODE_HIGH_QUALITY:kotlin.Int` Apply high-quality lens shading correction, at the cost of possibly reduced frame rate. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SHADING_MODE_OFF:kotlin.Int` No lens shading correction is applied. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_FACE_DETECT_MODE_FULL:kotlin.Int` Return all face metadata. In this mode, face rectangles, scores, landmarks, and face IDs are all valid. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_FACE_DETECT_MODE_OFF:kotlin.Int` Do not include face detection statistics in capture results. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_FACE_DETECT_MODE_SIMPLE:kotlin.Int` Return face rectangle and confidence values only. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_LENS_SHADING_MAP_MODE_OFF:kotlin.Int` Do not include a lens shading map in the capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_LENS_SHADING_MAP_MODE_ON:kotlin.Int` Include a lens shading map in the capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_OIS_DATA_MODE_OFF:kotlin.Int` Do not include OIS data in the capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_OIS_DATA_MODE_ON:kotlin.Int` Include OIS data in the capture result. `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_OIS_SAMPLES:android.hardware.camera2.CaptureResult.Key` provides OIS sample data in the output result metadata. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_SCENE_FLICKER_50HZ:kotlin.Int` The camera device detects illumination flickering at 50Hz in the current scene. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_SCENE_FLICKER_60HZ:kotlin.Int` The camera device detects illumination flickering at 60Hz in the current scene. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_SCENE_FLICKER_NONE:kotlin.Int` The camera device does not detect any flickering illumination in the current scene. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SYNC_MAX_LATENCY_PER_FRAME_CONTROL:kotlin.Int` Every frame has the requests immediately applied. Changing controls over multiple requests one after another will produce results that have those controls applied atomically each frame. All FULL capability devices will have this as their maxLatency. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SYNC_MAX_LATENCY_UNKNOWN:kotlin.Int` Each new frame has some subset (potentially the entire set) of the past requests applied to the camera settings. By submitting a series of identical requests, the camera device will eventually have the camera settings applied, but it is unknown when that exact point will be. All LEGACY capability devices will have this as their maxLatency. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_CONTRAST_CURVE:kotlin.Int` Use the tone mapping curve specified in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_CURVE:android.hardware.camera2.CaptureRequest.Key`\* entries. All color enhancement and tonemapping must be disabled, except for applying the tonemapping curve specified by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_CURVE:android.hardware.camera2.CaptureRequest.Key`. Must not slow down frame rate relative to raw sensor output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_FAST:kotlin.Int` Advanced gamma mapping and color enhancement may be applied, without reducing frame rate compared to raw sensor output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_GAMMA_VALUE:kotlin.Int` Use the gamma value specified in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_GAMMA:android.hardware.camera2.CaptureRequest.Key` to perform tonemapping. All color enhancement and tonemapping must be disabled, except for applying the tonemapping curve specified by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_GAMMA:android.hardware.camera2.CaptureRequest.Key`. Must not slow down frame rate relative to raw sensor output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_HIGH_QUALITY:kotlin.Int` High-quality gamma mapping and color enhancement will be applied, at the cost of possibly reduced frame rate compared to raw sensor output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_PRESET_CURVE:kotlin.Int` Use the preset tonemapping curve specified in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_PRESET_CURVE:android.hardware.camera2.CaptureRequest.Key` to perform tonemapping. All color enhancement and tonemapping must be disabled, except for applying the tonemapping curve specified by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_PRESET_CURVE:android.hardware.camera2.CaptureRequest.Key`. Must not slow down frame rate relative to raw sensor output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_PRESET_CURVE_REC709:kotlin.Int` Tonemapping curve is defined by ITU-R BT.709 <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_PRESET_CURVE_SRGB:kotlin.Int` Tonemapping curve is defined by sRGB <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Determine whether this CaptureRequest is equal to another CaptureRequest. |
| T? | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#get(android.hardware.camera2.CaptureRequest.Key)(key: https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Key<T>!)` Get a capture request field value. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\<\*\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#getKeys()()` Returns a list of the keys contained in this map. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#getTag()()` Retrieve the tag for this request, if any. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#hashCode()()` Returns a hash code value for the object. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#isReprocess()()` Determine if this is a reprocess capture request. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Protected methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

| Properties ||
|---|---|
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#BLACK_LEVEL_LOCK:android.hardware.camera2.CaptureRequest.Key` Whether black-level compensation is locked to its current values, or is free to vary. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_ABERRATION_MODE:android.hardware.camera2.CaptureRequest.Key` Mode of operation for the chromatic aberration correction algorithm. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_COLOR_TEMPERATURE:android.hardware.camera2.CaptureRequest.Key` Specifies the color temperature for CCT mode in Kelvin to adjust the white balance of the image. |
| --- | --- |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_COLOR_TINT:android.hardware.camera2.CaptureRequest.Key` Specifies the color tint for CCT mode to adjust the white balance of the image. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [RggbChannelVector](../android/hardware/camera2/params/RggbChannelVector.md)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` Gains applying to Bayer raw color channels for white-balance. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` The mode control selects how the image data is converted from the sensor's native color into linear sRGB color. |
| --- | --- |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [ColorSpaceTransform](../android/hardware/camera2/params/ColorSpaceTransform.md)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` A color transform matrix to use to transform from sensor RGB color space to output linear sRGB color space. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_ANTIBANDING_MODE:android.hardware.camera2.CaptureRequest.Key` The desired setting for the camera device's auto-exposure algorithm's antibanding compensation. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_EXPOSURE_COMPENSATION:android.hardware.camera2.CaptureRequest.Key` Adjustment to auto-exposure (AE) target image brightness. |
| --- | --- |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_LOCK:android.hardware.camera2.CaptureRequest.Key` Whether auto-exposure (AE) is currently locked to its latest calculated values. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key` The desired mode for the camera device's auto-exposure routine. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key` Whether the camera device will trigger a precapture metering sequence when it processes this request. |
| --- | --- |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRIORITY_MODE:android.hardware.camera2.CaptureRequest.Key` Turn on AE priority mode. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MeteringRectangle](../android/hardware/camera2/params/MeteringRectangle.md)!\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key` List of metering areas to use for auto-exposure adjustment. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Range](../android/util/Range.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key` Range over which the auto-exposure routine can adjust the capture frame rate to maintain good exposure. |
| --- | --- |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key` Whether auto-focus (AF) is currently enabled, and what mode it is set to. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MeteringRectangle](../android/hardware/camera2/params/MeteringRectangle.md)!\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureRequest.Key` List of metering areas to use for auto-focus. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key` Whether the camera device will trigger autofocus for this request. |
| --- | --- |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AUTOFRAMING:android.hardware.camera2.CaptureRequest.Key` Automatic crop, pan and zoom to keep objects in the center of the frame. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_LOCK:android.hardware.camera2.CaptureRequest.Key` Whether auto-white balance (AWB) is currently locked to its latest calculated values. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key` Whether auto-white balance (AWB) is currently setting the color transform fields, and what its illumination target is. |
| --- | --- |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MeteringRectangle](../android/hardware/camera2/params/MeteringRectangle.md)!\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_REGIONS:android.hardware.camera2.CaptureRequest.Key` List of metering areas to use for auto-white-balance illuminant estimation. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key` Information to the camera device 3A (auto-exposure, auto-focus, auto-white balance) routines about the purpose of this capture, to help the camera device to decide optimal 3A strategy. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EFFECT_MODE:android.hardware.camera2.CaptureRequest.Key` A special color effect to apply. |
| --- | --- |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ENABLE_ZSL:android.hardware.camera2.CaptureRequest.Key` Allow camera device to enable zero-shutter-lag mode for requests with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key` == STILL_CAPTURE. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EXTENDED_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key` Whether extended scene mode is enabled for a particular capture request. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` Overall mode of 3A (auto-exposure, auto-white-balance, auto-focus) control routines. |
| --- | --- |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_POST_RAW_SENSITIVITY_BOOST:android.hardware.camera2.CaptureRequest.Key` The amount of additional sensitivity boost applied to output images after RAW sensor data is captured. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key` Control for which scene mode is currently active. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SETTINGS_OVERRIDE:android.hardware.camera2.CaptureRequest.Key` The desired CaptureRequest settings override with which certain keys are applied earlier so that they can take effect sooner. |
| --- | --- |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_VIDEO_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key` Whether video stabilization is active. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_METHOD:android.hardware.camera2.CaptureRequest.Key` Whether the application uses `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` to control zoom levels. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` The desired zoom ratio |
| --- | --- |
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [CaptureRequest](../android/hardware/camera2/CaptureRequest.md)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CREATOR:android.os.Parcelable.Creator` <br /> |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` Mode of operation for the lens distortion correction block. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#EDGE_MODE:android.hardware.camera2.CaptureRequest.Key` Operation mode for edge enhancement. |
| --- | --- |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#EXTENSION_STRENGTH:android.hardware.camera2.CaptureRequest.Key` Strength of the extension post-processing effect |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_MODE:android.hardware.camera2.CaptureRequest.Key` The desired mode for for the camera device's flash control. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_STRENGTH_LEVEL:android.hardware.camera2.CaptureRequest.Key` Flash strength level to be used when manual flash control is active. |
| --- | --- |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#HOT_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` Operational mode for hot pixel correction. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Location](../android/location/Location.md)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#JPEG_GPS_LOCATION:android.hardware.camera2.CaptureRequest.Key` A location object to use when generating image GPS metadata. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#JPEG_ORIENTATION:android.hardware.camera2.CaptureRequest.Key` The orientation for a JPEG image. |
| --- | --- |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#JPEG_QUALITY:android.hardware.camera2.CaptureRequest.Key` Compression quality of the final JPEG image. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#JPEG_THUMBNAIL_QUALITY:android.hardware.camera2.CaptureRequest.Key` Compression quality of JPEG thumbnail. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Size](../android/util/Size.md)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#JPEG_THUMBNAIL_SIZE:android.hardware.camera2.CaptureRequest.Key` Resolution of embedded JPEG thumbnail. |
| --- | --- |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_APERTURE:android.hardware.camera2.CaptureRequest.Key` The desired lens aperture size, as a ratio of lens focal length to the effective aperture diameter. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FILTER_DENSITY:android.hardware.camera2.CaptureRequest.Key` The desired setting for the lens neutral density filter(s). |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key` The desired lens focal length |
| --- | --- |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key` Desired distance to plane of sharpest focus, measured from frontmost surface of the lens. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_OPTICAL_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key` Sets whether the camera device uses optical image stabilization (OIS) when capturing images. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LOGICAL_MULTI_CAMERA_ADDITIONAL_RESULTS:android.hardware.camera2.CaptureRequest.Key` Controls whether the camera device could also return additional physical cameras' metadata in the results. |
| --- | --- |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#NOISE_REDUCTION_MODE:android.hardware.camera2.CaptureRequest.Key` Mode of operation for the noise reduction algorithm. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#REPROCESS_EFFECTIVE_EXPOSURE_FACTOR:android.hardware.camera2.CaptureRequest.Key` The amount of exposure time increase factor applied to the original output frame by the application processing before sending for reprocessing. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Rect](../android/graphics/Rect.md)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` The desired region of the sensor to read out for this capture. |
| --- | --- |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_ROTATE_AND_CROP:android.hardware.camera2.CaptureRequest.Key` Whether a rotation-and-crop operation is applied to processed outputs from the camera. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key` Duration each pixel is exposed to light. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` Duration from start of frame readout to start of next frame readout. |
| --- | --- |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` Switches sensor pixel mode between maximum resolution mode and default mode. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key` The amount of gain applied to sensor data before processing. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_TEST_PATTERN_DATA:android.hardware.camera2.CaptureRequest.Key` A pixel `[R, G_even, G_odd, B]` that supplies the test pattern when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_TEST_PATTERN_MODE:android.hardware.camera2.CaptureRequest.Key` is SOLID_COLOR. |
| --- | --- |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_TEST_PATTERN_MODE:android.hardware.camera2.CaptureRequest.Key` When enabled, the sensor sends a test pattern instead of doing a real exposure from the camera. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SHADING_MODE:android.hardware.camera2.CaptureRequest.Key` Quality of lens shading correction applied to the image data. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_FACE_DETECT_MODE:android.hardware.camera2.CaptureRequest.Key` Operating mode for the face detector unit. |
| --- | --- |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_HOT_PIXEL_MAP_MODE:android.hardware.camera2.CaptureRequest.Key` Operating mode for hot pixel map generation. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_LENS_SHADING_MAP_MODE:android.hardware.camera2.CaptureRequest.Key` Whether the camera device will output the lens shading map in output result metadata. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_OIS_DATA_MODE:android.hardware.camera2.CaptureRequest.Key` A control for selecting whether optical stabilization (OIS) position information is included in output result metadata. |
| --- | --- |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [TonemapCurve](../android/hardware/camera2/params/TonemapCurve.md)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_CURVE:android.hardware.camera2.CaptureRequest.Key` Tonemapping / contrast / gamma curve to use when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key` is CONTRAST_CURVE. |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_GAMMA:android.hardware.camera2.CaptureRequest.Key` Tonemapping curve to use when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key` is GAMMA_VALUE |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key` High-level global contrast/gamma/tonemapping control. |
| --- | --- |
| static [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_PRESET_CURVE:android.hardware.camera2.CaptureRequest.Key` Tonemapping curve to use when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key` is PRESET_CURVE |

## Public methods

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Determine whether this CaptureRequest is equal to another CaptureRequest.

A request is considered equal to another is if it's set of key/values is equal, it's list of output surfaces is equal, the user tag is equal, and the return values of isReprocess() are equal.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: Another instance of CaptureRequest. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the requests are the same, false otherwise. |

### get

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> get(key: CaptureRequest.Key<T>!): T?
```

Get a capture request field value.

The field definitions can be found in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#`.

Querying the value for the same key more than once will return a value which is equal to the previous queried value.

| Parameters ||
|---|---|
| `key` | [CaptureRequest.Key](../android/hardware/camera2/CaptureRequest.Key.md)\<T\>!: The result field to read. |

| Return ||
|---|---|
| `T?` | The value of that key, or `null` if the field is not set. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the key was not valid |

### getKeys

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKeys(): MutableList<CaptureRequest.Key<*>!>
```

Returns a list of the keys contained in this map.

The list returned is not modifiable, so any attempts to modify it will throw a `UnsupportedOperationException`.

All values retrieved by a key from this list with `get` are guaranteed to be non-`null`. Each key is only listed once in the list. The order of the keys is undefined.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Key<*>!>` | This value cannot be `null`. |

### getTag

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTag(): Any?
```

Retrieve the tag for this request, if any.

This tag is not used for anything by the camera device, but can be used by an application to easily identify a CaptureRequest when it is returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback#onCaptureCompleted(android.hardware.camera2.CameraCaptureSession,%20android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.TotalCaptureResult)`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?` | the last tag Object set on this request, or `null` if no tag has been set. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder#setTag(kotlin.Any)`

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

### isReprocess

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isReprocess(): Boolean
```

Determine if this is a reprocess capture request.

A reprocess capture request produces output images from an input buffer from the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession`'s input `https://developer.android.com/reference/kotlin/android/view/Surface.html#`. A reprocess capture request can be created by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createReprocessCaptureRequest(android.hardware.camera2.TotalCaptureResult)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this is a reprocess capture request. `false` if this is not a reprocess capture request. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createReprocessCaptureRequest(android.hardware.camera2.TotalCaptureResult)`

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android/os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Protected methods

### finalize

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun finalize(): Unit
```

Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup.

The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded.

The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition.

The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates.

After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded.

The `finalize` method is never invoked more than once by a Java virtual machine for any given object.

Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored.

| Exceptions ||
|---|---|
| `java.lang.Throwable` | the `Exception` raised by this method |

## Properties

### BLACK_LEVEL_LOCK

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BLACK_LEVEL_LOCK: CaptureRequest.Key<Boolean!>
```

Whether black-level compensation is locked to its current values, or is free to vary.

When set to `true` (ON), the values used for black-level compensation will not change until the lock is set to `false` (OFF).

Since changes to certain capture parameters (such as exposure time) may require resetting of black level compensation, the camera device must report whether setting the black level lock was successful in the output result metadata.

For example, if a sequence of requests is as follows:

- Request 1: Exposure = 10ms, Black level lock = OFF
- Request 2: Exposure = 10ms, Black level lock = ON
- Request 3: Exposure = 10ms, Black level lock = ON
- Request 4: Exposure = 20ms, Black level lock = ON
- Request 5: Exposure = 20ms, Black level lock = ON
- Request 6: Exposure = 20ms, Black level lock = ON

And the exposure change in Request 4 requires the camera device to reset the black level offsets, then the output result metadata is expected to be:

- Result 1: Exposure = 10ms, Black level lock = OFF
- Result 2: Exposure = 10ms, Black level lock = ON
- Result 3: Exposure = 10ms, Black level lock = ON
- Result 4: Exposure = 20ms, Black level lock = OFF
- Result 5: Exposure = 20ms, Black level lock = ON
- Result 6: Exposure = 20ms, Black level lock = ON

This indicates to the application that on frame 4, black levels were reset due to exposure value changes, and pixel values may not be consistent across captures.

The camera device will maintain the lock to the extent possible, only overriding the lock to OFF when changes to other request parameters require a black level recalculation or reset.

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`

### COLOR_CORRECTION_ABERRATION_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_CORRECTION_ABERRATION_MODE: CaptureRequest.Key<Int!>
```

Mode of operation for the chromatic aberration correction algorithm.

Chromatic (color) aberration is caused by the fact that different wavelengths of light can not focus on the same point after exiting from the lens. This metadata defines the high level control of chromatic aberration correction algorithm, which aims to minimize the chromatic artifacts that may occur along the object boundaries in an image.

FAST/HIGH_QUALITY both mean that camera device determined aberration correction will be applied. HIGH_QUALITY mode indicates that the camera device will use the highest-quality aberration correction algorithms, even if it slows down capture rate. FAST means the camera device will not slow down capture rate when applying aberration correction.

LEGACY devices will always be in FAST mode.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_ABERRATION_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_ABERRATION_MODE_FAST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_ABERRATION_MODE_HIGH_QUALITY:kotlin.Int`

**Available values for this device:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#COLOR_CORRECTION_AVAILABLE_ABERRATION_MODES:android.hardware.camera2.CameraCharacteristics.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#COLOR_CORRECTION_AVAILABLE_ABERRATION_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_ABERRATION_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_ABERRATION_MODE_FAST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_ABERRATION_MODE_HIGH_QUALITY:kotlin.Int`

### COLOR_CORRECTION_COLOR_TEMPERATURE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_CORRECTION_COLOR_TEMPERATURE: CaptureRequest.Key<Int!>
```

Specifies the color temperature for CCT mode in Kelvin to adjust the white balance of the image.

Sets the color temperature in Kelvin units for when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` is CCT to adjust the white balance of the image.

If CCT mode is enabled without a requested color temperature, a default value will be set by the camera device. The default value can be retrieved by checking the corresponding capture result. Color temperatures requested outside the advertised `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#COLOR_CORRECTION_COLOR_TEMPERATURE_RANGE:android.hardware.camera2.CameraCharacteristics.Key` will be clamped.

**Units**: Kelvin

**Range of valid values:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#COLOR_CORRECTION_COLOR_TEMPERATURE_RANGE:android.hardware.camera2.CameraCharacteristics.Key`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#COLOR_CORRECTION_COLOR_TEMPERATURE_RANGE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`

### COLOR_CORRECTION_COLOR_TINT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_CORRECTION_COLOR_TINT: CaptureRequest.Key<Int!>
```

Specifies the color tint for CCT mode to adjust the white balance of the image.

Sets the color tint for when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` is CCT to adjust the white balance of the image.

If CCT mode is enabled without a requested color tint, a default value will be set by the camera device. The default value can be retrieved by checking the corresponding capture result. Color tints requested outside the supported range will be clamped to the nearest limit (-50 or +50).

**Units**: D_uv defined as the distance from the Planckian locus on the CIE 1931 xy chromaticity diagram, with the range ±50 mapping to ±0.01 D_uv

**Range of valid values:** 
The supported range, -50 to +50, corresponds to a D_uv distance of ±0.01 below and above the Planckian locus. Some camera devices may have limitations to achieving the full ±0.01 D_uv range at some color temperatures (e.g., below 1500K). In these cases, the applied D_uv value may be clamped and the actual color tint will be reported in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_COLOR_TINT:android.hardware.camera2.CaptureRequest.Key` result.

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_COLOR_TINT:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`

### COLOR_CORRECTION_GAINS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_CORRECTION_GAINS: CaptureRequest.Key<RggbChannelVector!>
```

Gains applying to Bayer raw color channels for white-balance.

These per-channel gains are either set by the camera device when the request `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` is not TRANSFORM_MATRIX, or directly by the application in the request when the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` is TRANSFORM_MATRIX.

The gains in the result metadata are the gains actually applied by the camera device to the current frame.

The valid range of gains varies on different devices, but gains between \[1.0, 3.0\] are guaranteed not to be clipped. Even if a given device allows gains below 1.0, this is usually not recommended because this can create color artifacts.

**Units**: Unitless gain factors

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`

### COLOR_CORRECTION_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_CORRECTION_MODE: CaptureRequest.Key<Int!>
```

The mode control selects how the image data is converted from the sensor's native color into linear sRGB color.

When auto-white balance (AWB) is enabled with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`, this control is overridden by the AWB routine. When AWB is disabled, the application controls how the color mapping is performed.

We define the expected processing pipeline below. For consistency across devices, this is always the case with TRANSFORM_MATRIX.

When either FAST or HIGH_QUALITY is used, the camera device may do additional processing but `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` will still be provided by the camera device (in the results) and be roughly correct.

Switching to TRANSFORM_MATRIX and using the data provided from FAST or HIGH_QUALITY will yield a picture with the same white point as what was produced by the camera device in the earlier frame.

The expected processing pipeline is as follows:

<br />

The white balance is encoded by two values, a 4-channel white-balance gain vector (applied in the Bayer domain), and a 3x3 color transform matrix (applied after demosaic).

The 4-channel white-balance gains are defined as:

```kotlin
<code><code><a docref="android.hardware.camera2.CaptureRequest$COLOR_CORRECTION_GAINS">android.colorCorrection.gains</a></code> = [ R G_even G_odd B ]
  </code>
```

where `G_even` is the gain for green pixels on even rows of the output, and `G_odd` is the gain for green pixels on the odd rows. These may be identical for a given camera device implementation; if the camera device does not support a separate gain for even/odd green channels, it will use the `G_even` value, and write `G_odd` equal to `G_even` in the output result metadata.

The matrices for color transforms are defined as a 9-entry vector:

```kotlin
<code><code><a docref="android.hardware.camera2.CaptureRequest$COLOR_CORRECTION_TRANSFORM">android.colorCorrection.transform</a></code> = [ I0 I1 I2 I3 I4 I5 I6 I7 I8 ]
  </code>
```

which define a transform from input sensor colors, `P_in = [ r g b ]`, to output linear sRGB, `P_out = [ r' g' b' ]`,

with colors as follows:

```kotlin
<code>r' = I0r + I1g + I2b
  g' = I3r + I4g + I5b
  b' = I6r + I7g + I8b
  </code>
```

Both the input and output value ranges must match. Overflow/underflow values are clipped to fit within the range.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_MODE_TRANSFORM_MATRIX:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_MODE_FAST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_MODE_HIGH_QUALITY:kotlin.Int`

**Available values for this device:** 
Starting from API level 36, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#COLOR_CORRECTION_AVAILABLE_MODES:android.hardware.camera2.CameraCharacteristics.Key` can be used to check the list of supported values. Prior to API level 36, TRANSFORM_MATRIX, HIGH_QUALITY, and FAST are guaranteed to be available as valid modes on devices that support this key.

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#COLOR_CORRECTION_AVAILABLE_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_MODE_TRANSFORM_MATRIX:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_MODE_FAST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_MODE_HIGH_QUALITY:kotlin.Int`

### COLOR_CORRECTION_TRANSFORM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_CORRECTION_TRANSFORM: CaptureRequest.Key<ColorSpaceTransform!>
```

A color transform matrix to use to transform from sensor RGB color space to output linear sRGB color space.

This matrix is either set by the camera device when the request `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` is not TRANSFORM_MATRIX, or directly by the application in the request when the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` is TRANSFORM_MATRIX.

In the latter case, the camera device may round the matrix to account for precision issues; the final rounded matrix should be reported back in this matrix result metadata. The transform should keep the magnitude of the output color values within `[0, 1.0]` (assuming input color values is within the normalized range `[0, 1.0]`), or clipping may occur.

The valid range of each matrix element varies on different devices, but values within \[-1.5, 3.0\] are guaranteed not to be clipped.

**Units**: Unitless scale factors

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`

### CONTROL_AE_ANTIBANDING_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_ANTIBANDING_MODE: CaptureRequest.Key<Int!>
```

The desired setting for the camera device's auto-exposure algorithm's antibanding compensation.

Some kinds of lighting fixtures, such as some fluorescent lights, flicker at the rate of the power supply frequency (60Hz or 50Hz, depending on country). While this is typically not noticeable to a person, it can be visible to a camera device. If a camera sets its exposure time to the wrong value, the flicker may become visible in the viewfinder as flicker or in a final captured image, as a set of variable-brightness bands across the image.

Therefore, the auto-exposure routines of camera devices include antibanding routines that ensure that the chosen exposure value will not cause such banding. The choice of exposure time depends on the rate of flicker, which the camera device can detect automatically, or the expected rate can be selected by the application using this control.

A given camera device may not support all of the possible options for the antibanding mode. The `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_ANTIBANDING_MODES:android.hardware.camera2.CameraCharacteristics.Key` key contains the available modes for a given camera device.

AUTO mode is the default if it is available on given camera device. When AUTO mode is not available, the default will be either 50HZ or 60HZ, and both 50HZ and 60HZ will be available.

If manual exposure control is enabled (by setting `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` to OFF), then this setting has no effect, and the application must ensure it selects exposure times that do not cause banding issues. The `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_SCENE_FLICKER:android.hardware.camera2.CaptureResult.Key` key can assist the application in this.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_ANTIBANDING_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_ANTIBANDING_MODE_50HZ:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_ANTIBANDING_MODE_60HZ:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_ANTIBANDING_MODE_AUTO:kotlin.Int`

**Available values for this device:** 

`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_ANTIBANDING_MODES:android.hardware.camera2.CameraCharacteristics.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_ANTIBANDING_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_SCENE_FLICKER:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_ANTIBANDING_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_ANTIBANDING_MODE_50HZ:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_ANTIBANDING_MODE_60HZ:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_ANTIBANDING_MODE_AUTO:kotlin.Int`

### CONTROL_AE_EXPOSURE_COMPENSATION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_EXPOSURE_COMPENSATION: CaptureRequest.Key<Int!>
```

Adjustment to auto-exposure (AE) target image brightness.

The adjustment is measured as a count of steps, with the step size defined by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_COMPENSATION_STEP:android.hardware.camera2.CameraCharacteristics.Key` and the allowed range by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_COMPENSATION_RANGE:android.hardware.camera2.CameraCharacteristics.Key`.

For example, if the exposure value (EV) step is 0.333, '6' will mean an exposure compensation of +2 EV; -3 will mean an exposure compensation of -1 EV. One EV represents a doubling of image brightness. Note that this control will only be effective if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key` `!=` OFF. This control will take effect even when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_LOCK:android.hardware.camera2.CaptureRequest.Key` `== true`.

In the event of exposure compensation value being changed, camera device may take several frames to reach the newly requested exposure target. During that time, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key` field will be in the SEARCHING state. Once the new exposure target is reached, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key` will change from SEARCHING to either CONVERGED, LOCKED (if AE lock is enabled), or FLASH_REQUIRED (if the scene is too dark for still capture).

**Units**: Compensation steps

**Range of valid values:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_COMPENSATION_RANGE:android.hardware.camera2.CameraCharacteristics.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_COMPENSATION_RANGE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_COMPENSATION_STEP:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_LOCK:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_AE_LOCK

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_LOCK: CaptureRequest.Key<Boolean!>
```

Whether auto-exposure (AE) is currently locked to its latest calculated values.

When set to `true` (ON), the AE algorithm is locked to its latest parameters, and will not change exposure settings until the lock is set to `false` (OFF).

Note that even when AE is locked, the flash may be fired if the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key` is ON_AUTO_FLASH / ON_ALWAYS_FLASH / ON_AUTO_FLASH_REDEYE.

When `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_EXPOSURE_COMPENSATION:android.hardware.camera2.CaptureRequest.Key` is changed, even if the AE lock is ON, the camera device will still adjust its exposure value.

If AE precapture is triggered (see `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key`) when AE is already locked, the camera device will not change the exposure time (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`) and sensitivity (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`) parameters. The flash may be fired if the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key` is ON_AUTO_FLASH/ON_AUTO_FLASH_REDEYE and the scene is too dark. If the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key` is ON_ALWAYS_FLASH, the scene may become overexposed. Similarly, AE precapture trigger CANCEL has no effect when AE is already locked.

When an AE precapture sequence is triggered, AE unlock will not be able to unlock the AE if AE is locked by the camera device internally during precapture metering sequence In other words, submitting requests with AE unlock has no effect for an ongoing precapture metering sequence. Otherwise, the precapture metering sequence will never succeed in a sequence of preview requests where AE lock is always set to `false`.

Since the camera device has a pipeline of in-flight requests, the settings that get locked do not necessarily correspond to the settings that were present in the latest capture result received from the camera device, since additional captures and AE updates may have occurred even before the result was sent out. If an application is switching between automatic and manual control and wishes to eliminate any flicker during the switch, the following procedure is recommended:

1. Starting in auto-AE mode:
2. Lock AE
3. Wait for the first result to be output that has the AE locked
4. Copy exposure settings from that result into a request, set the request to manual AE
5. Submit the capture request, proceed to run manual AE as desired.

See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key` for AE lock related state transition details.

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_EXPOSURE_COMPENSATION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_MODE: CaptureRequest.Key<Int!>
```

The desired mode for the camera device's auto-exposure routine.

This control is only effective if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` is AUTO.

When set to any of the ON modes, the camera device's auto-exposure routine is enabled, overriding the application's selected exposure time, sensor sensitivity, and frame duration (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key`). If `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRIORITY_MODE:android.hardware.camera2.CaptureRequest.Key` is enabled, the relevant priority CaptureRequest settings will not be overridden. See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRIORITY_MODE:android.hardware.camera2.CaptureRequest.Key` for more details. If one of the FLASH modes is selected, the camera device's flash unit controls are also overridden.

The FLASH modes are only available if the camera device has a flash unit (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_INFO_AVAILABLE:android.hardware.camera2.CameraCharacteristics.Key` is `true`).

If flash TORCH mode is desired, this field must be set to ON or OFF, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_MODE:android.hardware.camera2.CaptureRequest.Key` set to TORCH.

When set to any of the ON modes, the values chosen by the camera device auto-exposure routine for the overridden fields for a given capture will be available in its CaptureResult.

When `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key` is AE_MODE_ON and if the device supports manual flash strength control, i.e., if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_SINGLE_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_TORCH_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` are greater than 1, then the auto-exposure (AE) precapture metering sequence should be triggered to avoid the image being incorrectly exposed at different `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_STRENGTH_LEVEL:android.hardware.camera2.CaptureRequest.Key`.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_AUTO_FLASH:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_ALWAYS_FLASH:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_AUTO_FLASH_REDEYE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_EXTERNAL_FLASH:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_LOW_LIGHT_BOOST_BRIGHTNESS_PRIORITY:kotlin.Int`

**Available values for this device:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_MODES:android.hardware.camera2.CameraCharacteristics.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRIORITY_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_INFO_AVAILABLE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_SINGLE_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_STRENGTH_LEVEL:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_TORCH_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_AUTO_FLASH:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_ALWAYS_FLASH:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_AUTO_FLASH_REDEYE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_EXTERNAL_FLASH:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_LOW_LIGHT_BOOST_BRIGHTNESS_PRIORITY:kotlin.Int`

### CONTROL_AE_PRECAPTURE_TRIGGER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_PRECAPTURE_TRIGGER: CaptureRequest.Key<Int!>
```

Whether the camera device will trigger a precapture metering sequence when it processes this request.

This entry is normally set to IDLE, or is not included at all in the request settings. When included and set to START, the camera device will trigger the auto-exposure (AE) precapture metering sequence.

When set to CANCEL, the camera device will cancel any active precapture metering trigger, and return to its initial AE state. If a precapture metering sequence is already completed, and the camera device has implicitly locked the AE for subsequent still capture, the CANCEL trigger will unlock the AE and return to its initial AE state.

The precapture sequence should be triggered before starting a high-quality still capture for final metering decisions to be made, and for firing pre-capture flash pulses to estimate scene brightness and required final capture flash power, when the flash is enabled.

Flash is enabled during precapture sequence when:

- AE mode is ON_ALWAYS_FLASH
- AE mode is ON_AUTO_FLASH and the scene is deemed too dark without flash, or
- AE mode is ON and flash mode is TORCH or SINGLE

Normally, this entry should be set to START for only single request, and the application should wait until the sequence completes before starting a new one.

When a precapture metering sequence is finished, the camera device may lock the auto-exposure routine internally to be able to accurately expose the subsequent still capture image (`` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key` == STILL_CAPTURE ``). For this case, the AE may not resume normal scan if no subsequent still capture is submitted. To ensure that the AE routine restarts normal scan, the application should submit a request with `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_LOCK:android.hardware.camera2.CaptureRequest.Key` == true ``, followed by a request with `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_LOCK:android.hardware.camera2.CaptureRequest.Key` == false ``, if the application decides not to submit a still capture request after the precapture sequence completes. Alternatively, for API level 23 or newer devices, the CANCEL can be used to unlock the camera device internally locked AE if the application doesn't submit a still capture request after the AE precapture trigger. Note that, the CANCEL was added in API level 23, and must not be used in devices that have earlier API levels.

The exact effect of auto-exposure (AE) precapture trigger depends on the current AE mode and state; see `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key` for AE precapture state transition details.

On LEGACY-level devices, the precapture trigger is not supported; capturing a high-resolution JPEG image will automatically trigger a precapture sequence before the high-resolution capture, including potentially firing a pre-capture flash.

Using the precapture trigger and the auto-focus trigger `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key` simultaneously is allowed. However, since these triggers often require cooperation between the auto-focus and auto-exposure routines (for example, the may need to be enabled for a focus sweep), the camera device may delay acting on a later trigger until the previous trigger has been fully handled. This may lead to longer intervals between the trigger and changes to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key` indicating the start of the precapture sequence, for example.

If both the precapture and the auto-focus trigger are activated on the same request, then the camera device will complete them in the optimal order for that device.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRECAPTURE_TRIGGER_IDLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRECAPTURE_TRIGGER_START:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRECAPTURE_TRIGGER_CANCEL:kotlin.Int`

**Optional** - The value for this key may be `null` on some devices.

**Limited capability** - Present on all camera devices that report being at least `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_LOCK:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRECAPTURE_TRIGGER_IDLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRECAPTURE_TRIGGER_START:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRECAPTURE_TRIGGER_CANCEL:kotlin.Int`

### CONTROL_AE_PRIORITY_MODE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_PRIORITY_MODE: CaptureRequest.Key<Int!>
```

Turn on AE priority mode.

This control is only effective if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` is AUTO and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key` is set to one of its ON modes, with the exception of ON_LOW_LIGHT_BOOST_BRIGHTNESS_PRIORITY.

When a priority mode is enabled, the camera device's auto-exposure routine will maintain the application's selected parameters relevant to the priority mode while overriding the remaining exposure parameters (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key`). For example, if SENSOR_SENSITIVITY_PRIORITY mode is enabled, the camera device will maintain the application-selected `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key` while adjusting `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key`. The overridden fields for a given capture will be available in its CaptureResult.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRIORITY_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRIORITY_MODE_SENSOR_SENSITIVITY_PRIORITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRIORITY_MODE_SENSOR_EXPOSURE_TIME_PRIORITY:kotlin.Int`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRIORITY_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRIORITY_MODE_SENSOR_SENSITIVITY_PRIORITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRIORITY_MODE_SENSOR_EXPOSURE_TIME_PRIORITY:kotlin.Int`

### CONTROL_AE_REGIONS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_REGIONS: CaptureRequest.Key<Array<MeteringRectangle!>!>
```

List of metering areas to use for auto-exposure adjustment.

Not available if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_MAX_REGIONS_AE:android.hardware.camera2.CameraCharacteristics.Key` is 0. Otherwise will always be present.

The maximum number of regions supported by the device is determined by the value of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_MAX_REGIONS_AE:android.hardware.camera2.CameraCharacteristics.Key`.

For devices not supporting `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` control, the coordinate system always follows that of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`, with (0,0) being the top-left pixel in the active pixel array, and (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.width - 1, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.height - 1) being the bottom-right pixel in the active pixel array.

For devices supporting `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` control, the coordinate system depends on the mode being set. When the distortion correction mode is OFF, the coordinate system follows `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`, with `(0, 0)` being the top-left pixel of the pre-correction active array, and (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.width - 1, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.height - 1) being the bottom-right pixel in the pre-correction active pixel array. When the distortion correction mode is not OFF, the coordinate system follows `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`, with `(0, 0)` being the top-left pixel of the active array, and (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.width - 1, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.height - 1) being the bottom-right pixel in the active pixel array.

The weight must be within `[0, 1000]`, and represents a weight for every pixel in the area. This means that a large metering area with the same weight as a smaller area will have more effect in the metering result. Metering areas can partially overlap and the camera device will add the weights in the overlap region.

The weights are relative to weights of other exposure metering regions, so if only one region is used, all non-zero weights will have the same effect. A region with 0 weight is ignored.

If all regions have 0 weight, the camera device returns to the default auto-exposure metering behavior.

If the metering region is outside the used `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` returned in capture result metadata, the camera device will ignore the sections outside the crop region and output only the intersection rectangle as the metering region in the result metadata. If the region is entirely outside the crop region, it will be ignored and not reported in the result metadata.

When setting the AE metering regions, the application must consider the additional crop resulted from the aspect ratio differences between the preview stream and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`. For example, if the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` is the full active array size with 4:3 aspect ratio, and the preview stream is 16:9, the boundary of AE regions will be \[0, y_crop\] and \[active_width, active_height - 2 \* y_crop\] rather than \[0, 0\] and \[active_width, active_height\], where y_crop is the additional crop due to aspect ratio mismatch.

Starting from API level 30, the coordinate system of activeArraySize or preCorrectionActiveArraySize is used to represent post-zoomRatio field of view, not pre-zoom field of view. This means that the same aeRegions values at different `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` represent different parts of the scene. The aeRegions coordinates are relative to the activeArray/preCorrectionActiveArray representing the zoomed field of view. If `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` is set to 1.0 (default), the same aeRegions at different `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` still represent the same parts of the scene as they do before. See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` for details. Whether to use activeArraySize or preCorrectionActiveArraySize still depends on distortion correction mode.

For camera devices with the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR:kotlin.Int` capability or devices where `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getAvailableCaptureRequestKeys()` lists `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key` / `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key` must be used as the coordinate system for requests where `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` is set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`.

**Units** : Pixel coordinates within `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` depending on distortion correction capability and mode

**Range of valid values:** 
Coordinates must be between `[(0,0), (width, height))` of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` depending on distortion correction capability and mode

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_MAX_REGIONS_AE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_TARGET_FPS_RANGE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_TARGET_FPS_RANGE: CaptureRequest.Key<Range<Int!>!>
```

Range over which the auto-exposure routine can adjust the capture frame rate to maintain good exposure.

Only constrains auto-exposure (AE) algorithm, not manual control of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key`.

Note that the actual achievable max framerate also depends on the minimum frame duration of the output streams. The max frame rate will be `min(aeTargetFpsRange.maxFps, 1 / max(individual stream min durations))`. For example, if the application sets this key to `{60, 60}`, but the maximum minFrameDuration among all configured streams is 33ms, the maximum framerate won't be 60fps, but will be 30fps.

To start a CaptureSession with a target FPS range different from the capture request template's default value, the application is strongly recommended to call `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setSessionParameters(android.hardware.camera2.CaptureRequest)` with the target fps range before creating the capture session. The aeTargetFpsRange is typically a session parameter. Specifying it at session creation time helps avoid session reconfiguration delays in cases like 60fps or high speed recording.

**Units**: Frames per second (FPS)

**Range of valid values:** 
Any of the entries in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_TARGET_FPS_RANGES:android.hardware.camera2.CameraCharacteristics.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_TARGET_FPS_RANGES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AF_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AF_MODE: CaptureRequest.Key<Int!>
```

Whether auto-focus (AF) is currently enabled, and what mode it is set to.

Only effective if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` = AUTO and the lens is not fixed focus (i.e. `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key` > 0 ``). Also note that when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key` is OFF, the behavior of AF is device dependent. It is recommended to lock AF by using `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key` before setting `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key` to OFF, or set AF mode to OFF when AE is OFF.

If the lens is controlled by the camera device auto-focus algorithm, the camera device will report the current AF status in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AF_STATE:android.hardware.camera2.CaptureResult.Key` in result metadata.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_AUTO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_MACRO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_CONTINUOUS_VIDEO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_CONTINUOUS_PICTURE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_EDOF:kotlin.Int`

**Available values for this device:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AF_AVAILABLE_MODES:android.hardware.camera2.CameraCharacteristics.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AF_AVAILABLE_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AF_STATE:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_AUTO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_MACRO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_CONTINUOUS_VIDEO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_CONTINUOUS_PICTURE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_EDOF:kotlin.Int`

### CONTROL_AF_REGIONS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AF_REGIONS: CaptureRequest.Key<Array<MeteringRectangle!>!>
```

List of metering areas to use for auto-focus.

Not available if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_MAX_REGIONS_AF:android.hardware.camera2.CameraCharacteristics.Key` is 0. Otherwise will always be present.

The maximum number of focus areas supported by the device is determined by the value of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_MAX_REGIONS_AF:android.hardware.camera2.CameraCharacteristics.Key`.

For devices not supporting `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` control, the coordinate system always follows that of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`, with (0,0) being the top-left pixel in the active pixel array, and (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.width - 1, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.height - 1) being the bottom-right pixel in the active pixel array.

For devices supporting `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` control, the coordinate system depends on the mode being set. When the distortion correction mode is OFF, the coordinate system follows `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`, with `(0, 0)` being the top-left pixel of the pre-correction active array, and (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.width - 1, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.height - 1) being the bottom-right pixel in the pre-correction active pixel array. When the distortion correction mode is not OFF, the coordinate system follows `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`, with `(0, 0)` being the top-left pixel of the active array, and (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.width - 1, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.height - 1) being the bottom-right pixel in the active pixel array.

The weight must be within `[0, 1000]`, and represents a weight for every pixel in the area. This means that a large metering area with the same weight as a smaller area will have more effect in the metering result. Metering areas can partially overlap and the camera device will add the weights in the overlap region.

The weights are relative to weights of other metering regions, so if only one region is used, all non-zero weights will have the same effect. A region with 0 weight is ignored.

If all regions have 0 weight, the camera device returns to the default focus metering behavior. The capture result will either be a zero weight region as well, or the region selected by the camera device as the focus area of interest.

If the metering region is outside the used `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` returned in capture result metadata, the camera device will ignore the sections outside the crop region and output only the intersection rectangle as the metering region in the result metadata. If the region is entirely outside the crop region, it will be ignored and not reported in the result metadata.

When setting the AF metering regions, the application must consider the additional crop resulted from the aspect ratio differences between the preview stream and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`. For example, if the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` is the full active array size with 4:3 aspect ratio, and the preview stream is 16:9, the boundary of AF regions will be \[0, y_crop\] and \[active_width, active_height - 2 \* y_crop\] rather than \[0, 0\] and \[active_width, active_height\], where y_crop is the additional crop due to aspect ratio mismatch.

Starting from API level 30, the coordinate system of activeArraySize or preCorrectionActiveArraySize is used to represent post-zoomRatio field of view, not pre-zoom field of view. This means that the same afRegions values at different `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` represent different parts of the scene. The afRegions coordinates are relative to the activeArray/preCorrectionActiveArray representing the zoomed field of view. If `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` is set to 1.0 (default), the same afRegions at different `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` still represent the same parts of the scene as they do before. See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` for details. Whether to use activeArraySize or preCorrectionActiveArraySize still depends on distortion correction mode.

For camera devices with the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR:kotlin.Int` capability or devices where `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getAvailableCaptureRequestKeys()` lists `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key` / `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key` must be used as the coordinate system for requests where `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` is set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`.

**Units** : Pixel coordinates within `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` depending on distortion correction capability and mode

**Range of valid values:** 
Coordinates must be between `[(0,0), (width, height))` of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` depending on distortion correction capability and mode

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_MAX_REGIONS_AF:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AF_TRIGGER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AF_TRIGGER: CaptureRequest.Key<Int!>
```

Whether the camera device will trigger autofocus for this request.

This entry is normally set to IDLE, or is not included at all in the request settings.

When included and set to START, the camera device will trigger the autofocus algorithm. If autofocus is disabled, this trigger has no effect.

When set to CANCEL, the camera device will cancel any active trigger, and return to its initial AF state.

Generally, applications should set this entry to START or CANCEL for only a single capture, and then return it to IDLE (or not set at all). Specifying START for multiple captures in a row means restarting the AF operation over and over again.

See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AF_STATE:android.hardware.camera2.CaptureResult.Key` for what the trigger means for each AF mode.

Using the autofocus trigger and the precapture trigger `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key` simultaneously is allowed. However, since these triggers often require cooperation between the auto-focus and auto-exposure routines (for example, the may need to be enabled for a focus sweep), the camera device may delay acting on a later trigger until the previous trigger has been fully handled. This may lead to longer intervals between the trigger and changes to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AF_STATE:android.hardware.camera2.CaptureResult.Key`, for example.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_TRIGGER_IDLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_TRIGGER_START:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_TRIGGER_CANCEL:kotlin.Int`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AF_STATE:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_TRIGGER_IDLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_TRIGGER_START:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_TRIGGER_CANCEL:kotlin.Int`

### CONTROL_AUTOFRAMING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AUTOFRAMING: CaptureRequest.Key<Int!>
```

Automatic crop, pan and zoom to keep objects in the center of the frame.

Auto-framing is a special mode provided by the camera device to dynamically crop, zoom or pan the camera feed to try to ensure that the people in a scene occupy a reasonable portion of the viewport. It is primarily designed to support video calling in situations where the user isn't directly in front of the device, especially for wide-angle cameras. `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` in CaptureResult will be used to denote the coordinates of the auto-framed region. Zoom and video stabilization controls are disabled when auto-framing is enabled. The 3A regions must map the screen coordinates into the scaler crop returned from the capture result instead of using the active array sensor.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AUTOFRAMING_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AUTOFRAMING_ON:kotlin.Int`

**Optional** - The value for this key may be `null` on some devices.

**Limited capability** - Present on all camera devices that report being at least `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AUTOFRAMING_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AUTOFRAMING_ON:kotlin.Int`

### CONTROL_AWB_LOCK

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AWB_LOCK: CaptureRequest.Key<Boolean!>
```

Whether auto-white balance (AWB) is currently locked to its latest calculated values.

When set to `true` (ON), the AWB algorithm is locked to its latest parameters, and will not change color balance settings until the lock is set to `false` (OFF).

Since the camera device has a pipeline of in-flight requests, the settings that get locked do not necessarily correspond to the settings that were present in the latest capture result received from the camera device, since additional captures and AWB updates may have occurred even before the result was sent out. If an application is switching between automatic and manual control and wishes to eliminate any flicker during the switch, the following procedure is recommended:

1. Starting in auto-AWB mode:
2. Lock AWB
3. Wait for the first result to be output that has the AWB locked
4. Copy AWB settings from that result into a request, set the request to manual AWB
5. Submit the capture request, proceed to run manual AWB as desired.

Note that AWB lock is only meaningful when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key` is in the AUTO mode; in other modes, AWB is already fixed to a specific setting.

Some LEGACY devices may not support ON; the value is then overridden to OFF.

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AWB_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AWB_MODE: CaptureRequest.Key<Int!>
```

Whether auto-white balance (AWB) is currently setting the color transform fields, and what its illumination target is.

This control is only effective if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` is AUTO.

When set to the AUTO mode, the camera device's auto-white balance routine is enabled, overriding the application's selected `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`. Note that when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key` is OFF, the behavior of AWB is device dependent. It is recommended to also set AWB mode to OFF or lock AWB by using `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_LOCK:android.hardware.camera2.CaptureRequest.Key` before setting AE mode to OFF.

When set to the OFF mode, the camera device's auto-white balance routine is disabled. The application manually controls the white balance by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`.

When set to any other modes, the camera device's auto-white balance routine is disabled. The camera device uses each particular illumination target for white balance adjustment. The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` are ignored.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_AUTO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_INCANDESCENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_FLUORESCENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_WARM_FLUORESCENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_DAYLIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_CLOUDY_DAYLIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_TWILIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_SHADE:kotlin.Int`

**Available values for this device:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AWB_AVAILABLE_MODES:android.hardware.camera2.CameraCharacteristics.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AWB_AVAILABLE_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_LOCK:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_AUTO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_INCANDESCENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_FLUORESCENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_WARM_FLUORESCENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_DAYLIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_CLOUDY_DAYLIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_TWILIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_SHADE:kotlin.Int`

### CONTROL_AWB_REGIONS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AWB_REGIONS: CaptureRequest.Key<Array<MeteringRectangle!>!>
```

List of metering areas to use for auto-white-balance illuminant estimation.

Not available if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_MAX_REGIONS_AWB:android.hardware.camera2.CameraCharacteristics.Key` is 0. Otherwise will always be present.

The maximum number of regions supported by the device is determined by the value of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_MAX_REGIONS_AWB:android.hardware.camera2.CameraCharacteristics.Key`.

For devices not supporting `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` control, the coordinate system always follows that of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`, with (0,0) being the top-left pixel in the active pixel array, and (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.width - 1, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.height - 1) being the bottom-right pixel in the active pixel array.

For devices supporting `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` control, the coordinate system depends on the mode being set. When the distortion correction mode is OFF, the coordinate system follows `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`, with `(0, 0)` being the top-left pixel of the pre-correction active array, and (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.width - 1, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.height - 1) being the bottom-right pixel in the pre-correction active pixel array. When the distortion correction mode is not OFF, the coordinate system follows `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`, with `(0, 0)` being the top-left pixel of the active array, and (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.width - 1, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.height - 1) being the bottom-right pixel in the active pixel array.

The weight must range from 0 to 1000, and represents a weight for every pixel in the area. This means that a large metering area with the same weight as a smaller area will have more effect in the metering result. Metering areas can partially overlap and the camera device will add the weights in the overlap region.

The weights are relative to weights of other white balance metering regions, so if only one region is used, all non-zero weights will have the same effect. A region with 0 weight is ignored.

If all regions have 0 weight, the camera device returns to the default white balance metering behavior.

If the metering region is outside the used `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` returned in capture result metadata, the camera device will ignore the sections outside the crop region and output only the intersection rectangle as the metering region in the result metadata. If the region is entirely outside the crop region, it will be ignored and not reported in the result metadata.

When setting the AWB metering regions, the application must consider the additional crop resulted from the aspect ratio differences between the preview stream and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`. For example, if the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` is the full active array size with 4:3 aspect ratio, and the preview stream is 16:9, the boundary of AWB regions will be \[0, y_crop\] and \[active_width, active_height - 2 \* y_crop\] rather than \[0, 0\] and \[active_width, active_height\], where y_crop is the additional crop due to aspect ratio mismatch.

Starting from API level 30, the coordinate system of activeArraySize or preCorrectionActiveArraySize is used to represent post-zoomRatio field of view, not pre-zoom field of view. This means that the same awbRegions values at different `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` represent different parts of the scene. The awbRegions coordinates are relative to the activeArray/preCorrectionActiveArray representing the zoomed field of view. If `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` is set to 1.0 (default), the same awbRegions at different `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` still represent the same parts of the scene as they do before. See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` for details. Whether to use activeArraySize or preCorrectionActiveArraySize still depends on distortion correction mode.

For camera devices with the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR:kotlin.Int` capability or devices where `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getAvailableCaptureRequestKeys()` lists `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key` / `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key` must be used as the coordinate system for requests where `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` is set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`.

**Units** : Pixel coordinates within `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` depending on distortion correction capability and mode

**Range of valid values:** 
Coordinates must be between `[(0,0), (width, height))` of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` depending on distortion correction capability and mode

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_MAX_REGIONS_AWB:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_CAPTURE_INTENT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_CAPTURE_INTENT: CaptureRequest.Key<Int!>
```

Information to the camera device 3A (auto-exposure, auto-focus, auto-white balance) routines about the purpose of this capture, to help the camera device to decide optimal 3A strategy.

This control (except for MANUAL) is only effective if `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` != OFF `` and any 3A routine is active.

All intents are supported by all devices, except that:

- ZERO_SHUTTER_LAG will be supported if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` contains PRIVATE_REPROCESSING or YUV_REPROCESSING.
- MANUAL will be supported if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` contains MANUAL_SENSOR.
- MOTION_TRACKING will be supported if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` contains MOTION_TRACKING.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_CUSTOM:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_PREVIEW:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_STILL_CAPTURE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_VIDEO_RECORD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_VIDEO_SNAPSHOT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_ZERO_SHUTTER_LAG:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_MANUAL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_MOTION_TRACKING:kotlin.Int`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_CUSTOM:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_PREVIEW:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_STILL_CAPTURE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_VIDEO_RECORD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_VIDEO_SNAPSHOT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_ZERO_SHUTTER_LAG:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_MANUAL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_MOTION_TRACKING:kotlin.Int`

### CONTROL_EFFECT_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_EFFECT_MODE: CaptureRequest.Key<Int!>
```

A special color effect to apply.

When this mode is set, a color effect will be applied to images produced by the camera device. The interpretation and implementation of these color effects is left to the implementor of the camera device, and should not be depended on to be consistent (or present) across all devices.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_MONO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_NEGATIVE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_SOLARIZE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_SEPIA:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_POSTERIZE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_WHITEBOARD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_BLACKBOARD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_AQUA:kotlin.Int`

**Available values for this device:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_EFFECTS:android.hardware.camera2.CameraCharacteristics.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_EFFECTS:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_MONO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_NEGATIVE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_SOLARIZE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_SEPIA:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_POSTERIZE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_WHITEBOARD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_BLACKBOARD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_AQUA:kotlin.Int`

### CONTROL_ENABLE_ZSL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_ENABLE_ZSL: CaptureRequest.Key<Boolean!>
```

Allow camera device to enable zero-shutter-lag mode for requests with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key` == STILL_CAPTURE.

If enableZsl is `true`, the camera device may enable zero-shutter-lag mode for requests with STILL_CAPTURE capture intent. The camera device may use images captured in the past to produce output images for a zero-shutter-lag request. The result metadata including the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_TIMESTAMP:android.hardware.camera2.CaptureResult.Key` reflects the source frames used to produce output images. Therefore, the contents of the output images and the result metadata may be out of order compared to previous regular requests. enableZsl does not affect requests with other capture intents.

For example, when requests are submitted in the following order: Request A: enableZsl is ON, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key` is PREVIEW Request B: enableZsl is ON, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key` is STILL_CAPTURE

The output images for request B may have contents captured before the output images for request A, and the result metadata for request B may be older than the result metadata for request A.

Note that when enableZsl is `true`, it is not guaranteed to get output images captured in the past for requests with STILL_CAPTURE capture intent.

For applications targeting SDK versions O and newer, the value of enableZsl in TEMPLATE_STILL_CAPTURE template may be `true`. The value in other templates is always `false` if present.

For applications targeting SDK versions older than O, the value of enableZsl in all capture templates is always `false` if present.

For application-operated ZSL, use CAMERA3_TEMPLATE_ZERO_SHUTTER_LAG template.

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_TIMESTAMP:android.hardware.camera2.CaptureResult.Key`

### CONTROL_EXTENDED_SCENE_MODE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_EXTENDED_SCENE_MODE: CaptureRequest.Key<Int!>
```

Whether extended scene mode is enabled for a particular capture request.

With bokeh mode, the camera device may blur out the parts of scene that are not in focus, creating a bokeh (or shallow depth of field) effect for people or objects.

When set to BOKEH_STILL_CAPTURE mode with STILL_CAPTURE capture intent, due to the extra processing needed for high quality bokeh effect, the stall may be longer than when capture intent is not STILL_CAPTURE.

When set to BOKEH_STILL_CAPTURE mode with PREVIEW capture intent,

- If the camera device has BURST_CAPTURE capability, the frame rate requirement of BURST_CAPTURE must still be met.
- All streams not larger than the maximum streaming dimension for BOKEH_STILL_CAPTURE mode (queried via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_EXTENDED_SCENE_MODE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`) will have preview bokeh effect applied.

When set to BOKEH_CONTINUOUS mode, configured streams dimension should not exceed this mode's maximum streaming dimension in order to have bokeh effect applied. Bokeh effect may not be available for streams larger than the maximum streaming dimension.

Switching between different extended scene modes may involve reconfiguration of the camera pipeline, resulting in long latency. The application should check this key against the available session keys queried via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getAvailableSessionKeys()`.

For a logical multi-camera, bokeh may be implemented by stereo vision from sub-cameras with different field of view. As a result, when bokeh mode is enabled, the camera device may override `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`, and the field of view may be smaller than when bokeh mode is off.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EXTENDED_SCENE_MODE_DISABLED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EXTENDED_SCENE_MODE_BOKEH_STILL_CAPTURE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EXTENDED_SCENE_MODE_BOKEH_CONTINUOUS:kotlin.Int`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EXTENDED_SCENE_MODE_DISABLED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EXTENDED_SCENE_MODE_BOKEH_STILL_CAPTURE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EXTENDED_SCENE_MODE_BOKEH_CONTINUOUS:kotlin.Int`

### CONTROL_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_MODE: CaptureRequest.Key<Int!>
```

Overall mode of 3A (auto-exposure, auto-white-balance, auto-focus) control routines.

This is a top-level 3A control switch. When set to OFF, all 3A control by the camera device is disabled. The application must set the fields for capture parameters itself.

When set to AUTO, the individual algorithm controls in android.control.\* are in effect, such as `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`.

When set to USE_SCENE_MODE or USE_EXTENDED_SCENE_MODE, the individual controls in android.control.\* are mostly disabled, and the camera device implements one of the scene mode or extended scene mode settings (such as ACTION, SUNSET, PARTY, or BOKEH) as it wishes. The camera device scene mode 3A settings are provided by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult`.

When set to OFF_KEEP_STATE, it is similar to OFF mode, the only difference is that this frame will not be used by camera device background 3A statistics update, as if this frame is never captured. This mode can be used in the scenario where the application doesn't want a 3A manual control capture to affect the subsequent auto 3A capture results.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_AUTO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_USE_SCENE_MODE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_OFF_KEEP_STATE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_USE_EXTENDED_SCENE_MODE:kotlin.Int`

**Available values for this device:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_MODES:android.hardware.camera2.CameraCharacteristics.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_AUTO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_USE_SCENE_MODE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_OFF_KEEP_STATE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_USE_EXTENDED_SCENE_MODE:kotlin.Int`

### CONTROL_POST_RAW_SENSITIVITY_BOOST

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_POST_RAW_SENSITIVITY_BOOST: CaptureRequest.Key<Int!>
```

The amount of additional sensitivity boost applied to output images after RAW sensor data is captured.

Some camera devices support additional digital sensitivity boosting in the camera processing pipeline after sensor RAW image is captured. Such a boost will be applied to YUV/JPEG format output images but will not have effect on RAW output formats like RAW_SENSOR, RAW10, RAW12, RAW14 or RAW_OPAQUE.

This key will be `null` for devices that do not support any RAW format outputs. For devices that do support RAW format outputs, this key will always present, and if a device does not support post RAW sensitivity boost, it will list `100` in this key.

If the camera device cannot apply the exact boost requested, it will reduce the boost to the nearest supported value. The final boost value used will be available in the output capture result.

For devices that support post RAW sensitivity boost, the YUV/JPEG output images of such device will have the total sensitivity of `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key` * `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_POST_RAW_SENSITIVITY_BOOST:android.hardware.camera2.CaptureRequest.Key` / 100 `` The sensitivity of RAW format images will always be `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key` ``

This control is only effective if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` is set to OFF; otherwise the auto-exposure algorithm will override this value.

**Units** : ISO arithmetic units, the same as `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`

**Range of valid values:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_POST_RAW_SENSITIVITY_BOOST_RANGE:android.hardware.camera2.CameraCharacteristics.Key`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_POST_RAW_SENSITIVITY_BOOST:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_POST_RAW_SENSITIVITY_BOOST_RANGE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_SCENE_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_SCENE_MODE: CaptureRequest.Key<Int!>
```

Control for which scene mode is currently active.

Scene modes are custom camera modes optimized for a certain set of conditions and capture settings.

This is the mode that that is active when `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` == USE_SCENE_MODE ``. Aside from FACE_PRIORITY, these modes will disable `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key` while in use.

The interpretation and implementation of these scene modes is left to the implementor of the camera device. Their behavior will not be consistent across all devices, and any given device may only implement a subset of these modes.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_DISABLED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_FACE_PRIORITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_ACTION:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_PORTRAIT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_LANDSCAPE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_NIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_NIGHT_PORTRAIT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_THEATRE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_BEACH:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_SNOW:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_SUNSET:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_STEADYPHOTO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_FIREWORKS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_SPORTS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_PARTY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_CANDLELIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_BARCODE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_HIGH_SPEED_VIDEO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_HDR:kotlin.Int`

**Available values for this device:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_SCENE_MODES:android.hardware.camera2.CameraCharacteristics.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_SCENE_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_DISABLED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_FACE_PRIORITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_ACTION:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_PORTRAIT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_LANDSCAPE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_NIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_NIGHT_PORTRAIT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_THEATRE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_BEACH:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_SNOW:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_SUNSET:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_STEADYPHOTO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_FIREWORKS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_SPORTS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_PARTY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_CANDLELIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_BARCODE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_HIGH_SPEED_VIDEO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_HDR:kotlin.Int`

### CONTROL_SETTINGS_OVERRIDE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_SETTINGS_OVERRIDE: CaptureRequest.Key<Int!>
```

The desired CaptureRequest settings override with which certain keys are applied earlier so that they can take effect sooner.

There are some CaptureRequest keys which can be applied earlier than others when controls within a CaptureRequest aren't required to take effect at the same time. One such example is zoom. Zoom can be applied at a later stage of the camera pipeline. As soon as the camera device receives the CaptureRequest, it can apply the requested zoom value onto an earlier request that's already in the pipeline, thus improves zoom latency.

This key's value in the capture result reflects whether the controls for this capture are overridden "by" a newer request. This means that if a capture request turns on settings override, the capture result of an earlier request will contain the key value of ZOOM. On the other hand, if a capture request has settings override turned on, but all newer requests have it turned off, the key's value in the capture result will be OFF because this capture isn't overridden by a newer capture. In the two examples below, the capture results columns illustrate the settingsOverride values in different scenarios.

Assuming the zoom settings override can speed up by 1 frame, below example illustrates the speed-up at the start of capture session:

```kotlin
<code>Camera session created
  Request 1 (zoom=1.0x, override=ZOOM) -&gt;
  Request 2 (zoom=1.2x, override=ZOOM) -&gt;
  Request 3 (zoom=1.4x, override=ZOOM) -&gt;  Result 1 (zoom=1.2x, override=ZOOM)
  Request 4 (zoom=1.6x, override=ZOOM) -&gt;  Result 2 (zoom=1.4x, override=ZOOM)
  Request 5 (zoom=1.8x, override=ZOOM) -&gt;  Result 3 (zoom=1.6x, override=ZOOM)
                                       -&gt;  Result 4 (zoom=1.8x, override=ZOOM)
                                       -&gt;  Result 5 (zoom=1.8x, override=OFF)
  </code>
```

The application can turn on settings override and use zoom as normal. The example shows that the later zoom values (1.2x, 1.4x, 1.6x, and 1.8x) overwrite the zoom values (1.0x, 1.2x, 1.4x, and 1.8x) of earlier requests (#1, #2, #3, and #4).

The application must make sure the settings override doesn't interfere with user journeys requiring simultaneous application of all controls in CaptureRequest on the requested output targets. For example, if the application takes a still capture using CameraCaptureSession#capture, and the repeating request immediately sets a different zoom value using override, the inflight still capture could have its zoom value overwritten unexpectedly.

So the application is strongly recommended to turn off settingsOverride when taking still/burst captures, and turn it back on when there is only repeating viewfinder request and no inflight still/burst captures.

Below is the example demonstrating the transitions in and out of the settings override:

```kotlin
<code>Request 1 (zoom=1.0x, override=OFF)
  Request 2 (zoom=1.2x, override=OFF)
  Request 3 (zoom=1.4x, override=ZOOM)  -&gt; Result 1 (zoom=1.0x, override=OFF)
  Request 4 (zoom=1.6x, override=ZOOM)  -&gt; Result 2 (zoom=1.4x, override=ZOOM)
  Request 5 (zoom=1.8x, override=OFF)   -&gt; Result 3 (zoom=1.6x, override=ZOOM)
                                        -&gt; Result 4 (zoom=1.6x, override=OFF)
                                        -&gt; Result 5 (zoom=1.8x, override=OFF)
  </code>
```

This example shows that:

- The application "ramps in" settings override by setting the control to ZOOM. In the example, request #3 enables zoom settings override. Because the camera device can speed up applying zoom by 1 frame, the outputs of request #2 has 1.4x zoom, the value specified in request #3.
- The application "ramps out" of settings override by setting the control to OFF. In the example, request #5 changes the override to OFF. Because request #4's zoom takes effect in result #3, result #4's zoom remains the same until new value takes effect in result #5.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SETTINGS_OVERRIDE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SETTINGS_OVERRIDE_ZOOM:kotlin.Int`

**Available values for this device:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_SETTINGS_OVERRIDES:android.hardware.camera2.CameraCharacteristics.Key`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_SETTINGS_OVERRIDES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SETTINGS_OVERRIDE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SETTINGS_OVERRIDE_ZOOM:kotlin.Int`

### CONTROL_VIDEO_STABILIZATION_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_VIDEO_STABILIZATION_MODE: CaptureRequest.Key<Int!>
```

Whether video stabilization is active.

Video stabilization automatically warps images from the camera in order to stabilize motion between consecutive frames.

If enabled, video stabilization can modify the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` to keep the video stream stabilized.

Switching between different video stabilization modes may take several frames to initialize, the camera device will report the current mode in capture result metadata. For example, When "ON" mode is requested, the video stabilization modes in the first several capture results may still be "OFF", and it will become "ON" when the initialization is done.

In addition, not all recording sizes or frame rates may be supported for stabilization by a device that reports stabilization support. It is guaranteed that an output targeting a MediaRecorder or MediaCodec will be stabilized if the recording resolution is less than or equal to 1920 x 1080 (width less than or equal to 1920, height less than or equal to 1080), and the recording frame rate is less than or equal to 30fps. At other sizes, the CaptureResult `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_VIDEO_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key` field will return OFF if the recording output is not stabilized, or if there are no output Surface types that can be stabilized.

The application is strongly recommended to call `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setSessionParameters(android.hardware.camera2.CaptureRequest)` with the desired video stabilization mode before creating the capture session. Video stabilization mode is a session parameter on many devices. Specifying it at session creation time helps avoid reconfiguration delay caused by difference between the default value and the first CaptureRequest.

If a camera device supports both this mode and OIS (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_OPTICAL_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key`), turning both modes on may produce undesirable interaction, so it is recommended not to enable both at the same time.

If video stabilization is set to "PREVIEW_STABILIZATION", `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_OPTICAL_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key` is overridden. The camera sub-system may choose to turn on hardware based image stabilization in addition to software based stabilization if it deems that appropriate. This key may be a part of the available session keys, which camera clients may query via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getAvailableSessionKeys()`. If this is the case, changing this key over the life-time of a capture session may cause delays / glitches.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_VIDEO_STABILIZATION_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_VIDEO_STABILIZATION_MODE_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_VIDEO_STABILIZATION_MODE_PREVIEW_STABILIZATION:kotlin.Int`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_VIDEO_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_OPTICAL_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_VIDEO_STABILIZATION_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_VIDEO_STABILIZATION_MODE_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_VIDEO_STABILIZATION_MODE_PREVIEW_STABILIZATION:kotlin.Int`

### CONTROL_ZOOM_METHOD

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_ZOOM_METHOD: CaptureRequest.Key<Int!>
```

Whether the application uses `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` to control zoom levels.

If set to AUTO, the camera device detects which capture request key the application uses to do zoom, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`. If the application doesn't set `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` or sets it to 1.0 in the capture request, the effective zoom level is reflected in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` in capture results. If `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` is set to values other than 1.0, the effective zoom level is reflected in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`. AUTO is the default value for this control, and also the behavior of the OS before Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int`.

If set to ZOOM_RATIO, the application explicitly specifies zoom level be controlled by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`, and the effective zoom level is reflected in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` in capture results. This addresses an ambiguity with AUTO, with which the camera device cannot know if the application is using cropRegion or zoomRatio at 1.0x.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_ZOOM_METHOD_AUTO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_ZOOM_METHOD_ZOOM_RATIO:kotlin.Int`

**Optional** - The value for this key may be `null` on some devices.

**Limited capability** - Present on all camera devices that report being at least `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_ZOOM_METHOD_AUTO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_ZOOM_METHOD_ZOOM_RATIO:kotlin.Int`

### CONTROL_ZOOM_RATIO

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_ZOOM_RATIO: CaptureRequest.Key<Float!>
```

The desired zoom ratio

Instead of using `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` for zoom, the application can now choose to use this tag to specify the desired zoom level.

By using this control, the application gains a simpler way to control zoom, which can be a combination of optical and digital zoom. For example, a multi-camera system may contain more than one lens with different focal lengths, and the user can use optical zoom by switching between lenses. Using zoomRatio has benefits in the scenarios below:

- Zooming in from a wide-angle lens to a telephoto lens: A floating-point ratio provides better precision compared to an integer value of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`.
- Zooming out from a wide lens to an ultrawide lens: zoomRatio supports zoom-out whereas `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` doesn't.

To illustrate, here are several scenarios of different zoom ratios, crop regions, and output streams, for a hypothetical camera device with an active array of size `(2000,1500)`.

- Camera Configuration:
 - Active array size: `2000x1500` (3 MP, 4:3 aspect ratio)
 - Output stream #1: `640x480` (VGA, 4:3 aspect ratio)
 - Output stream #2: `1280x720` (720p, 16:9 aspect ratio)
- Case #1: 4:3 crop region with 2.0x zoom ratio
 - Zoomed field of view: 1/4 of original field of view
 - Crop region: `Rect(0, 0, 2000, 1500) // (left, top, right, bottom)` (post zoom)
-
 - `640x480` stream source area: `(0, 0, 2000, 1500)` (equal to crop region)
 - `1280x720` stream source area: `(0, 187, 2000, 1312)` (letterboxed)
- Case #2: 16:9 crop region with 2.0x zoom.
 - Zoomed field of view: 1/4 of original field of view
 - Crop region: `Rect(0, 187, 2000, 1312)`
 - 
 - `640x480` stream source area: `(250, 187, 1750, 1312)` (pillarboxed)
 - `1280x720` stream source area: `(0, 187, 2000, 1312)` (equal to crop region)
- Case #3: 1:1 crop region with 0.5x zoom out to ultrawide lens.
 - Zoomed field of view: 4x of original field of view (switched from wide lens to ultrawide lens)
 - Crop region: `Rect(250, 0, 1750, 1500)`
 - 
 - `640x480` stream source area: `(250, 187, 1750, 1312)` (letterboxed)
 - `1280x720` stream source area: `(250, 328, 1750, 1172)` (letterboxed)

As seen from the graphs above, the coordinate system of cropRegion now changes to the effective after-zoom field-of-view, and is represented by the rectangle of (0, 0, activeArrayWith, activeArrayHeight). The same applies to AE/AWB/AF regions, and faces. This coordinate system change isn't applicable to RAW capture and its related metadata such as intrinsicCalibration and lensShadingMap.

Using the same hypothetical example above, and assuming output stream #1 (640x480) is the viewfinder stream, the application can achieve 2.0x zoom in one of two ways:

- zoomRatio = 2.0, scaler.cropRegion = (0, 0, 2000, 1500)
- zoomRatio = 1.0 (default), scaler.cropRegion = (500, 375, 1500, 1125)

If the application intends to set aeRegions to be top-left quarter of the viewfinder field-of-view, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key` should be set to (0, 0, 1000, 750) with zoomRatio set to 2.0. Alternatively, the application can set aeRegions to the equivalent region of (500, 375, 1000, 750) for zoomRatio of 1.0. If the application doesn't explicitly set `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`, its value defaults to 1.0.

One limitation of controlling zoom using zoomRatio is that the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` must only be used for letterboxing or pillarboxing of the sensor active array, and no FREEFORM cropping can be used with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` other than 1.0. If `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` is not 1.0, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` is set to be windowboxing, the camera framework will override the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` to be the active array.

In the capture request, if the application sets `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` to a value != 1.0, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` tag in the capture result reflects the effective zoom ratio achieved by the camera device, and the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` adjusts for additional crops that are not zoom related. Otherwise, if the application sets `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` to 1.0, or does not set it at all, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` tag in the result metadata will also be 1.0.

When the application requests a physical stream for a logical multi-camera, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` in the physical camera result metadata will be 1.0, and the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` tag reflects the amount of zoom and crop done by the physical camera device.

**Range of valid values:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_ZOOM_RATIO_RANGE:android.hardware.camera2.CameraCharacteristics.Key`

**Optional** - The value for this key may be `null` on some devices.

**Limited capability** - Present on all camera devices that report being at least `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_ZOOM_RATIO_RANGE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<CaptureRequest!>
```

### DISTORTION_CORRECTION_MODE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISTORTION_CORRECTION_MODE: CaptureRequest.Key<Int!>
```

Mode of operation for the lens distortion correction block.

The lens distortion correction block attempts to improve image quality by fixing radial, tangential, or other geometric aberrations in the camera device's optics. If available, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key` field documents the lens's distortion parameters.

OFF means no distortion correction is done.

FAST/HIGH_QUALITY both mean camera device determined distortion correction will be applied. HIGH_QUALITY mode indicates that the camera device will use the highest-quality correction algorithms, even if it slows down capture rate. FAST means the camera device will not slow down capture rate when applying correction. FAST may be the same as OFF if any correction at all would slow down capture rate. Every output stream will have a similar amount of enhancement applied.

The correction only applies to processed outputs such as YUV, Y8, JPEG, or DEPTH16; it is not applied to any RAW output.

This control will be on by default on devices that support this control. Applications disabling distortion correction need to pay extra attention with the coordinate system of metering regions, crop region, and face rectangles. When distortion correction is OFF, metadata coordinates follow the coordinate system of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`. When distortion is not OFF, metadata coordinates follow the coordinate system of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`. The camera device will map these metadata fields to match the corrected image produced by the camera device, for both capture requests and results. However, this mapping is not very precise, since rectangles do not generally map to rectangles when corrected. Only linear scaling between the active array and precorrection active array coordinates is performed. Applications that require precise correction of metadata need to undo that linear scaling, and apply a more complete correction that takes into the account the app's own requirements.

The full list of metadata that is affected in this way by distortion correction is:

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_FACES:android.hardware.camera2.CaptureResult.Key`

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#DISTORTION_CORRECTION_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#DISTORTION_CORRECTION_MODE_FAST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#DISTORTION_CORRECTION_MODE_HIGH_QUALITY:kotlin.Int`

**Available values for this device:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#DISTORTION_CORRECTION_AVAILABLE_MODES:android.hardware.camera2.CameraCharacteristics.Key`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#DISTORTION_CORRECTION_AVAILABLE_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_FACES:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#DISTORTION_CORRECTION_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#DISTORTION_CORRECTION_MODE_FAST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#DISTORTION_CORRECTION_MODE_HIGH_QUALITY:kotlin.Int`

### EDGE_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EDGE_MODE: CaptureRequest.Key<Int!>
```

Operation mode for edge enhancement.

Edge enhancement improves sharpness and details in the captured image. OFF means no enhancement will be applied by the camera device.

FAST/HIGH_QUALITY both mean camera device determined enhancement will be applied. HIGH_QUALITY mode indicates that the camera device will use the highest-quality enhancement algorithms, even if it slows down capture rate. FAST means the camera device will not slow down capture rate when applying edge enhancement. FAST may be the same as OFF if edge enhancement will slow down capture rate. Every output stream will have a similar amount of enhancement applied.

ZERO_SHUTTER_LAG is meant to be used by applications that maintain a continuous circular buffer of high-resolution images during preview and reprocess image(s) from that buffer into a final capture when triggered by the user. In this mode, the camera device applies edge enhancement to low-resolution streams (below maximum recording resolution) to maximize preview quality, but does not apply edge enhancement to high-resolution streams, since those will be reprocessed later if necessary.

For YUV_REPROCESSING, these FAST/HIGH_QUALITY modes both mean that the camera device will apply FAST/HIGH_QUALITY YUV-domain edge enhancement, respectively. The camera device may adjust its internal edge enhancement parameters for best image quality based on the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#REPROCESS_EFFECTIVE_EXPOSURE_FACTOR:android.hardware.camera2.CaptureRequest.Key`, if it is set.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EDGE_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EDGE_MODE_FAST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EDGE_MODE_HIGH_QUALITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EDGE_MODE_ZERO_SHUTTER_LAG:kotlin.Int`

**Available values for this device:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#EDGE_AVAILABLE_EDGE_MODES:android.hardware.camera2.CameraCharacteristics.Key`

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#EDGE_AVAILABLE_EDGE_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#REPROCESS_EFFECTIVE_EXPOSURE_FACTOR:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EDGE_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EDGE_MODE_FAST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EDGE_MODE_HIGH_QUALITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EDGE_MODE_ZERO_SHUTTER_LAG:kotlin.Int`

### EXTENSION_STRENGTH

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTENSION_STRENGTH: CaptureRequest.Key<Int!>
```

Strength of the extension post-processing effect

This control allows Camera extension clients to configure the strength of the applied extension effect. Strength equal to 0 means that the extension must not apply any post-processing and return a regular captured frame. Strength equal to 100 is the maximum level of post-processing. Values between 0 and 100 will have different effect depending on the extension type as described below:

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_BOKEH:kotlin.Int` - the strength is expected to control the amount of blur.
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_HDR:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_NIGHT:kotlin.Int` - the strength can control the amount of images fused and the brightness of the final image.
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#EXTENSION_FACE_RETOUCH:kotlin.Int` - the strength value will control the amount of cosmetic enhancement and skin smoothing.

The control will be supported if the capture request key is part of the list generated by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics#getAvailableCaptureRequestKeys(kotlin.Int)`. The control is only defined and available to clients sending capture requests via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession`. If the client doesn't specify the extension strength value, then a default value will be set by the extension. Clients can retrieve the default value by checking the corresponding capture result.

**Range of valid values:** 
0 - 100

**Optional** - The value for this key may be `null` on some devices.

### FLASH_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLASH_MODE: CaptureRequest.Key<Int!>
```

The desired mode for for the camera device's flash control.

This control is only effective when flash unit is available (`` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_INFO_AVAILABLE:android.hardware.camera2.CameraCharacteristics.Key` == true ``).

When this control is used, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key` must be set to ON or OFF. Otherwise, the camera device auto-exposure related flash control (ON_AUTO_FLASH, ON_ALWAYS_FLASH, or ON_AUTO_FLASH_REDEYE) will override this control.

When set to OFF, the camera device will not fire flash for this capture.

When set to SINGLE, the camera device will fire flash regardless of the camera device's auto-exposure routine's result. When used in still capture case, this control should be used along with auto-exposure (AE) precapture metering sequence (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key`), otherwise, the image may be incorrectly exposed.

When set to TORCH, the flash will be on continuously. This mode can be used for use cases such as preview, auto-focus assist, still capture, or video recording.

The flash status will be reported by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#FLASH_STATE:android.hardware.camera2.CaptureResult.Key` in the capture result metadata.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_MODE_SINGLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_MODE_TORCH:kotlin.Int`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_INFO_AVAILABLE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#FLASH_STATE:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_MODE_SINGLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_MODE_TORCH:kotlin.Int`

### FLASH_STRENGTH_LEVEL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLASH_STRENGTH_LEVEL: CaptureRequest.Key<Int!>
```

Flash strength level to be used when manual flash control is active.

Flash strength level to use in capture mode i.e. when the applications control flash with either `SINGLE` or `TORCH` mode.

Use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_SINGLE_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_TORCH_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` to check whether the device supports flash strength control or not. If the values of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_SINGLE_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_TORCH_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` are greater than 1, then the device supports manual flash strength control.

If the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_MODE:android.hardware.camera2.CaptureRequest.Key` `==` `TORCH` the value must be \>= 1 and \<= `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_TORCH_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`. If the application doesn't set the key and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_TORCH_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` \> 1, then the flash will be fired at the default level set by HAL in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_TORCH_STRENGTH_DEFAULT_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`. If the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_MODE:android.hardware.camera2.CaptureRequest.Key` `==` `SINGLE`, then the value must be \>= 1 and \<= `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_SINGLE_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`. If the application does not set this key and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_SINGLE_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` \> 1, then the flash will be fired at the default level set by HAL in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_SINGLE_STRENGTH_DEFAULT_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`. If `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key` is set to any of `ON_AUTO_FLASH`, `ON_ALWAYS_FLASH`, `ON_AUTO_FLASH_REDEYE`, `ON_EXTERNAL_FLASH` values, then the strengthLevel will be ignored.

When AE mode is ON and flash mode is TORCH or SINGLE, the application should make sure the AE mode, flash mode, and flash strength level remain the same between precapture trigger request and final capture request. The flash strength level being set during precapture sequence is used by the camera device as a reference. The actual strength may be less, and the auto-exposure routine makes sure proper conversions of sensor exposure time and sensitivities between precapture and final capture for the specified strength level.

**Range of valid values:** 
``[1-`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_TORCH_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`]`` when the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_MODE:android.hardware.camera2.CaptureRequest.Key` is set to TORCH; ``[1-`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_SINGLE_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`]`` when the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_MODE:android.hardware.camera2.CaptureRequest.Key` is set to SINGLE

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_SINGLE_STRENGTH_DEFAULT_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_SINGLE_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_TORCH_STRENGTH_DEFAULT_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_TORCH_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`

### HOT_PIXEL_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HOT_PIXEL_MODE: CaptureRequest.Key<Int!>
```

Operational mode for hot pixel correction.

Hotpixel correction interpolates out, or otherwise removes, pixels that do not accurately measure the incoming light (i.e. pixels that are stuck at an arbitrary value or are oversensitive).

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#HOT_PIXEL_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#HOT_PIXEL_MODE_FAST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#HOT_PIXEL_MODE_HIGH_QUALITY:kotlin.Int`

**Available values for this device:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#HOT_PIXEL_AVAILABLE_HOT_PIXEL_MODES:android.hardware.camera2.CameraCharacteristics.Key`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#HOT_PIXEL_AVAILABLE_HOT_PIXEL_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#HOT_PIXEL_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#HOT_PIXEL_MODE_FAST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#HOT_PIXEL_MODE_HIGH_QUALITY:kotlin.Int`

### JPEG_GPS_LOCATION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JPEG_GPS_LOCATION: CaptureRequest.Key<Location!>
```

A location object to use when generating image GPS metadata.

Setting a location object in a request will include the GPS coordinates of the location into any JPEG images captured based on the request. These coordinates can then be viewed by anyone who receives the JPEG image.

This tag is also used for HEIC image capture.

This key is available on all devices.

### JPEG_ORIENTATION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JPEG_ORIENTATION: CaptureRequest.Key<Int!>
```

The orientation for a JPEG image.

The clockwise rotation angle in degrees, relative to the orientation to the camera, that the JPEG picture needs to be rotated by, to be viewed upright.

Camera devices may either encode this value into the JPEG EXIF header, or rotate the image data to match this orientation. When the image data is rotated, the thumbnail data will also be rotated. Additionally, in the case where the image data is rotated, `https://developer.android.com/reference/kotlin/android/media/Image.html#getWidth()` and `https://developer.android.com/reference/kotlin/android/media/Image.html#getHeight()` will not be updated to reflect the height and width of the rotated image.

Note that this orientation is relative to the orientation of the camera sensor, given by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_ORIENTATION:android.hardware.camera2.CameraCharacteristics.Key`.

To translate from the device orientation given by the Android sensor APIs for camera sensors which are not EXTERNAL, the following sample code may be used:

```kotlin
<code>private int getJpegOrientation(CameraCharacteristics c, int deviceOrientation) {
      if (deviceOrientation == android.view.OrientationEventListener.ORIENTATION_UNKNOWN) return 0;
      int sensorOrientation = c.get(CameraCharacteristics.SENSOR_ORIENTATION);
 
      // Round device orientation to a multiple of 90
      deviceOrientation = (deviceOrientation + 45) / 90 * 90;
 
      // Reverse device orientation for front-facing cameras
      boolean facingFront = c.get(CameraCharacteristics.LENS_FACING) == CameraCharacteristics.LENS_FACING_FRONT;
      if (facingFront) deviceOrientation = -deviceOrientation;
 
      // Calculate desired JPEG orientation relative to camera orientation to make
      // the image upright relative to the device orientation
      int jpegOrientation = (sensorOrientation + deviceOrientation + 360) % 360;
 
      return jpegOrientation;
  }
  </code>
```

For EXTERNAL cameras the sensor orientation will always be set to 0 and the facing will also be set to EXTERNAL. The above code is not relevant in such case.

This tag is also used to describe the orientation of the HEIC image capture, in which case the rotation is reflected by `https://developer.android.com/reference/kotlin/android/media/ExifInterface.html#TAG_ORIENTATION:kotlin.String`, and not by rotating the image data itself.

**Units**: Degrees in multiples of 90

**Range of valid values:** 
0, 90, 180, 270

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_ORIENTATION:android.hardware.camera2.CameraCharacteristics.Key`

### JPEG_QUALITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JPEG_QUALITY: CaptureRequest.Key<Byte!>
```

Compression quality of the final JPEG image.

85-95 is typical usage range. This tag is also used to describe the quality of the HEIC image capture.

**Range of valid values:** 
1-100; larger is higher quality

This key is available on all devices.

### JPEG_THUMBNAIL_QUALITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JPEG_THUMBNAIL_QUALITY: CaptureRequest.Key<Byte!>
```

Compression quality of JPEG thumbnail.

This tag is also used to describe the quality of the HEIC image capture.

**Range of valid values:** 
1-100; larger is higher quality

This key is available on all devices.

### JPEG_THUMBNAIL_SIZE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JPEG_THUMBNAIL_SIZE: CaptureRequest.Key<Size!>
```

Resolution of embedded JPEG thumbnail.

When set to (0, 0) value, the JPEG EXIF will not contain thumbnail, but the captured JPEG will still be a valid image.

For best results, when issuing a request for a JPEG image, the thumbnail size selected should have the same aspect ratio as the main JPEG output.

If the thumbnail image aspect ratio differs from the JPEG primary image aspect ratio, the camera device creates the thumbnail by cropping it from the primary image. For example, if the primary image has 4:3 aspect ratio, the thumbnail image has 16:9 aspect ratio, the primary image will be cropped vertically (letterbox) to generate the thumbnail image. The thumbnail image will always have a smaller Field Of View (FOV) than the primary image when aspect ratios differ.

When an `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#JPEG_ORIENTATION:android.hardware.camera2.CaptureRequest.Key` of non-zero degree is requested, the camera device will handle thumbnail rotation in one of the following ways:

- Set the `https://developer.android.com/reference/kotlin/android/media/ExifInterface.html#TAG_ORIENTATION:kotlin.String` and keep jpeg and thumbnail image data unrotated.
- Rotate the jpeg and thumbnail image data and not set `https://developer.android.com/reference/kotlin/android/media/ExifInterface.html#TAG_ORIENTATION:kotlin.String`. In this case, LIMITED or FULL hardware level devices will report rotated thumbnail size in capture result, so the width and height will be interchanged if 90 or 270 degree orientation is requested. LEGACY device will always report unrotated thumbnail size.

The tag is also used as thumbnail size for HEIC image format capture, in which case the the thumbnail rotation is reflected by `https://developer.android.com/reference/kotlin/android/media/ExifInterface.html#TAG_ORIENTATION:kotlin.String`, and not by rotating the thumbnail data itself.

**Range of valid values:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#JPEG_AVAILABLE_THUMBNAIL_SIZES:android.hardware.camera2.CameraCharacteristics.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#JPEG_AVAILABLE_THUMBNAIL_SIZES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#JPEG_ORIENTATION:android.hardware.camera2.CaptureRequest.Key`

### LENS_APERTURE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_APERTURE: CaptureRequest.Key<Float!>
```

The desired lens aperture size, as a ratio of lens focal length to the effective aperture diameter.

Setting this value is only supported on the camera devices that have a variable aperture lens.

When this is supported and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key` is OFF, this can be set along with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` to achieve manual exposure control.

The requested aperture value may take several frames to reach the requested value; the camera device will report the current (intermediate) aperture size in capture result metadata while the aperture is changing. While the aperture is still changing, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#LENS_STATE:android.hardware.camera2.CaptureResult.Key` will be set to MOVING.

When this is supported and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key` is one of the ON modes, this will be overridden by the camera device auto-exposure algorithm, the overridden values are then provided back to the user in the corresponding result.

**Units**: The f-number (f/N)

**Range of valid values:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_AVAILABLE_APERTURES:android.hardware.camera2.CameraCharacteristics.Key`

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_AVAILABLE_APERTURES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#LENS_STATE:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`

### LENS_FILTER_DENSITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_FILTER_DENSITY: CaptureRequest.Key<Float!>
```

The desired setting for the lens neutral density filter(s).

This control will not be supported on most camera devices.

Lens filters are typically used to lower the amount of light the sensor is exposed to (measured in steps of EV). As used here, an EV step is the standard logarithmic representation, which are non-negative, and inversely proportional to the amount of light hitting the sensor. For example, setting this to 0 would result in no reduction of the incoming light, and setting this to 2 would mean that the filter is set to reduce incoming light by two stops (allowing 1/4 of the prior amount of light to the sensor).

It may take several frames before the lens filter density changes to the requested value. While the filter density is still changing, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#LENS_STATE:android.hardware.camera2.CaptureResult.Key` will be set to MOVING.

**Units**: Exposure Value (EV)

**Range of valid values:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_AVAILABLE_FILTER_DENSITIES:android.hardware.camera2.CameraCharacteristics.Key`

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_AVAILABLE_FILTER_DENSITIES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#LENS_STATE:android.hardware.camera2.CaptureResult.Key`

### LENS_FOCAL_LENGTH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_FOCAL_LENGTH: CaptureRequest.Key<Float!>
```

The desired lens focal length

Focal length is the distance from the optical center of the lens to the focal point for a thin lens approximation of the camera optical system. The definition assumes the lens is focused at infinity.

The horizontal field-of-view of the processed full frame camera outputs can be derived as:

```kotlin
<code>fov = 2 * atan2(sw / 2, fl)
  </code>
```

where:

- `sw` is the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PHYSICAL_SIZE:android.hardware.camera2.CameraCharacteristics.Key` width,
- `fl` is `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key`.

Using this control to switch between lenses is not supported on most devices. Starting from API level 30, the application is strongly recommended to use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` for combined optical and digital zoom. To exclusively use a particular focal length lens in a logical multi-camera, applications can iterate over the physical cameras exposed by the logical multi-camera device via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getPhysicalCameraIds()` and select the one with the desired focal length.

**Units**: Millimeters

**Range of valid values:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_AVAILABLE_FOCAL_LENGTHS:android.hardware.camera2.CameraCharacteristics.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_AVAILABLE_FOCAL_LENGTHS:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PHYSICAL_SIZE:android.hardware.camera2.CameraCharacteristics.Key`

### LENS_FOCUS_DISTANCE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_FOCUS_DISTANCE: CaptureRequest.Key<Float!>
```

Desired distance to plane of sharpest focus, measured from frontmost surface of the lens.

This control can be used for setting manual focus, on devices that support the MANUAL_SENSOR capability and have a variable-focus lens (see `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key`).

A value of `0.0f` means infinity focus. The value set will be clamped to ``[0.0f, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key`]``.

Like `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key`, this setting won't be applied instantaneously, and it may take several frames before the lens can move to the requested focus distance. While the lens is still moving, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#LENS_STATE:android.hardware.camera2.CaptureResult.Key` will be set to MOVING.

LEGACY devices support at most setting this to `0.0f` for infinity focus.

**Units** : See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_FOCUS_DISTANCE_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key` for details

**Range of valid values:** 
\>= 0

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_FOCUS_DISTANCE_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#LENS_STATE:android.hardware.camera2.CaptureResult.Key`

### LENS_OPTICAL_STABILIZATION_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_OPTICAL_STABILIZATION_MODE: CaptureRequest.Key<Int!>
```

Sets whether the camera device uses optical image stabilization (OIS) when capturing images.

OIS is used to compensate for motion blur due to small movements of the camera during capture. Unlike digital image stabilization (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_VIDEO_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key`), OIS makes use of mechanical elements to stabilize the camera sensor, and thus allows for longer exposure times before camera shake becomes apparent.

Switching between different optical stabilization modes may take several frames to initialize, the camera device will report the current mode in capture result metadata. For example, When "ON" mode is requested, the optical stabilization modes in the first several capture results may still be "OFF", and it will become "ON" when the initialization is done.

If a camera device supports both OIS and digital image stabilization (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_VIDEO_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key`), turning both modes on may produce undesirable interaction, so it is recommended not to enable both at the same time.

If `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_VIDEO_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key` is set to "PREVIEW_STABILIZATION", `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_OPTICAL_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key` is overridden. The camera sub-system may choose to turn on hardware based image stabilization in addition to software based stabilization if it deems that appropriate. This key's value in the capture result will reflect which OIS mode was chosen.

Not all devices will support OIS; see `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_AVAILABLE_OPTICAL_STABILIZATION:android.hardware.camera2.CameraCharacteristics.Key` for available controls.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_OPTICAL_STABILIZATION_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_OPTICAL_STABILIZATION_MODE_ON:kotlin.Int`

**Available values for this device:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_AVAILABLE_OPTICAL_STABILIZATION:android.hardware.camera2.CameraCharacteristics.Key`

**Optional** - The value for this key may be `null` on some devices.

**Limited capability** - Present on all camera devices that report being at least `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_VIDEO_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_AVAILABLE_OPTICAL_STABILIZATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_OPTICAL_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_OPTICAL_STABILIZATION_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_OPTICAL_STABILIZATION_MODE_ON:kotlin.Int`

### LOGICAL_MULTI_CAMERA_ADDITIONAL_RESULTS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOGICAL_MULTI_CAMERA_ADDITIONAL_RESULTS: CaptureRequest.Key<Boolean!>
```

Controls whether the camera device could also return additional physical cameras' metadata in the results.

This control must only be turned on when device is using logical camera, which are devices that have `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_LOGICAL_MULTI_CAMERA:kotlin.Int` capability and the key is supported in the device's `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getAvailableCaptureRequestKeys()`. Once this key is set to ON, if the camera device has multiple physical cameras active, the TotalCaptureResult will contain additional physical camera metadata in the result. One of such scenario is at the time of lens switch during zoom, where in addition to the active physical camera, a secondary physical camera runs as a "follower" and produces an additional physical camera CaptureResult. The application can call `https://developer.android.com/reference/kotlin/android/hardware/camera2/TotalCaptureResult#getPhysicalCameraTotalResults()` to get the additional results.

**Optional** - The value for this key may be `null` on some devices.

### NOISE_REDUCTION_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NOISE_REDUCTION_MODE: CaptureRequest.Key<Int!>
```

Mode of operation for the noise reduction algorithm.

The noise reduction algorithm attempts to improve image quality by removing excessive noise added by the capture process, especially in dark conditions.

OFF means no noise reduction will be applied by the camera device, for both raw and YUV domain.

MINIMAL means that only sensor raw domain basic noise reduction is enabled ,to remove demosaicing or other processing artifacts. For YUV_REPROCESSING, MINIMAL is same as OFF. This mode is optional, may not be support by all devices. The application should check `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#NOISE_REDUCTION_AVAILABLE_NOISE_REDUCTION_MODES:android.hardware.camera2.CameraCharacteristics.Key` before using it.

FAST/HIGH_QUALITY both mean camera device determined noise filtering will be applied. HIGH_QUALITY mode indicates that the camera device will use the highest-quality noise filtering algorithms, even if it slows down capture rate. FAST means the camera device will not slow down capture rate when applying noise filtering. FAST may be the same as MINIMAL if MINIMAL is listed, or the same as OFF if any noise filtering will slow down capture rate. Every output stream will have a similar amount of enhancement applied.

ZERO_SHUTTER_LAG is meant to be used by applications that maintain a continuous circular buffer of high-resolution images during preview and reprocess image(s) from that buffer into a final capture when triggered by the user. In this mode, the camera device applies noise reduction to low-resolution streams (below maximum recording resolution) to maximize preview quality, but does not apply noise reduction to high-resolution streams, since those will be reprocessed later if necessary.

For YUV_REPROCESSING, these FAST/HIGH_QUALITY modes both mean that the camera device will apply FAST/HIGH_QUALITY YUV domain noise reduction, respectively. The camera device may adjust the noise reduction parameters for best image quality based on the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#REPROCESS_EFFECTIVE_EXPOSURE_FACTOR:android.hardware.camera2.CaptureRequest.Key` if it is set.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_FAST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_HIGH_QUALITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_MINIMAL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_ZERO_SHUTTER_LAG:kotlin.Int`

**Available values for this device:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#NOISE_REDUCTION_AVAILABLE_NOISE_REDUCTION_MODES:android.hardware.camera2.CameraCharacteristics.Key`

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#NOISE_REDUCTION_AVAILABLE_NOISE_REDUCTION_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#REPROCESS_EFFECTIVE_EXPOSURE_FACTOR:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_FAST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_HIGH_QUALITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_MINIMAL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_ZERO_SHUTTER_LAG:kotlin.Int`

### REPROCESS_EFFECTIVE_EXPOSURE_FACTOR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REPROCESS_EFFECTIVE_EXPOSURE_FACTOR: CaptureRequest.Key<Float!>
```

The amount of exposure time increase factor applied to the original output frame by the application processing before sending for reprocessing.

This is optional, and will be supported if the camera device supports YUV_REPROCESSING capability (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` contains YUV_REPROCESSING).

For some YUV reprocessing use cases, the application may choose to filter the original output frames to effectively reduce the noise to the same level as a frame that was captured with longer exposure time. To be more specific, assuming the original captured images were captured with a sensitivity of S and an exposure time of T, the model in the camera device is that the amount of noise in the image would be approximately what would be expected if the original capture parameters had been a sensitivity of S/effectiveExposureFactor and an exposure time of T\*effectiveExposureFactor, rather than S and T respectively. If the captured images were processed by the application before being sent for reprocessing, then the application may have used image processing algorithms and/or multi-frame image fusion to reduce the noise in the application-processed images (input images). By using the effectiveExposureFactor control, the application can communicate to the camera device the actual noise level improvement in the application-processed image. With this information, the camera device can select appropriate noise reduction and edge enhancement parameters to avoid excessive noise reduction (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#NOISE_REDUCTION_MODE:android.hardware.camera2.CaptureRequest.Key`) and insufficient edge enhancement (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#EDGE_MODE:android.hardware.camera2.CaptureRequest.Key`) being applied to the reprocessed frames.

For example, for multi-frame image fusion use case, the application may fuse multiple output frames together to a final frame for reprocessing. When N image are fused into 1 image for reprocessing, the exposure time increase factor could be up to square root of N (based on a simple photon shot noise model). The camera device will adjust the reprocessing noise reduction and edge enhancement parameters accordingly to produce the best quality images.

This is relative factor, 1.0 indicates the application hasn't processed the input buffer in a way that affects its effective exposure time.

This control is only effective for YUV reprocessing capture request. For noise reduction reprocessing, it is only effective when `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#NOISE_REDUCTION_MODE:android.hardware.camera2.CaptureRequest.Key` != OFF ``. Similarly, for edge enhancement reprocessing, it is only effective when `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#EDGE_MODE:android.hardware.camera2.CaptureRequest.Key` != OFF ``.

**Units**: Relative exposure time increase factor.

**Range of valid values:** 
\>= 1.0

**Optional** - The value for this key may be `null` on some devices.

**Limited capability** - Present on all camera devices that report being at least `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#EDGE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#NOISE_REDUCTION_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`

### SCALER_CROP_REGION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_CROP_REGION: CaptureRequest.Key<Rect!>
```

The desired region of the sensor to read out for this capture.

This control can be used to implement digital zoom.

For devices not supporting `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` control, the coordinate system always follows that of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`, with `(0, 0)` being the top-left pixel of the active array.

For devices supporting `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` control, the coordinate system depends on the mode being set. When the distortion correction mode is OFF, the coordinate system follows `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`, with `(0, 0)` being the top-left pixel of the pre-correction active array. When the distortion correction mode is not OFF, the coordinate system follows `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`, with `(0, 0)` being the top-left pixel of the active array.

Output streams use this rectangle to produce their output, cropping to a smaller region if necessary to maintain the stream's aspect ratio, then scaling the sensor input to match the output's configured resolution.

The crop region is usually applied after the RAW to other color space (e.g. YUV) conversion. As a result RAW streams are not croppable unless supported by the camera device. See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_STREAM_USE_CASES:android.hardware.camera2.CameraCharacteristics.Key`CROPPED_RAW for details.

For non-raw streams, any additional per-stream cropping will be done to maximize the final pixel area of the stream.

For example, if the crop region is set to a 4:3 aspect ratio, then 4:3 streams will use the exact crop region. 16:9 streams will further crop vertically (letterbox).

Conversely, if the crop region is set to a 16:9, then 4:3 outputs will crop horizontally (pillarbox), and 16:9 streams will match exactly. These additional crops will be centered within the crop region.

To illustrate, here are several scenarios of different crop regions and output streams, for a hypothetical camera device with an active array of size `(2000,1500)`. Note that several of these examples use non-centered crop regions for ease of illustration; such regions are only supported on devices with FREEFORM capability (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_CROPPING_TYPE:android.hardware.camera2.CameraCharacteristics.Key` `== FREEFORM`), but this does not affect the way the crop rules work otherwise.

- Camera Configuration:
 - Active array size: `2000x1500` (3 MP, 4:3 aspect ratio)
 - Output stream #1: `640x480` (VGA, 4:3 aspect ratio)
 - Output stream #2: `1280x720` (720p, 16:9 aspect ratio)
- Case #1: 4:3 crop region with 2x digital zoom
 - Crop region: `Rect(500, 375, 1500, 1125) // (left, top, right, bottom)`
 - 
 - `640x480` stream source area: `(500, 375, 1500, 1125)` (equal to crop region)
 - `1280x720` stream source area: `(500, 469, 1500, 1031)` (letterboxed)
- Case #2: 16:9 crop region with \~1.5x digital zoom.
 - Crop region: `Rect(500, 375, 1833, 1125)`
 - 
 - `640x480` stream source area: `(666, 375, 1666, 1125)` (pillarboxed)
 - `1280x720` stream source area: `(500, 375, 1833, 1125)` (equal to crop region)
- Case #3: 1:1 crop region with \~2.6x digital zoom.
 - Crop region: `Rect(500, 375, 1250, 1125)`
 - 
 - `640x480` stream source area: `(500, 469, 1250, 1031)` (letterboxed)
 - `1280x720` stream source area: `(500, 543, 1250, 957)` (letterboxed)
- Case #4: Replace `640x480` stream with `1024x1024` stream, with 4:3 crop region:
 - Crop region: `Rect(500, 375, 1500, 1125)`
 - 
 - `1024x1024` stream source area: `(625, 375, 1375, 1125)` (pillarboxed)
 - `1280x720` stream source area: `(500, 469, 1500, 1031)` (letterboxed)
 - Note that in this case, neither of the two outputs is a subset of the other, with each containing image data the other doesn't have.

If the coordinate system is `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`, the width and height of the crop region cannot be set to be smaller than ``floor( activeArraySize.width / `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_MAX_DIGITAL_ZOOM:android.hardware.camera2.CameraCharacteristics.Key` )`` and ``floor( activeArraySize.height / `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_MAX_DIGITAL_ZOOM:android.hardware.camera2.CameraCharacteristics.Key` )``, respectively.

If the coordinate system is `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`, the width and height of the crop region cannot be set to be smaller than ``floor( preCorrectionActiveArraySize.width / `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_MAX_DIGITAL_ZOOM:android.hardware.camera2.CameraCharacteristics.Key` )`` and ``floor( preCorrectionActiveArraySize.height / `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_MAX_DIGITAL_ZOOM:android.hardware.camera2.CameraCharacteristics.Key` )``, respectively.

The camera device may adjust the crop region to account for rounding and other hardware requirements; the final crop region used will be included in the output capture result.

The camera sensor output aspect ratio depends on factors such as output stream combination and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key`, and shouldn't be adjusted by using this control. And the camera device will treat different camera sensor output sizes (potentially with in-sensor crop) as the same crop of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`. As a result, the application shouldn't assume the maximum crop region always maps to the same aspect ratio or field of view for the sensor output.

Starting from API level 30, it's strongly recommended to use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` to take advantage of better support for zoom with logical multi-camera. The benefits include better precision with optical-digital zoom combination, and ability to do zoom-out from 1.0x. When using `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` for zoom, the crop region in the capture request should be left as the default activeArray size. The coordinate system is post-zoom, meaning that the activeArraySize or preCorrectionActiveArraySize covers the camera device's field of view "after" zoom. See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` for details.

For camera devices with the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR:kotlin.Int` capability or devices where `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getAvailableCaptureRequestKeys()` lists `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key` / `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key` must be used as the coordinate system for requests where `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` is set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`.

**Units** : Pixel coordinates relative to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` depending on distortion correction capability and mode

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_MAX_DIGITAL_ZOOM:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_STREAM_USE_CASES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_CROPPING_TYPE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`

### SCALER_ROTATE_AND_CROP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_ROTATE_AND_CROP: CaptureRequest.Key<Int!>
```

Whether a rotation-and-crop operation is applied to processed outputs from the camera.

This control is primarily intended to help camera applications with no support for multi-window modes to work correctly on devices where multi-window scenarios are unavoidable, such as foldables or other devices with variable display geometry or more free-form window placement (such as laptops, which often place portrait-orientation apps in landscape with pillarboxing).

If supported, the default value is `ROTATE_AND_CROP_AUTO`, which allows the camera API to enable backwards-compatibility support for applications that do not support resizing / multi-window modes, when the device is in fact in a multi-window mode (such as inset portrait on laptops, or on a foldable device in some fold states). In addition, `ROTATE_AND_CROP_NONE` and `ROTATE_AND_CROP_90` will always be available if this control is supported by the device. If not supported, devices API level 30 or higher will always list only `ROTATE_AND_CROP_NONE`.

When `CROP_AUTO` is in use, and the camera API activates backward-compatibility mode, several metadata fields will also be parsed differently to ensure that coordinates are correctly handled for features like drawing face detection boxes or passing in tap-to-focus coordinates. The camera API will convert positions in the active array coordinate system to/from the cropped-and-rotated coordinate system to make the operation transparent for applications. The following controls are affected:

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_FACES:android.hardware.camera2.CaptureResult.Key`

Capture results will contain the actual value selected by the API; `ROTATE_AND_CROP_AUTO` will never be seen in a capture result.

Applications can also select their preferred cropping mode, either to opt out of the backwards-compatibility treatment, or to use the cropping feature themselves as needed. In this case, no coordinate translation will be done automatically, and all controls will continue to use the normal active array coordinates.

Cropping and rotating is done after the application of digital zoom (via either `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`), but before each individual output is further cropped and scaled. It only affects processed outputs such as YUV, PRIVATE, and JPEG. It has no effect on RAW outputs.

When `CROP_90` or `CROP_270` are selected, there is a significant loss to the field of view. For example, with a 4:3 aspect ratio output of 1600x1200, `CROP_90` will still produce 1600x1200 output, but these buffers are cropped from a vertical 3:4 slice at the center of the 4:3 area, then rotated to be 4:3, and then upscaled to 1600x1200. Only 56.25% of the original FOV is still visible. In general, for an aspect ratio of `w:h`, the crop and rotate operation leaves `(h/w)^2` of the field of view visible. For 16:9, this is \~31.6%.

As a visual example, the figure below shows the effect of `ROTATE_AND_CROP_90` on the outputs for the following parameters:

- Sensor active array: `2000x1500`
- Crop region: top-left: `(500, 375)`, size: `(1000, 750)` (4:3 aspect ratio)
- Output streams: YUV `640x480` and YUV `1280x720`
- `ROTATE_AND_CROP_90`

<br />

With these settings, the regions of the active array covered by the output streams are:

- 640x480 stream crop: top-left: `(219, 375)`, size: `(562, 750)`
- 1280x720 stream crop: top-left: `(289, 375)`, size: `(422, 750)`

Since the buffers are rotated, the buffers as seen by the application are:

- 640x480 stream: top-left: `(781, 375)` on active array, size: `(640, 480)`, downscaled 1.17x from sensor pixels
- 1280x720 stream: top-left: `(711, 375)` on active array, size: `(1280, 720)`, upscaled 1.71x from sensor pixels

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_NONE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_90:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_180:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_270:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_AUTO:kotlin.Int`

**Available values for this device:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_ROTATE_AND_CROP_MODES:android.hardware.camera2.CameraCharacteristics.Key`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_ROTATE_AND_CROP_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_FACES:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_NONE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_90:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_180:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_270:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_AUTO:kotlin.Int`

### SENSOR_EXPOSURE_TIME

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_EXPOSURE_TIME: CaptureRequest.Key<Long!>
```

Duration each pixel is exposed to light.

If the sensor can't expose this exact duration, it will shorten the duration exposed to the nearest possible value (rather than expose longer). The final exposure time used will be available in the output capture result.

This control is only effective if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` is set to OFF; otherwise the auto-exposure algorithm will override this value. However, in the case that `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRIORITY_MODE:android.hardware.camera2.CaptureRequest.Key` is set to SENSOR_EXPOSURE_TIME_PRIORITY, this control will be effective and not controlled by the auto-exposure algorithm.

**Units**: Nanoseconds

**Range of valid values:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_EXPOSURE_TIME_RANGE:android.hardware.camera2.CameraCharacteristics.Key`

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRIORITY_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_EXPOSURE_TIME_RANGE:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_FRAME_DURATION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_FRAME_DURATION: CaptureRequest.Key<Long!>
```

Duration from start of frame readout to start of next frame readout.

The maximum frame rate that can be supported by a camera subsystem is a function of many factors:

- Requested resolutions of output image streams
- Availability of binning / skipping modes on the imager
- The bandwidth of the imager interface
- The bandwidth of the various ISP processing blocks

Since these factors can vary greatly between different ISPs and sensors, the camera abstraction tries to represent the bandwidth restrictions with as simple a model as possible.

The model presented has the following characteristics:

- The image sensor is always configured to output the smallest resolution possible given the application's requested output stream sizes. The smallest resolution is defined as being at least as large as the largest requested output stream size; the camera pipeline must never digitally upsample sensor data when the crop region covers the whole sensor. In general, this means that if only small output stream resolutions are configured, the sensor can provide a higher frame rate.
- Since any request may use any or all the currently configured output streams, the sensor and ISP must be configured to support scaling a single capture to all the streams at the same time. This means the camera pipeline must be ready to produce the largest requested output size without any delay. Therefore, the overall frame rate of a given configured stream set is governed only by the largest requested stream resolution.
- Using more than one output stream in a request does not affect the frame duration.
- Certain format-streams may need to do additional background processing before data is consumed/produced by that stream. These processors can run concurrently to the rest of the camera pipeline, but cannot process more than 1 capture at a time.

The necessary information for the application, given the model above, is provided via android.hardware.camera2.params.StreamConfigurationMap#getOutputMinFrameDuration. These are used to determine the maximum frame rate / minimum frame duration that is possible for a given stream configuration.

Specifically, the application can use the following rules to determine the minimum frame duration it can request from the camera device:

1. Let the set of currently configured input/output streams be called `S`.
2. Find the minimum frame durations for each stream in `S`, by looking it up in android.hardware.camera2.params.StreamConfigurationMap#getOutputMinFrameDuration (with its respective size/format). Let this set of frame durations be called `F`.
3. For any given request `R`, the minimum frame duration allowed for `R` is the maximum out of all values in `F`. Let the streams used in `R` be called `S_r`.

If none of the streams in `S_r` have a stall time (listed in android.hardware.camera2.params.StreamConfigurationMap#getOutputStallDuration using its respective size/format), then the frame duration in `F` determines the steady state frame rate that the application will get if it uses `R` as a repeating request. Let this special kind of request be called `Rsimple`.

A repeating request `Rsimple` can be *occasionally* interleaved by a single capture of a new request `Rstall` (which has at least one in-use stream with a non-0 stall time) and if `Rstall` has the same minimum frame duration this will not cause a frame rate loss if all buffers from the previous `Rstall` have already been delivered.

For more details about stalling, see android.hardware.camera2.params.StreamConfigurationMap#getOutputStallDuration.

This control is only effective if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` is set to OFF; otherwise the auto-exposure algorithm will override this value.

*Note:* Prior to Android 13, this field was described as measuring the duration from start of frame exposure to start of next frame exposure, which doesn't reflect the definition from sensor manufacturer. A mobile sensor defines the frame duration as intervals between sensor readouts.

**Units**: Nanoseconds

**Range of valid values:** 
See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_MAX_FRAME_DURATION:android.hardware.camera2.CameraCharacteristics.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap`. The duration is capped to `max(duration, exposureTime + overhead)`.

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_MAX_FRAME_DURATION:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_PIXEL_MODE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_PIXEL_MODE: CaptureRequest.Key<Int!>
```

Switches sensor pixel mode between maximum resolution mode and default mode.

This key controls whether the camera sensor operates in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int` mode or not. By default, all camera devices operate in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_DEFAULT:kotlin.Int` mode. When operating in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_DEFAULT:kotlin.Int` mode, sensors would typically perform pixel binning in order to improve low light performance, noise reduction etc. However, in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int` mode, sensors typically operate in unbinned mode allowing for a larger image size. The stream configurations supported in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int` mode are also different from those of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_DEFAULT:kotlin.Int` mode. They can be queried through `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#get(android.hardware.camera2.CameraCharacteristics.Key)` with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key`. Unless reported by both `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap`s, the outputs from `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key` `` and `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key` `` must not be mixed in the same CaptureRequest. In other words, these outputs are exclusive to each other. This key does not need to be set for reprocess requests. This key will be be present on devices supporting the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR:kotlin.Int` capability. It may also be present on devices which do not support the aforementioned capability. In that case:

- The mandatory stream combinations listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_MANDATORY_MAXIMUM_RESOLUTION_STREAM_COMBINATIONS:android.hardware.camera2.CameraCharacteristics.Key` would not apply.

- The bayer pattern of `RAW` streams when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int` is selected will be the one listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_BINNING_FACTOR:android.hardware.camera2.CameraCharacteristics.Key`.

- The following keys will always be present:

 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PIXEL_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key`

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_DEFAULT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_MANDATORY_MAXIMUM_RESOLUTION_STREAM_COMBINATIONS:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_BINNING_FACTOR:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PIXEL_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_DEFAULT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`

### SENSOR_SENSITIVITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_SENSITIVITY: CaptureRequest.Key<Int!>
```

The amount of gain applied to sensor data before processing.

The sensitivity is the standard ISO sensitivity value, as defined in ISO 12232:2006.

The sensitivity must be within `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_SENSITIVITY_RANGE:android.hardware.camera2.CameraCharacteristics.Key`, and if if it less than `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_MAX_ANALOG_SENSITIVITY:android.hardware.camera2.CameraCharacteristics.Key`, the camera device is guaranteed to use only analog amplification for applying the gain.

If the camera device cannot apply the exact sensitivity requested, it will reduce the gain to the nearest supported value. The final sensitivity used will be available in the output capture result.

This control is only effective if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` is set to OFF; otherwise the auto-exposure algorithm will override this value. However, in the case that `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRIORITY_MODE:android.hardware.camera2.CaptureRequest.Key` is set to SENSOR_SENSITIVITY_PRIORITY, this control will be effective and not controlled by the auto-exposure algorithm.

Note that for devices supporting postRawSensitivityBoost, the total sensitivity applied to the final processed image is the combination of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_POST_RAW_SENSITIVITY_BOOST:android.hardware.camera2.CaptureRequest.Key`. In case the application uses the sensor sensitivity from last capture result of an auto request for a manual request, in order to achieve the same brightness in the output image, the application should also set postRawSensitivityBoost.

**Units**: ISO arithmetic units

**Range of valid values:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_SENSITIVITY_RANGE:android.hardware.camera2.CameraCharacteristics.Key`

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRIORITY_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_POST_RAW_SENSITIVITY_BOOST:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_SENSITIVITY_RANGE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_MAX_ANALOG_SENSITIVITY:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`

### SENSOR_TEST_PATTERN_DATA

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_TEST_PATTERN_DATA: CaptureRequest.Key<IntArray!>
```

A pixel `[R, G_even, G_odd, B]` that supplies the test pattern when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_TEST_PATTERN_MODE:android.hardware.camera2.CaptureRequest.Key` is SOLID_COLOR.

Each color channel is treated as an unsigned 32-bit integer. The camera device then uses the most significant X bits that correspond to how many bits are in its Bayer raw sensor output.

For example, a sensor with RAW10 Bayer output would use the 10 most significant bits from each color channel.

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_TEST_PATTERN_MODE:android.hardware.camera2.CaptureRequest.Key`

### SENSOR_TEST_PATTERN_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_TEST_PATTERN_MODE: CaptureRequest.Key<Int!>
```

When enabled, the sensor sends a test pattern instead of doing a real exposure from the camera.

When a test pattern is enabled, all manual sensor controls specified by android.sensor.\* will be ignored. All other controls should work as normal.

For example, if manual flash is enabled, flash firing should still occur (and that the test pattern remain unmodified, since the flash would not actually affect it).

Defaults to OFF.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_SOLID_COLOR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_COLOR_BARS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_COLOR_BARS_FADE_TO_GRAY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_PN9:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_CUSTOM1:kotlin.Int`

**Available values for this device:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_AVAILABLE_TEST_PATTERN_MODES:android.hardware.camera2.CameraCharacteristics.Key`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_AVAILABLE_TEST_PATTERN_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_SOLID_COLOR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_COLOR_BARS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_COLOR_BARS_FADE_TO_GRAY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_PN9:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_CUSTOM1:kotlin.Int`

### SHADING_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SHADING_MODE: CaptureRequest.Key<Int!>
```

Quality of lens shading correction applied to the image data.

When set to OFF mode, no lens shading correction will be applied by the camera device, and an identity lens shading map data will be provided if `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_LENS_SHADING_MAP_MODE:android.hardware.camera2.CaptureRequest.Key` == ON ``. For example, for lens shading map with size of `[ 4, 3 ]`, the output `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_LENS_SHADING_CORRECTION_MAP:android.hardware.camera2.CaptureResult.Key` for this case will be an identity map shown below:

```kotlin
<code>[ 1.0, 1.0, 1.0, 1.0,  1.0, 1.0, 1.0, 1.0,
   1.0, 1.0, 1.0, 1.0,  1.0, 1.0, 1.0, 1.0,
   1.0, 1.0, 1.0, 1.0,  1.0, 1.0, 1.0, 1.0,
   1.0, 1.0, 1.0, 1.0,  1.0, 1.0, 1.0, 1.0,
   1.0, 1.0, 1.0, 1.0,  1.0, 1.0, 1.0, 1.0,
   1.0, 1.0, 1.0, 1.0,  1.0, 1.0, 1.0, 1.0 ]
  </code>
```

When set to other modes, lens shading correction will be applied by the camera device. Applications can request lens shading map data by setting `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_LENS_SHADING_MAP_MODE:android.hardware.camera2.CaptureRequest.Key` to ON, and then the camera device will provide lens shading map data in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_LENS_SHADING_CORRECTION_MAP:android.hardware.camera2.CaptureResult.Key`; the returned shading map data will be the one applied by the camera device for this capture request.

The shading map data may depend on the auto-exposure (AE) and AWB statistics, therefore the reliability of the map data may be affected by the AE and AWB algorithms. When AE and AWB are in AUTO modes(`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key` `!=` OFF and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key` `!=` OFF), to get best results, it is recommended that the applications wait for the AE and AWB to be converged before using the returned shading map data.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SHADING_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SHADING_MODE_FAST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SHADING_MODE_HIGH_QUALITY:kotlin.Int`

**Available values for this device:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SHADING_AVAILABLE_MODES:android.hardware.camera2.CameraCharacteristics.Key`

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SHADING_AVAILABLE_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_LENS_SHADING_CORRECTION_MAP:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_LENS_SHADING_MAP_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SHADING_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SHADING_MODE_FAST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SHADING_MODE_HIGH_QUALITY:kotlin.Int`

### STATISTICS_FACE_DETECT_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATISTICS_FACE_DETECT_MODE: CaptureRequest.Key<Int!>
```

Operating mode for the face detector unit.

Whether face detection is enabled, and whether it should output just the basic fields or the full set of fields.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_FACE_DETECT_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_FACE_DETECT_MODE_SIMPLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_FACE_DETECT_MODE_FULL:kotlin.Int`

**Available values for this device:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#STATISTICS_INFO_AVAILABLE_FACE_DETECT_MODES:android.hardware.camera2.CameraCharacteristics.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#STATISTICS_INFO_AVAILABLE_FACE_DETECT_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_FACE_DETECT_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_FACE_DETECT_MODE_SIMPLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_FACE_DETECT_MODE_FULL:kotlin.Int`

### STATISTICS_HOT_PIXEL_MAP_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATISTICS_HOT_PIXEL_MAP_MODE: CaptureRequest.Key<Boolean!>
```

Operating mode for hot pixel map generation.

If set to `true`, a hot pixel map is returned in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_HOT_PIXEL_MAP:android.hardware.camera2.CaptureResult.Key`. If set to `false`, no hot pixel map will be returned.

**Range of valid values:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#STATISTICS_INFO_AVAILABLE_HOT_PIXEL_MAP_MODES:android.hardware.camera2.CameraCharacteristics.Key`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_HOT_PIXEL_MAP:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#STATISTICS_INFO_AVAILABLE_HOT_PIXEL_MAP_MODES:android.hardware.camera2.CameraCharacteristics.Key`

### STATISTICS_LENS_SHADING_MAP_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATISTICS_LENS_SHADING_MAP_MODE: CaptureRequest.Key<Int!>
```

Whether the camera device will output the lens shading map in output result metadata.

When set to ON, android.statistics.lensShadingMap will be provided in the output result metadata.

ON is always supported on devices with the RAW capability.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_LENS_SHADING_MAP_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_LENS_SHADING_MAP_MODE_ON:kotlin.Int`

**Available values for this device:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#STATISTICS_INFO_AVAILABLE_LENS_SHADING_MAP_MODES:android.hardware.camera2.CameraCharacteristics.Key`

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#STATISTICS_INFO_AVAILABLE_LENS_SHADING_MAP_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_LENS_SHADING_MAP_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_LENS_SHADING_MAP_MODE_ON:kotlin.Int`

### STATISTICS_OIS_DATA_MODE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATISTICS_OIS_DATA_MODE: CaptureRequest.Key<Int!>
```

A control for selecting whether optical stabilization (OIS) position information is included in output result metadata.

Since optical image stabilization generally involves motion much faster than the duration of individual image exposure, multiple OIS samples can be included for a single capture result. For example, if the OIS reporting operates at 200 Hz, a typical camera operating at 30fps may have 6-7 OIS samples per capture result. This information can be combined with the rolling shutter skew to account for lens motion during image exposure in post-processing algorithms.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_OIS_DATA_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_OIS_DATA_MODE_ON:kotlin.Int`

**Available values for this device:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#STATISTICS_INFO_AVAILABLE_OIS_DATA_MODES:android.hardware.camera2.CameraCharacteristics.Key`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#STATISTICS_INFO_AVAILABLE_OIS_DATA_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_OIS_DATA_MODE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_OIS_DATA_MODE_ON:kotlin.Int`

### TONEMAP_CURVE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TONEMAP_CURVE: CaptureRequest.Key<TonemapCurve!>
```

Tonemapping / contrast / gamma curve to use when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key` is CONTRAST_CURVE.

The tonemapCurve consist of three curves for each of red, green, and blue channels respectively. The following example uses the red channel as an example. The same logic applies to green and blue channel. Each channel's curve is defined by an array of control points:

```kotlin
<code>curveRed =
    [ P0(in, out), P1(in, out), P2(in, out), P3(in, out), ..., PN(in, out) ]
  2 &lt;= N &lt;= <code><a docref="android.hardware.camera2.CameraCharacteristics$TONEMAP_MAX_CURVE_POINTS">android.tonemap.maxCurvePoints</a></code></code>
```

These are sorted in order of increasing `Pin`; it is always guaranteed that input values 0.0 and 1.0 are included in the list to define a complete mapping. For input values between control points, the camera device must linearly interpolate between the control points.

Each curve can have an independent number of points, and the number of points can be less than max (that is, the request doesn't have to always provide a curve with number of points equivalent to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#TONEMAP_MAX_CURVE_POINTS:android.hardware.camera2.CameraCharacteristics.Key`).

For devices with MONOCHROME capability, all three channels must have the same set of control points.

A few examples, and their corresponding graphical mappings; these only specify the red channel and the precision is limited to 4 digits, for conciseness.

Linear mapping:

```kotlin
<code>curveRed = [ (0, 0), (1.0, 1.0) ]
  </code>
```

<br />

Invert mapping:

```kotlin
<code>curveRed = [ (0, 1.0), (1.0, 0) ]
  </code>
```

<br />

Gamma 1/2.2 mapping, with 16 control points:

```kotlin
<code>curveRed = [
    (0.0000, 0.0000), (0.0667, 0.2920), (0.1333, 0.4002), (0.2000, 0.4812),
    (0.2667, 0.5484), (0.3333, 0.6069), (0.4000, 0.6594), (0.4667, 0.7072),
    (0.5333, 0.7515), (0.6000, 0.7928), (0.6667, 0.8317), (0.7333, 0.8685),
    (0.8000, 0.9035), (0.8667, 0.9370), (0.9333, 0.9691), (1.0000, 1.0000) ]
  </code>
```

<br />

Standard sRGB gamma mapping, per IEC 61966-2-1:1999, with 16 control points:

```kotlin
<code>curveRed = [
    (0.0000, 0.0000), (0.0667, 0.2864), (0.1333, 0.4007), (0.2000, 0.4845),
    (0.2667, 0.5532), (0.3333, 0.6125), (0.4000, 0.6652), (0.4667, 0.7130),
    (0.5333, 0.7569), (0.6000, 0.7977), (0.6667, 0.8360), (0.7333, 0.8721),
    (0.8000, 0.9063), (0.8667, 0.9389), (0.9333, 0.9701), (1.0000, 1.0000) ]
  </code>
```

<br />

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#TONEMAP_MAX_CURVE_POINTS:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key`

### TONEMAP_GAMMA

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TONEMAP_GAMMA: CaptureRequest.Key<Float!>
```

Tonemapping curve to use when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key` is GAMMA_VALUE

The tonemap curve will be defined the following formula:

- OUT = pow(IN, 1.0 / gamma)

where IN and OUT is the input pixel value scaled to range \[0.0, 1.0\], pow is the power function and gamma is the gamma value specified by this key.

The same curve will be applied to all color channels. The camera device may clip the input gamma value to its supported range. The actual applied value will be returned in capture result.

The valid range of gamma value varies on different devices, but values within \[1.0, 5.0\] are guaranteed not to be clipped.

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key`

### TONEMAP_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TONEMAP_MODE: CaptureRequest.Key<Int!>
```

High-level global contrast/gamma/tonemapping control.

When switching to an application-defined contrast curve by setting `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key` to CONTRAST_CURVE, the curve is defined per-channel with a set of `(in, out)` points that specify the mapping from input high-bit-depth pixel value to the output low-bit-depth value. Since the actual pixel ranges of both input and output may change depending on the camera pipeline, the values are specified by normalized floating-point numbers.

More-complex color mapping operations such as 3D color look-up tables, selective chroma enhancement, or other non-linear color transforms will be disabled when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key` is CONTRAST_CURVE.

When using either FAST or HIGH_QUALITY, the camera device will emit its own tonemap curve in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_CURVE:android.hardware.camera2.CaptureRequest.Key`. These values are always available, and as close as possible to the actually used nonlinear/nonglobal transforms.

If a request is sent with CONTRAST_CURVE with the camera device's provided curve in FAST or HIGH_QUALITY, the image's tonemap will be roughly the same.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_CONTRAST_CURVE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_FAST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_HIGH_QUALITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_GAMMA_VALUE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_PRESET_CURVE:kotlin.Int`

**Available values for this device:** 
`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#TONEMAP_AVAILABLE_TONE_MAP_MODES:android.hardware.camera2.CameraCharacteristics.Key`

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#TONEMAP_AVAILABLE_TONE_MAP_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_CURVE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_CONTRAST_CURVE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_FAST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_HIGH_QUALITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_GAMMA_VALUE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_PRESET_CURVE:kotlin.Int`

### TONEMAP_PRESET_CURVE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TONEMAP_PRESET_CURVE: CaptureRequest.Key<Int!>
```

Tonemapping curve to use when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key` is PRESET_CURVE

The tonemap curve will be defined by specified standard.

sRGB (approximated by 16 control points):

<br />

Rec. 709 (approximated by 16 control points):

<br />

Note that above figures show a 16 control points approximation of preset curves. Camera devices may apply a different approximation to the curve.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_PRESET_CURVE_SRGB:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_PRESET_CURVE_REC709:kotlin.Int`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_PRESET_CURVE_SRGB:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_PRESET_CURVE_REC709:kotlin.Int`
