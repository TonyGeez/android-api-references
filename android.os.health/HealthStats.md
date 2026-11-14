# HealthStats

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HealthStats

Kotlin | [Java](https://developer.android.com/reference/android/os/health/HealthStats "View this page in Java") 
| --- | --- |

```
open class HealthStats
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.health.HealthStats](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#) |

A HealthStats object contains system health data about an application.

**Data Types** 
Each of the keys references data in one of five data types:

A **measurement** metric contains a single `long` value. That value may be a count, a time, or some other type of value. The unit for a measurement (COUNT, MS, etc) will always be in the name of the constant for the key to retrieve it. For example, the [UidHealthStats.MEASUREMENT_WIFI_TX_MS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_WIFI_TX_MS:kotlin.Int) value is the number of milliseconds (ms) that were spent transmitting on wifi by an application. The [UidHealthStats.MEASUREMENT_MOBILE_RX_PACKETS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_MOBILE_RX_PACKETS:kotlin.Int) measurement is the number of packets received on behalf of an application. The [UidHealthStats.MEASUREMENT_TOUCH_USER_ACTIVITY_COUNT](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#MEASUREMENT_TOUCH_USER_ACTIVITY_COUNT:kotlin.Int) measurement is the number of times the user touched the screen, causing the screen to stay awake.

A **timer** metric contains an `int` count and a `long` time, measured in milliseconds. Timers track how many times a resource was used, and the total duration for that usage. For example, the [android.os.health.UidHealthStats#TIMER_FLASHLIGHT](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMER_FLASHLIGHT:kotlin.Int) timer tracks how many times the application turned on the flashlight, and for how many milliseconds total it kept it on.

A **measurement map** metric is a mapping of [java.lang.String](https://developer.android.com/reference/kotlin/java/lang/String.html#) names to [java.lang.Long](https://developer.android.com/reference/kotlin/java/lang/Long.html#) values. The names typically are application provided names. For example, the [PackageHealthStats.MEASUREMENTS_WAKEUP_ALARMS_COUNT](https://developer.android.com/reference/kotlin/android/os/health/PackageHealthStats#MEASUREMENTS_WAKEUP_ALARMS_COUNT:kotlin.Int) measurement map is a mapping of the tag provided to the [android.app.AlarmManager](https://developer.android.com/reference/kotlin/android/app/AlarmManager.html#) when the alarm is scheduled.

A **timer map** metric is a mapping of [java.lang.String](https://developer.android.com/reference/kotlin/java/lang/String.html#) names to [android.os.health.TimerStat](https://developer.android.com/reference/kotlin/android/os/health/TimerStat) objects. The names are typically application provided names. For example, the [UidHealthStats.TIMERS_WAKELOCKS_PARTIAL](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMERS_WAKELOCKS_PARTIAL:kotlin.Int) is a mapping of tag provided to the [android.os.PowerManager](https://developer.android.com/reference/kotlin/android/os/PowerManager.html#) when the wakelock is created to the number of times and for how long each wakelock was active.

Lastly, a **health stats** metric is a mapping of [java.lang.String](https://developer.android.com/reference/kotlin/java/lang/String.html#) names to a recursive [android.os.health.HealthStats](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#) object containing more detailed information. For example, the [UidHealthStats.STATS_PACKAGES](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#STATS_PACKAGES:kotlin.Int) metric is a mapping of the package names for each of the APKs sharing a uid to the information recorded for that apk. The returned HealthStats objects will each be associated with a different set of constants. For the HealthStats returned for UidHealthStats.STATS_PACKAGES, the keys come from the [android.os.health.PackageHealthStats](https://developer.android.com/reference/kotlin/android/os/health/PackageHealthStats) class.

The keys that are available are subject to change, depending on what a particular device or software version is capable of recording. Applications must handle the absence of data without crashing.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDataType](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getDataType())`()` Get a name representing the contents of this object. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMeasurement](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getMeasurement(kotlin.Int))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the measurement for the given key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMeasurementKeyAt](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getMeasurementKeyAt(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the key for the measurement at the given index. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMeasurementKeyCount](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getMeasurementKeyCount())`()` Get the number of measurement values in this object. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\>! | [getMeasurements](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getMeasurements(kotlin.Int))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the measurements map for the given key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMeasurementsKeyAt](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getMeasurementsKeyAt(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the key for the measurement map at the given index. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMeasurementsKeyCount](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getMeasurementsKeyCount())`()` Get the number of measurement map values in this object. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [HealthStats](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#)!\>! | [getStats](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getStats(kotlin.Int))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the HealthStats map for the given key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStatsKeyAt](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getStatsKeyAt(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the key for the timer at the given index. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStatsKeyCount](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getStatsKeyCount())`()` Get the number of HealthStat map values in this object. |
| open [TimerStat](https://developer.android.com/reference/kotlin/android/os/health/TimerStat)! | [getTimer](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getTimer(kotlin.Int))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return a TimerStat object for the given key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimerCount](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getTimerCount(kotlin.Int))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the count for the timer for the given key. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimerKeyAt](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getTimerKeyAt(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the key for the timer at the given index. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimerKeyCount](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getTimerKeyCount())`()` Get the number of timer values in this object. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimerTime](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getTimerTime(kotlin.Int))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the time for the timer for the given key, in milliseconds. |
| --- | --- |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [TimerStat](https://developer.android.com/reference/kotlin/android/os/health/TimerStat)!\>! | [getTimers](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getTimers(kotlin.Int))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the TimerStat map for the given key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimersKeyAt](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getTimersKeyAt(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the key for the timer map at the given index. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimersKeyCount](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getTimersKeyCount())`()` Get the number of timer map values in this object. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMeasurement](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#hasMeasurement(kotlin.Int))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return whether this object contains a measurement for the supplied key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMeasurements](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#hasMeasurements(kotlin.Int))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return whether this object contains a measurements map for the supplied key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStats](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#hasStats(kotlin.Int))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return whether this object contains a HealthStats map for the supplied key. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasTimer](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#hasTimer(kotlin.Int))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return whether this object contains a TimerStat for the supplied key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasTimers](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#hasTimers(kotlin.Int))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return whether this object contains a timers map for the supplied key. |

## Public methods

### getDataType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDataType(): String!
```

Get a name representing the contents of this object. 
**See Also**

- [android.os.health.UidHealthStats](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats)
- [android.os.health.PackageHealthStats](https://developer.android.com/reference/kotlin/android/os/health/PackageHealthStats)
- [android.os.health.PidHealthStats](https://developer.android.com/reference/kotlin/android/os/health/PidHealthStats)
- [android.os.health.ProcessHealthStats](https://developer.android.com/reference/kotlin/android/os/health/ProcessHealthStats)
- [android.os.health.ServiceHealthStats](https://developer.android.com/reference/kotlin/android/os/health/ServiceHealthStats) 

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

- [#hasMeasurement](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#hasMeasurement(kotlin.Int)) 

### getMeasurementKeyAt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMeasurementKeyAt(index: Int): Int
```

Get the key for the measurement at the given index. Index must be between 0 and the result of [getMeasurementKeyCount()](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getMeasurementKeyCount()). 
**See Also**

- [#getMeasurementKeyCount](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getMeasurementKeyCount()) 

### getMeasurementKeyCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMeasurementKeyCount(): Int
```

Get the number of measurement values in this object. Can be used to iterate through the available measurements. 
**See Also**

- [#getMeasurementKeyAt](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getMeasurementKeyAt(kotlin.Int)) 

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

- [#hasMeasurements](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#hasMeasurements(kotlin.Int)) 

### getMeasurementsKeyAt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMeasurementsKeyAt(index: Int): Int
```

Get the key for the measurement map at the given index. Index must be between 0 and the result of [getMeasurementsKeyCount()](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getMeasurementsKeyCount()). 
**See Also**

- [#getMeasurementsKeyCount](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getMeasurementsKeyCount()) 

### getMeasurementsKeyCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMeasurementsKeyCount(): Int
```

Get the number of measurement map values in this object. Can be used to iterate through the available measurement maps. 
**See Also**

- [#getMeasurementsKeyAt](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getMeasurementsKeyAt(kotlin.Int)) 

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

- [#hasStats](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#hasStats(kotlin.Int)) 

### getStatsKeyAt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStatsKeyAt(index: Int): Int
```

Get the key for the timer at the given index. Index must be between 0 and the result of [getStatsKeyCount()](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getStatsKeyCount()). 
**See Also**

- [#getStatsKeyCount](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getStatsKeyCount()) 

### getStatsKeyCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStatsKeyCount(): Int
```

Get the number of HealthStat map values in this object. Can be used to iterate through the available measurements. 
**See Also**

- [#getMeasurementKeyAt](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getMeasurementKeyAt(kotlin.Int)) 

### getTimer

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimer(key: Int): TimerStat!
```

Return a TimerStat object for the given key. This will allocate a new [TimerStat](https://developer.android.com/reference/kotlin/android/os/health/TimerStat) object, which may be wasteful. Instead, use [getTimerCount](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getTimerCount(kotlin.Int)) and [getTimerTime](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getTimerTime(kotlin.Int)).

| Exceptions ||
|---------------------------------------|---------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | When the key is not present in this object. |

**See Also**

- [#hasTimer](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#hasTimer(kotlin.Int)) 

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

- [#hasTimer](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#hasTimer(kotlin.Int)) 

### getTimerKeyAt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimerKeyAt(index: Int): Int
```

Get the key for the timer at the given index. Index must be between 0 and the result of [getTimerKeyCount()](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getTimerKeyCount()). 
**See Also**

- [#getTimerKeyCount](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getTimerKeyCount()) 

### getTimerKeyCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimerKeyCount(): Int
```

Get the number of timer values in this object. Can be used to iterate through the available timers. 
**See Also**

- [#getTimerKeyAt](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getTimerKeyAt(kotlin.Int)) 

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

- [#hasTimer](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#hasTimer(kotlin.Int)) 

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

- [#hasTimers](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#hasTimers(kotlin.Int)) 

### getTimersKeyAt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimersKeyAt(index: Int): Int
```

Get the key for the timer map at the given index. Index must be between 0 and the result of [getTimersKeyCount()](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getTimersKeyCount()). 
**See Also**

- [#getTimersKeyCount](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getTimersKeyCount()) 

### getTimersKeyCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimersKeyCount(): Int
```

Get the number of timer map values in this object. Can be used to iterate through the available timer maps. 
**See Also**

- [#getTimersKeyAt](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getTimersKeyAt(kotlin.Int)) 

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
