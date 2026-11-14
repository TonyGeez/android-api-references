# ScanCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScanCallback

Kotlin| [Java](../android/bluetooth/le/ScanCallback.md) 
| --- | --- |

```
abstract class ScanCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.le.ScanCallback](../android/bluetooth/le/ScanCallback.md) |

Bluetooth LE scan callbacks. Scan results are reported using these callbacks.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCAN_FAILED_ALREADY_STARTED](../android/bluetooth/le/ScanCallback.md) Fails to start scan as BLE scan with the same settings is already started by the app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCAN_FAILED_APPLICATION_REGISTRATION_FAILED](../android/bluetooth/le/ScanCallback.md) Fails to start scan as app cannot be registered. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCAN_FAILED_FEATURE_UNSUPPORTED](../android/bluetooth/le/ScanCallback.md) Fails to start power optimized scan as this feature is not supported. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCAN_FAILED_INTERNAL_ERROR](../android/bluetooth/le/ScanCallback.md) Fails to start scan due an internal error |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCAN_FAILED_OUT_OF_HARDWARE_RESOURCES](../android/bluetooth/le/ScanCallback.md) Fails to start scan as it is out of hardware resources. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCAN_FAILED_SCANNING_TOO_FREQUENTLY](../android/bluetooth/le/ScanCallback.md) Fails to start scan as application tries to scan too frequently. |
| --- | --- |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------|---|
| [ScanCallback](../android/bluetooth/le/ScanCallback.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBatchScanResults](../android/bluetooth/le/ScanCallback.md))`(`results:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ScanResult](../android/bluetooth/le/ScanResult.md)!>!`)` Callback when batch results are delivered. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScanFailed](../android/bluetooth/le/ScanCallback.md))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback when scan could not be started. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScanResult](../android/bluetooth/le/ScanCallback.md))`(`callbackType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `result:` ` [ScanResult](../android/bluetooth/le/ScanResult.md)!`)` Callback when a BLE advertisement has been found. |
| --- | --- |

## Constants

### SCAN_FAILED_ALREADY_STARTED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCAN_FAILED_ALREADY_STARTED: Int
```

Fails to start scan as BLE scan with the same settings is already started by the app. 

 Value: 1

### SCAN_FAILED_APPLICATION_REGISTRATION_FAILED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCAN_FAILED_APPLICATION_REGISTRATION_FAILED: Int
```

Fails to start scan as app cannot be registered. 

 Value: 2

### SCAN_FAILED_FEATURE_UNSUPPORTED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCAN_FAILED_FEATURE_UNSUPPORTED: Int
```

Fails to start power optimized scan as this feature is not supported. 

 Value: 4

### SCAN_FAILED_INTERNAL_ERROR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCAN_FAILED_INTERNAL_ERROR: Int
```

Fails to start scan due an internal error 

 Value: 3

### SCAN_FAILED_OUT_OF_HARDWARE_RESOURCES

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCAN_FAILED_OUT_OF_HARDWARE_RESOURCES: Int
```

Fails to start scan as it is out of hardware resources. 

 Value: 5

### SCAN_FAILED_SCANNING_TOO_FREQUENTLY

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCAN_FAILED_SCANNING_TOO_FREQUENTLY: Int
```

Fails to start scan as application tries to scan too frequently. 

 Value: 6

## Public constructors

### ScanCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ScanCallback()
```

## Public methods

### onBatchScanResults

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onBatchScanResults(results: MutableList<ScanResult!>!): Unit
```

Callback when batch results are delivered.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `results` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ScanResult](../android/bluetooth/le/ScanResult.md)!\>!:List of scan results that are previously scanned. |

### onScanFailed

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onScanFailed(errorCode: Int): Unit
```

Callback when scan could not be started.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Error code (one of SCAN_FAILED_\*) for scan failure. Value is [android.bluetooth.le.ScanCallback#SCAN_FAILED_ALREADY_STARTED](../android/bluetooth/le/ScanCallback.md), [android.bluetooth.le.ScanCallback#SCAN_FAILED_APPLICATION_REGISTRATION_FAILED](../android/bluetooth/le/ScanCallback.md), [android.bluetooth.le.ScanCallback#SCAN_FAILED_INTERNAL_ERROR](../android/bluetooth/le/ScanCallback.md), [android.bluetooth.le.ScanCallback#SCAN_FAILED_FEATURE_UNSUPPORTED](../android/bluetooth/le/ScanCallback.md), [android.bluetooth.le.ScanCallback#SCAN_FAILED_OUT_OF_HARDWARE_RESOURCES](../android/bluetooth/le/ScanCallback.md), or [android.bluetooth.le.ScanCallback#SCAN_FAILED_SCANNING_TOO_FREQUENTLY](../android/bluetooth/le/ScanCallback.md) |

### onScanResult

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onScanResult(
    callbackType: Int, 
    result: ScanResult!
): Unit
```

Callback when a BLE advertisement has been found.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callbackType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Determines how this callback was triggered. Could be one of [android.bluetooth.le.ScanSettings#CALLBACK_TYPE_ALL_MATCHES](../android/bluetooth/le/ScanSettings.md), [ScanSettings.CALLBACK_TYPE_FIRST_MATCH](../android/bluetooth/le/ScanSettings.md) or [ScanSettings.CALLBACK_TYPE_MATCH_LOST](../android/bluetooth/le/ScanSettings.md) |
| `result` | [ScanResult](../android/bluetooth/le/ScanResult.md)!:A Bluetooth LE scan result. |
