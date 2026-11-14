Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothGatt

```
class BluetoothGatt : BluetoothProfile
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothGatt](BluetoothGatt.md) |

Public API for the Bluetooth GATT Profile.

This class provides Bluetooth GATT functionality to enable communication with Bluetooth Smart or Smart Ready devices.

To connect to a remote peripheral device, create a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback` and call android.bluetooth.BluetoothDevice#connectGatt to get a instance of this class. GATT capable devices can be discovered using the Bluetooth device discovery or BLE scan process.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#CONNECTION_PRIORITY_BALANCED:kotlin.Int` Connection parameter update - Use the connection parameters recommended by the Bluetooth SIG. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#CONNECTION_PRIORITY_DCK:kotlin.Int` Connection parameter update - Request the priority preferred for Digital Car Key for a lower latency connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#CONNECTION_PRIORITY_HIGH:kotlin.Int` Connection parameter update - Request a high priority, low latency connection. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#CONNECTION_PRIORITY_LOW_POWER:kotlin.Int` Connection parameter update - Request low power, reduced data rate connection parameters. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_CONNECTION_CONGESTED:kotlin.Int` A remote device connection is congested. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_CONNECTION_TIMEOUT:kotlin.Int` GATT connection timed out, likely due to the remote device being out of range or not advertising as connectable. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_FAILURE:kotlin.Int` A GATT operation failed, errors other than the above |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_INSUFFICIENT_AUTHENTICATION:kotlin.Int` Insufficient authentication for a given operation |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_INSUFFICIENT_AUTHORIZATION:kotlin.Int` Insufficient authorization for a given operation |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_INSUFFICIENT_ENCRYPTION:kotlin.Int` Insufficient encryption for a given operation |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_INVALID_ATTRIBUTE_LENGTH:kotlin.Int` A write operation exceeds the maximum length of the attribute |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_INVALID_OFFSET:kotlin.Int` A read or write operation was requested with an invalid offset |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_READ_NOT_PERMITTED:kotlin.Int` GATT read operation is not permitted |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_REQUEST_NOT_SUPPORTED:kotlin.Int` The given request is not supported |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` A GATT operation completed successfully |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_WRITE_NOT_PERMITTED:kotlin.Int` GATT write operation is not permitted |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#SUBRATE_MODE_BALANCED:kotlin.Int` Connection subrate mode - Requests to enable subrate mode using balanced parameters to provide a compromise between power savings and performance. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#SUBRATE_MODE_HIGH:kotlin.Int` Connection subrate mode - Requests to enable subrate mode with parameters optimized for high burstiness, enhanced data transfer. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#SUBRATE_MODE_LOW:kotlin.Int` Connection Subrate mode - Requests to enable subrate mode with parameters optimized for low burstiness, minimum power consumption. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#SUBRATE_MODE_NOT_UPDATED:kotlin.Int` Connection Subrate mode - No Update applied due to error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#SUBRATE_MODE_OFF:kotlin.Int` Connection Subrate mode - Request to disable subrate mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#SUBRATE_MODE_SYSTEM_UPDATE:kotlin.Int` Connection Subrate mode - System Update. |

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
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#abortReliableWrite()()` Cancels a reliable write transaction for a given device. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#abortReliableWrite(android.bluetooth.BluetoothDevice)(mDevice: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!)` For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#beginReliableWrite()()` Initiates a reliable write transaction for a given remote device. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#close()()` Close this Bluetooth GATT client. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#connect()()` Connect back to remote device. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#disconnect()()` Disconnects an established connection, or cancels a connection attempt currently in progress. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#discoverServices()()` Discovers services offered by a remote device as well as their characteristics and descriptors. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#executeReliableWrite()()` Executes a reliable write transaction for a given remote device. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](BluetoothDevice.md)!\>! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#getConnectedDevices()()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#getConnectionState(android.bluetooth.BluetoothDevice)(device: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!)` <br /> |
| [BluetoothDevice](BluetoothDevice.md)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#getDevice()()` Return the remote bluetooth device this GATT client targets to |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](BluetoothDevice.md)!\>! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#getDevicesMatchingConnectionStates(kotlin.IntArray)(states: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!)` <br /> |
| --- | --- |
| [BluetoothGattService](BluetoothGattService.md)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#getService(java.util.UUID)(uuid: https://developer.android.com/reference/kotlin/java/util/UUID.html#!)` Returns a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService`, if the requested UUID is supported by the remote device. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothGattService](BluetoothGattService.md)!\>! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#getServices()()` Returns a list of GATT services offered by the remote device. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#readCharacteristic(android.bluetooth.BluetoothGattCharacteristic)(characteristic: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic!)` Reads the requested characteristic from the associated remote device. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#readDescriptor(android.bluetooth.BluetoothGattDescriptor)(descriptor: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor!)` Reads the value for a given descriptor from the associated remote device. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#readPhy()()` Read the current transmitter PHY and receiver PHY of the connection. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#readRemoteRssi()()` Read the RSSI for a connected remote device. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#requestConnectionPriority(kotlin.Int)(connectionPriority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Request a connection parameter update. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#requestMtu(kotlin.Int)(mtu: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Request an MTU size used for a given connection. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#requestSubrateMode(kotlin.Int)(subrateMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Request LE subrate mode. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#setCharacteristicNotification(android.bluetooth.BluetoothGattCharacteristic,%20kotlin.Boolean)(characteristic: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic!, enable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Enable or disable notifications/indications for a given characteristic. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#setPreferredPhy(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(txPhy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, rxPhy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, phyOptions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the preferred connection PHY for this app. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#writeCharacteristic(android.bluetooth.BluetoothGattCharacteristic)(characteristic: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic!)` Writes a given characteristic and its values to the associated remote device. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#writeCharacteristic(android.bluetooth.BluetoothGattCharacteristic,%20kotlin.ByteArray,%20kotlin.Int)(characteristic: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html, writeType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Writes a given characteristic and its values to the associated remote device. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#writeDescriptor(android.bluetooth.BluetoothGattDescriptor)(descriptor: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor!)` Write the value of a given descriptor to the associated remote device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#writeDescriptor(android.bluetooth.BluetoothGattDescriptor,%20kotlin.ByteArray)(descriptor: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)` Write the value of a given descriptor to the associated remote device. |
| --- | --- |

