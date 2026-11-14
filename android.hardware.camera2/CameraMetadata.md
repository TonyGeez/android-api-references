Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CameraMetadata

Kotlin | [Java](https://developer.android.com/reference/android/hardware/camera2/CameraMetadata "View this page in Java")
| --- | --- |

```
abstract class CameraMetadata<TKey : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.CameraMetadata](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#) |

| Known Direct Subclasses [CameraCharacteristics](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics), [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest), [CaptureResult](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult) |---|---| | [CameraCharacteristics](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics) | The properties describing a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice`. | | [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest) | An immutable package of settings and outputs needed to capture a single image from the camera device. | | [CaptureResult](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult) | The subset of the results of a single image capture from the image sensor. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [TotalCaptureResult](https://developer.android.com/reference/kotlin/android/hardware/camera2/TotalCaptureResult) |---|---| | [TotalCaptureResult](https://developer.android.com/reference/kotlin/android/hardware/camera2/TotalCaptureResult) | The total assembled results of a single image capture from the image sensor. | |
| --- | --- | --- | --- | --- | --- | --- |

The base class for camera controls and information.

This class defines the basic key/value map used for querying for camera characteristics or capture results, and for setting camera request parameters.

All instances of CameraMetadata are immutable. Beginning with API level 32, the list of keys returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#getKeys()` may change depending on the state of the device, as may the values returned by any key with `get` throughout the lifetime of the object. For information on whether a specific value is fixed, see the documentation for its key.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_FRONT:kotlin.Int` The camera device faces the front of the vehicle body frame. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_LEFT:kotlin.Int` The camera device faces the left side of the vehicle body frame. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_OTHER:kotlin.Int` The camera device faces the outside of the vehicle body frame but not exactly one of the exterior sides defined by this enum. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_REAR:kotlin.Int` The camera device faces the rear of the vehicle body frame. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_EXTERIOR_RIGHT:kotlin.Int` The camera device faces the right side of the vehicle body frame. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_OTHER:kotlin.Int` The camera device faces the inside of the vehicle body frame but not exactly one of seats described by this enum. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_1_CENTER:kotlin.Int` The camera device faces the center seat of the first row. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_1_LEFT:kotlin.Int` The camera device faces the left side seat of the first row. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_1_RIGHT:kotlin.Int` The camera device faces the right seat of the first row. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_2_CENTER:kotlin.Int` The camera device faces the center seat of the second row. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_2_LEFT:kotlin.Int` The camera device faces the left side seat of the second row. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_2_RIGHT:kotlin.Int` The camera device faces the right side seat of the second row. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_3_CENTER:kotlin.Int` The camera device faces the center seat of the third row. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_3_LEFT:kotlin.Int` The camera device faces the left side seat of the third row. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_3_RIGHT:kotlin.Int` The camera device faces the right seat of the third row. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_FRONT:kotlin.Int` The camera device exists outside of the vehicle body frame and on its front side. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_LEFT:kotlin.Int` The camera device exists outside and on left side of the vehicle body frame. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_OTHER:kotlin.Int` The camera exists outside of the vehicle body frame but not exactly on one of the exterior locations this enum defines. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_REAR:kotlin.Int` The camera device exists outside of the vehicle body frame and on its rear side. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTERIOR_RIGHT:kotlin.Int` The camera device exists outside and on right side of the vehicle body frame. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_FRONT:kotlin.Int` The camera device exists outside of the extra vehicle's body frame and on its front side. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_LEFT:kotlin.Int` The camera device exists outside and on left side of the extra vehicle body. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_OTHER:kotlin.Int` The camera device exists on an extra vehicle, such as the trailer, but not exactly on one of front, rear, left, or right side. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_REAR:kotlin.Int` The camera device exists outside of the extra vehicle's body frame and on its rear side. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_EXTRA_RIGHT:kotlin.Int` The camera device exists outside and on right side of the extra vehicle body. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#AUTOMOTIVE_LOCATION_INTERIOR:kotlin.Int` The camera device exists inside of the vehicle cabin. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_ABERRATION_MODE_FAST:kotlin.Int` Aberration correction will not slow down capture rate relative to sensor raw output. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_ABERRATION_MODE_HIGH_QUALITY:kotlin.Int` Aberration correction operates at improved quality but the capture rate might be reduced (relative to sensor raw output rate) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_ABERRATION_MODE_OFF:kotlin.Int` No aberration correction is applied. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_MODE_CCT:kotlin.Int` Use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_COLOR_TEMPERATURE:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_COLOR_TINT:android.hardware.camera2.CaptureRequest.Key` to adjust the white balance based on correlated color temperature. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_MODE_FAST:kotlin.Int` Color correction processing must not slow down capture rate relative to sensor raw output. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_MODE_HIGH_QUALITY:kotlin.Int` Color correction processing operates at improved quality but the capture rate might be reduced (relative to sensor raw output rate) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#COLOR_CORRECTION_MODE_TRANSFORM_MATRIX:kotlin.Int` Use the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` matrix and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` to do color conversion. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_ANTIBANDING_MODE_50HZ:kotlin.Int` The camera device will adjust exposure duration to avoid banding problems with 50Hz illumination sources. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_ANTIBANDING_MODE_60HZ:kotlin.Int` The camera device will adjust exposure duration to avoid banding problems with 60Hz illumination sources. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_ANTIBANDING_MODE_AUTO:kotlin.Int` The camera device will automatically adapt its antibanding routine to the current illumination condition. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_ANTIBANDING_MODE_OFF:kotlin.Int` The camera device will not adjust exposure duration to avoid banding problems. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_OFF:kotlin.Int` The camera device's autoexposure routine is disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON:kotlin.Int` The camera device's autoexposure routine is active, with no flash control. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_ALWAYS_FLASH:kotlin.Int` Like ON, except that the camera device also controls the camera's flash unit, always firing it for still captures. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_AUTO_FLASH:kotlin.Int` Like ON, except that the camera device also controls the camera's flash unit, firing it in low-light conditions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_AUTO_FLASH_REDEYE:kotlin.Int` Like ON_AUTO_FLASH, but with automatic red eye reduction. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_EXTERNAL_FLASH:kotlin.Int` An external flash has been turned on. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_MODE_ON_LOW_LIGHT_BOOST_BRIGHTNESS_PRIORITY:kotlin.Int` Like 'ON' but applies additional brightness boost in low light scenes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRECAPTURE_TRIGGER_CANCEL:kotlin.Int` The camera device will cancel any currently active or completed precapture metering sequence, the auto-exposure routine will return to its initial state. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRECAPTURE_TRIGGER_IDLE:kotlin.Int` The trigger is idle. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRECAPTURE_TRIGGER_START:kotlin.Int` The precapture metering sequence will be started by the camera device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRIORITY_MODE_OFF:kotlin.Int` Disable AE priority mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRIORITY_MODE_SENSOR_EXPOSURE_TIME_PRIORITY:kotlin.Int` The camera device's auto-exposure routine is active and prioritizes the application-selected exposure time (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_PRIORITY_MODE_SENSOR_SENSITIVITY_PRIORITY:kotlin.Int` The camera device's auto-exposure routine is active and prioritizes the application-selected ISO (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_STATE_CONVERGED:kotlin.Int` AE has a good set of control values for the current scene. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_STATE_FLASH_REQUIRED:kotlin.Int` AE has a good set of control values, but flash needs to be fired for good quality still capture. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_STATE_INACTIVE:kotlin.Int` AE is off or recently reset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_STATE_LOCKED:kotlin.Int` AE has been locked. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_STATE_PRECAPTURE:kotlin.Int` AE has been asked to do a precapture sequence and is currently executing it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AE_STATE_SEARCHING:kotlin.Int` AE doesn't yet have a good set of control values for the current scene. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_AUTO:kotlin.Int` Basic automatic focus mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_CONTINUOUS_PICTURE:kotlin.Int` In this mode, the AF algorithm modifies the lens position continually to attempt to provide a constantly-in-focus image stream. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_CONTINUOUS_VIDEO:kotlin.Int` In this mode, the AF algorithm modifies the lens position continually to attempt to provide a constantly-in-focus image stream. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_EDOF:kotlin.Int` Extended depth of field (digital focus) mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_MACRO:kotlin.Int` Close-up focusing mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_MODE_OFF:kotlin.Int` The auto-focus routine does not control the lens; `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key` is controlled by the application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_SCENE_CHANGE_DETECTED:kotlin.Int` Scene change is detected within the AF region(s). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_SCENE_CHANGE_NOT_DETECTED:kotlin.Int` Scene change is not detected within the AF region(s). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_STATE_ACTIVE_SCAN:kotlin.Int` AF is performing an AF scan because it was triggered by AF trigger. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_STATE_FOCUSED_LOCKED:kotlin.Int` AF believes it is focused correctly and has locked focus. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_STATE_INACTIVE:kotlin.Int` AF is off or has not yet tried to scan/been asked to scan. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_STATE_NOT_FOCUSED_LOCKED:kotlin.Int` AF has failed to focus successfully and has locked focus. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_STATE_PASSIVE_FOCUSED:kotlin.Int` AF currently believes it is in focus, but may restart scanning at any time. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_STATE_PASSIVE_SCAN:kotlin.Int` AF is currently performing an AF scan initiated the camera device in a continuous autofocus mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_STATE_PASSIVE_UNFOCUSED:kotlin.Int` AF finished a passive scan without finding focus, and may restart scanning at any time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_TRIGGER_CANCEL:kotlin.Int` Autofocus will return to its initial state, and cancel any currently active trigger. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_TRIGGER_IDLE:kotlin.Int` The trigger is idle. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AF_TRIGGER_START:kotlin.Int` Autofocus will trigger now. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AUTOFRAMING_OFF:kotlin.Int` Disable autoframing. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AUTOFRAMING_ON:kotlin.Int` Enable autoframing to keep people in the frame's field of view. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AUTOFRAMING_STATE_CONVERGED:kotlin.Int` Auto-framing has reached a stable state (frame/fov is not being adjusted). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AUTOFRAMING_STATE_FRAMING:kotlin.Int` Auto-framing is in process - either zooming in, zooming out or pan is taking place. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AUTOFRAMING_STATE_INACTIVE:kotlin.Int` Auto-framing is inactive. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_AUTO:kotlin.Int` The camera device's auto-white balance routine is active. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_CLOUDY_DAYLIGHT:kotlin.Int` The camera device's auto-white balance routine is disabled; the camera device uses cloudy daylight light as the assumed scene illumination for white balance. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_DAYLIGHT:kotlin.Int` The camera device's auto-white balance routine is disabled; the camera device uses daylight light as the assumed scene illumination for white balance. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_FLUORESCENT:kotlin.Int` The camera device's auto-white balance routine is disabled; the camera device uses fluorescent light as the assumed scene illumination for white balance. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_INCANDESCENT:kotlin.Int` The camera device's auto-white balance routine is disabled; the camera device uses incandescent light as the assumed scene illumination for white balance. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_OFF:kotlin.Int` The camera device's auto-white balance routine is disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_SHADE:kotlin.Int` The camera device's auto-white balance routine is disabled; the camera device uses shade light as the assumed scene illumination for white balance. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_TWILIGHT:kotlin.Int` The camera device's auto-white balance routine is disabled; the camera device uses twilight light as the assumed scene illumination for white balance. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_MODE_WARM_FLUORESCENT:kotlin.Int` The camera device's auto-white balance routine is disabled; the camera device uses warm fluorescent light as the assumed scene illumination for white balance. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_STATE_CONVERGED:kotlin.Int` AWB has a good set of control values for the current scene. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_STATE_INACTIVE:kotlin.Int` AWB is not in auto mode, or has not yet started metering. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_STATE_LOCKED:kotlin.Int` AWB has been locked. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_AWB_STATE_SEARCHING:kotlin.Int` AWB doesn't yet have a good set of control values for the current scene. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_CUSTOM:kotlin.Int` The goal of this request doesn't fall into the other categories. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_MANUAL:kotlin.Int` This request is for manual capture use case where the applications want to directly control the capture parameters. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_MOTION_TRACKING:kotlin.Int` This request is for a motion tracking use case, where the application will use camera and inertial sensor data to locate and track objects in the world. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_PREVIEW:kotlin.Int` This request is for a preview-like use case. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_STILL_CAPTURE:kotlin.Int` This request is for a still capture-type use case. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_VIDEO_RECORD:kotlin.Int` This request is for a video recording use case. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_VIDEO_SNAPSHOT:kotlin.Int` This request is for a video snapshot (still image while recording video) use case. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_CAPTURE_INTENT_ZERO_SHUTTER_LAG:kotlin.Int` This request is for a ZSL usecase; the application will stream full-resolution images and reprocess one or several later for a final capture. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_AQUA:kotlin.Int` An "aqua" effect where a blue hue is added to the image. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_BLACKBOARD:kotlin.Int` A "blackboard" effect where the image is typically displayed as regions of black, with white or grey details. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_MONO:kotlin.Int` A "monocolor" effect where the image is mapped into a single color. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_NEGATIVE:kotlin.Int` A "photo-negative" effect where the image's colors are inverted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_OFF:kotlin.Int` No color effect will be applied. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_POSTERIZE:kotlin.Int` A "posterization" effect where the image uses discrete regions of tone rather than a continuous gradient of tones. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_SEPIA:kotlin.Int` A "sepia" effect where the image is mapped into warm gray, red, and brown tones. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_SOLARIZE:kotlin.Int` A "solarisation" effect (Sabattier effect) where the image is wholly or partially reversed in tone. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EFFECT_MODE_WHITEBOARD:kotlin.Int` A "whiteboard" effect where the image is typically displayed as regions of white, with black or grey details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EXTENDED_SCENE_MODE_BOKEH_CONTINUOUS:kotlin.Int` Bokeh effect must not slow down capture rate relative to sensor raw output, and the effect is applied to all processed streams no larger than the maximum streaming dimension. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EXTENDED_SCENE_MODE_BOKEH_STILL_CAPTURE:kotlin.Int` High quality bokeh mode is enabled for all non-raw streams (including YUV, JPEG, and IMPLEMENTATION_DEFINED) when capture intent is STILL_CAPTURE. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_EXTENDED_SCENE_MODE_DISABLED:kotlin.Int` Extended scene mode is disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_LOW_LIGHT_BOOST_STATE_ACTIVE:kotlin.Int` The AE mode 'ON_LOW_LIGHT_BOOST_BRIGHTNESS_PRIORITY' is enabled and applied. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_LOW_LIGHT_BOOST_STATE_INACTIVE:kotlin.Int` The AE mode 'ON_LOW_LIGHT_BOOST_BRIGHTNESS_PRIORITY' is enabled but not applied. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_AUTO:kotlin.Int` Use settings for each individual 3A routine. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_OFF:kotlin.Int` Full application control of pipeline. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_OFF_KEEP_STATE:kotlin.Int` Same as OFF mode, except that this capture will not be used by camera device background auto-exposure, auto-white balance and auto-focus algorithms (3A) to update their statistics. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_USE_EXTENDED_SCENE_MODE:kotlin.Int` Use a specific extended scene mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_MODE_USE_SCENE_MODE:kotlin.Int` Use a specific scene mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_ACTION:kotlin.Int` Optimized for photos of quickly moving objects. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_BARCODE:kotlin.Int` Optimized for accurately capturing a photo of barcode for use by camera applications that wish to read the barcode value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_BEACH:kotlin.Int` Optimized for bright, outdoor beach settings. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_CANDLELIGHT:kotlin.Int` Optimized for dim settings where the main light source is a candle. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_DISABLED:kotlin.Int` Indicates that no scene modes are set for a given capture request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_FACE_PRIORITY:kotlin.Int` If face detection support exists, use face detection data for auto-focus, auto-white balance, and auto-exposure routines. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_FIREWORKS:kotlin.Int` Optimized for nighttime photos of fireworks. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_HDR:kotlin.Int` Turn on a device-specific high dynamic range (HDR) mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_HIGH_SPEED_VIDEO:kotlin.Int` This is deprecated, please use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createConstrainedHighSpeedCaptureSession(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraConstrainedHighSpeedCaptureSession#createHighSpeedRequestList(android.hardware.camera2.CaptureRequest)` for high speed video recording. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_LANDSCAPE:kotlin.Int` Optimized for photos of distant macroscopic objects. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_NIGHT:kotlin.Int` Optimized for low-light settings. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_NIGHT_PORTRAIT:kotlin.Int` Optimized for still photos of people in low-light settings. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_PARTY:kotlin.Int` Optimized for dim, indoor settings with multiple moving people. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_PORTRAIT:kotlin.Int` Optimized for still photos of people. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_SNOW:kotlin.Int` Optimized for bright, outdoor settings containing snow. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_SPORTS:kotlin.Int` Optimized for photos of quickly moving people. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_STEADYPHOTO:kotlin.Int` Optimized to avoid blurry photos due to small amounts of device motion (for example: due to hand shake). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_SUNSET:kotlin.Int` Optimized for scenes of the setting sun. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SCENE_MODE_THEATRE:kotlin.Int` Optimized for dim, indoor settings where flash must remain off. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SETTINGS_OVERRIDE_OFF:kotlin.Int` No keys are applied sooner than the other keys when applying CaptureRequest settings to the camera device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_SETTINGS_OVERRIDE_ZOOM:kotlin.Int` Zoom related keys are applied sooner than the other keys in the CaptureRequest. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_VIDEO_STABILIZATION_MODE_OFF:kotlin.Int` Video stabilization is disabled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_VIDEO_STABILIZATION_MODE_ON:kotlin.Int` Video stabilization is enabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_VIDEO_STABILIZATION_MODE_PREVIEW_STABILIZATION:kotlin.Int` Preview stabilization, where the preview in addition to all other non-RAW streams are stabilized with the same quality of stabilization, is enabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_ZOOM_METHOD_AUTO:kotlin.Int` The camera device automatically detects whether the application does zoom with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`, and in turn decides which metadata tag reflects the effective zoom level. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#CONTROL_ZOOM_METHOD_ZOOM_RATIO:kotlin.Int` The application intends to control zoom via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`, and the effective zoom level is reflected by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` in capture results. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#DISTORTION_CORRECTION_MODE_FAST:kotlin.Int` Lens distortion correction is applied without reducing frame rate relative to sensor output. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#DISTORTION_CORRECTION_MODE_HIGH_QUALITY:kotlin.Int` High-quality distortion correction is applied, at the cost of possibly reduced frame rate relative to sensor output. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#DISTORTION_CORRECTION_MODE_OFF:kotlin.Int` No distortion correction is applied. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EDGE_MODE_FAST:kotlin.Int` Apply edge enhancement at a quality level that does not slow down frame rate relative to sensor output. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EDGE_MODE_HIGH_QUALITY:kotlin.Int` Apply high-quality edge enhancement, at a cost of possibly reduced output frame rate. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EDGE_MODE_OFF:kotlin.Int` No edge enhancement is applied. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EDGE_MODE_ZERO_SHUTTER_LAG:kotlin.Int` Edge enhancement is applied at different levels for different output streams, based on resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EXTENSION_NIGHT_MODE_INDICATOR_OFF:kotlin.Int` The camera has detected lighting conditions that are sufficiently bright. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EXTENSION_NIGHT_MODE_INDICATOR_ON:kotlin.Int` The camera has detected low-light conditions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#EXTENSION_NIGHT_MODE_INDICATOR_UNKNOWN:kotlin.Int` The camera can't accurately assess the scene's lighting to determine if a Night Mode Camera Extension capture would improve the photo. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_MODE_OFF:kotlin.Int` Do not fire the flash for this capture. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_MODE_SINGLE:kotlin.Int` If the flash is available and charged, fire flash for this capture. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_MODE_TORCH:kotlin.Int` Transition flash to continuously on. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_STATE_CHARGING:kotlin.Int` Flash is charging and cannot be fired. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_STATE_FIRED:kotlin.Int` Flash fired for this capture. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_STATE_PARTIAL:kotlin.Int` Flash partially illuminated this frame. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_STATE_READY:kotlin.Int` Flash is ready to fire. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#FLASH_STATE_UNAVAILABLE:kotlin.Int` No flash on camera. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#HOT_PIXEL_MODE_FAST:kotlin.Int` Hot pixel correction is applied, without reducing frame rate relative to sensor raw output. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#HOT_PIXEL_MODE_HIGH_QUALITY:kotlin.Int` High-quality hot pixel correction is applied, at a cost of possibly reduced frame rate relative to sensor raw output. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#HOT_PIXEL_MODE_OFF:kotlin.Int` No hot pixel correction is applied. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_DEVICE_TYPE_BUILT_IN:kotlin.Int` This camera device is physically a part of this Android device, and the data produced is always within the device's control before it reaches the application requesting it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_DEVICE_TYPE_EXTERNAL:kotlin.Int` This camera device is not permanently connected to this Android device. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_DEVICE_TYPE_UNKNOWN:kotlin.Int` This camera device has an unknown classification. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_DEVICE_TYPE_VIRTUAL:kotlin.Int` This camera device produces purely virtual images, though they may be based on the output of a real hardware camera in some cases. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_3:kotlin.Int` This camera device is capable of YUV reprocessing and RAW data capture, in addition to FULL-level capabilities. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_EXTERNAL:kotlin.Int` This camera device is backed by an external camera connected to this Android device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_FULL:kotlin.Int` This camera device is capable of supporting advanced imaging applications. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LEGACY:kotlin.Int` This camera device is running in backward compatibility mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED:kotlin.Int` This camera device does not have enough capabilities to qualify as a `FULL` device or better. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_FACING_BACK:kotlin.Int` The camera device faces the opposite direction as the device's screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_FACING_EXTERNAL:kotlin.Int` The camera device is an external camera, and has no fixed facing relative to the device's screen. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_FACING_FRONT:kotlin.Int` The camera device faces the same direction as the device's screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_INFO_FOCUS_DISTANCE_CALIBRATION_APPROXIMATE:kotlin.Int` The lens focus distance is measured in diopters. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_INFO_FOCUS_DISTANCE_CALIBRATION_CALIBRATED:kotlin.Int` The lens focus distance is measured in diopters, and is calibrated. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_INFO_FOCUS_DISTANCE_CALIBRATION_UNCALIBRATED:kotlin.Int` The lens focus distance is not accurate, and the units used for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key` do not correspond to any physical units. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_OPTICAL_STABILIZATION_MODE_OFF:kotlin.Int` Optical stabilization is unavailable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_OPTICAL_STABILIZATION_MODE_ON:kotlin.Int` Optical stabilization is enabled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_POSE_REFERENCE_AUTOMOTIVE:kotlin.Int` The value of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` is relative to the origin of the automotive sensor coordinate system, which is at the center of the rear axle. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_POSE_REFERENCE_GYROSCOPE:kotlin.Int` The value of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` is relative to the position of the primary gyroscope of this Android device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_POSE_REFERENCE_PRIMARY_CAMERA:kotlin.Int` The value of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` is relative to the optical center of the largest camera device facing the same direction as this camera. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_POSE_REFERENCE_UNDEFINED:kotlin.Int` The camera device cannot represent the values of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key` accurately enough. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_STATE_MOVING:kotlin.Int` One or several of the lens parameters (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FILTER_DENSITY:android.hardware.camera2.CaptureRequest.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_APERTURE:android.hardware.camera2.CaptureRequest.Key`) is currently changing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LENS_STATE_STATIONARY:kotlin.Int` The lens parameters (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FILTER_DENSITY:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_APERTURE:android.hardware.camera2.CaptureRequest.Key`) are not changing. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LOGICAL_MULTI_CAMERA_SENSOR_SYNC_TYPE_APPROXIMATE:kotlin.Int` A software mechanism is used to synchronize between the physical cameras. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#LOGICAL_MULTI_CAMERA_SENSOR_SYNC_TYPE_CALIBRATED:kotlin.Int` The camera device supports frame timestamp synchronization at the hardware level, and the timestamp of a physical stream image accurately reflects its start-of-exposure time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_FAST:kotlin.Int` Noise reduction is applied without reducing frame rate relative to sensor output. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_HIGH_QUALITY:kotlin.Int` High-quality noise reduction is applied, at the cost of possibly reduced frame rate relative to sensor output. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_MINIMAL:kotlin.Int` MINIMAL noise reduction is applied without reducing frame rate relative to sensor output. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_OFF:kotlin.Int` No noise reduction is applied. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#NOISE_REDUCTION_MODE_ZERO_SHUTTER_LAG:kotlin.Int` Noise reduction is applied at different levels for different output streams, based on resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_BACKWARD_COMPATIBLE:kotlin.Int` The minimal set of capabilities that every camera device (regardless of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`) supports. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_BURST_CAPTURE:kotlin.Int` The camera device supports capturing high-resolution images at \>= 20 frames per second, in at least the uncompressed YUV format, when post-processing settings are set to FAST. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_COLOR_SPACE_PROFILES:kotlin.Int` The device supports querying the possible combinations of color spaces, image formats, and dynamic range profiles supported by the camera and requesting a particular color space for a session via `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setColorSpace(android.graphics.ColorSpace.Named)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_CONSTRAINED_HIGH_SPEED_VIDEO:kotlin.Int` The device supports constrained high speed video recording (frame rate \>=120fps) use case. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_DEPTH_OUTPUT:kotlin.Int` The camera device can produce depth measurements from its field of view. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_DYNAMIC_RANGE_TEN_BIT:kotlin.Int` The device supports one or more 10-bit camera outputs according to the dynamic range profiles specified in `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#getSupportedProfiles()`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_LOGICAL_MULTI_CAMERA:kotlin.Int` The camera device is a logical camera backed by two or more physical cameras. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_MANUAL_POST_PROCESSING:kotlin.Int` The camera device post-processing stages can be manually controlled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_MANUAL_SENSOR:kotlin.Int` The camera device can be manually controlled (3A algorithms such as auto-exposure, and auto-focus can be bypassed). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_MONOCHROME:kotlin.Int` The camera device is a monochrome camera that doesn't contain a color filter array, and for YUV_420_888 stream, the pixel values on U and V planes are all 128. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_MOTION_TRACKING:kotlin.Int` The camera device supports the MOTION_TRACKING value for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key`, which limits maximum exposure time to 20 ms. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_OFFLINE_PROCESSING:kotlin.Int` The camera device supports the OFFLINE_PROCESSING use case. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_PRIVATE_REPROCESSING:kotlin.Int` The camera device supports the Zero Shutter Lag reprocessing use case. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_RAW:kotlin.Int` The camera device supports outputting RAW buffers and metadata for interpreting them. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_READ_SENSOR_SETTINGS:kotlin.Int` The camera device supports accurately reporting the sensor settings for many of the sensor controls while the built-in 3A algorithm is running. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_REMOSAIC_REPROCESSING:kotlin.Int` The device supports reprocessing from the `RAW_SENSOR` format with a bayer pattern given by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_BINNING_FACTOR:android.hardware.camera2.CameraCharacteristics.Key` (m x n group of pixels with the same color filter) to a remosaiced regular bayer pattern. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_SECURE_IMAGE_DATA:kotlin.Int` The camera device is capable of writing image data into a region of memory inaccessible to Android userspace or the Android kernel, and only accessible to trusted execution environments (TEE). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_STREAM_USE_CASE:kotlin.Int` The camera device supports selecting a per-stream use case via `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#setStreamUseCase(kotlin.Long)` so that the device can optimize camera pipeline parameters such as tuning, sensor mode, or ISP settings for a specific user scenario. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_SYSTEM_CAMERA:kotlin.Int` The camera device is only accessible by Android's system components and privileged applications. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR:kotlin.Int` This camera device is capable of producing ultra high resolution images in addition to the image sizes described in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_YUV_REPROCESSING:kotlin.Int` The camera device supports the YUV_420_888 reprocessing use case, similar as PRIVATE_REPROCESSING, This capability requires the camera device to support the following: |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_CROPPED_RAW:kotlin.Int` Cropped RAW stream when the client chooses to crop the field of view. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_DEFAULT:kotlin.Int` Default stream use case. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_PREVIEW:kotlin.Int` Live stream shown to the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_PREVIEW_VIDEO_STILL:kotlin.Int` One single stream used for combined purposes of preview, video, and still capture. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_STILL_CAPTURE:kotlin.Int` Still photo capture. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_VIDEO_CALL:kotlin.Int` Long-running video call optimized for both power efficiency and video quality. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_AVAILABLE_STREAM_USE_CASES_VIDEO_RECORD:kotlin.Int` Recording video clips. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_CROPPING_TYPE_CENTER_ONLY:kotlin.Int` The camera device only supports centered crop regions. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_CROPPING_TYPE_FREEFORM:kotlin.Int` The camera device supports arbitrarily chosen crop regions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_180:kotlin.Int` Processed images are rotated by 180 degrees. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_270:kotlin.Int` Processed images are rotated by 270 degrees clockwise, and then cropped to the original aspect ratio. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_90:kotlin.Int` Processed images are rotated by 90 degrees clockwise, and then cropped to the original aspect ratio. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_AUTO:kotlin.Int` The camera API automatically selects the best concrete value for rotate-and-crop based on the application's support for resizability and the current multi-window mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SCALER_ROTATE_AND_CROP_NONE:kotlin.Int` No rotate and crop is applied. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_BGGR:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_GBRG:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_GRBG:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_MONO:kotlin.Int` Sensor doesn't have any Bayer color filter. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_NIR:kotlin.Int` Sensor has a near infrared filter capturing light with wavelength between roughly 750nm and 1400nm, and the same filter covers the whole sensor array. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_RGB:kotlin.Int` Sensor is not Bayer; output has 3 16-bit values for each pixel, instead of just 1 16-bit value per pixel. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_RGGB:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_TIMESTAMP_SOURCE_REALTIME:kotlin.Int` Timestamps from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_TIMESTAMP:android.hardware.camera2.CaptureResult.Key` are in the same timebase as `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtimeNanos()`, and they can be compared to other timestamps using that base. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_INFO_TIMESTAMP_SOURCE_UNKNOWN:kotlin.Int` Timestamps from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_TIMESTAMP:android.hardware.camera2.CaptureResult.Key` are in nanoseconds and monotonic, but can not be compared to timestamps from other subsystems (e.g. accelerometer, gyro etc.), or other instances of the same or different camera devices in the same system with accuracy. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_DEFAULT:kotlin.Int` This is the default sensor pixel mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int` In this mode, sensors typically do not bin pixels, as a result can offer larger image sizes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_READOUT_TIMESTAMP_HARDWARE:kotlin.Int` This camera device supports the onReadoutStarted callback as well as outputting readout timestamps. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_READOUT_TIMESTAMP_NOT_SUPPORTED:kotlin.Int` This camera device doesn't support readout timestamp and onReadoutStarted callback. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_CLOUDY_WEATHER:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_COOL_WHITE_FLUORESCENT:kotlin.Int` W 3900 - 4500K |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_D50:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_D55:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_D65:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_D75:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_DAYLIGHT:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_DAYLIGHT_FLUORESCENT:kotlin.Int` D 5700 - 7100K |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_DAY_WHITE_FLUORESCENT:kotlin.Int` N 4600 - 5400K |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_FINE_WEATHER:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_FLASH:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_FLUORESCENT:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_ISO_STUDIO_TUNGSTEN:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_SHADE:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_STANDARD_A:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_STANDARD_B:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_STANDARD_C:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_TUNGSTEN:kotlin.Int` Incandescent light |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_REFERENCE_ILLUMINANT1_WHITE_FLUORESCENT:kotlin.Int` WW 3200 - 3700K |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_COLOR_BARS:kotlin.Int` All pixel data is replaced with an 8-bar color pattern. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_COLOR_BARS_FADE_TO_GRAY:kotlin.Int` The test pattern is similar to COLOR_BARS, except that each bar should start at its specified color at the top, and fade to gray at the bottom. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_CUSTOM1:kotlin.Int` The first custom test pattern. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_OFF:kotlin.Int` No test pattern mode is used, and the camera device returns captures from the image sensor. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_PN9:kotlin.Int` All pixel data is replaced by a pseudo-random sequence generated from a PN9 512-bit sequence (typically implemented in hardware with a linear feedback shift register). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_TEST_PATTERN_MODE_SOLID_COLOR:kotlin.Int` Each pixel in `[R, G_even, G_odd, B]` is replaced by its respective color channel provided in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_TEST_PATTERN_DATA:android.hardware.camera2.CaptureRequest.Key`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SHADING_MODE_FAST:kotlin.Int` Apply lens shading corrections, without slowing frame rate relative to sensor raw output |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SHADING_MODE_HIGH_QUALITY:kotlin.Int` Apply high-quality lens shading correction, at the cost of possibly reduced frame rate. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SHADING_MODE_OFF:kotlin.Int` No lens shading correction is applied. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_FACE_DETECT_MODE_FULL:kotlin.Int` Return all face metadata. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_FACE_DETECT_MODE_OFF:kotlin.Int` Do not include face detection statistics in capture results. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_FACE_DETECT_MODE_SIMPLE:kotlin.Int` Return face rectangle and confidence values only. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_LENS_SHADING_MAP_MODE_OFF:kotlin.Int` Do not include a lens shading map in the capture result. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_LENS_SHADING_MAP_MODE_ON:kotlin.Int` Include a lens shading map in the capture result. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_OIS_DATA_MODE_OFF:kotlin.Int` Do not include OIS data in the capture result. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_OIS_DATA_MODE_ON:kotlin.Int` Include OIS data in the capture result. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_SCENE_FLICKER_50HZ:kotlin.Int` The camera device detects illumination flickering at 50Hz in the current scene. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_SCENE_FLICKER_60HZ:kotlin.Int` The camera device detects illumination flickering at 60Hz in the current scene. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#STATISTICS_SCENE_FLICKER_NONE:kotlin.Int` The camera device does not detect any flickering illumination in the current scene. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SYNC_MAX_LATENCY_PER_FRAME_CONTROL:kotlin.Int` Every frame has the requests immediately applied. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SYNC_MAX_LATENCY_UNKNOWN:kotlin.Int` Each new frame has some subset (potentially the entire set) of the past requests applied to the camera settings. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_CONTRAST_CURVE:kotlin.Int` Use the tone mapping curve specified in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_CURVE:android.hardware.camera2.CaptureRequest.Key`\* entries. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_FAST:kotlin.Int` Advanced gamma mapping and color enhancement may be applied, without reducing frame rate compared to raw sensor output. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_GAMMA_VALUE:kotlin.Int` Use the gamma value specified in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_GAMMA:android.hardware.camera2.CaptureRequest.Key` to perform tonemapping. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_HIGH_QUALITY:kotlin.Int` High-quality gamma mapping and color enhancement will be applied, at the cost of possibly reduced frame rate compared to raw sensor output. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_MODE_PRESET_CURVE:kotlin.Int` Use the preset tonemapping curve specified in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_PRESET_CURVE:android.hardware.camera2.CaptureRequest.Key` to perform tonemapping. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_PRESET_CURVE_REC709:kotlin.Int` Tonemapping curve is defined by ITU-R BT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#TONEMAP_PRESET_CURVE_SRGB:kotlin.Int` Tonemapping curve is defined by sRGB |
| --- | --- |

| Public methods ||
|---|---|
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<TKey\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#getKeys()()` Returns a list of the keys contained in this map. |

## Constants

### AUTOMOTIVE_LENS_FACING_EXTERIOR_FRONT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LENS_FACING_EXTERIOR_FRONT: Int
```

The camera device faces the front of the vehicle body frame.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LENS_FACING_EXTERIOR_LEFT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LENS_FACING_EXTERIOR_LEFT: Int
```

The camera device faces the left side of the vehicle body frame.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LENS_FACING_EXTERIOR_OTHER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LENS_FACING_EXTERIOR_OTHER: Int
```

The camera device faces the outside of the vehicle body frame but not exactly one of the exterior sides defined by this enum. Applications should determine the exact facing direction from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LENS_FACING_EXTERIOR_REAR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LENS_FACING_EXTERIOR_REAR: Int
```

The camera device faces the rear of the vehicle body frame.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LENS_FACING_EXTERIOR_RIGHT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LENS_FACING_EXTERIOR_RIGHT: Int
```

The camera device faces the right side of the vehicle body frame.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LENS_FACING_INTERIOR_OTHER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LENS_FACING_INTERIOR_OTHER: Int
```

The camera device faces the inside of the vehicle body frame but not exactly one of seats described by this enum. Applications should determine the exact facing direction from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`.

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_1_CENTER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_1_CENTER: Int
```

The camera device faces the center seat of the first row.

 Value: 7

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_1_LEFT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_1_LEFT: Int
```

The camera device faces the left side seat of the first row.

 Value: 6

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_1_RIGHT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_1_RIGHT: Int
```

The camera device faces the right seat of the first row.

 Value: 8

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_2_CENTER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_2_CENTER: Int
```

The camera device faces the center seat of the second row.

 Value: 10

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_2_LEFT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_2_LEFT: Int
```

The camera device faces the left side seat of the second row.

 Value: 9

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_2_RIGHT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_2_RIGHT: Int
```

The camera device faces the right side seat of the second row.

 Value: 11

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_3_CENTER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_3_CENTER: Int
```

The camera device faces the center seat of the third row.

 Value: 13

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_3_LEFT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_3_LEFT: Int
```

The camera device faces the left side seat of the third row.

 Value: 12

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_3_RIGHT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LENS_FACING_INTERIOR_SEAT_ROW_3_RIGHT: Int
```

The camera device faces the right seat of the third row.

 Value: 14

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LOCATION_EXTERIOR_FRONT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LOCATION_EXTERIOR_FRONT: Int
```

The camera device exists outside of the vehicle body frame and on its front side.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LOCATION:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LOCATION_EXTERIOR_LEFT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LOCATION_EXTERIOR_LEFT: Int
```

The camera device exists outside and on left side of the vehicle body frame.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LOCATION:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LOCATION_EXTERIOR_OTHER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LOCATION_EXTERIOR_OTHER: Int
```

The camera exists outside of the vehicle body frame but not exactly on one of the exterior locations this enum defines. The applications should determine the exact location from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LOCATION:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LOCATION_EXTERIOR_REAR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LOCATION_EXTERIOR_REAR: Int
```

The camera device exists outside of the vehicle body frame and on its rear side.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LOCATION:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LOCATION_EXTERIOR_RIGHT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LOCATION_EXTERIOR_RIGHT: Int
```

The camera device exists outside and on right side of the vehicle body frame.

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LOCATION:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LOCATION_EXTRA_FRONT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LOCATION_EXTRA_FRONT: Int
```

The camera device exists outside of the extra vehicle's body frame and on its front side.

 Value: 7

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LOCATION:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LOCATION_EXTRA_LEFT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LOCATION_EXTRA_LEFT: Int
```

The camera device exists outside and on left side of the extra vehicle body.

 Value: 9

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LOCATION:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LOCATION_EXTRA_OTHER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LOCATION_EXTRA_OTHER: Int
```

The camera device exists on an extra vehicle, such as the trailer, but not exactly on one of front, rear, left, or right side. Applications should determine the exact location from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`.

 Value: 6

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LOCATION:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LOCATION_EXTRA_REAR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LOCATION_EXTRA_REAR: Int
```

The camera device exists outside of the extra vehicle's body frame and on its rear side.

 Value: 8

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LOCATION:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LOCATION_EXTRA_RIGHT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LOCATION_EXTRA_RIGHT: Int
```

The camera device exists outside and on right side of the extra vehicle body.

 Value: 10

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LOCATION:android.hardware.camera2.CameraCharacteristics.Key`

### AUTOMOTIVE_LOCATION_INTERIOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTOMOTIVE_LOCATION_INTERIOR: Int
```

The camera device exists inside of the vehicle cabin.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#AUTOMOTIVE_LOCATION:android.hardware.camera2.CameraCharacteristics.Key`

### COLOR_CORRECTION_ABERRATION_MODE_FAST

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_CORRECTION_ABERRATION_MODE_FAST: Int
```

Aberration correction will not slow down capture rate relative to sensor raw output.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_ABERRATION_MODE:android.hardware.camera2.CaptureRequest.Key`

### COLOR_CORRECTION_ABERRATION_MODE_HIGH_QUALITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_CORRECTION_ABERRATION_MODE_HIGH_QUALITY: Int
```

Aberration correction operates at improved quality but the capture rate might be reduced (relative to sensor raw output rate)

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_ABERRATION_MODE:android.hardware.camera2.CaptureRequest.Key`

### COLOR_CORRECTION_ABERRATION_MODE_OFF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_CORRECTION_ABERRATION_MODE_OFF: Int
```

No aberration correction is applied.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_ABERRATION_MODE:android.hardware.camera2.CaptureRequest.Key`

### COLOR_CORRECTION_MODE_CCT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_CORRECTION_MODE_CCT: Int
```

Use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_COLOR_TEMPERATURE:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_COLOR_TINT:android.hardware.camera2.CaptureRequest.Key` to adjust the white balance based on correlated color temperature.

If AWB is enabled with `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key` != OFF ``, then CCT is ignored.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_COLOR_TEMPERATURE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_COLOR_TINT:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`

### COLOR_CORRECTION_MODE_FAST

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_CORRECTION_MODE_FAST: Int
```

Color correction processing must not slow down capture rate relative to sensor raw output.

Advanced white balance adjustments above and beyond the specified white balance pipeline may be applied.

If AWB is enabled with `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key` != OFF ``, then the camera device uses the last frame's AWB values (or defaults if AWB has never been run).

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`

### COLOR_CORRECTION_MODE_HIGH_QUALITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_CORRECTION_MODE_HIGH_QUALITY: Int
```

Color correction processing operates at improved quality but the capture rate might be reduced (relative to sensor raw output rate)

Advanced white balance adjustments above and beyond the specified white balance pipeline may be applied.

If AWB is enabled with `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key` != OFF ``, then the camera device uses the last frame's AWB values (or defaults if AWB has never been run).

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`

### COLOR_CORRECTION_MODE_TRANSFORM_MATRIX

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_CORRECTION_MODE_TRANSFORM_MATRIX: Int
```

Use the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` matrix and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` to do color conversion.

All advanced white balance adjustments (not specified by our white balance pipeline) must be disabled.

If AWB is enabled with `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key` != OFF ``, then TRANSFORM_MATRIX is ignored. The camera device will override this value to either FAST or HIGH_QUALITY.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_ANTIBANDING_MODE_50HZ

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_ANTIBANDING_MODE_50HZ: Int
```

The camera device will adjust exposure duration to avoid banding problems with 50Hz illumination sources.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_ANTIBANDING_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_ANTIBANDING_MODE_60HZ

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_ANTIBANDING_MODE_60HZ: Int
```

The camera device will adjust exposure duration to avoid banding problems with 60Hz illumination sources.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_ANTIBANDING_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_ANTIBANDING_MODE_AUTO

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_ANTIBANDING_MODE_AUTO: Int
```

The camera device will automatically adapt its antibanding routine to the current illumination condition. This is the default mode if AUTO is available on given camera device.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_ANTIBANDING_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_ANTIBANDING_MODE_OFF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_ANTIBANDING_MODE_OFF: Int
```

The camera device will not adjust exposure duration to avoid banding problems.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_ANTIBANDING_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_MODE_OFF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_MODE_OFF: Int
```

The camera device's autoexposure routine is disabled.

The application-selected `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` are used by the camera device, along with android.flash.\* fields, if there's a flash unit for this camera device.

Note that auto-white balance (AWB) and auto-focus (AF) behavior is device dependent when AE is in OFF mode. To have consistent behavior across different devices, it is recommended to either set AWB and AF to OFF mode or lock AWB and AF before setting AE to OFF. See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_LOCK:android.hardware.camera2.CaptureRequest.Key`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key` for more details.

LEGACY devices do not support the OFF mode and will override attempts to use this value to ON.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_LOCK:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_MODE_ON

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_MODE_ON: Int
```

The camera device's autoexposure routine is active, with no flash control.

The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` are ignored. The application has control over the various android.flash.\* fields.

If the device supports manual flash strength control, i.e., if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_SINGLE_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_TORCH_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` are greater than 1, then the auto-exposure (AE) precapture metering sequence should be triggered for the configured flash mode and strength to avoid the image being incorrectly exposed at different `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_STRENGTH_LEVEL:android.hardware.camera2.CaptureRequest.Key`.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_SINGLE_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_STRENGTH_LEVEL:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#FLASH_TORCH_STRENGTH_MAX_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_MODE_ON_ALWAYS_FLASH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_MODE_ON_ALWAYS_FLASH: Int
```

Like ON, except that the camera device also controls the camera's flash unit, always firing it for still captures.

The flash may be fired during a precapture sequence (triggered by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key`) and will always be fired for captures for which the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key` field is set to STILL_CAPTURE.

It's important to wait for the precapture sequence to complete (i.e., `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key` reaches FLASH_REQUIRED, CONVERGED, or LOCKED) Dbefore submitting a STILL_CAPTURE request. Otherwise, in low-light conditions, the image captures with flash fired won't have correct exposures.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_MODE_ON_AUTO_FLASH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_MODE_ON_AUTO_FLASH: Int
```

Like ON, except that the camera device also controls the camera's flash unit, firing it in low-light conditions.

The flash may be fired during a precapture sequence (triggered by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key`) and may be fired for captures for which the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key` field is set to STILL_CAPTURE.

It's important to wait for the precapture sequence to complete (i.e., `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key` reaches FLASH_REQUIRED, CONVERGED, or LOCKED) before submitting a STILL_CAPTURE request. Otherwise, in low-light conditions, the image captures with flash fired won't have correct exposures.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_MODE_ON_AUTO_FLASH_REDEYE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_MODE_ON_AUTO_FLASH_REDEYE: Int
```

Like ON_AUTO_FLASH, but with automatic red eye reduction.

If deemed necessary by the camera device, a red eye reduction flash will fire during the precapture sequence.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_MODE_ON_EXTERNAL_FLASH

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_MODE_ON_EXTERNAL_FLASH: Int
```

An external flash has been turned on.

It informs the camera device that an external flash has been turned on, and that metering (and continuous focus if active) should be quickly recalculated to account for the external flash. Otherwise, this mode acts like ON.

When the external flash is turned off, AE mode should be changed to one of the other available AE modes.

If the camera device supports AE external flash mode, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key` must be FLASH_REQUIRED after the camera device finishes AE scan and it's too dark without flash.

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_MODE_ON_LOW_LIGHT_BOOST_BRIGHTNESS_PRIORITY

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_MODE_ON_LOW_LIGHT_BOOST_BRIGHTNESS_PRIORITY: Int
```

Like 'ON' but applies additional brightness boost in low light scenes.

When the scene lighting conditions are within the range defined by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_LOW_LIGHT_BOOST_INFO_LUMINANCE_RANGE:android.hardware.camera2.CameraCharacteristics.Key` this mode will apply additional brightness boost.

This mode will automatically adjust the intensity of low light boost applied according to the scene lighting conditions. A darker scene will receive more boost while a brighter scene will receive less boost.

This mode can ignore the set target frame rate to allow more light to be captured which can result in choppier motion. The frame rate can extend to lower than the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_TARGET_FPS_RANGES:android.hardware.camera2.CameraCharacteristics.Key` but will not go below 10 FPS. This mode can also increase the sensor sensitivity gain which can result in increased luma and chroma noise. The sensor sensitivity gain can extend to higher values beyond `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_SENSITIVITY_RANGE:android.hardware.camera2.CameraCharacteristics.Key`. This mode may also apply additional processing to recover details in dark and bright areas of the image,and noise reduction at high sensitivity gain settings to manage the trade-off between light sensitivity and capture noise.

This mode is restricted to two output surfaces. One output surface type can either be SurfaceView or TextureView. Another output surface type can either be MediaCodec or MediaRecorder. This mode cannot be used with a target FPS range higher than 30 FPS.

If the session configuration is not supported, the AE mode reported in the CaptureResult will be 'ON' instead of 'ON_LOW_LIGHT_BOOST_BRIGHTNESS_PRIORITY'.

When this AE mode is enabled, the CaptureResult field `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_LOW_LIGHT_BOOST_STATE:android.hardware.camera2.CaptureResult.Key` will indicate when low light boost is 'ACTIVE' or 'INACTIVE'. By default `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_LOW_LIGHT_BOOST_STATE:android.hardware.camera2.CaptureResult.Key` will be 'INACTIVE'.

The low light boost is 'ACTIVE' once the scene lighting condition is less than the upper bound lux value defined by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_LOW_LIGHT_BOOST_INFO_LUMINANCE_RANGE:android.hardware.camera2.CameraCharacteristics.Key`. This mode will be 'INACTIVE' once the scene lighting condition is greater than the upper bound lux value defined by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_LOW_LIGHT_BOOST_INFO_LUMINANCE_RANGE:android.hardware.camera2.CameraCharacteristics.Key`.

 Value: 6

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_TARGET_FPS_RANGES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_LOW_LIGHT_BOOST_INFO_LUMINANCE_RANGE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_LOW_LIGHT_BOOST_STATE:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_SENSITIVITY_RANGE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_PRECAPTURE_TRIGGER_CANCEL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_PRECAPTURE_TRIGGER_CANCEL: Int
```

The camera device will cancel any currently active or completed precapture metering sequence, the auto-exposure routine will return to its initial state.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_PRECAPTURE_TRIGGER_IDLE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_PRECAPTURE_TRIGGER_IDLE: Int
```

The trigger is idle.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_PRECAPTURE_TRIGGER_START

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_PRECAPTURE_TRIGGER_START: Int
```

The precapture metering sequence will be started by the camera device.

The exact effect of the precapture trigger depends on the current AE mode and state.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_PRIORITY_MODE_OFF

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_PRIORITY_MODE_OFF: Int
```

Disable AE priority mode. This is the default value.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRIORITY_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_PRIORITY_MODE_SENSOR_EXPOSURE_TIME_PRIORITY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_PRIORITY_MODE_SENSOR_EXPOSURE_TIME_PRIORITY: Int
```

The camera device's auto-exposure routine is active and prioritizes the application-selected exposure time (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`).

The application has control over `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key` while the application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` are ignored.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRIORITY_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_PRIORITY_MODE_SENSOR_SENSITIVITY_PRIORITY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_PRIORITY_MODE_SENSOR_SENSITIVITY_PRIORITY: Int
```

The camera device's auto-exposure routine is active and prioritizes the application-selected ISO (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`).

The application has control over `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key` while the application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key` are ignored.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRIORITY_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AE_STATE_CONVERGED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_STATE_CONVERGED: Int
```

AE has a good set of control values for the current scene.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_AE_STATE_FLASH_REQUIRED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_STATE_FLASH_REQUIRED: Int
```

AE has a good set of control values, but flash needs to be fired for good quality still capture.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_AE_STATE_INACTIVE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_STATE_INACTIVE: Int
```

AE is off or recently reset.

When a camera device is opened, it starts in this state. This is a transient state, the camera device may skip reporting this state in capture result.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_AE_STATE_LOCKED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_STATE_LOCKED: Int
```

AE has been locked.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_AE_STATE_PRECAPTURE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_STATE_PRECAPTURE: Int
```

AE has been asked to do a precapture sequence and is currently executing it.

Precapture can be triggered through setting `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key` to START. Currently active and completed (if it causes camera device internal AE lock) precapture metering sequence can be canceled through setting `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key` to CANCEL.

Once PRECAPTURE completes, AE will transition to CONVERGED or FLASH_REQUIRED as appropriate. This is a transient state, the camera device may skip reporting this state in capture result.

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_AE_STATE_SEARCHING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AE_STATE_SEARCHING: Int
```

AE doesn't yet have a good set of control values for the current scene.

This is a transient state, the camera device may skip reporting this state in capture result.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AE_STATE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_AF_MODE_AUTO

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AF_MODE_AUTO: Int
```

Basic automatic focus mode.

In this mode, the lens does not move unless the autofocus trigger action is called. When that trigger is activated, AF will transition to ACTIVE_SCAN, then to the outcome of the scan (FOCUSED or NOT_FOCUSED).

Always supported if lens is not fixed focus.

Use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key` to determine if lens is fixed-focus.

Triggering AF_CANCEL resets the lens position to default, and sets the AF state to INACTIVE.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AF_MODE_CONTINUOUS_PICTURE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AF_MODE_CONTINUOUS_PICTURE: Int
```

In this mode, the AF algorithm modifies the lens position continually to attempt to provide a constantly-in-focus image stream.

The focusing behavior should be suitable for still image capture; typically this means focusing as fast as possible. When the AF trigger is not involved, the AF algorithm should start in INACTIVE state, and then transition into PASSIVE_SCAN and PASSIVE_FOCUSED states as appropriate as it attempts to maintain focus. When the AF trigger is activated, the algorithm should finish its PASSIVE_SCAN if active, and then transition into AF_FOCUSED or AF_NOT_FOCUSED as appropriate, and lock the lens position until a cancel AF trigger is received.

When the AF cancel trigger is activated, the algorithm should transition back to INACTIVE and then act as if it has just been started.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AF_MODE_CONTINUOUS_VIDEO

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AF_MODE_CONTINUOUS_VIDEO: Int
```

In this mode, the AF algorithm modifies the lens position continually to attempt to provide a constantly-in-focus image stream.

The focusing behavior should be suitable for good quality video recording; typically this means slower focus movement and no overshoots. When the AF trigger is not involved, the AF algorithm should start in INACTIVE state, and then transition into PASSIVE_SCAN and PASSIVE_FOCUSED states as appropriate. When the AF trigger is activated, the algorithm should immediately transition into AF_FOCUSED or AF_NOT_FOCUSED as appropriate, and lock the lens position until a cancel AF trigger is received.

Once cancel is received, the algorithm should transition back to INACTIVE and resume passive scan. Note that this behavior is not identical to CONTINUOUS_PICTURE, since an ongoing PASSIVE_SCAN must immediately be canceled.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AF_MODE_EDOF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AF_MODE_EDOF: Int
```

Extended depth of field (digital focus) mode.

The camera device will produce images with an extended depth of field automatically; no special focusing operations need to be done before taking a picture.

AF triggers are ignored, and the AF state will always be INACTIVE.

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AF_MODE_MACRO

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AF_MODE_MACRO: Int
```

Close-up focusing mode.

In this mode, the lens does not move unless the autofocus trigger action is called. When that trigger is activated, AF will transition to ACTIVE_SCAN, then to the outcome of the scan (FOCUSED or NOT_FOCUSED). This mode is optimized for focusing on objects very close to the camera.

When that trigger is activated, AF will transition to ACTIVE_SCAN, then to the outcome of the scan (FOCUSED or NOT_FOCUSED). Triggering cancel AF resets the lens position to default, and sets the AF state to INACTIVE.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AF_MODE_OFF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AF_MODE_OFF: Int
```

The auto-focus routine does not control the lens; `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key` is controlled by the application.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AF_SCENE_CHANGE_DETECTED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AF_SCENE_CHANGE_DETECTED: Int
```

Scene change is detected within the AF region(s).

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AF_SCENE_CHANGE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_AF_SCENE_CHANGE_NOT_DETECTED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AF_SCENE_CHANGE_NOT_DETECTED: Int
```

Scene change is not detected within the AF region(s).

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AF_SCENE_CHANGE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_AF_STATE_ACTIVE_SCAN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AF_STATE_ACTIVE_SCAN: Int
```

AF is performing an AF scan because it was triggered by AF trigger.

Only used by AUTO or MACRO AF modes. This is a transient state, the camera device may skip reporting this state in capture result.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AF_STATE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_AF_STATE_FOCUSED_LOCKED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AF_STATE_FOCUSED_LOCKED: Int
```

AF believes it is focused correctly and has locked focus.

This state is reached only after an explicit START AF trigger has been sent (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`), when good focus has been obtained.

The lens will remain stationary until the AF mode (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`) is changed or a new AF trigger is sent to the camera device (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`).

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AF_STATE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_AF_STATE_INACTIVE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AF_STATE_INACTIVE: Int
```

AF is off or has not yet tried to scan/been asked to scan.

When a camera device is opened, it starts in this state. This is a transient state, the camera device may skip reporting this state in capture result.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AF_STATE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_AF_STATE_NOT_FOCUSED_LOCKED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AF_STATE_NOT_FOCUSED_LOCKED: Int
```

AF has failed to focus successfully and has locked focus.

This state is reached only after an explicit START AF trigger has been sent (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`), when good focus cannot be obtained.

The lens will remain stationary until the AF mode (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`) is changed or a new AF trigger is sent to the camera device (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`).

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AF_STATE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_AF_STATE_PASSIVE_FOCUSED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AF_STATE_PASSIVE_FOCUSED: Int
```

AF currently believes it is in focus, but may restart scanning at any time.

Only used by CONTINUOUS_\* AF modes. This is a transient state, the camera device may skip reporting this state in capture result.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AF_STATE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_AF_STATE_PASSIVE_SCAN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AF_STATE_PASSIVE_SCAN: Int
```

AF is currently performing an AF scan initiated the camera device in a continuous autofocus mode.

Only used by CONTINUOUS_\* AF modes. This is a transient state, the camera device may skip reporting this state in capture result.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AF_STATE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_AF_STATE_PASSIVE_UNFOCUSED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AF_STATE_PASSIVE_UNFOCUSED: Int
```

AF finished a passive scan without finding focus, and may restart scanning at any time.

Only used by CONTINUOUS_\* AF modes. This is a transient state, the camera device may skip reporting this state in capture result.

LEGACY camera devices do not support this state. When a passive scan has finished, it will always go to PASSIVE_FOCUSED.

 Value: 6

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AF_STATE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_AF_TRIGGER_CANCEL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AF_TRIGGER_CANCEL: Int
```

Autofocus will return to its initial state, and cancel any currently active trigger.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AF_TRIGGER_IDLE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AF_TRIGGER_IDLE: Int
```

The trigger is idle.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AF_TRIGGER_START

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AF_TRIGGER_START: Int
```

Autofocus will trigger now.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AUTOFRAMING_OFF

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AUTOFRAMING_OFF: Int
```

Disable autoframing.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AUTOFRAMING:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AUTOFRAMING_ON

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AUTOFRAMING_ON: Int
```

Enable autoframing to keep people in the frame's field of view.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AUTOFRAMING:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AUTOFRAMING_STATE_CONVERGED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AUTOFRAMING_STATE_CONVERGED: Int
```

Auto-framing has reached a stable state (frame/fov is not being adjusted). The state may transition back to FRAMING if the scene changes.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AUTOFRAMING_STATE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_AUTOFRAMING_STATE_FRAMING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AUTOFRAMING_STATE_FRAMING: Int
```

Auto-framing is in process - either zooming in, zooming out or pan is taking place.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AUTOFRAMING_STATE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_AUTOFRAMING_STATE_INACTIVE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AUTOFRAMING_STATE_INACTIVE: Int
```

Auto-framing is inactive.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AUTOFRAMING_STATE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_AWB_MODE_AUTO

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AWB_MODE_AUTO: Int
```

The camera device's auto-white balance routine is active.

The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AWB_MODE_CLOUDY_DAYLIGHT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AWB_MODE_CLOUDY_DAYLIGHT: Int
```

The camera device's auto-white balance routine is disabled; the camera device uses cloudy daylight light as the assumed scene illumination for white balance.

The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request.

 Value: 6

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AWB_MODE_DAYLIGHT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AWB_MODE_DAYLIGHT: Int
```

The camera device's auto-white balance routine is disabled; the camera device uses daylight light as the assumed scene illumination for white balance.

While the exact white balance transforms are up to the camera device, they will approximately match the CIE standard illuminant D65.

The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request.

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AWB_MODE_FLUORESCENT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AWB_MODE_FLUORESCENT: Int
```

The camera device's auto-white balance routine is disabled; the camera device uses fluorescent light as the assumed scene illumination for white balance.

While the exact white balance transforms are up to the camera device, they will approximately match the CIE standard illuminant F2.

The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AWB_MODE_INCANDESCENT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AWB_MODE_INCANDESCENT: Int
```

The camera device's auto-white balance routine is disabled; the camera device uses incandescent light as the assumed scene illumination for white balance.

While the exact white balance transforms are up to the camera device, they will approximately match the CIE standard illuminant A.

The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AWB_MODE_OFF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AWB_MODE_OFF: Int
```

The camera device's auto-white balance routine is disabled.

The application-selected color transform matrix (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key`) and gains (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key`) are used by the camera device for manual white balance control.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AWB_MODE_SHADE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AWB_MODE_SHADE: Int
```

The camera device's auto-white balance routine is disabled; the camera device uses shade light as the assumed scene illumination for white balance.

The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request.

 Value: 8

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AWB_MODE_TWILIGHT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AWB_MODE_TWILIGHT: Int
```

The camera device's auto-white balance routine is disabled; the camera device uses twilight light as the assumed scene illumination for white balance.

The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request.

 Value: 7

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AWB_MODE_WARM_FLUORESCENT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AWB_MODE_WARM_FLUORESCENT: Int
```

The camera device's auto-white balance routine is disabled; the camera device uses warm fluorescent light as the assumed scene illumination for white balance.

While the exact white balance transforms are up to the camera device, they will approximately match the CIE standard illuminant F4.

The application's values for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key` are ignored. For devices that support the MANUAL_POST_PROCESSING capability, the values used by the camera device for the transform and gains will be available in the capture result for this request.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_AWB_STATE_CONVERGED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AWB_STATE_CONVERGED: Int
```

AWB has a good set of control values for the current scene.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AWB_STATE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_AWB_STATE_INACTIVE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AWB_STATE_INACTIVE: Int
```

AWB is not in auto mode, or has not yet started metering.

When a camera device is opened, it starts in this state. This is a transient state, the camera device may skip reporting this state in capture result.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AWB_STATE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_AWB_STATE_LOCKED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AWB_STATE_LOCKED: Int
```

AWB has been locked.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AWB_STATE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_AWB_STATE_SEARCHING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_AWB_STATE_SEARCHING: Int
```

AWB doesn't yet have a good set of control values for the current scene.

This is a transient state, the camera device may skip reporting this state in capture result.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_AWB_STATE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_CAPTURE_INTENT_CUSTOM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_CAPTURE_INTENT_CUSTOM: Int
```

The goal of this request doesn't fall into the other categories. The camera device will default to preview-like behavior.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_CAPTURE_INTENT_MANUAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_CAPTURE_INTENT_MANUAL: Int
```

This request is for manual capture use case where the applications want to directly control the capture parameters.

For example, the application may wish to manually control `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`, etc.

 Value: 6

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_CAPTURE_INTENT_MOTION_TRACKING

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_CAPTURE_INTENT_MOTION_TRACKING: Int
```

This request is for a motion tracking use case, where the application will use camera and inertial sensor data to locate and track objects in the world.

The camera device auto-exposure routine will limit the exposure time of the camera to no more than 20 milliseconds, to minimize motion blur.

 Value: 7

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_CAPTURE_INTENT_PREVIEW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_CAPTURE_INTENT_PREVIEW: Int
```

This request is for a preview-like use case.

The precapture trigger may be used to start off a metering w/flash sequence.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_CAPTURE_INTENT_STILL_CAPTURE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_CAPTURE_INTENT_STILL_CAPTURE: Int
```

This request is for a still capture-type use case.

If the flash unit is under automatic control, it may fire as needed.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_CAPTURE_INTENT_VIDEO_RECORD

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_CAPTURE_INTENT_VIDEO_RECORD: Int
```

This request is for a video recording use case.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_CAPTURE_INTENT_VIDEO_SNAPSHOT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_CAPTURE_INTENT_VIDEO_SNAPSHOT: Int
```

This request is for a video snapshot (still image while recording video) use case.

The camera device should take the highest-quality image possible (given the other settings) without disrupting the frame rate of video recording.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_CAPTURE_INTENT_ZERO_SHUTTER_LAG

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_CAPTURE_INTENT_ZERO_SHUTTER_LAG: Int
```

This request is for a ZSL usecase; the application will stream full-resolution images and reprocess one or several later for a final capture.

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_EFFECT_MODE_AQUA

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_EFFECT_MODE_AQUA: Int
```

An "aqua" effect where a blue hue is added to the image.

 Value: 8

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EFFECT_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_EFFECT_MODE_BLACKBOARD

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_EFFECT_MODE_BLACKBOARD: Int
```

A "blackboard" effect where the image is typically displayed as regions of black, with white or grey details.

 Value: 7

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EFFECT_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_EFFECT_MODE_MONO

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_EFFECT_MODE_MONO: Int
```

A "monocolor" effect where the image is mapped into a single color.

This will typically be grayscale.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EFFECT_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_EFFECT_MODE_NEGATIVE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_EFFECT_MODE_NEGATIVE: Int
```

A "photo-negative" effect where the image's colors are inverted.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EFFECT_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_EFFECT_MODE_OFF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_EFFECT_MODE_OFF: Int
```

No color effect will be applied.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EFFECT_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_EFFECT_MODE_POSTERIZE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_EFFECT_MODE_POSTERIZE: Int
```

A "posterization" effect where the image uses discrete regions of tone rather than a continuous gradient of tones.

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EFFECT_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_EFFECT_MODE_SEPIA

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_EFFECT_MODE_SEPIA: Int
```

A "sepia" effect where the image is mapped into warm gray, red, and brown tones.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EFFECT_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_EFFECT_MODE_SOLARIZE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_EFFECT_MODE_SOLARIZE: Int
```

A "solarisation" effect (Sabattier effect) where the image is wholly or partially reversed in tone.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EFFECT_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_EFFECT_MODE_WHITEBOARD

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_EFFECT_MODE_WHITEBOARD: Int
```

A "whiteboard" effect where the image is typically displayed as regions of white, with black or grey details.

 Value: 6

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EFFECT_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_EXTENDED_SCENE_MODE_BOKEH_CONTINUOUS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_EXTENDED_SCENE_MODE_BOKEH_CONTINUOUS: Int
```

Bokeh effect must not slow down capture rate relative to sensor raw output, and the effect is applied to all processed streams no larger than the maximum streaming dimension. This mode should be used if performance and power are a priority, such as video recording.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EXTENDED_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_EXTENDED_SCENE_MODE_BOKEH_STILL_CAPTURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_EXTENDED_SCENE_MODE_BOKEH_STILL_CAPTURE: Int
```

High quality bokeh mode is enabled for all non-raw streams (including YUV, JPEG, and IMPLEMENTATION_DEFINED) when capture intent is STILL_CAPTURE. Due to the extra image processing, this mode may introduce additional stall to non-raw streams. This mode should be used in high quality still capture use case.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EXTENDED_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_EXTENDED_SCENE_MODE_DISABLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_EXTENDED_SCENE_MODE_DISABLED: Int
```

Extended scene mode is disabled.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EXTENDED_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_LOW_LIGHT_BOOST_STATE_ACTIVE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_LOW_LIGHT_BOOST_STATE_ACTIVE: Int
```

The AE mode 'ON_LOW_LIGHT_BOOST_BRIGHTNESS_PRIORITY' is enabled and applied.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_LOW_LIGHT_BOOST_STATE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_LOW_LIGHT_BOOST_STATE_INACTIVE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_LOW_LIGHT_BOOST_STATE_INACTIVE: Int
```

The AE mode 'ON_LOW_LIGHT_BOOST_BRIGHTNESS_PRIORITY' is enabled but not applied.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#CONTROL_LOW_LIGHT_BOOST_STATE:android.hardware.camera2.CaptureResult.Key`

### CONTROL_MODE_AUTO

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_MODE_AUTO: Int
```

Use settings for each individual 3A routine.

Manual control of capture parameters is disabled. All controls in android.control.\* besides sceneMode take effect.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_MODE_OFF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_MODE_OFF: Int
```

Full application control of pipeline.

All control by the device's metering and focusing (3A) routines is disabled, and no other settings in android.control.\* have any effect, except that `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key` may be used by the camera device to select post-processing values for processing blocks that do not allow for manual control, or are not exposed by the camera API.

However, the camera device's 3A routines may continue to collect statistics and update their internal state so that when control is switched to AUTO mode, good control values can be immediately applied.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_MODE_OFF_KEEP_STATE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_MODE_OFF_KEEP_STATE: Int
```

Same as OFF mode, except that this capture will not be used by camera device background auto-exposure, auto-white balance and auto-focus algorithms (3A) to update their statistics.

Specifically, the 3A routines are locked to the last values set from a request with AUTO, OFF, or USE_SCENE_MODE, and any statistics or state updates collected from manual captures with OFF_KEEP_STATE will be discarded by the camera device.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_MODE_USE_EXTENDED_SCENE_MODE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_MODE_USE_EXTENDED_SCENE_MODE: Int
```

Use a specific extended scene mode.

When extended scene mode is on, the camera device may override certain control parameters, such as targetFpsRange, AE, AWB, and AF modes, to achieve best power and quality tradeoffs. Only the mandatory stream combinations of LIMITED hardware level are guaranteed.

This setting can only be used if extended scene mode is supported (i.e. android.control.availableExtendedSceneModes contains some modes other than DISABLED).

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_MODE_USE_SCENE_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_MODE_USE_SCENE_MODE: Int
```

Use a specific scene mode.

Enabling this disables control.aeMode, control.awbMode and control.afMode controls; the camera device will ignore those settings while USE_SCENE_MODE is active (except for FACE_PRIORITY scene mode). Other control entries are still active. This setting can only be used if scene mode is supported (i.e. `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_SCENE_MODES:android.hardware.camera2.CameraCharacteristics.Key` contain some modes other than DISABLED).

For extended scene modes such as BOKEH, please use USE_EXTENDED_SCENE_MODE instead.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AVAILABLE_SCENE_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_SCENE_MODE_ACTION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_SCENE_MODE_ACTION: Int
```

Optimized for photos of quickly moving objects.

Similar to SPORTS.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_SCENE_MODE_BARCODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_SCENE_MODE_BARCODE: Int
```

Optimized for accurately capturing a photo of barcode for use by camera applications that wish to read the barcode value.

 Value: 16

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_SCENE_MODE_BEACH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_SCENE_MODE_BEACH: Int
```

Optimized for bright, outdoor beach settings.

 Value: 8

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_SCENE_MODE_CANDLELIGHT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_SCENE_MODE_CANDLELIGHT: Int
```

Optimized for dim settings where the main light source is a candle.

 Value: 15

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_SCENE_MODE_DISABLED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_SCENE_MODE_DISABLED: Int
```

Indicates that no scene modes are set for a given capture request.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_SCENE_MODE_FACE_PRIORITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_SCENE_MODE_FACE_PRIORITY: Int
```

If face detection support exists, use face detection data for auto-focus, auto-white balance, and auto-exposure routines.

If face detection statistics are disabled (i.e. `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_FACE_DETECT_MODE:android.hardware.camera2.CaptureRequest.Key` is set to OFF), this should still operate correctly (but will not return face detection statistics to the framework).

Unlike the other scene modes, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key` remain active when FACE_PRIORITY is set.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_FACE_DETECT_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_SCENE_MODE_FIREWORKS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_SCENE_MODE_FIREWORKS: Int
```

Optimized for nighttime photos of fireworks.

 Value: 12

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_SCENE_MODE_HDR

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_SCENE_MODE_HDR: Int
```

Turn on a device-specific high dynamic range (HDR) mode.

In this scene mode, the camera device captures images that keep a larger range of scene illumination levels visible in the final image. For example, when taking a picture of a object in front of a bright window, both the object and the scene through the window may be visible when using HDR mode, while in normal AUTO mode, one or the other may be poorly exposed. As a tradeoff, HDR mode generally takes much longer to capture a single image, has no user control, and may have other artifacts depending on the HDR method used.

Therefore, HDR captures operate at a much slower rate than regular captures.

In this mode, on LIMITED or FULL devices, when a request is made with a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key` of STILL_CAPTURE, the camera device will capture an image using a high dynamic range capture technique. On LEGACY devices, captures that target a JPEG-format output will be captured with HDR, and the capture intent is not relevant.

The HDR capture may involve the device capturing a burst of images internally and combining them into one, or it may involve the device using specialized high dynamic range capture hardware. In all cases, a single image is produced in response to a capture request submitted while in HDR mode.

Since substantial post-processing is generally needed to produce an HDR image, only YUV, PRIVATE, and JPEG outputs are supported for LIMITED/FULL device HDR captures, and only JPEG outputs are supported for LEGACY HDR captures. Using a RAW output for HDR capture is not supported.

Some devices may also support always-on HDR, which applies HDR processing at full frame rate. For these devices, intents other than STILL_CAPTURE will also produce an HDR output with no frame rate impact compared to normal operation, though the quality may be lower than for STILL_CAPTURE intents.

If SCENE_MODE_HDR is used with unsupported output types or capture intents, the images captured will be as if the SCENE_MODE was not enabled at all.

 Value: 18

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_SCENE_MODE_HIGH_SPEED_VIDEO

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_SCENE_MODE_HIGH_SPEED_VIDEO: Int
```

**Deprecated:** *Please refer to this API documentation to find the alternatives*

This is deprecated, please use `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createConstrainedHighSpeedCaptureSession(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraConstrainedHighSpeedCaptureSession#createHighSpeedRequestList(android.hardware.camera2.CaptureRequest)` for high speed video recording.

Optimized for high speed video recording (frame rate \>=60fps) use case.

The supported high speed video sizes and fps ranges are specified in android.control.availableHighSpeedVideoConfigurations. To get desired output frame rates, the application is only allowed to select video size and fps range combinations listed in this static metadata. The fps range can be control via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key`.

In this mode, the camera device will override aeMode, awbMode, and afMode to ON, ON, and CONTINUOUS_VIDEO, respectively. All post-processing block mode controls will be overridden to be FAST. Therefore, no manual control of capture and post-processing parameters is possible. All other controls operate the same as when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` == AUTO. This means that all other android.control.\* fields continue to work, such as

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_EXPOSURE_COMPENSATION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_LOCK:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_LOCK:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EFFECT_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`

Outside of android.control.\*, the following controls will work:

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_MODE:android.hardware.camera2.CaptureRequest.Key` (automatic flash for still capture will not work since aeMode is ON)
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_OPTICAL_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key` (if it is supported)
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_FACE_DETECT_MODE:android.hardware.camera2.CaptureRequest.Key`

For high speed recording use case, the actual maximum supported frame rate may be lower than what camera can output, depending on the destination Surfaces for the image data. For example, if the destination surface is from video encoder, the application need check if the video encoder is capable of supporting the high frame rate for a given video size, or it will end up with lower recording frame rate. If the destination surface is from preview window, the preview frame rate will be bounded by the screen refresh rate.

The camera device will only support up to 2 output high speed streams (processed non-stalling format defined in android.request.maxNumOutputStreams) in this mode. This control will be effective only if all of below conditions are true:

- The application created no more than maxNumHighSpeedStreams processed non-stalling format output streams, where maxNumHighSpeedStreams is calculated as min(2, android.request.maxNumOutputStreams\[Processed (but not-stalling)\]).
- The stream sizes are selected from the sizes reported by android.control.availableHighSpeedVideoConfigurations.
- No processed non-stalling or raw streams are configured.

When above conditions are NOT satisfied, the controls of this mode and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key` will be ignored by the camera device, the camera device will fall back to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` `==` AUTO, and the returned capture result metadata will give the fps range chosen by the camera device.

Switching into or out of this mode may trigger some camera ISP/sensor reconfigurations, which may introduce extra latency. It is recommended that the application avoids unnecessary scene mode switch as much as possible.

 Value: 17

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_EXPOSURE_COMPENSATION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_LOCK:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_LOCK:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EFFECT_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_OPTICAL_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_FACE_DETECT_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_SCENE_MODE_LANDSCAPE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_SCENE_MODE_LANDSCAPE: Int
```

Optimized for photos of distant macroscopic objects.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_SCENE_MODE_NIGHT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_SCENE_MODE_NIGHT: Int
```

Optimized for low-light settings.

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_SCENE_MODE_NIGHT_PORTRAIT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_SCENE_MODE_NIGHT_PORTRAIT: Int
```

Optimized for still photos of people in low-light settings.

 Value: 6

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_SCENE_MODE_PARTY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_SCENE_MODE_PARTY: Int
```

Optimized for dim, indoor settings with multiple moving people.

 Value: 14

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_SCENE_MODE_PORTRAIT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_SCENE_MODE_PORTRAIT: Int
```

Optimized for still photos of people.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_SCENE_MODE_SNOW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_SCENE_MODE_SNOW: Int
```

Optimized for bright, outdoor settings containing snow.

 Value: 9

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_SCENE_MODE_SPORTS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_SCENE_MODE_SPORTS: Int
```

Optimized for photos of quickly moving people.

Similar to ACTION.

 Value: 13

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_SCENE_MODE_STEADYPHOTO

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_SCENE_MODE_STEADYPHOTO: Int
```

Optimized to avoid blurry photos due to small amounts of device motion (for example: due to hand shake).

 Value: 11

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_SCENE_MODE_SUNSET

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_SCENE_MODE_SUNSET: Int
```

Optimized for scenes of the setting sun.

 Value: 10

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_SCENE_MODE_THEATRE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_SCENE_MODE_THEATRE: Int
```

Optimized for dim, indoor settings where flash must remain off.

 Value: 7

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SCENE_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_SETTINGS_OVERRIDE_OFF

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_SETTINGS_OVERRIDE_OFF: Int
```

No keys are applied sooner than the other keys when applying CaptureRequest settings to the camera device. This is the default value.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SETTINGS_OVERRIDE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_SETTINGS_OVERRIDE_ZOOM

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_SETTINGS_OVERRIDE_ZOOM: Int
```

Zoom related keys are applied sooner than the other keys in the CaptureRequest. The zoom related keys are:

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureRequest.Key`

Even though `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_REGIONS:android.hardware.camera2.CaptureRequest.Key`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureRequest.Key` are not directly zoom related, applications typically scale these regions together with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` to have a consistent mapping within the current field of view. In this aspect, they are related to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_SETTINGS_OVERRIDE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_VIDEO_STABILIZATION_MODE_OFF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_VIDEO_STABILIZATION_MODE_OFF: Int
```

Video stabilization is disabled.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_VIDEO_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_VIDEO_STABILIZATION_MODE_ON

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_VIDEO_STABILIZATION_MODE_ON: Int
```

Video stabilization is enabled.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_VIDEO_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_VIDEO_STABILIZATION_MODE_PREVIEW_STABILIZATION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_VIDEO_STABILIZATION_MODE_PREVIEW_STABILIZATION: Int
```

Preview stabilization, where the preview in addition to all other non-RAW streams are stabilized with the same quality of stabilization, is enabled. This mode aims to give clients a 'what you see is what you get' effect. In this mode, the FoV reduction will be a maximum of 20 % both horizontally and vertically (10% from left, right, top, bottom) for the given zoom ratio / crop region. The resultant FoV will also be the same across all processed streams (that have the same aspect ratio).

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_VIDEO_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_ZOOM_METHOD_AUTO

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_ZOOM_METHOD_AUTO: Int
```

The camera device automatically detects whether the application does zoom with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`, and in turn decides which metadata tag reflects the effective zoom level.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_METHOD:android.hardware.camera2.CaptureRequest.Key`

### CONTROL_ZOOM_METHOD_ZOOM_RATIO

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL_ZOOM_METHOD_ZOOM_RATIO: Int
```

The application intends to control zoom via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`, and the effective zoom level is reflected by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key` in capture results.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_METHOD:android.hardware.camera2.CaptureRequest.Key`

### DISTORTION_CORRECTION_MODE_FAST

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISTORTION_CORRECTION_MODE_FAST: Int
```

Lens distortion correction is applied without reducing frame rate relative to sensor output. It may be the same as OFF if distortion correction would reduce frame rate relative to sensor.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`

### DISTORTION_CORRECTION_MODE_HIGH_QUALITY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISTORTION_CORRECTION_MODE_HIGH_QUALITY: Int
```

High-quality distortion correction is applied, at the cost of possibly reduced frame rate relative to sensor output.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`

### DISTORTION_CORRECTION_MODE_OFF

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISTORTION_CORRECTION_MODE_OFF: Int
```

No distortion correction is applied.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#DISTORTION_CORRECTION_MODE:android.hardware.camera2.CaptureRequest.Key`

### EDGE_MODE_FAST

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EDGE_MODE_FAST: Int
```

Apply edge enhancement at a quality level that does not slow down frame rate relative to sensor output. It may be the same as OFF if edge enhancement will slow down frame rate relative to sensor.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#EDGE_MODE:android.hardware.camera2.CaptureRequest.Key`

### EDGE_MODE_HIGH_QUALITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EDGE_MODE_HIGH_QUALITY: Int
```

Apply high-quality edge enhancement, at a cost of possibly reduced output frame rate.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#EDGE_MODE:android.hardware.camera2.CaptureRequest.Key`

### EDGE_MODE_OFF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EDGE_MODE_OFF: Int
```

No edge enhancement is applied.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#EDGE_MODE:android.hardware.camera2.CaptureRequest.Key`

### EDGE_MODE_ZERO_SHUTTER_LAG

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EDGE_MODE_ZERO_SHUTTER_LAG: Int
```

Edge enhancement is applied at different levels for different output streams, based on resolution. Streams at maximum recording resolution (see android.hardware.camera2.CameraDevice#createCaptureSession) or below have edge enhancement applied, while higher-resolution streams have no edge enhancement applied. The level of edge enhancement for low-resolution streams is tuned so that frame rate is not impacted, and the quality is equal to or better than FAST (since it is only applied to lower-resolution outputs, quality may improve from FAST).

This mode is intended to be used by applications operating in a zero-shutter-lag mode with YUV or PRIVATE reprocessing, where the application continuously captures high-resolution intermediate buffers into a circular buffer, from which a final image is produced via reprocessing when a user takes a picture. For such a use case, the high-resolution buffers must not have edge enhancement applied to maximize efficiency of preview and to avoid double-applying enhancement when reprocessed, while low-resolution buffers (used for recording or preview, generally) need edge enhancement applied for reasonable preview quality.

This mode is guaranteed to be supported by devices that support either the YUV_REPROCESSING or PRIVATE_REPROCESSING capabilities (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` lists either of those capabilities) and it will be the default mode for CAMERA3_TEMPLATE_ZERO_SHUTTER_LAG template.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#EDGE_MODE:android.hardware.camera2.CaptureRequest.Key`

