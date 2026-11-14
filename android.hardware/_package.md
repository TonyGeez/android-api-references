# android.hardware

# android.hardware

Kotlin | [Java](../android/hardware/_package.md)
| --- | --- |

## Interfaces

| [AutoFocusCallback](../android/hardware/Camera.AutoFocusCallback.md) | Callback interface used to notify on completion of camera auto focus. |
| --- | --- |
| [AutoFocusMoveCallback](../android/hardware/Camera.AutoFocusMoveCallback.md) | Callback interface used to notify on auto focus start and stop. |
| [ErrorCallback](../android/hardware/Camera.ErrorCallback.md) | Callback interface for camera error notification. |
| [FaceDetectionListener](../android/hardware/Camera.FaceDetectionListener.md) | Callback interface for face detected in the preview frame. |
| --- | --- |
| [OnZoomChangeListener](../android/hardware/Camera.OnZoomChangeListener.md) | Callback interface for zoom changes during a smooth zoom operation. |
| [PictureCallback](../android/hardware/Camera.PictureCallback.md) | Callback interface used to supply image data from a photo capture. |
| [PreviewCallback](../android/hardware/Camera.PreviewCallback.md) | Callback interface used to deliver copies of preview frames as they are displayed. |
| --- | --- |
| [ShutterCallback](../android/hardware/Camera.ShutterCallback.md) | Callback interface used to signal the moment of actual image capture. |
| [SensorEventListener](../android/hardware/SensorEventListener.md) | Used for receiving notifications from the SensorManager when there is new sensor data. |
| [SensorEventListener2](../android/hardware/SensorEventListener2.md) | Used for receiving a notification when a flush() has been successfully completed. |
| --- | --- |
| [SensorListener](../android/hardware/SensorListener.md) | Used for receiving notifications from the SensorManager when sensor values have changed. |

## Classes

| [BatteryState](../android/hardware/BatteryState.md) | The BatteryState class is a representation of a single battery on a device. |
| --- | --- |
| [Camera](../android/hardware/Camera.md) | The Camera class is used to set image capture settings, start/stop preview, snap pictures, and retrieve frames for encoding for video. |
| [ConsumerIrManager](../android/hardware/ConsumerIrManager.md) | Class that operates consumer infrared on the device. |
| [DataSpace](../android/hardware/DataSpace.md) | DataSpace identifies three components of colors - standard (primaries), transfer and range. |
| --- | --- |
| [DisplayLuts](../android/hardware/DisplayLuts.md) | DisplayLuts provides the developers to apply Lookup Tables (Luts) to a [android.view.SurfaceControl](../android/view/SurfaceControl.md). |
| [GeomagneticField](../android/hardware/GeomagneticField.md) | Estimates magnetic field at a given point on Earth, and in particular, to compute the magnetic declination from true north. |
| [HardwareBuffer](../android/hardware/HardwareBuffer.md) | HardwareBuffer wraps a native `AHardwareBuffer` object, which is a low-level object representing a memory buffer accessible by various hardware units. |
| --- | --- |
| [LutProperties](../android/hardware/LutProperties.md) | Provides Lut properties of the device. |
| [OverlayProperties](../android/hardware/OverlayProperties.md) | Provides supported overlay properties of the device. |
| [Sensor](../android/hardware/Sensor.md) | Class representing a sensor. |
| --- | --- |
| [SensorAdditionalInfo](../android/hardware/SensorAdditionalInfo.md) | This class represents a [Sensor](../android/hardware/Sensor.md) additional information frame, which is reported through listener callback [onSensorAdditionalInfo](../android/hardware/SensorEventCallback.md)). |
| [SensorDirectChannel](../android/hardware/SensorDirectChannel.md) | Class representing a sensor direct channel. |
| [SensorEvent](../android/hardware/SensorEvent.md) | This class represents a [Sensor](../android/hardware/Sensor.md) event and holds information such as the sensor's type, the time-stamp, accuracy and of course the sensor's [data](../android/hardware/SensorEvent.md). |
| --- | --- |
| [SensorEventCallback](../android/hardware/SensorEventCallback.md) | Used for receiving sensor additional information frames. |
| [SensorManager](../android/hardware/SensorManager.md) | SensorManager lets you access the device's [sensors](../android/hardware/Sensor.md). |
| [SensorPrivacyManager](../android/hardware/SensorPrivacyManager.md) | This class provides information about the microphone and camera toggles. |
| --- | --- |
| [SyncFence](../android/hardware/SyncFence.md) | A SyncFence represents a synchronization primitive which signals when hardware units have completed work on a particular resource. |
| [TriggerEvent](../android/hardware/TriggerEvent.md) | This class represents a Trigger Event - the event associated with a Trigger Sensor. |
| [TriggerEventListener](../android/hardware/TriggerEventListener.md) | This class is the listener used to handle Trigger Sensors. |
| --- | --- |
