Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProfilingManager

```
class ProfilingManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.os.ProfilingManager](https://developer.android.com/reference/kotlin/android/os/ProfilingManager#) |

This class allows the caller to:

- Request profiling and listen for results. Profiling types supported are: system traces, java heap dumps, heap profiles, and stack traces.
- Register triggers for the system to capture profiling on the apps behalf.

<br />

The `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#requestProfiling(kotlin.Int,%20android.os.Bundle,%20kotlin.String,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` API can be used to begin profiling. Profiling may be ended manually using the CancellationSignal provided in the request, or as a result of a timeout. The timeout may be either the system default or caller defined in the parameter bundle for select types.

The profiling results are delivered to the requesting app's data directory and a pointer to the file will be received using the app provided listeners.

Apps can provide listeners in one or both of two ways:

- A request-specific listener included with the request. This will trigger only with a result from the request it was provided with.
- A global listener provided by `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#registerForAllProfilingResults(java.util.concurrent.Executor,%20java.util.function.Consumer)`. This will be triggered for all results belonging to your app. This listener is the only way to receive results from system triggered profiling instances set up with `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#addProfilingTriggers(kotlin.collections.MutableList)`.

Requests are rate limited and not guaranteed to be filled. Rate limiting can be disabled for local testing of `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#requestProfiling(kotlin.Int,%20android.os.Bundle,%20kotlin.String,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` using the shell command `device_config put profiling_testing rate_limiter.disabled true`

For local testing, profiling results can be accessed more easily by enabling debug mode. This will retain output files in a temporary system directory. The locations of the retained files will be available in logcat. The behavior and command varies by version:

- For Android versions 16 and above, debug mode will retain both unredacted (where applicable) and redacted results in the temporary directory. It can be enabled with the shell command `device_config put profiling_testing delete_temporary_results.disabled true` and disabled by setting that same value back to false. Retained results are accessible on all build types.
- For Android version 15, debug mode will retain only the unredacted result (where applicable) in the temporary directory. It can be enabled with the shell command `device_config put profiling_testing delete_unredacted_trace.disabled true` and disabled by setting that same value back to false. The retained unredacted file can only be accessed on builds with root access. To access the redacted output file on an unrooted device, apps can copy the file from `/pkg/files/profiling/file.type` to `/pkg/cache/file.type`.

In order to test profiling triggers, enable testing mode for your app with the shell command `device_config put profiling_testing system_triggered_profiling.testing_package_name com.your.app` which will:

- Ensure that a background trace is running.
- Allow all triggers for the provided package name to pass the system level rate limiter. This mode will continue until manually stopped with the shell command `device_config delete profiling_testing system_triggered_profiling.testing_package_name`.

Results are redacted and contain specific information about the requesting process only.

