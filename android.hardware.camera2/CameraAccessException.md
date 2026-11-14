# CameraAccessException

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CameraAccessException

Kotlin| [Java](https://developer.android.com/reference/android/hardware/camera2/CameraAccessException "View this page in Java") 
| --- | --- |

```
open class CameraAccessException : AndroidException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [android.util.AndroidException](https://developer.android.com/reference/kotlin/android/util/AndroidException.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.hardware.camera2.CameraAccessException](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#) |

`CameraAccessException`is thrown if a camera device could not be queried or opened by the [CameraManager](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager), or if the connection to an opened [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice) is no longer valid.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAMERA_DISABLED](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_DISABLED:kotlin.Int) The camera is disabled due to a device policy, and cannot be opened. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAMERA_DISCONNECTED](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_DISCONNECTED:kotlin.Int) The camera device is removable and has been disconnected from the Android device, or the camera id used with android. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAMERA_ERROR](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_ERROR:kotlin.Int) The camera device is currently in the error state. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAMERA_IN_USE](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_IN_USE:kotlin.Int) The camera device is in use already. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_CAMERAS_IN_USE](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#MAX_CAMERAS_IN_USE:kotlin.Int) The system-wide limit for number of open cameras or camera resources has been reached, and more camera devices cannot be opened or torch mode cannot be turned on until previous instances are closed. |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CameraAccessException](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CameraAccessException(kotlin.Int))`(`problem:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [CameraAccessException](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CameraAccessException(kotlin.Int,%20kotlin.String))`(`problem:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [CameraAccessException](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CameraAccessException(kotlin.Int,%20kotlin.String,%20kotlin.Throwable))`(`problem:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |
| [CameraAccessException](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CameraAccessException(kotlin.Int,%20kotlin.Throwable))`(`problem:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReason](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#getReason())`()` The reason for the failure to access the camera. |

## Constants

### CAMERA_DISABLED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAMERA_DISABLED: Int
```

The camera is disabled due to a device policy, and cannot be opened. 

 Value: 1

**See Also**

- [android.app.admin.DevicePolicyManager#setCameraDisabled(android.content.ComponentName, boolean)](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#setCameraDisabled(android.content.ComponentName,%20kotlin.Boolean)) 

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

The camera has failed to open or has failed at a later time as a result of some non-user interaction. Refer to [CameraDevice.StateCallback.onError](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.StateCallback#onError(android.hardware.camera2.CameraDevice,%20kotlin.Int))for the exact nature of the error.

No further calls to the camera will succeed. Clean up the camera with [CameraDevice.close](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice#close())and try handling the error in order to successfully re-open the camera. 

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
| `problem` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.hardware.camera2.CameraAccessException#CAMERA_IN_USE](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_IN_USE:kotlin.Int), [android.hardware.camera2.CameraAccessException#MAX_CAMERAS_IN_USE](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#MAX_CAMERAS_IN_USE:kotlin.Int), [android.hardware.camera2.CameraAccessException#CAMERA_DISABLED](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_DISABLED:kotlin.Int), [android.hardware.camera2.CameraAccessException#CAMERA_DISCONNECTED](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_DISCONNECTED:kotlin.Int), or [android.hardware.camera2.CameraAccessException#CAMERA_ERROR](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_ERROR:kotlin.Int) |

### CameraAccessException

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CameraAccessException(
    problem: Int, 
    message: String!)
```

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `problem` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.hardware.camera2.CameraAccessException#CAMERA_IN_USE](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_IN_USE:kotlin.Int), [android.hardware.camera2.CameraAccessException#MAX_CAMERAS_IN_USE](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#MAX_CAMERAS_IN_USE:kotlin.Int), [android.hardware.camera2.CameraAccessException#CAMERA_DISABLED](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_DISABLED:kotlin.Int), [android.hardware.camera2.CameraAccessException#CAMERA_DISCONNECTED](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_DISCONNECTED:kotlin.Int), or [android.hardware.camera2.CameraAccessException#CAMERA_ERROR](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_ERROR:kotlin.Int) |

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
| `problem` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.hardware.camera2.CameraAccessException#CAMERA_IN_USE](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_IN_USE:kotlin.Int), [android.hardware.camera2.CameraAccessException#MAX_CAMERAS_IN_USE](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#MAX_CAMERAS_IN_USE:kotlin.Int), [android.hardware.camera2.CameraAccessException#CAMERA_DISABLED](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_DISABLED:kotlin.Int), [android.hardware.camera2.CameraAccessException#CAMERA_DISCONNECTED](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_DISCONNECTED:kotlin.Int), or [android.hardware.camera2.CameraAccessException#CAMERA_ERROR](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_ERROR:kotlin.Int) |

### CameraAccessException

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CameraAccessException(
    problem: Int, 
    cause: Throwable!)
```

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `problem` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.hardware.camera2.CameraAccessException#CAMERA_IN_USE](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_IN_USE:kotlin.Int), [android.hardware.camera2.CameraAccessException#MAX_CAMERAS_IN_USE](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#MAX_CAMERAS_IN_USE:kotlin.Int), [android.hardware.camera2.CameraAccessException#CAMERA_DISABLED](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_DISABLED:kotlin.Int), [android.hardware.camera2.CameraAccessException#CAMERA_DISCONNECTED](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_DISCONNECTED:kotlin.Int), or [android.hardware.camera2.CameraAccessException#CAMERA_ERROR](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_ERROR:kotlin.Int) |

## Public methods

### getReason

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getReason(): Int
```

The reason for the failure to access the camera.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.hardware.camera2.CameraAccessException#CAMERA_IN_USE](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_IN_USE:kotlin.Int), [android.hardware.camera2.CameraAccessException#MAX_CAMERAS_IN_USE](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#MAX_CAMERAS_IN_USE:kotlin.Int), [android.hardware.camera2.CameraAccessException#CAMERA_DISABLED](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_DISABLED:kotlin.Int), [android.hardware.camera2.CameraAccessException#CAMERA_DISCONNECTED](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_DISCONNECTED:kotlin.Int), or [android.hardware.camera2.CameraAccessException#CAMERA_ERROR](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_ERROR:kotlin.Int) |

**See Also**

- [#CAMERA_DISABLED](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_DISABLED:kotlin.Int)
- [#CAMERA_DISCONNECTED](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_DISCONNECTED:kotlin.Int)
- [#CAMERA_ERROR](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException#CAMERA_ERROR:kotlin.Int)
