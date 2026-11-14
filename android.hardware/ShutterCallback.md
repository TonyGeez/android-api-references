# Camera.ShutterCallback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ShutterCallback

Kotlin| [Java](https://developer.android.com/reference/android/hardware/Camera.ShutterCallback "View this page in Java") 
| --- | --- |

```
interface ShutterCallback
```

| [android.hardware.Camera.ShutterCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.ShutterCallback#) |

| **This interface was deprecated in API level 21.**
|
| We recommend using the new [android.hardware.camera2](https://developer.android.com/reference/kotlin/android/hardware/camera2/package-summary) API for new applications.

Callback interface used to signal the moment of actual image capture.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onShutter](https://developer.android.com/reference/kotlin/android/hardware/Camera.ShutterCallback#onShutter())`()` Called as near as possible to the moment when a photo is captured from the sensor. |

## Public methods

### onShutter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onShutter(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called as near as possible to the moment when a photo is captured from the sensor. This is a good opportunity to play a shutter sound or give other feedback of camera operation. This may be some time after the photo was triggered, but some time before the actual data is available.
