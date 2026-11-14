# android.hardware.camera2

# android.hardware.camera2

Kotlin| [Java](https://developer.android.com/reference/android/hardware/camera2/package-summary "View this page in Java")
| --- | --- |

## Classes

| [CameraCaptureSession](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession) | A configured capture session for a [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice), used for capturing images from the camera or reprocessing images captured from the camera in the same session previously. |
| --- | --- |
| [CameraCharacteristics](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics) | The properties describing a [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice). |
| [CameraConstrainedHighSpeedCaptureSession](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraConstrainedHighSpeedCaptureSession) | A constrained high speed capture session for a [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice), used for capturing high speed images from the [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice) for high speed video recording use case. |
| [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice) | The CameraDevice class is a representation of a single camera connected to an Android device, allowing for fine-grain control of image capture and post-processing at high frame rates. |
| --- | --- |
| [CameraExtensionCharacteristics](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionCharacteristics) | Allows clients to query availability and supported resolutions of camera extensions. |
| [CameraExtensionSession](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession) | A camera capture session that enables access to device-specific camera extensions, which often use multi-frame bursts and sophisticated post-process algorithms for image capture. |
| [CameraManager](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager) | A system service manager for detecting, characterizing, and connecting to [CameraDevices](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice). |
| --- | --- |
| [CameraMetadata](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata) | The base class for camera controls and information. |
| [CameraOfflineSession](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraOfflineSession) | A camera capture session that was switched to offline mode via successful call to [CameraCaptureSession.switchToOffline](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession#switchToOffline(kotlin.collections.MutableCollection,%20java.util.concurrent.Executor,%20android.hardware.camera2.CameraOfflineSession.CameraOfflineSessionCallback)). |
| [CaptureFailure](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureFailure) | A report of failed capture for a single image capture from the image sensor. |
| --- | --- |
| [CaptureRequest](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest) | An immutable package of settings and outputs needed to capture a single image from the camera device. |
| [CaptureResult](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult) | The subset of the results of a single image capture from the image sensor. |
| [DngCreator](https://developer.android.com/reference/kotlin/android/hardware/camera2/DngCreator) | The [DngCreator](https://developer.android.com/reference/kotlin/android/hardware/camera2/DngCreator) class provides functions to write raw pixel data as a DNG file. |
| --- | --- |
| [MultiResolutionImageReader](https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader) | The MultiResolutionImageReader class wraps a group of [ImageReaders](https://developer.android.com/reference/kotlin/android/media/ImageReader.html#) with the same format and different sizes, source camera Id, or camera sensor modes. |
| [TotalCaptureResult](https://developer.android.com/reference/kotlin/android/hardware/camera2/TotalCaptureResult) | The total assembled results of a single image capture from the image sensor. |

## Exceptions

| [CameraAccessException](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException) | `CameraAccessException`is thrown if a camera device could not be queried or opened by the [CameraManager](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager), or if the connection to an opened [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice) is no longer valid. |
| --- | --- |
