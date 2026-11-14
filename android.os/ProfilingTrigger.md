Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProfilingTrigger

```
class ProfilingTrigger
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.ProfilingTrigger](../android/os/ProfilingTrigger.md) |

Encapsulates a single profiling trigger.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger.Builder` Builder class to create a `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#` object. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_ANOMALY:kotlin.Int` Trigger occurs when the system detects an anomalous behavior by the app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_ANR:kotlin.Int` Trigger occurs after an ANR has been identified, but before the system would attempt to kill the app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_APP_COMPAT:kotlin.Int` Trigger occurs when the system detects an anomalous behavior by the app which will become unsupported in future Android versions. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_APP_FULLY_DRAWN:kotlin.Int` Trigger occurs after `https://developer.android.com/reference/kotlin/android/app/Activity.html#reportFullyDrawn()` is called for a cold start. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_APP_REQUEST_RUNNING_TRACE:kotlin.Int` Trigger occurs when an app requests the actively running trace by calling `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#requestRunningSystemTrace(kotlin.String)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_COLD_START:kotlin.Int` Trigger occurs as early as possible when an app cold starts. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_KILL_EXCESSIVE_CPU_USAGE:kotlin.Int` Trigger occurs when an app is killed due to excessive CPU usage with an `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo.html#getReason()` of `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo.html#REASON_EXCESSIVE_RESOURCE_USAGE:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_KILL_FORCE_STOP:kotlin.Int` Trigger occurs when an app is killed due to the user clicking the "Force stop" button of the App info page in Settings. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_KILL_RECENTS:kotlin.Int` Trigger occurs when an app is killed due to the user removing it in the [Recents screen](https://developer.android.com/guide/components/activities/recents). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_KILL_TASK_MANAGER:kotlin.Int` Trigger occurs when an app is killed due to the user clicking the "Stop" button for the application in [Task Manager](https://developer.android.com/develop/background-work/services/fgs/handle-user-stopping). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_NONE:kotlin.Int` No trigger. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_OOM:kotlin.Int` Trigger occurs when an app has an Out Of Memory Exception. |
| --- | --- |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#getRateLimitingPeriodHours()()` The requester set rate limiting period in hours. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#getTriggerType()()` The trigger type indicates which event should trigger the requested profiling. |

## Constants

### TRIGGER_TYPE_ANOMALY

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRIGGER_TYPE_ANOMALY: Int
```

Trigger occurs when the system detects an anomalous behavior by the app. Anomalous behaviors may span all areas. The artifact returned will vary by the anomaly.

The tag returned with the `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#getTag()` will contain additional information about the type of anomaly.