## Constants

### CONNECTION_PRIORITY_BALANCED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_PRIORITY_BALANCED: Int
```

Connection parameter update - Use the connection parameters recommended by the Bluetooth SIG. This is the default value if no connection parameter update is requested.

 Value: 0

### CONNECTION_PRIORITY_DCK

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_PRIORITY_DCK: Int
```

Connection parameter update - Request the priority preferred for Digital Car Key for a lower latency connection. This connection parameter will consume more power than `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#CONNECTION_PRIORITY_BALANCED:kotlin.Int`, so it is recommended that apps do not use this unless it specifically fits their use case.

 Value: 3

### CONNECTION_PRIORITY_HIGH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_PRIORITY_HIGH: Int
```

Connection parameter update - Request a high priority, low latency connection. An application should only request high priority connection parameters to transfer large amounts of data over LE quickly. Once the transfer is complete, the application should request `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#CONNECTION_PRIORITY_BALANCED:kotlin.Int` connection parameters to reduce energy use.

 Value: 1

### CONNECTION_PRIORITY_LOW_POWER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_PRIORITY_LOW_POWER: Int
```

Connection parameter update - Request low power, reduced data rate connection parameters.

 Value: 2

### GATT_CONNECTION_CONGESTED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GATT_CONNECTION_CONGESTED: Int
```

A remote device connection is congested.

 Value: 143

### GATT_CONNECTION_TIMEOUT

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GATT_CONNECTION_TIMEOUT: Int
```

GATT connection timed out, likely due to the remote device being out of range or not advertising as connectable.

 Value: 147

### GATT_FAILURE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GATT_FAILURE: Int
```

A GATT operation failed, errors other than the above

 Value: 257

### GATT_INSUFFICIENT_AUTHENTICATION

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GATT_INSUFFICIENT_AUTHENTICATION: Int
```

Insufficient authentication for a given operation

 Value: 5

### GATT_INSUFFICIENT_AUTHORIZATION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GATT_INSUFFICIENT_AUTHORIZATION: Int
```

