# EncryptionStatus

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EncryptionStatus

Kotlin| [Java](https://developer.android.com/reference/android/bluetooth/EncryptionStatus "View this page in Java") 

```
class EncryptionStatus
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.bluetooth.EncryptionStatus](https://developer.android.com/reference/kotlin/android/bluetooth/EncryptionStatus#) |

Represents the encryption status of a Bluetooth device.

This class is used to hold the encryption status details like key size and algorithm of a Bluetooth device.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EncryptionStatus](https://developer.android.com/reference/kotlin/android/bluetooth/EncryptionStatus#EncryptionStatus(kotlin.Int,%20kotlin.Int))`(`keySize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `algorithm:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAlgorithm](https://developer.android.com/reference/kotlin/android/bluetooth/EncryptionStatus#getAlgorithm())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getKeySize](https://developer.android.com/reference/kotlin/android/bluetooth/EncryptionStatus#getKeySize())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/bluetooth/EncryptionStatus#toString())`()` <br /> |

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
| `algorithm` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.bluetooth.BluetoothDevice#ENCRYPTION_ALGORITHM_NONE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ENCRYPTION_ALGORITHM_NONE:kotlin.Int), [android.bluetooth.BluetoothDevice#ENCRYPTION_ALGORITHM_E0](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ENCRYPTION_ALGORITHM_E0:kotlin.Int), [android.bluetooth.BluetoothDevice#ENCRYPTION_ALGORITHM_AES](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ENCRYPTION_ALGORITHM_AES:kotlin.Int), or [android.bluetooth.BluetoothDevice#ENCRYPTION_ALGORITHM_UNKNOWN](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ENCRYPTION_ALGORITHM_UNKNOWN:kotlin.Int) |

## Public methods

### getAlgorithm

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAlgorithm(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the encryption algorithm used for the encrypting the link. Value is [android.bluetooth.BluetoothDevice#ENCRYPTION_ALGORITHM_NONE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ENCRYPTION_ALGORITHM_NONE:kotlin.Int), [android.bluetooth.BluetoothDevice#ENCRYPTION_ALGORITHM_E0](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ENCRYPTION_ALGORITHM_E0:kotlin.Int), [android.bluetooth.BluetoothDevice#ENCRYPTION_ALGORITHM_AES](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ENCRYPTION_ALGORITHM_AES:kotlin.Int), or [android.bluetooth.BluetoothDevice#ENCRYPTION_ALGORITHM_UNKNOWN](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ENCRYPTION_ALGORITHM_UNKNOWN:kotlin.Int) |

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
