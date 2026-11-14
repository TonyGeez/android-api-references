# HardwarePropertiesManager

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HardwarePropertiesManager

Kotlin| [Java](HardwarePropertiesManager.md) 
| --- | --- |

```
open class HardwarePropertiesManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.HardwarePropertiesManager](HardwarePropertiesManager.md) |

The HardwarePropertiesManager class provides a mechanism of accessing hardware state of a device: CPU, GPU and battery temperatures, CPU usage per core, fan speed, etc.

## Summary

| Constants ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_TEMPERATURE_BATTERY](HardwarePropertiesManager.md) Temperature of battery in Celsius. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_TEMPERATURE_CPU](HardwarePropertiesManager.md) Temperature of CPUs in Celsius. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_TEMPERATURE_GPU](HardwarePropertiesManager.md) Temperature of GPUs in Celsius. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_TEMPERATURE_SKIN](HardwarePropertiesManager.md) Temperature of device skin in Celsius. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TEMPERATURE_CURRENT](HardwarePropertiesManager.md) Get current temperature. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TEMPERATURE_SHUTDOWN](HardwarePropertiesManager.md) Get shutdown temperature threshold. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TEMPERATURE_THROTTLING](HardwarePropertiesManager.md) Get throttling temperature threshold. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TEMPERATURE_THROTTLING_BELOW_VR_MIN](HardwarePropertiesManager.md) Get throttling temperature threshold above which minimum clockrates for VR mode will not be met. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [UNDEFINED_TEMPERATURE](HardwarePropertiesManager.md) Undefined temperature constant. |
| --- | --- |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CpuUsageInfo](CpuUsageInfo.md)!\> | [getCpuUsages](HardwarePropertiesManager.md))`()` Return an array of CPU usage info for each core. |
| open [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | [getDeviceTemperatures](HardwarePropertiesManager.md))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `source:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return an array of device temperatures in Celsius. |
| open [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | [getFanSpeeds](HardwarePropertiesManager.md))`()` Return an array of fan speeds in RPM. |
| --- | --- |

## Constants

### DEVICE_TEMPERATURE_BATTERY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_TEMPERATURE_BATTERY: Int
```

Temperature of battery in Celsius. 

 Value: 2

### DEVICE_TEMPERATURE_CPU

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_TEMPERATURE_CPU: Int
```

Temperature of CPUs in Celsius. 

 Value: 0

### DEVICE_TEMPERATURE_GPU

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_TEMPERATURE_GPU: Int
```

Temperature of GPUs in Celsius. 

 Value: 1

### DEVICE_TEMPERATURE_SKIN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_TEMPERATURE_SKIN: Int
```

Temperature of device skin in Celsius. 

 Value: 3

### TEMPERATURE_CURRENT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TEMPERATURE_CURRENT: Int
```

Get current temperature. 

 Value: 0

### TEMPERATURE_SHUTDOWN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TEMPERATURE_SHUTDOWN: Int
```

Get shutdown temperature threshold. 

 Value: 2

### TEMPERATURE_THROTTLING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TEMPERATURE_THROTTLING: Int
```

Get throttling temperature threshold. 

 Value: 1

### TEMPERATURE_THROTTLING_BELOW_VR_MIN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TEMPERATURE_THROTTLING_BELOW_VR_MIN: Int
```

Get throttling temperature threshold above which minimum clockrates for VR mode will not be met. 

 Value: 3

### UNDEFINED_TEMPERATURE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNDEFINED_TEMPERATURE: Float
```

Undefined temperature constant. 

 Value: -3.4028235E38f

## Public methods

### getCpuUsages

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCpuUsages(): Array<CpuUsageInfo!>
```

Return an array of CPU usage info for each core.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CpuUsageInfo](CpuUsageInfo.md)!> | an array of [android.os.CpuUsageInfo](CpuUsageInfo.md) for each core. Return`null`for each unplugged core. Empty if CPU usage is not supported on this system. |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if something other than the device owner or the current VR service tries to retrieve information provided by this service. |

### getDeviceTemperatures

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDeviceTemperatures(
    type: Int, 
    source: Int
): FloatArray
```

Return an array of device temperatures in Celsius.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):type of requested device temperature, one of [DEVICE_TEMPERATURE_CPU](HardwarePropertiesManager.md), [DEVICE_TEMPERATURE_GPU](HardwarePropertiesManager.md), [DEVICE_TEMPERATURE_BATTERY](HardwarePropertiesManager.md) or [DEVICE_TEMPERATURE_SKIN](HardwarePropertiesManager.md). Value is [android.os.HardwarePropertiesManager#DEVICE_TEMPERATURE_CPU](HardwarePropertiesManager.md), [android.os.HardwarePropertiesManager#DEVICE_TEMPERATURE_GPU](HardwarePropertiesManager.md), [android.os.HardwarePropertiesManager#DEVICE_TEMPERATURE_BATTERY](HardwarePropertiesManager.md), or [android.os.HardwarePropertiesManager#DEVICE_TEMPERATURE_SKIN](HardwarePropertiesManager.md) |
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):source of requested device temperature, one of [TEMPERATURE_CURRENT](HardwarePropertiesManager.md), [TEMPERATURE_THROTTLING](HardwarePropertiesManager.md), [TEMPERATURE_THROTTLING_BELOW_VR_MIN](HardwarePropertiesManager.md) or [TEMPERATURE_SHUTDOWN](HardwarePropertiesManager.md). Value is [android.os.HardwarePropertiesManager#TEMPERATURE_CURRENT](HardwarePropertiesManager.md), [android.os.HardwarePropertiesManager#TEMPERATURE_THROTTLING](HardwarePropertiesManager.md), [android.os.HardwarePropertiesManager#TEMPERATURE_SHUTDOWN](HardwarePropertiesManager.md), or [android.os.HardwarePropertiesManager#TEMPERATURE_THROTTLING_BELOW_VR_MIN](HardwarePropertiesManager.md) |

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | an array of requested float device temperatures. Temperature equals to [UNDEFINED_TEMPERATURE](HardwarePropertiesManager.md) if undefined. Empty if platform doesn't provide the queried temperature. This value cannot be`null`. |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if something other than the device owner or the current VR service tries to retrieve information provided by this service. |

### getFanSpeeds

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFanSpeeds(): FloatArray
```

Return an array of fan speeds in RPM.

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | an array of float fan speeds in RPM. Empty if there are no fans or fan speed is not supported on this system. This value cannot be`null`. |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if something other than the device owner or the current VR service tries to retrieve information provided by this service. |
