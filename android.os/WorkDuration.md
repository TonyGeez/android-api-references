# WorkDuration

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WorkDuration

Kotlin| [Java](https://developer.android.com/reference/android/os/WorkDuration "View this page in Java") 
| --- | --- |

```
class WorkDuration
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.WorkDuration](https://developer.android.com/reference/kotlin/android/os/WorkDuration#) |

WorkDuration contains the measured time in nano seconds of the workload in each component, see [PerformanceHintManager.Session.reportActualWorkDuration(WorkDuration)](https://developer.android.com/reference/kotlin/android/os/PerformanceHintManager.Session#reportActualWorkDuration(android.os.WorkDuration)). All timings should be in [SystemClock.uptimeNanos()](https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeNanos())and measured in wall time.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------|---|
| [WorkDuration](https://developer.android.com/reference/kotlin/android/os/WorkDuration#WorkDuration())`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/os/WorkDuration#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getActualCpuDurationNanos](https://developer.android.com/reference/kotlin/android/os/WorkDuration#getActualCpuDurationNanos())`()` Returns the actual CPU duration in nanoseconds. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getActualGpuDurationNanos](https://developer.android.com/reference/kotlin/android/os/WorkDuration#getActualGpuDurationNanos())`()` Returns the actual GPU duration in nanoseconds. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getActualTotalDurationNanos](https://developer.android.com/reference/kotlin/android/os/WorkDuration#getActualTotalDurationNanos())`()` Returns the actual total duration in nanoseconds. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getWorkPeriodStartTimestampNanos](https://developer.android.com/reference/kotlin/android/os/WorkDuration#getWorkPeriodStartTimestampNanos())`()` Returns the work period start timestamp based in nanoseconds. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/os/WorkDuration#hashCode())`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setActualCpuDurationNanos](https://developer.android.com/reference/kotlin/android/os/WorkDuration#setActualCpuDurationNanos(kotlin.Long))`(`actualCpuDurationNanos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the actual CPU duration in nanoseconds. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setActualGpuDurationNanos](https://developer.android.com/reference/kotlin/android/os/WorkDuration#setActualGpuDurationNanos(kotlin.Long))`(`actualGpuDurationNanos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the actual GPU duration in nanoseconds. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setActualTotalDurationNanos](https://developer.android.com/reference/kotlin/android/os/WorkDuration#setActualTotalDurationNanos(kotlin.Long))`(`actualTotalDurationNanos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the actual total duration in nanoseconds. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWorkPeriodStartTimestampNanos](https://developer.android.com/reference/kotlin/android/os/WorkDuration#setWorkPeriodStartTimestampNanos(kotlin.Long))`(`workPeriodStartTimestampNanos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the work period start timestamp in nanoseconds. |

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

Returns the actual CPU duration in nanoseconds. All timings should be in [SystemClock.uptimeNanos()](https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeNanos()). 

### getActualGpuDurationNanos

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActualGpuDurationNanos(): Long
```

Returns the actual GPU duration in nanoseconds. All timings should be in [SystemClock.uptimeNanos()](https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeNanos()). 

### getActualTotalDurationNanos

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActualTotalDurationNanos(): Long
```

Returns the actual total duration in nanoseconds. All timings should be in [SystemClock.uptimeNanos()](https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeNanos()). 

### getWorkPeriodStartTimestampNanos

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWorkPeriodStartTimestampNanos(): Long
```

Returns the work period start timestamp based in nanoseconds. All timings should be in [SystemClock.uptimeNanos()](https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeNanos()). 

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

Sets the actual CPU duration in nanoseconds. All timings should be in [SystemClock.uptimeNanos()](https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeNanos()). 

### setActualGpuDurationNanos

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setActualGpuDurationNanos(actualGpuDurationNanos: Long): Unit
```

Sets the actual GPU duration in nanoseconds. All timings should be in [SystemClock.uptimeNanos()](https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeNanos()). 

### setActualTotalDurationNanos

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setActualTotalDurationNanos(actualTotalDurationNanos: Long): Unit
```

Sets the actual total duration in nanoseconds. All timings should be in [SystemClock.uptimeNanos()](https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeNanos()). 

### setWorkPeriodStartTimestampNanos

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setWorkPeriodStartTimestampNanos(workPeriodStartTimestampNanos: Long): Unit
```

Sets the work period start timestamp in nanoseconds. All timings should be in [SystemClock.uptimeNanos()](https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeNanos()).
