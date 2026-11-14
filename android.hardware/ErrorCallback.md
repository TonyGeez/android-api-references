# Camera.ErrorCallback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ErrorCallback

Kotlin| [Java](../android/hardware/Camera.ErrorCallback.md) 
| --- | --- |

```
interface ErrorCallback
```

| [android.hardware.Camera.ErrorCallback](../android/hardware/Camera.ErrorCallback.md) |

| **This interface was deprecated in API level 21.**
|
| We recommend using the new [android.hardware.camera2](../android/hardware/camera2/_package.md) API for new applications.

Callback interface for camera error notification.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](../android/hardware/Camera.ErrorCallback.md))`(`error:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `camera:` ` [Camera](../android/hardware/Camera.md)!`)` Callback for camera errors. |

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
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):error code: - [CAMERA_ERROR_UNKNOWN](../android/hardware/Camera.md) - [CAMERA_ERROR_SERVER_DIED](../android/hardware/Camera.md) |
| `camera` | [Camera](../android/hardware/Camera.md)!:the Camera service object |