### EXTENSION_NIGHT_MODE_INDICATOR_OFF

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTENSION_NIGHT_MODE_INDICATOR_OFF: Int
```

The camera has detected lighting conditions that are sufficiently bright. Night Mode Camera Extensions is available but may not be able to optimize the camera settings to take a higher quality photo.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#EXTENSION_NIGHT_MODE_INDICATOR:android.hardware.camera2.CaptureResult.Key`

### EXTENSION_NIGHT_MODE_INDICATOR_ON

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTENSION_NIGHT_MODE_INDICATOR_ON: Int
```

The camera has detected low-light conditions. It is recommended to use Night Mode Camera Extension to optimize the camera settings to take a high-quality photo in the dark.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#EXTENSION_NIGHT_MODE_INDICATOR:android.hardware.camera2.CaptureResult.Key`

### EXTENSION_NIGHT_MODE_INDICATOR_UNKNOWN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTENSION_NIGHT_MODE_INDICATOR_UNKNOWN: Int
```

The camera can't accurately assess the scene's lighting to determine if a Night Mode Camera Extension capture would improve the photo. This can happen when the current camera configuration doesn't support night mode indicator detection, such as when the auto exposure mode is ON_AUTO_FLASH, ON_ALWAYS_FLASH, ON_AUTO_FLASH_REDEYE, or ON_EXTERNAL_FLASH.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#EXTENSION_NIGHT_MODE_INDICATOR:android.hardware.camera2.CaptureResult.Key`

