# AdvertisingSetCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AdvertisingSetCallback

Kotlin| [Java](https://developer.android.com/reference/android/bluetooth/le/AdvertisingSetCallback "View this page in Java") 

```
abstract class AdvertisingSetCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.bluetooth.le.AdvertisingSetCallback](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback#) |

Bluetooth LE advertising set callbacks, used to deliver advertising operation status.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_FAILED_ALREADY_STARTED](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback#ADVERTISE_FAILED_ALREADY_STARTED:kotlin.Int) Failed to start advertising as the advertising is already started. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_FAILED_DATA_TOO_LARGE](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback#ADVERTISE_FAILED_DATA_TOO_LARGE:kotlin.Int) Failed to start advertising as the advertise data to be broadcasted is too large. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_FAILED_FEATURE_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback#ADVERTISE_FAILED_FEATURE_UNSUPPORTED:kotlin.Int) This feature is not supported on this platform. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_FAILED_INTERNAL_ERROR](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback#ADVERTISE_FAILED_INTERNAL_ERROR:kotlin.Int) Operation failed due to an internal error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_FAILED_TOO_MANY_ADVERTISERS](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback#ADVERTISE_FAILED_TOO_MANY_ADVERTISERS:kotlin.Int) Failed to start advertising because no advertising instance is available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_SUCCESS](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback#ADVERTISE_SUCCESS:kotlin.Int) The requested operation was successful. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AdvertisingSetCallback](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback#AdvertisingSetCallback())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAdvertisingDataSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback#onAdvertisingDataSet(android.bluetooth.le.AdvertisingSet,%20kotlin.Int))`(`advertisingSet:` ` [AdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet)!`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback triggered in response to [AdvertisingSet.setAdvertisingData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet#setAdvertisingData(android.bluetooth.le.AdvertiseData))indicating result of the operation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAdvertisingEnabled](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback#onAdvertisingEnabled(android.bluetooth.le.AdvertisingSet,%20kotlin.Boolean,%20kotlin.Int))`(`advertisingSet:` ` [AdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet)!`, `enable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback triggered in response to android. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAdvertisingParametersUpdated](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback#onAdvertisingParametersUpdated(android.bluetooth.le.AdvertisingSet,%20kotlin.Int,%20kotlin.Int))`(`advertisingSet:` ` [AdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet)!`, `txPower:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback triggered in response to [AdvertisingSet.setAdvertisingParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet#setAdvertisingParameters(android.bluetooth.le.AdvertisingSetParameters))indicating result of the operation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAdvertisingSetStarted](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback#onAdvertisingSetStarted(android.bluetooth.le.AdvertisingSet,%20kotlin.Int,%20kotlin.Int))`(`advertisingSet:` ` [AdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet)!`, `txPower:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback triggered in response to android. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAdvertisingSetStopped](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback#onAdvertisingSetStopped(android.bluetooth.le.AdvertisingSet))`(`advertisingSet:` ` [AdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet)!`)` Callback triggered in response to [BluetoothLeAdvertiser.stopAdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeAdvertiser#stopAdvertisingSet(android.bluetooth.le.AdvertisingSetCallback))indicating advertising set is stopped. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPeriodicAdvertisingDataSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback#onPeriodicAdvertisingDataSet(android.bluetooth.le.AdvertisingSet,%20kotlin.Int))`(`advertisingSet:` ` [AdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet)!`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback triggered in response to [AdvertisingSet.setPeriodicAdvertisingData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet#setPeriodicAdvertisingData(android.bluetooth.le.AdvertiseData))indicating result of the operation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPeriodicAdvertisingEnabled](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback#onPeriodicAdvertisingEnabled(android.bluetooth.le.AdvertisingSet,%20kotlin.Boolean,%20kotlin.Int))`(`advertisingSet:` ` [AdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet)!`, `enable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback triggered in response to [AdvertisingSet.setPeriodicAdvertisingEnabled](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet#setPeriodicAdvertisingEnabled(kotlin.Boolean))indicating result of the operation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPeriodicAdvertisingParametersUpdated](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback#onPeriodicAdvertisingParametersUpdated(android.bluetooth.le.AdvertisingSet,%20kotlin.Int))`(`advertisingSet:` ` [AdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet)!`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback triggered in response to [AdvertisingSet.setPeriodicAdvertisingParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet#setPeriodicAdvertisingParameters(android.bluetooth.le.PeriodicAdvertisingParameters))indicating result of the operation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScanResponseDataSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback#onScanResponseDataSet(android.bluetooth.le.AdvertisingSet,%20kotlin.Int))`(`advertisingSet:` ` [AdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet)!`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback triggered in response to [AdvertisingSet.setAdvertisingData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet#setAdvertisingData(android.bluetooth.le.AdvertiseData))indicating result of the operation. |

## Constants

### ADVERTISE_FAILED_ALREADY_STARTED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADVERTISE_FAILED_ALREADY_STARTED: Int
```

Failed to start advertising as the advertising is already started. 

 Value: 3

### ADVERTISE_FAILED_DATA_TOO_LARGE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADVERTISE_FAILED_DATA_TOO_LARGE: Int
```

Failed to start advertising as the advertise data to be broadcasted is too large. 

 Value: 1

### ADVERTISE_FAILED_FEATURE_UNSUPPORTED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADVERTISE_FAILED_FEATURE_UNSUPPORTED: Int
```

This feature is not supported on this platform. 

 Value: 5

### ADVERTISE_FAILED_INTERNAL_ERROR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADVERTISE_FAILED_INTERNAL_ERROR: Int
```

Operation failed due to an internal error. 

 Value: 4

### ADVERTISE_FAILED_TOO_MANY_ADVERTISERS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADVERTISE_FAILED_TOO_MANY_ADVERTISERS: Int
```

Failed to start advertising because no advertising instance is available. 

 Value: 2

### ADVERTISE_SUCCESS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADVERTISE_SUCCESS: Int
```

The requested operation was successful. 

 Value: 0

## Public constructors

### AdvertisingSetCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AdvertisingSetCallback()
```

## Public methods

### onAdvertisingDataSet

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAdvertisingDataSet(
    advertisingSet: AdvertisingSet!, 
    status: Int
): Unit
```

Callback triggered in response to [AdvertisingSet.setAdvertisingData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet#setAdvertisingData(android.bluetooth.le.AdvertiseData))indicating result of the operation. If status is ADVERTISE_SUCCESS, then data was changed.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------|
| `advertisingSet` | [AdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet)!:The advertising set. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Status of the operation. |

### onAdvertisingEnabled

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAdvertisingEnabled(
    advertisingSet: AdvertisingSet!, 
    enable: Boolean, 
    status: Int
): Unit
```

Callback triggered in response to android.bluetooth.le.BluetoothLeAdvertiser#startAdvertisingSet indicating result of the operation. If status is ADVERTISE_SUCCESS, then advertising set is advertising.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------|
| `advertisingSet` | [AdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet)!:The advertising set. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Status of the operation. |

### onAdvertisingParametersUpdated

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAdvertisingParametersUpdated(
    advertisingSet: AdvertisingSet!, 
    txPower: Int, 
    status: Int
): Unit
```

Callback triggered in response to [AdvertisingSet.setAdvertisingParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet#setAdvertisingParameters(android.bluetooth.le.AdvertisingSetParameters))indicating result of the operation.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------|
| `advertisingSet` | [AdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet)!:The advertising set. |
| `txPower` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):tx power that will be used for this set. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Status of the operation. |

### onAdvertisingSetStarted

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAdvertisingSetStarted(
    advertisingSet: AdvertisingSet!, 
    txPower: Int, 
    status: Int
): Unit
```

Callback triggered in response to android.bluetooth.le.BluetoothLeAdvertiser#startAdvertisingSet indicating result of the operation. If status is ADVERTISE_SUCCESS, then advertisingSet contains the started set and it is advertising. If error occurred, advertisingSet is null, and status will be set to proper error code.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `advertisingSet` | [AdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet)!:The advertising set that was started or null if error. |
| `txPower` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):tx power that will be used for this set. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Status of the operation. |

### onAdvertisingSetStopped

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAdvertisingSetStopped(advertisingSet: AdvertisingSet!): Unit
```

Callback triggered in response to [BluetoothLeAdvertiser.stopAdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeAdvertiser#stopAdvertisingSet(android.bluetooth.le.AdvertisingSetCallback))indicating advertising set is stopped.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------|
| `advertisingSet` | [AdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet)!:The advertising set. |

### onPeriodicAdvertisingDataSet

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPeriodicAdvertisingDataSet(
    advertisingSet: AdvertisingSet!, 
    status: Int
): Unit
```

Callback triggered in response to [AdvertisingSet.setPeriodicAdvertisingData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet#setPeriodicAdvertisingData(android.bluetooth.le.AdvertiseData))indicating result of the operation.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------|
| `advertisingSet` | [AdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet)!:The advertising set. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Status of the operation. |

### onPeriodicAdvertisingEnabled

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPeriodicAdvertisingEnabled(
    advertisingSet: AdvertisingSet!, 
    enable: Boolean, 
    status: Int
): Unit
```

Callback triggered in response to [AdvertisingSet.setPeriodicAdvertisingEnabled](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet#setPeriodicAdvertisingEnabled(kotlin.Boolean))indicating result of the operation.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------|
| `advertisingSet` | [AdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet)!:The advertising set. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Status of the operation. |

### onPeriodicAdvertisingParametersUpdated

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPeriodicAdvertisingParametersUpdated(
    advertisingSet: AdvertisingSet!, 
    status: Int
): Unit
```

Callback triggered in response to [AdvertisingSet.setPeriodicAdvertisingParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet#setPeriodicAdvertisingParameters(android.bluetooth.le.PeriodicAdvertisingParameters))indicating result of the operation.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------|
| `advertisingSet` | [AdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet)!:The advertising set. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Status of the operation. |

### onScanResponseDataSet

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onScanResponseDataSet(
    advertisingSet: AdvertisingSet!, 
    status: Int
): Unit
```

Callback triggered in response to [AdvertisingSet.setAdvertisingData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet#setAdvertisingData(android.bluetooth.le.AdvertiseData))indicating result of the operation.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------|
| `advertisingSet` | [AdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet)!:The advertising set. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Status of the operation. |
