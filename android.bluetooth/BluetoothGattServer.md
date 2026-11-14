# BluetoothGattServer

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothGattServer

Kotlin| [Java](../android/bluetooth/BluetoothGattServer.md) 
| --- | --- |

```
class BluetoothGattServer : BluetoothProfile
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothGattServer](../android/bluetooth/BluetoothGattServer.md) |

Public API for the Bluetooth GATT Profile server role.

This class provides Bluetooth GATT server role functionality, allowing applications to create Bluetooth Smart services and characteristics.

BluetoothGattServer is a proxy object for controlling the Bluetooth Service via IPC. Use [BluetoothManager.openGattServer](../android/bluetooth/BluetoothManager.md))to get an instance of this class.

## Summary

| Inherited constants ||
|---|---|
| From class [BluetoothProfile](../android/bluetooth/BluetoothProfile.md) |----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [A2DP](../android/bluetooth/BluetoothProfile.md) <br /> Advanced Audio Distribution Profile (A2DP) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CSIP_SET_COORDINATOR](../android/bluetooth/BluetoothProfile.md) <br /> Coordinated Set Identification Profile (CSIP) set coordinator <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PREVIOUS_STATE](../android/bluetooth/BluetoothProfile.md) <br /> Extra for the connection state intents of the individual profiles. This extra represents the previous connection state of the profile of the Bluetooth device. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PROFILE](../android/bluetooth/BluetoothProfile.md) <br /> Extra for the [BluetoothProfile](../android/bluetooth/BluetoothProfile.md) that the intent applies to. This extra represents the Bluetooth profile that the intent applies to. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_STATE](../android/bluetooth/BluetoothProfile.md) <br /> Extra for the connection state intents of the individual profiles. This extra represents the current connection state of the profile of the Bluetooth device. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GATT](../android/bluetooth/BluetoothProfile.md) <br /> Generic Attribute Profile (GATT) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GATT_SERVER](../android/bluetooth/BluetoothProfile.md) <br /> Generic Attribute Profile (GATT) Server <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HAP_CLIENT](../android/bluetooth/BluetoothProfile.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEADSET](../android/bluetooth/BluetoothProfile.md) <br /> Headset and Handsfree profile <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEALTH](../android/bluetooth/BluetoothProfile.md) <br /> Health Profile <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEARING_AID](../android/bluetooth/BluetoothProfile.md) <br /> Hearing Aid Device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HID_DEVICE](../android/bluetooth/BluetoothProfile.md) <br /> Human Interface Device (HID) Device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LE_AUDIO](../android/bluetooth/BluetoothProfile.md) <br /> LE Audio Device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAP](../android/bluetooth/BluetoothProfile.md) <br /> SIM Access Profile (SAP) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CONNECTED](../android/bluetooth/BluetoothProfile.md) <br /> The profile is in connected state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CONNECTING](../android/bluetooth/BluetoothProfile.md) <br /> The profile is in connecting state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISCONNECTED](../android/bluetooth/BluetoothProfile.md) <br /> The profile is in disconnected state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISCONNECTING](../android/bluetooth/BluetoothProfile.md) <br /> The profile is in disconnecting state <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addService](../android/bluetooth/BluetoothGattServer.md))`(`service:` ` [BluetoothGattService](../android/bluetooth/BluetoothGattService.md)!`)` Add a service to the list of services to be hosted. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancelConnection](../android/bluetooth/BluetoothGattServer.md))`(`device:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!`)` Disconnects an established connection, or cancels a connection attempt currently in progress. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearServices](../android/bluetooth/BluetoothGattServer.md))`()` Remove all services from the list of provided services. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/bluetooth/BluetoothGattServer.md))`()` Close this GATT server instance. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [connect](../android/bluetooth/BluetoothGattServer.md))`(`device:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!`, `autoConnect:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Initiate a connection to a Bluetooth GATT capable device. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!\>! | [getConnectedDevices](../android/bluetooth/BluetoothGattServer.md))`()` Not supported - please use [BluetoothManager.getConnectedDevices(int)](../android/bluetooth/BluetoothManager.md))with [android.bluetooth.BluetoothProfile#GATT](../android/bluetooth/BluetoothProfile.md) as argument |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConnectionState](../android/bluetooth/BluetoothGattServer.md))`(`device:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!`)` Not supported - please use [BluetoothManager.getConnectedDevices(int)](../android/bluetooth/BluetoothManager.md))with [android.bluetooth.BluetoothProfile#GATT](../android/bluetooth/BluetoothProfile.md) as argument |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!\>! | [getDevicesMatchingConnectionStates](../android/bluetooth/BluetoothGattServer.md))`(`states:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Not supported - please use [BluetoothManager.getDevicesMatchingConnectionStates(int,](../android/bluetooth/BluetoothManager.md))with [BluetoothProfile.GATT](../android/bluetooth/BluetoothProfile.md) as first argument |
| [BluetoothGattService](../android/bluetooth/BluetoothGattService.md)! | [getService](../android/bluetooth/BluetoothGattServer.md))`(`uuid:` ` [UUID](../java/util/UUID.md)!`)` Returns a [BluetoothGattService](../android/bluetooth/BluetoothGattService.md) from the list of services offered by this device. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothGattService](../android/bluetooth/BluetoothGattService.md)!\>! | [getServices](../android/bluetooth/BluetoothGattServer.md))`()` Returns a list of GATT services offered by this device. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [notifyCharacteristicChanged](../android/bluetooth/BluetoothGattServer.md))`(`device:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!`, `characteristic:` ` [BluetoothGattCharacteristic](../android/bluetooth/BluetoothGattCharacteristic.md)!`, `confirm:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Send a notification or indication that a local characteristic has been updated. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [notifyCharacteristicChanged](../android/bluetooth/BluetoothGattServer.md))`(`device:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)`, `characteristic:` ` [BluetoothGattCharacteristic](../android/bluetooth/BluetoothGattCharacteristic.md)`, `confirm:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `value:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Send a notification or indication that a local characteristic has been updated. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readPhy](../android/bluetooth/BluetoothGattServer.md))`(`device:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!`)` Read the current transmitter PHY and receiver PHY of the connection. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeService](../android/bluetooth/BluetoothGattServer.md))`(`service:` ` [BluetoothGattService](../android/bluetooth/BluetoothGattService.md)!`)` Removes a service from the list of services to be provided. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [sendResponse](../android/bluetooth/BluetoothGattServer.md))`(`device:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!`, `requestId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Send a response to a read or write request to a remote device. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreferredPhy](../android/bluetooth/BluetoothGattServer.md))`(`device:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!`, `txPhy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `rxPhy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `phyOptions:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the preferred connection PHY for this app. |