Insufficient authorization for a given operation

 Value: 8

### GATT_INSUFFICIENT_ENCRYPTION

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GATT_INSUFFICIENT_ENCRYPTION: Int
```

Insufficient encryption for a given operation

 Value: 15

### GATT_INVALID_ATTRIBUTE_LENGTH

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GATT_INVALID_ATTRIBUTE_LENGTH: Int
```

A write operation exceeds the maximum length of the attribute

 Value: 13

### GATT_INVALID_OFFSET

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GATT_INVALID_OFFSET: Int
```

A read or write operation was requested with an invalid offset

 Value: 7

### GATT_READ_NOT_PERMITTED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GATT_READ_NOT_PERMITTED: Int
```

GATT read operation is not permitted

 Value: 2

### GATT_REQUEST_NOT_SUPPORTED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GATT_REQUEST_NOT_SUPPORTED: Int
```

The given request is not supported

 Value: 6

### GATT_SUCCESS

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GATT_SUCCESS: Int
```

A GATT operation completed successfully

 Value: 0

### GATT_WRITE_NOT_PERMITTED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GATT_WRITE_NOT_PERMITTED: Int
```

GATT write operation is not permitted

 Value: 3

### SUBRATE_MODE_BALANCED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUBRATE_MODE_BALANCED: Int
```

Connection subrate mode - Requests to enable subrate mode using balanced parameters to provide a compromise between power savings and performance.

 Value: 2

### SUBRATE_MODE_HIGH

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUBRATE_MODE_HIGH: Int
```

Connection subrate mode - Requests to enable subrate mode with parameters optimized for high burstiness, enhanced data transfer.

 Value: 3

### SUBRATE_MODE_LOW

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUBRATE_MODE_LOW: Int
```

Connection Subrate mode - Requests to enable subrate mode with parameters optimized for low burstiness, minimum power consumption. This is the most power-efficient subrate configuration.

 Value: 1

### SUBRATE_MODE_NOT_UPDATED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUBRATE_MODE_NOT_UPDATED: Int
```

Connection Subrate mode - No Update applied due to error.

 Value: 255

### SUBRATE_MODE_OFF

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUBRATE_MODE_OFF: Int
```

Connection Subrate mode - Request to disable subrate mode.

 Value: 0

### SUBRATE_MODE_SYSTEM_UPDATE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUBRATE_MODE_SYSTEM_UPDATE: Int
```

Connection Subrate mode - System Update.

 Value: 99

## Public methods

### abortReliableWrite

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun abortReliableWrite(): Unit
```

Cancels a reliable write transaction for a given device.

Calling this function will discard all queued characteristic write operations for a given remote device. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

### abortReliableWrite

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun abortReliableWrite(mDevice: BluetoothDevice!): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#abortReliableWrite()`*

For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

### beginReliableWrite

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun beginReliableWrite(): Boolean
```

Initiates a reliable write transaction for a given remote device.

Once a reliable write transaction has been initiated, all calls to #writeCharacteristic are sent to the remote device for verification and queued up for atomic execution. The application will receive a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onCharacteristicWrite(android.bluetooth.BluetoothGatt,%20android.bluetooth.BluetoothGattCharacteristic,%20kotlin.Int)` callback in response to every `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#writeCharacteristic(android.bluetooth.BluetoothGattCharacteristic,%20kotlin.ByteArray,%20kotlin.Int)` call and is responsible for verifying if the value has been transmitted accurately.

After all characteristics have been queued up and verified, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#executeReliableWrite()` will execute all writes. If a characteristic was not written correctly, calling #abortReliableWrite will cancel the current transaction without committing any values on the remote device. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true, if the reliable write transaction has been initiated |

### close

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun close(): Unit
```

Close this Bluetooth GATT client.

Application should call this method as early as possible after it is done with this GATT client. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

### connect

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun connect(): Boolean
```

Connect back to remote device.

This method is used to re-connect to a remote device after the connection has been dropped. If the device is not in range, the re-connection will be triggered once the device is back in range. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true, if the connection attempt was initiated successfully |

