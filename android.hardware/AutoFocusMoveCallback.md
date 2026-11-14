# Camera.AutoFocusMoveCallback

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AutoFocusMoveCallback

Kotlin| [Java](../android/hardware/Camera.AutoFocusMoveCallback.md) 
| --- | --- |

```
interface AutoFocusMoveCallback
```

| [android.hardware.Camera.AutoFocusMoveCallback](../android/hardware/Camera.AutoFocusMoveCallback.md) |

| **This interface was deprecated in API level 21.**
|
| We recommend using the new [android.hardware.camera2](../android/hardware/camera2/_package.md) API for new applications.

Callback interface used to notify on auto focus start and stop.

This is only supported in continuous autofocus modes -- [android.hardware.Camera.Parameters#FOCUS_MODE_CONTINUOUS_VIDEO](../android/hardware/Camera.Parameters.md) and [android.hardware.Camera.Parameters#FOCUS_MODE_CONTINUOUS_PICTURE](../android/hardware/Camera.Parameters.md). Applications can show autofocus animation based on this.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAutoFocusMoving](../android/hardware/Camera.AutoFocusMoveCallback.md))`(`start:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `camera:` ` [Camera](../android/hardware/Camera.md)!`)` Called when the camera auto focus starts or stops. |

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
| `camera` | [Camera](../android/hardware/Camera.md)!:the Camera service object |
