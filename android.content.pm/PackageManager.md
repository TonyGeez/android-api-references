Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PackageManager

```
abstract class PackageManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.pm.PackageManager](PackageManager.md) |

Known Direct Subclasses [MockPackageManager](../android.test.mock/MockPackageManager.md) [MockPackageManager](../android.test.mock/MockPackageManager.md) A mock PackageManager class.

Class for retrieving various kinds of information related to the application packages that are currently installed on the device. You can find this class through getPackageManager.

**Note:** If your app targets Android 11 (API level 30) or higher, the methods in this class each return a filtered list of apps. Learn more about how to [manage package visibility](../training/basics/intents/package-visibility.md).

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.ApplicationInfoFlags` Specific flags used for retrieving application info. |
| | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.ComponentEnabledSetting` The class containing the enabled setting of a package component. |
| | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.ComponentInfoFlags` Specific flags used for retrieving component info. |
| --- | --- |
| open | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.NameNotFoundException` This exception is thrown when a given package, application, or component name cannot be found. |
| abstract | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.OnChecksumsReadyListener` Listener that gets notified when checksums are available. |
| | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.PackageInfoFlags` Specific flags used for retrieving package info. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property` A property value set within the manifest. |
| | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.ResolveInfoFlags` Specific flags used for retrieving resolve info. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#CERT_INPUT_RAW_X509:kotlin.Int` Certificate input bytes: the input bytes represent an encoded X. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#CERT_INPUT_SHA256:kotlin.Int` Certificate input bytes: the input bytes represent the SHA256 output of an encoded X. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DEFAULT:kotlin.Int` Flag for setApplicationEnabledSetting and setComponentEnabledSetting: This component or application is in its default enabled state (as specified in its manifest). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DISABLED:kotlin.Int` Flag for setApplicationEnabledSetting and setComponentEnabledSetting: This component or application has been explicitly disabled, regardless of what it has specified in its manifest. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DISABLED_UNTIL_USED:kotlin.Int` Flag for setApplicationEnabledSetting only: This application should be considered, until the point where the user actually wants to use it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DISABLED_USER:kotlin.Int` Flag for setApplicationEnabledSetting only: The user has explicitly disabled the application, regardless of what it has specified in its manifest. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_ENABLED:kotlin.Int` Flag for setApplicationEnabledSetting and setComponentEnabledSetting: This component or application has been explictily enabled, regardless of what it has specified in its manifest. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#DELETE_ARCHIVE:kotlin.Int` Flag parameter for uninstall to indicate that the deletion is an archival. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#DONT_KILL_APP:kotlin.Int` Flag parameter for setComponentEnabledSetting to indicate that you don't want to kill the app containing the component. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#EXTRA_VERIFICATION_ID:kotlin.String` Extra field name for the ID of a package pending verification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#EXTRA_VERIFICATION_RESULT:kotlin.String` Extra field name for the result of a verification, either `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#VERIFICATION_ALLOW:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#VERIFICATION_REJECT:kotlin.Int`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_ACTIVITIES_ON_SECONDARY_DISPLAYS:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports running activities on secondary displays. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_APP_WIDGETS:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports app widgets. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_AUDIO_LOW_LATENCY:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device's audio pipeline is low-latency, more suitable for audio applications sensitive to delays or lag in sound input or output. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_AUDIO_OUTPUT:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes at least one form of audio output, as defined in the Android Compatibility Definition Document (CDD) [section 7.8 Audio](https://source.android.com/compatibility/android-cdd#7_8_audio). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_AUDIO_PRO:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has professional audio level of functionality and performance. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_AUDIO_SPATIAL_HEADTRACKING_LOW_LATENCY:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature which indicates whether head tracking for spatial audio operates with low-latency, as defined by the CDD criteria for the feature. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_AUTOFILL:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports autofill of user credentials, addresses, credit cards, etc via integration with `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_AUTOMOTIVE:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: This is a device dedicated to showing UI on a vehicle headunit. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_BACKUP:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device can perform backup and restore operations on installed applications. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_BLUETOOTH:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device is capable of communicating with other devices via Bluetooth. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_BLUETOOTH_LE:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device is capable of communicating with other devices via Bluetooth Low Energy radio. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_BLUETOOTH_LE_CHANNEL_SOUNDING:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device is capable of ranging with other devices using channel sounding via Bluetooth Low Energy radio. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_CAMERA:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a camera facing away from the screen. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_CAMERA_ANY:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has at least one camera pointing in some direction, or can support an external or a `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice.html#` camera being connected to it. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_CAMERA_AR:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: At least one of the cameras on the device supports the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_MOTION_TRACKING:kotlin.Int` capability level. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_CAMERA_AUTOFOCUS:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device's camera supports auto-focus. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_CAMERA_CAPABILITY_MANUAL_POST_PROCESSING:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: At least one of the cameras on the device supports the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_MANUAL_POST_PROCESSING:kotlin.Int` capability level. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_CAMERA_CAPABILITY_MANUAL_SENSOR:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: At least one of the cameras on the device supports the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_MANUAL_SENSOR:kotlin.Int` capability level. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_CAMERA_CAPABILITY_RAW:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: At least one of the cameras on the device supports the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_RAW:kotlin.Int` capability level. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_CAMERA_CONCURRENT:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device's main front and back cameras can stream concurrently as described in getConcurrentCameraIds. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_CAMERA_EXTERNAL:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device can support having an external camera connected to it. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_CAMERA_FLASH:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device's camera supports flash. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_CAMERA_FRONT:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a front facing camera. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_CAMERA_LEVEL_FULL:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: At least one of the cameras on the device supports the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` capability level. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_CANT_SAVE_STATE:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports the `https://developer.android.com/reference/kotlin/android/R.attr.html#cantSaveState:kotlin.Int` API. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports android. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_CONNECTION_SERVICE:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The Connection Service API is enabled on the device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_CONSUMER_IR:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device is capable of communicating with consumer IR devices. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_CONTROLS:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports a system interface for the user to select and bind device control services provided by applications. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_CREDENTIALS:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports retrieval of user credentials, via integration with credential providers. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_DEVICE_ADMIN:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports device policy enforcement via device admins. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_DEVICE_ID_ATTESTATION:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a KeyMint (or Keymaster) implementation that supports device ID attestation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_DEVICE_LOCK:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports locking (for example, by a financing provider in case of a missed payment). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_EMBEDDED:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: This is a device for IoT and may not have an UI. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_ETHERNET:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: This device supports ethernet. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_EXPANDED_PICTURE_IN_PICTURE:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports expanded picture-in-picture multi-window mode. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_FACE:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has biometric hardware to perform face authentication. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_FAKETOUCH:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device does not have a touch screen, but does support touch emulation for basic events. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_FAKETOUCH_MULTITOUCH_DISTINCT:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device does not have a touch screen, but does support touch emulation for basic events that supports distinct tracking of two or more fingers. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_FAKETOUCH_MULTITOUCH_JAZZHAND:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device does not have a touch screen, but does support touch emulation for basic events that supports tracking a hand of fingers (5 or more fingers) fully independently. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_FINGERPRINT:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has biometric hardware to detect a fingerprint. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_FREEFORM_WINDOW_MANAGEMENT:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports freeform window management. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_GAMEPAD:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has all of the inputs necessary to be considered a compatible game controller, or includes a compatible game controller in the box. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_HARDWARE_KEYSTORE:kotlin.String` Feature for getSystemAvailableFeatures and hasSystemFeature: If this feature is supported, the device implements the Android Keystore backed by an isolated execution environment. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_HIFI_SENSORS:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports high fidelity sensor processing capabilities. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_HOME_SCREEN:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports a home screen that is replaceable by third party applications. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_IDENTITY_CREDENTIAL_HARDWARE:kotlin.String` Feature for getSystemAvailableFeatures and hasSystemFeature: If this feature is supported, the device supports `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore.html#` implemented in secure hardware at the given feature version. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_IDENTITY_CREDENTIAL_HARDWARE_DIRECT_ACCESS:kotlin.String` Feature for getSystemAvailableFeatures and hasSystemFeature: If this feature is supported, the device supports `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore.html#` implemented in secure hardware with direct access at the given feature version. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_INPUT_METHODS:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports adding new input methods implemented with the `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#` API. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_IPSEC_TUNNELS:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has the requisite kernel support for multinetworking-capable IPsec tunnels. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_IPSEC_TUNNEL_MIGRATION:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has the requisite kernel support for migrating IPsec tunnels to new source/destination addresses. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_IRIS:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has biometric hardware to perform iris authentication. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_KEYSTORE_APP_ATTEST_KEY:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a Keystore implementation that can create application-specific attestation keys. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_KEYSTORE_LIMITED_USE_KEY:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a Keystore implementation that can enforce limited use key in hardware with any max usage count (including count equals to 1). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_KEYSTORE_SINGLE_USE_KEY:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a Keystore implementation that can only enforce limited use key in hardware with max usage count equals to 1. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_LEANBACK:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports leanback UI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_LEANBACK_ONLY:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports only leanback UI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_LIVE_TV:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports live TV and can display contents from TV inputs implemented with the `https://developer.android.com/reference/kotlin/android/media/tv/TvInputService.html#` API. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_LIVE_WALLPAPER:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports live wallpapers. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_LOCATION:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports one or more methods of reporting current location. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_LOCATION_GPS:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a Global Positioning System receiver and can report precise location. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_LOCATION_NETWORK:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device can report location with coarse accuracy using a network-based geolocation system. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_MANAGED_USERS:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports creating secondary users and managed profiles via `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_MICROPHONE:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device can record audio via a microphone. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_MIDI:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a full implementation of the android. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_NEURAL_PROCESSING_UNIT:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: This device has a NPU (Neural Processing Unit) or similar hardware for accelerating AI workloads. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_NFC:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device can communicate using Near-Field Communications (NFC), acting as a reader. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_NFC_BEAM:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The Beam API is enabled on the device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_NFC_HOST_CARD_EMULATION:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports host- based NFC card emulation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_NFC_HOST_CARD_EMULATION_NFCF:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports host- based NFC-F card emulation. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_NFC_OFF_HOST_CARD_EMULATION_ESE:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports eSE- based NFC card emulation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_NFC_OFF_HOST_CARD_EMULATION_UICC:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports uicc- based NFC card emulation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_OPENGLES_DEQP_LEVEL:kotlin.String` Feature for getSystemAvailableFeatures and hasSystemFeature: If this feature is supported, the feature version specifies a date such that the device is known to pass the OpenGLES dEQP test suite associated with that date. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_OPENGLES_EXTENSION_PACK:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports the OpenGL ES [Android Extension Pack](http://www.khronos.org/registry/gles/extensions/ANDROID/ANDROID_extension_pack_es31a.txt). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_PC:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: This is a device dedicated to be primarily used with keyboard, mouse or touchpad. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_PICTURE_IN_PICTURE:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports picture-in-picture multi-window mode. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_PRINTING:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports printing. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_RAM_LOW:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device's isLowRamDevice method returns true. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_RAM_NORMAL:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device's isLowRamDevice method returns false. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SCREEN_LANDSCAPE:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports landscape orientation screens. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SCREEN_PORTRAIT:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports portrait orientation screens. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SECURELY_REMOVES_USERS:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports secure removal of users. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SECURE_LOCK_SCREEN:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a secure implementation of keyguard, meaning the device supports PIN, pattern and password as defined in Android CDD |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SECURITY_MODEL_COMPATIBLE:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device is compatible with Android's security model. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SENSOR_ACCELEROMETER:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes an accelerometer. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SENSOR_ACCELEROMETER_LIMITED_AXES:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a limited axes accelerometer. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SENSOR_ACCELEROMETER_LIMITED_AXES_UNCALIBRATED:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes an uncalibrated limited axes accelerometer. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SENSOR_AMBIENT_TEMPERATURE:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes an ambient temperature sensor. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SENSOR_BAROMETER:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a barometer (air pressure sensor.) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SENSOR_COMPASS:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a magnetometer (compass). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SENSOR_DYNAMIC_HEAD_TRACKER:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports exposing head tracker sensors from peripheral devices via the dynamic sensors API. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SENSOR_GYROSCOPE:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a gyroscope. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SENSOR_GYROSCOPE_LIMITED_AXES:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a limited axes gyroscope. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SENSOR_GYROSCOPE_LIMITED_AXES_UNCALIBRATED:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes an uncalibrated limited axes gyroscope. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SENSOR_HEADING:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a heading sensor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SENSOR_HEART_RATE:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a heart rate monitor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SENSOR_HEART_RATE_ECG:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The heart rate sensor on this device is an Electrocardiogram. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SENSOR_HINGE_ANGLE:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a hinge angle sensor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SENSOR_LIGHT:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a light sensor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SENSOR_PROXIMITY:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a proximity sensor. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SENSOR_RELATIVE_HUMIDITY:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a relative humidity sensor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SENSOR_STEP_COUNTER:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a hardware step counter. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SENSOR_STEP_DETECTOR:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a hardware step detector. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SE_OMAPI_ESE:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Open Mobile API capable eSE-based secure elements. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SE_OMAPI_SD:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Open Mobile API capable SD-based secure elements. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SE_OMAPI_UICC:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Open Mobile API capable UICC-based secure elements. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SIP:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The SIP API is enabled on the device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SIP_VOIP:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports SIP-based VOIP. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_STRONGBOX_KEYSTORE:kotlin.String` Feature for getSystemAvailableFeatures, hasSystemFeature, and hasSystemFeature: If this feature is supported, the device implements the Android Keystore backed by a dedicated secure processor referred to as [StrongBox](https://source.android.com/security/best-practices/hardware#strongbox-keymaster). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELECOM:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Telecom Service APIs. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a telephony radio with data communication support. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY_CALLING:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Telephony APIs for calling service. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY_CDMA:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a CDMA telephony stack. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY_DATA:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Telephony APIs for data service. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY_EUICC:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports embedded subscriptions on eUICCs. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY_EUICC_MEP:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports multiple enabled profiles on eUICCs. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY_GSM:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a GSM telephony stack. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY_IMS:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports attaching to IMS implementations using the ImsService API in telephony. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY_MBMS:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports cell-broadcast reception using the MBMS APIs. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY_MESSAGING:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Telephony APIs for SMS and MMS. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Telephony APIs for the radio access. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Telephony APIs for the subscription. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEVISION:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: This is a device dedicated to showing UI on a television. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_THREAD_NETWORK:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device is capable of communicating with other devices via [Thread](https://www.threadgroup.org) networking protocol. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TOUCHSCREEN:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device's display has a touch screen. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TOUCHSCREEN_MULTITOUCH:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device's touch screen supports multitouch sufficient for basic two-finger gesture detection. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TOUCHSCREEN_MULTITOUCH_DISTINCT:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device's touch screen is capable of tracking two or more fingers fully independently. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TOUCHSCREEN_MULTITOUCH_JAZZHAND:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device's touch screen is capable of tracking a full hand of fingers fully independently -- that is, 5 or more simultaneous independent pointers. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_USB_ACCESSORY:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports connecting to USB accessories. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_USB_HOST:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports connecting to USB devices as the USB host. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_UWB:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device is capable of communicating with other devices via ultra wideband. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_VERIFIED_BOOT:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports verified boot. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_VR_HEADTRACKING:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device implements headtracking suitable for a VR device. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_VR_MODE:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device implements an optimized mode for virtual reality (VR) applications that handles stereoscopic rendering of notifications, and disables most monocular system UI components while a VR application has user focus. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_VR_MODE_HIGH_PERFORMANCE:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device implements an optimized mode for virtual reality (VR) applications that handles stereoscopic rendering of notifications, disables most monocular system UI components while a VR application has user focus and meets extra CDD requirements to provide a high-quality VR experience. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_VULKAN_DEQP_LEVEL:kotlin.String` Feature for getSystemAvailableFeatures and hasSystemFeature: If this feature is supported, the feature version specifies a date such that the device is known to pass the Vulkan dEQP test suite associated with that date. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_VULKAN_HARDWARE_COMPUTE:kotlin.String` Feature for getSystemAvailableFeatures and hasSystemFeature: If this feature is supported, the Vulkan implementation on this device is hardware accelerated, and the Vulkan native API will enumerate at least one `VkPhysicalDevice`, and the feature version will indicate what level of optional compute features that device supports beyond the Vulkan 1. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_VULKAN_HARDWARE_LEVEL:kotlin.String` Feature for getSystemAvailableFeatures and hasSystemFeature: If this feature is supported, the Vulkan implementation on this device is hardware accelerated, and the Vulkan native API will enumerate at least one `VkPhysicalDevice`, and the feature version will indicate what level of optional hardware features limits it supports. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_VULKAN_HARDWARE_VERSION:kotlin.String` Feature for getSystemAvailableFeatures and hasSystemFeature: If this feature is supported, the Vulkan implementation on this device is hardware accelerated, and the feature version will indicate the highest `VkPhysicalDeviceProperties::apiVersion` supported by the physical devices that support the hardware level indicated by `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_VULKAN_HARDWARE_LEVEL:kotlin.String`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_WALLET_LOCATION_BASED_SUGGESTIONS:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports showing location-based suggestions for wallet cards provided by the default payment app. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_WATCH:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: This is a device dedicated to showing UI on a watch. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_WEBVIEW:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a full implementation of the android. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_WIFI:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports WiFi (802.11) networking. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_WIFI_AWARE:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Wi-Fi Aware. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_WIFI_DIRECT:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Wi-Fi Direct networking. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_WIFI_PASSPOINT:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Wi-Fi Passpoint and all Passpoint related APIs in `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#` are supported. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_WIFI_RTT:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Wi-Fi RTT (IEEE 802.11mc). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_WINDOW_MAGNIFICATION:kotlin.String` Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports window magnification. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_INSTALLER:kotlin.Int` Permission whitelist flag: permissions whitelisted by the installer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_SYSTEM:kotlin.Int` Permission whitelist flag: permissions whitelisted by the system. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_UPGRADE:kotlin.Int` Permission whitelist flag: permissions whitelisted by the system when upgrading from an OS version where the permission was not restricted to an OS version where the permission is restricted. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_ACTIVITIES:kotlin.Int` PackageInfo flag: return information about activities in the package in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#activities:kotlin.Array`. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_APP_LOCK_INFO:kotlin.Long` ApplicationInfo, ComponentInfo, and ResolveInfo flag: return the `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#isAppLockSupported:kotlin.Boolean` and `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#isAppLockEnabled:kotlin.Boolean` associated with an application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_ATTRIBUTIONS:kotlin.Int` <br /> |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_ATTRIBUTIONS_LONG:kotlin.Long` PackageInfo flag: return all attributions declared in the package manifest |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_CONFIGURATIONS:kotlin.Int` PackageInfo flag: return information about hardware preferences in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#configPreferences:kotlin.Array`, and requested features in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#reqFeatures:kotlin.Array` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#featureGroups:kotlin.Array`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_DISABLED_COMPONENTS:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_DISABLED_UNTIL_USED_COMPONENTS:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_GIDS:kotlin.Int` PackageInfo flag: return the `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#gids:kotlin.IntArray` that are associated with an application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_INSTRUMENTATION:kotlin.Int` PackageInfo flag: return information about instrumentation in the package in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#instrumentation:kotlin.Array`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_INTENT_FILTERS:kotlin.Int` PackageInfo flag: return information about the intent filters supported by the activity. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_META_DATA:kotlin.Int` ComponentInfo flag: return the `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#metaData:android.os.Bundle` data `https://developer.android.com/reference/kotlin/android/os/Bundle.html#`s that are associated with a component. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_PERMISSIONS:kotlin.Int` PackageInfo flag: return information about permissions in the package in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#permissions:kotlin.Array`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_PROVIDERS:kotlin.Int` PackageInfo flag: return information about content providers in the package in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#providers:kotlin.Array`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_RECEIVERS:kotlin.Int` PackageInfo flag: return information about intent receivers in the package in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#receivers:kotlin.Array`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_RESOLVED_FILTER:kotlin.Int` ResolveInfo flag: return the IntentFilter that was matched for a particular ResolveInfo in `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#filter:android.content.IntentFilter`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_SERVICES:kotlin.Int` PackageInfo flag: return information about services in the package in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#services:kotlin.Array`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_SHARED_LIBRARY_FILES:kotlin.Int` ApplicationInfo flag: return the `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#sharedLibraryFiles:kotlin.Array` that are associated with an application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_SIGNATURES:kotlin.Int` PackageInfo flag: return information about the signatures included in the package. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_SIGNING_CERTIFICATES:kotlin.Int` PackageInfo flag: return the signing certificates associated with this package. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_UNINSTALLED_PACKAGES:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_URI_PERMISSION_PATTERNS:kotlin.Int` ProviderInfo flag: return the `https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo#uriPermissionPatterns:kotlin.Array` that are associated with a content provider. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#INSTALL_REASON_DEVICE_RESTORE:kotlin.Int` Code indicating that this package was installed as part of restoring from another device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#INSTALL_REASON_DEVICE_SETUP:kotlin.Int` Code indicating that this package was installed as part of device setup. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#INSTALL_REASON_POLICY:kotlin.Int` Code indicating that this package was installed due to enterprise policy. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#INSTALL_REASON_UNKNOWN:kotlin.Int` Code indicating that the reason for installing this package is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#INSTALL_REASON_USER:kotlin.Int` Code indicating that the package installation was initiated by the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#INSTALL_SCENARIO_BULK:kotlin.Int` Installation scenario indicating a bulk operation with the desired result of a fully optimized application. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#INSTALL_SCENARIO_BULK_SECONDARY:kotlin.Int` Installation scenario indicating a bulk operation that prioritizes minimal system health impact over application optimization. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#INSTALL_SCENARIO_DEFAULT:kotlin.Int` A value to indicate the lack of CUJ information, disabling all installation scenario logic. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#INSTALL_SCENARIO_FAST:kotlin.Int` Installation scenario providing the fastest "install button to launch" experience possible. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_ALL:kotlin.Int` Querying flag: if set and if the platform is doing any filtering of the results, then the filtering will not happen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_APEX:kotlin.Int` PackageInfo flag: include APEX packages that are currently installed. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_ARCHIVED_PACKAGES:kotlin.Long` Flag parameter to also retrieve some information about archived packages. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DEFAULT_ONLY:kotlin.Int` Resolution and querying flag: if set, only filters that support the `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_DEFAULT:kotlin.String` will be considered for matching. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DIRECT_BOOT_AUTO:kotlin.Int` Querying flag: automatically match components based on their Direct Boot awareness and the current user state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DIRECT_BOOT_AWARE:kotlin.Int` Querying flag: match components which are direct boot *aware* in the returned info, regardless of the current user state. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DIRECT_BOOT_UNAWARE:kotlin.Int` Querying flag: match components which are direct boot *unaware* in the returned info, regardless of the current user state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DISABLED_COMPONENTS:kotlin.Int` PackageInfo flag: include disabled components in the returned info. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DISABLED_UNTIL_USED_COMPONENTS:kotlin.Int` PackageInfo flag: include disabled components which are in that state only because of `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DISABLED_UNTIL_USED:kotlin.Int` in the returned info. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_SYSTEM_ONLY:kotlin.Int` Querying flag: include only components from applications that are marked with `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_SYSTEM:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_UNINSTALLED_PACKAGES:kotlin.Int` Flag parameter to retrieve some information about all applications (even uninstalled ones) which have data directories. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MAXIMUM_VERIFICATION_TIMEOUT:kotlin.Long` Can be used as the `millisecondsToDelay` argument for extendVerificationTimeout. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_DENIED:kotlin.Int` Permission check result: this is returned by checkPermission if the permission has not been granted to the given package. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_GRANTED:kotlin.Int` Permission check result: this is returned by checkPermission if the permission has been granted to the given package. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PROPERTY_COMPAT_OVERRIDE_LANDSCAPE_TO_PORTRAIT:kotlin.String` Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property` for an app to inform the system that the app can be opted-in or opted-out from the compatibility treatment that rotates camera output by 90 degrees on landscape sensors on devices known to have compatibility issues. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PROPERTY_MEDIA_CAPABILITIES:kotlin.String` \<application\> level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property` tag specifying the XML resource ID containing an application's media capabilities XML file For example: \<application\> \<property android:name="android. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PROPERTY_NATIVE_SERVICE_FUNCTION_NAME:kotlin.String` Service level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property` tag for native services specifying the symbol name of the entry point function for the service. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PROPERTY_NATIVE_SERVICE_LIBRARY_NAME:kotlin.String` Service level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property` tag for native services specifying the name of the library to be loaded to the process that hosts the service. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PROPERTY_SELF_CERTIFIED_NETWORK_CAPABILITIES:kotlin.String` \<application\> level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property` tag specifying the XML resource ID containing the declaration of the self-certified network capabilities used by the application. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PROPERTY_SPECIAL_USE_FGS_SUBTYPE:kotlin.String` \<service\> level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property` tag specifying the actual use case of the service if it's foreground service with the type `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_SPECIAL_USE:kotlin.Int`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PROPERTY_USE_RESTRICTED_BACKUP_MODE:kotlin.String` \<application\> level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property` tag specifying whether the app should be put into the "restricted" backup mode when it's started for backup and restore operations. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_FIRST_NOT_SIGNED:kotlin.Int` Signature check result: this is returned by #checkSignatures if the first package is not signed but the second is. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_MATCH:kotlin.Int` Signature check result: this is returned by #checkSignatures if all signatures on the two packages match. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_NEITHER_SIGNED:kotlin.Int` Signature check result: this is returned by #checkSignatures if neither of the two packages is signed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_NO_MATCH:kotlin.Int` Signature check result: this is returned by #checkSignatures if not all signatures on both packages match. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_SECOND_NOT_SIGNED:kotlin.Int` Signature check result: this is returned by #checkSignatures if the second package is not signed but the first is. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_UNKNOWN_PACKAGE:kotlin.Int` Signature check result: this is returned by #checkSignatures if either of the packages are not valid. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SYNCHRONOUS:kotlin.Int` Flag parameter for setComponentEnabledSetting to indicate that the given user's package restrictions state will be serialised to disk after the component state has been updated. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#VERIFICATION_ALLOW:kotlin.Int` Used as the `verificationCode` argument for verifyPendingInstall to indicate that the calling package verifier allows the installation to proceed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#VERIFICATION_REJECT:kotlin.Int` Used as the `verificationCode` argument for verifyPendingInstall to indicate the calling package verifier does not vote to allow the installation to proceed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#VERSION_CODE_HIGHEST:kotlin.Int` Constant for specifying the highest installed package version code. |

