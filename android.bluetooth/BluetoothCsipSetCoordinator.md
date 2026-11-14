# BluetoothCsipSetCoordinator

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothCsipSetCoordinator

Kotlin| [Java](BluetoothCsipSetCoordinator.md) 
| --- | --- |

```
class BluetoothCsipSetCoordinator : AutoCloseable, BluetoothProfile
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothCsipSetCoordinator](BluetoothCsipSetCoordinator.md) |

This class provides the public APIs to control the Bluetooth CSIP set coordinator.

BluetoothCsipSetCoordinator is a proxy object for controlling the Bluetooth CSIP set Service via IPC. Use [BluetoothAdapter.getProfileProxy](BluetoothAdapter.md))to get the BluetoothCsipSetCoordinator proxy object.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_CSIS_CONNECTION_STATE_CHANGED](BluetoothCsipSetCoordinator.md) Intent used to broadcast the change in connection state of the CSIS Client. |

| Inherited constants ||
|---|---|
| From class [BluetoothProfile](BluetoothProfile.md) |----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [A2DP](BluetoothProfile.md) <br /> Advanced Audio Distribution Profile (A2DP) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CSIP_SET_COORDINATOR](BluetoothProfile.md) <br /> Coordinated Set Identification Profile (CSIP) set coordinator <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PREVIOUS_STATE](BluetoothProfile.md) <br /> Extra for the connection state intents of the individual profiles. This extra represents the previous connection state of the profile of the Bluetooth device. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PROFILE](BluetoothProfile.md) <br /> Extra for the [BluetoothProfile](BluetoothProfile.md) that the intent applies to. This extra represents the Bluetooth profile that the intent applies to. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_STATE](BluetoothProfile.md) <br /> Extra for the connection state intents of the individual profiles. This extra represents the current connection state of the profile of the Bluetooth device. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GATT](BluetoothProfile.md) <br /> Generic Attribute Profile (GATT) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GATT_SERVER](BluetoothProfile.md) <br /> Generic Attribute Profile (GATT) Server <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HAP_CLIENT](BluetoothProfile.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEADSET](BluetoothProfile.md) <br /> Headset and Handsfree profile <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEALTH](BluetoothProfile.md) <br /> Health Profile <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEARING_AID](BluetoothProfile.md) <br /> Hearing Aid Device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HID_DEVICE](BluetoothProfile.md) <br /> Human Interface Device (HID) Device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LE_AUDIO](BluetoothProfile.md) <br /> LE Audio Device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAP](BluetoothProfile.md) <br /> SIM Access Profile (SAP) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CONNECTED](BluetoothProfile.md) <br /> The profile is in connected state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CONNECTING](BluetoothProfile.md) <br /> The profile is in connecting state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISCONNECTED](BluetoothProfile.md) <br /> The profile is in disconnected state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISCONNECTING](BluetoothProfile.md) <br /> The profile is in disconnecting state <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](BluetoothDevice.md)!\> | [getConnectedDevices](BluetoothCsipSetCoordinator.md))`()` Get connected devices for this specific profile. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConnectionState](BluetoothCsipSetCoordinator.md))`(`device:` ` [BluetoothDevice](BluetoothDevice.md)?`)` Get the current connection state of the profile For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](BluetoothDevice.md)!\> | [getDevicesMatchingConnectionStates](BluetoothCsipSetCoordinator.md))`(`states:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` Get a list of devices that match any of the given connection states. |
| --- | --- |

## Constants

### ACTION_CSIS_CONNECTION_STATE_CHANGED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_CSIS_CONNECTION_STATE_CHANGED: String
```

Intent used to broadcast the change in connection state of the CSIS Client.

This intent will have 3 extras:

- [EXTRA_STATE](BluetoothProfile.md)- The current state of the profile.
- [EXTRA_PREVIOUS_STATE](BluetoothProfile.md)- The previous state of the profile.
- [BluetoothDevice.EXTRA_DEVICE](BluetoothDevice.md)- The remote device.

[EXTRA_STATE](BluetoothProfile.md) or [EXTRA_PREVIOUS_STATE](BluetoothProfile.md) can be any of [STATE_DISCONNECTED](BluetoothProfile.md), [STATE_CONNECTING](BluetoothProfile.md), [STATE_CONNECTED](BluetoothProfile.md), [STATE_DISCONNECTING](BluetoothProfile.md). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md) 

 Value: "android.bluetooth.action.CSIS_CONNECTION_STATE_CHANGED"

## Public methods

### getConnectedDevices

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnectedDevices(): MutableList<BluetoothDevice!>
```

Get connected devices for this specific profile.

Return the set of devices which are in state [STATE_CONNECTED](BluetoothProfile.md) 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md) and [android.Manifest.permission#BLUETOOTH_PRIVILEGED](../android/Manifest.permission.md)

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothDevice](BluetoothDevice.md)!> | This value cannot be`null`. |

### getConnectionState

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnectionState(device: BluetoothDevice?): Int
```

Get the current connection state of the profile 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md) and [android.Manifest.permission#BLUETOOTH_PRIVILEGED](../android/Manifest.permission.md)

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](BluetoothDevice.md)?:This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.bluetooth.BluetoothProfile#STATE_DISCONNECTED](BluetoothProfile.md), [android.bluetooth.BluetoothProfile#STATE_CONNECTING](BluetoothProfile.md), [android.bluetooth.BluetoothProfile#STATE_CONNECTED](BluetoothProfile.md), or [android.bluetooth.BluetoothProfile#STATE_DISCONNECTING](BluetoothProfile.md) |

### getDevicesMatchingConnectionStates

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDevicesMatchingConnectionStates(states: IntArray): MutableList<BluetoothDevice!>
```

Get a list of devices that match any of the given connection states.

If none of the devices match any of the given states, an empty list will be returned. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md) and [android.Manifest.permission#BLUETOOTH_PRIVILEGED](../android/Manifest.permission.md)

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------|
| `states` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html):This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothDevice](BluetoothDevice.md)!> | This value cannot be`null`. |
