# CaptureFailure

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CaptureFailure

Kotlin| [Java](https://developer.android.com/reference/android/hardware/camera2/CaptureFailure "View this page in Java") 

```
open class CaptureFailure
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.hardware.camera2.CaptureFailure](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureFailure#) |

A report of failed capture for a single image capture from the image sensor.

CaptureFailures are produced by a [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice) if processing a [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest) fails, either partially or fully. Use [getReason](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureFailure#getReason())to determine the specific nature of the failed capture.

Receiving a CaptureFailure means that the metadata associated with that frame number has been dropped -- no [CaptureResult](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult) with the same frame number will be produced.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_ERROR](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureFailure#REASON_ERROR:kotlin.Int) The [CaptureResult](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult) has been dropped this frame only due to an error in the framework. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_FLUSHED](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureFailure#REASON_FLUSHED:kotlin.Int) The capture has failed due to a [CameraCaptureSession.abortCaptures](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#abortCaptures())call from the application. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getFrameNumber](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureFailure#getFrameNumber())`()` Get the frame number associated with this failed capture. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPhysicalCameraId](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureFailure#getPhysicalCameraId())`()` The physical camera device ID in case the capture failure comes from a [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest) with configured physical camera streams for a logical camera. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReason](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureFailure#getReason())`()` Determine why the request was dropped, whether due to an error or to a user action. |
| open [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest) | [getRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureFailure#getRequest())`()` Get the request associated with this failed capture. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSequenceId](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureFailure#getSequenceId())`()` The sequence ID for this failed capture that was returned by the [CameraCaptureSession.capture](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#capture(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler))family of functions. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [wasImageCaptured](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureFailure#wasImageCaptured())`()` Determine if the image was captured from the camera. |

## Constants

### REASON_ERROR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_ERROR: Int
```

The [CaptureResult](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult) has been dropped this frame only due to an error in the framework. 

 Value: 0

**See Also**

- <https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureFailure#getReason()> 

### REASON_FLUSHED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_FLUSHED: Int
```

The capture has failed due to a [CameraCaptureSession.abortCaptures](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#abortCaptures())call from the application. 

 Value: 1

**See Also**

- <https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureFailure#getReason()>

## Public methods

### getFrameNumber

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFrameNumber(): Long
```

Get the frame number associated with this failed capture.

Whenever a request has been processed, regardless of failed capture or success, it gets a unique frame number assigned to its future result/failed capture.

This value monotonically increments, starting with 0, for every new result or failure; and the scope is the lifetime of the [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice).

| Return ||
|------------------------------------------------------------------------------|-------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | long frame number |

### getPhysicalCameraId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPhysicalCameraId(): String?
```

The physical camera device ID in case the capture failure comes from a [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest) with configured physical camera streams for a logical camera.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | String The physical camera device ID of the respective failing output.`null`in case the capture request has no associated physical camera device. |

**See Also**

- [android.hardware.camera2.CaptureRequest.Builder#setPhysicalCameraKey](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.Builder#setPhysicalCameraKey(android.hardware.camera2.CaptureRequest.Key,%20android.hardware.camera2.CaptureRequest.Builder.setPhysicalCameraKey.T,%20kotlin.String))
- [android.hardware.camera2.params.OutputConfiguration#setPhysicalCameraId](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#setPhysicalCameraId(kotlin.String)) 

### getReason

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReason(): Int
```

Determine why the request was dropped, whether due to an error or to a user action.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | int The reason code. Value is [android.hardware.camera2.CaptureFailure#REASON_ERROR](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureFailure#REASON_ERROR:kotlin.Int), or [android.hardware.camera2.CaptureFailure#REASON_FLUSHED](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureFailure#REASON_FLUSHED:kotlin.Int) |

**See Also**

- [#REASON_ERROR](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureFailure#REASON_ERROR:kotlin.Int)
- [#REASON_FLUSHED](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureFailure#REASON_FLUSHED:kotlin.Int) 

### getRequest

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRequest(): CaptureRequest
```

Get the request associated with this failed capture.

Whenever a request is unsuccessfully captured, with [CameraCaptureSession.CaptureCallback.onCaptureFailed](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback#onCaptureFailed(android.hardware.camera2.CameraCaptureSession,%20android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CaptureFailure)), the`failed capture`'s`getRequest()`will return that`request`.

In particular, 

```kotlin
<code>cameraDevice.capture(someRequest, new CaptureCallback() {
      @Override
      void onCaptureFailed(CaptureRequest myRequest, CaptureFailure myFailure) {
          assert(myFailure.getRequest.equals(myRequest) == true);
      }
  };
  </code>
```

<br />

| Return ||
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest) | The request associated with this failed capture. Never`null`. |

### getSequenceId

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSequenceId(): Int
```

The sequence ID for this failed capture that was returned by the [CameraCaptureSession.capture](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#capture(android.hardware.camera2.CaptureRequest,%20android.hardware.camera2.CameraCaptureSession.CaptureCallback,%20android.os.Handler))family of functions.

The sequence ID is a unique monotonically increasing value starting from 0, incremented every time a new group of requests is submitted to the CameraDevice.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | int The ID for the sequence of requests that this capture failure is the result of |

**See Also**

- [android.hardware.camera2.CameraCaptureSession.CaptureCallback#onCaptureSequenceCompleted](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.CaptureCallback#onCaptureSequenceCompleted(android.hardware.camera2.CameraCaptureSession,%20kotlin.Int,%20kotlin.Long)) 

### wasImageCaptured

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun wasImageCaptured(): Boolean
```

Determine if the image was captured from the camera.

If the image was not captured, no image buffers will be available. If the image was captured, then image buffers may be available.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean True if the image was captured, false otherwise. |