| Public constructors ||
|---|---|
| PackageManager <br /> |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addPackageToPreferred <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | addPermission Add a new dynamic permission to the system. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | addPermissionAsync Like addPermission but asynchronously persists the package manager state after returning from the call, allowing it to return quicker and batch a series of adds at the expense of no guarantee the added permission will be retained if the device is rebooted before it is written. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addPreferredActivity Add a new preferred activity mapping to the system. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | addWhitelistedRestrictedPermission Adds a whitelisted restricted permission for an app. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | canPackageQuery Returns `true` if the source package is able to query for details about the target package. |
| --- | --- |
| open [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html) | canPackageQuery Same as canPackageQuery but accepts an array of target packages to be queried. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | canRequestPackageInstalls Checks whether the calling package is allowed to request package installs through package installer. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | canonicalToCurrentPackageNames Map from a packages canonical name to the current name in use on the device. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | checkPermission Check whether a particular package has been granted a particular permission. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | checkSignatures Like checkSignatures, but takes UIDs of the two packages to be checked. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | checkSignatures Compare the signatures of two packages to determine if the same signature appears in both of them. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | clearInstantAppCookie Clears the instant application cookie for the calling app. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | clearPackagePreferredActivities Remove all preferred activity mappings, previously added with addPreferredActivity, from the system whose activities are implemented in the given package name. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | currentToCanonicalPackageNames Map from the current package names in use on the device to whatever the current canonical name of that package is. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | extendVerificationTimeout Allows a package listening to the `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_NEEDS_VERIFICATION:kotlin.String` to extend the default timeout for a response and declare what action to perform after the timeout occurs. |
| abstract [Drawable](../android.graphics.drawable/Drawable.md)? | getActivityBanner Retrieve the banner associated with an activity. |
| abstract [Drawable](../android.graphics.drawable/Drawable.md)? | getActivityBanner Retrieve the banner associated with an Intent. |
| --- | --- |
| abstract [Drawable](../android.graphics.drawable/Drawable.md) | getActivityIcon Retrieve the icon associated with an activity. |
| abstract [Drawable](../android.graphics.drawable/Drawable.md) | getActivityIcon Retrieve the icon associated with an Intent. |
| open [ActivityInfo](ActivityInfo.md) | getActivityInfo See getActivityInfo. |
| --- | --- |
| abstract [ActivityInfo](ActivityInfo.md) | getActivityInfo Retrieve all of the information we know about a particular activity class. |
| abstract [Drawable](../android.graphics.drawable/Drawable.md)? | getActivityLogo Retrieve the logo associated with an activity. |
| abstract [Drawable](../android.graphics.drawable/Drawable.md)? | getActivityLogo Retrieve the logo associated with an Intent. |
| --- | --- |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PermissionGroupInfo](PermissionGroupInfo.md)!\> | getAllPermissionGroups Retrieve all of the known permission groups in the system. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getAppUidForPrivateComputeCoreUid Maps a Private Compute Core (PCC) UID to its corresponding application UID. |
| abstract [Drawable](../android.graphics.drawable/Drawable.md)? | getApplicationBanner Retrieve the banner associated with an application. |
| --- | --- |
| abstract [Drawable](../android.graphics.drawable/Drawable.md)? | getApplicationBanner Retrieve the banner associated with an application. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getApplicationEnabledSetting Return the enabled setting for an application. |
| abstract [Drawable](../android.graphics.drawable/Drawable.md) | getApplicationIcon Retrieve the icon associated with an application. |
| --- | --- |
| abstract [Drawable](../android.graphics.drawable/Drawable.md) | getApplicationIcon Retrieve the icon associated with an application. |
| open [ApplicationInfo](ApplicationInfo.md) | getApplicationInfo See getApplicationInfo. |
| abstract [ApplicationInfo](ApplicationInfo.md) | getApplicationInfo Retrieve all of the information we know about a particular package/application. |
| --- | --- |
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | getApplicationLabel Return the label to use for this application. |
| abstract [Drawable](../android.graphics.drawable/Drawable.md)? | getApplicationLogo Retrieve the logo associated with an application. |
| abstract [Drawable](../android.graphics.drawable/Drawable.md)? | getApplicationLogo Retrieve the logo associated with an application. |
| --- | --- |
| open [ArchivedPackageInfo](ArchivedPackageInfo.md)? | getArchivedPackage Return archived package info for the package or null if the package is not installed. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | getBackgroundPermissionOptionLabel Gets the localized label that corresponds to the option in settings for granting background access. |
| abstract [ChangedPackages](ChangedPackages.md)? | getChangedPackages Returns the names of the packages that have been changed \[eg. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getComponentEnabledSetting Return the enabled setting for a package component (activity, receiver, service, provider). |
| abstract [Drawable](../android.graphics.drawable/Drawable.md) | getDefaultActivityIcon Return the generic icon for an activity that is used when no specific icon is defined. |
| abstract [Drawable](../android.graphics.drawable/Drawable.md)? | getDrawable Retrieve an image from a package. |
| --- | --- |
| open [PendingIntent](../android.app/PendingIntent.md)? | getEnableAppLockIntentForPackage Returns a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` to launch an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` that allows the caller to set App Lock for the specified package. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getGroupOfPlatformPermission Get the platform-defined permission group of a particular permission, if the permission is a platform-defined permission. |
| open [InstallSourceInfo](InstallSourceInfo.md) | getInstallSourceInfo Retrieves information about how a package was installed or updated. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ApplicationInfo](ApplicationInfo.md)!\> | getInstalledApplications See getInstalledApplications |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ApplicationInfo](ApplicationInfo.md)!\> | getInstalledApplications Return a List of all application packages that are installed for the current user. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ModuleInfo](ModuleInfo.md)!\> | getInstalledModules Return a List of all modules that are installed. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PackageInfo](PackageInfo.md)!\> | getInstalledPackages See getInstalledPackages. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PackageInfo](PackageInfo.md)!\> | getInstalledPackages Return a List of all packages that are installed for the current user. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getInstallerPackageName Retrieve the package name of the application that installed a package. |
| --- | --- |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | getInstantAppCookie Gets the instant application cookie for this app. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getInstantAppCookieMaxBytes Gets the maximum size in bytes of the cookie data an instant app can store on the device. |
| abstract [InstrumentationInfo](InstrumentationInfo.md) | getInstrumentationInfo Retrieve all of the information we know about a particular instrumentation class. |
| --- | --- |
| abstract [Intent](../android.content/Intent.md)? | getLaunchIntentForPackage Returns a "good" intent to launch a front-door activity in a package. |
| open [IntentSender](../android.content/IntentSender.md) | getLaunchIntentSenderForPackage Returns an `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` that can be used to launch a front-door activity in a package. |
| abstract [Intent](../android.content/Intent.md)? | getLeanbackLaunchIntentForPackage Return a "good" intent to launch a front-door Leanback activity in a package, for use for example to implement an "open" button when browsing through packages. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MemoryBudgetInfo](MemoryBudgetInfo.md)!\> | getMemoryBudgets Return the memory budgets for the application described by the given ApplicationInfo. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | getMimeGroup Gets all MIME types contained by MIME group. |
| open [ModuleInfo](ModuleInfo.md) | getModuleInfo Retrieve information for a particular module. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getNameForUid Retrieve the official name associated with a uid. |
| open [PackageInfo](PackageInfo.md)? | getPackageArchiveInfo See getPackageArchiveInfo. |
| open [PackageInfo](PackageInfo.md)? | getPackageArchiveInfo Retrieve overall information about an application package defined in a package archive file Use getPackageArchiveInfo when long flags are needed. |
| --- | --- |
| abstract [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | getPackageGids Return an array of all of the POSIX secondary group IDs that have been assigned to the given package. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | getPackageGids See getPackageGids. |
| abstract [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | getPackageGids Return an array of all of the POSIX secondary group IDs that have been assigned to the given package. |
| --- | --- |
| open [PackageInfo](PackageInfo.md) | getPackageInfo See getPackageInfo |
| abstract [PackageInfo](PackageInfo.md)! | getPackageInfo Retrieve overall information about an application package that is installed on the system. |
| open [PackageInfo](PackageInfo.md) | getPackageInfo See getPackageInfo |
| --- | --- |
| abstract [PackageInfo](PackageInfo.md)! | getPackageInfo Retrieve overall information about an application package that is installed on the system. |
| abstract [PackageInstaller](PackageInstaller.md) | getPackageInstaller Return interface that offers the ability to install, upgrade, and remove applications on the device. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPackageUid See getPackageUid. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPackageUid Return the UID associated with the given package name. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | getPackagesForUid Retrieve the names of all packages that are associated with a particular user id. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PackageInfo](PackageInfo.md)!\> | getPackagesHoldingPermissions See getPackagesHoldingPermissions. |
| --- | --- |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PackageInfo](PackageInfo.md)!\> | getPackagesHoldingPermissions Return a List of all installed packages that are currently holding any of the given permissions. |
| abstract [PermissionGroupInfo](PermissionGroupInfo.md) | getPermissionGroupInfo Retrieve all of the information we know about a particular group of permissions. |
| abstract [PermissionInfo](PermissionInfo.md)! | getPermissionInfo Retrieve all of the information we know about a particular permission. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getPlatformPermissionsForGroup Get the platform-defined permissions which belong to a particular permission group. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPreferredActivities Retrieve all preferred activities, previously added with addPreferredActivity, that are currently registered with the system. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PackageInfo](PackageInfo.md)!\> | getPreferredPackages Retrieve the list of all currently configured preferred packages. |
| --- | --- |
| open [PackageManager.Property](../android/content/pm/PackageManager.Property.md) | getProperty Returns the property defined in the given component declaration. |
| open [PackageManager.Property](../android/content/pm/PackageManager.Property.md) | getProperty Returns the property defined in the given package's \<application\> tag. |
| open [ProviderInfo](ProviderInfo.md) | getProviderInfo See getProviderInfo. |
| --- | --- |
| abstract [ProviderInfo](ProviderInfo.md) | getProviderInfo Retrieve all of the information we know about a particular content provider class. |
| open [ActivityInfo](ActivityInfo.md) | getReceiverInfo See getReceiverInfo. |
| abstract [ActivityInfo](ActivityInfo.md) | getReceiverInfo Retrieve all of the information we know about a particular receiver class. |
| --- | --- |
| abstract [Resources](../android.content.res/Resources.md) | getResourcesForActivity Retrieve the resources associated with an activity. |
| abstract [Resources](../android.content.res/Resources.md) | getResourcesForApplication Retrieve the resources for an application. |
| open [Resources](../android.content.res/Resources.md) | getResourcesForApplication Retrieve the resources for an application for the provided configuration. |
| --- | --- |
| abstract [Resources](../android.content.res/Resources.md) | getResourcesForApplication Retrieve the resources associated with an application. |
| open [ServiceInfo](ServiceInfo.md) | getServiceInfo See getServiceInfo. |
| abstract [ServiceInfo](ServiceInfo.md) | getServiceInfo Retrieve all of the information we know about a particular service class. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SharedLibraryInfo](SharedLibraryInfo.md)!\> | getSharedLibraries See getSharedLibraries. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SharedLibraryInfo](SharedLibraryInfo.md)!\> | getSharedLibraries Get a list of shared libraries on the device. |
| open [Bundle](../android.os/Bundle.md)? | getSuspendedPackageAppExtras Returns a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` of extras that was meant to be sent to the calling app when it was suspended. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getSyntheticAppDetailsActivityEnabled Return whether a synthetic app details activity will be generated if the app has no enabled launcher activity. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [FeatureInfo](FeatureInfo.md)!\> | getSystemAvailableFeatures Get a list of features that are available on the system. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | getSystemSharedLibraryNames Get a list of shared libraries that are available on the system. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getTargetSdkVersion <br /> |
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | getText Retrieve text from a package. |
| abstract [Drawable](../android.graphics.drawable/Drawable.md) | getUserBadgedDrawableForDensity If the target user is a managed profile of the calling user or the caller is itself a managed profile, then this returns a badged copy of the given drawable allowing the user to distinguish it from the original drawable. |
| --- | --- |
| abstract [Drawable](../android.graphics.drawable/Drawable.md) | getUserBadgedIcon If the target user is a managed profile, then this returns a badged copy of the given icon to be able to distinguish it from the original icon. |
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | getUserBadgedLabel If the target user is a managed profile of the calling user or the caller is itself a managed profile, then this returns a copy of the label with badging for accessibility services like talkback. |
| open static [SigningInfo](SigningInfo.md) | getVerifiedSigningInfo Verifies and returns the [app signing](https://source.android.com/docs/security/features/apksigning) information of the file at the given path. |
| --- | --- |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | getWhitelistedRestrictedPermissions Gets the restricted permissions that have been whitelisted and the app is allowed to have them granted in their full form. |
| abstract [XmlResourceParser](../android.content.res/XmlResourceParser.md)? | getXml Retrieve an XML file from a package. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasSigningCertificate Searches the set of signing certificates by which the package(s) for the given uid has proven to have been signed. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasSigningCertificate Searches the set of signing certificates by which the given package has proven to have been signed. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasSystemFeature Check whether the given feature name is one of the available features as returned by getSystemAvailableFeatures. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasSystemFeature Check whether the given feature name and version is one of the available features as returned by getSystemAvailableFeatures. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isAppArchivable Returns true if an app is archivable. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isAutoRevokeWhitelisted **Note:**In retrospect it would have been preferred to use more inclusive terminology when naming this API. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isAutoRevokeWhitelisted Checks whether an application is exempt from having its permissions be automatically revoked when the app is unused for an extended period of time. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isDefaultApplicationIcon Returns if the provided drawable represents the default activity icon provided by the system. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isDeviceUpgrading Returns true if the device is upgrading, such as first boot after OTA. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isInstantApp Gets whether this application is an instant app. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isInstantApp Gets whether the given package is an instant app. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isPackageStopped Query if an app is currently stopped. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isPackageSuspended Apps can query this to know if they have been suspended. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isPackageSuspended Query if an app is currently suspended. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isPermissionRevokedByPolicy Checks whether a particular permissions has been revoked for a package by policy. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isSafeMode Return whether the device has been booted into safe mode. |
| --- | --- |
| open T | parseAndroidManifest Similar to parseAndroidManifest, but accepting a file descriptor instead of a File object. |
| open T | parseAndroidManifest Retrieve AndroidManifest. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PackageManager.Property](../android/content/pm/PackageManager.Property.md)!\> | queryActivityProperty Returns the property definition for all \<activity\> and \<activity-alias\> tags. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PackageManager.Property](../android/content/pm/PackageManager.Property.md)!\> | queryApplicationProperty Returns the property definition for all \<application\> tags. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ResolveInfo](ResolveInfo.md)!\> | queryBroadcastReceivers See queryBroadcastReceivers. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ResolveInfo](ResolveInfo.md)!\> | queryBroadcastReceivers Retrieve all receivers that can handle a broadcast of the given intent. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ProviderInfo](ProviderInfo.md)!\> | queryContentProviders See queryContentProviders. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ProviderInfo](ProviderInfo.md)!\> | queryContentProviders Retrieve content provider information. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [InstrumentationInfo](InstrumentationInfo.md)!\> | queryInstrumentation Retrieve information about available instrumentation code. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ResolveInfo](ResolveInfo.md)!\> | queryIntentActivities See queryIntentActivities. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ResolveInfo](ResolveInfo.md)!\> | queryIntentActivities Retrieve all activities that can be performed for the given intent. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ResolveInfo](ResolveInfo.md)!\> | queryIntentActivityOptions Retrieve a set of activities that should be presented to the user as similar options. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ResolveInfo](ResolveInfo.md)!\> | queryIntentActivityOptions See queryIntentActivityOptions. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ResolveInfo](ResolveInfo.md)!\> | queryIntentContentProviders See queryIntentContentProviders. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ResolveInfo](ResolveInfo.md)!\> | queryIntentContentProviders Retrieve all providers that can match the given intent. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ResolveInfo](ResolveInfo.md)!\> | queryIntentServices See queryIntentServices. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ResolveInfo](ResolveInfo.md)!\> | queryIntentServices Retrieve all services that can match the given intent. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PermissionInfo](PermissionInfo.md)!\> | queryPermissionsByGroup Query for all of the permissions associated with a particular group. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PackageManager.Property](../android/content/pm/PackageManager.Property.md)!\> | queryProviderProperty Returns the property definition for all \<provider\> tags. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PackageManager.Property](../android/content/pm/PackageManager.Property.md)!\> | queryReceiverProperty Returns the property definition for all \<receiver\> tags. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PackageManager.Property](../android/content/pm/PackageManager.Property.md)!\> | queryServiceProperty Returns the property definition for all \<service\> tags. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | relinquishUpdateOwnership Attempt to relinquish the update ownership of the given package. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removePackageFromPreferred <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removePermission Removes a permission that was previously added with addPermission. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | removeWhitelistedRestrictedPermission Removes a whitelisted restricted permission for an app. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | requestChecksums Requests the checksums for APKs within a package. |
| open [ResolveInfo](ResolveInfo.md)? | resolveActivity See resolveActivity. |
| --- | --- |
| abstract [ResolveInfo](ResolveInfo.md)? | resolveActivity Determine the best action to perform for a given Intent. |
| open [ProviderInfo](ProviderInfo.md)? | resolveContentProvider See resolveContentProvider. |
| abstract [ProviderInfo](ProviderInfo.md)? | resolveContentProvider Find a single content provider by its authority. |
| --- | --- |
| open [ResolveInfo](ResolveInfo.md)? | resolveService See resolveService. |
| abstract [ResolveInfo](ResolveInfo.md)? | resolveService Determine the best service to handle for a given Intent. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setApplicationCategoryHint Provide a hint of what the `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#category:kotlin.Int` value should be for the given package. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setApplicationEnabledSetting Set the enabled setting for an application This setting will override any enabled state which may have been set by the application in its manifest. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setAutoRevokeWhitelisted Marks an application exempt from having its permissions be automatically revoked when the app is unused for an extended period of time. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setComponentEnabledSetting Set the enabled setting for a package component (activity, receiver, service, provider). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setComponentEnabledSettings Set the enabled settings for package components such as activities, receivers, services and providers. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setInstallerPackageName Change the installer associated with a given package. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setMimeGroup Sets MIME group's MIME types. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | updateInstantAppCookie Updates the instant application cookie for the calling app. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | verifyPendingInstall Allows a package listening to the `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_NEEDS_VERIFICATION:kotlin.String` to respond to the package manager. |

| Properties ||
|---|---|
| static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Certificate](../java.security.cert/Certificate.md)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#TRUST_ALL:kotlin.collections.MutableList` Trust any Installer to provide checksums for the package. |
| static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Certificate](../java.security.cert/Certificate.md)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#TRUST_NONE:kotlin.collections.MutableList` Don't trust any Installer to provide checksums for the package. |

## Constants

### CERT_INPUT_RAW_X509

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CERT_INPUT_RAW_X509: Int
```

Certificate input bytes: the input bytes represent an encoded X.509 Certificate which could be generated using an `CertificateFactory`

 Value: 0

### CERT_INPUT_SHA256

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CERT_INPUT_SHA256: Int
```

Certificate input bytes: the input bytes represent the SHA256 output of an encoded X.509 Certificate.

 Value: 1

### COMPONENT_ENABLED_STATE_DEFAULT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COMPONENT_ENABLED_STATE_DEFAULT: Int
```

Flag for setApplicationEnabledSetting and setComponentEnabledSetting: This component or application is in its default enabled state (as specified in its manifest).

Explicitly setting the component state to this value restores it's enabled state to whatever is set in the manifest.

 Value: 0

### COMPONENT_ENABLED_STATE_DISABLED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COMPONENT_ENABLED_STATE_DISABLED: Int
```

Flag for setApplicationEnabledSetting and setComponentEnabledSetting: This component or application has been explicitly disabled, regardless of what it has specified in its manifest.

 Value: 2

### COMPONENT_ENABLED_STATE_DISABLED_UNTIL_USED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COMPONENT_ENABLED_STATE_DISABLED_UNTIL_USED: Int
```

Flag for setApplicationEnabledSetting only: This application should be considered, until the point where the user actually wants to use it. This means that it will not normally show up to the user (such as in the launcher), but various parts of the user interface can use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_DISABLED_UNTIL_USED_COMPONENTS:kotlin.Int` to still see it and allow the user to select it (as for example an IME, device admin, etc). Such code, once the user has selected the app, should at that point also make it enabled. This option currently **can not** be used with setComponentEnabledSetting.

 Value: 4

### COMPONENT_ENABLED_STATE_DISABLED_USER

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COMPONENT_ENABLED_STATE_DISABLED_USER: Int
```

Flag for setApplicationEnabledSetting only: The user has explicitly disabled the application, regardless of what it has specified in its manifest. Because this is due to the user's request, they may re-enable it if desired through the appropriate system UI. This option currently **cannot** be used with setComponentEnabledSetting.

 Value: 3

### COMPONENT_ENABLED_STATE_ENABLED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COMPONENT_ENABLED_STATE_ENABLED: Int
```

Flag for setApplicationEnabledSetting and setComponentEnabledSetting: This component or application has been explictily enabled, regardless of what it has specified in its manifest.

 Value: 1

### DELETE_ARCHIVE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DELETE_ARCHIVE: Int
```

Flag parameter for uninstall to indicate that the deletion is an archival. This flag is only for internal usage as part of requestArchive.

 Value: 16

### DONT_KILL_APP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DONT_KILL_APP: Int
```

Flag parameter for setComponentEnabledSetting to indicate that you don't want to kill the app containing the component. Be careful when you set this since changing component states can make the containing application's behavior unpredictable.

 Value: 1

### EXTRA_VERIFICATION_ID

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_VERIFICATION_ID: String
```

Extra field name for the ID of a package pending verification. Passed to a package verifier and is used to call back to verifyPendingInstall

 Value: "android.content.pm.extra.VERIFICATION_ID"

### EXTRA_VERIFICATION_RESULT

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_VERIFICATION_RESULT: String
```

Extra field name for the result of a verification, either `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#VERIFICATION_ALLOW:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#VERIFICATION_REJECT:kotlin.Int`. Passed to package verifiers after a package is verified.

 Value: "android.content.pm.extra.VERIFICATION_RESULT"

### FEATURE_ACTIVITIES_ON_SECONDARY_DISPLAYS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_ACTIVITIES_ON_SECONDARY_DISPLAYS: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports running activities on secondary displays. Displays here refers to both physical and virtual displays. Disabling this feature can impact support for application projection use-cases and support for virtual devices on the device.

 Value: "android.software.activities_on_secondary_displays"

### FEATURE_APP_WIDGETS

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_APP_WIDGETS: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports app widgets.

 Value: "android.software.app_widgets"

### FEATURE_AUDIO_LOW_LATENCY

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_AUDIO_LOW_LATENCY: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device's audio pipeline is low-latency, more suitable for audio applications sensitive to delays or lag in sound input or output.

 Value: "android.hardware.audio.low_latency"

### FEATURE_AUDIO_OUTPUT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_AUDIO_OUTPUT: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes at least one form of audio output, as defined in the Android Compatibility Definition Document (CDD) [section 7.8 Audio](https://source.android.com/compatibility/android-cdd#7_8_audio).

 Value: "android.hardware.audio.output"

### FEATURE_AUDIO_PRO

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_AUDIO_PRO: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has professional audio level of functionality and performance.

 Value: "android.hardware.audio.pro"

### FEATURE_AUDIO_SPATIAL_HEADTRACKING_LOW_LATENCY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_AUDIO_SPATIAL_HEADTRACKING_LOW_LATENCY: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature which indicates whether head tracking for spatial audio operates with low-latency, as defined by the CDD criteria for the feature.

 Value: "android.hardware.audio.spatial.headtracking.low_latency"

### FEATURE_AUTOFILL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_AUTOFILL: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports autofill of user credentials, addresses, credit cards, etc via integration with `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#`.

 Value: "android.software.autofill"

### FEATURE_AUTOMOTIVE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_AUTOMOTIVE: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: This is a device dedicated to showing UI on a vehicle headunit. A headunit here is defined to be inside a vehicle that may or may not be moving. A headunit uses either a primary display in the center console and/or additional displays in the instrument cluster or elsewhere in the vehicle. Headunit display(s) have limited size and resolution. The user will likely be focused on driving so limiting driver distraction is a primary concern. User input can be a variety of hard buttons, touch, rotary controllers and even mouse- like interfaces.

 Value: "android.hardware.type.automotive"

### FEATURE_BACKUP

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_BACKUP: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device can perform backup and restore operations on installed applications.

 Value: "android.software.backup"