### disconnect

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun disconnect(): Unit
```

Disconnects an established connection, or cancels a connection attempt currently in progress. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

### discoverServices

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun discoverServices(): Boolean
```

Discovers services offered by a remote device as well as their characteristics and descriptors.

This is an asynchronous operation. Once service discovery is completed, the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onServicesDiscovered(android.bluetooth.BluetoothGatt,%20kotlin.Int)` callback is triggered. If the discovery was successful, the remote services can be retrieved using the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#getServices()` function. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true, if the remote service discovery has been started |

### executeReliableWrite

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun executeReliableWrite(): Boolean
```

Executes a reliable write transaction for a given remote device.

This function will commit all queued up characteristic write operations for a given remote device.

A `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onReliableWriteCompleted(android.bluetooth.BluetoothGatt,%20kotlin.Int)` callback is invoked to indicate whether the transaction has been executed correctly. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true, if the request to execute the transaction has been sent |

### getConnectedDevices

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConnectedDevices(): MutableList<BluetoothDevice!>!
```

**Deprecated:** *Not supported - please use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager#getConnectedDevices(kotlin.Int)` with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#GATT:kotlin.Int` as argument*

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!>!` | List of devices. The list will be empty on error. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | on every call |

### getConnectionState

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConnectionState(device: BluetoothDevice!): Int
```

**Deprecated:** *Not supported - please use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager#getConnectedDevices(kotlin.Int)` with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#GATT:kotlin.Int` as argument*

| Parameters ||
|---|---|
| `device` | [BluetoothDevice](BluetoothDevice.md)!: Remote bluetooth device. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | State of the profile connection. One of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | on every call |

### getDevice

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDevice(): BluetoothDevice!
```

Return the remote bluetooth device this GATT client targets to

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!` | remote bluetooth device |

### getDevicesMatchingConnectionStates

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDevicesMatchingConnectionStates(states: IntArray!): MutableList<BluetoothDevice!>!
```

**Deprecated:** *Not supported - please use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager#getDevicesMatchingConnectionStates(kotlin.Int,%20kotlin.IntArray)` with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#GATT:kotlin.Int` as first argument*

| Parameters ||
|---|---|
| `states` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: Array of states. States can be one of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int`, |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!>!` | List of devices. The list will be empty on error. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | on every call |

### getService

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getService(uuid: UUID!): BluetoothGattService!
```

Returns a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService`, if the requested UUID is supported by the remote device.

This function requires that service discovery has been completed for the given device.

If multiple instances of the same service (as identified by UUID) exist, the first instance of the service is returned. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag.

| Parameters ||
|---|---|
| `uuid` | [UUID](../java.util/UUID.md)!: UUID of the requested service |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService!` | BluetoothGattService if supported, or null if the requested service is not offered by the remote device. |

### getServices

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getServices(): MutableList<BluetoothGattService!>!
```

Returns a list of GATT services offered by the remote device.

This function requires that service discovery has been completed for the given device. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService!>!` | List of services on the remote device. Returns an empty list if service discovery has not yet been performed. |

### readCharacteristic

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readCharacteristic(characteristic: BluetoothGattCharacteristic!): Boolean
```

Reads the requested characteristic from the associated remote device.

This is an asynchronous operation. The result of the read operation is reported by the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onCharacteristicRead(android.bluetooth.BluetoothGatt,%20android.bluetooth.BluetoothGattCharacteristic,%20kotlin.ByteArray,%20kotlin.Int)` callback. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `characteristic` | [BluetoothGattCharacteristic](BluetoothGattCharacteristic.md)!: Characteristic to read from the remote device |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true, if the read operation was initiated successfully |

### readDescriptor

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readDescriptor(descriptor: BluetoothGattDescriptor!): Boolean
```

Reads the value for a given descriptor from the associated remote device.

Once the read operation has been completed, the android.bluetooth.BluetoothGattCallback#onDescriptorRead callback is triggered, signaling the result of the operation. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `descriptor` | [BluetoothGattDescriptor](BluetoothGattDescriptor.md)!: Descriptor value to read from the remote device |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true, if the read operation was initiated successfully |

