# Camera.AutoFocusCallback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AutoFocusCallback

Kotlin| [Java](https://developer.android.com/reference/android/hardware/Camera.AutoFocusCallback "View this page in Java") 

```
interface AutoFocusCallback
```

| [android.hardware.Camera.AutoFocusCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.AutoFocusCallback#) |

| **This interface was deprecated in API level 21.**
|
| We recommend using the new [android.hardware.camera2](https://developer.android.com/reference/kotlin/android/hardware/camera2/package-summary) API for new applications.

Callback interface used to notify on completion of camera auto focus.

Devices that do not support auto-focus will receive a "fake" callback to this interface. If your application needs auto-focus and should not be installed on devices*without* auto-focus, you must declare that your app uses the`android.hardware.camera.autofocus`feature, in the [\<uses-feature\>](https://developer.android.com/guide/topics/manifest/uses-feature-element.html) manifest element.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAutoFocus](https://developer.android.com/reference/kotlin/android/hardware/Camera.AutoFocusCallback#onAutoFocus(kotlin.Boolean,%20android.hardware.Camera))`(`success:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `camera:` ` [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera)!`)` Called when the camera auto focus completes. |

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
| `camera` | [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera)!:the Camera service object |

**See Also**

- [android.hardware.Camera.Parameters#setAutoExposureLock(boolean)](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#setAutoExposureLock(kotlin.Boolean))
- [android.hardware.Camera.Parameters#setAutoWhiteBalanceLock(boolean)](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#setAutoWhiteBalanceLock(kotlin.Boolean))