### FEATURE_BLUETOOTH

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_BLUETOOTH: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device is capable of communicating with other devices via Bluetooth.

 Value: "android.hardware.bluetooth"

### FEATURE_BLUETOOTH_LE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_BLUETOOTH_LE: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device is capable of communicating with other devices via Bluetooth Low Energy radio.

 Value: "android.hardware.bluetooth_le"

### FEATURE_BLUETOOTH_LE_CHANNEL_SOUNDING

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_BLUETOOTH_LE_CHANNEL_SOUNDING: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device is capable of ranging with other devices using channel sounding via Bluetooth Low Energy radio.

 Value: "android.hardware.bluetooth_le.channel_sounding"

### FEATURE_CAMERA

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_CAMERA: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a camera facing away from the screen.

 Value: "android.hardware.camera"

### FEATURE_CAMERA_ANY

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_CAMERA_ANY: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has at least one camera pointing in some direction, or can support an external or a `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice.html#` camera being connected to it.

 Value: "android.hardware.camera.any"

### FEATURE_CAMERA_AR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_CAMERA_AR: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: At least one of the cameras on the device supports the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_MOTION_TRACKING:kotlin.Int` capability level.

 Value: "android.hardware.camera.ar"

### FEATURE_CAMERA_AUTOFOCUS

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_CAMERA_AUTOFOCUS: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device's camera supports auto-focus.

 Value: "android.hardware.camera.autofocus"

### FEATURE_CAMERA_CAPABILITY_MANUAL_POST_PROCESSING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_CAMERA_CAPABILITY_MANUAL_POST_PROCESSING: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: At least one of the cameras on the device supports the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_MANUAL_POST_PROCESSING:kotlin.Int` capability level.

 Value: "android.hardware.camera.capability.manual_post_processing"

### FEATURE_CAMERA_CAPABILITY_MANUAL_SENSOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_CAMERA_CAPABILITY_MANUAL_SENSOR: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: At least one of the cameras on the device supports the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_MANUAL_SENSOR:kotlin.Int` capability level.

 Value: "android.hardware.camera.capability.manual_sensor"

### FEATURE_CAMERA_CAPABILITY_RAW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_CAMERA_CAPABILITY_RAW: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: At least one of the cameras on the device supports the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_RAW:kotlin.Int` capability level.

 Value: "android.hardware.camera.capability.raw"

### FEATURE_CAMERA_CONCURRENT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_CAMERA_CONCURRENT: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device's main front and back cameras can stream concurrently as described in getConcurrentCameraIds.

<br />

While getConcurrentCameraIds and associated APIs are only available on API level 30 or newer, this feature flag may be advertised by devices on API levels below 30. If present on such a device, the same guarantees hold: The main front and main back camera can be used at the same time, with guaranteed stream configurations as defined in the table for concurrent streaming at createCaptureSession.

 Value: "android.hardware.camera.concurrent"

### FEATURE_CAMERA_EXTERNAL

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_CAMERA_EXTERNAL: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device can support having an external camera connected to it. The external camera may not always be connected or available to applications to use.

 Value: "android.hardware.camera.external"

### FEATURE_CAMERA_FLASH

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_CAMERA_FLASH: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device's camera supports flash.

 Value: "android.hardware.camera.flash"

### FEATURE_CAMERA_FRONT

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_CAMERA_FRONT: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a front facing camera.

 Value: "android.hardware.camera.front"

### FEATURE_CAMERA_LEVEL_FULL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_CAMERA_LEVEL_FULL: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: At least one of the cameras on the device supports the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key` capability level.

 Value: "android.hardware.camera.level.full"

### FEATURE_CANT_SAVE_STATE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_CANT_SAVE_STATE: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports the `https://developer.android.com/reference/kotlin/android/R.attr.html#cantSaveState:kotlin.Int` API.

 Value: "android.software.cant_save_state"

### FEATURE_COMPANION_DEVICE_SETUP

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_COMPANION_DEVICE_SETUP: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports android.companion.CompanionDeviceManager#associate with devices via `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.html#`.

 Value: "android.software.companion_device_setup"

### FEATURE_CONNECTION_SERVICE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_CONNECTION_SERVICE: String
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELECOM:kotlin.String` instead.*

Feature for getSystemAvailableFeatures and #hasSystemFeature: The Connection Service API is enabled on the device.

 Value: "android.software.connectionservice"

### FEATURE_CONSUMER_IR

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_CONSUMER_IR: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device is capable of communicating with consumer IR devices.

 Value: "android.hardware.consumerir"

### FEATURE_CONTROLS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_CONTROLS: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports a system interface for the user to select and bind device control services provided by applications.

 Value: "android.software.controls"

**See Also**

- `https://developer.android.com/reference/kotlin/android/service/controls/ControlsProviderService.html#`

### FEATURE_CREDENTIALS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_CREDENTIALS: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports retrieval of user credentials, via integration with credential providers.

 Value: "android.software.credentials"

### FEATURE_DEVICE_ADMIN

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_DEVICE_ADMIN: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports device policy enforcement via device admins.

 Value: "android.software.device_admin"