Note: Check out [Capture Real User Data Using ProfilingManager](https://developer.android.com/topic/performance/tracing/profiling-manager/overview) for a detailed guide on using this API, covering capturing Profiling all they way through interpreting the results.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#PROFILING_TYPE_HEAP_PROFILE:kotlin.Int` Profiling type for `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#requestProfiling(kotlin.Int,%20android.os.Bundle,%20kotlin.String,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` to request a heap profile. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#PROFILING_TYPE_JAVA_HEAP_DUMP:kotlin.Int` Profiling type for `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#requestProfiling(kotlin.Int,%20android.os.Bundle,%20kotlin.String,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` to request a java heap dump. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#PROFILING_TYPE_STACK_SAMPLING:kotlin.Int` Profiling type for `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#requestProfiling(kotlin.Int,%20android.os.Bundle,%20kotlin.String,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` to request a stack sample. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#PROFILING_TYPE_SYSTEM_TRACE:kotlin.Int` Profiling type for `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#requestProfiling(kotlin.Int,%20android.os.Bundle,%20kotlin.String,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` to request a system trace. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#addAllProfilingTriggers()()` Register this process for all triggers. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#addProfilingTriggers(kotlin.collections.MutableList)(triggers: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger!>)` Register the provided list of triggers for this process. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#clearProfilingTriggers()()` Remove all triggers for this process. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#registerForAllProfilingResults(java.util.concurrent.Executor,%20java.util.function.Consumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/os/ProfilingResult!>)` Register a listener to be called for all profiling results for this uid. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#removeProfilingTriggersByType(kotlin.IntArray)(triggers: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)` Remove triggers for this process with trigger types in the provided list. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#requestProfiling(kotlin.Int,%20android.os.Bundle,%20kotlin.String,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer)(profilingType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, parameters: https://developer.android.com/reference/kotlin/android/os/Bundle?, tag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal?, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#?, listener: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/os/ProfilingResult!>?)` Request system profiling. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#requestRunningSystemTrace(kotlin.String)(tag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Request a snapshot of a background trace, if one is running. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#unregisterForAllProfilingResults(java.util.function.Consumer)(listener: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/os/ProfilingResult!>?)` Unregister a listener that was to be called for all profiling results. |

## Constants

### PROFILING_TYPE_HEAP_PROFILE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROFILING_TYPE_HEAP_PROFILE: Int
```

Profiling type for `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#requestProfiling(kotlin.Int,%20android.os.Bundle,%20kotlin.String,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` to request a heap profile.

 Value: 2

### PROFILING_TYPE_JAVA_HEAP_DUMP

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROFILING_TYPE_JAVA_HEAP_DUMP: Int
```

Profiling type for `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#requestProfiling(kotlin.Int,%20android.os.Bundle,%20kotlin.String,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` to request a java heap dump.

 Value: 1

### PROFILING_TYPE_STACK_SAMPLING

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROFILING_TYPE_STACK_SAMPLING: Int
```

Profiling type for `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#requestProfiling(kotlin.Int,%20android.os.Bundle,%20kotlin.String,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` to request a stack sample.

 Value: 3

### PROFILING_TYPE_SYSTEM_TRACE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROFILING_TYPE_SYSTEM_TRACE: Int
```

Profiling type for `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#requestProfiling(kotlin.Int,%20android.os.Bundle,%20kotlin.String,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` to request a system trace.

 Value: 4

## Public methods

### addAllProfilingTriggers

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addAllProfilingTriggers(): Unit
```

Register this process for all triggers.

Registering for all triggers is in addition to any specific triggers registered. Any triggers already registered when this is called, along with their parameters, will not be impacted. Any triggers specifically registered after calling this, along with any parameters set on them, will take precedence over what is set here.

See `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#addProfilingTriggers(kotlin.collections.MutableList)` for more on triggers.

### addProfilingTriggers

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addProfilingTriggers(triggers: MutableList<ProfilingTrigger!>): Unit
```

Register the provided list of triggers for this process.

Profiling triggers are system events that an app can register interest in, and then receive profiling data when any of the registered triggers occur. There is no guarantee that these triggers will be filled. Results, if available, will be delivered only to a global listener added using `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#registerForAllProfilingResults(java.util.concurrent.Executor,%20java.util.function.Consumer)`.

Only one of each trigger type can be added at a time.

- If the provided list contains a trigger type that is already registered then the new one will replace the existing one.
- If the provided list contains more than one trigger object for a trigger type then only one will be kept.

The filename of the file placed in app storage will contain the trigger type for which it was collected in the form: "trigger-type-x", where x is equal to the API value of the trigger type, found in `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger`. Example filename for `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_ANR:kotlin.Int`: profile_trigger-type-2_2025-01-23-04-56-12.perfetto-trace

Apps can define their own per-trigger rate limiting to help ensure they receive results aligned with their needs. More details can be found at `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger.Builder#setRateLimitingPeriodHours(kotlin.Int)`.

| Parameters ||
|---|---|
| `triggers` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ProfilingTrigger](https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger)!\>: This value cannot be `null`. |

### clearProfilingTriggers

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun clearProfilingTriggers(): Unit
```

Remove all triggers for this process.

### registerForAllProfilingResults

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerForAllProfilingResults(
    executor: Executor, 
    listener: Consumer<ProfilingResult!>
): Unit
```

Register a listener to be called for all profiling results for this uid. Listeners set here will be called in addition to any provided with the request.

Note: If a callback attempt fails (for example, because your app is killed while a trace is in progress) re-delivery may be attempted using a listener added via this method.