Note: For some anomalous behaviors, the system may not provide artifacts if this trigger is registered by more than one package with the same user id (see PackageManager#getPackagesForUid(int)).

 Value: 8

### TRIGGER_TYPE_ANR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRIGGER_TYPE_ANR: Int
```

Trigger occurs after an ANR has been identified, but before the system would attempt to kill the app. The trigger does not necessarily indicate that the app was killed due to the ANR.

System will provide a snapshot of a running system trace in response to this trigger.

 Value: 2

### TRIGGER_TYPE_APP_COMPAT

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRIGGER_TYPE_APP_COMPAT: Int
```

Trigger occurs when the system detects an anomalous behavior by the app which will become unsupported in future Android versions. The artifact returned will vary by the anomaly.

The tag returned with the `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#getTag()` will contain additional information about the app compatibility issues.

 Value: 11

### TRIGGER_TYPE_APP_FULLY_DRAWN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRIGGER_TYPE_APP_FULLY_DRAWN: Int
```

Trigger occurs after `https://developer.android.com/reference/kotlin/android/app/Activity.html#reportFullyDrawn()` is called for a cold start.

System will provide a snapshot of a running system trace in response to this trigger.

 Value: 1

### TRIGGER_TYPE_APP_REQUEST_RUNNING_TRACE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRIGGER_TYPE_APP_REQUEST_RUNNING_TRACE: Int
```

Trigger occurs when an app requests the actively running trace by calling `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#requestRunningSystemTrace(kotlin.String)`.

System will provide a snapshot of a running system trace in response to this trigger.

 Value: 3

### TRIGGER_TYPE_COLD_START

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRIGGER_TYPE_COLD_START: Int
```

Trigger occurs as early as possible when an app cold starts.

This happens when the `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo.html#getStartType()` start type is `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo.html#START_TYPE_COLD:kotlin.Int`.

The system will provide a newly started system trace and stack sampling profile in response to this trigger. Profiling will continue until the app calls `https://developer.android.com/reference/kotlin/android/app/Activity.html#reportFullyDrawn()`; otherwise, it will stop after a default period of 5 seconds.

The system uses a discard buffer for this trigger. This means that if the buffer fills up, newer events are discarded. This ensures that the earliest available tracepoints are always retained.

Note: There might be a delay before profiling begins, similar to when `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#requestProfiling(kotlin.Int,%20android.os.Bundle,%20kotlin.String,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` is used.

 Value: 10

### TRIGGER_TYPE_KILL_EXCESSIVE_CPU_USAGE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRIGGER_TYPE_KILL_EXCESSIVE_CPU_USAGE: Int
```

Trigger occurs when an app is killed due to excessive CPU usage with an `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo.html#getReason()` of `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo.html#REASON_EXCESSIVE_RESOURCE_USAGE:kotlin.Int`.

System will provide a snapshot of a running system trace in response to this trigger.

 Value: 9

### TRIGGER_TYPE_KILL_FORCE_STOP

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRIGGER_TYPE_KILL_FORCE_STOP: Int
```

Trigger occurs when an app is killed due to the user clicking the "Force stop" button of the App info page in Settings.

System will provide a snapshot of a running system trace in response to this trigger.

 Value: 4

### TRIGGER_TYPE_KILL_RECENTS

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRIGGER_TYPE_KILL_RECENTS: Int
```

Trigger occurs when an app is killed due to the user removing it in the [Recents screen](https://developer.android.com/guide/components/activities/recents).

System will provide a snapshot of a running system trace in response to this trigger.

 Value: 5

### TRIGGER_TYPE_KILL_TASK_MANAGER

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRIGGER_TYPE_KILL_TASK_MANAGER: Int
```

Trigger occurs when an app is killed due to the user clicking the "Stop" button for the application in [Task Manager](https://developer.android.com/develop/background-work/services/fgs/handle-user-stopping).

System will provide a snapshot of a running system trace in response to this trigger.

 Value: 6

### TRIGGER_TYPE_NONE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRIGGER_TYPE_NONE: Int
```

No trigger. Used in `https://developer.android.com/reference/kotlin/android/os/ProfilingResult` for non trigger caused results.

 Value: 0

### TRIGGER_TYPE_OOM

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRIGGER_TYPE_OOM: Int
```

Trigger occurs when an app has an Out Of Memory Exception.

System will provide a Java heap dump in response to this trigger.

Use of this trigger requires that any custom `https://developer.android.com/reference/kotlin/java/lang/Thread.UncaughtExceptionHandler.html#` call through to the default uncaught exception handler (`https://developer.android.com/reference/kotlin/java/lang/Thread.html#getDefaultUncaughtExceptionHandler()`). If the default uncaught exception handler is not called, then this trigger cannot be used. The app can still obtain a Java heap dump in this case, but will have to request the profiling itself using `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#requestProfiling(kotlin.Int,%20android.os.Bundle,%20kotlin.String,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`.

 Value: 7

## Public methods

### getRateLimitingPeriodHours

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRateLimitingPeriodHours(): Int
```

The requester set rate limiting period in hours.

The period is the minimum time the system should wait before providing another profiling result for the same trigger; actual time between events may be longer.

If the rate limiting period is set to 0, no app-provided rate limiting will be used.

This rate limiting is in addition to any system level rate limiting that may be applied.

### getTriggerType

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTriggerType(): Int
```

The trigger type indicates which event should trigger the requested profiling.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_APP_FULLY_DRAWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_ANR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_APP_REQUEST_RUNNING_TRACE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_KILL_FORCE_STOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_KILL_RECENTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_KILL_TASK_MANAGER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_OOM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_ANOMALY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_KILL_EXCESSIVE_CPU_USAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_COLD_START:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_APP_COMPAT:kotlin.Int` |
