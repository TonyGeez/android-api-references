# BluetoothStatusCodes

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothStatusCodes

Kotlin | [Java](BluetoothStatusCodes.md) 
| --- | --- |

```
class BluetoothStatusCodes
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothStatusCodes](BluetoothStatusCodes.md) |

A class with constants representing possible return values for Bluetooth APIs. General return values occupy the range 0 to 199. Profile-specific return values occupy the range 200-999. API-specific return values start at 1000. The exception to this is the "UNKNOWN" error code which occupies the max integer value.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_BLUETOOTH_NOT_ALLOWED](BluetoothStatusCodes.md) Error code indicating that the API call was initiated by neither the system nor the active user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_BLUETOOTH_NOT_ENABLED](BluetoothStatusCodes.md) Error code indicating that Bluetooth is not enabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DEVICE_NOT_BONDED](BluetoothStatusCodes.md) Error code indicating that the Bluetooth Device specified is not bonded. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_GATT_WRITE_NOT_ALLOWED](BluetoothStatusCodes.md) A GATT writeCharacteristic request is not permitted on the remote device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_GATT_WRITE_REQUEST_BUSY](BluetoothStatusCodes.md) A GATT writeCharacteristic request is issued to a busy remote device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_MISSING_BLUETOOTH_CONNECT_PERMISSION](BluetoothStatusCodes.md) Error code indicating that the caller does not have the [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_PROFILE_SERVICE_NOT_BOUND](BluetoothStatusCodes.md) Error code indicating that the profile service is not bound. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNKNOWN](BluetoothStatusCodes.md) Indicates that an unknown error has occurred. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FEATURE_NOT_CONFIGURED](BluetoothStatusCodes.md) Indicates that the feature status is not configured yet. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FEATURE_NOT_SUPPORTED](BluetoothStatusCodes.md) Indicates that the feature is not supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FEATURE_SUPPORTED](BluetoothStatusCodes.md) Indicates that the feature is supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](BluetoothStatusCodes.md) Indicates that the API call was successful. |
| --- | --- |

## Constants

### ERROR_BLUETOOTH_NOT_ALLOWED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_BLUETOOTH_NOT_ALLOWED: Int
```

Error code indicating that the API call was initiated by neither the system nor the active user. 

 Value: 2

### ERROR_BLUETOOTH_NOT_ENABLED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_BLUETOOTH_NOT_ENABLED: Int
```

Error code indicating that Bluetooth is not enabled. 

 Value: 1

### ERROR_DEVICE_NOT_BONDED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_DEVICE_NOT_BONDED: Int
```

Error code indicating that the Bluetooth Device specified is not bonded. 

 Value: 3

### ERROR_GATT_WRITE_NOT_ALLOWED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_GATT_WRITE_NOT_ALLOWED: Int
```

A GATT writeCharacteristic request is not permitted on the remote device. 

 Value: 200

### ERROR_GATT_WRITE_REQUEST_BUSY

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_GATT_WRITE_REQUEST_BUSY: Int
```

A GATT writeCharacteristic request is issued to a busy remote device. 

 Value: 201

### ERROR_MISSING_BLUETOOTH_CONNECT_PERMISSION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_MISSING_BLUETOOTH_CONNECT_PERMISSION: Int
```

Error code indicating that the caller does not have the [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission. 

 Value: 6

### ERROR_PROFILE_SERVICE_NOT_BOUND

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_PROFILE_SERVICE_NOT_BOUND: Int
```

Error code indicating that the profile service is not bound. You can bind a profile service by calling [BluetoothAdapter.getProfileProxy](BluetoothAdapter.md)). 

 Value: 9

### ERROR_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_UNKNOWN: Int
```

Indicates that an unknown error has occurred. 

 Value: 2147483647

### FEATURE_NOT_CONFIGURED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_NOT_CONFIGURED: Int
```

Indicates that the feature status is not configured yet. 

 Value: 30

### FEATURE_NOT_SUPPORTED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_NOT_SUPPORTED: Int
```

Indicates that the feature is not supported. 

 Value: 11

### FEATURE_SUPPORTED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_SUPPORTED: Int
```

Indicates that the feature is supported. 

 Value: 10

### SUCCESS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUCCESS: Int
```

Indicates that the API call was successful. 

 Value: 0
