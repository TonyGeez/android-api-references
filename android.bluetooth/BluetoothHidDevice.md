# BluetoothHidDevice

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothHidDevice

Kotlin| [Java](../android/bluetooth/BluetoothHidDevice.md) 
| --- | --- |

```
class BluetoothHidDevice : BluetoothProfile
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothHidDevice](../android/bluetooth/BluetoothHidDevice.md) |

Provides the public APIs to control the Bluetooth HID Device profile.

BluetoothHidDevice is a proxy object for controlling the Bluetooth HID Device Service via IPC. Use [BluetoothAdapter.getProfileProxy](../android/bluetooth/BluetoothAdapter.md))to get the BluetoothHidDevice proxy object.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Callback](../android/bluetooth/BluetoothHidDevice.Callback.md) The template class that applications use to call callback functions on events from the HID host. |

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_CONNECTION_STATE_CHANGED](../android/bluetooth/BluetoothHidDevice.md) Intent used to broadcast the change in connection state of the Input Host profile. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [ERROR_RSP_INVALID_PARAM](../android/bluetooth/BluetoothHidDevice.md) Constant representing error response for Set Report due to "invalid parameter". |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [ERROR_RSP_INVALID_RPT_ID](../android/bluetooth/BluetoothHidDevice.md) Constant representing error response for Set Report due to "invalid report ID". |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [ERROR_RSP_NOT_READY](../android/bluetooth/BluetoothHidDevice.md) Constant representing error response for Set Report due to "not ready". |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [ERROR_RSP_SUCCESS](../android/bluetooth/BluetoothHidDevice.md) Constant representing success response for Set Report. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [ERROR_RSP_UNKNOWN](../android/bluetooth/BluetoothHidDevice.md) Constant representing error response for Set Report with unknown reason. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [ERROR_RSP_UNSUPPORTED_REQ](../android/bluetooth/BluetoothHidDevice.md) Constant representing error response for Set Report due to "unsupported request". |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [PROTOCOL_BOOT_MODE](../android/bluetooth/BluetoothHidDevice.md) Constant representing boot protocol mode used set by host. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [PROTOCOL_REPORT_MODE](../android/bluetooth/BluetoothHidDevice.md) Constant representing report protocol mode used set by host. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [REPORT_TYPE_FEATURE](../android/bluetooth/BluetoothHidDevice.md) Constant representing HID Feature Report type. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [REPORT_TYPE_INPUT](../android/bluetooth/BluetoothHidDevice.md) Constant representing HID Input Report type. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [REPORT_TYPE_OUTPUT](../android/bluetooth/BluetoothHidDevice.md) Constant representing HID Output Report type. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SUBCLASS1_COMBO](../android/bluetooth/BluetoothHidDevice.md) Constant representing combo keyboard and mouse subclass. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SUBCLASS1_KEYBOARD](../android/bluetooth/BluetoothHidDevice.md) Constant representing keyboard subclass. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SUBCLASS1_MOUSE](../android/bluetooth/BluetoothHidDevice.md) Constant representing mouse subclass. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SUBCLASS1_NONE](../android/bluetooth/BluetoothHidDevice.md) Constant representing unspecified HID device subclass. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SUBCLASS2_CARD_READER](../android/bluetooth/BluetoothHidDevice.md) Constant representing card reader subclass. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SUBCLASS2_DIGITIZER_TABLET](../android/bluetooth/BluetoothHidDevice.md) Constant representing digitizer tablet subclass. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SUBCLASS2_GAMEPAD](../android/bluetooth/BluetoothHidDevice.md) Constant representing gamepad subclass. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SUBCLASS2_JOYSTICK](../android/bluetooth/BluetoothHidDevice.md) Constant representing joystick subclass. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SUBCLASS2_REMOTE_CONTROL](../android/bluetooth/BluetoothHidDevice.md) Constant representing remote control subclass. |
| --- | --- |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SUBCLASS2_SENSING_DEVICE](../android/bluetooth/BluetoothHidDevice.md) Constant representing sensing device subclass. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SUBCLASS2_UNCATEGORIZED](../android/bluetooth/BluetoothHidDevice.md) Constant representing uncategorized HID device subclass. |

| Inherited constants ||
|---|---|
| From class [BluetoothProfile](../android/bluetooth/BluetoothProfile.md) |----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [A2DP](../android/bluetooth/BluetoothProfile.md) <br /> Advanced Audio Distribution Profile (A2DP) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CSIP_SET_COORDINATOR](../android/bluetooth/BluetoothProfile.md) <br /> Coordinated Set Identification Profile (CSIP) set coordinator <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PREVIOUS_STATE](../android/bluetooth/BluetoothProfile.md) <br /> Extra for the connection state intents of the individual profiles. This extra represents the previous connection state of the profile of the Bluetooth device. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PROFILE](../android/bluetooth/BluetoothProfile.md) <br /> Extra for the [BluetoothProfile](../android/bluetooth/BluetoothProfile.md) that the intent applies to. This extra represents the Bluetooth profile that the intent applies to. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_STATE](../android/bluetooth/BluetoothProfile.md) <br /> Extra for the connection state intents of the individual profiles. This extra represents the current connection state of the profile of the Bluetooth device. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GATT](../android/bluetooth/BluetoothProfile.md) <br /> Generic Attribute Profile (GATT) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GATT_SERVER](../android/bluetooth/BluetoothProfile.md) <br /> Generic Attribute Profile (GATT) Server <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HAP_CLIENT](../android/bluetooth/BluetoothProfile.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEADSET](../android/bluetooth/BluetoothProfile.md) <br /> Headset and Handsfree profile <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEALTH](../android/bluetooth/BluetoothProfile.md) <br /> Health Profile <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEARING_AID](../android/bluetooth/BluetoothProfile.md) <br /> Hearing Aid Device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HID_DEVICE](../android/bluetooth/BluetoothProfile.md) <br /> Human Interface Device (HID) Device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LE_AUDIO](../android/bluetooth/BluetoothProfile.md) <br /> LE Audio Device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAP](../android/bluetooth/BluetoothProfile.md) <br /> SIM Access Profile (SAP) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CONNECTED](../android/bluetooth/BluetoothProfile.md) <br /> The profile is in connected state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CONNECTING](../android/bluetooth/BluetoothProfile.md) <br /> The profile is in connecting state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISCONNECTED](../android/bluetooth/BluetoothProfile.md) <br /> The profile is in disconnected state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISCONNECTING](../android/bluetooth/BluetoothProfile.md) <br /> The profile is in disconnecting state <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [connect](../android/bluetooth/BluetoothHidDevice.md))`(`device:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!`)` Initiates connection to host which is currently paired with this device. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [disconnect](../android/bluetooth/BluetoothHidDevice.md))`(`device:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!`)` Disconnects from currently connected host. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!\>! | [getConnectedDevices](../android/bluetooth/BluetoothHidDevice.md))`()` Get connected devices for this specific profile. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConnectionState](../android/bluetooth/BluetoothHidDevice.md))`(`device:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!`)` Get the current connection state of the profile For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!\>! | [getDevicesMatchingConnectionStates](../android/bluetooth/BluetoothHidDevice.md))`(`states:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Get a list of devices that match any of the given connection states. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerApp](../android/bluetooth/BluetoothHidDevice.md))`(`sdp:` ` [BluetoothHidDeviceAppSdpSettings](../android/bluetooth/BluetoothHidDeviceAppSdpSettings.md)!`, `inQos:` ` [BluetoothHidDeviceAppQosSettings](../android/bluetooth/BluetoothHidDeviceAppQosSettings.md)!`, `outQos:` ` [BluetoothHidDeviceAppQosSettings](../android/bluetooth/BluetoothHidDeviceAppQosSettings.md)!`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)!`, `callback:` ` [BluetoothHidDevice.Callback](../android/bluetooth/BluetoothHidDevice.Callback.md)!`)` Registers application to be used for HID device. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [replyReport](../android/bluetooth/BluetoothHidDevice.md))`(`device:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!`, `type:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`, `id:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Sends report to remote host as reply for GET_REPORT request from [android.bluetooth.BluetoothHidDevice.Callback#onGetReport(android.bluetooth.BluetoothDevice,byte,byte,int)](../android/bluetooth/BluetoothHidDevice.Callback.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [reportError](../android/bluetooth/BluetoothHidDevice.md))`(`device:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!`, `error:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Sends error handshake message as reply for invalid SET_REPORT request from[android.bluetooth.BluetoothHidDevice.Callback#onSetReport(android.bluetooth.BluetoothDevice,byte,byte,byte[])](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice.Callback#onSetReport(android.bluetooth.BluetoothDevice,%20kotlin.Byte,%20kotlin.Byte,%20kotlin.ByteArray)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [sendReport](../android/bluetooth/BluetoothHidDevice.md))`(`device:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!`, `id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Sends report to remote host using interrupt channel. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [unregisterApp](../android/bluetooth/BluetoothHidDevice.md))`()` Unregisters application. |

## Constants

### ACTION_CONNECTION_STATE_CHANGED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_CONNECTION_STATE_CHANGED: String
```

Intent used to broadcast the change in connection state of the Input Host profile.

This intent will have 3 extras:

- [EXTRA_STATE](../android/bluetooth/BluetoothProfile.md)- The current state of the profile.
- [EXTRA_PREVIOUS_STATE](../android/bluetooth/BluetoothProfile.md)- The previous state of the profile.
- [BluetoothDevice.EXTRA_DEVICE](../android/bluetooth/BluetoothDevice.md)- The remote device.

[EXTRA_STATE](../android/bluetooth/BluetoothProfile.md) or [EXTRA_PREVIOUS_STATE](../android/bluetooth/BluetoothProfile.md) can be any of [STATE_DISCONNECTED](../android/bluetooth/BluetoothProfile.md), [STATE_CONNECTING](../android/bluetooth/BluetoothProfile.md), [STATE_CONNECTED](../android/bluetooth/BluetoothProfile.md), [STATE_DISCONNECTING](../android/bluetooth/BluetoothProfile.md). 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH](../android/Manifest.permission.md) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md) 

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

Constant representing boot protocol mode used set by host. Default is always [PROTOCOL_REPORT_MODE](../android/bluetooth/BluetoothHidDevice.md) unless notified otherwise. 

 Value: 0

**See Also**

- [android.bluetooth.BluetoothHidDevice.Callback#onSetProtocol(BluetoothDevice, byte)](../android/bluetooth/BluetoothHidDevice.Callback.md)) 

### PROTOCOL_REPORT_MODE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROTOCOL_REPORT_MODE: Byte
```

Constant representing report protocol mode used set by host. Default is always [PROTOCOL_REPORT_MODE](../android/bluetooth/BluetoothHidDevice.md) unless notified otherwise. 

 Value: 1

**See Also**

- [android.bluetooth.BluetoothHidDevice.Callback#onSetProtocol(BluetoothDevice, byte)](../android/bluetooth/BluetoothHidDevice.Callback.md)) 

### REPORT_TYPE_FEATURE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REPORT_TYPE_FEATURE: Byte
```

Constant representing HID Feature Report type. 

 Value: 3

**See Also**

- [android.bluetooth.BluetoothHidDevice.Callback#onGetReport(BluetoothDevice, byte, byte, int)](../android/bluetooth/BluetoothHidDevice.Callback.md))
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

- [android.bluetooth.BluetoothHidDevice.Callback#onGetReport(BluetoothDevice, byte, byte, int)](../android/bluetooth/BluetoothHidDevice.Callback.md))
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

- [android.bluetooth.BluetoothHidDevice.Callback#onGetReport(BluetoothDevice, byte, byte, int)](../android/bluetooth/BluetoothHidDevice.Callback.md))
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

- [#registerApp](../android/bluetooth/BluetoothHidDevice.md)) 

### SUBCLASS1_KEYBOARD

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBCLASS1_KEYBOARD: Byte
```

Constant representing keyboard subclass. 

 Value: 64

**See Also**

- [#registerApp](../android/bluetooth/BluetoothHidDevice.md)) 

### SUBCLASS1_MOUSE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBCLASS1_MOUSE: Byte
```

Constant representing mouse subclass. 

 Value: -128

**See Also**

- [#registerApp](../android/bluetooth/BluetoothHidDevice.md)) 

### SUBCLASS1_NONE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBCLASS1_NONE: Byte
```

Constant representing unspecified HID device subclass. 

 Value: 0

**See Also**

- [#registerApp](../android/bluetooth/BluetoothHidDevice.md)) 

### SUBCLASS2_CARD_READER

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBCLASS2_CARD_READER: Byte
```

Constant representing card reader subclass. 

 Value: 6

**See Also**

- [#registerApp](../android/bluetooth/BluetoothHidDevice.md)) 

### SUBCLASS2_DIGITIZER_TABLET

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBCLASS2_DIGITIZER_TABLET: Byte
```

Constant representing digitizer tablet subclass. 

 Value: 5

**See Also**

- [#registerApp](../android/bluetooth/BluetoothHidDevice.md)) 

### SUBCLASS2_GAMEPAD

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBCLASS2_GAMEPAD: Byte
```

Constant representing gamepad subclass. 

 Value: 2

**See Also**

- [#registerApp](../android/bluetooth/BluetoothHidDevice.md)) 

### SUBCLASS2_JOYSTICK

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBCLASS2_JOYSTICK: Byte
```

Constant representing joystick subclass. 

 Value: 1

**See Also**

- [#registerApp](../android/bluetooth/BluetoothHidDevice.md)) 

### SUBCLASS2_REMOTE_CONTROL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBCLASS2_REMOTE_CONTROL: Byte
```

Constant representing remote control subclass. 

 Value: 3

**See Also**

- [#registerApp](../android/bluetooth/BluetoothHidDevice.md)) 

### SUBCLASS2_SENSING_DEVICE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBCLASS2_SENSING_DEVICE: Byte
```

Constant representing sensing device subclass. 

 Value: 4

**See Also**

- [#registerApp](../android/bluetooth/BluetoothHidDevice.md)) 

### SUBCLASS2_UNCATEGORIZED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBCLASS2_UNCATEGORIZED: Byte
```

Constant representing uncategorized HID device subclass. 

 Value: 0

**See Also**

- [#registerApp](../android/bluetooth/BluetoothHidDevice.md))

## Public methods

### connect

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun connect(device: BluetoothDevice!): Boolean
```

Initiates connection to host which is currently paired with this device. If the application is not registered, #connect(BluetoothDevice) will fail. The connection state should be tracked by the application by handling callback from Callback#onConnectionStateChanged. The connection state is not related to the return value of this method. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the command is successfully sent; otherwise false. |

### disconnect

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun disconnect(device: BluetoothDevice!): Boolean
```

Disconnects from currently connected host. The connection state should be tracked by the application by handling callback from Callback#onConnectionStateChanged. The connection state is not related to the return value of this method. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the command is successfully sent; otherwise false. |

### getConnectedDevices

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnectedDevices(): MutableList<BluetoothDevice!>!
```

Get connected devices for this specific profile.

Return the set of devices which are in state [STATE_CONNECTED](../android/bluetooth/BluetoothProfile.md) 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!>! | List of devices. The list will be empty on error. |

### getConnectionState

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnectionState(device: BluetoothDevice!): Int
```

Get the current connection state of the profile 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!:Remote bluetooth device. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | State of the profile connection. One of [STATE_CONNECTED](../android/bluetooth/BluetoothProfile.md), [STATE_CONNECTING](../android/bluetooth/BluetoothProfile.md), [STATE_DISCONNECTED](../android/bluetooth/BluetoothProfile.md), [STATE_DISCONNECTING](../android/bluetooth/BluetoothProfile.md) Value is [android.bluetooth.BluetoothProfile#STATE_DISCONNECTED](../android/bluetooth/BluetoothProfile.md), [android.bluetooth.BluetoothProfile#STATE_CONNECTING](../android/bluetooth/BluetoothProfile.md), [android.bluetooth.BluetoothProfile#STATE_CONNECTED](../android/bluetooth/BluetoothProfile.md), or [android.bluetooth.BluetoothProfile#STATE_DISCONNECTING](../android/bluetooth/BluetoothProfile.md) |

### getDevicesMatchingConnectionStates

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDevicesMatchingConnectionStates(states: IntArray!): MutableList<BluetoothDevice!>!
```

Get a list of devices that match any of the given connection states.

If none of the devices match any of the given states, an empty list will be returned. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `states` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:Array of states. States can be one of [STATE_CONNECTED](../android/bluetooth/BluetoothProfile.md), [STATE_CONNECTING](../android/bluetooth/BluetoothProfile.md), [STATE_DISCONNECTED](../android/bluetooth/BluetoothProfile.md), [STATE_DISCONNECTING](../android/bluetooth/BluetoothProfile.md), |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!>! | List of devices. The list will be empty on error. |

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

Registers application to be used for HID device. Connections to HID Device are only possible when application is registered. Only one application can be registered at one time. When an application is registered, the HID Host service will be disabled until it is unregistered. When no longer used, application should be unregistered using [unregisterApp()](../android/bluetooth/BluetoothHidDevice.md)). The app will be automatically unregistered if it is not foreground. The registration status should be tracked by the application by handling callback from Callback#onAppStatusChanged. The app registration status is not related to the return value of this method. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sdp` | [BluetoothHidDeviceAppSdpSettings](../android/bluetooth/BluetoothHidDeviceAppSdpSettings.md)!: [BluetoothHidDeviceAppSdpSettings](../android/bluetooth/BluetoothHidDeviceAppSdpSettings.md) object of HID Device SDP record. The HID Device SDP record is required. |
| `inQos` | [BluetoothHidDeviceAppQosSettings](../android/bluetooth/BluetoothHidDeviceAppQosSettings.md)!: [BluetoothHidDeviceAppQosSettings](../android/bluetooth/BluetoothHidDeviceAppQosSettings.md) object of Incoming QoS Settings. The Incoming QoS Settings is not required. Use null or default BluetoothHidDeviceAppQosSettings.Builder for default values. |
| `outQos` | [BluetoothHidDeviceAppQosSettings](../android/bluetooth/BluetoothHidDeviceAppQosSettings.md)!: [BluetoothHidDeviceAppQosSettings](../android/bluetooth/BluetoothHidDeviceAppQosSettings.md) object of Outgoing QoS Settings. The Outgoing QoS Settings is not required. Use null or default BluetoothHidDeviceAppQosSettings.Builder for default values. |
| --- | --- |
| `executor` | [Executor](../java/util/concurrent/Executor.md)!: [Executor](../java/util/concurrent/Executor.md) object on which callback will be executed. The Executor object is required. |
| `callback` | [BluetoothHidDevice.Callback](../android/bluetooth/BluetoothHidDevice.Callback.md)!: [Callback](../android/bluetooth/BluetoothHidDevice.Callback.md) object to which callback messages will be sent. The Callback object is required. |

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

Sends report to remote host as reply for GET_REPORT request from [android.bluetooth.BluetoothHidDevice.Callback#onGetReport(android.bluetooth.BluetoothDevice,byte,byte,int)](../android/bluetooth/BluetoothHidDevice.Callback.md)). 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

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
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

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
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

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

Unregisters application. Active connection will be disconnected and no new connections will be allowed until registered again using [(android.bluetooth.BluetoothHidDeviceAppQosSettings,android.bluetooth.BluetoothHidDeviceAppQosSettings,android.bluetooth.BluetoothHidDeviceAppQosSettings,java.util.concurrent.Executor,android.bluetooth.BluetoothHidDevice.Callback)](../android/bluetooth/BluetoothHidDevice.md)). The registration status should be tracked by the application by handling callback from Callback#onAppStatusChanged. The app registration status is not related to the return value of this method. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the command is successfully sent; otherwise false. |