### FEATURE_DEVICE_ID_ATTESTATION

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_DEVICE_ID_ATTESTATION: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a KeyMint (or Keymaster) implementation that supports device ID attestation. See [the public documentation](https://source.android.com/docs/security/features/keystore/attestation#id-attestation) for more information about device ID attestation.

 Value: "android.software.device_id_attestation"

**See Also**

- isDeviceIdAttestationSupported

### FEATURE_DEVICE_LOCK

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_DEVICE_LOCK: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports locking (for example, by a financing provider in case of a missed payment).

 Value: "android.software.device_lock"

### FEATURE_EMBEDDED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_EMBEDDED: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: This is a device for IoT and may not have an UI. An embedded device is defined as a full stack Android device with or without a display and no user-installable apps.

 Value: "android.hardware.type.embedded"

### FEATURE_ETHERNET

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_ETHERNET: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: This device supports ethernet.

 Value: "android.hardware.ethernet"

### FEATURE_EXPANDED_PICTURE_IN_PICTURE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_EXPANDED_PICTURE_IN_PICTURE: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports expanded picture-in-picture multi-window mode.

 Value: "android.software.expanded_picture_in_picture"

**See Also**

- setExpandedAspectRatio

### FEATURE_FACE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_FACE: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has biometric hardware to perform face authentication.

 Value: "android.hardware.biometrics.face"

### FEATURE_FAKETOUCH

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_FAKETOUCH: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device does not have a touch screen, but does support touch emulation for basic events. For instance, the device might use a mouse or remote control to drive a cursor, and emulate basic touch pointer events like down, up, drag, etc. All devices that support android.hardware.touchscreen or a sub-feature are presumed to also support faketouch.

 Value: "android.hardware.faketouch"

### FEATURE_FAKETOUCH_MULTITOUCH_DISTINCT

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_FAKETOUCH_MULTITOUCH_DISTINCT: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device does not have a touch screen, but does support touch emulation for basic events that supports distinct tracking of two or more fingers. This is an extension of `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_FAKETOUCH:kotlin.String` for input devices with this capability. Note that unlike a distinct multitouch screen as defined by `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TOUCHSCREEN_MULTITOUCH_DISTINCT:kotlin.String`, these kinds of input devices will not actually provide full two-finger gestures since the input is being transformed to cursor movement on the screen. That is, single finger gestures will move a cursor; two-finger swipes will result in single-finger touch events; other two-finger gestures will result in the corresponding two-finger touch event.

 Value: "android.hardware.faketouch.multitouch.distinct"

### FEATURE_FAKETOUCH_MULTITOUCH_JAZZHAND

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_FAKETOUCH_MULTITOUCH_JAZZHAND: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device does not have a touch screen, but does support touch emulation for basic events that supports tracking a hand of fingers (5 or more fingers) fully independently. This is an extension of `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_FAKETOUCH:kotlin.String` for input devices with this capability. Note that unlike a multitouch screen as defined by `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TOUCHSCREEN_MULTITOUCH_JAZZHAND:kotlin.String`, not all two finger gestures can be detected due to the limitations described for `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_FAKETOUCH_MULTITOUCH_DISTINCT:kotlin.String`.

 Value: "android.hardware.faketouch.multitouch.jazzhand"

### FEATURE_FINGERPRINT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_FINGERPRINT: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has biometric hardware to detect a fingerprint.

 Value: "android.hardware.fingerprint"

### FEATURE_FREEFORM_WINDOW_MANAGEMENT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_FREEFORM_WINDOW_MANAGEMENT: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports freeform window management. Windows have title bars and can be moved and resized.

 Value: "android.software.freeform_window_management"

### FEATURE_GAMEPAD

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_GAMEPAD: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has all of the inputs necessary to be considered a compatible game controller, or includes a compatible game controller in the box.

 Value: "android.hardware.gamepad"

### FEATURE_HARDWARE_KEYSTORE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_HARDWARE_KEYSTORE: String
```

Feature for getSystemAvailableFeatures and hasSystemFeature: If this feature is supported, the device implements the Android Keystore backed by an isolated execution environment. The version indicates which features are implemented in the isolated execution environment:

- 500: Hardware support for ML-DSA signature generation.
- 400: Inclusion of module information (via tag MODULE_HASH) in the attestation record.
- 300: Ability to include a second IMEI in the ID attestation record, see `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#ID_TYPE_IMEI:kotlin.Int`.
- 200: Hardware support for Curve 25519 (including both Ed25519 signature generation and X25519 key agreement).
- 100: Hardware support for ECDH (see `https://developer.android.com/reference/kotlin/javax/crypto/KeyAgreement.html#`) and support for app-generated attestation keys (see setAttestKeyAlias).
- 41: Hardware enforcement of device-unlocked keys (see setUnlockedDeviceRequired).
- 40: Support for wrapped key import (see `https://developer.android.com/reference/kotlin/android/security/keystore/WrappedKeyEntry.html#`), optional support for ID attestation (see setDevicePropertiesAttestationIncluded), attestation (see setAttestationChallenge), AES, HMAC, ECDSA and RSA support where the secret or private key never leaves secure hardware, and support for requiring user authentication before a key can be used.

This feature version is guaranteed to be set for all devices launching with Android 12 and may be set on devices launching with an earlier version. If the feature version is set, it will at least have the value 40. If it's not set the device may have a version of hardware-backed keystore but it may not support all features listed above.

<br />

 Value: "android.hardware.hardware_keystore"

### FEATURE_HIFI_SENSORS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_HIFI_SENSORS: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports high fidelity sensor processing capabilities.

 Value: "android.hardware.sensor.hifi_sensors"

### FEATURE_HOME_SCREEN

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_HOME_SCREEN: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports a home screen that is replaceable by third party applications.

 Value: "android.software.home_screen"

### FEATURE_IDENTITY_CREDENTIAL_HARDWARE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_IDENTITY_CREDENTIAL_HARDWARE: String
```

Feature for getSystemAvailableFeatures and hasSystemFeature: If this feature is supported, the device supports `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore.html#` implemented in secure hardware at the given feature version.

Known feature versions include:

- `202009`: corresponds to the features included in the Identity Credential API shipped in Android 11.
- `202101`: corresponds to the features included in the Identity Credential API shipped in Android 12.
- `202201`: corresponds to the features included in the Identity Credential API shipped in Android 13.

 Value: "android.hardware.identity_credential"

### FEATURE_IDENTITY_CREDENTIAL_HARDWARE_DIRECT_ACCESS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_IDENTITY_CREDENTIAL_HARDWARE_DIRECT_ACCESS: String
```

Feature for getSystemAvailableFeatures and hasSystemFeature: If this feature is supported, the device supports `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore.html#` implemented in secure hardware with direct access at the given feature version. See `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_IDENTITY_CREDENTIAL_HARDWARE:kotlin.String` for known feature versions.

 Value: "android.hardware.identity_credential_direct_access"

### FEATURE_INPUT_METHODS

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_INPUT_METHODS: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports adding new input methods implemented with the `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#` API.

 Value: "android.software.input_methods"

### FEATURE_IPSEC_TUNNELS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_IPSEC_TUNNELS: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has the requisite kernel support for multinetworking-capable IPsec tunnels.

This feature implies that the device supports XFRM Interfaces (CONFIG_XFRM_INTERFACE), or VTIs with kernel patches allowing updates of output/set mark via UPDSA.

 Value: "android.software.ipsec_tunnels"

### FEATURE_IPSEC_TUNNEL_MIGRATION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_IPSEC_TUNNEL_MIGRATION: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has the requisite kernel support for migrating IPsec tunnels to new source/destination addresses.

This feature implies that the device supports XFRM Migration (CONFIG_XFRM_MIGRATE) and has the kernel fixes to support cross-address-family IPsec tunnel migration

 Value: "android.software.ipsec_tunnel_migration"

### FEATURE_IRIS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_IRIS: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has biometric hardware to perform iris authentication.

 Value: "android.hardware.biometrics.iris"

### FEATURE_KEYSTORE_APP_ATTEST_KEY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_KEYSTORE_APP_ATTEST_KEY: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a Keystore implementation that can create application-specific attestation keys. See setAttestKeyAlias.

 Value: "android.hardware.keystore.app_attest_key"

### FEATURE_KEYSTORE_LIMITED_USE_KEY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_KEYSTORE_LIMITED_USE_KEY: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a Keystore implementation that can enforce limited use key in hardware with any max usage count (including count equals to 1).

 Value: "android.hardware.keystore.limited_use_key"

### FEATURE_KEYSTORE_SINGLE_USE_KEY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_KEYSTORE_SINGLE_USE_KEY: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a Keystore implementation that can only enforce limited use key in hardware with max usage count equals to 1.

 Value: "android.hardware.keystore.single_use_key"

### FEATURE_LEANBACK

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_LEANBACK: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports leanback UI. This is typically used in a living room television experience, but is a software feature unlike `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEVISION:kotlin.String`. Devices running with this feature will use resources associated with the "television" UI mode.

 Value: "android.software.leanback"

### FEATURE_LEANBACK_ONLY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_LEANBACK_ONLY: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports only leanback UI. Only applications designed for this experience should be run, though this is not enforced by the system.

 Value: "android.software.leanback_only"

### FEATURE_LIVE_TV

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_LIVE_TV: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports live TV and can display contents from TV inputs implemented with the `https://developer.android.com/reference/kotlin/android/media/tv/TvInputService.html#` API.

 Value: "android.software.live_tv"

### FEATURE_LIVE_WALLPAPER

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_LIVE_WALLPAPER: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports live wallpapers.

 Value: "android.software.live_wallpaper"

### FEATURE_LOCATION

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_LOCATION: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports one or more methods of reporting current location.

 Value: "android.hardware.location"

### FEATURE_LOCATION_GPS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_LOCATION_GPS: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a Global Positioning System receiver and can report precise location.

 Value: "android.hardware.location.gps"

### FEATURE_LOCATION_NETWORK

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_LOCATION_NETWORK: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device can report location with coarse accuracy using a network-based geolocation system.

 Value: "android.hardware.location.network"

### FEATURE_MANAGED_USERS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_MANAGED_USERS: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports creating secondary users and managed profiles via `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#`.

 Value: "android.software.managed_users"

### FEATURE_MICROPHONE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_MICROPHONE: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device can record audio via a microphone.

 Value: "android.hardware.microphone"

### FEATURE_MIDI

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_MIDI: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a full implementation of the android.media.midi.\* APIs.

 Value: "android.software.midi"

### FEATURE_NEURAL_PROCESSING_UNIT

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_NEURAL_PROCESSING_UNIT: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: This device has a NPU (Neural Processing Unit) or similar hardware for accelerating AI workloads.

 Value: "android.hardware.npu"

### FEATURE_NFC

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_NFC: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device can communicate using Near-Field Communications (NFC), acting as a reader.

 Value: "android.hardware.nfc"

### FEATURE_NFC_BEAM

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_NFC_BEAM: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The Beam API is enabled on the device.

 Value: "android.sofware.nfc.beam"

### FEATURE_NFC_HOST_CARD_EMULATION

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_NFC_HOST_CARD_EMULATION: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports host- based NFC card emulation.

 Value: "android.hardware.nfc.hce"

### FEATURE_NFC_HOST_CARD_EMULATION_NFCF

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_NFC_HOST_CARD_EMULATION_NFCF: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports host- based NFC-F card emulation.

 Value: "android.hardware.nfc.hcef"

### FEATURE_NFC_OFF_HOST_CARD_EMULATION_ESE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_NFC_OFF_HOST_CARD_EMULATION_ESE: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports eSE- based NFC card emulation.

 Value: "android.hardware.nfc.ese"

### FEATURE_NFC_OFF_HOST_CARD_EMULATION_UICC

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_NFC_OFF_HOST_CARD_EMULATION_UICC: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports uicc- based NFC card emulation.

 Value: "android.hardware.nfc.uicc"

### FEATURE_OPENGLES_DEQP_LEVEL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_OPENGLES_DEQP_LEVEL: String
```

Feature for getSystemAvailableFeatures and hasSystemFeature: If this feature is supported, the feature version specifies a date such that the device is known to pass the OpenGLES dEQP test suite associated with that date. The date is encoded as follows:

- Year in bits 31-16
- Month in bits 15-8
- Day in bits 7-0

<br />

Example: 2021-03-01 is encoded as 0x07E50301, and would indicate that the device passes the OpenGL ES dEQP test suite version that was current on 2021-03-01.

 Value: "android.software.opengles.deqp.level"

### FEATURE_OPENGLES_EXTENSION_PACK

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_OPENGLES_EXTENSION_PACK: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports the OpenGL ES [Android Extension Pack](http://www.khronos.org/registry/gles/extensions/ANDROID/ANDROID_extension_pack_es31a.txt).

 Value: "android.hardware.opengles.aep"

### FEATURE_PC

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_PC: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: This is a device dedicated to be primarily used with keyboard, mouse or touchpad. This includes traditional desktop computers, laptops and variants such as convertibles or detachables. Due to the larger screen, the device will most likely use the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_FREEFORM_WINDOW_MANAGEMENT:kotlin.String` feature as well.

 Value: "android.hardware.type.pc"

### FEATURE_PICTURE_IN_PICTURE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_PICTURE_IN_PICTURE: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports picture-in-picture multi-window mode.

 Value: "android.software.picture_in_picture"

### FEATURE_PRINTING

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_PRINTING: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports printing.

 Value: "android.software.print"

### FEATURE_RAM_LOW

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_RAM_LOW: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device's isLowRamDevice method returns true.

 Value: "android.hardware.ram.low"

### FEATURE_RAM_NORMAL

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_RAM_NORMAL: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device's isLowRamDevice method returns false.

 Value: "android.hardware.ram.normal"

### FEATURE_SCREEN_LANDSCAPE

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SCREEN_LANDSCAPE: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports landscape orientation screens. For backwards compatibility, you can assume that if neither this nor `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SCREEN_PORTRAIT:kotlin.String` is set then the device supports both portrait and landscape.

 Value: "android.hardware.screen.landscape"

### FEATURE_SCREEN_PORTRAIT

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SCREEN_PORTRAIT: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports portrait orientation screens. For backwards compatibility, you can assume that if neither this nor `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_SCREEN_LANDSCAPE:kotlin.String` is set then the device supports both portrait and landscape.

 Value: "android.hardware.screen.portrait"

### FEATURE_SECURELY_REMOVES_USERS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SECURELY_REMOVES_USERS: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports secure removal of users. When a user is deleted the data associated with that user is securely deleted and no longer available.

 Value: "android.software.securely_removes_users"

### FEATURE_SECURE_LOCK_SCREEN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SECURE_LOCK_SCREEN: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a secure implementation of keyguard, meaning the device supports PIN, pattern and password as defined in Android CDD

 Value: "android.software.secure_lock_screen"

### FEATURE_SECURITY_MODEL_COMPATIBLE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SECURITY_MODEL_COMPATIBLE: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device is compatible with Android's security model.

See sections 2 and 9 in the [Android CDD](https://source.android.com/compatibility/android-cdd) for more details.

 Value: "android.hardware.security.model.compatible"

### FEATURE_SENSOR_ACCELEROMETER

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SENSOR_ACCELEROMETER: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes an accelerometer.

 Value: "android.hardware.sensor.accelerometer"

### FEATURE_SENSOR_ACCELEROMETER_LIMITED_AXES

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SENSOR_ACCELEROMETER_LIMITED_AXES: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a limited axes accelerometer.

 Value: "android.hardware.sensor.accelerometer_limited_axes"

### FEATURE_SENSOR_ACCELEROMETER_LIMITED_AXES_UNCALIBRATED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SENSOR_ACCELEROMETER_LIMITED_AXES_UNCALIBRATED: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes an uncalibrated limited axes accelerometer.

 Value: "android.hardware.sensor.accelerometer_limited_axes_uncalibrated"

### FEATURE_SENSOR_AMBIENT_TEMPERATURE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SENSOR_AMBIENT_TEMPERATURE: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes an ambient temperature sensor.

 Value: "android.hardware.sensor.ambient_temperature"

### FEATURE_SENSOR_BAROMETER

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SENSOR_BAROMETER: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a barometer (air pressure sensor.)

 Value: "android.hardware.sensor.barometer"

### FEATURE_SENSOR_COMPASS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SENSOR_COMPASS: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a magnetometer (compass).

 Value: "android.hardware.sensor.compass"

### FEATURE_SENSOR_DYNAMIC_HEAD_TRACKER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SENSOR_DYNAMIC_HEAD_TRACKER: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports exposing head tracker sensors from peripheral devices via the dynamic sensors API.

 Value: "android.hardware.sensor.dynamic.head_tracker"

### FEATURE_SENSOR_GYROSCOPE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SENSOR_GYROSCOPE: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a gyroscope.

 Value: "android.hardware.sensor.gyroscope"

### FEATURE_SENSOR_GYROSCOPE_LIMITED_AXES

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SENSOR_GYROSCOPE_LIMITED_AXES: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a limited axes gyroscope.

 Value: "android.hardware.sensor.gyroscope_limited_axes"

### FEATURE_SENSOR_GYROSCOPE_LIMITED_AXES_UNCALIBRATED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SENSOR_GYROSCOPE_LIMITED_AXES_UNCALIBRATED: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes an uncalibrated limited axes gyroscope.

 Value: "android.hardware.sensor.gyroscope_limited_axes_uncalibrated"

### FEATURE_SENSOR_HEADING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SENSOR_HEADING: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a heading sensor.

 Value: "android.hardware.sensor.heading"

### FEATURE_SENSOR_HEART_RATE

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SENSOR_HEART_RATE: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a heart rate monitor.

 Value: "android.hardware.sensor.heartrate"

### FEATURE_SENSOR_HEART_RATE_ECG

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SENSOR_HEART_RATE_ECG: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The heart rate sensor on this device is an Electrocardiogram.

 Value: "android.hardware.sensor.heartrate.ecg"

### FEATURE_SENSOR_HINGE_ANGLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SENSOR_HINGE_ANGLE: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a hinge angle sensor.

 Value: "android.hardware.sensor.hinge_angle"

### FEATURE_SENSOR_LIGHT

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SENSOR_LIGHT: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a light sensor.

 Value: "android.hardware.sensor.light"

### FEATURE_SENSOR_PROXIMITY

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SENSOR_PROXIMITY: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a proximity sensor.

 Value: "android.hardware.sensor.proximity"

### FEATURE_SENSOR_RELATIVE_HUMIDITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SENSOR_RELATIVE_HUMIDITY: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a relative humidity sensor.

 Value: "android.hardware.sensor.relative_humidity"

### FEATURE_SENSOR_STEP_COUNTER

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SENSOR_STEP_COUNTER: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a hardware step counter.

 Value: "android.hardware.sensor.stepcounter"

### FEATURE_SENSOR_STEP_DETECTOR

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SENSOR_STEP_DETECTOR: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device includes a hardware step detector.

 Value: "android.hardware.sensor.stepdetector"

### FEATURE_SE_OMAPI_ESE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SE_OMAPI_ESE: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Open Mobile API capable eSE-based secure elements.

 Value: "android.hardware.se.omapi.ese"

### FEATURE_SE_OMAPI_SD

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SE_OMAPI_SD: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Open Mobile API capable SD-based secure elements.

 Value: "android.hardware.se.omapi.sd"

### FEATURE_SE_OMAPI_UICC

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SE_OMAPI_UICC: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Open Mobile API capable UICC-based secure elements.

 Value: "android.hardware.se.omapi.uicc"

### FEATURE_SIP

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SIP: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The SIP API is enabled on the device.

 Value: "android.software.sip"

### FEATURE_SIP_VOIP

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_SIP_VOIP: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports SIP-based VOIP.

 Value: "android.software.sip.voip"

### FEATURE_STRONGBOX_KEYSTORE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_STRONGBOX_KEYSTORE: String
```

Feature for getSystemAvailableFeatures, hasSystemFeature, and hasSystemFeature: If this feature is supported, the device implements the Android Keystore backed by a dedicated secure processor referred to as [StrongBox](https://source.android.com/security/best-practices/hardware#strongbox-keymaster). If this feature has a version, the version number indicates which features are implemented in StrongBox:

- 400: Inclusion of module information (via tag MODULE_HASH) in the attestation record.
- 300: Ability to include a second IMEI in the ID attestation record, see `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#ID_TYPE_IMEI:kotlin.Int`.
- 200: No new features for StrongBox (the Android Keystore environment backed by an isolated execution environment has gained support for Curve 25519 in this version, but the implementation backed by a dedicated secure processor is not expected to implement it).
- 100: Hardware support for ECDH (see `https://developer.android.com/reference/kotlin/javax/crypto/KeyAgreement.html#`) and support for app-generated attestation keys (see setAttestKeyAlias).
- 41: Hardware enforcement of device-unlocked keys (see setUnlockedDeviceRequired).
- 40: Support for wrapped key import (see `https://developer.android.com/reference/kotlin/android/security/keystore/WrappedKeyEntry.html#`), optional support for ID attestation (see setDevicePropertiesAttestationIncluded), attestation (see setAttestationChallenge), AES, HMAC, ECDSA and RSA support where the secret or private key never leaves secure hardware, and support for requiring user authentication before a key can be used.

If a device has StrongBox, this feature version number is guaranteed to be set for all devices launching with Android 12 and may be set on devices launching with an earlier version. If the feature version is set, it will at least have the value 40. If it's not set the device may have StrongBox but it may not support all features listed above.

<br />

 Value: "android.hardware.strongbox_keystore"

### FEATURE_TELECOM

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_TELECOM: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Telecom Service APIs.

 Value: "android.software.telecom"

### FEATURE_TELEPHONY

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_TELEPHONY: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a telephony radio with data communication support.

 Value: "android.hardware.telephony"

### FEATURE_TELEPHONY_CALLING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_TELEPHONY_CALLING: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Telephony APIs for calling service.

This feature should only be defined if `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String`, and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELECOM:kotlin.String` have been defined.

 Value: "android.hardware.telephony.calling"

### FEATURE_TELEPHONY_CDMA

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_TELEPHONY_CDMA: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a CDMA telephony stack.

This feature should only be defined if `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY:kotlin.String` has been defined.

 Value: "android.hardware.telephony.cdma"

### FEATURE_TELEPHONY_DATA

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_TELEPHONY_DATA: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Telephony APIs for data service.

This feature should only be defined if both `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` have been defined.

 Value: "android.hardware.telephony.data"

### FEATURE_TELEPHONY_EUICC

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_TELEPHONY_EUICC: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports embedded subscriptions on eUICCs. This feature should only be defined if `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` has been defined.

 Value: "android.hardware.telephony.euicc"

### FEATURE_TELEPHONY_EUICC_MEP

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_TELEPHONY_EUICC_MEP: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports multiple enabled profiles on eUICCs.

Devices declaring this feature must have an implementation of the getPorts, isMultipleEnabledProfilesSupported and android.telephony.euicc.EuiccManager#switchToSubscription. This feature should only be defined if `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY_EUICC:kotlin.String` have been defined.

 Value: "android.hardware.telephony.euicc.mep"

### FEATURE_TELEPHONY_GSM

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_TELEPHONY_GSM: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a GSM telephony stack.

This feature should only be defined if `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY:kotlin.String` has been defined.

 Value: "android.hardware.telephony.gsm"

### FEATURE_TELEPHONY_IMS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_TELEPHONY_IMS: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports attaching to IMS implementations using the ImsService API in telephony.

This feature should only be defined if `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY_DATA:kotlin.String` has been defined.

 Value: "android.hardware.telephony.ims"

### FEATURE_TELEPHONY_MBMS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_TELEPHONY_MBMS: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports cell-broadcast reception using the MBMS APIs.

This feature should only be defined if both `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` have been defined.

 Value: "android.hardware.telephony.mbms"

### FEATURE_TELEPHONY_MESSAGING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_TELEPHONY_MESSAGING: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Telephony APIs for SMS and MMS.

This feature should only be defined if both `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY_SUBSCRIPTION:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY_RADIO_ACCESS:kotlin.String` have been defined.

 Value: "android.hardware.telephony.messaging"

### FEATURE_TELEPHONY_RADIO_ACCESS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_TELEPHONY_RADIO_ACCESS: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Telephony APIs for the radio access.

This feature should only be defined if `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY:kotlin.String` has been defined.

 Value: "android.hardware.telephony.radio.access"

### FEATURE_TELEPHONY_SUBSCRIPTION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_TELEPHONY_SUBSCRIPTION: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Telephony APIs for the subscription.

This feature should only be defined if `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_TELEPHONY:kotlin.String` has been defined.

 Value: "android.hardware.telephony.subscription"

### FEATURE_TELEVISION

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_TELEVISION: String
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_LEANBACK:kotlin.String` instead.*

Feature for getSystemAvailableFeatures and #hasSystemFeature: This is a device dedicated to showing UI on a television. Television here is defined to be a typical living room television experience: displayed on a big screen, where the user is sitting far away from it, and the dominant form of input will be something like a DPAD, not through touch or mouse.

 Value: "android.hardware.type.television"

### FEATURE_THREAD_NETWORK

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_THREAD_NETWORK: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device is capable of communicating with other devices via [Thread](https://www.threadgroup.org) networking protocol.

 Value: "android.hardware.thread_network"

### FEATURE_TOUCHSCREEN

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_TOUCHSCREEN: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device's display has a touch screen.

 Value: "android.hardware.touchscreen"

### FEATURE_TOUCHSCREEN_MULTITOUCH

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_TOUCHSCREEN_MULTITOUCH: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device's touch screen supports multitouch sufficient for basic two-finger gesture detection.

 Value: "android.hardware.touchscreen.multitouch"

### FEATURE_TOUCHSCREEN_MULTITOUCH_DISTINCT

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_TOUCHSCREEN_MULTITOUCH_DISTINCT: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device's touch screen is capable of tracking two or more fingers fully independently.

 Value: "android.hardware.touchscreen.multitouch.distinct"

### FEATURE_TOUCHSCREEN_MULTITOUCH_JAZZHAND

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_TOUCHSCREEN_MULTITOUCH_JAZZHAND: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device's touch screen is capable of tracking a full hand of fingers fully independently -- that is, 5 or more simultaneous independent pointers.

 Value: "android.hardware.touchscreen.multitouch.jazzhand"

### FEATURE_USB_ACCESSORY

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_USB_ACCESSORY: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports connecting to USB accessories.

 Value: "android.hardware.usb.accessory"

### FEATURE_USB_HOST

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_USB_HOST: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports connecting to USB devices as the USB host.

 Value: "android.hardware.usb.host"

### FEATURE_UWB

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_UWB: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device is capable of communicating with other devices via ultra wideband.

 Value: "android.hardware.uwb"

### FEATURE_VERIFIED_BOOT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_VERIFIED_BOOT: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports verified boot.

 Value: "android.software.verified_boot"

### FEATURE_VR_HEADTRACKING

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_VR_HEADTRACKING: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device implements headtracking suitable for a VR device.

 Value: "android.hardware.vr.headtracking"

### FEATURE_VR_MODE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_VR_MODE: String
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_VR_MODE_HIGH_PERFORMANCE:kotlin.String` instead.*

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device implements an optimized mode for virtual reality (VR) applications that handles stereoscopic rendering of notifications, and disables most monocular system UI components while a VR application has user focus. Devices declaring this feature must include an application implementing a `https://developer.android.com/reference/kotlin/android/service/vr/VrListenerService.html#` that can be targeted by VR applications via setVrModeEnabled.

 Value: "android.software.vr.mode"

### FEATURE_VR_MODE_HIGH_PERFORMANCE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_VR_MODE_HIGH_PERFORMANCE: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device implements an optimized mode for virtual reality (VR) applications that handles stereoscopic rendering of notifications, disables most monocular system UI components while a VR application has user focus and meets extra CDD requirements to provide a high-quality VR experience. Devices declaring this feature must include an application implementing a `https://developer.android.com/reference/kotlin/android/service/vr/VrListenerService.html#` that can be targeted by VR applications via setVrModeEnabled. and must meet CDD requirements to provide a high-quality VR experience.

 Value: "android.hardware.vr.high_performance"

### FEATURE_VULKAN_DEQP_LEVEL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_VULKAN_DEQP_LEVEL: String
```

Feature for getSystemAvailableFeatures and hasSystemFeature: If this feature is supported, the feature version specifies a date such that the device is known to pass the Vulkan dEQP test suite associated with that date. The date is encoded as follows:

- Year in bits 31-16
- Month in bits 15-8
- Day in bits 7-0

<br />

Example: 2019-03-01 is encoded as 0x07E30301, and would indicate that the device passes the Vulkan dEQP test suite version that was current on 2019-03-01.

 Value: "android.software.vulkan.deqp.level"

### FEATURE_VULKAN_HARDWARE_COMPUTE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_VULKAN_HARDWARE_COMPUTE: String
```

Feature for getSystemAvailableFeatures and hasSystemFeature: If this feature is supported, the Vulkan implementation on this device is hardware accelerated, and the Vulkan native API will enumerate at least one `VkPhysicalDevice`, and the feature version will indicate what level of optional compute features that device supports beyond the Vulkan 1.0 requirements.

Compute level 0 indicates:

- The `VK_KHR_variable_pointers` extension and `VkPhysicalDeviceVariablePointerFeaturesKHR::variablePointers` feature are supported.
- `VkPhysicalDeviceLimits::maxPerStageDescriptorStorageBuffers` is at least 16.

 Value: "android.hardware.vulkan.compute"

### FEATURE_VULKAN_HARDWARE_LEVEL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_VULKAN_HARDWARE_LEVEL: String
```

Feature for getSystemAvailableFeatures and hasSystemFeature: If this feature is supported, the Vulkan implementation on this device is hardware accelerated, and the Vulkan native API will enumerate at least one `VkPhysicalDevice`, and the feature version will indicate what level of optional hardware features limits it supports.

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

 Value: "android.hardware.vulkan.level"

### FEATURE_VULKAN_HARDWARE_VERSION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_VULKAN_HARDWARE_VERSION: String
```

Feature for getSystemAvailableFeatures and hasSystemFeature: If this feature is supported, the Vulkan implementation on this device is hardware accelerated, and the feature version will indicate the highest `VkPhysicalDeviceProperties::apiVersion` supported by the physical devices that support the hardware level indicated by `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_VULKAN_HARDWARE_LEVEL:kotlin.String`. The feature version uses the same encoding as Vulkan version numbers:

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

 Value: "android.hardware.vulkan.version"

### FEATURE_WALLET_LOCATION_BASED_SUGGESTIONS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_WALLET_LOCATION_BASED_SUGGESTIONS: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports showing location-based suggestions for wallet cards provided by the default payment app.

 Value: "android.software.wallet_location_based_suggestions"

### FEATURE_WATCH

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_WATCH: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: This is a device dedicated to showing UI on a watch. A watch here is defined to be a device worn on the body, perhaps on the wrist. The user is very close when interacting with the device.

 Value: "android.hardware.type.watch"

### FEATURE_WEBVIEW

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_WEBVIEW: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device has a full implementation of the android.webkit.\* APIs. Devices lacking this feature will not have a functioning WebView implementation.

 Value: "android.software.webview"

### FEATURE_WIFI

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_WIFI: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports WiFi (802.11) networking.

 Value: "android.hardware.wifi"

### FEATURE_WIFI_AWARE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_WIFI_AWARE: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Wi-Fi Aware.

 Value: "android.hardware.wifi.aware"

### FEATURE_WIFI_DIRECT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_WIFI_DIRECT: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Wi-Fi Direct networking.

 Value: "android.hardware.wifi.direct"

### FEATURE_WIFI_PASSPOINT

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_WIFI_PASSPOINT: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Wi-Fi Passpoint and all Passpoint related APIs in `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#` are supported. Refer to addOrUpdatePasspointConfiguration for more info.

 Value: "android.hardware.wifi.passpoint"

### FEATURE_WIFI_RTT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_WIFI_RTT: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports Wi-Fi RTT (IEEE 802.11mc).

 Value: "android.hardware.wifi.rtt"

### FEATURE_WINDOW_MAGNIFICATION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_WINDOW_MAGNIFICATION: String
```

Feature for getSystemAvailableFeatures and #hasSystemFeature: The device supports window magnification.

 Value: "android.software.window_magnification"

**See Also**

- `https://developer.android.com/reference/kotlin/android/accessibilityservice/MagnificationConfig.html#MAGNIFICATION_MODE_WINDOW:kotlin.Int`

### FLAG_PERMISSION_WHITELIST_INSTALLER

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_PERMISSION_WHITELIST_INSTALLER: Int
```

Permission whitelist flag: permissions whitelisted by the installer. Permissions can also be whitelisted by the system, on upgrade, or on role grant.

**Note:**In retrospect it would have been preferred to use more inclusive terminology when naming this API. Similar APIs added will refrain from using the term "whitelist".

 Value: 2

### FLAG_PERMISSION_WHITELIST_SYSTEM

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_PERMISSION_WHITELIST_SYSTEM: Int
```

Permission whitelist flag: permissions whitelisted by the system. Permissions can also be whitelisted by the installer, on upgrade, or on role grant.

**Note:**In retrospect it would have been preferred to use more inclusive terminology when naming this API. Similar APIs added will refrain from using the term "whitelist".

 Value: 1

### FLAG_PERMISSION_WHITELIST_UPGRADE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_PERMISSION_WHITELIST_UPGRADE: Int
```

Permission whitelist flag: permissions whitelisted by the system when upgrading from an OS version where the permission was not restricted to an OS version where the permission is restricted. Permissions can also be whitelisted by the installer, the system, or on role grant.

**Note:**In retrospect it would have been preferred to use more inclusive terminology when naming this API. Similar APIs added will refrain from using the term "whitelist".

 Value: 4

### GET_ACTIVITIES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_ACTIVITIES: Int
```

PackageInfo flag: return information about activities in the package in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#activities:kotlin.Array`.

 Value: 1

### GET_APP_LOCK_INFO

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_APP_LOCK_INFO: Long
```

ApplicationInfo, ComponentInfo, and ResolveInfo flag: return the `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#isAppLockSupported:kotlin.Boolean` and `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#isAppLockEnabled:kotlin.Boolean` associated with an application.

The caller should have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#LOCK_APPS:kotlin.String` permission, or a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown. This flag cannot be used with `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_ATTRIBUTIONS:kotlin.Int`, if the caller wishes to retrieve attributions, they must use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_ATTRIBUTIONS_LONG:kotlin.Long`.

 Value: 34359738368L

### GET_ATTRIBUTIONS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_ATTRIBUTIONS: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_ATTRIBUTIONS_LONG:kotlin.Long` to avoid unintended sign extension. Operations with this flag may cause unintended results and potential `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#`.*

 Value: -2147483648

### GET_ATTRIBUTIONS_LONG

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_ATTRIBUTIONS_LONG: Long
```

PackageInfo flag: return all attributions declared in the package manifest

 Value: 2147483648L

### GET_CONFIGURATIONS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_CONFIGURATIONS: Int
```

PackageInfo flag: return information about hardware preferences in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#configPreferences:kotlin.Array`, and requested features in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#reqFeatures:kotlin.Array` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#featureGroups:kotlin.Array`.

 Value: 16384

### GET_DISABLED_COMPONENTS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_DISABLED_COMPONENTS: Int
```

**Deprecated:** *replaced with `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DISABLED_COMPONENTS:kotlin.Int`*

 Value: 512

### GET_DISABLED_UNTIL_USED_COMPONENTS

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_DISABLED_UNTIL_USED_COMPONENTS: Int
```

**Deprecated:** *replaced with `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DISABLED_UNTIL_USED_COMPONENTS:kotlin.Int`.*

 Value: 32768

### GET_GIDS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_GIDS: Int
```

PackageInfo flag: return the `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#gids:kotlin.IntArray` that are associated with an application. This applies for any API returning a PackageInfo class, either directly or nested inside of another.

 Value: 256

### GET_INSTRUMENTATION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_INSTRUMENTATION: Int
```

PackageInfo flag: return information about instrumentation in the package in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#instrumentation:kotlin.Array`.

 Value: 16

### GET_INTENT_FILTERS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_INTENT_FILTERS: Int
```

**Deprecated:** *The platform does not support getting `https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#`s for the package.*

PackageInfo flag: return information about the intent filters supported by the activity.

 Value: 32

### GET_META_DATA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_META_DATA: Int
```

ComponentInfo flag: return the `https://developer.android.com/reference/kotlin/android/content/pm/PackageItemInfo#metaData:android.os.Bundle` data `https://developer.android.com/reference/kotlin/android/os/Bundle.html#`s that are associated with a component. This applies for any API returning a ComponentInfo subclass.

 Value: 128

### GET_PERMISSIONS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_PERMISSIONS: Int
```

PackageInfo flag: return information about permissions in the package in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#permissions:kotlin.Array`.

 Value: 4096

### GET_PROVIDERS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_PROVIDERS: Int
```

PackageInfo flag: return information about content providers in the package in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#providers:kotlin.Array`.

 Value: 8

### GET_RECEIVERS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_RECEIVERS: Int
```

PackageInfo flag: return information about intent receivers in the package in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#receivers:kotlin.Array`.

 Value: 2

### GET_RESOLVED_FILTER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_RESOLVED_FILTER: Int
```

ResolveInfo flag: return the IntentFilter that was matched for a particular ResolveInfo in `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo#filter:android.content.IntentFilter`.

 Value: 64

### GET_SERVICES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_SERVICES: Int
```

PackageInfo flag: return information about services in the package in `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo#services:kotlin.Array`.

 Value: 4

### GET_SHARED_LIBRARY_FILES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_SHARED_LIBRARY_FILES: Int
```

ApplicationInfo flag: return the `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#sharedLibraryFiles:kotlin.Array` that are associated with an application. This applies for any API returning an ApplicationInfo class, either directly or nested inside of another.

 Value: 1024

### GET_SIGNATURES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_SIGNATURES: Int
```

**Deprecated:** *use `GET_SIGNING_CERTIFICATES` instead*

PackageInfo flag: return information about the signatures included in the package.

 Value: 64

### GET_SIGNING_CERTIFICATES

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_SIGNING_CERTIFICATES: Int
```

PackageInfo flag: return the signing certificates associated with this package. Each entry is a signing certificate that the package has proven it is authorized to use, usually a past signing certificate from which it has rotated.

 Value: 134217728

### GET_UNINSTALLED_PACKAGES

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_UNINSTALLED_PACKAGES: Int
```

**Deprecated:** *replaced with `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_UNINSTALLED_PACKAGES:kotlin.Int`*

 Value: 8192

### GET_URI_PERMISSION_PATTERNS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_URI_PERMISSION_PATTERNS: Int
```

ProviderInfo flag: return the `https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo#uriPermissionPatterns:kotlin.Array` that are associated with a content provider. This applies for any API returning a ProviderInfo class, either directly or nested inside of another.

 Value: 2048

### INSTALL_REASON_DEVICE_RESTORE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INSTALL_REASON_DEVICE_RESTORE: Int
```

Code indicating that this package was installed as part of restoring from another device.

 Value: 2

### INSTALL_REASON_DEVICE_SETUP

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INSTALL_REASON_DEVICE_SETUP: Int
```

Code indicating that this package was installed as part of device setup.

 Value: 3

### INSTALL_REASON_POLICY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INSTALL_REASON_POLICY: Int
```

Code indicating that this package was installed due to enterprise policy.

 Value: 1

### INSTALL_REASON_UNKNOWN

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INSTALL_REASON_UNKNOWN: Int
```

Code indicating that the reason for installing this package is unknown.

 Value: 0

### INSTALL_REASON_USER

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INSTALL_REASON_USER: Int
```

Code indicating that the package installation was initiated by the user.

 Value: 4

### INSTALL_SCENARIO_BULK

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INSTALL_SCENARIO_BULK: Int
```

Installation scenario indicating a bulk operation with the desired result of a fully optimized application. If the system is busy or resources are scarce the system will perform less work to avoid impacting system health. Examples of bulk installation scenarios might include device restore, background updates of multiple applications, or user-triggered updates for all applications. The decision to use BULK or BULK_SECONDARY should be based on the desired user experience. BULK_SECONDARY operations may take less time to complete but, when they do, will produce less optimized applications. The device state (e.g. memory usage or battery status) should not be considered when making this decision as those factors are taken into account by the Package Manager when acting on the installation scenario.

 Value: 2

### INSTALL_SCENARIO_BULK_SECONDARY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INSTALL_SCENARIO_BULK_SECONDARY: Int
```

Installation scenario indicating a bulk operation that prioritizes minimal system health impact over application optimization. The application may undergo additional optimization if the system is idle and system resources are abundant. The more elements of a bulk operation that are marked BULK_SECONDARY, the faster the entire bulk operation will be. See the comments for INSTALL_SCENARIO_BULK for more information.

 Value: 3

### INSTALL_SCENARIO_DEFAULT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INSTALL_SCENARIO_DEFAULT: Int
```

A value to indicate the lack of CUJ information, disabling all installation scenario logic.

 Value: 0

### INSTALL_SCENARIO_FAST

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INSTALL_SCENARIO_FAST: Int
```

Installation scenario providing the fastest "install button to launch" experience possible.

 Value: 1

### MATCH_ALL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_ALL: Int
```

Querying flag: if set and if the platform is doing any filtering of the results, then the filtering will not happen. This is a synonym for saying that all results should be returned.

*This flag should be used with extreme care.*

 Value: 131072

### MATCH_APEX

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_APEX: Int
```

PackageInfo flag: include APEX packages that are currently installed. In APEX terminology, this corresponds to packages that are currently active, i.e. mounted and available to other processes of the OS. In particular, this flag alone will not match APEX files that are staged for activation at next reboot.

 Value: 1073741824

### MATCH_ARCHIVED_PACKAGES

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_ARCHIVED_PACKAGES: Long
```

Flag parameter to also retrieve some information about archived packages. Packages can be archived through requestArchive and do not have any APKs stored on the device, but do keep the data directory.

Note: Archived apps are a subset of apps returned by `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_UNINSTALLED_PACKAGES:kotlin.Int`.

Note: this flag may cause less information about currently installed applications to be returned.

Note: use of this flag requires the android.permission.QUERY_ALL_PACKAGES permission to see uninstalled packages.

 Value: 4294967296L

### MATCH_DEFAULT_ONLY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_DEFAULT_ONLY: Int
```

Resolution and querying flag: if set, only filters that support the `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_DEFAULT:kotlin.String` will be considered for matching. This is a synonym for including the CATEGORY_DEFAULT in your supplied Intent.

 Value: 65536

### MATCH_DIRECT_BOOT_AUTO

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_DIRECT_BOOT_AUTO: Int
```

Querying flag: automatically match components based on their Direct Boot awareness and the current user state.

Since the default behavior is to automatically apply the current user state, this is effectively a sentinel value that doesn't change the output of any queries based on its presence or absence.

Instead, this value can be useful in conjunction with detectImplicitDirectBoot to detect when a caller is relying on implicit automatic matching, instead of confirming the explicit behavior they want, using a combination of these flags:

- `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DIRECT_BOOT_AWARE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DIRECT_BOOT_UNAWARE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DIRECT_BOOT_AUTO:kotlin.Int`

 Value: 268435456

### MATCH_DIRECT_BOOT_AWARE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_DIRECT_BOOT_AWARE: Int
```

Querying flag: match components which are direct boot *aware* in the returned info, regardless of the current user state.

When neither `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DIRECT_BOOT_AWARE:kotlin.Int` nor `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DIRECT_BOOT_UNAWARE:kotlin.Int` are specified, the default behavior is to match only runnable components based on the user state. For example, when a user is started but credentials have not been presented yet, the user is running "locked" and only `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DIRECT_BOOT_AWARE:kotlin.Int` components are returned. Once the user credentials have been presented, the user is running "unlocked" and both `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DIRECT_BOOT_AWARE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DIRECT_BOOT_UNAWARE:kotlin.Int` components are returned.

 Value: 524288

**See Also**

- isUserUnlocked

### MATCH_DIRECT_BOOT_UNAWARE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_DIRECT_BOOT_UNAWARE: Int
```

Querying flag: match components which are direct boot *unaware* in the returned info, regardless of the current user state.

When neither `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DIRECT_BOOT_AWARE:kotlin.Int` nor `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DIRECT_BOOT_UNAWARE:kotlin.Int` are specified, the default behavior is to match only runnable components based on the user state. For example, when a user is started but credentials have not been presented yet, the user is running "locked" and only `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DIRECT_BOOT_AWARE:kotlin.Int` components are returned. Once the user credentials have been presented, the user is running "unlocked" and both `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DIRECT_BOOT_AWARE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DIRECT_BOOT_UNAWARE:kotlin.Int` components are returned.

 Value: 262144

**See Also**

- isUserUnlocked

### MATCH_DISABLED_COMPONENTS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_DISABLED_COMPONENTS: Int
```

PackageInfo flag: include disabled components in the returned info.

 Value: 512

### MATCH_DISABLED_UNTIL_USED_COMPONENTS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_DISABLED_UNTIL_USED_COMPONENTS: Int
```

PackageInfo flag: include disabled components which are in that state only because of `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DISABLED_UNTIL_USED:kotlin.Int` in the returned info. Note that if you set this flag, applications that are in this disabled state will be reported as enabled.

 Value: 32768

### MATCH_SYSTEM_ONLY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_SYSTEM_ONLY: Int
```

Querying flag: include only components from applications that are marked with `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_SYSTEM:kotlin.Int`.

 Value: 1048576

### MATCH_UNINSTALLED_PACKAGES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_UNINSTALLED_PACKAGES: Int
```

Flag parameter to retrieve some information about all applications (even uninstalled ones) which have data directories. This state could have resulted if applications have been deleted with flag `DELETE_KEEP_DATA` with a possibility of being replaced or reinstalled in future.

Note: this flag may cause less information about currently installed applications to be returned.

Note: use of this flag requires the android.permission.QUERY_ALL_PACKAGES permission to see uninstalled packages.

 Value: 8192

### MAXIMUM_VERIFICATION_TIMEOUT

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAXIMUM_VERIFICATION_TIMEOUT: Long
```

Can be used as the `millisecondsToDelay` argument for extendVerificationTimeout. This is the maximum time `PackageManager` waits for the verification agent to return (in milliseconds).

 Value: 3600000L

### PERMISSION_DENIED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PERMISSION_DENIED: Int
```

Permission check result: this is returned by checkPermission if the permission has not been granted to the given package.

 Value: -1

### PERMISSION_GRANTED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PERMISSION_GRANTED: Int
```

Permission check result: this is returned by checkPermission if the permission has been granted to the given package.

 Value: 0

### PROPERTY_COMPAT_OVERRIDE_LANDSCAPE_TO_PORTRAIT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_COMPAT_OVERRIDE_LANDSCAPE_TO_PORTRAIT: String
```

Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property` for an app to inform the system that the app can be opted-in or opted-out from the compatibility treatment that rotates camera output by 90 degrees on landscape sensors on devices known to have compatibility issues.

The treatment is disabled by default but device manufacturers can enable the treatment using their discretion to improve camera compatibility. With this property set to `false`, the rotation will not be applied. A value of `true` will ensure that rotation is applied, provided it is enabled for the device. In most cases, if rotation is the desired behavior this property need not be set. However, if your app experiences stretching or incorrect rotation on these devices, explicitly setting this to `true` may resolve that behavior. Apps should set this to `false` if there is confidence that the app handles `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SENSOR_ORIENTATION:android.hardware.camera2.CameraCharacteristics.Key` correctly. See [the documentation for best practice.](https://developer.android.com/training/camera2/camera-preview)

**Syntax:**

```kotlin
<application>
    <property
      android:name="android.camera.PROPERTY_COMPAT_OVERRIDE_LANDSCAPE_TO_PORTRAIT"
      android:value="true|false"/>
  </application>
  
```

 Value: "android.camera.PROPERTY_COMPAT_OVERRIDE_LANDSCAPE_TO_PORTRAIT"

### PROPERTY_MEDIA_CAPABILITIES

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_MEDIA_CAPABILITIES: String
```

\<application\> level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property` tag specifying the XML resource ID containing an application's media capabilities XML file For example: \<application\> \<property android:name="android.media.PROPERTY_MEDIA_CAPABILITIES" android:resource="@xml/media_capabilities"\> \<application\>

 Value: "android.media.PROPERTY_MEDIA_CAPABILITIES"

### PROPERTY_NATIVE_SERVICE_FUNCTION_NAME

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_NATIVE_SERVICE_FUNCTION_NAME: String
```

Service level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property` tag for native services specifying the symbol name of the entry point function for the service. If not specified, the system executes `ANativeService_onCreate`.

Example:

```kotlin
<service android:isolatedProcess="true"
                    android:nativeService="true">
    <property
      android:name="android.app.PROPERTY_NATIVE_SERVICE_FUNCTION_NAME"
      android:value="native_service_createService"/>
  </service>
  
```

 Value: "android.app.PROPERTY_NATIVE_SERVICE_FUNCTION_NAME"

### PROPERTY_NATIVE_SERVICE_LIBRARY_NAME

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_NATIVE_SERVICE_LIBRARY_NAME: String
```

Service level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property` tag for native services specifying the name of the library to be loaded to the process that hosts the service. If not specified, the system tries to load `libmain.so`.

Example:

```kotlin
<service android:isolatedProcess="true"
                    android:nativeService="true">
    <property
      android:name="android.app.PROPERTY_NATIVE_SERVICE_LIBRARY_NAME"
      android:value="libnativeservice.so"/>
  </service>
  
```

 Value: "android.app.PROPERTY_NATIVE_SERVICE_LIBRARY_NAME"

### PROPERTY_SELF_CERTIFIED_NETWORK_CAPABILITIES

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_SELF_CERTIFIED_NETWORK_CAPABILITIES: String
```

\<application\> level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property` tag specifying the XML resource ID containing the declaration of the self-certified network capabilities used by the application.

Starting from Android 14, usage of some network capabilities in android.net.ConnectivityManager#requestNetwork require the application to declare its usage of that particular capability in this resource. Only some capabilities require a declaration. Please look up the specific capability you want to use in `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#` to see if it needs declaration in this property. For example: \<application\> \<property android:name="android.net.PROPERTY_SELF_CERTIFIED_NETWORK_CAPABILITIES" android:resource="@xml/self_certified_network_capabilities"\> \<application\>

The detail format of self_certified_network_capabilities.xml is described in `https://developer.android.com/reference/kotlin/android/net/NetworkRequest.html#`

 Value: "android.net.PROPERTY_SELF_CERTIFIED_NETWORK_CAPABILITIES"

### PROPERTY_SPECIAL_USE_FGS_SUBTYPE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_SPECIAL_USE_FGS_SUBTYPE: String
```

\<service\> level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property` tag specifying the actual use case of the service if it's foreground service with the type `https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo#FOREGROUND_SERVICE_TYPE_SPECIAL_USE:kotlin.Int`.

For example: \<service\> \<property android:name="android.app.PROPERTY_SPECIAL_USE_FGS_SUBTYPE" android:value="foo"/\> \</service\>

 Value: "android.app.PROPERTY_SPECIAL_USE_FGS_SUBTYPE"

### PROPERTY_USE_RESTRICTED_BACKUP_MODE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_USE_RESTRICTED_BACKUP_MODE: String
```

\<application\> level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property` tag specifying whether the app should be put into the "restricted" backup mode when it's started for backup and restore operations.

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

 Value: "android.app.backup.PROPERTY_USE_RESTRICTED_BACKUP_MODE"

### SIGNATURE_FIRST_NOT_SIGNED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNATURE_FIRST_NOT_SIGNED: Int
```

Signature check result: this is returned by #checkSignatures if the first package is not signed but the second is.

 Value: -1

### SIGNATURE_MATCH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNATURE_MATCH: Int
```

Signature check result: this is returned by #checkSignatures if all signatures on the two packages match.

 Value: 0

### SIGNATURE_NEITHER_SIGNED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNATURE_NEITHER_SIGNED: Int
```

Signature check result: this is returned by #checkSignatures if neither of the two packages is signed.

 Value: 1

### SIGNATURE_NO_MATCH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNATURE_NO_MATCH: Int
```

Signature check result: this is returned by #checkSignatures if not all signatures on both packages match.

 Value: -3

### SIGNATURE_SECOND_NOT_SIGNED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNATURE_SECOND_NOT_SIGNED: Int
```

Signature check result: this is returned by #checkSignatures if the second package is not signed but the first is.

 Value: -2

### SIGNATURE_UNKNOWN_PACKAGE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNATURE_UNKNOWN_PACKAGE: Int
```

Signature check result: this is returned by #checkSignatures if either of the packages are not valid.

 Value: -4

### SYNCHRONOUS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYNCHRONOUS: Int
```

Flag parameter for setComponentEnabledSetting to indicate that the given user's package restrictions state will be serialised to disk after the component state has been updated. Note that this is synchronous disk access, so calls using this flag should be run on a background thread.

 Value: 2

### VERIFICATION_ALLOW

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VERIFICATION_ALLOW: Int
```

Used as the `verificationCode` argument for verifyPendingInstall to indicate that the calling package verifier allows the installation to proceed.

 Value: 1

### VERIFICATION_REJECT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VERIFICATION_REJECT: Int
```

Used as the `verificationCode` argument for verifyPendingInstall to indicate the calling package verifier does not vote to allow the installation to proceed.

 Value: -1

### VERSION_CODE_HIGHEST

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VERSION_CODE_HIGHEST: Int
```

Constant for specifying the highest installed package version code.

 Value: -1

## Public constructors

### PackageManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PackageManager()
```

**Deprecated:** *Do not instantiate or subclass - obtain an instance from getPackageManager*

## Public methods

### addPackageToPreferred

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun addPackageToPreferred(packageName: String): Unit
```

**Deprecated:** *This function no longer does anything. It is the platform's responsibility to assign preferred activities and this cannot be modified directly. To determine the activities resolved by the platform, use #resolveActivity or #queryIntentActivities. To configure an app to be responsible for a particular role and to check current role holders, see `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#`.*

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### addPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun addPermission(info: PermissionInfo): Boolean
```

Add a new dynamic permission to the system. For this to work, your package must have defined a permission tree through the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestPermissionTree:kotlin.IntArray` tag in its manifest. A package can only add permissions to trees that were defined by either its own package or another with the same user id; a permission is in a tree if it matches the name of the permission tree + ".": for example, "com.foo.bar" is a member of the permission tree "com.foo".

It is good to make your permission tree name descriptive, because you are taking possession of that entire set of permission names. Thus, it must be under a domain you control, with a suffix that will not match any normal permissions that may be declared in any applications that are part of that domain.

New permissions must be added before any .apks are installed that use those permissions. Permissions you add through this method are remembered across reboots of the device. If the given permission already exists, the info you supply here will be used to update it.

| Parameters ||
|---|---|
| `info` | [PermissionInfo](PermissionInfo.md): Description of the permission to be added. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if a new permission was created, false if an existing one was updated. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if you are not allowed to add the given permission name. |

**See Also**

- removePermission

### addPermissionAsync

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun addPermissionAsync(info: PermissionInfo): Boolean
```

Like addPermission but asynchronously persists the package manager state after returning from the call, allowing it to return quicker and batch a series of adds at the expense of no guarantee the added permission will be retained if the device is rebooted before it is written.

| Parameters ||
|---|---|
| `info` | [PermissionInfo](PermissionInfo.md): This value cannot be `null`. |

### addPreferredActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun addPreferredActivity(
    filter: IntentFilter, 
    match: Int, 
    set: Array<ComponentName!>?, 
    activity: ComponentName
): Unit
```

**Deprecated:** *This function no longer does anything. It is the platform's responsibility to assign preferred activities and this cannot be modified directly. To determine the activities resolved by the platform, use #resolveActivity or #queryIntentActivities. To configure an app to be responsible for a particular role and to check current role holders, see `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#`.*

Add a new preferred activity mapping to the system. This will be used to automatically select the given activity component when startActivity finds multiple matching activities and also matches the given filter.

| Parameters ||
|---|---|
| `filter` | [IntentFilter](../android.content/IntentFilter.md): The set of intents under which this activity will be made preferred. This value cannot be `null`. |
| `match` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The IntentFilter match category that this preference applies to. |
| `set` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ComponentName](../android.content/ComponentName.md)!\>?: The set of activities that the user was picking from when this preference was made. This value may be `null`. |
| --- | --- |
| `activity` | [ComponentName](../android.content/ComponentName.md): The component name of the activity that is to be preferred. This value cannot be `null`. |

### addWhitelistedRestrictedPermission

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addWhitelistedRestrictedPermission(
    packageName: String, 
    permName: String, 
    whitelistFlags: Int
): Boolean
```

Adds a whitelisted restricted permission for an app.

Permissions can be hard restricted which means that the app cannot hold them or soft restricted where the app can hold the permission but in a weaker form. Whether a permission is `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#FLAG_HARD_RESTRICTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#FLAG_SOFT_RESTRICTED:kotlin.Int` depends on the permission declaration. Whitelisting a hard restricted permission allows for the to hold that permission and whitelisting a soft restricted permission allows the app to hold the permission in its full, unrestricted form.

<br />

There are four whitelists:
1. one for cases where the system permission policy whitelists a permission This list corresponds to the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_SYSTEM:kotlin.Int` flag. Can only be modified by pre-installed holders of a dedicated permission.
2. one for cases where the system whitelists the permission when upgrading from an OS version in which the permission was not restricted to an OS version in which the permission is restricted. This list corresponds to the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_UPGRADE:kotlin.Int` flag. Can be modified by pre-installed holders of a dedicated permission. The installer on record can only remove permissions from this whitelist.
3. one for cases where the installer of the package whitelists a permission. This list corresponds to the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_INSTALLER:kotlin.Int` flag. Can be modified by pre-installed holders of a dedicated permission or the installer on record.

You need to specify the whitelists for which to set the whitelisted permissions which will clear the previous whitelisted permissions and replace them with the provided ones.

**Note:**In retrospect it would have been preferred to use more inclusive terminology when naming this API. Similar APIs added will refrain from using the term "whitelist".

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The app for which to get whitelisted permissions. This value cannot be `null`. |
| `permName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The whitelisted permission to add. This value cannot be `null`. |
| `whitelistFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The whitelists to which to add. Passing multiple flags updates all specified whitelists. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_INSTALLER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_UPGRADE:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the permission was added to the whitelist. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if you try to modify a whitelist that you have no access to. |

**See Also**

- getWhitelistedRestrictedPermissions
- removeWhitelistedRestrictedPermission
- `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_SYSTEM:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_UPGRADE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_INSTALLER:kotlin.Int`

### canPackageQuery

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canPackageQuery(
    sourcePackageName: String, 
    targetPackageName: String
): Boolean
```

Returns `true` if the source package is able to query for details about the target package. Applications that share details about other applications should use this API to determine if those details should be withheld from callers that do not otherwise have visibility of them.

Note: The caller must be able to query for details about the source and target package. A `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.NameNotFoundException` is thrown if it isn't.

| Parameters ||
|---|---|
| `sourcePackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The source package that would receive details about the target package. This value cannot be `null`. |
| `targetPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The target package whose details would be shared with the source package. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the source package is able to query for details about the target package. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if either a given package can not be found on the system, or if the caller is not able to query for details about the source or target package. |

### canPackageQuery

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canPackageQuery(
    sourcePackageName: String, 
    targetPackageNames: Array<String!>
): BooleanArray
```

Same as canPackageQuery but accepts an array of target packages to be queried.

| Parameters ||
|---|---|
| `sourcePackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The source package that would receive details about the target package. This value cannot be `null`. |
| `targetPackageNames` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: An array of target packages whose details would be shared with the source package. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html` | An array of booleans where each member specifies whether the source package is able to query for details about the target package given by the corresponding value at the same index in the array of target packages. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if either a given package can not be found on the system, or if the caller is not able to query for details about the source or target packages. |

### canRequestPackageInstalls

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun canRequestPackageInstalls(): Boolean
```

Checks whether the calling package is allowed to request package installs through package installer. Apps are encouraged to call this API before launching the package installer via intent `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_INSTALL_PACKAGE:kotlin.String`. Starting from Android O, the user can explicitly choose what external sources they trust to install apps on the device. If this API returns false, the install request will be blocked by the package installer and a dialog will be shown to the user with an option to launch settings to change their preference. An application must target Android O or higher and declare permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REQUEST_INSTALL_PACKAGES:kotlin.String` in order to use this API.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the calling package is trusted by the user to request install packages on the device, false otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_INSTALL_PACKAGE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/provider/Settings.html#ACTION_MANAGE_UNKNOWN_APP_SOURCES:kotlin.String`

### canonicalToCurrentPackageNames

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun canonicalToCurrentPackageNames(packageNames: Array<String!>): Array<String!>!
```

Map from a packages canonical name to the current name in use on the device.

| Parameters ||
|---|---|
| `packageNames` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: Array of new names to be mapped. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | Returns an array of the same size as the original, containing the current name for each package. |

### checkPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun checkPermission(
    permName: String, 
    packageName: String
): Int
```

Check whether a particular package has been granted a particular permission.

**Note:** This API returns the underlying permission state as-is and is mostly intended for permission managing system apps. To perform an access check for a certain app, please use the checkPermission APIs instead.

| Parameters ||
|---|---|
| `permName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the permission you are checking for. This value cannot be `null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the package you are checking against. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | If the package has the permission, PERMISSION_GRANTED is returned. If it does not have the permission, PERMISSION_DENIED is returned. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_GRANTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_DENIED:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_GRANTED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_DENIED:kotlin.Int`

### checkSignatures

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun checkSignatures(
    uid1: Int, 
    uid2: Int
): Int
```

Like checkSignatures, but takes UIDs of the two packages to be checked. This can be useful, for example, when doing the check in an IPC, where the UID is the only identity available. It is functionally identical to determining the package associated with the UIDs and checking their signatures.

| Parameters ||
|---|---|
| `uid1` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): First UID whose signature will be compared. |
| `uid2` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Second UID whose signature will be compared. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns an integer indicating whether all signatures on the two packages match. The value is \>= 0 (`https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_MATCH:kotlin.Int`) if all signatures match or \< 0 if there is not a match (`https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_NO_MATCH:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_UNKNOWN_PACKAGE:kotlin.Int`). Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_MATCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_NEITHER_SIGNED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_FIRST_NOT_SIGNED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_SECOND_NOT_SIGNED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_NO_MATCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_UNKNOWN_PACKAGE:kotlin.Int` |

**See Also**

- checkSignatures

### checkSignatures

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun checkSignatures(
    packageName1: String, 
    packageName2: String
): Int
```

Compare the signatures of two packages to determine if the same signature appears in both of them. If they do contain the same signature, then they are allowed special privileges when working with each other: they can share the same user-id, run instrumentation against each other, etc.

| Parameters ||
|---|---|
| `packageName1` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): First package name whose signature will be compared. This value cannot be `null`. |
| `packageName2` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Second package name whose signature will be compared. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns an integer indicating whether all signatures on the two packages match. The value is \>= 0 (`https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_MATCH:kotlin.Int`) if all signatures match or \< 0 if there is not a match (`https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_NO_MATCH:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_UNKNOWN_PACKAGE:kotlin.Int`). Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_MATCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_NEITHER_SIGNED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_FIRST_NOT_SIGNED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_SECOND_NOT_SIGNED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_NO_MATCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SIGNATURE_UNKNOWN_PACKAGE:kotlin.Int` |

**See Also**

- checkSignatures

### clearInstantAppCookie

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun clearInstantAppCookie(): Unit
```

