# android.hardware.camera2.params

# android.hardware.camera2.params

Kotlin| [Java](../android/hardware/camera2/params/_package.md)
| --- | --- |

## Classes

| [BlackLevelPattern](../android/hardware/camera2/params/BlackLevelPattern.md) | Immutable class to store a 4-element vector of integers corresponding to a 2x2 pattern of color channel offsets used for the black level offsets of each color channel. |
| --- | --- |
| [Capability](../android/hardware/camera2/params/Capability.md) | Immutable class to store the camera capability, its corresponding maximum streaming dimension and zoom range. |
| [ColorSpaceProfiles](../android/hardware/camera2/params/ColorSpaceProfiles.md) | Immutable class with information about supported color space profiles. |
| [ColorSpaceTransform](../android/hardware/camera2/params/ColorSpaceTransform.md) | Immutable class for describing a 3x3 matrix of [Rational](../android/util/Rational.md) values in row-major order. |
| --- | --- |
| [DeviceStateSensorOrientationMap](../android/hardware/camera2/params/DeviceStateSensorOrientationMap.md) | Immutable class that maps the device fold state to sensor orientation. |
| [DynamicRangeProfiles](../android/hardware/camera2/params/DynamicRangeProfiles.md) | Immutable class with information about supported 10-bit dynamic range profiles. |
| [ExtensionSessionConfiguration](../android/hardware/camera2/params/ExtensionSessionConfiguration.md) | A class that aggregates all supported arguments for [CameraExtensionSession](../android/hardware/camera2/CameraExtensionSession.md) initialization. |
| --- | --- |
| [Face](../android/hardware/camera2/params/Face.md) | Describes a face detected in an image. |
| [InputConfiguration](../android/hardware/camera2/params/InputConfiguration.md) | Immutable class to store an input configuration that is used to create a reprocessable capture session. |
| [LensIntrinsicsSample](../android/hardware/camera2/params/LensIntrinsicsSample.md) | Immutable class to store an [lens intrinsics intra-frame sample](../android/hardware/camera2/CaptureResult.md). |
| --- | --- |
| [LensShadingMap](../android/hardware/camera2/params/LensShadingMap.md) | Immutable class for describing a`4 x N x M`lens shading map of floats. |
| [MandatoryStreamCombination](../android/hardware/camera2/params/MandatoryStreamCombination.md) | Immutable class to store the available mandatory stream combination. |
| [MeteringRectangle](../android/hardware/camera2/params/MeteringRectangle.md) | An immutable class to represent a rectangle`(x, y, width, height)`with an additional weight component. |
| --- | --- |
| [MultiResolutionStreamConfigurationMap](../android/hardware/camera2/params/MultiResolutionStreamConfigurationMap.md) | Immutable class to store the information of the multi-resolution streams supported by the camera device. |
| [MultiResolutionStreamInfo](../android/hardware/camera2/params/MultiResolutionStreamInfo.md) | A utility class describing the properties of one stream of fixed-size image buffers backing a multi-resolution image stream. |
| [OisSample](../android/hardware/camera2/params/OisSample.md) | Immutable class to store an [optical image stabilization sample](../android/hardware/camera2/CaptureResult.md). |
| --- | --- |
| [OutputConfiguration](../android/hardware/camera2/params/OutputConfiguration.md) | A class for describing camera output, which contains a [Surface](../android/view/Surface.md) and its specific configuration for creating capture session. |
| [RecommendedStreamConfigurationMap](../android/hardware/camera2/params/RecommendedStreamConfigurationMap.md) | Immutable class to store the recommended stream configurations to set up [Surfaces](../android/view/Surface.md) for creating a [capture session](../android/hardware/camera2/CameraCaptureSession.md) with [android.hardware.camera2.CameraDevice#createCaptureSession(SessionConfiguration)](../android/hardware/camera2/CameraDevice.md)). |
| [RggbChannelVector](../android/hardware/camera2/params/RggbChannelVector.md) | Immutable class to store a 4-element vector of floats indexable by a bayer RAW 2x2 pixel block. |
| --- | --- |
| [SessionConfiguration](../android/hardware/camera2/params/SessionConfiguration.md) | A helper class that aggregates all supported arguments for capture session initialization. |
| [StreamConfigurationMap](../android/hardware/camera2/params/StreamConfigurationMap.md) | Immutable class to store the available stream [configurations](../android/hardware/camera2/CameraCharacteristics.md) to set up [Surfaces](../android/view/Surface.md) for creating a [capture session](../android/hardware/camera2/CameraCaptureSession.md) with [android.hardware.camera2.CameraDevice#createCaptureSession(SessionConfiguration)](../android/hardware/camera2/CameraDevice.md)). |
| [TonemapCurve](../android/hardware/camera2/params/TonemapCurve.md) | Immutable class for describing a`2 x M x 3`tonemap curve of floats. |
| --- | --- |
