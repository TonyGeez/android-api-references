# android.hardware.camera2

# android.hardware.camera2

Kotlin| [Java](_package.md)
| --- | --- |

## Classes

| [CameraCaptureSession](CameraCaptureSession.md) | A configured capture session for a [CameraDevice](CameraDevice.md), used for capturing images from the camera or reprocessing images captured from the camera in the same session previously. |
| --- | --- |
| [CameraCharacteristics](CameraCharacteristics.md) | The properties describing a [CameraDevice](CameraDevice.md). |
| [CameraConstrainedHighSpeedCaptureSession](CameraConstrainedHighSpeedCaptureSession.md) | A constrained high speed capture session for a [CameraDevice](CameraDevice.md), used for capturing high speed images from the [CameraDevice](CameraDevice.md) for high speed video recording use case. |
| [CameraDevice](CameraDevice.md) | The CameraDevice class is a representation of a single camera connected to an Android device, allowing for fine-grain control of image capture and post-processing at high frame rates. |
| --- | --- |
| [CameraExtensionCharacteristics](CameraExtensionCharacteristics.md) | Allows clients to query availability and supported resolutions of camera extensions. |
| [CameraExtensionSession](CameraExtensionSession.md) | A camera capture session that enables access to device-specific camera extensions, which often use multi-frame bursts and sophisticated post-process algorithms for image capture. |
| [CameraManager](CameraManager.md) | A system service manager for detecting, characterizing, and connecting to [CameraDevices](CameraDevice.md). |
| --- | --- |
| [CameraMetadata](CameraMetadata.md) | The base class for camera controls and information. |
| [CameraOfflineSession](CameraOfflineSession.md) | A camera capture session that was switched to offline mode via successful call to [CameraCaptureSession.switchToOffline](CameraCaptureSession.md)). |
| [CaptureFailure](CaptureFailure.md) | A report of failed capture for a single image capture from the image sensor. |
| --- | --- |
| [CaptureRequest](CaptureRequest.md) | An immutable package of settings and outputs needed to capture a single image from the camera device. |
| [CaptureResult](CaptureResult.md) | The subset of the results of a single image capture from the image sensor. |
| [DngCreator](DngCreator.md) | The [DngCreator](DngCreator.md) class provides functions to write raw pixel data as a DNG file. |
| --- | --- |
| [MultiResolutionImageReader](MultiResolutionImageReader.md) | The MultiResolutionImageReader class wraps a group of [ImageReaders](../android.media/ImageReader.md) with the same format and different sizes, source camera Id, or camera sensor modes. |
| [TotalCaptureResult](TotalCaptureResult.md) | The total assembled results of a single image capture from the image sensor. |

## Exceptions

| [CameraAccessException](CameraAccessException.md) | `CameraAccessException`is thrown if a camera device could not be queried or opened by the [CameraManager](CameraManager.md), or if the connection to an opened [CameraDevice](CameraDevice.md) is no longer valid. |
| --- | --- |
