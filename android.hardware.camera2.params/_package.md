# android.hardware.camera2.params

# android.hardware.camera2.params

Kotlin| [Java](https://developer.android.com/reference/android/hardware/camera2/params/package-summary "View this page in Java")
| --- | --- |

## Classes

| [BlackLevelPattern](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/BlackLevelPattern) | Immutable class to store a 4-element vector of integers corresponding to a 2x2 pattern of color channel offsets used for the black level offsets of each color channel. |
| --- | --- |
| [Capability](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Capability) | Immutable class to store the camera capability, its corresponding maximum streaming dimension and zoom range. |
| [ColorSpaceProfiles](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceProfiles) | Immutable class with information about supported color space profiles. |
| [ColorSpaceTransform](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ColorSpaceTransform) | Immutable class for describing a 3x3 matrix of [Rational](https://developer.android.com/reference/kotlin/android/util/Rational.html#) values in row-major order. |
| --- | --- |
| [DeviceStateSensorOrientationMap](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DeviceStateSensorOrientationMap) | Immutable class that maps the device fold state to sensor orientation. |
| [DynamicRangeProfiles](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles) | Immutable class with information about supported 10-bit dynamic range profiles. |
| [ExtensionSessionConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/ExtensionSessionConfiguration) | A class that aggregates all supported arguments for [CameraExtensionSession](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraExtensionSession.html#) initialization. |
| --- | --- |
| [Face](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/Face) | Describes a face detected in an image. |
| [InputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/InputConfiguration) | Immutable class to store an input configuration that is used to create a reprocessable capture session. |
| [LensIntrinsicsSample](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/LensIntrinsicsSample) | Immutable class to store an [lens intrinsics intra-frame sample](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult.html#STATISTICS_LENS_INTRINSICS_SAMPLES:android.hardware.camera2.CaptureResult.Key). |
| --- | --- |
| [LensShadingMap](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/LensShadingMap) | Immutable class for describing a`4 x N x M`lens shading map of floats. |
| [MandatoryStreamCombination](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MandatoryStreamCombination) | Immutable class to store the available mandatory stream combination. |
| [MeteringRectangle](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MeteringRectangle) | An immutable class to represent a rectangle`(x, y, width, height)`with an additional weight component. |
| --- | --- |
| [MultiResolutionStreamConfigurationMap](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MultiResolutionStreamConfigurationMap) | Immutable class to store the information of the multi-resolution streams supported by the camera device. |
| [MultiResolutionStreamInfo](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/MultiResolutionStreamInfo) | A utility class describing the properties of one stream of fixed-size image buffers backing a multi-resolution image stream. |
| [OisSample](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OisSample) | Immutable class to store an [optical image stabilization sample](https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult.html#STATISTICS_OIS_SAMPLES:android.hardware.camera2.CaptureResult.Key). |
| --- | --- |
| [OutputConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration) | A class for describing camera output, which contains a [Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#) and its specific configuration for creating capture session. |
| [RecommendedStreamConfigurationMap](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RecommendedStreamConfigurationMap) | Immutable class to store the recommended stream configurations to set up [Surfaces](https://developer.android.com/reference/kotlin/android/view/Surface.html#) for creating a [capture session](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.html#) with [android.hardware.camera2.CameraDevice#createCaptureSession(SessionConfiguration)](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)). |
| [RggbChannelVector](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/RggbChannelVector) | Immutable class to store a 4-element vector of floats indexable by a bayer RAW 2x2 pixel block. |
| --- | --- |
| [SessionConfiguration](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/SessionConfiguration) | A helper class that aggregates all supported arguments for capture session initialization. |
| [StreamConfigurationMap](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap) | Immutable class to store the available stream [configurations](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key) to set up [Surfaces](https://developer.android.com/reference/kotlin/android/view/Surface.html#) for creating a [capture session](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCaptureSession.html#) with [android.hardware.camera2.CameraDevice#createCaptureSession(SessionConfiguration)](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)). |
| [TonemapCurve](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/TonemapCurve) | Immutable class for describing a`2 x M x 3`tonemap curve of floats. |
| --- | --- |
