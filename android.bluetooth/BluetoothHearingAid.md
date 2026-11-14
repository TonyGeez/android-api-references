Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothHearingAid

```
class BluetoothHearingAid : BluetoothProfile
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothHearingAid](BluetoothHearingAid.md) |

This class provides the public APIs to control the Hearing Aid profile.

BluetoothHearingAid is a proxy object for controlling the Bluetooth Hearing Aid Service via IPC. Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getProfileProxy(android.content.Context,%20android.bluetooth.BluetoothProfile.ServiceListener,%20kotlin.Int)` to get the BluetoothHearingAid proxy object.

Android only supports one set of connected Bluetooth Hearing Aid device at a time. Each method is protected with its appropriate permission.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHearingAid#ACTION_CONNECTION_STATE_CHANGED:kotlin.String` Intent used to broadcast the change in connection state of the Hearing Aid profile. |

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
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](BluetoothDevice.md)!\> | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHearingAid#getConnectedDevices()()` Get connected devices for this specific profile. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHearingAid#getConnectionState(android.bluetooth.BluetoothDevice)(device: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)` Get the current connection state of the profile For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](BluetoothDevice.md)!\> | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHearingAid#getDevicesMatchingConnectionStates(kotlin.IntArray)(states: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)` Get a list of devices that match any of the given connection states. |
| --- | --- |

## Constants

### ACTION_CONNECTION_STATE_CHANGED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CONNECTION_STATE_CHANGED: String
```

Intent used to broadcast the change in connection state of the Hearing Aid profile. Please note that in the binaural case, there will be two different LE devices for the left and right side and each device will have their own connection state changes.

This intent will have the following extras:

- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_STATE:kotlin.String` - The current state of the profile.
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_PREVIOUS_STATE:kotlin.String`- The previous state of the profile.
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DEVICE:kotlin.String` - The remote device.
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_CLASS:kotlin.String` - The class of the remote device, if available, when the new state is `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int`.
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_LE_APPEARANCE:kotlin.String` - The LE appearance of the remote device, if available, when the new state is `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int`.

`https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_PREVIOUS_STATE:kotlin.String` can be any of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int`. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

 Value: "android.bluetooth.hearingaid.profile.action.CONNECTION_STATE_CHANGED"

## Public methods

### getConnectedDevices

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConnectedDevices(): MutableList<BluetoothDevice!>
```

Get connected devices for this specific profile.

Return the set of devices which are in state `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int` 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!>` | This value cannot be `null`. |

### getConnectionState

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConnectionState(device: BluetoothDevice): Int
```

Get the current connection state of the profile 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `device` | [BluetoothDevice](BluetoothDevice.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int` |

### getDevicesMatchingConnectionStates

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDevicesMatchingConnectionStates(states: IntArray): MutableList<BluetoothDevice!>
```

Get a list of devices that match any of the given connection states.

If none of the devices match any of the given states, an empty list will be returned. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `states` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!>` | This value cannot be `null`. |