Clears the instant application cookie for the calling app.
**See Also**

- isInstantApp
- isInstantApp
- getInstantAppCookieMaxBytes
- getInstantAppCookie
- clearInstantAppCookie

### clearPackagePreferredActivities

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun clearPackagePreferredActivities(packageName: String): Unit
```

**Deprecated:** *This function no longer does anything. It is the platform's responsibility to assign preferred activities and this cannot be modified directly. To determine the activities resolved by the platform, use #resolveActivity or #queryIntentActivities. To configure an app to be responsible for a particular role and to check current role holders, see `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#`.*

Remove all preferred activity mappings, previously added with addPreferredActivity, from the system whose activities are implemented in the given package name. An application can only clear its own package(s).

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the package whose preferred activity mappings are to be removed. This value cannot be `null`. |

### currentToCanonicalPackageNames

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun currentToCanonicalPackageNames(packageNames: Array<String!>): Array<String!>!
```

Map from the current package names in use on the device to whatever the current canonical name of that package is.

| Parameters ||
|---|---|
| `packageNames` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: Array of current names to be mapped. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | Returns an array of the same size as the original, containing the canonical name for each package. |

### extendVerificationTimeout

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun extendVerificationTimeout(
    id: Int, 
    verificationCodeAtTimeout: Int, 
    millisecondsToDelay: Long
): Unit
```

Allows a package listening to the `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_NEEDS_VERIFICATION:kotlin.String` to extend the default timeout for a response and declare what action to perform after the timeout occurs. The response must include the `verificationCodeAtTimeout` which is one of `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#VERIFICATION_ALLOW:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#VERIFICATION_REJECT:kotlin.Int`. This method can be called multiple times, but the total amount of time extension time will be limited to `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MAXIMUM_VERIFICATION_TIMEOUT:kotlin.Long`. If the method is called multiple times with different `verificationCodeAtTimeout`, then previous `verificationCodeAtTimeout` will be ignored and only the latest one will take effect. If this method is called after calling verifyPendingInstall, it may nullify the result set by verifyPendingInstall.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): pending package identifier as passed via the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#EXTRA_VERIFICATION_ID:kotlin.String` Intent extra. |
| `verificationCodeAtTimeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): either `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#VERIFICATION_ALLOW:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#VERIFICATION_REJECT:kotlin.Int`. If `verificationCodeAtTimeout` is neither `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#VERIFICATION_ALLOW:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#VERIFICATION_REJECT:kotlin.Int`, then `verificationCodeAtTimeout` will default to `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#VERIFICATION_REJECT:kotlin.Int`. |
| `millisecondsToDelay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the amount of time requested for the timeout. Must be positive and less than `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MAXIMUM_VERIFICATION_TIMEOUT:kotlin.Long`. If `millisecondsToDelay` is out of bounds, `millisecondsToDelay` will be set to the closest in bounds value; namely, 0 or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MAXIMUM_VERIFICATION_TIMEOUT:kotlin.Long`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller does not have the PACKAGE_VERIFICATION_AGENT permission. |

### getActivityBanner

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getActivityBanner(activityName: ComponentName): Drawable?
```

Retrieve the banner associated with an activity. Given the full name of an activity, retrieves the information about it and calls loadIcon to return its banner. If the activity cannot be found, NameNotFoundException is thrown.

The returned drawable is subject to the same size capping limits as described in getApplicationIcon.

| Parameters ||
|---|---|
| `activityName` | [ComponentName](../android.content/ComponentName.md): Name of the activity whose banner is to be retrieved. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | Returns the image of the banner, or null if the activity has no banner specified. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for the given activity could not be loaded. |

**See Also**

- getActivityBanner

### getActivityBanner

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getActivityBanner(intent: Intent): Drawable?
```

Retrieve the banner associated with an Intent. If intent.getClassName() is set, this simply returns the result of getActivityBanner(intent.getClassName()). Otherwise it resolves the intent's component and returns the banner associated with the resolved component. If intent.getClassName() cannot be found or the Intent cannot be resolved to a component, NameNotFoundException is thrown.

| Parameters ||
|---|---|
| `intent` | [Intent](../android.content/Intent.md): The intent for which you would like to retrieve a banner. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | Returns the image of the banner, or null if the activity has no banner specified. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for application matching the given intent could not be loaded. |

**See Also**

- getActivityBanner

### getActivityIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getActivityIcon(activityName: ComponentName): Drawable
```

Retrieve the icon associated with an activity. Given the full name of an activity, retrieves the information about it and calls loadIcon to return its icon. If the activity cannot be found, NameNotFoundException is thrown.

The returned drawable is subject to the same size capping limits as described in getApplicationIcon.

| Parameters ||
|---|---|
| `activityName` | [ComponentName](../android.content/ComponentName.md): Name of the activity whose icon is to be retrieved. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` | Returns the image of the icon, or the default activity icon if it could not be found. Does not return null. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for the given activity could not be loaded. |

**See Also**

- getActivityIcon

### getActivityIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getActivityIcon(intent: Intent): Drawable
```

Retrieve the icon associated with an Intent. If intent.getClassName() is set, this simply returns the result of getActivityIcon(intent.getClassName()). Otherwise it resolves the intent's component and returns the icon associated with the resolved component. If intent.getClassName() cannot be found or the Intent cannot be resolved to a component, NameNotFoundException is thrown.

| Parameters ||
|---|---|
| `intent` | [Intent](../android.content/Intent.md): The intent for which you would like to retrieve an icon. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` | Returns the image of the icon, or the default activity icon if it could not be found. Does not return null. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for application matching the given intent could not be loaded. |

**See Also**

- getActivityIcon

### getActivityInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActivityInfo(
    component: ComponentName, 
    flags: PackageManager.ComponentInfoFlags
): ActivityInfo
```

See getActivityInfo.

| Parameters ||
|---|---|
| `component` | [ComponentName](../android.content/ComponentName.md): This value cannot be `null`. |
| `flags` | [PackageManager.ComponentInfoFlags](../android/content/pm/PackageManager.ComponentInfoFlags.md): This value cannot be `null`. |

| Return ||
|---|---|
| ActivityInfo | This value cannot be `null`. |

### getActivityInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getActivityInfo(
    component: ComponentName, 
    flags: Int
): ActivityInfo
```

Retrieve all of the information we know about a particular activity class. Use getActivityInfo when long flags are needed.

| Parameters ||
|---|---|
| `component` | [ComponentName](../android.content/ComponentName.md): The full component name (i.e. com.google.apps.contacts/com.google.apps.contacts. ContactsList) of an Activity class. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| ActivityInfo | An ActivityInfo containing information about the activity. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if a package with the given name cannot be found on the system. |

### getActivityLogo

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getActivityLogo(activityName: ComponentName): Drawable?
```

Retrieve the logo associated with an activity. Given the full name of an activity, retrieves the information about it and calls loadLogo to return its logo. If the activity cannot be found, NameNotFoundException is thrown.

The returned drawable is subject to the same size capping limits as described in getApplicationIcon.

| Parameters ||
|---|---|
| `activityName` | [ComponentName](../android.content/ComponentName.md): Name of the activity whose logo is to be retrieved. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | Returns the image of the logo or null if the activity has no logo specified. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for the given activity could not be loaded. |

**See Also**

- getActivityLogo

### getActivityLogo

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getActivityLogo(intent: Intent): Drawable?
```

Retrieve the logo associated with an Intent. If intent.getClassName() is set, this simply returns the result of getActivityLogo(intent.getClassName()). Otherwise it resolves the intent's component and returns the logo associated with the resolved component. If intent.getClassName() cannot be found or the Intent cannot be resolved to a component, NameNotFoundException is thrown.

| Parameters ||
|---|---|
| `intent` | [Intent](../android.content/Intent.md): The intent for which you would like to retrieve a logo. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | Returns the image of the logo, or null if the activity has no logo specified. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for application matching the given intent could not be loaded. |

**See Also**

- getActivityLogo

### getAllPermissionGroups

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getAllPermissionGroups(flags: Int): MutableList<PermissionGroupInfo!>
```

Retrieve all of the known permission groups in the system.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_META_DATA:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PermissionGroupInfo!>` | Returns a list of PermissionGroupInfo containing information about all of the known permission groups. This value cannot be `null`. |

