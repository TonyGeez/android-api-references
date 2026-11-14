# BluetoothGattServer

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothGattServer

Kotlin| [Java](https://developer.android.com/reference/android/bluetooth/BluetoothGattServer "View this page in Java") 
| --- | --- |

```
class BluetoothGattServer : BluetoothProfile
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothGattServer](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#) |

Public API for the Bluetooth GATT Profile server role.

This class provides Bluetooth GATT server role functionality, allowing applications to create Bluetooth Smart services and characteristics.

BluetoothGattServer is a proxy object for controlling the Bluetooth Service via IPC. Use [BluetoothManager.openGattServer](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager#openGattServer(android.content.Context,%20android.bluetooth.BluetoothGattServerCallback))to get an instance of this class.

## Summary

| Inherited constants ||
|---|---|
| From class [BluetoothProfile](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile) |----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [A2DP](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#A2DP:kotlin.Int) <br /> Advanced Audio Distribution Profile (A2DP) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CSIP_SET_COORDINATOR](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#CSIP_SET_COORDINATOR:kotlin.Int) <br /> Coordinated Set Identification Profile (CSIP) set coordinator <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PREVIOUS_STATE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_PREVIOUS_STATE:kotlin.String) <br /> Extra for the connection state intents of the individual profiles. This extra represents the previous connection state of the profile of the Bluetooth device. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PROFILE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_PROFILE:kotlin.String) <br /> Extra for the [BluetoothProfile](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile) that the intent applies to. This extra represents the Bluetooth profile that the intent applies to. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_STATE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_STATE:kotlin.String) <br /> Extra for the connection state intents of the individual profiles. This extra represents the current connection state of the profile of the Bluetooth device. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GATT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#GATT:kotlin.Int) <br /> Generic Attribute Profile (GATT) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GATT_SERVER](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#GATT_SERVER:kotlin.Int) <br /> Generic Attribute Profile (GATT) Server <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HAP_CLIENT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HAP_CLIENT:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEADSET](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HEADSET:kotlin.Int) <br /> Headset and Handsfree profile <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEALTH](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HEALTH:kotlin.Int) <br /> Health Profile <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEARING_AID](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HEARING_AID:kotlin.Int) <br /> Hearing Aid Device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HID_DEVICE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HID_DEVICE:kotlin.Int) <br /> Human Interface Device (HID) Device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LE_AUDIO](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#LE_AUDIO:kotlin.Int) <br /> LE Audio Device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAP](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#SAP:kotlin.Int) <br /> SIM Access Profile (SAP) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int) <br /> The profile is in connected state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int) <br /> The profile is in connecting state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int) <br /> The profile is in disconnected state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISCONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int) <br /> The profile is in disconnecting state <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#addService(android.bluetooth.BluetoothGattService))`(`service:` ` [BluetoothGattService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService)!`)` Add a service to the list of services to be hosted. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancelConnection](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#cancelConnection(android.bluetooth.BluetoothDevice))`(`device:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!`)` Disconnects an established connection, or cancels a connection attempt currently in progress. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearServices](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#clearServices())`()` Remove all services from the list of provided services. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#close())`()` Close this GATT server instance. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [connect](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#connect(android.bluetooth.BluetoothDevice,%20kotlin.Boolean))`(`device:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!`, `autoConnect:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Initiate a connection to a Bluetooth GATT capable device. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!\>! | [getConnectedDevices](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#getConnectedDevices())`()` Not supported - please use [BluetoothManager.getConnectedDevices(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager#getConnectedDevices(kotlin.Int))with [android.bluetooth.BluetoothProfile#GATT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#GATT:kotlin.Int) as argument |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConnectionState](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#getConnectionState(android.bluetooth.BluetoothDevice))`(`device:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!`)` Not supported - please use [BluetoothManager.getConnectedDevices(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager#getConnectedDevices(kotlin.Int))with [android.bluetooth.BluetoothProfile#GATT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#GATT:kotlin.Int) as argument |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!\>! | [getDevicesMatchingConnectionStates](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#getDevicesMatchingConnectionStates(kotlin.IntArray))`(`states:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Not supported - please use [BluetoothManager.getDevicesMatchingConnectionStates(int,](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager#getDevicesMatchingConnectionStates(kotlin.Int,%20kotlin.IntArray))with [BluetoothProfile.GATT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#GATT:kotlin.Int) as first argument |
| [BluetoothGattService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService)! | [getService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#getService(java.util.UUID))`(`uuid:` ` [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)!`)` Returns a [BluetoothGattService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService) from the list of services offered by this device. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothGattService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService)!\>! | [getServices](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#getServices())`()` Returns a list of GATT services offered by this device. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [notifyCharacteristicChanged](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#notifyCharacteristicChanged(android.bluetooth.BluetoothDevice,%20android.bluetooth.BluetoothGattCharacteristic,%20kotlin.Boolean))`(`device:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!`, `characteristic:` ` [BluetoothGattCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic)!`, `confirm:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Send a notification or indication that a local characteristic has been updated. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [notifyCharacteristicChanged](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#notifyCharacteristicChanged(android.bluetooth.BluetoothDevice,%20android.bluetooth.BluetoothGattCharacteristic,%20kotlin.Boolean,%20kotlin.ByteArray))`(`device:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)`, `characteristic:` ` [BluetoothGattCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic)`, `confirm:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `value:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Send a notification or indication that a local characteristic has been updated. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readPhy](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#readPhy(android.bluetooth.BluetoothDevice))`(`device:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!`)` Read the current transmitter PHY and receiver PHY of the connection. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#removeService(android.bluetooth.BluetoothGattService))`(`service:` ` [BluetoothGattService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService)!`)` Removes a service from the list of services to be provided. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [sendResponse](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#sendResponse(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.ByteArray))`(`device:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!`, `requestId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Send a response to a read or write request to a remote device. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreferredPhy](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#setPreferredPhy(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`device:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!`, `txPhy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `rxPhy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `phyOptions:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the preferred connection PHY for this app. |

## Public methods

### addService

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addService(service: BluetoothGattService!): Boolean
```

Add a service to the list of services to be hosted.

Once a service has been added to the list, the service and its included characteristics will be provided by the local device.

If the local device has already exposed services when this function is called, a service update notification will be sent to all clients.

The [BluetoothGattServerCallback.onServiceAdded](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback#onServiceAdded(kotlin.Int,%20android.bluetooth.BluetoothGattService))callback will indicate whether this service has been added successfully. Do not add another service before this callback. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `service` | [BluetoothGattService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService)!:Service to be added to the list of services provided by this device. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true, if the request to add service has been initiated |

### cancelConnection

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun cancelConnection(device: BluetoothDevice!): Unit
```

Disconnects an established connection, or cancels a connection attempt currently in progress. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!:Remote device |

### clearServices

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clearServices(): Unit
```

Remove all services from the list of provided services. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) 

### close

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

Close this GATT server instance.

Application should call this method as early as possible after it is done with this GATT server. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) 

### connect

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun connect(
    device: BluetoothDevice!, 
    autoConnect: Boolean
): Boolean
```

Initiate a connection to a Bluetooth GATT capable device.

The connection may not be established right away, but will be completed when the remote device is available. A [BluetoothGattServerCallback.onConnectionStateChange](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback#onConnectionStateChange(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int))callback will be invoked when the connection state changes as a result of this function.

The autoConnect parameter determines whether to actively connect to the remote device, or rather passively scan and finalize the connection when the remote device is in range/available. Generally, the first ever connection to a device should be direct (autoConnect set to false) and subsequent connections to known devices should be invoked with the autoConnect parameter set to true. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `autoConnect` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether to directly connect to the remote device (false) or to automatically connect as soon as the remote device becomes available (true). |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true, if the connection attempt was initiated successfully |

### getConnectedDevices

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnectedDevices(): MutableList<BluetoothDevice!>!
```

Not supported - please use [BluetoothManager.getConnectedDevices(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager#getConnectedDevices(kotlin.Int))with [android.bluetooth.BluetoothProfile#GATT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#GATT:kotlin.Int) as argument

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!>! | List of devices. The list will be empty on error. |

| Exceptions ||
|-------------------------------------------|---------------|
| `java.lang.UnsupportedOperationException` | on every call |

### getConnectionState

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnectionState(device: BluetoothDevice!): Int
```

Not supported - please use [BluetoothManager.getConnectedDevices(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager#getConnectedDevices(kotlin.Int))with [android.bluetooth.BluetoothProfile#GATT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#GATT:kotlin.Int) as argument

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!:Remote bluetooth device. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | State of the profile connection. One of [STATE_CONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int), [STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int), [STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int), [STATE_DISCONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int) Value is [android.bluetooth.BluetoothProfile#STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int), [android.bluetooth.BluetoothProfile#STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int), [android.bluetooth.BluetoothProfile#STATE_CONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int), or [android.bluetooth.BluetoothProfile#STATE_DISCONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int) |

| Exceptions ||
|-------------------------------------------|---------------|
| `java.lang.UnsupportedOperationException` | on every call |

### getDevicesMatchingConnectionStates

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDevicesMatchingConnectionStates(states: IntArray!): MutableList<BluetoothDevice!>!
```

Not supported - please use [BluetoothManager.getDevicesMatchingConnectionStates(int,](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager#getDevicesMatchingConnectionStates(kotlin.Int,%20kotlin.IntArray))with [BluetoothProfile.GATT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#GATT:kotlin.Int) as first argument

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `states` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:Array of states. States can be one of [STATE_CONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int), [STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int), [STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int), [STATE_DISCONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int), |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!>! | List of devices. The list will be empty on error. |

| Exceptions ||
|-------------------------------------------|---------------|
| `java.lang.UnsupportedOperationException` | on every call |

### getService

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getService(uuid: UUID!): BluetoothGattService!
```

Returns a [BluetoothGattService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService) from the list of services offered by this device.

If multiple instances of the same service (as identified by UUID) exist, the first instance of the service is returned. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String) permission which can be gained with a simple`<uses-permission>`manifest tag.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `uuid` | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)!:UUID of the requested service |

| Return ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [BluetoothGattService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService)! | BluetoothGattService if supported, or null if the requested service is not offered by this device. |

### getServices

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServices(): MutableList<BluetoothGattService!>!
```

Returns a list of GATT services offered by this device.

An application must call [addService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#addService(android.bluetooth.BluetoothGattService))to add a service to the list of services offered by this device. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String) permission which can be gained with a simple`<uses-permission>`manifest tag.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothGattService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService)!>! | List of services. Returns an empty list if no services have been added yet. |

### notifyCharacteristicChanged

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun notifyCharacteristicChanged(
    device: BluetoothDevice!, 
    characteristic: BluetoothGattCharacteristic!, 
    confirm: Boolean
): Boolean
```

**Deprecated:** *Use [BluetoothGattServer.notifyCharacteristicChanged(BluetoothDevice,](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#notifyCharacteristicChanged(android.bluetooth.BluetoothDevice,%20android.bluetooth.BluetoothGattCharacteristic,%20kotlin.Boolean,%20kotlin.ByteArray))as this is not memory safe.*

Send a notification or indication that a local characteristic has been updated.

A notification or indication is sent to the remote device to signal that the characteristic has been updated. This function should be invoked for every client that requests notifications/indications by writing to the "Client Configuration" descriptor for the given characteristic. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!:The remote device to receive the notification/indication |
| `characteristic` | [BluetoothGattCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic)!:The local characteristic that has been updated |
| `confirm` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true to request confirmation from the client (indication), false to send a notification |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true, if the notification has been triggered successfully |

| Exceptions ||
|--------------------------------------|------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the characteristic value or service is null |

### notifyCharacteristicChanged

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun notifyCharacteristicChanged(
    device: BluetoothDevice, 
    characteristic: BluetoothGattCharacteristic, 
    confirm: Boolean, 
    value: ByteArray
): Int
```

Send a notification or indication that a local characteristic has been updated.

A notification or indication is sent to the remote device to signal that the characteristic has been updated. This function should be invoked for every client that requests notifications/indications by writing to the "Client Configuration" descriptor for the given characteristic. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice):the remote device to receive the notification/indication This value cannot be`null`. |
| `characteristic` | [BluetoothGattCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic):the local characteristic that has been updated This value cannot be`null`. |
| `confirm` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`to request confirmation from the client (indication) or`false`to send a notification |
| --- | --- |
| `value` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the characteristic value This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | whether the notification has been triggered successfully Value is [android.bluetooth.BluetoothStatusCodes#SUCCESS](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#SUCCESS:kotlin.Int), [android.bluetooth.BluetoothStatusCodes#ERROR_MISSING_BLUETOOTH_CONNECT_PERMISSION](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_MISSING_BLUETOOTH_CONNECT_PERMISSION:kotlin.Int), android.bluetooth.BluetoothStatusCodes.ERROR_DEVICE_NOT_CONNECTED, [android.bluetooth.BluetoothStatusCodes#ERROR_PROFILE_SERVICE_NOT_BOUND](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_PROFILE_SERVICE_NOT_BOUND:kotlin.Int), or [android.bluetooth.BluetoothStatusCodes#ERROR_UNKNOWN](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_UNKNOWN:kotlin.Int) |

| Exceptions ||
|--------------------------------------|------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the characteristic value or service is null |

### readPhy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readPhy(device: BluetoothDevice!): Unit
```

Read the current transmitter PHY and receiver PHY of the connection. The values are returned in [BluetoothGattServerCallback.onPhyRead](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback#onPhyRead(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)) 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!:The remote device to send this response to |

### removeService

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeService(service: BluetoothGattService!): Boolean
```

Removes a service from the list of services to be provided. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| `service` | [BluetoothGattService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService)!:Service to be removed. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true, if the service has been removed |

### sendResponse

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sendResponse(
    device: BluetoothDevice!, 
    requestId: Int, 
    status: Int, 
    offset: Int, 
    value: ByteArray!
): Boolean
```

Send a response to a read or write request to a remote device.

This function must be invoked in when a remote read/write request is received by one of these callback methods:

- [BluetoothGattServerCallback.onCharacteristicReadRequest](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback#onCharacteristicReadRequest(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int,%20android.bluetooth.BluetoothGattCharacteristic))
- [BluetoothGattServerCallback.onCharacteristicWriteRequest](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback#onCharacteristicWriteRequest(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20android.bluetooth.BluetoothGattCharacteristic,%20kotlin.Boolean,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.ByteArray))
- [BluetoothGattServerCallback.onDescriptorReadRequest](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback#onDescriptorReadRequest(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int,%20android.bluetooth.BluetoothGattDescriptor))
- [BluetoothGattServerCallback.onDescriptorWriteRequest](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback#onDescriptorWriteRequest(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20android.bluetooth.BluetoothGattDescriptor,%20kotlin.Boolean,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.ByteArray))

<br />

For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!:The remote device to send this response to |
| `requestId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The ID of the request that was received with the callback |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The status of the request to be sent to the remote devices |
| --- | --- |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value offset for partial read/write response |
| `value` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:The value of the attribute that was read/written (optional) |

### setPreferredPhy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPreferredPhy(
    device: BluetoothDevice!, 
    txPhy: Int, 
    rxPhy: Int, 
    phyOptions: Int
): Unit
```

Set the preferred connection PHY for this app. Please note that this is just a recommendation, whether the PHY change will happen depends on other applications preferences, local and remote controller capabilities. Controller can override these settings.

[BluetoothGattServerCallback.onPhyUpdate](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback#onPhyUpdate(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))will be triggered as a result of this call, even if no PHY change happens. It is also triggered when remote device updates the PHY. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!:The remote device to send this response to |
| `txPhy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):preferred transmitter PHY. Bitwise OR of any of [android.bluetooth.BluetoothDevice#PHY_LE_1M_MASK](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_1M_MASK:kotlin.Int), [BluetoothDevice.PHY_LE_2M_MASK](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_2M_MASK:kotlin.Int), and [android.bluetooth.BluetoothDevice#PHY_LE_CODED_MASK](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_CODED_MASK:kotlin.Int). |
| `rxPhy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):preferred receiver PHY. Bitwise OR of any of [android.bluetooth.BluetoothDevice#PHY_LE_1M_MASK](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_1M_MASK:kotlin.Int), [BluetoothDevice.PHY_LE_2M_MASK](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_2M_MASK:kotlin.Int), and [android.bluetooth.BluetoothDevice#PHY_LE_CODED_MASK](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_CODED_MASK:kotlin.Int). |
| --- | --- |
| `phyOptions` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):preferred coding to use when transmitting on the LE Coded PHY. Can be one of [BluetoothDevice.PHY_OPTION_NO_PREFERRED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_OPTION_NO_PREFERRED:kotlin.Int), [BluetoothDevice.PHY_OPTION_S2](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_OPTION_S2:kotlin.Int) or [BluetoothDevice.PHY_OPTION_S8](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_OPTION_S8:kotlin.Int) |