### FLASH_MODE_OFF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLASH_MODE_OFF: Int
```

Do not fire the flash for this capture.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_MODE:android.hardware.camera2.CaptureRequest.Key`

### FLASH_MODE_SINGLE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLASH_MODE_SINGLE: Int
```

If the flash is available and charged, fire flash for this capture.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_MODE:android.hardware.camera2.CaptureRequest.Key`

### FLASH_MODE_TORCH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLASH_MODE_TORCH: Int
```

Transition flash to continuously on.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_MODE:android.hardware.camera2.CaptureRequest.Key`

### FLASH_STATE_CHARGING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLASH_STATE_CHARGING: Int
```

Flash is charging and cannot be fired.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#FLASH_STATE:android.hardware.camera2.CaptureResult.Key`

### FLASH_STATE_FIRED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLASH_STATE_FIRED: Int
```

Flash fired for this capture.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#FLASH_STATE:android.hardware.camera2.CaptureResult.Key`

### FLASH_STATE_PARTIAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLASH_STATE_PARTIAL: Int
```

Flash partially illuminated this frame.

This is usually due to the next or previous frame having the flash fire, and the flash spilling into this capture due to hardware limitations.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#FLASH_STATE:android.hardware.camera2.CaptureResult.Key`

### FLASH_STATE_READY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLASH_STATE_READY: Int
```

Flash is ready to fire.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#FLASH_STATE:android.hardware.camera2.CaptureResult.Key`