### getAppUidForPrivateComputeCoreUid

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAppUidForPrivateComputeCoreUid(pccUid: Int): Int
```

Maps a Private Compute Core (PCC) UID to its corresponding application UID.

| Parameters ||
|---|---|
| `pccUid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The PCC UID to map. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The corresponding application UID, or java.lang.Process#INVALID_UID if the provided UID is not a valid PCC UID or no mapping exists. |

### getApplicationBanner

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getApplicationBanner(info: ApplicationInfo): Drawable?
```

Retrieve the banner associated with an application.

| Parameters ||
|---|---|
| `info` | [ApplicationInfo](ApplicationInfo.md): Information about application being queried. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | Returns the image of the banner or null if the application has no banner specified. |

**See Also**

- getApplicationBanner

### getApplicationBanner

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getApplicationBanner(packageName: String): Drawable?
```

Retrieve the banner associated with an application. Given the name of the application's package, retrieves the information about it and calls getApplicationIcon() to return its banner. If the application cannot be found, NameNotFoundException is thrown.

The returned drawable is subject to the same size capping limits as described in getApplicationIcon.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Name of the package whose application banner is to be retrieved. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | Returns the image of the banner or null if the application has no banner specified. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for the given application could not be loaded. |

**See Also**

- getApplicationBanner

### getApplicationEnabledSetting

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getApplicationEnabledSetting(packageName: String): Int
```

Return the enabled setting for an application. This returns the last value set by setApplicationEnabledSetting; in most cases this value will be `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DEFAULT:kotlin.Int` since the value originally specified in the manifest has not been modified.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The package name of the application to retrieve. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns the current enabled state for the application. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DISABLED_USER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DISABLED_UNTIL_USED:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the named package does not exist. |

### getApplicationIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getApplicationIcon(info: ApplicationInfo): Drawable
```

Retrieve the icon associated with an application. If it has not defined an icon, the default app icon is returned. Does not return null.

Note: The returned drawable's dimensions are capped to a maximum size of `2048 x 2048` pixels. If the resource's intrinsic dimensions exceed this limit, it will be downsampled automatically, preserving its aspect ratio.

| Parameters ||
|---|---|
| `info` | [ApplicationInfo](ApplicationInfo.md): Information about application being queried. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` | Returns the image of the icon, or the default application icon if it could not be found. |

**See Also**

- getApplicationIcon

### getApplicationIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getApplicationIcon(packageName: String): Drawable
```

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

**See Also**

- getApplicationIcon

### getApplicationInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApplicationInfo(
    packageName: String, 
    flags: PackageManager.ApplicationInfoFlags
): ApplicationInfo
```

See getApplicationInfo.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `flags` | [PackageManager.ApplicationInfoFlags](../android/content/pm/PackageManager.ApplicationInfoFlags.md): This value cannot be `null`. |

| Return ||
|---|---|
| ApplicationInfo | This value cannot be `null`. |

### getApplicationInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getApplicationInfo(
    packageName: String, 
    flags: Int
): ApplicationInfo
```

Retrieve all of the information we know about a particular package/application. Use getApplicationInfo when long flags are needed.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The full name (i.e. com.google.apps.contacts) of an application. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| ApplicationInfo | An ApplicationInfo containing information about the package. If flag `MATCH_UNINSTALLED_PACKAGES` is set and if the package is not found in the list of installed applications, the application information is retrieved from the list of uninstalled applications (which includes installed applications as well as applications with data directory i.e. applications which had been deleted with `DELETE_KEEP_DATA` flag set). This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if a package with the given name cannot be found on the system. |

### getApplicationLabel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getApplicationLabel(info: ApplicationInfo): CharSequence
```

Return the label to use for this application.

| Parameters ||
|---|---|
| `info` | [ApplicationInfo](ApplicationInfo.md): The ApplicationInfo of the application to get the label of. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` | Returns a `https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#` containing the label associated with this application, or its name the item does not have a label. This value cannot be `null`. |

### getApplicationLogo

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getApplicationLogo(info: ApplicationInfo): Drawable?
```

Retrieve the logo associated with an application. If it has not specified a logo, this method returns null.

| Parameters ||
|---|---|
| `info` | [ApplicationInfo](ApplicationInfo.md): Information about application being queried. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | Returns the image of the logo, or null if no logo is specified by the application. |

**See Also**

- getApplicationLogo

### getApplicationLogo

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getApplicationLogo(packageName: String): Drawable?
```

Retrieve the logo associated with an application. Given the name of the application's package, retrieves the information about it and calls getApplicationLogo() to return its logo. If the application cannot be found, NameNotFoundException is thrown.

The returned drawable is subject to the same size capping limits as described in getApplicationIcon.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Name of the package whose application logo is to be retrieved. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | Returns the image of the logo, or null if no application logo has been specified. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for the given application could not be loaded. |

**See Also**

- getApplicationLogo

### getArchivedPackage

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getArchivedPackage(packageName: String): ArchivedPackageInfo?
```

Return archived package info for the package or null if the package is not installed.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

**See Also**

- installPackageArchived

### getBackgroundPermissionOptionLabel

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBackgroundPermissionOptionLabel(): CharSequence
```

Gets the localized label that corresponds to the option in settings for granting background access.

The intended use is for apps to reference this label in its instruction for users to grant a background permission.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` | the localized label that corresponds to the settings option for granting background access. This value cannot be `null`. |

### getChangedPackages

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getChangedPackages(sequenceNumber: Int): ChangedPackages?
```

Returns the names of the packages that have been changed \[eg. added, removed or updated\] since the given sequence number.

If no packages have been changed, returns `null`.

The sequence number starts at `0` and is reset every boot.

| Parameters ||
|---|---|
| `sequenceNumber` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The first sequence number for which to retrieve package changes. Value is 0 or greater |

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/Settings.Global.html#BOOT_COUNT:kotlin.String`

### getComponentEnabledSetting

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getComponentEnabledSetting(componentName: ComponentName): Int
```

Return the enabled setting for a package component (activity, receiver, service, provider). This returns the last value set by setComponentEnabledSetting; in most cases this value will be `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DEFAULT:kotlin.Int` since the value originally specified in the manifest has not been modified.

| Parameters ||
|---|---|
| `componentName` | [ComponentName](../android.content/ComponentName.md): The component to retrieve. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns the current enabled state for the component. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DISABLED_USER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DISABLED_UNTIL_USED:kotlin.Int` |

### getDefaultActivityIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getDefaultActivityIcon(): Drawable
```

Return the generic icon for an activity that is used when no specific icon is defined.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` | Drawable Image of the icon. This value cannot be `null`. |

### getDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getDrawable(
    packageName: String, 
    resid: Int, 
    appInfo: ApplicationInfo?
): Drawable?
```

Retrieve an image from a package. This is a low-level API used by the various package manager info structures (such as ComponentInfo to implement retrieval of their associated icon.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the package that this icon is coming from. Cannot be null. |
| `resid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource identifier of the desired image. Cannot be 0. |
| `appInfo` | [ApplicationInfo](ApplicationInfo.md)?: Overall information about packageName. This may be null, in which case the application information will be retrieved for you if needed; if you already have this information around, it can be much more efficient to supply it here. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | Returns a Drawable holding the requested image. Returns null if an image could not be found for any reason. |

### getEnableAppLockIntentForPackage

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEnableAppLockIntentForPackage(
    packageName: String, 
    enabled: Boolean
): PendingIntent?
```

Returns a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` to launch an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` that allows the caller to set App Lock for the specified package. Returns null if the App Lock state of the package cannot be set, either because App Lock is not supported for that package, or because it is already set to that value.

App Lock is a feature that allows users to add authentication as a requirement to open individual apps, even if the device is unlocked. When App Lock is enabled for an app, the system performs the following protections:

- Requires authentication using device credentials (e.g. PIN, pattern, or password) or Class 3 biometrics, whenever the user attempts to open the app (including after reinstallation), or share information to it via the Sharesheet.
- Redacts sensitive content of notifications sent by the app.
- Removes the app's widgets and shortcuts from the home screen.
- Displays a locked view of the app in Recents to prevent content leakage.
- Hides the app's Direct Share targets from the Sharesheet.

Once authenticated, an App Lock enabled app remains unlocked while it is visible in the foreground. The app will remain unlocked for a short grace period after the user navigates away, after which the system will re-lock it. Additionally, all App Lock enabled apps are immediately locked whenever the device is locked.

Before calling this API to avoid getting a null `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` callers should first verify that App Lock is supported for the specified package by first checking `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#isAppLockSupported:kotlin.Boolean`, or if it's already at the target state for that package by checking `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#isAppLockEnabled:kotlin.Boolean`. The `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` resolves to an activity, which allows the user to enroll a device credential if one isn't enrolled, and then requires authentication before setting the App Lock enablement state as enabled or disabled. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#LOCK_APPS:kotlin.String`

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the package to enable or disable App Lock. This value cannot be `null`. |
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true when the user would like to enable App Lock for the given package, false otherwise |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#?` | a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` to launch an activity to set App Lock for the passed in package. If the package does not support App Lock or the package's App Lock state is already in the passed in state, return null. |

### getGroupOfPlatformPermission

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGroupOfPlatformPermission(
    permissionName: String, 
    executor: Executor, 
    callback: Consumer<String!>
): Unit
```

Get the platform-defined permission group of a particular permission, if the permission is a platform-defined permission.

| Parameters ||
|---|---|
| `permissionName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the permission whose group is desired. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): the `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: the callback which will receive the name of the permission group this permission belongs to, or `null` if it has no group, is not a platform-defined permission, or there was an exception |
| --- | --- |

### getInstallSourceInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInstallSourceInfo(packageName: String): InstallSourceInfo
```

Retrieves information about how a package was installed or updated.

If the calling application does not hold the INSTALL_PACKAGES permission then the result will always return `null` from getOriginatingPackageName.

If the package that requested the install has been uninstalled, then information about it will only be returned from getInitiatingPackageName and getInitiatingPackageSigningInfo if the calling package is requesting its own install information and is not an instant app.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the package to query. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if the given package name is not available to the caller. |

### getInstalledApplications

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInstalledApplications(flags: PackageManager.ApplicationInfoFlags): MutableList<ApplicationInfo!>
```

See getInstalledApplications

| Parameters ||
|---|---|
| `flags` | [PackageManager.ApplicationInfoFlags](../android/content/pm/PackageManager.ApplicationInfoFlags.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo!>` | This value cannot be `null`. |

### getInstalledApplications

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getInstalledApplications(flags: Int): MutableList<ApplicationInfo!>
```

Return a List of all application packages that are installed for the current user. If flag GET_UNINSTALLED_PACKAGES has been set, a list of all applications including those deleted with `DELETE_KEEP_DATA` (partially installed apps with data directory) will be returned. Use getInstalledApplications when long flags are needed.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo!>` | A List of ApplicationInfo objects, one for each installed application. In the unlikely case there are no installed packages, an empty list is returned. If flag `MATCH_UNINSTALLED_PACKAGES` is set, the application information is retrieved from the list of uninstalled applications (which includes installed applications as well as applications with data directory i.e. applications which had been deleted with `DELETE_KEEP_DATA` flag set). This value cannot be `null`. |

### getInstalledModules

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInstalledModules(flags: Int): MutableList<ModuleInfo!>
```

Return a List of all modules that are installed.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_ALL:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ModuleInfo!>` | A `https://developer.android.com/reference/kotlin/java/util/List.html#` of ModuleInfo objects, one for each installed module, containing information about the module. In the unlikely case there are no installed modules, an empty list is returned. This value cannot be `null`. |

### getInstalledPackages

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInstalledPackages(flags: PackageManager.PackageInfoFlags): MutableList<PackageInfo!>
```

See getInstalledPackages.

| Parameters ||
|---|---|
| `flags` | [PackageManager.PackageInfoFlags](../android/content/pm/PackageManager.PackageInfoFlags.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo!>` | This value cannot be `null`. |

### getInstalledPackages

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getInstalledPackages(flags: Int): MutableList<PackageInfo!>
```

Return a List of all packages that are installed for the current user. Use getInstalledPackages when long flags are needed.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo!>` | A List of PackageInfo objects, one for each installed package, containing information about the package. In the unlikely case there are no installed packages, an empty list is returned. If flag `MATCH_UNINSTALLED_PACKAGES` is set, the package information is retrieved from the list of uninstalled applications (which includes installed applications as well as applications with data directory i.e. applications which had been deleted with `DELETE_KEEP_DATA` flag set). This value cannot be `null`. |

### getInstallerPackageName

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getInstallerPackageName(packageName: String): String?
```

**Deprecated:** *use getInstallSourceInfo instead*

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

```
abstract fun getInstantAppCookie(): ByteArray
```

Gets the instant application cookie for this app. Non instant apps and apps that were instant but were upgraded to normal apps can still access this API. For instant apps this cookie is cached for some time after uninstall while for normal apps the cookie is deleted after the app is uninstalled. The cookie is always present while the app is installed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | The cookie. This value cannot be `null`. |

**See Also**

- isInstantApp
- isInstantApp
- updateInstantAppCookie
- getInstantAppCookieMaxBytes
- clearInstantAppCookie

### getInstantAppCookieMaxBytes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getInstantAppCookieMaxBytes(): Int
```

Gets the maximum size in bytes of the cookie data an instant app can store on the device.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The max cookie size in bytes. |

**See Also**

- isInstantApp
- isInstantApp
- updateInstantAppCookie
- getInstantAppCookie
- clearInstantAppCookie

### getInstrumentationInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getInstrumentationInfo(
    className: ComponentName, 
    flags: Int
): InstrumentationInfo
```

Retrieve all of the information we know about a particular instrumentation class.

| Parameters ||
|---|---|
| `className` | [ComponentName](../android.content/ComponentName.md): The full name (i.e. com.google.apps.contacts.InstrumentList) of an Instrumentation class. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_META_DATA:kotlin.Int` |

| Return ||
|---|---|
| InstrumentationInfo | An InstrumentationInfo object containing information about the instrumentation. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if a package with the given name cannot be found on the system. |

### getLaunchIntentForPackage

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getLaunchIntentForPackage(packageName: String): Intent?
```

Returns a "good" intent to launch a front-door activity in a package. This is used, for example, to implement an "open" button when browsing through packages. The current implementation looks first for a main activity in the category `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_INFO:kotlin.String`, and next for a main activity in the category `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_LAUNCHER:kotlin.String`. Returns `null` if neither are found.

Consider using getLaunchIntentSenderForPackage if the caller is not allowed to query for the `packageName`.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the package to inspect. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Intent.html#?` | A fully-qualified `https://developer.android.com/reference/kotlin/android/content/Intent.html#` that can be used to launch the main activity in the package. Returns `null` if the package does not contain such an activity, or if *packageName* is not recognized. |

**See Also**

- getLaunchIntentSenderForPackage

### getLaunchIntentSenderForPackage

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLaunchIntentSenderForPackage(packageName: String): IntentSender
```

Returns an `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` that can be used to launch a front-door activity in a package. This is used, for example, to implement an "open" button when browsing through packages. The current implementation is the same with getLaunchIntentForPackage. Instead of returning the `https://developer.android.com/reference/kotlin/android/content/Intent.html#`, it returns the `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` which is not restricted by the package visibility.

The caller can invoke sendIntent to launch the activity. An `https://developer.android.com/reference/kotlin/android/content/IntentSender.SendIntentException.html#` is thrown if the package does not contain such an activity, or if *packageName* is not recognized.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the package to inspect. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` | Returns a `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` to launch the activity. This value cannot be `null`. |

**See Also**

- getLaunchIntentForPackage

### getLeanbackLaunchIntentForPackage

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getLeanbackLaunchIntentForPackage(packageName: String): Intent?
```

Return a "good" intent to launch a front-door Leanback activity in a package, for use for example to implement an "open" button when browsing through packages. The current implementation will look for a main activity in the category `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_LEANBACK_LAUNCHER:kotlin.String`, or return null if no main leanback activities are found.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the package to inspect. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Intent.html#?` | Returns either a fully-qualified Intent that can be used to launch the main Leanback activity in the package, or null if the package does not contain such an activity. |

### getMemoryBudgets

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMemoryBudgets(info: ApplicationInfo): MutableList<MemoryBudgetInfo!>
```

Return the memory budgets for the application described by the given ApplicationInfo.

| Parameters ||
|---|---|
| `info` | [ApplicationInfo](ApplicationInfo.md): The ApplicationInfo of the application to query. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo!>` | This value cannot be `null`. |

### getMimeGroup

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMimeGroup(mimeGroup: String): MutableSet<String!>
```

Gets all MIME types contained by MIME group. Libraries should use a reverse-DNS prefix followed by a ':' character and library-specific group name to avoid namespace collisions, e.g. "com.example:myFeature".

| Parameters ||
|---|---|
| `mimeGroup` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): MIME group to retrieve. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | MIME types contained by the MIME group. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the MIME group was not declared in the manifest. |

### getModuleInfo

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getModuleInfo(
    packageName: String, 
    flags: Int
): ModuleInfo
```

Retrieve information for a particular module.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the module. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. Value is either `0` or |

| Return ||
|---|---|
| ModuleInfo | A ModuleInfo object containing information about the module. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if a module with the given name cannot be found on the system. |

### getNameForUid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getNameForUid(uid: Int): String?
```

Retrieve the official name associated with a uid. This name is guaranteed to never change, though it is possible for the underlying uid to be changed. That is, if you are storing information about uids in persistent storage, you should use the string returned by this function instead of the raw uid.

| Parameters ||
|---|---|
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The uid for which you would like to retrieve a name. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | Returns a unique name for the given uid, or null if the uid is not currently assigned. |

### getPackageArchiveInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackageArchiveInfo(
    archiveFilePath: String, 
    flags: PackageManager.PackageInfoFlags
): PackageInfo?
```

See getPackageArchiveInfo.

| Parameters ||
|---|---|
| `archiveFilePath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `flags` | [PackageManager.PackageInfoFlags](../android/content/pm/PackageManager.PackageInfoFlags.md): This value cannot be `null`. |

| Return ||
|---|---|
| PackageInfo | This value may be `null`. |

### getPackageArchiveInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackageArchiveInfo(
    archiveFilePath: String, 
    flags: Int
): PackageInfo?
```

Retrieve overall information about an application package defined in a package archive file Use getPackageArchiveInfo when long flags are needed.

| Parameters ||
|---|---|
| `archiveFilePath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The path to the archive file. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| PackageInfo | A PackageInfo object containing information about the package archive. If the package could not be parsed, returns null. |

### getPackageGids

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getPackageGids(packageName: String): IntArray!
```

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

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackageGids(
    packageName: String, 
    flags: PackageManager.PackageInfoFlags
): IntArray?
```

See getPackageGids.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `flags` | [PackageManager.PackageInfoFlags](../android/content/pm/PackageManager.PackageInfoFlags.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html?` | This value may be `null`. |

### getPackageGids

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getPackageGids(
    packageName: String, 
    flags: Int
): IntArray!
```

Return an array of all of the POSIX secondary group IDs that have been assigned to the given package.

Note that the same package may have different GIDs under different `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` on the same device. Use getPackageGids when long flags are needed.

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

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackageInfo(
    versionedPackage: VersionedPackage, 
    flags: PackageManager.PackageInfoFlags
): PackageInfo
```

See getPackageInfo

| Parameters ||
|---|---|
| `versionedPackage` | [VersionedPackage](VersionedPackage.md): This value cannot be `null`. |
| `flags` | [PackageManager.PackageInfoFlags](../android/content/pm/PackageManager.PackageInfoFlags.md): This value cannot be `null`. |

| Return ||
|---|---|
| PackageInfo | This value cannot be `null`. |

### getPackageInfo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getPackageInfo(
    versionedPackage: VersionedPackage, 
    flags: Int
): PackageInfo!
```

Retrieve overall information about an application package that is installed on the system. This method can be used for retrieving information about packages for which multiple versions can be installed at the time. Currently only packages hosting static shared libraries can have multiple installed versions. The method can also be used to get info for a package that has a single version installed by passing `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#VERSION_CODE_HIGHEST:kotlin.Int` in the VersionedPackage constructor. Use getPackageInfo when long flags are needed.

| Parameters ||
|---|---|
| `versionedPackage` | [VersionedPackage](VersionedPackage.md): The versioned package for which to query. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo!` | A PackageInfo object containing information about the package. If flag `MATCH_UNINSTALLED_PACKAGES` is set and if the package is not found in the list of installed applications, the package information is retrieved from the list of uninstalled applications (which includes installed applications as well as applications with data directory i.e. applications which had been deleted with `DELETE_KEEP_DATA` flag set). |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if no such package is available to the caller. |

### getPackageInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackageInfo(
    packageName: String, 
    flags: PackageManager.PackageInfoFlags
): PackageInfo
```

See getPackageInfo

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `flags` | [PackageManager.PackageInfoFlags](../android/content/pm/PackageManager.PackageInfoFlags.md): This value cannot be `null`. |

| Return ||
|---|---|
| PackageInfo | This value cannot be `null`. |

### getPackageInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getPackageInfo(
    packageName: String, 
    flags: Int
): PackageInfo!
```

Retrieve overall information about an application package that is installed on the system. Use getPackageInfo when long flags are needed.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The full name (i.e. com.google.apps.contacts) of the desired package. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo!` | A PackageInfo object containing information about the package. If flag `MATCH_UNINSTALLED_PACKAGES` is set and if the package is not found in the list of installed applications, the package information is retrieved from the list of uninstalled applications (which includes installed applications as well as applications with data directory i.e. applications which had been deleted with `DELETE_KEEP_DATA` flag set). |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if no such package is available to the caller. |

### getPackageInstaller

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getPackageInstaller(): PackageInstaller
```

Return interface that offers the ability to install, upgrade, and remove applications on the device.

| Return ||
|---|---|
| PackageInstaller | This value cannot be `null`. |

### getPackageUid

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackageUid(
    packageName: String, 
    flags: PackageManager.PackageInfoFlags
): Int
```

See getPackageUid.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `flags` | [PackageManager.PackageInfoFlags](../android/content/pm/PackageManager.PackageInfoFlags.md): This value cannot be `null`. |

### getPackageUid

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getPackageUid(
    packageName: String, 
    flags: Int
): Int
```

Return the UID associated with the given package name.

Note that the same package will have different UIDs under different `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` on the same device. Use getPackageUid when long flags are needed.

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
abstract fun getPackagesForUid(uid: Int): Array<String!>?
```

Retrieve the names of all packages that are associated with a particular user id. In most cases, this will be a single package name, the package that has been assigned that user id. Where there are multiple packages sharing the same user id through the "sharedUserId" mechanism, all packages with that id will be returned.

| Parameters ||
|---|---|
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The user id for which you would like to retrieve the associated packages. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | Returns an array of one or more packages assigned to the user id, or null if there are no known packages with the given id. |

### getPackagesHoldingPermissions

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackagesHoldingPermissions(
    permissions: Array<String!>, 
    flags: PackageManager.PackageInfoFlags
): MutableList<PackageInfo!>
```

See getPackagesHoldingPermissions.

| Parameters ||
|---|---|
| `permissions` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: This value cannot be `null`. |
| `flags` | [PackageManager.PackageInfoFlags](../android/content/pm/PackageManager.PackageInfoFlags.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo!>` | This value cannot be `null`. |

### getPackagesHoldingPermissions

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getPackagesHoldingPermissions(
    permissions: Array<String!>, 
    flags: Int
): MutableList<PackageInfo!>
```

Return a List of all installed packages that are currently holding any of the given permissions. Use getPackagesHoldingPermissions when long flags are needed.

| Parameters ||
|---|---|
| `permissions` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo!>` | A List of PackageInfo objects, one for each installed package that holds any of the permissions that were provided, containing information about the package. If no installed packages hold any of the permissions, an empty list is returned. If flag `MATCH_UNINSTALLED_PACKAGES` is set, the package information is retrieved from the list of uninstalled applications (which includes installed applications as well as applications with data directory i.e. applications which had been deleted with `DELETE_KEEP_DATA` flag set). This value cannot be `null`. |

### getPermissionGroupInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getPermissionGroupInfo(
    groupName: String, 
    flags: Int
): PermissionGroupInfo
```

Retrieve all of the information we know about a particular group of permissions.

| Parameters ||
|---|---|
| `groupName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The fully qualified name (i.e. com.google.permission_group.APPS) of the permission you are interested in. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_META_DATA:kotlin.Int` |

| Return ||
|---|---|
| PermissionGroupInfo | Returns a PermissionGroupInfo containing information about the permission. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if a package with the given name cannot be found on the system. |

### getPermissionInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getPermissionInfo(
    permName: String, 
    flags: Int
): PermissionInfo!
```

Retrieve all of the information we know about a particular permission.

| Parameters ||
|---|---|
| `permName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The fully qualified name (i.e. com.google.permission.LOGIN) of the permission you are interested in. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_META_DATA:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo!` | Returns a PermissionInfo containing information about the permission. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if a package with the given name cannot be found on the system. |

### getPlatformPermissionsForGroup

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPlatformPermissionsForGroup(
    permissionGroupName: String, 
    executor: Executor, 
    callback: Consumer<MutableList<String!>!>
): Unit
```

Get the platform-defined permissions which belong to a particular permission group.

| Parameters ||
|---|---|
| `permissionGroupName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the permission group whose permissions are desired. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): the `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [Consumer](../java.util.function/Consumer.md)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>: the callback which will receive a list of the platform-defined permissions in the group, or empty if the group is not a valid platform-defined permission group, or there was an exception. This value cannot be `null`. |
| --- | --- |

### getPreferredActivities

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getPreferredActivities(
    outFilters: MutableList<IntentFilter!>, 
    outActivities: MutableList<ComponentName!>, 
    packageName: String?
): Int
```

