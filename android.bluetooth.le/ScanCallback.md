# ScanCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScanCallback

Kotlin| [Java](https://developer.android.com/reference/android/bluetooth/le/ScanCallback "View this page in Java") 

```
abstract class ScanCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.bluetooth.le.ScanCallback](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback#) |

Bluetooth LE scan callbacks. Scan results are reported using these callbacks.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCAN_FAILED_ALREADY_STARTED](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback#SCAN_FAILED_ALREADY_STARTED:kotlin.Int) Fails to start scan as BLE scan with the same settings is already started by the app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCAN_FAILED_APPLICATION_REGISTRATION_FAILED](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback#SCAN_FAILED_APPLICATION_REGISTRATION_FAILED:kotlin.Int) Fails to start scan as app cannot be registered. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCAN_FAILED_FEATURE_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback#SCAN_FAILED_FEATURE_UNSUPPORTED:kotlin.Int) Fails to start power optimized scan as this feature is not supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCAN_FAILED_INTERNAL_ERROR](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback#SCAN_FAILED_INTERNAL_ERROR:kotlin.Int) Fails to start scan due an internal error |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCAN_FAILED_OUT_OF_HARDWARE_RESOURCES](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback#SCAN_FAILED_OUT_OF_HARDWARE_RESOURCES:kotlin.Int) Fails to start scan as it is out of hardware resources. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCAN_FAILED_SCANNING_TOO_FREQUENTLY](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback#SCAN_FAILED_SCANNING_TOO_FREQUENTLY:kotlin.Int) Fails to start scan as application tries to scan too frequently. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------|---|
| [ScanCallback](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback#ScanCallback())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBatchScanResults](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback#onBatchScanResults(kotlin.collections.MutableList))`(`results:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ScanResult](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult)!>!`)` Callback when batch results are delivered. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScanFailed](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback#onScanFailed(kotlin.Int))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback when scan could not be started. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScanResult](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback#onScanResult(kotlin.Int,%20android.bluetooth.le.ScanResult))`(`callbackType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `result:` ` [ScanResult](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult)!`)` Callback when a BLE advertisement has been found. |

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
| `results` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ScanResult](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult)!\>!:List of scan results that are previously scanned. |

### onScanFailed

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onScanFailed(errorCode: Int): Unit
```

Callback when scan could not be started.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Error code (one of SCAN_FAILED_\*) for scan failure. Value is [android.bluetooth.le.ScanCallback#SCAN_FAILED_ALREADY_STARTED](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback#SCAN_FAILED_ALREADY_STARTED:kotlin.Int), [android.bluetooth.le.ScanCallback#SCAN_FAILED_APPLICATION_REGISTRATION_FAILED](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback#SCAN_FAILED_APPLICATION_REGISTRATION_FAILED:kotlin.Int), [android.bluetooth.le.ScanCallback#SCAN_FAILED_INTERNAL_ERROR](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback#SCAN_FAILED_INTERNAL_ERROR:kotlin.Int), [android.bluetooth.le.ScanCallback#SCAN_FAILED_FEATURE_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback#SCAN_FAILED_FEATURE_UNSUPPORTED:kotlin.Int), [android.bluetooth.le.ScanCallback#SCAN_FAILED_OUT_OF_HARDWARE_RESOURCES](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback#SCAN_FAILED_OUT_OF_HARDWARE_RESOURCES:kotlin.Int), or [android.bluetooth.le.ScanCallback#SCAN_FAILED_SCANNING_TOO_FREQUENTLY](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanCallback#SCAN_FAILED_SCANNING_TOO_FREQUENTLY:kotlin.Int) |

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
| `callbackType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Determines how this callback was triggered. Could be one of [android.bluetooth.le.ScanSettings#CALLBACK_TYPE_ALL_MATCHES](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#CALLBACK_TYPE_ALL_MATCHES:kotlin.Int), [ScanSettings.CALLBACK_TYPE_FIRST_MATCH](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#CALLBACK_TYPE_FIRST_MATCH:kotlin.Int) or [ScanSettings.CALLBACK_TYPE_MATCH_LOST](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#CALLBACK_TYPE_MATCH_LOST:kotlin.Int) |
| `result` | [ScanResult](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult)!:A Bluetooth LE scan result. |
