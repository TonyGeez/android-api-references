# AdvertiseCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AdvertiseCallback

Kotlin| [Java](AdvertiseCallback.md) 
| --- | --- |

```
abstract class AdvertiseCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.le.AdvertiseCallback](AdvertiseCallback.md) |

Bluetooth LE advertising callbacks, used to deliver advertising operation status.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_FAILED_ALREADY_STARTED](AdvertiseCallback.md) Failed to start advertising as the advertising is already started. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_FAILED_DATA_TOO_LARGE](AdvertiseCallback.md) Failed to start advertising as the advertise data to be broadcasted is larger than 31 bytes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_FAILED_FEATURE_UNSUPPORTED](AdvertiseCallback.md) This feature is not supported on this platform. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_FAILED_INTERNAL_ERROR](AdvertiseCallback.md) Operation failed due to an internal error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADVERTISE_FAILED_TOO_MANY_ADVERTISERS](AdvertiseCallback.md) Failed to start advertising because no advertising instance is available. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AdvertiseCallback](AdvertiseCallback.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStartFailure](AdvertiseCallback.md))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback when advertising could not be started. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStartSuccess](AdvertiseCallback.md))`(`settingsInEffect:` ` [AdvertiseSettings](AdvertiseSettings.md)!`)` Callback triggered in response to android. |

## Constants

### ADVERTISE_FAILED_ALREADY_STARTED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADVERTISE_FAILED_ALREADY_STARTED: Int
```

Failed to start advertising as the advertising is already started. 

 Value: 3

### ADVERTISE_FAILED_DATA_TOO_LARGE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADVERTISE_FAILED_DATA_TOO_LARGE: Int
```

Failed to start advertising as the advertise data to be broadcasted is larger than 31 bytes. 

 Value: 1

### ADVERTISE_FAILED_FEATURE_UNSUPPORTED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADVERTISE_FAILED_FEATURE_UNSUPPORTED: Int
```

This feature is not supported on this platform. 

 Value: 5

### ADVERTISE_FAILED_INTERNAL_ERROR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADVERTISE_FAILED_INTERNAL_ERROR: Int
```

Operation failed due to an internal error. 

 Value: 4

### ADVERTISE_FAILED_TOO_MANY_ADVERTISERS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADVERTISE_FAILED_TOO_MANY_ADVERTISERS: Int
```

Failed to start advertising because no advertising instance is available. 

 Value: 2

## Public constructors

### AdvertiseCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AdvertiseCallback()
```

## Public methods

### onStartFailure

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onStartFailure(errorCode: Int): Unit
```

Callback when advertising could not be started.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Error code (see ADVERTISE_FAILED_\* constants) for advertising start failures. |

### onStartSuccess

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onStartSuccess(settingsInEffect: AdvertiseSettings!): Unit
```

Callback triggered in response to android.bluetooth.le.BluetoothLeAdvertiser#startAdvertising indicating that the advertising has been started successfully.

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `settingsInEffect` | [AdvertiseSettings](AdvertiseSettings.md)!:The actual settings used for advertising, which may be different from what has been requested. |
