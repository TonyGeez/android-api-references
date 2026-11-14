# CameraAccessException

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CameraAccessException

Kotlin| [Java](../android/hardware/camera2/CameraAccessException.md) 
| --- | --- |

```
open class CameraAccessException : AndroidException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [android.util.AndroidException](../android/util/AndroidException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.hardware.camera2.CameraAccessException](../android/hardware/camera2/CameraAccessException.md) |

`CameraAccessException`is thrown if a camera device could not be queried or opened by the [CameraManager](../android/hardware/camera2/CameraManager.md), or if the connection to an opened [CameraDevice](../android/hardware/camera2/CameraDevice.md) is no longer valid.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAMERA_DISABLED](../android/hardware/camera2/CameraAccessException.md) The camera is disabled due to a device policy, and cannot be opened. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAMERA_DISCONNECTED](../android/hardware/camera2/CameraAccessException.md) The camera device is removable and has been disconnected from the Android device, or the camera id used with android. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAMERA_ERROR](../android/hardware/camera2/CameraAccessException.md) The camera device is currently in the error state. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAMERA_IN_USE](../android/hardware/camera2/CameraAccessException.md) The camera device is in use already. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_CAMERAS_IN_USE](../android/hardware/camera2/CameraAccessException.md) The system-wide limit for number of open cameras or camera resources has been reached, and more camera devices cannot be opened or torch mode cannot be turned on until previous instances are closed. |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CameraAccessException](../android/hardware/camera2/CameraAccessException.md))`(`problem:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [CameraAccessException](../android/hardware/camera2/CameraAccessException.md))`(`problem:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [CameraAccessException](../android/hardware/camera2/CameraAccessException.md))`(`problem:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |
| [CameraAccessException](../android/hardware/camera2/CameraAccessException.md))`(`problem:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReason](../android/hardware/camera2/CameraAccessException.md))`()` The reason for the failure to access the camera. |

## Constants

### CAMERA_DISABLED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAMERA_DISABLED: Int
```

The camera is disabled due to a device policy, and cannot be opened. 

 Value: 1

**See Also**

- [android.app.admin.DevicePolicyManager#setCameraDisabled(android.content.ComponentName, boolean)](../android/app/admin/DevicePolicyManager.md)) 

### CAMERA_DISCONNECTED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAMERA_DISCONNECTED: Int
```

The camera device is removable and has been disconnected from the Android device, or the camera id used with android.hardware.camera2.CameraManager#openCamera is no longer valid, or the camera service has shut down the connection due to a higher-priority access request for the camera device. 

 Value: 2

### CAMERA_ERROR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAMERA_ERROR: Int
```

The camera device is currently in the error state.

The camera has failed to open or has failed at a later time as a result of some non-user interaction. Refer to [CameraDevice.StateCallback.onError](../android/hardware/camera2/CameraDevice.StateCallback.md))for the exact nature of the error.

No further calls to the camera will succeed. Clean up the camera with [CameraDevice.close](../android/hardware/camera2/CameraDevice.md))and try handling the error in order to successfully re-open the camera. 

 Value: 3

### CAMERA_IN_USE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAMERA_IN_USE: Int
```

The camera device is in use already. 

 Value: 4

### MAX_CAMERAS_IN_USE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_CAMERAS_IN_USE: Int
```

The system-wide limit for number of open cameras or camera resources has been reached, and more camera devices cannot be opened or torch mode cannot be turned on until previous instances are closed. 

 Value: 5

## Public constructors

### CameraAccessException

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CameraAccessException(problem: Int)
```

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `problem` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.hardware.camera2.CameraAccessException#CAMERA_IN_USE](../android/hardware/camera2/CameraAccessException.md), [android.hardware.camera2.CameraAccessException#MAX_CAMERAS_IN_USE](../android/hardware/camera2/CameraAccessException.md), [android.hardware.camera2.CameraAccessException#CAMERA_DISABLED](../android/hardware/camera2/CameraAccessException.md), [android.hardware.camera2.CameraAccessException#CAMERA_DISCONNECTED](../android/hardware/camera2/CameraAccessException.md), or [android.hardware.camera2.CameraAccessException#CAMERA_ERROR](../android/hardware/camera2/CameraAccessException.md) |

### CameraAccessException

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CameraAccessException(
    problem: Int, 
    message: String!)
```

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `problem` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.hardware.camera2.CameraAccessException#CAMERA_IN_USE](../android/hardware/camera2/CameraAccessException.md), [android.hardware.camera2.CameraAccessException#MAX_CAMERAS_IN_USE](../android/hardware/camera2/CameraAccessException.md), [android.hardware.camera2.CameraAccessException#CAMERA_DISABLED](../android/hardware/camera2/CameraAccessException.md), [android.hardware.camera2.CameraAccessException#CAMERA_DISCONNECTED](../android/hardware/camera2/CameraAccessException.md), or [android.hardware.camera2.CameraAccessException#CAMERA_ERROR](../android/hardware/camera2/CameraAccessException.md) |

### CameraAccessException

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CameraAccessException(
    problem: Int, 
    message: String!, 
    cause: Throwable!)
```

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `problem` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.hardware.camera2.CameraAccessException#CAMERA_IN_USE](../android/hardware/camera2/CameraAccessException.md), [android.hardware.camera2.CameraAccessException#MAX_CAMERAS_IN_USE](../android/hardware/camera2/CameraAccessException.md), [android.hardware.camera2.CameraAccessException#CAMERA_DISABLED](../android/hardware/camera2/CameraAccessException.md), [android.hardware.camera2.CameraAccessException#CAMERA_DISCONNECTED](../android/hardware/camera2/CameraAccessException.md), or [android.hardware.camera2.CameraAccessException#CAMERA_ERROR](../android/hardware/camera2/CameraAccessException.md) |

### CameraAccessException

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CameraAccessException(
    problem: Int, 
    cause: Throwable!)
```

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `problem` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.hardware.camera2.CameraAccessException#CAMERA_IN_USE](../android/hardware/camera2/CameraAccessException.md), [android.hardware.camera2.CameraAccessException#MAX_CAMERAS_IN_USE](../android/hardware/camera2/CameraAccessException.md), [android.hardware.camera2.CameraAccessException#CAMERA_DISABLED](../android/hardware/camera2/CameraAccessException.md), [android.hardware.camera2.CameraAccessException#CAMERA_DISCONNECTED](../android/hardware/camera2/CameraAccessException.md), or [android.hardware.camera2.CameraAccessException#CAMERA_ERROR](../android/hardware/camera2/CameraAccessException.md) |

## Public methods

### getReason

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getReason(): Int
```

The reason for the failure to access the camera.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.hardware.camera2.CameraAccessException#CAMERA_IN_USE](../android/hardware/camera2/CameraAccessException.md), [android.hardware.camera2.CameraAccessException#MAX_CAMERAS_IN_USE](../android/hardware/camera2/CameraAccessException.md), [android.hardware.camera2.CameraAccessException#CAMERA_DISABLED](../android/hardware/camera2/CameraAccessException.md), [android.hardware.camera2.CameraAccessException#CAMERA_DISCONNECTED](../android/hardware/camera2/CameraAccessException.md), or [android.hardware.camera2.CameraAccessException#CAMERA_ERROR](../android/hardware/camera2/CameraAccessException.md) |

**See Also**

- [#CAMERA_DISABLED](../android/hardware/camera2/CameraAccessException.md)
- [#CAMERA_DISCONNECTED](../android/hardware/camera2/CameraAccessException.md)
- [#CAMERA_ERROR](../android/hardware/camera2/CameraAccessException.md)
