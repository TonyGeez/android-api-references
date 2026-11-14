Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FederatedComputeScheduler

Kotlin | [Java](https://developer.android.com/reference/android/adservices/ondevicepersonalization/FederatedComputeScheduler "View this page in Java")
| --- | --- |

```
open class FederatedComputeScheduler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.FederatedComputeScheduler](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduler#) |

Handles scheduling federated compute jobs. See `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService#getFederatedComputeScheduler(android.adservices.ondevicepersonalization.RequestToken)`.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduler.Params` The parameters related to job scheduling. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduler#cancel(android.adservices.ondevicepersonalization.FederatedComputeInput)(input: https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeInput)` Cancels a federated compute job with input training params. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduler#schedule(android.adservices.ondevicepersonalization.FederatedComputeScheduler.Params,%20android.adservices.ondevicepersonalization.FederatedComputeInput)(params: https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduler.Params, input: https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeInput)` Schedules a federated compute job. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduler#schedule(android.adservices.ondevicepersonalization.FederatedComputeScheduleRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(federatedComputeScheduleRequest: https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduleRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, outcomeReceiver: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduleResponse!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>)` Schedules a federated compute job. |
| --- | --- |

## Public methods

### cancel

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cancel(input: FederatedComputeInput): Unit
```

**Deprecated:** *Deprecated in Java.*

Cancels a federated compute job with input training params. In `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService#onRequest(android.adservices.ondevicepersonalization.RequestToken)`, the app can call `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService#getFederatedComputeScheduler(android.adservices.ondevicepersonalization.RequestToken)` to pass scheduler when constructing the `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker`. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `input` | [FederatedComputeInput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeInput): the configuration of the federated compute. It should be consistent with the federated compute server setup. This value cannot be `null`. |

### schedule

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun schedule(
    params: FederatedComputeScheduler.Params, 
    input: FederatedComputeInput
): Unit
```

**Deprecated:** *Deprecated in Java.*

Schedules a federated compute job. In `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService#onRequest(android.adservices.ondevicepersonalization.RequestToken)`, the app can call `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService#getFederatedComputeScheduler(android.adservices.ondevicepersonalization.RequestToken)` to pass the scheduler when constructing the `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker`. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `params` | [FederatedComputeScheduler.Params](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduler.Params): parameters related to job scheduling. This value cannot be `null`. |
| `input` | [FederatedComputeInput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeInput): the configuration of the federated computation. It should be consistent with the federated compute server setup as described in [Federated Compute Server documentation.](https://developers.google.com/privacy-sandbox/protections/on-device-personalization/federated-compute-server). This value cannot be `null`. |

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

Schedules a federated compute job. In `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService#onRequest(android.adservices.ondevicepersonalization.RequestToken)`, the app can call `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService#getFederatedComputeScheduler(android.adservices.ondevicepersonalization.RequestToken)` to pass the scheduler when constructing the `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker`. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `federatedComputeScheduleRequest` | [FederatedComputeScheduleRequest](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduleRequest): input parameters related to job scheduling. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `outcomeReceiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [FederatedComputeScheduleResponse](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduleResponse)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>: This either returns a `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduleResponse` on success, or `https://developer.android.com/reference/kotlin/java/lang/Exception.html#` on failure. The exception type is `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException` with error code `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_INVALID_TRAINING_MANIFEST:kotlin.Int` if the manifest is missing the federated compute server URL or `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_SCHEDULE_TRAINING_FAILED:kotlin.Int` when scheduling fails for other reasons. This value cannot be `null`. |
| --- | --- |
