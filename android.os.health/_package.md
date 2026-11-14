# android.os.health

# android.os.health

Kotlin| [Java](_package.md)
| --- | --- |

## Classes

| [HealthStats](HealthStats.md) | A HealthStats object contains system health data about an application. |
| --- | --- |
| [PackageHealthStats](PackageHealthStats.md) | Keys for [HealthStats](HealthStats.md) returned from [HealthStats.getStats(int)](HealthStats.md))with the [UidHealthStats.STATS_PACKAGES](UidHealthStats.md) key. |
| [PidHealthStats](PidHealthStats.md) | Keys for [HealthStats](HealthStats.md) returned from [HealthStats.getStats(int)](HealthStats.md))with the [UidHealthStats.STATS_PIDS](UidHealthStats.md) key. |
| [ProcessHealthStats](ProcessHealthStats.md) | Keys for [HealthStats](HealthStats.md) returned from [HealthStats.getStats(int)](HealthStats.md))with the [UidHealthStats.STATS_PROCESSES](UidHealthStats.md) key. |
| --- | --- |
| [ServiceHealthStats](ServiceHealthStats.md) | Keys for [HealthStats](HealthStats.md) returned from [HealthStats.getStats(int)](HealthStats.md))with the [PackageHealthStats.STATS_SERVICES](PackageHealthStats.md) key. |
| [SystemHealthManager](SystemHealthManager.md) | Provides access to data about how various system resources are used by applications. |
| [TimerStat](TimerStat.md) | A TimerStat object stores a count and a time. |
| --- | --- |
| [UidHealthStats](UidHealthStats.md) | Keys for [HealthStats](HealthStats.md) returned from [SystemHealthManager.takeUidSnapshot(int)](SystemHealthManager.md)), [SystemHealthManager.takeMyUidSnapshot()](SystemHealthManager.md)), and[SystemHealthManager.takeUidSnapshots(int[])](https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#takeUidSnapshots(kotlin.IntArray)). |
