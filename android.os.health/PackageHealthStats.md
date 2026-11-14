# PackageHealthStats

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PackageHealthStats

Kotlin| [Java](../android/os/health/PackageHealthStats.md) 
| --- | --- |

```
class PackageHealthStats
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.health.PackageHealthStats](../android/os/health/PackageHealthStats.md) |

Keys for [HealthStats](../android/os/health/HealthStats.md) returned from [HealthStats.getStats(int)](../android/os/health/HealthStats.md))with the [UidHealthStats.STATS_PACKAGES](../android/os/health/UidHealthStats.md) key.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENTS_WAKEUP_ALARMS_COUNT](../android/os/health/PackageHealthStats.md) Key for a map of the number of times that a package's wakeup alarms have fired while the device was on battery. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATS_SERVICES](../android/os/health/PackageHealthStats.md) Key for a HealthStats with [ServiceHealthStats](../android/os/health/ServiceHealthStats.md) keys for each of the services defined in this apk. |

## Constants

### MEASUREMENTS_WAKEUP_ALARMS_COUNT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENTS_WAKEUP_ALARMS_COUNT: Int
```

Key for a map of the number of times that a package's wakeup alarms have fired while the device was on battery. 

 Value: 40002

**See Also**

- [android.app.AlarmManager](../android/app/AlarmManager.md) 

### STATS_SERVICES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATS_SERVICES: Int
```

Key for a HealthStats with [ServiceHealthStats](../android/os/health/ServiceHealthStats.md) keys for each of the services defined in this apk. 

 Value: 40001
