# Camera.OnZoomChangeListener

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnZoomChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/hardware/Camera.OnZoomChangeListener "View this page in Java") 

```
interface OnZoomChangeListener
```

| [android.hardware.Camera.OnZoomChangeListener](https://developer.android.com/reference/kotlin/android/hardware/Camera.OnZoomChangeListener#) |

| **This interface was deprecated in API level 21.**
|
| We recommend using the new [android.hardware.camera2](https://developer.android.com/reference/kotlin/android/hardware/camera2/package-summary) API for new applications.

Callback interface for zoom changes during a smooth zoom operation.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onZoomChange](https://developer.android.com/reference/kotlin/android/hardware/Camera.OnZoomChangeListener#onZoomChange(kotlin.Int,%20kotlin.Boolean,%20android.hardware.Camera))`(`zoomValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `stopped:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `camera:` ` [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera)!`)` Called when the zoom value has changed during a smooth zoom. |

## Public methods

### onZoomChange

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onZoomChange(
    zoomValue: Int, 
    stopped: Boolean, 
    camera: Camera!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the zoom value has changed during a smooth zoom.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `zoomValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the current zoom value. In smooth zoom mode, camera calls this for every new zoom value. |
| `stopped` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether smooth zoom is stopped. If the value is true, this is the last zoom update for the application. |
| `camera` | [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera)!:the Camera service object |