### FLASH_STATE_UNAVAILABLE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLASH_STATE_UNAVAILABLE: Int
```

No flash on camera.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#FLASH_STATE:android.hardware.camera2.CaptureResult.Key`

### HOT_PIXEL_MODE_FAST

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HOT_PIXEL_MODE_FAST: Int
```

Hot pixel correction is applied, without reducing frame rate relative to sensor raw output.

The hotpixel map may be returned in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_HOT_PIXEL_MAP:android.hardware.camera2.CaptureResult.Key`.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_HOT_PIXEL_MAP:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#HOT_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`

### HOT_PIXEL_MODE_HIGH_QUALITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HOT_PIXEL_MODE_HIGH_QUALITY: Int
```

High-quality hot pixel correction is applied, at a cost of possibly reduced frame rate relative to sensor raw output.

The hotpixel map may be returned in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_HOT_PIXEL_MAP:android.hardware.camera2.CaptureResult.Key`.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_HOT_PIXEL_MAP:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#HOT_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`

### HOT_PIXEL_MODE_OFF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HOT_PIXEL_MODE_OFF: Int
```

No hot pixel correction is applied.

The frame rate must not be reduced relative to sensor raw output for this option.

The hotpixel map may be returned in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_HOT_PIXEL_MAP:android.hardware.camera2.CaptureResult.Key`.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_HOT_PIXEL_MAP:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#HOT_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`