The provided executor may also be used for other tasks required by ProfilingManager such as cleaning up old delivered profiles.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor to call back with. This value cannot be `null`. |
| `listener` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [ProfilingResult](https://developer.android.com/reference/kotlin/android/os/ProfilingResult)!\>: Listener to be triggered with result. This value cannot be `null`. |

### removeProfilingTriggersByType

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeProfilingTriggersByType(triggers: IntArray): Unit
```

Remove triggers for this process with trigger types in the provided list.

| Parameters ||
|---|---|
| `triggers` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_APP_FULLY_DRAWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_ANR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_APP_REQUEST_RUNNING_TRACE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_KILL_FORCE_STOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_KILL_RECENTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_KILL_TASK_MANAGER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_OOM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_ANOMALY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_KILL_EXCESSIVE_CPU_USAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_COLD_START:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_APP_COMPAT:kotlin.Int` |

### requestProfiling

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun requestProfiling(
    profilingType: Int, 
    parameters: Bundle?, 
    tag: String?, 
    cancellationSignal: CancellationSignal?, 
    executor: Executor?, 
    listener: Consumer<ProfilingResult!>?
): Unit
```

Request system profiling.

Note: use of this API directly is not recommended for most use cases. Consider using the [higher level wrappers provided by AndroidX](https://developer.android.com/reference/androidx/core/os/Profiling) that will construct the request correctly, supporting available options with simplified request parameters.

Both a listener and an executor must be set at the time of the request for the request to be considered for fulfillment. Listener/executor pairs can be set in this method, with `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#registerForAllProfilingResults(java.util.concurrent.Executor,%20java.util.function.Consumer)`, or both. The listener and executor must be set together, in the same call. If no listener and executor combination is set, the request will be discarded and no callback will be received.

Requests will be rate limited and are not guaranteed to be filled.

There might be a delay before profiling begins. For continuous profiling types (system tracing, stack sampling, and heap profiling), we recommend starting the collection early and stopping it with `cancellationSignal` immediately after the area of interest to ensure that the section you want profiled is captured. For heap dumps, we recommend testing locally to ensure that the heap dump is collected at the proper time.

The provided executor may also be used to perform a cleanup of old delivered profiles, if necessary.

| Parameters ||
|---|---|
| `profilingType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Type of profiling to collect. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#PROFILING_TYPE_JAVA_HEAP_DUMP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#PROFILING_TYPE_HEAP_PROFILE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#PROFILING_TYPE_STACK_SAMPLING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#PROFILING_TYPE_SYSTEM_TRACE:kotlin.Int` |
| `parameters` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle)?: Bundle of request related parameters. If the bundle contains any unrecognized parameters, the request will be fail with `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#ERROR_FAILED_INVALID_REQUEST:kotlin.Int`. If the values for the parameters are out of supported range, the closest possible in range value will be chosen. Use of [androidx wrappers](https://developer.android.com/reference/androidx/core/os/Profiling) is recommended over generating this directly. This value may be `null`. |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: Caller defined data to help identify the output. The first 20 alphanumeric characters, plus dashes, will be lowercased and included in the output filename. This value may be `null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal)?: for caller requested cancellation. Results will be returned if available. If this is null, the requesting app will not be able to stop the collection. The collection will stop after timing out with either the provided configurations or with system defaults |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)?: The executor to call back with. Will only be used for the listener provided in this method. If this is null, and no global executor and listener combinations are registered at the time of the request, the request will be dropped. |
| `listener` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [ProfilingResult](https://developer.android.com/reference/kotlin/android/os/ProfilingResult)!\>?: Listener to be triggered with result. Any global listeners registered via `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#registerForAllProfilingResults(java.util.concurrent.Executor,%20java.util.function.Consumer)` will also be triggered. If this is null, and no global listener and executor combinations are registered at the time of the request, the request will be dropped. |

### requestRunningSystemTrace

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun requestRunningSystemTrace(tag: String?): Unit
```

Request a snapshot of a background trace, if one is running.

This request sends a `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_APP_REQUEST_RUNNING_TRACE:kotlin.Int` trigger. Apps must register interest in this trigger in order to receive the result using either `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#addProfilingTriggers(kotlin.collections.MutableList)` or `https://developer.android.com/reference/kotlin/android/os/ProfilingManager#addAllProfilingTriggers()`.

| Parameters ||
|---|---|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

### unregisterForAllProfilingResults

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterForAllProfilingResults(listener: Consumer<ProfilingResult!>?): Unit
```

Unregister a listener that was to be called for all profiling results. If no listener is provided, all listeners for this process that were not submitted with a profiling request will be removed.

| Parameters ||
|---|---|
| `listener` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [ProfilingResult](https://developer.android.com/reference/kotlin/android/os/ProfilingResult)!\>?: Listener to unregister and no longer be triggered with the results. Null to remove all global listeners for this uid. This value may be `null`. |
