# ServiceHealthStats

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceHealthStats

Kotlin| [Java](https://developer.android.com/reference/android/os/health/ServiceHealthStats "View this page in Java") 

```
class ServiceHealthStats
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.os.health.ServiceHealthStats](https://developer.android.com/reference/kotlin/android/os/health/ServiceHealthStats#) |

Keys for [HealthStats](https://developer.android.com/reference/kotlin/android/os/health/HealthStats) returned from [HealthStats.getStats(int)](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getStats(kotlin.Int))with the [PackageHealthStats.STATS_SERVICES](https://developer.android.com/reference/kotlin/android/os/health/PackageHealthStats#STATS_SERVICES:kotlin.Int) key.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_LAUNCH_COUNT](https://developer.android.com/reference/kotlin/android/os/health/ServiceHealthStats#MEASUREMENT_LAUNCH_COUNT:kotlin.Int) Key for a measurement of the total number of times this service was started due to calls to [startService()](https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent))or android. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_START_SERVICE_COUNT](https://developer.android.com/reference/kotlin/android/os/health/ServiceHealthStats#MEASUREMENT_START_SERVICE_COUNT:kotlin.Int) Key for a measurement of the number of times this service was started due to calls to [startService()](https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)), including re-launches after crashes. |

## Constants

### MEASUREMENT_LAUNCH_COUNT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_LAUNCH_COUNT: Int
```

Key for a measurement of the total number of times this service was started due to calls to [startService()](https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent))or android.content.Context#bindService including re-launches after crashes. 

 Value: 50002

### MEASUREMENT_START_SERVICE_COUNT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_START_SERVICE_COUNT: Int
```

Key for a measurement of the number of times this service was started due to calls to [startService()](https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)), including re-launches after crashes. 

 Value: 50001