**Deprecated:** *This function no longer does anything. It is the platform's responsibility to assign preferred activities and this cannot be modified directly. To determine the activities resolved by the platform, use #resolveActivity or #queryIntentActivities. To configure an app to be responsible for a particular role and to check current role holders, see `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#`.*

Retrieve all preferred activities, previously added with addPreferredActivity, that are currently registered with the system.

| Parameters ||
|---|---|
| `outFilters` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [IntentFilter](../android.content/IntentFilter.md)!\>: A required list in which to place the filters of all of the preferred activities. This value cannot be `null`. |
| `outActivities` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ComponentName](../android.content/ComponentName.md)!\>: A required list in which to place the component names of all of the preferred activities. This value cannot be `null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: An optional package in which you would like to limit the list. If null, all activities will be returned; if non-null, only those activities in the given package are returned. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns the total number of registered preferred activities (the number of distinct IntentFilter records, not the number of unique activity components) that were found. |

### getPreferredPackages

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getPreferredPackages(flags: Int): MutableList<PackageInfo!>
```

**Deprecated:** *This function no longer does anything. It is the platform's responsibility to assign preferred activities and this cannot be modified directly. To determine the activities resolved by the platform, use #resolveActivity or #queryIntentActivities. To configure an app to be responsible for a particular role and to check current role holders, see `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#`.*

Retrieve the list of all currently configured preferred packages. The first package on the list is the most preferred, the last is the least preferred.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PackageInfo!>` | A List of PackageInfo objects, one for each preferred application, in order of preference. This value cannot be `null`. |

### getProperty

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getProperty(
    propertyName: String, 
    component: ComponentName
): PackageManager.Property
```

Returns the property defined in the given component declaration.

| Parameters ||
|---|---|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `component` | [ComponentName](../android.content/ComponentName.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if either the given component does not exist or if the given property is not defined within the component declaration. |

### getProperty

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getProperty(
    propertyName: String, 
    packageName: String
): PackageManager.Property
```

Returns the property defined in the given package's \<application\> tag.

| Parameters ||
|---|---|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if either the given package is not installed or if the given property is not defined within the \<application\> tag. |

### getProviderInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getProviderInfo(
    component: ComponentName, 
    flags: PackageManager.ComponentInfoFlags
): ProviderInfo
```

See getProviderInfo.

| Parameters ||
|---|---|
| `component` | [ComponentName](../android.content/ComponentName.md): This value cannot be `null`. |
| `flags` | [PackageManager.ComponentInfoFlags](../android/content/pm/PackageManager.ComponentInfoFlags.md): This value cannot be `null`. |

| Return ||
|---|---|
| ProviderInfo | This value cannot be `null`. |

### getProviderInfo

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getProviderInfo(
    component: ComponentName, 
    flags: Int
): ProviderInfo
```

Retrieve all of the information we know about a particular content provider class. Use getProviderInfo when long flags are needed.

| Parameters ||
|---|---|
| `component` | [ComponentName](../android.content/ComponentName.md): The full component name (i.e. com.google.providers.media/com.google.providers.media. MediaProvider) of a ContentProvider class. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| ProviderInfo | A ProviderInfo object containing information about the provider. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if a package with the given name cannot be found on the system. |

### getReceiverInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getReceiverInfo(
    component: ComponentName, 
    flags: PackageManager.ComponentInfoFlags
): ActivityInfo
```

See getReceiverInfo.

| Parameters ||
|---|---|
| `component` | [ComponentName](../android.content/ComponentName.md): This value cannot be `null`. |
| `flags` | [PackageManager.ComponentInfoFlags](../android/content/pm/PackageManager.ComponentInfoFlags.md): This value cannot be `null`. |

| Return ||
|---|---|
| ActivityInfo | This value cannot be `null`. |

### getReceiverInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getReceiverInfo(
    component: ComponentName, 
    flags: Int
): ActivityInfo
```

Retrieve all of the information we know about a particular receiver class. Use getReceiverInfo when long flags are needed.

| Parameters ||
|---|---|
| `component` | [ComponentName](../android.content/ComponentName.md): The full component name (i.e. com.google.apps.calendar/com.google.apps.calendar. CalendarAlarm) of a Receiver class. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| ActivityInfo | An ActivityInfo containing information about the receiver. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if a package with the given name cannot be found on the system. |

### getResourcesForActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getResourcesForActivity(activityName: ComponentName): Resources
```

Retrieve the resources associated with an activity. Given the full name of an activity, retrieves the information about it and calls getResources() to return its application's resources. If the activity cannot be found, NameNotFoundException is thrown.

| Parameters ||
|---|---|
| `activityName` | [ComponentName](../android.content/ComponentName.md): Name of the activity whose resources are to be retrieved. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#` | Returns the application's Resources. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for the given application could not be loaded. |

**See Also**

- getResourcesForApplication

### getResourcesForApplication

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getResourcesForApplication(app: ApplicationInfo): Resources
```

Retrieve the resources for an application. Throws NameNotFoundException if the package is no longer installed.

| Parameters ||
|---|---|
| `app` | [ApplicationInfo](ApplicationInfo.md): Information about the desired application. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#` | Returns the application's Resources. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for the given application could not be loaded (most likely because it was uninstalled). |

### getResourcesForApplication

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getResourcesForApplication(
    app: ApplicationInfo, 
    configuration: Configuration?
): Resources
```

Retrieve the resources for an application for the provided configuration.

| Parameters ||
|---|---|
| `app` | [ApplicationInfo](ApplicationInfo.md): Information about the desired application. This value cannot be `null`. |
| `configuration` | [Configuration](../android.content.res/Configuration.md)?: Overridden configuration when loading the Resources. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#` | Returns the application's Resources. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for the given application could not be loaded (most likely because it was uninstalled). |

### getResourcesForApplication

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getResourcesForApplication(packageName: String): Resources
```

Retrieve the resources associated with an application. Given the full package name of an application, retrieves the information about it and calls getResources() to return its application's resources. If the appPackageName cannot be found, NameNotFoundException is thrown.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Package name of the application whose resources are to be retrieved. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#` | Returns the application's Resources. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | Thrown if the resources for the given application could not be loaded. |

**See Also**

- getResourcesForApplication

### getServiceInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getServiceInfo(
    component: ComponentName, 
    flags: PackageManager.ComponentInfoFlags
): ServiceInfo
```

See getServiceInfo.

| Parameters ||
|---|---|
| `component` | [ComponentName](../android.content/ComponentName.md): This value cannot be `null`. |
| `flags` | [PackageManager.ComponentInfoFlags](../android/content/pm/PackageManager.ComponentInfoFlags.md): This value cannot be `null`. |

| Return ||
|---|---|
| ServiceInfo | This value cannot be `null`. |

### getServiceInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getServiceInfo(
    component: ComponentName, 
    flags: Int
): ServiceInfo
```

Retrieve all of the information we know about a particular service class. Use getServiceInfo when long flags are needed.

| Parameters ||
|---|---|
| `component` | [ComponentName](../android.content/ComponentName.md): The full component name (i.e. com.google.apps.media/com.google.apps.media. BackgroundPlayback) of a Service class. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| ServiceInfo | A ServiceInfo object containing information about the service. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if the component cannot be found on the system. |

### getSharedLibraries

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSharedLibraries(flags: PackageManager.PackageInfoFlags): MutableList<SharedLibraryInfo!>
```

See getSharedLibraries.

| Parameters ||
|---|---|
| `flags` | [PackageManager.PackageInfoFlags](../android/content/pm/PackageManager.PackageInfoFlags.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo!>` | This value cannot be `null`. |

### getSharedLibraries

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSharedLibraries(flags: Int): MutableList<SharedLibraryInfo!>
```

Get a list of shared libraries on the device. Use getSharedLibraries when long flags are needed.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): To filter the libraries to return. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo!>` | The shared library list. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_UNINSTALLED_PACKAGES:kotlin.Int`

### getSuspendedPackageAppExtras

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSuspendedPackageAppExtras(): Bundle?
```

Returns a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` of extras that was meant to be sent to the calling app when it was suspended. An app with the permission `android.permission.SUSPEND_APPS` can supply this to the system at the time of suspending an app.

This is the same `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` that is sent along with the broadcast `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MY_PACKAGE_SUSPENDED:kotlin.String`, whenever the app is suspended. The contents of this `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` are a contract between the suspended app and the suspending app.

Note: These extras are optional, so if no extras were supplied to the system, this method will return `null`, even when the calling app has been suspended.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#?` | A `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` containing the extras for the app, or `null` if the package is not currently suspended. |

**See Also**

- isPackageSuspended
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MY_PACKAGE_UNSUSPENDED:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MY_PACKAGE_SUSPENDED:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_SUSPENDED_PACKAGE_EXTRAS:kotlin.String`

### getSyntheticAppDetailsActivityEnabled

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSyntheticAppDetailsActivityEnabled(packageName: String): Boolean
```

Return whether a synthetic app details activity will be generated if the app has no enabled launcher activity.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The package name of the app. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns the enabled state for the synthetic app details activity. |

### getSystemAvailableFeatures

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSystemAvailableFeatures(): Array<FeatureInfo!>
```

Get a list of features that are available on the system.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo!>` | An array of FeatureInfo classes describing the features that are available on the system, or null if there are none(!!). |

### getSystemSharedLibraryNames

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSystemSharedLibraryNames(): Array<String!>?
```

Get a list of shared libraries that are available on the system.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | An array of shared library names that are available on the system, or null if none are installed. |

### getTargetSdkVersion

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTargetSdkVersion(packageName: String): Int
```

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The target SDK version for the given package name. Value is 0 or greater |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if a package with the given name cannot be found on the system. |

### getText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getText(
    packageName: String, 
    resid: Int, 
    appInfo: ApplicationInfo?
): CharSequence?
```

Retrieve text from a package. This is a low-level API used by the various package manager info structures (such as ComponentInfo to implement retrieval of their associated labels and other text.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the package that this text is coming from. Cannot be null. |
| `resid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource identifier of the desired text. Cannot be 0. |
| `appInfo` | [ApplicationInfo](ApplicationInfo.md)?: Overall information about packageName. This may be null, in which case the application information will be retrieved for you if needed; if you already have this information around, it can be much more efficient to supply it here. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | Returns a CharSequence holding the requested text. Returns null if the text could not be found for any reason. |

### getUserBadgedDrawableForDensity

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getUserBadgedDrawableForDensity(
    drawable: Drawable, 
    user: UserHandle, 
    badgeLocation: Rect?, 
    badgeDensity: Int
): Drawable
```

If the target user is a managed profile of the calling user or the caller is itself a managed profile, then this returns a badged copy of the given drawable allowing the user to distinguish it from the original drawable. The caller can specify the location in the bounds of the drawable to be badged where the badge should be applied as well as the density of the badge to be used.

If the original drawable is a BitmapDrawable and the backing bitmap is mutable as per isMutable, the badging is performed in place and the original drawable is returned.

| Parameters ||
|---|---|
| `drawable` | [Drawable](../android.graphics.drawable/Drawable.md): The drawable to badge. This value cannot be `null`. |
| `user` | [UserHandle](../android.os/UserHandle.md): The target user. This value cannot be `null`. |
| `badgeLocation` | [Rect](../android.graphics/Rect.md)?: Where in the bounds of the badged drawable to place the badge. If it's `null`, the badge is applied on top of the entire drawable being badged. |
| --- | --- |
| `badgeDensity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The optional desired density for the badge as per `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#densityDpi:kotlin.Int`. If it's not positive, the density of the display is used. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` | A drawable that combines the original drawable and a badge as determined by the system. This value cannot be `null`. |

### getUserBadgedIcon

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getUserBadgedIcon(
    drawable: Drawable, 
    user: UserHandle
): Drawable
```

If the target user is a managed profile, then this returns a badged copy of the given icon to be able to distinguish it from the original icon. For badging an arbitrary drawable use getUserBadgedDrawableForDensity.

If the original drawable is a BitmapDrawable and the backing bitmap is mutable as per isMutable, the badging is performed in place and the original drawable is returned.

| Parameters ||
|---|---|
| `drawable` | [Drawable](../android.graphics.drawable/Drawable.md): The drawable to badge. This value cannot be `null`. |
| `user` | [UserHandle](../android.os/UserHandle.md): The target user. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` | A drawable that combines the original icon and a badge as determined by the system. This value cannot be `null`. |

### getUserBadgedLabel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getUserBadgedLabel(
    label: CharSequence, 
    user: UserHandle
): CharSequence
```

If the target user is a managed profile of the calling user or the caller is itself a managed profile, then this returns a copy of the label with badging for accessibility services like talkback. E.g. passing in "Email" and it might return "Work Email" for Email in the work profile.

| Parameters ||
|---|---|
| `label` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): The label to change. This value cannot be `null`. |
| `user` | [UserHandle](../android.os/UserHandle.md): The target user. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` | A label that combines the original label and a badge as determined by the system. This value cannot be `null`. |

### getVerifiedSigningInfo

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getVerifiedSigningInfo(
    path: String, 
    minAppSigningSchemeVersion: Int
): SigningInfo
```

Verifies and returns the [app signing](https://source.android.com/docs/security/features/apksigning) information of the file at the given path. This operation takes a few milliseconds. Unlike getPackageArchiveInfo with `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_SIGNING_CERTIFICATES:kotlin.Int`, this method does not require the file to be a package archive file.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `minAppSigningSchemeVersion` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/SigningInfo#VERSION_JAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/SigningInfo#VERSION_SIGNING_BLOCK_V2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/SigningInfo#VERSION_SIGNING_BLOCK_V3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/SigningInfo#VERSION_SIGNING_BLOCK_V4:kotlin.Int` |

| Return ||
|---|---|
| SigningInfo | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.SigningInfoException` | if the verification fails |

### getWhitelistedRestrictedPermissions

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWhitelistedRestrictedPermissions(
    packageName: String, 
    whitelistFlag: Int
): MutableSet<String!>
```

Gets the restricted permissions that have been whitelisted and the app is allowed to have them granted in their full form.

Permissions can be hard restricted which means that the app cannot hold them or soft restricted where the app can hold the permission but in a weaker form. Whether a permission is `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#FLAG_HARD_RESTRICTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#FLAG_SOFT_RESTRICTED:kotlin.Int` depends on the permission declaration. Whitelisting a hard restricted permission allows for the to hold that permission and whitelisting a soft restricted permission allows the app to hold the permission in its full, unrestricted form.

<br />

There are four allowlists:
1. one for cases where the system permission policy whitelists a permission This list corresponds to the`https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_SYSTEM:kotlin.Int` flag. Can only be accessed by pre-installed holders of a dedicated permission.
2. one for cases where the system whitelists the permission when upgrading from an OS version in which the permission was not restricted to an OS version in which the permission is restricted. This list corresponds to the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_UPGRADE:kotlin.Int` flag. Can be accessed by pre-installed holders of a dedicated permission or the installer on record.
3. one for cases where the installer of the package whitelists a permission. This list corresponds to the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_INSTALLER:kotlin.Int` flag. Can be accessed by pre-installed holders of a dedicated permission or the installer on record.

**Note:**In retrospect it would have been preferred to use more inclusive terminology when naming this API. Similar APIs added will refrain from using the term "whitelist".

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The app for which to get whitelisted permissions. This value cannot be `null`. |
| `whitelistFlag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The flag to determine which whitelist to query. Only one flag can be passed.s. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_INSTALLER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_UPGRADE:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | The whitelisted permissions that are on any of the whitelists you query for. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if you try to access a whitelist that you have no access to. |

**See Also**

- addWhitelistedRestrictedPermission
- removeWhitelistedRestrictedPermission
- `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_SYSTEM:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_UPGRADE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_INSTALLER:kotlin.Int`

### getXml

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getXml(
    packageName: String, 
    resid: Int, 
    appInfo: ApplicationInfo?
): XmlResourceParser?
```

Retrieve an XML file from a package. This is a low-level API used to retrieve XML meta data.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the package that this xml is coming from. Cannot be null. |
| `resid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource identifier of the desired xml. Cannot be 0. |
| `appInfo` | [ApplicationInfo](ApplicationInfo.md)?: Overall information about packageName. This may be null, in which case the application information will be retrieved for you if needed; if you already have this information around, it can be much more efficient to supply it here. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser.html#?` | Returns an XmlPullParser allowing you to parse out the XML data. Returns null if the xml resource could not be found for any reason. |

### hasSigningCertificate

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasSigningCertificate(
    uid: Int, 
    certificate: ByteArray, 
    type: Int
): Boolean
```

Searches the set of signing certificates by which the package(s) for the given uid has proven to have been signed. For multiple packages sharing the same uid, this will return the signing certificates found in the signing history of the "newest" package, where "newest" indicates the package with the newest signing certificate in the shared uid group. This method should be used instead of `getPackageInfo` with `GET_SIGNATURES` since it takes into account the possibility of signing certificate rotation, except in the case of packages that are signed by multiple certificates, for which signing certificate rotation is not supported. This method is analogous to using `getPackagesForUid` followed by `getPackageInfo` with `GET_SIGNING_CERTIFICATES`, selecting the `PackageInfo` of the newest-signed bpackage , and finally searching through the resulting `signingInfo` field to see if the desired certificate is there.

| Parameters ||
|---|---|
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): uid whose signing certificates to check |
| `certificate` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): signing certificate for which to search. This value cannot be `null`. |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): representation of the `certificate` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#CERT_INPUT_RAW_X509:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#CERT_INPUT_SHA256:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this package was or is signed by exactly the certificate `certificate` |

### hasSigningCertificate

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasSigningCertificate(
    packageName: String, 
    certificate: ByteArray, 
    type: Int
): Boolean
```

Searches the set of signing certificates by which the given package has proven to have been signed. This should be used instead of `getPackageInfo` with `GET_SIGNATURES` since it takes into account the possibility of signing certificate rotation, except in the case of packages that are signed by multiple certificates, for which signing certificate rotation is not supported. This method is analogous to using `getPackageInfo` with `GET_SIGNING_CERTIFICATES` and then searching through the resulting `signingInfo` field to see if the desired certificate is present.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): package whose signing certificates to check. This value cannot be `null`. |
| `certificate` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): signing certificate for which to search. This value cannot be `null`. |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): representation of the `certificate` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#CERT_INPUT_RAW_X509:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#CERT_INPUT_SHA256:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this package was or is signed by exactly the certificate `certificate` |

### hasSystemFeature

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun hasSystemFeature(featureName: String): Boolean
```

Check whether the given feature name is one of the available features as returned by getSystemAvailableFeatures. This tests for the presence of *any* version of the given feature name; use hasSystemFeature to check for a minimum version.

| Parameters ||
|---|---|
| `featureName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the devices supports the feature, else false. |

### hasSystemFeature

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun hasSystemFeature(
    featureName: String, 
    version: Int
): Boolean
```

Check whether the given feature name and version is one of the available features as returned by getSystemAvailableFeatures. Since features are defined to always be backwards compatible, this returns true if the available feature version is greater than or equal to the requested version.

| Parameters ||
|---|---|
| `featureName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the devices supports the feature, else false. |

### isAppArchivable

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAppArchivable(packageName: String): Boolean
```

Returns true if an app is archivable.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if the given package name is not available to the caller. |

**See Also**

- requestArchive

### isAutoRevokeWhitelisted

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAutoRevokeWhitelisted(): Boolean
```

**Note:**In retrospect it would have been preferred to use more inclusive terminology when naming this API. Similar APIs added will refrain from using the term "whitelist".

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether this package is whitelisted from having its runtime permission be auto-revoked if unused for an extended period of time. |

### isAutoRevokeWhitelisted

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAutoRevokeWhitelisted(packageName: String): Boolean
```

Checks whether an application is exempt from having its permissions be automatically revoked when the app is unused for an extended period of time. Only the installer on record that installed the given package, or a holder of `WHITELIST_AUTO_REVOKE_PERMISSIONS` is allowed to call this.

**Note:**In retrospect it would have been preferred to use more inclusive terminology when naming this API. Similar APIs added will refrain from using the term "whitelist".

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The app for which to set exemption. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the app is whitelisted. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if you you have no access to this. |

**See Also**

- setAutoRevokeWhitelisted

### isDefaultApplicationIcon

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDefaultApplicationIcon(drawable: Drawable): Boolean
```

Returns if the provided drawable represents the default activity icon provided by the system. PackageManager silently returns a default application icon for any package/activity if the app itself does not define one or if the system encountered any error when loading the icon. Developers can use this to check implement app specific logic around retrying or caching.

| Parameters ||
|---|---|
| `drawable` | [Drawable](../android.graphics.drawable/Drawable.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the drawable represents the default activity icon, false otherwise |

**See Also**

- getDefaultActivityIcon
- getIcon

### isDeviceUpgrading

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDeviceUpgrading(): Boolean
```

Returns true if the device is upgrading, such as first boot after OTA.

### isInstantApp

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun isInstantApp(): Boolean
```

Gets whether this application is an instant app.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether caller is an instant app. |

**See Also**

- isInstantApp
- updateInstantAppCookie
- getInstantAppCookie
- getInstantAppCookieMaxBytes

### isInstantApp

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun isInstantApp(packageName: String): Boolean
```

Gets whether the given package is an instant app.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The package to check. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the given package is an instant app. |

**See Also**

- isInstantApp
- updateInstantAppCookie
- getInstantAppCookie
- getInstantAppCookieMaxBytes
- clearInstantAppCookie

### isPackageStopped

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isPackageStopped(packageName: String): Boolean
```

Query if an app is currently stopped.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the given package is stopped, `false` otherwise |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if the package could not be found. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#FLAG_STOPPED:kotlin.Int`

### isPackageSuspended

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isPackageSuspended(): Boolean
```

Apps can query this to know if they have been suspended. A system app with the permission `android.permission.SUSPEND_APPS` can put any app on the device into a suspended state.

While in this state, the application's notifications will be hidden, any of its started activities will be stopped and it will not be able to show toasts or dialogs or play audio. When the user tries to launch a suspended app, the system will, instead, show a dialog to the user informing them that they cannot use this app while it is suspended.

When an app is put into this state, the broadcast action `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MY_PACKAGE_SUSPENDED:kotlin.String` will be delivered to any of its broadcast receivers that included this action in their intent-filters, *including manifest receivers.* Similarly, a broadcast action `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MY_PACKAGE_UNSUSPENDED:kotlin.String` is delivered when a previously suspended app is taken out of this state. Apps are expected to use these to gracefully deal with transitions to and from this state.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the calling package has been suspended, `false` otherwise. |

**See Also**

- getSuspendedPackageAppExtras
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MY_PACKAGE_SUSPENDED:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MY_PACKAGE_UNSUSPENDED:kotlin.String`

### isPackageSuspended

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isPackageSuspended(packageName: String): Boolean
```

Query if an app is currently suspended.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the given package is suspended, `false` otherwise |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if the package could not be found. |

**See Also**

- isPackageSuspended

### isPermissionRevokedByPolicy

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun isPermissionRevokedByPolicy(
    permName: String, 
    packageName: String
): Boolean
```

Checks whether a particular permissions has been revoked for a package by policy. Typically the device owner or the profile owner may apply such a policy. The user cannot grant policy revoked permissions, hence the only way for an app to get such a permission is by a policy change.

| Parameters ||
|---|---|
| `permName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the permission you are checking for. This value cannot be `null`. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the package you are checking against. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the permission is restricted by policy. |

### isSafeMode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun isSafeMode(): Boolean
```

Return whether the device has been booted into safe mode.

### parseAndroidManifest

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <T : Any!> parseAndroidManifest(
    apkFileDescriptor: ParcelFileDescriptor, 
    parserFunction: Function<XmlResourceParser!, T>
): T
```

Similar to parseAndroidManifest, but accepting a file descriptor instead of a File object. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `apkFileDescriptor` | [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md): The file descriptor of an application apk. The parserFunction will be invoked with the XmlResourceParser object after getting the AndroidManifest.xml of an application package. This value cannot be `null`. |
| `parserFunction` | [Function](../java.util.function/Function.md)\< [XmlResourceParser](../android.content.res/XmlResourceParser.md)!, T\>: This value cannot be `null`. |

| Return ||
|---|---|
| `T` | Returns the result of the apply. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if the AndroidManifest.xml of an application package cannot be read or accessed. |

### parseAndroidManifest

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <T : Any!> parseAndroidManifest(
    apkFile: File, 
    parserFunction: Function<XmlResourceParser!, T>
): T
```

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

| Parameters ||
|---|---|
| `apkFile` | [File](../java.io/File.md): The file of an application apk. This value cannot be `null`. |
| `parserFunction` | [Function](../java.util.function/Function.md)\< [XmlResourceParser](../android.content.res/XmlResourceParser.md)!, T\>: The parserFunction will be invoked with the XmlResourceParser object after getting the AndroidManifest.xml of an application package. This value cannot be `null`. |

| Return ||
|---|---|
| `T` | Returns the result of the apply. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if the AndroidManifest.xml of an application package cannot be read or accessed. |

### queryActivityProperty

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryActivityProperty(propertyName: String): MutableList<PackageManager.Property!>
```

Returns the property definition for all \<activity\> and \<activity-alias\> tags.

If the property is not defined with any \<activity\> and \<activity-alias\> tag, returns and empty list.

| Parameters ||
|---|---|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property!>` | This value cannot be `null`. |

### queryApplicationProperty

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryApplicationProperty(propertyName: String): MutableList<PackageManager.Property!>
```

Returns the property definition for all \<application\> tags.

If the property is not defined with any \<application\> tag, returns and empty list.

| Parameters ||
|---|---|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property!>` | This value cannot be `null`. |

### queryBroadcastReceivers

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryBroadcastReceivers(
    intent: Intent, 
    flags: PackageManager.ResolveInfoFlags
): MutableList<ResolveInfo!>
```

See queryBroadcastReceivers.

| Parameters ||
|---|---|
| `intent` | [Intent](../android.content/Intent.md): This value cannot be `null`. |
| `flags` | [PackageManager.ResolveInfoFlags](../android/content/pm/PackageManager.ResolveInfoFlags.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo!>` | This value cannot be `null`. |

### queryBroadcastReceivers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun queryBroadcastReceivers(
    intent: Intent, 
    flags: Int
): MutableList<ResolveInfo!>
```

Retrieve all receivers that can handle a broadcast of the given intent. Use queryBroadcastReceivers when long flags are needed.

| Parameters ||
|---|---|
| `intent` | [Intent](../android.content/Intent.md): The desired intent as per resolveActivity(). This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo!>` | Returns a List of ResolveInfo objects containing one entry for each matching receiver, ordered from best to worst. If there are no matching receivers, returns an empty list. This value cannot be `null`. |

