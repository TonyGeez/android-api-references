# ProcessHealthStats

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProcessHealthStats

Kotlin| [Java](../android/os/health/ProcessHealthStats.md) 
| --- | --- |

```
class ProcessHealthStats
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.health.ProcessHealthStats](../android/os/health/ProcessHealthStats.md) |

Keys for [HealthStats](../android/os/health/HealthStats.md) returned from [HealthStats.getStats(int)](../android/os/health/HealthStats.md))with the [UidHealthStats.STATS_PROCESSES](../android/os/health/UidHealthStats.md) key.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_ANR_COUNT](../android/os/health/ProcessHealthStats.md) Key for a measurement of the number of ANRs that happened in this process. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_CRASHES_COUNT](../android/os/health/ProcessHealthStats.md) Key for a measurement of the number of crashes that happened in this process. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_FOREGROUND_MS](../android/os/health/ProcessHealthStats.md) Key for a measurement of the number of milliseconds this process spent with an activity in the foreground. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_STARTS_COUNT](../android/os/health/ProcessHealthStats.md) Key for a measurement of the number of times this process was started for any reason. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_SYSTEM_TIME_MS](../android/os/health/ProcessHealthStats.md) Key for a measurement of number of millseconds the CPU spent running in kernel space for this process. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_USER_TIME_MS](../android/os/health/ProcessHealthStats.md) Key for a measurement of number of millseconds the CPU spent running in user space for this process. |
| --- | --- |

## Constants

### MEASUREMENT_ANR_COUNT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_ANR_COUNT: Int
```

Key for a measurement of the number of ANRs that happened in this process. 

 Value: 30005

### MEASUREMENT_CRASHES_COUNT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_CRASHES_COUNT: Int
```

Key for a measurement of the number of crashes that happened in this process. 

 Value: 30004

### MEASUREMENT_FOREGROUND_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_FOREGROUND_MS: Int
```

Key for a measurement of the number of milliseconds this process spent with an activity in the foreground. 

 Value: 30006

### MEASUREMENT_STARTS_COUNT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_STARTS_COUNT: Int
```

Key for a measurement of the number of times this process was started for any reason. 

 Value: 30003

### MEASUREMENT_SYSTEM_TIME_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_SYSTEM_TIME_MS: Int
```

Key for a measurement of number of millseconds the CPU spent running in kernel space for this process. 

 Value: 30002

### MEASUREMENT_USER_TIME_MS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_USER_TIME_MS: Int
```

Key for a measurement of number of millseconds the CPU spent running in user space for this process. 

 Value: 30001
