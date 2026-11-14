# Camera.ErrorCallback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ErrorCallback

Kotlin| [Java](https://developer.android.com/reference/android/hardware/Camera.ErrorCallback "View this page in Java") 
| --- | --- |

```
interface ErrorCallback
```

| [android.hardware.Camera.ErrorCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.ErrorCallback#) |

| **This interface was deprecated in API level 21.**
|
| We recommend using the new [android.hardware.camera2](https://developer.android.com/reference/kotlin/android/hardware/camera2/package-summary) API for new applications.

Callback interface for camera error notification.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](https://developer.android.com/reference/kotlin/android/hardware/Camera.ErrorCallback#onError(kotlin.Int,%20android.hardware.Camera))`(`error:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `camera:` ` [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera)!`)` Callback for camera errors. |

## Public methods

### onError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onError(
    error: Int, 
    camera: Camera!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Callback for camera errors.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):error code: - [CAMERA_ERROR_UNKNOWN](https://developer.android.com/reference/kotlin/android/hardware/Camera#CAMERA_ERROR_UNKNOWN:kotlin.Int) - [CAMERA_ERROR_SERVER_DIED](https://developer.android.com/reference/kotlin/android/hardware/Camera#CAMERA_ERROR_SERVER_DIED:kotlin.Int) |
| `camera` | [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera)!:the Camera service object |