### queryContentProviders

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryContentProviders(
    processName: String?, 
    uid: Int, 
    flags: PackageManager.ComponentInfoFlags
): MutableList<ProviderInfo!>
```

See queryContentProviders.

| Parameters ||
|---|---|
| `processName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `flags` | [PackageManager.ComponentInfoFlags](../android/content/pm/PackageManager.ComponentInfoFlags.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo!>` | This value cannot be `null`. |

### queryContentProviders

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun queryContentProviders(
    processName: String?, 
    uid: Int, 
    flags: Int
): MutableList<ProviderInfo!>
```

Retrieve content provider information.

*Note: unlike most other methods, an empty result set is indicated by a null return instead of an empty list.* Use queryContentProviders when long flags are needed.

| Parameters ||
|---|---|
| `processName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: If non-null, limits the returned providers to only those that are hosted by the given process. If null, all content providers are returned. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): If processName is non-null, this is the required uid owning the requested content providers. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo!>` | A list of ProviderInfo objects containing one entry for each provider either matching processName or, if processName is null, all known content providers. *If there are no matching providers, null is returned.* |

### queryInstrumentation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun queryInstrumentation(
    targetPackage: String, 
    flags: Int
): MutableList<InstrumentationInfo!>
```

Retrieve information about available instrumentation code. May be used to retrieve either all instrumentation code, or only the code targeting a particular package.

| Parameters ||
|---|---|
| `targetPackage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): If null, all instrumentation is returned; only the instrumentation targeting this package name is returned. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_META_DATA:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/InstrumentationInfo!>` | A list of InstrumentationInfo objects containing one entry for each matching instrumentation. If there are no instrumentation available, returns an empty list. This value cannot be `null`. |

### queryIntentActivities

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryIntentActivities(
    intent: Intent, 
    flags: PackageManager.ResolveInfoFlags
): MutableList<ResolveInfo!>
```

See queryIntentActivities.

| Parameters ||
|---|---|
| `intent` | [Intent](../android.content/Intent.md): This value cannot be `null`. |
| `flags` | [PackageManager.ResolveInfoFlags](../android/content/pm/PackageManager.ResolveInfoFlags.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo!>` | This value cannot be `null`. |

### queryIntentActivities

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun queryIntentActivities(
    intent: Intent, 
    flags: Int
): MutableList<ResolveInfo!>
```

Retrieve all activities that can be performed for the given intent. Use queryIntentActivities when long flags are needed.

| Parameters ||
|---|---|
| `intent` | [Intent](../android.content/Intent.md): The desired intent as per resolveActivity(). This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. The most important is `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DEFAULT_ONLY:kotlin.Int`, to limit the resolution to only those activities that support the `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_DEFAULT:kotlin.String`. Or, set `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_ALL:kotlin.Int` to prevent any filtering of the results. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo!>` | Returns a List of ResolveInfo objects containing one entry for each matching activity, ordered from best to worst. In other words, the first item is what would be returned by #resolveActivity. If there are no matching activities, an empty list is returned. This value cannot be `null`. |

### queryIntentActivityOptions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun queryIntentActivityOptions(
    caller: ComponentName?, 
    specifics: Array<Intent!>?, 
    intent: Intent, 
    flags: Int
): MutableList<ResolveInfo!>
```

Retrieve a set of activities that should be presented to the user as similar options. This is like #queryIntentActivities, except it also allows you to supply a list of more explicit Intents that you would like to resolve to particular options, and takes care of returning the final ResolveInfo list in a reasonable order, with no duplicates, based on those inputs. Use queryIntentActivityOptions when long flags are needed.

| Parameters ||
|---|---|
| `caller` | [ComponentName](../android.content/ComponentName.md)?: The class name of the activity that is making the request. This activity will never appear in the output list. Can be null. |
| `specifics` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Intent](../android.content/Intent.md)!\>?: An array of Intents that should be resolved to the first specific results. Can be null. |
| `intent` | [Intent](../android.content/Intent.md): The desired intent as per resolveActivity(). This value cannot be `null`. |
| --- | --- |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. The most important is `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DEFAULT_ONLY:kotlin.Int`, to limit the resolution to only those activities that support the `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_DEFAULT:kotlin.String`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo!>` | Returns a List of ResolveInfo objects containing one entry for each matching activity. The list is ordered first by all of the intents resolved in specifics and then any additional activities that can handle intent but did not get included by one of the specifics intents. If there are no matching activities, an empty list is returned. This value cannot be `null`. |

### queryIntentActivityOptions

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryIntentActivityOptions(
    caller: ComponentName?, 
    specifics: MutableList<Intent!>?, 
    intent: Intent, 
    flags: PackageManager.ResolveInfoFlags
): MutableList<ResolveInfo!>
```

See queryIntentActivityOptions.

| Parameters ||
|---|---|
| `caller` | [ComponentName](../android.content/ComponentName.md)?: This value may be `null`. |
| `specifics` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Intent](../android.content/Intent.md)!\>?: This value may be `null`. |
| `intent` | [Intent](../android.content/Intent.md): This value cannot be `null`. |
| --- | --- |
| `flags` | [PackageManager.ResolveInfoFlags](../android/content/pm/PackageManager.ResolveInfoFlags.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo!>` | This value cannot be `null`. |

### queryIntentContentProviders

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryIntentContentProviders(
    intent: Intent, 
    flags: PackageManager.ResolveInfoFlags
): MutableList<ResolveInfo!>
```

See queryIntentContentProviders.

| Parameters ||
|---|---|
| `intent` | [Intent](../android.content/Intent.md): This value cannot be `null`. |
| `flags` | [PackageManager.ResolveInfoFlags](../android/content/pm/PackageManager.ResolveInfoFlags.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo!>` | This value cannot be `null`. |

### queryIntentContentProviders

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun queryIntentContentProviders(
    intent: Intent, 
    flags: Int
): MutableList<ResolveInfo!>
```

Retrieve all providers that can match the given intent. Use queryIntentContentProviders when long flags are needed.

| Parameters ||
|---|---|
| `intent` | [Intent](../android.content/Intent.md): An intent containing all of the desired specification (action, data, type, category, and/or component). This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo!>` | Returns a List of ResolveInfo objects containing one entry for each matching provider, ordered from best to worst. If there are no matching services, returns an empty list. This value cannot be `null`. |

### queryIntentServices

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryIntentServices(
    intent: Intent, 
    flags: PackageManager.ResolveInfoFlags
): MutableList<ResolveInfo!>
```

See queryIntentServices.

| Parameters ||
|---|---|
| `intent` | [Intent](../android.content/Intent.md): This value cannot be `null`. |
| `flags` | [PackageManager.ResolveInfoFlags](../android/content/pm/PackageManager.ResolveInfoFlags.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo!>` | This value cannot be `null`. |

### queryIntentServices

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun queryIntentServices(
    intent: Intent, 
    flags: Int
): MutableList<ResolveInfo!>
```

Retrieve all services that can match the given intent. Use queryIntentServices when long flags are needed.

| Parameters ||
|---|---|
| `intent` | [Intent](../android.content/Intent.md): The desired intent as per resolveService(). This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo!>` | Returns a List of ResolveInfo objects containing one entry for each matching service, ordered from best to worst. In other words, the first item is what would be returned by #resolveService. If there are no matching services, returns an empty list. This value cannot be `null`. |

### queryPermissionsByGroup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun queryPermissionsByGroup(
    permissionGroup: String?, 
    flags: Int
): MutableList<PermissionInfo!>
```

Query for all of the permissions associated with a particular group.

| Parameters ||
|---|---|
| `permissionGroup` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The fully qualified name (i.e. com.google.permission.LOGIN) of the permission group you are interested in. Use `null` to find all of the permissions not associated with a group. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#GET_META_DATA:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo!>` | Returns a list of PermissionInfo containing information about all of the permissions in the given group. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if a group with the given name cannot be found on the system. |

### queryProviderProperty

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryProviderProperty(propertyName: String): MutableList<PackageManager.Property!>
```

Returns the property definition for all \<provider\> tags.

If the property is not defined with any \<provider\> tag, returns and empty list.

| Parameters ||
|---|---|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property!>` | This value cannot be `null`. |

### queryReceiverProperty

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryReceiverProperty(propertyName: String): MutableList<PackageManager.Property!>
```

Returns the property definition for all \<receiver\> tags.

If the property is not defined with any \<receiver\> tag, returns and empty list.

| Parameters ||
|---|---|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property!>` | This value cannot be `null`. |

### queryServiceProperty

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryServiceProperty(propertyName: String): MutableList<PackageManager.Property!>
```

Returns the property definition for all \<service\> tags.

If the property is not defined with any \<service\> tag, returns and empty list.

| Parameters ||
|---|---|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property!>` | This value cannot be `null`. |

### relinquishUpdateOwnership

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun relinquishUpdateOwnership(targetPackage: String): Unit
```

Attempt to relinquish the update ownership of the given package. Only the current update owner of the given package can use this API.

| Parameters ||
|---|---|
| `targetPackage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The installed package whose update owner will be changed. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the given package is invalid. |
| `java.lang.SecurityException` | if you are not the current update owner of the given package. |

**See Also**

- setRequestUpdateOwnership

### removePackageFromPreferred

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun removePackageFromPreferred(packageName: String): Unit
```

**Deprecated:** *This function no longer does anything. It is the platform's responsibility to assign preferred activities and this cannot be modified directly. To determine the activities resolved by the platform, use #resolveActivity or #queryIntentActivities. To configure an app to be responsible for a particular role and to check current role holders, see `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#`.*

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### removePermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun removePermission(permName: String): Unit
```

Removes a permission that was previously added with addPermission. The same ownership rules apply -- you are only allowed to remove permissions that you are allowed to add.

| Parameters ||
|---|---|
| `permName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the permission to remove. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if you are not allowed to remove the given permission name. |

**See Also**

- addPermission

### removeWhitelistedRestrictedPermission

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeWhitelistedRestrictedPermission(
    packageName: String, 
    permName: String, 
    whitelistFlags: Int
): Boolean
```

Removes a whitelisted restricted permission for an app.

Permissions can be hard restricted which means that the app cannot hold them or soft restricted where the app can hold the permission but in a weaker form. Whether a permission is `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#FLAG_HARD_RESTRICTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo#FLAG_SOFT_RESTRICTED:kotlin.Int` depends on the permission declaration. Whitelisting a hard restricted permission allows for the to hold that permission and whitelisting a soft restricted permission allows the app to hold the permission in its full, unrestricted form.

<br />

There are four whitelists:
1. one for cases where the system permission policy whitelists a permission This list corresponds to the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_SYSTEM:kotlin.Int` flag. Can only be modified by pre-installed holders of a dedicated permission.
2. one for cases where the system whitelists the permission when upgrading from an OS version in which the permission was not restricted to an OS version in which the permission is restricted. This list corresponds to the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_UPGRADE:kotlin.Int` flag. Can be modified by pre-installed holders of a dedicated permission. The installer on record can only remove permissions from this whitelist.
3. one for cases where the installer of the package whitelists a permission. This list corresponds to the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_INSTALLER:kotlin.Int` flag. Can be modified by pre-installed holders of a dedicated permission or the installer on record.
4. one for cases where the system exempts the permission when upgrading from an OS version in which the permission was not restricted to an OS version in which the permission is restricted. This list corresponds to the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_UPGRADE:kotlin.Int` flag. Can be modified by pre-installed holders of a dedicated permission. The installer on record can only remove permissions from this allowlist.

You need to specify the whitelists for which to set the whitelisted permissions which will clear the previous whitelisted permissions and replace them with the provided ones.

**Note:**In retrospect it would have been preferred to use more inclusive terminology when naming this API. Similar APIs added will refrain from using the term "whitelist".

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The app for which to get whitelisted permissions. This value cannot be `null`. |
| `permName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The whitelisted permission to remove. This value cannot be `null`. |
| `whitelistFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The whitelists from which to remove. Passing multiple flags updates all specified whitelists. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_INSTALLER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_UPGRADE:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the permission was removed from the whitelist. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if you try to modify a whitelist that you have no access to. |

**See Also**

- getWhitelistedRestrictedPermissions
- addWhitelistedRestrictedPermission
- `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_SYSTEM:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_UPGRADE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FLAG_PERMISSION_WHITELIST_INSTALLER:kotlin.Int`

### requestChecksums

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestChecksums(
    packageName: String, 
    includeSplits: Boolean, 
    required: Int, 
    trustedInstallers: MutableList<Certificate!>, 
    onChecksumsReadyListener: PackageManager.OnChecksumsReadyListener
): Unit
```

Requests the checksums for APKs within a package. The checksums will be returned asynchronously via onChecksumsReadyListener. By default returns all readily available checksums: - enforced by platform, - enforced by installer. If caller needs a specific checksum kind, they can specify it as required. **Caution: Android can not verify installer-provided checksums. Make sure you specify trusted installers.**

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): whose checksums to return. This value cannot be `null`. |
| `includeSplits` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether to include checksums for non-base splits. |
| `required` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): explicitly request the checksum types. May incur significant CPU/memory/disk usage. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_MERKLE_ROOT_4K_SHA256:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_MD5:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_SHA1:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_SHA256:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_WHOLE_SHA512:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_PARTIAL_MERKLE_ROOT_1M_SHA256:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/Checksum#TYPE_PARTIAL_MERKLE_ROOT_1M_SHA512:kotlin.Int` |
| --- | --- |
| `trustedInstallers` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Certificate](../java.security.cert/Certificate.md)!\>: for checksums enforced by installer, which installers are to be trusted. `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#TRUST_ALL:kotlin.collections.MutableList` will return checksums from any installer, `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#TRUST_NONE:kotlin.collections.MutableList` disables optimized installer-enforced checksums, otherwise the list has to be non-empty list of certificates. This value cannot be `null`. |
| `onChecksumsReadyListener` | [PackageManager.OnChecksumsReadyListener](../android/content/pm/PackageManager.OnChecksumsReadyListener.md): called once when the results are available. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if a package with the given name cannot be found on the system. |
| `java.lang.IllegalArgumentException` | if the list of trusted installer certificates is empty. |
| `java.security.cert.CertificateEncodingException` | if an encoding error occurs for trustedInstallers. |
| --- | --- |

### resolveActivity

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun resolveActivity(
    intent: Intent, 
    flags: PackageManager.ResolveInfoFlags
): ResolveInfo?
```

See resolveActivity.

| Parameters ||
|---|---|
| `intent` | [Intent](../android.content/Intent.md): This value cannot be `null`. |
| `flags` | [PackageManager.ResolveInfoFlags](../android/content/pm/PackageManager.ResolveInfoFlags.md): This value cannot be `null`. |

| Return ||
|---|---|
| ResolveInfo | This value may be `null`. |

### resolveActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun resolveActivity(
    intent: Intent, 
    flags: Int
): ResolveInfo?
```

Determine the best action to perform for a given Intent. This is how resolveActivity finds an activity if a class has not been explicitly specified.

*Note:* if using an implicit Intent (without an explicit ComponentName specified), be sure to consider whether to set the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DEFAULT_ONLY:kotlin.Int` only flag. You need to do so to resolve the activity in the same way that startActivity and resolveActivity do.
Use resolveActivity when long flags are needed.

| Parameters ||
|---|---|
| `intent` | [Intent](../android.content/Intent.md): An intent containing all of the desired specification (action, data, type, category, and/or component). This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. The most important is `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#MATCH_DEFAULT_ONLY:kotlin.Int`, to limit the resolution to only those activities that support the `https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_DEFAULT:kotlin.String`. |

| Return ||
|---|---|
| ResolveInfo | Returns a ResolveInfo object containing the final activity intent that was determined to be the best action. Returns null if no matching activity was found. If multiple matching activities are found and there is no default set, returns a ResolveInfo object containing something else, such as the activity resolver. |

### resolveContentProvider

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun resolveContentProvider(
    authority: String, 
    flags: PackageManager.ComponentInfoFlags
): ProviderInfo?
```

See resolveContentProvider.

| Parameters ||
|---|---|
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `flags` | [PackageManager.ComponentInfoFlags](../android/content/pm/PackageManager.ComponentInfoFlags.md): This value cannot be `null`. |

| Return ||
|---|---|
| ProviderInfo | This value may be `null`. |

### resolveContentProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun resolveContentProvider(
    authority: String, 
    flags: Int
): ProviderInfo?
```

Find a single content provider by its authority.

Example:

```kotlin
Uri uri = Uri.parse("content://com.example.app.provider/table1");
  ProviderInfo info = packageManager.resolveContentProvider(uri.getAuthority(), flags);
  
```
Use resolveContentProvider when long flags are needed.

| Parameters ||
|---|---|
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The authority of the provider to find. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| ProviderInfo | A ProviderInfo object containing information about the provider. If a provider was not found, returns null. |

### resolveService

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun resolveService(
    intent: Intent, 
    flags: PackageManager.ResolveInfoFlags
): ResolveInfo?
```

See resolveService.

| Parameters ||
|---|---|
| `intent` | [Intent](../android.content/Intent.md): This value cannot be `null`. |
| `flags` | [PackageManager.ResolveInfoFlags](../android/content/pm/PackageManager.ResolveInfoFlags.md): This value cannot be `null`. |

| Return ||
|---|---|
| ResolveInfo | This value may be `null`. |

### resolveService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun resolveService(
    intent: Intent, 
    flags: Int
): ResolveInfo?
```

Determine the best service to handle for a given Intent. Use resolveService when long flags are needed.

| Parameters ||
|---|---|
| `intent` | [Intent](../android.content/Intent.md): An intent containing all of the desired specification (action, data, type, category, and/or component). This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional option flags to modify the data returned. |

| Return ||
|---|---|
| ResolveInfo | Returns a ResolveInfo object containing the final service intent that was determined to be the best action. Returns null if no matching service was found. |

### setApplicationCategoryHint

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setApplicationCategoryHint(
    packageName: String, 
    categoryHint: Int
): Unit
```

Provide a hint of what the `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#category:kotlin.Int` value should be for the given package.

This hint can only be set by the app which installed this package, as determined by getInstallerPackageName.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the package to change the category hint for. This value cannot be `null`. |
| `categoryHint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the category hint to set. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_UNDEFINED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_GAME:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_AUDIO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_VIDEO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_IMAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_SOCIAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_NEWS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_MAPS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_PRODUCTIVITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo#CATEGORY_ACCESSIBILITY:kotlin.Int` |

### setApplicationEnabledSetting

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setApplicationEnabledSetting(
    packageName: String, 
    newState: Int, 
    flags: Int
): Unit
```

Set the enabled setting for an application This setting will override any enabled state which may have been set by the application in its manifest. It also overrides the enabled state set in the manifest for any of the application's components. It does not override any enabled state set by setComponentEnabledSetting for any of the application's components.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The package name of the application to enable. This value cannot be `null`. |
| `newState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new enabled state for the application. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DISABLED_USER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DISABLED_UNTIL_USED:kotlin.Int` |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Optional behavior flags. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#DONT_KILL_APP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SYNCHRONOUS:kotlin.Int` |
| --- | --- |

### setAutoRevokeWhitelisted

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAutoRevokeWhitelisted(
    packageName: String, 
    whitelisted: Boolean
): Boolean
```

Marks an application exempt from having its permissions be automatically revoked when the app is unused for an extended period of time. Only the installer on record that installed the given package is allowed to call this. Packages start in whitelisted state, and it is the installer's responsibility to un-whitelist the packages it installs, unless auto-revoking permissions from that package would cause breakages beyond having to re-request the permission(s).

**Note:**In retrospect it would have been preferred to use more inclusive terminology when naming this API. Similar APIs added will refrain from using the term "whitelist".

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The app for which to set exemption. This value cannot be `null`. |
| `whitelisted` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether the app should be whitelisted. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether any change took effect. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if you you have no access to modify this. |

**See Also**

### setComponentEnabledSetting

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setComponentEnabledSetting(
    componentName: ComponentName, 
    newState: Int, 
    flags: Int
): Unit
```

Set the enabled setting for a package component (activity, receiver, service, provider). This setting will override any enabled state which may have been set by the component in its manifest.

Consider using setComponentEnabledSettings if multiple components need to be updated atomically.

| Parameters ||
|---|---|
| `componentName` | [ComponentName](../android.content/ComponentName.md): The component to enable. This value cannot be `null`. |
| `newState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new enabled state for the component. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DISABLED_USER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#COMPONENT_ENABLED_STATE_DISABLED_UNTIL_USED:kotlin.Int` |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Optional behavior flags. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#DONT_KILL_APP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#SYNCHRONOUS:kotlin.Int` |
| --- | --- |

### setComponentEnabledSettings

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setComponentEnabledSettings(settings: MutableList<PackageManager.ComponentEnabledSetting!>): Unit
```

Set the enabled settings for package components such as activities, receivers, services and providers. This setting will override any enabled state which may have been set by the component in its manifest.

This api accepts a list of component changes, and applies them all atomically. The application can use this api if components have dependencies and need to be updated atomically.

The permission is not required if target components are running under the same uid with the caller.

| Parameters ||
|---|---|
| `settings` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PackageManager.ComponentEnabledSetting](../android/content/pm/PackageManager.ComponentEnabledSetting.md)!\>: The list of component enabled settings to update. Note that an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` is thrown if the duplicated component name is in the list or there's a conflict `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#DONT_KILL_APP:kotlin.Int` flag between different components in the same package. This value cannot be `null`. |

**See Also**

- setComponentEnabledSetting

### setInstallerPackageName

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setInstallerPackageName(
    targetPackage: String, 
    installerPackageName: String?
): Unit
```

Change the installer associated with a given package. There are limitations on how the installer package can be changed; in particular:

- A SecurityException will be thrown if installerPackageName is not signed with the same certificate as the calling application.
- A SecurityException will be thrown if targetPackage already has an installer package, and that installer package is not signed with the same certificate as the calling application.

<br />

| Parameters ||
|---|---|
| `targetPackage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The installed package whose installer will be changed. This value cannot be `null`. |
| `installerPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The package name of the new installer. May be null to clear the association. |

### setMimeGroup

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMimeGroup(
    mimeGroup: String, 
    mimeTypes: MutableSet<String!>
): Unit
```

Sets MIME group's MIME types. Libraries should use a reverse-DNS prefix followed by a ':' character and library-specific group name to avoid namespace collisions, e.g. "com.example:myFeature".

| Parameters ||
|---|---|
| `mimeGroup` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): MIME group to modify. This value cannot be `null`. |
| `mimeTypes` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: new MIME types contained by MIME group. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the MIME group was not declared in the manifest. |

### updateInstantAppCookie

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun updateInstantAppCookie(cookie: ByteArray?): Unit
```

Updates the instant application cookie for the calling app. Non instant apps and apps that were instant but were upgraded to normal apps can still access this API. For instant apps this cookie is cached for some time after uninstall while for normal apps the cookie is deleted after the app is uninstalled. The cookie is always present while the app is installed. The cookie size is limited by getInstantAppCookieMaxBytes. Passing `null` or an empty array clears the cookie.

<br />

| Parameters ||
|---|---|
| `cookie` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: The cookie data. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the array exceeds max cookie size. |

**See Also**

- isInstantApp
- isInstantApp
- getInstantAppCookieMaxBytes
- getInstantAppCookie
- clearInstantAppCookie

### verifyPendingInstall

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun verifyPendingInstall(
    id: Int, 
    verificationCode: Int
): Unit
```

Allows a package listening to the `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_PACKAGE_NEEDS_VERIFICATION:kotlin.String` to respond to the package manager. The response must include the `verificationCode` which is one of `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#VERIFICATION_ALLOW:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#VERIFICATION_REJECT:kotlin.Int`.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): pending package identifier as passed via the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#EXTRA_VERIFICATION_ID:kotlin.String` Intent extra. |
| `verificationCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): either `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#VERIFICATION_ALLOW:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#VERIFICATION_REJECT:kotlin.Int`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller does not have the PACKAGE_VERIFICATION_AGENT permission. |

## Properties

### TRUST_ALL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRUST_ALL: MutableList<Certificate!>
```

Trust any Installer to provide checksums for the package.
**See Also**

- requestChecksums

### TRUST_NONE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRUST_NONE: MutableList<Certificate!>
```

Don't trust any Installer to provide checksums for the package. This effectively disables optimized Installer-enforced checksums.
**See Also**

- requestChecksums
