# PidHealthStats

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PidHealthStats

Kotlin| [Java](https://developer.android.com/reference/android/os/health/PidHealthStats "View this page in Java") 
| --- | --- |

```
class PidHealthStats
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.health.PidHealthStats](https://developer.android.com/reference/kotlin/android/os/health/PidHealthStats#) |

Keys for [HealthStats](https://developer.android.com/reference/kotlin/android/os/health/HealthStats) returned from [HealthStats.getStats(int)](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getStats(kotlin.Int))with the [UidHealthStats.STATS_PIDS](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#STATS_PIDS:kotlin.Int) key.

The values coming from PidHealthStats are a little bit different from the other HealthStats values. These values are not aggregate or historical values, but instead live values from when the snapshot is taken. These tend to be more useful in debugging rogue processes than in gathering aggregate metrics across the fleet of devices.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_WAKE_NESTING_COUNT](https://developer.android.com/reference/kotlin/android/os/health/PidHealthStats#MEASUREMENT_WAKE_NESTING_COUNT:kotlin.Int) Key for a measurement of the current nesting depth of wakelocks for this process. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_WAKE_START_MS](https://developer.android.com/reference/kotlin/android/os/health/PidHealthStats#MEASUREMENT_WAKE_START_MS:kotlin.Int) Key for a measurement of the time in the [android.os.SystemClock#elapsedRealtime](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtime())timebase that a wakelock was first acquired in this process. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_WAKE_SUM_MS](https://developer.android.com/reference/kotlin/android/os/health/PidHealthStats#MEASUREMENT_WAKE_SUM_MS:kotlin.Int) Key for a measurement of the total number of milleseconds that this process has held a wake lock. |
| --- | --- |

## Constants

### MEASUREMENT_WAKE_NESTING_COUNT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_WAKE_NESTING_COUNT: Int
```

Key for a measurement of the current nesting depth of wakelocks for this process. That is to say, the number of times a nested wakelock has been started but not stopped. A high number here indicates an improperly paired wakelock acquire/release combination.

More details on the individual wake locks is available by getting the [UidHealthStats.TIMERS_WAKELOCKS_FULL](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMERS_WAKELOCKS_FULL:kotlin.Int), [UidHealthStats.TIMERS_WAKELOCKS_PARTIAL](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMERS_WAKELOCKS_PARTIAL:kotlin.Int), [UidHealthStats.TIMERS_WAKELOCKS_WINDOW](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMERS_WAKELOCKS_WINDOW:kotlin.Int) and [UidHealthStats.TIMERS_WAKELOCKS_DRAW](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMERS_WAKELOCKS_DRAW:kotlin.Int) keys. 

 Value: 20001

### MEASUREMENT_WAKE_START_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_WAKE_START_MS: Int
```

Key for a measurement of the time in the [android.os.SystemClock#elapsedRealtime](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtime())timebase that a wakelock was first acquired in this process.

More details on the individual wake locks is available by getting the [UidHealthStats.TIMERS_WAKELOCKS_FULL](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMERS_WAKELOCKS_FULL:kotlin.Int), [UidHealthStats.TIMERS_WAKELOCKS_PARTIAL](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMERS_WAKELOCKS_PARTIAL:kotlin.Int), [UidHealthStats.TIMERS_WAKELOCKS_WINDOW](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMERS_WAKELOCKS_WINDOW:kotlin.Int) and [UidHealthStats.TIMERS_WAKELOCKS_DRAW](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMERS_WAKELOCKS_DRAW:kotlin.Int) keys. 

 Value: 20003

### MEASUREMENT_WAKE_SUM_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_WAKE_SUM_MS: Int
```

Key for a measurement of the total number of milleseconds that this process has held a wake lock.

More details on the individual wake locks is available by getting the [UidHealthStats.TIMERS_WAKELOCKS_FULL](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMERS_WAKELOCKS_FULL:kotlin.Int), [UidHealthStats.TIMERS_WAKELOCKS_PARTIAL](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMERS_WAKELOCKS_PARTIAL:kotlin.Int), [UidHealthStats.TIMERS_WAKELOCKS_WINDOW](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMERS_WAKELOCKS_WINDOW:kotlin.Int) and [UidHealthStats.TIMERS_WAKELOCKS_DRAW](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#TIMERS_WAKELOCKS_DRAW:kotlin.Int) keys. 

 Value: 20002