## Public methods

### addService

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addService(service: BluetoothGattService!): Boolean
```

Add a service to the list of services to be hosted.

Once a service has been added to the list, the service and its included characteristics will be provided by the local device.

If the local device has already exposed services when this function is called, a service update notification will be sent to all clients.

The [BluetoothGattServerCallback.onServiceAdded](../android/bluetooth/BluetoothGattServerCallback.md))callback will indicate whether this service has been added successfully. Do not add another service before this callback. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH](../android/Manifest.permission.md) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `service` | [BluetoothGattService](../android/bluetooth/BluetoothGattService.md)!:Service to be added to the list of services provided by this device. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true, if the request to add service has been initiated |

### cancelConnection

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun cancelConnection(device: BluetoothDevice!): Unit
```

Disconnects an established connection, or cancels a connection attempt currently in progress. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH](../android/Manifest.permission.md) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!:Remote device |

### clearServices

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clearServices(): Unit
```

Remove all services from the list of provided services. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH](../android/Manifest.permission.md) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md) 

### close

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

Close this GATT server instance.

Application should call this method as early as possible after it is done with this GATT server. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md) 

### connect

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun connect(
    device: BluetoothDevice!, 
    autoConnect: Boolean
): Boolean
```

Initiate a connection to a Bluetooth GATT capable device.

The connection may not be established right away, but will be completed when the remote device is available. A [BluetoothGattServerCallback.onConnectionStateChange](../android/bluetooth/BluetoothGattServerCallback.md))callback will be invoked when the connection state changes as a result of this function.

The autoConnect parameter determines whether to actively connect to the remote device, or rather passively scan and finalize the connection when the remote device is in range/available. Generally, the first ever connection to a device should be direct (autoConnect set to false) and subsequent connections to known devices should be invoked with the autoConnect parameter set to true. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH](../android/Manifest.permission.md) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

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