### INFO_DEVICE_TYPE_BUILT_IN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INFO_DEVICE_TYPE_BUILT_IN: Int
```

This camera device is physically a part of this Android device, and the data produced is always within the device's control before it reaches the application requesting it.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_DEVICE_TYPE:android.hardware.camera2.CameraCharacteristics.Key`

### INFO_DEVICE_TYPE_EXTERNAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INFO_DEVICE_TYPE_EXTERNAL: Int
```

This camera device is not permanently connected to this Android device. It may be connected by a wired connection, such as a USB webcam, or it might be connected wirelessly, such as via WiFi or other communication mechanism.

The provenance of the image data from the external camera cannot be guaranteed, since it is produced by hardware that is not controlled by this Android device.

Note that an `EXTERNAL` `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_DEVICE_TYPE:android.hardware.camera2.CameraCharacteristics.Key` `` does not mean the `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` `` must be `EXTERNAL`. A basic USB webcam would likely have an `EXTERNAL` hardware level, but more sophisticated remote camera systems may have more capabilities than that, and be listed with a `LIMITED` or better hardware level.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_DEVICE_TYPE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_DEVICE_TYPE:android.hardware.camera2.CameraCharacteristics.Key`

### INFO_DEVICE_TYPE_UNKNOWN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INFO_DEVICE_TYPE_UNKNOWN: Int
```

This camera device has an unknown classification.

This value will be used when new device classifications need to be added in future Android versions, so that applications targeting older SDK levels do not have to handle unknown enumeration values.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_DEVICE_TYPE:android.hardware.camera2.CameraCharacteristics.Key`

### INFO_DEVICE_TYPE_VIRTUAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INFO_DEVICE_TYPE_VIRTUAL: Int
```

This camera device produces purely virtual images, though they may be based on the output of a real hardware camera in some cases. For example, a virtual reality headset may have a virtual camera as the front-facing camera, producing a virtual avatar to represent the user, which is animated based on sensors on the headset.

The image data should not be assumed to be real.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_DEVICE_TYPE:android.hardware.camera2.CameraCharacteristics.Key`

### INFO_SUPPORTED_HARDWARE_LEVEL_3

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INFO_SUPPORTED_HARDWARE_LEVEL_3: Int
```

This camera device is capable of YUV reprocessing and RAW data capture, in addition to FULL-level capabilities.

The stream configurations listed in the `LEVEL_3`, `RAW`, `FULL`, `LEGACY` and `LIMITED` [tables](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#level-3-additional-guaranteed-configurations) in the documentation are guaranteed to be supported.

The following additional capabilities are guaranteed to be supported:

- `YUV_REPROCESSING` capability (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` contains `YUV_REPROCESSING`)
- `RAW` capability (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` contains `RAW`)

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`

### INFO_SUPPORTED_HARDWARE_LEVEL_EXTERNAL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INFO_SUPPORTED_HARDWARE_LEVEL_EXTERNAL: Int
```

This camera device is backed by an external camera connected to this Android device.

The device has capability identical to a LIMITED level device, with the following exceptions:

- The device may not report lens/sensor related information such as
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_HYPERFOCAL_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PHYSICAL_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_WHITE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_BLACK_LEVEL_PATTERN:android.hardware.camera2.CameraCharacteristics.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT:android.hardware.camera2.CameraCharacteristics.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_ROLLING_SHUTTER_SKEW:android.hardware.camera2.CaptureResult.Key`
- The device will report 0 for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_ORIENTATION:android.hardware.camera2.CameraCharacteristics.Key`
- The device has less guarantee on stable framerate, as the framerate partly depends on the external camera being used.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_HYPERFOCAL_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_BLACK_LEVEL_PATTERN:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PHYSICAL_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_WHITE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_ORIENTATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_ROLLING_SHUTTER_SKEW:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`

### INFO_SUPPORTED_HARDWARE_LEVEL_FULL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INFO_SUPPORTED_HARDWARE_LEVEL_FULL: Int
```

This camera device is capable of supporting advanced imaging applications.

The stream configurations listed in the `FULL`, `LEGACY` and `LIMITED` [tables](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#full-level-additional-guaranteed-configurations) in the documentation are guaranteed to be supported.

A `FULL` device will support below capabilities:

- `BURST_CAPTURE` capability (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` contains `BURST_CAPTURE`)
- Per frame control (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SYNC_MAX_LATENCY:android.hardware.camera2.CameraCharacteristics.Key` `==` PER_FRAME_CONTROL)
- Manual sensor control (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` contains `MANUAL_SENSOR`)
- Manual post-processing control (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` contains `MANUAL_POST_PROCESSING`)
- The required exposure time range defined in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_EXPOSURE_TIME_RANGE:android.hardware.camera2.CameraCharacteristics.Key`
- The required maxFrameDuration defined in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_MAX_FRAME_DURATION:android.hardware.camera2.CameraCharacteristics.Key`

Note: Pre-API level 23, FULL devices also supported arbitrary cropping region (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_CROPPING_TYPE:android.hardware.camera2.CameraCharacteristics.Key` `== FREEFORM`); this requirement was relaxed in API level 23, and `FULL` devices may only support `CENTERED` cropping.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_CROPPING_TYPE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_EXPOSURE_TIME_RANGE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_MAX_FRAME_DURATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SYNC_MAX_LATENCY:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`

### INFO_SUPPORTED_HARDWARE_LEVEL_LEGACY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INFO_SUPPORTED_HARDWARE_LEVEL_LEGACY: Int
```

This camera device is running in backward compatibility mode.

Only the stream configurations listed in the `LEGACY` [table](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#legacy-level-guaranteed-configurations) in the documentation are supported.

A `LEGACY` device does not support per-frame control, manual sensor control, manual post-processing, arbitrary cropping regions, and has relaxed performance constraints. No additional capabilities beyond `BACKWARD_COMPATIBLE` will ever be listed by a `LEGACY` device in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`.

In addition, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key` is not functional on `LEGACY` devices. Instead, every request that includes a JPEG-format output target is treated as triggering a still capture, internally executing a precapture trigger. This may fire the flash for flash power metering during precapture, and then fire the flash for the final capture, if a flash is available on the device and the AE mode is set to enable the flash.

Devices that initially shipped with Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` or newer will not include any LEGACY-level devices.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`

### INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INFO_SUPPORTED_HARDWARE_LEVEL_LIMITED: Int
```

This camera device does not have enough capabilities to qualify as a `FULL` device or better.

Only the stream configurations listed in the `LEGACY` and `LIMITED` [tables](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#limited-level-additional-guaranteed-configurations) in the documentation are guaranteed to be supported.

All `LIMITED` devices support the `BACKWARDS_COMPATIBLE` capability, indicating basic support for color image capture. The only exception is that the device may alternatively support only the `DEPTH_OUTPUT` capability, if it can only output depth measurements and not color images.

`LIMITED` devices and above require the use of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key` to lock exposure metering (and calculate flash power, for cameras with flash) before capturing a high-quality still image.

A `LIMITED` device that only lists the `BACKWARDS_COMPATIBLE` capability is only required to support full-automatic operation and post-processing (`OFF` is not supported for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`, or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`)

Additional capabilities may optionally be supported by a `LIMITED`-level device, and can be checked for in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`

### LENS_FACING_BACK

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_FACING_BACK: Int
```

The camera device faces the opposite direction as the device's screen.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key`

### LENS_FACING_EXTERNAL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_FACING_EXTERNAL: Int
```

The camera device is an external camera, and has no fixed facing relative to the device's screen.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key`

### LENS_FACING_FRONT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_FACING_FRONT: Int
```

The camera device faces the same direction as the device's screen.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key`

### LENS_INFO_FOCUS_DISTANCE_CALIBRATION_APPROXIMATE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_INFO_FOCUS_DISTANCE_CALIBRATION_APPROXIMATE: Int
```

The lens focus distance is measured in diopters.

However, setting the lens to the same focus distance on separate occasions may result in a different real focus distance, depending on factors such as the orientation of the device, the age of the focusing mechanism, and the device temperature.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_FOCUS_DISTANCE_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key`

### LENS_INFO_FOCUS_DISTANCE_CALIBRATION_CALIBRATED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_INFO_FOCUS_DISTANCE_CALIBRATION_CALIBRATED: Int
```

The lens focus distance is measured in diopters, and is calibrated.

The lens mechanism is calibrated so that setting the same focus distance is repeatable on multiple occasions with good accuracy, and the focus distance corresponds to the real physical distance to the plane of best focus.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_FOCUS_DISTANCE_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key`

### LENS_INFO_FOCUS_DISTANCE_CALIBRATION_UNCALIBRATED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_INFO_FOCUS_DISTANCE_CALIBRATION_UNCALIBRATED: Int
```

The lens focus distance is not accurate, and the units used for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key` do not correspond to any physical units.

Setting the lens to the same focus distance on separate occasions may result in a different real focus distance, depending on factors such as the orientation of the device, the age of the focusing mechanism, and the device temperature. The focus distance value will still be in the range of ``[0, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key`]``, where 0 represents the farthest focus.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_FOCUS_DISTANCE_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key`

### LENS_OPTICAL_STABILIZATION_MODE_OFF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_OPTICAL_STABILIZATION_MODE_OFF: Int
```

Optical stabilization is unavailable.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_OPTICAL_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key`

### LENS_OPTICAL_STABILIZATION_MODE_ON

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_OPTICAL_STABILIZATION_MODE_ON: Int
```

Optical stabilization is enabled.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_OPTICAL_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key`

### LENS_POSE_REFERENCE_AUTOMOTIVE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_POSE_REFERENCE_AUTOMOTIVE: Int
```

The value of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` is relative to the origin of the automotive sensor coordinate system, which is at the center of the rear axle.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key`

### LENS_POSE_REFERENCE_GYROSCOPE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_POSE_REFERENCE_GYROSCOPE: Int
```

The value of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` is relative to the position of the primary gyroscope of this Android device.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key`

### LENS_POSE_REFERENCE_PRIMARY_CAMERA

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_POSE_REFERENCE_PRIMARY_CAMERA: Int
```

The value of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` is relative to the optical center of the largest camera device facing the same direction as this camera.

This is the default value for API levels before Android P.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key`

### LENS_POSE_REFERENCE_UNDEFINED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_POSE_REFERENCE_UNDEFINED: Int
```

The camera device cannot represent the values of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key` accurately enough. One such example is a camera device on the cover of a foldable phone: in order to measure the pose translation and rotation, some kind of hinge position sensor would be needed.

The value of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key` must be all zeros, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key` must be values matching its default facing.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key`

### LENS_STATE_MOVING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_STATE_MOVING: Int
```

One or several of the lens parameters (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FILTER_DENSITY:android.hardware.camera2.CaptureRequest.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_APERTURE:android.hardware.camera2.CaptureRequest.Key`) is currently changing.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_APERTURE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FILTER_DENSITY:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#LENS_STATE:android.hardware.camera2.CaptureResult.Key`

### LENS_STATE_STATIONARY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LENS_STATE_STATIONARY: Int
```

The lens parameters (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FILTER_DENSITY:android.hardware.camera2.CaptureRequest.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_APERTURE:android.hardware.camera2.CaptureRequest.Key`) are not changing.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_APERTURE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FILTER_DENSITY:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#LENS_STATE:android.hardware.camera2.CaptureResult.Key`

### LOGICAL_MULTI_CAMERA_SENSOR_SYNC_TYPE_APPROXIMATE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOGICAL_MULTI_CAMERA_SENSOR_SYNC_TYPE_APPROXIMATE: Int
```

A software mechanism is used to synchronize between the physical cameras. As a result, the timestamp of an image from a physical stream is only an approximation of the image sensor start-of-exposure time.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LOGICAL_MULTI_CAMERA_SENSOR_SYNC_TYPE:android.hardware.camera2.CameraCharacteristics.Key`

### LOGICAL_MULTI_CAMERA_SENSOR_SYNC_TYPE_CALIBRATED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOGICAL_MULTI_CAMERA_SENSOR_SYNC_TYPE_CALIBRATED: Int
```

The camera device supports frame timestamp synchronization at the hardware level, and the timestamp of a physical stream image accurately reflects its start-of-exposure time.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LOGICAL_MULTI_CAMERA_SENSOR_SYNC_TYPE:android.hardware.camera2.CameraCharacteristics.Key`

### NOISE_REDUCTION_MODE_FAST

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NOISE_REDUCTION_MODE_FAST: Int
```

Noise reduction is applied without reducing frame rate relative to sensor output. It may be the same as OFF if noise reduction will reduce frame rate relative to sensor.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#NOISE_REDUCTION_MODE:android.hardware.camera2.CaptureRequest.Key`

### NOISE_REDUCTION_MODE_HIGH_QUALITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NOISE_REDUCTION_MODE_HIGH_QUALITY: Int
```

High-quality noise reduction is applied, at the cost of possibly reduced frame rate relative to sensor output.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#NOISE_REDUCTION_MODE:android.hardware.camera2.CaptureRequest.Key`

### NOISE_REDUCTION_MODE_MINIMAL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NOISE_REDUCTION_MODE_MINIMAL: Int
```

MINIMAL noise reduction is applied without reducing frame rate relative to sensor output.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#NOISE_REDUCTION_MODE:android.hardware.camera2.CaptureRequest.Key`

### NOISE_REDUCTION_MODE_OFF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NOISE_REDUCTION_MODE_OFF: Int
```

No noise reduction is applied.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#NOISE_REDUCTION_MODE:android.hardware.camera2.CaptureRequest.Key`

### NOISE_REDUCTION_MODE_ZERO_SHUTTER_LAG

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NOISE_REDUCTION_MODE_ZERO_SHUTTER_LAG: Int
```

Noise reduction is applied at different levels for different output streams, based on resolution. Streams at maximum recording resolution (see android.hardware.camera2.CameraDevice#createCaptureSession) or below have noise reduction applied, while higher-resolution streams have MINIMAL (if supported) or no noise reduction applied (if MINIMAL is not supported.) The degree of noise reduction for low-resolution streams is tuned so that frame rate is not impacted, and the quality is equal to or better than FAST (since it is only applied to lower-resolution outputs, quality may improve from FAST).

This mode is intended to be used by applications operating in a zero-shutter-lag mode with YUV or PRIVATE reprocessing, where the application continuously captures high-resolution intermediate buffers into a circular buffer, from which a final image is produced via reprocessing when a user takes a picture. For such a use case, the high-resolution buffers must not have noise reduction applied to maximize efficiency of preview and to avoid over-applying noise filtering when reprocessing, while low-resolution buffers (used for recording or preview, generally) need noise reduction applied for reasonable preview quality.

This mode is guaranteed to be supported by devices that support either the YUV_REPROCESSING or PRIVATE_REPROCESSING capabilities (`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key` lists either of those capabilities) and it will be the default mode for CAMERA3_TEMPLATE_ZERO_SHUTTER_LAG template.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#NOISE_REDUCTION_MODE:android.hardware.camera2.CaptureRequest.Key`

