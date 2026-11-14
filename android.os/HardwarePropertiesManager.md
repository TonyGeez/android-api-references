# HardwarePropertiesManager

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HardwarePropertiesManager

Kotlin| [Java](https://developer.android.com/reference/android/os/HardwarePropertiesManager "View this page in Java") 
| --- | --- |

```
open class HardwarePropertiesManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.HardwarePropertiesManager](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#) |

The HardwarePropertiesManager class provides a mechanism of accessing hardware state of a device: CPU, GPU and battery temperatures, CPU usage per core, fan speed, etc.

## Summary

| Constants ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_TEMPERATURE_BATTERY](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#DEVICE_TEMPERATURE_BATTERY:kotlin.Int) Temperature of battery in Celsius. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_TEMPERATURE_CPU](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#DEVICE_TEMPERATURE_CPU:kotlin.Int) Temperature of CPUs in Celsius. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_TEMPERATURE_GPU](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#DEVICE_TEMPERATURE_GPU:kotlin.Int) Temperature of GPUs in Celsius. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_TEMPERATURE_SKIN](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#DEVICE_TEMPERATURE_SKIN:kotlin.Int) Temperature of device skin in Celsius. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TEMPERATURE_CURRENT](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#TEMPERATURE_CURRENT:kotlin.Int) Get current temperature. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TEMPERATURE_SHUTDOWN](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#TEMPERATURE_SHUTDOWN:kotlin.Int) Get shutdown temperature threshold. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TEMPERATURE_THROTTLING](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#TEMPERATURE_THROTTLING:kotlin.Int) Get throttling temperature threshold. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TEMPERATURE_THROTTLING_BELOW_VR_MIN](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#TEMPERATURE_THROTTLING_BELOW_VR_MIN:kotlin.Int) Get throttling temperature threshold above which minimum clockrates for VR mode will not be met. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [UNDEFINED_TEMPERATURE](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#UNDEFINED_TEMPERATURE:kotlin.Float) Undefined temperature constant. |
| --- | --- |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CpuUsageInfo](https://developer.android.com/reference/kotlin/android/os/CpuUsageInfo)!\> | [getCpuUsages](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#getCpuUsages())`()` Return an array of CPU usage info for each core. |
| open [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | [getDeviceTemperatures](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#getDeviceTemperatures(kotlin.Int,%20kotlin.Int))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `source:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return an array of device temperatures in Celsius. |
| open [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | [getFanSpeeds](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#getFanSpeeds())`()` Return an array of fan speeds in RPM. |
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
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CpuUsageInfo](https://developer.android.com/reference/kotlin/android/os/CpuUsageInfo)!> | an array of [android.os.CpuUsageInfo](https://developer.android.com/reference/kotlin/android/os/CpuUsageInfo) for each core. Return`null`for each unplugged core. Empty if CPU usage is not supported on this system. |

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
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):type of requested device temperature, one of [DEVICE_TEMPERATURE_CPU](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#DEVICE_TEMPERATURE_CPU:kotlin.Int), [DEVICE_TEMPERATURE_GPU](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#DEVICE_TEMPERATURE_GPU:kotlin.Int), [DEVICE_TEMPERATURE_BATTERY](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#DEVICE_TEMPERATURE_BATTERY:kotlin.Int) or [DEVICE_TEMPERATURE_SKIN](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#DEVICE_TEMPERATURE_SKIN:kotlin.Int). Value is [android.os.HardwarePropertiesManager#DEVICE_TEMPERATURE_CPU](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#DEVICE_TEMPERATURE_CPU:kotlin.Int), [android.os.HardwarePropertiesManager#DEVICE_TEMPERATURE_GPU](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#DEVICE_TEMPERATURE_GPU:kotlin.Int), [android.os.HardwarePropertiesManager#DEVICE_TEMPERATURE_BATTERY](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#DEVICE_TEMPERATURE_BATTERY:kotlin.Int), or [android.os.HardwarePropertiesManager#DEVICE_TEMPERATURE_SKIN](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#DEVICE_TEMPERATURE_SKIN:kotlin.Int) |
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):source of requested device temperature, one of [TEMPERATURE_CURRENT](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#TEMPERATURE_CURRENT:kotlin.Int), [TEMPERATURE_THROTTLING](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#TEMPERATURE_THROTTLING:kotlin.Int), [TEMPERATURE_THROTTLING_BELOW_VR_MIN](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#TEMPERATURE_THROTTLING_BELOW_VR_MIN:kotlin.Int) or [TEMPERATURE_SHUTDOWN](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#TEMPERATURE_SHUTDOWN:kotlin.Int). Value is [android.os.HardwarePropertiesManager#TEMPERATURE_CURRENT](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#TEMPERATURE_CURRENT:kotlin.Int), [android.os.HardwarePropertiesManager#TEMPERATURE_THROTTLING](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#TEMPERATURE_THROTTLING:kotlin.Int), [android.os.HardwarePropertiesManager#TEMPERATURE_SHUTDOWN](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#TEMPERATURE_SHUTDOWN:kotlin.Int), or [android.os.HardwarePropertiesManager#TEMPERATURE_THROTTLING_BELOW_VR_MIN](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#TEMPERATURE_THROTTLING_BELOW_VR_MIN:kotlin.Int) |

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | an array of requested float device temperatures. Temperature equals to [UNDEFINED_TEMPERATURE](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager#UNDEFINED_TEMPERATURE:kotlin.Float) if undefined. Empty if platform doesn't provide the queried temperature. This value cannot be`null`. |

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
