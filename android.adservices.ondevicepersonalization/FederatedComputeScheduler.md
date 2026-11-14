Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FederatedComputeScheduler

Kotlin | [Java](FederatedComputeScheduler.md)
| --- | --- |

```
open class FederatedComputeScheduler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.FederatedComputeScheduler](FederatedComputeScheduler.md) |

Handles scheduling federated compute jobs. See getFederatedComputeScheduler.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduler.Params` The parameters related to job scheduling. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | cancel Cancels a federated compute job with input training params. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | schedule Schedules a federated compute job. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | schedule Schedules a federated compute job. |
| --- | --- |

## Public methods

### cancel

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cancel(input: FederatedComputeInput): Unit
```

**Deprecated:** *Deprecated in Java.*

Cancels a federated compute job with input training params. In onRequest, the app can call getFederatedComputeScheduler to pass scheduler when constructing the IsolatedWorker. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `input` | [FederatedComputeInput](FederatedComputeInput.md): the configuration of the federated compute. It should be consistent with the federated compute server setup. This value cannot be `null`. |

### schedule

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun schedule(
    params: FederatedComputeScheduler.Params, 
    input: FederatedComputeInput
): Unit
```

**Deprecated:** *Deprecated in Java.*

Schedules a federated compute job. In onRequest, the app can call getFederatedComputeScheduler to pass the scheduler when constructing the IsolatedWorker. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `params` | [FederatedComputeScheduler.Params](../android/adservices/ondevicepersonalization/FederatedComputeScheduler.Params.md): parameters related to job scheduling. This value cannot be `null`. |
| `input` | [FederatedComputeInput](FederatedComputeInput.md): the configuration of the federated computation. It should be consistent with the federated compute server setup as described in [Federated Compute Server documentation.](https://developers.google.com/privacy-sandbox/protections/on-device-personalization/federated-compute-server). This value cannot be `null`. |

### schedule

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun schedule(
    federatedComputeScheduleRequest: FederatedComputeScheduleRequest, 
    executor: Executor, 
    outcomeReceiver: OutcomeReceiver<FederatedComputeScheduleResponse!, Exception!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Schedules a federated compute job. In onRequest, the app can call getFederatedComputeScheduler to pass the scheduler when constructing the IsolatedWorker. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `federatedComputeScheduleRequest` | [FederatedComputeScheduleRequest](FederatedComputeScheduleRequest.md): input parameters related to job scheduling. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): the `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `outcomeReceiver` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [FederatedComputeScheduleResponse](FederatedComputeScheduleResponse.md)!, [Exception](../java.lang/Exception.md)!\>: This either returns a FederatedComputeScheduleResponse on success, or `https://developer.android.com/reference/kotlin/java/lang/Exception.html#` on failure. The exception type is OnDevicePersonalizationException with error code `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_INVALID_TRAINING_MANIFEST:kotlin.Int` if the manifest is missing the federated compute server URL or `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_SCHEDULE_TRAINING_FAILED:kotlin.Int` when scheduling fails for other reasons. This value cannot be `null`. |
| --- | --- |
