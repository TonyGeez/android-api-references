# Camera.AutoFocusCallback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AutoFocusCallback

Kotlin| [Java](../android/hardware/Camera.AutoFocusCallback.md) 
| --- | --- |

```
interface AutoFocusCallback
```

| [android.hardware.Camera.AutoFocusCallback](../android/hardware/Camera.AutoFocusCallback.md) |

| **This interface was deprecated in API level 21.**
|
| We recommend using the new [android.hardware.camera2](../android.hardware.camera2/_package.md) API for new applications.

Callback interface used to notify on completion of camera auto focus.

Devices that do not support auto-focus will receive a "fake" callback to this interface. If your application needs auto-focus and should not be installed on devices*without* auto-focus, you must declare that your app uses the`android.hardware.camera.autofocus`feature, in the [\<uses-feature\>](https://developer.android.com/guide/topics/manifest/uses-feature-element.html) manifest element.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAutoFocus](../android/hardware/Camera.AutoFocusCallback.md))`(`success:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `camera:` ` [Camera](Camera.md)!`)` Called when the camera auto focus completes. |

## Public methods

### onAutoFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAutoFocus(
    success: Boolean, 
    camera: Camera!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the camera auto focus completes. If the camera does not support auto-focus and autoFocus is called, onAutoFocus will be called immediately with a fake value of`success`set to`true`. The auto-focus routine does not lock auto-exposure and auto-white balance after it completes.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------|
| `success` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if focus was successful, false if otherwise |
| `camera` | [Camera](Camera.md)!:the Camera service object |

**See Also**

- [android.hardware.Camera.Parameters#setAutoExposureLock(boolean)](../android/hardware/Camera.Parameters.md))
- [android.hardware.Camera.Parameters#setAutoWhiteBalanceLock(boolean)](../android/hardware/Camera.Parameters.md))
