# AdvertisingSetCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AdvertisingSetCallback

Kotlin| [Java](AdvertisingSetCallback.md) 
| --- | --- |

```
abstract class AdvertisingSetCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.le.AdvertisingSetCallback](AdvertisingSetCallback.md) |

Bluetooth LE advertising set callbacks, used to deliver advertising operation status.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_FAILED_ALREADY_STARTED](AdvertisingSetCallback.md) Failed to start advertising as the advertising is already started. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_FAILED_DATA_TOO_LARGE](AdvertisingSetCallback.md) Failed to start advertising as the advertise data to be broadcasted is too large. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_FAILED_FEATURE_UNSUPPORTED](AdvertisingSetCallback.md) This feature is not supported on this platform. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_FAILED_INTERNAL_ERROR](AdvertisingSetCallback.md) Operation failed due to an internal error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_FAILED_TOO_MANY_ADVERTISERS](AdvertisingSetCallback.md) Failed to start advertising because no advertising instance is available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_SUCCESS](AdvertisingSetCallback.md) The requested operation was successful. |
| --- | --- |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AdvertisingSetCallback](AdvertisingSetCallback.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAdvertisingDataSet](AdvertisingSetCallback.md))`(`advertisingSet:` ` [AdvertisingSet](AdvertisingSet.md)!`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback triggered in response to [AdvertisingSet.setAdvertisingData](AdvertisingSet.md))indicating result of the operation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAdvertisingEnabled](AdvertisingSetCallback.md))`(`advertisingSet:` ` [AdvertisingSet](AdvertisingSet.md)!`, `enable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback triggered in response to android. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAdvertisingParametersUpdated](AdvertisingSetCallback.md))`(`advertisingSet:` ` [AdvertisingSet](AdvertisingSet.md)!`, `txPower:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback triggered in response to [AdvertisingSet.setAdvertisingParameters](AdvertisingSet.md))indicating result of the operation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAdvertisingSetStarted](AdvertisingSetCallback.md))`(`advertisingSet:` ` [AdvertisingSet](AdvertisingSet.md)!`, `txPower:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback triggered in response to android. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAdvertisingSetStopped](AdvertisingSetCallback.md))`(`advertisingSet:` ` [AdvertisingSet](AdvertisingSet.md)!`)` Callback triggered in response to [BluetoothLeAdvertiser.stopAdvertisingSet](BluetoothLeAdvertiser.md))indicating advertising set is stopped. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPeriodicAdvertisingDataSet](AdvertisingSetCallback.md))`(`advertisingSet:` ` [AdvertisingSet](AdvertisingSet.md)!`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback triggered in response to [AdvertisingSet.setPeriodicAdvertisingData](AdvertisingSet.md))indicating result of the operation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPeriodicAdvertisingEnabled](AdvertisingSetCallback.md))`(`advertisingSet:` ` [AdvertisingSet](AdvertisingSet.md)!`, `enable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback triggered in response to [AdvertisingSet.setPeriodicAdvertisingEnabled](AdvertisingSet.md))indicating result of the operation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPeriodicAdvertisingParametersUpdated](AdvertisingSetCallback.md))`(`advertisingSet:` ` [AdvertisingSet](AdvertisingSet.md)!`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback triggered in response to [AdvertisingSet.setPeriodicAdvertisingParameters](AdvertisingSet.md))indicating result of the operation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScanResponseDataSet](AdvertisingSetCallback.md))`(`advertisingSet:` ` [AdvertisingSet](AdvertisingSet.md)!`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback triggered in response to [AdvertisingSet.setAdvertisingData](AdvertisingSet.md))indicating result of the operation. |
| --- | --- |

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

Callback triggered in response to [AdvertisingSet.setAdvertisingData](AdvertisingSet.md))indicating result of the operation. If status is ADVERTISE_SUCCESS, then data was changed.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------|
| `advertisingSet` | [AdvertisingSet](AdvertisingSet.md)!:The advertising set. |
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
| `advertisingSet` | [AdvertisingSet](AdvertisingSet.md)!:The advertising set. |
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

Callback triggered in response to [AdvertisingSet.setAdvertisingParameters](AdvertisingSet.md))indicating result of the operation.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------|
| `advertisingSet` | [AdvertisingSet](AdvertisingSet.md)!:The advertising set. |
| `txPower` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):tx power that will be used for this set. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Status of the operation. |
| --- | --- |

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
| `advertisingSet` | [AdvertisingSet](AdvertisingSet.md)!:The advertising set that was started or null if error. |
| `txPower` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):tx power that will be used for this set. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Status of the operation. |
| --- | --- |

### onAdvertisingSetStopped

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAdvertisingSetStopped(advertisingSet: AdvertisingSet!): Unit
```

Callback triggered in response to [BluetoothLeAdvertiser.stopAdvertisingSet](BluetoothLeAdvertiser.md))indicating advertising set is stopped.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------|
| `advertisingSet` | [AdvertisingSet](AdvertisingSet.md)!:The advertising set. |

### onPeriodicAdvertisingDataSet

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPeriodicAdvertisingDataSet(
    advertisingSet: AdvertisingSet!, 
    status: Int
): Unit
```

Callback triggered in response to [AdvertisingSet.setPeriodicAdvertisingData](AdvertisingSet.md))indicating result of the operation.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------|
| `advertisingSet` | [AdvertisingSet](AdvertisingSet.md)!:The advertising set. |
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

Callback triggered in response to [AdvertisingSet.setPeriodicAdvertisingEnabled](AdvertisingSet.md))indicating result of the operation.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------|
| `advertisingSet` | [AdvertisingSet](AdvertisingSet.md)!:The advertising set. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Status of the operation. |

### onPeriodicAdvertisingParametersUpdated

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPeriodicAdvertisingParametersUpdated(
    advertisingSet: AdvertisingSet!, 
    status: Int
): Unit
```

Callback triggered in response to [AdvertisingSet.setPeriodicAdvertisingParameters](AdvertisingSet.md))indicating result of the operation.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------|
| `advertisingSet` | [AdvertisingSet](AdvertisingSet.md)!:The advertising set. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Status of the operation. |

### onScanResponseDataSet

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onScanResponseDataSet(
    advertisingSet: AdvertisingSet!, 
    status: Int
): Unit
```

Callback triggered in response to [AdvertisingSet.setAdvertisingData](AdvertisingSet.md))indicating result of the operation.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------|
| `advertisingSet` | [AdvertisingSet](AdvertisingSet.md)!:The advertising set. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Status of the operation. |