### readPhy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readPhy(): Unit
```

Read the current transmitter PHY and receiver PHY of the connection. The values are returned in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onPhyRead(android.bluetooth.BluetoothGatt,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

### readRemoteRssi

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readRemoteRssi(): Boolean
```

Read the RSSI for a connected remote device.

The `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onReadRemoteRssi(android.bluetooth.BluetoothGatt,%20kotlin.Int,%20kotlin.Int)` callback will be invoked when the RSSI value has been read. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true, if the RSSI value has been requested successfully |

### requestConnectionPriority

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun requestConnectionPriority(connectionPriority: Int): Boolean
```

Request a connection parameter update.

This function will send a connection parameter update request to the remote device. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `connectionPriority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Request a specific connection priority. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#CONNECTION_PRIORITY_BALANCED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#CONNECTION_PRIORITY_HIGH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#CONNECTION_PRIORITY_LOW_POWER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#CONNECTION_PRIORITY_DCK:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the parameters are outside of their specified range. |

### requestMtu

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun requestMtu(mtu: Int): Boolean
```

Request an MTU size used for a given connection. Please note that starting from Android 14, the Android Bluetooth stack requests the BLE ATT MTU to 517 bytes when the first GATT client requests an MTU, and disregards all subsequent MTU requests. Check out [MTU is set to 517 for the first GATT client requesting an MTU](https://developer.android.com/about/versions/14/behavior-changes-all#mtu-set-to-517) for more information.

When performing a write request operation (write without response), the data sent is truncated to the MTU size. This function may be used to request a larger MTU size to be able to send more data at once.

A `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onMtuChanged(android.bluetooth.BluetoothGatt,%20kotlin.Int,%20kotlin.Int)` callback will indicate whether this operation was successful. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true, if the new MTU value has been requested successfully |

### requestSubrateMode

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun requestSubrateMode(subrateMode: Int): Int
```

Request LE subrate mode.

Configure/Request subrating with this API, sending a subrate request to the remote device based on Subrate Mode. This function should be used in conjunction with requestConnectionPriority to manage link latency and power consumption effectively.

This method requires the calling app to have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission. Additionally, an app must either have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_PRIVILEGED:kotlin.String` or be associated with the Companion Device manager (see android.companion.CompanionDeviceManager#associate(AssociationRequest,android.companion.CompanionDeviceManager.Callback,android.os.Handler)). 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `subrateMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Request a specific subrate mode. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#SUBRATE_MODE_OFF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#SUBRATE_MODE_LOW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#SUBRATE_MODE_BALANCED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#SUBRATE_MODE_HIGH:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | true, if the request is send to the Bluetooth stack. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#SUCCESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_BLUETOOTH_NOT_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_BLUETOOTH_NOT_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_MISSING_BLUETOOTH_CONNECT_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_DEVICE_NOT_BONDED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#FEATURE_NOT_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_UNKNOWN:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the parameters are outside of their specified range. |

### setCharacteristicNotification

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCharacteristicNotification(
    characteristic: BluetoothGattCharacteristic!, 
    enable: Boolean
): Boolean
```

Enable or disable notifications/indications for a given characteristic.

Once notifications are enabled for a characteristic, a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onCharacteristicChanged(android.bluetooth.BluetoothGatt,%20android.bluetooth.BluetoothGattCharacteristic,%20kotlin.ByteArray)` callback will be triggered if the remote device indicates that the given characteristic has changed. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `characteristic` | [BluetoothGattCharacteristic](BluetoothGattCharacteristic.md)!: The characteristic for which to enable notifications |
| `enable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Set to true to enable notifications/indications |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true, if the requested notification status was set successfully |

### setPreferredPhy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPreferredPhy(
    txPhy: Int, 
    rxPhy: Int, 
    phyOptions: Int
): Unit
```

Set the preferred connection PHY for this app. Please note that this is just a recommendation, whether the PHY change will happen depends on other applications preferences, local and remote controller capabilities. Controller can override these settings.

