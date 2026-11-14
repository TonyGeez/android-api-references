# EncryptionStatus

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EncryptionStatus

Kotlin| [Java](EncryptionStatus.md) 
| --- | --- |

```
class EncryptionStatus
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.EncryptionStatus](EncryptionStatus.md) |

Represents the encryption status of a Bluetooth device.

This class is used to hold the encryption status details like key size and algorithm of a Bluetooth device.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EncryptionStatus](EncryptionStatus.md))`(`keySize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `algorithm:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAlgorithm](EncryptionStatus.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getKeySize](EncryptionStatus.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](EncryptionStatus.md))`()` <br /> |
| --- | --- |

## Public constructors

### EncryptionStatus

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EncryptionStatus(
    keySize: Int, 
    algorithm: Int)
```

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keySize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is between 1 and 16 inclusive |
| `algorithm` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.bluetooth.BluetoothDevice#ENCRYPTION_ALGORITHM_NONE](BluetoothDevice.md), [android.bluetooth.BluetoothDevice#ENCRYPTION_ALGORITHM_E0](BluetoothDevice.md), [android.bluetooth.BluetoothDevice#ENCRYPTION_ALGORITHM_AES](BluetoothDevice.md), or [android.bluetooth.BluetoothDevice#ENCRYPTION_ALGORITHM_UNKNOWN](BluetoothDevice.md) |

## Public methods

### getAlgorithm

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAlgorithm(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the encryption algorithm used for the encrypting the link. Value is [android.bluetooth.BluetoothDevice#ENCRYPTION_ALGORITHM_NONE](BluetoothDevice.md), [android.bluetooth.BluetoothDevice#ENCRYPTION_ALGORITHM_E0](BluetoothDevice.md), [android.bluetooth.BluetoothDevice#ENCRYPTION_ALGORITHM_AES](BluetoothDevice.md), or [android.bluetooth.BluetoothDevice#ENCRYPTION_ALGORITHM_UNKNOWN](BluetoothDevice.md) |

### getKeySize

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getKeySize(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the size of the encryption key, in number of bytes. i.e. value of 16 means 16-octets, or 128 bit key size. Value is between 1 and 16 inclusive |

### toString

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
