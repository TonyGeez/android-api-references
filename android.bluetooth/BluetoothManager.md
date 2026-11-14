Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothManager

Kotlin | [Java](https://developer.android.com/reference/android/bluetooth/BluetoothManager "View this page in Java")
| --- | --- |

```
class BluetoothManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothManager](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager#) |

High level manager used to obtain an instance of an `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter` and to conduct overall Bluetooth Management.

Use `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` with `https://developer.android.com/reference/kotlin/android/content/Context.html#BLUETOOTH_SERVICE:kotlin.String` to create an `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager#`, then call `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager#getAdapter()` to obtain the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter`.
|
| ### Developer Guides
|
| For more information about using BLUETOOTH, read the [Bluetooth](https://developer.android.com/guide/topics/connectivity/bluetooth.html) developer guide.
. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_BLUETOOTH:kotlin.String` feature which can be detected using `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)`.

## Summary

| Public methods ||
|---|---|
| [BluetoothAdapter](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager#getAdapter()()` Get the BluetoothAdapter for this device. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!\>! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager#getConnectedDevices(kotlin.Int)(profile: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get connected devices for the specified profile. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager#getConnectionState(android.bluetooth.BluetoothDevice,%20kotlin.Int)(device: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!, profile: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the current connection state of the profile to the remote device. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!\>! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager#getDevicesMatchingConnectionStates(kotlin.Int,%20kotlin.IntArray)(profile: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, states: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!)` Get a list of devices that match any of the given connection states. |
| [BluetoothGattServer](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager#openGattServer(android.content.Context,%20android.bluetooth.BluetoothGattServerCallback)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, callback: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback!)` Open a GATT Server The callback is used to deliver results to Caller, such as connection status as well as the results of any other GATT server operations. |

## Public methods

### getAdapter

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAdapter(): BluetoothAdapter!
```

Get the BluetoothAdapter for this device.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter!` | the BluetoothAdapter |

### getConnectedDevices

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConnectedDevices(profile: Int): MutableList<BluetoothDevice!>!
```

Get connected devices for the specified profile.

Return the set of devices which are in state `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int`

This is not specific to any application configuration but represents the connection state of Bluetooth for this profile. This can be used by applications like status bar which would just like to know the state of Bluetooth. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `profile` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): GATT or GATT_SERVER |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!>!` | List of devices. The list will be empty on error. |

### getConnectionState

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConnectionState(
    device: BluetoothDevice!, 
    profile: Int
): Int
```

Get the current connection state of the profile to the remote device.

This is not specific to any application configuration but represents the connection state of the local Bluetooth adapter for certain profile. This can be used by applications like status bar which would just like to know the state of Bluetooth. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `device` | [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!: Remote bluetooth device. |
| `profile` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): GATT or GATT_SERVER |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | State of the profile connection. One of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int` |

### getDevicesMatchingConnectionStates

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDevicesMatchingConnectionStates(
    profile: Int, 
    states: IntArray!
): MutableList<BluetoothDevice!>!
```

Get a list of devices that match any of the given connection states.

If none of the devices match any of the given states, an empty list will be returned.

This is not specific to any application configuration but represents the connection state of the local Bluetooth adapter for this profile. This can be used by applications like status bar which would just like to know the state of the local adapter. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `profile` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): GATT or GATT_SERVER |
| `states` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: Array of states. States can be one of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int`, |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!>!` | List of devices. The list will be empty on error. |

### openGattServer

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun openGattServer(
    context: Context!, 
    callback: BluetoothGattServerCallback!
): BluetoothGattServer!
```

Open a GATT Server The callback is used to deliver results to Caller, such as connection status as well as the results of any other GATT server operations. The method returns a BluetoothGattServer instance. You can use BluetoothGattServer to conduct GATT server operations. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: App context |
| `callback` | [BluetoothGattServerCallback](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback)!: GATT server callback handler that will receive asynchronous callbacks. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer!` | BluetoothGattServer instance |
