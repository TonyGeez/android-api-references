Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OutputConfiguration

```
class OutputConfiguration : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.params.OutputConfiguration](OutputConfiguration.md) |

A class for describing camera output, which contains a `https://developer.android.com/reference/kotlin/android/view/Surface.html#` and its specific configuration for creating capture session.

There are several ways to instantiate, modify and use OutputConfigurations. The most common and recommended usage patterns are summarized in the following list:

- Passing a `https://developer.android.com/reference/kotlin/android/view/Surface.html#` to the constructor and using the OutputConfiguration instance as argument to createCaptureSessionByOutputConfigurations. This is the most frequent usage and clients should consider it first before other more complicated alternatives.
- Passing only a surface source class as an argument to the constructor. This is usually followed by a call to create a capture session (see createCaptureSessionByOutputConfigurations and a `https://developer.android.com/reference/kotlin/android/view/Surface.html#` add call addSurface with a valid `https://developer.android.com/reference/kotlin/android/view/Surface.html#`. The sequence completes with finalizeOutputConfigurations. This is the deferred usage case which aims to enhance performance by allowing the resource-intensive capture session create call to execute in parallel with any `https://developer.android.com/reference/kotlin/android/view/Surface.html#` initialization, such as waiting for a `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#` to be ready as part of the UI initialization.
- The third and most complex usage pattern involves surface sharing. Once instantiated an OutputConfiguration can be enabled for surface sharing via enableSurfaceSharing. This must be done before creating a new capture session and enables calls to updateOutputConfiguration. An OutputConfiguration with enabled surface sharing can be modified via addSurface or removeSurface. The updates to this OutputConfiguration will only come into effect after updateOutputConfiguration returns without throwing exceptions. Such updates can be done as long as the session is active. Clients should always consider the additional requirements and limitations placed on the output surfaces (for more details see enableSurfaceSharing, addSurface, removeSurface, updateOutputConfiguration). A trade-off exists between additional complexity and flexibility. If exercised correctly surface sharing can switch between different output surfaces without interrupting any ongoing repeating capture requests. This saves time and can significantly improve the user experience.
- Surface sharing can be used in combination with deferred surfaces. The rules from both cases are combined and clients must call enableSurfaceSharing before creating a capture session. Attach and/or remove output surfaces via addSurface/removeSurface and finalize the configuration using finalizeOutputConfigurations. updateOutputConfiguration can be called after the configuration finalize method returns without exceptions.
- If the camera device supports multi-resolution output streams, `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SCALER_MULTI_RESOLUTION_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key` will contain the formats and their corresponding stream info. The application can use an OutputConfiguration created with the multi-resolution stream info queried from getOutputInfo and `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader.html#` to capture variable size images.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int`, all formats except `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#JPEG:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#RAW_PRIVATE:kotlin.Int` can be used for sharing, subject to device support. On prior API levels, only `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` format may be used.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#MIRROR_MODE_AUTO:kotlin.Int` Automatic mirroring based on camera facing |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#MIRROR_MODE_H:kotlin.Int` Camera output is mirrored horizontally |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#MIRROR_MODE_NONE:kotlin.Int` No mirror transform is applied |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#MIRROR_MODE_V:kotlin.Int` Camera output is mirrored vertically |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#SURFACE_GROUP_ID_NONE:kotlin.Int` Invalid surface group ID. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_CHOREOGRAPHER_SYNCED:kotlin.Int` Timestamp is synchronized to choreographer. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_DEFAULT:kotlin.Int` Default timestamp base. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_MONOTONIC:kotlin.Int` Timestamp base roughly the same as uptimeMillis. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_REALTIME:kotlin.Int` Timestamp base roughly the same as elapsedRealtime. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_SENSOR:kotlin.Int` Timestamp base of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SENSOR_INFO_TIMESTAMP_SOURCE:android.hardware.camera2.CameraCharacteristics.Key`. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| OutputConfiguration Create a new OutputConfiguration instance, with desired Surface size and Surface source class. |
| OutputConfiguration Create a new OutputConfiguration instance with a `https://developer.android.com/reference/kotlin/android/view/Surface.html#`. |
| OutputConfiguration Create a new OutputConfiguration instance for an `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#` for a given format and size. |
| OutputConfiguration Create a new OutputConfiguration instance for an `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#` for a given format, size, and usage flags. |
| OutputConfiguration Create a new OutputConfiguration instance with a `https://developer.android.com/reference/kotlin/android/view/Surface.html#`, with a surface group ID. |
| OutputConfiguration Create a new OutputConfiguration instance for an `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#` for a given surfaceGroupId, format, and size. |
| OutputConfiguration Create a new OutputConfiguration instance for an `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#` for a given surface group id, format, size, and usage flags. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addSensorPixelModeUsed Add a sensor pixel mode that this OutputConfiguration will be used in. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addSurface Add a surface to this OutputConfiguration. |
| static [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [OutputConfiguration](OutputConfiguration.md)!\> | createInstancesForMultiResolutionOutput Create a list of OutputConfiguration instances for the outputs used by a `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader.html#`. |
| --- | --- |
| static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [OutputConfiguration](OutputConfiguration.md)!\> | createInstancesForMultiResolutionOutput Create a list of OutputConfiguration instances for a `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader.html#`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | enableSurfaceSharing Enable multiple surfaces sharing the same OutputConfiguration |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Check if this OutputConfiguration is equal to another OutputConfiguration. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getConfiguredFormat Get the configured format associated with this OutputConfiguration. |
| [Size](../android.util/Size.md) | getConfiguredSize Get the latest configured size associated with this OutputConfiguration. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getDynamicRangeProfile Return current dynamic range profile. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMaxSharedSurfaceCount Get the maximum supported shared `https://developer.android.com/reference/kotlin/android/view/Surface.html#` count. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMirrorMode Get the current mirroring mode |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMirrorMode Get the current mirroring mode for an output surface |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getPhysicalCameraId Get the physical camera ID associated with this OutputConfiguration. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getStreamUseCase Get the current stream use case |
| --- | --- |
| [Surface](../android.view/Surface.md)? | getSurface Get the `https://developer.android.com/reference/kotlin/android/view/Surface.html#` associated with this OutputConfiguration. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSurfaceGroupId Get the surface group ID associated with this OutputConfiguration. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Surface](../android.view/Surface.md)!\> | getSurfaces Get the immutable list of surfaces associated with this OutputConfiguration. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getTimestampBase Get the current timestamp base |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getUsage Get the usage flag associated with this OutputConfiguration. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isReadoutTimestampEnabled Whether readout timestamp is used for this OutputConfiguration. |
| [OutputConfiguration](OutputConfiguration.md) | makeDeferredAndRemoveSurfaces Clear any valid output surfaces and mark the configuration as deferred. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeSensorPixelModeUsed Remove a sensor pixel mode, previously added through addSensorPixelModeUsed, from this OutputConfiguration. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeSurface Remove a surface from this OutputConfiguration. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setDynamicRangeProfile Set a specific device supported dynamic range profile. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setMirrorMode Set the mirroring mode for a surface belonging to this OutputConfiguration |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setMirrorMode Set the mirroring mode for this output target |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPhysicalCameraId Set the id of the physical camera for this OutputConfiguration |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setReadoutTimestampEnabled Use the camera sensor's readout time for the image timestamp. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setStreamUseCase Set stream use case for this OutputConfiguration |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setSurfacesForMultiResolutionOutput Set the OutputConfiguration surfaces corresponding to the `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader.html#`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTimestampBase Set timestamp base for this output target |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [OutputConfiguration](OutputConfiguration.md)!\> | `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### MIRROR_MODE_AUTO

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIRROR_MODE_AUTO: Int
```

Automatic mirroring based on camera facing

This is the default mirroring mode for the camera device. With this mode, the camera output is mirrored horizontally for front-facing cameras. There is no mirroring for rear-facing and external cameras.

 Value: 0

### MIRROR_MODE_H

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIRROR_MODE_H: Int
```

Camera output is mirrored horizontally

The camera output is mirrored horizontally, the same behavior as in AUTO mode for front facing camera.

 Value: 2

### MIRROR_MODE_NONE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIRROR_MODE_NONE: Int
```

No mirror transform is applied

No mirroring is applied to the camera output regardless of the camera facing.

 Value: 1

### MIRROR_MODE_V

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIRROR_MODE_V: Int
```

Camera output is mirrored vertically

 Value: 3

### SURFACE_GROUP_ID_NONE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SURFACE_GROUP_ID_NONE: Int
```

Invalid surface group ID.

An OutputConfiguration with this value indicates that the included surface doesn't belong to any surface group.

 Value: -1

### TIMESTAMP_BASE_CHOREOGRAPHER_SYNCED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TIMESTAMP_BASE_CHOREOGRAPHER_SYNCED: Int
```

Timestamp is synchronized to choreographer.

The timestamp of the output images are overridden with choreographer pulses from the display subsystem for smoother display of camera frames. An output target of SurfaceView uses this time base by default. Note that the timestamp override is done for fixed camera frame rate only.

This timestamp base isn't applicable to SurfaceTexture targets. SurfaceTexture's updateTexImage function always uses the latest image from the camera stream. In the case of a TextureView, the image is displayed right away.

Timestamps with this time base cannot directly match the timestamps in onCaptureStarted, onReadoutStarted, or the sensor timestamps in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult.html#`. This timestamp base shouldn't be used if the timestamp needs to be used for audio-video synchronization.

 Value: 4

### TIMESTAMP_BASE_DEFAULT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TIMESTAMP_BASE_DEFAULT: Int
```

Default timestamp base.

The camera device decides the timestamp based on the properties of the output surface.
- For a SurfaceView output surface, the timestamp base is `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_CHOREOGRAPHER_SYNCED:kotlin.Int`. The timestamp is overridden with choreographer pulses from the display subsystem for smoother display of camera frames when the camera device runs in fixed frame rate. The timestamp is roughly in the same time base as uptimeMillis.
- For an output surface of MediaRecorder, MediaCodec, or ImageReader with `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_VIDEO_ENCODE:kotlin.Long` usage flag, the timestamp base is `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_MONOTONIC:kotlin.Int`, which is roughly the same time base as uptimeMillis.
- For all other cases, the timestamp base is `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_SENSOR:kotlin.Int`, the same as what's specified by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SENSOR_INFO_TIMESTAMP_SOURCE:android.hardware.camera2.CameraCharacteristics.Key`.
 - For a SurfaceTexture output surface, the camera system re-spaces the delivery of output frames based on image readout intervals, reducing viewfinder jitter. The timestamps of images remain to be `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_SENSOR:kotlin.Int`.
- Note that the reduction of frame jitter for SurfaceView and SurfaceTexture comes with slight increase in photon-to-photon latency, which is the time from when photons hit the scene to when the corresponding pixels show up on the screen. If the photon-to-photon latency is more important than the smoothness of viewfinder, `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_SENSOR:kotlin.Int` should be used instead.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_CHOREOGRAPHER_SYNCED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_MONOTONIC:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_SENSOR:kotlin.Int`

### TIMESTAMP_BASE_MONOTONIC

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TIMESTAMP_BASE_MONOTONIC: Int
```

Timestamp base roughly the same as uptimeMillis.

The timestamps of the output images are monotonically increasing, and are roughly in the same time base as uptimeMillis. The timestamps with this time base can be directly used for audio-video sync in video recording.

If the camera device's `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SENSOR_INFO_TIMESTAMP_SOURCE:android.hardware.camera2.CameraCharacteristics.Key` is REALTIME, timestamps with this time base cannot directly match the timestamps in onCaptureStarted, onReadoutStarted, or the sensor timestamps in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult.html#`.

 Value: 2

### TIMESTAMP_BASE_REALTIME

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TIMESTAMP_BASE_REALTIME: Int
```

Timestamp base roughly the same as elapsedRealtime.

The timestamps of the output images are roughly in the same time base as elapsedRealtime. The timestamps with this time base cannot be directly used for audio-video sync in video recording.

If the camera device's `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SENSOR_INFO_TIMESTAMP_SOURCE:android.hardware.camera2.CameraCharacteristics.Key` is UNKNOWN, timestamps with this time base cannot directly match the timestamps in onCaptureStarted, onReadoutStarted, or the sensor timestamps in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureResult.html#`.

If using a REALTIME timestamp base on a device that supports only TIMESTAMP_SOURCE_UNKNOWN, the accuracy of timestamps is only what is guaranteed in the documentation for UNKNOWN. In particular, they have no guarantees about being accurate enough to use in fusing image data with the output of inertial sensors, for features such as image stabilization or augmented reality.

 Value: 3

### TIMESTAMP_BASE_SENSOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TIMESTAMP_BASE_SENSOR: Int
```

Timestamp base of `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SENSOR_INFO_TIMESTAMP_SOURCE:android.hardware.camera2.CameraCharacteristics.Key`.

The timestamps of the output images are in the time base as specified by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SENSOR_INFO_TIMESTAMP_SOURCE:android.hardware.camera2.CameraCharacteristics.Key`. The application can look up the corresponding result metadata by matching the timestamp with a onCaptureStarted, or with a onReadoutStarted if readout timestamp is used.

 Value: 1

## Public constructors

### OutputConfiguration

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
OutputConfiguration(
    surfaceSize: Size, 
    klass: Class<T>)
```

Create a new OutputConfiguration instance, with desired Surface size and Surface source class.

This constructor takes an argument for desired Surface size and the Surface source class without providing the actual output Surface. This is used to setup an output configuration with a deferred Surface. The application can use this output configuration to create a session.

Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`, the deferred Surface can be obtained: (1) from `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#` by calling getSurface, (2) from `https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#` via Surface, (3) from `https://developer.android.com/reference/kotlin/android/media/MediaRecorder.html#` via getSurface or createPersistentInputSurface, or (4) from `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#` via createInputSurface or createPersistentInputSurface.

Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int`, the `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#` deferred Surface can be obtained from getSurface. Do note that you should use OutputConfiguration to instantiate a deferred ImageReader output configuration or by calling makeDeferredAndRemoveSurfaces on an output configuration that has a non-deferred ImageReader surface.

- Surfaces for `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#` and `https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#` can be deferred until after android.hardware.camera2.CameraDevice#createCaptureSession. In that case, the output Surface must be set via addSurface, and the Surface configuration must be finalized via finalizeOutputConfigurations before submitting a request with the Surface target.
- For all other target types, the output Surface must be set by addSurface, and finalizeOutputConfigurations is not needed because the OutputConfiguration used to create the session will contain the actual Surface.

Before `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`, only `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#` and `https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#` are supported. Both kind of outputs can be deferred until after createCaptureSessionByOutputConfigurations.

An OutputConfiguration object created by this constructor can be used for isSessionConfigurationSupported and getSessionCharacteristics without having called addSurface.

| Parameters ||
|---|---|
| `surfaceSize` | [Size](../android.util/Size.md): Size for the deferred surface. This value cannot be `null`. |
| `klass` | [Class](../java.lang/Class.md)\<T\>: a non-`null` `https://developer.android.com/reference/kotlin/java/lang/Class.html#` object reference that indicates the source of this surface. Only `https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.html#`, `https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#`, `https://developer.android.com/reference/kotlin/android/media/MediaRecorder.html#`, and `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#` are supported. Before `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int`, only `https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.html#` and `https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#` are supported. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the Surface source class is not supported, or Surface size is zero. |

### OutputConfiguration

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
OutputConfiguration(surface: Surface)
```

Create a new OutputConfiguration instance with a `https://developer.android.com/reference/kotlin/android/view/Surface.html#`.

| Parameters ||
|---|---|
| `surface` | [Surface](../android.view/Surface.md): A Surface for camera to output to. This constructor creates a default configuration, with a surface group ID of {@value #SURFACE_GROUP_ID_NONE}. . This value cannot be `null`. |

### OutputConfiguration

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
OutputConfiguration(
    format: Int, 
    surfaceSize: Size)
```

Create a new OutputConfiguration instance for an `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#` for a given format and size.

This constructor creates an OutputConfiguration for an ImageReader without providing the actual output Surface. The actual output Surface must be set via addSurface before creating the capture session.

An OutputConfiguration object created by this constructor can be used for isSessionConfigurationSupported and getSessionCharacteristics without having called addSurface.

| Parameters ||
|---|---|
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The format of the ImageReader output. This must be one of the `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#` constants. Note that not all formats are supported by the camera device. |
| `surfaceSize` | [Size](../android.util/Size.md): Size for the ImageReader surface. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the Surface size is null or zero. |

### OutputConfiguration

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
OutputConfiguration(
    format: Int, 
    surfaceSize: Size, 
    usage: Long)
```

Create a new OutputConfiguration instance for an `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#` for a given format, size, and usage flags.

This constructor creates an OutputConfiguration for an ImageReader without providing the actual output Surface. The actual output Surface must be set via addSurface before creating the capture session.

An OutputConfiguration object created by this constructor can be used for isSessionConfigurationSupported and getSessionCharacteristics without having called addSurface.

| Parameters ||
|---|---|
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The format of the ImageReader output. This must be one of the `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#` constants. Note that not all formats are supported by the camera device. |
| `surfaceSize` | [Size](../android.util/Size.md): Size for the ImageReader surface. This value cannot be `null`. |
| `usage` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The usage flags of the ImageReader output surface. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_READ_RARELY:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_READ_OFTEN:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_WRITE_RARELY:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_WRITE_OFTEN:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_SAMPLED_IMAGE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_COLOR_OUTPUT:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_COMPOSER_OVERLAY:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_PROTECTED_CONTENT:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_VIDEO_ENCODE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_DATA_BUFFER:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_SENSOR_DIRECT_DATA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_CUBE_MAP:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_MIPMAP_COMPLETE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_FRONT_BUFFER:kotlin.Long` |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the Surface size is null or zero. |

### OutputConfiguration

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
OutputConfiguration(
    surfaceGroupId: Int, 
    surface: Surface)
```

Create a new OutputConfiguration instance with a `https://developer.android.com/reference/kotlin/android/view/Surface.html#`, with a surface group ID.

A surface group ID is used to identify which surface group this output surface belongs to. A surface group is a group of output surfaces that are not intended to receive camera output buffer streams simultaneously. The `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#` may be able to share the buffers used by all the surfaces from the same surface group, therefore may reduce the overall memory footprint. The application should only set the same set ID for the streams that are not simultaneously streaming. A negative ID indicates that this surface doesn't belong to any surface group. The default value is {@value #SURFACE_GROUP_ID_NONE}.

For example, a video chat application that has an adaptive output resolution feature would need two (or more) output resolutions, to switch resolutions without any output glitches. However, at any given time, only one output is active to minimize outgoing network bandwidth and encoding overhead. To save memory, the application should set the video outputs to have the same non-negative group ID, so that the camera device can share the same memory region for the alternating outputs.

It is not an error to include output streams with the same group ID in the same capture request, but the resulting memory consumption may be higher than if the two streams were not in the same surface group to begin with, especially if the outputs have substantially different dimensions.

| Parameters ||
|---|---|
| `surfaceGroupId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A group ID for this output, used for sharing memory between multiple outputs. |
| `surface` | [Surface](../android.view/Surface.md): A Surface for camera to output to. This value cannot be `null`. |

### OutputConfiguration

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
OutputConfiguration(
    surfaceGroupId: Int, 
    format: Int, 
    surfaceSize: Size)
```

Create a new OutputConfiguration instance for an `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#` for a given surfaceGroupId, format, and size.

This constructor creates an OutputConfiguration for an ImageReader without providing the actual output Surface. The actual output Surface must be set via addSurface before creating the capture session.

An OutputConfiguration object created by this constructor can be used for isSessionConfigurationSupported and getSessionCharacteristics without having called addSurface.

| Parameters ||
|---|---|
| `surfaceGroupId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A group ID for this output, used for sharing memory between multiple outputs. |
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The format of the ImageReader output. This must be one of the `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#` constants. Note that not all formats are supported by the camera device. |
| `surfaceSize` | [Size](../android.util/Size.md): Size for the ImageReader surface. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the Surface size is null or zero. |

### OutputConfiguration

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
OutputConfiguration(
    surfaceGroupId: Int, 
    format: Int, 
    surfaceSize: Size, 
    usage: Long)
```

Create a new OutputConfiguration instance for an `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#` for a given surface group id, format, size, and usage flags.

This constructor creates an OutputConfiguration for an ImageReader without providing the actual output Surface. Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int` the actual output Surface must be set via addSurface before creating the capture session. After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int`, deferred ImageReader output configurations can be used to create a capture session and then dynamically updated by calling updateOutputConfigurations before included in capture requests.

An OutputConfiguration object created by this constructor can be used for isSessionConfigurationSupported and getSessionCharacteristics without having called addSurface.

| Parameters ||
|---|---|
| `surfaceGroupId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A group ID for this output, used for sharing memory between multiple outputs. |
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The format of the ImageReader output. This must be one of the `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#` constants. Note that not all formats are supported by the camera device. |
| `surfaceSize` | [Size](../android.util/Size.md): Size for the ImageReader surface. This value cannot be `null`. |
| --- | --- |
| `usage` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The usage flags of the ImageReader output surface. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_READ_RARELY:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_READ_OFTEN:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_WRITE_RARELY:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_WRITE_OFTEN:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_SAMPLED_IMAGE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_COLOR_OUTPUT:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_COMPOSER_OVERLAY:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_PROTECTED_CONTENT:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_VIDEO_ENCODE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_DATA_BUFFER:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_SENSOR_DIRECT_DATA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_CUBE_MAP:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_MIPMAP_COMPLETE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_FRONT_BUFFER:kotlin.Long` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the Surface size is null or zero. |

## Public methods

### addSensorPixelModeUsed

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addSensorPixelModeUsed(sensorPixelModeUsed: Int): Unit
```

Add a sensor pixel mode that this OutputConfiguration will be used in.

In the case that this output stream configuration (format, width, height) is available through `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key` configurations and `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SCALER_STREAM_CONFIGURATION_MAP_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key`, configurations, the camera sub-system will assume that this OutputConfiguration will be used only with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#`s which has `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#SENSOR_PIXEL_MODE_DEFAULT:kotlin.Int`. In such cases, if clients intend to use the OutputConfiguration(s) in a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#` with other sensor pixel modes, they must specify which `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key`(s) they will use this OutputConfiguration with, by calling this method. In case this output stream configuration (format, width, height) is only in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SCALER_STREAM_CONFIGURATION_MAP_MAXIMUM_RESOLUTION:android.hardware.camera2.CameraCharacteristics.Key`, configurations, this output target must only be used with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#`s which has `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int` and that is what the camera sub-system will assume. If clients add `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#SENSOR_PIXEL_MODE_DEFAULT:kotlin.Int` in this case, session configuration will fail, if this OutputConfiguration is included. In case this output stream configuration (format, width, height) is only in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key`, configurations, this output target must only be used with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#`s which has `https://developer.android.com/reference/kotlin/android/hardware/camera2/CaptureRequest.html#SENSOR_PIXEL_MODE:android.hardware.camera2.CaptureRequest.Key` set to `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#SENSOR_PIXEL_MODE_DEFAULT:kotlin.Int` and that is what the camera sub-system will assume. If clients add `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int` in this case, session configuration will fail, if this OutputConfiguration is included.

| Parameters ||
|---|---|
| `sensorPixelModeUsed` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The sensor pixel mode this OutputConfiguration will be used with <br /> . Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#SENSOR_PIXEL_MODE_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int` |

### addSurface

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addSurface(surface: Surface): Unit
```

Add a surface to this OutputConfiguration.

This function can be called before or after createCaptureSessionByOutputConfigurations. If it's called after, the application must finalize the capture session with finalizeOutputConfigurations. It is possible to call this method after the output configurations have been finalized only in cases of enabled surface sharing see enableSurfaceSharing. The modified output configuration must be updated with updateOutputConfiguration. If this function is called before session creation, finalizeOutputConfigurations doesn't need to be called.

If the OutputConfiguration was constructed by OutputConfiguration, the added surface must be obtained:

- from `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#` by calling getSurface
- from `https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#` by calling Surface
- from `https://developer.android.com/reference/kotlin/android/media/MediaRecorder.html#` by calling getSurface or createPersistentInputSurface
- from `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#` by calling createInputSurface or createPersistentInputSurface

If the OutputConfiguration was constructed by OutputConfiguration or its variants, the added surface must be obtained from `https://developer.android.com/reference/kotlin/android/media/ImageReader.html#` by calling getSurface.

If the OutputConfiguration was constructed by other constructors, the added surface must be compatible with the existing surface. See enableSurfaceSharing for details of compatible surfaces.

If the OutputConfiguration already contains a Surface, enableSurfaceSharing must be called before calling this function to add a new Surface.

| Parameters ||
|---|---|
| `surface` | [Surface](../android.view/Surface.md): The surface to be added. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the Surface is invalid, the Surface's dataspace/format doesn't match, or adding the Surface would exceed number of shared surfaces supported. |
| `java.lang.IllegalStateException` | if the Surface was already added to this OutputConfiguration, or if the OutputConfiguration is not shared and it already has a surface associated with it. |

### createInstancesForMultiResolutionOutput

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createInstancesForMultiResolutionOutput(multiResolutionImageReader: MultiResolutionImageReader): MutableCollection<OutputConfiguration!>
```

Create a list of OutputConfiguration instances for the outputs used by a `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader.html#`.

This constructor takes an argument for a `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader.html#`.

For the output configurations returned by this function, the application must not enable surface sharing.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int`, the application must not set different timestamp bases or different readout timestamp enablements among the outputs. Otherwise, android.hardware.camera2.CameraDevice#createCaptureSession will fail.

| Parameters ||
|---|---|
| `multiResolutionImageReader` | [MultiResolutionImageReader](../android.hardware.camera2/MultiResolutionImageReader.md): The multi-resolution image reader object. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#!>` | This value cannot be `null`. |

### createInstancesForMultiResolutionOutput

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createInstancesForMultiResolutionOutput(
    streams: MutableCollection<MultiResolutionStreamInfo!>, 
    format: Int
): MutableList<OutputConfiguration!>
```

Create a list of OutputConfiguration instances for a `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader.html#`.

This method can be used to create query OutputConfigurations for a MultiResolutionImageReader that can be included in a SessionConfiguration passed into isSessionConfigurationSupported before opening and setting up a camera device in full, at which point setSurfacesForMultiResolutionOutput can be used to link to the actual MultiResolutionImageReader.

This constructor takes same arguments used to create a `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader.html#`: a collection of MultiResolutionStreamInfo objects and the format.

| Parameters ||
|---|---|
| `streams` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [MultiResolutionStreamInfo](MultiResolutionStreamInfo.md)!\>: The group of multi-resolution stream info objects, which are used to create a multi-resolution image reader containing a number of ImageReaders. This value cannot be `null`. |
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The format of the MultiResolutionImageReader. This must be one of the `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#` constants supported by the camera device. Note that not all formats are supported, like `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#NV21:kotlin.Int`. The supported multi-resolution reader format can be queried by getOutputFormats. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#!>` | The list of OutputConfiguration objects for a MultiResolutionImageReader. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the `streams` is null or doesn't contain at least 2 items, or if `format` isn't a valid camera format. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader.html#`
- MultiResolutionStreamInfo

### describeContents

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### enableSurfaceSharing

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun enableSurfaceSharing(): Unit
```

Enable multiple surfaces sharing the same OutputConfiguration

For advanced use cases, a camera application may require more streams than the combination guaranteed by android.hardware.camera2.CameraDevice#createCaptureSession. In this case, more than one compatible surface can be attached to an OutputConfiguration so that they map to one camera stream, and the outputs share memory buffers when possible. Due to buffer sharing clients should be careful when adding surface outputs that modify their input data. If such case exists, camera clients should have an additional mechanism to synchronize read and write access between individual consumers.

Two surfaces are compatible in the below cases:
- Surfaces with the same size, format, dataSpace, and Surface source class. In this case, createCaptureSessionByOutputConfigurations is guaranteed to succeed.
- Surfaces with the same size, format, and dataSpace, but different Surface source classes that are generally not compatible. However, on some devices, the underlying camera device is able to use the same buffer layout for both surfaces. The only way to discover if this is the case is to create a capture session with that output configuration. For example, if the camera device uses the same private buffer format between a SurfaceView/SurfaceTexture and a MediaRecorder/MediaCodec, createCaptureSessionByOutputConfigurations will succeed. Otherwise, it fails with onConfigureFailed.

 To enable surface sharing, this function must be called before createCaptureSessionByOutputConfigurations or createReprocessableCaptureSessionByConfigurations. Calling this function after createCaptureSessionByOutputConfigurations has no effect.

 Up to getMaxSharedSurfaceCount surfaces can be shared for an OutputConfiguration. The supported surfaces for sharing must be of type SurfaceTexture, SurfaceView, MediaRecorder, MediaCodec, or implementation defined ImageReader.

 This function must not be called from OutputConfigurations created by #createInstancesForMultiResolutionOutput.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If this OutputConfiguration is created via #createInstancesForMultiResolutionOutput to back a MultiResolutionImageReader. |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Check if this OutputConfiguration is equal to another OutputConfiguration.

Two output configurations are only equal if and only if the underlying surfaces, surface properties (width, height, format, dataspace) when the output configurations are created, and all other configuration parameters are equal.

| Parameters ||
|---|---|
| `obj` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the objects were equal, `false` otherwise |

### getConfiguredFormat

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConfiguredFormat(): Int
```

Get the configured format associated with this OutputConfiguration.

This function handles all ImageFormats and output targets supported by the camera APIs, and isn't designed for all possible OS supported formats and surfaces. For example, an ImageReader can be created using any combinations of HardwareBuffer format and dataspace. If the combination is not supported by the camera APIs, this function returns ImageFormat.UNKNOWN.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#` associated with this OutputConfiguration. |

### getConfiguredSize

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConfiguredSize(): Size
```

Get the latest configured size associated with this OutputConfiguration.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Size.html#` | The configured size associated with this OutputConfiguration. This value cannot be `null`. |

### getDynamicRangeProfile

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDynamicRangeProfile(): Long
```

Return current dynamic range profile.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the currently set dynamic range profile. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#STANDARD:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#HLG10:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#HDR10:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#HDR10_PLUS:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_REF:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_REF_PO:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_OEM:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_OEM_PO:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_REF:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_REF_PO:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_OEM:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_OEM_PO:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#STANDARD_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#HLG10_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#HDR10_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#HDR10_PLUS_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_REF_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_REF_PO_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_OEM_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_OEM_PO_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_REF_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_REF_PO_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_OEM_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_OEM_PO_SMPTE_2094_50:kotlin.Long` |

### getMaxSharedSurfaceCount

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaxSharedSurfaceCount(): Int
```

Get the maximum supported shared `https://developer.android.com/reference/kotlin/android/view/Surface.html#` count.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the maximum number of surfaces that can be added per each OutputConfiguration. |

**See Also**

- enableSurfaceSharing

### getMirrorMode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMirrorMode(): Int
```

Get the current mirroring mode

If no #setMirrorMode is called first, this function returns `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#MIRROR_MODE_AUTO:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The currently set mirroring mode. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#MIRROR_MODE_AUTO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#MIRROR_MODE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#MIRROR_MODE_H:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#MIRROR_MODE_V:kotlin.Int` |

### getMirrorMode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMirrorMode(surface: Surface): Int
```

Get the current mirroring mode for an output surface

If no #setMirrorMode is called first, this function returns `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#MIRROR_MODE_AUTO:kotlin.Int`.

If only setMirrorMode is called, the mirroring mode set by that function will be returned here as long as the `surface` belongs to this output configuration.

| Parameters ||
|---|---|
| `surface` | [Surface](../android.view/Surface.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The mirroring mode for the specified output surface. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#MIRROR_MODE_AUTO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#MIRROR_MODE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#MIRROR_MODE_H:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#MIRROR_MODE_V:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the `surface` doesn't belong to this OutputConfiguration. |

### getPhysicalCameraId

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPhysicalCameraId(): String?
```

Get the physical camera ID associated with this OutputConfiguration.

If this OutputConfiguration isn't targeting a physical camera of a logical multi-camera, this function returns `null`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | The physical camera Id associated with this OutputConfiguration. |

### getStreamUseCase

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStreamUseCase(): Long
```

Get the current stream use case

If no setStreamUseCase is called first, this function returns `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#SCALER_AVAILABLE_STREAM_USE_CASES_DEFAULT:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the currently set stream use case |

### getSurface

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSurface(): Surface?
```

Get the `https://developer.android.com/reference/kotlin/android/view/Surface.html#` associated with this OutputConfiguration. If more than one surface is associated with this OutputConfiguration, return the first one as specified in the constructor or addSurface.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/Surface.html#?` | This value may be `null`. |

### getSurfaceGroupId

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSurfaceGroupId(): Int
```

Get the surface group ID associated with this OutputConfiguration.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the surface group ID associated with this OutputConfiguration. The default value is {@value #SURFACE_GROUP_ID_NONE}. |

### getSurfaces

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSurfaces(): MutableList<Surface!>
```

Get the immutable list of surfaces associated with this OutputConfiguration.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/view/Surface.html#!>` | the list of surfaces associated with this OutputConfiguration as specified in the constructor and addSurface. The list should not be modified. This value cannot be `null`. |

### getTimestampBase

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTimestampBase(): Int
```

Get the current timestamp base

If no setTimestampBase is called first, this function returns `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_DEFAULT:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The currently set timestamp base. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_SENSOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_MONOTONIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_REALTIME:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_CHOREOGRAPHER_SYNCED:kotlin.Int` |

### getUsage

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUsage(): Long
```

Get the usage flag associated with this OutputConfiguration.

If the OutputConfiguration is created using an output surface, or using a Surface source class, this function returns the consumer usage flag of the output surface or the Surface source class.

If the OutputConfiguration is created using an Image format, this function returns the application specified usage flag. If the application doesn't specify the usage flag, the return value is 0 for `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_READ_OFTEN:kotlin.Long` for all other cases.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The usage flag associated with this OutputConfiguration, as defined in `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_READ_RARELY:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_READ_OFTEN:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_WRITE_RARELY:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_CPU_WRITE_OFTEN:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_SAMPLED_IMAGE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_COLOR_OUTPUT:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_COMPOSER_OVERLAY:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_PROTECTED_CONTENT:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_VIDEO_ENCODE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_DATA_BUFFER:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_SENSOR_DIRECT_DATA:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_CUBE_MAP:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_GPU_MIPMAP_COMPLETE:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer.html#USAGE_FRONT_BUFFER:kotlin.Long` |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the equals method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the equals method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isReadoutTimestampEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isReadoutTimestampEnabled(): Boolean
```

Whether readout timestamp is used for this OutputConfiguration.
**See Also**

- setReadoutTimestampEnabled

### makeDeferredAndRemoveSurfaces

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun makeDeferredAndRemoveSurfaces(): OutputConfiguration
```

Clear any valid output surfaces and mark the configuration as deferred.

Do note that this method is intended to be used in conjunction with updateOutputConfigurations and not finalizeOutputConfigurations. The latter method is intended to be used only when clients want to finalize an already registered deferred OutputConfiguration with a valid Surface. However surface finalization doesn't accept deferred output configurations. Switching a valid registered surface to deferred state is only possible with updateOutputConfiguration.

| Return ||
|---|---|
| OutputConfiguration | This value cannot be `null`. |

**See Also**

- updateOutputConfigurations

### removeSensorPixelModeUsed

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeSensorPixelModeUsed(sensorPixelModeUsed: Int): Unit
```

Remove a sensor pixel mode, previously added through addSensorPixelModeUsed, from this OutputConfiguration.

Sensor pixel modes added via calls to addSensorPixelModeUsed can also be removed from the OutputConfiguration.

| Parameters ||
|---|---|
| `sensorPixelModeUsed` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The sensor pixel mode to be removed. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#SENSOR_PIXEL_MODE_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#SENSOR_PIXEL_MODE_MAXIMUM_RESOLUTION:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the sensor pixel mode wasn't previously added through addSensorPixelModeUsed. |

### removeSurface

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeSurface(surface: Surface): Unit
```

Remove a surface from this OutputConfiguration.

Surfaces added via calls to addSurface can also be removed from the OutputConfiguration. The only notable exception is the surface associated with the OutputConfiguration (see getSurface) which was passed as part of the constructor or was added first in the case of OutputConfiguration, OutputConfiguration, OutputConfiguration, OutputConfiguration, OutputConfiguration.

| Parameters ||
|---|---|
| `surface` | [Surface](../android.view/Surface.md): The surface to be removed. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the surface is associated with this OutputConfiguration (see getSurface) or the surface didn't get added with addSurface. |

### setDynamicRangeProfile

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setDynamicRangeProfile(profile: Long): Unit
```

Set a specific device supported dynamic range profile.

Clients can choose from any profile advertised as supported in CameraCharacteristics.REQUEST_AVAILABLE_DYNAMIC_RANGE_PROFILES queried using getSupportedProfiles. If this is not explicitly set, then the default profile will be `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#STANDARD:kotlin.Long`.

Do note that invalid combinations between the registered output surface pixel format and the configured dynamic range profile will cause capture session initialization failure. Invalid combinations include any 10-bit dynamic range profile advertised in getSupportedProfiles combined with an output Surface pixel format different from `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#PRIVATE:kotlin.Int` (the default for Surfaces initialized by `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#`, `https://developer.android.com/reference/kotlin/android/view/TextureView.html#`, `https://developer.android.com/reference/kotlin/android/media/MediaRecorder.html#`, `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#` etc.) or `https://developer.android.com/reference/kotlin/android/graphics/ImageFormat.html#YCBCR_P010:kotlin.Int`.

| Parameters ||
|---|---|
| `profile` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#STANDARD:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#HLG10:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#HDR10:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#HDR10_PLUS:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_REF:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_REF_PO:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_OEM:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_OEM_PO:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_REF:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_REF_PO:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_OEM:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_OEM_PO:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#STANDARD_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#HLG10_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#HDR10_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#HDR10_PLUS_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_REF_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_REF_PO_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_OEM_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_10B_HDR_OEM_PO_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_REF_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_REF_PO_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_OEM_SMPTE_2094_50:kotlin.Long` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/DynamicRangeProfiles#DOLBY_VISION_8B_HDR_OEM_PO_SMPTE_2094_50:kotlin.Long` |

### setMirrorMode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setMirrorMode(
    surface: Surface, 
    mirrorMode: Int
): Unit
```

Set the mirroring mode for a surface belonging to this OutputConfiguration

This function is identical to setMirrorMode if `surface` is the only surface belonging to this OutputConfiguration.

If this OutputConfiguration contains a deferred surface, the application can either call setMirrorMode, or call this function after calling addSurface.

If this OutputConfiguration contains shared surfaces, the application can set different mirroring modes for different surfaces.

For efficiency, the mirror effect is applied as a transform flag, so it is only effective in some outputs. It works automatically for SurfaceView and TextureView outputs. For manual use of SurfaceTexture, it is reflected in the value of getTransformMatrix. For other end points, such as ImageReader, MediaRecorder, or MediaCodec, the mirror mode has no effect. If mirroring is needed for such outputs, the application needs to mirror the image buffers itself before passing them onward.

| Parameters ||
|---|---|
| `surface` | [Surface](../android.view/Surface.md): This value cannot be `null`. |
| `mirrorMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#MIRROR_MODE_AUTO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#MIRROR_MODE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#MIRROR_MODE_H:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#MIRROR_MODE_V:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the `surface` doesn't belong to this OutputConfiguration, or the `mirrorMode` value is not valid. |

### setMirrorMode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setMirrorMode(mirrorMode: Int): Unit
```

Set the mirroring mode for this output target

If this function is not called, the mirroring mode for this output is `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#MIRROR_MODE_AUTO:kotlin.Int`, with which the camera API will mirror the output images horizontally for front facing camera.

For efficiency, the mirror effect is applied as a transform flag, so it is only effective in some outputs. It works automatically for SurfaceView and TextureView outputs. For manual use of SurfaceTexture, it is reflected in the value of getTransformMatrix. For other end points, such as ImageReader, MediaRecorder, or MediaCodec, the mirror mode has no effect. If mirroring is needed for such outputs, the application needs to mirror the image buffers itself before passing them onward.

Starting from Android 16, this function sets the mirror modes for all of the output surfaces contained within this OutputConfiguration. To set the mirror mode for a particular output surface, the application can call setMirrorMode. Prior to Android 16, this function is only applicable if surface sharing is not enabled.

| Parameters ||
|---|---|
| `mirrorMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#MIRROR_MODE_AUTO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#MIRROR_MODE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#MIRROR_MODE_H:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#MIRROR_MODE_V:kotlin.Int` |

### setPhysicalCameraId

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPhysicalCameraId(physicalCameraId: String?): Unit
```

Set the id of the physical camera for this OutputConfiguration

In the case one logical camera is made up of multiple physical cameras, it could be desirable for the camera application to request streams from individual physical cameras. This call achieves it by mapping the OutputConfiguration to the physical camera id.

The valid physical camera ids can be queried by getPhysicalCameraIds.

Passing in a null physicalCameraId means that the OutputConfiguration is for a logical stream.

This function must be called before createCaptureSessionByOutputConfigurations or createReprocessableCaptureSessionByConfigurations. Calling this function after createCaptureSessionByOutputConfigurations or createReprocessableCaptureSessionByConfigurations has no effect.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, an image buffer from a physical camera stream can be used for reprocessing to logical camera streams and streams from the same physical camera if the camera device supports multi-resolution input and output streams. See `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SCALER_MULTI_RESOLUTION_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key` for details. The behaviors of reprocessing from a non-physical camera stream to a physical camera stream, and from a physical camera stream to a physical camera stream of different physical camera, are device-specific and not guaranteed to be supported.

On prior API levels, the surface belonging to a physical camera OutputConfiguration must not be used as input or output of a reprocessing request.

| Parameters ||
|---|---|
| `physicalCameraId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

### setReadoutTimestampEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setReadoutTimestampEnabled(on: Boolean): Unit
```

Use the camera sensor's readout time for the image timestamp.

The start of the camera sensor readout after exposure. For a rolling shutter camera sensor, the timestamp is typically equal to `(the start of exposure time) + (exposure time) + (certain fixed offset)`. The fixed offset can vary per session, depending on the underlying sensor configuration. The benefit of using readout time is that when camera runs in a fixed frame rate, the timestamp intervals between frames are constant.

Readout timestamp is supported only if `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SENSOR_READOUT_TIMESTAMP:android.hardware.camera2.CameraCharacteristics.Key` is `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#SENSOR_READOUT_TIMESTAMP_HARDWARE:kotlin.Int`.

As long as readout timestamp is supported, if the timestamp base is `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_CHOREOGRAPHER_SYNCED:kotlin.Int`, or if the timestamp base is DEFAULT for a SurfaceView output, the image timestamps for the output are always readout time regardless of whether this function is called.

| Parameters ||
|---|---|
| `on` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The output image timestamp is the start of exposure time if false, and the start of readout time if true. |

### setStreamUseCase

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setStreamUseCase(streamUseCase: Long): Unit
```

Set stream use case for this OutputConfiguration

Stream use case is used to describe the purpose of the stream, whether it's for live preview, still image capture, video recording, or their combinations. This flag is useful for scenarios where the immediate consumer target isn't sufficient to indicate the stream's usage.

The main difference between stream use case and capture intent is that the former enables the camera device to optimize camera hardware and software pipelines based on user scenarios for each stream, whereas the latter is mainly a hint to camera to decide optimal 3A strategy that's applicable to the whole session. The camera device carries out configurations such as selecting tuning parameters, choosing camera sensor mode, and constructing image processing pipeline based on the streams's use cases. Capture intents are then used to fine tune 3A behaviors such as adjusting AE/AF convergence speed, and capture intents may change during the lifetime of a session. For example, for a session with a PREVIEW_VIDEO_STILL use case stream and a STILL_CAPTURE use case stream, the capture intents may be PREVIEW with fast 3A convergence speed and flash metering with automatic control for live preview, STILL_CAPTURE with best 3A parameters for still photo capture, or VIDEO_RECORD with slower 3A convergence speed for better video playback experience.

The supported stream use cases supported by a camera device can be queried by `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SCALER_AVAILABLE_STREAM_USE_CASES:android.hardware.camera2.CameraCharacteristics.Key`.

The mandatory stream combinations involving stream use cases can be found at android.hardware.camera2.CameraDevice#createCaptureSession, as well as queried via MandatoryStreamCombination. The application is strongly recommended to select one of the guaranteed stream combinations where all streams' use cases are set to non-DEFAULT values. If the application chooses a stream combination not in the mandatory list, the camera device may ignore some use case flags due to hardware constraints or implementation details.

This function must be called before android.hardware.camera2.CameraDevice#createCaptureSession or createCaptureSessionByOutputConfigurations. Calling this function after android.hardware.camera2.CameraDevice#createCaptureSession or createCaptureSessionByOutputConfigurations has no effect to the camera session.

| Parameters ||
|---|---|
| `streamUseCase` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The stream use case to be set. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#SCALER_AVAILABLE_STREAM_USE_CASES_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#SCALER_AVAILABLE_STREAM_USE_CASES_PREVIEW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#SCALER_AVAILABLE_STREAM_USE_CASES_STILL_CAPTURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#SCALER_AVAILABLE_STREAM_USE_CASES_VIDEO_RECORD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#SCALER_AVAILABLE_STREAM_USE_CASES_PREVIEW_VIDEO_STILL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#SCALER_AVAILABLE_STREAM_USE_CASES_VIDEO_CALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#SCALER_AVAILABLE_STREAM_USE_CASES_CROPPED_RAW:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the streamUseCase isn't within the range of valid values. |

### setSurfacesForMultiResolutionOutput

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setSurfacesForMultiResolutionOutput(
    outputConfigurations: MutableCollection<OutputConfiguration!>, 
    multiResolutionImageReader: MultiResolutionImageReader
): Unit
```

Set the OutputConfiguration surfaces corresponding to the `https://developer.android.com/reference/kotlin/android/hardware/camera2/MultiResolutionImageReader.html#`.

This function should be used together with #createInstancesForMultiResolutionOutput. The application calls #createInstancesForMultiResolutionOutput first to create a list of OutputConfiguration objects without the actual MultiResolutionImageReader. Once the MultiResolutionImageReader is created later during full camera setup, the application then calls this function to assign the surfaces to the OutputConfiguration instances.

| Parameters ||
|---|---|
| `outputConfigurations` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [OutputConfiguration](OutputConfiguration.md)!\>: The OutputConfiguration objects created by #createInstancesForMultiResolutionOutput This value cannot be `null`. |
| `multiResolutionImageReader` | [MultiResolutionImageReader](../android.hardware.camera2/MultiResolutionImageReader.md): The MultiResolutionImageReader object created from the same MultiResolutionStreamInfo parameters as `outputConfigurations`. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If `outputConfigurations` or `multiResolutionImageReader` is `null`, the `outputConfigurations` and `multiResolutionImageReader` sizes don't match, or if the `multiResolutionImageReader`'s surfaces don't match with the `outputConfigurations`. |
| `java.lang.IllegalStateException` | If `outputConfigurations` already contains valid output surfaces. |

### setTimestampBase

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setTimestampBase(timestampBase: Int): Unit
```

Set timestamp base for this output target

Timestamp base describes the time domain of images from this camera output and its relationship with `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SENSOR_INFO_TIMESTAMP_SOURCE:android.hardware.camera2.CameraCharacteristics.Key`.

If this function is not called, the timestamp base for this output is `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_DEFAULT:kotlin.Int`, with which the camera device adjusts timestamps based on the output target.

See `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_DEFAULT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_SENSOR:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_CHOREOGRAPHER_SYNCED:kotlin.Int` for details of each timestamp base.

| Parameters ||
|---|---|
| `timestampBase` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The timestamp base to be set. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_SENSOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_MONOTONIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_REALTIME:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/camera2/params/OutputConfiguration#TIMESTAMP_BASE_CHOREOGRAPHER_SYNCED:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the timestamp base isn't within the range of valid values. |

### writeToParcel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<OutputConfiguration!>
```
