# Camera.FaceDetectionListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FaceDetectionListener

Kotlin| [Java](https://developer.android.com/reference/android/hardware/Camera.FaceDetectionListener "View this page in Java") 
| --- | --- |

```
interface FaceDetectionListener
```

| [android.hardware.Camera.FaceDetectionListener](https://developer.android.com/reference/kotlin/android/hardware/Camera.FaceDetectionListener#) |

| **This interface was deprecated in API level 21.**
|
| We recommend using the new [android.hardware.camera2](https://developer.android.com/reference/kotlin/android/hardware/camera2/package-summary) API for new applications.

Callback interface for face detected in the preview frame.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFaceDetection](https://developer.android.com/reference/kotlin/android/hardware/Camera.FaceDetectionListener#onFaceDetection(kotlin.Array,%20android.hardware.Camera))`(`faces:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Camera.Face](https://developer.android.com/reference/kotlin/android/hardware/Camera.Face)!>!`, `camera:` ` [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera)!`)` Notify the listener of the detected faces in the preview frame. |

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
| `faces` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Camera.Face](https://developer.android.com/reference/kotlin/android/hardware/Camera.Face)!\>!:The detected faces in a list |
| `camera` | [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera)!:The [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera) service object |
