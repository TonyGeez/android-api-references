# PackageHealthStats

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PackageHealthStats

Kotlin| [Java](https://developer.android.com/reference/android/os/health/PackageHealthStats "View this page in Java") 

```
class PackageHealthStats
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.os.health.PackageHealthStats](https://developer.android.com/reference/kotlin/android/os/health/PackageHealthStats#) |

Keys for [HealthStats](https://developer.android.com/reference/kotlin/android/os/health/HealthStats) returned from [HealthStats.getStats(int)](https://developer.android.com/reference/kotlin/android/os/health/HealthStats#getStats(kotlin.Int))with the [UidHealthStats.STATS_PACKAGES](https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats#STATS_PACKAGES:kotlin.Int) key.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENTS_WAKEUP_ALARMS_COUNT](https://developer.android.com/reference/kotlin/android/os/health/PackageHealthStats#MEASUREMENTS_WAKEUP_ALARMS_COUNT:kotlin.Int) Key for a map of the number of times that a package's wakeup alarms have fired while the device was on battery. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATS_SERVICES](https://developer.android.com/reference/kotlin/android/os/health/PackageHealthStats#STATS_SERVICES:kotlin.Int) Key for a HealthStats with [ServiceHealthStats](https://developer.android.com/reference/kotlin/android/os/health/ServiceHealthStats) keys for each of the services defined in this apk. |

## Constants

### MEASUREMENTS_WAKEUP_ALARMS_COUNT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENTS_WAKEUP_ALARMS_COUNT: Int
```

Key for a map of the number of times that a package's wakeup alarms have fired while the device was on battery. 

 Value: 40002

**See Also**

- [android.app.AlarmManager](https://developer.android.com/reference/kotlin/android/app/AlarmManager.html#) 

### STATS_SERVICES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATS_SERVICES: Int
```

Key for a HealthStats with [ServiceHealthStats](https://developer.android.com/reference/kotlin/android/os/health/ServiceHealthStats) keys for each of the services defined in this apk. 

 Value: 40001
