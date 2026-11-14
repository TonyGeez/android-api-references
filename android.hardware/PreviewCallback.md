# Camera.PreviewCallback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PreviewCallback

Kotlin| [Java](../android/hardware/Camera.PreviewCallback.md) 
| --- | --- |

```
interface PreviewCallback
```

| [android.hardware.Camera.PreviewCallback](../android/hardware/Camera.PreviewCallback.md) |

| **This interface was deprecated in API level 21.**
|
| We recommend using the new [android.hardware.camera2](../android/hardware/camera2/_package.md) API for new applications.

Callback interface used to deliver copies of preview frames as they are displayed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPreviewFrame](../android/hardware/Camera.PreviewCallback.md))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `camera:` ` [Camera](../android/hardware/Camera.md)!`)` Called as preview frames are displayed. |

## Public methods

### onPreviewFrame

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPreviewFrame(
    data: ByteArray!, 
    camera: Camera!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called as preview frames are displayed. This callback is invoked on the event thread [open(int)](../android/hardware/Camera.md))was called from.

If using the [android.graphics.ImageFormat#YV12](../android/graphics/ImageFormat.md) format, refer to the equations in [Camera.Parameters.setPreviewFormat](../android/hardware/Camera.Parameters.md))for the arrangement of the pixel data in the preview callback buffers.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the contents of the preview frame in the format defined by [android.graphics.ImageFormat](../android/graphics/ImageFormat.md), which can be queried with [android.hardware.Camera.Parameters#getPreviewFormat()](../android/hardware/Camera.Parameters.md)). If [android.hardware.Camera.Parameters#setPreviewFormat(int)](../android/hardware/Camera.Parameters.md))is never called, the default will be the YCbCr_420_SP (NV21) format. |
| `camera` | [Camera](../android/hardware/Camera.md)!:the Camera service object. |
