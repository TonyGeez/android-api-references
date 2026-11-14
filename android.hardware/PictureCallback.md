# Camera.PictureCallback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PictureCallback

Kotlin| [Java](https://developer.android.com/reference/android/hardware/Camera.PictureCallback "View this page in Java") 
| --- | --- |

```
interface PictureCallback
```

| [android.hardware.Camera.PictureCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.PictureCallback#) |

| **This interface was deprecated in API level 21.**
|
| We recommend using the new [android.hardware.camera2](https://developer.android.com/reference/kotlin/android/hardware/camera2/package-summary) API for new applications.

Callback interface used to supply image data from a photo capture.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPictureTaken](https://developer.android.com/reference/kotlin/android/hardware/Camera.PictureCallback#onPictureTaken(kotlin.ByteArray,%20android.hardware.Camera))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `camera:` ` [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera)!`)` Called when image data is available after a picture is taken. |

## Public methods

### onPictureTaken

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPictureTaken(
    data: ByteArray!, 
    camera: Camera!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when image data is available after a picture is taken. The format of the data depends on the context of the callback and [Camera.Parameters](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters) settings.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:a byte array of the picture data |
| `camera` | [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera)!:the Camera service object |
