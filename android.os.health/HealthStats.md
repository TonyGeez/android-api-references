# HealthStats

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HealthStats

Kotlin | [Java](HealthStats.md) 
| --- | --- |

```
open class HealthStats
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.health.HealthStats](HealthStats.md) |

A HealthStats object contains system health data about an application.

**Data Types** 
Each of the keys references data in one of five data types:

A **measurement** metric contains a single `long` value. That value may be a count, a time, or some other type of value. The unit for a measurement (COUNT, MS, etc) will always be in the name of the constant for the key to retrieve it. For example, the [UidHealthStats.MEASUREMENT_WIFI_TX_MS](UidHealthStats.md) value is the number of milliseconds (ms) that were spent transmitting on wifi by an application. The [UidHealthStats.MEASUREMENT_MOBILE_RX_PACKETS](UidHealthStats.md) measurement is the number of packets received on behalf of an application. The [UidHealthStats.MEASUREMENT_TOUCH_USER_ACTIVITY_COUNT](UidHealthStats.md) measurement is the number of times the user touched the screen, causing the screen to stay awake.

A **timer** metric contains an `int` count and a `long` time, measured in milliseconds. Timers track how many times a resource was used, and the total duration for that usage. For example, the [android.os.health.UidHealthStats#TIMER_FLASHLIGHT](UidHealthStats.md) timer tracks how many times the application turned on the flashlight, and for how many milliseconds total it kept it on.

A **measurement map** metric is a mapping of [java.lang.String](../java.lang/String.md) names to [java.lang.Long](../java.lang/Long.md) values. The names typically are application provided names. For example, the [PackageHealthStats.MEASUREMENTS_WAKEUP_ALARMS_COUNT](PackageHealthStats.md) measurement map is a mapping of the tag provided to the [android.app.AlarmManager](../android.app/AlarmManager.md) when the alarm is scheduled.

A **timer map** metric is a mapping of [java.lang.String](../java.lang/String.md) names to [android.os.health.TimerStat](TimerStat.md) objects. The names are typically application provided names. For example, the [UidHealthStats.TIMERS_WAKELOCKS_PARTIAL](UidHealthStats.md) is a mapping of tag provided to the [android.os.PowerManager](../android.os/PowerManager.md) when the wakelock is created to the number of times and for how long each wakelock was active.

Lastly, a **health stats** metric is a mapping of [java.lang.String](../java.lang/String.md) names to a recursive [android.os.health.HealthStats](HealthStats.md) object containing more detailed information. For example, the [UidHealthStats.STATS_PACKAGES](UidHealthStats.md) metric is a mapping of the package names for each of the APKs sharing a uid to the information recorded for that apk. The returned HealthStats objects will each be associated with a different set of constants. For the HealthStats returned for UidHealthStats.STATS_PACKAGES, the keys come from the [android.os.health.PackageHealthStats](PackageHealthStats.md) class.

The keys that are available are subject to change, depending on what a particular device or software version is capable of recording. Applications must handle the absence of data without crashing.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDataType](HealthStats.md))`()` Get a name representing the contents of this object. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMeasurement](HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the measurement for the given key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMeasurementKeyAt](HealthStats.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the key for the measurement at the given index. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMeasurementKeyCount](HealthStats.md))`()` Get the number of measurement values in this object. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\>! | [getMeasurements](HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the measurements map for the given key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMeasurementsKeyAt](HealthStats.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the key for the measurement map at the given index. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMeasurementsKeyCount](HealthStats.md))`()` Get the number of measurement map values in this object. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [HealthStats](HealthStats.md)!\>! | [getStats](HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the HealthStats map for the given key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStatsKeyAt](HealthStats.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the key for the timer at the given index. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStatsKeyCount](HealthStats.md))`()` Get the number of HealthStat map values in this object. |
| open [TimerStat](TimerStat.md)! | [getTimer](HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return a TimerStat object for the given key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimerCount](HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the count for the timer for the given key. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimerKeyAt](HealthStats.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the key for the timer at the given index. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimerKeyCount](HealthStats.md))`()` Get the number of timer values in this object. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimerTime](HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the time for the timer for the given key, in milliseconds. |
| --- | --- |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [TimerStat](TimerStat.md)!\>! | [getTimers](HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the TimerStat map for the given key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimersKeyAt](HealthStats.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the key for the timer map at the given index. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimersKeyCount](HealthStats.md))`()` Get the number of timer map values in this object. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMeasurement](HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return whether this object contains a measurement for the supplied key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMeasurements](HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return whether this object contains a measurements map for the supplied key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStats](HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return whether this object contains a HealthStats map for the supplied key. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasTimer](HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return whether this object contains a TimerStat for the supplied key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasTimers](HealthStats.md))`(`key:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return whether this object contains a timers map for the supplied key. |

## Public methods

### getDataType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDataType(): String!
```

Get a name representing the contents of this object. 
**See Also**

- [android.os.health.UidHealthStats](UidHealthStats.md)
- [android.os.health.PackageHealthStats](PackageHealthStats.md)
- [android.os.health.PidHealthStats](PidHealthStats.md)
- [android.os.health.ProcessHealthStats](ProcessHealthStats.md)
- [android.os.health.ServiceHealthStats](ServiceHealthStats.md) 

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

- [#hasMeasurement](HealthStats.md)) 

### getMeasurementKeyAt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMeasurementKeyAt(index: Int): Int
```

Get the key for the measurement at the given index. Index must be between 0 and the result of [getMeasurementKeyCount()](HealthStats.md)). 
**See Also**

- [#getMeasurementKeyCount](HealthStats.md)) 

### getMeasurementKeyCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMeasurementKeyCount(): Int
```

Get the number of measurement values in this object. Can be used to iterate through the available measurements. 
**See Also**

- [#getMeasurementKeyAt](HealthStats.md)) 

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

- [#hasMeasurements](HealthStats.md)) 

### getMeasurementsKeyAt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMeasurementsKeyAt(index: Int): Int
```

Get the key for the measurement map at the given index. Index must be between 0 and the result of [getMeasurementsKeyCount()](HealthStats.md)). 
**See Also**

- [#getMeasurementsKeyCount](HealthStats.md)) 

### getMeasurementsKeyCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMeasurementsKeyCount(): Int
```

Get the number of measurement map values in this object. Can be used to iterate through the available measurement maps. 
**See Also**

- [#getMeasurementsKeyAt](HealthStats.md)) 

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

- [#hasStats](HealthStats.md)) 

### getStatsKeyAt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStatsKeyAt(index: Int): Int
```

Get the key for the timer at the given index. Index must be between 0 and the result of [getStatsKeyCount()](HealthStats.md)). 
**See Also**

- [#getStatsKeyCount](HealthStats.md)) 

### getStatsKeyCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStatsKeyCount(): Int
```

Get the number of HealthStat map values in this object. Can be used to iterate through the available measurements. 
**See Also**

- [#getMeasurementKeyAt](HealthStats.md)) 

### getTimer

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimer(key: Int): TimerStat!
```

Return a TimerStat object for the given key. This will allocate a new [TimerStat](TimerStat.md) object, which may be wasteful. Instead, use [getTimerCount](HealthStats.md)) and [getTimerTime](HealthStats.md)).

| Exceptions ||
|---------------------------------------|---------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | When the key is not present in this object. |

**See Also**

- [#hasTimer](HealthStats.md)) 

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

- [#hasTimer](HealthStats.md)) 

### getTimerKeyAt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimerKeyAt(index: Int): Int
```

Get the key for the timer at the given index. Index must be between 0 and the result of [getTimerKeyCount()](HealthStats.md)). 
**See Also**

- [#getTimerKeyCount](HealthStats.md)) 

### getTimerKeyCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimerKeyCount(): Int
```

Get the number of timer values in this object. Can be used to iterate through the available timers. 
**See Also**

- [#getTimerKeyAt](HealthStats.md)) 

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

- [#hasTimer](HealthStats.md)) 

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

- [#hasTimers](HealthStats.md)) 

### getTimersKeyAt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimersKeyAt(index: Int): Int
```

Get the key for the timer map at the given index. Index must be between 0 and the result of [getTimersKeyCount()](HealthStats.md)). 
**See Also**

- [#getTimersKeyCount](HealthStats.md)) 

### getTimersKeyCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimersKeyCount(): Int
```

Get the number of timer map values in this object. Can be used to iterate through the available timer maps. 
**See Also**

- [#getTimersKeyAt](HealthStats.md)) 

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
