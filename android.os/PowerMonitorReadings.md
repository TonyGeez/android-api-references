# PowerMonitorReadings

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PowerMonitorReadings

Kotlin | [Java](https://developer.android.com/reference/android/os/PowerMonitorReadings "View this page in Java") 
| --- | --- |

```
class PowerMonitorReadings
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.PowerMonitorReadings](https://developer.android.com/reference/kotlin/android/os/PowerMonitorReadings#) |

A collection of energy measurements from Power Monitors.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENERGY_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/os/PowerMonitorReadings#ENERGY_UNAVAILABLE:kotlin.Int) <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getConsumedEnergy](https://developer.android.com/reference/kotlin/android/os/PowerMonitorReadings#getConsumedEnergy(android.os.PowerMonitor))`(`powerMonitor:` ` [PowerMonitor](https://developer.android.com/reference/kotlin/android/os/PowerMonitor)`)` Returns energy consumed by the specified power monitor since boot in microwatt-seconds. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimestampMillis](https://developer.android.com/reference/kotlin/android/os/PowerMonitorReadings#getTimestampMillis(android.os.PowerMonitor))`(`powerMonitor:` ` [PowerMonitor](https://developer.android.com/reference/kotlin/android/os/PowerMonitor)`)` Elapsed realtime, in milliseconds, when the snapshot was taken. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/os/PowerMonitorReadings#toString())`()` <br /> |
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
| `powerMonitor` | [PowerMonitor](https://developer.android.com/reference/kotlin/android/os/PowerMonitor): This value cannot be `null`. |

### getTimestampMillis

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimestampMillis(powerMonitor: PowerMonitor): Long
```

Elapsed realtime, in milliseconds, when the snapshot was taken. 
Value is a non-negative timestamp in the [android.os.SystemClock#elapsedRealtime()](https://developer.android.com/reference/kotlin/android/os/SystemClock#elapsedRealtime()) time base.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------|
| `powerMonitor` | [PowerMonitor](https://developer.android.com/reference/kotlin/android/os/PowerMonitor): This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is a non-negative timestamp in the [android.os.SystemClock#elapsedRealtime()](https://developer.android.com/reference/kotlin/android/os/SystemClock#elapsedRealtime()) time base. |

### toString

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
