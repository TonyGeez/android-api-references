# PackageHealthStats

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PackageHealthStats

Kotlin| [Java](PackageHealthStats.md) 
| --- | --- |

```
class PackageHealthStats
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.health.PackageHealthStats](PackageHealthStats.md) |

Keys for [HealthStats](HealthStats.md) returned from [HealthStats.getStats(int)](HealthStats.md))with the [UidHealthStats.STATS_PACKAGES](UidHealthStats.md) key.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENTS_WAKEUP_ALARMS_COUNT](PackageHealthStats.md) Key for a map of the number of times that a package's wakeup alarms have fired while the device was on battery. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATS_SERVICES](PackageHealthStats.md) Key for a HealthStats with [ServiceHealthStats](ServiceHealthStats.md) keys for each of the services defined in this apk. |

## Constants

### MEASUREMENTS_WAKEUP_ALARMS_COUNT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENTS_WAKEUP_ALARMS_COUNT: Int
```

Key for a map of the number of times that a package's wakeup alarms have fired while the device was on battery. 

 Value: 40002

**See Also**

- [android.app.AlarmManager](../android.app/AlarmManager.md) 

### STATS_SERVICES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATS_SERVICES: Int
```

Key for a HealthStats with [ServiceHealthStats](ServiceHealthStats.md) keys for each of the services defined in this apk. 

 Value: 40001
