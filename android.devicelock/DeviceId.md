# DeviceId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeviceId

Kotlin| [Java](../android/devicelock/DeviceId.md) 
| --- | --- |

```
class DeviceId
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.devicelock.DeviceId](../android/devicelock/DeviceId.md) |

The response returned from [DeviceLockManager.getDeviceId](../android/devicelock/DeviceLockManager.md))on success. A DeviceId represents a stable identifier (i.e. an identifier that is preserved after a factory reset). At this moment, the only supported identifiers are IMEI, MEID and the Device Serial Number.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_ID_TYPE_IMEI](../android/devicelock/DeviceId.md) The device id is an IMEI |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_ID_TYPE_MEID](../android/devicelock/DeviceId.md) The device id is a MEID |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_ID_TYPE_SERIAL_NUMBER](../android/devicelock/DeviceId.md) The device id is a serial number |
| --- | --- |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getId](../android/devicelock/DeviceId.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](../android/devicelock/DeviceId.md))`()` <br /> |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.devicelock.DeviceId#DEVICE_ID_TYPE_IMEI](../android/devicelock/DeviceId.md), [android.devicelock.DeviceId#DEVICE_ID_TYPE_MEID](../android/devicelock/DeviceId.md), or [android.devicelock.DeviceId#DEVICE_ID_TYPE_SERIAL_NUMBER](../android/devicelock/DeviceId.md) |
