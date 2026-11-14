# BluetoothSocketSettings

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothSocketSettings

Kotlin| [Java](https://developer.android.com/reference/android/bluetooth/BluetoothSocketSettings "View this page in Java") 

```
class BluetoothSocketSettings
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.bluetooth.BluetoothSocketSettings](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketSettings#) |

Defines parameters for creating Bluetooth server and client socket channels.

Used with [BluetoothAdapter.listenUsingSocketSettings](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingSocketSettings(android.bluetooth.BluetoothSocketSettings))to create a server socket and [BluetoothDevice.createUsingSocketSettings](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createUsingSocketSettings(android.bluetooth.BluetoothSocketSettings))to create a client socket.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketSettings.Builder) Builder for [BluetoothSocketSettings](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketSettings#). |

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getL2capPsm](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketSettings#getL2capPsm())`()` Returns the L2CAP PSM value used for a BluetoothSocket#TYPE_LE socket. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getRfcommServiceName](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketSettings#getRfcommServiceName())`()` Returns the RFCOMM service name used for a BluetoothSocket#TYPE_RFCOMM socket. |
| [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)? | [getRfcommUuid](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketSettings#getRfcommUuid())`()` Returns the RFCOMM service UUID used for a BluetoothSocket#TYPE_RFCOMM socket. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSocketType](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketSettings#getSocketType())`()` Returns the type of the Bluetooth socket. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAuthenticationRequired](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketSettings#isAuthenticationRequired())`()` Checks if authentication is enabled for the Bluetooth socket. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEncryptionRequired](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketSettings#isEncryptionRequired())`()` Checks if encryption is enabled for the Bluetooth socket. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketSettings#toString())`()` Returns a [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) that describes each BluetoothSocketSettings parameter current value. |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.bluetooth.BluetoothSocket#TYPE_RFCOMM](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#TYPE_RFCOMM:kotlin.Int), [android.bluetooth.BluetoothSocket#TYPE_SCO](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#TYPE_SCO:kotlin.Int), [android.bluetooth.BluetoothSocket#TYPE_L2CAP](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#TYPE_L2CAP:kotlin.Int), or [android.bluetooth.BluetoothSocket#TYPE_LE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#TYPE_LE:kotlin.Int) |

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

Returns a [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) that describes each BluetoothSocketSettings parameter current value.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