`https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onPhyUpdate(android.bluetooth.BluetoothGatt,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` will be triggered as a result of this call, even if no PHY change happens. It is also triggered when remote device updates the PHY. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `txPhy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): preferred transmitter PHY. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_1M_MASK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_2M_MASK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_CODED_MASK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_HDT_MASK:kotlin.Int` |
| `rxPhy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): preferred receiver PHY. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_1M_MASK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_2M_MASK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_CODED_MASK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_HDT_MASK:kotlin.Int` |
| `phyOptions` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): preferred coding to use when transmitting on the LE Coded PHY. Can be one of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_OPTION_NO_PREFERRED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_OPTION_S2:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_OPTION_S8:kotlin.Int`. |
| --- | --- |

### writeCharacteristic

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeCharacteristic(characteristic: BluetoothGattCharacteristic!): Boolean
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#writeCharacteristic(android.bluetooth.BluetoothGattCharacteristic,%20kotlin.ByteArray,%20kotlin.Int)` as this is not memory safe because it relies on a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic` object whose underlying fields are subject to change outside this method.*

Writes a given characteristic and its values to the associated remote device.

Once the write operation has been completed, the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onCharacteristicWrite(android.bluetooth.BluetoothGatt,%20android.bluetooth.BluetoothGattCharacteristic,%20kotlin.Int)` callback is invoked, reporting the result of the operation. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `characteristic` | [BluetoothGattCharacteristic](BluetoothGattCharacteristic.md)!: Characteristic to write on the remote device |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true, if the write operation was initiated successfully |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if characteristic or its value are null |

### writeCharacteristic

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeCharacteristic(
    characteristic: BluetoothGattCharacteristic, 
    value: ByteArray, 
    writeType: Int
): Int
```

Writes a given characteristic and its values to the associated remote device.

Once the write operation has been completed, the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onCharacteristicWrite(android.bluetooth.BluetoothGatt,%20android.bluetooth.BluetoothGattCharacteristic,%20kotlin.Int)` callback is invoked, reporting the result of the operation. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `characteristic` | [BluetoothGattCharacteristic](BluetoothGattCharacteristic.md): Characteristic to write on the remote device. This value cannot be `null`. |
| `value` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): This value cannot be `null`. |
| `writeType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#WRITE_TYPE_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#WRITE_TYPE_NO_RESPONSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#WRITE_TYPE_SIGNED:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | whether the characteristic was successfully written to. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#SUCCESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_MISSING_BLUETOOTH_CONNECT_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_PROFILE_SERVICE_NOT_BOUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_GATT_WRITE_NOT_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_GATT_WRITE_REQUEST_BUSY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_UNKNOWN:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if characteristic or value are null |

### writeDescriptor

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeDescriptor(descriptor: BluetoothGattDescriptor!): Boolean
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#writeDescriptor(android.bluetooth.BluetoothGattDescriptor,%20kotlin.ByteArray)` as this is not memory safe because it relies on a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor` object whose underlying fields are subject to change outside this method.*

Write the value of a given descriptor to the associated remote device.

A `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onDescriptorWrite(android.bluetooth.BluetoothGatt,%20android.bluetooth.BluetoothGattDescriptor,%20kotlin.Int)` callback is triggered to report the result of the write operation. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `descriptor` | [BluetoothGattDescriptor](BluetoothGattDescriptor.md)!: Descriptor to write to the associated remote device |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true, if the write operation was initiated successfully |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if descriptor or its value are null |

### writeDescriptor

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeDescriptor(
    descriptor: BluetoothGattDescriptor, 
    value: ByteArray
): Int
```

Write the value of a given descriptor to the associated remote device.

A `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onDescriptorWrite(android.bluetooth.BluetoothGatt,%20android.bluetooth.BluetoothGattDescriptor,%20kotlin.Int)` callback is triggered to report the result of the write operation. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `descriptor` | [BluetoothGattDescriptor](BluetoothGattDescriptor.md): Descriptor to write to the associated remote device. This value cannot be `null`. |
| `value` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | true, if the write operation was initiated successfully. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#SUCCESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_MISSING_BLUETOOTH_CONNECT_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_PROFILE_SERVICE_NOT_BOUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_GATT_WRITE_NOT_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_GATT_WRITE_REQUEST_BUSY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_UNKNOWN:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if descriptor or value are null |
