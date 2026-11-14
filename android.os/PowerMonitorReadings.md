# PowerMonitorReadings

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PowerMonitorReadings

Kotlin | [Java](../android/os/PowerMonitorReadings.md) 
| --- | --- |

```
class PowerMonitorReadings
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.PowerMonitorReadings](../android/os/PowerMonitorReadings.md) |

A collection of energy measurements from Power Monitors.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENERGY_UNAVAILABLE](../android/os/PowerMonitorReadings.md) <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getConsumedEnergy](../android/os/PowerMonitorReadings.md))`(`powerMonitor:` ` [PowerMonitor](../android/os/PowerMonitor.md)`)` Returns energy consumed by the specified power monitor since boot in microwatt-seconds. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimestampMillis](../android/os/PowerMonitorReadings.md))`(`powerMonitor:` ` [PowerMonitor](../android/os/PowerMonitor.md)`)` Elapsed realtime, in milliseconds, when the snapshot was taken. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/os/PowerMonitorReadings.md))`()` <br /> |
| --- | --- |

## Constants

### ENERGY_UNAVAILABLE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENERGY_UNAVAILABLE: Int
```  

 Value: -1

## Public methods

### getConsumedEnergy

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConsumedEnergy(powerMonitor: PowerMonitor): Long
```

Returns energy consumed by the specified power monitor since boot in microwatt-seconds. Does not persist across reboots. Represents total energy: both on-battery and plugged-in.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------|
| `powerMonitor` | [PowerMonitor](../android/os/PowerMonitor.md): This value cannot be `null`. |

### getTimestampMillis

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimestampMillis(powerMonitor: PowerMonitor): Long
```

Elapsed realtime, in milliseconds, when the snapshot was taken. 
Value is a non-negative timestamp in the [android.os.SystemClock#elapsedRealtime()](../android/os/SystemClock.md)) time base.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------|
| `powerMonitor` | [PowerMonitor](../android/os/PowerMonitor.md): This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative timestamp in the [android.os.SystemClock#elapsedRealtime()](../android/os/SystemClock.md)) time base. |

### toString

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
