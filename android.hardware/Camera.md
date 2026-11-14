# Camera

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Camera

Kotlin| [Java](https://developer.android.com/reference/android/hardware/Camera "View this page in Java") 
| --- | --- |

```
open class Camera
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera#) |

| **This class was deprecated in API level 21.**
|
| We recommend using the new [android.hardware.camera2](https://developer.android.com/reference/kotlin/android/hardware/camera2/package-summary) API for new applications.

The Camera class is used to set image capture settings, start/stop preview, snap pictures, and retrieve frames for encoding for video. This class is a client for the Camera service, which manages the actual camera hardware.

To access the device camera, you must declare the [android.Manifest.permission#CAMERA](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String) permission in your Android Manifest. Also be sure to include the [\<uses-feature\>](https://developer.android.com/guide/topics/manifest/uses-feature-element.html) manifest element to declare camera features used by your application. For example, if you use the camera and auto-focus feature, your Manifest should include the following: 

```kotlin
<uses-permission android:name="android.permission.CAMERA" />
  <uses-feature android:name="android.hardware.camera" />
  <uses-feature android:name="android.hardware.camera.autofocus" />
```

To take pictures with this class, use the following steps:

1. Obtain an instance of Camera from [open(int)](https://developer.android.com/reference/kotlin/android/hardware/Camera#open(kotlin.Int)).
2. Get existing (default) settings with [getParameters()](https://developer.android.com/reference/kotlin/android/hardware/Camera#getParameters()).
3. If necessary, modify the returned [Camera.Parameters](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters) object and call [setParameters(android.hardware.Camera.Parameters)](https://developer.android.com/reference/kotlin/android/hardware/Camera#setParameters(android.hardware.Camera.Parameters)).
4. Call [setDisplayOrientation(int)](https://developer.android.com/reference/kotlin/android/hardware/Camera#setDisplayOrientation(kotlin.Int))to ensure correct orientation of preview.
5. **Important** : Pass a fully initialized [SurfaceHolder](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.html#) to [setPreviewDisplay(android.view.SurfaceHolder)](https://developer.android.com/reference/kotlin/android/hardware/Camera#setPreviewDisplay(android.view.SurfaceHolder)). Without a surface, the camera will be unable to start the preview.
6. **Important** : Call [startPreview()](https://developer.android.com/reference/kotlin/android/hardware/Camera#startPreview())to start updating the preview surface. Preview must be started before you can take a picture.
7. When you want, call [takePicture(android.hardware.Camera.ShutterCallback,android.hardware.Camera.PictureCallback,android.hardware.Camera.PictureCallback,android.hardware.Camera.PictureCallback)](https://developer.android.com/reference/kotlin/android/hardware/Camera#takePicture(android.hardware.Camera.ShutterCallback,%20android.hardware.Camera.PictureCallback,%20android.hardware.Camera.PictureCallback,%20android.hardware.Camera.PictureCallback))to capture a photo. Wait for the callbacks to provide the actual image data.
8. After taking a picture, preview display will have stopped. To take more photos, call [startPreview()](https://developer.android.com/reference/kotlin/android/hardware/Camera#startPreview())again first.
9. Call [stopPreview()](https://developer.android.com/reference/kotlin/android/hardware/Camera#stopPreview())to stop updating the preview surface.
10. **Important:** Call [release()](https://developer.android.com/reference/kotlin/android/hardware/Camera#release())to release the camera for use by other applications. Applications should release the camera immediately in [android.app.Activity#onPause()](https://developer.android.com/reference/kotlin/android/app/Activity.html#onPause())(and re- [open()](https://developer.android.com/reference/kotlin/android/hardware/Camera#open())it in [android.app.Activity#onResume()](https://developer.android.com/reference/kotlin/android/app/Activity.html#onResume())).

To quickly switch to video recording mode, use these steps:

1. Obtain and initialize a Camera and start preview as described above.
2. Call [unlock()](https://developer.android.com/reference/kotlin/android/hardware/Camera#unlock())to allow the media process to access the camera.
3. Pass the camera to [android.media.MediaRecorder#setCamera(Camera)](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.html#setCamera(android.hardware.Camera)). See [android.media.MediaRecorder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.html#) information about video recording.
4. When finished recording, call [reconnect()](https://developer.android.com/reference/kotlin/android/hardware/Camera#reconnect())to re-acquire and re-lock the camera.
5. If desired, restart preview and take more photos or videos.
6. Call [stopPreview()](https://developer.android.com/reference/kotlin/android/hardware/Camera#stopPreview())and [release()](https://developer.android.com/reference/kotlin/android/hardware/Camera#release())as described above.

This class is not thread-safe, and is meant for use from one event thread. Most long-running operations (preview, focus, photo capture, etc) happen asynchronously and invoke callbacks as necessary. Callbacks will be invoked on the event thread [open(int)](https://developer.android.com/reference/kotlin/android/hardware/Camera#open(kotlin.Int))was called from. This class's methods must never be called from multiple threads at once.

**Caution:**Different Android-powered devices may have different hardware specifications, such as megapixel ratings and auto-focus capabilities. In order for your application to be compatible with more devices, you should not make assumptions about the device camera specifications.
|
| ### Developer Guides
|
| For more information about using cameras, read the [Camera](https://developer.android.com/guide/topics/media/camera.html) developer guide.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Area](https://developer.android.com/reference/kotlin/android/hardware/Camera.Area) The Area class is used for choosing specific metering and focus areas for the camera to use when calculating auto-exposure, auto-white balance, and auto-focus. |
| abstract | [AutoFocusCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.AutoFocusCallback) Callback interface used to notify on completion of camera auto focus. |
| abstract | [AutoFocusMoveCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.AutoFocusMoveCallback) Callback interface used to notify on auto focus start and stop. |
| --- | --- |
| open | [CameraInfo](https://developer.android.com/reference/kotlin/android/hardware/Camera.CameraInfo) Information about a camera |
| abstract | [ErrorCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.ErrorCallback) Callback interface for camera error notification. |
| open | [Face](https://developer.android.com/reference/kotlin/android/hardware/Camera.Face) Information about a face identified through camera face detection. |
| --- | --- |
| abstract | [FaceDetectionListener](https://developer.android.com/reference/kotlin/android/hardware/Camera.FaceDetectionListener) Callback interface for face detected in the preview frame. |
| abstract | [OnZoomChangeListener](https://developer.android.com/reference/kotlin/android/hardware/Camera.OnZoomChangeListener) Callback interface for zoom changes during a smooth zoom operation. |
| open | [Parameters](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters) Camera service settings. |
| --- | --- |
| abstract | [PictureCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.PictureCallback) Callback interface used to supply image data from a photo capture. |
| abstract | [PreviewCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.PreviewCallback) Callback interface used to deliver copies of preview frames as they are displayed. |
| abstract | [ShutterCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.ShutterCallback) Callback interface used to signal the moment of actual image capture. |
| --- | --- |
| open | [Size](https://developer.android.com/reference/kotlin/android/hardware/Camera.Size) Image size (width and height dimensions). |

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_NEW_PICTURE](https://developer.android.com/reference/kotlin/android/hardware/Camera#ACTION_NEW_PICTURE:kotlin.String) Broadcast Action: A new picture is taken by the camera, and the entry of the picture has been added to the media store. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_NEW_VIDEO](https://developer.android.com/reference/kotlin/android/hardware/Camera#ACTION_NEW_VIDEO:kotlin.String) Broadcast Action: A new video is recorded by the camera, and the entry of the video has been added to the media store. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAMERA_ERROR_EVICTED](https://developer.android.com/reference/kotlin/android/hardware/Camera#CAMERA_ERROR_EVICTED:kotlin.Int) Camera was disconnected due to use by higher priority user. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAMERA_ERROR_SERVER_DIED](https://developer.android.com/reference/kotlin/android/hardware/Camera#CAMERA_ERROR_SERVER_DIED:kotlin.Int) Media server died. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAMERA_ERROR_UNKNOWN](https://developer.android.com/reference/kotlin/android/hardware/Camera#CAMERA_ERROR_UNKNOWN:kotlin.Int) Unspecified camera error. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addCallbackBuffer](https://developer.android.com/reference/kotlin/android/hardware/Camera#addCallbackBuffer(kotlin.ByteArray))`(`callbackBuffer:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Adds a pre-allocated buffer to the preview callback buffer queue. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [autoFocus](https://developer.android.com/reference/kotlin/android/hardware/Camera#autoFocus(android.hardware.Camera.AutoFocusCallback))`(`cb:` ` [Camera.AutoFocusCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.AutoFocusCallback)!`)` Starts camera auto-focus and registers a callback function to run when the camera is focused. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancelAutoFocus](https://developer.android.com/reference/kotlin/android/hardware/Camera#cancelAutoFocus())`()` Cancels any auto-focus function in progress. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [enableShutterSound](https://developer.android.com/reference/kotlin/android/hardware/Camera#enableShutterSound(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enable or disable the default shutter sound when taking a picture. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getCameraInfo](https://developer.android.com/reference/kotlin/android/hardware/Camera#getCameraInfo(kotlin.Int,%20android.hardware.Camera.CameraInfo))`(`cameraId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cameraInfo:` ` [Camera.CameraInfo](https://developer.android.com/reference/kotlin/android/hardware/Camera.CameraInfo)!`)` Returns the information about a particular camera. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNumberOfCameras](https://developer.android.com/reference/kotlin/android/hardware/Camera#getNumberOfCameras())`()` Returns the number of physical cameras available on this device. |
| --- | --- |
| open [Camera.Parameters](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters)! | [getParameters](https://developer.android.com/reference/kotlin/android/hardware/Camera#getParameters())`()` Returns the current settings for this Camera service. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [lock](https://developer.android.com/reference/kotlin/android/hardware/Camera#lock())`()` Re-locks the camera to prevent other processes from accessing it. |
| openstatic [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera#)! | [open](https://developer.android.com/reference/kotlin/android/hardware/Camera#open())`()` Creates a new Camera object to access the first back-facing camera on the device. |
| --- | --- |
| openstatic [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera#)! | [open](https://developer.android.com/reference/kotlin/android/hardware/Camera#open(kotlin.Int))`(`cameraId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new Camera object to access a particular hardware camera. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reconnect](https://developer.android.com/reference/kotlin/android/hardware/Camera#reconnect())`()` Reconnects to the camera service after another process used it. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](https://developer.android.com/reference/kotlin/android/hardware/Camera#release())`()` Disconnects and releases the Camera object resources. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutoFocusMoveCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera#setAutoFocusMoveCallback(android.hardware.Camera.AutoFocusMoveCallback))`(`cb:` ` [Camera.AutoFocusMoveCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.AutoFocusMoveCallback)!`)` Sets camera auto-focus move callback. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDisplayOrientation](https://developer.android.com/reference/kotlin/android/hardware/Camera#setDisplayOrientation(kotlin.Int))`(`degrees:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the clockwise rotation of preview display in degrees. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setErrorCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera#setErrorCallback(android.hardware.Camera.ErrorCallback))`(`cb:` ` [Camera.ErrorCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.ErrorCallback)!`)` Registers a callback to be invoked when an error occurs. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFaceDetectionListener](https://developer.android.com/reference/kotlin/android/hardware/Camera#setFaceDetectionListener(android.hardware.Camera.FaceDetectionListener))`(`listener:` ` [Camera.FaceDetectionListener](https://developer.android.com/reference/kotlin/android/hardware/Camera.FaceDetectionListener)!`)` Registers a listener to be notified about the faces detected in the preview frame. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOneShotPreviewCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera#setOneShotPreviewCallback(android.hardware.Camera.PreviewCallback))`(`cb:` ` [Camera.PreviewCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.PreviewCallback)!`)` Installs a callback to be invoked for the next preview frame in addition to displaying it on the screen. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setParameters](https://developer.android.com/reference/kotlin/android/hardware/Camera#setParameters(android.hardware.Camera.Parameters))`(`params:` ` [Camera.Parameters](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters)!`)` Changes the settings for this Camera service. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreviewCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera#setPreviewCallback(android.hardware.Camera.PreviewCallback))`(`cb:` ` [Camera.PreviewCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.PreviewCallback)!`)` Installs a callback to be invoked for every preview frame in addition to displaying them on the screen. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreviewCallbackWithBuffer](https://developer.android.com/reference/kotlin/android/hardware/Camera#setPreviewCallbackWithBuffer(android.hardware.Camera.PreviewCallback))`(`cb:` ` [Camera.PreviewCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.PreviewCallback)!`)` Installs a callback to be invoked for every preview frame, using buffers supplied with[addCallbackBuffer(byte[])](https://developer.android.com/reference/kotlin/android/hardware/Camera#addCallbackBuffer(kotlin.ByteArray)), in addition to displaying them on the screen. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreviewDisplay](https://developer.android.com/reference/kotlin/android/hardware/Camera#setPreviewDisplay(android.view.SurfaceHolder))`(`holder:` ` [SurfaceHolder](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.html#)!`)` Sets the [Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#) to be used for live preview. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreviewTexture](https://developer.android.com/reference/kotlin/android/hardware/Camera#setPreviewTexture(android.graphics.SurfaceTexture))`(`surfaceTexture:` ` [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#)!`)` Sets the [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#) to be used for live preview. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setZoomChangeListener](https://developer.android.com/reference/kotlin/android/hardware/Camera#setZoomChangeListener(android.hardware.Camera.OnZoomChangeListener))`(`listener:` ` [Camera.OnZoomChangeListener](https://developer.android.com/reference/kotlin/android/hardware/Camera.OnZoomChangeListener)!`)` Registers a listener to be notified when the zoom value is updated by the camera driver during smooth zoom. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startFaceDetection](https://developer.android.com/reference/kotlin/android/hardware/Camera#startFaceDetection())`()` Starts the face detection. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startPreview](https://developer.android.com/reference/kotlin/android/hardware/Camera#startPreview())`()` Starts capturing and drawing preview frames to the screen. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startSmoothZoom](https://developer.android.com/reference/kotlin/android/hardware/Camera#startSmoothZoom(kotlin.Int))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Zooms to the requested value smoothly. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopFaceDetection](https://developer.android.com/reference/kotlin/android/hardware/Camera#stopFaceDetection())`()` Stops the face detection. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopPreview](https://developer.android.com/reference/kotlin/android/hardware/Camera#stopPreview())`()` Stops capturing and drawing preview frames to the surface, and resets the camera for a future call to [startPreview()](https://developer.android.com/reference/kotlin/android/hardware/Camera#startPreview()). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopSmoothZoom](https://developer.android.com/reference/kotlin/android/hardware/Camera#stopSmoothZoom())`()` Stops the smooth zoom. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [takePicture](https://developer.android.com/reference/kotlin/android/hardware/Camera#takePicture(android.hardware.Camera.ShutterCallback,%20android.hardware.Camera.PictureCallback,%20android.hardware.Camera.PictureCallback))`(`shutter:` ` [Camera.ShutterCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.ShutterCallback)!`, `raw:` ` [Camera.PictureCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.PictureCallback)!`, `jpeg:` ` [Camera.PictureCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.PictureCallback)!`)` Equivalent to ```kotlin takePicture(Shutter, raw, null, jpeg) ``` . <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [takePicture](https://developer.android.com/reference/kotlin/android/hardware/Camera#takePicture(android.hardware.Camera.ShutterCallback,%20android.hardware.Camera.PictureCallback,%20android.hardware.Camera.PictureCallback,%20android.hardware.Camera.PictureCallback))`(`shutter:` ` [Camera.ShutterCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.ShutterCallback)!`, `raw:` ` [Camera.PictureCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.PictureCallback)!`, `postview:` ` [Camera.PictureCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.PictureCallback)!`, `jpeg:` ` [Camera.PictureCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.PictureCallback)!`)` Triggers an asynchronous image capture. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unlock](https://developer.android.com/reference/kotlin/android/hardware/Camera#unlock())`()` Unlocks the camera to allow another process to access it. |

| Protected methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/hardware/Camera#finalize())`()` <br /> |

## Constants

### ACTION_NEW_PICTURE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_NEW_PICTURE: String
```

**Deprecated:** *Deprecated in Java.*

Broadcast Action: A new picture is taken by the camera, and the entry of the picture has been added to the media store. [android.content.Intent#getData](https://developer.android.com/reference/kotlin/android/content/Intent.html#getData())is URI of the picture.

In [Android N](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int) this broadcast was removed, and applications are recommended to use [JobInfo.Builder](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder.html#). [android.app.job.JobInfo.Builder#addTriggerContentUri](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder.html#addTriggerContentUri(android.app.job.JobInfo.TriggerContentUri))instead.

In [Android O](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int) this broadcast has been brought back, but only for*registered*receivers. Apps that are actively running can again listen to the broadcast if they want an immediate clear signal about a picture being taken, however anything doing heavy work (or needing to be launched) as a result of this should still use JobScheduler. 

 Value: "android.hardware.action.NEW_PICTURE"

### ACTION_NEW_VIDEO

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_NEW_VIDEO: String
```

**Deprecated:** *Deprecated in Java.*

Broadcast Action: A new video is recorded by the camera, and the entry of the video has been added to the media store. [android.content.Intent#getData](https://developer.android.com/reference/kotlin/android/content/Intent.html#getData())is URI of the video.

In [Android N](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int) this broadcast was removed, and applications are recommended to use [JobInfo.Builder](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder.html#). [android.app.job.JobInfo.Builder#addTriggerContentUri](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder.html#addTriggerContentUri(android.app.job.JobInfo.TriggerContentUri))instead.

In [Android O](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int) this broadcast has been brought back, but only for*registered*receivers. Apps that are actively running can again listen to the broadcast if they want an immediate clear signal about a video being taken, however anything doing heavy work (or needing to be launched) as a result of this should still use JobScheduler. 

 Value: "android.hardware.action.NEW_VIDEO"

### CAMERA_ERROR_EVICTED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAMERA_ERROR_EVICTED: Int
```

**Deprecated:** *Deprecated in Java.*

Camera was disconnected due to use by higher priority user. 

 Value: 2

**See Also**

- [android.hardware.Camera.ErrorCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.ErrorCallback) 

### CAMERA_ERROR_SERVER_DIED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAMERA_ERROR_SERVER_DIED: Int
```

**Deprecated:** *Deprecated in Java.*

Media server died. In this case, the application must release the Camera object and instantiate a new one. 

 Value: 100

**See Also**

- [android.hardware.Camera.ErrorCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.ErrorCallback) 

### CAMERA_ERROR_UNKNOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAMERA_ERROR_UNKNOWN: Int
```

**Deprecated:** *Deprecated in Java.*

Unspecified camera error. 

 Value: 1

**See Also**

- [android.hardware.Camera.ErrorCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.ErrorCallback)

## Public methods

### addCallbackBuffer

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addCallbackBuffer(callbackBuffer: ByteArray!): Unit
```

**Deprecated:** *Deprecated in Java.*

Adds a pre-allocated buffer to the preview callback buffer queue. Applications can add one or more buffers to the queue. When a preview frame arrives and there is still at least one available buffer, the buffer will be used and removed from the queue. Then preview callback is invoked with the buffer. If a frame arrives and there is no buffer left, the frame is discarded. Applications should add buffers back when they finish processing the data in them.

For formats besides YV12, the size of the buffer is determined by multiplying the preview image width, height, and bytes per pixel. The width and height can be read from [Camera.Parameters.getPreviewSize()](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#getPreviewSize()). Bytes per pixel can be computed from [android.graphics.ImageFormat#getBitsPerPixel(int)](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#getBitsPerPixel(kotlin.Int))/ 8, using the image format from [Camera.Parameters.getPreviewFormat()](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#getPreviewFormat()).

If using the [android.graphics.ImageFormat#YV12](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YV12:kotlin.Int) format, the size can be calculated using the equations listed in [Camera.Parameters.setPreviewFormat](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#setPreviewFormat(kotlin.Int)).

This method is only necessary when [setPreviewCallbackWithBuffer(android.hardware.Camera.PreviewCallback)](https://developer.android.com/reference/kotlin/android/hardware/Camera#setPreviewCallbackWithBuffer(android.hardware.Camera.PreviewCallback))is used. When [setPreviewCallback(android.hardware.Camera.PreviewCallback)](https://developer.android.com/reference/kotlin/android/hardware/Camera#setPreviewCallback(android.hardware.Camera.PreviewCallback))or [setOneShotPreviewCallback(android.hardware.Camera.PreviewCallback)](https://developer.android.com/reference/kotlin/android/hardware/Camera#setOneShotPreviewCallback(android.hardware.Camera.PreviewCallback))are used, buffers are automatically allocated. When a supplied buffer is too small to hold the preview frame data, preview callback will return null and the buffer will be removed from the buffer queue.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callbackBuffer` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer to add to the queue. The size of the buffer must match the values described above. |

**See Also**

- [#setPreviewCallbackWithBuffer(PreviewCallback)](https://developer.android.com/reference/kotlin/android/hardware/Camera#setPreviewCallbackWithBuffer(android.hardware.Camera.PreviewCallback)) 

### autoFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun autoFocus(cb: Camera.AutoFocusCallback!): Unit
```

**Deprecated:** *Deprecated in Java.*

Starts camera auto-focus and registers a callback function to run when the camera is focused. This method is only valid when preview is active (between [startPreview()](https://developer.android.com/reference/kotlin/android/hardware/Camera#startPreview())and before [stopPreview()](https://developer.android.com/reference/kotlin/android/hardware/Camera#stopPreview())).

Callers should check [android.hardware.Camera.Parameters#getFocusMode()](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#getFocusMode())to determine if this method should be called. If the camera does not support auto-focus, it is a no-op and [AutoFocusCallback.onAutoFocus(boolean, Camera)](https://developer.android.com/reference/kotlin/android/hardware/Camera.AutoFocusCallback#onAutoFocus(kotlin.Boolean,%20android.hardware.Camera))callback will be called immediately.

If your application should not be installed on devices without auto-focus, you must declare that your application uses auto-focus with the [\<uses-feature\>](https://developer.android.com/guide/topics/manifest/uses-feature-element.html) manifest element.

If the current flash mode is not [android.hardware.Camera.Parameters#FLASH_MODE_OFF](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#FLASH_MODE_OFF:kotlin.String), flash may be fired during auto-focus, depending on the driver and camera hardware.

<br />

Auto-exposure lock [android.hardware.Camera.Parameters#getAutoExposureLock()](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#getAutoExposureLock())and auto-white balance locks [android.hardware.Camera.Parameters#getAutoWhiteBalanceLock()](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#getAutoWhiteBalanceLock())do not change during and after autofocus. But auto-focus routine may stop auto-exposure and auto-white balance transiently during focusing.

Stopping preview with [stopPreview()](https://developer.android.com/reference/kotlin/android/hardware/Camera#stopPreview()), or triggering still image capture with [takePicture(android.hardware.Camera.ShutterCallback,android.hardware.Camera.PictureCallback,android.hardware.Camera.PictureCallback)](https://developer.android.com/reference/kotlin/android/hardware/Camera#takePicture(android.hardware.Camera.ShutterCallback,%20android.hardware.Camera.PictureCallback,%20android.hardware.Camera.PictureCallback)), will not change the the focus position. Applications must call cancelAutoFocus to reset the focus.

If autofocus is successful, consider using [android.media.MediaActionSound](https://developer.android.com/reference/kotlin/android/media/MediaActionSound.html#) to properly play back an autofocus success sound to the user.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `cb` | [Camera.AutoFocusCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.AutoFocusCallback)!:the callback to run |

| Exceptions ||
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.RuntimeException` | if starting autofocus fails; usually this would be because of a hardware or other low-level error, or because release() has been called on this Camera instance. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/hardware/Camera#cancelAutoFocus()>
- [android.hardware.Camera.Parameters#setAutoExposureLock(boolean)](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#setAutoExposureLock(kotlin.Boolean))
- [android.hardware.Camera.Parameters#setAutoWhiteBalanceLock(boolean)](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#setAutoWhiteBalanceLock(kotlin.Boolean))
- [android.media.MediaActionSound](https://developer.android.com/reference/kotlin/android/media/MediaActionSound.html#) 

### cancelAutoFocus

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun cancelAutoFocus(): Unit
```

**Deprecated:** *Deprecated in Java.*

Cancels any auto-focus function in progress. Whether or not auto-focus is currently in progress, this function will return the focus position to the default. If the camera does not support auto-focus, this is a no-op.

| Exceptions ||
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.RuntimeException` | if canceling autofocus fails; usually this would be because of a hardware or other low-level error, or because release() has been called on this Camera instance. |

**See Also**

- [#autoFocus(Camera.AutoFocusCallback)](https://developer.android.com/reference/kotlin/android/hardware/Camera#autoFocus(android.hardware.Camera.AutoFocusCallback)) 

### enableShutterSound

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun enableShutterSound(enabled: Boolean): Boolean
```

**Deprecated:** *Deprecated in Java.*

Enable or disable the default shutter sound when taking a picture.

By default, the camera plays the system-defined camera shutter sound when #takePicture is called. Using this method, the shutter sound can be disabled. It is strongly recommended that an alternative shutter sound is played in the [ShutterCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.ShutterCallback) when the system shutter sound is disabled.

Note that devices may not always allow disabling the camera shutter sound. If the shutter sound state cannot be set to the desired value, this method will return false. [CameraInfo.canDisableShutterSound](https://developer.android.com/reference/kotlin/android/hardware/Camera.CameraInfo#canDisableShutterSound:kotlin.Boolean) can be used to determine whether the device will allow the shutter sound to be disabled.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the camera should play the system shutter sound when #takePicture is called. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the shutter sound state was successfully changed.`false`if the shutter sound state could not be changed.`true`is also returned if shutter sound playback is already set to the requested state. |

| Exceptions ||
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.RuntimeException` | if the call fails; usually this would be because of a hardware or other low-level error, or because release() has been called on this Camera instance. |

**See Also**

- [android.hardware.Camera.CameraInfo#canDisableShutterSound](https://developer.android.com/reference/kotlin/android/hardware/Camera.CameraInfo#canDisableShutterSound:kotlin.Boolean)
- [android.hardware.Camera.ShutterCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.ShutterCallback) 

### getCameraInfo

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getCameraInfo(
    cameraId: Int, 
    cameraInfo: Camera.CameraInfo!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Returns the information about a particular camera. If [getNumberOfCameras()](https://developer.android.com/reference/kotlin/android/hardware/Camera#getNumberOfCameras())returns N, the valid id is 0 to N-1.

| Exceptions ||
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.RuntimeException` | if an invalid ID is provided, or if there is an error retrieving the information (generally due to a hardware or other low-level failure). |

### getNumberOfCameras

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getNumberOfCameras(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the number of physical cameras available on this device. The return value of this method might change dynamically if the device supports external cameras and an external camera is connected or disconnected. If there is a [logical multi-camera](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata#REQUEST_AVAILABLE_CAPABILITIES_LOGICAL_MULTI_CAMERA:kotlin.Int) in the system, to maintain app backward compatibility, this method will only expose one camera per facing for all logical camera and physical camera groups. Use camera2 API to see all cameras.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | total number of accessible camera devices, or 0 if there are no cameras or an error was encountered enumerating them. |

### getParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParameters(): Camera.Parameters!
```

**Deprecated:** *Deprecated in Java.*

Returns the current settings for this Camera service. If modifications are made to the returned Parameters, they must be passed to [setParameters(android.hardware.Camera.Parameters)](https://developer.android.com/reference/kotlin/android/hardware/Camera#setParameters(android.hardware.Camera.Parameters))to take effect.

| Exceptions ||
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.RuntimeException` | if reading parameters fails; usually this would be because of a hardware or other low-level error, or because release() has been called on this Camera instance. |

**See Also**

- [#setParameters(Camera.Parameters)](https://developer.android.com/reference/kotlin/android/hardware/Camera#setParameters(android.hardware.Camera.Parameters)) 

### lock

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun lock(): Unit
```

**Deprecated:** *Deprecated in Java.*

Re-locks the camera to prevent other processes from accessing it. Camera objects are locked by default unless [unlock()](https://developer.android.com/reference/kotlin/android/hardware/Camera#unlock())is called. Normally [reconnect()](https://developer.android.com/reference/kotlin/android/hardware/Camera#reconnect())is used instead.

Since API level 14, camera is automatically locked for applications in [android.media.MediaRecorder#start()](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.html#start()). Applications can use the camera (ex: zoom) after recording starts. There is no need to call this after recording starts or stops.

If you are not recording video, you probably do not need this method.

| Exceptions ||
|------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.RuntimeException` | if the camera cannot be re-locked (for example, if the camera is still in use by another process). |

### open

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun open(): Camera!
```

**Deprecated:** *Deprecated in Java.*

Creates a new Camera object to access the first back-facing camera on the device. If the device does not have a back-facing camera, this returns null. Otherwise acts like the [open(int)](https://developer.android.com/reference/kotlin/android/hardware/Camera#open(kotlin.Int))call.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera#)! | a new Camera object for the first back-facing camera, or null if there is no backfacing camera |

**See Also**

- [#open(int)](https://developer.android.com/reference/kotlin/android/hardware/Camera#open(kotlin.Int)) 

### open

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun open(cameraId: Int): Camera!
```

**Deprecated:** *Deprecated in Java.*

Creates a new Camera object to access a particular hardware camera. If the same camera is opened by other applications, this will throw a RuntimeException.

You must call [release()](https://developer.android.com/reference/kotlin/android/hardware/Camera#release())when you are done using the camera, otherwise it will remain locked and be unavailable to other applications.

Your application should only have one Camera object active at a time for a particular hardware camera.

Callbacks from other methods are delivered to the event loop of the thread which called open(). If this thread has no event loop, then callbacks are delivered to the main application event loop. If there is no main application event loop, callbacks are not delivered.

**Caution:** On some devices, this method may take a long time to complete. It is best to call this method from a worker thread (possibly using [android.os.AsyncTask](https://developer.android.com/reference/kotlin/android/os/AsyncTask.html#)) to avoid blocking the main application UI thread.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cameraId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the hardware camera to access, between 0 and [getNumberOfCameras()](https://developer.android.com/reference/kotlin/android/hardware/Camera#getNumberOfCameras())-1. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera#)! | a new Camera object, connected, locked and ready for use. |

| Exceptions ||
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.RuntimeException` | if opening the camera fails (for example, if the camera is in use by another process or device policy manager has disabled the camera). |

**See Also**

- [android.app.admin.DevicePolicyManager#getCameraDisabled(android.content.ComponentName)](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#getCameraDisabled(android.content.ComponentName)) 

### reconnect

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun reconnect(): Unit
```

**Deprecated:** *Deprecated in Java.*

Reconnects to the camera service after another process used it. After [unlock()](https://developer.android.com/reference/kotlin/android/hardware/Camera#unlock())is called, another process may use the camera; when the process is done, you must reconnect to the camera, which will re-acquire the lock and allow you to continue using the camera.

Since API level 14, camera is automatically locked for applications in [android.media.MediaRecorder#start()](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.html#start()). Applications can use the camera (ex: zoom) after recording starts. There is no need to call this after recording starts or stops.

If you are not recording video, you probably do not need this method.

| Exceptions ||
|------------------------------|-----------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if a connection cannot be re-established (for example, if the camera is still in use by another process). |
| `java.lang.RuntimeException` | if release() has been called on this Camera instance. |

### release

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun release(): Unit
```

**Deprecated:** *Deprecated in Java.*

Disconnects and releases the Camera object resources.

You must call this as soon as you're done with the Camera object. 

### setAutoFocusMoveCallback

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAutoFocusMoveCallback(cb: Camera.AutoFocusMoveCallback!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets camera auto-focus move callback.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `cb` | [Camera.AutoFocusMoveCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.AutoFocusMoveCallback)!:the callback to run |

| Exceptions ||
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.RuntimeException` | if enabling the focus move callback fails; usually this would be because of a hardware or other low-level error, or because release() has been called on this Camera instance. |

### setDisplayOrientation

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDisplayOrientation(degrees: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the clockwise rotation of preview display in degrees. This affects the preview frames and the picture displayed after snapshot. This method is useful for portrait mode applications. Note that preview display of front-facing cameras is flipped horizontally before the rotation, that is, the image is reflected along the central vertical axis of the camera sensor. So the users can see themselves as looking into a mirror.

This does not affect the order of byte array passed in [android.hardware.Camera.PreviewCallback#onPreviewFrame](https://developer.android.com/reference/kotlin/android/hardware/Camera.PreviewCallback#onPreviewFrame(kotlin.ByteArray,%20android.hardware.Camera)), JPEG pictures, or recorded videos. This method is not allowed to be called during preview.

If you want to make the camera image show in the same orientation as the display, you can use the following code. 

```kotlin
public static void setCameraDisplayOrientation(Activity activity,
          int cameraId, android.hardware.Camera camera) {
      android.hardware.Camera.CameraInfo info =
              new android.hardware.Camera.CameraInfo();
      android.hardware.Camera.getCameraInfo(cameraId, info);
      int rotation = activity.getWindowManager().getDefaultDisplay()
              .getRotation();
      int degrees = 0;
      switch (rotation) {
          case Surface.ROTATION_0: degrees = 0; break;
          case Surface.ROTATION_90: degrees = 90; break;
          case Surface.ROTATION_180: degrees = 180; break;
          case Surface.ROTATION_270: degrees = 270; break;
      }
 
      int result;
      if (info.facing == Camera.CameraInfo.CAMERA_FACING_FRONT) {
          result = (info.orientation + degrees) % 360;
          result = (360 - result) % 360;  // compensate the mirror
      } else {  // back-facing
          result = (info.orientation - degrees + 360) % 360;
      }
      camera.setDisplayOrientation(result);
  }
  
```

Starting from API level 14, this method can be called when preview is active.

**Note:**Before API level 24, the default value for orientation is 0. Starting in API level 24, the default orientation will be such that applications in forced-landscape mode will have correct preview orientation, which may be either a default of 0 or 180. Applications that operate in portrait mode or allow for changing orientation must still call this method after each orientation change to ensure correct preview display in all cases.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `degrees` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the angle that the picture will be rotated clockwise. Valid values are 0, 90, 180, and 270. |

| Exceptions ||
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.RuntimeException` | if setting orientation fails; usually this would be because of a hardware or other low-level error, or because release() has been called on this Camera instance. |

**See Also**

- [#setPreviewDisplay(SurfaceHolder)](https://developer.android.com/reference/kotlin/android/hardware/Camera#setPreviewDisplay(android.view.SurfaceHolder)) 

### setErrorCallback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setErrorCallback(cb: Camera.ErrorCallback!): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers a callback to be invoked when an error occurs.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------|
| `cb` | [Camera.ErrorCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.ErrorCallback)!:The callback to run |

### setFaceDetectionListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setFaceDetectionListener(listener: Camera.FaceDetectionListener!): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers a listener to be notified about the faces detected in the preview frame.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [Camera.FaceDetectionListener](https://developer.android.com/reference/kotlin/android/hardware/Camera.FaceDetectionListener)!:the listener to notify |

**See Also**

- <https://developer.android.com/reference/kotlin/android/hardware/Camera#startFaceDetection()> 

### setOneShotPreviewCallback

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOneShotPreviewCallback(cb: Camera.PreviewCallback!): Unit
```

**Deprecated:** *Deprecated in Java.*

Installs a callback to be invoked for the next preview frame in addition to displaying it on the screen. After one invocation, the callback is cleared. This method can be called any time, even when preview is live. Any other preview callbacks are overridden.

If you are using the preview data to create video or still images, strongly consider using [android.media.MediaActionSound](https://developer.android.com/reference/kotlin/android/media/MediaActionSound.html#) to properly indicate image capture or recording start/stop to the user.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cb` | [Camera.PreviewCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.PreviewCallback)!:a callback object that receives a copy of the next preview frame, or null to stop receiving callbacks. |

| Exceptions ||
|------------------------------|-------------------------------------------------------|
| `java.lang.RuntimeException` | if release() has been called on this Camera instance. |

**See Also**

- [android.media.MediaActionSound](https://developer.android.com/reference/kotlin/android/media/MediaActionSound.html#) 

### setParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setParameters(params: Camera.Parameters!): Unit
```

**Deprecated:** *Deprecated in Java.*

Changes the settings for this Camera service.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [Camera.Parameters](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters)!:the Parameters to use for this Camera service |

| Exceptions ||
|------------------------------|-----------------------------------------------|
| `java.lang.RuntimeException` | if any parameter is invalid or not supported. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/hardware/Camera#getParameters()> 

### setPreviewCallback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPreviewCallback(cb: Camera.PreviewCallback!): Unit
```

**Deprecated:** *Deprecated in Java.*

Installs a callback to be invoked for every preview frame in addition to displaying them on the screen. The callback will be repeatedly called for as long as preview is active. This method can be called at any time, even while preview is live. Any other preview callbacks are overridden.

If you are using the preview data to create video or still images, strongly consider using [android.media.MediaActionSound](https://developer.android.com/reference/kotlin/android/media/MediaActionSound.html#) to properly indicate image capture or recording start/stop to the user.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cb` | [Camera.PreviewCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.PreviewCallback)!:a callback object that receives a copy of each preview frame, or null to stop receiving callbacks. |

| Exceptions ||
|------------------------------|-------------------------------------------------------|
| `java.lang.RuntimeException` | if release() has been called on this Camera instance. |

**See Also**

- [android.media.MediaActionSound](https://developer.android.com/reference/kotlin/android/media/MediaActionSound.html#) 

### setPreviewCallbackWithBuffer

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPreviewCallbackWithBuffer(cb: Camera.PreviewCallback!): Unit
```

**Deprecated:** *Deprecated in Java.*

Installs a callback to be invoked for every preview frame, using buffers supplied with[addCallbackBuffer(byte[])](https://developer.android.com/reference/kotlin/android/hardware/Camera#addCallbackBuffer(kotlin.ByteArray)), in addition to displaying them on the screen. The callback will be repeatedly called for as long as preview is active and buffers are available. Any other preview callbacks are overridden.

The purpose of this method is to improve preview efficiency and frame rate by allowing preview frame memory reuse. You must call[addCallbackBuffer(byte[])](https://developer.android.com/reference/kotlin/android/hardware/Camera#addCallbackBuffer(kotlin.ByteArray))at some point -- before or after calling this method -- or no callbacks will received.

The buffer queue will be cleared if this method is called with a null callback, [setPreviewCallback(android.hardware.Camera.PreviewCallback)](https://developer.android.com/reference/kotlin/android/hardware/Camera#setPreviewCallback(android.hardware.Camera.PreviewCallback))is called, or [setOneShotPreviewCallback(android.hardware.Camera.PreviewCallback)](https://developer.android.com/reference/kotlin/android/hardware/Camera#setOneShotPreviewCallback(android.hardware.Camera.PreviewCallback))is called.

If you are using the preview data to create video or still images, strongly consider using [android.media.MediaActionSound](https://developer.android.com/reference/kotlin/android/media/MediaActionSound.html#) to properly indicate image capture or recording start/stop to the user.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cb` | [Camera.PreviewCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.PreviewCallback)!:a callback object that receives a copy of the preview frame, or null to stop receiving callbacks and clear the buffer queue. |

| Exceptions ||
|------------------------------|-------------------------------------------------------|
| `java.lang.RuntimeException` | if release() has been called on this Camera instance. |

**See Also**

- [#addCallbackBuffer(byte[])](https://developer.android.com/reference/kotlin/android/hardware/Camera#addCallbackBuffer(kotlin.ByteArray))
- [android.media.MediaActionSound](https://developer.android.com/reference/kotlin/android/media/MediaActionSound.html#) 

### setPreviewDisplay

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPreviewDisplay(holder: SurfaceHolder!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the [Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#) to be used for live preview. Either a surface or surface texture is necessary for preview, and preview is necessary to take pictures. The same surface can be re-set without harm. Setting a preview surface will un-set any preview surface texture that was set via [setPreviewTexture](https://developer.android.com/reference/kotlin/android/hardware/Camera#setPreviewTexture(android.graphics.SurfaceTexture)).

The [SurfaceHolder](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.html#) must already contain a surface when this method is called. If you are using [android.view.SurfaceView](https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#), you will need to register a [SurfaceHolder.Callback](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.Callback.html#) with [SurfaceHolder.addCallback(SurfaceHolder.Callback)](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.html#addCallback(android.view.SurfaceHolder.Callback))and wait for [SurfaceHolder.Callback.surfaceCreated(SurfaceHolder)](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.Callback.html#surfaceCreated(android.view.SurfaceHolder))before calling setPreviewDisplay() or starting preview.

This method must be called before [startPreview()](https://developer.android.com/reference/kotlin/android/hardware/Camera#startPreview()). The one exception is that if the preview surface is not set (or set to null) before startPreview() is called, then this method may be called once with a non-null parameter to set the preview surface. (This allows camera setup and surface creation to happen in parallel, saving time.) The preview surface may not otherwise change while preview is running.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `holder` | [SurfaceHolder](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.html#)!:containing the Surface on which to place the preview, or null to remove the preview surface |

| Exceptions ||
|------------------------------|---------------------------------------------------------------------------------|
| `java.io.IOException` | if the method fails (for example, if the surface is unavailable or unsuitable). |
| `java.lang.RuntimeException` | if release() has been called on this Camera instance. |

### setPreviewTexture

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPreviewTexture(surfaceTexture: SurfaceTexture!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#) to be used for live preview. Either a surface or surface texture is necessary for preview, and preview is necessary to take pictures. The same surface texture can be re-set without harm. Setting a preview surface texture will un-set any preview surface that was set via [setPreviewDisplay](https://developer.android.com/reference/kotlin/android/hardware/Camera#setPreviewDisplay(android.view.SurfaceHolder)).

This method must be called before [startPreview()](https://developer.android.com/reference/kotlin/android/hardware/Camera#startPreview()). The one exception is that if the preview surface texture is not set (or set to null) before startPreview() is called, then this method may be called once with a non-null parameter to set the preview surface. (This allows camera setup and surface creation to happen in parallel, saving time.) The preview surface texture may not otherwise change while preview is running.

The timestamps provided by [SurfaceTexture.getTimestamp()](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#getTimestamp())for a SurfaceTexture set as the preview texture have an unspecified zero point, and cannot be directly compared between different cameras or different instances of the same camera, or across multiple runs of the same program.

If you are using the preview data to create video or still images, strongly consider using [android.media.MediaActionSound](https://developer.android.com/reference/kotlin/android/media/MediaActionSound.html#) to properly indicate image capture or recording start/stop to the user.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `surfaceTexture` | [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#)!:the [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#) to which the preview images are to be sent or null to remove the current preview surface texture |

| Exceptions ||
|------------------------------|-----------------------------------------------------------------------------------------|
| `java.io.IOException` | if the method fails (for example, if the surface texture is unavailable or unsuitable). |
| `java.lang.RuntimeException` | if release() has been called on this Camera instance. |

**See Also**

- [android.media.MediaActionSound](https://developer.android.com/reference/kotlin/android/media/MediaActionSound.html#)
- [android.graphics.SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#)
- [android.view.TextureView](https://developer.android.com/reference/kotlin/android/view/TextureView.html#) 

### setZoomChangeListener

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setZoomChangeListener(listener: Camera.OnZoomChangeListener!): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers a listener to be notified when the zoom value is updated by the camera driver during smooth zoom.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [Camera.OnZoomChangeListener](https://developer.android.com/reference/kotlin/android/hardware/Camera.OnZoomChangeListener)!:the listener to notify |

**See Also**

- [#startSmoothZoom(int)](https://developer.android.com/reference/kotlin/android/hardware/Camera#startSmoothZoom(kotlin.Int)) 

### startFaceDetection

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun startFaceDetection(): Unit
```

**Deprecated:** *Deprecated in Java.*

Starts the face detection. This should be called after preview is started. The camera will notify [FaceDetectionListener](https://developer.android.com/reference/kotlin/android/hardware/Camera.FaceDetectionListener) of the detected faces in the preview frame. The detected faces may be the same as the previous ones. Applications should call [stopFaceDetection](https://developer.android.com/reference/kotlin/android/hardware/Camera#stopFaceDetection())to stop the face detection. This method is supported if [android.hardware.Camera.Parameters#getMaxNumDetectedFaces()](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#getMaxNumDetectedFaces())returns a number larger than 0. If the face detection has started, apps should not call this again.

When the face detection is running, [Parameters.setWhiteBalance(String)](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#setWhiteBalance(kotlin.String)), [Parameters.setFocusAreas(List)](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#setFocusAreas(kotlin.collections.MutableList)), and [Parameters.setMeteringAreas(List)](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#setMeteringAreas(kotlin.collections.MutableList))have no effect. The camera uses the detected faces to do auto-white balance, auto exposure, and autofocus.

If the apps call [autoFocus(android.hardware.Camera.AutoFocusCallback)](https://developer.android.com/reference/kotlin/android/hardware/Camera#autoFocus(android.hardware.Camera.AutoFocusCallback)), the camera will stop sending face callbacks. The last face callback indicates the areas used to do autofocus. After focus completes, face detection will resume sending face callbacks. If the apps call [cancelAutoFocus()](https://developer.android.com/reference/kotlin/android/hardware/Camera#cancelAutoFocus()), the face callbacks will also resume.

After calling [takePicture(android.hardware.Camera.ShutterCallback,android.hardware.Camera.PictureCallback,android.hardware.Camera.PictureCallback)](https://developer.android.com/reference/kotlin/android/hardware/Camera#takePicture(android.hardware.Camera.ShutterCallback,%20android.hardware.Camera.PictureCallback,%20android.hardware.Camera.PictureCallback))or [stopPreview()](https://developer.android.com/reference/kotlin/android/hardware/Camera#stopPreview()), and then resuming preview with [startPreview()](https://developer.android.com/reference/kotlin/android/hardware/Camera#startPreview()), the apps should call this method again to resume face detection.

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the face detection is unsupported. |
| `java.lang.RuntimeException` | if the method fails or the face detection is already running. |

**See Also**

- [android.hardware.Camera.FaceDetectionListener](https://developer.android.com/reference/kotlin/android/hardware/Camera.FaceDetectionListener)
- <https://developer.android.com/reference/kotlin/android/hardware/Camera#stopFaceDetection()>
- [android.hardware.Camera.Parameters#getMaxNumDetectedFaces()](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#getMaxNumDetectedFaces()) 

### startPreview

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun startPreview(): Unit
```

**Deprecated:** *Deprecated in Java.*

Starts capturing and drawing preview frames to the screen. Preview will not actually start until a surface is supplied with [setPreviewDisplay(android.view.SurfaceHolder)](https://developer.android.com/reference/kotlin/android/hardware/Camera#setPreviewDisplay(android.view.SurfaceHolder))or [setPreviewTexture(android.graphics.SurfaceTexture)](https://developer.android.com/reference/kotlin/android/hardware/Camera#setPreviewTexture(android.graphics.SurfaceTexture)).

If [setPreviewCallback(android.hardware.Camera.PreviewCallback)](https://developer.android.com/reference/kotlin/android/hardware/Camera#setPreviewCallback(android.hardware.Camera.PreviewCallback)), [setOneShotPreviewCallback(android.hardware.Camera.PreviewCallback)](https://developer.android.com/reference/kotlin/android/hardware/Camera#setOneShotPreviewCallback(android.hardware.Camera.PreviewCallback)), or [setPreviewCallbackWithBuffer(android.hardware.Camera.PreviewCallback)](https://developer.android.com/reference/kotlin/android/hardware/Camera#setPreviewCallbackWithBuffer(android.hardware.Camera.PreviewCallback))were called,[Camera.PreviewCallback.onPreviewFrame(byte[], Camera)](https://developer.android.com/reference/kotlin/android/hardware/Camera.PreviewCallback#onPreviewFrame(kotlin.ByteArray,%20android.hardware.Camera))will be called when preview data becomes available.

| Exceptions ||
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.RuntimeException` | if starting preview fails; usually this would be because of a hardware or other low-level error, or because release() has been called on this Camera instance. The QCIF (176x144) exception mentioned in [setPreviewSize](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#setPreviewSize(kotlin.Int,%20kotlin.Int))and [setPictureSize](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#setPictureSize(kotlin.Int,%20kotlin.Int))can also cause this exception be thrown. |

### startSmoothZoom

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun startSmoothZoom(value: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Zooms to the requested value smoothly. The driver will notify [OnZoomChangeListener](https://developer.android.com/reference/kotlin/android/hardware/Camera.OnZoomChangeListener) of the zoom value and whether zoom is stopped at the time. For example, suppose the current zoom is 0 and startSmoothZoom is called with value 3. The [Camera.OnZoomChangeListener.onZoomChange(int, boolean, Camera)](https://developer.android.com/reference/kotlin/android/hardware/Camera.OnZoomChangeListener#onZoomChange(kotlin.Int,%20kotlin.Boolean,%20android.hardware.Camera))method will be called three times with zoom values 1, 2, and 3. Applications can call [stopSmoothZoom](https://developer.android.com/reference/kotlin/android/hardware/Camera#stopSmoothZoom())to stop the zoom earlier. Applications should not call startSmoothZoom again or change the zoom value before zoom stops. If the supplied zoom value equals to the current zoom value, no zoom callback will be generated. This method is supported if [android.hardware.Camera.Parameters#isSmoothZoomSupported](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#isSmoothZoomSupported())returns true.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):zoom value. The valid range is 0 to [android.hardware.Camera.Parameters#getMaxZoom](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#getMaxZoom()). |

| Exceptions ||
|--------------------------------------|-------------------------------|
| `java.lang.IllegalArgumentException` | if the zoom value is invalid. |
| `java.lang.RuntimeException` | if the method fails. |

**See Also**

- [#setZoomChangeListener(OnZoomChangeListener)](https://developer.android.com/reference/kotlin/android/hardware/Camera#setZoomChangeListener(android.hardware.Camera.OnZoomChangeListener)) 

### stopFaceDetection

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stopFaceDetection(): Unit
```

**Deprecated:** *Deprecated in Java.*

Stops the face detection. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/hardware/Camera#startFaceDetection()> 

### stopPreview

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stopPreview(): Unit
```

**Deprecated:** *Deprecated in Java.*

Stops capturing and drawing preview frames to the surface, and resets the camera for a future call to [startPreview()](https://developer.android.com/reference/kotlin/android/hardware/Camera#startPreview()).

| Exceptions ||
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.RuntimeException` | if stopping preview fails; usually this would be because of a hardware or other low-level error, or because release() has been called on this Camera instance. |

### stopSmoothZoom

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stopSmoothZoom(): Unit
```

**Deprecated:** *Deprecated in Java.*

Stops the smooth zoom. Applications should wait for the [OnZoomChangeListener](https://developer.android.com/reference/kotlin/android/hardware/Camera.OnZoomChangeListener) to know when the zoom is actually stopped. This method is supported if [android.hardware.Camera.Parameters#isSmoothZoomSupported](https://developer.android.com/reference/kotlin/android/hardware/Camera.Parameters#isSmoothZoomSupported())is true.

| Exceptions ||
|------------------------------|----------------------|
| `java.lang.RuntimeException` | if the method fails. |

### takePicture

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun takePicture(
    shutter: Camera.ShutterCallback!, 
    raw: Camera.PictureCallback!, 
    jpeg: Camera.PictureCallback!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Equivalent to 

```kotlin
takePicture(Shutter, raw, null, jpeg)
```
.

<br />

**See Also**

- [#takePicture(ShutterCallback, PictureCallback, PictureCallback, PictureCallback)](https://developer.android.com/reference/kotlin/android/hardware/Camera#takePicture(android.hardware.Camera.ShutterCallback,%20android.hardware.Camera.PictureCallback,%20android.hardware.Camera.PictureCallback,%20android.hardware.Camera.PictureCallback)) 

### takePicture

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun takePicture(
    shutter: Camera.ShutterCallback!, 
    raw: Camera.PictureCallback!, 
    postview: Camera.PictureCallback!, 
    jpeg: Camera.PictureCallback!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Triggers an asynchronous image capture. The camera service will initiate a series of callbacks to the application as the image capture progresses. The shutter callback occurs after the image is captured. This can be used to trigger a sound to let the user know that image has been captured. The raw callback occurs when the raw image data is available (NOTE: the data will be null if there is no raw image callback buffer available or the raw image callback buffer is not large enough to hold the raw image). The postview callback occurs when a scaled, fully processed postview image is available (NOTE: not all hardware supports this). The jpeg callback occurs when the compressed image is available. If the application does not need a particular callback, a null can be passed instead of a callback method.

This method is only valid when preview is active (after [startPreview()](https://developer.android.com/reference/kotlin/android/hardware/Camera#startPreview())). Preview will be stopped after the image is taken; callers must call [startPreview()](https://developer.android.com/reference/kotlin/android/hardware/Camera#startPreview())again if they want to re-start preview or take more pictures. This should not be called between [android.media.MediaRecorder#start()](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.html#start())and [android.media.MediaRecorder#stop()](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.html#stop()).

After calling this method, you must not call [startPreview()](https://developer.android.com/reference/kotlin/android/hardware/Camera#startPreview())or take another picture until the JPEG callback has returned.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `shutter` | [Camera.ShutterCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.ShutterCallback)!:the callback for image capture moment, or null |
| `raw` | [Camera.PictureCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.PictureCallback)!:the callback for raw (uncompressed) image data, or null |
| `postview` | [Camera.PictureCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.PictureCallback)!:callback with postview image data, may be null |
| --- | --- |
| `jpeg` | [Camera.PictureCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.PictureCallback)!:the callback for JPEG image data, or null |

| Exceptions ||
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.RuntimeException` | if starting picture capture fails; usually this would be because of a hardware or other low-level error, or because release() has been called on this Camera instance. |

### unlock

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unlock(): Unit
```

**Deprecated:** *Deprecated in Java.*

Unlocks the camera to allow another process to access it. Normally, the camera is locked to the process with an active Camera object until [release()](https://developer.android.com/reference/kotlin/android/hardware/Camera#release())is called. To allow rapid handoff between processes, you can call this method to release the camera temporarily for another process to use; once the other process is done you can call [reconnect()](https://developer.android.com/reference/kotlin/android/hardware/Camera#reconnect())to reclaim the camera.

This must be done before calling [android.media.MediaRecorder#setCamera(Camera)](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.html#setCamera(android.hardware.Camera)). This cannot be called after recording starts.

If you are not recording video, you probably do not need this method.

| Exceptions ||
|------------------------------|-----------------------------------|
| `java.lang.RuntimeException` | if the camera cannot be unlocked. |

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

**Deprecated:** *Deprecated in Java.*

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
