# WorkDuration

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WorkDuration

Kotlin| [Java](../android/os/WorkDuration.md) 
| --- | --- |

```
class WorkDuration
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.WorkDuration](../android/os/WorkDuration.md) |

WorkDuration contains the measured time in nano seconds of the workload in each component, see [PerformanceHintManager.Session.reportActualWorkDuration(WorkDuration)](../android/os/PerformanceHintManager.Session.md)). All timings should be in [SystemClock.uptimeNanos()](../android/os/SystemClock.md))and measured in wall time.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------|---|
| [WorkDuration](../android/os/WorkDuration.md))`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/os/WorkDuration.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getActualCpuDurationNanos](../android/os/WorkDuration.md))`()` Returns the actual CPU duration in nanoseconds. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getActualGpuDurationNanos](../android/os/WorkDuration.md))`()` Returns the actual GPU duration in nanoseconds. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getActualTotalDurationNanos](../android/os/WorkDuration.md))`()` Returns the actual total duration in nanoseconds. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getWorkPeriodStartTimestampNanos](../android/os/WorkDuration.md))`()` Returns the work period start timestamp based in nanoseconds. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/os/WorkDuration.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setActualCpuDurationNanos](../android/os/WorkDuration.md))`(`actualCpuDurationNanos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the actual CPU duration in nanoseconds. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setActualGpuDurationNanos](../android/os/WorkDuration.md))`(`actualGpuDurationNanos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the actual GPU duration in nanoseconds. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setActualTotalDurationNanos](../android/os/WorkDuration.md))`(`actualTotalDurationNanos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the actual total duration in nanoseconds. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWorkPeriodStartTimestampNanos](../android/os/WorkDuration.md))`(`workPeriodStartTimestampNanos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the work period start timestamp in nanoseconds. |

## Public constructors

### WorkDuration

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WorkDuration()
```

## Public methods

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getActualCpuDurationNanos

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActualCpuDurationNanos(): Long
```

Returns the actual CPU duration in nanoseconds. All timings should be in [SystemClock.uptimeNanos()](../android/os/SystemClock.md)). 

### getActualGpuDurationNanos

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActualGpuDurationNanos(): Long
```

Returns the actual GPU duration in nanoseconds. All timings should be in [SystemClock.uptimeNanos()](../android/os/SystemClock.md)). 

### getActualTotalDurationNanos

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActualTotalDurationNanos(): Long
```

Returns the actual total duration in nanoseconds. All timings should be in [SystemClock.uptimeNanos()](../android/os/SystemClock.md)). 

### getWorkPeriodStartTimestampNanos

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWorkPeriodStartTimestampNanos(): Long
```

Returns the work period start timestamp based in nanoseconds. All timings should be in [SystemClock.uptimeNanos()](../android/os/SystemClock.md)). 

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### setActualCpuDurationNanos

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setActualCpuDurationNanos(actualCpuDurationNanos: Long): Unit
```

Sets the actual CPU duration in nanoseconds. All timings should be in [SystemClock.uptimeNanos()](../android/os/SystemClock.md)). 

### setActualGpuDurationNanos

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setActualGpuDurationNanos(actualGpuDurationNanos: Long): Unit
```

Sets the actual GPU duration in nanoseconds. All timings should be in [SystemClock.uptimeNanos()](../android/os/SystemClock.md)). 

### setActualTotalDurationNanos

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setActualTotalDurationNanos(actualTotalDurationNanos: Long): Unit
```

Sets the actual total duration in nanoseconds. All timings should be in [SystemClock.uptimeNanos()](../android/os/SystemClock.md)). 

### setWorkPeriodStartTimestampNanos

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setWorkPeriodStartTimestampNanos(workPeriodStartTimestampNanos: Long): Unit
```

Sets the work period start timestamp in nanoseconds. All timings should be in [SystemClock.uptimeNanos()](../android/os/SystemClock.md)).
