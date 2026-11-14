Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SystemHealthManager

```
open class SystemHealthManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.health.SystemHealthManager](SystemHealthManager.md) |

Provides access to data about how various system resources are used by applications.

## Summary

| Public methods ||
|---|---|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#getCpuHeadroom(android.os.CpuHeadroomParams)(params: https://developer.android.com/reference/kotlin/android/os/CpuHeadroomParams.html#?)` Provides an estimate of available CPU capacity headroom of the device. |
| open [Pair](../android.util/Pair.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#getCpuHeadroomCalculationWindowRange()()` Gets the range of the calculation window size for CPU headroom. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#getCpuHeadroomMinIntervalMillis()()` Gets minimum polling interval for calling `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#getCpuHeadroom(android.os.CpuHeadroomParams)` in milliseconds. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#getGpuHeadroom(android.os.GpuHeadroomParams)(params: https://developer.android.com/reference/kotlin/android/os/GpuHeadroomParams.html#?)` Provides an estimate of available GPU capacity headroom of the device. |
| open [Pair](../android.util/Pair.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#getGpuHeadroomCalculationWindowRange()()` Gets the range of the calculation window size for GPU headroom. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#getGpuHeadroomMinIntervalMillis()()` Gets minimum polling interval for calling `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#getGpuHeadroom(android.os.GpuHeadroomParams)` in milliseconds. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#getMaxCpuHeadroomTidsSize()()` Gets the maximum number of TIDs this device supports for getting CPU headroom. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#getPowerMonitorReadings(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(powerMonitors: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/os/PowerMonitor.html#!>, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#?, onResult: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/os/PowerMonitorReadings.html#!, https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#!>)` Asynchronously retrieves the accumulated power consumption reported by the specified power monitors. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#getSupportedPowerMonitors(java.util.concurrent.Executor,%20java.util.function.Consumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#?, onResult: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/os/PowerMonitor.html#!>!>)` Asynchronously retrieves a list of supported `https://developer.android.com/reference/kotlin/android/os/PowerMonitor.html#`'s, which include raw ODPM (on-device power rail monitor) rails and modeled energy consumers. |
| --- | --- |
| open [HealthStats](HealthStats.md)! | `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#takeMyUidSnapshot()()` Return a `https://developer.android.com/reference/kotlin/android/os/health/HealthStats` object containing a snapshot of system health metrics for the application calling this API. |
| open [HealthStats](HealthStats.md)! | `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#takeUidSnapshot(kotlin.Int)(uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return a `https://developer.android.com/reference/kotlin/android/os/health/HealthStats` object containing a snapshot of system health metrics for the given uid (user-id, which in usually corresponds to application). |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [HealthStats](HealthStats.md)!\>! | `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#takeUidSnapshots(kotlin.IntArray)(uids: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!)` Return a `https://developer.android.com/reference/kotlin/android/os/health/HealthStats` object containing a snapshot of system health metrics for the given uids (user-id, which in usually corresponds to application). |
| --- | --- |

## Public methods

### getCpuHeadroom

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCpuHeadroom(params: CpuHeadroomParams?): Float
```

Provides an estimate of available CPU capacity headroom of the device.

The value can be used by the calling application to determine if the workload was CPU bound and then take action accordingly to ensure that the workload can be completed smoothly. It can also be used with the thermal status and headroom to determine if reducing the CPU bound workload can help reduce the device temperature to avoid thermal throttling.

If the params are valid, each call will perform at least one synchronous binder transaction that can take more than 1ms. So it's not recommended to call or wait for this on critical threads. Some devices may implement this as an on-demand API with lazy initialization, so the caller should expect higher latency when making the first call (especially with non-default params) since app starts or after changing params, as the device may need to change its data collection.

| Parameters ||
|---|---|
| `params` | [CpuHeadroomParams](../android.os/CpuHeadroomParams.md)?: params to customize the CPU headroom calculation, or null to use default. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | a single value headroom or a `Float.NaN` if it's temporarily unavailable due to server error or not enough user CPU workload. Each valid value ranges from \[0, 100\], where 0 indicates no more cpu resources can be granted. Value is between 0.0f and 100.0f inclusive |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the params are invalid. |
| `java.lang.IllegalStateException` | if the TIDs of the params don't have the same affinity setting. |
| `java.lang.SecurityException` | if the TIDs of the params don't belong to the same process. |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the API is unsupported. |

### getCpuHeadroomCalculationWindowRange

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCpuHeadroomCalculationWindowRange(): Pair<Int!, Int!>
```

Gets the range of the calculation window size for CPU headroom.

See `https://developer.android.com/reference/kotlin/android/os/CpuHeadroomParams.Builder.html#setCalculationWindowMillis(kotlin.Int)`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Pair.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | the range of the calculation window size supported in milliseconds. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the CPU headroom API is unsupported. |

### getCpuHeadroomMinIntervalMillis

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCpuHeadroomMinIntervalMillis(): Long
```

Gets minimum polling interval for calling `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#getCpuHeadroom(android.os.CpuHeadroomParams)` in milliseconds.

The `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#getCpuHeadroom(android.os.CpuHeadroomParams)` API may return cached result if called more frequent than the interval.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the API is unsupported. |

### getGpuHeadroom

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGpuHeadroom(params: GpuHeadroomParams?): Float
```

Provides an estimate of available GPU capacity headroom of the device.

The value can be used by the calling application to determine if the workload was GPU bound and then take action accordingly to ensure that the workload can be completed smoothly. It can also be used with the thermal status and headroom to determine if reducing the GPU bound workload can help reduce the device temperature to avoid thermal throttling.

If the params are valid, each call will perform at least one synchronous binder transaction that can take more than 1ms. So it's not recommended to call or wait for this on critical threads. Some devices may implement this as an on-demand API with lazy initialization, so the caller should expect higher latency when making the first call (especially with non-default params) since app starts or after changing params, as the device may need to change its data collection.

| Parameters ||
|---|---|
| `params` | [GpuHeadroomParams](../android.os/GpuHeadroomParams.md)?: params to customize the GPU headroom calculation, or null to use default. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | a single value headroom or a `Float.NaN` if it's temporarily unavailable. Each valid value ranges from \[0, 100\], where 0 indicates no more cpu resources can be granted. Value is between 0.0f and 100.0f inclusive |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the params are invalid. |
| `java.lang.UnsupportedOperationException` | if the API is unsupported. |

### getGpuHeadroomCalculationWindowRange

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGpuHeadroomCalculationWindowRange(): Pair<Int!, Int!>
```

Gets the range of the calculation window size for GPU headroom.

See `https://developer.android.com/reference/kotlin/android/os/GpuHeadroomParams.Builder.html#setCalculationWindowMillis(kotlin.Int)`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Pair.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | the range of the calculation window size supported in milliseconds. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the GPU headroom API is unsupported. |

### getGpuHeadroomMinIntervalMillis

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGpuHeadroomMinIntervalMillis(): Long
```

Gets minimum polling interval for calling `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#getGpuHeadroom(android.os.GpuHeadroomParams)` in milliseconds.

The `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#getGpuHeadroom(android.os.GpuHeadroomParams)` API may return cached result if called more frequent than the interval.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the API is unsupported. |

### getMaxCpuHeadroomTidsSize

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMaxCpuHeadroomTidsSize(): Int
```

Gets the maximum number of TIDs this device supports for getting CPU headroom.

See `https://developer.android.com/reference/kotlin/android/os/CpuHeadroomParams.Builder.html#setTids(kotlin.Int)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the maximum size of TIDs supported. Value is 1 or greater |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the CPU headroom API is unsupported. |

### getPowerMonitorReadings

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPowerMonitorReadings(
    powerMonitors: MutableList<PowerMonitor!>, 
    executor: Executor?, 
    onResult: OutcomeReceiver<PowerMonitorReadings!, RuntimeException!>
): Unit
```

Asynchronously retrieves the accumulated power consumption reported by the specified power monitors.

| Parameters ||
|---|---|
| `powerMonitors` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PowerMonitor](../android.os/PowerMonitor.md)!\>: power monitors to be retrieved. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md)?: optional Executor to deliver the callbacks. If not supplied, the callback may be invoked on an arbitrary thread. This value may be `null`. |
| `onResult` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [PowerMonitorReadings](../android.os/PowerMonitorReadings.md)!, [RuntimeException](../java.lang/RuntimeException.md)!\>: callback for the result. This value cannot be `null`. |
| --- | --- |

### getSupportedPowerMonitors

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSupportedPowerMonitors(
    executor: Executor?, 
    onResult: Consumer<MutableList<PowerMonitor!>!>
): Unit
```

Asynchronously retrieves a list of supported `https://developer.android.com/reference/kotlin/android/os/PowerMonitor.html#`'s, which include raw ODPM (on-device power rail monitor) rails and modeled energy consumers. If ODPM is unsupported on this device this method delivers an empty list.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md)?: optional Handler to deliver the callback. If not supplied, the callback may be invoked on an arbitrary thread. This value may be `null`. |
| `onResult` | [Consumer](../java.util.function/Consumer.md)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PowerMonitor](../android.os/PowerMonitor.md)!\>!\>: callback for the result. This value cannot be `null`. |

### takeMyUidSnapshot

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun takeMyUidSnapshot(): HealthStats!
```

Return a `https://developer.android.com/reference/kotlin/android/os/health/HealthStats` object containing a snapshot of system health metrics for the application calling this API. This method is the same as calling `takeUidSnapshot(Process.myUid())`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/health/HealthStats!` | A `https://developer.android.com/reference/kotlin/android/os/health/HealthStats` object containing the metrics for this application. The keys for this HealthStats object will be from the `https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats` class. |

### takeUidSnapshot

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun takeUidSnapshot(uid: Int): HealthStats!
```

Return a `https://developer.android.com/reference/kotlin/android/os/health/HealthStats` object containing a snapshot of system health metrics for the given uid (user-id, which in usually corresponds to application).

| Parameters ||
|---|---|
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): User ID for a given application. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/health/HealthStats!` | A `https://developer.android.com/reference/kotlin/android/os/health/HealthStats` object containing the metrics for the requested application. The keys for this HealthStats object will be from the `https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats` class. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller attempts to retrieve stats for a uid other than its own without holding the appropriate permission. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/Process.html#myUid()`

### takeUidSnapshots

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun takeUidSnapshots(uids: IntArray!): Array<HealthStats!>!
```

Return a `https://developer.android.com/reference/kotlin/android/os/health/HealthStats` object containing a snapshot of system health metrics for the given uids (user-id, which in usually corresponds to application).

| Parameters ||
|---|---|
| `uids` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: An array of User IDs to retrieve. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/os/health/HealthStats!>!` | An array of `https://developer.android.com/reference/kotlin/android/os/health/HealthStats` objects containing the metrics for each of the requested uids. The keys for this HealthStats object will be from the `https://developer.android.com/reference/kotlin/android/os/health/UidHealthStats` class. |