Not supported - please use [BluetoothManager.getConnectedDevices(int)](../android/bluetooth/BluetoothManager.md))with [android.bluetooth.BluetoothProfile#GATT](../android/bluetooth/BluetoothProfile.md) as argument

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!>! | List of devices. The list will be empty on error. |

| Exceptions ||
|-------------------------------------------|---------------|
| `java.lang.UnsupportedOperationException` | on every call |

### getConnectionState

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnectionState(device: BluetoothDevice!): Int
```

Not supported - please use [BluetoothManager.getConnectedDevices(int)](../android/bluetooth/BluetoothManager.md))with [android.bluetooth.BluetoothProfile#GATT](../android/bluetooth/BluetoothProfile.md) as argument

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!:Remote bluetooth device. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | State of the profile connection. One of [STATE_CONNECTED](../android/bluetooth/BluetoothProfile.md), [STATE_CONNECTING](../android/bluetooth/BluetoothProfile.md), [STATE_DISCONNECTED](../android/bluetooth/BluetoothProfile.md), [STATE_DISCONNECTING](../android/bluetooth/BluetoothProfile.md) Value is [android.bluetooth.BluetoothProfile#STATE_DISCONNECTED](../android/bluetooth/BluetoothProfile.md), [android.bluetooth.BluetoothProfile#STATE_CONNECTING](../android/bluetooth/BluetoothProfile.md), [android.bluetooth.BluetoothProfile#STATE_CONNECTED](../android/bluetooth/BluetoothProfile.md), or [android.bluetooth.BluetoothProfile#STATE_DISCONNECTING](../android/bluetooth/BluetoothProfile.md) |

| Exceptions ||
|-------------------------------------------|---------------|
| `java.lang.UnsupportedOperationException` | on every call |

### getDevicesMatchingConnectionStates

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDevicesMatchingConnectionStates(states: IntArray!): MutableList<BluetoothDevice!>!
```

Not supported - please use [BluetoothManager.getDevicesMatchingConnectionStates(int,](../android/bluetooth/BluetoothManager.md))with [BluetoothProfile.GATT](../android/bluetooth/BluetoothProfile.md) as first argument

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `states` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:Array of states. States can be one of [STATE_CONNECTED](../android/bluetooth/BluetoothProfile.md), [STATE_CONNECTING](../android/bluetooth/BluetoothProfile.md), [STATE_DISCONNECTED](../android/bluetooth/BluetoothProfile.md), [STATE_DISCONNECTING](../android/bluetooth/BluetoothProfile.md), |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!>! | List of devices. The list will be empty on error. |

| Exceptions ||
|-------------------------------------------|---------------|
| `java.lang.UnsupportedOperationException` | on every call |

### getService

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getService(uuid: UUID!): BluetoothGattService!
```

Returns a [BluetoothGattService](../android/bluetooth/BluetoothGattService.md) from the list of services offered by this device.

If multiple instances of the same service (as identified by UUID) exist, the first instance of the service is returned. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH](../android/Manifest.permission.md) permission which can be gained with a simple`<uses-permission>`manifest tag.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `uuid` | [UUID](../java/util/UUID.md)!:UUID of the requested service |

| Return ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [BluetoothGattService](../android/bluetooth/BluetoothGattService.md)! | BluetoothGattService if supported, or null if the requested service is not offered by this device. |

### getServices

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServices(): MutableList<BluetoothGattService!>!
```

Returns a list of GATT services offered by this device.

An application must call [addService](../android/bluetooth/BluetoothGattServer.md))to add a service to the list of services offered by this device. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH](../android/Manifest.permission.md) permission which can be gained with a simple`<uses-permission>`manifest tag.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothGattService](../android/bluetooth/BluetoothGattService.md)!>! | List of services. Returns an empty list if no services have been added yet. |

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

**Deprecated:** *Use [BluetoothGattServer.notifyCharacteristicChanged(BluetoothDevice,](../android/bluetooth/BluetoothGattServer.md))as this is not memory safe.*

Send a notification or indication that a local characteristic has been updated.

