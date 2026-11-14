Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MockPackageManager

```
open class MockPackageManager : PackageManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.content.pm.PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#) ||
| | ↳ | [android.test.mock.MockPackageManager](https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#) |

> [!CAUTION]
> **This class was deprecated in API level 24.**
>
> Use a mocking framework like [Mockito](https://github.com/mockito/mockito). New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

A mock `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#` class. All methods are non-functional and throw `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`. Override it to provide the operations that you need.

## Summary

Inherited constants From class `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#CERT_INPUT_RAW_X509:kotlin.Int`

Certificate input bytes: the input bytes represent an encoded X.509 Certificate which could be generated using an `CertificateFactory`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#CERT_INPUT_SHA256:kotlin.Int`

Certificate input bytes: the input bytes represent the SHA256 output of an encoded X.509 Certificate.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_DEFAULT:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#setApplicationEnabledSetting(kotlin.String,%20kotlin.Int,%20kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#setComponentEnabledSetting(android.content.ComponentName,%20kotlin.Int,%20kotlin.Int)`: This component or application is in its default enabled state (as specified in its manifest).

Explicitly setting the component state to this value restores it's enabled state to whatever is set in the manifest.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_DISABLED:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#setApplicationEnabledSetting(kotlin.String,%20kotlin.Int,%20kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#setComponentEnabledSetting(android.content.ComponentName,%20kotlin.Int,%20kotlin.Int)`: This component or application has been explicitly disabled, regardless of what it has specified in its manifest.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_DISABLED_UNTIL_USED:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#setApplicationEnabledSetting(kotlin.String,%20kotlin.Int,%20kotlin.Int)` only: This application should be considered, until the point where the user actually wants to use it. This means that it will not normally show up to the user (such as in the launcher), but various parts of the user interface can use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_DISABLED_UNTIL_USED_COMPONENTS:kotlin.Int` to still see it and allow the user to select it (as for example an IME, device admin, etc). Such code, once the user has selected the app, should at that point also make it enabled. This option currently **can not** be used with `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#setComponentEnabledSetting(android.content.ComponentName,%20kotlin.Int,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_DISABLED_USER:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#setApplicationEnabledSetting(kotlin.String,%20kotlin.Int,%20kotlin.Int)` only: The user has explicitly disabled the application, regardless of what it has specified in its manifest. Because this is due to the user's request, they may re-enable it if desired through the appropriate system UI. This option currently **cannot** be used with `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#setComponentEnabledSetting(android.content.ComponentName,%20kotlin.Int,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_ENABLED:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#setApplicationEnabledSetting(kotlin.String,%20kotlin.Int,%20kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#setComponentEnabledSetting(android.content.ComponentName,%20kotlin.Int,%20kotlin.Int)`: This component or application has been explictily enabled, regardless of what it has specified in its manifest.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#DELETE_ARCHIVE:kotlin.Int`

Flag parameter for `https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.html#uninstall(android.content.pm.VersionedPackage,%20kotlin.Int,%20android.content.IntentSender)` to indicate that the deletion is an archival. This flag is only for internal usage as part of `https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.html#requestArchive(kotlin.String,%20android.content.IntentSender)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#DONT_KILL_APP:kotlin.Int`

Flag parameter for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#setComponentEnabledSetting(android.content.ComponentName,%20kotlin.Int,%20kotlin.Int)` to indicate that you don't want to kill the app containing the component. Be careful when you set this since changing component states can make the containing application's behavior unpredictable.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#EXTRA_VERIFICATION_ID:kotlin.String`

Extra field name for the ID of a package pending verification. Passed to a package verifier and is used to call back to `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#verifyPendingInstall(kotlin.Int,%20kotlin.Int)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#EXTRA_VERIFICATION_RESULT:kotlin.String`

Extra field name for the result of a verification, either `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#VERIFICATION_ALLOW:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#VERIFICATION_REJECT:kotlin.Int`. Passed to package verifiers after a package is verified.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_ACTIVITIES_ON_SECONDARY_DISPLAYS:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports running activities on secondary displays. Displays here refers to both physical and virtual displays. Disabling this feature can impact support for application projection use-cases and support for virtual devices on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_APP_WIDGETS:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports app widgets.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_AUDIO_LOW_LATENCY:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device's audio pipeline is low-latency, more suitable for audio applications sensitive to delays or lag in sound input or output.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_AUDIO_OUTPUT:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device includes at least one form of audio output, as defined in the Android Compatibility Definition Document (CDD) [section 7.8 Audio](https://source.android.com/compatibility/android-cdd#7_8_audio).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_AUDIO_PRO:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device has professional audio level of functionality and performance.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_AUDIO_SPATIAL_HEADTRACKING_LOW_LATENCY:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature which indicates whether head tracking for spatial audio operates with low-latency, as defined by the CDD criteria for the feature.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_AUTOFILL:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports autofill of user credentials, addresses, credit cards, etc via integration with `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_AUTOMOTIVE:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: This is a device dedicated to showing UI on a vehicle headunit. A headunit here is defined to be inside a vehicle that may or may not be moving. A headunit uses either a primary display in the center console and/or additional displays in the instrument cluster or elsewhere in the vehicle. Headunit display(s) have limited size and resolution. The user will likely be focused on driving so limiting driver distraction is a primary concern. User input can be a variety of hard buttons, touch, rotary controllers and even mouse- like interfaces.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_BACKUP:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device can perform backup and restore operations on installed applications.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_BLUETOOTH:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device is capable of communicating with other devices via Bluetooth.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_BLUETOOTH_LE:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device is capable of communicating with other devices via Bluetooth Low Energy radio.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_BLUETOOTH_LE_CHANNEL_SOUNDING:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device is capable of ranging with other devices using channel sounding via Bluetooth Low Energy radio.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_CAMERA:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device has a camera facing away from the screen.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_CAMERA_ANY:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device has at least one camera pointing in some direction, or can support an external or a `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice.html#` camera being connected to it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_CAMERA_AR:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: At least one of the cameras on the device supports the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_MOTION_TRACKING:kotlin.Int` capability level.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_CAMERA_AUTOFOCUS:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device's camera supports auto-focus.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_CAMERA_CAPABILITY_MANUAL_POST_PROCESSING:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: At least one of the cameras on the device supports the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_MANUAL_POST_PROCESSING:kotlin.Int` capability level.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_CAMERA_CAPABILITY_MANUAL_SENSOR:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: At least one of the cameras on the device supports the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_MANUAL_SENSOR:kotlin.Int` capability level.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_CAMERA_CAPABILITY_RAW:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: At least one of the cameras on the device supports the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_RAW:kotlin.Int` capability level.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_CAMERA_CONCURRENT:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device's main front and back cameras can stream concurrently as described in `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.html#getConcurrentCameraIds()`.

<br />

While `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.html#getConcurrentCameraIds()` and associated APIs are only available on API level 30 or newer, this feature flag may be advertised by devices on API levels below 30. If present on such a device, the same guarantees hold: The main front and main back camera can be used at the same time, with guaranteed stream configurations as defined in the table for concurrent streaming at `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#createCaptureSession(android.hardware.camera2.params.SessionConfiguration)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_CAMERA_EXTERNAL:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device can support having an external camera connected to it. The external camera may not always be connected or available to applications to use.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_CAMERA_FLASH:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device's camera supports flash.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_CAMERA_FRONT:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device has a front facing camera.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_CAMERA_LEVEL_FULL:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: At least one of the cameras on the device supports the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` capability level.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_CANT_SAVE_STATE:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports the `https://developer.android.com/reference/kotlin/android/R.attr.html#cantSaveState:kotlin.Int` API.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports android.companion.CompanionDeviceManager#associate with devices via `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_CONNECTION_SERVICE:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The Connection Service API is enabled on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_CONSUMER_IR:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device is capable of communicating with consumer IR devices.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_CONTROLS:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports a system interface for the user to select and bind device control services provided by applications.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_CREDENTIALS:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports retrieval of user credentials, via integration with credential providers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_DEVICE_ADMIN:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports device policy enforcement via device admins.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_DEVICE_ID_ATTESTATION:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device has a KeyMint (or Keymaster) implementation that supports device ID attestation. See [the public documentation](https://source.android.com/docs/security/features/keystore/attestation#id-attestation) for more information about device ID attestation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_DEVICE_LOCK:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports locking (for example, by a financing provider in case of a missed payment).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_EMBEDDED:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: This is a device for IoT and may not have an UI. An embedded device is defined as a full stack Android device with or without a display and no user-installable apps.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_ETHERNET:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: This device supports ethernet.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_EXPANDED_PICTURE_IN_PICTURE:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports expanded picture-in-picture multi-window mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_FACE:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device has biometric hardware to perform face authentication.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_FAKETOUCH:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device does not have a touch screen, but does support touch emulation for basic events. For instance, the device might use a mouse or remote control to drive a cursor, and emulate basic touch pointer events like down, up, drag, etc. All devices that support android.hardware.touchscreen or a sub-feature are presumed to also support faketouch.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_FAKETOUCH_MULTITOUCH_DISTINCT:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device does not have a touch screen, but does support touch emulation for basic events that supports distinct tracking of two or more fingers. This is an extension of `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_FAKETOUCH:kotlin.String` for input devices with this capability. Note that unlike a distinct multitouch screen as defined by `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TOUCHSCREEN_MULTITOUCH_DISTINCT:kotlin.String`, these kinds of input devices will not actually provide full two-finger gestures since the input is being transformed to cursor movement on the screen. That is, single finger gestures will move a cursor; two-finger swipes will result in single-finger touch events; other two-finger gestures will result in the corresponding two-finger touch event.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_FAKETOUCH_MULTITOUCH_JAZZHAND:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device does not have a touch screen, but does support touch emulation for basic events that supports tracking a hand of fingers (5 or more fingers) fully independently. This is an extension of `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_FAKETOUCH:kotlin.String` for input devices with this capability. Note that unlike a multitouch screen as defined by `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TOUCHSCREEN_MULTITOUCH_JAZZHAND:kotlin.String`, not all two finger gestures can be detected due to the limitations described for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_FAKETOUCH_MULTITOUCH_DISTINCT:kotlin.String`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_FINGERPRINT:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device has biometric hardware to detect a fingerprint.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_FREEFORM_WINDOW_MANAGEMENT:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports freeform window management. Windows have title bars and can be moved and resized.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_GAMEPAD:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device has all of the inputs necessary to be considered a compatible game controller, or includes a compatible game controller in the box.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_HARDWARE_KEYSTORE:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String,%20kotlin.Int)`: If this feature is supported, the device implements the Android Keystore backed by an isolated execution environment. The version indicates which features are implemented in the isolated execution environment:

- 500: Hardware support for ML-DSA signature generation.
- 400: Inclusion of module information (via tag MODULE_HASH) in the attestation record.
- 300: Ability to include a second IMEI in the ID attestation record, see `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#ID_TYPE_IMEI:kotlin.Int`.
- 200: Hardware support for Curve 25519 (including both Ed25519 signature generation and X25519 key agreement).
- 100: Hardware support for ECDH (see `https://developer.android.com/reference/kotlin/javax/crypto/KeyAgreement.html#`) and support for app-generated attestation keys (see `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder.html#setAttestKeyAlias(kotlin.String)`).
- 41: Hardware enforcement of device-unlocked keys (see `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder.html#setUnlockedDeviceRequired(kotlin.Boolean)`).
- 40: Support for wrapped key import (see `https://developer.android.com/reference/kotlin/android/security/keystore/WrappedKeyEntry.html#`), optional support for ID attestation (see `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder.html#setDevicePropertiesAttestationIncluded(kotlin.Boolean)`), attestation (see `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder.html#setAttestationChallenge(kotlin.ByteArray)`), AES, HMAC, ECDSA and RSA support where the secret or private key never leaves secure hardware, and support for requiring user authentication before a key can be used.

This feature version is guaranteed to be set for all devices launching with Android 12 and may be set on devices launching with an earlier version. If the feature version is set, it will at least have the value 40. If it's not set the device may have a version of hardware-backed keystore but it may not support all features listed above.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_HIFI_SENSORS:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports high fidelity sensor processing capabilities.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_HOME_SCREEN:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports a home screen that is replaceable by third party applications.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_IDENTITY_CREDENTIAL_HARDWARE:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String,%20kotlin.Int)`: If this feature is supported, the device supports `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore.html#` implemented in secure hardware at the given feature version.

Known feature versions include:

- `202009`: corresponds to the features included in the Identity Credential API shipped in Android 11.
- `202101`: corresponds to the features included in the Identity Credential API shipped in Android 12.
- `202201`: corresponds to the features included in the Identity Credential API shipped in Android 13.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_IDENTITY_CREDENTIAL_HARDWARE_DIRECT_ACCESS:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String,%20kotlin.Int)`: If this feature is supported, the device supports `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore.html#` implemented in secure hardware with direct access at the given feature version. See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_IDENTITY_CREDENTIAL_HARDWARE:kotlin.String` for known feature versions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_INPUT_METHODS:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports adding new input methods implemented with the `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#` API.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_IPSEC_TUNNELS:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device has the requisite kernel support for multinetworking-capable IPsec tunnels.

This feature implies that the device supports XFRM Interfaces (CONFIG_XFRM_INTERFACE), or VTIs with kernel patches allowing updates of output/set mark via UPDSA.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_IPSEC_TUNNEL_MIGRATION:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device has the requisite kernel support for migrating IPsec tunnels to new source/destination addresses.

This feature implies that the device supports XFRM Migration (CONFIG_XFRM_MIGRATE) and has the kernel fixes to support cross-address-family IPsec tunnel migration

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_IRIS:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device has biometric hardware to perform iris authentication.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_KEYSTORE_APP_ATTEST_KEY:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device has a Keystore implementation that can create application-specific attestation keys. See `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder.html#setAttestKeyAlias(kotlin.String)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_KEYSTORE_LIMITED_USE_KEY:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device has a Keystore implementation that can enforce limited use key in hardware with any max usage count (including count equals to 1).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_KEYSTORE_SINGLE_USE_KEY:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device has a Keystore implementation that can only enforce limited use key in hardware with max usage count equals to 1.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_LEANBACK:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports leanback UI. This is typically used in a living room television experience, but is a software feature unlike `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEVISION:kotlin.String`. Devices running with this feature will use resources associated with the "television" UI mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_LEANBACK_ONLY:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports only leanback UI. Only applications designed for this experience should be run, though this is not enforced by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_LIVE_TV:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports live TV and can display contents from TV inputs implemented with the `https://developer.android.com/reference/kotlin/android/media/tv/TvInputService.html#` API.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_LIVE_WALLPAPER:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports live wallpapers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_LOCATION:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports one or more methods of reporting current location.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_LOCATION_GPS:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device has a Global Positioning System receiver and can report precise location.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_LOCATION_NETWORK:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device can report location with coarse accuracy using a network-based geolocation system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_MANAGED_USERS:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports creating secondary users and managed profiles via `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_MICROPHONE:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device can record audio via a microphone.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_MIDI:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device has a full implementation of the android.media.midi.\* APIs.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_NEURAL_PROCESSING_UNIT:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: This device has a NPU (Neural Processing Unit) or similar hardware for accelerating AI workloads.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_NFC:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device can communicate using Near-Field Communications (NFC), acting as a reader.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_NFC_BEAM:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The Beam API is enabled on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_NFC_HOST_CARD_EMULATION:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports host- based NFC card emulation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_NFC_HOST_CARD_EMULATION_NFCF:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports host- based NFC-F card emulation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_NFC_OFF_HOST_CARD_EMULATION_ESE:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports eSE- based NFC card emulation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_NFC_OFF_HOST_CARD_EMULATION_UICC:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports uicc- based NFC card emulation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_OPENGLES_DEQP_LEVEL:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String,%20kotlin.Int)`: If this feature is supported, the feature version specifies a date such that the device is known to pass the OpenGLES dEQP test suite associated with that date. The date is encoded as follows:

- Year in bits 31-16
- Month in bits 15-8
- Day in bits 7-0

<br />

