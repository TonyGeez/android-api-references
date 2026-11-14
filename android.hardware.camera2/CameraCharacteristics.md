Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CameraCharacteristics

```
class CameraCharacteristics : CameraMetadata<CameraCharacteristics.Key<*>!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.hardware.camera2.CameraMetadata](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata)\< [android.hardware.camera2.CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [\*](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#)\>\> ||
| | ↳ | [android.hardware.camera2.CameraCharacteristics](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#) |

The properties describing a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice`.

These properties are primarily fixed for a given CameraDevice, and can be queried through the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager` interface with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraCharacteristics(kotlin.String)`. Beginning with API level 32, some properties such as `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_ORIENTATION:android.hardware.camera2.CameraCharacteristics.Key` may change dynamically based on the state of the device. For information on whether a specific value is fixed, see the documentation for its key.

When obtained by a client that does not hold the CAMERA permission, some metadata values are not included. The list of keys that require the permission is given by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getKeysNeedingPermission()`.

`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#` objects are immutable.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key` A `Key` is used to do camera characteristics field lookups with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#get(android.hardware.camera2.CameraCharacteristics.Key)`. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_FRONT:kotlin.Int` The camera device faces the front of the vehicle body frame. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_LEFT:kotlin.Int` The camera device faces the left side of the vehicle body frame. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_OTHER:kotlin.Int` The camera device faces the outside of the vehicle body frame but not exactly one of the exterior sides defined by this enum. Applications should determine the exact facing direction from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_REAR:kotlin.Int` The camera device faces the rear of the vehicle body frame. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_RIGHT:kotlin.Int` The camera device faces the right side of the vehicle body frame. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_OTHER:kotlin.Int` The camera device faces the inside of the vehicle body frame but not exactly one of seats described by this enum. Applications should determine the exact facing direction from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_1_CENTER:kotlin.Int` The camera device faces the center seat of the first row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_1_LEFT:kotlin.Int` The camera device faces the left side seat of the first row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_1_RIGHT:kotlin.Int` The camera device faces the right seat of the first row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_2_CENTER:kotlin.Int` The camera device faces the center seat of the second row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_2_LEFT:kotlin.Int` The camera device faces the left side seat of the second row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_2_RIGHT:kotlin.Int` The camera device faces the right side seat of the second row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_3_CENTER:kotlin.Int` The camera device faces the center seat of the third row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_3_LEFT:kotlin.Int` The camera device faces the left side seat of the third row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_3_RIGHT:kotlin.Int` The camera device faces the right seat of the third row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_FRONT:kotlin.Int` The camera device exists outside of the vehicle body frame and on its front side. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_LEFT:kotlin.Int` The camera device exists outside and on left side of the vehicle body frame. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_OTHER:kotlin.Int` The camera exists outside of the vehicle body frame but not exactly on one of the exterior locations this enum defines. The applications should determine the exact location from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_REAR:kotlin.Int` The camera device exists outside of the vehicle body frame and on its rear side. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_RIGHT:kotlin.Int` The camera device exists outside and on right side of the vehicle body frame. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_FRONT:kotlin.Int` The camera device exists outside of the extra vehicle's body frame and on its front side. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_LEFT:kotlin.Int` The camera device exists outside and on left side of the extra vehicle body. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_OTHER:kotlin.Int` The camera device exists on an extra vehicle, such as the trailer, but not exactly on one of front, rear, left, or right side. Applications should determine the exact location from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_REAR:kotlin.Int` The camera device exists outside of the extra vehicle's body frame and on its rear side. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_RIGHT:kotlin.Int` The camera device exists outside and on right side of the extra vehicle body. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_INTERIOR:kotlin.Int` The camera device exists inside of the vehicle cabin. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_ABERRATION_MODE_FAST:kotlin.Int` Aberration correction will not slow down capture rate relative to sensor raw output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_ABERRATION_MODE_HIGH_QUALITY:kotlin.Int` Aberration correction operates at improved quality but the capture rate might be reduced (relative to sensor raw output rate) <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_ABERRATION_MODE_OFF:kotlin.Int` No aberration correction is applied. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_MODE_CCT:kotlin.Int` Use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_COLOR_TEMPERATURE:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_COLOR_TINT:android.hardware.camera2.CaptureRequest.Key` to adjust the white balance based on correlated color temperature. If AWB is enabled with `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key` != OFF ``, then CCT is ignored. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_MODE_FAST:kotlin.Int` Color correction processing must not slow down capture rate relative to sensor raw output. Advanced white balance adjustments above and beyond the specified white balance pipeline may be applied. If AWB is enabled with `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key` != OFF ``, then the camera device uses the last frame's AWB values (or defaults if AWB has never been run). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_MODE_HIGH_QUALITY:kotlin.Int` Color correction processing operates at improved quality but the capture rate might be reduced (relative to sensor raw output rate) Advanced white balance adjustments above and beyond the specified white balance pipeline may be applied. If AWB is enabled with `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key` != OFF ``, then the camera device uses the last frame's AWB values (or defaults if AWB has never been run). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_MODE_TRANSFORM_MATRIX:kotlin.Int` Use the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` matrix and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` to do color conversion. All advanced white balance adjustments (not specified by our white balance pipeline) must be disabled. If AWB is enabled with `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key` != OFF ``, then TRANSFORM_MATRIX is ignored. The camera device will override this value to either FAST or HIGH_QUALITY. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_ANTIBANDING_MODE_50HZ:kotlin.Int` The camera device will adjust exposure duration to avoid banding problems with 50Hz illumination sources. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_ANTIBANDING_MODE_60HZ:kotlin.Int` The camera device will adjust exposure duration to avoid banding problems with 60Hz illumination sources. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_ANTIBANDING_MODE_AUTO:kotlin.Int` The camera device will automatically adapt its antibanding routine to the current illumination condition. This is the default mode if AUTO is available on given camera device. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_ANTIBANDING_MODE_OFF:kotlin.Int` The camera device will not adjust exposure duration to avoid banding problems. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_OFF:kotlin.Int` The camera device's autoexposure routine is disabled. The application-selected `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` are used by the camera device, along with android.flash.\* fields, if there's a flash unit for this camera device. Note that auto-white balance (AWB) and auto-focus (AF) behavior is device dependent when AE is in OFF mode. To have consistent behavior across different devices, it is recommended to either set AWB and AF to OFF mode or lock AWB and AF before setting AE to OFF. See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_LOCK:android.hardware.camera2.CaptureRequest.Key`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key` for more details. LEGACY devices do not support the OFF mode and will override attempts to use this value to ON. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON:kotlin.Int` The camera device's autoexposure routine is active, with no flash control. The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` are ignored. The application has control over the various android.flash.\* fields. If the device supports manual flash strength control, i.e., if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_SINGLE_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_TORCH_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` are greater than 1, then the auto-exposure (AE) precapture metering sequence should be triggered for the configured flash mode and strength to avoid the image being incorrectly exposed at different `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_STRENGTH_LEVEL:android.hardware.camera2.CaptureRequest.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_ALWAYS_FLASH:kotlin.Int` Like ON, except that the camera device also controls the camera's flash unit, always firing it for still captures. The flash may be fired during a precapture sequence (triggered by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key`) and will always be fired for captures for which the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key` field is set to STILL_CAPTURE. It's important to wait for the precapture sequence to complete (i.e., `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key` reaches FLASH_REQUIRED, CONVERGED, or LOCKED) Dbefore submitting a STILL_CAPTURE request. Otherwise, in low-light conditions, the image captures with flash fired won't have correct exposures. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_AUTO_FLASH:kotlin.Int` Like ON, except that the camera device also controls the camera's flash unit, firing it in low-light conditions. The flash may be fired during a precapture sequence (triggered by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key`) and may be fired for captures for which the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key` field is set to STILL_CAPTURE. It's important to wait for the precapture sequence to complete (i.e., `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key` reaches FLASH_REQUIRED, CONVERGED, or LOCKED) before submitting a STILL_CAPTURE request. Otherwise, in low-light conditions, the image captures with flash fired won't have correct exposures. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_AUTO_FLASH_REDEYE:kotlin.Int` Like ON_AUTO_FLASH, but with automatic red eye reduction. If deemed necessary by the camera device, a red eye reduction flash will fire during the precapture sequence. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_EXTERNAL_FLASH:kotlin.Int` An external flash has been turned on. It informs the camera device that an external flash has been turned on, and that metering (and continuous focus if active) should be quickly recalculated to account for the external flash. Otherwise, this mode acts like ON. When the external flash is turned off, AE mode should be changed to one of the other available AE modes. If the camera device supports AE external flash mode, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key` must be FLASH_REQUIRED after the camera device finishes AE scan and it's too dark without flash. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_LOW_LIGHT_BOOST_BRIGHTNESS_PRIORITY:kotlin.Int` Like 'ON' but applies additional brightness boost in low light scenes. When the scene lighting conditions are within the range defined by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_LOW_LIGHT_BOOST_INFO_LUMINANCE_RANGE:android.hardware.camera2.CameraCharacteristics.Key` this mode will apply additional brightness boost. This mode will automatically adjust the intensity of low light boost applied according to the scene lighting conditions. A darker scene will receive more boost while a brighter scene will receive less boost. This mode can ignore the set target frame rate to allow more light to be captured which can result in choppier motion. The frame rate can extend to lower than the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_TARGET_FPS_RANGES:android.hardware.camera2.CameraCharacteristics.Key` but will not go below 10 FPS. This mode can also increase the sensor sensitivity gain which can result in increased luma and chroma noise. The sensor sensitivity gain can extend to higher values beyond `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_SENSITIVITY_RANGE:android.hardware.camera2.CameraCharacteristics.Key`. This mode may also apply additional processing to recover details in dark and bright areas of the image,and noise reduction at high sensitivity gain settings to manage the trade-off between light sensitivity and capture noise. This mode is restricted to two output surfaces. One output surface type can either be SurfaceView or TextureView. Another output surface type can either be MediaCodec or MediaRecorder. This mode cannot be used with a target FPS range higher than 30 FPS. If the session configuration is not supported, the AE mode reported in the CaptureResult will be 'ON' instead of 'ON_LOW_LIGHT_BOOST_BRIGHTNESS_PRIORITY'. When this AE mode is enabled, the CaptureResult field `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_LOW_LIGHT_BOOST_STATE:android.hardware.camera2.CaptureResult.Key` will indicate when low light boost is 'ACTIVE' or 'INACTIVE'. By default `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_LOW_LIGHT_BOOST_STATE:android.hardware.camera2.CaptureResult.Key` will be 'INACTIVE'. The low light boost is 'ACTIVE' once the scene lighting condition is less than the upper bound lux value defined by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_LOW_LIGHT_BOOST_INFO_LUMINANCE_RANGE:android.hardware.camera2.CameraCharacteristics.Key`. This mode will be 'INACTIVE' once the scene lighting condition is greater than the upper bound lux value defined by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_LOW_LIGHT_BOOST_INFO_LUMINANCE_RANGE:android.hardware.camera2.CameraCharacteristics.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRECAPTURE_TRIGGER_CANCEL:kotlin.Int` The camera device will cancel any currently active or completed precapture metering sequence, the auto-exposure routine will return to its initial state. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRECAPTURE_TRIGGER_IDLE:kotlin.Int` The trigger is idle. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRECAPTURE_TRIGGER_START:kotlin.Int` The precapture metering sequence will be started by the camera device. The exact effect of the precapture trigger depends on the current AE mode and state. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRIORITY_MODE_OFF:kotlin.Int` Disable AE priority mode. This is the default value. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRIORITY_MODE_SENSOR_EXPOSURE_TIME_PRIORITY:kotlin.Int` The camera device's auto-exposure routine is active and prioritizes the application-selected exposure time (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`). The application has control over `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key` while the application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` are ignored. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRIORITY_MODE_SENSOR_SENSITIVITY_PRIORITY:kotlin.Int` The camera device's auto-exposure routine is active and prioritizes the application-selected ISO (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`). The application has control over `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key` while the application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` are ignored. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_STATE_CONVERGED:kotlin.Int` AE has a good set of control values for the current scene. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_STATE_FLASH_REQUIRED:kotlin.Int` AE has a good set of control values, but flash needs to be fired for good quality still capture. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_STATE_INACTIVE:kotlin.Int` AE is off or recently reset. When a camera device is opened, it starts in this state. This is a transient state, the camera device may skip reporting this state in capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_STATE_LOCKED:kotlin.Int` AE has been locked. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_STATE_PRECAPTURE:kotlin.Int` AE has been asked to do a precapture sequence and is currently executing it. Precapture can be triggered through setting `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key` to START. Currently active and completed (if it causes camera device internal AE lock) precapture metering sequence can be canceled through setting `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key` to CANCEL. Once PRECAPTURE completes, AE will transition to CONVERGED or FLASH_REQUIRED as appropriate. This is a transient state, the camera device may skip reporting this state in capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_STATE_SEARCHING:kotlin.Int` AE doesn't yet have a good set of control values for the current scene. This is a transient state, the camera device may skip reporting this state in capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_AUTO:kotlin.Int` Basic automatic focus mode. In this mode, the lens does not move unless the autofocus trigger action is called. When that trigger is activated, AF will transition to ACTIVE_SCAN, then to the outcome of the scan (FOCUSED or NOT_FOCUSED). Always supported if lens is not fixed focus. Use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key` to determine if lens is fixed-focus. Triggering AF_CANCEL resets the lens position to default, and sets the AF state to INACTIVE. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_CONTINUOUS_PICTURE:kotlin.Int` In this mode, the AF algorithm modifies the lens position continually to attempt to provide a constantly-in-focus image stream. The focusing behavior should be suitable for still image capture; typically this means focusing as fast as possible. When the AF trigger is not involved, the AF algorithm should start in INACTIVE state, and then transition into PASSIVE_SCAN and PASSIVE_FOCUSED states as appropriate as it attempts to maintain focus. When the AF trigger is activated, the algorithm should finish its PASSIVE_SCAN if active, and then transition into AF_FOCUSED or AF_NOT_FOCUSED as appropriate, and lock the lens position until a cancel AF trigger is received. When the AF cancel trigger is activated, the algorithm should transition back to INACTIVE and then act as if it has just been started. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_CONTINUOUS_VIDEO:kotlin.Int` In this mode, the AF algorithm modifies the lens position continually to attempt to provide a constantly-in-focus image stream. The focusing behavior should be suitable for good quality video recording; typically this means slower focus movement and no overshoots. When the AF trigger is not involved, the AF algorithm should start in INACTIVE state, and then transition into PASSIVE_SCAN and PASSIVE_FOCUSED states as appropriate. When the AF trigger is activated, the algorithm should immediately transition into AF_FOCUSED or AF_NOT_FOCUSED as appropriate, and lock the lens position until a cancel AF trigger is received. Once cancel is received, the algorithm should transition back to INACTIVE and resume passive scan. Note that this behavior is not identical to CONTINUOUS_PICTURE, since an ongoing PASSIVE_SCAN must immediately be canceled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_EDOF:kotlin.Int` Extended depth of field (digital focus) mode. The camera device will produce images with an extended depth of field automatically; no special focusing operations need to be done before taking a picture. AF triggers are ignored, and the AF state will always be INACTIVE. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_MACRO:kotlin.Int` Close-up focusing mode. In this mode, the lens does not move unless the autofocus trigger action is called. When that trigger is activated, AF will transition to ACTIVE_SCAN, then to the outcome of the scan (FOCUSED or NOT_FOCUSED). This mode is optimized for focusing on objects very close to the camera. When that trigger is activated, AF will transition to ACTIVE_SCAN, then to the outcome of the scan (FOCUSED or NOT_FOCUSED). Triggering cancel AF resets the lens position to default, and sets the AF state to INACTIVE. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_OFF:kotlin.Int` The auto-focus routine does not control the lens; `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key` is controlled by the application. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_SCENE_CHANGE_DETECTED:kotlin.Int` Scene change is detected within the AF region(s). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_SCENE_CHANGE_NOT_DETECTED:kotlin.Int` Scene change is not detected within the AF region(s). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_STATE_ACTIVE_SCAN:kotlin.Int` AF is performing an AF scan because it was triggered by AF trigger. Only used by AUTO or MACRO AF modes. This is a transient state, the camera device may skip reporting this state in capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_STATE_FOCUSED_LOCKED:kotlin.Int` AF believes it is focused correctly and has locked focus. This state is reached only after an explicit START AF trigger has been sent (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`), when good focus has been obtained. The lens will remain stationary until the AF mode (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`) is changed or a new AF trigger is sent to the camera device (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_STATE_INACTIVE:kotlin.Int` AF is off or has not yet tried to scan/been asked to scan. When a camera device is opened, it starts in this state. This is a transient state, the camera device may skip reporting this state in capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_STATE_NOT_FOCUSED_LOCKED:kotlin.Int` AF has failed to focus successfully and has locked focus. This state is reached only after an explicit START AF trigger has been sent (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`), when good focus cannot be obtained. The lens will remain stationary until the AF mode (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`) is changed or a new AF trigger is sent to the camera device (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_STATE_PASSIVE_FOCUSED:kotlin.Int` AF currently believes it is in focus, but may restart scanning at any time. Only used by CONTINUOUS_\* AF modes. This is a transient state, the camera device may skip reporting this state in capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_STATE_PASSIVE_SCAN:kotlin.Int` AF is currently performing an AF scan initiated the camera device in a continuous autofocus mode. Only used by CONTINUOUS_\* AF modes. This is a transient state, the camera device may skip reporting this state in capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_STATE_PASSIVE_UNFOCUSED:kotlin.Int` AF finished a passive scan without finding focus, and may restart scanning at any time. Only used by CONTINUOUS_\* AF modes. This is a transient state, the camera device may skip reporting this state in capture result. LEGACY camera devices do not support this state. When a passive scan has finished, it will always go to PASSIVE_FOCUSED. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_TRIGGER_CANCEL:kotlin.Int` Autofocus will return to its initial state, and cancel any currently active trigger. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_TRIGGER_IDLE:kotlin.Int` The trigger is idle. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_TRIGGER_START:kotlin.Int` Autofocus will trigger now. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AUTOFRAMING_OFF:kotlin.Int` Disable autoframing. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AUTOFRAMING_ON:kotlin.Int` Enable autoframing to keep people in the frame's field of view. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AUTOFRAMING_STATE_CONVERGED:kotlin.Int` Auto-framing has reached a stable state (frame/fov is not being adjusted). The state may transition back to FRAMING if the scene changes. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AUTOFRAMING_STATE_FRAMING:kotlin.Int` Auto-framing is in process - either zooming in, zooming out or pan is taking place. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AUTOFRAMING_STATE_INACTIVE:kotlin.Int` Auto-framing is inactive. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_AUTO:kotlin.Int` The camera device's auto-white balance routine is active. The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_CLOUDY_DAYLIGHT:kotlin.Int` The camera device's auto-white balance routine is disabled; the camera device uses cloudy daylight light as the assumed scene illumination for white balance. The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_DAYLIGHT:kotlin.Int` The camera device's auto-white balance routine is disabled; the camera device uses daylight light as the assumed scene illumination for white balance. While the exact white balance transforms are up to the camera device, they will approximately match the CIE standard illuminant D65. The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_FLUORESCENT:kotlin.Int` The camera device's auto-white balance routine is disabled; the camera device uses fluorescent light as the assumed scene illumination for white balance. While the exact white balance transforms are up to the camera device, they will approximately match the CIE standard illuminant F2. The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_INCANDESCENT:kotlin.Int` The camera device's auto-white balance routine is disabled; the camera device uses incandescent light as the assumed scene illumination for white balance. While the exact white balance transforms are up to the camera device, they will approximately match the CIE standard illuminant A. The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_OFF:kotlin.Int` The camera device's auto-white balance routine is disabled. The application-selected color transform matrix (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key`) and gains (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key`) are used by the camera device for manual white balance control. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_SHADE:kotlin.Int` The camera device's auto-white balance routine is disabled; the camera device uses shade light as the assumed scene illumination for white balance. The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_TWILIGHT:kotlin.Int` The camera device's auto-white balance routine is disabled; the camera device uses twilight light as the assumed scene illumination for white balance. The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_WARM_FLUORESCENT:kotlin.Int` The camera device's auto-white balance routine is disabled; the camera device uses warm fluorescent light as the assumed scene illumination for white balance. While the exact white balance transforms are up to the camera device, they will approximately match the CIE standard illuminant F4. The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_STATE_CONVERGED:kotlin.Int` AWB has a good set of control values for the current scene. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_STATE_INACTIVE:kotlin.Int` AWB is not in auto mode, or has not yet started metering. When a camera device is opened, it starts in this state. This is a transient state, the camera device may skip reporting this state in capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_STATE_LOCKED:kotlin.Int` AWB has been locked. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_STATE_SEARCHING:kotlin.Int` AWB doesn't yet have a good set of control values for the current scene. This is a transient state, the camera device may skip reporting this state in capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_CUSTOM:kotlin.Int` The goal of this request doesn't fall into the other categories. The camera device will default to preview-like behavior. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_MANUAL:kotlin.Int` This request is for manual capture use case where the applications want to directly control the capture parameters. For example, the application may wish to manually control `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`, etc. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_MOTION_TRACKING:kotlin.Int` This request is for a motion tracking use case, where the application will use camera and inertial sensor data to locate and track objects in the world. The camera device auto-exposure routine will limit the exposure time of the camera to no more than 20 milliseconds, to minimize motion blur. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_PREVIEW:kotlin.Int` This request is for a preview-like use case. The precapture trigger may be used to start off a metering w/flash sequence. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_STILL_CAPTURE:kotlin.Int` This request is for a still capture-type use case. If the flash unit is under automatic control, it may fire as needed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_VIDEO_RECORD:kotlin.Int` This request is for a video recording use case. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_VIDEO_SNAPSHOT:kotlin.Int` This request is for a video snapshot (still image while recording video) use case. The camera device should take the highest-quality image possible (given the other settings) without disrupting the frame rate of video recording. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_ZERO_SHUTTER_LAG:kotlin.Int` This request is for a ZSL usecase; the application will stream full-resolution images and reprocess one or several later for a final capture. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_AQUA:kotlin.Int` An "aqua" effect where a blue hue is added to the image. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_BLACKBOARD:kotlin.Int` A "blackboard" effect where the image is typically displayed as regions of black, with white or grey details. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_MONO:kotlin.Int` A "monocolor" effect where the image is mapped into a single color. This will typically be grayscale. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_NEGATIVE:kotlin.Int` A "photo-negative" effect where the image's colors are inverted. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_OFF:kotlin.Int` No color effect will be applied. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_POSTERIZE:kotlin.Int` A "posterization" effect where the image uses discrete regions of tone rather than a continuous gradient of tones. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_SEPIA:kotlin.Int` A "sepia" effect where the image is mapped into warm gray, red, and brown tones. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_SOLARIZE:kotlin.Int` A "solarisation" effect (Sabattier effect) where the image is wholly or partially reversed in tone. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_WHITEBOARD:kotlin.Int` A "whiteboard" effect where the image is typically displayed as regions of white, with black or grey details. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EXTENDED_SCENE_MODE_BOKEH_CONTINUOUS:kotlin.Int` Bokeh effect must not slow down capture rate relative to sensor raw output, and the effect is applied to all processed streams no larger than the maximum streaming dimension. This mode should be used if performance and power are a priority, such as video recording. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EXTENDED_SCENE_MODE_BOKEH_STILL_CAPTURE:kotlin.Int` High quality bokeh mode is enabled for all non-raw streams (including YUV, JPEG, and IMPLEMENTATION_DEFINED) when capture intent is STILL_CAPTURE. Due to the extra image processing, this mode may introduce additional stall to non-raw streams. This mode should be used in high quality still capture use case. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EXTENDED_SCENE_MODE_DISABLED:kotlin.Int` Extended scene mode is disabled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_LOW_LIGHT_BOOST_STATE_ACTIVE:kotlin.Int` The AE mode 'ON_LOW_LIGHT_BOOST_BRIGHTNESS_PRIORITY' is enabled and applied. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_LOW_LIGHT_BOOST_STATE_INACTIVE:kotlin.Int` The AE mode 'ON_LOW_LIGHT_BOOST_BRIGHTNESS_PRIORITY' is enabled but not applied. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_AUTO:kotlin.Int` Use settings for each individual 3A routine. Manual control of capture parameters is disabled. All controls in android.control.\* besides sceneMode take effect. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_OFF:kotlin.Int` Full application control of pipeline. All control by the device's metering and focusing (3A) routines is disabled, and no other settings in android.control.\* have any effect, except that `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key` may be used by the camera device to select post-processing values for processing blocks that do not allow for manual control, or are not exposed by the camera API. However, the camera device's 3A routines may continue to collect statistics and update their internal state so that when control is switched to AUTO mode, good control values can be immediately applied. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_OFF_KEEP_STATE:kotlin.Int` Same as OFF mode, except that this capture will not be used by camera device background auto-exposure, auto-white balance and auto-focus algorithms (3A) to update their statistics. Specifically, the 3A routines are locked to the last values set from a request with AUTO, OFF, or USE_SCENE_MODE, and any statistics or state updates collected from manual captures with OFF_KEEP_STATE will be discarded by the camera device. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_USE_EXTENDED_SCENE_MODE:kotlin.Int` Use a specific extended scene mode. When extended scene mode is on, the camera device may override certain control parameters, such as targetFpsRange, AE, AWB, and AF modes, to achieve best power and quality tradeoffs. Only the mandatory stream combinations of LIMITED hardware level are guaranteed. This setting can only be used if extended scene mode is supported (i.e. android.control.availableExtendedSceneModes contains some modes other than DISABLED). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_USE_SCENE_MODE:kotlin.Int` Use a specific scene mode. Enabling this disables control.aeMode, control.awbMode and control.afMode controls; the camera device will ignore those settings while USE_SCENE_MODE is active (except for FACE_PRIORITY scene mode). Other control entries are still active. This setting can only be used if scene mode is supported (i.e. `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_SCENE_MODES:android.hardware.camera2.CameraCharacteristics.Key` contain some modes other than DISABLED). For extended scene modes such as BOKEH, please use USE_EXTENDED_SCENE_MODE instead. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_ACTION:kotlin.Int` Optimized for photos of quickly moving objects. Similar to SPORTS. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_BARCODE:kotlin.Int` Optimized for accurately capturing a photo of barcode for use by camera applications that wish to read the barcode value. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_BEACH:kotlin.Int` Optimized for bright, outdoor beach settings. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_CANDLELIGHT:kotlin.Int` Optimized for dim settings where the main light source is a candle. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_DISABLED:kotlin.Int` Indicates that no scene modes are set for a given capture request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_FACE_PRIORITY:kotlin.Int` If face detection support exists, use face detection data for auto-focus, auto-white balance, and auto-exposure routines. If face detection statistics are disabled (i.e. `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_FACE_DETECT_MODE:android.hardware.camera2.CaptureRequest.Key` is set to OFF), this should still operate correctly (but will not return face detection statistics to the framework). Unlike the other scene modes, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key` remain active when FACE_PRIORITY is set. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_FIREWORKS:kotlin.Int` Optimized for nighttime photos of fireworks. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_HDR:kotlin.Int` Turn on a device-specific high dynamic range (HDR) mode. In this scene mode, the camera device captures images that keep a larger range of scene illumination levels visible in the final image. For example, when taking a picture of a object in front of a bright window, both the object and the scene through the window may be visible when using HDR mode, while in normal AUTO mode, one or the other may be poorly exposed. As a tradeoff, HDR mode generally takes much longer to capture a single image, has no user control, and may have other artifacts depending on the HDR method used. Therefore, HDR captures operate at a much slower rate than regular captures. In this mode, on LIMITED or FULL devices, when a request is made with a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key` of STILL_CAPTURE, the camera device will capture an image using a high dynamic range capture technique. On LEGACY devices, captures that target a JPEG-format output will be captured with HDR, and the capture intent is not relevant. The HDR capture may involve the device capturing a burst of images internally and combining them into one, or it may involve the device using specialized high dynamic range capture hardware. In all cases, a single image is produced in response to a capture request submitted while in HDR mode. Since substantial post-processing is generally needed to produce an HDR image, only YUV, PRIVATE, and JPEG outputs are supported for LIMITED/FULL device HDR captures, and only JPEG outputs are supported for LEGACY HDR captures. Using a RAW output for HDR capture is not supported. Some devices may also support always-on HDR, which applies HDR processing at full frame rate. For these devices, intents other than STILL_CAPTURE will also produce an HDR output with no frame rate impact compared to normal operation, though the quality may be lower than for STILL_CAPTURE intents. If SCENE_MODE_HDR is used with unsupported output types or capture intents, the images captured will be as if the SCENE_MODE was not enabled at all. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_HIGH_SPEED_VIDEO:kotlin.Int` This is deprecated, please use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createConstrainedHighSpeedCaptureSession(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraConstrainedHighSpeedCaptureSession#createHighSpeedRequestList(android.hardware.camera2.CaptureRequest)` for high speed video recording. Optimized for high speed video recording (frame rate \>=60fps) use case. The supported high speed video sizes and fps ranges are specified in android.control.availableHighSpeedVideoConfigurations. To get desired output frame rates, the application is only allowed to select video size and fps range combinations listed in this static metadata. The fps range can be control via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key`. In this mode, the camera device will override aeMode, awbMode, and afMode to ON, ON, and CONTINUOUS_VIDEO, respectively. All post-processing block mode controls will be overridden to be FAST. Therefore, no manual control of capture and post-processing parameters is possible. All other controls operate the same as when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` == AUTO. This means that all other android.control.\* fields continue to work, such as - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_EXPOSURE_COMPENSATION:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_LOCK:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_LOCK:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EFFECT_MODE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_REGIONS:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` Outside of android.control.\*, the following controls will work: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_MODE:android.hardware.camera2.CaptureRequest.Key` (automatic flash for still capture will not work since aeMode is ON) - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_OPTICAL_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key` (if it is supported) - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_FACE_DETECT_MODE:android.hardware.camera2.CaptureRequest.Key` For high speed recording use case, the actual maximum supported frame rate may be lower than what camera can output, depending on the destination Surfaces for the image data. For example, if the destination surface is from video encoder, the application need check if the video encoder is capable of supporting the high frame rate for a given video size, or it will end up with lower recording frame rate. If the destination surface is from preview window, the preview frame rate will be bounded by the screen refresh rate. The camera device will only support up to 2 output high speed streams (processed non-stalling format defined in android.request.maxNumOutputStreams) in this mode. This control will be effective only if all of below conditions are true: - The application created no more than maxNumHighSpeedStreams processed non-stalling format output streams, where maxNumHighSpeedStreams is calculated as min(2, android.request.maxNumOutputStreams\[Processed (but not-stalling)\]). - The stream sizes are selected from the sizes reported by android.control.availableHighSpeedVideoConfigurations. - No processed non-stalling or raw streams are configured. When above conditions are NOT satisfied, the controls of this mode and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key` will be ignored by the camera device, the camera device will fall back to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` `==` AUTO, and the returned capture result metadata will give the fps range chosen by the camera device. Switching into or out of this mode may trigger some camera ISP/sensor reconfigurations, which may introduce extra latency. It is recommended that the application avoids unnecessary scene mode switch as much as possible. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_LANDSCAPE:kotlin.Int` Optimized for photos of distant macroscopic objects. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_NIGHT:kotlin.Int` Optimized for low-light settings. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_NIGHT_PORTRAIT:kotlin.Int` Optimized for still photos of people in low-light settings. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_PARTY:kotlin.Int` Optimized for dim, indoor settings with multiple moving people. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_PORTRAIT:kotlin.Int` Optimized for still photos of people. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_SNOW:kotlin.Int` Optimized for bright, outdoor settings containing snow. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_SPORTS:kotlin.Int` Optimized for photos of quickly moving people. Similar to ACTION. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_STEADYPHOTO:kotlin.Int` Optimized to avoid blurry photos due to small amounts of device motion (for example: due to hand shake). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_SUNSET:kotlin.Int` Optimized for scenes of the setting sun. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_THEATRE:kotlin.Int` Optimized for dim, indoor settings where flash must remain off. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SETTINGS_OVERRIDE_OFF:kotlin.Int` No keys are applied sooner than the other keys when applying CaptureRequest settings to the camera device. This is the default value. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SETTINGS_OVERRIDE_ZOOM:kotlin.Int` Zoom related keys are applied sooner than the other keys in the CaptureRequest. The zoom related keys are: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_REGIONS:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureRequest.Key` Even though `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_REGIONS:android.hardware.camera2.CaptureRequest.Key`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureRequest.Key` are not directly zoom related, applications typically scale these regions together with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` to have a consistent mapping within the current field of view. In this aspect, they are related to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_VIDEO_STABILIZATION_MODE_OFF:kotlin.Int` Video stabilization is disabled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_VIDEO_STABILIZATION_MODE_ON:kotlin.Int` Video stabilization is enabled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_VIDEO_STABILIZATION_MODE_PREVIEW_STABILIZATION:kotlin.Int` Preview stabilization, where the preview in addition to all other non-RAW streams are stabilized with the same quality of stabilization, is enabled. This mode aims to give clients a 'what you see is what you get' effect. In this mode, the FoV reduction will be a maximum of 20 % both horizontally and vertically (10% from left, right, top, bottom) for the given zoom ratio / crop region. The resultant FoV will also be the same across all processed streams (that have the same aspect ratio). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_ZOOM_METHOD_AUTO:kotlin.Int` The camera device automatically detects whether the application does zoom with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`, and in turn decides which metadata tag reflects the effective zoom level. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_ZOOM_METHOD_ZOOM_RATIO:kotlin.Int` The application intends to control zoom via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`, and the effective zoom level is reflected by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` in capture results. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#DISTORTION_CORRECTION_MODE_FAST:kotlin.Int` Lens distortion correction is applied without reducing frame rate relative to sensor output. It may be the same as OFF if distortion correction would reduce frame rate relative to sensor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#DISTORTION_CORRECTION_MODE_HIGH_QUALITY:kotlin.Int` High-quality distortion correction is applied, at the cost of possibly reduced frame rate relative to sensor output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#DISTORTION_CORRECTION_MODE_OFF:kotlin.Int` No distortion correction is applied. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EDGE_MODE_FAST:kotlin.Int` Apply edge enhancement at a quality level that does not slow down frame rate relative to sensor output. It may be the same as OFF if edge enhancement will slow down frame rate relative to sensor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EDGE_MODE_HIGH_QUALITY:kotlin.Int` Apply high-quality edge enhancement, at a cost of possibly reduced output frame rate. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EDGE_MODE_OFF:kotlin.Int` No edge enhancement is applied. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EDGE_MODE_ZERO_SHUTTER_LAG:kotlin.Int` Edge enhancement is applied at different levels for different output streams, based on resolution. Streams at maximum recording resolution (see android.hardware.camera2.CameraDevice#createCaptureSession) or below have edge enhancement applied, while higher-resolution streams have no edge enhancement applied. The level of edge enhancement for low-resolution streams is tuned so that frame rate is not impacted, and the quality is equal to or better than FAST (since it is only applied to lower-resolution outputs, quality may improve from FAST). This mode is intended to be used by applications operating in a zero-shutter-lag mode with YUV or PRIVATE reprocessing, where the application continuously captures high-resolution intermediate buffers into a circular buffer, from which a final image is produced via reprocessing when a user takes a picture. For such a use case, the high-resolution buffers must not have edge enhancement applied to maximize efficiency of preview and to avoid double-applying enhancement when reprocessed, while low-resolution buffers (used for recording or preview, generally) need edge enhancement applied for reasonable preview quality. This mode is guaranteed to be supported by devices that support either the YUV_REPROCESSING or PRIVATE_REPROCESSING capabilities (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` lists either of those capabilities) and it will be the default mode for CAMERA3_TEMPLATE_ZERO_SHUTTER_LAG template. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EXTENSION_NIGHT_MODE_INDICATOR_OFF:kotlin.Int` The camera has detected lighting conditions that are sufficiently bright. Night Mode Camera Extensions is available but may not be able to optimize the camera settings to take a higher quality photo. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EXTENSION_NIGHT_MODE_INDICATOR_ON:kotlin.Int` The camera has detected low-light conditions. It is recommended to use Night Mode Camera Extension to optimize the camera settings to take a high-quality photo in the dark. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EXTENSION_NIGHT_MODE_INDICATOR_UNKNOWN:kotlin.Int` The camera can't accurately assess the scene's lighting to determine if a Night Mode Camera Extension capture would improve the photo. This can happen when the current camera configuration doesn't support night mode indicator detection, such as when the auto exposure mode is ON_AUTO_FLASH, ON_ALWAYS_FLASH, ON_AUTO_FLASH_REDEYE, or ON_EXTERNAL_FLASH. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_MODE_OFF:kotlin.Int` Do not fire the flash for this capture. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_MODE_SINGLE:kotlin.Int` If the flash is available and charged, fire flash for this capture. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_MODE_TORCH:kotlin.Int` Transition flash to continuously on. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_STATE_CHARGING:kotlin.Int` Flash is charging and cannot be fired. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_STATE_FIRED:kotlin.Int` Flash fired for this capture. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_STATE_PARTIAL:kotlin.Int` Flash partially illuminated this frame. This is usually due to the next or previous frame having the flash fire, and the flash spilling into this capture due to hardware limitations. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_STATE_READY:kotlin.Int` Flash is ready to fire. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_STATE_UNAVAILABLE:kotlin.Int` No flash on camera. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#HOT_PIXEL_MODE_FAST:kotlin.Int` Hot pixel correction is applied, without reducing frame rate relative to sensor raw output. The hotpixel map may be returned in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_HOT_PIXEL_MAP:android.hardware.camera2.CaptureResult.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#HOT_PIXEL_MODE_HIGH_QUALITY:kotlin.Int` High-quality hot pixel correction is applied, at a cost of possibly reduced frame rate relative to sensor raw output. The hotpixel map may be returned in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_HOT_PIXEL_MAP:android.hardware.camera2.CaptureResult.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#HOT_PIXEL_MODE_OFF:kotlin.Int` No hot pixel correction is applied. The frame rate must not be reduced relative to sensor raw output for this option. The hotpixel map may be returned in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_HOT_PIXEL_MAP:android.hardware.camera2.CaptureResult.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_DEVICE_TYPE_BUILT_IN:kotlin.Int` This camera device is physically a part of this Android device, and the data produced is always within the device's control before it reaches the application requesting it. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_DEVICE_TYPE_EXTERNAL:kotlin.Int` This camera device is not permanently connected to this Android device. It may be connected by a wired connection, such as a USB webcam, or it might be connected wirelessly, such as via WiFi or other communication mechanism. The provenance of the image data from the external camera cannot be guaranteed, since it is produced by hardware that is not controlled by this Android device. Note that an `EXTERNAL` `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_DEVICE_TYPE:android.hardware.camera2.CameraCharacteristics.Key` `` does not mean the `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` `` must be `EXTERNAL`. A basic USB webcam would likely have an `EXTERNAL` hardware level, but more sophisticated remote camera systems may have more capabilities than that, and be listed with a `LIMITED` or better hardware level. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_DEVICE_TYPE_UNKNOWN:kotlin.Int` This camera device has an unknown classification. This value will be used when new device classifications need to be added in future Android versions, so that applications targeting older SDK levels do not have to handle unknown enumeration values. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_DEVICE_TYPE_VIRTUAL:kotlin.Int` This camera device produces purely virtual images, though they may be based on the output of a real hardware camera in some cases. For example, a virtual reality headset may have a virtual camera as the front-facing camera, producing a virtual avatar to represent the user, which is animated based on sensors on the headset. The image data should not be assumed to be real. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_3:kotlin.Int` This camera device is capable of YUV reprocessing and RAW data capture, in addition to FULL-level capabilities. The stream configurations listed in the `LEVEL_3`, `RAW`, `FULL`, `LEGACY` and `LIMITED` [tables](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#level-3-additional-guaranteed-configurations) in the documentation are guaranteed to be supported. The following additional capabilities are guaranteed to be supported: - `YUV_REPROCESSING` capability (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` contains `YUV_REPROCESSING`) - `RAW` capability (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` contains `RAW`) <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_EXTERNAL:kotlin.Int` This camera device is backed by an external camera connected to this Android device. The device has capability identical to a LIMITED level device, with the following exceptions: - The device may not report lens/sensor related information such as - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_HYPERFOCAL_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PHYSICAL_SIZE:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_WHITE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_BLACK_LEVEL_PATTERN:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_ROLLING_SHUTTER_SKEW:android.hardware.camera2.CaptureResult.Key` - The device will report 0 for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_ORIENTATION:android.hardware.camera2.CameraCharacteristics.Key` - The device has less guarantee on stable framerate, as the framerate partly depends on the external camera being used. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` This camera device is capable of supporting advanced imaging applications. The stream configurations listed in the `FULL`, `LEGACY` and `LIMITED` [tables](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#full-level-additional-guaranteed-configurations) in the documentation are guaranteed to be supported. A `FULL` device will support below capabilities: - `BURST_CAPTURE` capability (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` contains `BURST_CAPTURE`) - Per frame control (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SYNC_MAX_LATENCY:android.hardware.camera2.CameraCharacteristics.Key` `==` PER_FRAME_CONTROL) - Manual sensor control (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` contains `MANUAL_SENSOR`) - Manual post-processing control (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` contains `MANUAL_POST_PROCESSING`) - The required exposure time range defined in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_EXPOSURE_TIME_RANGE:android.hardware.camera2.CameraCharacteristics.Key` - The required maxFrameDuration defined in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_MAX_FRAME_DURATION:android.hardware.camera2.CameraCharacteristics.Key` Note: Pre-API level 23, FULL devices also supported arbitrary cropping region (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_CROPPING_TYPE:android.hardware.camera2.CameraCharacteristics.Key` `== FREEFORM`); this requirement was relaxed in API level 23, and `FULL` devices may only support `CENTERED` cropping. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LEGACY:kotlin.Int` This camera device is running in backward compatibility mode. Only the stream configurations listed in the `LEGACY` [table](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#legacy-level-guaranteed-configurations) in the documentation are supported. A `LEGACY` device does not support per-frame control, manual sensor control, manual post-processing, arbitrary cropping regions, and has relaxed performance constraints. No additional capabilities beyond `BACKWARD_COMPATIBLE` will ever be listed by a `LEGACY` device in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`. In addition, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key` is not functional on `LEGACY` devices. Instead, every request that includes a JPEG-format output target is treated as triggering a still capture, internally executing a precapture trigger. This may fire the flash for flash power metering during precapture, and then fire the flash for the final capture, if a flash is available on the device and the AE mode is set to enable the flash. Devices that initially shipped with Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` or newer will not include any LEGACY-level devices. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` This camera device does not have enough capabilities to qualify as a `FULL` device or better. Only the stream configurations listed in the `LEGACY` and `LIMITED` [tables](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#limited-level-additional-guaranteed-configurations) in the documentation are guaranteed to be supported. All `LIMITED` devices support the `BACKWARDS_COMPATIBLE` capability, indicating basic support for color image capture. The only exception is that the device may alternatively support only the `DEPTH_OUTPUT` capability, if it can only output depth measurements and not color images. `LIMITED` devices and above require the use of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key` to lock exposure metering (and calculate flash power, for cameras with flash) before capturing a high-quality still image. A `LIMITED` device that only lists the `BACKWARDS_COMPATIBLE` capability is only required to support full-automatic operation and post-processing (`OFF` is not supported for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`, or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`) Additional capabilities may optionally be supported by a `LIMITED`-level device, and can be checked for in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_FACING_BACK:kotlin.Int` The camera device faces the opposite direction as the device's screen. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_FACING_EXTERNAL:kotlin.Int` The camera device is an external camera, and has no fixed facing relative to the device's screen. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_FACING_FRONT:kotlin.Int` The camera device faces the same direction as the device's screen. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_INFO_FOCUS_DISTANCE_CALIBRATION_APPROXIMATE:kotlin.Int` The lens focus distance is measured in diopters. However, setting the lens to the same focus distance on separate occasions may result in a different real focus distance, depending on factors such as the orientation of the device, the age of the focusing mechanism, and the device temperature. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_INFO_FOCUS_DISTANCE_CALIBRATION_CALIBRATED:kotlin.Int` The lens focus distance is measured in diopters, and is calibrated. The lens mechanism is calibrated so that setting the same focus distance is repeatable on multiple occasions with good accuracy, and the focus distance corresponds to the real physical distance to the plane of best focus. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_INFO_FOCUS_DISTANCE_CALIBRATION_UNCALIBRATED:kotlin.Int` The lens focus distance is not accurate, and the units used for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key` do not correspond to any physical units. Setting the lens to the same focus distance on separate occasions may result in a different real focus distance, depending on factors such as the orientation of the device, the age of the focusing mechanism, and the device temperature. The focus distance value will still be in the range of ``[0, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key`]``, where 0 represents the farthest focus. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_OPTICAL_STABILIZATION_MODE_OFF:kotlin.Int` Optical stabilization is unavailable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_OPTICAL_STABILIZATION_MODE_ON:kotlin.Int` Optical stabilization is enabled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_POSE_REFERENCE_AUTOMOTIVE:kotlin.Int` The value of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` is relative to the origin of the automotive sensor coordinate system, which is at the center of the rear axle. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_POSE_REFERENCE_GYROSCOPE:kotlin.Int` The value of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` is relative to the position of the primary gyroscope of this Android device. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_POSE_REFERENCE_PRIMARY_CAMERA:kotlin.Int` The value of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` is relative to the optical center of the largest camera device facing the same direction as this camera. This is the default value for API levels before Android P. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_POSE_REFERENCE_UNDEFINED:kotlin.Int` The camera device cannot represent the values of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key` accurately enough. One such example is a camera device on the cover of a foldable phone: in order to measure the pose translation and rotation, some kind of hinge position sensor would be needed. The value of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` must be all zeros, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key` must be values matching its default facing. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_STATE_MOVING:kotlin.Int` One or several of the lens parameters (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FILTER_DENSITY:android.hardware.camera2.CaptureRequest.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_APERTURE:android.hardware.camera2.CaptureRequest.Key`) is currently changing. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_STATE_STATIONARY:kotlin.Int` The lens parameters (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FILTER_DENSITY:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_APERTURE:android.hardware.camera2.CaptureRequest.Key`) are not changing. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LOGICAL_MULTI_CAMERA_SENSOR_SYNC_TYPE_APPROXIMATE:kotlin.Int` A software mechanism is used to synchronize between the physical cameras. As a result, the timestamp of an image from a physical stream is only an approximation of the image sensor start-of-exposure time. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LOGICAL_MULTI_CAMERA_SENSOR_SYNC_TYPE_CALIBRATED:kotlin.Int` The camera device supports frame timestamp synchronization at the hardware level, and the timestamp of a physical stream image accurately reflects its start-of-exposure time. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_FAST:kotlin.Int` Noise reduction is applied without reducing frame rate relative to sensor output. It may be the same as OFF if noise reduction will reduce frame rate relative to sensor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_HIGH_QUALITY:kotlin.Int` High-quality noise reduction is applied, at the cost of possibly reduced frame rate relative to sensor output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_MINIMAL:kotlin.Int` MINIMAL noise reduction is applied without reducing frame rate relative to sensor output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_OFF:kotlin.Int` No noise reduction is applied. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_ZERO_SHUTTER_LAG:kotlin.Int` Noise reduction is applied at different levels for different output streams, based on resolution. Streams at maximum recording resolution (see android.hardware.camera2.CameraDevice#createCaptureSession) or below have noise reduction applied, while higher-resolution streams have MINIMAL (if supported) or no noise reduction applied (if MINIMAL is not supported.) The degree of noise reduction for low-resolution streams is tuned so that frame rate is not impacted, and the quality is equal to or better than FAST (since it is only applied to lower-resolution outputs, quality may improve from FAST). This mode is intended to be used by applications operating in a zero-shutter-lag mode with YUV or PRIVATE reprocessing, where the application continuously captures high-resolution intermediate buffers into a circular buffer, from which a final image is produced via reprocessing when a user takes a picture. For such a use case, the high-resolution buffers must not have noise reduction applied to maximize efficiency of preview and to avoid over-applying noise filtering when reprocessing, while low-resolution buffers (used for recording or preview, generally) need noise reduction applied for reasonable preview quality. This mode is guaranteed to be supported by devices that support either the YUV_REPROCESSING or PRIVATE_REPROCESSING capabilities (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` lists either of those capabilities) and it will be the default mode for CAMERA3_TEMPLATE_ZERO_SHUTTER_LAG template. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_BACKWARD_COMPATIBLE:kotlin.Int` The minimal set of capabilities that every camera device (regardless of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`) supports. This capability is listed by all normal devices, and indicates that the camera device has a feature set that's comparable to the baseline requirements for the older android.hardware.Camera API. Devices with the DEPTH_OUTPUT capability might not list this capability, indicating that they support only depth measurement, not standard color output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_BURST_CAPTURE:kotlin.Int` The camera device supports capturing high-resolution images at \>= 20 frames per second, in at least the uncompressed YUV format, when post-processing settings are set to FAST. Additionally, all image resolutions less than 24 megapixels can be captured at \>= 10 frames per second. Here, 'high resolution' means at least 8 megapixels, or the maximum resolution of the device, whichever is smaller. More specifically, this means that a size matching the camera device's active array size is listed as a supported size for the `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` format in either android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes or `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighResolutionOutputSizes(kotlin.Int)`, with a minimum frame duration for that format and size of either \<= 1/20 s, or \<= 1/10 s if the image size is less than 24 megapixels, respectively; and the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_TARGET_FPS_RANGES:android.hardware.camera2.CameraCharacteristics.Key` entry lists at least one FPS range where the minimum FPS is \>= 1 / minimumFrameDuration for the maximum-size YUV_420_888 format. If that maximum size is listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighResolutionOutputSizes(kotlin.Int)`, then the list of resolutions for YUV_420_888 from android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes contains at least one resolution \>= 8 megapixels, with a minimum frame duration of \<= 1/20 s. If the device supports the `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW10:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW12:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW14:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int`, then those can also be captured at the same rate as the maximum-size YUV_420_888 resolution is. If the device supports the PRIVATE_REPROCESSING capability, then the same guarantees as for the YUV_420_888 format also apply to the `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` format. In addition, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SYNC_MAX_LATENCY:android.hardware.camera2.CameraCharacteristics.Key` field is guaranteed to have a value between 0 and 4, inclusive. `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_LOCK_AVAILABLE:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AWB_LOCK_AVAILABLE:android.hardware.camera2.CameraCharacteristics.Key` are also guaranteed to be `true` so burst capture with these two locks ON yields consistent image output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_COLOR_SPACE_PROFILES:kotlin.Int` The device supports querying the possible combinations of color spaces, image formats, and dynamic range profiles supported by the camera and requesting a particular color space for a session via `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setColorSpace(android.graphics.ColorSpace.Named)`. Cameras that enable this capability may or may not also implement dynamic range profiles. If they don't, `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceProfiles#getSupportedDynamicRangeProfiles(android.graphics.ColorSpace.Named,%20kotlin.Int)` will return only `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#STANDARD:kotlin.Long` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceProfiles#getSupportedColorSpacesForDynamicRange(kotlin.Int,%20kotlin.Long)` will assume support of the `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#STANDARD:kotlin.Long` profile in all combinations of color spaces and image formats. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_CONSTRAINED_HIGH_SPEED_VIDEO:kotlin.Int` The device supports constrained high speed video recording (frame rate \>=120fps) use case. The camera device will support high speed capture session created by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createConstrainedHighSpeedCaptureSession(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)`, which only accepts high speed request lists created by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraConstrainedHighSpeedCaptureSession#createHighSpeedRequestList(android.hardware.camera2.CaptureRequest)`. A camera device can still support high speed video streaming by advertising the high speed FPS ranges in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_TARGET_FPS_RANGES:android.hardware.camera2.CameraCharacteristics.Key`. For this case, all normal capture request per frame control and synchronization requirements will apply to the high speed fps ranges, the same as all other fps ranges. This capability describes the capability of a specialized operating mode with many limitations (see below), which is only targeted at high speed video recording. The supported high speed video sizes and fps ranges are specified in `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoFpsRanges()`. To get desired output frame rates, the application is only allowed to select video size and FPS range combinations provided by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoSizes()`. The fps range can be controlled via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key`. In this capability, the camera device will override aeMode, awbMode, and afMode to ON, AUTO, and CONTINUOUS_VIDEO, respectively. All post-processing block mode controls will be overridden to be FAST. Therefore, no manual control of capture and post-processing parameters is possible. All other controls operate the same as when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` == AUTO. This means that all other android.control.\* fields continue to work, such as - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_EXPOSURE_COMPENSATION:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_LOCK:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_LOCK:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EFFECT_MODE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_REGIONS:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` Outside of android.control.\*, the following controls will work: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_MODE:android.hardware.camera2.CaptureRequest.Key` (TORCH mode only, automatic flash for still capture will not work since aeMode is ON) - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_OPTICAL_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key` (if it is supported) - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_FACE_DETECT_MODE:android.hardware.camera2.CaptureRequest.Key` (if it is supported) For high speed recording use case, the actual maximum supported frame rate may be lower than what camera can output, depending on the destination Surfaces for the image data. For example, if the destination surface is from video encoder, the application need check if the video encoder is capable of supporting the high frame rate for a given video size, or it will end up with lower recording frame rate. If the destination surface is from preview window, the actual preview frame rate will be bounded by the screen refresh rate. The camera device will only support up to 2 high speed simultaneous output surfaces (preview and recording surfaces) in this mode. Above controls will be effective only if all of below conditions are true: - The application creates a camera capture session with no more than 2 surfaces via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createConstrainedHighSpeedCaptureSession(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)`. The targeted surfaces must be preview surface (either from `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#` or `https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#`) or recording surface(either from `https://developer.android.com/reference/kotlin/android/media/MediaRecorder.html#getSurface()` or `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#createInputSurface()`). - The stream sizes are selected from the sizes reported by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoSizes()`. - The FPS ranges are selected from `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoFpsRanges()`. When above conditions are NOT satisfied, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createConstrainedHighSpeedCaptureSession(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)` will fail. Switching to a FPS range that has different maximum FPS may trigger some camera device reconfigurations, which may introduce extra latency. It is recommended that the application avoids unnecessary maximum target FPS changes as much as possible during high speed streaming. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_DEPTH_OUTPUT:kotlin.Int` The camera device can produce depth measurements from its field of view. This capability requires the camera device to support the following: - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH16:kotlin.Int` is supported as an output format. - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_POINT_CLOUD:kotlin.Int` is optionally supported as an output format. - This camera device, and all camera devices with the same `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key`, will list the following calibration metadata entries in both `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult`: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key` - The `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#DEPTH_DEPTH_IS_EXCLUSIVE:android.hardware.camera2.CameraCharacteristics.Key` entry is listed by this device. - As of Android P, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key` entry is listed by this device. - A LIMITED camera with only the DEPTH_OUTPUT capability does not have to support normal YUV_420_888, Y8, JPEG, and PRIV-format outputs. It only has to support the DEPTH16 format. Generally, depth output operates at a slower frame rate than standard color capture, so the DEPTH16 and DEPTH_POINT_CLOUD formats will commonly have a stall duration that should be accounted for (see android.hardware.camera2.params.StreamConfigurationMap#getOutputStallDuration). On a device that supports both depth and color-based output, to enable smooth preview, using a repeating burst is recommended, where a depth-output target is only included once every N frames, where N is the ratio between preview output rate and depth output rate, including depth stall time. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_DYNAMIC_RANGE_TEN_BIT:kotlin.Int` The device supports one or more 10-bit camera outputs according to the dynamic range profiles specified in `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#getSupportedProfiles()`. They can be configured as part of the capture session initialization via `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#setDynamicRangeProfile(kotlin.Long)`. Cameras that enable this capability must also support the following: - Profile `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#HLG10:kotlin.Long` - All mandatory stream combinations for this specific capability as per [documentation](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#10-bit-output-additional-guaranteed-configurations) - In case the device is not able to capture some combination of supported standard 8-bit and/or 10-bit dynamic range profiles within the same capture request, then those constraints must be listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#getProfileCaptureRequestConstraints(kotlin.Long)` - Recommended dynamic range profile listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_RECOMMENDED_TEN_BIT_DYNAMIC_RANGE_PROFILE:android.hardware.camera2.CameraCharacteristics.Key`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_LOGICAL_MULTI_CAMERA:kotlin.Int` The camera device is a logical camera backed by two or more physical cameras. In API level 28, the physical cameras must also be exposed to the application via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList()`. Starting from API level 29: - Some or all physical cameras may not be independently exposed to the application, in which case the physical camera IDs will not be available in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList()`. But the application can still query the physical cameras' characteristics by calling `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraCharacteristics(kotlin.String)`. - If a physical camera is hidden from camera ID list, the mandatory stream combinations for that physical camera must be supported through the logical camera using physical streams. One exception is that in API level 30, a physical camera may become unavailable via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.AvailabilityCallback#onPhysicalCameraUnavailable(kotlin.String,%20kotlin.String)` callback. Combinations of logical and physical streams, or physical streams from different physical cameras are not guaranteed. However, if the camera device supports `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#isSessionConfigurationSupported(android.hardware.camera2.params.SessionConfiguration)`, application must be able to query whether a stream combination involving physical streams is supported by calling `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#isSessionConfigurationSupported(android.hardware.camera2.params.SessionConfiguration)`. Camera application shouldn't assume that there are at most 1 rear camera and 1 front camera in the system. For an application that switches between front and back cameras, the recommendation is to switch between the first rear camera and the first front camera in the list of supported camera devices. This capability requires the camera device to support the following: - The IDs of underlying physical cameras are returned via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getPhysicalCameraIds()`. - This camera device must list static metadata `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LOGICAL_MULTI_CAMERA_SENSOR_SYNC_TYPE:android.hardware.camera2.CameraCharacteristics.Key` in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#`. - The underlying physical cameras' static metadata must list the following entries, so that the application can correlate pixels from the physical streams: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key` - The SENSOR_INFO_TIMESTAMP_SOURCE of the logical device and physical devices must be the same. - The logical camera must be LIMITED or higher device. A logical camera device's dynamic metadata may contain `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#LOGICAL_MULTI_CAMERA_ACTIVE_PHYSICAL_ID:android.hardware.camera2.CaptureResult.Key` to notify the application of the current active physical camera Id. An active physical camera is the physical camera from which the logical camera's main image data outputs (YUV or RAW) and metadata come from. In addition, this serves as an indication which physical camera is used to output to a RAW stream, or in case only physical cameras support RAW, which physical RAW stream the application should request. Logical camera's static metadata tags below describe the default active physical camera. An active physical camera is default if it's used when application directly uses requests built from a template. All templates will default to the same active physical camera. - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_SENSITIVITY_RANGE:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_EXPOSURE_TIME_RANGE:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_MAX_FRAME_DURATION:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PHYSICAL_SIZE:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_WHITE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_LENS_SHADING_APPLIED:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT2:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_CALIBRATION_TRANSFORM1:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_CALIBRATION_TRANSFORM2:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_COLOR_TRANSFORM1:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_COLOR_TRANSFORM2:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_FORWARD_MATRIX1:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_FORWARD_MATRIX2:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_BLACK_LEVEL_PATTERN:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_MAX_ANALOG_SENSITIVITY:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_OPTICAL_BLACK_REGIONS:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_AVAILABLE_TEST_PATTERN_MODES:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_HYPERFOCAL_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_FOCUS_DISTANCE_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key` The field of view of non-RAW physical streams must not be smaller than that of the non-RAW logical streams, or the maximum field-of-view of the physical camera, whichever is smaller. The application should check the physical capture result metadata and physical camera characteristics for how the physical streams are cropped or zoomed. See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key` on how field-of-view is calculated. Typically the physical stream of active physical camera has the same field-of-view as the logical streams. However, the same may not be true for physical streams from non-active physical cameras. For example, if the logical camera has a wide-ultrawide configuration where the wide lens is the default, when the crop region is set to the logical camera's active array size, (and the zoom ratio set to 1.0 starting from Android 11), a physical stream for the ultrawide camera may prefer outputting images with larger field-of-view than that of the wide camera for better stereo matching margin or more robust motion tracking. At the same time, the physical non-RAW streams' field of view must not be smaller than the requested crop region and zoom ratio, as long as it's within the physical lens' capability. For example, for a logical camera with wide-tele lens configuration where the wide lens is the default, if the logical camera's crop region is set to maximum size, and zoom ratio set to 1.0, the physical stream for the tele lens will be configured to its maximum size crop region (no zoom). *Deprecated:* Prior to Android 11, the field of view of all non-RAW physical streams cannot be larger than that of non-RAW logical streams. If the logical camera has a wide-ultrawide lens configuration where the wide lens is the default, when the logical camera's crop region is set to maximum size, the FOV of the physical streams for the ultrawide lens will be the same as the logical stream, by making the crop region smaller than its active array size to compensate for the smaller focal length. For a logical camera, typically the underlying physical cameras have different RAW capabilities (such as resolution or CFA pattern). There are two ways for the application to capture RAW images from the logical camera: - If the logical camera has RAW capability, the application can create and use RAW streams in the same way as before. In case a RAW stream is configured, to maintain backward compatibility, the camera device makes sure the default active physical camera remains active and does not switch to other physical cameras. (One exception is that, if the logical camera consists of identical image sensors and advertises multiple focalLength due to different lenses, the camera device may generate RAW images from different physical cameras based on the focalLength being set by the application.) This backward-compatible approach usually results in loss of optical zoom, to telephoto lens or to ultrawide lens. - Alternatively, if supported by the device, `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader` can be used to capture RAW images from one of the underlying physical cameras ( depending on current zoom level). Because different physical cameras may have different RAW characteristics, the application needs to use the characteristics and result metadata of the active physical camera for the relevant RAW metadata. The capture request and result metadata tags required for backward compatible camera functionalities will be solely based on the logical camera capability. On the other hand, the use of manual capture controls (sensor or post-processing) with a logical camera may result in unexpected behavior when the HAL decides to switch between physical cameras with different characteristics under the hood. For example, when the application manually sets exposure time and sensitivity while zooming in, the brightness of the camera images may suddenly change because HAL switches from one physical camera to the other. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_MANUAL_POST_PROCESSING:kotlin.Int` The camera device post-processing stages can be manually controlled. The camera device supports basic manual control of the image post-processing stages. This means the following controls are guaranteed to be supported: - Manual tonemap control - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_CURVE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#TONEMAP_MAX_CURVE_POINTS:android.hardware.camera2.CameraCharacteristics.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_GAMMA:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_PRESET_CURVE:android.hardware.camera2.CaptureRequest.Key` - Manual white balance control - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` - Manual lens shading map control - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SHADING_MODE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_LENS_SHADING_MAP_MODE:android.hardware.camera2.CaptureRequest.Key` - android.statistics.lensShadingMap - android.lens.info.shadingMapSize - Manual aberration correction control (if aberration correction is supported) - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_ABERRATION_MODE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#COLOR_CORRECTION_AVAILABLE_ABERRATION_MODES:android.hardware.camera2.CameraCharacteristics.Key` - Auto white balance lock - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_LOCK:android.hardware.camera2.CaptureRequest.Key` If auto white balance is enabled, then the camera device will accurately report the values applied by AWB in the result. A given camera device may also support additional post-processing controls, but this capability only covers the above list of controls. For camera devices with LOGICAL_MULTI_CAMERA capability, when underlying active physical camera switches, tonemap, white balance, and shading map may change even if awb is locked. However, the overall post-processing experience for users will be consistent. Refer to LOGICAL_MULTI_CAMERA capability for details. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_MANUAL_SENSOR:kotlin.Int` The camera device can be manually controlled (3A algorithms such as auto-exposure, and auto-focus can be bypassed). The camera device supports basic manual control of the sensor image acquisition related stages. This means the following controls are guaranteed to be supported: - Manual frame duration control - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_MAX_FRAME_DURATION:android.hardware.camera2.CameraCharacteristics.Key` - Manual exposure control - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_EXPOSURE_TIME_RANGE:android.hardware.camera2.CameraCharacteristics.Key` - Manual sensitivity control - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_SENSITIVITY_RANGE:android.hardware.camera2.CameraCharacteristics.Key` - Manual lens control (if the lens is adjustable) - android.lens.\* - Manual flash control (if a flash unit is present) - android.flash.\* - Manual black level locking - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#BLACK_LEVEL_LOCK:android.hardware.camera2.CaptureRequest.Key` - Auto exposure lock - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_LOCK:android.hardware.camera2.CaptureRequest.Key` If any of the above 3A algorithms are enabled, then the camera device will accurately report the values applied by 3A in the result. A given camera device may also support additional manual sensor controls, but this capability only covers the above list of controls. If this is supported, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key` will additionally return a min frame duration that is greater than zero for each supported size-format combination. For camera devices with LOGICAL_MULTI_CAMERA capability, when the underlying active physical camera switches, exposureTime, sensitivity, and lens properties may change even if AE/AF is locked. However, the overall auto exposure and auto focus experience for users will be consistent. Refer to LOGICAL_MULTI_CAMERA capability for details. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_MONOCHROME:kotlin.Int` The camera device is a monochrome camera that doesn't contain a color filter array, and for YUV_420_888 stream, the pixel values on U and V planes are all 128. A MONOCHROME camera must support the guaranteed stream combinations required for its device level and capabilities. Additionally, if the monochrome camera device supports Y8 format, all mandatory stream combination requirements related to `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` apply to `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int` as well. There are no mandatory stream combination requirements with regard to `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int` for Bayer camera devices. Starting from Android Q, the SENSOR_INFO_COLOR_FILTER_ARRANGEMENT of a MONOCHROME camera will be either MONO or NIR. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_MOTION_TRACKING:kotlin.Int` The camera device supports the MOTION_TRACKING value for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key`, which limits maximum exposure time to 20 ms. This limits the motion blur of capture images, resulting in better image tracking results for use cases such as image stabilization or augmented reality. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_OFFLINE_PROCESSING:kotlin.Int` The camera device supports the OFFLINE_PROCESSING use case. With OFFLINE_PROCESSING capability, the application can switch an ongoing capture session to offline mode by calling the CameraCaptureSession#switchToOffline method and specify streams to be kept in offline mode. The camera will then stop currently active repeating requests, prepare for some requests to go into offline mode, and return an offline session object. After the switchToOffline call returns, the original capture session is in closed state as if the CameraCaptureSession#close method has been called. In the offline mode, all inflight requests will continue to be processed in the background, and the application can immediately close the camera or create a new capture session without losing those requests' output images and capture results. While the camera device is processing offline requests, it might not be able to support all stream configurations it can support without offline requests. When that happens, the createCaptureSession method call will fail. The following stream configurations are guaranteed to work without hitting the resource busy exception: - One ongoing offline session: target one output surface of YUV or JPEG format, any resolution. - The active camera capture session: 1. One preview surface (SurfaceView or SurfaceTexture) up to 1920 width 2. One YUV ImageReader surface up to 1920 width 3. One Jpeg ImageReader, any resolution: the camera device is allowed to slow down JPEG output speed by 50% if there is any ongoing offline session. 4. If the device supports PRIVATE_REPROCESSING, one pair of ImageWriter/ImageReader surfaces of private format, with the same resolution that is larger or equal to the JPEG ImageReader resolution above. - Alternatively, the active camera session above can be replaced by an legacy `https://developer.android.com/reference/kotlin/android/hardware/Camera.html#` with the following parameter settings: 1. Preview size up to 1920 width 2. Preview callback size up to 1920 width 3. Video size up to 1920 width 4. Picture size, any resolution: the camera device is allowed to slow down JPEG output speed by 50% if there is any ongoing offline session. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_PRIVATE_REPROCESSING:kotlin.Int` The camera device supports the Zero Shutter Lag reprocessing use case. - One input stream is supported, that is, `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_MAX_NUM_INPUT_STREAMS:android.hardware.camera2.CameraCharacteristics.Key` == 1 ``. - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` is supported as an output/input format, that is, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` is included in the lists of formats returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputFormats()`. - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getValidOutputFormatsForInput(kotlin.Int)` returns non-empty int\[\] for each supported input format returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()`. - Each size returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputSizes(kotlin.Int)` is also included in android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes - Using `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` does not cause a frame rate drop relative to the sensor's maximum capture rate (at that resolution). - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` will be reprocessable into both `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` formats. - For a MONOCHROME camera supporting Y8 format, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` will be reprocessable into `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int`. - The maximum available resolution for PRIVATE streams (both input/output) will match the maximum available resolution of JPEG streams. - Static metadata `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REPROCESS_MAX_CAPTURE_STALL:android.hardware.camera2.CameraCharacteristics.Key`. - Only below controls are effective for reprocessing requests and will be present in capture results, other controls in reprocess requests will be ignored by the camera device. - android.jpeg.\* - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#NOISE_REDUCTION_MODE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#EDGE_MODE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#NOISE_REDUCTION_AVAILABLE_NOISE_REDUCTION_MODES:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#EDGE_AVAILABLE_EDGE_MODES:android.hardware.camera2.CameraCharacteristics.Key` will both list ZERO_SHUTTER_LAG as a supported mode. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_RAW:kotlin.Int` The camera device supports outputting RAW buffers and metadata for interpreting them. Devices supporting the RAW capability allow both for saving DNG files, and for direct application processing of raw sensor images. - RAW_SENSOR is supported as an output format. - The maximum available resolution for RAW_SENSOR streams will match either the value in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PIXEL_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`. - All DNG-related optional metadata entries are provided by the camera device. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_READ_SENSOR_SETTINGS:kotlin.Int` The camera device supports accurately reporting the sensor settings for many of the sensor controls while the built-in 3A algorithm is running. This allows reporting of sensor settings even when these settings cannot be manually changed. The values reported for the following controls are guaranteed to be available in the CaptureResult, including when 3A is enabled: - Exposure control - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key` - Sensitivity control - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key` - Lens controls (if the lens is adjustable) - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_APERTURE:android.hardware.camera2.CaptureRequest.Key` This capability is a subset of the MANUAL_SENSOR control capability, and will always be included if the MANUAL_SENSOR capability is available. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_REMOSAIC_REPROCESSING:kotlin.Int` The device supports reprocessing from the `RAW_SENSOR` format with a bayer pattern given by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_BINNING_FACTOR:android.hardware.camera2.CameraCharacteristics.Key` (m x n group of pixels with the same color filter) to a remosaiced regular bayer pattern. This capability will only be present for devices with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR:kotlin.Int` capability. When `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR:kotlin.Int` devices do not advertise this capability, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` images will already have a regular bayer pattern. If a `RAW_SENSOR` stream is requested along with another non-RAW stream in a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest` (if multiple streams are supported when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` is set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`), the `RAW_SENSOR` stream will have a regular bayer pattern. This capability requires the camera device to support the following : - The `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap` mentioned below refers to the one, described by `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key` ``. - One input stream is supported, that is, `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_MAX_NUM_INPUT_STREAMS:android.hardware.camera2.CameraCharacteristics.Key` == 1 ``. - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` is supported as an output/input format, that is, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` is included in the lists of formats returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputFormats()`. - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getValidOutputFormatsForInput(kotlin.Int)` returns non-empty int\[\] for each supported input format returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()`. - Each size returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputSizes(kotlin.Int)` is also included in android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes - Using `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` does not cause a frame rate drop relative to the sensor's maximum capture rate (at that resolution). - No CaptureRequest controls will be applicable when a request has an input target with `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` format. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_SECURE_IMAGE_DATA:kotlin.Int` The camera device is capable of writing image data into a region of memory inaccessible to Android userspace or the Android kernel, and only accessible to trusted execution environments (TEE). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_STREAM_USE_CASE:kotlin.Int` The camera device supports selecting a per-stream use case via `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#setStreamUseCase(kotlin.Long)` so that the device can optimize camera pipeline parameters such as tuning, sensor mode, or ISP settings for a specific user scenario. Some sample usages of this capability are: - Distinguish high quality YUV captures from a regular YUV stream where the image quality may not be as good as the JPEG stream, or - Use one stream to serve multiple purposes: viewfinder, video recording and still capture. This is common with applications that wish to apply edits equally to preview, saved images, and saved videos. This capability requires the camera device to support the following stream use cases: - DEFAULT for backward compatibility where the application doesn't set a stream use case - PREVIEW for live viewfinder and in-app image analysis - STILL_CAPTURE for still photo capture - VIDEO_RECORD for recording video clips - PREVIEW_VIDEO_STILL for one single stream used for viewfinder, video recording, and still capture. - VIDEO_CALL for long running video calls `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_STREAM_USE_CASES:android.hardware.camera2.CameraCharacteristics.Key` lists all of the supported stream use cases. Refer to the [guideline](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#stream-use-case-capability-additional-guaranteed-configurations) for the mandatory stream combinations involving stream use cases, which can also be queried via `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_SYSTEM_CAMERA:kotlin.Int` The camera device is only accessible by Android's system components and privileged applications. Processes need to have the android.permission.SYSTEM_CAMERA in addition to android.permission.CAMERA in order to connect to this camera device. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR:kotlin.Int` This camera device is capable of producing ultra high resolution images in addition to the image sizes described in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key`. It can operate in 'default' mode and 'max resolution' mode. It generally does this by binning pixels in 'default' mode and not binning them in 'max resolution' mode. `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key` `` describes the streams supported in 'default' mode. The stream configurations supported in 'max resolution' mode are described by `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key` ``. The maximum resolution mode pixel array size of a camera device (`` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PIXEL_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` ``) with this capability, will be at least 24 megapixels. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_YUV_REPROCESSING:kotlin.Int` The camera device supports the YUV_420_888 reprocessing use case, similar as PRIVATE_REPROCESSING, This capability requires the camera device to support the following: - One input stream is supported, that is, `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_MAX_NUM_INPUT_STREAMS:android.hardware.camera2.CameraCharacteristics.Key` == 1 ``. - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` is supported as an output/input format, that is, YUV_420_888 is included in the lists of formats returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputFormats()`. - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getValidOutputFormatsForInput(kotlin.Int)` returns non-empty int\[\] for each supported input format returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()`. - Each size returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputSizes(kotlin.Int)` is also included in android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes - Using `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` does not cause a frame rate drop relative to the sensor's maximum capture rate (at that resolution). - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` will be reprocessable into both `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` formats. - The maximum available resolution for `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` streams (both input/output) will match the maximum available resolution of `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` streams. - For a MONOCHROME camera with Y8 format support, all the requirements mentioned above for YUV_420_888 apply for Y8 format as well. - Static metadata `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REPROCESS_MAX_CAPTURE_STALL:android.hardware.camera2.CameraCharacteristics.Key`. - Only the below controls are effective for reprocessing requests and will be present in capture results. The reprocess requests are from the original capture results that are associated with the intermediate `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` output buffers. All other controls in the reprocess requests will be ignored by the camera device. - android.jpeg.\* - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#NOISE_REDUCTION_MODE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#EDGE_MODE:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#REPROCESS_EFFECTIVE_EXPOSURE_FACTOR:android.hardware.camera2.CaptureRequest.Key` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#NOISE_REDUCTION_AVAILABLE_NOISE_REDUCTION_MODES:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#EDGE_AVAILABLE_EDGE_MODES:android.hardware.camera2.CameraCharacteristics.Key` will both list ZERO_SHUTTER_LAG as a supported mode. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_CROPPED_RAW:kotlin.Int` Cropped RAW stream when the client chooses to crop the field of view. Certain types of image sensors can run in binned modes in order to improve signal to noise ratio while capturing frames. However, at certain zoom levels and / or when other scene conditions are deemed fit, the camera sub-system may choose to un-bin and remosaic the sensor's output. This results in a RAW frame which is cropped in field of view and yet has the same number of pixels as full field of view RAW, thereby improving image detail. The resultant field of view of the RAW stream will be greater than or equal to croppable non-RAW streams. The effective crop region for this RAW stream will be reflected in the CaptureResult key `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SCALER_RAW_CROP_REGION:android.hardware.camera2.CaptureResult.Key`. If this stream use case is set on a non-RAW stream, i.e. not one of : - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW10:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW12:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW14:kotlin.Int` session configuration is not guaranteed to succeed. This stream use case may not be supported on some devices. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_DEFAULT:kotlin.Int` Default stream use case. This use case is the same as when the application doesn't set any use case for the stream. The camera device uses the properties of the output target, such as format, dataSpace, or surface class type, to optimize the image processing pipeline. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_PREVIEW:kotlin.Int` Live stream shown to the user. Optimized for performance and usability as a viewfinder, but not necessarily for image quality. The output is not meant to be persisted as saved images or video. No stall if android.control.\* are set to FAST. There may be stall if they are set to HIGH_QUALITY. This use case has the same behavior as the default SurfaceView and SurfaceTexture targets. Additionally, this use case can be used for in-app image analysis. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_PREVIEW_VIDEO_STILL:kotlin.Int` One single stream used for combined purposes of preview, video, and still capture. For such multi-purpose streams, the camera device aims to make the best tradeoff between the individual use cases. For example, the STILL_CAPTURE use case by itself may have stalls for achieving best image quality. But if combined with PREVIEW and VIDEO_RECORD, the camera device needs to trade off the additional image processing for speed so that preview and video recording aren't slowed down. Similarly, VIDEO_RECORD may produce frames with a substantial lag, but PREVIEW_VIDEO_STILL must have minimal output delay. This means that to enable video stabilization with this use case, the device must support and the app must select the PREVIEW_STABILIZATION mode for video stabilization. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_STILL_CAPTURE:kotlin.Int` Still photo capture. Optimized for high-quality high-resolution capture, and not expected to maintain preview-like frame rates. The stream may have stalls regardless of whether android.control.\* is HIGH_QUALITY. This use case has the same behavior as the default JPEG and RAW related formats. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_VIDEO_CALL:kotlin.Int` Long-running video call optimized for both power efficiency and video quality. The camera sensor may run in a lower-resolution mode to reduce power consumption at the cost of some image and digital zoom quality. Unlike VIDEO_RECORD, VIDEO_CALL outputs are expected to work in dark conditions, so are usually accompanied with variable frame rate settings to allow sufficient exposure time in low light. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_VIDEO_RECORD:kotlin.Int` Recording video clips. Optimized for high-quality video capture, including high-quality image stabilization if supported by the device and enabled by the application. As a result, may produce output frames with a substantial lag from real time, to allow for highest-quality stabilization or other processing. As such, such an output is not suitable for drawing to screen directly, and is expected to be persisted to disk or similar for later playback or processing. Only streams that set the VIDEO_RECORD use case are guaranteed to have video stabilization applied when the video stabilization control is set to ON, as opposed to PREVIEW_STABILIZATION. This use case has the same behavior as the default MediaRecorder and MediaCodec targets. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_CROPPING_TYPE_CENTER_ONLY:kotlin.Int` The camera device only supports centered crop regions. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_CROPPING_TYPE_FREEFORM:kotlin.Int` The camera device supports arbitrarily chosen crop regions. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_180:kotlin.Int` Processed images are rotated by 180 degrees. Since the aspect ratio does not change, no cropping is performed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_270:kotlin.Int` Processed images are rotated by 270 degrees clockwise, and then cropped to the original aspect ratio. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_90:kotlin.Int` Processed images are rotated by 90 degrees clockwise, and then cropped to the original aspect ratio. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_AUTO:kotlin.Int` The camera API automatically selects the best concrete value for rotate-and-crop based on the application's support for resizability and the current multi-window mode. If the application does not support resizing but the display mode for its main Activity is not in a typical orientation, the camera API will set `ROTATE_AND_CROP_90` or some other supported rotation value, depending on device configuration, to ensure preview and captured images are correctly shown to the user. Otherwise, `ROTATE_AND_CROP_NONE` will be selected. When a value other than NONE is selected, several metadata fields will also be parsed differently to ensure that coordinates are correctly handled for features like drawing face detection boxes or passing in tap-to-focus coordinates. The camera API will convert positions in the active array coordinate system to/from the cropped-and-rotated coordinate system to make the operation transparent for applications. No coordinate mapping will be done when the application selects a non-AUTO mode. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_NONE:kotlin.Int` No rotate and crop is applied. Processed outputs are in the sensor orientation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_BGGR:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_GBRG:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_GRBG:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_MONO:kotlin.Int` Sensor doesn't have any Bayer color filter. Such sensor captures visible light in monochrome. The exact weighting and wavelengths captured is not specified, but generally only includes the visible frequencies. This value implies a MONOCHROME camera. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_NIR:kotlin.Int` Sensor has a near infrared filter capturing light with wavelength between roughly 750nm and 1400nm, and the same filter covers the whole sensor array. This value implies a MONOCHROME camera. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_RGB:kotlin.Int` Sensor is not Bayer; output has 3 16-bit values for each pixel, instead of just 1 16-bit value per pixel. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_RGGB:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_TIMESTAMP_SOURCE_REALTIME:kotlin.Int` Timestamps from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_TIMESTAMP:android.hardware.camera2.CaptureResult.Key` are in the same timebase as `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtimeNanos()`, and they can be compared to other timestamps using that base. When buffers from a REALTIME device are passed directly to a video encoder from the camera, automatic compensation is done to account for differing timebases of the audio and camera subsystems. If the application is receiving buffers and then later sending them to a video encoder or other application where they are compared with audio subsystem timestamps or similar, this compensation is not present. In those cases, applications need to adjust the timestamps themselves. Since `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtimeNanos()` and `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()` only diverge while the device is asleep, an offset between the two sources can be measured once per active session and applied to timestamps for sufficient accuracy for A/V sync. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_TIMESTAMP_SOURCE_UNKNOWN:kotlin.Int` Timestamps from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_TIMESTAMP:android.hardware.camera2.CaptureResult.Key` are in nanoseconds and monotonic, but can not be compared to timestamps from other subsystems (e.g. accelerometer, gyro etc.), or other instances of the same or different camera devices in the same system with accuracy. However, the timestamps are roughly in the same timebase as `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()`. The accuracy is sufficient for tasks like A/V synchronization for video recording, at least, and the timestamps can be directly used together with timestamps from the audio subsystem for that task. Timestamps between streams and results for a single camera instance are comparable, and the timestamps for all buffers and the result metadata generated by a single capture are identical. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_DEFAULT:kotlin.Int` This is the default sensor pixel mode. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int` In this mode, sensors typically do not bin pixels, as a result can offer larger image sizes. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_READOUT_TIMESTAMP_HARDWARE:kotlin.Int` This camera device supports the onReadoutStarted callback as well as outputting readout timestamps. The readout timestamp is generated by the camera hardware and it has the same accuracy and timing characteristics of the start-of-exposure time. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_READOUT_TIMESTAMP_NOT_SUPPORTED:kotlin.Int` This camera device doesn't support readout timestamp and onReadoutStarted callback. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_CLOUDY_WEATHER:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_COOL_WHITE_FLUORESCENT:kotlin.Int` W 3900 - 4500K <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_D50:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_D55:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_D65:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_D75:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_DAYLIGHT:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_DAYLIGHT_FLUORESCENT:kotlin.Int` D 5700 - 7100K <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_DAY_WHITE_FLUORESCENT:kotlin.Int` N 4600 - 5400K <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_FINE_WEATHER:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_FLASH:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_FLUORESCENT:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_ISO_STUDIO_TUNGSTEN:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_SHADE:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_STANDARD_A:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_STANDARD_B:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_STANDARD_C:kotlin.Int` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_TUNGSTEN:kotlin.Int` Incandescent light <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_WHITE_FLUORESCENT:kotlin.Int` WW 3200 - 3700K <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_COLOR_BARS:kotlin.Int` All pixel data is replaced with an 8-bar color pattern. The vertical bars (left-to-right) are as follows: - 100% white - yellow - cyan - green - magenta - red - blue - black In general the image would look like the following: ```kotlin <code>W Y C G M R B K W Y C G M R B K W Y C G M R B K W Y C G M R B K W Y C G M R B K . . . . . . . . . . . . . . . . . . . . . . . . (B = Blue, K = Black) </code> ``` Each bar should take up 1/8 of the sensor pixel array width. When this is not possible, the bar size should be rounded down to the nearest integer and the pattern can repeat on the right side. Each bar's height must always take up the full sensor pixel array height. Each pixel in this test pattern must be set to either 0% intensity or 100% intensity. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_COLOR_BARS_FADE_TO_GRAY:kotlin.Int` The test pattern is similar to COLOR_BARS, except that each bar should start at its specified color at the top, and fade to gray at the bottom. Furthermore each bar is further subdivided into a left and right half. The left half should have a smooth gradient, and the right half should have a quantized gradient. In particular, the right half's should consist of blocks of the same color for 1/16th active sensor pixel array width. The least significant bits in the quantized gradient should be copied from the most significant bits of the smooth gradient. The height of each bar should always be a multiple of 128. When this is not the case, the pattern should repeat at the bottom of the image. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_CUSTOM1:kotlin.Int` The first custom test pattern. All custom patterns that are available only on this camera device are at least this numeric value. All of the custom test patterns will be static (that is the raw image must not vary from frame to frame). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_OFF:kotlin.Int` No test pattern mode is used, and the camera device returns captures from the image sensor. This is the default if the key is not set. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_PN9:kotlin.Int` All pixel data is replaced by a pseudo-random sequence generated from a PN9 512-bit sequence (typically implemented in hardware with a linear feedback shift register). The generator should be reset at the beginning of each frame, and thus each subsequent raw frame with this test pattern should be exactly the same as the last. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_SOLID_COLOR:kotlin.Int` Each pixel in `[R, G_even, G_odd, B]` is replaced by its respective color channel provided in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_TEST_PATTERN_DATA:android.hardware.camera2.CaptureRequest.Key`. For example: ```kotlin <code><code><a docref="android.hardware.camera2.CaptureRequest$SENSOR_TEST_PATTERN_DATA">android.sensor.testPatternData</a></code> = [0, 0xFFFFFFFF, 0xFFFFFFFF, 0] </code> ``` All green pixels are 100% green. All red/blue pixels are black. ```kotlin <code><code><a docref="android.hardware.camera2.CaptureRequest$SENSOR_TEST_PATTERN_DATA">android.sensor.testPatternData</a></code> = [0xFFFFFFFF, 0, 0xFFFFFFFF, 0] </code> ``` All red pixels are 100% red. Only the odd green pixels are 100% green. All blue pixels are 100% black. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SHADING_MODE_FAST:kotlin.Int` Apply lens shading corrections, without slowing frame rate relative to sensor raw output <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SHADING_MODE_HIGH_QUALITY:kotlin.Int` Apply high-quality lens shading correction, at the cost of possibly reduced frame rate. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SHADING_MODE_OFF:kotlin.Int` No lens shading correction is applied. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_FACE_DETECT_MODE_FULL:kotlin.Int` Return all face metadata. In this mode, face rectangles, scores, landmarks, and face IDs are all valid. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_FACE_DETECT_MODE_OFF:kotlin.Int` Do not include face detection statistics in capture results. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_FACE_DETECT_MODE_SIMPLE:kotlin.Int` Return face rectangle and confidence values only. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_LENS_SHADING_MAP_MODE_OFF:kotlin.Int` Do not include a lens shading map in the capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_LENS_SHADING_MAP_MODE_ON:kotlin.Int` Include a lens shading map in the capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_OIS_DATA_MODE_OFF:kotlin.Int` Do not include OIS data in the capture result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_OIS_DATA_MODE_ON:kotlin.Int` Include OIS data in the capture result. `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_OIS_SAMPLES:android.hardware.camera2.CaptureResult.Key` provides OIS sample data in the output result metadata. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_SCENE_FLICKER_50HZ:kotlin.Int` The camera device detects illumination flickering at 50Hz in the current scene. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_SCENE_FLICKER_60HZ:kotlin.Int` The camera device detects illumination flickering at 60Hz in the current scene. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_SCENE_FLICKER_NONE:kotlin.Int` The camera device does not detect any flickering illumination in the current scene. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SYNC_MAX_LATENCY_PER_FRAME_CONTROL:kotlin.Int` Every frame has the requests immediately applied. Changing controls over multiple requests one after another will produce results that have those controls applied atomically each frame. All FULL capability devices will have this as their maxLatency. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SYNC_MAX_LATENCY_UNKNOWN:kotlin.Int` Each new frame has some subset (potentially the entire set) of the past requests applied to the camera settings. By submitting a series of identical requests, the camera device will eventually have the camera settings applied, but it is unknown when that exact point will be. All LEGACY capability devices will have this as their maxLatency. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_CONTRAST_CURVE:kotlin.Int` Use the tone mapping curve specified in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_CURVE:android.hardware.camera2.CaptureRequest.Key`\* entries. All color enhancement and tonemapping must be disabled, except for applying the tonemapping curve specified by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_CURVE:android.hardware.camera2.CaptureRequest.Key`. Must not slow down frame rate relative to raw sensor output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_FAST:kotlin.Int` Advanced gamma mapping and color enhancement may be applied, without reducing frame rate compared to raw sensor output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_GAMMA_VALUE:kotlin.Int` Use the gamma value specified in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_GAMMA:android.hardware.camera2.CaptureRequest.Key` to perform tonemapping. All color enhancement and tonemapping must be disabled, except for applying the tonemapping curve specified by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_GAMMA:android.hardware.camera2.CaptureRequest.Key`. Must not slow down frame rate relative to raw sensor output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_HIGH_QUALITY:kotlin.Int` High-quality gamma mapping and color enhancement will be applied, at the cost of possibly reduced frame rate compared to raw sensor output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_PRESET_CURVE:kotlin.Int` Use the preset tonemapping curve specified in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_PRESET_CURVE:android.hardware.camera2.CaptureRequest.Key` to perform tonemapping. All color enhancement and tonemapping must be disabled, except for applying the tonemapping curve specified by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_PRESET_CURVE:android.hardware.camera2.CaptureRequest.Key`. Must not slow down frame rate relative to raw sensor output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_PRESET_CURVE_REC709:kotlin.Int` Tonemapping curve is defined by ITU-R BT.709 <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_PRESET_CURVE_SRGB:kotlin.Int` Tonemapping curve is defined by sRGB <br /> | ||

