Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothHeadset

```
class BluetoothHeadset : BluetoothProfile
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothHeadset](BluetoothHeadset.md) |

Public API for controlling the Bluetooth Headset Service. This includes both Bluetooth Headset and Handsfree (v1.5) profiles.

BluetoothHeadset is a proxy object for controlling the Bluetooth Headset Service via IPC.

Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getProfileProxy(android.content.Context,%20android.bluetooth.BluetoothProfile.ServiceListener,%20kotlin.Int)` to get the BluetoothHeadset proxy object. Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#closeProfileProxy(kotlin.Int,%20android.bluetooth.BluetoothProfile)` to close the service connection.

Android only supports one connected Bluetooth Headset at a time. Each method is protected with its appropriate permission.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#ACTION_AUDIO_STATE_CHANGED:kotlin.String` Intent used to broadcast the change in the Audio Connection state of the HFP profile. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#ACTION_CONNECTION_STATE_CHANGED:kotlin.String` Intent used to broadcast the change in connection state of the Headset profile. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#ACTION_VENDOR_SPECIFIC_HEADSET_EVENT:kotlin.String` Intent used to broadcast that the headset has posted a vendor-specific event. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#AT_CMD_TYPE_ACTION:kotlin.Int` AT command type ACTION used with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_CMD_TYPE:kotlin.String` For example, AT+CHUP. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#AT_CMD_TYPE_BASIC:kotlin.Int` AT command type BASIC used with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_CMD_TYPE:kotlin.String` For example, ATD. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#AT_CMD_TYPE_READ:kotlin.Int` AT command type READ used with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_CMD_TYPE:kotlin.String` For example, AT+VGM?. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#AT_CMD_TYPE_SET:kotlin.Int` AT command type SET used with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_CMD_TYPE:kotlin.String` For example, AT+VGM=. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#AT_CMD_TYPE_TEST:kotlin.Int` AT command type TEST used with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_CMD_TYPE:kotlin.String` For example, AT+VGM=?. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#CODEC_TYPE_CVSD:kotlin.Int` HFP codec type CVSD. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#CODEC_TYPE_LC3_SWB:kotlin.Int` HFP codec type LC3 SWB. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#CODEC_TYPE_MSBC:kotlin.Int` HFP codec type mSBC. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#CODEC_TYPE_UNSUPPORTED:kotlin.Int` HFP codec type is not supported or cannot be determined |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#CODEC_TYPE_VENDOR_SPECIFIC:kotlin.Int` HFP vendor specific codec Type |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#EXTRA_DISCONNECTED_REASON:kotlin.String` Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#ACTION_CONNECTION_STATE_CHANGED:kotlin.String` intents for connection failure reasons. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_ARGS:kotlin.String` A Parcelable String array extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#ACTION_VENDOR_SPECIFIC_HEADSET_EVENT:kotlin.String` intents that contains the arguments to the vendor-specific command. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_CMD:kotlin.String` A String extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#ACTION_VENDOR_SPECIFIC_HEADSET_EVENT:kotlin.String` intents that contains the name of the vendor-specific command. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_CMD_TYPE:kotlin.String` An int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#ACTION_VENDOR_SPECIFIC_HEADSET_EVENT:kotlin.String` intents that contains the AT command type of the vendor-specific command. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#STATE_AUDIO_CONNECTED:kotlin.Int` Headset state when SCO audio is connected. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#STATE_AUDIO_CONNECTING:kotlin.Int` Headset state when SCO audio is connecting. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#STATE_AUDIO_DISCONNECTED:kotlin.Int` Headset state when SCO audio is not connected. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#VENDOR_RESULT_CODE_COMMAND_ANDROID:kotlin.String` A vendor-specific command for unsolicited result code. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#VENDOR_SPECIFIC_HEADSET_EVENT_COMPANY_ID_CATEGORY:kotlin.String` The intent category to be used with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#ACTION_VENDOR_SPECIFIC_HEADSET_EVENT:kotlin.String` for the companyId |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#A2DP:kotlin.Int`

Advanced Audio Distribution Profile (A2DP)

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#CSIP_SET_COORDINATOR:kotlin.Int`

