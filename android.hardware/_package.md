# android.hardware

# android.hardware

Kotlin | [Java](https://developer.android.com/reference/android/hardware/package-summary "View this page in Java")
| --- | --- |

## Interfaces

| [AutoFocusCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.AutoFocusCallback) | Callback interface used to notify on completion of camera auto focus. |
| --- | --- |
| [AutoFocusMoveCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.AutoFocusMoveCallback) | Callback interface used to notify on auto focus start and stop. |
| [ErrorCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.ErrorCallback) | Callback interface for camera error notification. |
| [FaceDetectionListener](https://developer.android.com/reference/kotlin/android/hardware/Camera.FaceDetectionListener) | Callback interface for face detected in the preview frame. |
| --- | --- |
| [OnZoomChangeListener](https://developer.android.com/reference/kotlin/android/hardware/Camera.OnZoomChangeListener) | Callback interface for zoom changes during a smooth zoom operation. |
| [PictureCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.PictureCallback) | Callback interface used to supply image data from a photo capture. |
| [PreviewCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.PreviewCallback) | Callback interface used to deliver copies of preview frames as they are displayed. |
| --- | --- |
| [ShutterCallback](https://developer.android.com/reference/kotlin/android/hardware/Camera.ShutterCallback) | Callback interface used to signal the moment of actual image capture. |
| [SensorEventListener](https://developer.android.com/reference/kotlin/android/hardware/SensorEventListener) | Used for receiving notifications from the SensorManager when there is new sensor data. |
| [SensorEventListener2](https://developer.android.com/reference/kotlin/android/hardware/SensorEventListener2) | Used for receiving a notification when a flush() has been successfully completed. |
| --- | --- |
| [SensorListener](https://developer.android.com/reference/kotlin/android/hardware/SensorListener) | Used for receiving notifications from the SensorManager when sensor values have changed. |

## Classes

| [BatteryState](https://developer.android.com/reference/kotlin/android/hardware/BatteryState) | The BatteryState class is a representation of a single battery on a device. |
| --- | --- |
| [Camera](https://developer.android.com/reference/kotlin/android/hardware/Camera) | The Camera class is used to set image capture settings, start/stop preview, snap pictures, and retrieve frames for encoding for video. |
| [ConsumerIrManager](https://developer.android.com/reference/kotlin/android/hardware/ConsumerIrManager) | Class that operates consumer infrared on the device. |
| [DataSpace](https://developer.android.com/reference/kotlin/android/hardware/DataSpace) | DataSpace identifies three components of colors - standard (primaries), transfer and range. |
| --- | --- |
| [DisplayLuts](https://developer.android.com/reference/kotlin/android/hardware/DisplayLuts) | DisplayLuts provides the developers to apply Lookup Tables (Luts) to a [android.view.SurfaceControl](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.html#). |
| [GeomagneticField](https://developer.android.com/reference/kotlin/android/hardware/GeomagneticField) | Estimates magnetic field at a given point on Earth, and in particular, to compute the magnetic declination from true north. |
| [HardwareBuffer](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer) | HardwareBuffer wraps a native `AHardwareBuffer` object, which is a low-level object representing a memory buffer accessible by various hardware units. |
| --- | --- |
| [LutProperties](https://developer.android.com/reference/kotlin/android/hardware/LutProperties) | Provides Lut properties of the device. |
| [OverlayProperties](https://developer.android.com/reference/kotlin/android/hardware/OverlayProperties) | Provides supported overlay properties of the device. |
| [Sensor](https://developer.android.com/reference/kotlin/android/hardware/Sensor) | Class representing a sensor. |
| --- | --- |
| [SensorAdditionalInfo](https://developer.android.com/reference/kotlin/android/hardware/SensorAdditionalInfo) | This class represents a [Sensor](https://developer.android.com/reference/kotlin/android/hardware/Sensor) additional information frame, which is reported through listener callback [onSensorAdditionalInfo](https://developer.android.com/reference/kotlin/android/hardware/SensorEventCallback#onSensorAdditionalInfo(android.hardware.SensorAdditionalInfo)). |
| [SensorDirectChannel](https://developer.android.com/reference/kotlin/android/hardware/SensorDirectChannel) | Class representing a sensor direct channel. |
| [SensorEvent](https://developer.android.com/reference/kotlin/android/hardware/SensorEvent) | This class represents a [Sensor](https://developer.android.com/reference/kotlin/android/hardware/Sensor) event and holds information such as the sensor's type, the time-stamp, accuracy and of course the sensor's [data](https://developer.android.com/reference/kotlin/android/hardware/SensorEvent#values:kotlin.FloatArray). |
| --- | --- |
| [SensorEventCallback](https://developer.android.com/reference/kotlin/android/hardware/SensorEventCallback) | Used for receiving sensor additional information frames. |
| [SensorManager](https://developer.android.com/reference/kotlin/android/hardware/SensorManager) | SensorManager lets you access the device's [sensors](https://developer.android.com/reference/kotlin/android/hardware/Sensor). |
| [SensorPrivacyManager](https://developer.android.com/reference/kotlin/android/hardware/SensorPrivacyManager) | This class provides information about the microphone and camera toggles. |
| --- | --- |
| [SyncFence](https://developer.android.com/reference/kotlin/android/hardware/SyncFence) | A SyncFence represents a synchronization primitive which signals when hardware units have completed work on a particular resource. |
| [TriggerEvent](https://developer.android.com/reference/kotlin/android/hardware/TriggerEvent) | This class represents a Trigger Event - the event associated with a Trigger Sensor. |
| [TriggerEventListener](https://developer.android.com/reference/kotlin/android/hardware/TriggerEventListener) | This class is the listener used to handle Trigger Sensors. |
| --- | --- |
