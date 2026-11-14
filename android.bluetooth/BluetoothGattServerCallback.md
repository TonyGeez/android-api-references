Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothGattServerCallback

```
abstract class BluetoothGattServerCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothGattServerCallback](../android/bluetooth/BluetoothGattServerCallback.md) |

This abstract class is used to implement `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer` callbacks.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback#BluetoothGattServerCallback()()` <br /> |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback#onCharacteristicReadRequest(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int,%20android.bluetooth.BluetoothGattCharacteristic)(device: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!, requestId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, characteristic: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic!)` A remote client has requested to read a local characteristic. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback#onCharacteristicWriteRequest(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20android.bluetooth.BluetoothGattCharacteristic,%20kotlin.Boolean,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.ByteArray)(device: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!, requestId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, characteristic: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic!, preparedWrite: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, responseNeeded: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` A remote client has requested to write to a local characteristic. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback#onConnectionStateChange(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int)(device: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!, status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, newState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Callback indicating when a remote device has been connected or disconnected. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback#onConnectionUpdated(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(device: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice, interval: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, latency: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, supervisionTimeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Callback indicating the connection parameters were updated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback#onDescriptorReadRequest(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int,%20android.bluetooth.BluetoothGattDescriptor)(device: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!, requestId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, descriptor: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor!)` A remote client has requested to read a local descriptor. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback#onDescriptorWriteRequest(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20android.bluetooth.BluetoothGattDescriptor,%20kotlin.Boolean,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.ByteArray)(device: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!, requestId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, descriptor: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor!, preparedWrite: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, responseNeeded: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` A remote client has requested to write to a local descriptor. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback#onExecuteWrite(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Boolean)(device: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!, requestId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, execute: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Execute all pending write operations for this device. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback#onMtuChanged(android.bluetooth.BluetoothDevice,%20kotlin.Int)(device: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!, mtu: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Callback indicating the MTU for a given device connection has changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback#onNotificationSent(android.bluetooth.BluetoothDevice,%20kotlin.Int)(device: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!, status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Callback invoked when a notification or indication has been sent to a remote device. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback#onPhyRead(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(device: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!, txPhy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, rxPhy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Callback triggered as result of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#readPhy(android.bluetooth.BluetoothDevice)` |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback#onPhyUpdate(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(device: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!, txPhy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, rxPhy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Callback triggered as result of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#setPreferredPhy(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`, or as a result of remote device changing the PHY. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback#onServiceAdded(kotlin.Int,%20android.bluetooth.BluetoothGattService)(status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, service: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService!)` Indicates whether a local service has been added successfully. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServerCallback#onSubrateChange(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int)(device: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice, subrateMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Callback indicating LE connection's subrate parameters have changed. |

## Public constructors

### BluetoothGattServerCallback

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BluetoothGattServerCallback()
```

## Public methods

### onCharacteristicReadRequest

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCharacteristicReadRequest(
    device: BluetoothDevice!, 
    requestId: Int, 
    offset: Int, 
    characteristic: BluetoothGattCharacteristic!
): Unit
```

A remote client has requested to read a local characteristic.

An application must call `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#sendResponse(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.ByteArray)` to complete the request.

| Parameters ||
|---|---|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!: The remote device that has requested the read operation |
| `requestId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The Id of the request |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Offset into the value of the characteristic |
| --- | --- |
| `characteristic` | [BluetoothGattCharacteristic](../android/bluetooth/BluetoothGattCharacteristic.md)!: Characteristic to be read |

### onCharacteristicWriteRequest

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCharacteristicWriteRequest(
    device: BluetoothDevice!, 
    requestId: Int, 
    characteristic: BluetoothGattCharacteristic!, 
    preparedWrite: Boolean, 
    responseNeeded: Boolean, 
    offset: Int, 
    value: ByteArray!
): Unit
```

A remote client has requested to write to a local characteristic.

An application must call `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#sendResponse(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.ByteArray)` to complete the request.

| Parameters ||
|---|---|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!: The remote device that has requested the write operation |
| `requestId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The Id of the request |
| `characteristic` | [BluetoothGattCharacteristic](../android/bluetooth/BluetoothGattCharacteristic.md)!: Characteristic to be written to. |
| --- | --- |
| `preparedWrite` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true, if this write operation should be queued for later execution. |
| `responseNeeded` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true, if the remote device requires a response |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset given for the value |
| --- | --- |
| `value` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: The value the client wants to assign to the characteristic |

### onConnectionStateChange

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onConnectionStateChange(
    device: BluetoothDevice!, 
    status: Int, 
    newState: Int
): Unit
```

Callback indicating when a remote device has been connected or disconnected.

| Parameters ||
|---|---|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!: Remote device that has been connected or disconnected. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Status of the connect or disconnect operation. |
| `newState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Returns the new connection state. Can be one of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int` |
| --- | --- |

### onConnectionUpdated

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onConnectionUpdated(
    device: BluetoothDevice, 
    interval: Int, 
    latency: Int, 
    supervisionTimeout: Int, 
    status: Int
): Unit
```

Callback indicating the connection parameters were updated.

| Parameters ||
|---|---|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md): The remote device involved. This value cannot be `null`. |
| `interval` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Connection interval used on this connection, 1.25ms unit. Valid range is from 6 (7.5ms) to 3200 (4000ms). Value is between 6 and 3200 inclusive |
| `latency` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Worker latency for the connection in number of connection events. Valid range is from 0 to 499. Value is between 0 and 499 inclusive |
| --- | --- |
| `supervisionTimeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Supervision timeout for this connection, in 10ms unit. Valid range is from 10 (0.1s) to 3200 (32s). Value is between 10 and 3200 inclusive |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` if the connection has been updated successfully. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_READ_NOT_PERMITTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_WRITE_NOT_PERMITTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_INSUFFICIENT_AUTHENTICATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_REQUEST_NOT_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_INSUFFICIENT_ENCRYPTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_INVALID_OFFSET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_INSUFFICIENT_AUTHORIZATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_INVALID_ATTRIBUTE_LENGTH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_CONNECTION_CONGESTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_CONNECTION_TIMEOUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_FAILURE:kotlin.Int` |

