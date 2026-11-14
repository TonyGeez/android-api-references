# SensorDirectChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SensorDirectChannel

Kotlin| [Java](../android/hardware/SensorDirectChannel.md) 
| --- | --- |

```
class SensorDirectChannel : Channel
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.SensorDirectChannel](../android/hardware/SensorDirectChannel.md) |

Class representing a sensor direct channel. Use [SensorManager.createDirectChannel(android.os.MemoryFile)](../android/hardware/SensorManager.md))or [SensorManager.createDirectChannel(android.hardware.HardwareBuffer)](../android/hardware/SensorManager.md))to obtain an object. The channel object can be then configured (see [configure(android.hardware.Sensor,int)](../android/hardware/SensorDirectChannel.md))) to start delivery of sensor events into shared memory buffer.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RATE_FAST](../android/hardware/SensorDirectChannel.md) Sensor operates at nominal rate of 200Hz. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RATE_NORMAL](../android/hardware/SensorDirectChannel.md) Sensor operates at nominal rate of 50Hz. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RATE_STOP](../android/hardware/SensorDirectChannel.md) Sensor stopped (no event output). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RATE_VERY_FAST](../android/hardware/SensorDirectChannel.md) Sensor operates at nominal rate of 800Hz. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_HARDWARE_BUFFER](../android/hardware/SensorDirectChannel.md) Shared memory type wrapped by HardwareBuffer object. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_MEMORY_FILE](../android/hardware/SensorDirectChannel.md) Shared memory type ashmem, wrapped in MemoryFile object. |
| --- | --- |

| Public methods ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/hardware/SensorDirectChannel.md))`()` Close sensor direct channel. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [configure](../android/hardware/SensorDirectChannel.md))`(`sensor:` ` [Sensor](../android/hardware/Sensor.md)!`, `rateLevel:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Configure sensor rate or stop sensor report. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](../android/hardware/SensorDirectChannel.md))`()` Determine if a channel is still valid. |
| --- | --- |

| Protected methods ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/hardware/SensorDirectChannel.md))`()` <br /> |

## Constants

### RATE_FAST

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RATE_FAST: Int
```

Sensor operates at nominal rate of 200Hz. The actual rate is expected to be between 55% to 220% of nominal rate, thus between 110Hz to 440Hz. 

 Value: 2

**See Also**

- [#configure(Sensor, int)](../android/hardware/SensorDirectChannel.md)) 

### RATE_NORMAL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RATE_NORMAL: Int
```

Sensor operates at nominal rate of 50Hz. The actual rate is expected to be between 55% to 220% of nominal rate, thus between 27.5Hz to 110Hz. 

 Value: 1

**See Also**

- [#configure(Sensor, int)](../android/hardware/SensorDirectChannel.md)) 

### RATE_STOP

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RATE_STOP: Int
```

Sensor stopped (no event output). 

 Value: 0

**See Also**

- [#configure(Sensor, int)](../android/hardware/SensorDirectChannel.md)) 

### RATE_VERY_FAST

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RATE_VERY_FAST: Int
```

Sensor operates at nominal rate of 800Hz. The actual rate is expected to be between 55% to 220% of nominal rate, thus between 440Hz to 1760Hz. 

 Value: 3

**See Also**

- [#configure(Sensor, int)](../android/hardware/SensorDirectChannel.md)) 

### TYPE_HARDWARE_BUFFER

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_HARDWARE_BUFFER: Int
```

Shared memory type wrapped by HardwareBuffer object. 

 Value: 2

**See Also**

- [android.hardware.SensorManager#createDirectChannel(HardwareBuffer)](../android/hardware/SensorManager.md)) 

### TYPE_MEMORY_FILE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_MEMORY_FILE: Int
```

Shared memory type ashmem, wrapped in MemoryFile object. 

 Value: 1

**See Also**

- [android.hardware.SensorManager#createDirectChannel(MemoryFile)](../android/hardware/SensorManager.md))

## Public methods

### close

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

Close sensor direct channel. Stop all active sensor in the channel and free sensor system resource related to channel. Shared memory used for creating the direct channel need to be closed or freed separately.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | If an I/O error occurs |

**See Also**

- [android.hardware.SensorManager#createDirectChannel(MemoryFile)](../android/hardware/SensorManager.md))
- [android.hardware.SensorManager#createDirectChannel(HardwareBuffer)](../android/hardware/SensorManager.md)) 

### configure

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun configure(
    sensor: Sensor!, 
    rateLevel: Int
): Int
```

Configure sensor rate or stop sensor report. To start event report of a sensor, or change rate of existing report, call this function with rateLevel other than [android.hardware.SensorDirectChannel#RATE_STOP](../android/hardware/SensorDirectChannel.md). Sensor events will be added into a queue formed by the shared memory used in creation of direction channel. Each element of the queue has size of 104 bytes and represents a sensor event. Data structure of an element (all fields in little-endian): 

```kotlin
offset   type                    name
  ------------------------------------------------------------------------
    0x0000   int32_t                 size (always 104)
    0x0004   int32_t                 sensor report token
    0x0008   int32_t                 type (see SensorType)
    0x000C   uint32_t                atomic counter
    0x0010   int64_t                 timestamp (see Event)
    0x0018   float[16]/int64_t[8]    data (data type depends on sensor type)
    0x0058   int32_t[4]              reserved (set to zero)
  
```
There are no head or tail pointers. The sequence and frontier of new sensor events is determined by the atomic counter, which counts from 1 after creation of direct channel and increments 1 for each new event. Atomic counter will wrap back to 1 after it reaches UINT32_MAX, skipping value 0 to avoid confusion with uninitialized memory. The writer in sensor system will wrap around from the start of shared memory region when it reaches the end. If size of memory region is not a multiple of size of element (104 bytes), the residual is not used at the end. Function returns a positive sensor report token on success. This token can be used to differentiate sensor events from multiple sensor of the same type. For example, if there are two accelerometers in the system A and B, it is guaranteed different report tokens will be returned when starting sensor A and B. To stop a sensor, call this function with rateLevel equal [android.hardware.SensorDirectChannel#RATE_STOP](../android/hardware/SensorDirectChannel.md). If the sensor parameter is left to be null, this will stop all active sensor report associated with the direct channel specified. Function return 1 on success or 0 on failure.

<br />

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sensor` | [Sensor](../android/hardware/Sensor.md)!:A [android.hardware.Sensor](../android/hardware/Sensor.md) object to denote sensor to be operated. |
| `rateLevel` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):rate level defined in [android.hardware.SensorDirectChannel](../android/hardware/SensorDirectChannel.md). Value is [android.hardware.SensorDirectChannel#RATE_STOP](../android/hardware/SensorDirectChannel.md), [android.hardware.SensorDirectChannel#RATE_NORMAL](../android/hardware/SensorDirectChannel.md), [android.hardware.SensorDirectChannel#RATE_FAST](../android/hardware/SensorDirectChannel.md), or [android.hardware.SensorDirectChannel#RATE_VERY_FAST](../android/hardware/SensorDirectChannel.md) |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | \* starting report or changing rate: positive sensor report token on success, 0 on failure; \* stopping report: 1 on success, 0 on failure. |

| Exceptions ||
|----------------------------------|-----------------------|
| `java.lang.NullPointerException` | when channel is null. |

### isOpen

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isOpen(): Boolean
```

Determine if a channel is still valid. A channel is invalidated after #close() is called.

| Return ||
|------------------------------------------------------------------------------------|----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if channel is valid. |

## Protected methods

### finalize

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