### REQUEST_AVAILABLE_CAPABILITIES_BACKWARD_COMPATIBLE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_CAPABILITIES_BACKWARD_COMPATIBLE: Int
```

The minimal set of capabilities that every camera device (regardless of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`) supports.

This capability is listed by all normal devices, and indicates that the camera device has a feature set that's comparable to the baseline requirements for the older android.hardware.Camera API.

Devices with the DEPTH_OUTPUT capability might not list this capability, indicating that they support only depth measurement, not standard color output.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_AVAILABLE_CAPABILITIES_BURST_CAPTURE

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_CAPABILITIES_BURST_CAPTURE: Int
```

The camera device supports capturing high-resolution images at \>= 20 frames per second, in at least the uncompressed YUV format, when post-processing settings are set to FAST. Additionally, all image resolutions less than 24 megapixels can be captured at \>= 10 frames per second. Here, 'high resolution' means at least 8 megapixels, or the maximum resolution of the device, whichever is smaller.

More specifically, this means that a size matching the camera device's active array size is listed as a supported size for the `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` format in either android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes or `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighResolutionOutputSizes(kotlin.Int)`, with a minimum frame duration for that format and size of either \<= 1/20 s, or \<= 1/10 s if the image size is less than 24 megapixels, respectively; and the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_TARGET_FPS_RANGES:android.hardware.camera2.CameraCharacteristics.Key` entry lists at least one FPS range where the minimum FPS is \>= 1 / minimumFrameDuration for the maximum-size YUV_420_888 format. If that maximum size is listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighResolutionOutputSizes(kotlin.Int)`, then the list of resolutions for YUV_420_888 from android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes contains at least one resolution \>= 8 megapixels, with a minimum frame duration of \<= 1/20 s.

If the device supports the `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW10:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW12:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW14:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int`, then those can also be captured at the same rate as the maximum-size YUV_420_888 resolution is.

If the device supports the PRIVATE_REPROCESSING capability, then the same guarantees as for the YUV_420_888 format also apply to the `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` format.

In addition, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SYNC_MAX_LATENCY:android.hardware.camera2.CameraCharacteristics.Key` field is guaranteed to have a value between 0 and 4, inclusive. `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_LOCK_AVAILABLE:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AWB_LOCK_AVAILABLE:android.hardware.camera2.CameraCharacteristics.Key` are also guaranteed to be `true` so burst capture with these two locks ON yields consistent image output.

 Value: 6

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_TARGET_FPS_RANGES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_LOCK_AVAILABLE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AWB_LOCK_AVAILABLE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SYNC_MAX_LATENCY:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_AVAILABLE_CAPABILITIES_COLOR_SPACE_PROFILES

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_CAPABILITIES_COLOR_SPACE_PROFILES: Int
```

The device supports querying the possible combinations of color spaces, image formats, and dynamic range profiles supported by the camera and requesting a particular color space for a session via `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration#setColorSpace(android.graphics.ColorSpace.Named)`.

Cameras that enable this capability may or may not also implement dynamic range profiles. If they don't, `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceProfiles#getSupportedDynamicRangeProfiles(android.graphics.ColorSpace.Named,%20kotlin.Int)` will return only `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#STANDARD:kotlin.Long` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceProfiles#getSupportedColorSpacesForDynamicRange(kotlin.Int,%20kotlin.Long)` will assume support of the `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#STANDARD:kotlin.Long` profile in all combinations of color spaces and image formats.

 Value: 20

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_AVAILABLE_CAPABILITIES_CONSTRAINED_HIGH_SPEED_VIDEO

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_CAPABILITIES_CONSTRAINED_HIGH_SPEED_VIDEO: Int
```

The device supports constrained high speed video recording (frame rate \>=120fps) use case. The camera device will support high speed capture session created by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createConstrainedHighSpeedCaptureSession(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)`, which only accepts high speed request lists created by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraConstrainedHighSpeedCaptureSession#createHighSpeedRequestList(android.hardware.camera2.CaptureRequest)`.

A camera device can still support high speed video streaming by advertising the high speed FPS ranges in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_TARGET_FPS_RANGES:android.hardware.camera2.CameraCharacteristics.Key`. For this case, all normal capture request per frame control and synchronization requirements will apply to the high speed fps ranges, the same as all other fps ranges. This capability describes the capability of a specialized operating mode with many limitations (see below), which is only targeted at high speed video recording.

The supported high speed video sizes and fps ranges are specified in `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoFpsRanges()`. To get desired output frame rates, the application is only allowed to select video size and FPS range combinations provided by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoSizes()`. The fps range can be controlled via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key`.

In this capability, the camera device will override aeMode, awbMode, and afMode to ON, AUTO, and CONTINUOUS_VIDEO, respectively. All post-processing block mode controls will be overridden to be FAST. Therefore, no manual control of capture and post-processing parameters is possible. All other controls operate the same as when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key` == AUTO. This means that all other android.control.\* fields continue to work, such as

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_EXPOSURE_COMPENSATION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_LOCK:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_LOCK:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EFFECT_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`

Outside of android.control.\*, the following controls will work:

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_MODE:android.hardware.camera2.CaptureRequest.Key` (TORCH mode only, automatic flash for still capture will not work since aeMode is ON)
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_OPTICAL_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key` (if it is supported)
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_FACE_DETECT_MODE:android.hardware.camera2.CaptureRequest.Key` (if it is supported)

For high speed recording use case, the actual maximum supported frame rate may be lower than what camera can output, depending on the destination Surfaces for the image data. For example, if the destination surface is from video encoder, the application need check if the video encoder is capable of supporting the high frame rate for a given video size, or it will end up with lower recording frame rate. If the destination surface is from preview window, the actual preview frame rate will be bounded by the screen refresh rate.

The camera device will only support up to 2 high speed simultaneous output surfaces (preview and recording surfaces) in this mode. Above controls will be effective only if all of below conditions are true:

- The application creates a camera capture session with no more than 2 surfaces via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createConstrainedHighSpeedCaptureSession(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)`. The targeted surfaces must be preview surface (either from `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#` or `https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#`) or recording surface(either from `https://developer.android.com/reference/kotlin/android/media/MediaRecorder.html#getSurface()` or `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#createInputSurface()`).
- The stream sizes are selected from the sizes reported by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoSizes()`.
- The FPS ranges are selected from `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getHighSpeedVideoFpsRanges()`.

When above conditions are NOT satisfied, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#createConstrainedHighSpeedCaptureSession(kotlin.collections.MutableList,%20android.hardware.camera2.CameraCaptureSession.StateCallback,%20android.os.Handler)` will fail.

Switching to a FPS range that has different maximum FPS may trigger some camera device reconfigurations, which may introduce extra latency. It is recommended that the application avoids unnecessary maximum target FPS changes as much as possible during high speed streaming.

 Value: 9

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#CONTROL_AE_AVAILABLE_TARGET_FPS_RANGES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_EXPOSURE_COMPENSATION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_LOCK:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_PRECAPTURE_TRIGGER:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_TARGET_FPS_RANGE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AF_TRIGGER:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_LOCK:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_REGIONS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_EFFECT_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_ZOOM_RATIO:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#FLASH_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_OPTICAL_STABILIZATION_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_CROP_REGION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_FACE_DETECT_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_AVAILABLE_CAPABILITIES_DEPTH_OUTPUT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_CAPABILITIES_DEPTH_OUTPUT: Int
```

The camera device can produce depth measurements from its field of view.

This capability requires the camera device to support the following:

- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH16:kotlin.Int` is supported as an output format.
- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#DEPTH_POINT_CLOUD:kotlin.Int` is optionally supported as an output format.
- This camera device, and all camera devices with the same `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key`, will list the following calibration metadata entries in both `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult`:
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key`
- The `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#DEPTH_DEPTH_IS_EXCLUSIVE:android.hardware.camera2.CameraCharacteristics.Key` entry is listed by this device.
- As of Android P, the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key` entry is listed by this device.
- A LIMITED camera with only the DEPTH_OUTPUT capability does not have to support normal YUV_420_888, Y8, JPEG, and PRIV-format outputs. It only has to support the DEPTH16 format.

Generally, depth output operates at a slower frame rate than standard color capture, so the DEPTH16 and DEPTH_POINT_CLOUD formats will commonly have a stall duration that should be accounted for (see android.hardware.camera2.params.StreamConfigurationMap#getOutputStallDuration). On a device that supports both depth and color-based output, to enable smooth preview, using a repeating burst is recommended, where a depth-output target is only included once every N frames, where N is the ratio between preview output rate and depth output rate, including depth stall time.

 Value: 8

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#DEPTH_DEPTH_IS_EXCLUSIVE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_FACING:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_AVAILABLE_CAPABILITIES_DYNAMIC_RANGE_TEN_BIT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_CAPABILITIES_DYNAMIC_RANGE_TEN_BIT: Int
```

The device supports one or more 10-bit camera outputs according to the dynamic range profiles specified in `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#getSupportedProfiles()`. They can be configured as part of the capture session initialization via `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#setDynamicRangeProfile(kotlin.Long)`. Cameras that enable this capability must also support the following:

- Profile `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#HLG10:kotlin.Long`
- All mandatory stream combinations for this specific capability as per [documentation](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#10-bit-output-additional-guaranteed-configurations)
- In case the device is not able to capture some combination of supported standard 8-bit and/or 10-bit dynamic range profiles within the same capture request, then those constraints must be listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#getProfileCaptureRequestConstraints(kotlin.Long)`
- Recommended dynamic range profile listed in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_RECOMMENDED_TEN_BIT_DYNAMIC_RANGE_PROFILE:android.hardware.camera2.CameraCharacteristics.Key`.

 Value: 18

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_AVAILABLE_CAPABILITIES_LOGICAL_MULTI_CAMERA

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_CAPABILITIES_LOGICAL_MULTI_CAMERA: Int
```

The camera device is a logical camera backed by two or more physical cameras.

In API level 28, the physical cameras must also be exposed to the application via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList()`.

Starting from API level 29:

- Some or all physical cameras may not be independently exposed to the application, in which case the physical camera IDs will not be available in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraIdList()`. But the application can still query the physical cameras' characteristics by calling `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager#getCameraCharacteristics(kotlin.String)`.
- If a physical camera is hidden from camera ID list, the mandatory stream combinations for that physical camera must be supported through the logical camera using physical streams. One exception is that in API level 30, a physical camera may become unavailable via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.AvailabilityCallback#onPhysicalCameraUnavailable(kotlin.String,%20kotlin.String)` callback.

Combinations of logical and physical streams, or physical streams from different physical cameras are not guaranteed. However, if the camera device supports `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#isSessionConfigurationSupported(android.hardware.camera2.params.SessionConfiguration)`, application must be able to query whether a stream combination involving physical streams is supported by calling `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#isSessionConfigurationSupported(android.hardware.camera2.params.SessionConfiguration)`.

Camera application shouldn't assume that there are at most 1 rear camera and 1 front camera in the system. For an application that switches between front and back cameras, the recommendation is to switch between the first rear camera and the first front camera in the list of supported camera devices.

This capability requires the camera device to support the following:

- The IDs of underlying physical cameras are returned via `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#getPhysicalCameraIds()`.
- This camera device must list static metadata `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LOGICAL_MULTI_CAMERA_SENSOR_SYNC_TYPE:android.hardware.camera2.CameraCharacteristics.Key` in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics`.
- The underlying physical cameras' static metadata must list the following entries, so that the application can correlate pixels from the physical streams:
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key`
- The SENSOR_INFO_TIMESTAMP_SOURCE of the logical device and physical devices must be the same.
- The logical camera must be LIMITED or higher device.

A logical camera device's dynamic metadata may contain `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#LOGICAL_MULTI_CAMERA_ACTIVE_PHYSICAL_ID:android.hardware.camera2.CaptureResult.Key` to notify the application of the current active physical camera Id. An active physical camera is the physical camera from which the logical camera's main image data outputs (YUV or RAW) and metadata come from. In addition, this serves as an indication which physical camera is used to output to a RAW stream, or in case only physical cameras support RAW, which physical RAW stream the application should request.

Logical camera's static metadata tags below describe the default active physical camera. An active physical camera is default if it's used when application directly uses requests built from a template. All templates will default to the same active physical camera.

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_SENSITIVITY_RANGE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_EXPOSURE_TIME_RANGE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_MAX_FRAME_DURATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PHYSICAL_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_WHITE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_LENS_SHADING_APPLIED:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT2:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_CALIBRATION_TRANSFORM1:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_CALIBRATION_TRANSFORM2:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_COLOR_TRANSFORM1:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_COLOR_TRANSFORM2:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_FORWARD_MATRIX1:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_FORWARD_MATRIX2:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_BLACK_LEVEL_PATTERN:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_MAX_ANALOG_SENSITIVITY:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_OPTICAL_BLACK_REGIONS:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_AVAILABLE_TEST_PATTERN_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_HYPERFOCAL_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_FOCUS_DISTANCE_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key`

The field of view of non-RAW physical streams must not be smaller than that of the non-RAW logical streams, or the maximum field-of-view of the physical camera, whichever is smaller. The application should check the physical capture result metadata and physical camera characteristics for how the physical streams are cropped or zoomed. See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key` on how field-of-view is calculated.

Typically the physical stream of active physical camera has the same field-of-view as the logical streams. However, the same may not be true for physical streams from non-active physical cameras. For example, if the logical camera has a wide-ultrawide configuration where the wide lens is the default, when the crop region is set to the logical camera's active array size, (and the zoom ratio set to 1.0 starting from Android 11), a physical stream for the ultrawide camera may prefer outputting images with larger field-of-view than that of the wide camera for better stereo matching margin or more robust motion tracking. At the same time, the physical non-RAW streams' field of view must not be smaller than the requested crop region and zoom ratio, as long as it's within the physical lens' capability. For example, for a logical camera with wide-tele lens configuration where the wide lens is the default, if the logical camera's crop region is set to maximum size, and zoom ratio set to 1.0, the physical stream for the tele lens will be configured to its maximum size crop region (no zoom).

*Deprecated:* Prior to Android 11, the field of view of all non-RAW physical streams cannot be larger than that of non-RAW logical streams. If the logical camera has a wide-ultrawide lens configuration where the wide lens is the default, when the logical camera's crop region is set to maximum size, the FOV of the physical streams for the ultrawide lens will be the same as the logical stream, by making the crop region smaller than its active array size to compensate for the smaller focal length.

For a logical camera, typically the underlying physical cameras have different RAW capabilities (such as resolution or CFA pattern). There are two ways for the application to capture RAW images from the logical camera:

- If the logical camera has RAW capability, the application can create and use RAW streams in the same way as before. In case a RAW stream is configured, to maintain backward compatibility, the camera device makes sure the default active physical camera remains active and does not switch to other physical cameras. (One exception is that, if the logical camera consists of identical image sensors and advertises multiple focalLength due to different lenses, the camera device may generate RAW images from different physical cameras based on the focalLength being set by the application.) This backward-compatible approach usually results in loss of optical zoom, to telephoto lens or to ultrawide lens.
- Alternatively, if supported by the device, `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader` can be used to capture RAW images from one of the underlying physical cameras ( depending on current zoom level). Because different physical cameras may have different RAW characteristics, the application needs to use the characteristics and result metadata of the active physical camera for the relevant RAW metadata.

The capture request and result metadata tags required for backward compatible camera functionalities will be solely based on the logical camera capability. On the other hand, the use of manual capture controls (sensor or post-processing) with a logical camera may result in unexpected behavior when the HAL decides to switch between physical cameras with different characteristics under the hood. For example, when the application manually sets exposure time and sensitivity while zooming in, the brightness of the camera images may suddenly change because HAL switches from one physical camera to the other.

 Value: 11

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_DISTORTION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCAL_LENGTH:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_FOCUS_DISTANCE_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_HYPERFOCAL_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INFO_MINIMUM_FOCUS_DISTANCE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_INTRINSIC_CALIBRATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_REFERENCE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_ROTATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LENS_POSE_TRANSLATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#LOGICAL_MULTI_CAMERA_ACTIVE_PHYSICAL_ID:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#LOGICAL_MULTI_CAMERA_SENSOR_SYNC_TYPE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_AVAILABLE_TEST_PATTERN_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_BLACK_LEVEL_PATTERN:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_CALIBRATION_TRANSFORM1:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_CALIBRATION_TRANSFORM2:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_COLOR_TRANSFORM1:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_COLOR_TRANSFORM2:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_FORWARD_MATRIX1:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_FORWARD_MATRIX2:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_EXPOSURE_TIME_RANGE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_LENS_SHADING_APPLIED:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_MAX_FRAME_DURATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PHYSICAL_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_SENSITIVITY_RANGE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_WHITE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_MAX_ANALOG_SENSITIVITY:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_OPTICAL_BLACK_REGIONS:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT2:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_AVAILABLE_CAPABILITIES_MANUAL_POST_PROCESSING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_CAPABILITIES_MANUAL_POST_PROCESSING: Int
```

The camera device post-processing stages can be manually controlled. The camera device supports basic manual control of the image post-processing stages. This means the following controls are guaranteed to be supported:

- Manual tonemap control

 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_CURVE:android.hardware.camera2.CaptureRequest.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#TONEMAP_MAX_CURVE_POINTS:android.hardware.camera2.CameraCharacteristics.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_GAMMA:android.hardware.camera2.CaptureRequest.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_PRESET_CURVE:android.hardware.camera2.CaptureRequest.Key`
- Manual white balance control

 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key`
- Manual lens shading map control
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SHADING_MODE:android.hardware.camera2.CaptureRequest.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_LENS_SHADING_MAP_MODE:android.hardware.camera2.CaptureRequest.Key`
 - android.statistics.lensShadingMap
 - android.lens.info.shadingMapSize
- Manual aberration correction control (if aberration correction is supported)
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_ABERRATION_MODE:android.hardware.camera2.CaptureRequest.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#COLOR_CORRECTION_AVAILABLE_ABERRATION_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- Auto white balance lock
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_LOCK:android.hardware.camera2.CaptureRequest.Key`

If auto white balance is enabled, then the camera device will accurately report the values applied by AWB in the result.

A given camera device may also support additional post-processing controls, but this capability only covers the above list of controls.

For camera devices with LOGICAL_MULTI_CAMERA capability, when underlying active physical camera switches, tonemap, white balance, and shading map may change even if awb is locked. However, the overall post-processing experience for users will be consistent. Refer to LOGICAL_MULTI_CAMERA capability for details.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_ABERRATION_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#COLOR_CORRECTION_AVAILABLE_ABERRATION_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_GAINS:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#COLOR_CORRECTION_TRANSFORM:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AWB_LOCK:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SHADING_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_LENS_SHADING_MAP_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_CURVE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_GAMMA:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#TONEMAP_MAX_CURVE_POINTS:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_PRESET_CURVE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_AVAILABLE_CAPABILITIES_MANUAL_SENSOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_CAPABILITIES_MANUAL_SENSOR: Int
```

The camera device can be manually controlled (3A algorithms such as auto-exposure, and auto-focus can be bypassed). The camera device supports basic manual control of the sensor image acquisition related stages. This means the following controls are guaranteed to be supported:

- Manual frame duration control
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_MAX_FRAME_DURATION:android.hardware.camera2.CameraCharacteristics.Key`
- Manual exposure control
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_EXPOSURE_TIME_RANGE:android.hardware.camera2.CameraCharacteristics.Key`
- Manual sensitivity control
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_SENSITIVITY_RANGE:android.hardware.camera2.CameraCharacteristics.Key`
- Manual lens control (if the lens is adjustable)
 - android.lens.\*
- Manual flash control (if a flash unit is present)
 - android.flash.\*
- Manual black level locking
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#BLACK_LEVEL_LOCK:android.hardware.camera2.CaptureRequest.Key`
- Auto exposure lock
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_LOCK:android.hardware.camera2.CaptureRequest.Key`

If any of the above 3A algorithms are enabled, then the camera device will accurately report the values applied by 3A in the result.

A given camera device may also support additional manual sensor controls, but this capability only covers the above list of controls.

If this is supported, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key` will additionally return a min frame duration that is greater than zero for each supported size-format combination.

For camera devices with LOGICAL_MULTI_CAMERA capability, when the underlying active physical camera switches, exposureTime, sensitivity, and lens properties may change even if AE/AF is locked. However, the overall auto exposure and auto focus experience for users will be consistent. Refer to LOGICAL_MULTI_CAMERA capability for details.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#BLACK_LEVEL_LOCK:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_AE_LOCK:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_FRAME_DURATION:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_EXPOSURE_TIME_RANGE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_MAX_FRAME_DURATION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_SENSITIVITY_RANGE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_AVAILABLE_CAPABILITIES_MONOCHROME

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_CAPABILITIES_MONOCHROME: Int
```

The camera device is a monochrome camera that doesn't contain a color filter array, and for YUV_420_888 stream, the pixel values on U and V planes are all 128.

A MONOCHROME camera must support the guaranteed stream combinations required for its device level and capabilities. Additionally, if the monochrome camera device supports Y8 format, all mandatory stream combination requirements related to `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` apply to `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int` as well. There are no mandatory stream combination requirements with regard to `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int` for Bayer camera devices.

Starting from Android Q, the SENSOR_INFO_COLOR_FILTER_ARRANGEMENT of a MONOCHROME camera will be either MONO or NIR.

 Value: 12

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_AVAILABLE_CAPABILITIES_MOTION_TRACKING

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_CAPABILITIES_MOTION_TRACKING: Int
```

The camera device supports the MOTION_TRACKING value for `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key`, which limits maximum exposure time to 20 ms.

This limits the motion blur of capture images, resulting in better image tracking results for use cases such as image stabilization or augmented reality.

 Value: 10

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#CONTROL_CAPTURE_INTENT:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_AVAILABLE_CAPABILITIES_OFFLINE_PROCESSING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_CAPABILITIES_OFFLINE_PROCESSING: Int
```

The camera device supports the OFFLINE_PROCESSING use case.

With OFFLINE_PROCESSING capability, the application can switch an ongoing capture session to offline mode by calling the CameraCaptureSession#switchToOffline method and specify streams to be kept in offline mode. The camera will then stop currently active repeating requests, prepare for some requests to go into offline mode, and return an offline session object. After the switchToOffline call returns, the original capture session is in closed state as if the CameraCaptureSession#close method has been called. In the offline mode, all inflight requests will continue to be processed in the background, and the application can immediately close the camera or create a new capture session without losing those requests' output images and capture results.

While the camera device is processing offline requests, it might not be able to support all stream configurations it can support without offline requests. When that happens, the createCaptureSession method call will fail. The following stream configurations are guaranteed to work without hitting the resource busy exception:

- One ongoing offline session: target one output surface of YUV or JPEG format, any resolution.
- The active camera capture session:
 1. One preview surface (SurfaceView or SurfaceTexture) up to 1920 width
 2. One YUV ImageReader surface up to 1920 width
 3. One Jpeg ImageReader, any resolution: the camera device is allowed to slow down JPEG output speed by 50% if there is any ongoing offline session.
 4. If the device supports PRIVATE_REPROCESSING, one pair of ImageWriter/ImageReader surfaces of private format, with the same resolution that is larger or equal to the JPEG ImageReader resolution above.
- Alternatively, the active camera session above can be replaced by an legacy `https://developer.android.com/reference/kotlin/android/hardware/Camera.html#` with the following parameter settings:
 1. Preview size up to 1920 width
 2. Preview callback size up to 1920 width
 3. Video size up to 1920 width
 4. Picture size, any resolution: the camera device is allowed to slow down JPEG output speed by 50% if there is any ongoing offline session.

 Value: 15

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_AVAILABLE_CAPABILITIES_PRIVATE_REPROCESSING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_CAPABILITIES_PRIVATE_REPROCESSING: Int
```

The camera device supports the Zero Shutter Lag reprocessing use case.

- One input stream is supported, that is, `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_MAX_NUM_INPUT_STREAMS:android.hardware.camera2.CameraCharacteristics.Key` == 1 ``.
- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` is supported as an output/input format, that is, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` is included in the lists of formats returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputFormats()`.
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getValidOutputFormatsForInput(kotlin.Int)` returns non-empty int\[\] for each supported input format returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()`.
- Each size returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputSizes(kotlin.Int)` is also included in android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes
- Using `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` does not cause a frame rate drop relative to the sensor's maximum capture rate (at that resolution).
- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` will be reprocessable into both `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` formats.
- For a MONOCHROME camera supporting Y8 format, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` will be reprocessable into `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#Y8:kotlin.Int`.
- The maximum available resolution for PRIVATE streams (both input/output) will match the maximum available resolution of JPEG streams.
- Static metadata `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REPROCESS_MAX_CAPTURE_STALL:android.hardware.camera2.CameraCharacteristics.Key`.
- Only below controls are effective for reprocessing requests and will be present in capture results, other controls in reprocess requests will be ignored by the camera device.
 - android.jpeg.\*
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#NOISE_REDUCTION_MODE:android.hardware.camera2.CaptureRequest.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#EDGE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#NOISE_REDUCTION_AVAILABLE_NOISE_REDUCTION_MODES:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#EDGE_AVAILABLE_EDGE_MODES:android.hardware.camera2.CameraCharacteristics.Key` will both list ZERO_SHUTTER_LAG as a supported mode.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#EDGE_AVAILABLE_EDGE_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#EDGE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#NOISE_REDUCTION_AVAILABLE_NOISE_REDUCTION_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#NOISE_REDUCTION_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REPROCESS_MAX_CAPTURE_STALL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_MAX_NUM_INPUT_STREAMS:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_AVAILABLE_CAPABILITIES_RAW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_CAPABILITIES_RAW: Int
```

The camera device supports outputting RAW buffers and metadata for interpreting them.

Devices supporting the RAW capability allow both for saving DNG files, and for direct application processing of raw sensor images.

- RAW_SENSOR is supported as an output format.
- The maximum available resolution for RAW_SENSOR streams will match either the value in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PIXEL_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` or `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`.
- All DNG-related optional metadata entries are provided by the camera device.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PIXEL_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PRE_CORRECTION_ACTIVE_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_AVAILABLE_CAPABILITIES_READ_SENSOR_SETTINGS

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_CAPABILITIES_READ_SENSOR_SETTINGS: Int
```

The camera device supports accurately reporting the sensor settings for many of the sensor controls while the built-in 3A algorithm is running. This allows reporting of sensor settings even when these settings cannot be manually changed.

The values reported for the following controls are guaranteed to be available in the CaptureResult, including when 3A is enabled:

- Exposure control
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`
- Sensitivity control
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`
- Lens controls (if the lens is adjustable)
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_APERTURE:android.hardware.camera2.CaptureRequest.Key`

This capability is a subset of the MANUAL_SENSOR control capability, and will always be included if the MANUAL_SENSOR capability is available.

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_APERTURE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#LENS_FOCUS_DISTANCE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_EXPOSURE_TIME:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_SENSITIVITY:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_AVAILABLE_CAPABILITIES_REMOSAIC_REPROCESSING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_CAPABILITIES_REMOSAIC_REPROCESSING: Int
```

The device supports reprocessing from the `RAW_SENSOR` format with a bayer pattern given by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_BINNING_FACTOR:android.hardware.camera2.CameraCharacteristics.Key` (m x n group of pixels with the same color filter) to a remosaiced regular bayer pattern.

This capability will only be present for devices with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR:kotlin.Int` capability. When `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR:kotlin.Int` devices do not advertise this capability, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` images will already have a regular bayer pattern.

If a `RAW_SENSOR` stream is requested along with another non-RAW stream in a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest` (if multiple streams are supported when `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` is set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int`), the `RAW_SENSOR` stream will have a regular bayer pattern.