Example: 2021-03-01 is encoded as 0x07E50301, and would indicate that the device passes the OpenGL ES dEQP test suite version that was current on 2021-03-01.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_OPENGLES_EXTENSION_PACK:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports the OpenGL ES [Android Extension Pack](http://www.khronos.org/registry/gles/extensions/ANDROID/ANDROID_extension_pack_es31a.txt).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_PC:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: This is a device dedicated to be primarily used with keyboard, mouse or touchpad. This includes traditional desktop computers, laptops and variants such as convertibles or detachables. Due to the larger screen, the device will most likely use the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_FREEFORM_WINDOW_MANAGEMENT:kotlin.String` feature as well.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_PICTURE_IN_PICTURE:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports picture-in-picture multi-window mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_PRINTING:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports printing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_RAM_LOW:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device's `https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#isLowRamDevice()` method returns true.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_RAM_NORMAL:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device's `https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#isLowRamDevice()` method returns false.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SCREEN_LANDSCAPE:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports landscape orientation screens. For backwards compatibility, you can assume that if neither this nor `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SCREEN_PORTRAIT:kotlin.String` is set then the device supports both portrait and landscape.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SCREEN_PORTRAIT:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports portrait orientation screens. For backwards compatibility, you can assume that if neither this nor `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SCREEN_LANDSCAPE:kotlin.String` is set then the device supports both portrait and landscape.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SECURELY_REMOVES_USERS:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports secure removal of users. When a user is deleted the data associated with that user is securely deleted and no longer available.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SECURE_LOCK_SCREEN:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device has a secure implementation of keyguard, meaning the device supports PIN, pattern and password as defined in Android CDD

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SECURITY_MODEL_COMPATIBLE:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device is compatible with Android's security model.

See sections 2 and 9 in the [Android CDD](https://source.android.com/compatibility/android-cdd) for more details.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SENSOR_ACCELEROMETER:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device includes an accelerometer.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SENSOR_ACCELEROMETER_LIMITED_AXES:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device includes a limited axes accelerometer.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SENSOR_ACCELEROMETER_LIMITED_AXES_UNCALIBRATED:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device includes an uncalibrated limited axes accelerometer.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SENSOR_AMBIENT_TEMPERATURE:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device includes an ambient temperature sensor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SENSOR_BAROMETER:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device includes a barometer (air pressure sensor.)

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SENSOR_COMPASS:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device includes a magnetometer (compass).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SENSOR_DYNAMIC_HEAD_TRACKER:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports exposing head tracker sensors from peripheral devices via the dynamic sensors API.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SENSOR_GYROSCOPE:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device includes a gyroscope.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SENSOR_GYROSCOPE_LIMITED_AXES:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device includes a limited axes gyroscope.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SENSOR_GYROSCOPE_LIMITED_AXES_UNCALIBRATED:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device includes an uncalibrated limited axes gyroscope.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SENSOR_HEADING:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device includes a heading sensor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SENSOR_HEART_RATE:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device includes a heart rate monitor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SENSOR_HEART_RATE_ECG:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The heart rate sensor on this device is an Electrocardiogram.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SENSOR_HINGE_ANGLE:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device includes a hinge angle sensor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SENSOR_LIGHT:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device includes a light sensor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SENSOR_PROXIMITY:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device includes a proximity sensor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SENSOR_RELATIVE_HUMIDITY:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device includes a relative humidity sensor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SENSOR_STEP_COUNTER:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device includes a hardware step counter.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SENSOR_STEP_DETECTOR:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device includes a hardware step detector.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SE_OMAPI_ESE:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports Open Mobile API capable eSE-based secure elements.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SE_OMAPI_SD:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports Open Mobile API capable SD-based secure elements.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SE_OMAPI_UICC:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports Open Mobile API capable UICC-based secure elements.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SIP:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The SIP API is enabled on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SIP_VOIP:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports SIP-based VOIP.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_STRONGBOX_KEYSTORE:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()`, `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)`, and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String,%20kotlin.Int)`: If this feature is supported, the device implements the Android Keystore backed by a dedicated secure processor referred to as [StrongBox](https://source.android.com/security/best-practices/hardware#strongbox-keymaster). If this feature has a version, the version number indicates which features are implemented in StrongBox:

- 400: Inclusion of module information (via tag MODULE_HASH) in the attestation record.
- 300: Ability to include a second IMEI in the ID attestation record, see `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#ID_TYPE_IMEI:kotlin.Int`.
- 200: No new features for StrongBox (the Android Keystore environment backed by an isolated execution environment has gained support for Curve 25519 in this version, but the implementation backed by a dedicated secure processor is not expected to implement it).
- 100: Hardware support for ECDH (see `https://developer.android.com/reference/kotlin/javax/crypto/KeyAgreement.html#`) and support for app-generated attestation keys (see `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder.html#setAttestKeyAlias(kotlin.String)`).
- 41: Hardware enforcement of device-unlocked keys (see `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder.html#setUnlockedDeviceRequired(kotlin.Boolean)`).
- 40: Support for wrapped key import (see `https://developer.android.com/reference/kotlin/android/security/keystore/WrappedKeyEntry.html#`), optional support for ID attestation (see `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder.html#setDevicePropertiesAttestationIncluded(kotlin.Boolean)`), attestation (see `https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder.html#setAttestationChallenge(kotlin.ByteArray)`), AES, HMAC, ECDSA and RSA support where the secret or private key never leaves secure hardware, and support for requiring user authentication before a key can be used.

If a device has StrongBox, this feature version number is guaranteed to be set for all devices launching with Android 12 and may be set on devices launching with an earlier version. If the feature version is set, it will at least have the value 40. If it's not set the device may have StrongBox but it may not support all features listed above.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELECOM:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports Telecom Service APIs.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device has a telephony radio with data communication support.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CALLING:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports Telephony APIs for calling service.

This feature should only be defined if `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`, and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELECOM:kotlin.String` have been defined.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_CDMA:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device has a CDMA telephony stack.

This feature should only be defined if `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY:kotlin.String` has been defined.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports Telephony APIs for data service.

This feature should only be defined if both `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` have been defined.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports embedded subscriptions on eUICCs. This feature should only be defined if `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` has been defined.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC_MEP:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports multiple enabled profiles on eUICCs.

Devices declaring this feature must have an implementation of the `https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo.html#getPorts()`, `https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo.html#isMultipleEnabledProfilesSupported()` and android.telephony.euicc.EuiccManager#switchToSubscription. This feature should only be defined if `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC:kotlin.String` have been defined.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_GSM:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device has a GSM telephony stack.

This feature should only be defined if `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY:kotlin.String` has been defined.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_IMS:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports attaching to IMS implementations using the ImsService API in telephony.

This feature should only be defined if `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_DATA:kotlin.String` has been defined.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MBMS:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports cell-broadcast reception using the MBMS APIs.

This feature should only be defined if both `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` have been defined.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_MESSAGING:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports Telephony APIs for SMS and MMS.

This feature should only be defined if both `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` have been defined.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports Telephony APIs for the radio access.

This feature should only be defined if `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY:kotlin.String` has been defined.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports Telephony APIs for the subscription.

This feature should only be defined if `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY:kotlin.String` has been defined.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEVISION:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: This is a device dedicated to showing UI on a television. Television here is defined to be a typical living room television experience: displayed on a big screen, where the user is sitting far away from it, and the dominant form of input will be something like a DPAD, not through touch or mouse.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_THREAD_NETWORK:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device is capable of communicating with other devices via [Thread](https://www.threadgroup.org) networking protocol.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TOUCHSCREEN:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device's display has a touch screen.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TOUCHSCREEN_MULTITOUCH:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device's touch screen supports multitouch sufficient for basic two-finger gesture detection.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TOUCHSCREEN_MULTITOUCH_DISTINCT:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device's touch screen is capable of tracking two or more fingers fully independently.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TOUCHSCREEN_MULTITOUCH_JAZZHAND:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device's touch screen is capable of tracking a full hand of fingers fully independently -- that is, 5 or more simultaneous independent pointers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_USB_ACCESSORY:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports connecting to USB accessories.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_USB_HOST:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports connecting to USB devices as the USB host.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_UWB:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device is capable of communicating with other devices via ultra wideband.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_VERIFIED_BOOT:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports verified boot.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_VR_HEADTRACKING:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device implements headtracking suitable for a VR device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_VR_MODE:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device implements an optimized mode for virtual reality (VR) applications that handles stereoscopic rendering of notifications, and disables most monocular system UI components while a VR application has user focus. Devices declaring this feature must include an application implementing a `https://developer.android.com/reference/kotlin/android/service/vr/VrListenerService.html#` that can be targeted by VR applications via `https://developer.android.com/reference/kotlin/android/app/Activity.html#setVrModeEnabled(kotlin.Boolean,%20android.content.ComponentName)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_VR_MODE_HIGH_PERFORMANCE:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device implements an optimized mode for virtual reality (VR) applications that handles stereoscopic rendering of notifications, disables most monocular system UI components while a VR application has user focus and meets extra CDD requirements to provide a high-quality VR experience. Devices declaring this feature must include an application implementing a `https://developer.android.com/reference/kotlin/android/service/vr/VrListenerService.html#` that can be targeted by VR applications via `https://developer.android.com/reference/kotlin/android/app/Activity.html#setVrModeEnabled(kotlin.Boolean,%20android.content.ComponentName)`. and must meet CDD requirements to provide a high-quality VR experience.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_VULKAN_DEQP_LEVEL:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String,%20kotlin.Int)`: If this feature is supported, the feature version specifies a date such that the device is known to pass the Vulkan dEQP test suite associated with that date. The date is encoded as follows:

- Year in bits 31-16
- Month in bits 15-8
- Day in bits 7-0

<br />

Example: 2019-03-01 is encoded as 0x07E30301, and would indicate that the device passes the Vulkan dEQP test suite version that was current on 2019-03-01.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_VULKAN_HARDWARE_COMPUTE:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String,%20kotlin.Int)`: If this feature is supported, the Vulkan implementation on this device is hardware accelerated, and the Vulkan native API will enumerate at least one `VkPhysicalDevice`, and the feature version will indicate what level of optional compute features that device supports beyond the Vulkan 1.0 requirements.

Compute level 0 indicates:

- The `VK_KHR_variable_pointers` extension and `VkPhysicalDeviceVariablePointerFeaturesKHR::variablePointers` feature are supported.
- `VkPhysicalDeviceLimits::maxPerStageDescriptorStorageBuffers` is at least 16.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_VULKAN_HARDWARE_LEVEL:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String,%20kotlin.Int)`: If this feature is supported, the Vulkan implementation on this device is hardware accelerated, and the Vulkan native API will enumerate at least one `VkPhysicalDevice`, and the feature version will indicate what level of optional hardware features limits it supports.

Level 0 includes the base Vulkan requirements as well as:

- `VkPhysicalDeviceFeatures::textureCompressionETC2`

Level 1 additionally includes:

- `VkPhysicalDeviceFeatures::fullDrawIndexUint32`
- `VkPhysicalDeviceFeatures::imageCubeArray`
- `VkPhysicalDeviceFeatures::independentBlend`
- `VkPhysicalDeviceFeatures::geometryShader`
- `VkPhysicalDeviceFeatures::tessellationShader`
- `VkPhysicalDeviceFeatures::sampleRateShading`
- `VkPhysicalDeviceFeatures::textureCompressionASTC_LDR`
- `VkPhysicalDeviceFeatures::fragmentStoresAndAtomics`
- `VkPhysicalDeviceFeatures::shaderImageGatherExtended`
- `VkPhysicalDeviceFeatures::shaderUniformBufferArrayDynamicIndexing`
- `VkPhysicalDeviceFeatures::shaderSampledImageArrayDynamicIndexing`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_VULKAN_HARDWARE_VERSION:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String,%20kotlin.Int)`: If this feature is supported, the Vulkan implementation on this device is hardware accelerated, and the feature version will indicate the highest `VkPhysicalDeviceProperties::apiVersion` supported by the physical devices that support the hardware level indicated by `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_VULKAN_HARDWARE_LEVEL:kotlin.String`. The feature version uses the same encoding as Vulkan version numbers:

- Major version number in bits 31-22
- Minor version number in bits 21-12
- Patch version number in bits 11-0

A version of 1.1.0 or higher also indicates:

<!-- -->

- The `VK_ANDROID_external_memory_android_hardware_buffer` extension is supported.
- `SYNC_FD` external semaphore and fence handles are supported.
- `VkPhysicalDeviceSamplerYcbcrConversionFeatures::samplerYcbcrConversion` is supported.

A subset of devices that support Vulkan 1.1 do so via software emulation. For more information, see [Vulkan Design Guidelines](https://developer.android.com/ndk/guides/graphics/design-notes).

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_WALLET_LOCATION_BASED_SUGGESTIONS:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports showing location-based suggestions for wallet cards provided by the default payment app.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_WATCH:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: This is a device dedicated to showing UI on a watch. A watch here is defined to be a device worn on the body, perhaps on the wrist. The user is very close when interacting with the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_WEBVIEW:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device has a full implementation of the android.webkit.\* APIs. Devices lacking this feature will not have a functioning WebView implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_WIFI:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports WiFi (802.11) networking.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_WIFI_AWARE:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports Wi-Fi Aware.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_WIFI_DIRECT:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports Wi-Fi Direct networking.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_WIFI_PASSPOINT:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports Wi-Fi Passpoint and all Passpoint related APIs in `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#` are supported. Refer to `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#addOrUpdatePasspointConfiguration(android.net.wifi.hotspot2.PasspointConfiguration)` for more info.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_WIFI_RTT:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports Wi-Fi RTT (IEEE 802.11mc).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_WINDOW_MAGNIFICATION:kotlin.String`

Feature for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()` and #hasSystemFeature: The device supports window magnification.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_INSTALLER:kotlin.Int`

Permission whitelist flag: permissions whitelisted by the installer. Permissions can also be whitelisted by the system, on upgrade, or on role grant.

**Note:**In retrospect it would have been preferred to use more inclusive terminology when naming this API. Similar APIs added will refrain from using the term "whitelist".

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_SYSTEM:kotlin.Int`

Permission whitelist flag: permissions whitelisted by the system. Permissions can also be whitelisted by the installer, on upgrade, or on role grant.

**Note:**In retrospect it would have been preferred to use more inclusive terminology when naming this API. Similar APIs added will refrain from using the term "whitelist".

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_UPGRADE:kotlin.Int`

Permission whitelist flag: permissions whitelisted by the system when upgrading from an OS version where the permission was not restricted to an OS version where the permission is restricted. Permissions can also be whitelisted by the installer, the system, or on role grant.

**Note:**In retrospect it would have been preferred to use more inclusive terminology when naming this API. Similar APIs added will refrain from using the term "whitelist".

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_ACTIVITIES:kotlin.Int`

`https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#` flag: return information about activities in the package in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#activities:kotlin.Array`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_APP_LOCK_INFO:kotlin.Long`

`https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#`, `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo.html#`, and `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#` flag: return the `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#isAppLockSupported:kotlin.Boolean` and `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#isAppLockEnabled:kotlin.Boolean` associated with an application.

The caller should have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#LOCK_APPS:kotlin.String` permission, or a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown. This flag cannot be used with `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_ATTRIBUTIONS:kotlin.Int`, if the caller wishes to retrieve attributions, they must use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_ATTRIBUTIONS_LONG:kotlin.Long`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_ATTRIBUTIONS:kotlin.Int`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_ATTRIBUTIONS_LONG:kotlin.Long`

`https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#` flag: return all attributions declared in the package manifest

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_CONFIGURATIONS:kotlin.Int`

`https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#` flag: return information about hardware preferences in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#configPreferences:kotlin.Array`, and requested features in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#reqFeatures:kotlin.Array` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#featureGroups:kotlin.Array`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_DISABLED_COMPONENTS:kotlin.Int`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_DISABLED_UNTIL_USED_COMPONENTS:kotlin.Int`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_GIDS:kotlin.Int`

`https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#` flag: return the `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#gids:kotlin.IntArray` that are associated with an application. This applies for any API returning a PackageInfo class, either directly or nested inside of another.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_INSTRUMENTATION:kotlin.Int`

`https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#` flag: return information about instrumentation in the package in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#instrumentation:kotlin.Array`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_INTENT_FILTERS:kotlin.Int`

`https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#` flag: return information about the intent filters supported by the activity.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_META_DATA:kotlin.Int`

`https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo.html#` flag: return the `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo.html#metaData:android.os.Bundle` data `https://developer.android.com/reference/kotlin/android/os/Bundle.html#`s that are associated with a component. This applies for any API returning a ComponentInfo subclass.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_PERMISSIONS:kotlin.Int`

`https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#` flag: return information about permissions in the package in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#permissions:kotlin.Array`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_PROVIDERS:kotlin.Int`

`https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#` flag: return information about content providers in the package in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#providers:kotlin.Array`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_RECEIVERS:kotlin.Int`

`https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#` flag: return information about intent receivers in the package in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#receivers:kotlin.Array`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_RESOLVED_FILTER:kotlin.Int`

`https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#` flag: return the IntentFilter that was matched for a particular ResolveInfo in `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#filter:android.content.IntentFilter`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_SERVICES:kotlin.Int`

`https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#` flag: return information about services in the package in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#services:kotlin.Array`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_SHARED_LIBRARY_FILES:kotlin.Int`

`https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#` flag: return the `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#sharedLibraryFiles:kotlin.Array` that are associated with an application. This applies for any API returning an ApplicationInfo class, either directly or nested inside of another.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_SIGNATURES:kotlin.Int`

`https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#` flag: return information about the signatures included in the package.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_SIGNING_CERTIFICATES:kotlin.Int`

`https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#` flag: return the signing certificates associated with this package. Each entry is a signing certificate that the package has proven it is authorized to use, usually a past signing certificate from which it has rotated.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_UNINSTALLED_PACKAGES:kotlin.Int`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_URI_PERMISSION_PATTERNS:kotlin.Int`

`https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo.html#` flag: return the `https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo.html#uriPermissionPatterns:kotlin.Array` that are associated with a content provider. This applies for any API returning a ProviderInfo class, either directly or nested inside of another.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#INSTALL_REASON_DEVICE_RESTORE:kotlin.Int`

Code indicating that this package was installed as part of restoring from another device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#INSTALL_REASON_DEVICE_SETUP:kotlin.Int`

Code indicating that this package was installed as part of device setup.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#INSTALL_REASON_POLICY:kotlin.Int`

Code indicating that this package was installed due to enterprise policy.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#INSTALL_REASON_UNKNOWN:kotlin.Int`

Code indicating that the reason for installing this package is unknown.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#INSTALL_REASON_USER:kotlin.Int`

Code indicating that the package installation was initiated by the user.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#INSTALL_SCENARIO_BULK:kotlin.Int`

Installation scenario indicating a bulk operation with the desired result of a fully optimized application. If the system is busy or resources are scarce the system will perform less work to avoid impacting system health. Examples of bulk installation scenarios might include device restore, background updates of multiple applications, or user-triggered updates for all applications. The decision to use BULK or BULK_SECONDARY should be based on the desired user experience. BULK_SECONDARY operations may take less time to complete but, when they do, will produce less optimized applications. The device state (e.g. memory usage or battery status) should not be considered when making this decision as those factors are taken into account by the Package Manager when acting on the installation scenario.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#INSTALL_SCENARIO_BULK_SECONDARY:kotlin.Int`

Installation scenario indicating a bulk operation that prioritizes minimal system health impact over application optimization. The application may undergo additional optimization if the system is idle and system resources are abundant. The more elements of a bulk operation that are marked BULK_SECONDARY, the faster the entire bulk operation will be. See the comments for INSTALL_SCENARIO_BULK for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#INSTALL_SCENARIO_DEFAULT:kotlin.Int`

A value to indicate the lack of CUJ information, disabling all installation scenario logic.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#INSTALL_SCENARIO_FAST:kotlin.Int`

Installation scenario providing the fastest "install button to launch" experience possible.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_ALL:kotlin.Int`

Querying flag: if set and if the platform is doing any filtering of the results, then the filtering will not happen. This is a synonym for saying that all results should be returned.

*This flag should be used with extreme care.*

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_APEX:kotlin.Int`

`https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#` flag: include APEX packages that are currently installed. In APEX terminology, this corresponds to packages that are currently active, i.e. mounted and available to other processes of the OS. In particular, this flag alone will not match APEX files that are staged for activation at next reboot.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_ARCHIVED_PACKAGES:kotlin.Long`

Flag parameter to also retrieve some information about archived packages. Packages can be archived through `https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.html#requestArchive(kotlin.String,%20android.content.IntentSender)` and do not have any APKs stored on the device, but do keep the data directory.

Note: Archived apps are a subset of apps returned by `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_UNINSTALLED_PACKAGES:kotlin.Int`.

Note: this flag may cause less information about currently installed applications to be returned.

Note: use of this flag requires the android.permission.QUERY_ALL_PACKAGES permission to see uninstalled packages.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DEFAULT_ONLY:kotlin.Int`

Resolution and querying flag: if set, only filters that support the `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_DEFAULT:kotlin.String` will be considered for matching. This is a synonym for including the CATEGORY_DEFAULT in your supplied Intent.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DIRECT_BOOT_AUTO:kotlin.Int`

Querying flag: automatically match components based on their Direct Boot awareness and the current user state.

Since the default behavior is to automatically apply the current user state, this is effectively a sentinel value that doesn't change the output of any queries based on its presence or absence.

Instead, this value can be useful in conjunction with `https://developer.android.com/reference/kotlin/android/os/StrictMode.VmPolicy.Builder.html#detectImplicitDirectBoot()` to detect when a caller is relying on implicit automatic matching, instead of confirming the explicit behavior they want, using a combination of these flags:

- `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DIRECT_BOOT_AWARE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DIRECT_BOOT_UNAWARE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DIRECT_BOOT_AUTO:kotlin.Int`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DIRECT_BOOT_AWARE:kotlin.Int`

Querying flag: match components which are direct boot *aware* in the returned info, regardless of the current user state.

When neither `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DIRECT_BOOT_AWARE:kotlin.Int` nor `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DIRECT_BOOT_UNAWARE:kotlin.Int` are specified, the default behavior is to match only runnable components based on the user state. For example, when a user is started but credentials have not been presented yet, the user is running "locked" and only `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DIRECT_BOOT_AWARE:kotlin.Int` components are returned. Once the user credentials have been presented, the user is running "unlocked" and both `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DIRECT_BOOT_AWARE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DIRECT_BOOT_UNAWARE:kotlin.Int` components are returned.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DIRECT_BOOT_UNAWARE:kotlin.Int`

Querying flag: match components which are direct boot *unaware* in the returned info, regardless of the current user state.

When neither `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DIRECT_BOOT_AWARE:kotlin.Int` nor `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DIRECT_BOOT_UNAWARE:kotlin.Int` are specified, the default behavior is to match only runnable components based on the user state. For example, when a user is started but credentials have not been presented yet, the user is running "locked" and only `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DIRECT_BOOT_AWARE:kotlin.Int` components are returned. Once the user credentials have been presented, the user is running "unlocked" and both `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DIRECT_BOOT_AWARE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DIRECT_BOOT_UNAWARE:kotlin.Int` components are returned.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DISABLED_COMPONENTS:kotlin.Int`

`https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#` flag: include disabled components in the returned info.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DISABLED_UNTIL_USED_COMPONENTS:kotlin.Int`

`https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#` flag: include disabled components which are in that state only because of `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_DISABLED_UNTIL_USED:kotlin.Int` in the returned info. Note that if you set this flag, applications that are in this disabled state will be reported as enabled.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_SYSTEM_ONLY:kotlin.Int`

Querying flag: include only components from applications that are marked with `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#FLAG_SYSTEM:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_UNINSTALLED_PACKAGES:kotlin.Int`

Flag parameter to retrieve some information about all applications (even uninstalled ones) which have data directories. This state could have resulted if applications have been deleted with flag `DELETE_KEEP_DATA` with a possibility of being replaced or reinstalled in future.

Note: this flag may cause less information about currently installed applications to be returned.

Note: use of this flag requires the android.permission.QUERY_ALL_PACKAGES permission to see uninstalled packages.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MAXIMUM_VERIFICATION_TIMEOUT:kotlin.Long`

Can be used as the `millisecondsToDelay` argument for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#extendVerificationTimeout(kotlin.Int,%20kotlin.Int,%20kotlin.Long)`. This is the maximum time `PackageManager` waits for the verification agent to return (in milliseconds).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PERMISSION_DENIED:kotlin.Int`

Permission check result: this is returned by `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#checkPermission(kotlin.String,%20kotlin.String)` if the permission has not been granted to the given package.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PERMISSION_GRANTED:kotlin.Int`

Permission check result: this is returned by `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#checkPermission(kotlin.String,%20kotlin.String)` if the permission has been granted to the given package.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PROPERTY_COMPAT_OVERRIDE_LANDSCAPE_TO_PORTRAIT:kotlin.String`

Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` for an app to inform the system that the app can be opted-in or opted-out from the compatibility treatment that rotates camera output by 90 degrees on landscape sensors on devices known to have compatibility issues.

The treatment is disabled by default but device manufacturers can enable the treatment using their discretion to improve camera compatibility. With this property set to `false`, the rotation will not be applied. A value of `true` will ensure that rotation is applied, provided it is enabled for the device. In most cases, if rotation is the desired behavior this property need not be set. However, if your app experiences stretching or incorrect rotation on these devices, explicitly setting this to `true` may resolve that behavior. Apps should set this to `false` if there is confidence that the app handles `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SENSOR_ORIENTATION:android.hardware.camera2.CameraCharacteristics.Key` correctly. See [the documentation for best practice.](https://developer.android.com/training/camera2/camera-preview)

**Syntax:**

```kotlin
<application>
    <property
      android:name="android.camera.PROPERTY_COMPAT_OVERRIDE_LANDSCAPE_TO_PORTRAIT"
      android:value="true|false"/>
  </application>
  
```

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PROPERTY_MEDIA_CAPABILITIES:kotlin.String`

\<application\> level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` tag specifying the XML resource ID containing an application's media capabilities XML file For example: \<application\> \<property android:name="android.media.PROPERTY_MEDIA_CAPABILITIES" android:resource="@xml/media_capabilities"\> \<application\>

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PROPERTY_NATIVE_SERVICE_FUNCTION_NAME:kotlin.String`

Service level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` tag for native services specifying the symbol name of the entry point function for the service. If not specified, the system executes `ANativeService_onCreate`.

Example:

```kotlin
<service android:isolatedProcess="true"
                    android:nativeService="true">
    <property
      android:name="android.app.PROPERTY_NATIVE_SERVICE_FUNCTION_NAME"
      android:value="native_service_createService"/>
  </service>
  
```

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PROPERTY_NATIVE_SERVICE_LIBRARY_NAME:kotlin.String`

Service level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` tag for native services specifying the name of the library to be loaded to the process that hosts the service. If not specified, the system tries to load `libmain.so`.

Example:

```kotlin
<service android:isolatedProcess="true"
                    android:nativeService="true">
    <property
      android:name="android.app.PROPERTY_NATIVE_SERVICE_LIBRARY_NAME"
      android:value="libnativeservice.so"/>
  </service>
  
```

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PROPERTY_SELF_CERTIFIED_NETWORK_CAPABILITIES:kotlin.String`

\<application\> level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` tag specifying the XML resource ID containing the declaration of the self-certified network capabilities used by the application.

Starting from Android 14, usage of some network capabilities in android.net.ConnectivityManager#requestNetwork require the application to declare its usage of that particular capability in this resource. Only some capabilities require a declaration. Please look up the specific capability you want to use in `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#` to see if it needs declaration in this property. For example: \<application\> \<property android:name="android.net.PROPERTY_SELF_CERTIFIED_NETWORK_CAPABILITIES" android:resource="@xml/self_certified_network_capabilities"\> \<application\>

The detail format of self_certified_network_capabilities.xml is described in `https://developer.android.com/reference/kotlin/android/net/NetworkRequest.html#`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PROPERTY_SPECIAL_USE_FGS_SUBTYPE:kotlin.String`

\<service\> level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` tag specifying the actual use case of the service if it's foreground service with the type `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_SPECIAL_USE:kotlin.Int`.

For example: \<service\> \<property android:name="android.app.PROPERTY_SPECIAL_USE_FGS_SUBTYPE" android:value="foo"/\> \</service\>

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PROPERTY_USE_RESTRICTED_BACKUP_MODE:kotlin.String`

\<application\> level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` tag specifying whether the app should be put into the "restricted" backup mode when it's started for backup and restore operations.

See [for information about restricted mode](https://developer.android.com/identity/data/autobackup#ImplementingBackupAgent).

Starting with Android 16 apps may not be started in restricted mode based on this property.

**Syntax:**

```kotlin
<application>
    <property
      android:name="android.app.backup.PROPERTY_USE_RESTRICTED_BACKUP_MODE"
      android:value="true|false"/>
  </application>
  
```

If this property is set, the operating system will respect it for now (see Note below). If it's not set, the behavior depends on the SDK level that the app is targeting. For apps targeting SDK level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int` or lower, the property defaults to `true`. For apps targeting SDK level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int` or higher, the operating system will make a decision dynamically.

Note: It's not recommended to set this property to `true` unless absolutely necessary. In a future Android version, this property may be deprecated in favor of removing restricted mode completely.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_FIRST_NOT_SIGNED:kotlin.Int`

Signature check result: this is returned by #checkSignatures if the first package is not signed but the second is.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_MATCH:kotlin.Int`

Signature check result: this is returned by #checkSignatures if all signatures on the two packages match.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_NEITHER_SIGNED:kotlin.Int`

Signature check result: this is returned by #checkSignatures if neither of the two packages is signed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_NO_MATCH:kotlin.Int`

Signature check result: this is returned by #checkSignatures if not all signatures on both packages match.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_SECOND_NOT_SIGNED:kotlin.Int`

Signature check result: this is returned by #checkSignatures if the second package is not signed but the first is.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_UNKNOWN_PACKAGE:kotlin.Int`

Signature check result: this is returned by #checkSignatures if either of the packages are not valid.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SYNCHRONOUS:kotlin.Int`

Flag parameter for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#setComponentEnabledSetting(android.content.ComponentName,%20kotlin.Int,%20kotlin.Int)` to indicate that the given user's package restrictions state will be serialised to disk after the component state has been updated. Note that this is synchronous disk access, so calls using this flag should be run on a background thread.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#VERIFICATION_ALLOW:kotlin.Int`

Used as the `verificationCode` argument for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#verifyPendingInstall(kotlin.Int,%20kotlin.Int)` to indicate that the calling package verifier allows the installation to proceed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#VERIFICATION_REJECT:kotlin.Int`

Used as the `verificationCode` argument for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#verifyPendingInstall(kotlin.Int,%20kotlin.Int)` to indicate the calling package verifier does not vote to allow the installation to proceed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#VERSION_CODE_HIGHEST:kotlin.Int`

Constant for specifying the highest installed package version code.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#MockPackageManager()()` <br /> |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#addPackageToPreferred(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#addPermission(android.content.pm.PermissionInfo)(info: https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#)` Add a new dynamic permission to the system. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#addPermissionAsync(android.content.pm.PermissionInfo)(info: https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#)` Like `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#addPermission(android.content.pm.PermissionInfo)` but asynchronously persists the package manager state after returning from the call, allowing it to return quicker and batch a series of adds at the expense of no guarantee the added permission will be retained if the device is rebooted before it is written. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#addPreferredActivity(android.content.IntentFilter,%20kotlin.Int,%20kotlin.Array,%20android.content.ComponentName)(filter: https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#, match: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, set: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!>?, activity: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)` Add a new preferred activity mapping to the system. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#addWhitelistedRestrictedPermission(kotlin.String,%20kotlin.String,%20kotlin.Int)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, whitelistFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Adds a whitelisted restricted permission for an app. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#canRequestPackageInstalls()()` Checks whether the calling package is allowed to request package installs through package installer. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#canonicalToCurrentPackageNames(kotlin.Array)(names: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)` Map from a packages canonical name to the current name in use on the device. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#checkPermission(kotlin.String,%20kotlin.String)(permName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, pkgName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Check whether a particular package has been granted a particular permission. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#checkSignatures(kotlin.Int,%20kotlin.Int)(uid1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Like `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#checkSignatures(kotlin.String,%20kotlin.String)`, but takes UIDs of the two packages to be checked. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#checkSignatures(kotlin.String,%20kotlin.String)(pkg1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, pkg2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Compare the signatures of two packages to determine if the same signature appears in both of them. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#clearInstantAppCookie()()` Clears the instant application cookie for the calling app. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#clearPackagePreferredActivities(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Remove all preferred activity mappings, previously added with `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#addPreferredActivity(android.content.IntentFilter,%20kotlin.Int,%20kotlin.Array,%20android.content.ComponentName)`, from the system whose activities are implemented in the given package name. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#currentToCanonicalPackageNames(kotlin.Array)(names: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)` Map from the current package names in use on the device to whatever the current canonical name of that package is. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#extendVerificationTimeout(kotlin.Int,%20kotlin.Int,%20kotlin.Long)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, verificationCodeAtTimeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, millisecondsToDelay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Allows a package listening to the `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_NEEDS_VERIFICATION:kotlin.String` to extend the default timeout for a response and declare what action to perform after the timeout occurs. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getActivityBanner(android.content.ComponentName)(activityName: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)` Retrieve the banner associated with an activity. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getActivityBanner(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#)` Retrieve the banner associated with an Intent. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getActivityIcon(android.content.ComponentName)(activityName: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)` Retrieve the icon associated with an activity. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getActivityIcon(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#)` Retrieve the icon associated with an Intent. |
| open [ActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getActivityInfo(android.content.ComponentName,%20kotlin.Int)(className: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve all of the information we know about a particular activity class. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getActivityLogo(android.content.ComponentName)(activityName: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)` Retrieve the logo associated with an activity. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getActivityLogo(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#)` Retrieve the logo associated with an Intent. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [IntentFilter](https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#)!\>! | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getAllIntentFilters(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` <br /> |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PermissionGroupInfo](https://developer.android.com/reference/kotlin/android/content/pm/PermissionGroupInfo.html#)!\> | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getAllPermissionGroups(kotlin.Int)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve all of the known permission groups in the system. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getApplicationBanner(android.content.pm.ApplicationInfo)(info: https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#)` Retrieve the banner associated with an application. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getApplicationBanner(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieve the banner associated with an application. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getApplicationEnabledSetting(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Return the enabled setting for an application. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getApplicationIcon(android.content.pm.ApplicationInfo)(info: https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#)` Retrieve the icon associated with an application. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getApplicationIcon(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieve the icon associated with an application. |
| open [ApplicationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getApplicationInfo(kotlin.String,%20kotlin.Int)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve all of the information we know about a particular package/application. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getApplicationLabel(android.content.pm.ApplicationInfo)(info: https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#)` Return the label to use for this application. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getApplicationLogo(android.content.pm.ApplicationInfo)(info: https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#)` Retrieve the logo associated with an application. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getApplicationLogo(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieve the logo associated with an application. |
| open [ChangedPackages](https://developer.android.com/reference/kotlin/android/content/pm/ChangedPackages.html#)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getChangedPackages(kotlin.Int)(sequenceNumber: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the names of the packages that have been changed \[eg. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getComponentEnabledSetting(android.content.ComponentName)(componentName: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)` Return the enabled setting for a package component (activity, receiver, service, provider). |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getDefaultActivityIcon()()` Return the generic icon for an activity that is used when no specific icon is defined. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getDrawable(kotlin.String,%20kotlin.Int,%20android.content.pm.ApplicationInfo)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, resid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, appInfo: https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#?)` Retrieve an image from a package. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ApplicationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#)!\> | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getInstalledApplications(kotlin.Int)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return a List of all application packages that are installed for the current user. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#)!\> | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getInstalledPackages(kotlin.Int)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return a List of all packages that are installed for the current user. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getInstallerPackageName(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieve the package name of the application that installed a package. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getInstantAppCookie()()` Gets the instant application cookie for this app. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getInstantAppCookieMaxBytes()()` Gets the maximum size in bytes of the cookie data an instant app can store on the device. |
| open [InstrumentationInfo](https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo.html#) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getInstrumentationInfo(android.content.ComponentName,%20kotlin.Int)(className: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve all of the information we know about a particular instrumentation class. |
| open [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getLaunchIntentForPackage(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns a "good" intent to launch a front-door activity in a package. |
| open [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getLeanbackLaunchIntentForPackage(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Return a "good" intent to launch a front-door Leanback activity in a package, for use for example to implement an "open" button when browsing through packages. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MemoryBudgetInfo](https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo.html#)!\> | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getMemoryBudgets(android.content.pm.ApplicationInfo)(info: https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#)` Return the memory budgets for the application described by the given `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getNameForUid(kotlin.Int)(uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve the official name associated with a uid. |
| open [PackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getPackageArchiveInfo(kotlin.String,%20kotlin.Int)(archiveFilePath: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve overall information about an application package defined in a package archive file Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPackageArchiveInfo(kotlin.String,%20android.content.pm.PackageManager.PackageInfoFlags)` when long flags are needed. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getPackageGids(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Return an array of all of the POSIX secondary group IDs that have been assigned to the given package. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getPackageGids(kotlin.String,%20kotlin.Int)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return an array of all of the POSIX secondary group IDs that have been assigned to the given package. |
| open [PackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#)! | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getPackageInfo(android.content.pm.VersionedPackage,%20kotlin.Int)(versionedPackage: https://developer.android.com/reference/kotlin/android/content/pm/VersionedPackage.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve overall information about an application package that is installed on the system. |
| open [PackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#)! | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getPackageInfo(kotlin.String,%20kotlin.Int)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve overall information about an application package that is installed on the system. |
| open [PackageInstaller](https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.html#) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getPackageInstaller()()` Return interface that offers the ability to install, upgrade, and remove applications on the device. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getPackageUid(kotlin.String,%20kotlin.Int)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the UID associated with the given package name. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getPackagesForUid(kotlin.Int)(uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve the names of all packages that are associated with a particular user id. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#)!\> | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getPackagesHoldingPermissions(kotlin.Array,%20kotlin.Int)(permissions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return a List of all installed packages that are currently holding any of the given permissions. |
| open [PermissionGroupInfo](https://developer.android.com/reference/kotlin/android/content/pm/PermissionGroupInfo.html#) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getPermissionGroupInfo(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve all of the information we know about a particular group of permissions. |
| open [PermissionInfo](https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#)! | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getPermissionInfo(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve all of the information we know about a particular permission. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getPreferredActivities(kotlin.collections.MutableList,%20kotlin.collections.MutableList,%20kotlin.String)(outFilters: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#!>, outActivities: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!>, packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Retrieve all preferred activities, previously added with `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#addPreferredActivity(android.content.IntentFilter,%20kotlin.Int,%20kotlin.Array,%20android.content.ComponentName)`, that are currently registered with the system. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PackageInfo](https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#)!\> | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getPreferredPackages(kotlin.Int)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve the list of all currently configured preferred packages. |
| open [ProviderInfo](https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo.html#) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getProviderInfo(android.content.ComponentName,%20kotlin.Int)(className: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve all of the information we know about a particular content provider class. |
| open [ActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getReceiverInfo(android.content.ComponentName,%20kotlin.Int)(className: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve all of the information we know about a particular receiver class. |
| open [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getResourcesForActivity(android.content.ComponentName)(activityName: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)` Retrieve the resources associated with an activity. |
| open [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getResourcesForApplication(android.content.pm.ApplicationInfo)(app: https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#)` Retrieve the resources for an application. |
| open [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getResourcesForApplication(kotlin.String)(appPackageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieve the resources associated with an application. |
| open [ServiceInfo](https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getServiceInfo(android.content.ComponentName,%20kotlin.Int)(className: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve all of the information we know about a particular service class. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SharedLibraryInfo](https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo.html#)!\> | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getSharedLibraries(kotlin.Int)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get a list of shared libraries on the device. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [FeatureInfo](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo.html#)!\> | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getSystemAvailableFeatures()()` Get a list of features that are available on the system. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getSystemSharedLibraryNames()()` Get a list of shared libraries that are available on the system. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getText(kotlin.String,%20kotlin.Int,%20android.content.pm.ApplicationInfo)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, resid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, appInfo: https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#?)` Retrieve text from a package. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getUserBadgedDrawableForDensity(android.graphics.drawable.Drawable,%20android.os.UserHandle,%20android.graphics.Rect,%20kotlin.Int)(drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#, badgeLocation: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#?, badgeDensity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` If the target user is a managed profile of the calling user or the caller is itself a managed profile, then this returns a badged copy of the given drawable allowing the user to distinguish it from the original drawable. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getUserBadgedIcon(android.graphics.drawable.Drawable,%20android.os.UserHandle)(icon: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)` If the target user is a managed profile, then this returns a badged copy of the given icon to be able to distinguish it from the original icon. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getUserBadgedLabel(kotlin.CharSequence,%20android.os.UserHandle)(label: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)` If the target user is a managed profile of the calling user or the caller is itself a managed profile, then this returns a copy of the label with badging for accessibility services like talkback. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getWhitelistedRestrictedPermissions(kotlin.String,%20kotlin.Int)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, whitelistFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the restricted permissions that have been whitelisted and the app is allowed to have them granted in their full form. |
| open [XmlResourceParser](https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser.html#)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#getXml(kotlin.String,%20kotlin.Int,%20android.content.pm.ApplicationInfo)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, resid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, appInfo: https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#?)` Retrieve an XML file from a package. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#hasSigningCertificate(kotlin.Int,%20kotlin.ByteArray,%20kotlin.Int)(uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, certificate: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html, type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Searches the set of signing certificates by which the package(s) for the given uid has proven to have been signed. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#hasSigningCertificate(kotlin.String,%20kotlin.ByteArray,%20kotlin.Int)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, certificate: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html, type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Searches the set of signing certificates by which the given package has proven to have been signed. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#hasSystemFeature(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Check whether the given feature name is one of the available features as returned by `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#hasSystemFeature(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, version: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Check whether the given feature name and version is one of the available features as returned by `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#isDeviceUpgrading()()` Returns true if the device is upgrading, such as first boot after OTA. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#isInstantApp()()` Gets whether this application is an instant app. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#isInstantApp(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Gets whether the given package is an instant app. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#isPermissionRevokedByPolicy(kotlin.String,%20kotlin.String)(permName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, pkgName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Checks whether a particular permissions has been revoked for a package by policy. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#isSafeMode()()` Return whether the device has been booted into safe mode. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ResolveInfo](https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#)!\> | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#queryBroadcastReceivers(android.content.Intent,%20kotlin.Int)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve all receivers that can handle a broadcast of the given intent. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ProviderInfo](https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo.html#)!\> | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#queryContentProviders(kotlin.String,%20kotlin.Int,%20kotlin.Int)(processName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve content provider information. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [InstrumentationInfo](https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo.html#)!\> | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#queryInstrumentation(kotlin.String,%20kotlin.Int)(targetPackage: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve information about available instrumentation code. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ResolveInfo](https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#)!\> | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#queryIntentActivities(android.content.Intent,%20kotlin.Int)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve all activities that can be performed for the given intent. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ResolveInfo](https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#)!\> | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#queryIntentActivityOptions(android.content.ComponentName,%20kotlin.Array,%20android.content.Intent,%20kotlin.Int)(caller: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#?, specifics: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/Intent.html#!>?, intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve a set of activities that should be presented to the user as similar options. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ResolveInfo](https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#)!\> | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#queryIntentContentProviders(android.content.Intent,%20kotlin.Int)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve all providers that can match the given intent. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ResolveInfo](https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#)!\> | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#queryIntentServices(android.content.Intent,%20kotlin.Int)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve all services that can match the given intent. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PermissionInfo](https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#)!\> | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#queryPermissionsByGroup(kotlin.String,%20kotlin.Int)(group: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Query for all of the permissions associated with a particular group. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#removePackageFromPreferred(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#removePermission(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Removes a permission that was previously added with `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#addPermission(android.content.pm.PermissionInfo)`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#removeWhitelistedRestrictedPermission(kotlin.String,%20kotlin.String,%20kotlin.Int)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, whitelistFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Removes a whitelisted restricted permission for an app. |
| open [ResolveInfo](https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#resolveActivity(android.content.Intent,%20kotlin.Int)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determine the best action to perform for a given Intent. |
| open [ProviderInfo](https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo.html#)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#resolveContentProvider(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Find a single content provider by its authority. |
| open [ResolveInfo](https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#)? | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#resolveService(android.content.Intent,%20kotlin.Int)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determine the best service to handle for a given Intent. |
| open [ResolveInfo](https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#)! | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#resolveServiceAsUser(android.content.Intent,%20kotlin.Int,%20kotlin.Int)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, userId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#setApplicationCategoryHint(kotlin.String,%20kotlin.Int)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, categoryHint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Provide a hint of what the `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#category:kotlin.Int` value should be for the given package. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#setApplicationEnabledSetting(kotlin.String,%20kotlin.Int,%20kotlin.Int)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, newState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the enabled setting for an application This setting will override any enabled state which may have been set by the application in its manifest. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#setComponentEnabledSetting(android.content.ComponentName,%20kotlin.Int,%20kotlin.Int)(componentName: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, newState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the enabled setting for a package component (activity, receiver, service, provider). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#setInstallerPackageName(kotlin.String,%20kotlin.String)(targetPackage: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, installerPackageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Change the installer associated with a given package. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#setInstantAppCookie(kotlin.ByteArray)(cookie: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#updateInstantAppCookie(kotlin.ByteArray)(cookie: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Updates the instant application cookie for the calling app. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/test/mock/MockPackageManager#verifyPendingInstall(kotlin.Int,%20kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, verificationCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Allows a package listening to the `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_NEEDS_VERIFICATION:kotlin.String` to respond to the package manager. |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#canPackageQuery(kotlin.String,%20kotlin.String)(sourcePackageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, targetPackageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Returns `true` if the source package is able to query for details about the target package. Applications that share details about other applications should use this API to determine if those details should be withheld from callers that do not otherwise have visibility of them.

Note: The caller must be able to query for details about the source and target package. A `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.NameNotFoundException.html#` is thrown if it isn't.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#canPackageQuery(kotlin.String,%20kotlin.Array)(sourcePackageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, targetPackageNames: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)`

Same as `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#canPackageQuery(kotlin.String,%20kotlin.String)` but accepts an array of target packages to be queried.

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getActivityInfo(android.content.ComponentName,%20android.content.pm.PackageManager.ComponentInfoFlags)(component: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, flags: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.ComponentInfoFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getActivityInfo(android.content.ComponentName,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getAppUidForPrivateComputeCoreUid(kotlin.Int)(pccUid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Maps a Private Compute Core (PCC) UID to its corresponding application UID.

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getApplicationInfo(kotlin.String,%20android.content.pm.PackageManager.ApplicationInfoFlags)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, flags: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.ApplicationInfoFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getApplicationInfo(kotlin.String,%20kotlin.Int)`.

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/ArchivedPackageInfo.html#?` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getArchivedPackage(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Return archived package info for the package or null if the package is not installed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getBackgroundPermissionOptionLabel()()`

Gets the localized label that corresponds to the option in settings for granting background access.

The intended use is for apps to reference this label in its instruction for users to grant a background permission.

<br />

`https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#?` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getEnableAppLockIntentForPackage(kotlin.String,%20kotlin.Boolean)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Returns a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` to launch an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` that allows the caller to set App Lock for the specified package. Returns null if the App Lock state of the package cannot be set, either because App Lock is not supported for that package, or because it is already set to that value.

App Lock is a feature that allows users to add authentication as a requirement to open individual apps, even if the device is unlocked. When App Lock is enabled for an app, the system performs the following protections:

- Requires authentication using device credentials (e.g. PIN, pattern, or password) or Class 3 biometrics, whenever the user attempts to open the app (including after reinstallation), or share information to it via the Sharesheet.
- Redacts sensitive content of notifications sent by the app.
- Removes the app's widgets and shortcuts from the home screen.
- Displays a locked view of the app in Recents to prevent content leakage.
- Hides the app's Direct Share targets from the Sharesheet.

Once authenticated, an App Lock enabled app remains unlocked while it is visible in the foreground. The app will remain unlocked for a short grace period after the user navigates away, after which the system will re-lock it. Additionally, all App Lock enabled apps are immediately locked whenever the device is locked.

Before calling this API to avoid getting a null `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` callers should first verify that App Lock is supported for the specified package by first checking `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#isAppLockSupported:kotlin.Boolean`, or if it's already at the target state for that package by checking `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#isAppLockEnabled:kotlin.Boolean`. The `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` resolves to an activity, which allows the user to enroll a device credential if one isn't enrolled, and then requires authentication before setting the App Lock enablement state as enabled or disabled. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#LOCK_APPS:kotlin.String`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getGroupOfPlatformPermission(kotlin.String,%20java.util.concurrent.Executor,%20java.util.function.Consumer)(permissionName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)`

Get the platform-defined permission group of a particular permission, if the permission is a platform-defined permission.

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/InstallSourceInfo.html#` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getInstallSourceInfo(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Retrieves information about how a package was installed or updated.

If the calling application does not hold the INSTALL_PACKAGES permission then the result will always return `null` from `https://developer.android.com/reference/kotlin/android/content/pm/InstallSourceInfo.html#getOriginatingPackageName()`.

If the package that requested the install has been uninstalled, then information about it will only be returned from `https://developer.android.com/reference/kotlin/android/content/pm/InstallSourceInfo.html#getInitiatingPackageName()` and `https://developer.android.com/reference/kotlin/android/content/pm/InstallSourceInfo.html#getInitiatingPackageSigningInfo()` if the calling package is requesting its own install information and is not an instant app.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#!>` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getInstalledApplications(android.content.pm.PackageManager.ApplicationInfoFlags)(flags: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.ApplicationInfoFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getInstalledApplications(kotlin.Int)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ModuleInfo.html#!>` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getInstalledModules(kotlin.Int)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Return a List of all modules that are installed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#!>` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getInstalledPackages(android.content.pm.PackageManager.PackageInfoFlags)(flags: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.PackageInfoFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getInstalledPackages(kotlin.Int)`.

<br />

`https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getLaunchIntentSenderForPackage(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Returns an `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` that can be used to launch a front-door activity in a package. This is used, for example, to implement an "open" button when browsing through packages. The current implementation is the same with `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getLaunchIntentForPackage(kotlin.String)`. Instead of returning the `https://developer.android.com/reference/kotlin/android/content/Intent.html#`, it returns the `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` which is not restricted by the package visibility.

The caller can invoke `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#sendIntent(android.content.Context,%20kotlin.Int,%20android.content.Intent,%20android.content.IntentSender.OnFinished,%20android.os.Handler)` to launch the activity. An `https://developer.android.com/reference/kotlin/android/content/IntentSender.SendIntentException.html#` is thrown if the package does not contain such an activity, or if *packageName* is not recognized.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getMimeGroup(kotlin.String)(mimeGroup: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Gets all MIME types contained by MIME group. Libraries should use a reverse-DNS prefix followed by a ':' character and library-specific group name to avoid namespace collisions, e.g. "com.example:myFeature".

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/ModuleInfo.html#` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getModuleInfo(kotlin.String,%20kotlin.Int)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Retrieve information for a particular module.

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#?` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPackageArchiveInfo(kotlin.String,%20android.content.pm.PackageManager.PackageInfoFlags)(archiveFilePath: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, flags: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.PackageInfoFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPackageArchiveInfo(kotlin.String,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html?` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPackageGids(kotlin.String,%20android.content.pm.PackageManager.PackageInfoFlags)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, flags: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.PackageInfoFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPackageGids(kotlin.String,%20kotlin.Int)`.

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPackageInfo(android.content.pm.VersionedPackage,%20android.content.pm.PackageManager.PackageInfoFlags)(versionedPackage: https://developer.android.com/reference/kotlin/android/content/pm/VersionedPackage.html#, flags: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.PackageInfoFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPackageInfo(android.content.pm.VersionedPackage,%20kotlin.Int)`

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPackageInfo(kotlin.String,%20android.content.pm.PackageManager.PackageInfoFlags)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, flags: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.PackageInfoFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPackageInfo(kotlin.String,%20kotlin.Int)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPackageUid(kotlin.String,%20android.content.pm.PackageManager.PackageInfoFlags)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, flags: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.PackageInfoFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPackageUid(kotlin.String,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#!>` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPackagesHoldingPermissions(kotlin.Array,%20android.content.pm.PackageManager.PackageInfoFlags)(permissions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>, flags: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.PackageInfoFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPackagesHoldingPermissions(kotlin.Array,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPlatformPermissionsForGroup(kotlin.String,%20java.util.concurrent.Executor,%20java.util.function.Consumer)(permissionGroupName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!>)`

Get the platform-defined permissions which belong to a particular permission group.

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getProperty(kotlin.String,%20android.content.ComponentName)(propertyName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, component: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)`

Returns the property defined in the given component declaration.

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getProperty(kotlin.String,%20kotlin.String)(propertyName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Returns the property defined in the given package's \<application\> tag.

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo.html#` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getProviderInfo(android.content.ComponentName,%20android.content.pm.PackageManager.ComponentInfoFlags)(component: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, flags: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.ComponentInfoFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getProviderInfo(android.content.ComponentName,%20kotlin.Int)`.

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getReceiverInfo(android.content.ComponentName,%20android.content.pm.PackageManager.ComponentInfoFlags)(component: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, flags: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.ComponentInfoFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getReceiverInfo(android.content.ComponentName,%20kotlin.Int)`.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/Resources.html#` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getResourcesForApplication(android.content.pm.ApplicationInfo,%20android.content.res.Configuration)(app: https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#, configuration: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#?)`

Retrieve the resources for an application for the provided configuration.

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getServiceInfo(android.content.ComponentName,%20android.content.pm.PackageManager.ComponentInfoFlags)(component: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, flags: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.ComponentInfoFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getServiceInfo(android.content.ComponentName,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo.html#!>` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSharedLibraries(android.content.pm.PackageManager.PackageInfoFlags)(flags: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.PackageInfoFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSharedLibraries(kotlin.Int)`.

<br />

`https://developer.android.com/reference/kotlin/android/os/Bundle.html#?` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSuspendedPackageAppExtras()()`

Returns a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` of extras that was meant to be sent to the calling app when it was suspended. An app with the permission `android.permission.SUSPEND_APPS` can supply this to the system at the time of suspending an app.

This is the same `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` that is sent along with the broadcast `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MY_PACKAGE_SUSPENDED:kotlin.String`, whenever the app is suspended. The contents of this `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` are a contract between the suspended app and the suspending app.

Note: These extras are optional, so if no extras were supplied to the system, this method will return `null`, even when the calling app has been suspended.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSyntheticAppDetailsActivityEnabled(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Return whether a synthetic app details activity will be generated if the app has no enabled launcher activity.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getTargetSdkVersion(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/SigningInfo.html#` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getVerifiedSigningInfo(kotlin.String,%20kotlin.Int)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, minAppSigningSchemeVersion: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Verifies and returns the [app signing](https://source.android.com/docs/security/features/apksigning) information of the file at the given path. This operation takes a few milliseconds. Unlike `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPackageArchiveInfo(kotlin.String,%20android.content.pm.PackageManager.PackageInfoFlags)` with `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_SIGNING_CERTIFICATES:kotlin.Int`, this method does not require the file to be a package archive file.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#isAppArchivable(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Returns true if an app is archivable.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#isAutoRevokeWhitelisted()()`

**Note:**In retrospect it would have been preferred to use more inclusive terminology when naming this API. Similar APIs added will refrain from using the term "whitelist".

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#isAutoRevokeWhitelisted(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Checks whether an application is exempt from having its permissions be automatically revoked when the app is unused for an extended period of time. Only the installer on record that installed the given package, or a holder of `WHITELIST_AUTO_REVOKE_PERMISSIONS` is allowed to call this.

**Note:**In retrospect it would have been preferred to use more inclusive terminology when naming this API. Similar APIs added will refrain from using the term "whitelist".

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#isDefaultApplicationIcon(android.graphics.drawable.Drawable)(drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)`

Returns if the provided drawable represents the default activity icon provided by the system. PackageManager silently returns a default application icon for any package/activity if the app itself does not define one or if the system encountered any error when loading the icon. Developers can use this to check implement app specific logic around retrying or caching.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#isPackageStopped(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Query if an app is currently stopped.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#isPackageSuspended()()`

Apps can query this to know if they have been suspended. A system app with the permission `android.permission.SUSPEND_APPS` can put any app on the device into a suspended state.

While in this state, the application's notifications will be hidden, any of its started activities will be stopped and it will not be able to show toasts or dialogs or play audio. When the user tries to launch a suspended app, the system will, instead, show a dialog to the user informing them that they cannot use this app while it is suspended.

When an app is put into this state, the broadcast action `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MY_PACKAGE_SUSPENDED:kotlin.String` will be delivered to any of its broadcast receivers that included this action in their intent-filters, *including manifest receivers.* Similarly, a broadcast action `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MY_PACKAGE_UNSUSPENDED:kotlin.String` is delivered when a previously suspended app is taken out of this state. Apps are expected to use these to gracefully deal with transitions to and from this state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#isPackageSuspended(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Query if an app is currently suspended.

<br />

`T` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#parseAndroidManifest(android.os.ParcelFileDescriptor,%20java.util.function.Function)(apkFileDescriptor: https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#, parserFunction: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser.html#!, T>)`

Similar to `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#parseAndroidManifest(java.io.File,%20java.util.function.Function)`, but accepting a file descriptor instead of a File object. 
This method may take several seconds to complete, so it should only be called from a worker thread.

<br />

`T` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#parseAndroidManifest(java.io.File,%20java.util.function.Function)(apkFile: https://developer.android.com/reference/kotlin/java/io/File.html#, parserFunction: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser.html#!, T>)`

Retrieve AndroidManifest.xml information for the given application apk file.

Example:

```kotlin
<code>
  Bundle result;
  try {
      result = getContext().getPackageManager().parseAndroidManifest(apkFile,
              xmlResourceParser -&gt; {
                  Bundle bundle = new Bundle();
                  // Search the start tag
                  int type;
                  while ((type = xmlResourceParser.next()) != XmlPullParser.START_TAG
                          &amp;&amp; type != XmlPullParser.END_DOCUMENT) {
                  }
                  if (type != XmlPullParser.START_TAG) {
                      return bundle;
                  }
 
                  // Start to read the tags and attributes from the xmlResourceParser
                  if (!xmlResourceParser.getName().equals("manifest")) {
                      return bundle;
                  }
                  String packageName = xmlResourceParser.getAttributeValue(null, "package");
                  bundle.putString("package", packageName);
 
                  // Continue to read the tags and attributes from the xmlResourceParser
 
                  return bundle;
              });
  } catch (IOException e) {
  }
  </code>
```
Note: When the parserFunction is invoked, the client can read the AndroidManifest.xml information by the XmlResourceParser object. After leaving the parserFunction, the XmlResourceParser object will be closed. The caller should also handle the exception for calling this method. 
This method may take several seconds to complete, so it should only be called from a worker thread.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#!>` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryActivityProperty(kotlin.String)(propertyName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Returns the property definition for all \<activity\> and \<activity-alias\> tags.

If the property is not defined with any \<activity\> and \<activity-alias\> tag, returns and empty list.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#!>` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryApplicationProperty(kotlin.String)(propertyName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Returns the property definition for all \<application\> tags.

If the property is not defined with any \<application\> tag, returns and empty list.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#!>` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryBroadcastReceivers(android.content.Intent,%20android.content.pm.PackageManager.ResolveInfoFlags)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.ResolveInfoFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryBroadcastReceivers(android.content.Intent,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo.html#!>` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryContentProviders(kotlin.String,%20kotlin.Int,%20android.content.pm.PackageManager.ComponentInfoFlags)(processName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.ComponentInfoFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryContentProviders(kotlin.String,%20kotlin.Int,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#!>` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryIntentActivities(android.content.Intent,%20android.content.pm.PackageManager.ResolveInfoFlags)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.ResolveInfoFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryIntentActivities(android.content.Intent,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#!>` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryIntentActivityOptions(android.content.ComponentName,%20kotlin.collections.MutableList,%20android.content.Intent,%20android.content.pm.PackageManager.ResolveInfoFlags)(caller: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#?, specifics: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/Intent.html#!>?, intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.ResolveInfoFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryIntentActivityOptions(android.content.ComponentName,%20kotlin.Array,%20android.content.Intent,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#!>` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryIntentContentProviders(android.content.Intent,%20android.content.pm.PackageManager.ResolveInfoFlags)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.ResolveInfoFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryIntentContentProviders(android.content.Intent,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#!>` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryIntentServices(android.content.Intent,%20android.content.pm.PackageManager.ResolveInfoFlags)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.ResolveInfoFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryIntentServices(android.content.Intent,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#!>` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryProviderProperty(kotlin.String)(propertyName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Returns the property definition for all \<provider\> tags.

If the property is not defined with any \<provider\> tag, returns and empty list.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#!>` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryReceiverProperty(kotlin.String)(propertyName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Returns the property definition for all \<receiver\> tags.

If the property is not defined with any \<receiver\> tag, returns and empty list.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#!>` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryServiceProperty(kotlin.String)(propertyName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Returns the property definition for all \<service\> tags.

If the property is not defined with any \<service\> tag, returns and empty list.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#relinquishUpdateOwnership(kotlin.String)(targetPackage: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Attempt to relinquish the update ownership of the given package. Only the current update owner of the given package can use this API.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#requestChecksums(kotlin.String,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.collections.MutableList,%20android.content.pm.PackageManager.OnChecksumsReadyListener)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, includeSplits: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, required: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, trustedInstallers: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/security/cert/Certificate.html#!>, onChecksumsReadyListener: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.OnChecksumsReadyListener.html#)`

Requests the checksums for APKs within a package. The checksums will be returned asynchronously via onChecksumsReadyListener. By default returns all readily available checksums: - enforced by platform, - enforced by installer. If caller needs a specific checksum kind, they can specify it as required. **Caution: Android can not verify installer-provided checksums. Make sure you specify trusted installers.**

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#?` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#resolveActivity(android.content.Intent,%20android.content.pm.PackageManager.ResolveInfoFlags)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.ResolveInfoFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#resolveActivity(android.content.Intent,%20kotlin.Int)`.

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo.html#?` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#resolveContentProvider(kotlin.String,%20android.content.pm.PackageManager.ComponentInfoFlags)(authority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, flags: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.ComponentInfoFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#resolveContentProvider(kotlin.String,%20kotlin.Int)`.

<br />

`https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#?` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#resolveService(android.content.Intent,%20android.content.pm.PackageManager.ResolveInfoFlags)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, flags: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.ResolveInfoFlags.html#)`

See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#resolveService(android.content.Intent,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#setAutoRevokeWhitelisted(kotlin.String,%20kotlin.Boolean)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, whitelisted: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Marks an application exempt from having its permissions be automatically revoked when the app is unused for an extended period of time. Only the installer on record that installed the given package is allowed to call this. Packages start in whitelisted state, and it is the installer's responsibility to un-whitelist the packages it installs, unless auto-revoking permissions from that package would cause breakages beyond having to re-request the permission(s).

**Note:**In retrospect it would have been preferred to use more inclusive terminology when naming this API. Similar APIs added will refrain from using the term "whitelist".

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#setComponentEnabledSettings(kotlin.collections.MutableList)(settings: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.ComponentEnabledSetting.html#!>)`

Set the enabled settings for package components such as activities, receivers, services and providers. This setting will override any enabled state which may have been set by the component in its manifest.

This api accepts a list of component changes, and applies them all atomically. The application can use this api if components have dependencies and need to be updated atomically.

The permission is not required if target components are running under the same uid with the caller.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#setMimeGroup(kotlin.String,%20kotlin.collections.MutableSet)(mimeGroup: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, mimeTypes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)`

Sets MIME group's MIME types. Libraries should use a reverse-DNS prefix followed by a ':' character and library-specific group name to avoid namespace collisions, e.g. "com.example:myFeature".

<br />

Inherited properties From class `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/security/cert/Certificate.html#!>` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#TRUST_ALL:kotlin.collections.MutableList`

Trust any Installer to provide checksums for the package.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/security/cert/Certificate.html#!>` `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#TRUST_NONE:kotlin.collections.MutableList`

Don't trust any Installer to provide checksums for the package. This effectively disables optimized Installer-enforced checksums.

<br />

## Public constructors

### MockPackageManager

```
MockPackageManager()
```

## Public methods

### addPackageToPreferred

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addPackageToPreferred(packageName: String): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### addPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addPermission(info: PermissionInfo): Boolean
```

**Deprecated:** *Deprecated in Java.*

Add a new dynamic permission to the system. For this to work, your package must have defined a permission tree through the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestPermissionTree:kotlin.IntArray` tag in its manifest. A package can only add permissions to trees that were defined by either its own package or another with the same user id; a permission is in a tree if it matches the name of the permission tree + ".": for example, "com.foo.bar" is a member of the permission tree "com.foo".

It is good to make your permission tree name descriptive, because you are taking possession of that entire set of permission names. Thus, it must be under a domain you control, with a suffix that will not match any normal permissions that may be declared in any applications that are part of that domain.

New permissions must be added before any .apks are installed that use those permissions. Permissions you add through this method are remembered across reboots of the device. If the given permission already exists, the info you supply here will be used to update it.

| Parameters ||
|---|---|
| `info` | [PermissionInfo](https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#): Description of the permission to be added. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if a new permission was created, false if an existing one was updated. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if you are not allowed to add the given permission name. |

### addPermissionAsync

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addPermissionAsync(info: PermissionInfo): Boolean
```

**Deprecated:** *Deprecated in Java.*

Like `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#addPermission(android.content.pm.PermissionInfo)` but asynchronously persists the package manager state after returning from the call, allowing it to return quicker and batch a series of adds at the expense of no guarantee the added permission will be retained if the device is rebooted before it is written.

| Parameters ||
|---|---|
| `info` | [PermissionInfo](https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#): This value cannot be `null`. |

### addPreferredActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addPreferredActivity(
    filter: IntentFilter, 
    match: Int, 
    set: Array<ComponentName!>?, 
    activity: ComponentName
): Unit
```

**Deprecated:** *Deprecated in Java.*

Add a new preferred activity mapping to the system. This will be used to automatically select the given activity component when `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)` finds multiple matching activities and also matches the given filter.

| Parameters ||
|---|---|
| `filter` | [IntentFilter](https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#): The set of intents under which this activity will be made preferred. This value cannot be `null`. |
| `match` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The IntentFilter match category that this preference applies to. |
| `set` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!\>?: The set of activities that the user was picking from when this preference was made. This value may be `null`. |
| `activity` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#): The component name of the activity that is to be preferred. This value cannot be `null`. |

### addWhitelistedRestrictedPermission

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addWhitelistedRestrictedPermission(
    packageName: String, 
    permission: String, 
    whitelistFlags: Int
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Adds a whitelisted restricted permission for an app.

Permissions can be hard restricted which means that the app cannot hold them or soft restricted where the app can hold the permission but in a weaker form. Whether a permission is `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#FLAG_HARD_RESTRICTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#FLAG_SOFT_RESTRICTED:kotlin.Int` depends on the permission declaration. Whitelisting a hard restricted permission allows for the to hold that permission and whitelisting a soft restricted permission allows the app to hold the permission in its full, unrestricted form.

<br />

There are four whitelists:
1. one for cases where the system permission policy whitelists a permission This list corresponds to the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_SYSTEM:kotlin.Int` flag. Can only be modified by pre-installed holders of a dedicated permission.
2. one for cases where the system whitelists the permission when upgrading from an OS version in which the permission was not restricted to an OS version in which the permission is restricted. This list corresponds to the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_UPGRADE:kotlin.Int` flag. Can be modified by pre-installed holders of a dedicated permission. The installer on record can only remove permissions from this whitelist.
3. one for cases where the installer of the package whitelists a permission. This list corresponds to the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_INSTALLER:kotlin.Int` flag. Can be modified by pre-installed holders of a dedicated permission or the installer on record.

You need to specify the whitelists for which to set the whitelisted permissions which will clear the previous whitelisted permissions and replace them with the provided ones.

**Note:**In retrospect it would have been preferred to use more inclusive terminology when naming this API. Similar APIs added will refrain from using the term "whitelist".

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `permName` | The whitelisted permission to add. This value cannot be `null`. |
| `whitelistFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_INSTALLER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_UPGRADE:kotlin.Int` |
| `permission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the permission was added to the whitelist. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if you try to modify a whitelist that you have no access to. |

### canRequestPackageInstalls

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canRequestPackageInstalls(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks whether the calling package is allowed to request package installs through package installer. Apps are encouraged to call this API before launching the package installer via intent `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_INSTALL_PACKAGE:kotlin.String`. Starting from Android O, the user can explicitly choose what external sources they trust to install apps on the device. If this API returns false, the install request will be blocked by the package installer and a dialog will be shown to the user with an option to launch settings to change their preference. An application must target Android O or higher and declare permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_INSTALL_PACKAGES:kotlin.String` in order to use this API.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the calling package is trusted by the user to request install packages on the device, false otherwise. |

### canonicalToCurrentPackageNames

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canonicalToCurrentPackageNames(names: Array<String!>): Array<String!>!
```

**Deprecated:** *Deprecated in Java.*

Map from a packages canonical name to the current name in use on the device.

| Parameters ||
|---|---|
| `packageNames` | Array of new names to be mapped. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | Returns an array of the same size as the original, containing the current name for each package. |

### checkPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkPermission(
    permName: String, 
    pkgName: String
): Int
```

**Deprecated:** *Deprecated in Java.*

Check whether a particular package has been granted a particular permission.

**Note:** This API returns the underlying permission state as-is and is mostly intended for permission managing system apps. To perform an access check for a certain app, please use the `https://developer.android.com/reference/kotlin/android/content/Context.html#checkPermission(kotlin.String,%20kotlin.Int,%20kotlin.Int)` APIs instead.

| Parameters ||
|---|---|
| `permName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the permission you are checking for. This value cannot be `null`. |
| `packageName` | The name of the package you are checking against. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | If the package has the permission, PERMISSION_GRANTED is returned. If it does not have the permission, PERMISSION_DENIED is returned. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PERMISSION_GRANTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PERMISSION_DENIED:kotlin.Int` |

### checkSignatures

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkSignatures(
    uid1: Int, 
    uid2: Int
): Int
```

**Deprecated:** *Deprecated in Java.*

Like `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#checkSignatures(kotlin.String,%20kotlin.String)`, but takes UIDs of the two packages to be checked. This can be useful, for example, when doing the check in an IPC, where the UID is the only identity available. It is functionally identical to determining the package associated with the UIDs and checking their signatures.

| Parameters ||
|---|---|
| `uid1` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): First UID whose signature will be compared. |
| `uid2` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Second UID whose signature will be compared. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns an integer indicating whether all signatures on the two packages match. The value is \>= 0 (`https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_MATCH:kotlin.Int`) if all signatures match or \< 0 if there is not a match (`https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_NO_MATCH:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_UNKNOWN_PACKAGE:kotlin.Int`). Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_MATCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_NEITHER_SIGNED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_FIRST_NOT_SIGNED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_SECOND_NOT_SIGNED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_NO_MATCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_UNKNOWN_PACKAGE:kotlin.Int` |

### checkSignatures

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkSignatures(
    pkg1: String, 
    pkg2: String
): Int
```

**Deprecated:** *Deprecated in Java.*

Compare the signatures of two packages to determine if the same signature appears in both of them. If they do contain the same signature, then they are allowed special privileges when working with each other: they can share the same user-id, run instrumentation against each other, etc.

| Parameters ||
|---|---|
| `packageName1` | First package name whose signature will be compared. This value cannot be `null`. |
| `packageName2` | Second package name whose signature will be compared. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns an integer indicating whether all signatures on the two packages match. The value is \>= 0 (`https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_MATCH:kotlin.Int`) if all signatures match or \< 0 if there is not a match (`https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_NO_MATCH:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_UNKNOWN_PACKAGE:kotlin.Int`). Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_MATCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_NEITHER_SIGNED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_FIRST_NOT_SIGNED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_SECOND_NOT_SIGNED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_NO_MATCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SIGNATURE_UNKNOWN_PACKAGE:kotlin.Int` |

### clearInstantAppCookie

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearInstantAppCookie(): Unit
```

**Deprecated:** *Deprecated in Java.*

Clears the instant application cookie for the calling app.

### clearPackagePreferredActivities

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearPackagePreferredActivities(packageName: String): Unit
```

**Deprecated:** *Deprecated in Java.*

Remove all preferred activity mappings, previously added with `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#addPreferredActivity(android.content.IntentFilter,%20kotlin.Int,%20kotlin.Array,%20android.content.ComponentName)`, from the system whose activities are implemented in the given package name. An application can only clear its own package(s).

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the package whose preferred activity mappings are to be removed. This value cannot be `null`. |

### currentToCanonicalPackageNames

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun currentToCanonicalPackageNames(names: Array<String!>): Array<String!>!
```

**Deprecated:** *Deprecated in Java.*

Map from the current package names in use on the device to whatever the current canonical name of that package is.

| Parameters ||
|---|---|
| `packageNames` | Array of current names to be mapped. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | Returns an array of the same size as the original, containing the canonical name for each package. |

### extendVerificationTimeout

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun extendVerificationTimeout(
    id: Int, 
    verificationCodeAtTimeout: Int, 
    millisecondsToDelay: Long
): Unit
```

**Deprecated:** *Deprecated in Java.*

Allows a package listening to the `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_NEEDS_VERIFICATION:kotlin.String` to extend the default timeout for a response and declare what action to perform after the timeout occurs. The response must include the `verificationCodeAtTimeout` which is one of `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#VERIFICATION_ALLOW:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#VERIFICATION_REJECT:kotlin.Int`. This method can be called multiple times, but the total amount of time extension time will be limited to `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MAXIMUM_VERIFICATION_TIMEOUT:kotlin.Long`. If the method is called multiple times with different `verificationCodeAtTimeout`, then previous `verificationCodeAtTimeout` will be ignored and only the latest one will take effect. If this method is called after calling `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#verifyPendingInstall(kotlin.Int,%20kotlin.Int)`, it may nullify the result set by verifyPendingInstall.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): pending package identifier as passed via the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#EXTRA_VERIFICATION_ID:kotlin.String` Intent extra. |
| `verificationCodeAtTimeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): either `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#VERIFICATION_ALLOW:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#VERIFICATION_REJECT:kotlin.Int`. If `verificationCodeAtTimeout` is neither `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#VERIFICATION_ALLOW:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#VERIFICATION_REJECT:kotlin.Int`, then `verificationCodeAtTimeout` will default to `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#VERIFICATION_REJECT:kotlin.Int`. |
| `millisecondsToDelay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the amount of time requested for the timeout. Must be positive and less than `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MAXIMUM_VERIFICATION_TIMEOUT:kotlin.Long`. If `millisecondsToDelay` is out of bounds, `millisecondsToDelay` will be set to the closest in bounds value; namely, 0 or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MAXIMUM_VERIFICATION_TIMEOUT:kotlin.Long`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller does not have the PACKAGE_VERIFICATION_AGENT permission. |

### getActivityBanner

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActivityBanner(activityName: ComponentName): Drawable?
```

**Deprecated:** *Deprecated in Java.*

Retrieve the banner associated with an activity. Given the full name of an activity, retrieves the information about it and calls `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo.html#loadIcon(android.content.pm.PackageManager)` to return its banner. If the activity cannot be found, NameNotFoundException is thrown.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getApplicationIcon(android.content.pm.ApplicationInfo)`.

| Parameters ||
|---|---|
| `activityName` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#): Name of the activity whose banner is to be retrieved. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | Returns the image of the banner, or null if the activity has no banner specified. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for the given activity could not be loaded. |

### getActivityBanner

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActivityBanner(intent: Intent): Drawable?
```

**Deprecated:** *Deprecated in Java.*

Retrieve the banner associated with an Intent. If intent.getClassName() is set, this simply returns the result of getActivityBanner(intent.getClassName()). Otherwise it resolves the intent's component and returns the banner associated with the resolved component. If intent.getClassName() cannot be found or the Intent cannot be resolved to a component, NameNotFoundException is thrown.

| Parameters ||
|---|---|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#): The intent for which you would like to retrieve a banner. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | Returns the image of the banner, or null if the activity has no banner specified. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for application matching the given intent could not be loaded. |

### getActivityIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActivityIcon(activityName: ComponentName): Drawable
```

**Deprecated:** *Deprecated in Java.*

Retrieve the icon associated with an activity. Given the full name of an activity, retrieves the information about it and calls `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo.html#loadIcon(android.content.pm.PackageManager)` to return its icon. If the activity cannot be found, NameNotFoundException is thrown.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getApplicationIcon(android.content.pm.ApplicationInfo)`.

| Parameters ||
|---|---|
| `activityName` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#): Name of the activity whose icon is to be retrieved. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` | Returns the image of the icon, or the default activity icon if it could not be found. Does not return null. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for the given activity could not be loaded. |

### getActivityIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActivityIcon(intent: Intent): Drawable
```

**Deprecated:** *Deprecated in Java.*

Retrieve the icon associated with an Intent. If intent.getClassName() is set, this simply returns the result of getActivityIcon(intent.getClassName()). Otherwise it resolves the intent's component and returns the icon associated with the resolved component. If intent.getClassName() cannot be found or the Intent cannot be resolved to a component, NameNotFoundException is thrown.

| Parameters ||
|---|---|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#): The intent for which you would like to retrieve an icon. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` | Returns the image of the icon, or the default activity icon if it could not be found. Does not return null. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for application matching the given intent could not be loaded. |

### getActivityInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActivityInfo(
    className: ComponentName, 
    flags: Int
): ActivityInfo
```

**Deprecated:** *Deprecated in Java.*

Retrieve all of the information we know about a particular activity class. Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getActivityInfo(android.content.ComponentName,%20android.content.pm.PackageManager.ComponentInfoFlags)` when long flags are needed.

| Parameters ||
|---|---|
| `component` | The full component name (i.e. com.google.apps.contacts/com.google.apps.contacts. ContactsList) of an Activity class. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#` | An `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#` containing information about the activity. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if a package with the given name cannot be found on the system. |

### getActivityLogo

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActivityLogo(activityName: ComponentName): Drawable?
```

**Deprecated:** *Deprecated in Java.*

Retrieve the logo associated with an activity. Given the full name of an activity, retrieves the information about it and calls `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo.html#loadLogo(android.content.pm.PackageManager)` to return its logo. If the activity cannot be found, NameNotFoundException is thrown.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getApplicationIcon(android.content.pm.ApplicationInfo)`.

| Parameters ||
|---|---|
| `activityName` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#): Name of the activity whose logo is to be retrieved. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | Returns the image of the logo or null if the activity has no logo specified. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for the given activity could not be loaded. |

### getActivityLogo

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActivityLogo(intent: Intent): Drawable?
```

**Deprecated:** *Deprecated in Java.*

Retrieve the logo associated with an Intent. If intent.getClassName() is set, this simply returns the result of getActivityLogo(intent.getClassName()). Otherwise it resolves the intent's component and returns the logo associated with the resolved component. If intent.getClassName() cannot be found or the Intent cannot be resolved to a component, NameNotFoundException is thrown.

| Parameters ||
|---|---|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#): The intent for which you would like to retrieve a logo. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | Returns the image of the logo, or null if the activity has no logo specified. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for application matching the given intent could not be loaded. |

### getAllIntentFilters

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAllIntentFilters(packageName: String!): MutableList<IntentFilter!>!
```

**Deprecated:** *Deprecated in Java.*

### getAllPermissionGroups

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAllPermissionGroups(flags: Int): MutableList<PermissionGroupInfo!>
```

**Deprecated:** *Deprecated in Java.*

Retrieve all of the known permission groups in the system.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_META_DATA:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PermissionGroupInfo.html#!>` | Returns a list of `https://developer.android.com/reference/kotlin/android/content/pm/PermissionGroupInfo.html#` containing information about all of the known permission groups. This value cannot be `null`. |

### getApplicationBanner

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApplicationBanner(info: ApplicationInfo): Drawable?
```

**Deprecated:** *Deprecated in Java.*

Retrieve the banner associated with an application.

| Parameters ||
|---|---|
| `info` | [ApplicationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#): Information about application being queried. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | Returns the image of the banner or null if the application has no banner specified. |

### getApplicationBanner

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApplicationBanner(packageName: String): Drawable?
```

**Deprecated:** *Deprecated in Java.*

Retrieve the banner associated with an application. Given the name of the application's package, retrieves the information about it and calls getApplicationIcon() to return its banner. If the application cannot be found, NameNotFoundException is thrown.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getApplicationIcon(android.content.pm.ApplicationInfo)`.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Name of the package whose application banner is to be retrieved. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | Returns the image of the banner or null if the application has no banner specified. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for the given application could not be loaded. |

### getApplicationEnabledSetting

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApplicationEnabledSetting(packageName: String): Int
```

**Deprecated:** *Deprecated in Java.*

Return the enabled setting for an application. This returns the last value set by `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#setApplicationEnabledSetting(kotlin.String,%20kotlin.Int,%20kotlin.Int)`; in most cases this value will be `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_DEFAULT:kotlin.Int` since the value originally specified in the manifest has not been modified.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The package name of the application to retrieve. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns the current enabled state for the application. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_DISABLED_USER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_DISABLED_UNTIL_USED:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the named package does not exist. |

### getApplicationIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApplicationIcon(info: ApplicationInfo): Drawable
```

**Deprecated:** *Deprecated in Java.*

Retrieve the icon associated with an application. If it has not defined an icon, the default app icon is returned. Does not return null.

Note: The returned drawable's dimensions are capped to a maximum size of `2048 x 2048` pixels. If the resource's intrinsic dimensions exceed this limit, it will be downsampled automatically, preserving its aspect ratio.

| Parameters ||
|---|---|
| `info` | [ApplicationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#): Information about application being queried. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` | Returns the image of the icon, or the default application icon if it could not be found. |

### getApplicationIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApplicationIcon(packageName: String): Drawable
```

**Deprecated:** *Deprecated in Java.*

Retrieve the icon associated with an application. Given the name of the application's package, retrieves the information about it and calls getApplicationIcon() to return its icon. If the application cannot be found, NameNotFoundException is thrown.

Note: The returned drawable's dimensions are capped to a maximum size of `2048 x 2048` pixels. If the resource's intrinsic dimensions exceed this limit, it will be downsampled automatically, preserving its aspect ratio.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Name of the package whose application icon is to be retrieved. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` | Returns the image of the icon, or the default application icon if it could not be found. Does not return null. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for the given application could not be loaded. |

### getApplicationInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApplicationInfo(
    packageName: String, 
    flags: Int
): ApplicationInfo
```

**Deprecated:** *Deprecated in Java.*

Retrieve all of the information we know about a particular package/application. Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getApplicationInfo(kotlin.String,%20android.content.pm.PackageManager.ApplicationInfoFlags)` when long flags are needed.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The full name (i.e. com.google.apps.contacts) of an application. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#` | An `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#` containing information about the package. If flag `MATCH_UNINSTALLED_PACKAGES` is set and if the package is not found in the list of installed applications, the application information is retrieved from the list of uninstalled applications (which includes installed applications as well as applications with data directory i.e. applications which had been deleted with `DELETE_KEEP_DATA` flag set). This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if a package with the given name cannot be found on the system. |

### getApplicationLabel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApplicationLabel(info: ApplicationInfo): CharSequence
```

**Deprecated:** *Deprecated in Java.*

Return the label to use for this application.

| Parameters ||
|---|---|
| `info` | [ApplicationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#): The `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#` of the application to get the label of. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` | Returns a `https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#` containing the label associated with this application, or its name the item does not have a label. This value cannot be `null`. |

### getApplicationLogo

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApplicationLogo(info: ApplicationInfo): Drawable?
```

**Deprecated:** *Deprecated in Java.*

Retrieve the logo associated with an application. If it has not specified a logo, this method returns null.

| Parameters ||
|---|---|
| `info` | [ApplicationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#): Information about application being queried. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | Returns the image of the logo, or null if no logo is specified by the application. |

### getApplicationLogo

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApplicationLogo(packageName: String): Drawable?
```

**Deprecated:** *Deprecated in Java.*

Retrieve the logo associated with an application. Given the name of the application's package, retrieves the information about it and calls getApplicationLogo() to return its logo. If the application cannot be found, NameNotFoundException is thrown.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getApplicationIcon(android.content.pm.ApplicationInfo)`.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Name of the package whose application logo is to be retrieved. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | Returns the image of the logo, or null if no application logo has been specified. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for the given application could not be loaded. |

### getChangedPackages

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChangedPackages(sequenceNumber: Int): ChangedPackages?
```

**Deprecated:** *Deprecated in Java.*

Returns the names of the packages that have been changed \[eg. added, removed or updated\] since the given sequence number.

If no packages have been changed, returns `null`.

The sequence number starts at `0` and is reset every boot.

| Parameters ||
|---|---|
| `sequenceNumber` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The first sequence number for which to retrieve package changes. Value is 0 or greater |

### getComponentEnabledSetting

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getComponentEnabledSetting(componentName: ComponentName): Int
```

**Deprecated:** *Deprecated in Java.*

Return the enabled setting for a package component (activity, receiver, service, provider). This returns the last value set by `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#setComponentEnabledSetting(android.content.ComponentName,%20kotlin.Int,%20kotlin.Int)`; in most cases this value will be `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_DEFAULT:kotlin.Int` since the value originally specified in the manifest has not been modified.

| Parameters ||
|---|---|
| `componentName` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#): The component to retrieve. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns the current enabled state for the component. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_DISABLED_USER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_DISABLED_UNTIL_USED:kotlin.Int` |

### getDefaultActivityIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDefaultActivityIcon(): Drawable
```

**Deprecated:** *Deprecated in Java.*

Return the generic icon for an activity that is used when no specific icon is defined.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` | Drawable Image of the icon. This value cannot be `null`. |

### getDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawable(
    packageName: String, 
    resid: Int, 
    appInfo: ApplicationInfo?
): Drawable?
```

**Deprecated:** *Deprecated in Java.*

Retrieve an image from a package. This is a low-level API used by the various package manager info structures (such as `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo.html#` to implement retrieval of their associated icon.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the package that this icon is coming from. Cannot be null. |
| `resid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource identifier of the desired image. Cannot be 0. |
| `appInfo` | [ApplicationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#)?: Overall information about packageName. This may be null, in which case the application information will be retrieved for you if needed; if you already have this information around, it can be much more efficient to supply it here. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | Returns a Drawable holding the requested image. Returns null if an image could not be found for any reason. |

### getInstalledApplications

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInstalledApplications(flags: Int): MutableList<ApplicationInfo!>
```

**Deprecated:** *Deprecated in Java.*

Return a List of all application packages that are installed for the current user. If flag GET_UNINSTALLED_PACKAGES has been set, a list of all applications including those deleted with `DELETE_KEEP_DATA` (partially installed apps with data directory) will be returned. Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getInstalledApplications(android.content.pm.PackageManager.ApplicationInfoFlags)` when long flags are needed.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#!>` | A List of ApplicationInfo objects, one for each installed application. In the unlikely case there are no installed packages, an empty list is returned. If flag `MATCH_UNINSTALLED_PACKAGES` is set, the application information is retrieved from the list of uninstalled applications (which includes installed applications as well as applications with data directory i.e. applications which had been deleted with `DELETE_KEEP_DATA` flag set). This value cannot be `null`. |

### getInstalledPackages

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInstalledPackages(flags: Int): MutableList<PackageInfo!>
```

**Deprecated:** *Deprecated in Java.*

Return a List of all packages that are installed for the current user. Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getInstalledPackages(android.content.pm.PackageManager.PackageInfoFlags)` when long flags are needed.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#!>` | A List of PackageInfo objects, one for each installed package, containing information about the package. In the unlikely case there are no installed packages, an empty list is returned. If flag `MATCH_UNINSTALLED_PACKAGES` is set, the package information is retrieved from the list of uninstalled applications (which includes installed applications as well as applications with data directory i.e. applications which had been deleted with `DELETE_KEEP_DATA` flag set). This value cannot be `null`. |

### getInstallerPackageName

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInstallerPackageName(packageName: String): String?
```

**Deprecated:** *Deprecated in Java.*

Retrieve the package name of the application that installed a package. This identifies which market the package came from.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the package to query. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the given package name is not installed |

### getInstantAppCookie

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInstantAppCookie(): ByteArray
```

**Deprecated:** *Deprecated in Java.*

Gets the instant application cookie for this app. Non instant apps and apps that were instant but were upgraded to normal apps can still access this API. For instant apps this cookie is cached for some time after uninstall while for normal apps the cookie is deleted after the app is uninstalled. The cookie is always present while the app is installed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | The cookie. This value cannot be `null`. |

### getInstantAppCookieMaxBytes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInstantAppCookieMaxBytes(): Int
```

**Deprecated:** *Deprecated in Java.*

Gets the maximum size in bytes of the cookie data an instant app can store on the device.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The max cookie size in bytes. |

### getInstrumentationInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInstrumentationInfo(
    className: ComponentName, 
    flags: Int
): InstrumentationInfo
```

**Deprecated:** *Deprecated in Java.*

Retrieve all of the information we know about a particular instrumentation class.

| Parameters ||
|---|---|
| `className` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#): The full name (i.e. com.google.apps.contacts.InstrumentList) of an Instrumentation class. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_META_DATA:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo.html#` | An `https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo.html#` object containing information about the instrumentation. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if a package with the given name cannot be found on the system. |

### getLaunchIntentForPackage

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLaunchIntentForPackage(packageName: String): Intent?
```

**Deprecated:** *Deprecated in Java.*

Returns a "good" intent to launch a front-door activity in a package. This is used, for example, to implement an "open" button when browsing through packages. The current implementation looks first for a main activity in the category `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_INFO:kotlin.String`, and next for a main activity in the category `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_LAUNCHER:kotlin.String`. Returns `null` if neither are found.

Consider using `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getLaunchIntentSenderForPackage(kotlin.String)` if the caller is not allowed to query for the `packageName`.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the package to inspect. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Intent.html#?` | A fully-qualified `https://developer.android.com/reference/kotlin/android/content/Intent.html#` that can be used to launch the main activity in the package. Returns `null` if the package does not contain such an activity, or if *packageName* is not recognized. |

### getLeanbackLaunchIntentForPackage

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLeanbackLaunchIntentForPackage(packageName: String): Intent?
```

**Deprecated:** *Deprecated in Java.*

Return a "good" intent to launch a front-door Leanback activity in a package, for use for example to implement an "open" button when browsing through packages. The current implementation will look for a main activity in the category `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_LEANBACK_LAUNCHER:kotlin.String`, or return null if no main leanback activities are found.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the package to inspect. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Intent.html#?` | Returns either a fully-qualified Intent that can be used to launch the main Leanback activity in the package, or null if the package does not contain such an activity. |

### getMemoryBudgets

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMemoryBudgets(info: ApplicationInfo): MutableList<MemoryBudgetInfo!>
```

**Deprecated:** *Deprecated in Java.*

Return the memory budgets for the application described by the given `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#`.

| Parameters ||
|---|---|
| `info` | [ApplicationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo.html#!>` | This value cannot be `null`. |

### getNameForUid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNameForUid(uid: Int): String?
```

**Deprecated:** *Deprecated in Java.*

Retrieve the official name associated with a uid. This name is guaranteed to never change, though it is possible for the underlying uid to be changed. That is, if you are storing information about uids in persistent storage, you should use the string returned by this function instead of the raw uid.

| Parameters ||
|---|---|
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The uid for which you would like to retrieve a name. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | Returns a unique name for the given uid, or null if the uid is not currently assigned. |

### getPackageArchiveInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackageArchiveInfo(
    archiveFilePath: String, 
    flags: Int
): PackageInfo?
```

**Deprecated:** *Deprecated in Java.*

Retrieve overall information about an application package defined in a package archive file Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPackageArchiveInfo(kotlin.String,%20android.content.pm.PackageManager.PackageInfoFlags)` when long flags are needed.

| Parameters ||
|---|---|
| `archiveFilePath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The path to the archive file. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#?` | A PackageInfo object containing information about the package archive. If the package could not be parsed, returns null. |

### getPackageGids

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackageGids(packageName: String): IntArray!
```

**Deprecated:** *Deprecated in Java.*

Return an array of all of the POSIX secondary group IDs that have been assigned to the given package.

Note that the same package may have different GIDs under different `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` on the same device.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The full name (i.e. com.google.apps.contacts) of the desired package. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` | Returns an int array of the assigned GIDs, or null if there are none. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if no such package is available to the caller. |

### getPackageGids

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackageGids(
    packageName: String, 
    flags: Int
): IntArray!
```

**Deprecated:** *Deprecated in Java.*

Return an array of all of the POSIX secondary group IDs that have been assigned to the given package.

Note that the same package may have different GIDs under different `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` on the same device. Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPackageGids(kotlin.String,%20android.content.pm.PackageManager.PackageInfoFlags)` when long flags are needed.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The full name (i.e. com.google.apps.contacts) of the desired package. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` | Returns an int array of the assigned gids, or null if there are none. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if no such package is available to the caller. |

### getPackageInfo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackageInfo(
    versionedPackage: VersionedPackage, 
    flags: Int
): PackageInfo!
```

**Deprecated:** *Deprecated in Java.*

Retrieve overall information about an application package that is installed on the system. This method can be used for retrieving information about packages for which multiple versions can be installed at the time. Currently only packages hosting static shared libraries can have multiple installed versions. The method can also be used to get info for a package that has a single version installed by passing `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#VERSION_CODE_HIGHEST:kotlin.Int` in the `https://developer.android.com/reference/kotlin/android/content/pm/VersionedPackage.html#` constructor. Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPackageInfo(android.content.pm.VersionedPackage,%20android.content.pm.PackageManager.PackageInfoFlags)` when long flags are needed.

| Parameters ||
|---|---|
| `versionedPackage` | [VersionedPackage](https://developer.android.com/reference/kotlin/android/content/pm/VersionedPackage.html#): The versioned package for which to query. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#!` | A PackageInfo object containing information about the package. If flag `MATCH_UNINSTALLED_PACKAGES` is set and if the package is not found in the list of installed applications, the package information is retrieved from the list of uninstalled applications (which includes installed applications as well as applications with data directory i.e. applications which had been deleted with `DELETE_KEEP_DATA` flag set). |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if no such package is available to the caller. |

### getPackageInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackageInfo(
    packageName: String, 
    flags: Int
): PackageInfo!
```

**Deprecated:** *Deprecated in Java.*

Retrieve overall information about an application package that is installed on the system. Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPackageInfo(kotlin.String,%20android.content.pm.PackageManager.PackageInfoFlags)` when long flags are needed.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The full name (i.e. com.google.apps.contacts) of the desired package. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#!` | A PackageInfo object containing information about the package. If flag `MATCH_UNINSTALLED_PACKAGES` is set and if the package is not found in the list of installed applications, the package information is retrieved from the list of uninstalled applications (which includes installed applications as well as applications with data directory i.e. applications which had been deleted with `DELETE_KEEP_DATA` flag set). |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if no such package is available to the caller. |

### getPackageInstaller

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackageInstaller(): PackageInstaller
```

**Deprecated:** *Deprecated in Java.*

Return interface that offers the ability to install, upgrade, and remove applications on the device.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.html#` | This value cannot be `null`. |

### getPackageUid

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackageUid(
    packageName: String, 
    flags: Int
): Int
```

**Deprecated:** *Deprecated in Java.*

Return the UID associated with the given package name.

Note that the same package will have different UIDs under different `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` on the same device. Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPackageUid(kotlin.String,%20android.content.pm.PackageManager.PackageInfoFlags)` when long flags are needed.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The full name (i.e. com.google.apps.contacts) of the desired package. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns an integer UID who owns the given package name. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if no such package is available to the caller. |

### getPackagesForUid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackagesForUid(uid: Int): Array<String!>?
```

**Deprecated:** *Deprecated in Java.*

Retrieve the names of all packages that are associated with a particular user id. In most cases, this will be a single package name, the package that has been assigned that user id. Where there are multiple packages sharing the same user id through the "sharedUserId" mechanism, all packages with that id will be returned.

| Parameters ||
|---|---|
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The user id for which you would like to retrieve the associated packages. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | Returns an array of one or more packages assigned to the user id, or null if there are no known packages with the given id. |

### getPackagesHoldingPermissions

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackagesHoldingPermissions(
    permissions: Array<String!>, 
    flags: Int
): MutableList<PackageInfo!>
```

**Deprecated:** *Deprecated in Java.*

Return a List of all installed packages that are currently holding any of the given permissions. Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getPackagesHoldingPermissions(kotlin.Array,%20android.content.pm.PackageManager.PackageInfoFlags)` when long flags are needed.

| Parameters ||
|---|---|
| `permissions` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#!>` | A List of PackageInfo objects, one for each installed package that holds any of the permissions that were provided, containing information about the package. If no installed packages hold any of the permissions, an empty list is returned. If flag `MATCH_UNINSTALLED_PACKAGES` is set, the package information is retrieved from the list of uninstalled applications (which includes installed applications as well as applications with data directory i.e. applications which had been deleted with `DELETE_KEEP_DATA` flag set). This value cannot be `null`. |

### getPermissionGroupInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPermissionGroupInfo(
    name: String, 
    flags: Int
): PermissionGroupInfo
```

**Deprecated:** *Deprecated in Java.*

Retrieve all of the information we know about a particular group of permissions.

| Parameters ||
|---|---|
| `groupName` | The fully qualified name (i.e. com.google.permission_group.APPS) of the permission you are interested in. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_META_DATA:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/PermissionGroupInfo.html#` | Returns a `https://developer.android.com/reference/kotlin/android/content/pm/PermissionGroupInfo.html#` containing information about the permission. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if a package with the given name cannot be found on the system. |

### getPermissionInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPermissionInfo(
    name: String, 
    flags: Int
): PermissionInfo!
```

**Deprecated:** *Deprecated in Java.*

Retrieve all of the information we know about a particular permission.

| Parameters ||
|---|---|
| `permName` | The fully qualified name (i.e. com.google.permission.LOGIN) of the permission you are interested in. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_META_DATA:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#!` | Returns a `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#` containing information about the permission. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if a package with the given name cannot be found on the system. |

### getPreferredActivities

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPreferredActivities(
    outFilters: MutableList<IntentFilter!>, 
    outActivities: MutableList<ComponentName!>, 
    packageName: String?
): Int
```

**Deprecated:** *Deprecated in Java.*

Retrieve all preferred activities, previously added with `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#addPreferredActivity(android.content.IntentFilter,%20kotlin.Int,%20kotlin.Array,%20android.content.ComponentName)`, that are currently registered with the system.

| Parameters ||
|---|---|
| `outFilters` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [IntentFilter](https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#)!\>: A required list in which to place the filters of all of the preferred activities. This value cannot be `null`. |
| `outActivities` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!\>: A required list in which to place the component names of all of the preferred activities. This value cannot be `null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: An optional package in which you would like to limit the list. If null, all activities will be returned; if non-null, only those activities in the given package are returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns the total number of registered preferred activities (the number of distinct IntentFilter records, not the number of unique activity components) that were found. |

### getPreferredPackages

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPreferredPackages(flags: Int): MutableList<PackageInfo!>
```

**Deprecated:** *Deprecated in Java.*

Retrieve the list of all currently configured preferred packages. The first package on the list is the most preferred, the last is the least preferred.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo.html#!>` | A List of PackageInfo objects, one for each preferred application, in order of preference. This value cannot be `null`. |

### getProviderInfo

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getProviderInfo(
    className: ComponentName, 
    flags: Int
): ProviderInfo
```

**Deprecated:** *Deprecated in Java.*

Retrieve all of the information we know about a particular content provider class. Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getProviderInfo(android.content.ComponentName,%20android.content.pm.PackageManager.ComponentInfoFlags)` when long flags are needed.

| Parameters ||
|---|---|
| `component` | The full component name (i.e. com.google.providers.media/com.google.providers.media. MediaProvider) of a ContentProvider class. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo.html#` | A `https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo.html#` object containing information about the provider. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if a package with the given name cannot be found on the system. |

### getReceiverInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getReceiverInfo(
    className: ComponentName, 
    flags: Int
): ActivityInfo
```

**Deprecated:** *Deprecated in Java.*

Retrieve all of the information we know about a particular receiver class. Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getReceiverInfo(android.content.ComponentName,%20android.content.pm.PackageManager.ComponentInfoFlags)` when long flags are needed.

| Parameters ||
|---|---|
| `component` | The full component name (i.e. com.google.apps.calendar/com.google.apps.calendar. CalendarAlarm) of a Receiver class. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#` | An `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#` containing information about the receiver. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if a package with the given name cannot be found on the system. |

### getResourcesForActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getResourcesForActivity(activityName: ComponentName): Resources
```

**Deprecated:** *Deprecated in Java.*

Retrieve the resources associated with an activity. Given the full name of an activity, retrieves the information about it and calls getResources() to return its application's resources. If the activity cannot be found, NameNotFoundException is thrown.

| Parameters ||
|---|---|
| `activityName` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#): Name of the activity whose resources are to be retrieved. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#` | Returns the application's Resources. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for the given application could not be loaded. |

### getResourcesForApplication

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getResourcesForApplication(app: ApplicationInfo): Resources
```

**Deprecated:** *Deprecated in Java.*

Retrieve the resources for an application. Throws NameNotFoundException if the package is no longer installed.

| Parameters ||
|---|---|
| `app` | [ApplicationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#): Information about the desired application. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#` | Returns the application's Resources. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for the given application could not be loaded (most likely because it was uninstalled). |

### getResourcesForApplication

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getResourcesForApplication(appPackageName: String): Resources
```

**Deprecated:** *Deprecated in Java.*

Retrieve the resources associated with an application. Given the full package name of an application, retrieves the information about it and calls getResources() to return its application's resources. If the appPackageName cannot be found, NameNotFoundException is thrown.

| Parameters ||
|---|---|
| `packageName` | Package name of the application whose resources are to be retrieved. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#` | Returns the application's Resources. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for the given application could not be loaded. |

### getServiceInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getServiceInfo(
    className: ComponentName, 
    flags: Int
): ServiceInfo
```

**Deprecated:** *Deprecated in Java.*

Retrieve all of the information we know about a particular service class. Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getServiceInfo(android.content.ComponentName,%20android.content.pm.PackageManager.ComponentInfoFlags)` when long flags are needed.

| Parameters ||
|---|---|
| `component` | The full component name (i.e. com.google.apps.media/com.google.apps.media. BackgroundPlayback) of a Service class. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#` | A `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#` object containing information about the service. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if the component cannot be found on the system. |

### getSharedLibraries

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSharedLibraries(flags: Int): MutableList<SharedLibraryInfo!>
```

**Deprecated:** *Deprecated in Java.*

Get a list of shared libraries on the device. Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSharedLibraries(android.content.pm.PackageManager.PackageInfoFlags)` when long flags are needed.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): To filter the libraries to return. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo.html#!>` | This value cannot be `null`. |

### getSystemAvailableFeatures

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSystemAvailableFeatures(): Array<FeatureInfo!>
```

**Deprecated:** *Deprecated in Java.*

Get a list of features that are available on the system.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo.html#!>` | An array of FeatureInfo classes describing the features that are available on the system, or null if there are none(!!). |

### getSystemSharedLibraryNames

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSystemSharedLibraryNames(): Array<String!>?
```

**Deprecated:** *Deprecated in Java.*

Get a list of shared libraries that are available on the system.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | An array of shared library names that are available on the system, or null if none are installed. |

### getText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getText(
    packageName: String, 
    resid: Int, 
    appInfo: ApplicationInfo?
): CharSequence?
```

**Deprecated:** *Deprecated in Java.*

Retrieve text from a package. This is a low-level API used by the various package manager info structures (such as `https://developer.android.com/reference/kotlin/android/content/pm/ComponentInfo.html#` to implement retrieval of their associated labels and other text.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the package that this text is coming from. Cannot be null. |
| `resid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource identifier of the desired text. Cannot be 0. |
| `appInfo` | [ApplicationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#)?: Overall information about packageName. This may be null, in which case the application information will be retrieved for you if needed; if you already have this information around, it can be much more efficient to supply it here. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | Returns a CharSequence holding the requested text. Returns null if the text could not be found for any reason. |

### getUserBadgedDrawableForDensity

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUserBadgedDrawableForDensity(
    drawable: Drawable, 
    user: UserHandle, 
    badgeLocation: Rect?, 
    badgeDensity: Int
): Drawable
```

**Deprecated:** *Deprecated in Java.*

If the target user is a managed profile of the calling user or the caller is itself a managed profile, then this returns a badged copy of the given drawable allowing the user to distinguish it from the original drawable. The caller can specify the location in the bounds of the drawable to be badged where the badge should be applied as well as the density of the badge to be used.

If the original drawable is a BitmapDrawable and the backing bitmap is mutable as per `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#isMutable()`, the badging is performed in place and the original drawable is returned.

| Parameters ||
|---|---|
| `drawable` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#): The drawable to badge. This value cannot be `null`. |
| `user` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#): The target user. This value cannot be `null`. |
| `badgeLocation` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)?: Where in the bounds of the badged drawable to place the badge. If it's `null`, the badge is applied on top of the entire drawable being badged. |
| `badgeDensity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The optional desired density for the badge as per `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#densityDpi:kotlin.Int`. If it's not positive, the density of the display is used. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` | A drawable that combines the original drawable and a badge as determined by the system. This value cannot be `null`. |

### getUserBadgedIcon

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUserBadgedIcon(
    icon: Drawable, 
    user: UserHandle
): Drawable
```

**Deprecated:** *Deprecated in Java.*

If the target user is a managed profile, then this returns a badged copy of the given icon to be able to distinguish it from the original icon. For badging an arbitrary drawable use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getUserBadgedDrawableForDensity(android.graphics.drawable.Drawable,%20android.os.UserHandle,%20android.graphics.Rect,%20kotlin.Int)`.

If the original drawable is a BitmapDrawable and the backing bitmap is mutable as per `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#isMutable()`, the badging is performed in place and the original drawable is returned.

| Parameters ||
|---|---|
| `drawable` | The drawable to badge. This value cannot be `null`. |
| `user` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#): The target user. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` | A drawable that combines the original icon and a badge as determined by the system. This value cannot be `null`. |

### getUserBadgedLabel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUserBadgedLabel(
    label: CharSequence, 
    user: UserHandle
): CharSequence
```

**Deprecated:** *Deprecated in Java.*

If the target user is a managed profile of the calling user or the caller is itself a managed profile, then this returns a copy of the label with badging for accessibility services like talkback. E.g. passing in "Email" and it might return "Work Email" for Email in the work profile.

| Parameters ||
|---|---|
| `label` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): The label to change. This value cannot be `null`. |
| `user` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#): The target user. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` | A label that combines the original label and a badge as determined by the system. This value cannot be `null`. |

### getWhitelistedRestrictedPermissions

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWhitelistedRestrictedPermissions(
    packageName: String, 
    whitelistFlags: Int
): MutableSet<String!>
```

**Deprecated:** *Deprecated in Java.*

Gets the restricted permissions that have been whitelisted and the app is allowed to have them granted in their full form.

Permissions can be hard restricted which means that the app cannot hold them or soft restricted where the app can hold the permission but in a weaker form. Whether a permission is `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#FLAG_HARD_RESTRICTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#FLAG_SOFT_RESTRICTED:kotlin.Int` depends on the permission declaration. Whitelisting a hard restricted permission allows for the to hold that permission and whitelisting a soft restricted permission allows the app to hold the permission in its full, unrestricted form.

<br />

There are four allowlists:
1. one for cases where the system permission policy whitelists a permission This list corresponds to the`https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_SYSTEM:kotlin.Int` flag. Can only be accessed by pre-installed holders of a dedicated permission.
2. one for cases where the system whitelists the permission when upgrading from an OS version in which the permission was not restricted to an OS version in which the permission is restricted. This list corresponds to the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_UPGRADE:kotlin.Int` flag. Can be accessed by pre-installed holders of a dedicated permission or the installer on record.
3. one for cases where the installer of the package whitelists a permission. This list corresponds to the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_INSTALLER:kotlin.Int` flag. Can be accessed by pre-installed holders of a dedicated permission or the installer on record.

**Note:**In retrospect it would have been preferred to use more inclusive terminology when naming this API. Similar APIs added will refrain from using the term "whitelist".

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `whitelistFlag` | The flag to determine which whitelist to query. Only one flag can be passed.s. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_INSTALLER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_UPGRADE:kotlin.Int` |
| `whitelistFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_INSTALLER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_UPGRADE:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if you try to access a whitelist that you have no access to. |

### getXml

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getXml(
    packageName: String, 
    resid: Int, 
    appInfo: ApplicationInfo?
): XmlResourceParser?
```

**Deprecated:** *Deprecated in Java.*

Retrieve an XML file from a package. This is a low-level API used to retrieve XML meta data.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the package that this xml is coming from. Cannot be null. |
| `resid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource identifier of the desired xml. Cannot be 0. |
| `appInfo` | [ApplicationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#)?: Overall information about packageName. This may be null, in which case the application information will be retrieved for you if needed; if you already have this information around, it can be much more efficient to supply it here. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser.html#?` | Returns an XmlPullParser allowing you to parse out the XML data. Returns null if the xml resource could not be found for any reason. |

### hasSigningCertificate

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasSigningCertificate(
    uid: Int, 
    certificate: ByteArray, 
    type: Int
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Searches the set of signing certificates by which the package(s) for the given uid has proven to have been signed. For multiple packages sharing the same uid, this will return the signing certificates found in the signing history of the "newest" package, where "newest" indicates the package with the newest signing certificate in the shared uid group. This method should be used instead of `getPackageInfo` with `GET_SIGNATURES` since it takes into account the possibility of signing certificate rotation, except in the case of packages that are signed by multiple certificates, for which signing certificate rotation is not supported. This method is analogous to using `getPackagesForUid` followed by `getPackageInfo` with `GET_SIGNING_CERTIFICATES`, selecting the `PackageInfo` of the newest-signed bpackage , and finally searching through the resulting `signingInfo` field to see if the desired certificate is there.

| Parameters ||
|---|---|
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): uid whose signing certificates to check |
| `certificate` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): signing certificate for which to search. This value cannot be `null`. |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#CERT_INPUT_RAW_X509:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#CERT_INPUT_SHA256:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this package was or is signed by exactly the certificate `certificate` |

### hasSigningCertificate

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasSigningCertificate(
    packageName: String, 
    certificate: ByteArray, 
    type: Int
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Searches the set of signing certificates by which the given package has proven to have been signed. This should be used instead of `getPackageInfo` with `GET_SIGNATURES` since it takes into account the possibility of signing certificate rotation, except in the case of packages that are signed by multiple certificates, for which signing certificate rotation is not supported. This method is analogous to using `getPackageInfo` with `GET_SIGNING_CERTIFICATES` and then searching through the resulting `signingInfo` field to see if the desired certificate is present.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): package whose signing certificates to check. This value cannot be `null`. |
| `certificate` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): signing certificate for which to search. This value cannot be `null`. |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#CERT_INPUT_RAW_X509:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#CERT_INPUT_SHA256:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this package was or is signed by exactly the certificate `certificate` |

### hasSystemFeature

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasSystemFeature(name: String): Boolean
```

**Deprecated:** *Deprecated in Java.*

Check whether the given feature name is one of the available features as returned by `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()`. This tests for the presence of *any* version of the given feature name; use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String,%20kotlin.Int)` to check for a minimum version.

| Parameters ||
|---|---|
| `featureName` | This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the devices supports the feature, else false. |

### hasSystemFeature

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasSystemFeature(
    name: String, 
    version: Int
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Check whether the given feature name and version is one of the available features as returned by `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getSystemAvailableFeatures()`. Since features are defined to always be backwards compatible, this returns true if the available feature version is greater than or equal to the requested version.

| Parameters ||
|---|---|
| `featureName` | This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the devices supports the feature, else false. |

### isDeviceUpgrading

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDeviceUpgrading(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if the device is upgrading, such as first boot after OTA.

### isInstantApp

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isInstantApp(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Gets whether this application is an instant app.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether caller is an instant app. |

### isInstantApp

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isInstantApp(packageName: String): Boolean
```

**Deprecated:** *Deprecated in Java.*

Gets whether the given package is an instant app.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The package to check. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the given package is an instant app. |

### isPermissionRevokedByPolicy

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isPermissionRevokedByPolicy(
    permName: String, 
    pkgName: String
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks whether a particular permissions has been revoked for a package by policy. Typically the device owner or the profile owner may apply such a policy. The user cannot grant policy revoked permissions, hence the only way for an app to get such a permission is by a policy change.

| Parameters ||
|---|---|
| `permName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the permission you are checking for. This value cannot be `null`. |
| `packageName` | The name of the package you are checking against. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the permission is restricted by policy. |

### isSafeMode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isSafeMode(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return whether the device has been booted into safe mode.

### queryBroadcastReceivers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryBroadcastReceivers(
    intent: Intent, 
    flags: Int
): MutableList<ResolveInfo!>
```

**Deprecated:** *Deprecated in Java.*

Retrieve all receivers that can handle a broadcast of the given intent. Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryBroadcastReceivers(android.content.Intent,%20android.content.pm.PackageManager.ResolveInfoFlags)` when long flags are needed.

| Parameters ||
|---|---|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#): The desired intent as per resolveActivity(). This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#!>` | Returns a List of ResolveInfo objects containing one entry for each matching receiver, ordered from best to worst. If there are no matching receivers, returns an empty list. This value cannot be `null`. |

### queryContentProviders

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryContentProviders(
    processName: String?, 
    uid: Int, 
    flags: Int
): MutableList<ProviderInfo!>
```

**Deprecated:** *Deprecated in Java.*

Retrieve content provider information.

*Note: unlike most other methods, an empty result set is indicated by a null return instead of an empty list.* Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryContentProviders(kotlin.String,%20kotlin.Int,%20android.content.pm.PackageManager.ComponentInfoFlags)` when long flags are needed.

| Parameters ||
|---|---|
| `processName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: If non-null, limits the returned providers to only those that are hosted by the given process. If null, all content providers are returned. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): If processName is non-null, this is the required uid owning the requested content providers. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo.html#!>` | A list of `https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo.html#` objects containing one entry for each provider either matching processName or, if processName is null, all known content providers. *If there are no matching providers, null is returned.* |

### queryInstrumentation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryInstrumentation(
    targetPackage: String, 
    flags: Int
): MutableList<InstrumentationInfo!>
```

**Deprecated:** *Deprecated in Java.*

Retrieve information about available instrumentation code. May be used to retrieve either all instrumentation code, or only the code targeting a particular package.

| Parameters ||
|---|---|
| `targetPackage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): If null, all instrumentation is returned; only the instrumentation targeting this package name is returned. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_META_DATA:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo.html#!>` | A list of `https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo.html#` objects containing one entry for each matching instrumentation. If there are no instrumentation available, returns an empty list. This value cannot be `null`. |

### queryIntentActivities

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryIntentActivities(
    intent: Intent, 
    flags: Int
): MutableList<ResolveInfo!>
```

**Deprecated:** *Deprecated in Java.*

Retrieve all activities that can be performed for the given intent. Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryIntentActivities(android.content.Intent,%20android.content.pm.PackageManager.ResolveInfoFlags)` when long flags are needed.

| Parameters ||
|---|---|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#): The desired intent as per resolveActivity(). This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. The most important is `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DEFAULT_ONLY:kotlin.Int`, to limit the resolution to only those activities that support the `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_DEFAULT:kotlin.String`. Or, set `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_ALL:kotlin.Int` to prevent any filtering of the results. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#!>` | Returns a List of ResolveInfo objects containing one entry for each matching activity, ordered from best to worst. In other words, the first item is what would be returned by #resolveActivity. If there are no matching activities, an empty list is returned. This value cannot be `null`. |

### queryIntentActivityOptions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryIntentActivityOptions(
    caller: ComponentName?, 
    specifics: Array<Intent!>?, 
    intent: Intent, 
    flags: Int
): MutableList<ResolveInfo!>
```

**Deprecated:** *Deprecated in Java.*

Retrieve a set of activities that should be presented to the user as similar options. This is like #queryIntentActivities, except it also allows you to supply a list of more explicit Intents that you would like to resolve to particular options, and takes care of returning the final ResolveInfo list in a reasonable order, with no duplicates, based on those inputs. Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryIntentActivityOptions(android.content.ComponentName,%20kotlin.collections.MutableList,%20android.content.Intent,%20android.content.pm.PackageManager.ResolveInfoFlags)` when long flags are needed.

| Parameters ||
|---|---|
| `caller` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)?: The class name of the activity that is making the request. This activity will never appear in the output list. Can be null. |
| `specifics` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!\>?: An array of Intents that should be resolved to the first specific results. Can be null. |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#): The desired intent as per resolveActivity(). This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. The most important is `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DEFAULT_ONLY:kotlin.Int`, to limit the resolution to only those activities that support the `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_DEFAULT:kotlin.String`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#!>` | Returns a List of ResolveInfo objects containing one entry for each matching activity. The list is ordered first by all of the intents resolved in specifics and then any additional activities that can handle intent but did not get included by one of the specifics intents. If there are no matching activities, an empty list is returned. This value cannot be `null`. |

### queryIntentContentProviders

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryIntentContentProviders(
    intent: Intent, 
    flags: Int
): MutableList<ResolveInfo!>
```

**Deprecated:** *Deprecated in Java.*

Retrieve all providers that can match the given intent. Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryIntentContentProviders(android.content.Intent,%20android.content.pm.PackageManager.ResolveInfoFlags)` when long flags are needed.

| Parameters ||
|---|---|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#): An intent containing all of the desired specification (action, data, type, category, and/or component). This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#!>` | Returns a List of ResolveInfo objects containing one entry for each matching provider, ordered from best to worst. If there are no matching services, returns an empty list. This value cannot be `null`. |

### queryIntentServices

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryIntentServices(
    intent: Intent, 
    flags: Int
): MutableList<ResolveInfo!>
```

**Deprecated:** *Deprecated in Java.*

Retrieve all services that can match the given intent. Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#queryIntentServices(android.content.Intent,%20android.content.pm.PackageManager.ResolveInfoFlags)` when long flags are needed.

| Parameters ||
|---|---|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#): The desired intent as per resolveService(). This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#!>` | Returns a List of ResolveInfo objects containing one entry for each matching service, ordered from best to worst. In other words, the first item is what would be returned by #resolveService. If there are no matching services, returns an empty list. This value cannot be `null`. |

### queryPermissionsByGroup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryPermissionsByGroup(
    group: String?, 
    flags: Int
): MutableList<PermissionInfo!>
```

**Deprecated:** *Deprecated in Java.*

Query for all of the permissions associated with a particular group.

| Parameters ||
|---|---|
| `permissionGroup` | The fully qualified name (i.e. com.google.permission.LOGIN) of the permission group you are interested in. Use `null` to find all of the permissions not associated with a group. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#GET_META_DATA:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#!>` | Returns a list of `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#` containing information about all of the permissions in the given group. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if a group with the given name cannot be found on the system. |

### removePackageFromPreferred

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removePackageFromPreferred(packageName: String): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### removePermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removePermission(name: String): Unit
```

**Deprecated:** *Deprecated in Java.*

Removes a permission that was previously added with `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#addPermission(android.content.pm.PermissionInfo)`. The same ownership rules apply -- you are only allowed to remove permissions that you are allowed to add.

| Parameters ||
|---|---|
| `permName` | The name of the permission to remove. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if you are not allowed to remove the given permission name. |

### removeWhitelistedRestrictedPermission

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeWhitelistedRestrictedPermission(
    packageName: String, 
    permission: String, 
    whitelistFlags: Int
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Removes a whitelisted restricted permission for an app.

Permissions can be hard restricted which means that the app cannot hold them or soft restricted where the app can hold the permission but in a weaker form. Whether a permission is `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#FLAG_HARD_RESTRICTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#FLAG_SOFT_RESTRICTED:kotlin.Int` depends on the permission declaration. Whitelisting a hard restricted permission allows for the to hold that permission and whitelisting a soft restricted permission allows the app to hold the permission in its full, unrestricted form.

<br />

There are four whitelists:
1. one for cases where the system permission policy whitelists a permission This list corresponds to the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_SYSTEM:kotlin.Int` flag. Can only be modified by pre-installed holders of a dedicated permission.
2. one for cases where the system whitelists the permission when upgrading from an OS version in which the permission was not restricted to an OS version in which the permission is restricted. This list corresponds to the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_UPGRADE:kotlin.Int` flag. Can be modified by pre-installed holders of a dedicated permission. The installer on record can only remove permissions from this whitelist.
3. one for cases where the installer of the package whitelists a permission. This list corresponds to the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_INSTALLER:kotlin.Int` flag. Can be modified by pre-installed holders of a dedicated permission or the installer on record.
4. one for cases where the system exempts the permission when upgrading from an OS version in which the permission was not restricted to an OS version in which the permission is restricted. This list corresponds to the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_UPGRADE:kotlin.Int` flag. Can be modified by pre-installed holders of a dedicated permission. The installer on record can only remove permissions from this allowlist.

You need to specify the whitelists for which to set the whitelisted permissions which will clear the previous whitelisted permissions and replace them with the provided ones.

**Note:**In retrospect it would have been preferred to use more inclusive terminology when naming this API. Similar APIs added will refrain from using the term "whitelist".

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `permName` | The whitelisted permission to remove. This value cannot be `null`. |
| `whitelistFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_INSTALLER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FLAG_PERMISSION_WHITELIST_UPGRADE:kotlin.Int` |
| `permission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the permission was removed from the whitelist. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if you try to modify a whitelist that you have no access to. |

### resolveActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun resolveActivity(
    intent: Intent, 
    flags: Int
): ResolveInfo?
```

**Deprecated:** *Deprecated in Java.*

Determine the best action to perform for a given Intent. This is how `https://developer.android.com/reference/kotlin/android/content/Intent.html#resolveActivity(android.content.pm.PackageManager)` finds an activity if a class has not been explicitly specified.

*Note:* if using an implicit Intent (without an explicit ComponentName specified), be sure to consider whether to set the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DEFAULT_ONLY:kotlin.Int` only flag. You need to do so to resolve the activity in the same way that `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#resolveActivity(android.content.pm.PackageManager)` do.
Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#resolveActivity(android.content.Intent,%20android.content.pm.PackageManager.ResolveInfoFlags)` when long flags are needed.

| Parameters ||
|---|---|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#): An intent containing all of the desired specification (action, data, type, category, and/or component). This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. The most important is `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#MATCH_DEFAULT_ONLY:kotlin.Int`, to limit the resolution to only those activities that support the `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_DEFAULT:kotlin.String`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#?` | Returns a ResolveInfo object containing the final activity intent that was determined to be the best action. Returns null if no matching activity was found. If multiple matching activities are found and there is no default set, returns a ResolveInfo object containing something else, such as the activity resolver. |

### resolveContentProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun resolveContentProvider(
    name: String, 
    flags: Int
): ProviderInfo?
```

**Deprecated:** *Deprecated in Java.*

Find a single content provider by its authority.

Example:

```kotlin
Uri uri = Uri.parse("content://com.example.app.provider/table1");
  ProviderInfo info = packageManager.resolveContentProvider(uri.getAuthority(), flags);
  
```
Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#resolveContentProvider(kotlin.String,%20android.content.pm.PackageManager.ComponentInfoFlags)` when long flags are needed.

| Parameters ||
|---|---|
| `authority` | The authority of the provider to find. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo.html#?` | A `https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo.html#` object containing information about the provider. If a provider was not found, returns null. |

### resolveService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun resolveService(
    intent: Intent, 
    flags: Int
): ResolveInfo?
```

**Deprecated:** *Deprecated in Java.*

Determine the best service to handle for a given Intent. Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#resolveService(android.content.Intent,%20android.content.pm.PackageManager.ResolveInfoFlags)` when long flags are needed.

| Parameters ||
|---|---|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#): An intent containing all of the desired specification (action, data, type, category, and/or component). This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#?` | Returns a ResolveInfo object containing the final service intent that was determined to be the best action. Returns null if no matching service was found. |

### resolveServiceAsUser

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun resolveServiceAsUser(
    intent: Intent!, 
    flags: Int, 
    userId: Int
): ResolveInfo!
```

**Deprecated:** *Deprecated in Java.*

### setApplicationCategoryHint

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setApplicationCategoryHint(
    packageName: String, 
    categoryHint: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Provide a hint of what the `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#category:kotlin.Int` value should be for the given package.

This hint can only be set by the app which installed this package, as determined by `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getInstallerPackageName(kotlin.String)`.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the package to change the category hint for. This value cannot be `null`. |
| `categoryHint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the category hint to set. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#CATEGORY_UNDEFINED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#CATEGORY_GAME:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#CATEGORY_AUDIO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#CATEGORY_VIDEO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#CATEGORY_IMAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#CATEGORY_SOCIAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#CATEGORY_NEWS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#CATEGORY_MAPS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#CATEGORY_PRODUCTIVITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#CATEGORY_ACCESSIBILITY:kotlin.Int` |

### setApplicationEnabledSetting

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setApplicationEnabledSetting(
    packageName: String, 
    newState: Int, 
    flags: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the enabled setting for an application This setting will override any enabled state which may have been set by the application in its manifest. It also overrides the enabled state set in the manifest for any of the application's components. It does not override any enabled state set by `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#setComponentEnabledSetting(android.content.ComponentName,%20kotlin.Int,%20kotlin.Int)` for any of the application's components.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The package name of the application to enable. This value cannot be `null`. |
| `newState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new enabled state for the application. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_DISABLED_USER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_DISABLED_UNTIL_USED:kotlin.Int` |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Optional behavior flags. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#DONT_KILL_APP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SYNCHRONOUS:kotlin.Int` |

### setComponentEnabledSetting

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setComponentEnabledSetting(
    componentName: ComponentName, 
    newState: Int, 
    flags: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the enabled setting for a package component (activity, receiver, service, provider). This setting will override any enabled state which may have been set by the component in its manifest.

Consider using `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#setComponentEnabledSettings(kotlin.collections.MutableList)` if multiple components need to be updated atomically.

| Parameters ||
|---|---|
| `componentName` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#): The component to enable. This value cannot be `null`. |
| `newState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new enabled state for the component. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_DISABLED_USER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#COMPONENT_ENABLED_STATE_DISABLED_UNTIL_USED:kotlin.Int` |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Optional behavior flags. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#DONT_KILL_APP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#SYNCHRONOUS:kotlin.Int` |

### setInstallerPackageName

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInstallerPackageName(
    targetPackage: String, 
    installerPackageName: String?
): Unit
```

**Deprecated:** *Deprecated in Java.*

Change the installer associated with a given package. There are limitations on how the installer package can be changed; in particular:

- A SecurityException will be thrown if installerPackageName is not signed with the same certificate as the calling application.
- A SecurityException will be thrown if targetPackage already has an installer package, and that installer package is not signed with the same certificate as the calling application.

<br />

| Parameters ||
|---|---|
| `targetPackage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The installed package whose installer will be changed. This value cannot be `null`. |
| `installerPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The package name of the new installer. May be null to clear the association. |

### setInstantAppCookie

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInstantAppCookie(cookie: ByteArray): Boolean
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|---|---|
| `cookie` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): This value cannot be `null`. |

### updateInstantAppCookie

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateInstantAppCookie(cookie: ByteArray!): Unit
```

**Deprecated:** *Deprecated in Java.*

Updates the instant application cookie for the calling app. Non instant apps and apps that were instant but were upgraded to normal apps can still access this API. For instant apps this cookie is cached for some time after uninstall while for normal apps the cookie is deleted after the app is uninstalled. The cookie is always present while the app is installed. The cookie size is limited by `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getInstantAppCookieMaxBytes()`. Passing `null` or an empty array clears the cookie.

<br />

| Parameters ||
|---|---|
| `cookie` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the array exceeds max cookie size. |

### verifyPendingInstall

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun verifyPendingInstall(
    id: Int, 
    verificationCode: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Allows a package listening to the `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_NEEDS_VERIFICATION:kotlin.String` to respond to the package manager. The response must include the `verificationCode` which is one of `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#VERIFICATION_ALLOW:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#VERIFICATION_REJECT:kotlin.Int`.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): pending package identifier as passed via the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#EXTRA_VERIFICATION_ID:kotlin.String` Intent extra. |
| `verificationCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): either `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#VERIFICATION_ALLOW:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#VERIFICATION_REJECT:kotlin.Int`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller does not have the PACKAGE_VERIFICATION_AGENT permission. |
