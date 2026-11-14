# android.hardware.camera2

# android.hardware.camera2

Kotlin| [Java](../android/hardware/camera2/_package.md)
| --- | --- |

## Classes

| [CameraCaptureSession](../android/hardware/camera2/CameraCaptureSession.md) | A configured capture session for a [CameraDevice](../android/hardware/camera2/CameraDevice.md), used for capturing images from the camera or reprocessing images captured from the camera in the same session previously. |
| --- | --- |
| [CameraCharacteristics](../android/hardware/camera2/CameraCharacteristics.md) | The properties describing a [CameraDevice](../android/hardware/camera2/CameraDevice.md). |
| [CameraConstrainedHighSpeedCaptureSession](../android/hardware/camera2/CameraConstrainedHighSpeedCaptureSession.md) | A constrained high speed capture session for a [CameraDevice](../android/hardware/camera2/CameraDevice.md), used for capturing high speed images from the [CameraDevice](../android/hardware/camera2/CameraDevice.md) for high speed video recording use case. |
| [CameraDevice](../android/hardware/camera2/CameraDevice.md) | The CameraDevice class is a representation of a single camera connected to an Android device, allowing for fine-grain control of image capture and post-processing at high frame rates. |
| --- | --- |
| [CameraExtensionCharacteristics](../android/hardware/camera2/CameraExtensionCharacteristics.md) | Allows clients to query availability and supported resolutions of camera extensions. |
| [CameraExtensionSession](../android/hardware/camera2/CameraExtensionSession.md) | A camera capture session that enables access to device-specific camera extensions, which often use multi-frame bursts and sophisticated post-process algorithms for image capture. |
| [CameraManager](../android/hardware/camera2/CameraManager.md) | A system service manager for detecting, characterizing, and connecting to [CameraDevices](../android/hardware/camera2/CameraDevice.md). |
| --- | --- |
| [CameraMetadata](../android/hardware/camera2/CameraMetadata.md) | The base class for camera controls and information. |
| [CameraOfflineSession](../android/hardware/camera2/CameraOfflineSession.md) | A camera capture session that was switched to offline mode via successful call to [CameraCaptureSession.switchToOffline](../android/hardware/camera2/CameraCaptureSession.md)). |
| [CaptureFailure](../android/hardware/camera2/CaptureFailure.md) | A report of failed capture for a single image capture from the image sensor. |
| --- | --- |
| [CaptureRequest](../android/hardware/camera2/CaptureRequest.md) | An immutable package of settings and outputs needed to capture a single image from the camera device. |
| [CaptureResult](../android/hardware/camera2/CaptureResult.md) | The subset of the results of a single image capture from the image sensor. |
| [DngCreator](../android/hardware/camera2/DngCreator.md) | The [DngCreator](../android/hardware/camera2/DngCreator.md) class provides functions to write raw pixel data as a DNG file. |
| --- | --- |
| [MultiResolutionImageReader](../android/hardware/camera2/MultiResolutionImageReader.md) | The MultiResolutionImageReader class wraps a group of [ImageReaders](../android/media/ImageReader.md) with the same format and different sizes, source camera Id, or camera sensor modes. |
| [TotalCaptureResult](../android/hardware/camera2/TotalCaptureResult.md) | The total assembled results of a single image capture from the image sensor. |

## Exceptions

| [CameraAccessException](../android/hardware/camera2/CameraAccessException.md) | `CameraAccessException`is thrown if a camera device could not be queried or opened by the [CameraManager](../android/hardware/camera2/CameraManager.md), or if the connection to an opened [CameraDevice](../android/hardware/camera2/CameraDevice.md) is no longer valid. |
| --- | --- |
