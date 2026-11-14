# PerformanceHintManager

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PerformanceHintManager

Kotlin| [Java](../android/os/PerformanceHintManager.md) 
| --- | --- |

```
class PerformanceHintManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.PerformanceHintManager](../android/os/PerformanceHintManager.md) |

The PerformanceHintManager allows apps to send performance hint to system.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Session](../android/os/PerformanceHintManager.Session.md) A Session represents a group of threads with an inter-related workload such that hints for their performance should be considered as a unit. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PerformanceHintManager.Session](../android/os/PerformanceHintManager.Session.md)? | [createHintSession](../android/os/PerformanceHintManager.md))`(`tids:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`, `initialTargetWorkDurationNanos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Creates a [Session](../android/os/PerformanceHintManager.Session.md) for the given set of threads and sets their initial target work duration. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getPreferredUpdateRateNanos](../android/os/PerformanceHintManager.md))`()` Get preferred update rate information for this device. |

## Public methods

### createHintSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createHintSession(
    tids: IntArray, 
    initialTargetWorkDurationNanos: Long
): PerformanceHintManager.Session?
```

Creates a [Session](../android/os/PerformanceHintManager.Session.md) for the given set of threads and sets their initial target work duration.

| Parameters ||
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tids` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html):The list of threads to be associated with this session. They must be part of this process' thread group This value cannot be`null`. |
| `initialTargetWorkDurationNanos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The desired duration in nanoseconds for the new session |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PerformanceHintManager.Session](../android/os/PerformanceHintManager.Session.md)? | the new session if it is supported on this device, null if hint session is not supported on this device or the tid doesn't belong to the application |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the thread id list is empty, or initialTargetWorkDurationNanos is non-positive |

### getPreferredUpdateRateNanos

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPreferredUpdateRateNanos(): Long
```

Get preferred update rate information for this device.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the preferred update rate supported by device software |
