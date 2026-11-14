# BluetoothHidDevice

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothHidDevice

Kotlin| [Java](https://developer.android.com/reference/android/bluetooth/BluetoothHidDevice "View this page in Java") 
| --- | --- |

```
class BluetoothHidDevice : BluetoothProfile
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothHidDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#) |

Provides the public APIs to control the Bluetooth HID Device profile.

BluetoothHidDevice is a proxy object for controlling the Bluetooth HID Device Service via IPC. Use [BluetoothAdapter.getProfileProxy](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getProfileProxy(android.content.Context,%20android.bluetooth.BluetoothProfile.ServiceListener,%20kotlin.Int))to get the BluetoothHidDevice proxy object.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Callback](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback) The template class that applications use to call callback functions on events from the HID host. |

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_CONNECTION_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#ACTION_CONNECTION_STATE_CHANGED:kotlin.String) Intent used to broadcast the change in connection state of the Input Host profile. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [ERROR_RSP_INVALID_PARAM](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#ERROR_RSP_INVALID_PARAM:kotlin.Byte) Constant representing error response for Set Report due to "invalid parameter". |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [ERROR_RSP_INVALID_RPT_ID](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#ERROR_RSP_INVALID_RPT_ID:kotlin.Byte) Constant representing error response for Set Report due to "invalid report ID". |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [ERROR_RSP_NOT_READY](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#ERROR_RSP_NOT_READY:kotlin.Byte) Constant representing error response for Set Report due to "not ready". |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [ERROR_RSP_SUCCESS](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#ERROR_RSP_SUCCESS:kotlin.Byte) Constant representing success response for Set Report. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [ERROR_RSP_UNKNOWN](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#ERROR_RSP_UNKNOWN:kotlin.Byte) Constant representing error response for Set Report with unknown reason. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [ERROR_RSP_UNSUPPORTED_REQ](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#ERROR_RSP_UNSUPPORTED_REQ:kotlin.Byte) Constant representing error response for Set Report due to "unsupported request". |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [PROTOCOL_BOOT_MODE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#PROTOCOL_BOOT_MODE:kotlin.Byte) Constant representing boot protocol mode used set by host. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [PROTOCOL_REPORT_MODE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#PROTOCOL_REPORT_MODE:kotlin.Byte) Constant representing report protocol mode used set by host. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [REPORT_TYPE_FEATURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#REPORT_TYPE_FEATURE:kotlin.Byte) Constant representing HID Feature Report type. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [REPORT_TYPE_INPUT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#REPORT_TYPE_INPUT:kotlin.Byte) Constant representing HID Input Report type. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [REPORT_TYPE_OUTPUT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#REPORT_TYPE_OUTPUT:kotlin.Byte) Constant representing HID Output Report type. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SUBCLASS1_COMBO](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#SUBCLASS1_COMBO:kotlin.Byte) Constant representing combo keyboard and mouse subclass. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SUBCLASS1_KEYBOARD](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#SUBCLASS1_KEYBOARD:kotlin.Byte) Constant representing keyboard subclass. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SUBCLASS1_MOUSE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#SUBCLASS1_MOUSE:kotlin.Byte) Constant representing mouse subclass. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SUBCLASS1_NONE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#SUBCLASS1_NONE:kotlin.Byte) Constant representing unspecified HID device subclass. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SUBCLASS2_CARD_READER](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#SUBCLASS2_CARD_READER:kotlin.Byte) Constant representing card reader subclass. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SUBCLASS2_DIGITIZER_TABLET](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#SUBCLASS2_DIGITIZER_TABLET:kotlin.Byte) Constant representing digitizer tablet subclass. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SUBCLASS2_GAMEPAD](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#SUBCLASS2_GAMEPAD:kotlin.Byte) Constant representing gamepad subclass. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SUBCLASS2_JOYSTICK](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#SUBCLASS2_JOYSTICK:kotlin.Byte) Constant representing joystick subclass. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SUBCLASS2_REMOTE_CONTROL](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#SUBCLASS2_REMOTE_CONTROL:kotlin.Byte) Constant representing remote control subclass. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SUBCLASS2_SENSING_DEVICE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#SUBCLASS2_SENSING_DEVICE:kotlin.Byte) Constant representing sensing device subclass. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SUBCLASS2_UNCATEGORIZED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#SUBCLASS2_UNCATEGORIZED:kotlin.Byte) Constant representing uncategorized HID device subclass. |

| Inherited constants ||
|---|---|
| From class [BluetoothProfile](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile) |----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [A2DP](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#A2DP:kotlin.Int) <br /> Advanced Audio Distribution Profile (A2DP) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CSIP_SET_COORDINATOR](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#CSIP_SET_COORDINATOR:kotlin.Int) <br /> Coordinated Set Identification Profile (CSIP) set coordinator <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PREVIOUS_STATE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_PREVIOUS_STATE:kotlin.String) <br /> Extra for the connection state intents of the individual profiles. This extra represents the previous connection state of the profile of the Bluetooth device. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PROFILE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_PROFILE:kotlin.String) <br /> Extra for the [BluetoothProfile](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile) that the intent applies to. This extra represents the Bluetooth profile that the intent applies to. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_STATE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_STATE:kotlin.String) <br /> Extra for the connection state intents of the individual profiles. This extra represents the current connection state of the profile of the Bluetooth device. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GATT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#GATT:kotlin.Int) <br /> Generic Attribute Profile (GATT) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GATT_SERVER](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#GATT_SERVER:kotlin.Int) <br /> Generic Attribute Profile (GATT) Server <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HAP_CLIENT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HAP_CLIENT:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEADSET](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HEADSET:kotlin.Int) <br /> Headset and Handsfree profile <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEALTH](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HEALTH:kotlin.Int) <br /> Health Profile <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEARING_AID](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HEARING_AID:kotlin.Int) <br /> Hearing Aid Device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HID_DEVICE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HID_DEVICE:kotlin.Int) <br /> Human Interface Device (HID) Device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LE_AUDIO](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#LE_AUDIO:kotlin.Int) <br /> LE Audio Device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAP](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#SAP:kotlin.Int) <br /> SIM Access Profile (SAP) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int) <br /> The profile is in connected state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int) <br /> The profile is in connecting state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int) <br /> The profile is in disconnected state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISCONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int) <br /> The profile is in disconnecting state <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [connect](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#connect(android.bluetooth.BluetoothDevice))`(`device:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!`)` Initiates connection to host which is currently paired with this device. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [disconnect](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#disconnect(android.bluetooth.BluetoothDevice))`(`device:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!`)` Disconnects from currently connected host. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!\>! | [getConnectedDevices](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#getConnectedDevices())`()` Get connected devices for this specific profile. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConnectionState](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#getConnectionState(android.bluetooth.BluetoothDevice))`(`device:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!`)` Get the current connection state of the profile For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!\>! | [getDevicesMatchingConnectionStates](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#getDevicesMatchingConnectionStates(kotlin.IntArray))`(`states:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Get a list of devices that match any of the given connection states. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerApp](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#registerApp(android.bluetooth.BluetoothHidDeviceAppSdpSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20java.util.concurrent.Executor,%20android.bluetooth.BluetoothHidDevice.Callback))`(`sdp:` ` [BluetoothHidDeviceAppSdpSettings](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppSdpSettings)!`, `inQos:` ` [BluetoothHidDeviceAppQosSettings](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppQosSettings)!`, `outQos:` ` [BluetoothHidDeviceAppQosSettings](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppQosSettings)!`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)!`, `callback:` ` [BluetoothHidDevice.Callback](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback)!`)` Registers application to be used for HID device. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [replyReport](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#replyReport(android.bluetooth.BluetoothDevice,%20kotlin.Byte,%20kotlin.Byte,%20kotlin.ByteArray))`(`device:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!`, `type:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`, `id:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Sends report to remote host as reply for GET_REPORT request from [android.bluetooth.BluetoothHidDevice.Callback#onGetReport(android.bluetooth.BluetoothDevice,byte,byte,int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback#onGetReport(android.bluetooth.BluetoothDevice,%20kotlin.Byte,%20kotlin.Byte,%20kotlin.Int)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [reportError](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#reportError(android.bluetooth.BluetoothDevice,%20kotlin.Byte))`(`device:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!`, `error:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Sends error handshake message as reply for invalid SET_REPORT request from[android.bluetooth.BluetoothHidDevice.Callback#onSetReport(android.bluetooth.BluetoothDevice,byte,byte,byte[])](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback#onSetReport(android.bluetooth.BluetoothDevice,%20kotlin.Byte,%20kotlin.Byte,%20kotlin.ByteArray)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [sendReport](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#sendReport(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.ByteArray))`(`device:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!`, `id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Sends report to remote host using interrupt channel. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [unregisterApp](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#unregisterApp())`()` Unregisters application. |

## Constants

### ACTION_CONNECTION_STATE_CHANGED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_CONNECTION_STATE_CHANGED: String
```

Intent used to broadcast the change in connection state of the Input Host profile.

This intent will have 3 extras:

- [EXTRA_STATE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_STATE:kotlin.String)- The current state of the profile.
- [EXTRA_PREVIOUS_STATE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_PREVIOUS_STATE:kotlin.String)- The previous state of the profile.
- [BluetoothDevice.EXTRA_DEVICE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DEVICE:kotlin.String)- The remote device.

[EXTRA_STATE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_STATE:kotlin.String) or [EXTRA_PREVIOUS_STATE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_PREVIOUS_STATE:kotlin.String) can be any of [STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int), [STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int), [STATE_CONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int), [STATE_DISCONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int). 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) 

 Value: "android.bluetooth.hiddevice.profile.action.CONNECTION_STATE_CHANGED"

### ERROR_RSP_INVALID_PARAM

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_RSP_INVALID_PARAM: Byte
```

Constant representing error response for Set Report due to "invalid parameter". 

 Value: 4

**See Also**

- [android.bluetooth.BluetoothHidDevice.Callback#onSetReport(BluetoothDevice, byte, byte, byte[])](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback#onSetReport(android.bluetooth.BluetoothDevice,%20kotlin.Byte,%20kotlin.Byte,%20kotlin.ByteArray)) 

### ERROR_RSP_INVALID_RPT_ID

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_RSP_INVALID_RPT_ID: Byte
```

Constant representing error response for Set Report due to "invalid report ID". 

 Value: 2

**See Also**

- [android.bluetooth.BluetoothHidDevice.Callback#onSetReport(BluetoothDevice, byte, byte, byte[])](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback#onSetReport(android.bluetooth.BluetoothDevice,%20kotlin.Byte,%20kotlin.Byte,%20kotlin.ByteArray)) 

### ERROR_RSP_NOT_READY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_RSP_NOT_READY: Byte
```

Constant representing error response for Set Report due to "not ready". 

 Value: 1

**See Also**

- [android.bluetooth.BluetoothHidDevice.Callback#onSetReport(BluetoothDevice, byte, byte, byte[])](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback#onSetReport(android.bluetooth.BluetoothDevice,%20kotlin.Byte,%20kotlin.Byte,%20kotlin.ByteArray)) 

### ERROR_RSP_SUCCESS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_RSP_SUCCESS: Byte
```

Constant representing success response for Set Report. 

 Value: 0

**See Also**

- [android.bluetooth.BluetoothHidDevice.Callback#onSetReport(BluetoothDevice, byte, byte, byte[])](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback#onSetReport(android.bluetooth.BluetoothDevice,%20kotlin.Byte,%20kotlin.Byte,%20kotlin.ByteArray)) 

### ERROR_RSP_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_RSP_UNKNOWN: Byte
```

Constant representing error response for Set Report with unknown reason. 

 Value: 14

**See Also**

- [android.bluetooth.BluetoothHidDevice.Callback#onSetReport(BluetoothDevice, byte, byte, byte[])](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback#onSetReport(android.bluetooth.BluetoothDevice,%20kotlin.Byte,%20kotlin.Byte,%20kotlin.ByteArray)) 

### ERROR_RSP_UNSUPPORTED_REQ

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_RSP_UNSUPPORTED_REQ: Byte
```

Constant representing error response for Set Report due to "unsupported request". 

 Value: 3

**See Also**

- [android.bluetooth.BluetoothHidDevice.Callback#onSetReport(BluetoothDevice, byte, byte, byte[])](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback#onSetReport(android.bluetooth.BluetoothDevice,%20kotlin.Byte,%20kotlin.Byte,%20kotlin.ByteArray)) 

### PROTOCOL_BOOT_MODE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROTOCOL_BOOT_MODE: Byte
```

Constant representing boot protocol mode used set by host. Default is always [PROTOCOL_REPORT_MODE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#PROTOCOL_REPORT_MODE:kotlin.Byte) unless notified otherwise. 

 Value: 0

**See Also**

- [android.bluetooth.BluetoothHidDevice.Callback#onSetProtocol(BluetoothDevice, byte)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback#onSetProtocol(android.bluetooth.BluetoothDevice,%20kotlin.Byte)) 

### PROTOCOL_REPORT_MODE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROTOCOL_REPORT_MODE: Byte
```

Constant representing report protocol mode used set by host. Default is always [PROTOCOL_REPORT_MODE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#PROTOCOL_REPORT_MODE:kotlin.Byte) unless notified otherwise. 

 Value: 1

**See Also**

- [android.bluetooth.BluetoothHidDevice.Callback#onSetProtocol(BluetoothDevice, byte)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback#onSetProtocol(android.bluetooth.BluetoothDevice,%20kotlin.Byte)) 

### REPORT_TYPE_FEATURE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REPORT_TYPE_FEATURE: Byte
```

Constant representing HID Feature Report type. 

 Value: 3

**See Also**

- [android.bluetooth.BluetoothHidDevice.Callback#onGetReport(BluetoothDevice, byte, byte, int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback#onGetReport(android.bluetooth.BluetoothDevice,%20kotlin.Byte,%20kotlin.Byte,%20kotlin.Int))
- [android.bluetooth.BluetoothHidDevice.Callback#onSetReport(BluetoothDevice, byte, byte, byte[])](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback#onSetReport(android.bluetooth.BluetoothDevice,%20kotlin.Byte,%20kotlin.Byte,%20kotlin.ByteArray))
- [android.bluetooth.BluetoothHidDevice.Callback#onInterruptData(BluetoothDevice, byte, byte[])](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback#onInterruptData(android.bluetooth.BluetoothDevice,%20kotlin.Byte,%20kotlin.ByteArray)) 

### REPORT_TYPE_INPUT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REPORT_TYPE_INPUT: Byte
```

Constant representing HID Input Report type. 

 Value: 1

**See Also**

- [android.bluetooth.BluetoothHidDevice.Callback#onGetReport(BluetoothDevice, byte, byte, int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback#onGetReport(android.bluetooth.BluetoothDevice,%20kotlin.Byte,%20kotlin.Byte,%20kotlin.Int))
- [android.bluetooth.BluetoothHidDevice.Callback#onSetReport(BluetoothDevice, byte, byte, byte[])](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback#onSetReport(android.bluetooth.BluetoothDevice,%20kotlin.Byte,%20kotlin.Byte,%20kotlin.ByteArray))
- [android.bluetooth.BluetoothHidDevice.Callback#onInterruptData(BluetoothDevice, byte, byte[])](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback#onInterruptData(android.bluetooth.BluetoothDevice,%20kotlin.Byte,%20kotlin.ByteArray)) 

### REPORT_TYPE_OUTPUT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REPORT_TYPE_OUTPUT: Byte
```

Constant representing HID Output Report type. 

 Value: 2

**See Also**

- [android.bluetooth.BluetoothHidDevice.Callback#onGetReport(BluetoothDevice, byte, byte, int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback#onGetReport(android.bluetooth.BluetoothDevice,%20kotlin.Byte,%20kotlin.Byte,%20kotlin.Int))
- [android.bluetooth.BluetoothHidDevice.Callback#onSetReport(BluetoothDevice, byte, byte, byte[])](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback#onSetReport(android.bluetooth.BluetoothDevice,%20kotlin.Byte,%20kotlin.Byte,%20kotlin.ByteArray))
- [android.bluetooth.BluetoothHidDevice.Callback#onInterruptData(BluetoothDevice, byte, byte[])](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback#onInterruptData(android.bluetooth.BluetoothDevice,%20kotlin.Byte,%20kotlin.ByteArray)) 

### SUBCLASS1_COMBO

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBCLASS1_COMBO: Byte
```

Constant representing combo keyboard and mouse subclass. 

 Value: -64

**See Also**

- [#registerApp](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#registerApp(android.bluetooth.BluetoothHidDeviceAppSdpSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20java.util.concurrent.Executor,%20android.bluetooth.BluetoothHidDevice.Callback)) 

### SUBCLASS1_KEYBOARD

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBCLASS1_KEYBOARD: Byte
```

Constant representing keyboard subclass. 

 Value: 64

**See Also**

- [#registerApp](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#registerApp(android.bluetooth.BluetoothHidDeviceAppSdpSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20java.util.concurrent.Executor,%20android.bluetooth.BluetoothHidDevice.Callback)) 

### SUBCLASS1_MOUSE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBCLASS1_MOUSE: Byte
```

Constant representing mouse subclass. 

 Value: -128

**See Also**

- [#registerApp](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#registerApp(android.bluetooth.BluetoothHidDeviceAppSdpSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20java.util.concurrent.Executor,%20android.bluetooth.BluetoothHidDevice.Callback)) 

### SUBCLASS1_NONE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBCLASS1_NONE: Byte
```

Constant representing unspecified HID device subclass. 

 Value: 0

**See Also**

- [#registerApp](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#registerApp(android.bluetooth.BluetoothHidDeviceAppSdpSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20java.util.concurrent.Executor,%20android.bluetooth.BluetoothHidDevice.Callback)) 

### SUBCLASS2_CARD_READER

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBCLASS2_CARD_READER: Byte
```

Constant representing card reader subclass. 

 Value: 6

**See Also**

- [#registerApp](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#registerApp(android.bluetooth.BluetoothHidDeviceAppSdpSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20java.util.concurrent.Executor,%20android.bluetooth.BluetoothHidDevice.Callback)) 

### SUBCLASS2_DIGITIZER_TABLET

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBCLASS2_DIGITIZER_TABLET: Byte
```

Constant representing digitizer tablet subclass. 

 Value: 5

**See Also**

- [#registerApp](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#registerApp(android.bluetooth.BluetoothHidDeviceAppSdpSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20java.util.concurrent.Executor,%20android.bluetooth.BluetoothHidDevice.Callback)) 

### SUBCLASS2_GAMEPAD

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBCLASS2_GAMEPAD: Byte
```

Constant representing gamepad subclass. 

 Value: 2

**See Also**

- [#registerApp](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#registerApp(android.bluetooth.BluetoothHidDeviceAppSdpSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20java.util.concurrent.Executor,%20android.bluetooth.BluetoothHidDevice.Callback)) 

### SUBCLASS2_JOYSTICK

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBCLASS2_JOYSTICK: Byte
```

Constant representing joystick subclass. 

 Value: 1

**See Also**

- [#registerApp](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#registerApp(android.bluetooth.BluetoothHidDeviceAppSdpSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20java.util.concurrent.Executor,%20android.bluetooth.BluetoothHidDevice.Callback)) 

### SUBCLASS2_REMOTE_CONTROL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBCLASS2_REMOTE_CONTROL: Byte
```

Constant representing remote control subclass. 

 Value: 3

**See Also**

- [#registerApp](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#registerApp(android.bluetooth.BluetoothHidDeviceAppSdpSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20java.util.concurrent.Executor,%20android.bluetooth.BluetoothHidDevice.Callback)) 

### SUBCLASS2_SENSING_DEVICE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBCLASS2_SENSING_DEVICE: Byte
```

Constant representing sensing device subclass. 

 Value: 4

**See Also**

- [#registerApp](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#registerApp(android.bluetooth.BluetoothHidDeviceAppSdpSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20java.util.concurrent.Executor,%20android.bluetooth.BluetoothHidDevice.Callback)) 

### SUBCLASS2_UNCATEGORIZED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBCLASS2_UNCATEGORIZED: Byte
```

Constant representing uncategorized HID device subclass. 

 Value: 0

**See Also**

- [#registerApp](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#registerApp(android.bluetooth.BluetoothHidDeviceAppSdpSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20java.util.concurrent.Executor,%20android.bluetooth.BluetoothHidDevice.Callback))

## Public methods

### connect

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun connect(device: BluetoothDevice!): Boolean
```

Initiates connection to host which is currently paired with this device. If the application is not registered, #connect(BluetoothDevice) will fail. The connection state should be tracked by the application by handling callback from Callback#onConnectionStateChanged. The connection state is not related to the return value of this method. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the command is successfully sent; otherwise false. |

### disconnect

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun disconnect(device: BluetoothDevice!): Boolean
```

Disconnects from currently connected host. The connection state should be tracked by the application by handling callback from Callback#onConnectionStateChanged. The connection state is not related to the return value of this method. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the command is successfully sent; otherwise false. |

### getConnectedDevices

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnectedDevices(): MutableList<BluetoothDevice!>!
```

Get connected devices for this specific profile.

Return the set of devices which are in state [STATE_CONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int) 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!>! | List of devices. The list will be empty on error. |

### getConnectionState

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnectionState(device: BluetoothDevice!): Int
```

Get the current connection state of the profile 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!:Remote bluetooth device. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | State of the profile connection. One of [STATE_CONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int), [STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int), [STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int), [STATE_DISCONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int) Value is [android.bluetooth.BluetoothProfile#STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int), [android.bluetooth.BluetoothProfile#STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int), [android.bluetooth.BluetoothProfile#STATE_CONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int), or [android.bluetooth.BluetoothProfile#STATE_DISCONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int) |

### getDevicesMatchingConnectionStates

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDevicesMatchingConnectionStates(states: IntArray!): MutableList<BluetoothDevice!>!
```

Get a list of devices that match any of the given connection states.

If none of the devices match any of the given states, an empty list will be returned. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `states` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:Array of states. States can be one of [STATE_CONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int), [STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int), [STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int), [STATE_DISCONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int), |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!>! | List of devices. The list will be empty on error. |

### registerApp

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerApp(
    sdp: BluetoothHidDeviceAppSdpSettings!, 
    inQos: BluetoothHidDeviceAppQosSettings!, 
    outQos: BluetoothHidDeviceAppQosSettings!, 
    executor: Executor!, 
    callback: BluetoothHidDevice.Callback!
): Boolean
```

Registers application to be used for HID device. Connections to HID Device are only possible when application is registered. Only one application can be registered at one time. When an application is registered, the HID Host service will be disabled until it is unregistered. When no longer used, application should be unregistered using [unregisterApp()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#unregisterApp()). The app will be automatically unregistered if it is not foreground. The registration status should be tracked by the application by handling callback from Callback#onAppStatusChanged. The app registration status is not related to the return value of this method. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sdp` | [BluetoothHidDeviceAppSdpSettings](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppSdpSettings)!: [BluetoothHidDeviceAppSdpSettings](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppSdpSettings) object of HID Device SDP record. The HID Device SDP record is required. |
| `inQos` | [BluetoothHidDeviceAppQosSettings](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppQosSettings)!: [BluetoothHidDeviceAppQosSettings](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppQosSettings) object of Incoming QoS Settings. The Incoming QoS Settings is not required. Use null or default BluetoothHidDeviceAppQosSettings.Builder for default values. |
| `outQos` | [BluetoothHidDeviceAppQosSettings](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppQosSettings)!: [BluetoothHidDeviceAppQosSettings](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppQosSettings) object of Outgoing QoS Settings. The Outgoing QoS Settings is not required. Use null or default BluetoothHidDeviceAppQosSettings.Builder for default values. |
| --- | --- |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)!: [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) object on which callback will be executed. The Executor object is required. |
| `callback` | [BluetoothHidDevice.Callback](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback)!: [Callback](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback) object to which callback messages will be sent. The Callback object is required. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the command is successfully sent; otherwise false. |

### replyReport

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun replyReport(
    device: BluetoothDevice!, 
    type: Byte, 
    id: Byte, 
    data: ByteArray!
): Boolean
```

Sends report to remote host as reply for GET_REPORT request from [android.bluetooth.BluetoothHidDevice.Callback#onGetReport(android.bluetooth.BluetoothDevice,byte,byte,int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback#onGetReport(android.bluetooth.BluetoothDevice,%20kotlin.Byte,%20kotlin.Byte,%20kotlin.Int)). 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):Report Type, as in request. |
| `id` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):Report Id, as in request. |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:Report data, not including Report Id. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the command is successfully sent; otherwise false. |

### reportError

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun reportError(
    device: BluetoothDevice!, 
    error: Byte
): Boolean
```

Sends error handshake message as reply for invalid SET_REPORT request from[android.bluetooth.BluetoothHidDevice.Callback#onSetReport(android.bluetooth.BluetoothDevice,byte,byte,byte[])](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback#onSetReport(android.bluetooth.BluetoothDevice,%20kotlin.Byte,%20kotlin.Byte,%20kotlin.ByteArray)). 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------|
| `error` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):Error to be sent for SET_REPORT via HANDSHAKE. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the command is successfully sent; otherwise false. |

### sendReport

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sendReport(
    device: BluetoothDevice!, 
    id: Int, 
    data: ByteArray!
): Boolean
```

Sends report to remote host using interrupt channel. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Report Id, as defined in descriptor. Can be 0 in case Report Id are not defined in descriptor. |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:Report data, not including Report Id. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the command is successfully sent; otherwise false. |

### unregisterApp

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterApp(): Boolean
```

Unregisters application. Active connection will be disconnected and no new connections will be allowed until registered again using [(android.bluetooth.BluetoothHidDeviceAppQosSettings,android.bluetooth.BluetoothHidDeviceAppQosSettings,android.bluetooth.BluetoothHidDeviceAppQosSettings,java.util.concurrent.Executor,android.bluetooth.BluetoothHidDevice.Callback)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice#registerApp(android.bluetooth.BluetoothHidDeviceAppSdpSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20android.bluetooth.BluetoothHidDeviceAppQosSettings,%20java.util.concurrent.Executor,%20android.bluetooth.BluetoothHidDevice.Callback)). The registration status should be tracked by the application by handling callback from Callback#onAppStatusChanged. The app registration status is not related to the return value of this method. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the command is successfully sent; otherwise false. |
