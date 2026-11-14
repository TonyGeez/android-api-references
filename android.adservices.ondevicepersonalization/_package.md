# android.adservices.ondevicepersonalization

Kotlin | [Java](_package.md)
| --- | --- |

## Interfaces

| [IsolatedWorker](IsolatedWorker.md) | Interface with methods that need to be implemented to handle requests from the OnDevicePersonalization service to an `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService`. |
| --- | --- |
| [KeyValueStore](KeyValueStore.md) | An interface to a read-only key-value store. |
| [MutableKeyValueStore](MutableKeyValueStore.md) | An interface to a read-write key-value store. |

## Classes

| [AppInfo](AppInfo.md) | Information about apps. |
| --- | --- |
| [DownloadCompletedInput](DownloadCompletedInput.md) | The input data for `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onDownloadCompleted(android.adservices.ondevicepersonalization.DownloadCompletedInput,%20android.os.OutcomeReceiver)`. |
| [DownloadCompletedOutput](DownloadCompletedOutput.md) | The result returned by `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onDownloadCompleted(android.adservices.ondevicepersonalization.DownloadCompletedInput,%20android.os.OutcomeReceiver)`. |
| [EventInput](EventInput.md) | The input data for `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onEvent(android.adservices.ondevicepersonalization.EventInput,%20android.os.OutcomeReceiver)`. |
| --- | --- |
| [EventLogRecord](EventLogRecord.md) | Data to be logged in the EVENTS table. |
| [EventOutput](EventOutput.md) | The result returned by `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onEvent(android.adservices.ondevicepersonalization.EventInput,%20android.os.OutcomeReceiver)`. |
| [EventUrlProvider](EventUrlProvider.md) | Generates event tracking URLs for a request. |
| --- | --- |
| [ExecuteInIsolatedServiceRequest](ExecuteInIsolatedServiceRequest.md) | The request of `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationManager#executeInIsolatedService(android.adservices.ondevicepersonalization.ExecuteInIsolatedServiceRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |
| [ExecuteInIsolatedServiceResponse](ExecuteInIsolatedServiceResponse.md) | The response of `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationManager#executeInIsolatedService(android.adservices.ondevicepersonalization.ExecuteInIsolatedServiceRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |
| [ExecuteInput](ExecuteInput.md) | The input data for `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,%20android.os.OutcomeReceiver)`. |
| --- | --- |
| [ExecuteOutput](ExecuteOutput.md) | The result returned by `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,%20android.os.OutcomeReceiver)` in response to a call to `OnDevicePersonalizationManager#execute(ComponentName, PersistableBundle, java.util.concurrent.Executor, OutcomeReceiver)` from a client app. |
| [FederatedComputeInput](FederatedComputeInput.md) | The input data for android. |
| [FederatedComputeScheduler](FederatedComputeScheduler.md) | Handles scheduling federated compute jobs. |
| --- | --- |
| [FederatedComputeScheduleRequest](FederatedComputeScheduleRequest.md) | The input for `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduler#schedule(android.adservices.ondevicepersonalization.FederatedComputeScheduleRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |
| [FederatedComputeScheduleResponse](FederatedComputeScheduleResponse.md) | The result returned by `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduler#schedule(android.adservices.ondevicepersonalization.FederatedComputeScheduleRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` when successful. |
| [InferenceInput](InferenceInput.md) | Contains all the information needed for a run of model inference. |
| --- | --- |
| [InferenceOutput](InferenceOutput.md) | The result returned by `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ModelManager#run(android.adservices.ondevicepersonalization.InferenceInput,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |
| [IsolatedService](IsolatedService.md) | Base class for services that are started by ODP on a call to `OnDevicePersonalizationManager#execute(ComponentName, PersistableBundle, java.util.concurrent.Executor, OutcomeReceiver)` and run in an [isolated process](https://developer.android.com/guide/topics/manifest/service-element#isolated). |
| [LogReader](LogReader.md) | An interface to a read logs from REQUESTS and EVENTS Used as a Data Access Object for the REQUESTS and EVENTS table. |
| --- | --- |
| [ModelManager](ModelManager.md) | Handles model inference and only support TFLite model inference now. |
| [OnDevicePersonalizationManager](OnDevicePersonalizationManager.md) | OnDevicePersonalizationManager provides APIs for apps to load an `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService` in an isolated process and interact with it. |
| [RenderingConfig](RenderingConfig.md) | Information returned by `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,%20android.os.OutcomeReceiver)` that is used in a subesequent call to `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onRender(android.adservices.ondevicepersonalization.RenderInput,%20android.os.OutcomeReceiver)` to identify the content to be displayed in a single `https://developer.android.com/reference/kotlin/android/view/View.html#`. |
| --- | --- |
| [RenderInput](RenderInput.md) | The input data for `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onRender(android.adservices.ondevicepersonalization.RenderInput,%20android.os.OutcomeReceiver)`. |
| [RenderOutput](RenderOutput.md) | The result returned by `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onRender(android.adservices.ondevicepersonalization.RenderInput,%20android.os.OutcomeReceiver)`. |
| [RequestLogRecord](RequestLogRecord.md) | Contains data that will be written to the REQUESTS table at the end of a call to `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,%20android.os.OutcomeReceiver)`. |
| --- | --- |
| [RequestToken](RequestToken.md) | An opaque token that identifies the current request to an `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService`. |
| [SurfacePackageToken](SurfacePackageToken.md) | An opaque reference to content that can be displayed in a `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#`. |
| [TrainingExampleRecord](TrainingExampleRecord.md) | One record of `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingExamplesOutput`. |
| --- | --- |
| [TrainingExamplesInput](TrainingExamplesInput.md) | The input data for `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onTrainingExamples(android.adservices.ondevicepersonalization.TrainingExamplesInput,%20android.os.OutcomeReceiver)`. |
| [TrainingExamplesOutput](TrainingExamplesOutput.md) | The output data of `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onTrainingExamples(android.adservices.ondevicepersonalization.TrainingExamplesInput,%20android.os.OutcomeReceiver)` |
| [TrainingInterval](TrainingInterval.md) | Training interval settings required for federated computation jobs. |
| --- | --- |
| [UserData](UserData.md) | User data provided by the platform to an `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService`. |
| [WebTriggerInput](WebTriggerInput.md) | The input data for `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onWebTrigger(android.adservices.ondevicepersonalization.WebTriggerInput,%20android.os.OutcomeReceiver)`. |
| [WebTriggerOutput](WebTriggerOutput.md) | The result that should be returned by `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onWebTrigger(android.adservices.ondevicepersonalization.WebTriggerInput,%20android.os.OutcomeReceiver)`. |
| --- | --- |

## Exceptions

| [IsolatedServiceException](IsolatedServiceException.md) | A class that an `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService` can use to signal a failure in handling a request and return an error to be logged and aggregated. |
| --- | --- |
| [OnDevicePersonalizationException](OnDevicePersonalizationException.md) | Exception thrown by OnDevicePersonalization APIs. |
