# HealthStats

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HealthStats

Kotlin | [Java](../android/os/health/HealthStats.md) 
| --- | --- |

```
open class HealthStats
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.health.HealthStats](../android/os/health/HealthStats.md) |

A HealthStats object contains system health data about an application.

**Data Types** 
Each of the keys references data in one of five data types:

A **measurement** metric contains a single `long` value. That value may be a count, a time, or some other type of value. The unit for a measurement (COUNT, MS, etc) will always be in the name of the constant for the key to retrieve it. For example, the [UidHealthStats.MEASUREMENT_WIFI_TX_MS](../android/os/health/UidHealthStats.md) value is the number of milliseconds (ms) that were spent transmitting on wifi by an application. The [UidHealthStats.MEASUREMENT_MOBILE_RX_PACKETS](../android/os/health/UidHealthStats.md) measurement is the number of packets received on behalf of an application. The [UidHealthStats.MEASUREMENT_TOUCH_USER_ACTIVITY_COUNT](../android/os/health/UidHealthStats.md) measurement is the number of times the user touched the screen, causing the screen to stay awake.

A **timer** metric contains an `int` count and a `long` time, measured in milliseconds. Timers track how many times a resource was used, and the total duration for that usage. For example, the [android.os.health.UidHealthStats#TIMER_FLASHLIGHT](../android/os/health/UidHealthStats.md) timer tracks how many times the application turned on the flashlight, and for how many milliseconds total it kept it on.

A **measurement map** metric is a mapping of [java.lang.String](../java/lang/String.md) names to [java.lang.Long](../java/lang/Long.md) values. The names typically are application provided names. For example, the [PackageHealthStats.MEASUREMENTS_WAKEUP_ALARMS_COUNT](../android/os/health/PackageHealthStats.md) measurement map is a mapping of the tag provided to the [android.app.AlarmManager](../android/app/AlarmManager.md) when the alarm is scheduled.

A **timer map** metric is a mapping of [java.lang.String](../java/lang/String.md) names to [android.os.health.TimerStat](../android/os/health/TimerStat.md) objects. The names are typically application provided names. For example, the [UidHealthStats.TIMERS_WAKELOCKS_PARTIAL](../android/os/health/UidHealthStats.md) is a mapping of tag provided to the [android.os.PowerManager](../android/os/PowerManager.md) when the wakelock is created to the number of times and for how long each wakelock was active.

Lastly, a **health stats** metric is a mapping of [java.lang.String](../java/lang/String.md) names to a recursive [android.os.health.HealthStats](../android/os/health/HealthStats.md) object containing more detailed information. For example, the [UidHealthStats.STATS_PACKAGES](../android/os/health/UidHealthStats.md) metric is a mapping of the package names for each of the APKs sharing a uid to the information recorded for that apk. The returned HealthStats objects will each be associated with a different set of constants. For the HealthStats returned for UidHealthStats.STATS_PACKAGES, the keys come from the [android.os.health.PackageHealthStats](../android/os/health/PackageHealthStats.md) class.

The keys that are available are subject to change, depending on what a particular device or software version is capable of recording. Applications must handle the absence of data without crashing.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDataType](../android/os/health/HealthStats.md))`()` Get a name representing the contents of this object. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMeasurement](../android/os/health/HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the measurement for the given key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMeasurementKeyAt](../android/os/health/HealthStats.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the key for the measurement at the given index. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMeasurementKeyCount](../android/os/health/HealthStats.md))`()` Get the number of measurement values in this object. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\>! | [getMeasurements](../android/os/health/HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the measurements map for the given key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMeasurementsKeyAt](../android/os/health/HealthStats.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the key for the measurement map at the given index. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMeasurementsKeyCount](../android/os/health/HealthStats.md))`()` Get the number of measurement map values in this object. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [HealthStats](../android/os/health/HealthStats.md)!\>! | [getStats](../android/os/health/HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the HealthStats map for the given key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStatsKeyAt](../android/os/health/HealthStats.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the key for the timer at the given index. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStatsKeyCount](../android/os/health/HealthStats.md))`()` Get the number of HealthStat map values in this object. |
| open [TimerStat](../android/os/health/TimerStat.md)! | [getTimer](../android/os/health/HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return a TimerStat object for the given key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimerCount](../android/os/health/HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the count for the timer for the given key. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimerKeyAt](../android/os/health/HealthStats.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the key for the timer at the given index. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimerKeyCount](../android/os/health/HealthStats.md))`()` Get the number of timer values in this object. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimerTime](../android/os/health/HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the time for the timer for the given key, in milliseconds. |
| --- | --- |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [TimerStat](../android/os/health/TimerStat.md)!\>! | [getTimers](../android/os/health/HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the TimerStat map for the given key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimersKeyAt](../android/os/health/HealthStats.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the key for the timer map at the given index. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimersKeyCount](../android/os/health/HealthStats.md))`()` Get the number of timer map values in this object. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMeasurement](../android/os/health/HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return whether this object contains a measurement for the supplied key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMeasurements](../android/os/health/HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return whether this object contains a measurements map for the supplied key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStats](../android/os/health/HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return whether this object contains a HealthStats map for the supplied key. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasTimer](../android/os/health/HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return whether this object contains a TimerStat for the supplied key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasTimers](../android/os/health/HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return whether this object contains a timers map for the supplied key. |

## Public methods

### getDataType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDataType(): String!
```

Get a name representing the contents of this object. 
**See Also**

- [android.os.health.UidHealthStats](../android/os/health/UidHealthStats.md)
- [android.os.health.PackageHealthStats](../android/os/health/PackageHealthStats.md)
- [android.os.health.PidHealthStats](../android/os/health/PidHealthStats.md)
- [android.os.health.ProcessHealthStats](../android/os/health/ProcessHealthStats.md)
- [android.os.health.ServiceHealthStats](../android/os/health/ServiceHealthStats.md) 