Coordinated Set Identification Profile (CSIP) set coordinator

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_PREVIOUS_STATE:kotlin.String`

Extra for the connection state intents of the individual profiles.

This extra represents the previous connection state of the profile of the Bluetooth device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_PROFILE:kotlin.String`

Extra for the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile` that the intent applies to.

This extra represents the Bluetooth profile that the intent applies to.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_STATE:kotlin.String`

Extra for the connection state intents of the individual profiles.

This extra represents the current connection state of the profile of the Bluetooth device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#GATT:kotlin.Int`

Generic Attribute Profile (GATT)

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#GATT_SERVER:kotlin.Int`

Generic Attribute Profile (GATT) Server

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HAP_CLIENT:kotlin.Int`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HEADSET:kotlin.Int`

Headset and Handsfree profile

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HEALTH:kotlin.Int`

Health Profile

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HEARING_AID:kotlin.Int`

Hearing Aid Device

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HID_DEVICE:kotlin.Int`

Human Interface Device (HID) Device

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#LE_AUDIO:kotlin.Int`

LE Audio Device

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#SAP:kotlin.Int`

SIM Access Profile (SAP)

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int`

The profile is in connected state

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int`

The profile is in connecting state

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int`

The profile is in disconnected state

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int`

The profile is in disconnecting state

<br />

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#getCodecType(android.bluetooth.BluetoothDevice)(device: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)` Get the codec type of the given HFP connected device. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](BluetoothDevice.md)!\>! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#getConnectedDevices()()` Get connected devices for this specific profile. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#getConnectionState(android.bluetooth.BluetoothDevice)(device: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!)` Get the current connection state of the profile For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](BluetoothDevice.md)!\>! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#getDevicesMatchingConnectionStates(kotlin.IntArray)(states: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!)` Get a list of devices that match any of the given connection states. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#isAudioConnected(android.bluetooth.BluetoothDevice)(device: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!)` Check if Bluetooth SCO audio is connected. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#isNoiseReductionSupported(android.bluetooth.BluetoothDevice)(device: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)` Checks whether the headset supports some form of noise reduction. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#isVoiceRecognitionSupported(android.bluetooth.BluetoothDevice)(device: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)` Checks whether the headset supports voice recognition. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#sendVendorSpecificResultCode(android.bluetooth.BluetoothDevice,%20kotlin.String,%20kotlin.String)(device: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!, command: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Sends a vendor-specific unsolicited result code to the headset. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#startVoiceRecognition(android.bluetooth.BluetoothDevice)(device: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!)` Start Bluetooth voice recognition. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#stopVoiceRecognition(android.bluetooth.BluetoothDevice)(device: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!)` Stop Bluetooth Voice Recognition mode, and shut down the Bluetooth audio path. |

| Protected methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

## Constants

### ACTION_AUDIO_STATE_CHANGED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_AUDIO_STATE_CHANGED: String
```

Intent used to broadcast the change in the Audio Connection state of the HFP profile.

This intent will have 3 extras:

- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_STATE:kotlin.String` - The current state of the profile.
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_PREVIOUS_STATE:kotlin.String`- The previous state of the profile.
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DEVICE:kotlin.String` - The remote device.

`https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_PREVIOUS_STATE:kotlin.String` can be any of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#STATE_AUDIO_CONNECTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#STATE_AUDIO_DISCONNECTED:kotlin.Int`,. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

 Value: "android.bluetooth.headset.profile.action.AUDIO_STATE_CHANGED"

### ACTION_CONNECTION_STATE_CHANGED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CONNECTION_STATE_CHANGED: String
```

Intent used to broadcast the change in connection state of the Headset profile.

This intent will have the following extras:

- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_STATE:kotlin.String` - The current state of the profile.
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_PREVIOUS_STATE:kotlin.String`- The previous state of the profile.
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DEVICE:kotlin.String` - The remote device.
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#EXTRA_DISCONNECTED_REASON:kotlin.String` - A disconnection reason if moved from `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int`.
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_CLASS:kotlin.String` - The class of the remote device, if available, when the new state is `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int`.
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_LE_APPEARANCE:kotlin.String` - The LE appearance of the remote device, if available, when the new state is `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int`.

