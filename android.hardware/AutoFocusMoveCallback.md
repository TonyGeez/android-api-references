# Camera.AutoFocusMoveCallback

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AutoFocusMoveCallback

Kotlin| [Java](https://developer.android.com/reference/android/hardware/Camera.AutoFocusMoveCallback "View this page in Java") 

```
interface AutoFocusMoveCallback
```

| [android.hardware.Camera.AutoFocusMoveCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.AutoFocusMoveCallback#) |

| **This interface was deprecated in API level 21.**
|
| We recommend using the new [android.hardware.camera2](https://developer.android.com/reference/kotlin/android/hardware/camera2/package-summary) API for new applications.

Callback interface used to notify on auto focus start and stop.

This is only supported in continuous autofocus modes -- [android.hardware.Camera.Parameters#FOCUS_MODE_CONTINUOUS_VIDEO](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#FOCUS_MODE_CONTINUOUS_VIDEO:kotlin.String) and [android.hardware.Camera.Parameters#FOCUS_MODE_CONTINUOUS_PICTURE](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#FOCUS_MODE_CONTINUOUS_PICTURE:kotlin.String). Applications can show autofocus animation based on this.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAutoFocusMoving](https://developer.android.com/reference/kotlin/android/hardware/Camera.AutoFocusMoveCallback#onAutoFocusMoving(kotlin.Boolean,%20android.hardware.Camera))`(`start:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `camera:` ` [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera)!`)` Called when the camera auto focus starts or stops. |

## Public methods

### onAutoFocusMoving

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAutoFocusMoving(
    start: Boolean, 
    camera: Camera!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the camera auto focus starts or stops.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `start` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if focus starts to move, false if focus stops to move |
| `camera` | [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera)!:the Camera service object |
