# DeviceId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeviceId

Kotlin| [Java](https://developer.android.com/reference/android/devicelock/DeviceId "View this page in Java") 

```
class DeviceId
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.devicelock.DeviceId](https://developer.android.com/reference/kotlin/android/devicelock/DeviceId#) |

The response returned from [DeviceLockManager.getDeviceId](https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager#getDeviceId(java.util.concurrent.Executor,%20android.os.OutcomeReceiver))on success. A DeviceId represents a stable identifier (i.e. an identifier that is preserved after a factory reset). At this moment, the only supported identifiers are IMEI, MEID and the Device Serial Number.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_ID_TYPE_IMEI](https://developer.android.com/reference/kotlin/android/devicelock/DeviceId#DEVICE_ID_TYPE_IMEI:kotlin.Int) The device id is an IMEI |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_ID_TYPE_MEID](https://developer.android.com/reference/kotlin/android/devicelock/DeviceId#DEVICE_ID_TYPE_MEID:kotlin.Int) The device id is a MEID |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_ID_TYPE_SERIAL_NUMBER](https://developer.android.com/reference/kotlin/android/devicelock/DeviceId#DEVICE_ID_TYPE_SERIAL_NUMBER:kotlin.Int) The device id is a serial number |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getId](https://developer.android.com/reference/kotlin/android/devicelock/DeviceId#getId())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/devicelock/DeviceId#getType())`()` <br /> |

## Constants

### DEVICE_ID_TYPE_IMEI

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_ID_TYPE_IMEI: Int
```

The device id is an IMEI 

 Value: 0

### DEVICE_ID_TYPE_MEID

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_ID_TYPE_MEID: Int
```

The device id is a MEID 

 Value: 1

### DEVICE_ID_TYPE_SERIAL_NUMBER

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_ID_TYPE_SERIAL_NUMBER: Int
```

The device id is a serial number 

 Value: 2

## Public methods

### getId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): String
```

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.devicelock.DeviceId#DEVICE_ID_TYPE_IMEI](https://developer.android.com/reference/kotlin/android/devicelock/DeviceId#DEVICE_ID_TYPE_IMEI:kotlin.Int), [android.devicelock.DeviceId#DEVICE_ID_TYPE_MEID](https://developer.android.com/reference/kotlin/android/devicelock/DeviceId#DEVICE_ID_TYPE_MEID:kotlin.Int), or [android.devicelock.DeviceId#DEVICE_ID_TYPE_SERIAL_NUMBER](https://developer.android.com/reference/kotlin/android/devicelock/DeviceId#DEVICE_ID_TYPE_SERIAL_NUMBER:kotlin.Int) |
