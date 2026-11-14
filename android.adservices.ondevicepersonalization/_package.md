# android.adservices.ondevicepersonalization

Kotlin | [Java](../android/adservices/ondevicepersonalization/_package.md)
| --- | --- |

## Interfaces

| [IsolatedWorker](../android/adservices/ondevicepersonalization/IsolatedWorker.md) | Interface with methods that need to be implemented to handle requests from the OnDevicePersonalization service to an `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService`. |
| --- | --- |
| [KeyValueStore](../android/adservices/ondevicepersonalization/KeyValueStore.md) | An interface to a read-only key-value store. |
| [MutableKeyValueStore](../android/adservices/ondevicepersonalization/MutableKeyValueStore.md) | An interface to a read-write key-value store. |

## Classes

| [AppInfo](../android/adservices/ondevicepersonalization/AppInfo.md) | Information about apps. |
| --- | --- |
| [DownloadCompletedInput](../android/adservices/ondevicepersonalization/DownloadCompletedInput.md) | The input data for `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onDownloadCompleted(android.adservices.ondevicepersonalization.DownloadCompletedInput,%20android.os.OutcomeReceiver)`. |
| [DownloadCompletedOutput](../android/adservices/ondevicepersonalization/DownloadCompletedOutput.md) | The result returned by `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onDownloadCompleted(android.adservices.ondevicepersonalization.DownloadCompletedInput,%20android.os.OutcomeReceiver)`. |
| [EventInput](../android/adservices/ondevicepersonalization/EventInput.md) | The input data for `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onEvent(android.adservices.ondevicepersonalization.EventInput,%20android.os.OutcomeReceiver)`. |
| --- | --- |
| [EventLogRecord](../android/adservices/ondevicepersonalization/EventLogRecord.md) | Data to be logged in the EVENTS table. |
| [EventOutput](../android/adservices/ondevicepersonalization/EventOutput.md) | The result returned by `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onEvent(android.adservices.ondevicepersonalization.EventInput,%20android.os.OutcomeReceiver)`. |
| [EventUrlProvider](../android/adservices/ondevicepersonalization/EventUrlProvider.md) | Generates event tracking URLs for a request. |
| --- | --- |
| [ExecuteInIsolatedServiceRequest](../android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest.md) | The request of `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationManager#executeInIsolatedService(android.adservices.ondevicepersonalization.ExecuteInIsolatedServiceRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |
| [ExecuteInIsolatedServiceResponse](../android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceResponse.md) | The response of `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationManager#executeInIsolatedService(android.adservices.ondevicepersonalization.ExecuteInIsolatedServiceRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |
| [ExecuteInput](../android/adservices/ondevicepersonalization/ExecuteInput.md) | The input data for `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,%20android.os.OutcomeReceiver)`. |
| --- | --- |
| [ExecuteOutput](../android/adservices/ondevicepersonalization/ExecuteOutput.md) | The result returned by `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,%20android.os.OutcomeReceiver)` in response to a call to `OnDevicePersonalizationManager#execute(ComponentName, PersistableBundle, java.util.concurrent.Executor, OutcomeReceiver)` from a client app. |
| [FederatedComputeInput](../android/adservices/ondevicepersonalization/FederatedComputeInput.md) | The input data for android. |
| [FederatedComputeScheduler](../android/adservices/ondevicepersonalization/FederatedComputeScheduler.md) | Handles scheduling federated compute jobs. |
| --- | --- |
| [FederatedComputeScheduleRequest](../android/adservices/ondevicepersonalization/FederatedComputeScheduleRequest.md) | The input for `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduler#schedule(android.adservices.ondevicepersonalization.FederatedComputeScheduleRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |
| [FederatedComputeScheduleResponse](../android/adservices/ondevicepersonalization/FederatedComputeScheduleResponse.md) | The result returned by `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduler#schedule(android.adservices.ondevicepersonalization.FederatedComputeScheduleRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` when successful. |
| [InferenceInput](../android/adservices/ondevicepersonalization/InferenceInput.md) | Contains all the information needed for a run of model inference. |
| --- | --- |
| [InferenceOutput](../android/adservices/ondevicepersonalization/InferenceOutput.md) | The result returned by `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ModelManager#run(android.adservices.ondevicepersonalization.InferenceInput,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |
| [IsolatedService](../android/adservices/ondevicepersonalization/IsolatedService.md) | Base class for services that are started by ODP on a call to `OnDevicePersonalizationManager#execute(ComponentName, PersistableBundle, java.util.concurrent.Executor, OutcomeReceiver)` and run in an [isolated process](https://developer.android.com/guide/topics/manifest/service-element#isolated). |
| [LogReader](../android/adservices/ondevicepersonalization/LogReader.md) | An interface to a read logs from REQUESTS and EVENTS Used as a Data Access Object for the REQUESTS and EVENTS table. |
| --- | --- |
| [ModelManager](../android/adservices/ondevicepersonalization/ModelManager.md) | Handles model inference and only support TFLite model inference now. |
| [OnDevicePersonalizationManager](../android/adservices/ondevicepersonalization/OnDevicePersonalizationManager.md) | OnDevicePersonalizationManager provides APIs for apps to load an `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService` in an isolated process and interact with it. |
| [RenderingConfig](../android/adservices/ondevicepersonalization/RenderingConfig.md) | Information returned by `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,%20android.os.OutcomeReceiver)` that is used in a subesequent call to `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onRender(android.adservices.ondevicepersonalization.RenderInput,%20android.os.OutcomeReceiver)` to identify the content to be displayed in a single `https://developer.android.com/reference/kotlin/android/view/View.html#`. |
| --- | --- |
| [RenderInput](../android/adservices/ondevicepersonalization/RenderInput.md) | The input data for `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onRender(android.adservices.ondevicepersonalization.RenderInput,%20android.os.OutcomeReceiver)`. |
| [RenderOutput](../android/adservices/ondevicepersonalization/RenderOutput.md) | The result returned by `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onRender(android.adservices.ondevicepersonalization.RenderInput,%20android.os.OutcomeReceiver)`. |
| [RequestLogRecord](../android/adservices/ondevicepersonalization/RequestLogRecord.md) | Contains data that will be written to the REQUESTS table at the end of a call to `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,%20android.os.OutcomeReceiver)`. |
| --- | --- |
| [RequestToken](../android/adservices/ondevicepersonalization/RequestToken.md) | An opaque token that identifies the current request to an `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService`. |
| [SurfacePackageToken](../android/adservices/ondevicepersonalization/SurfacePackageToken.md) | An opaque reference to content that can be displayed in a `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#`. |
| [TrainingExampleRecord](../android/adservices/ondevicepersonalization/TrainingExampleRecord.md) | One record of `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingExamplesOutput`. |
| --- | --- |
| [TrainingExamplesInput](../android/adservices/ondevicepersonalization/TrainingExamplesInput.md) | The input data for `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onTrainingExamples(android.adservices.ondevicepersonalization.TrainingExamplesInput,%20android.os.OutcomeReceiver)`. |
| [TrainingExamplesOutput](../android/adservices/ondevicepersonalization/TrainingExamplesOutput.md) | The output data of `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onTrainingExamples(android.adservices.ondevicepersonalization.TrainingExamplesInput,%20android.os.OutcomeReceiver)` |
| [TrainingInterval](../android/adservices/ondevicepersonalization/TrainingInterval.md) | Training interval settings required for federated computation jobs. |
| --- | --- |
| [UserData](../android/adservices/ondevicepersonalization/UserData.md) | User data provided by the platform to an `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService`. |
| [WebTriggerInput](../android/adservices/ondevicepersonalization/WebTriggerInput.md) | The input data for `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onWebTrigger(android.adservices.ondevicepersonalization.WebTriggerInput,%20android.os.OutcomeReceiver)`. |
| [WebTriggerOutput](../android/adservices/ondevicepersonalization/WebTriggerOutput.md) | The result that should be returned by `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onWebTrigger(android.adservices.ondevicepersonalization.WebTriggerInput,%20android.os.OutcomeReceiver)`. |
| --- | --- |

## Exceptions

| [IsolatedServiceException](../android/adservices/ondevicepersonalization/IsolatedServiceException.md) | A class that an `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService` can use to signal a failure in handling a request and return an error to be logged and aggregated. |
| --- | --- |
| [OnDevicePersonalizationException](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md) | Exception thrown by OnDevicePersonalization APIs. |
