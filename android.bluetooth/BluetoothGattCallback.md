Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothGattCallback

```
abstract class BluetoothGattCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.bluetooth.BluetoothGattCallback](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#) |

This abstract class is used to implement `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt` callbacks.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#BluetoothGattCallback()()` <br /> |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onCharacteristicChanged(android.bluetooth.BluetoothGatt,%20android.bluetooth.BluetoothGattCharacteristic)(gatt: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt!, characteristic: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic!)` Callback triggered as a result of a remote characteristic notification. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onCharacteristicChanged(android.bluetooth.BluetoothGatt,%20android.bluetooth.BluetoothGattCharacteristic,%20kotlin.ByteArray)(gatt: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt, characteristic: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)` Callback triggered as a result of a remote characteristic notification. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onCharacteristicRead(android.bluetooth.BluetoothGatt,%20android.bluetooth.BluetoothGattCharacteristic,%20kotlin.ByteArray,%20kotlin.Int)(gatt: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt, characteristic: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html, status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Callback reporting the result of a characteristic read operation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onCharacteristicRead(android.bluetooth.BluetoothGatt,%20android.bluetooth.BluetoothGattCharacteristic,%20kotlin.Int)(gatt: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt!, characteristic: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic!, status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Callback reporting the result of a characteristic read operation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onCharacteristicWrite(android.bluetooth.BluetoothGatt,%20android.bluetooth.BluetoothGattCharacteristic,%20kotlin.Int)(gatt: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt!, characteristic: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic!, status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Callback indicating the result of a characteristic write operation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onConnectionStateChange(android.bluetooth.BluetoothGatt,%20kotlin.Int,%20kotlin.Int)(gatt: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt!, status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, newState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Callback indicating when GATT client has connected/disconnected to/from a remote GATT server. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onConnectionUpdated(android.bluetooth.BluetoothGatt,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(gatt: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt, interval: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, latency: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, supervisionTimeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Callback indicating the connection parameters were updated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onDescriptorRead(android.bluetooth.BluetoothGatt,%20android.bluetooth.BluetoothGattDescriptor,%20kotlin.Int)(gatt: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt!, descriptor: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor!, status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Callback reporting the result of a descriptor read operation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onDescriptorRead(android.bluetooth.BluetoothGatt,%20android.bluetooth.BluetoothGattDescriptor,%20kotlin.Int,%20kotlin.ByteArray)(gatt: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt, descriptor: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor, status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)` Callback reporting the result of a descriptor read operation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onDescriptorWrite(android.bluetooth.BluetoothGatt,%20android.bluetooth.BluetoothGattDescriptor,%20kotlin.Int)(gatt: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt!, descriptor: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor!, status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Callback indicating the result of a descriptor write operation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onMtuChanged(android.bluetooth.BluetoothGatt,%20kotlin.Int,%20kotlin.Int)(gatt: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt!, mtu: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Callback indicating the MTU for a given device connection has changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onPhyRead(android.bluetooth.BluetoothGatt,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(gatt: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt!, txPhy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, rxPhy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Callback triggered as result of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#readPhy()` |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onPhyUpdate(android.bluetooth.BluetoothGatt,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(gatt: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt!, txPhy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, rxPhy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Callback triggered as result of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#setPreferredPhy(kotlin.Int,%20kotlin.Int,%20kotlin.Int)`, or as a result of remote device changing the PHY. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onReadRemoteRssi(android.bluetooth.BluetoothGatt,%20kotlin.Int,%20kotlin.Int)(gatt: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt!, rssi: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Callback reporting the RSSI for a remote device connection. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onReliableWriteCompleted(android.bluetooth.BluetoothGatt,%20kotlin.Int)(gatt: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt!, status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Callback invoked when a reliable write transaction has been completed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onServiceChanged(android.bluetooth.BluetoothGatt)(gatt: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt)` Callback indicating service changed event is received |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onServicesDiscovered(android.bluetooth.BluetoothGatt,%20kotlin.Int)(gatt: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt!, status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Callback invoked when the list of remote services, characteristics and descriptors for the remote device have been updated, ie new services have been discovered. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onSubrateChange(android.bluetooth.BluetoothGatt,%20kotlin.Int,%20kotlin.Int)(gatt: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt, subrateMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Callback indicating LE connection's subrate parameters have changed. |

## Public constructors

### BluetoothGattCallback

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BluetoothGattCallback()
```

## Public methods

### onCharacteristicChanged

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCharacteristicChanged(
    gatt: BluetoothGatt!, 
    characteristic: BluetoothGattCharacteristic!
): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onCharacteristicChanged(android.bluetooth.BluetoothGatt,%20android.bluetooth.BluetoothGattCharacteristic,%20kotlin.ByteArray)` as it is memory safe by providing the characteristic value at the time of notification.*

Callback triggered as a result of a remote characteristic notification.

| Parameters ||
|---|---|
| `gatt` | [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt)!: GATT client the characteristic is associated with |
| `characteristic` | [BluetoothGattCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic)!: Characteristic that has been updated as a result of a remote notification event. |

### onCharacteristicChanged

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCharacteristicChanged(
    gatt: BluetoothGatt, 
    characteristic: BluetoothGattCharacteristic, 
    value: ByteArray
): Unit
```

Callback triggered as a result of a remote characteristic notification. Note that the value within the characteristic object may have changed since receiving the remote characteristic notification, so check the parameter value for the value at the time of notification.

| Parameters ||
|---|---|
| `gatt` | [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt): GATT client the characteristic is associated with. This value cannot be `null`. |
| `characteristic` | [BluetoothGattCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic): Characteristic that has been updated as a result of a remote notification event. This value cannot be `null`. |
| `value` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): notified characteristic value. This value cannot be `null`. |

### onCharacteristicRead

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCharacteristicRead(
    gatt: BluetoothGatt, 
    characteristic: BluetoothGattCharacteristic, 
    value: ByteArray, 
    status: Int
): Unit
```

Callback reporting the result of a characteristic read operation.

| Parameters ||
|---|---|
| `gatt` | [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt): GATT client invoked `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#readCharacteristic(android.bluetooth.BluetoothGattCharacteristic)` This value cannot be `null`. |
| `characteristic` | [BluetoothGattCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic): Characteristic that was read from the associated remote device. This value cannot be `null`. |
| `value` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the value of the characteristic. This value cannot be `null`. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` if the read operation was completed successfully. |

### onCharacteristicRead

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCharacteristicRead(
    gatt: BluetoothGatt!, 
    characteristic: BluetoothGattCharacteristic!, 
    status: Int
): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onCharacteristicRead(android.bluetooth.BluetoothGatt,%20android.bluetooth.BluetoothGattCharacteristic,%20kotlin.ByteArray,%20kotlin.Int)` as it is memory safe*

Callback reporting the result of a characteristic read operation.

| Parameters ||
|---|---|
| `gatt` | [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt)!: GATT client invoked `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#readCharacteristic(android.bluetooth.BluetoothGattCharacteristic)` |
| `characteristic` | [BluetoothGattCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic)!: Characteristic that was read from the associated remote device. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` if the read operation was completed successfully. |

### onCharacteristicWrite

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCharacteristicWrite(
    gatt: BluetoothGatt!, 
    characteristic: BluetoothGattCharacteristic!, 
    status: Int
): Unit
```

Callback indicating the result of a characteristic write operation.

If this callback is invoked while a reliable write transaction is in progress, the value of the characteristic represents the value reported by the remote device. An application should compare this value to the desired value to be written. If the values don't match, the application must abort the reliable write transaction.

| Parameters ||
|---|---|
| `gatt` | [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt)!: GATT client that invoked `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#writeCharacteristic(android.bluetooth.BluetoothGattCharacteristic,%20kotlin.ByteArray,%20kotlin.Int)` |
| `characteristic` | [BluetoothGattCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic)!: Characteristic that was written to the associated remote device. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The result of the write operation `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` if the operation succeeds. |

### onConnectionStateChange

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onConnectionStateChange(
    gatt: BluetoothGatt!, 
    status: Int, 
    newState: Int
): Unit
```

Callback indicating when GATT client has connected/disconnected to/from a remote GATT server.

| Parameters ||
|---|---|
| `gatt` | [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt)!: GATT client |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Status of the connect or disconnect operation. `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` if the operation succeeds. |
| `newState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Returns the new connection state. Can be one of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int` |

### onConnectionUpdated

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onConnectionUpdated(
    gatt: BluetoothGatt, 
    interval: Int, 
    latency: Int, 
    supervisionTimeout: Int, 
    status: Int
): Unit
```

Callback indicating the connection parameters were updated.

| Parameters ||
|---|---|
| `gatt` | [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt): GATT client involved. This value cannot be `null`. |
| `interval` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Connection interval used on this connection, 1.25ms unit. Valid range is from 6 (7.5ms) to 3200 (4000ms). Value is between 6 and 3200 inclusive |
| `latency` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Worker latency for the connection in number of connection events. Valid range is from 0 to 499. Value is between 0 and 499 inclusive |
| `supervisionTimeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Supervision timeout for this connection, in 10ms unit. Valid range is from 10 (0.1s) to 3200 (32s). Value is between 10 and 3200 inclusive |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` if the connection has been updated successfully. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_READ_NOT_PERMITTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_WRITE_NOT_PERMITTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_INSUFFICIENT_AUTHENTICATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_REQUEST_NOT_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_INSUFFICIENT_ENCRYPTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_INVALID_OFFSET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_INSUFFICIENT_AUTHORIZATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_INVALID_ATTRIBUTE_LENGTH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_CONNECTION_CONGESTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_CONNECTION_TIMEOUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_FAILURE:kotlin.Int` |

### onDescriptorRead

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDescriptorRead(
    gatt: BluetoothGatt!, 
    descriptor: BluetoothGattDescriptor!, 
    status: Int
): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback#onDescriptorRead(android.bluetooth.BluetoothGatt,%20android.bluetooth.BluetoothGattDescriptor,%20kotlin.Int,%20kotlin.ByteArray)` as it is memory safe by providing the descriptor value at the time it was read.*

Callback reporting the result of a descriptor read operation.

| Parameters ||
|---|---|
| `gatt` | [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt)!: GATT client invoked `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#readDescriptor(android.bluetooth.BluetoothGattDescriptor)` |
| `descriptor` | [BluetoothGattDescriptor](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor)!: Descriptor that was read from the associated remote device. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` if the read operation was completed successfully |

### onDescriptorRead

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDescriptorRead(
    gatt: BluetoothGatt, 
    descriptor: BluetoothGattDescriptor, 
    status: Int, 
    value: ByteArray
): Unit
```

Callback reporting the result of a descriptor read operation.

| Parameters ||
|---|---|
| `gatt` | [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt): GATT client invoked `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#readDescriptor(android.bluetooth.BluetoothGattDescriptor)` This value cannot be `null`. |
| `descriptor` | [BluetoothGattDescriptor](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor): Descriptor that was read from the associated remote device. This value cannot be `null`. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` if the read operation was completed successfully |
| `value` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the descriptor value at the time of the read operation. This value cannot be `null`. |

### onDescriptorWrite

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDescriptorWrite(
    gatt: BluetoothGatt!, 
    descriptor: BluetoothGattDescriptor!, 
    status: Int
): Unit
```

Callback indicating the result of a descriptor write operation.

| Parameters ||
|---|---|
| `gatt` | [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt)!: GATT client invoked android.bluetooth.BluetoothGatt#writeDescriptor |
| `descriptor` | [BluetoothGattDescriptor](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor)!: Descriptor that was written to the associated remote device. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The result of the write operation `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` if the operation succeeds. |

### onMtuChanged

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onMtuChanged(
    gatt: BluetoothGatt!, 
    mtu: Int, 
    status: Int
): Unit
```

Callback indicating the MTU for a given device connection has changed.

This callback is triggered in response to the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#requestMtu(kotlin.Int)` function, or in response to a connection event.

| Parameters ||
|---|---|
| `gatt` | [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt)!: GATT client invoked `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#requestMtu(kotlin.Int)` |
| `mtu` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new MTU size |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` if the MTU has been changed successfully |

### onPhyRead

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPhyRead(
    gatt: BluetoothGatt!, 
    txPhy: Int, 
    rxPhy: Int, 
    status: Int
): Unit
```

Callback triggered as result of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#readPhy()`

| Parameters ||
|---|---|
| `gatt` | [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt)!: GATT client |
| `txPhy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the transmitter PHY in use. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_1M:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_2M:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_CODED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_HDT:kotlin.Int` |
| `rxPhy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the receiver PHY in use. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_1M:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_2M:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_CODED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_HDT:kotlin.Int` |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Status of the PHY read operation. `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` if the operation succeeds. |

### onPhyUpdate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPhyUpdate(
    gatt: BluetoothGatt!, 
    txPhy: Int, 
    rxPhy: Int, 
    status: Int
): Unit
```

Callback triggered as result of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#setPreferredPhy(kotlin.Int,%20kotlin.Int,%20kotlin.Int)`, or as a result of remote device changing the PHY.

| Parameters ||
|---|---|
| `gatt` | [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt)!: GATT client |
| `txPhy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the transmitter PHY in use. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_1M:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_2M:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_CODED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_HDT:kotlin.Int` |
| `rxPhy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the receiver PHY in use. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_1M:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_2M:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_CODED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_HDT:kotlin.Int` |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Status of the PHY update operation. `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` if the operation succeeds. |

### onReadRemoteRssi

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onReadRemoteRssi(
    gatt: BluetoothGatt!, 
    rssi: Int, 
    status: Int
): Unit
```

Callback reporting the RSSI for a remote device connection.

This callback is triggered in response to the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#readRemoteRssi()` function.

| Parameters ||
|---|---|
| `gatt` | [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt)!: GATT client invoked `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#readRemoteRssi()` |
| `rssi` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The RSSI value for the remote device |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` if the RSSI was read successfully |

### onReliableWriteCompleted

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onReliableWriteCompleted(
    gatt: BluetoothGatt!, 
    status: Int
): Unit
```

Callback invoked when a reliable write transaction has been completed.

| Parameters ||
|---|---|
| `gatt` | [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt)!: GATT client invoked `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#executeReliableWrite()` |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` if the reliable write transaction was executed successfully |

### onServiceChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onServiceChanged(gatt: BluetoothGatt): Unit
```

Callback indicating service changed event is received

Receiving this event means that the GATT database is out of sync with the remote device. `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#discoverServices()` should be called to re-discover the services.

| Parameters ||
|---|---|
| `gatt` | [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt): GATT client involved. This value cannot be `null`. |

### onServicesDiscovered

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onServicesDiscovered(
    gatt: BluetoothGatt!, 
    status: Int
): Unit
```

Callback invoked when the list of remote services, characteristics and descriptors for the remote device have been updated, ie new services have been discovered.

| Parameters ||
|---|---|
| `gatt` | [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt)!: GATT client invoked `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#discoverServices()` |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` if the remote device has been explored successfully. |

### onSubrateChange

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onSubrateChange(
    gatt: BluetoothGatt, 
    subrateMode: Int, 
    status: Int
): Unit
```

Callback indicating LE connection's subrate parameters have changed.

| Parameters ||
|---|---|
| `gatt` | [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt): The remote device involved. This value cannot be `null`. |
| `subrateMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): for this LE connection. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#SUBRATE_MODE_OFF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#SUBRATE_MODE_LOW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#SUBRATE_MODE_BALANCED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#SUBRATE_MODE_HIGH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#SUBRATE_MODE_SYSTEM_UPDATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#SUBRATE_MODE_NOT_UPDATED:kotlin.Int` |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#GATT_SUCCESS:kotlin.Int` if the connection subrating has been updated successfully. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#SUCCESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_UNKNOWN:kotlin.Int` |
