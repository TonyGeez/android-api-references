# Camera.FaceDetectionListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FaceDetectionListener

Kotlin| [Java](../android/hardware/Camera.FaceDetectionListener.md) 
| --- | --- |

```
interface FaceDetectionListener
```

| [android.hardware.Camera.FaceDetectionListener](../android/hardware/Camera.FaceDetectionListener.md) |

| **This interface was deprecated in API level 21.**
|
| We recommend using the new [android.hardware.camera2](../android.hardware.camera2/_package.md) API for new applications.

Callback interface for face detected in the preview frame.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFaceDetection](../android/hardware/Camera.FaceDetectionListener.md))`(`faces:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Camera.Face](../android/hardware/Camera.Face.md)!>!`, `camera:` ` [Camera](Camera.md)!`)` Notify the listener of the detected faces in the preview frame. |

## Public methods

### onFaceDetection

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFaceDetection(
    faces: Array<Camera.Face!>!, 
    camera: Camera!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Notify the listener of the detected faces in the preview frame.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `faces` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Camera.Face](../android/hardware/Camera.Face.md)!\>!:The detected faces in a list |
| `camera` | [Camera](Camera.md)!:The [Camera](Camera.md) service object |