### getMeasurement

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMeasurement(key: Int): Long
```

Get the measurement for the given key.

| Exceptions ||
|---------------------------------------|---------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | When the key is not present in this object. |

**See Also**

- [#hasMeasurement](../android/os/health/HealthStats.md)) 

### getMeasurementKeyAt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMeasurementKeyAt(index: Int): Int
```

Get the key for the measurement at the given index. Index must be between 0 and the result of [getMeasurementKeyCount()](../android/os/health/HealthStats.md)). 
**See Also**

- [#getMeasurementKeyCount](../android/os/health/HealthStats.md)) 

### getMeasurementKeyCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMeasurementKeyCount(): Int
```

Get the number of measurement values in this object. Can be used to iterate through the available measurements. 
**See Also**

- [#getMeasurementKeyAt](../android/os/health/HealthStats.md)) 

### getMeasurements

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMeasurements(key: Int): MutableMap<String!, Long!>!
```

Get the measurements map for the given key.

| Exceptions ||
|---------------------------------------|---------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | When the key is not present in this object. |

**See Also**

- [#hasMeasurements](../android/os/health/HealthStats.md)) 

### getMeasurementsKeyAt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMeasurementsKeyAt(index: Int): Int
```

Get the key for the measurement map at the given index. Index must be between 0 and the result of [getMeasurementsKeyCount()](../android/os/health/HealthStats.md)). 
**See Also**

- [#getMeasurementsKeyCount](../android/os/health/HealthStats.md)) 

### getMeasurementsKeyCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMeasurementsKeyCount(): Int
```

Get the number of measurement map values in this object. Can be used to iterate through the available measurement maps. 
**See Also**

- [#getMeasurementsKeyAt](../android/os/health/HealthStats.md)) 

### getStats

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStats(key: Int): MutableMap<String!, HealthStats!>!
```

Get the HealthStats map for the given key.

| Exceptions ||
|---------------------------------------|---------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | When the key is not present in this object. |

**See Also**

- [#hasStats](../android/os/health/HealthStats.md)) 

### getStatsKeyAt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStatsKeyAt(index: Int): Int
```

Get the key for the timer at the given index. Index must be between 0 and the result of [getStatsKeyCount()](../android/os/health/HealthStats.md)). 
**See Also**

- [#getStatsKeyCount](../android/os/health/HealthStats.md)) 

### getStatsKeyCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStatsKeyCount(): Int
```

Get the number of HealthStat map values in this object. Can be used to iterate through the available measurements. 
**See Also**

- [#getMeasurementKeyAt](../android/os/health/HealthStats.md)) 

### getTimer

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimer(key: Int): TimerStat!
```

Return a TimerStat object for the given key. This will allocate a new [TimerStat](../android/os/health/TimerStat.md) object, which may be wasteful. Instead, use [getTimerCount](../android/os/health/HealthStats.md)) and [getTimerTime](../android/os/health/HealthStats.md)).

| Exceptions ||
|---------------------------------------|---------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | When the key is not present in this object. |

**See Also**

- [#hasTimer](../android/os/health/HealthStats.md)) 

### getTimerCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimerCount(key: Int): Int
```

Get the count for the timer for the given key.

| Exceptions ||
|---------------------------------------|---------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | When the key is not present in this object. |

**See Also**

- [#hasTimer](../android/os/health/HealthStats.md)) 

### getTimerKeyAt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimerKeyAt(index: Int): Int
```

Get the key for the timer at the given index. Index must be between 0 and the result of [getTimerKeyCount()](../android/os/health/HealthStats.md)). 
**See Also**

- [#getTimerKeyCount](../android/os/health/HealthStats.md)) 

### getTimerKeyCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimerKeyCount(): Int
```

Get the number of timer values in this object. Can be used to iterate through the available timers. 
**See Also**

- [#getTimerKeyAt](../android/os/health/HealthStats.md)) 

### getTimerTime

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimerTime(key: Int): Long
```

Get the time for the timer for the given key, in milliseconds.

| Exceptions ||
|---------------------------------------|---------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | When the key is not present in this object. |

**See Also**

- [#hasTimer](../android/os/health/HealthStats.md)) 

### getTimers

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimers(key: Int): MutableMap<String!, TimerStat!>!
```

Get the TimerStat map for the given key.

| Exceptions ||
|---------------------------------------|---------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | When the key is not present in this object. |

**See Also**

- [#hasTimers](../android/os/health/HealthStats.md)) 

### getTimersKeyAt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimersKeyAt(index: Int): Int
```

Get the key for the timer map at the given index. Index must be between 0 and the result of [getTimersKeyCount()](../android/os/health/HealthStats.md)). 
**See Also**

- [#getTimersKeyCount](../android/os/health/HealthStats.md)) 

### getTimersKeyCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimersKeyCount(): Int
```

Get the number of timer map values in this object. Can be used to iterate through the available timer maps. 
**See Also**

- [#getTimersKeyAt](../android/os/health/HealthStats.md)) 

### hasMeasurement

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasMeasurement(key: Int): Boolean
```

Return whether this object contains a measurement for the supplied key. 

### hasMeasurements

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasMeasurements(key: Int): Boolean
```

Return whether this object contains a measurements map for the supplied key. 

### hasStats

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasStats(key: Int): Boolean
```

Return whether this object contains a HealthStats map for the supplied key. 

### hasTimer

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasTimer(key: Int): Boolean
```

Return whether this object contains a TimerStat for the supplied key. 

### hasTimers

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasTimers(key: Int): Boolean
```

Return whether this object contains a timers map for the supplied key.