### onDescriptorReadRequest

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDescriptorReadRequest(
    device: BluetoothDevice!, 
    requestId: Int, 
    offset: Int, 
    descriptor: BluetoothGattDescriptor!
): Unit
```

A remote client has requested to read a local descriptor.

An application must call `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#sendResponse(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.ByteArray)` to complete the request.

| Parameters ||
|---|---|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!: The remote device that has requested the read operation |
| `requestId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The Id of the request |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Offset into the value of the characteristic |
| --- | --- |
| `descriptor` | [BluetoothGattDescriptor](../android/bluetooth/BluetoothGattDescriptor.md)!: Descriptor to be read |

### onDescriptorWriteRequest

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDescriptorWriteRequest(
    device: BluetoothDevice!, 
    requestId: Int, 
    descriptor: BluetoothGattDescriptor!, 
    preparedWrite: Boolean, 
    responseNeeded: Boolean, 
    offset: Int, 
    value: ByteArray!
): Unit
```

A remote client has requested to write to a local descriptor.

An application must call `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#sendResponse(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.ByteArray)` to complete the request.

| Parameters ||
|---|---|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!: The remote device that has requested the write operation |
| `requestId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The Id of the request |
| `descriptor` | [BluetoothGattDescriptor](../android/bluetooth/BluetoothGattDescriptor.md)!: Descriptor to be written to. |
| --- | --- |
| `preparedWrite` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true, if this write operation should be queued for later execution. |
| `responseNeeded` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true, if the remote device requires a response |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset given for the value |
| --- | --- |
| `value` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: The value the client wants to assign to the descriptor |

### onExecuteWrite

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onExecuteWrite(
    device: BluetoothDevice!, 
    requestId: Int, 
    execute: Boolean
): Unit
```

Execute all pending write operations for this device.

An application must call `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#sendResponse(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.ByteArray)` to complete the request.

| Parameters ||
|---|---|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!: The remote device that has requested the write operations |
| `requestId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The Id of the request |
| `execute` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether the pending writes should be executed (true) or cancelled (false) |
| --- | --- |

### onMtuChanged

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onMtuChanged(
    device: BluetoothDevice!, 
    mtu: Int
): Unit
```

Callback indicating the MTU for a given device connection has changed.

This callback will be invoked if a remote client has requested to change the MTU for a given connection.

| Parameters ||
|---|---|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!: The remote device that requested the MTU change |
| `mtu` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new MTU size |

### onNotificationSent

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onNotificationSent(
    device: BluetoothDevice!, 
    status: Int
): Unit
```

Callback invoked when a notification or indication has been sent to a remote device.

When multiple notifications are to be sent, an application must wait for this callback to be received before sending additional notifications.

| Parameters ||
|---|---|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!: The remote device the notification has been sent to |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` if the operation was successful |

### onPhyRead

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPhyRead(
    device: BluetoothDevice!, 
    txPhy: Int, 
    rxPhy: Int, 
    status: Int
): Unit
```

Callback triggered as result of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#readPhy(android.bluetooth.BluetoothDevice)`

| Parameters ||
|---|---|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!: The remote device that requested the PHY read. |
| `txPhy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the transmitter PHY in use. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_1M:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_2M:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_CODED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_HDT:kotlin.Int` |
| `rxPhy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the receiver PHY in use. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_1M:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_2M:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_CODED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_HDT:kotlin.Int` |
| --- | --- |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Status of the PHY read operation. `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` if the operation succeeds. |

### onPhyUpdate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPhyUpdate(
    device: BluetoothDevice!, 
    txPhy: Int, 
    rxPhy: Int, 
    status: Int
): Unit
```

Callback triggered as result of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer#setPreferredPhy(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`, or as a result of remote device changing the PHY.

| Parameters ||
|---|---|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!: The remote device. |
| `txPhy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the transmitter PHY in use. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_1M:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_2M:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_CODED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_HDT:kotlin.Int` |
| `rxPhy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the receiver PHY in use. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_1M:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_2M:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_CODED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_HDT:kotlin.Int` |
| --- | --- |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Status of the PHY update operation. `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` if the operation succeeds. |

### onServiceAdded

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onServiceAdded(
    status: Int, 
    service: BluetoothGattService!
): Unit
```

Indicates whether a local service has been added successfully.

| Parameters ||
|---|---|
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Returns `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` if the service was added successfully. |
| `service` | [BluetoothGattService](../android/bluetooth/BluetoothGattService.md)!: The service that has been added |

### onSubrateChange

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onSubrateChange(
    device: BluetoothDevice, 
    subrateMode: Int, 
    status: Int
): Unit
```

Callback indicating LE connection's subrate parameters have changed.

| Parameters ||
|---|---|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md): The remote device involved. This value cannot be `null`. |
| `subrateMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): for this LE connection. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#SUBRATE_MODE_OFF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#SUBRATE_MODE_LOW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#SUBRATE_MODE_BALANCED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#SUBRATE_MODE_HIGH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#SUBRATE_MODE_SYSTEM_UPDATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#SUBRATE_MODE_NOT_UPDATED:kotlin.Int` |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` if the connection subrating has been updated successfully. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#SUCCESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_UNKNOWN:kotlin.Int` |
| --- | --- |
