# PidHealthStats

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PidHealthStats

Kotlin| [Java](PidHealthStats.md) 
| --- | --- |

```
class PidHealthStats
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.health.PidHealthStats](PidHealthStats.md) |

Keys for [HealthStats](HealthStats.md) returned from [HealthStats.getStats(int)](HealthStats.md))with the [UidHealthStats.STATS_PIDS](UidHealthStats.md) key.

The values coming from PidHealthStats are a little bit different from the other HealthStats values. These values are not aggregate or historical values, but instead live values from when the snapshot is taken. These tend to be more useful in debugging rogue processes than in gathering aggregate metrics across the fleet of devices.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_WAKE_NESTING_COUNT](PidHealthStats.md) Key for a measurement of the current nesting depth of wakelocks for this process. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_WAKE_START_MS](PidHealthStats.md) Key for a measurement of the time in the [android.os.SystemClock#elapsedRealtime](../android.os/SystemClock.md))timebase that a wakelock was first acquired in this process. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_WAKE_SUM_MS](PidHealthStats.md) Key for a measurement of the total number of milleseconds that this process has held a wake lock. |
| --- | --- |

## Constants

### MEASUREMENT_WAKE_NESTING_COUNT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_WAKE_NESTING_COUNT: Int
```

Key for a measurement of the current nesting depth of wakelocks for this process. That is to say, the number of times a nested wakelock has been started but not stopped. A high number here indicates an improperly paired wakelock acquire/release combination.

More details on the individual wake locks is available by getting the [UidHealthStats.TIMERS_WAKELOCKS_FULL](UidHealthStats.md), [UidHealthStats.TIMERS_WAKELOCKS_PARTIAL](UidHealthStats.md), [UidHealthStats.TIMERS_WAKELOCKS_WINDOW](UidHealthStats.md) and [UidHealthStats.TIMERS_WAKELOCKS_DRAW](UidHealthStats.md) keys. 

 Value: 20001

### MEASUREMENT_WAKE_START_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_WAKE_START_MS: Int
```

Key for a measurement of the time in the [android.os.SystemClock#elapsedRealtime](../android.os/SystemClock.md))timebase that a wakelock was first acquired in this process.

More details on the individual wake locks is available by getting the [UidHealthStats.TIMERS_WAKELOCKS_FULL](UidHealthStats.md), [UidHealthStats.TIMERS_WAKELOCKS_PARTIAL](UidHealthStats.md), [UidHealthStats.TIMERS_WAKELOCKS_WINDOW](UidHealthStats.md) and [UidHealthStats.TIMERS_WAKELOCKS_DRAW](UidHealthStats.md) keys. 

 Value: 20003

### MEASUREMENT_WAKE_SUM_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_WAKE_SUM_MS: Int
```

Key for a measurement of the total number of milleseconds that this process has held a wake lock.

More details on the individual wake locks is available by getting the [UidHealthStats.TIMERS_WAKELOCKS_FULL](UidHealthStats.md), [UidHealthStats.TIMERS_WAKELOCKS_PARTIAL](UidHealthStats.md), [UidHealthStats.TIMERS_WAKELOCKS_WINDOW](UidHealthStats.md) and [UidHealthStats.TIMERS_WAKELOCKS_DRAW](UidHealthStats.md) keys. 

 Value: 20002