`https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_PREVIOUS_STATE:kotlin.String` can be any of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int`. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

 Value: "android.bluetooth.headset.profile.action.CONNECTION_STATE_CHANGED"

### ACTION_VENDOR_SPECIFIC_HEADSET_EVENT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_VENDOR_SPECIFIC_HEADSET_EVENT: String
```

Intent used to broadcast that the headset has posted a vendor-specific event.

This intent will have 4 extras and 1 category.

- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DEVICE:kotlin.String` - The remote Bluetooth Device
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_CMD:kotlin.String` - The vendor specific command
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_CMD_TYPE:kotlin.String` - The AT command type which can be one of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#AT_CMD_TYPE_READ:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#AT_CMD_TYPE_TEST:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#AT_CMD_TYPE_SET:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#AT_CMD_TYPE_BASIC:kotlin.Int`,`https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#AT_CMD_TYPE_ACTION:kotlin.Int`.
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_ARGS:kotlin.String` - Command arguments.

The category is the Company ID of the vendor defining the vendor-specific command. `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAssignedNumbers`

For example, for Plantronics specific events Category will be `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#VENDOR_SPECIFIC_HEADSET_EVENT_COMPANY_ID_CATEGORY:kotlin.String`.55

For example, an AT+XEVENT=foo,3 will get translated into

- EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_CMD = +XEVENT
- EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_CMD_TYPE = AT_CMD_TYPE_SET
- EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_ARGS = foo, 3

. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

 Value: "android.bluetooth.headset.action.VENDOR_SPECIFIC_HEADSET_EVENT"

### AT_CMD_TYPE_ACTION

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AT_CMD_TYPE_ACTION: Int
```

AT command type ACTION used with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_CMD_TYPE:kotlin.String` For example, AT+CHUP. There are no arguments for action commands.

 Value: 4

### AT_CMD_TYPE_BASIC

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AT_CMD_TYPE_BASIC: Int
```

AT command type BASIC used with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_CMD_TYPE:kotlin.String` For example, ATD. Single character commands and everything following the character are arguments.

 Value: 3

### AT_CMD_TYPE_READ

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AT_CMD_TYPE_READ: Int
```

AT command type READ used with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_CMD_TYPE:kotlin.String` For example, AT+VGM?. There are no arguments for this command type.

 Value: 0

### AT_CMD_TYPE_SET

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AT_CMD_TYPE_SET: Int
```

AT command type SET used with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_CMD_TYPE:kotlin.String` For example, AT+VGM=.

 Value: 2

### AT_CMD_TYPE_TEST

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AT_CMD_TYPE_TEST: Int
```

AT command type TEST used with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_CMD_TYPE:kotlin.String` For example, AT+VGM=?. There are no arguments for this command type.

 Value: 1

### CODEC_TYPE_CVSD

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODEC_TYPE_CVSD: Int
```

HFP codec type CVSD.

Continuous Variable Slope Delta modulation (CVSD) as defined by the Bluetooth SIG in the HFP Specification.

 Value: 1

### CODEC_TYPE_LC3_SWB

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODEC_TYPE_LC3_SWB: Int
```

HFP codec type LC3 SWB.

Low Complexity Communication Codec (LC3) for Super Wideband (SWB) as defined by the Bluetooth SIG in the HFP Specification.

 Value: 3

### CODEC_TYPE_MSBC

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODEC_TYPE_MSBC: Int
```

HFP codec type mSBC.

Modified Sub-Band Codec (mSBC) as defined by the Bluetooth SIG in the HFP Specification.

 Value: 2

### CODEC_TYPE_UNSUPPORTED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODEC_TYPE_UNSUPPORTED: Int
```

HFP codec type is not supported or cannot be determined

 Value: -1

### CODEC_TYPE_VENDOR_SPECIFIC

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CODEC_TYPE_VENDOR_SPECIFIC: Int
```

HFP vendor specific codec Type

 Value: 0

### EXTRA_DISCONNECTED_REASON

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DISCONNECTED_REASON: String
```

Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#ACTION_CONNECTION_STATE_CHANGED:kotlin.String` intents for connection failure reasons.

The value is one of the following:

- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#SUCCESS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_UNKNOWN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_INSUFFICIENT_RESOURCES:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_SDP_DISCOVERY_FAILED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_RFCOMM_CONNECTION_FAILED:kotlin.Int`

 Value: "android.bluetooth.headset.extra.DISCONNECTED_REASON"

### EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_ARGS

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_ARGS: String
```

A Parcelable String array extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#ACTION_VENDOR_SPECIFIC_HEADSET_EVENT:kotlin.String` intents that contains the arguments to the vendor-specific command.

 Value: "android.bluetooth.headset.extra.VENDOR_SPECIFIC_HEADSET_EVENT_ARGS"

### EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_CMD

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_CMD: String
```

A String extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#ACTION_VENDOR_SPECIFIC_HEADSET_EVENT:kotlin.String` intents that contains the name of the vendor-specific command.

 Value: "android.bluetooth.headset.extra.VENDOR_SPECIFIC_HEADSET_EVENT_CMD"

### EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_CMD_TYPE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_VENDOR_SPECIFIC_HEADSET_EVENT_CMD_TYPE: String
```

An int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#ACTION_VENDOR_SPECIFIC_HEADSET_EVENT:kotlin.String` intents that contains the AT command type of the vendor-specific command.

 Value: "android.bluetooth.headset.extra.VENDOR_SPECIFIC_HEADSET_EVENT_CMD_TYPE"

### STATE_AUDIO_CONNECTED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_AUDIO_CONNECTED: Int
```

Headset state when SCO audio is connected. This state can be one of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_PREVIOUS_STATE:kotlin.String` of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#ACTION_AUDIO_STATE_CHANGED:kotlin.String` intent.

 Value: 12

### STATE_AUDIO_CONNECTING

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_AUDIO_CONNECTING: Int
```

Headset state when SCO audio is connecting. This state can be one of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_PREVIOUS_STATE:kotlin.String` of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#ACTION_AUDIO_STATE_CHANGED:kotlin.String` intent.

 Value: 11

### STATE_AUDIO_DISCONNECTED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_AUDIO_DISCONNECTED: Int
```

Headset state when SCO audio is not connected. This state can be one of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_PREVIOUS_STATE:kotlin.String` of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#ACTION_AUDIO_STATE_CHANGED:kotlin.String` intent.

 Value: 10

### VENDOR_RESULT_CODE_COMMAND_ANDROID

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VENDOR_RESULT_CODE_COMMAND_ANDROID: String
```

A vendor-specific command for unsolicited result code.

 Value: "+ANDROID"

### VENDOR_SPECIFIC_HEADSET_EVENT_COMPANY_ID_CATEGORY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VENDOR_SPECIFIC_HEADSET_EVENT_COMPANY_ID_CATEGORY: String
```

The intent category to be used with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#ACTION_VENDOR_SPECIFIC_HEADSET_EVENT:kotlin.String` for the companyId

 Value: "android.bluetooth.headset.intent.category.companyid"

## Public methods

### getCodecType

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCodecType(device: BluetoothDevice): Int
```

Get the codec type of the given HFP connected device.

This method returns the codec type that has been negotiated between the AG and HF which is available once the HFP SLC is established and the codec negotiation process is completed. The negotiated codec can be retrieved regardless of whether a SCO audio connection is currently active or not. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `device` | [BluetoothDevice](BluetoothDevice.md): The remote Bluetooth device. Must not be null. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The codec type of the given HFP connected device. Returns `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#CODEC_TYPE_UNSUPPORTED:kotlin.Int` if Bluetooth is off, the profile is not connected, the device is not connected, the codec negotiation is not completed, or an error occurs. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#CODEC_TYPE_LC3_SWB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#CODEC_TYPE_MSBC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#CODEC_TYPE_CVSD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#CODEC_TYPE_VENDOR_SPECIFIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#CODEC_TYPE_UNSUPPORTED:kotlin.Int` |

### getConnectedDevices

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConnectedDevices(): MutableList<BluetoothDevice!>!
```

Get connected devices for this specific profile.

Return the set of devices which are in state `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int` 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!>!` | List of devices. The list will be empty on error. |

### getConnectionState

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConnectionState(device: BluetoothDevice!): Int
```

Get the current connection state of the profile 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `device` | [BluetoothDevice](BluetoothDevice.md)!: Remote bluetooth device. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | State of the profile connection. One of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int` |