A notification or indication is sent to the remote device to signal that the characteristic has been updated. This function should be invoked for every client that requests notifications/indications by writing to the "Client Configuration" descriptor for the given characteristic. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH](../android/Manifest.permission.md) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!:The remote device to receive the notification/indication |
| `characteristic` | [BluetoothGattCharacteristic](../android/bluetooth/BluetoothGattCharacteristic.md)!:The local characteristic that has been updated |
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
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH](../android/Manifest.permission.md) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md):the remote device to receive the notification/indication This value cannot be`null`. |
| `characteristic` | [BluetoothGattCharacteristic](../android/bluetooth/BluetoothGattCharacteristic.md):the local characteristic that has been updated This value cannot be`null`. |
| `confirm` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`to request confirmation from the client (indication) or`false`to send a notification |
| --- | --- |
| `value` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the characteristic value This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | whether the notification has been triggered successfully Value is [android.bluetooth.BluetoothStatusCodes#SUCCESS](../android/bluetooth/BluetoothStatusCodes.md), [android.bluetooth.BluetoothStatusCodes#ERROR_MISSING_BLUETOOTH_CONNECT_PERMISSION](../android/bluetooth/BluetoothStatusCodes.md), android.bluetooth.BluetoothStatusCodes.ERROR_DEVICE_NOT_CONNECTED, [android.bluetooth.BluetoothStatusCodes#ERROR_PROFILE_SERVICE_NOT_BOUND](../android/bluetooth/BluetoothStatusCodes.md), or [android.bluetooth.BluetoothStatusCodes#ERROR_UNKNOWN](../android/bluetooth/BluetoothStatusCodes.md) |

| Exceptions ||
|--------------------------------------|------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the characteristic value or service is null |

### readPhy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readPhy(device: BluetoothDevice!): Unit
```

Read the current transmitter PHY and receiver PHY of the connection. The values are returned in [BluetoothGattServerCallback.onPhyRead](../android/bluetooth/BluetoothGattServerCallback.md)) 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!:The remote device to send this response to |

### removeService

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeService(service: BluetoothGattService!): Boolean
```

Removes a service from the list of services to be provided. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH](../android/Manifest.permission.md) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| `service` | [BluetoothGattService](../android/bluetooth/BluetoothGattService.md)!:Service to be removed. |

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

- [BluetoothGattServerCallback.onCharacteristicReadRequest](../android/bluetooth/BluetoothGattServerCallback.md))
- [BluetoothGattServerCallback.onCharacteristicWriteRequest](../android/bluetooth/BluetoothGattServerCallback.md))
- [BluetoothGattServerCallback.onDescriptorReadRequest](../android/bluetooth/BluetoothGattServerCallback.md))
- [BluetoothGattServerCallback.onDescriptorWriteRequest](../android/bluetooth/BluetoothGattServerCallback.md))

<br />

For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH](../android/Manifest.permission.md) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!:The remote device to send this response to |
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

[BluetoothGattServerCallback.onPhyUpdate](../android/bluetooth/BluetoothGattServerCallback.md))will be triggered as a result of this call, even if no PHY change happens. It is also triggered when remote device updates the PHY. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!:The remote device to send this response to |
| `txPhy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):preferred transmitter PHY. Bitwise OR of any of [android.bluetooth.BluetoothDevice#PHY_LE_1M_MASK](../android/bluetooth/BluetoothDevice.md), [BluetoothDevice.PHY_LE_2M_MASK](../android/bluetooth/BluetoothDevice.md), and [android.bluetooth.BluetoothDevice#PHY_LE_CODED_MASK](../android/bluetooth/BluetoothDevice.md). |
| `rxPhy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):preferred receiver PHY. Bitwise OR of any of [android.bluetooth.BluetoothDevice#PHY_LE_1M_MASK](../android/bluetooth/BluetoothDevice.md), [BluetoothDevice.PHY_LE_2M_MASK](../android/bluetooth/BluetoothDevice.md), and [android.bluetooth.BluetoothDevice#PHY_LE_CODED_MASK](../android/bluetooth/BluetoothDevice.md). |
| --- | --- |
| `phyOptions` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):preferred coding to use when transmitting on the LE Coded PHY. Can be one of [BluetoothDevice.PHY_OPTION_NO_PREFERRED](../android/bluetooth/BluetoothDevice.md), [BluetoothDevice.PHY_OPTION_S2](../android/bluetooth/BluetoothDevice.md) or [BluetoothDevice.PHY_OPTION_S8](../android/bluetooth/BluetoothDevice.md) |