This capability requires the camera device to support the following :

- The `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap` mentioned below refers to the one, described by `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key` ``.
- One input stream is supported, that is, `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_MAX_NUM_INPUT_STREAMS:android.hardware.camera2.CameraCharacteristics.Key` == 1 ``.
- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` is supported as an output/input format, that is, `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` is included in the lists of formats returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputFormats()`.
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getValidOutputFormatsForInput(kotlin.Int)` returns non-empty int\[\] for each supported input format returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()`.
- Each size returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputSizes(kotlin.Int)` is also included in android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes
- Using `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` does not cause a frame rate drop relative to the sensor's maximum capture rate (at that resolution).
- No CaptureRequest controls will be applicable when a request has an input target with `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int` format.

 Value: 17

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_MAX_NUM_INPUT_STREAMS:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_BINNING_FACTOR:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_AVAILABLE_CAPABILITIES_SECURE_IMAGE_DATA

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_CAPABILITIES_SECURE_IMAGE_DATA: Int
```

The camera device is capable of writing image data into a region of memory inaccessible to Android userspace or the Android kernel, and only accessible to trusted execution environments (TEE).

 Value: 13

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_AVAILABLE_CAPABILITIES_STREAM_USE_CASE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_CAPABILITIES_STREAM_USE_CASE: Int
```

The camera device supports selecting a per-stream use case via `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#setStreamUseCase(kotlin.Long)` so that the device can optimize camera pipeline parameters such as tuning, sensor mode, or ISP settings for a specific user scenario. Some sample usages of this capability are:

- Distinguish high quality YUV captures from a regular YUV stream where the image quality may not be as good as the JPEG stream, or
- Use one stream to serve multiple purposes: viewfinder, video recording and still capture. This is common with applications that wish to apply edits equally to preview, saved images, and saved videos.

This capability requires the camera device to support the following stream use cases:

- DEFAULT for backward compatibility where the application doesn't set a stream use case
- PREVIEW for live viewfinder and in-app image analysis
- STILL_CAPTURE for still photo capture
- VIDEO_RECORD for recording video clips
- PREVIEW_VIDEO_STILL for one single stream used for viewfinder, video recording, and still capture.
- VIDEO_CALL for long running video calls

`https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_STREAM_USE_CASES:android.hardware.camera2.CameraCharacteristics.Key` lists all of the supported stream use cases.

Refer to the [guideline](https://developer.android.com/reference/android/hardware/camera2/CameraDevice#stream-use-case-capability-additional-guaranteed-configurations) for the mandatory stream combinations involving stream use cases, which can also be queried via `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination`.

 Value: 19

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_AVAILABLE_CAPABILITIES_SYSTEM_CAMERA

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_CAPABILITIES_SYSTEM_CAMERA: Int
```

The camera device is only accessible by Android's system components and privileged applications. Processes need to have the android.permission.SYSTEM_CAMERA in addition to android.permission.CAMERA in order to connect to this camera device.

 Value: 14

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_CAPABILITIES_ULTRA_HIGH_RESOLUTION_SENSOR: Int
```

This camera device is capable of producing ultra high resolution images in addition to the image sizes described in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key`. It can operate in 'default' mode and 'max resolution' mode. It generally does this by binning pixels in 'default' mode and not binning them in 'max resolution' mode. `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key` `` describes the streams supported in 'default' mode. The stream configurations supported in 'max resolution' mode are described by `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key` ``. The maximum resolution mode pixel array size of a camera device (`` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PIXEL_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key` ``) with this capability, will be at least 24 megapixels.

 Value: 16

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_PIXEL_ARRAY_SIZE:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`

### REQUEST_AVAILABLE_CAPABILITIES_YUV_REPROCESSING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_AVAILABLE_CAPABILITIES_YUV_REPROCESSING: Int
```

The camera device supports the YUV_420_888 reprocessing use case, similar as PRIVATE_REPROCESSING, This capability requires the camera device to support the following:

- One input stream is supported, that is, `` `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_MAX_NUM_INPUT_STREAMS:android.hardware.camera2.CameraCharacteristics.Key` == 1 ``.
- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` is supported as an output/input format, that is, YUV_420_888 is included in the lists of formats returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getOutputFormats()`.
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getValidOutputFormatsForInput(kotlin.Int)` returns non-empty int\[\] for each supported input format returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputFormats()`.
- Each size returned by `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap#getInputSizes(kotlin.Int)` is also included in android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes
- Using `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` does not cause a frame rate drop relative to the sensor's maximum capture rate (at that resolution).
- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` will be reprocessable into both `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` formats.
- The maximum available resolution for `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` streams (both input/output) will match the maximum available resolution of `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` streams.
- For a MONOCHROME camera with Y8 format support, all the requirements mentioned above for YUV_420_888 apply for Y8 format as well.
- Static metadata `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REPROCESS_MAX_CAPTURE_STALL:android.hardware.camera2.CameraCharacteristics.Key`.
- Only the below controls are effective for reprocessing requests and will be present in capture results. The reprocess requests are from the original capture results that are associated with the intermediate `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YUV_420_888:kotlin.Int` output buffers. All other controls in the reprocess requests will be ignored by the camera device.
 - android.jpeg.\*
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#NOISE_REDUCTION_MODE:android.hardware.camera2.CaptureRequest.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#EDGE_MODE:android.hardware.camera2.CaptureRequest.Key`
 - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#REPROCESS_EFFECTIVE_EXPOSURE_FACTOR:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#NOISE_REDUCTION_AVAILABLE_NOISE_REDUCTION_MODES:android.hardware.camera2.CameraCharacteristics.Key` and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#EDGE_AVAILABLE_EDGE_MODES:android.hardware.camera2.CameraCharacteristics.Key` will both list ZERO_SHUTTER_LAG as a supported mode.

 Value: 7

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#EDGE_AVAILABLE_EDGE_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#EDGE_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#NOISE_REDUCTION_AVAILABLE_NOISE_REDUCTION_MODES:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#NOISE_REDUCTION_MODE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#REPROCESS_EFFECTIVE_EXPOSURE_FACTOR:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REPROCESS_MAX_CAPTURE_STALL:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_MAX_NUM_INPUT_STREAMS:android.hardware.camera2.CameraCharacteristics.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES:android.hardware.camera2.CameraCharacteristics.Key`

### SCALER_AVAILABLE_STREAM_USE_CASES_CROPPED_RAW

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_AVAILABLE_STREAM_USE_CASES_CROPPED_RAW: Int
```

Cropped RAW stream when the client chooses to crop the field of view.

Certain types of image sensors can run in binned modes in order to improve signal to noise ratio while capturing frames. However, at certain zoom levels and / or when other scene conditions are deemed fit, the camera sub-system may choose to un-bin and remosaic the sensor's output. This results in a RAW frame which is cropped in field of view and yet has the same number of pixels as full field of view RAW, thereby improving image detail.

The resultant field of view of the RAW stream will be greater than or equal to croppable non-RAW streams. The effective crop region for this RAW stream will be reflected in the CaptureResult key `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SCALER_RAW_CROP_REGION:android.hardware.camera2.CaptureResult.Key`.

If this stream use case is set on a non-RAW stream, i.e. not one of :

- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_SENSOR:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW10:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW12:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW14:kotlin.Int`

session configuration is not guaranteed to succeed.

This stream use case may not be supported on some devices.

 Value: 6

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SCALER_RAW_CROP_REGION:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_STREAM_USE_CASES:android.hardware.camera2.CameraCharacteristics.Key`

### SCALER_AVAILABLE_STREAM_USE_CASES_DEFAULT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_AVAILABLE_STREAM_USE_CASES_DEFAULT: Int
```

Default stream use case.

This use case is the same as when the application doesn't set any use case for the stream. The camera device uses the properties of the output target, such as format, dataSpace, or surface class type, to optimize the image processing pipeline.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_STREAM_USE_CASES:android.hardware.camera2.CameraCharacteristics.Key`

### SCALER_AVAILABLE_STREAM_USE_CASES_PREVIEW

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_AVAILABLE_STREAM_USE_CASES_PREVIEW: Int
```

Live stream shown to the user.

Optimized for performance and usability as a viewfinder, but not necessarily for image quality. The output is not meant to be persisted as saved images or video.

No stall if android.control.\* are set to FAST. There may be stall if they are set to HIGH_QUALITY. This use case has the same behavior as the default SurfaceView and SurfaceTexture targets. Additionally, this use case can be used for in-app image analysis.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_STREAM_USE_CASES:android.hardware.camera2.CameraCharacteristics.Key`

### SCALER_AVAILABLE_STREAM_USE_CASES_PREVIEW_VIDEO_STILL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_AVAILABLE_STREAM_USE_CASES_PREVIEW_VIDEO_STILL: Int
```

One single stream used for combined purposes of preview, video, and still capture.

For such multi-purpose streams, the camera device aims to make the best tradeoff between the individual use cases. For example, the STILL_CAPTURE use case by itself may have stalls for achieving best image quality. But if combined with PREVIEW and VIDEO_RECORD, the camera device needs to trade off the additional image processing for speed so that preview and video recording aren't slowed down.

Similarly, VIDEO_RECORD may produce frames with a substantial lag, but PREVIEW_VIDEO_STILL must have minimal output delay. This means that to enable video stabilization with this use case, the device must support and the app must select the PREVIEW_STABILIZATION mode for video stabilization.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_STREAM_USE_CASES:android.hardware.camera2.CameraCharacteristics.Key`

### SCALER_AVAILABLE_STREAM_USE_CASES_STILL_CAPTURE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_AVAILABLE_STREAM_USE_CASES_STILL_CAPTURE: Int
```

Still photo capture.

Optimized for high-quality high-resolution capture, and not expected to maintain preview-like frame rates.

The stream may have stalls regardless of whether android.control.\* is HIGH_QUALITY. This use case has the same behavior as the default JPEG and RAW related formats.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_STREAM_USE_CASES:android.hardware.camera2.CameraCharacteristics.Key`

### SCALER_AVAILABLE_STREAM_USE_CASES_VIDEO_CALL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_AVAILABLE_STREAM_USE_CASES_VIDEO_CALL: Int
```

Long-running video call optimized for both power efficiency and video quality.

The camera sensor may run in a lower-resolution mode to reduce power consumption at the cost of some image and digital zoom quality. Unlike VIDEO_RECORD, VIDEO_CALL outputs are expected to work in dark conditions, so are usually accompanied with variable frame rate settings to allow sufficient exposure time in low light.

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_STREAM_USE_CASES:android.hardware.camera2.CameraCharacteristics.Key`

### SCALER_AVAILABLE_STREAM_USE_CASES_VIDEO_RECORD

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_AVAILABLE_STREAM_USE_CASES_VIDEO_RECORD: Int
```

Recording video clips.

Optimized for high-quality video capture, including high-quality image stabilization if supported by the device and enabled by the application. As a result, may produce output frames with a substantial lag from real time, to allow for highest-quality stabilization or other processing. As such, such an output is not suitable for drawing to screen directly, and is expected to be persisted to disk or similar for later playback or processing. Only streams that set the VIDEO_RECORD use case are guaranteed to have video stabilization applied when the video stabilization control is set to ON, as opposed to PREVIEW_STABILIZATION.

This use case has the same behavior as the default MediaRecorder and MediaCodec targets.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_STREAM_USE_CASES:android.hardware.camera2.CameraCharacteristics.Key`

### SCALER_CROPPING_TYPE_CENTER_ONLY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_CROPPING_TYPE_CENTER_ONLY: Int
```

The camera device only supports centered crop regions.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_CROPPING_TYPE:android.hardware.camera2.CameraCharacteristics.Key`

### SCALER_CROPPING_TYPE_FREEFORM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_CROPPING_TYPE_FREEFORM: Int
```

The camera device supports arbitrarily chosen crop regions.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SCALER_CROPPING_TYPE:android.hardware.camera2.CameraCharacteristics.Key`

### SCALER_ROTATE_AND_CROP_180

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_ROTATE_AND_CROP_180: Int
```

Processed images are rotated by 180 degrees. Since the aspect ratio does not change, no cropping is performed.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_ROTATE_AND_CROP:android.hardware.camera2.CaptureRequest.Key`

