# android.adservices.ondevicepersonalization

Kotlin | [Java](_package.md)
| --- | --- |

## Interfaces

| [IsolatedWorker](IsolatedWorker.md) | Interface with methods that need to be implemented to handle requests from the OnDevicePersonalization service to an IsolatedService. |
| --- | --- |
| [KeyValueStore](KeyValueStore.md) | An interface to a read-only key-value store. |
| [MutableKeyValueStore](MutableKeyValueStore.md) | An interface to a read-write key-value store. |

## Classes

| [AppInfo](AppInfo.md) | Information about apps. |
| --- | --- |
| [DownloadCompletedInput](DownloadCompletedInput.md) | The input data for onDownloadCompleted. |
| [DownloadCompletedOutput](DownloadCompletedOutput.md) | The result returned by onDownloadCompleted. |
| [EventInput](EventInput.md) | The input data for onEvent. |
| --- | --- |
| [EventLogRecord](EventLogRecord.md) | Data to be logged in the EVENTS table. |
| [EventOutput](EventOutput.md) | The result returned by onEvent. |
| [EventUrlProvider](EventUrlProvider.md) | Generates event tracking URLs for a request. |
| --- | --- |
| [ExecuteInIsolatedServiceRequest](ExecuteInIsolatedServiceRequest.md) | The request of executeInIsolatedService. |
| [ExecuteInIsolatedServiceResponse](ExecuteInIsolatedServiceResponse.md) | The response of executeInIsolatedService. |
| [ExecuteInput](ExecuteInput.md) | The input data for onExecute. |
| --- | --- |
| [ExecuteOutput](ExecuteOutput.md) | The result returned by onExecute in response to a call to `OnDevicePersonalizationManager#execute(ComponentName, PersistableBundle, java.util.concurrent.Executor, OutcomeReceiver)` from a client app. |
| [FederatedComputeInput](FederatedComputeInput.md) | The input data for android. |
| [FederatedComputeScheduler](FederatedComputeScheduler.md) | Handles scheduling federated compute jobs. |
| --- | --- |
| [FederatedComputeScheduleRequest](FederatedComputeScheduleRequest.md) | The input for schedule. |
| [FederatedComputeScheduleResponse](FederatedComputeScheduleResponse.md) | The result returned by schedule when successful. |
| [InferenceInput](InferenceInput.md) | Contains all the information needed for a run of model inference. |
| --- | --- |
| [InferenceOutput](InferenceOutput.md) | The result returned by run. |
| [IsolatedService](IsolatedService.md) | Base class for services that are started by ODP on a call to `OnDevicePersonalizationManager#execute(ComponentName, PersistableBundle, java.util.concurrent.Executor, OutcomeReceiver)` and run in an [isolated process](https://developer.android.com/guide/topics/manifest/service-element#isolated). |
| [LogReader](LogReader.md) | An interface to a read logs from REQUESTS and EVENTS Used as a Data Access Object for the REQUESTS and EVENTS table. |
| --- | --- |
| [ModelManager](ModelManager.md) | Handles model inference and only support TFLite model inference now. |
| [OnDevicePersonalizationManager](OnDevicePersonalizationManager.md) | OnDevicePersonalizationManager provides APIs for apps to load an IsolatedService in an isolated process and interact with it. |
| [RenderingConfig](RenderingConfig.md) | Information returned by onExecute that is used in a subesequent call to onRender to identify the content to be displayed in a single `https://developer.android.com/reference/kotlin/android/view/View.html#`. |
| --- | --- |
| [RenderInput](RenderInput.md) | The input data for onRender. |
| [RenderOutput](RenderOutput.md) | The result returned by onRender. |
| [RequestLogRecord](RequestLogRecord.md) | Contains data that will be written to the REQUESTS table at the end of a call to onExecute. |
| --- | --- |
| [RequestToken](RequestToken.md) | An opaque token that identifies the current request to an IsolatedService. |
| [SurfacePackageToken](SurfacePackageToken.md) | An opaque reference to content that can be displayed in a `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#`. |
| [TrainingExampleRecord](TrainingExampleRecord.md) | One record of TrainingExamplesOutput. |
| --- | --- |
| [TrainingExamplesInput](TrainingExamplesInput.md) | The input data for onTrainingExamples. |
| [TrainingExamplesOutput](TrainingExamplesOutput.md) | The output data of onTrainingExamples |
| [TrainingInterval](TrainingInterval.md) | Training interval settings required for federated computation jobs. |
| --- | --- |
| [UserData](UserData.md) | User data provided by the platform to an IsolatedService. |
| [WebTriggerInput](WebTriggerInput.md) | The input data for onWebTrigger. |
| [WebTriggerOutput](WebTriggerOutput.md) | The result that should be returned by onWebTrigger. |
| --- | --- |

## Exceptions

| [IsolatedServiceException](IsolatedServiceException.md) | A class that an IsolatedService can use to signal a failure in handling a request and return an error to be logged and aggregated. |
| --- | --- |
| [OnDevicePersonalizationException](OnDevicePersonalizationException.md) | Exception thrown by OnDevicePersonalization APIs. |
