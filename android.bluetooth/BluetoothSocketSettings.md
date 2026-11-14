# BluetoothSocketSettings

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothSocketSettings

Kotlin| [Java](../android/bluetooth/BluetoothSocketSettings.md) 
| --- | --- |

```
class BluetoothSocketSettings
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothSocketSettings](../android/bluetooth/BluetoothSocketSettings.md) |

Defines parameters for creating Bluetooth server and client socket channels.

Used with [BluetoothAdapter.listenUsingSocketSettings](../android/bluetooth/BluetoothAdapter.md))to create a server socket and [BluetoothDevice.createUsingSocketSettings](../android/bluetooth/BluetoothDevice.md))to create a client socket.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/bluetooth/BluetoothSocketSettings.Builder.md) Builder for [BluetoothSocketSettings](../android/bluetooth/BluetoothSocketSettings.md). |

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getL2capPsm](../android/bluetooth/BluetoothSocketSettings.md))`()` Returns the L2CAP PSM value used for a BluetoothSocket#TYPE_LE socket. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getRfcommServiceName](../android/bluetooth/BluetoothSocketSettings.md))`()` Returns the RFCOMM service name used for a BluetoothSocket#TYPE_RFCOMM socket. |
| [UUID](../java/util/UUID.md)? | [getRfcommUuid](../android/bluetooth/BluetoothSocketSettings.md))`()` Returns the RFCOMM service UUID used for a BluetoothSocket#TYPE_RFCOMM socket. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSocketType](../android/bluetooth/BluetoothSocketSettings.md))`()` Returns the type of the Bluetooth socket. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAuthenticationRequired](../android/bluetooth/BluetoothSocketSettings.md))`()` Checks if authentication is enabled for the Bluetooth socket. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEncryptionRequired](../android/bluetooth/BluetoothSocketSettings.md))`()` Checks if encryption is enabled for the Bluetooth socket. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/bluetooth/BluetoothSocketSettings.md))`()` Returns a [String](../java/lang/String.md) that describes each BluetoothSocketSettings parameter current value. |

## Public methods

### getL2capPsm

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getL2capPsm(): Int
```

Returns the L2CAP PSM value used for a BluetoothSocket#TYPE_LE socket.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is between 128 and 255 inclusive |

### getRfcommServiceName

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRfcommServiceName(): String?
```

Returns the RFCOMM service name used for a BluetoothSocket#TYPE_RFCOMM socket.

Defaults to`null`. 

### getRfcommUuid

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRfcommUuid(): UUID?
```

Returns the RFCOMM service UUID used for a BluetoothSocket#TYPE_RFCOMM socket.

Defaults to`null`. 

### getSocketType

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSocketType(): Int
```

Returns the type of the Bluetooth socket.

Defaults to`BluetoothSocket#TYPE_RFCOMM`.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.bluetooth.BluetoothSocket#TYPE_RFCOMM](../android/bluetooth/BluetoothSocket.md), [android.bluetooth.BluetoothSocket#TYPE_SCO](../android/bluetooth/BluetoothSocket.md), [android.bluetooth.BluetoothSocket#TYPE_L2CAP](../android/bluetooth/BluetoothSocket.md), or [android.bluetooth.BluetoothSocket#TYPE_LE](../android/bluetooth/BluetoothSocket.md) |

### isAuthenticationRequired

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAuthenticationRequired(): Boolean
```

Checks if authentication is enabled for the Bluetooth socket.

Defaults to`false`. 

### isEncryptionRequired

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isEncryptionRequired(): Boolean
```

Checks if encryption is enabled for the Bluetooth socket.

Defaults to`false`. 

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a [String](../java/lang/String.md) that describes each BluetoothSocketSettings parameter current value.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
