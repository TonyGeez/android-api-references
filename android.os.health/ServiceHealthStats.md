# ServiceHealthStats

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceHealthStats

Kotlin| [Java](../android/os/health/ServiceHealthStats.md) 
| --- | --- |

```
class ServiceHealthStats
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.health.ServiceHealthStats](../android/os/health/ServiceHealthStats.md) |

Keys for [HealthStats](../android/os/health/HealthStats.md) returned from [HealthStats.getStats(int)](../android/os/health/HealthStats.md))with the [PackageHealthStats.STATS_SERVICES](../android/os/health/PackageHealthStats.md) key.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_LAUNCH_COUNT](../android/os/health/ServiceHealthStats.md) Key for a measurement of the total number of times this service was started due to calls to [startService()](../android/content/Context.md))or android. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_START_SERVICE_COUNT](../android/os/health/ServiceHealthStats.md) Key for a measurement of the number of times this service was started due to calls to [startService()](../android/content/Context.md)), including re-launches after crashes. |

## Constants

### MEASUREMENT_LAUNCH_COUNT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_LAUNCH_COUNT: Int
```

Key for a measurement of the total number of times this service was started due to calls to [startService()](../android/content/Context.md))or android.content.Context#bindService including re-launches after crashes. 

 Value: 50002

### MEASUREMENT_START_SERVICE_COUNT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_START_SERVICE_COUNT: Int
```

Key for a measurement of the number of times this service was started due to calls to [startService()](../android/content/Context.md)), including re-launches after crashes. 

 Value: 50001