### SCALER_ROTATE_AND_CROP_270

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_ROTATE_AND_CROP_270: Int
```

Processed images are rotated by 270 degrees clockwise, and then cropped to the original aspect ratio.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_ROTATE_AND_CROP:android.hardware.camera2.CaptureRequest.Key`

### SCALER_ROTATE_AND_CROP_90

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_ROTATE_AND_CROP_90: Int
```

Processed images are rotated by 90 degrees clockwise, and then cropped to the original aspect ratio.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_ROTATE_AND_CROP:android.hardware.camera2.CaptureRequest.Key`

### SCALER_ROTATE_AND_CROP_AUTO

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_ROTATE_AND_CROP_AUTO: Int
```

The camera API automatically selects the best concrete value for rotate-and-crop based on the application's support for resizability and the current multi-window mode.

If the application does not support resizing but the display mode for its main Activity is not in a typical orientation, the camera API will set `ROTATE_AND_CROP_90` or some other supported rotation value, depending on device configuration, to ensure preview and captured images are correctly shown to the user. Otherwise, `ROTATE_AND_CROP_NONE` will be selected.

When a value other than NONE is selected, several metadata fields will also be parsed differently to ensure that coordinates are correctly handled for features like drawing face detection boxes or passing in tap-to-focus coordinates. The camera API will convert positions in the active array coordinate system to/from the cropped-and-rotated coordinate system to make the operation transparent for applications.

No coordinate mapping will be done when the application selects a non-AUTO mode.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_ROTATE_AND_CROP:android.hardware.camera2.CaptureRequest.Key`

### SCALER_ROTATE_AND_CROP_NONE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCALER_ROTATE_AND_CROP_NONE: Int
```

No rotate and crop is applied. Processed outputs are in the sensor orientation.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SCALER_ROTATE_AND_CROP:android.hardware.camera2.CaptureRequest.Key`

### SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_BGGR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_BGGR: Int
```

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_GBRG

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_GBRG: Int
```

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_GRBG

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_GRBG: Int
```

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_MONO

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_MONO: Int
```

Sensor doesn't have any Bayer color filter. Such sensor captures visible light in monochrome. The exact weighting and wavelengths captured is not specified, but generally only includes the visible frequencies. This value implies a MONOCHROME camera.

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_NIR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_NIR: Int
```

Sensor has a near infrared filter capturing light with wavelength between roughly 750nm and 1400nm, and the same filter covers the whole sensor array. This value implies a MONOCHROME camera.

 Value: 6

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_RGB

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_RGB: Int
```

Sensor is not Bayer; output has 3 16-bit values for each pixel, instead of just 1 16-bit value per pixel.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_RGGB

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_COLOR_FILTER_ARRANGEMENT_RGGB: Int
```

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_COLOR_FILTER_ARRANGEMENT:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_INFO_TIMESTAMP_SOURCE_REALTIME

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_TIMESTAMP_SOURCE_REALTIME: Int
```

Timestamps from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_TIMESTAMP:android.hardware.camera2.CaptureResult.Key` are in the same timebase as `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtimeNanos()`, and they can be compared to other timestamps using that base.

When buffers from a REALTIME device are passed directly to a video encoder from the camera, automatic compensation is done to account for differing timebases of the audio and camera subsystems. If the application is receiving buffers and then later sending them to a video encoder or other application where they are compared with audio subsystem timestamps or similar, this compensation is not present. In those cases, applications need to adjust the timestamps themselves. Since `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtimeNanos()` and `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()` only diverge while the device is asleep, an offset between the two sources can be measured once per active session and applied to timestamps for sufficient accuracy for A/V sync.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_TIMESTAMP:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_TIMESTAMP_SOURCE:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_INFO_TIMESTAMP_SOURCE_UNKNOWN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_INFO_TIMESTAMP_SOURCE_UNKNOWN: Int
```

Timestamps from `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_TIMESTAMP:android.hardware.camera2.CaptureResult.Key` are in nanoseconds and monotonic, but can not be compared to timestamps from other subsystems (e.g. accelerometer, gyro etc.), or other instances of the same or different camera devices in the same system with accuracy. However, the timestamps are roughly in the same timebase as `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()`. The accuracy is sufficient for tasks like A/V synchronization for video recording, at least, and the timestamps can be directly used together with timestamps from the audio subsystem for that task.

Timestamps between streams and results for a single camera instance are comparable, and the timestamps for all buffers and the result metadata generated by a single capture are identical.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#SENSOR_TIMESTAMP:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_INFO_TIMESTAMP_SOURCE:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_PIXEL_MODE_DEFAULT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_PIXEL_MODE_DEFAULT: Int
```

This is the default sensor pixel mode.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`

### SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION: Int
```

In this mode, sensors typically do not bin pixels, as a result can offer larger image sizes.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`

### SENSOR_READOUT_TIMESTAMP_HARDWARE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_READOUT_TIMESTAMP_HARDWARE: Int
```

This camera device supports the onReadoutStarted callback as well as outputting readout timestamps. The readout timestamp is generated by the camera hardware and it has the same accuracy and timing characteristics of the start-of-exposure time.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_READOUT_TIMESTAMP:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_READOUT_TIMESTAMP_NOT_SUPPORTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_READOUT_TIMESTAMP_NOT_SUPPORTED: Int
```

This camera device doesn't support readout timestamp and onReadoutStarted callback.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_READOUT_TIMESTAMP:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_REFERENCE_ILLUMINANT1_CLOUDY_WEATHER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_REFERENCE_ILLUMINANT1_CLOUDY_WEATHER: Int
```

 Value: 10

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_REFERENCE_ILLUMINANT1_COOL_WHITE_FLUORESCENT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_REFERENCE_ILLUMINANT1_COOL_WHITE_FLUORESCENT: Int
```

W 3900 - 4500K

 Value: 14

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_REFERENCE_ILLUMINANT1_D50

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_REFERENCE_ILLUMINANT1_D50: Int
```

 Value: 23

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_REFERENCE_ILLUMINANT1_D55

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_REFERENCE_ILLUMINANT1_D55: Int
```

 Value: 20

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_REFERENCE_ILLUMINANT1_D65

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_REFERENCE_ILLUMINANT1_D65: Int
```

 Value: 21

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_REFERENCE_ILLUMINANT1_D75

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_REFERENCE_ILLUMINANT1_D75: Int
```

 Value: 22

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_REFERENCE_ILLUMINANT1_DAYLIGHT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_REFERENCE_ILLUMINANT1_DAYLIGHT: Int
```

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_REFERENCE_ILLUMINANT1_DAYLIGHT_FLUORESCENT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_REFERENCE_ILLUMINANT1_DAYLIGHT_FLUORESCENT: Int
```

D 5700 - 7100K

 Value: 12

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_REFERENCE_ILLUMINANT1_DAY_WHITE_FLUORESCENT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_REFERENCE_ILLUMINANT1_DAY_WHITE_FLUORESCENT: Int
```

N 4600 - 5400K

 Value: 13

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_REFERENCE_ILLUMINANT1_FINE_WEATHER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_REFERENCE_ILLUMINANT1_FINE_WEATHER: Int
```

 Value: 9

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_REFERENCE_ILLUMINANT1_FLASH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_REFERENCE_ILLUMINANT1_FLASH: Int
```

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_REFERENCE_ILLUMINANT1_FLUORESCENT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_REFERENCE_ILLUMINANT1_FLUORESCENT: Int
```

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_REFERENCE_ILLUMINANT1_ISO_STUDIO_TUNGSTEN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_REFERENCE_ILLUMINANT1_ISO_STUDIO_TUNGSTEN: Int
```

 Value: 24

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_REFERENCE_ILLUMINANT1_SHADE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_REFERENCE_ILLUMINANT1_SHADE: Int
```

 Value: 11

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_REFERENCE_ILLUMINANT1_STANDARD_A

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_REFERENCE_ILLUMINANT1_STANDARD_A: Int
```

 Value: 17

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_REFERENCE_ILLUMINANT1_STANDARD_B

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_REFERENCE_ILLUMINANT1_STANDARD_B: Int
```

 Value: 18

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_REFERENCE_ILLUMINANT1_STANDARD_C

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_REFERENCE_ILLUMINANT1_STANDARD_C: Int
```

 Value: 19

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_REFERENCE_ILLUMINANT1_TUNGSTEN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_REFERENCE_ILLUMINANT1_TUNGSTEN: Int
```

Incandescent light

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_REFERENCE_ILLUMINANT1_WHITE_FLUORESCENT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_REFERENCE_ILLUMINANT1_WHITE_FLUORESCENT: Int
```

WW 3200 - 3700K

 Value: 15

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SENSOR_REFERENCE_ILLUMINANT1:android.hardware.camera2.CameraCharacteristics.Key`

### SENSOR_TEST_PATTERN_MODE_COLOR_BARS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_TEST_PATTERN_MODE_COLOR_BARS: Int
```

All pixel data is replaced with an 8-bar color pattern.

The vertical bars (left-to-right) are as follows:

- 100% white
- yellow
- cyan
- green
- magenta
- red
- blue
- black

In general the image would look like the following:

```kotlin
<code>W Y C G M R B K
  W Y C G M R B K
  W Y C G M R B K
  W Y C G M R B K
  W Y C G M R B K
  . . . . . . . .
  . . . . . . . .
  . . . . . . . .
 
  (B = Blue, K = Black)
  </code>
```

Each bar should take up 1/8 of the sensor pixel array width. When this is not possible, the bar size should be rounded down to the nearest integer and the pattern can repeat on the right side.

Each bar's height must always take up the full sensor pixel array height.

Each pixel in this test pattern must be set to either 0% intensity or 100% intensity.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_TEST_PATTERN_MODE:android.hardware.camera2.CaptureRequest.Key`

### SENSOR_TEST_PATTERN_MODE_COLOR_BARS_FADE_TO_GRAY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_TEST_PATTERN_MODE_COLOR_BARS_FADE_TO_GRAY: Int
```

The test pattern is similar to COLOR_BARS, except that each bar should start at its specified color at the top, and fade to gray at the bottom.

Furthermore each bar is further subdivided into a left and right half. The left half should have a smooth gradient, and the right half should have a quantized gradient.

In particular, the right half's should consist of blocks of the same color for 1/16th active sensor pixel array width.

The least significant bits in the quantized gradient should be copied from the most significant bits of the smooth gradient.

The height of each bar should always be a multiple of 128. When this is not the case, the pattern should repeat at the bottom of the image.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_TEST_PATTERN_MODE:android.hardware.camera2.CaptureRequest.Key`

### SENSOR_TEST_PATTERN_MODE_CUSTOM1

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_TEST_PATTERN_MODE_CUSTOM1: Int
```

The first custom test pattern. All custom patterns that are available only on this camera device are at least this numeric value.

All of the custom test patterns will be static (that is the raw image must not vary from frame to frame).

 Value: 256

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_TEST_PATTERN_MODE:android.hardware.camera2.CaptureRequest.Key`

### SENSOR_TEST_PATTERN_MODE_OFF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_TEST_PATTERN_MODE_OFF: Int
```

No test pattern mode is used, and the camera device returns captures from the image sensor.

This is the default if the key is not set.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_TEST_PATTERN_MODE:android.hardware.camera2.CaptureRequest.Key`

### SENSOR_TEST_PATTERN_MODE_PN9

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_TEST_PATTERN_MODE_PN9: Int
```

All pixel data is replaced by a pseudo-random sequence generated from a PN9 512-bit sequence (typically implemented in hardware with a linear feedback shift register).

The generator should be reset at the beginning of each frame, and thus each subsequent raw frame with this test pattern should be exactly the same as the last.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_TEST_PATTERN_MODE:android.hardware.camera2.CaptureRequest.Key`

### SENSOR_TEST_PATTERN_MODE_SOLID_COLOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SENSOR_TEST_PATTERN_MODE_SOLID_COLOR: Int
```

Each pixel in `[R, G_even, G_odd, B]` is replaced by its respective color channel provided in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_TEST_PATTERN_DATA:android.hardware.camera2.CaptureRequest.Key`.

For example:

```kotlin
<code><code><a docref="android.hardware.camera2.CaptureRequest$SENSOR_TEST_PATTERN_DATA">android.sensor.testPatternData</a></code> = [0, 0xFFFFFFFF, 0xFFFFFFFF, 0]
  </code>
```

All green pixels are 100% green. All red/blue pixels are black.

```kotlin
<code><code><a docref="android.hardware.camera2.CaptureRequest$SENSOR_TEST_PATTERN_DATA">android.sensor.testPatternData</a></code> = [0xFFFFFFFF, 0, 0xFFFFFFFF, 0]
  </code>
```

All red pixels are 100% red. Only the odd green pixels are 100% green. All blue pixels are 100% black.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_TEST_PATTERN_DATA:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SENSOR_TEST_PATTERN_MODE:android.hardware.camera2.CaptureRequest.Key`

### SHADING_MODE_FAST

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SHADING_MODE_FAST: Int
```

Apply lens shading corrections, without slowing frame rate relative to sensor raw output

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SHADING_MODE:android.hardware.camera2.CaptureRequest.Key`

### SHADING_MODE_HIGH_QUALITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SHADING_MODE_HIGH_QUALITY: Int
```

Apply high-quality lens shading correction, at the cost of possibly reduced frame rate.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SHADING_MODE:android.hardware.camera2.CaptureRequest.Key`

### SHADING_MODE_OFF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SHADING_MODE_OFF: Int
```

No lens shading correction is applied.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#SHADING_MODE:android.hardware.camera2.CaptureRequest.Key`

### STATISTICS_FACE_DETECT_MODE_FULL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATISTICS_FACE_DETECT_MODE_FULL: Int
```

Return all face metadata.

In this mode, face rectangles, scores, landmarks, and face IDs are all valid.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_FACE_DETECT_MODE:android.hardware.camera2.CaptureRequest.Key`

### STATISTICS_FACE_DETECT_MODE_OFF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATISTICS_FACE_DETECT_MODE_OFF: Int
```

Do not include face detection statistics in capture results.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_FACE_DETECT_MODE:android.hardware.camera2.CaptureRequest.Key`

### STATISTICS_FACE_DETECT_MODE_SIMPLE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATISTICS_FACE_DETECT_MODE_SIMPLE: Int
```

Return face rectangle and confidence values only.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_FACE_DETECT_MODE:android.hardware.camera2.CaptureRequest.Key`

### STATISTICS_LENS_SHADING_MAP_MODE_OFF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATISTICS_LENS_SHADING_MAP_MODE_OFF: Int
```

Do not include a lens shading map in the capture result.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_LENS_SHADING_MAP_MODE:android.hardware.camera2.CaptureRequest.Key`

### STATISTICS_LENS_SHADING_MAP_MODE_ON

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATISTICS_LENS_SHADING_MAP_MODE_ON: Int
```

Include a lens shading map in the capture result.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_LENS_SHADING_MAP_MODE:android.hardware.camera2.CaptureRequest.Key`

### STATISTICS_OIS_DATA_MODE_OFF

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATISTICS_OIS_DATA_MODE_OFF: Int
```

Do not include OIS data in the capture result.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_OIS_DATA_MODE:android.hardware.camera2.CaptureRequest.Key`

### STATISTICS_OIS_DATA_MODE_ON

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATISTICS_OIS_DATA_MODE_ON: Int
```

Include OIS data in the capture result.

`https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_OIS_SAMPLES:android.hardware.camera2.CaptureResult.Key` provides OIS sample data in the output result metadata.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_OIS_SAMPLES:android.hardware.camera2.CaptureResult.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#STATISTICS_OIS_DATA_MODE:android.hardware.camera2.CaptureRequest.Key`

### STATISTICS_SCENE_FLICKER_50HZ

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATISTICS_SCENE_FLICKER_50HZ: Int
```

The camera device detects illumination flickering at 50Hz in the current scene.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_SCENE_FLICKER:android.hardware.camera2.CaptureResult.Key`

### STATISTICS_SCENE_FLICKER_60HZ

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATISTICS_SCENE_FLICKER_60HZ: Int
```

The camera device detects illumination flickering at 60Hz in the current scene.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_SCENE_FLICKER:android.hardware.camera2.CaptureResult.Key`

### STATISTICS_SCENE_FLICKER_NONE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATISTICS_SCENE_FLICKER_NONE: Int
```

The camera device does not detect any flickering illumination in the current scene.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult#STATISTICS_SCENE_FLICKER:android.hardware.camera2.CaptureResult.Key`

### SYNC_MAX_LATENCY_PER_FRAME_CONTROL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYNC_MAX_LATENCY_PER_FRAME_CONTROL: Int
```

Every frame has the requests immediately applied.

Changing controls over multiple requests one after another will produce results that have those controls applied atomically each frame.

All FULL capability devices will have this as their maxLatency.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SYNC_MAX_LATENCY:android.hardware.camera2.CameraCharacteristics.Key`

### SYNC_MAX_LATENCY_UNKNOWN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYNC_MAX_LATENCY_UNKNOWN: Int
```

Each new frame has some subset (potentially the entire set) of the past requests applied to the camera settings.

By submitting a series of identical requests, the camera device will eventually have the camera settings applied, but it is unknown when that exact point will be.

All LEGACY capability devices will have this as their maxLatency.

 Value: -1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics#SYNC_MAX_LATENCY:android.hardware.camera2.CameraCharacteristics.Key`

### TONEMAP_MODE_CONTRAST_CURVE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TONEMAP_MODE_CONTRAST_CURVE: Int
```

Use the tone mapping curve specified in the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_CURVE:android.hardware.camera2.CaptureRequest.Key`\* entries.

All color enhancement and tonemapping must be disabled, except for applying the tonemapping curve specified by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_CURVE:android.hardware.camera2.CaptureRequest.Key`.

Must not slow down frame rate relative to raw sensor output.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_CURVE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key`

### TONEMAP_MODE_FAST

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TONEMAP_MODE_FAST: Int
```

Advanced gamma mapping and color enhancement may be applied, without reducing frame rate compared to raw sensor output.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key`

### TONEMAP_MODE_GAMMA_VALUE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TONEMAP_MODE_GAMMA_VALUE: Int
```

Use the gamma value specified in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_GAMMA:android.hardware.camera2.CaptureRequest.Key` to perform tonemapping.

All color enhancement and tonemapping must be disabled, except for applying the tonemapping curve specified by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_GAMMA:android.hardware.camera2.CaptureRequest.Key`.

Must not slow down frame rate relative to raw sensor output.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_GAMMA:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key`

### TONEMAP_MODE_HIGH_QUALITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TONEMAP_MODE_HIGH_QUALITY: Int
```

High-quality gamma mapping and color enhancement will be applied, at the cost of possibly reduced frame rate compared to raw sensor output.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key`

### TONEMAP_MODE_PRESET_CURVE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TONEMAP_MODE_PRESET_CURVE: Int
```

Use the preset tonemapping curve specified in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_PRESET_CURVE:android.hardware.camera2.CaptureRequest.Key` to perform tonemapping.

All color enhancement and tonemapping must be disabled, except for applying the tonemapping curve specified by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_PRESET_CURVE:android.hardware.camera2.CaptureRequest.Key`.

Must not slow down frame rate relative to raw sensor output.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_PRESET_CURVE:android.hardware.camera2.CaptureRequest.Key`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_MODE:android.hardware.camera2.CaptureRequest.Key`

### TONEMAP_PRESET_CURVE_REC709

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TONEMAP_PRESET_CURVE_REC709: Int
```

Tonemapping curve is defined by ITU-R BT.709

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_PRESET_CURVE:android.hardware.camera2.CaptureRequest.Key`

### TONEMAP_PRESET_CURVE_SRGB

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TONEMAP_PRESET_CURVE_SRGB: Int
```

Tonemapping curve is defined by sRGB

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest#TONEMAP_PRESET_CURVE:android.hardware.camera2.CaptureRequest.Key`

## Public methods

### getKeys

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getKeys(): MutableList<TKey>
```

Returns a list of the keys contained in this map.

The list returned is not modifiable, so any attempts to modify it will throw a `UnsupportedOperationException`.

All values retrieved by a key from this list with `get` are guaranteed to be non-`null`. Each key is only listed once in the list. The order of the keys is undefined.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<TKey>` | List of the keys contained in this map. |
