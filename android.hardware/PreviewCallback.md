# Camera.PreviewCallback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PreviewCallback

Kotlin| [Java](https://developer.android.com/reference/android/hardware/Camera.PreviewCallback "View this page in Java") 
| --- | --- |

```
interface PreviewCallback
```

| [android.hardware.Camera.PreviewCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.PreviewCallback#) |

| **This interface was deprecated in API level 21.**
|
| We recommend using the new [android.hardware.camera2](https://developer.android.com/reference/kotlin/android/hardware/camera2/package-summary) API for new applications.

Callback interface used to deliver copies of preview frames as they are displayed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPreviewFrame](https://developer.android.com/reference/kotlin/android/hardware/Camera.PreviewCallback#onPreviewFrame(kotlin.ByteArray,%20android.hardware.Camera))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `camera:` ` [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera)!`)` Called as preview frames are displayed. |

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

Called as preview frames are displayed. This callback is invoked on the event thread [open(int)](https://developer.android.com/reference/kotlin/android/hardware/Camera#open(kotlin.Int))was called from.

If using the [android.graphics.ImageFormat#YV12](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YV12:kotlin.Int) format, refer to the equations in [Camera.Parameters.setPreviewFormat](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#setPreviewFormat(kotlin.Int))for the arrangement of the pixel data in the preview callback buffers.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the contents of the preview frame in the format defined by [android.graphics.ImageFormat](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#), which can be queried with [android.hardware.Camera.Parameters#getPreviewFormat()](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#getPreviewFormat()). If [android.hardware.Camera.Parameters#setPreviewFormat(int)](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#setPreviewFormat(kotlin.Int))is never called, the default will be the YCbCr_420_SP (NV21) format. |
| `camera` | [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera)!:the Camera service object. |
