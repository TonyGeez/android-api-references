# Camera.PictureCallback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PictureCallback

Kotlin| [Java](../android/hardware/Camera.PictureCallback.md) 
| --- | --- |

```
interface PictureCallback
```

| [android.hardware.Camera.PictureCallback](../android/hardware/Camera.PictureCallback.md) |

| **This interface was deprecated in API level 21.**
|
| We recommend using the new [android.hardware.camera2](../android/hardware/camera2/_package.md) API for new applications.

Callback interface used to supply image data from a photo capture.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPictureTaken](../android/hardware/Camera.PictureCallback.md))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `camera:` ` [Camera](../android/hardware/Camera.md)!`)` Called when image data is available after a picture is taken. |

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

Called when image data is available after a picture is taken. The format of the data depends on the context of the callback and [Camera.Parameters](../android/hardware/Camera.Parameters.md) settings.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:a byte array of the picture data |
| `camera` | [Camera](../android/hardware/Camera.md)!:the Camera service object |
