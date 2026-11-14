# CaptureFailure

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CaptureFailure

Kotlin| [Java](../android/hardware/camera2/CaptureFailure.md) 
| --- | --- |

```
open class CaptureFailure
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.CaptureFailure](../android/hardware/camera2/CaptureFailure.md) |

A report of failed capture for a single image capture from the image sensor.

CaptureFailures are produced by a [CameraDevice](../android/hardware/camera2/CameraDevice.md) if processing a [CaptureRequest](../android/hardware/camera2/CaptureRequest.md) fails, either partially or fully. Use [getReason](../android/hardware/camera2/CaptureFailure.md))to determine the specific nature of the failed capture.

Receiving a CaptureFailure means that the metadata associated with that frame number has been dropped -- no [CaptureResult](../android/hardware/camera2/CaptureResult.md) with the same frame number will be produced.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_ERROR](../android/hardware/camera2/CaptureFailure.md) The [CaptureResult](../android/hardware/camera2/CaptureResult.md) has been dropped this frame only due to an error in the framework. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REASON_FLUSHED](../android/hardware/camera2/CaptureFailure.md) The capture has failed due to a [CameraCaptureSession.abortCaptures](../android/hardware/camera2/CameraCaptureSession.md))call from the application. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getFrameNumber](../android/hardware/camera2/CaptureFailure.md))`()` Get the frame number associated with this failed capture. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPhysicalCameraId](../android/hardware/camera2/CaptureFailure.md))`()` The physical camera device ID in case the capture failure comes from a [CaptureRequest](../android/hardware/camera2/CaptureRequest.md) with configured physical camera streams for a logical camera. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReason](../android/hardware/camera2/CaptureFailure.md))`()` Determine why the request was dropped, whether due to an error or to a user action. |
| --- | --- |
| open [CaptureRequest](../android/hardware/camera2/CaptureRequest.md) | [getRequest](../android/hardware/camera2/CaptureFailure.md))`()` Get the request associated with this failed capture. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSequenceId](../android/hardware/camera2/CaptureFailure.md))`()` The sequence ID for this failed capture that was returned by the [CameraCaptureSession.capture](../android/hardware/camera2/CameraCaptureSession.md))family of functions. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [wasImageCaptured](../android/hardware/camera2/CaptureFailure.md))`()` Determine if the image was captured from the camera. |
| --- | --- |

## Constants

### REASON_ERROR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_ERROR: Int
```

The [CaptureResult](../android/hardware/camera2/CaptureResult.md) has been dropped this frame only due to an error in the framework. 

 Value: 0

**See Also**

- <https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureFailure#getReason()> 

### REASON_FLUSHED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REASON_FLUSHED: Int
```

The capture has failed due to a [CameraCaptureSession.abortCaptures](../android/hardware/camera2/CameraCaptureSession.md))call from the application. 

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

This value monotonically increments, starting with 0, for every new result or failure; and the scope is the lifetime of the [CameraDevice](../android/hardware/camera2/CameraDevice.md).

| Return ||
|------------------------------------------------------------------------------|-------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | long frame number |

### getPhysicalCameraId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPhysicalCameraId(): String?
```

The physical camera device ID in case the capture failure comes from a [CaptureRequest](../android/hardware/camera2/CaptureRequest.md) with configured physical camera streams for a logical camera.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | String The physical camera device ID of the respective failing output.`null`in case the capture request has no associated physical camera device. |

**See Also**

- [android.hardware.camera2.CaptureRequest.Builder#setPhysicalCameraKey](../android/hardware/camera2/CaptureRequest.Builder.md))
- [android.hardware.camera2.params.OutputConfiguration#setPhysicalCameraId](../android/hardware/camera2/params/OutputConfiguration.md)) 

### getReason

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReason(): Int
```

Determine why the request was dropped, whether due to an error or to a user action.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | int The reason code. Value is [android.hardware.camera2.CaptureFailure#REASON_ERROR](../android/hardware/camera2/CaptureFailure.md), or [android.hardware.camera2.CaptureFailure#REASON_FLUSHED](../android/hardware/camera2/CaptureFailure.md) |

**See Also**

- [#REASON_ERROR](../android/hardware/camera2/CaptureFailure.md)
- [#REASON_FLUSHED](../android/hardware/camera2/CaptureFailure.md) 

### getRequest

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRequest(): CaptureRequest
```

Get the request associated with this failed capture.

Whenever a request is unsuccessfully captured, with [CameraCaptureSession.CaptureCallback.onCaptureFailed](../android/hardware/camera2/CameraCaptureSession.CaptureCallback.md)), the`failed capture`'s`getRequest()`will return that`request`.

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
| [CaptureRequest](../android/hardware/camera2/CaptureRequest.md) | The request associated with this failed capture. Never`null`. |

### getSequenceId

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSequenceId(): Int
```

The sequence ID for this failed capture that was returned by the [CameraCaptureSession.capture](../android/hardware/camera2/CameraCaptureSession.md))family of functions.

The sequence ID is a unique monotonically increasing value starting from 0, incremented every time a new group of requests is submitted to the CameraDevice.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | int The ID for the sequence of requests that this capture failure is the result of |

**See Also**

- [android.hardware.camera2.CameraCaptureSession.CaptureCallback#onCaptureSequenceCompleted](../android/hardware/camera2/CameraCaptureSession.CaptureCallback.md)) 

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