| Public methods ||
|---|---|
| T? | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#get(android.hardware.camera2.CameraCharacteristics.Key)(key: https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key<T>!)` Get a camera characteristics field value. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CaptureRequest.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Key)\<\*\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getAvailableCaptureRequestKeys()()` Returns the list of keys supported by this `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice` for querying with a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest`. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CaptureResult.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult.Key)\<\*\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getAvailableCaptureResultKeys()()` Returns the list of keys supported by this `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice` for querying with a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult`. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CaptureRequest.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Key)\<\*\>!\>! | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getAvailablePhysicalCameraRequestKeys()()` Returns a subset of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getAvailableCaptureRequestKeys()` keys that can be overridden for physical devices backing a logical multi-camera. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\<\*\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getAvailableSessionCharacteristicsKeys()()` Get the keys in Camera Characteristics whose values are capture session specific. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CaptureRequest.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Key)\<\*\>!\>! | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getAvailableSessionKeys()()` Returns a subset of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getAvailableCaptureRequestKeys()` keys that the camera device can pass as part of the capture session initialization. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\<\*\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getKeys()()` Returns a list of the keys contained in this map. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\<\*\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getKeysNeedingPermission()()` Returns a subset of the list returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getKeys()` with all keys that require camera clients to obtain the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` permission. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getPhysicalCameraIds()()` Returns the set of physical camera ids that this logical `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice` is made up of. |
| [RecommendedStreamConfigurationMap](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap)? | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getRecommendedStreamConfigurationMap(kotlin.Int)(usecase: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve camera device recommended stream configuration map `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap` for a given use case. |

| Properties ||
|---|---|
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key` The direction of the camera faces relative to the vehicle body frame and the passenger seats. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LOCATION:android.hardware.camera2.CameraCharacteristics.Key` Location of the cameras on the automotive devices. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#COLOR_CORRECTION_AVAILABLE_ABERRATION_MODES:android.hardware.camera2.CameraCharacteristics.Key` List of aberration correction modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_ABERRATION_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#COLOR_CORRECTION_AVAILABLE_MODES:android.hardware.camera2.CameraCharacteristics.Key` List of color correction modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Range](https://developer.android.com/reference/kotlin/android/util/Range.html#)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#COLOR_CORRECTION_COLOR_TEMPERATURE_RANGE:android.hardware.camera2.CameraCharacteristics.Key` The range of supported color temperature values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_COLOR_TEMPERATURE:android.hardware.camera2.CaptureRequest.Key`. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_ANTIBANDING_MODES:android.hardware.camera2.CameraCharacteristics.Key` List of auto-exposure antibanding modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_ANTIBANDING_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_MODES:android.hardware.camera2.CameraCharacteristics.Key` List of auto-exposure modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_PRIORITY_MODES:android.hardware.camera2.CameraCharacteristics.Key` List of auto-exposure priority modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRIORITY_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Range](https://developer.android.com/reference/kotlin/android/util/Range.html#)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_TARGET_FPS_RANGES:android.hardware.camera2.CameraCharacteristics.Key` List of frame rate ranges for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key` supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Range](https://developer.android.com/reference/kotlin/android/util/Range.html#)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_COMPENSATION_RANGE:android.hardware.camera2.CameraCharacteristics.Key` Maximum and minimum exposure compensation values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_EXPOSURE_COMPENSATION:android.hardware.camera2.CaptureRequest.Key`, in counts of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_COMPENSATION_STEP:android.hardware.camera2.CameraCharacteristics.Key`, that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Rational](https://developer.android.com/reference/kotlin/android/util/Rational.html#)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_COMPENSATION_STEP:android.hardware.camera2.CameraCharacteristics.Key` Smallest step by which the exposure compensation can be changed. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_LOCK_AVAILABLE:android.hardware.camera2.CameraCharacteristics.Key` Whether the camera device supports `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_LOCK:android.hardware.camera2.CaptureRequest.Key` |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AF_AVAILABLE_MODES:android.hardware.camera2.CameraCharacteristics.Key` List of auto-focus (AF) modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AUTOFRAMING_AVAILABLE:android.hardware.camera2.CameraCharacteristics.Key` Whether the camera device supports `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AUTOFRAMING:android.hardware.camera2.CaptureRequest.Key`. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_EFFECTS:android.hardware.camera2.CameraCharacteristics.Key` List of color effects for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EFFECT_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Capability](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Capability)!\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_EXTENDED_SCENE_MODE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` The list of extended scene modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EXTENDED_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device, and each extended scene mode's capabilities such as maximum streaming size, and supported zoom ratio ranges. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_MODES:android.hardware.camera2.CameraCharacteristics.Key` List of control modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_SCENE_MODES:android.hardware.camera2.CameraCharacteristics.Key` List of scene modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_SETTINGS_OVERRIDES:android.hardware.camera2.CameraCharacteristics.Key` List of available settings overrides supported by the camera device that can be used to speed up certain controls. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_VIDEO_STABILIZATION_MODES:android.hardware.camera2.CameraCharacteristics.Key` List of video stabilization modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_VIDEO_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AWB_AVAILABLE_MODES:android.hardware.camera2.CameraCharacteristics.Key` List of auto-white-balance modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AWB_LOCK_AVAILABLE:android.hardware.camera2.CameraCharacteristics.Key` Whether the camera device supports `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_LOCK:android.hardware.camera2.CaptureRequest.Key` |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Range](https://developer.android.com/reference/kotlin/android/util/Range.html#)\< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_LOW_LIGHT_BOOST_INFO_LUMINANCE_RANGE:android.hardware.camera2.CameraCharacteristics.Key` The operating luminance range of low light boost measured in lux (lx). |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_MAX_REGIONS_AE:android.hardware.camera2.CameraCharacteristics.Key` The maximum number of metering regions that can be used by the auto-exposure (AE) routine. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_MAX_REGIONS_AF:android.hardware.camera2.CameraCharacteristics.Key` The maximum number of metering regions that can be used by the auto-focus (AF) routine. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_MAX_REGIONS_AWB:android.hardware.camera2.CameraCharacteristics.Key` The maximum number of metering regions that can be used by the auto-white balance (AWB) routine. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Range](https://developer.android.com/reference/kotlin/android/util/Range.html#)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_POST_RAW_SENSITIVITY_BOOST_RANGE:android.hardware.camera2.CameraCharacteristics.Key` Range of boosts for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_POST_RAW_SENSITIVITY_BOOST:android.hardware.camera2.CaptureRequest.Key` supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Range](https://developer.android.com/reference/kotlin/android/util/Range.html#)\< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_ZOOM_RATIO_RANGE:android.hardware.camera2.CameraCharacteristics.Key` Minimum and maximum zoom ratios supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#DEPTH_DEPTH_IS_EXCLUSIVE:android.hardware.camera2.CameraCharacteristics.Key` Indicates whether a capture request may target both a DEPTH16 / DEPTH_POINT_CLOUD output, and normal color outputs (such as YUV_420_888, JPEG, or RAW) simultaneously. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#DISTORTION_CORRECTION_AVAILABLE_MODES:android.hardware.camera2.CameraCharacteristics.Key` List of distortion correction modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#EDGE_AVAILABLE_EDGE_MODES:android.hardware.camera2.CameraCharacteristics.Key` List of edge enhancement modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#EDGE_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_INFO_AVAILABLE:android.hardware.camera2.CameraCharacteristics.Key` Whether this camera device has a flash unit. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_INFO_STRENGTH_DEFAULT_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` Default flashlight brightness level to be set via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#turnOnTorchWithStrengthLevel(kotlin.String,%20kotlin.Int)`. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_INFO_STRENGTH_MAXIMUM_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` Maximum flashlight brightness level. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_SINGLE_STRENGTH_DEFAULT_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` Default flash brightness level for manual flash control in `SINGLE` mode. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_SINGLE_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` Maximum flash brightness level for manual flash control in `SINGLE` mode. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_TORCH_STRENGTH_DEFAULT_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` Default flash brightness level for manual flash control in `TORCH` mode |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_TORCH_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` Maximum flash brightness level for manual flash control in `TORCH` mode |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#HOT_PIXEL_AVAILABLE_HOT_PIXEL_MODES:android.hardware.camera2.CameraCharacteristics.Key` List of hot pixel correction modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#HOT_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [DeviceStateSensorOrientationMap](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DeviceStateSensorOrientationMap)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_DEVICE_STATE_SENSOR_ORIENTATION_MAP:android.hardware.camera2.CameraCharacteristics.Key` This lists the mapping between a device folding state and specific camera sensor orientation for logical cameras on a foldable device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_DEVICE_TYPE:android.hardware.camera2.CameraCharacteristics.Key` A classification of the underlying hardware and source of image data for this camera device, or for a specific camera output frame. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SESSION_CONFIGURATION_QUERY_VERSION:android.hardware.camera2.CameraCharacteristics.Key` The version of the session configuration query `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup#isSessionConfigurationSupported(android.hardware.camera2.params.SessionConfiguration)` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup#getSessionCharacteristics(android.hardware.camera2.params.SessionConfiguration)` APIs. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` Generally classifies the overall set of the camera device functionality. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_VERSION:android.hardware.camera2.CameraCharacteristics.Key` A short string for manufacturer version information about the camera device, such as ISP hardware, sensors, etc. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#JPEG_AVAILABLE_THUMBNAIL_SIZES:android.hardware.camera2.CameraCharacteristics.Key` List of JPEG thumbnail sizes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#JPEG_THUMBNAIL_SIZE:android.hardware.camera2.CaptureRequest.Key` supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key` The correction coefficients to correct for this camera device's radial and tangential lens distortion. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key` The correction coefficients to correct for this camera device's radial and tangential lens distortion for a CaptureRequest with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key` Direction the camera faces relative to device screen. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_AVAILABLE_APERTURES:android.hardware.camera2.CameraCharacteristics.Key` List of aperture size values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_APERTURE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_AVAILABLE_FILTER_DENSITIES:android.hardware.camera2.CameraCharacteristics.Key` List of neutral density filter values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FILTER_DENSITY:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_AVAILABLE_FOCAL_LENGTHS:android.hardware.camera2.CameraCharacteristics.Key` List of focal lengths for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_AVAILABLE_OPTICAL_STABILIZATION:android.hardware.camera2.CameraCharacteristics.Key` List of optical image stabilization (OIS) modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_OPTICAL_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_FOCUS_DISTANCE_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key` The lens focus distance calibration quality. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_HYPERFOCAL_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key` Hyperfocal distance for this lens. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key` Shortest distance from frontmost surface of the lens that can be brought into sharp focus. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key` The parameters for this camera device's intrinsic calibration. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INTRINSIC_CALIBRATION_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key` The parameters for this camera device's intrinsic calibration when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` is set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key` The origin for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`, and the accuracy of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key`. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key` The orientation of the camera relative to the sensor coordinate system. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` Position of the camera optical center. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_RADIAL_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key` The correction coefficients to correct for this camera device's radial and tangential lens distortion. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LOGICAL_MULTI_CAMERA_SENSOR_SYNC_TYPE:android.hardware.camera2.CameraCharacteristics.Key` The accuracy of frame timestamp synchronization between physical cameras |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#NOISE_REDUCTION_AVAILABLE_NOISE_REDUCTION_MODES:android.hardware.camera2.CameraCharacteristics.Key` List of noise reduction modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#NOISE_REDUCTION_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REPROCESS_MAX_CAPTURE_STALL:android.hardware.camera2.CameraCharacteristics.Key` The maximal camera capture pipeline stall (in unit of frame count) introduced by a reprocess capture request. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` List of capabilities that this camera device advertises as fully supporting. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [ColorSpaceProfiles](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceProfiles)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_COLOR_SPACE_PROFILES:android.hardware.camera2.CameraCharacteristics.Key` An interface for querying the color space profiles supported by a camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [DynamicRangeProfiles](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_DYNAMIC_RANGE_PROFILES:android.hardware.camera2.CameraCharacteristics.Key` Devices supporting the 10-bit output capability `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_DYNAMIC_RANGE_TEN_BIT:kotlin.Int` must list their supported dynamic range profiles along with capture request constraints for specific profile combinations. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_MAX_NUM_INPUT_STREAMS:android.hardware.camera2.CameraCharacteristics.Key` The maximum numbers of any type of input streams that can be configured and used simultaneously by a camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_MAX_NUM_OUTPUT_PROC:android.hardware.camera2.CameraCharacteristics.Key` The maximum numbers of different types of output streams that can be configured and used simultaneously by a camera device for any processed (but not-stalling) formats. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_MAX_NUM_OUTPUT_PROC_STALLING:android.hardware.camera2.CameraCharacteristics.Key` The maximum numbers of different types of output streams that can be configured and used simultaneously by a camera device for any processed (and stalling) formats. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_MAX_NUM_OUTPUT_RAW:android.hardware.camera2.CameraCharacteristics.Key` The maximum numbers of different types of output streams that can be configured and used simultaneously by a camera device for any `RAW` formats. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_PARTIAL_RESULT_COUNT:android.hardware.camera2.CameraCharacteristics.Key` Defines how many sub-components a result will be composed of. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_PIPELINE_MAX_DEPTH:android.hardware.camera2.CameraCharacteristics.Key` Specifies the number of maximum pipeline stages a frame has to go through from when it's exposed to when it's available to the framework. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_RECOMMENDED_TEN_BIT_DYNAMIC_RANGE_PROFILE:android.hardware.camera2.CameraCharacteristics.Key` Recommended 10-bit dynamic range profile. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_MAX_DIGITAL_ZOOM:android.hardware.camera2.CameraCharacteristics.Key` The maximum ratio between both active area width and crop region width, and active area height and crop region height, for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_ROTATE_AND_CROP_MODES:android.hardware.camera2.CameraCharacteristics.Key` List of rotate-and-crop modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_ROTATE_AND_CROP:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_STREAM_USE_CASES:android.hardware.camera2.CameraCharacteristics.Key` The stream use cases supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_CROPPING_TYPE:android.hardware.camera2.CameraCharacteristics.Key` The crop type that this camera device supports. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_DEFAULT_SECURE_IMAGE_SIZE:android.hardware.camera2.CameraCharacteristics.Key` Default YUV/PRIVATE size to use for requesting secure image buffers. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MandatoryStreamCombination](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination)!\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_MANDATORY_CONCURRENT_STREAM_COMBINATIONS:android.hardware.camera2.CameraCharacteristics.Key` An array of mandatory concurrent stream combinations. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MandatoryStreamCombination](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination)!\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_MANDATORY_MAXIMUM_RESOLUTION_STREAM_COMBINATIONS:android.hardware.camera2.CameraCharacteristics.Key` An array of mandatory stream combinations which are applicable when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest` has `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MandatoryStreamCombination](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination)!\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_MANDATORY_PREVIEW_STABILIZATION_OUTPUT_STREAM_COMBINATIONS:android.hardware.camera2.CameraCharacteristics.Key` An array of mandatory stream combinations which are applicable when device lists `PREVIEW_STABILIZATION` in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_VIDEO_STABILIZATION_MODES:android.hardware.camera2.CameraCharacteristics.Key`. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MandatoryStreamCombination](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination)!\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_MANDATORY_STREAM_COMBINATIONS:android.hardware.camera2.CameraCharacteristics.Key` An array of mandatory stream combinations generated according to the camera device `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MandatoryStreamCombination](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination)!\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_MANDATORY_TEN_BIT_OUTPUT_STREAM_COMBINATIONS:android.hardware.camera2.CameraCharacteristics.Key` An array of mandatory stream combinations which are applicable when device support the 10-bit output capability `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_DYNAMIC_RANGE_TEN_BIT:kotlin.Int` This is an app-readable conversion of the 10 bit output mandatory stream combination [tables](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#10-bit-output-additional-guaranteed-configurations). |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MandatoryStreamCombination](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination)!\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_MANDATORY_USE_CASE_STREAM_COMBINATIONS:android.hardware.camera2.CameraCharacteristics.Key` An array of mandatory stream combinations with stream use cases. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [MultiResolutionStreamConfigurationMap](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MultiResolutionStreamConfigurationMap)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_MULTI_RESOLUTION_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key` The multi-resolution stream configurations supported by this logical camera or ultra high resolution sensor camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [StreamConfigurationMap](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key` The available stream configurations that this camera device supports; also includes the minimum frame durations and the stall durations for each format/size combination. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [StreamConfigurationMap](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key` The available stream configurations that this camera device supports when given a CaptureRequest with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`; also includes the minimum frame durations and the stall durations for each format/size combination. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_AVAILABLE_TEST_PATTERN_MODES:android.hardware.camera2.CameraCharacteristics.Key` List of sensor test pattern modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_TEST_PATTERN_MODE:android.hardware.camera2.CaptureRequest.Key` supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [BlackLevelPattern](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/BlackLevelPattern)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_BLACK_LEVEL_PATTERN:android.hardware.camera2.CameraCharacteristics.Key` A fixed black level offset for each of the color filter arrangement (CFA) mosaic channels. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [ColorSpaceTransform](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_CALIBRATION_TRANSFORM1:android.hardware.camera2.CameraCharacteristics.Key` A per-device calibration transform matrix that maps from the reference sensor colorspace to the actual device sensor colorspace. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [ColorSpaceTransform](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_CALIBRATION_TRANSFORM2:android.hardware.camera2.CameraCharacteristics.Key` A per-device calibration transform matrix that maps from the reference sensor colorspace to the actual device sensor colorspace (this is the colorspace of the raw buffer data). |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [ColorSpaceTransform](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_COLOR_TRANSFORM1:android.hardware.camera2.CameraCharacteristics.Key` A matrix that transforms color values from CIE XYZ color space to reference sensor color space. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [ColorSpaceTransform](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_COLOR_TRANSFORM2:android.hardware.camera2.CameraCharacteristics.Key` A matrix that transforms color values from CIE XYZ color space to reference sensor color space. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [ColorSpaceTransform](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_FORWARD_MATRIX1:android.hardware.camera2.CameraCharacteristics.Key` A matrix that transforms white balanced camera colors from the reference sensor colorspace to the CIE XYZ colorspace with a D50 whitepoint. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [ColorSpaceTransform](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_FORWARD_MATRIX2:android.hardware.camera2.CameraCharacteristics.Key` A matrix that transforms white balanced camera colors from the reference sensor colorspace to the CIE XYZ colorspace with a D50 whitepoint. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` The area of the image sensor which corresponds to active pixels after any geometric distortion correction has been applied. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key` The area of the image sensor which corresponds to active pixels after any geometric distortion correction has been applied, when the sensor runs in maximum resolution mode. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_BINNING_FACTOR:android.hardware.camera2.CameraCharacteristics.Key` Dimensions of the group of pixels which are under the same color filter. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT:android.hardware.camera2.CameraCharacteristics.Key` The arrangement of color filters on sensor; represents the colors in the top-left 2x2 section of the sensor, in reading order, for a Bayer camera, or the light spectrum it captures for MONOCHROME camera. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Range](https://developer.android.com/reference/kotlin/android/util/Range.html#)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_EXPOSURE_TIME_RANGE:android.hardware.camera2.CameraCharacteristics.Key` The range of image exposure times for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key` supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_LENS_SHADING_APPLIED:android.hardware.camera2.CameraCharacteristics.Key` Whether the RAW images output from this camera device are subject to lens shading correction. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_MAX_FRAME_DURATION:android.hardware.camera2.CameraCharacteristics.Key` The maximum possible frame duration (minimum frame rate) for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` that is supported this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [SizeF](https://developer.android.com/reference/kotlin/android/util/SizeF.html#)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PHYSICAL_SIZE:android.hardware.camera2.CameraCharacteristics.Key` The physical dimensions of the full pixel array. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PIXEL_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` Dimensions of the full pixel array, possibly including black calibration pixels. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PIXEL_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key` Dimensions of the full pixel array, possibly including black calibration pixels, when the sensor runs in maximum resolution mode. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` The area of the image sensor which corresponds to active pixels prior to the application of any geometric distortion correction. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key` The area of the image sensor which corresponds to active pixels prior to the application of any geometric distortion correction, when the sensor runs in maximum resolution mode. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Range](https://developer.android.com/reference/kotlin/android/util/Range.html#)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_SENSITIVITY_RANGE:android.hardware.camera2.CameraCharacteristics.Key` Range of sensitivities for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key` supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_TIMESTAMP_SOURCE:android.hardware.camera2.CameraCharacteristics.Key` The time base source for sensor capture start timestamps. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_WHITE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` Maximum raw value output by sensor. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_MAX_ANALOG_SENSITIVITY:android.hardware.camera2.CameraCharacteristics.Key` Maximum sensitivity that is implemented purely through analog gain. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!\>!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_OPTICAL_BLACK_REGIONS:android.hardware.camera2.CameraCharacteristics.Key` List of disjoint rectangles indicating the sensor optically shielded black pixel regions. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_ORIENTATION:android.hardware.camera2.CameraCharacteristics.Key` Clockwise angle through which the output image needs to be rotated to be upright on the device screen in its native orientation. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_READOUT_TIMESTAMP:android.hardware.camera2.CameraCharacteristics.Key` Whether or not the camera device supports readout timestamp and `onReadoutStarted` callback. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key` The standard reference illuminant used as the scene light source when calculating the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_COLOR_TRANSFORM1:android.hardware.camera2.CameraCharacteristics.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_CALIBRATION_TRANSFORM1:android.hardware.camera2.CameraCharacteristics.Key`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_FORWARD_MATRIX1:android.hardware.camera2.CameraCharacteristics.Key` matrices. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT2:android.hardware.camera2.CameraCharacteristics.Key` The standard reference illuminant used as the scene light source when calculating the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_COLOR_TRANSFORM2:android.hardware.camera2.CameraCharacteristics.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_CALIBRATION_TRANSFORM2:android.hardware.camera2.CameraCharacteristics.Key`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_FORWARD_MATRIX2:android.hardware.camera2.CameraCharacteristics.Key` matrices. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SHADING_AVAILABLE_MODES:android.hardware.camera2.CameraCharacteristics.Key` List of lens shading modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SHADING_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#STATISTICS_INFO_AVAILABLE_FACE_DETECT_MODES:android.hardware.camera2.CameraCharacteristics.Key` List of face detection modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_FACE_DETECT_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#STATISTICS_INFO_AVAILABLE_HOT_PIXEL_MAP_MODES:android.hardware.camera2.CameraCharacteristics.Key` List of hot pixel map output modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_HOT_PIXEL_MAP_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#STATISTICS_INFO_AVAILABLE_LENS_SHADING_MAP_MODES:android.hardware.camera2.CameraCharacteristics.Key` List of lens shading map output modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_LENS_SHADING_MAP_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#STATISTICS_INFO_AVAILABLE_OIS_DATA_MODES:android.hardware.camera2.CameraCharacteristics.Key` List of OIS data output modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_OIS_DATA_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#STATISTICS_INFO_MAX_FACE_COUNT:android.hardware.camera2.CameraCharacteristics.Key` The maximum number of simultaneously detectable faces. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SYNC_MAX_LATENCY:android.hardware.camera2.CameraCharacteristics.Key` The maximum number of frames that can occur after a request (different than the previous) has been submitted, and before the result's state becomes synchronized. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#TONEMAP_AVAILABLE_TONE_MAP_MODES:android.hardware.camera2.CameraCharacteristics.Key` List of tonemapping modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device. |
| static [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#TONEMAP_MAX_CURVE_POINTS:android.hardware.camera2.CameraCharacteristics.Key` Maximum number of supported points in the tonemap curve that can be used for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_CURVE:android.hardware.camera2.CaptureRequest.Key`. |

## Public methods

### get

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : Any!> get(key: CameraCharacteristics.Key<T>!): T?
```

Get a camera characteristics field value.

The field definitions can be found in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#`.

| Parameters ||
|---|---|
| `key` | [CameraCharacteristics.Key](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key)\<T\>!: The characteristics field to read. |

| Return ||
|---|---|
| `T?` | The value of that key, or `null` if the field is not set. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the key was not valid |

### getAvailableCaptureRequestKeys

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAvailableCaptureRequestKeys(): MutableList<CaptureRequest.Key<*>!>
```

Returns the list of keys supported by this `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice` for querying with a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest`.

The list returned is not modifiable, so any attempts to modify it will throw a `UnsupportedOperationException`.

Each key is only listed once in the list. The order of the keys is undefined.

Note that there is no `getAvailableCameraCharacteristicsKeys()` -- use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getKeys()` instead.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Key<*>!>` | List of keys supported by this CameraDevice for CaptureRequests. This value cannot be `null`. |

### getAvailableCaptureResultKeys

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAvailableCaptureResultKeys(): MutableList<CaptureResult.Key<*>!>
```

Returns the list of keys supported by this `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice` for querying with a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult`.

The list returned is not modifiable, so any attempts to modify it will throw a `UnsupportedOperationException`.

Each key is only listed once in the list. The order of the keys is undefined.

Note that there is no `getAvailableCameraCharacteristicsKeys()` -- use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getKeys()` instead.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult.Key<*>!>` | List of keys supported by this CameraDevice for CaptureResults. This value cannot be `null`. |

### getAvailablePhysicalCameraRequestKeys

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAvailablePhysicalCameraRequestKeys(): MutableList<CaptureRequest.Key<*>!>!
```

Returns a subset of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getAvailableCaptureRequestKeys()` keys that can be overridden for physical devices backing a logical multi-camera.

This is a subset of android.request.availableRequestKeys which contains a list of keys that can be overridden using `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder#setPhysicalCameraKey(android.hardware.camera2.CaptureRequest.Key,%20android.hardware.camera2.CaptureRequest.Builder.setPhysicalCameraKey.T,%20kotlin.String)`. The respective value of such request key can be obtained by calling `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder#getPhysicalCameraKey(android.hardware.camera2.CaptureRequest.Key,%20kotlin.String)`. Capture requests that contain individual physical device requests must be built via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createCaptureRequest(kotlin.Int,%20kotlin.collections.MutableSet)`.

The list returned is not modifiable, so any attempts to modify it will throw a `UnsupportedOperationException`.

Each key is only listed once in the list. The order of the keys is undefined.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Key<*>!>!` | List of keys that can be overridden in individual physical device requests. In case the camera device doesn't support such keys the list can be null. |

### getAvailableSessionCharacteristicsKeys

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAvailableSessionCharacteristicsKeys(): MutableList<CameraCharacteristics.Key<*>!>
```

Get the keys in Camera Characteristics whose values are capture session specific. The session specific characteristics can be acquired by calling CameraDevice.getSessionCharacteristics().

Note that getAvailableSessionKeys returns the CaptureRequest keys that are difficult to apply per-frame, whereas this function returns CameraCharacteristics keys that are dependent on a particular SessionConfiguration.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key<*>!>` | List of CameraCharacteristic keys containing characterisitics specific to a session configuration. If `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SESSION_CONFIGURATION_QUERY_VERSION:android.hardware.camera2.CameraCharacteristics.Key` is at least `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`, then this list will only contain CONTROL_ZOOM_RATIO_RANGE and SCALER_AVAILABLE_MAX_DIGITAL_ZOOM. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SESSION_CONFIGURATION_QUERY_VERSION:android.hardware.camera2.CameraCharacteristics.Key`

### getAvailableSessionKeys

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAvailableSessionKeys(): MutableList<CaptureRequest.Key<*>!>!
```

Returns a subset of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getAvailableCaptureRequestKeys()` keys that the camera device can pass as part of the capture session initialization.

This list includes keys that are difficult to apply per-frame and can result in unexpected delays when modified during the capture session lifetime. Typical examples include parameters that require a time-consuming hardware re-configuration or internal camera pipeline change. For performance reasons we suggest clients to pass their initial values as part of `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setSessionParameters(android.hardware.camera2.CaptureRequest)`. Once the camera capture session is enabled it is also recommended to avoid changing them from their initial values set in `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setSessionParameters(android.hardware.camera2.CaptureRequest)`. Control over session parameters can still be exerted in capture requests but clients should be aware and expect delays during their application. An example usage scenario could look like this:

- The camera client starts by querying the session parameter key list via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getAvailableSessionKeys()`.
- Before triggering the capture session create sequence, a capture request must be built via android.hardware.camera2.CameraDevice#createCaptureRequest using an appropriate template matching the particular use case.
- The client should go over the list of session parameters and check whether some of the keys listed matches with the parameters that they intend to modify as part of the first capture request.
- If there is no such match, the capture request can be passed unmodified to `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setSessionParameters(android.hardware.camera2.CaptureRequest)`.
- If matches do exist, the client should update the respective values and pass the request to `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setSessionParameters(android.hardware.camera2.CaptureRequest)`.
- After the capture session initialization completes the session parameter key list can continue to serve as reference when posting or updating further requests. As mentioned above further changes to session parameters should ideally be avoided, if updates are necessary however clients could expect a delay/glitch during the parameter switch.

The list returned is not modifiable, so any attempts to modify it will throw a `UnsupportedOperationException`.

Each key is only listed once in the list. The order of the keys is undefined.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Key<*>!>!` | List of keys that can be passed during capture session initialization. In case the camera device doesn't support such keys the list can be null. |

### getKeys

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKeys(): MutableList<CameraCharacteristics.Key<*>!>
```

Returns a list of the keys contained in this map.

The list returned is not modifiable, so any attempts to modify it will throw a `UnsupportedOperationException`.

All values retrieved by a key from this list with `get` are guaranteed to be non-`null`. Each key is only listed once in the list. The order of the keys is undefined.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key<*>!>` | This value cannot be `null`. |

### getKeysNeedingPermission

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKeysNeedingPermission(): MutableList<CameraCharacteristics.Key<*>!>
```

Returns a subset of the list returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getKeys()` with all keys that require camera clients to obtain the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` permission.

If an application calls `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraCharacteristics(kotlin.String)` without holding the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` permission, all keys in this list will not be available, and calling `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#get(android.hardware.camera2.CameraCharacteristics.Key)` will return null for those keys. If the application obtains the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` permission, then the CameraCharacteristics from a call to a subsequent `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraCharacteristics(kotlin.String)` will have the keys available.

The list returned is not modifiable, so any attempts to modify it will throw a `UnsupportedOperationException`.

Each key is only listed once in the list. The order of the keys is undefined.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.Key<*>!>` | List of camera characteristic keys that require the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` permission. The list can be empty in case there are no currently present keys that need additional permission. |

### getPhysicalCameraIds

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPhysicalCameraIds(): MutableSet<String!>
```

Returns the set of physical camera ids that this logical `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice` is made up of.

A camera device is a logical camera if it has REQUEST_AVAILABLE_CAPABILITIES_LOGICAL_MULTI_CAMERA capability. If the camera device doesn't have the capability, the return value will be an empty set.

Prior to API level 29, all returned IDs are guaranteed to be returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList()`, and can be opened directly by android.hardware.camera2.CameraManager#openCamera. Starting from API level 29, for each of the returned ID, if it's also returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList()`, it can be used as a standalone camera by android.hardware.camera2.CameraManager#openCamera. Otherwise, the camera ID can only be used as part of the current logical camera.

The set returned is not modifiable, so any attempts to modify it will throw a `UnsupportedOperationException`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | Set of physical camera ids for this logical camera device. This value cannot be `null`. |

### getRecommendedStreamConfigurationMap

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRecommendedStreamConfigurationMap(usecase: Int): RecommendedStreamConfigurationMap?
```

Retrieve camera device recommended stream configuration map `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap` for a given use case.

The stream configurations advertised here are efficient in terms of power and performance for common use cases like preview, video, snapshot, etc. The recommended maps are usually only small subsets of the exhaustive list provided in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key` and suggested for a particular use case by the camera device implementation. For further information about the expected configurations in various scenarios please refer to:

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_PREVIEW:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_RECORD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_VIDEO_SNAPSHOT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_SNAPSHOT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_RAW:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_ZSL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_LOW_LATENCY_SNAPSHOT:kotlin.Int`

<br />

For example on how this can be used by camera clients to find out the maximum recommended preview and snapshot resolution, consider the following pseudo-code:

```kotlin
<code>
  public static Size getMaxSize(Size... sizes) {
      if (sizes == null || sizes.length == 0) {
          throw new IllegalArgumentException("sizes was empty");
      }
 
      Size sz = sizes[0];
      for (Size size : sizes) {
          if (size.getWidth() * size.getHeight() &gt; sz.getWidth() * sz.getHeight()) {
              sz = size;
          }
      }
 
      return sz;
  }
 
  CameraCharacteristics characteristics =
          cameraManager.getCameraCharacteristics(cameraId);
  RecommendedStreamConfigurationMap previewConfig =
          characteristics.getRecommendedStreamConfigurationMap(
                   RecommendedStreamConfigurationMap.USECASE_PREVIEW);
  RecommendedStreamConfigurationMap snapshotConfig =
          characteristics.getRecommendedStreamConfigurationMap(
                   RecommendedStreamConfigurationMap.USECASE_SNAPSHOT);
 
  if ((previewConfig != null) &amp;&amp; (snapshotConfig != null)) {
 
       Set
 <size>
   snapshotSizeSet = snapshotConfig.getOutputSizes( ImageFormat.JPEG); Size[] snapshotSizes = new Size[snapshotSizeSet.size()]; snapshotSizes = snapshotSizeSet.toArray(snapshotSizes); Size suggestedMaxJpegSize = getMaxSize(snapshotSizes); Set
  <size>
    previewSizeSet = snapshotConfig.getOutputSizes( ImageFormat.PRIVATE); Size[] previewSizes = new Size[previewSizeSet.size()]; previewSizes = previewSizeSet.toArray(previewSizes); Size suggestedMaxPreviewSize = getMaxSize(previewSizes); } 
  </size>
 </size></code>
```

Similar logic can be used for other use cases as well.

Support for recommended stream configurations is optional. In case there a no suggested configurations for the particular use case, please refer to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key` for the exhaustive available list.

| Parameters ||
|---|---|
| `usecase` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Use case id. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_PREVIEW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_RECORD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_VIDEO_SNAPSHOT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_SNAPSHOT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_ZSL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_RAW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_LOW_LATENCY_SNAPSHOT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap#USECASE_10BIT_OUTPUT:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap?` | Valid `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap` or null in case the camera device doesn't have any recommendation for this use case or the recommended configurations are invalid. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | In case the use case argument is invalid. |

## Properties

### AUTOMOTIVE_LENS_FACING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LENS_FACING: CameraCharacteristics.Key<IntArray!>
```

The direction of the camera faces relative to the vehicle body frame and the passenger seats.

This enum defines the lens facing characteristic of the cameras on the automotive devices with locations `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LOCATION:android.hardware.camera2.CameraCharacteristics.Key` defines. If the system has FEATURE_AUTOMOTIVE, the camera will have this entry in its static metadata.

When `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LOCATION:android.hardware.camera2.CameraCharacteristics.Key` is INTERIOR, this has one or more INTERIOR_\* values or a single EXTERIOR_\* value. When this has more than one INTERIOR_\*, the first value must be the one for the seat closest to the optical axis. If this contains INTERIOR_OTHER, all other values will be ineffective.

When `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LOCATION:android.hardware.camera2.CameraCharacteristics.Key` is EXTERIOR_\* or EXTRA, this has a single EXTERIOR_\* value.

If a camera has INTERIOR_OTHER or EXTERIOR_OTHER, or more than one camera is at the same location and facing the same direction, their static metadata will list the following entries, so that applications can determine their lenses' exact facing directions:

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_OTHER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_FRONT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_REAR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_LEFT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_RIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_OTHER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_1_LEFT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_1_CENTER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_1_RIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_2_LEFT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_2_CENTER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_2_RIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_3_LEFT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_3_CENTER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_3_RIGHT:kotlin.Int`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LOCATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_OTHER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_FRONT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_REAR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_LEFT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_RIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_OTHER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_1_LEFT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_1_CENTER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_1_RIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_2_LEFT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_2_CENTER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_2_RIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_3_LEFT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_3_CENTER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_3_RIGHT:kotlin.Int`

### AUTOMOTIVE_LOCATION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LOCATION: CameraCharacteristics.Key<Int!>
```

Location of the cameras on the automotive devices.

This enum defines the locations of the cameras relative to the vehicle body frame on [the automotive sensor coordinate system](https://source.android.com/devices/sensors/sensor-types#auto_axes). If the system has FEATURE_AUTOMOTIVE, the camera will have this entry in its static metadata.

- INTERIOR is the inside of the vehicle body frame (or the passenger cabin).
- EXTERIOR is the outside of the vehicle body frame.
- EXTRA is the extra vehicle such as a trailer.

Each side of the vehicle body frame on this coordinate system is defined as below:

- FRONT is where the Y-axis increases toward.
- REAR is where the Y-axis decreases toward.
- LEFT is where the X-axis decreases toward.
- RIGHT is where the X-axis increases toward.

If the camera has either EXTERIOR_OTHER or EXTRA_OTHER, its static metadata will list the following entries, so that applications can determine the camera's exact location:

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_INTERIOR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_OTHER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_FRONT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_REAR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_LEFT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_RIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_OTHER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_FRONT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_REAR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_LEFT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_RIGHT:kotlin.Int`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_INTERIOR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_OTHER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_FRONT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_REAR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_LEFT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_RIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_OTHER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_FRONT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_REAR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_LEFT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_RIGHT:kotlin.Int`

### COLOR_CORRECTION_AVAILABLE_ABERRATION_MODES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_CORRECTION_AVAILABLE_ABERRATION_MODES: CameraCharacteristics.Key<IntArray!>
```

List of aberration correction modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_ABERRATION_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

This key lists the valid modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_ABERRATION_MODE:android.hardware.camera2.CaptureRequest.Key`. If no aberration correction modes are available for a device, this list will solely include OFF mode. All camera devices will support either OFF or FAST mode.

Camera devices that support the MANUAL_POST_PROCESSING capability will always list OFF mode. This includes all FULL level devices.

LEGACY devices will always only support FAST mode.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_ABERRATION_MODE:android.hardware.camera2.CaptureRequest.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_ABERRATION_MODE:android.hardware.camera2.CaptureRequest.Key`

### COLOR_CORRECTION_AVAILABLE_MODES

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_CORRECTION_AVAILABLE_MODES: CameraCharacteristics.Key<IntArray!>
```

List of color correction modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

This key lists the valid modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`. If no color correction modes are available for a device, this key will be null.

Camera devices that have a FULL hardware level will always include at least FAST, HIGH_QUALITY, and TRANSFORM_MATRIX modes.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`

### COLOR_CORRECTION_COLOR_TEMPERATURE_RANGE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_CORRECTION_COLOR_TEMPERATURE_RANGE: CameraCharacteristics.Key<Range<Int!>!>
```

The range of supported color temperature values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_COLOR_TEMPERATURE:android.hardware.camera2.CaptureRequest.Key`.

This key lists the valid range of color temperature values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_COLOR_TEMPERATURE:android.hardware.camera2.CaptureRequest.Key` supported by this camera device.

This key will be null on devices that do not support CCT mode for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`.

**Range of valid values:** 

The minimum supported range will be \[2856K,6500K\]. The maximum supported range will be \[1000K,40000K\].

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_COLOR_TEMPERATURE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_AVAILABLE_ANTIBANDING_MODES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_AVAILABLE_ANTIBANDING_MODES: CameraCharacteristics.Key<IntArray!>
```

List of auto-exposure antibanding modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_ANTIBANDING_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

Not all of the auto-exposure anti-banding modes may be supported by a given camera device. This field lists the valid anti-banding modes that the application may request for this camera device with the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_ANTIBANDING_MODE:android.hardware.camera2.CaptureRequest.Key` control.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_ANTIBANDING_MODE:android.hardware.camera2.CaptureRequest.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_ANTIBANDING_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_AVAILABLE_MODES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_AVAILABLE_MODES: CameraCharacteristics.Key<IntArray!>
```

List of auto-exposure modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

Not all the auto-exposure modes may be supported by a given camera device, especially if no flash unit is available. This entry lists the valid modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key` for this camera device.

All camera devices support ON, and all camera devices with flash units support ON_AUTO_FLASH and ON_ALWAYS_FLASH.

FULL mode camera devices always support OFF mode, which enables application control of camera exposure time, sensitivity, and frame duration.

LEGACY mode camera devices never support OFF mode. LIMITED mode devices support OFF if they support the MANUAL_SENSOR capability.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_AVAILABLE_PRIORITY_MODES

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_AVAILABLE_PRIORITY_MODES: CameraCharacteristics.Key<IntArray!>
```

List of auto-exposure priority modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRIORITY_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

This entry lists the valid modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRIORITY_MODE:android.hardware.camera2.CaptureRequest.Key` for this camera device. If no AE priority modes are available for a device, this will only list OFF.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRIORITY_MODE:android.hardware.camera2.CaptureRequest.Key`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRIORITY_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_AVAILABLE_TARGET_FPS_RANGES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_AVAILABLE_TARGET_FPS_RANGES: CameraCharacteristics.Key<Array<Range<Int!>!>!>
```

List of frame rate ranges for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key` supported by this camera device.

For devices at the LEGACY level or above:

- For constant-framerate recording, for each normal `https://developer.android.com/reference/kotlin/android/media/CamcorderProfile.html#`, that is, a `https://developer.android.com/reference/kotlin/android/media/CamcorderProfile.html#` that has `https://developer.android.com/reference/kotlin/android/media/CamcorderProfile.html#quality:kotlin.Int` in the range \[`https://developer.android.com/reference/kotlin/android/media/CamcorderProfile.html#QUALITY_LOW:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/CamcorderProfile.html#QUALITY_2160P:kotlin.Int`\], if the profile is supported by the device and has `https://developer.android.com/reference/kotlin/android/media/CamcorderProfile.html#videoFrameRate:kotlin.Int` `x`, this list will always include (`x`,`x`).

- Also, a camera device must either not support any `https://developer.android.com/reference/kotlin/android/media/CamcorderProfile.html#`, or support at least one normal `https://developer.android.com/reference/kotlin/android/media/CamcorderProfile.html#` that has `https://developer.android.com/reference/kotlin/android/media/CamcorderProfile.html#videoFrameRate:kotlin.Int` `x` \>= 24.

For devices at the LIMITED level or above:

- For devices that advertise NIR color filter arrangement in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT:android.hardware.camera2.CameraCharacteristics.Key`, this list will always include (`max`, `max`) where `max` = the maximum output frame rate of the maximum YUV_420_888 output size.
- For devices advertising any color filter arrangement other than NIR, or devices not advertising color filter arrangement, this list will always include (`min`, `max`) and (`max`, `max`) where `min` \<= 15 and `max` = the maximum output frame rate of the maximum YUV_420_888 output size.

**Units**: Frames per second (FPS)

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT:android.hardware.camera2.CameraCharacteristics.Key`

### CONTROL_AE_COMPENSATION_RANGE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_COMPENSATION_RANGE: CameraCharacteristics.Key<Range<Int!>!>
```

Maximum and minimum exposure compensation values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_EXPOSURE_COMPENSATION:android.hardware.camera2.CaptureRequest.Key`, in counts of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_COMPENSATION_STEP:android.hardware.camera2.CameraCharacteristics.Key`, that are supported by this camera device.

**Range of valid values:** 

Range \[0,0\] indicates that exposure compensation is not supported.

For LIMITED and FULL devices, range must follow below requirements if exposure compensation is supported (`range != [0, 0]`):

``Min.exposure compensation * `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_COMPENSATION_STEP:android.hardware.camera2.CameraCharacteristics.Key` <= -2 EV``

``Max.exposure compensation * `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_COMPENSATION_STEP:android.hardware.camera2.CameraCharacteristics.Key` >= 2 EV``

LEGACY devices may support a smaller range than this.

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_COMPENSATION_STEP:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_EXPOSURE_COMPENSATION:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_COMPENSATION_STEP

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_COMPENSATION_STEP: CameraCharacteristics.Key<Rational!>
```

Smallest step by which the exposure compensation can be changed.

This is the unit for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_EXPOSURE_COMPENSATION:android.hardware.camera2.CaptureRequest.Key`. For example, if this key has a value of `1/2`, then a setting of `-2` for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_EXPOSURE_COMPENSATION:android.hardware.camera2.CaptureRequest.Key` means that the target EV offset for the auto-exposure routine is -1 EV.

One unit of EV compensation changes the brightness of the captured image by a factor of two. +1 EV doubles the image brightness, while -1 EV halves the image brightness.

**Units**: Exposure Value (EV)

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_EXPOSURE_COMPENSATION:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_LOCK_AVAILABLE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_LOCK_AVAILABLE: CameraCharacteristics.Key<Boolean!>
```

Whether the camera device supports `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_LOCK:android.hardware.camera2.CaptureRequest.Key`

Devices with MANUAL_SENSOR capability or BURST_CAPTURE capability will always list `true`. This includes FULL devices.

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_LOCK:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AF_AVAILABLE_MODES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AF_AVAILABLE_MODES: CameraCharacteristics.Key<IntArray!>
```

List of auto-focus (AF) modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

Not all the auto-focus modes may be supported by a given camera device. This entry lists the valid modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key` for this camera device.

All LIMITED and FULL mode camera devices will support OFF mode, and all camera devices with adjustable focuser units (`` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key` > 0 ``) will support AUTO mode.

LEGACY devices will support OFF mode only if they support focusing to infinity (by also setting `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key` to `0.0f`).

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key`

### CONTROL_AUTOFRAMING_AVAILABLE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AUTOFRAMING_AVAILABLE: CameraCharacteristics.Key<Boolean!>
```

Whether the camera device supports `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AUTOFRAMING:android.hardware.camera2.CaptureRequest.Key`.

Will be `false` if auto-framing is not available.

**Optional** - The value for this key may be `null` on some devices.

**Limited capability** - Present on all camera devices that report being at least `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AUTOFRAMING:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`

### CONTROL_AVAILABLE_EFFECTS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AVAILABLE_EFFECTS: CameraCharacteristics.Key<IntArray!>
```

List of color effects for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EFFECT_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

This list contains the color effect modes that can be applied to images produced by the camera device. Implementations are not expected to be consistent across all devices. If no color effect modes are available for a device, this will only list OFF.

A color effect will only be applied if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` != OFF. OFF is always included in this list.

This control has no effect on the operation of other control routines such as auto-exposure, white balance, or focus.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EFFECT_MODE:android.hardware.camera2.CaptureRequest.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EFFECT_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AVAILABLE_EXTENDED_SCENE_MODE_CAPABILITIES

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AVAILABLE_EXTENDED_SCENE_MODE_CAPABILITIES: CameraCharacteristics.Key<Array<Capability!>!>
```

The list of extended scene modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EXTENDED_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device, and each extended scene mode's capabilities such as maximum streaming size, and supported zoom ratio ranges.

For DISABLED mode, the camera behaves normally with no extended scene mode enabled.

For BOKEH_STILL_CAPTURE mode, the maximum streaming dimension specifies the limit under which bokeh is effective when capture intent is PREVIEW. Note that when capture intent is PREVIEW, the bokeh effect may not be as high quality compared to STILL_CAPTURE intent in order to maintain reasonable frame rate. The maximum streaming dimension must be one of the YUV_420_888 or PRIVATE resolutions in availableStreamConfigurations, or (0, 0) if preview bokeh is not supported. If the application configures a stream larger than the maximum streaming dimension, bokeh effect may not be applied for this stream for PREVIEW intent.

For BOKEH_CONTINUOUS mode, the maximum streaming dimension specifies the limit under which bokeh is effective. This dimension must be one of the YUV_420_888 or PRIVATE resolutions in availableStreamConfigurations, and if the sensor maximum resolution is larger than or equal to 1080p, the maximum streaming dimension must be at least 1080p. If the application configures a stream with larger dimension, the stream may not have bokeh effect applied.

When extended scene mode is set, the camera device may have limited range of zoom ratios compared to when the mode is DISABLED. availableExtendedSceneModeCapabilities lists the zoom ranges for all supported extended modes. A range of (1.0, 1.0) means that no zoom (optical or digital) is supported.

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EXTENDED_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AVAILABLE_MODES

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AVAILABLE_MODES: CameraCharacteristics.Key<IntArray!>
```

List of control modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

This list contains control modes that can be set for the camera device. LEGACY mode devices will always support AUTO mode. LIMITED and FULL devices will always support OFF, AUTO modes.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AVAILABLE_SCENE_MODES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AVAILABLE_SCENE_MODES: CameraCharacteristics.Key<IntArray!>
```

List of scene modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

This list contains scene modes that can be set for the camera device. Only scene modes that have been fully implemented for the camera device may be included here. Implementations are not expected to be consistent across all devices.

If no scene modes are supported by the camera device, this will be set to DISABLED. Otherwise DISABLED will not be listed.

FACE_PRIORITY is always listed if face detection is supported (i.e.`` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#STATISTICS_INFO_MAX_FACE_COUNT:android.hardware.camera2.CameraCharacteristics.Key` > 0 ``).

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#STATISTICS_INFO_MAX_FACE_COUNT:android.hardware.camera2.CameraCharacteristics.Key`

### CONTROL_AVAILABLE_SETTINGS_OVERRIDES

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AVAILABLE_SETTINGS_OVERRIDES: CameraCharacteristics.Key<IntArray!>
```

List of available settings overrides supported by the camera device that can be used to speed up certain controls.

When not all controls within a CaptureRequest are required to take effect at the same time on the outputs, the camera device may apply certain request keys sooner to improve latency. This list contains such supported settings overrides. Each settings override corresponds to a set of CaptureRequest keys that can be sped up when applying.

A supported settings override can be passed in via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SETTINGS_OVERRIDE:android.hardware.camera2.CaptureRequest.Key`, and the CaptureRequest keys corresponding to the override are applied as soon as possible, not bound by per-frame synchronization. See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SETTINGS_OVERRIDE:android.hardware.camera2.CaptureRequest.Key` for the CaptureRequest keys for each override.

OFF is always included in this list.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SETTINGS_OVERRIDE:android.hardware.camera2.CaptureRequest.Key`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SETTINGS_OVERRIDE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AVAILABLE_VIDEO_STABILIZATION_MODES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AVAILABLE_VIDEO_STABILIZATION_MODES: CameraCharacteristics.Key<IntArray!>
```

List of video stabilization modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_VIDEO_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

OFF will always be listed.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_VIDEO_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_VIDEO_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AWB_AVAILABLE_MODES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AWB_AVAILABLE_MODES: CameraCharacteristics.Key<IntArray!>
```

List of auto-white-balance modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

Not all the auto-white-balance modes may be supported by a given camera device. This entry lists the valid modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key` for this camera device.

All camera devices will support ON mode.

Camera devices that support the MANUAL_POST_PROCESSING capability will always support OFF mode, which enables application control of white balance, by using `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key`(`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` must be set to TRANSFORM_MATRIX). This includes all FULL mode camera devices.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AWB_LOCK_AVAILABLE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AWB_LOCK_AVAILABLE: CameraCharacteristics.Key<Boolean!>
```

Whether the camera device supports `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_LOCK:android.hardware.camera2.CaptureRequest.Key`

Devices with MANUAL_POST_PROCESSING capability or BURST_CAPTURE capability will always list `true`. This includes FULL devices.

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_LOCK:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_LOW_LIGHT_BOOST_INFO_LUMINANCE_RANGE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_LOW_LIGHT_BOOST_INFO_LUMINANCE_RANGE: CameraCharacteristics.Key<Range<Float!>!>
```

The operating luminance range of low light boost measured in lux (lx).

**Range of valid values:** 

The lower bound indicates the lowest scene luminance value the AE mode 'ON_LOW_LIGHT_BOOST_BRIGHTNESS_PRIORITY' can operate within. Scenes of lower luminance than this may receive less brightening, increased noise, or artifacts.

The upper bound indicates the luminance threshold at the point when the mode is enabled. For example, 'Range\[0.3, 30.0\]' defines 0.3 lux being the lowest scene luminance the mode can reliably support. 30.0 lux represents the threshold when this mode is activated. Scenes measured at less than or equal to 30 lux will activate low light boost.

If this key is defined, then the AE mode 'ON_LOW_LIGHT_BOOST_BRIGHTNESS_PRIORITY' will also be present.

**Optional** - The value for this key may be `null` on some devices.

### CONTROL_MAX_REGIONS_AE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_MAX_REGIONS_AE: CameraCharacteristics.Key<Int!>
```

The maximum number of metering regions that can be used by the auto-exposure (AE) routine.

This corresponds to the maximum allowed number of elements in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key`.

**Range of valid values:** 
Value will be \>= 0. For FULL-capability devices, this value will be \>= 1.

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_MAX_REGIONS_AF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_MAX_REGIONS_AF: CameraCharacteristics.Key<Int!>
```

The maximum number of metering regions that can be used by the auto-focus (AF) routine.

This corresponds to the maximum allowed number of elements in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureRequest.Key`.

**Range of valid values:** 
Value will be \>= 0. For FULL-capability devices, this value will be \>= 1.

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_MAX_REGIONS_AWB

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_MAX_REGIONS_AWB: CameraCharacteristics.Key<Int!>
```

The maximum number of metering regions that can be used by the auto-white balance (AWB) routine.

This corresponds to the maximum allowed number of elements in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_REGIONS:android.hardware.camera2.CaptureRequest.Key`.

**Range of valid values:** 
Value will be \>= 0.

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_REGIONS:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_POST_RAW_SENSITIVITY_BOOST_RANGE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_POST_RAW_SENSITIVITY_BOOST_RANGE: CameraCharacteristics.Key<Range<Int!>!>
```

Range of boosts for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_POST_RAW_SENSITIVITY_BOOST:android.hardware.camera2.CaptureRequest.Key` supported by this camera device.

Devices support post RAW sensitivity boost will advertise `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_POST_RAW_SENSITIVITY_BOOST:android.hardware.camera2.CaptureRequest.Key` key for controlling post RAW sensitivity boost.

This key will be `null` for devices that do not support any RAW format outputs. For devices that do support RAW format outputs, this key will always present, and if a device does not support post RAW sensitivity boost, it will list `(100, 100)` in this key.

**Units** : ISO arithmetic units, the same as `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_POST_RAW_SENSITIVITY_BOOST:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_ZOOM_RATIO_RANGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_ZOOM_RATIO_RANGE: CameraCharacteristics.Key<Range<Float!>!>
```

Minimum and maximum zoom ratios supported by this camera device.

If the camera device supports zoom-out from 1x zoom, minZoom will be less than 1.0, and setting `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` to values less than 1.0 increases the camera's field of view.

**Units**: A pair of zoom ratio in floating-points: (minZoom, maxZoom)

**Range of valid values:** 

maxZoom \>= 1.0 \>= minZoom

**Optional** - The value for this key may be `null` on some devices.

**Limited capability** - Present on all camera devices that report being at least `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`

### DEPTH_DEPTH_IS_EXCLUSIVE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEPTH_DEPTH_IS_EXCLUSIVE: CameraCharacteristics.Key<Boolean!>
```

Indicates whether a capture request may target both a DEPTH16 / DEPTH_POINT_CLOUD output, and normal color outputs (such as YUV_420_888, JPEG, or RAW) simultaneously.

If TRUE, including both depth and color outputs in a single capture request is not supported. An application must interleave color and depth requests. If FALSE, a single request can target both types of output.

Typically, this restriction exists on camera devices that need to emit a specific pattern or wavelength of light to measure depth values, which causes the color image to be corrupted during depth measurement.

**Optional** - The value for this key may be `null` on some devices.

**Limited capability** - Present on all camera devices that report being at least `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`

### DISTORTION_CORRECTION_AVAILABLE_MODES

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISTORTION_CORRECTION_AVAILABLE_MODES: CameraCharacteristics.Key<IntArray!>
```

List of distortion correction modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

No device is required to support this API; such devices will always list only 'OFF'. All devices that support this API will list both FAST and HIGH_QUALITY.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`

### EDGE_AVAILABLE_EDGE_MODES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EDGE_AVAILABLE_EDGE_MODES: CameraCharacteristics.Key<IntArray!>
```

List of edge enhancement modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#EDGE_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

Full-capability camera devices must always support OFF; camera devices that support YUV_REPROCESSING or PRIVATE_REPROCESSING will list ZERO_SHUTTER_LAG; all devices will list FAST.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#EDGE_MODE:android.hardware.camera2.CaptureRequest.Key`

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#EDGE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`

### FLASH_INFO_AVAILABLE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLASH_INFO_AVAILABLE: CameraCharacteristics.Key<Boolean!>
```

Whether this camera device has a flash unit.

Will be `false` if no flash is available.

If there is no flash unit, none of the flash controls do anything. This key is available on all devices.

### FLASH_INFO_STRENGTH_DEFAULT_LEVEL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLASH_INFO_STRENGTH_DEFAULT_LEVEL: CameraCharacteristics.Key<Int!>
```

Default flashlight brightness level to be set via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#turnOnTorchWithStrengthLevel(kotlin.String,%20kotlin.Int)`.

If flash unit is available this will be greater than or equal to 1 and less or equal to `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_INFO_STRENGTH_MAXIMUM_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` ``.

Setting flashlight brightness above the default level (i.e.`` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_INFO_STRENGTH_DEFAULT_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` ``) may make the device more likely to reach thermal throttling conditions and slow down, or drain the battery quicker than normal. To minimize such issues, it is recommended to start the flashlight at this default brightness until a user explicitly requests a brighter level. Note that the value for this key will be null for devices with no flash unit. The default level should always be \> 0.

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_INFO_STRENGTH_DEFAULT_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_INFO_STRENGTH_MAXIMUM_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`

### FLASH_INFO_STRENGTH_MAXIMUM_LEVEL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLASH_INFO_STRENGTH_MAXIMUM_LEVEL: CameraCharacteristics.Key<Int!>
```

Maximum flashlight brightness level.

If this value is greater than 1, then the device supports controlling the flashlight brightness level via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#turnOnTorchWithStrengthLevel(kotlin.String,%20kotlin.Int)`. If this value is equal to 1, flashlight brightness control is not supported. The value for this key will be null for devices with no flash unit.

The maximum value is guaranteed to be safe to use for an indefinite duration in terms of device flashlight lifespan, but may be too bright for comfort for many use cases. Use the default torch brightness value to avoid problems with an over-bright flashlight.

**Optional** - The value for this key may be `null` on some devices.

### FLASH_SINGLE_STRENGTH_DEFAULT_LEVEL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLASH_SINGLE_STRENGTH_DEFAULT_LEVEL: CameraCharacteristics.Key<Int!>
```

Default flash brightness level for manual flash control in `SINGLE` mode.

If flash unit is available this will be greater than or equal to 1 and less or equal to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_SINGLE_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`. Note for devices that do not support the manual flash strength control feature, this level will always be equal to 1.

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_SINGLE_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`

### FLASH_SINGLE_STRENGTH_MAX_LEVEL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLASH_SINGLE_STRENGTH_MAX_LEVEL: CameraCharacteristics.Key<Int!>
```

Maximum flash brightness level for manual flash control in `SINGLE` mode.

Maximum flash brightness level in camera capture mode and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_MODE:android.hardware.camera2.CaptureRequest.Key` set to `SINGLE`. Value will be \> 1 if the manual flash strength control feature is supported, otherwise the value will be equal to 1. Note that this level is just a number of supported levels (the granularity of control). There is no actual physical power units tied to this level.

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_MODE:android.hardware.camera2.CaptureRequest.Key`

### FLASH_TORCH_STRENGTH_DEFAULT_LEVEL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLASH_TORCH_STRENGTH_DEFAULT_LEVEL: CameraCharacteristics.Key<Int!>
```

Default flash brightness level for manual flash control in `TORCH` mode

If flash unit is available this will be greater than or equal to 1 and less or equal to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_TORCH_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`. Note for the devices that do not support the manual flash strength control feature, this level will always be equal to 1.

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_TORCH_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`

### FLASH_TORCH_STRENGTH_MAX_LEVEL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLASH_TORCH_STRENGTH_MAX_LEVEL: CameraCharacteristics.Key<Int!>
```

Maximum flash brightness level for manual flash control in `TORCH` mode

Maximum flash brightness level in camera capture mode and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_MODE:android.hardware.camera2.CaptureRequest.Key` set to `TORCH`. Value will be \> 1 if the manual flash strength control feature is supported, otherwise the value will be equal to 1.

Note that this level is just a number of supported levels(the granularity of control). There is no actual physical power units tied to this level. There is no relation between `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_TORCH_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_SINGLE_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` i.e. the ratio of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_TORCH_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`:`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_SINGLE_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` is not guaranteed to be the ratio of actual brightness.

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_SINGLE_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_TORCH_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`

### HOT_PIXEL_AVAILABLE_HOT_PIXEL_MODES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HOT_PIXEL_AVAILABLE_HOT_PIXEL_MODES: CameraCharacteristics.Key<IntArray!>
```

List of hot pixel correction modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#HOT_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

FULL mode camera devices will always support FAST.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#HOT_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#HOT_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`

### INFO_DEVICE_STATE_SENSOR_ORIENTATION_MAP

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INFO_DEVICE_STATE_SENSOR_ORIENTATION_MAP: CameraCharacteristics.Key<DeviceStateSensorOrientationMap!>
```

This lists the mapping between a device folding state and specific camera sensor orientation for logical cameras on a foldable device.

Logical cameras on foldable devices can support sensors with different orientation values. The orientation value may need to change depending on the specific folding state. Information about the mapping between the device folding state and the sensor orientation can be obtained in `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DeviceStateSensorOrientationMap`. Device state orientation maps are optional and maybe present on devices that support `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_ROTATE_AND_CROP:android.hardware.camera2.CaptureRequest.Key`.

**Optional** - The value for this key may be `null` on some devices.

**Limited capability** - Present on all camera devices that report being at least `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_ROTATE_AND_CROP:android.hardware.camera2.CaptureRequest.Key`

### INFO_DEVICE_TYPE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INFO_DEVICE_TYPE: CameraCharacteristics.Key<Int!>
```

A classification of the underlying hardware and source of image data for this camera device, or for a specific camera output frame.

Historically, camera devices listed by the camera2 API could be assumed to be built-in cameras on the Android device, or in the case of the `EXTERNAL` `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` ``, USB webcams.

However, it is increasingly possible for camera devices to not be restricted to device-internal sensors and processing pipelines. Such devices can provide a wide range of useful capabilities to applications, but may also not be suitable for all camera use cases.

This key provides a basic classification of the type of camera this camera ID represents, so that applications may decide on the appropriate level of trust to extend to the image data produced by it.

Note that in some cases, it is possible for the user to swap the definition of a camera ID to a different one, such as when connecting a remote camera to act as the front camera of the device. This is normally transparent to the camera-using application to minimize user friction, but applications that care about this possibility should always verify the value of this key in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#` before opening a camera, instead of caching it, and should also watch the value of this key in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult` as well, since it may change mid-session.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_DEVICE_TYPE_BUILT_IN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_DEVICE_TYPE_EXTERNAL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_DEVICE_TYPE_VIRTUAL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_DEVICE_TYPE_UNKNOWN:kotlin.Int`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_DEVICE_TYPE_BUILT_IN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_DEVICE_TYPE_EXTERNAL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_DEVICE_TYPE_VIRTUAL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_DEVICE_TYPE_UNKNOWN:kotlin.Int`

### INFO_SESSION_CONFIGURATION_QUERY_VERSION

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INFO_SESSION_CONFIGURATION_QUERY_VERSION: CameraCharacteristics.Key<Int!>
```

The version of the session configuration query `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup#isSessionConfigurationSupported(android.hardware.camera2.params.SessionConfiguration)` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup#getSessionCharacteristics(android.hardware.camera2.params.SessionConfiguration)` APIs.

The possible values in this key correspond to the values defined in android.os.Build.VERSION_CODES. Each version defines a set of feature combinations the camera device must reliably report whether they are supported via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup#isSessionConfigurationSupported(android.hardware.camera2.params.SessionConfiguration)`. It also defines the set of session specific keys in CameraCharacteristics when returned from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup#getSessionCharacteristics(android.hardware.camera2.params.SessionConfiguration)`. The version is always less or equal to android.os.Build.VERSION.SDK_INT.

If set to UPSIDE_DOWN_CAKE, this camera device doesn't support the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup` API. Trying to create a CameraDeviceSetup instance throws an UnsupportedOperationException.

From VANILLA_ICE_CREAM onwards, the camera compliance tests verify a set of commonly used SessionConfigurations to ensure that the outputs of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup#isSessionConfigurationSupported(android.hardware.camera2.params.SessionConfiguration)` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.CameraDeviceSetup#getSessionCharacteristics(android.hardware.camera2.params.SessionConfiguration)` are accurate. The application is encouraged to use these SessionConfigurations when turning on multiple features at the same time.

When set to VANILLA_ICE_CREAM, the combinations of the following configurations are verified by the compliance tests:

- A set of commonly used stream combinations:

 | Target 1 | Size | Target 2 | Size |
 |---|---|---|---|
 | PRIV | S1080P | | |
 | PRIV | S720P | | |
 | PRIV | S1080P | JPEG/JPEG_R | MAXIMUM_16_9 |
 | PRIV | S1080P | JPEG/JPEG_R | UHD |
 | PRIV | S1080P | JPEG/JPEG_R | S1440P |
 | PRIV | S1080P | JPEG/JPEG_R | S1080P |
 | PRIV | S720P | JPEG/JPEG_R | MAXIMUM_16_9 |
 | PRIV | S720P | JPEG/JPEG_R | UHD |
 | PRIV | S720P | JPEG/JPEG_R | S1080P |
 | PRIV | XVGA | JPEG/JPEG_R | MAXIMUM_4_3 |
 | PRIV | S1080P_4_3 | JPEG/JPEG_R | MAXIMUM_4_3 |

 - `MAXIMUM_4_3` refers to the camera device's maximum output resolution with 4:3 aspect ratio for that format from `StreamConfigurationMap#getOutputSizes`.
 - `MAXIMUM_16_9` is the maximum output resolution with 16:9 aspect ratio.
 - `S1440P` refers to `2560x1440 (16:9)`.
 - `S1080P` refers to `1920x1080 (16:9)`.
 - `S720P` refers to `1280x720 (16:9)`.
 - `UHD` refers to `3840x2160 (16:9)`.
 - `XVGA` refers to `1024x768 (4:3)`.
 - `S1080P_43` refers to `1440x1080 (4:3)`.
- VIDEO_STABILIZATION_MODE: {OFF, PREVIEW}

- AE_TARGET_FPS_RANGE: { {\*, 30}, {\*, 60} }

- DYNAMIC_RANGE_PROFILE: {STANDARD, HLG10}

When set to BAKLAVA, the additional stream combinations below are verified by the compliance tests:

| Target 1 | Size | Target 2 | Size | Target 3 | Size |
|---|---|---|---|---|---|
| PRIV Preview | S1080P | PRIV Video | S1080P | | |
| PRIV Preview | S1080P | PRIV Video | S1440P | | |
| PRIV Preview | S1080P | PRIV Video | UHD | | |
| PRIV Preview | S1080P | YUV Analysis | S1080P | PRIV Video | 1080P |

- VIDEO_STABILIZATION_MODE: {OFF, ON} for the newly added stream combinations given the presence of dedicated video stream

All of the above configurations can be set up with a SessionConfiguration. The list of OutputConfiguration contains the stream configurations and DYNAMIC_RANGE_PROFILE, and the AE_TARGET_FPS_RANGE and VIDEO_STABILIZATION_MODE are set as session parameters.

This key is available on all devices.

### INFO_SUPPORTED_HARDWARE_LEVEL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INFO_SUPPORTED_HARDWARE_LEVEL: CameraCharacteristics.Key<Int!>
```

Generally classifies the overall set of the camera device functionality.

The supported hardware level is a high-level description of the camera device's capabilities, summarizing several capabilities into one field. Each level adds additional features to the previous one, and is always a strict superset of the previous level. The ordering is `LEGACY < LIMITED < FULL < LEVEL_3`.

Starting from `LEVEL_3`, the level enumerations are guaranteed to be in increasing numerical value as well. To check if a given device is at least at a given hardware level, the following code snippet can be used:

```kotlin
<code>// Returns true if the device supports the required hardware level, or better.
  boolean isHardwareLevelSupported(CameraCharacteristics c, int requiredLevel) {
      final int[] sortedHwLevels = {
          CameraCharacteristics.INFO_SUPPORTED_HARDWARE_LEVEL_LEGACY,
          CameraCharacteristics.INFO_SUPPORTED_HARDWARE_LEVEL_EXTERNAL,
          CameraCharacteristics.INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED,
          CameraCharacteristics.INFO_SUPPORTED_HARDWARE_LEVEL_FULL,
          CameraCharacteristics.INFO_SUPPORTED_HARDWARE_LEVEL_3
      };
      int deviceLevel = c.get(CameraCharacteristics.INFO_SUPPORTED_HARDWARE_LEVEL);
      if (requiredLevel == deviceLevel) {
          return true;
      }
 
      for (int sortedlevel : sortedHwLevels) {
          if (sortedlevel == requiredLevel) {
              return true;
          } else if (sortedlevel == deviceLevel) {
              return false;
          }
      }
      return false; // Should never reach here
  }
  </code>
```

At a high level, the levels are:

- `LEGACY` devices operate in a backwards-compatibility mode for older Android devices, and have very limited capabilities.
- `LIMITED` devices represent the baseline feature set, and may also include additional capabilities that are subsets of `FULL`.
- `FULL` devices additionally support per-frame manual control of sensor, flash, lens and post-processing settings, and image capture at a high rate.
- `LEVEL_3` devices additionally support YUV reprocessing and RAW image capture, along with additional output stream configurations.
- `EXTERNAL` devices are similar to `LIMITED` devices with exceptions like some sensor or lens information not reported or less stable framerates.

See the individual level enums for full descriptions of the supported capabilities. The `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` entry describes the device's capabilities at a finer-grain level, if needed. In addition, many controls have their available settings or ranges defined in individual entries from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#`.

Some features are not part of any particular hardware level or capability and must be queried separately. These include:

- Calibrated timestamps (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_TIMESTAMP_SOURCE:android.hardware.camera2.CameraCharacteristics.Key` `==` REALTIME)
- Precision lens control (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_FOCUS_DISTANCE_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key` `==` CALIBRATED)
- Face detection (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#STATISTICS_INFO_AVAILABLE_FACE_DETECT_MODES:android.hardware.camera2.CameraCharacteristics.Key`)
- Optical or electrical image stabilization (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_AVAILABLE_OPTICAL_STABILIZATION:android.hardware.camera2.CameraCharacteristics.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_VIDEO_STABILIZATION_MODES:android.hardware.camera2.CameraCharacteristics.Key`)

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LEGACY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_3:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_EXTERNAL:kotlin.Int`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_VIDEO_STABILIZATION_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_AVAILABLE_OPTICAL_STABILIZATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_FOCUS_DISTANCE_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_TIMESTAMP_SOURCE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#STATISTICS_INFO_AVAILABLE_FACE_DETECT_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LEGACY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_3:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_EXTERNAL:kotlin.Int`

### INFO_VERSION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INFO_VERSION: CameraCharacteristics.Key<String!>
```

A short string for manufacturer version information about the camera device, such as ISP hardware, sensors, etc.

This can be used in `https://developer.android.com/reference/kotlin/android/media/ExifInterface.html#TAG_IMAGE_DESCRIPTION:kotlin.String` in jpeg EXIF. This key may be absent if no version information is available on the device.

**Optional** - The value for this key may be `null` on some devices.

### JPEG_AVAILABLE_THUMBNAIL_SIZES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JPEG_AVAILABLE_THUMBNAIL_SIZES: CameraCharacteristics.Key<Array<Size!>!>
```

List of JPEG thumbnail sizes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#JPEG_THUMBNAIL_SIZE:android.hardware.camera2.CaptureRequest.Key` supported by this camera device.

This list will include at least one non-zero resolution, plus `(0,0)` for indicating no thumbnail should be generated.

Below conditions will be satisfied for this size list:

- The sizes will be sorted by increasing pixel area (width x height). If several resolutions have the same area, they will be sorted by increasing width.
- The aspect ratio of the largest thumbnail size will be same as the aspect ratio of largest JPEG output size in android.scaler.availableStreamConfigurations. The largest size is defined as the size that has the largest pixel area in a given size list.
- Each output JPEG size in android.scaler.availableStreamConfigurations will have at least one corresponding size that has the same aspect ratio in availableThumbnailSizes, and vice versa.
- All non-`(0, 0)` sizes will have non-zero widths and heights.

This list is also used as supported thumbnail sizes for HEIC image format capture.

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#JPEG_THUMBNAIL_SIZE:android.hardware.camera2.CaptureRequest.Key`

### LENS_DISTORTION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_DISTORTION: CameraCharacteristics.Key<FloatArray!>
```

The correction coefficients to correct for this camera device's radial and tangential lens distortion.

Replaces the deprecated `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_RADIAL_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key` field, which was inconsistently defined.

Three radial distortion coefficients `[kappa_1, kappa_2, kappa_3]` and two tangential distortion coefficients `[kappa_4, kappa_5]` that can be used to correct the lens's geometric distortion with the mapping equations:

```kotlin
<code> x_c = x_i * ( 1 + kappa_1 * r^2 + kappa_2 * r^4 + kappa_3 * r^6 ) +
         kappa_4 * (2 * x_i * y_i) + kappa_5 * ( r^2 + 2 * x_i^2 )
   y_c = y_i * ( 1 + kappa_1 * r^2 + kappa_2 * r^4 + kappa_3 * r^6 ) +
         kappa_5 * (2 * x_i * y_i) + kappa_4 * ( r^2 + 2 * y_i^2 )
  </code>
```

Here, `[x_c, y_c]` are the coordinates to sample in the input image that correspond to the pixel values in the corrected image at the coordinate `[x_i, y_i]`:

```kotlin
<code> correctedImage(x_i, y_i) = sample_at(x_c, y_c, inputImage)
  </code>
```

The pixel coordinates are defined in a coordinate system related to the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key` calibration fields; see that entry for details of the mapping stages. Both `[x_i, y_i]` and `[x_c, y_c]` have `(0,0)` at the lens optical center `[c_x, c_y]`, and the range of the coordinates depends on the focal length terms of the intrinsic calibration.

Finally, `r` represents the radial distance from the optical center, `r^2 = x_i^2 + y_i^2`.

The distortion model used is the Brown-Conrady model.

**Units**: Unitless coefficients.

**Optional** - The value for this key may be `null` on some devices.

**Permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` is needed to access this property**
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_RADIAL_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key`

### LENS_DISTORTION_MAXIMUM_RESOLUTION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_DISTORTION_MAXIMUM_RESOLUTION: CameraCharacteristics.Key<FloatArray!>
```

The correction coefficients to correct for this camera device's radial and tangential lens distortion for a CaptureRequest with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`.

Analogous to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key`, when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` is set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`.

**Units**: Unitless coefficients.

**Optional** - The value for this key may be `null` on some devices.

**Permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` is needed to access this property**
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`

### LENS_FACING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_FACING: CameraCharacteristics.Key<Int!>
```

Direction the camera faces relative to device screen.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_FACING_FRONT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_FACING_BACK:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_FACING_EXTERNAL:kotlin.Int`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_FACING_FRONT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_FACING_BACK:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_FACING_EXTERNAL:kotlin.Int`

### LENS_INFO_AVAILABLE_APERTURES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_INFO_AVAILABLE_APERTURES: CameraCharacteristics.Key<FloatArray!>
```

List of aperture size values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_APERTURE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

If the camera device doesn't support a variable lens aperture, this list will contain only one value, which is the fixed aperture size.

If the camera device supports a variable aperture, the aperture values in this list will be sorted in ascending order.

**Units**: The aperture f-number

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_APERTURE:android.hardware.camera2.CaptureRequest.Key`

### LENS_INFO_AVAILABLE_FILTER_DENSITIES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_INFO_AVAILABLE_FILTER_DENSITIES: CameraCharacteristics.Key<FloatArray!>
```

List of neutral density filter values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FILTER_DENSITY:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

If a neutral density filter is not supported by this camera device, this list will contain only 0. Otherwise, this list will include every filter density supported by the camera device, in ascending order.

**Units**: Exposure value (EV)

**Range of valid values:** 

Values are \>= 0

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FILTER_DENSITY:android.hardware.camera2.CaptureRequest.Key`

### LENS_INFO_AVAILABLE_FOCAL_LENGTHS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_INFO_AVAILABLE_FOCAL_LENGTHS: CameraCharacteristics.Key<FloatArray!>
```

List of focal lengths for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

In most cases this list will only contain a single value corresponding to the fixed focal length of the device. Otherwise, this list will include every focal length supported by the camera device, in ascending order.

**Units**: Millimeters

**Range of valid values:** 

Values are \> 0

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key`

### LENS_INFO_AVAILABLE_OPTICAL_STABILIZATION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_INFO_AVAILABLE_OPTICAL_STABILIZATION: CameraCharacteristics.Key<IntArray!>
```

List of optical image stabilization (OIS) modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_OPTICAL_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

If OIS is not supported by a given camera device, this list will contain only OFF.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_OPTICAL_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key`

**Optional** - The value for this key may be `null` on some devices.

**Limited capability** - Present on all camera devices that report being at least `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_OPTICAL_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key`

### LENS_INFO_FOCUS_DISTANCE_CALIBRATION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_INFO_FOCUS_DISTANCE_CALIBRATION: CameraCharacteristics.Key<Int!>
```

The lens focus distance calibration quality.

The lens focus distance calibration quality determines the reliability of focus related metadata entries, i.e. `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#LENS_FOCUS_RANGE:android.hardware.camera2.CaptureResult.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_HYPERFOCAL_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key`.

APPROXIMATE and CALIBRATED devices report the focus metadata in units of diopters (1/meter), so `0.0f` represents focusing at infinity, and increasing positive numbers represent focusing closer and closer to the camera device. The focus distance control also uses diopters on these devices.

UNCALIBRATED devices do not use units that are directly comparable to any real physical measurement, but `0.0f` still represents farthest focus, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key` represents the nearest focus the device can achieve.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_INFO_FOCUS_DISTANCE_CALIBRATION_UNCALIBRATED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_INFO_FOCUS_DISTANCE_CALIBRATION_APPROXIMATE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_INFO_FOCUS_DISTANCE_CALIBRATION_CALIBRATED:kotlin.Int`

**Optional** - The value for this key may be `null` on some devices.

**Limited capability** - Present on all camera devices that report being at least `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#LENS_FOCUS_RANGE:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_HYPERFOCAL_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_INFO_FOCUS_DISTANCE_CALIBRATION_UNCALIBRATED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_INFO_FOCUS_DISTANCE_CALIBRATION_APPROXIMATE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_INFO_FOCUS_DISTANCE_CALIBRATION_CALIBRATED:kotlin.Int`

### LENS_INFO_HYPERFOCAL_DISTANCE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_INFO_HYPERFOCAL_DISTANCE: CameraCharacteristics.Key<Float!>
```

Hyperfocal distance for this lens.

If the lens is not fixed focus, the camera device will report this field when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_FOCUS_DISTANCE_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key` is APPROXIMATE or CALIBRATED.

**Units** : See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_FOCUS_DISTANCE_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key` for details

**Range of valid values:** 
If lens is fixed focus, \>= 0. If lens has focuser unit, the value is within ``(0.0f, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key`]``

**Optional** - The value for this key may be `null` on some devices.

**Limited capability** - Present on all camera devices that report being at least `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key

**Permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` is needed to access this property**
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_FOCUS_DISTANCE_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key`

### LENS_INFO_MINIMUM_FOCUS_DISTANCE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_INFO_MINIMUM_FOCUS_DISTANCE: CameraCharacteristics.Key<Float!>
```

Shortest distance from frontmost surface of the lens that can be brought into sharp focus.

If the lens is fixed-focus, this will be 0.

**Units** : See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_FOCUS_DISTANCE_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key` for details

**Range of valid values:** 
\>= 0

**Optional** - The value for this key may be `null` on some devices.

**Limited capability** - Present on all camera devices that report being at least `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key

**Permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` is needed to access this property**
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_FOCUS_DISTANCE_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key`

### LENS_INTRINSIC_CALIBRATION

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_INTRINSIC_CALIBRATION: CameraCharacteristics.Key<FloatArray!>
```

The parameters for this camera device's intrinsic calibration.

The five calibration parameters that describe the transform from camera-centric 3D coordinates to sensor pixel coordinates:

```kotlin
<code>[f_x, f_y, c_x, c_y, s]
  </code>
```

Where `f_x` and `f_y` are the horizontal and vertical focal lengths, `[c_x, c_y]` is the position of the optical axis, and `s` is a skew parameter for the sensor plane not being aligned with the lens plane.

These are typically used within a transformation matrix K:

```kotlin
<code>K = [ f_x,   s, c_x,
         0, f_y, c_y,
         0    0,   1 ]
  </code>
```

which can then be combined with the camera pose rotation `R` and translation `t` (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`, respectively) to calculate the complete transform from world coordinates to pixel coordinates:

```kotlin
<code>P = [ K 0   * [ R -Rt
       0 1 ]      0 1 ]
  </code>
```

(Note the negation of poseTranslation when mapping from camera to world coordinates, and multiplication by the rotation).

With `p_w` being a point in the world coordinate system and `p_s` being a point in the camera active pixel array coordinate system, and with the mapping including the homogeneous division by z:

```kotlin
<code> p_h = (x_h, y_h, z_h) = P p_w
  p_s = p_h / z_h
  </code>
```

so `[x_s, y_s]` is the pixel coordinates of the world point, `z_s = 1`, and `w_s` is a measurement of disparity (depth) in pixel coordinates.

Note that the coordinate system for this transform is the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` system, where `(0,0)` is the top-left of the preCorrectionActiveArraySize rectangle. Once the pose and intrinsic calibration transforms have been applied to a world point, then the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key` transform needs to be applied, and the result adjusted to be in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` coordinate system (where `(0, 0)` is the top-left of the activeArraySize rectangle), to determine the final pixel coordinate of the world point for processed (non-RAW) output buffers.

For camera devices, the center of pixel `(x,y)` is located at coordinate `(x + 0.5, y + 0.5)`. So on a device with a precorrection active array of size `(10,10)`, the valid pixel indices go from `(0,0)-(9,9)`, and an perfectly-built camera would have an optical center at the exact center of the pixel grid, at coordinates `(5.0, 5.0)`, which is the top-left corner of pixel `(5,5)`.

**Units** : Pixels in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` coordinate system.

**Optional** - The value for this key may be `null` on some devices.

**Permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` is needed to access this property**
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`

### LENS_INTRINSIC_CALIBRATION_MAXIMUM_RESOLUTION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_INTRINSIC_CALIBRATION_MAXIMUM_RESOLUTION: CameraCharacteristics.Key<FloatArray!>
```

The parameters for this camera device's intrinsic calibration when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` is set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`.

Analogous to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key`, when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` is set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`.

**Units** : Pixels in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key` coordinate system.

**Optional** - The value for this key may be `null` on some devices.

**Permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` is needed to access this property**
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`

### LENS_POSE_REFERENCE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_POSE_REFERENCE: CameraCharacteristics.Key<Int!>
```

The origin for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`, and the accuracy of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key`.

Different calibration methods and use cases can produce better or worse results depending on the selected coordinate origin.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_POSE_REFERENCE_PRIMARY_CAMERA:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_POSE_REFERENCE_GYROSCOPE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_POSE_REFERENCE_UNDEFINED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_POSE_REFERENCE_AUTOMOTIVE:kotlin.Int`

**Optional** - The value for this key may be `null` on some devices.

**Permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` is needed to access this property**
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_POSE_REFERENCE_PRIMARY_CAMERA:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_POSE_REFERENCE_GYROSCOPE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_POSE_REFERENCE_UNDEFINED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_POSE_REFERENCE_AUTOMOTIVE:kotlin.Int`

### LENS_POSE_ROTATION

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_POSE_ROTATION: CameraCharacteristics.Key<FloatArray!>
```

The orientation of the camera relative to the sensor coordinate system.

The four coefficients that describe the quaternion rotation from the Android sensor coordinate system to a camera-aligned coordinate system where the X-axis is aligned with the long side of the image sensor, the Y-axis is aligned with the short side of the image sensor, and the Z-axis is aligned with the optical axis of the sensor.

To convert from the quaternion coefficients `(x,y,z,w)` to the axis of rotation `(a_x, a_y, a_z)` and rotation amount `theta`, the following formulas can be used:

```kotlin
<code> theta = 2 * acos(w)
  a_x = x / sin(theta/2)
  a_y = y / sin(theta/2)
  a_z = z / sin(theta/2)
  </code>
```

To create a 3x3 rotation matrix that applies the rotation defined by this quaternion, the following matrix can be used:

```kotlin
<code>R = [ 1 - 2y^2 - 2z^2,       2xy - 2zw,       2xz + 2yw,
             2xy + 2zw, 1 - 2x^2 - 2z^2,       2yz - 2xw,
             2xz - 2yw,       2yz + 2xw, 1 - 2x^2 - 2y^2 ]
  </code>
```

This matrix can then be used to apply the rotation to a column vector point with

`p' = Rp`

where `p` is in the device sensor coordinate system, and `p'` is in the camera-oriented coordinate system.

If `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key` is UNDEFINED, the quaternion rotation cannot be accurately represented by the camera device, and will be represented by default values matching its default facing.

**Units**: Quaternion coefficients

**Optional** - The value for this key may be `null` on some devices.

**Permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` is needed to access this property**
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key`

### LENS_POSE_TRANSLATION

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_POSE_TRANSLATION: CameraCharacteristics.Key<FloatArray!>
```

Position of the camera optical center.

The position of the camera device's lens optical center, as a three-dimensional vector `(x,y,z)`.

Prior to Android P, or when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key` is PRIMARY_CAMERA, this position is relative to the optical center of the largest camera device facing in the same direction as this camera, in the `https://developer.android.com/reference/kotlin/android/hardware/SensorEvent.html#`. Note that only the axis definitions are shared with the sensor coordinate system, but not the origin.

If this device is the largest or only camera device with a given facing, then this position will be `(0, 0, 0)`; a camera device with a lens optical center located 3 cm from the main sensor along the +X axis (to the right from the user's perspective) will report `(0.03, 0, 0)`. Note that this means that, for many computer vision applications, the position needs to be negated to convert it to a translation from the camera to the origin.

To transform a pixel coordinates between two cameras facing the same direction, first the source camera `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key` must be corrected for. Then the source camera `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key` needs to be applied, followed by the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key` of the source camera, the translation of the source camera relative to the destination camera, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key` of the destination camera, and finally the inverse of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key` of the destination camera. This obtains a radial-distortion-free coordinate in the destination camera pixel coordinates.

To compare this against a real image from the destination camera, the destination camera image then needs to be corrected for radial distortion before comparison or sampling.

When `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key` is GYROSCOPE, then this position is relative to the center of the primary gyroscope on the device. The axis definitions are the same as with PRIMARY_CAMERA.

When `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key` is UNDEFINED, this position cannot be accurately represented by the camera device, and will be represented as `(0, 0, 0)`.

When `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key` is AUTOMOTIVE, then this position is relative to the origin of the automotive sensor coordinate system, which is at the center of the rear axle.

**Units**: Meters

**Optional** - The value for this key may be `null` on some devices.

**Permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` is needed to access this property**
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key`

### LENS_RADIAL_DISTORTION

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_RADIAL_DISTORTION: CameraCharacteristics.Key<FloatArray!>
```

**Deprecated:**

*This field was inconsistently defined in terms of its normalization. Use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key` instead.*

<br />

The correction coefficients to correct for this camera device's radial and tangential lens distortion.

Four radial distortion coefficients `[kappa_0, kappa_1, kappa_2, kappa_3]` and two tangential distortion coefficients `[kappa_4, kappa_5]` that can be used to correct the lens's geometric distortion with the mapping equations:

```kotlin
<code> x_c = x_i * ( kappa_0 + kappa_1 * r^2 + kappa_2 * r^4 + kappa_3 * r^6 ) +
         kappa_4 * (2 * x_i * y_i) + kappa_5 * ( r^2 + 2 * x_i^2 )
   y_c = y_i * ( kappa_0 + kappa_1 * r^2 + kappa_2 * r^4 + kappa_3 * r^6 ) +
         kappa_5 * (2 * x_i * y_i) + kappa_4 * ( r^2 + 2 * y_i^2 )
  </code>
```

Here, `[x_c, y_c]` are the coordinates to sample in the input image that correspond to the pixel values in the corrected image at the coordinate `[x_i, y_i]`:

```kotlin
<code> correctedImage(x_i, y_i) = sample_at(x_c, y_c, inputImage)
  </code>
```

The pixel coordinates are defined in a normalized coordinate system related to the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key` calibration fields. Both `[x_i, y_i]` and `[x_c, y_c]` have `(0,0)` at the lens optical center `[c_x, c_y]`. The maximum magnitudes of both x and y coordinates are normalized to be 1 at the edge further from the optical center, so the range for both dimensions is `-1 <= x <= 1`.

Finally, `r` represents the radial distance from the optical center, `r^2 = x_i^2 + y_i^2`, and its magnitude is therefore no larger than `|r| <= sqrt(2)`.

The distortion model used is the Brown-Conrady model.

**Units**: Unitless coefficients.

**Optional** - The value for this key may be `null` on some devices.

**Permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` is needed to access this property**
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key`

### LOGICAL_MULTI_CAMERA_SENSOR_SYNC_TYPE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOGICAL_MULTI_CAMERA_SENSOR_SYNC_TYPE: CameraCharacteristics.Key<Int!>
```

The accuracy of frame timestamp synchronization between physical cameras

The accuracy of the frame timestamp synchronization determines the physical cameras' ability to start exposure at the same time. If the sensorSyncType is CALIBRATED, the physical camera sensors usually run in leader/follower mode where one sensor generates a timing signal for the other, so that their shutter time is synchronized. For APPROXIMATE sensorSyncType, the camera sensors usually run in leader/leader mode, where both sensors use their own timing generator, and there could be offset between their start of exposure.

In both cases, all images generated for a particular capture request still carry the same timestamps, so that they can be used to look up the matching frame number and onCaptureStarted callback.

This tag is only applicable if the logical camera device supports concurrent physical streams from different physical cameras.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LOGICAL_MULTI_CAMERA_SENSOR_SYNC_TYPE_APPROXIMATE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LOGICAL_MULTI_CAMERA_SENSOR_SYNC_TYPE_CALIBRATED:kotlin.Int`

**Optional** - The value for this key may be `null` on some devices.

**Limited capability** - Present on all camera devices that report being at least `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LOGICAL_MULTI_CAMERA_SENSOR_SYNC_TYPE_APPROXIMATE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LOGICAL_MULTI_CAMERA_SENSOR_SYNC_TYPE_CALIBRATED:kotlin.Int`

### NOISE_REDUCTION_AVAILABLE_NOISE_REDUCTION_MODES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NOISE_REDUCTION_AVAILABLE_NOISE_REDUCTION_MODES: CameraCharacteristics.Key<IntArray!>
```

List of noise reduction modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#NOISE_REDUCTION_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

Full-capability camera devices will always support OFF and FAST.

Camera devices that support YUV_REPROCESSING or PRIVATE_REPROCESSING will support ZERO_SHUTTER_LAG.

Legacy-capability camera devices will only support FAST mode.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#NOISE_REDUCTION_MODE:android.hardware.camera2.CaptureRequest.Key`

**Optional** - The value for this key may be `null` on some devices.

**Limited capability** - Present on all camera devices that report being at least `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#NOISE_REDUCTION_MODE:android.hardware.camera2.CaptureRequest.Key`

### REPROCESS_MAX_CAPTURE_STALL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REPROCESS_MAX_CAPTURE_STALL: CameraCharacteristics.Key<Int!>
```

The maximal camera capture pipeline stall (in unit of frame count) introduced by a reprocess capture request.

The key describes the maximal interference that one reprocess (input) request can introduce to the camera simultaneous streaming of regular (output) capture requests, including repeating requests.

When a reprocessing capture request is submitted while a camera output repeating request (e.g. preview) is being served by the camera device, it may preempt the camera capture pipeline for at least one frame duration so that the camera device is unable to process the following capture request in time for the next sensor start of exposure boundary. When this happens, the application may observe a capture time gap (longer than one frame duration) between adjacent capture output frames, which usually exhibits as preview glitch if the repeating request output targets include a preview surface. This key gives the worst-case number of frame stall introduced by one reprocess request with any kind of formats/sizes combination.

If this key reports 0, it means a reprocess request doesn't introduce any glitch to the ongoing camera repeating request outputs, as if this reprocess request is never issued.

This key is supported if the camera device supports PRIVATE or YUV reprocessing ( i.e. `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` contains PRIVATE_REPROCESSING or YUV_REPROCESSING).

**Units**: Number of frames.

**Range of valid values:** 
\<= 4

**Optional** - The value for this key may be `null` on some devices.

**Limited capability** - Present on all camera devices that report being at least `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_AVAILABLE_CAPABILITIES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_CAPABILITIES: CameraCharacteristics.Key<IntArray!>
```

List of capabilities that this camera device advertises as fully supporting.

A capability is a contract that the camera device makes in order to be able to satisfy one or more use cases.

Listing a capability guarantees that the whole set of features required to support a common use will all be available.

Using a subset of the functionality provided by an unsupported capability may be possible on a specific camera device implementation; to do this query each of android.request.availableRequestKeys, android.request.availableResultKeys, android.request.availableCharacteristicsKeys.

The following capabilities are guaranteed to be available on `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` `==` FULL devices:

- MANUAL_SENSOR
- MANUAL_POST_PROCESSING

Other capabilities may be available on either FULL or LIMITED devices, but the application should query this key to be sure.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_BACKWARD_COMPATIBLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_MANUAL_SENSOR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_MANUAL_POST_PROCESSING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_RAW:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_PRIVATE_REPROCESSING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_READ_SENSOR_SETTINGS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_BURST_CAPTURE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_YUV_REPROCESSING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_DEPTH_OUTPUT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_CONSTRAINED_HIGH_SPEED_VIDEO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_MOTION_TRACKING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_LOGICAL_MULTI_CAMERA:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_MONOCHROME:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_SECURE_IMAGE_DATA:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_SYSTEM_CAMERA:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_OFFLINE_PROCESSING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_REMOSAIC_REPROCESSING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_DYNAMIC_RANGE_TEN_BIT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_STREAM_USE_CASE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_COLOR_SPACE_PROFILES:kotlin.Int`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_BACKWARD_COMPATIBLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_MANUAL_SENSOR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_MANUAL_POST_PROCESSING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_RAW:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_PRIVATE_REPROCESSING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_READ_SENSOR_SETTINGS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_BURST_CAPTURE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_YUV_REPROCESSING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_DEPTH_OUTPUT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_CONSTRAINED_HIGH_SPEED_VIDEO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_MOTION_TRACKING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_LOGICAL_MULTI_CAMERA:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_MONOCHROME:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_SECURE_IMAGE_DATA:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_SYSTEM_CAMERA:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_OFFLINE_PROCESSING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_REMOSAIC_REPROCESSING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_DYNAMIC_RANGE_TEN_BIT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_STREAM_USE_CASE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_COLOR_SPACE_PROFILES:kotlin.Int`

### REQUEST_AVAILABLE_COLOR_SPACE_PROFILES

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_COLOR_SPACE_PROFILES: CameraCharacteristics.Key<ColorSpaceProfiles!>
```

An interface for querying the color space profiles supported by a camera device.

A color space profile is a combination of a color space, an image format, and a dynamic range profile. Camera clients can retrieve the list of supported color spaces by calling `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceProfiles#getSupportedColorSpaces(kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceProfiles#getSupportedColorSpacesForDynamicRange(kotlin.Int,%20kotlin.Long)`. If a camera does not support the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_DYNAMIC_RANGE_TEN_BIT:kotlin.Int` capability, the dynamic range profile will always be `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#STANDARD:kotlin.Long`. Color space capabilities are queried in combination with an `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#`. If a camera client wants to know the general color space capabilities of a camera device regardless of image format, it can specify `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#UNKNOWN:kotlin.Int`. The color space for a session can be configured by setting the SessionConfiguration color space via `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setColorSpace(android.graphics.ColorSpace.Named)`.

**Optional** - The value for this key may be `null` on some devices.

### REQUEST_AVAILABLE_DYNAMIC_RANGE_PROFILES

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_DYNAMIC_RANGE_PROFILES: CameraCharacteristics.Key<DynamicRangeProfiles!>
```

Devices supporting the 10-bit output capability `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_DYNAMIC_RANGE_TEN_BIT:kotlin.Int` must list their supported dynamic range profiles along with capture request constraints for specific profile combinations.

Camera clients can retrieve the list of supported 10-bit dynamic range profiles by calling `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#getSupportedProfiles()`. Any of them can be configured by setting OutputConfiguration dynamic range profile in `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#setDynamicRangeProfile(kotlin.Long)`. Clients can also check if there are any constraints that limit the combination of supported profiles that can be referenced within a single capture request by calling `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#getProfileCaptureRequestConstraints(kotlin.Long)`.

**Optional** - The value for this key may be `null` on some devices.

### REQUEST_MAX_NUM_INPUT_STREAMS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_MAX_NUM_INPUT_STREAMS: CameraCharacteristics.Key<Int!>
```

The maximum numbers of any type of input streams that can be configured and used simultaneously by a camera device.

When set to 0, it means no input stream is supported.

The image format for a input stream can be any supported format returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()`. When using an input stream, there must be at least one output stream configured to to receive the reprocessed images.

When an input stream and some output streams are used in a reprocessing request, only the input buffer will be used to produce these output stream buffers, and a new sensor image will not be captured.

For example, for Zero Shutter Lag (ZSL) still capture use case, the input stream image format will be PRIVATE, the associated output stream image format should be JPEG.

**Range of valid values:** 

0 or 1.

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_MAX_NUM_OUTPUT_PROC

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_MAX_NUM_OUTPUT_PROC: CameraCharacteristics.Key<Int!>
```

The maximum numbers of different types of output streams that can be configured and used simultaneously by a camera device for any processed (but not-stalling) formats.

This value contains the max number of output simultaneous streams for any processed (but not-stalling) formats.

This lists the upper bound of the number of output streams supported by the camera device. Using more streams simultaneously may require more hardware and CPU resources that will consume more power. The image format for this kind of an output stream can be any non-`RAW` and supported format provided by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key`.

Processed (but not-stalling) is defined as any non-RAW format without a stall duration. Typically:

- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int`
- Implementation-defined formats, i.e. `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#isOutputSupportedFor(java.lang.Class)`
- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int`

For full guarantees, query android.hardware.camera2.params.StreamConfigurationMap#getOutputStallDuration with a processed format -- it will return 0 for a non-stalling stream.

LEGACY devices will support at least 2 processing/non-stalling streams.

**Range of valid values:** 

\>= 3 for FULL mode devices (`` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` == FULL ``); \>= 2 for LIMITED mode devices (`` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` == LIMITED ``).

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_MAX_NUM_OUTPUT_PROC_STALLING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_MAX_NUM_OUTPUT_PROC_STALLING: CameraCharacteristics.Key<Int!>
```

The maximum numbers of different types of output streams that can be configured and used simultaneously by a camera device for any processed (and stalling) formats.

This value contains the max number of output simultaneous streams for any processed (but not-stalling) formats.

This lists the upper bound of the number of output streams supported by the camera device. Using more streams simultaneously may require more hardware and CPU resources that will consume more power. The image format for this kind of an output stream can be any non-`RAW` and supported format provided by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key`.

A processed and stalling format is defined as any non-RAW format with a stallDurations \> 0. Typically only the `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` is a stalling format.

For full guarantees, query android.hardware.camera2.params.StreamConfigurationMap#getOutputStallDuration with a processed format -- it will return a non-0 value for a stalling stream.

LEGACY devices will support up to 1 processing/stalling stream.

**Range of valid values:** 

\>= 1

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_MAX_NUM_OUTPUT_RAW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_MAX_NUM_OUTPUT_RAW: CameraCharacteristics.Key<Int!>
```

The maximum numbers of different types of output streams that can be configured and used simultaneously by a camera device for any `RAW` formats.

This value contains the max number of output simultaneous streams from the raw sensor.

This lists the upper bound of the number of output streams supported by the camera device. Using more streams simultaneously may require more hardware and CPU resources that will consume more power. The image format for this kind of an output stream can be any `RAW` and supported format provided by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key`.

In particular, a `RAW` format is typically one of:

- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW10:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW12:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW14:kotlin.Int`

LEGACY mode devices (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` `==` LEGACY) never support raw streams.

**Range of valid values:** 

\>= 0

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_PARTIAL_RESULT_COUNT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_PARTIAL_RESULT_COUNT: CameraCharacteristics.Key<Int!>
```

Defines how many sub-components a result will be composed of.

In order to combat the pipeline latency, partial results may be delivered to the application layer from the camera device as soon as they are available.

Optional; defaults to 1. A value of 1 means that partial results are not supported, and only the final TotalCaptureResult will be produced by the camera device.

A typical use case for this might be: after requesting an auto-focus (AF) lock the new AF state might be available 50% of the way through the pipeline. The camera device could then immediately dispatch this state via a partial result to the application, and the rest of the metadata via later partial results.

**Range of valid values:** 
\>= 1

**Optional** - The value for this key may be `null` on some devices.

### REQUEST_PIPELINE_MAX_DEPTH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_PIPELINE_MAX_DEPTH: CameraCharacteristics.Key<Byte!>
```

Specifies the number of maximum pipeline stages a frame has to go through from when it's exposed to when it's available to the framework.

A typical minimum value for this is 2 (one stage to expose, one stage to readout) from the sensor. The ISP then usually adds its own stages to do custom HW processing. Further stages may be added by SW processing.

Depending on what settings are used (e.g. YUV, JPEG) and what processing is enabled (e.g. face detection), the actual pipeline depth (specified by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#REQUEST_PIPELINE_DEPTH:android.hardware.camera2.CaptureResult.Key`) may be less than the max pipeline depth.

A pipeline depth of X stages is equivalent to a pipeline latency of X frame intervals.

This value will normally be 8 or less, however, for high speed capture session, the max pipeline depth will be up to 8 x size of high speed capture request list.

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#REQUEST_PIPELINE_DEPTH:android.hardware.camera2.CaptureResult.Key`

### REQUEST_RECOMMENDED_TEN_BIT_DYNAMIC_RANGE_PROFILE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_RECOMMENDED_TEN_BIT_DYNAMIC_RANGE_PROFILE: CameraCharacteristics.Key<Long!>
```

Recommended 10-bit dynamic range profile.

Devices supporting the 10-bit output capability `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_DYNAMIC_RANGE_TEN_BIT:kotlin.Int` must list a 10-bit supported dynamic range profile that is expected to perform optimally in terms of image quality, power and performance. The value advertised can be used as a hint by camera clients when configuring the dynamic range profile when calling `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#setDynamicRangeProfile(kotlin.Long)`.

**Optional** - The value for this key may be `null` on some devices.

### SCALER_AVAILABLE_MAX_DIGITAL_ZOOM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_AVAILABLE_MAX_DIGITAL_ZOOM: CameraCharacteristics.Key<Float!>
```

The maximum ratio between both active area width and crop region width, and active area height and crop region height, for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`.

This represents the maximum amount of zooming possible by the camera device, or equivalently, the minimum cropping window size.

Crop regions that have a width or height that is smaller than this ratio allows will be rounded up to the minimum allowed size by the camera device.

Starting from API level 30, when using `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` to zoom in or out, the application must use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_ZOOM_RATIO_RANGE:android.hardware.camera2.CameraCharacteristics.Key` to query both the minimum and maximum zoom ratio.

**Units**: Zoom scale factor

**Range of valid values:** 
\>=1

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_ZOOM_RATIO_RANGE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`

### SCALER_AVAILABLE_ROTATE_AND_CROP_MODES

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_AVAILABLE_ROTATE_AND_CROP_MODES: CameraCharacteristics.Key<IntArray!>
```

List of rotate-and-crop modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_ROTATE_AND_CROP:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

This entry lists the valid modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_ROTATE_AND_CROP:android.hardware.camera2.CaptureRequest.Key` for this camera device.

Starting with API level 30, all devices will list at least `ROTATE_AND_CROP_NONE`. Devices with support for rotate-and-crop will additionally list at least `ROTATE_AND_CROP_AUTO` and `ROTATE_AND_CROP_90`.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_ROTATE_AND_CROP:android.hardware.camera2.CaptureRequest.Key`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_ROTATE_AND_CROP:android.hardware.camera2.CaptureRequest.Key`

### SCALER_AVAILABLE_STREAM_USE_CASES

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_AVAILABLE_STREAM_USE_CASES: CameraCharacteristics.Key<LongArray!>
```

The stream use cases supported by this camera device.

The stream use case indicates the purpose of a particular camera stream from the end-user perspective. Some examples of camera use cases are: preview stream for live viewfinder shown to the user, still capture for generating high quality photo capture, video record for encoding the camera output for the purpose of future playback, and video call for live realtime video conferencing.

With this flag, the camera device can optimize the image processing pipeline parameters, such as tuning, sensor mode, and ISP settings, independent of the properties of the immediate camera output surface. For example, if the output surface is a SurfaceTexture, the stream use case flag can be used to indicate whether the camera frames eventually go to display, video encoder, still image capture, or all of them combined.

The application sets the use case of a camera stream by calling `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#setStreamUseCase(kotlin.Long)`.

A camera device with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_STREAM_USE_CASE:kotlin.Int` capability must support the following stream use cases:

- DEFAULT
- PREVIEW
- STILL_CAPTURE
- VIDEO_RECORD
- PREVIEW_VIDEO_STILL
- VIDEO_CALL

The guaranteed stream combinations related to stream use case for a camera device with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_STREAM_USE_CASE:kotlin.Int` capability is documented in the camera device [guideline](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#stream-use-case-capability-additional-guaranteed-configurations). The application is strongly recommended to use one of the guaranteed stream combinations. If the application creates a session with a stream combination not in the guaranteed list, or with mixed DEFAULT and non-DEFAULT use cases within the same session, the camera device may ignore some stream use cases due to hardware constraints and implementation details.

For stream combinations not covered by the stream use case mandatory lists, such as reprocessable session, constrained high speed session, or RAW stream combinations, the application should leave stream use cases within the session as DEFAULT.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_DEFAULT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_PREVIEW:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_STILL_CAPTURE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_VIDEO_RECORD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_PREVIEW_VIDEO_STILL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_VIDEO_CALL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_CROPPED_RAW:kotlin.Int`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_DEFAULT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_PREVIEW:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_STILL_CAPTURE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_VIDEO_RECORD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_PREVIEW_VIDEO_STILL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_VIDEO_CALL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_CROPPED_RAW:kotlin.Int`

### SCALER_CROPPING_TYPE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_CROPPING_TYPE: CameraCharacteristics.Key<Int!>
```

The crop type that this camera device supports.

When passing a non-centered crop region (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`) to a camera device that only supports CENTER_ONLY cropping, the camera device will move the crop region to the center of the sensor active array (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`) and keep the crop region width and height unchanged. The camera device will return the final used crop region in metadata result `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`.

Camera devices that support FREEFORM cropping will support any crop region that is inside of the active array. The camera device will apply the same crop region and return the final used crop region in capture result metadata `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`.

Starting from API level 30,

- If the camera device supports FREEFORM cropping, in order to do FREEFORM cropping, the application must set `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` to 1.0, and use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` for zoom.
- To do CENTER_ONLY zoom, the application has below 2 options:
 1. Set `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` to 1.0; adjust zoom by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`.
 2. Adjust zoom by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`; use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` to crop the field of view vertically (letterboxing) or horizontally (pillarboxing), but not windowboxing.
- Setting `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` to values different than 1.0 and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` to be windowboxing at the same time are not supported. In this case, the camera framework will override the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` to be the active array.

LEGACY capability devices will only support CENTER_ONLY cropping.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_CROPPING_TYPE_CENTER_ONLY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_CROPPING_TYPE_FREEFORM:kotlin.Int`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_CROPPING_TYPE_CENTER_ONLY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_CROPPING_TYPE_FREEFORM:kotlin.Int`

### SCALER_DEFAULT_SECURE_IMAGE_SIZE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_DEFAULT_SECURE_IMAGE_SIZE: CameraCharacteristics.Key<Size!>
```

Default YUV/PRIVATE size to use for requesting secure image buffers.

This entry lists the default size supported in the secure camera mode. This entry is optional on devices support the SECURE_IMAGE_DATA capability. This entry will be null if the camera device does not list SECURE_IMAGE_DATA capability.

When the key is present, only a PRIVATE/YUV output of the specified size is guaranteed to be supported by the camera HAL in the secure camera mode. Any other format or resolutions might not be supported. Use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#isSessionConfigurationSupported(android.hardware.camera2.params.SessionConfiguration)` API to query if a secure session configuration is supported if the device supports this API.

If this key returns null on a device with SECURE_IMAGE_DATA capability, the application can assume all output sizes listed in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap` are supported.

**Units**: Pixels

**Optional** - The value for this key may be `null` on some devices.

### SCALER_MANDATORY_CONCURRENT_STREAM_COMBINATIONS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_MANDATORY_CONCURRENT_STREAM_COMBINATIONS: CameraCharacteristics.Key<Array<MandatoryStreamCombination!>!>
```

An array of mandatory concurrent stream combinations. This is an app-readable conversion of the concurrent mandatory stream combination [tables](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#concurrent-stream-guaranteed-configurations).

The array of `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination` is generated according to the documented [guideline](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#concurrent-stream-guaranteed-configurations) for each device which has its Id present in the set returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getConcurrentCameraIds()`. Clients can use the array as a quick reference to find an appropriate camera stream combination. The mandatory stream combination array will be `null` in case the device is not a part of at least one set of combinations returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getConcurrentCameraIds()`.

**Optional** - The value for this key may be `null` on some devices.

### SCALER_MANDATORY_MAXIMUM_RESOLUTION_STREAM_COMBINATIONS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_MANDATORY_MAXIMUM_RESOLUTION_STREAM_COMBINATIONS: CameraCharacteristics.Key<Array<MandatoryStreamCombination!>!>
```

An array of mandatory stream combinations which are applicable when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest` has `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`. This is an app-readable conversion of the maximum resolution mandatory stream combination [tables](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#additional-guaranteed-combinations-for-ultra-high-resolution-sensors).

The array of `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination` is generated according to the documented [guideline](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#additional-guaranteed-combinations-for-ultra-high-resolution-sensors) for each device which has the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR:kotlin.Int` capability. Clients can use the array as a quick reference to find an appropriate camera stream combination. The mandatory stream combination array will be `null` in case the device is not an `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR:kotlin.Int` device.

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`

### SCALER_MANDATORY_PREVIEW_STABILIZATION_OUTPUT_STREAM_COMBINATIONS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_MANDATORY_PREVIEW_STABILIZATION_OUTPUT_STREAM_COMBINATIONS: CameraCharacteristics.Key<Array<MandatoryStreamCombination!>!>
```

An array of mandatory stream combinations which are applicable when device lists `PREVIEW_STABILIZATION` in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_VIDEO_STABILIZATION_MODES:android.hardware.camera2.CameraCharacteristics.Key`. This is an app-readable conversion of the preview stabilization mandatory stream combination [tables](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#preview-stabilization-guaranteed-stream-configurations).

The array of `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination` is generated according to the documented [guideline](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#preview-stabilization-guaranteed-stream-configurations) for each device which supports `PREVIEW_STABILIZATION` Clients can use the array as a quick reference to find an appropriate camera stream combination. The mandatory stream combination array will be `null` in case the device does not list `PREVIEW_STABILIZATION` in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_VIDEO_STABILIZATION_MODES:android.hardware.camera2.CameraCharacteristics.Key`.

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_VIDEO_STABILIZATION_MODES:android.hardware.camera2.CameraCharacteristics.Key`

### SCALER_MANDATORY_STREAM_COMBINATIONS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_MANDATORY_STREAM_COMBINATIONS: CameraCharacteristics.Key<Array<MandatoryStreamCombination!>!>
```

An array of mandatory stream combinations generated according to the camera device `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`. This is an app-readable conversion of the mandatory stream combination [tables](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#legacy-level-guaranteed-configurations).

The array of `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination` is generated according to the documented [guideline](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#legacy-level-guaranteed-configurations). based on specific device level and capabilities. Clients can use the array as a quick reference to find an appropriate camera stream combination. As per documentation, the stream combinations with given PREVIEW, RECORD and MAXIMUM resolutions and anything smaller from the list given by android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes are guaranteed to work. For a physical camera not independently exposed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList()`, the mandatory stream combinations for that physical camera Id are also generated, so that the application can configure them as physical streams via the logical camera. The mandatory stream combination array will be `null` in case the device is not backward compatible.

**Optional** - The value for this key may be `null` on some devices.

**Limited capability** - Present on all camera devices that report being at least `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`

### SCALER_MANDATORY_TEN_BIT_OUTPUT_STREAM_COMBINATIONS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_MANDATORY_TEN_BIT_OUTPUT_STREAM_COMBINATIONS: CameraCharacteristics.Key<Array<MandatoryStreamCombination!>!>
```

An array of mandatory stream combinations which are applicable when device support the 10-bit output capability `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_DYNAMIC_RANGE_TEN_BIT:kotlin.Int` This is an app-readable conversion of the 10 bit output mandatory stream combination [tables](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#10-bit-output-additional-guaranteed-configurations).

The array of `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination` is generated according to the documented [guideline](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#10-bit-output-additional-guaranteed-configurations) for each device which has the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_DYNAMIC_RANGE_TEN_BIT:kotlin.Int` capability. Clients can use the array as a quick reference to find an appropriate camera stream combination. The mandatory stream combination array will be `null` in case the device is not an `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_DYNAMIC_RANGE_TEN_BIT:kotlin.Int` device.

**Optional** - The value for this key may be `null` on some devices.

### SCALER_MANDATORY_USE_CASE_STREAM_COMBINATIONS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_MANDATORY_USE_CASE_STREAM_COMBINATIONS: CameraCharacteristics.Key<Array<MandatoryStreamCombination!>!>
```

An array of mandatory stream combinations with stream use cases. This is an app-readable conversion of the mandatory stream combination [tables](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#stream-use-case-capability-additional-guaranteed-configurations) with each stream's use case being set.

The array of `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination` is generated according to the documented [guildeline](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#stream-use-case-capability-additional-guaranteed-configurations) for a camera device with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_STREAM_USE_CASE:kotlin.Int` capability. The mandatory stream combination array will be `null` in case the device doesn't have `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_STREAM_USE_CASE:kotlin.Int` capability.

**Optional** - The value for this key may be `null` on some devices.

### SCALER_MULTI_RESOLUTION_STREAM_CONFIGURATION_MAP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_MULTI_RESOLUTION_STREAM_CONFIGURATION_MAP: CameraCharacteristics.Key<MultiResolutionStreamConfigurationMap!>
```

The multi-resolution stream configurations supported by this logical camera or ultra high resolution sensor camera device.

Multi-resolution streams can be used by a LOGICAL_MULTI_CAMERA or an ULTRA_HIGH_RESOLUTION_SENSOR camera where the images sent or received can vary in resolution per frame. This is useful in cases where the camera device's effective full resolution changes depending on factors such as the current zoom level, lighting condition, focus distance, or pixel mode.

- For a logical multi-camera implementing optical zoom, at different zoom level, a different physical camera may be active, resulting in different full-resolution image sizes.
- For an ultra high resolution camera, depending on whether the camera operates in default mode, or maximum resolution mode, the output full-size images may be of either binned resolution or maximum resolution.

To use multi-resolution output streams, the supported formats can be queried by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MultiResolutionStreamConfigurationMap#getOutputFormats()`. A `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader` can then be created for a supported format with the MultiResolutionStreamInfo group queried by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MultiResolutionStreamConfigurationMap#getOutputInfo(kotlin.Int)`.

If a camera device supports multi-resolution output streams for a particular format, for each of its mandatory stream combinations, the camera device will support using a MultiResolutionImageReader for the MAXIMUM stream of supported formats. Refer to [the table](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#legacy-level-additional-guaranteed-combinations-with-multiresolutionoutputs) for additional details.

To use multi-resolution input streams, the supported formats can be queried by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MultiResolutionStreamConfigurationMap#getInputFormats()`. A reprocessable CameraCaptureSession can then be created using an `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration` constructed with the input MultiResolutionStreamInfo group, queried by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MultiResolutionStreamConfigurationMap#getInputInfo(kotlin.Int)`.

If a camera device supports multi-resolution `YUV` input and multi-resolution `YUV` output, or multi-resolution `PRIVATE` input and multi-resolution `PRIVATE` output, `JPEG` and `YUV` are guaranteed to be supported multi-resolution output stream formats. Refer to [the table](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#legacy-level-additional-guaranteed-combinations-with-multiresolutionoutputs) for details about the additional mandatory stream combinations in this case.

**Optional** - The value for this key may be `null` on some devices.

### SCALER_STREAM_CONFIGURATION_MAP

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_STREAM_CONFIGURATION_MAP: CameraCharacteristics.Key<StreamConfigurationMap!>
```

The available stream configurations that this camera device supports; also includes the minimum frame durations and the stall durations for each format/size combination.

All camera devices will support sensor maximum resolution (defined by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`) for the JPEG format.

For a given use case, the actual maximum supported resolution may be lower than what is listed here, depending on the destination Surface for the image data. For example, for recording video, the video encoder chosen may have a maximum size limit (e.g. 1080p) smaller than what the camera (e.g. maximum resolution is 3264x2448) can provide.

Please reference the documentation for the image data destination to check if it limits the maximum size for image data.

For applications targeting SDK version older than 31, the following table describes the minimum required output stream configurations based on the hardware level (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`):

| Format | Size | Hardware Level | Notes |
|---|---|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` (\*1) | Any | |
| `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` | 1920x1080 (1080p) | Any | if 1080p \<= activeArraySize |
| `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` | 1280x720 (720p) | Any | if 720p \<= activeArraySize |
| `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` | 640x480 (480p) | Any | if 480p \<= activeArraySize |
| `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` | 320x240 (240p) | Any | if 240p \<= activeArraySize |
| `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` | all output sizes available for JPEG | FULL | |
| `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` | all output sizes available for JPEG, up to the maximum video size | LIMITED | |
| `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` | same as YUV_420_888 | Any | |

For applications targeting SDK version 31 or newer, if the mobile device declares to be media performance class 12 or higher by setting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION.html#MEDIA_PERFORMANCE_CLASS:kotlin.Int` to be 31 or larger, the primary camera devices (first rear/front camera in the camera ID list) will not support JPEG sizes smaller than 1080p. If the application configures a JPEG stream smaller than 1080p, the camera device will round up the JPEG image size to at least 1080p. The requirements for IMPLEMENTATION_DEFINED and YUV_420_888 stay the same. This new minimum required output stream configurations are illustrated by the table below:

| Format | Size | Hardware Level | Notes |
|---|---|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` (\*1) | Any | |
| `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` | 1920x1080 (1080p) | Any | if 1080p \<= activeArraySize |
| `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` | FULL | |
| `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` | 1920x1080 (1080p) | FULL | if 1080p \<= activeArraySize |
| `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` | 1280x720 (720) | FULL | if 720p \<= activeArraySize |
| `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` | 640x480 (480p) | FULL | if 480p \<= activeArraySize |
| `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` | 320x240 (240p) | FULL | if 240p \<= activeArraySize |
| `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` | all output sizes available for JPEG | FULL | |
| `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` | all output sizes available for FULL hardware level, up to the maximum video size | LIMITED | |
| `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` | same as YUV_420_888 | Any | |

For applications targeting SDK version 31 or newer, if the mobile device doesn't declare to be media performance class 12 or better by setting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION.html#MEDIA_PERFORMANCE_CLASS:kotlin.Int` to be 31 or larger, or if the camera device isn't a primary rear/front camera, the minimum required output stream configurations are the same as for applications targeting SDK version older than 31.

Refer to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` and [the table](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#legacy-level-guaranteed-configurations) for additional mandatory stream configurations on a per-capability basis.

\*1: For JPEG format, the sizes may be restricted by below conditions:

- The HAL may choose the aspect ratio of each Jpeg size to be one of well known ones (e.g. 4:3, 16:9, 3:2 etc.). If the sensor maximum resolution (defined by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`) has an aspect ratio other than these, it does not have to be included in the supported JPEG sizes.
- Some hardware JPEG encoders may have pixel boundary alignment requirements, such as the dimensions being a multiple of 16. Therefore, the maximum JPEG size may be smaller than sensor maximum resolution. However, the largest JPEG size will be as close as possible to the sensor maximum resolution given above constraints. It is required that after aspect ratio adjustments, additional size reduction due to other issues must be less than 3% in area. For example, if the sensor maximum resolution is 3280x2464, if the maximum JPEG size has aspect ratio 4:3, and the JPEG encoder alignment requirement is 16, the maximum JPEG size will be 3264x2448.

Exception on 176x144 (QCIF) resolution: camera devices usually have a fixed capability on downscaling from larger resolution to smaller ones, and the QCIF resolution can sometimes not be fully supported due to this limitation on devices with high-resolution image sensors. Therefore, trying to configure a QCIF resolution stream together with any other stream larger than 1920x1080 resolution (either width or height) might not be supported, and capture session creation will fail if it is not.

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`

### SCALER_STREAM_CONFIGURATION_MAP_MAXIMUM_RESOLUTION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_STREAM_CONFIGURATION_MAP_MAXIMUM_RESOLUTION: CameraCharacteristics.Key<StreamConfigurationMap!>
```

The available stream configurations that this camera device supports when given a CaptureRequest with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`; also includes the minimum frame durations and the stall durations for each format/size combination.

Analogous to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key` for CaptureRequests where `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` is `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`.

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`

### SENSOR_AVAILABLE_TEST_PATTERN_MODES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_AVAILABLE_TEST_PATTERN_MODES: CameraCharacteristics.Key<IntArray!>
```

List of sensor test pattern modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_TEST_PATTERN_MODE:android.hardware.camera2.CaptureRequest.Key` supported by this camera device.

Defaults to OFF, and always includes OFF if defined.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_TEST_PATTERN_MODE:android.hardware.camera2.CaptureRequest.Key`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_TEST_PATTERN_MODE:android.hardware.camera2.CaptureRequest.Key`

### SENSOR_BLACK_LEVEL_PATTERN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_BLACK_LEVEL_PATTERN: CameraCharacteristics.Key<BlackLevelPattern!>
```

A fixed black level offset for each of the color filter arrangement (CFA) mosaic channels.

This key specifies the zero light value for each of the CFA mosaic channels in the camera sensor. The maximal value output by the sensor is represented by the value in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_WHITE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`.

The values are given in the same order as channels listed for the CFA layout key (see `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT:android.hardware.camera2.CameraCharacteristics.Key`), i.e. the nth value given corresponds to the black level offset for the nth color channel listed in the CFA.

The black level values of captured images may vary for different capture settings (e.g., `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`). This key represents a coarse approximation for such case. It is recommended to use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_DYNAMIC_BLACK_LEVEL:android.hardware.camera2.CaptureResult.Key` or use pixels from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_OPTICAL_BLACK_REGIONS:android.hardware.camera2.CameraCharacteristics.Key` directly for captures when supported by the camera device, which provides more accurate black level values. For raw capture in particular, it is recommended to use pixels from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_OPTICAL_BLACK_REGIONS:android.hardware.camera2.CameraCharacteristics.Key` to calculate black level values for each frame.

For a MONOCHROME camera device, all of the 2x2 channels must have the same values.

**Range of valid values:** 
\>= 0 for each.

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_DYNAMIC_BLACK_LEVEL:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_WHITE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_OPTICAL_BLACK_REGIONS:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`

### SENSOR_CALIBRATION_TRANSFORM1

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_CALIBRATION_TRANSFORM1: CameraCharacteristics.Key<ColorSpaceTransform!>
```

A per-device calibration transform matrix that maps from the reference sensor colorspace to the actual device sensor colorspace.

This matrix is used to correct for per-device variations in the sensor colorspace, and is used for processing raw buffer data.

The matrix is expressed as a 3x3 matrix in row-major-order, and contains a per-device calibration transform that maps colors from reference sensor color space (i.e. the "golden module" colorspace) into this camera device's native sensor color space under the first reference illuminant (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`).

Starting from Android Q, this key will not be present for a MONOCHROME camera, even if the camera device has RAW capability.

**Optional** - The value for this key may be `null` on some devices.

**Permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` is needed to access this property**
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_CALIBRATION_TRANSFORM2

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_CALIBRATION_TRANSFORM2: CameraCharacteristics.Key<ColorSpaceTransform!>
```

A per-device calibration transform matrix that maps from the reference sensor colorspace to the actual device sensor colorspace (this is the colorspace of the raw buffer data).

This matrix is used to correct for per-device variations in the sensor colorspace, and is used for processing raw buffer data.

The matrix is expressed as a 3x3 matrix in row-major-order, and contains a per-device calibration transform that maps colors from reference sensor color space (i.e. the "golden module" colorspace) into this camera device's native sensor color space under the second reference illuminant (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT2:android.hardware.camera2.CameraCharacteristics.Key`).

This matrix will only be present if the second reference illuminant is present.

Starting from Android Q, this key will not be present for a MONOCHROME camera, even if the camera device has RAW capability.

**Optional** - The value for this key may be `null` on some devices.

**Permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` is needed to access this property**
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT2:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_COLOR_TRANSFORM1

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_COLOR_TRANSFORM1: CameraCharacteristics.Key<ColorSpaceTransform!>
```

A matrix that transforms color values from CIE XYZ color space to reference sensor color space.

This matrix is used to convert from the standard CIE XYZ color space to the reference sensor colorspace, and is used when processing raw buffer data.

The matrix is expressed as a 3x3 matrix in row-major-order, and contains a color transform matrix that maps colors from the CIE XYZ color space to the reference sensor color space (i.e. the "golden module" colorspace) under the first reference illuminant (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`).

The white points chosen in both the reference sensor color space and the CIE XYZ colorspace when calculating this transform will match the standard white point for the first reference illuminant (i.e. no chromatic adaptation will be applied by this transform).

Starting from Android Q, this key will not be present for a MONOCHROME camera, even if the camera device has RAW capability.

**Optional** - The value for this key may be `null` on some devices.

**Permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` is needed to access this property**
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_COLOR_TRANSFORM2

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_COLOR_TRANSFORM2: CameraCharacteristics.Key<ColorSpaceTransform!>
```

A matrix that transforms color values from CIE XYZ color space to reference sensor color space.

This matrix is used to convert from the standard CIE XYZ color space to the reference sensor colorspace, and is used when processing raw buffer data.

The matrix is expressed as a 3x3 matrix in row-major-order, and contains a color transform matrix that maps colors from the CIE XYZ color space to the reference sensor color space (i.e. the "golden module" colorspace) under the second reference illuminant (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT2:android.hardware.camera2.CameraCharacteristics.Key`).

The white points chosen in both the reference sensor color space and the CIE XYZ colorspace when calculating this transform will match the standard white point for the second reference illuminant (i.e. no chromatic adaptation will be applied by this transform).

This matrix will only be present if the second reference illuminant is present.

Starting from Android Q, this key will not be present for a MONOCHROME camera, even if the camera device has RAW capability.

**Optional** - The value for this key may be `null` on some devices.

**Permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` is needed to access this property**
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT2:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_FORWARD_MATRIX1

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_FORWARD_MATRIX1: CameraCharacteristics.Key<ColorSpaceTransform!>
```

A matrix that transforms white balanced camera colors from the reference sensor colorspace to the CIE XYZ colorspace with a D50 whitepoint.

This matrix is used to convert to the standard CIE XYZ colorspace, and is used when processing raw buffer data.

This matrix is expressed as a 3x3 matrix in row-major-order, and contains a color transform matrix that maps white balanced colors from the reference sensor color space to the CIE XYZ color space with a D50 white point.

Under the first reference illuminant (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`) this matrix is chosen so that the standard white point for this reference illuminant in the reference sensor colorspace is mapped to D50 in the CIE XYZ colorspace.

Starting from Android Q, this key will not be present for a MONOCHROME camera, even if the camera device has RAW capability.

**Optional** - The value for this key may be `null` on some devices.

**Permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` is needed to access this property**
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_FORWARD_MATRIX2

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_FORWARD_MATRIX2: CameraCharacteristics.Key<ColorSpaceTransform!>
```

A matrix that transforms white balanced camera colors from the reference sensor colorspace to the CIE XYZ colorspace with a D50 whitepoint.

This matrix is used to convert to the standard CIE XYZ colorspace, and is used when processing raw buffer data.

This matrix is expressed as a 3x3 matrix in row-major-order, and contains a color transform matrix that maps white balanced colors from the reference sensor color space to the CIE XYZ color space with a D50 white point.

Under the second reference illuminant (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT2:android.hardware.camera2.CameraCharacteristics.Key`) this matrix is chosen so that the standard white point for this reference illuminant in the reference sensor colorspace is mapped to D50 in the CIE XYZ colorspace.

This matrix will only be present if the second reference illuminant is present.

Starting from Android Q, this key will not be present for a MONOCHROME camera, even if the camera device has RAW capability.

**Optional** - The value for this key may be `null` on some devices.

**Permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` is needed to access this property**
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT2:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_INFO_ACTIVE_ARRAY_SIZE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_ACTIVE_ARRAY_SIZE: CameraCharacteristics.Key<Rect!>
```

The area of the image sensor which corresponds to active pixels after any geometric distortion correction has been applied.

This is the rectangle representing the size of the active region of the sensor (i.e. the region that actually receives light from the scene) after any geometric correction has been applied, and should be treated as the maximum size in pixels of any of the image output formats aside from the raw formats.

This rectangle is defined relative to the full pixel array; (0,0) is the top-left of the full pixel array, and the size of the full pixel array is given by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PIXEL_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.

The coordinate system for most other keys that list pixel coordinates, including `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`, is defined relative to the active array rectangle given in this field, with `(0, 0)` being the top-left of this rectangle.

The active array may be smaller than the full pixel array, since the full array may include black calibration pixels or other inactive regions.

For devices that do not support `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` control, the active array must be the same as `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.

For devices that support `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` control, the active array must be enclosed by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`. The difference between pre-correction active array and active array accounts for scaling or cropping caused by lens geometric distortion correction.

In general, application should always refer to active array size for controls like metering regions or crop region. Two exceptions are when the application is dealing with RAW image buffers (RAW_SENSOR, RAW10, RAW12, RAW14 etc), or when application explicitly set `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key` to OFF. In these cases, application should refer to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.

**Units**: Pixel coordinates on the image sensor

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PIXEL_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_INFO_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION: CameraCharacteristics.Key<Rect!>
```

The area of the image sensor which corresponds to active pixels after any geometric distortion correction has been applied, when the sensor runs in maximum resolution mode.

Analogous to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`, when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` is set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`. Refer to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` for details, with sensor array related keys replaced with their `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int` counterparts. This key will only be present for devices which advertise the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR:kotlin.Int` capability or devices where `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getAvailableCaptureRequestKeys()` lists `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`.

**Units**: Pixel coordinates on the image sensor

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`

### SENSOR_INFO_BINNING_FACTOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_BINNING_FACTOR: CameraCharacteristics.Key<Size!>
```

Dimensions of the group of pixels which are under the same color filter. This specifies the width and height (pair of integers) of the group of pixels which fall under the same color filter for ULTRA_HIGH_RESOLUTION sensors.

Sensors can have pixels grouped together under the same color filter in order to improve various aspects of imaging such as noise reduction, low light performance etc. These groups can be of various sizes such as 2X2 (quad bayer), 3X3 (nona-bayer). This key specifies the length and width of the pixels grouped under the same color filter. In case the device has the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR:kotlin.Int` capability :

- This key will not be present if REMOSAIC_REPROCESSING is not supported, since RAW images will have a regular bayer pattern.

In case the device does not have the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR:kotlin.Int` capability :

- This key will be present if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getAvailableCaptureRequestKeys()` lists `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`, since RAW images may not necessarily have a regular bayer pattern when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` is set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`.

**Units**: Pixels

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`

### SENSOR_INFO_COLOR_FILTER_ARRANGEMENT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_COLOR_FILTER_ARRANGEMENT: CameraCharacteristics.Key<Int!>
```

The arrangement of color filters on sensor; represents the colors in the top-left 2x2 section of the sensor, in reading order, for a Bayer camera, or the light spectrum it captures for MONOCHROME camera.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_RGGB:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_GRBG:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_GBRG:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_BGGR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_RGB:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_MONO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_NIR:kotlin.Int`

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_RGGB:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_GRBG:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_GBRG:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_BGGR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_RGB:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_MONO:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_NIR:kotlin.Int`

### SENSOR_INFO_EXPOSURE_TIME_RANGE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_EXPOSURE_TIME_RANGE: CameraCharacteristics.Key<Range<Long!>!>
```

The range of image exposure times for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key` supported by this camera device.

**Units**: Nanoseconds

**Range of valid values:** 
The minimum exposure time will be less than 100 us. For FULL capability devices (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` == FULL), the maximum exposure time will be greater than 100ms.

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`

### SENSOR_INFO_LENS_SHADING_APPLIED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_LENS_SHADING_APPLIED: CameraCharacteristics.Key<Boolean!>
```

Whether the RAW images output from this camera device are subject to lens shading correction.

If `true`, all images produced by the camera device in the `RAW` image formats will have at least some lens shading correction already applied to it. If `false`, the images will not be adjusted for lens shading correction. See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_MAX_NUM_OUTPUT_RAW:android.hardware.camera2.CameraCharacteristics.Key` for a list of RAW image formats.

When `true`, the `lensShadingCorrectionMap` key may still have values greater than 1.0, and those will need to be applied to any captured RAW frames for them to match the shading correction of processed buffers such as `YUV` or `JPEG` images. This may occur, for example, when some basic fixed lens shading correction is applied by hardware to RAW data, and additional correction is done dynamically in the camera processing pipeline after demosaicing.

This key will be `null` for all devices do not report this information. Devices with RAW capability will always report this information in this key.

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_MAX_NUM_OUTPUT_RAW:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_INFO_MAX_FRAME_DURATION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_MAX_FRAME_DURATION: CameraCharacteristics.Key<Long!>
```

The maximum possible frame duration (minimum frame rate) for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` that is supported this camera device.

Attempting to use frame durations beyond the maximum will result in the frame duration being clipped to the maximum. See that control for a full definition of frame durations.

Refer to android.hardware.camera2.params.StreamConfigurationMap#getOutputMinFrameDuration for the minimum frame duration values.

**Units**: Nanoseconds

**Range of valid values:** 
For FULL capability devices (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` == FULL), at least 100ms.

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key`

### SENSOR_INFO_PHYSICAL_SIZE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_PHYSICAL_SIZE: CameraCharacteristics.Key<SizeF!>
```

The physical dimensions of the full pixel array.

This is the physical size of the sensor pixel array defined by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PIXEL_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.

**Units**: Millimeters

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PIXEL_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_INFO_PIXEL_ARRAY_SIZE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_PIXEL_ARRAY_SIZE: CameraCharacteristics.Key<Size!>
```

Dimensions of the full pixel array, possibly including black calibration pixels.

The pixel count of the full pixel array of the image sensor, which covers `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PHYSICAL_SIZE:android.hardware.camera2.CameraCharacteristics.Key` area. This represents the full pixel dimensions of the raw buffers produced by this sensor.

If a camera device supports raw sensor formats, either this or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` is the maximum dimensions for the raw output formats listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap` (this depends on whether or not the image sensor returns buffers containing pixels that are not part of the active array region for blacklevel calibration or other purposes).

Some parts of the full pixel array may not receive light from the scene, or be otherwise inactive. The `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` key defines the rectangle of active pixels that will be included in processed image formats.

**Units**: Pixels

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PHYSICAL_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_INFO_PIXEL_ARRAY_SIZE_MAXIMUM_RESOLUTION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_PIXEL_ARRAY_SIZE_MAXIMUM_RESOLUTION: CameraCharacteristics.Key<Size!>
```

Dimensions of the full pixel array, possibly including black calibration pixels, when the sensor runs in maximum resolution mode. Analogous to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PIXEL_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`, when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` is set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`.

The pixel count of the full pixel array of the image sensor, which covers `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PHYSICAL_SIZE:android.hardware.camera2.CameraCharacteristics.Key` area. This represents the full pixel dimensions of the raw buffers produced by this sensor, when it runs in maximum resolution mode. That is, when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` is set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`. This key will only be present for devices which advertise the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR:kotlin.Int` capability or devices where `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getAvailableCaptureRequestKeys()` lists `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`.

**Units**: Pixels

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PHYSICAL_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PIXEL_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`

### SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE: CameraCharacteristics.Key<Rect!>
```

The area of the image sensor which corresponds to active pixels prior to the application of any geometric distortion correction.

This is the rectangle representing the size of the active region of the sensor (i.e. the region that actually receives light from the scene) before any geometric correction has been applied, and should be treated as the active region rectangle for any of the raw formats. All metadata associated with raw processing (e.g. the lens shading correction map, and radial distortion fields) treats the top, left of this rectangle as the origin, (0,0).

The size of this region determines the maximum field of view and the maximum number of pixels that an image from this sensor can contain, prior to the application of geometric distortion correction. The effective maximum pixel dimensions of a post-distortion-corrected image is given by the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` field, and the effective maximum field of view for a post-distortion-corrected image can be calculated by applying the geometric distortion correction fields to this rectangle, and cropping to the rectangle given in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.

E.g. to calculate position of a pixel, (x,y), in a processed YUV output image with the dimensions in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` given the position of a pixel, (x', y'), in the raw pixel array with dimensions given in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PIXEL_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`:

1. Choose a pixel (x', y') within the active array region of the raw buffer given in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`, otherwise this pixel is considered to be outside of the FOV, and will not be shown in the processed output image.
2. Apply geometric distortion correction to get the post-distortion pixel coordinate, (x_i, y_i). When applying geometric correction metadata, note that metadata for raw buffers is defined relative to the top, left of the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` rectangle.
3. If the resulting corrected pixel coordinate is within the region given in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`, then the position of this pixel in the processed output image buffer is `(x_i - activeArray.left, y_i - activeArray.top)`, when the top, left coordinate of that buffer is treated as (0, 0).

Thus, for pixel x',y' = (25, 25) on a sensor where `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PIXEL_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` is (100,100), `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` is (10, 10, 100, 100), `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` is (20, 20, 80, 80), and the geometric distortion correction doesn't change the pixel coordinate, the resulting pixel selected in pixel coordinates would be x,y = (25, 25) relative to the top,left of the raw buffer with dimensions given in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PIXEL_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`, and would be (5, 5) relative to the top,left of post-processed YUV output buffer with dimensions given in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.

The currently supported fields that correct for geometric distortion are:

1. `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key`.

If the camera device doesn't support geometric distortion correction, or all of the geometric distortion fields are no-ops, this rectangle will be the same as the post-distortion-corrected rectangle given in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.

This rectangle is defined relative to the full pixel array; (0,0) is the top-left of the full pixel array, and the size of the full pixel array is given by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PIXEL_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.

The pre-correction active array may be smaller than the full pixel array, since the full array may include black calibration pixels or other inactive regions.

**Units**: Pixel coordinates on the image sensor

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PIXEL_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE_MAXIMUM_RESOLUTION: CameraCharacteristics.Key<Rect!>
```

The area of the image sensor which corresponds to active pixels prior to the application of any geometric distortion correction, when the sensor runs in maximum resolution mode. This key must be used for crop / metering regions, only when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` is set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`.

Analogous to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`, when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` is set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`. This key will only be present for devices which advertise the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR:kotlin.Int` capability or devices where `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getAvailableCaptureRequestKeys()` lists `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`.

**Units**: Pixel coordinates on the image sensor

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`

### SENSOR_INFO_SENSITIVITY_RANGE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_SENSITIVITY_RANGE: CameraCharacteristics.Key<Range<Int!>!>
```

Range of sensitivities for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key` supported by this camera device.

The values are the standard ISO sensitivity values, as defined in ISO 12232:2006.

**Range of valid values:** 
Min \<= 100, Max \>= 800

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`

### SENSOR_INFO_TIMESTAMP_SOURCE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_TIMESTAMP_SOURCE: CameraCharacteristics.Key<Int!>
```

The time base source for sensor capture start timestamps.

The timestamps provided for captures are always in nanoseconds and monotonic, but may not based on a time source that can be compared to other system time sources.

This characteristic defines the source for the timestamps, and therefore whether they can be compared against other system time sources/timestamps.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_TIMESTAMP_SOURCE_UNKNOWN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_TIMESTAMP_SOURCE_REALTIME:kotlin.Int`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_TIMESTAMP_SOURCE_UNKNOWN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_TIMESTAMP_SOURCE_REALTIME:kotlin.Int`

### SENSOR_INFO_WHITE_LEVEL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_WHITE_LEVEL: CameraCharacteristics.Key<Int!>
```

Maximum raw value output by sensor.

This specifies the fully-saturated encoding level for the raw sample values from the sensor. This is typically caused by the sensor becoming highly non-linear or clipping. The minimum for each channel is specified by the offset in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_BLACK_LEVEL_PATTERN:android.hardware.camera2.CameraCharacteristics.Key` key.

The white level is typically determined either by sensor bit depth (8-14 bits is expected), or by the point where the sensor response becomes too non-linear to be useful. The default value for this is maximum representable value for a 16-bit raw sample (2\^16 - 1).

The white level values of captured images may vary for different capture settings (e.g., `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`). This key represents a coarse approximation for such case. It is recommended to use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_DYNAMIC_WHITE_LEVEL:android.hardware.camera2.CaptureResult.Key` for captures when supported by the camera device, which provides more accurate white level values.

**Range of valid values:** 
\> 255 (8-bit output)

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_BLACK_LEVEL_PATTERN:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_DYNAMIC_WHITE_LEVEL:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`

### SENSOR_MAX_ANALOG_SENSITIVITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_MAX_ANALOG_SENSITIVITY: CameraCharacteristics.Key<Int!>
```

Maximum sensitivity that is implemented purely through analog gain.

For `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key` values less than or equal to this, all applied gain must be analog. For values above this, the gain applied can be a mix of analog and digital.

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`

### SENSOR_OPTICAL_BLACK_REGIONS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_OPTICAL_BLACK_REGIONS: CameraCharacteristics.Key<Array<Rect!>!>
```

List of disjoint rectangles indicating the sensor optically shielded black pixel regions.

In most camera sensors, the active array is surrounded by some optically shielded pixel areas. By blocking light, these pixels provides a reliable black reference for black level compensation in active array region.

This key provides a list of disjoint rectangles specifying the regions of optically shielded (with metal shield) black pixel regions if the camera device is capable of reading out these black pixels in the output raw images. In comparison to the fixed black level values reported by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_BLACK_LEVEL_PATTERN:android.hardware.camera2.CameraCharacteristics.Key`, this key may provide a more accurate way for the application to calculate black level of each captured raw images.

When this key is reported, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_DYNAMIC_BLACK_LEVEL:android.hardware.camera2.CaptureResult.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_DYNAMIC_WHITE_LEVEL:android.hardware.camera2.CaptureResult.Key` will also be reported.

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_BLACK_LEVEL_PATTERN:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_DYNAMIC_BLACK_LEVEL:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_DYNAMIC_WHITE_LEVEL:android.hardware.camera2.CaptureResult.Key`

### SENSOR_ORIENTATION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_ORIENTATION: CameraCharacteristics.Key<Int!>
```

Clockwise angle through which the output image needs to be rotated to be upright on the device screen in its native orientation.

Also defines the direction of rolling shutter readout, which is from top to bottom in the sensor's coordinate system.

Starting with Android API level 32, camera clients that query the orientation via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#get(android.hardware.camera2.CameraCharacteristics.Key)` on foldable devices which include logical cameras can receive a value that can dynamically change depending on the device/fold state. Clients are advised to not cache or store the orientation value of such logical sensors. In case repeated queries to CameraCharacteristics are not preferred, then clients can also access the entire mapping from device state to sensor orientation in `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DeviceStateSensorOrientationMap`. Do note that a dynamically changing sensor orientation value in camera characteristics will not be the best way to establish the orientation per frame. Clients that want to know the sensor orientation of a particular captured frame should query the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#LOGICAL_MULTI_CAMERA_ACTIVE_PHYSICAL_ID:android.hardware.camera2.CaptureResult.Key` from the corresponding capture result and check the respective physical camera orientation.

**Units**: Degrees of clockwise rotation; always a multiple of 90

**Range of valid values:** 
0, 90, 180, 270

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#LOGICAL_MULTI_CAMERA_ACTIVE_PHYSICAL_ID:android.hardware.camera2.CaptureResult.Key`

### SENSOR_READOUT_TIMESTAMP

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_READOUT_TIMESTAMP: CameraCharacteristics.Key<Int!>
```

Whether or not the camera device supports readout timestamp and `onReadoutStarted` callback.

If this tag is `HARDWARE`, the camera device calls `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback#onReadoutStarted(android.hardware.camera2.CameraCaptureSession,%20android.hardware.camera2.CaptureRequest,%20kotlin.Long,%20kotlin.Long)` in addition to the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback#onCaptureStarted(android.hardware.camera2.CameraCaptureSession,%20android.hardware.camera2.CaptureRequest,%20kotlin.Long,%20kotlin.Long)` callback for each capture. The timestamp passed into the callback is the start of camera image readout rather than the start of the exposure. The timestamp source of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback#onReadoutStarted(android.hardware.camera2.CameraCaptureSession,%20android.hardware.camera2.CaptureRequest,%20kotlin.Long,%20kotlin.Long)` is the same as that of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback#onCaptureStarted(android.hardware.camera2.CameraCaptureSession,%20android.hardware.camera2.CaptureRequest,%20kotlin.Long,%20kotlin.Long)`.

In addition, the application can switch an output surface's timestamp from start of exposure to start of readout by calling `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#setReadoutTimestampEnabled(kotlin.Boolean)`.

The readout timestamp is beneficial for video recording, because the encoder favors uniform timestamps, and the readout timestamps better reflect the cadence camera sensors output data.

Note that the camera device produces the start-of-exposure and start-of-readout callbacks together. As a result, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback#onReadoutStarted(android.hardware.camera2.CameraCaptureSession,%20android.hardware.camera2.CaptureRequest,%20kotlin.Long,%20kotlin.Long)` is called right after `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback#onCaptureStarted(android.hardware.camera2.CameraCaptureSession,%20android.hardware.camera2.CaptureRequest,%20kotlin.Long,%20kotlin.Long)`. The difference in start-of-readout and start-of-exposure is the sensor exposure time, plus certain constant offset. The offset is usually due to camera sensor level crop, and it is generally constant over time for the same set of output resolutions and capture settings.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_READOUT_TIMESTAMP_NOT_SUPPORTED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_READOUT_TIMESTAMP_HARDWARE:kotlin.Int`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_READOUT_TIMESTAMP_NOT_SUPPORTED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_READOUT_TIMESTAMP_HARDWARE:kotlin.Int`

### SENSOR_REFERENCE_ILLUMINANT1

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_REFERENCE_ILLUMINANT1: CameraCharacteristics.Key<Int!>
```

The standard reference illuminant used as the scene light source when calculating the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_COLOR_TRANSFORM1:android.hardware.camera2.CameraCharacteristics.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_CALIBRATION_TRANSFORM1:android.hardware.camera2.CameraCharacteristics.Key`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_FORWARD_MATRIX1:android.hardware.camera2.CameraCharacteristics.Key` matrices.

The values in this key correspond to the values defined for the EXIF LightSource tag. These illuminants are standard light sources that are often used calibrating camera devices.

If this key is present, then `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_COLOR_TRANSFORM1:android.hardware.camera2.CameraCharacteristics.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_CALIBRATION_TRANSFORM1:android.hardware.camera2.CameraCharacteristics.Key`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_FORWARD_MATRIX1:android.hardware.camera2.CameraCharacteristics.Key` will also be present.

Some devices may choose to provide a second set of calibration information for improved quality, including `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT2:android.hardware.camera2.CameraCharacteristics.Key` and its corresponding matrices.

Starting from Android Q, this key will not be present for a MONOCHROME camera, even if the camera device has RAW capability.

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_DAYLIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_FLUORESCENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_TUNGSTEN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_FLASH:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_FINE_WEATHER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_CLOUDY_WEATHER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_SHADE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_DAYLIGHT_FLUORESCENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_DAY_WHITE_FLUORESCENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_COOL_WHITE_FLUORESCENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_WHITE_FLUORESCENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_STANDARD_A:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_STANDARD_B:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_STANDARD_C:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_D55:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_D65:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_D75:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_D50:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_ISO_STUDIO_TUNGSTEN:kotlin.Int`

**Optional** - The value for this key may be `null` on some devices.

**Permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` is needed to access this property**
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_CALIBRATION_TRANSFORM1:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_COLOR_TRANSFORM1:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_FORWARD_MATRIX1:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT2:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_DAYLIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_FLUORESCENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_TUNGSTEN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_FLASH:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_FINE_WEATHER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_CLOUDY_WEATHER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_SHADE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_DAYLIGHT_FLUORESCENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_DAY_WHITE_FLUORESCENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_COOL_WHITE_FLUORESCENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_WHITE_FLUORESCENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_STANDARD_A:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_STANDARD_B:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_STANDARD_C:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_D55:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_D65:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_D75:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_D50:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_ISO_STUDIO_TUNGSTEN:kotlin.Int`

### SENSOR_REFERENCE_ILLUMINANT2

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_REFERENCE_ILLUMINANT2: CameraCharacteristics.Key<Byte!>
```

The standard reference illuminant used as the scene light source when calculating the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_COLOR_TRANSFORM2:android.hardware.camera2.CameraCharacteristics.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_CALIBRATION_TRANSFORM2:android.hardware.camera2.CameraCharacteristics.Key`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_FORWARD_MATRIX2:android.hardware.camera2.CameraCharacteristics.Key` matrices.

See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key` for more details.

If this key is present, then `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_COLOR_TRANSFORM2:android.hardware.camera2.CameraCharacteristics.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_CALIBRATION_TRANSFORM2:android.hardware.camera2.CameraCharacteristics.Key`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_FORWARD_MATRIX2:android.hardware.camera2.CameraCharacteristics.Key` will also be present.

Starting from Android Q, this key will not be present for a MONOCHROME camera, even if the camera device has RAW capability.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

**Optional** - The value for this key may be `null` on some devices.

**Permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String` is needed to access this property**
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_CALIBRATION_TRANSFORM2:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_COLOR_TRANSFORM2:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_FORWARD_MATRIX2:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

### SHADING_AVAILABLE_MODES

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SHADING_AVAILABLE_MODES: CameraCharacteristics.Key<IntArray!>
```

List of lens shading modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SHADING_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

This list contains lens shading modes that can be set for the camera device. Camera devices that support the MANUAL_POST_PROCESSING capability will always list OFF and FAST mode. This includes all FULL level devices. LEGACY devices will always only support FAST mode.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SHADING_MODE:android.hardware.camera2.CaptureRequest.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SHADING_MODE:android.hardware.camera2.CaptureRequest.Key`

### STATISTICS_INFO_AVAILABLE_FACE_DETECT_MODES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATISTICS_INFO_AVAILABLE_FACE_DETECT_MODES: CameraCharacteristics.Key<IntArray!>
```

List of face detection modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_FACE_DETECT_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

OFF is always supported.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_FACE_DETECT_MODE:android.hardware.camera2.CaptureRequest.Key`

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_FACE_DETECT_MODE:android.hardware.camera2.CaptureRequest.Key`

### STATISTICS_INFO_AVAILABLE_HOT_PIXEL_MAP_MODES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATISTICS_INFO_AVAILABLE_HOT_PIXEL_MAP_MODES: CameraCharacteristics.Key<BooleanArray!>
```

List of hot pixel map output modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_HOT_PIXEL_MAP_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

If no hotpixel map output is available for this camera device, this will contain only `false`.

ON is always supported on devices with the RAW capability.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_HOT_PIXEL_MAP_MODE:android.hardware.camera2.CaptureRequest.Key`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_HOT_PIXEL_MAP_MODE:android.hardware.camera2.CaptureRequest.Key`

### STATISTICS_INFO_AVAILABLE_LENS_SHADING_MAP_MODES

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATISTICS_INFO_AVAILABLE_LENS_SHADING_MAP_MODES: CameraCharacteristics.Key<IntArray!>
```

List of lens shading map output modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_LENS_SHADING_MAP_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

If no lens shading map output is available for this camera device, this key will contain only OFF.

ON is always supported on devices with the RAW capability. LEGACY mode devices will always only support OFF.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_LENS_SHADING_MAP_MODE:android.hardware.camera2.CaptureRequest.Key`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_LENS_SHADING_MAP_MODE:android.hardware.camera2.CaptureRequest.Key`

### STATISTICS_INFO_AVAILABLE_OIS_DATA_MODES

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATISTICS_INFO_AVAILABLE_OIS_DATA_MODES: CameraCharacteristics.Key<IntArray!>
```

List of OIS data output modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_OIS_DATA_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

If no OIS data output is available for this camera device, this key will contain only OFF.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_OIS_DATA_MODE:android.hardware.camera2.CaptureRequest.Key`

**Optional** - The value for this key may be `null` on some devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_OIS_DATA_MODE:android.hardware.camera2.CaptureRequest.Key`

### STATISTICS_INFO_MAX_FACE_COUNT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATISTICS_INFO_MAX_FACE_COUNT: CameraCharacteristics.Key<Int!>
```

The maximum number of simultaneously detectable faces.

**Range of valid values:** 
0 for cameras without available face detection; otherwise: `>=4` for LIMITED or FULL hwlevel devices or `>0` for LEGACY devices.

This key is available on all devices.

### SYNC_MAX_LATENCY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYNC_MAX_LATENCY: CameraCharacteristics.Key<Int!>
```

The maximum number of frames that can occur after a request (different than the previous) has been submitted, and before the result's state becomes synchronized.

This defines the maximum distance (in number of metadata results), between the frame number of the request that has new controls to apply and the frame number of the result that has all the controls applied.

In other words this acts as an upper boundary for how many frames must occur before the camera device knows for a fact that the new submitted camera settings have been applied in outgoing frames.

**Units**: Frame counts

**Possible values:**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SYNC_MAX_LATENCY_PER_FRAME_CONTROL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SYNC_MAX_LATENCY_UNKNOWN:kotlin.Int`

**Available values for this device:** 
A positive value, PER_FRAME_CONTROL, or UNKNOWN.

This key is available on all devices.
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SYNC_MAX_LATENCY_PER_FRAME_CONTROL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SYNC_MAX_LATENCY_UNKNOWN:kotlin.Int`

### TONEMAP_AVAILABLE_TONE_MAP_MODES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TONEMAP_AVAILABLE_TONE_MAP_MODES: CameraCharacteristics.Key<IntArray!>
```

List of tonemapping modes for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key` that are supported by this camera device.

Camera devices that support the MANUAL_POST_PROCESSING capability will always contain at least one of below mode combinations:

- CONTRAST_CURVE, FAST and HIGH_QUALITY
- GAMMA_VALUE, PRESET_CURVE, FAST and HIGH_QUALITY

This includes all FULL level devices.

**Range of valid values:** 
Any value listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key`

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key`

### TONEMAP_MAX_CURVE_POINTS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TONEMAP_MAX_CURVE_POINTS: CameraCharacteristics.Key<Int!>
```

Maximum number of supported points in the tonemap curve that can be used for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_CURVE:android.hardware.camera2.CaptureRequest.Key`.

If the actual number of points provided by the application (in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_CURVE:android.hardware.camera2.CaptureRequest.Key`\*) is less than this maximum, the camera device will resample the curve to its internal representation, using linear interpolation.

The output curves in the result metadata may have a different number of points than the input curves, and will represent the actual hardware curves used as closely as possible when linearly interpolated.

**Optional** - The value for this key may be `null` on some devices.

**Full capability** - Present on all camera devices that report being `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` devices in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` key
**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_CURVE:android.hardware.camera2.CaptureRequest.Key`