### getDevicesMatchingConnectionStates

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDevicesMatchingConnectionStates(states: IntArray!): MutableList<BluetoothDevice!>!
```

Get a list of devices that match any of the given connection states.

If none of the devices match any of the given states, an empty list will be returned. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `states` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: Array of states. States can be one of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int`, |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!>!` | List of devices. The list will be empty on error. |

### isAudioConnected

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAudioConnected(device: BluetoothDevice!): Boolean
```

Check if Bluetooth SCO audio is connected. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `device` | [BluetoothDevice](BluetoothDevice.md)!: Bluetooth headset |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if SCO is connected, false otherwise or on error |

### isNoiseReductionSupported

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isNoiseReductionSupported(device: BluetoothDevice): Boolean
```

Checks whether the headset supports some form of noise reduction. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `device` | [BluetoothDevice](BluetoothDevice.md): Bluetooth device. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if echo cancellation and/or noise reduction is supported, false otherwise |

### isVoiceRecognitionSupported

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isVoiceRecognitionSupported(device: BluetoothDevice): Boolean
```

Checks whether the headset supports voice recognition. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `device` | [BluetoothDevice](BluetoothDevice.md): Bluetooth device. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if voice recognition is supported, false otherwise |

### sendVendorSpecificResultCode

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendVendorSpecificResultCode(
    device: BluetoothDevice!, 
    command: String!, 
    arg: String!
): Boolean
```

Sends a vendor-specific unsolicited result code to the headset.

The actual string to be sent is `command + ": " + arg`. For example, if `command` is `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#VENDOR_RESULT_CODE_COMMAND_ANDROID:kotlin.String` and `arg` is `"0"`, the string `"+ANDROID: 0"` will be sent.

Currently only `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#VENDOR_RESULT_CODE_COMMAND_ANDROID:kotlin.String` is allowed as `command`. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `device` | [BluetoothDevice](BluetoothDevice.md)!: Bluetooth headset. |
| `command` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A vendor-specific command. |
| `arg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The argument that will be attached to the command. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `false` if there is no headset connected, or if the command is not an allowed vendor-specific unsolicited result code, or on error. `true` otherwise. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `command` is `null`. |

### startVoiceRecognition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun startVoiceRecognition(device: BluetoothDevice!): Boolean
```

Start Bluetooth voice recognition. This methods sends the voice recognition AT command to the headset and establishes the audio connection.

Users can listen to `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#ACTION_AUDIO_STATE_CHANGED:kotlin.String`. If this function returns true, this intent will be broadcasted with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_STATE:kotlin.String` set to `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#STATE_AUDIO_CONNECTING:kotlin.Int`.

`https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_STATE:kotlin.String` will transition from `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#STATE_AUDIO_CONNECTING:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#STATE_AUDIO_CONNECTED:kotlin.Int` when audio connection is established and to `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#STATE_AUDIO_DISCONNECTED:kotlin.Int` in case of failure to establish the audio connection. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `device` | [BluetoothDevice](BluetoothDevice.md)!: Bluetooth headset |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | false if there is no headset connected, or the connected headset doesn't support voice recognition, or voice recognition is already started, or audio channel is occupied, or on error, true otherwise |

### stopVoiceRecognition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun stopVoiceRecognition(device: BluetoothDevice!): Boolean
```

Stop Bluetooth Voice Recognition mode, and shut down the Bluetooth audio path.

Users can listen to `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#ACTION_AUDIO_STATE_CHANGED:kotlin.String`. If this function returns true, this intent will be broadcasted with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_STATE:kotlin.String` set to `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset#STATE_AUDIO_DISCONNECTED:kotlin.Int`. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `device` | [BluetoothDevice](BluetoothDevice.md)!: Bluetooth headset |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | false if there is no headset connected, or voice recognition has not started, or voice recognition has ended on this headset, or on error, true otherwise |

## Protected methods

### finalize

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun finalize(): Unit
```

Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup.

The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded.

The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition.

The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates.

After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded.

The `finalize` method is never invoked more than once by a Java virtual machine for any given object.

Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored.

| Exceptions ||
|---|---|
| `java.lang.Throwable` | the `Exception` raised by this method |
