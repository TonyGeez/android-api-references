Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IsolatedWorker

```
interface IsolatedWorker
```

| [android.adservices.ondevicepersonalization.IsolatedWorker](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#) |

> [!CAUTION]
> **This interface was deprecated in API level 37.**
>
> The ODP APIs are deprecated and will not be supported in future Android releases. There is no direct replacement API available. Developers currently integrated with these APIs must cease further integration efforts. For comprehensive details regarding this deprecation and the future roadmap of Privacy Sandbox on Android, please consult the official Privacy Sandbox developer documentation and announcements: <https://privacysandbox.google.com>

Interface with methods that need to be implemented to handle requests from the OnDevicePersonalization service to an `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService`. The `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService` creates an instance of `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#` on each request and calls one of the methods below, depending the type of the request. The `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService` calls the method on a Binder thread and the `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#` should offload long running operations to a worker thread. The `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#` should use the `receiver` parameter of each method to return results. If any of these methods throws a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#`, the platform treats it as an unrecoverable error in the `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService` and ends processing the request.

## Summary

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onDownloadCompleted(android.adservices.ondevicepersonalization.DownloadCompletedInput,%20android.os.OutcomeReceiver)(input: https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/DownloadCompletedInput, receiver: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/DownloadCompletedOutput!, https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedServiceException!>)` Handles a completed download. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onEvent(android.adservices.ondevicepersonalization.EventInput,%20android.os.OutcomeReceiver)(input: https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventInput, receiver: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventOutput!, https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedServiceException!>)` Handles an event triggered by a request to a platform-provided tracking URL `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventUrlProvider` that was embedded in the HTML output returned by `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onRender(android.adservices.ondevicepersonalization.RenderInput,%20android.os.OutcomeReceiver)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,%20android.os.OutcomeReceiver)(input: https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInput, receiver: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteOutput!, https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedServiceException!>)` Handles a request from an app. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onRender(android.adservices.ondevicepersonalization.RenderInput,%20android.os.OutcomeReceiver)(input: https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderInput, receiver: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderOutput!, https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedServiceException!>)` Generates HTML for the results that were returned as a result of `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,%20android.os.OutcomeReceiver)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onTrainingExamples(android.adservices.ondevicepersonalization.TrainingExamplesInput,%20android.os.OutcomeReceiver)(input: https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingExamplesInput, receiver: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingExamplesOutput!, https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedServiceException!>)` Generate a list of training examples used for federated compute job. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onWebTrigger(android.adservices.ondevicepersonalization.WebTriggerInput,%20android.os.OutcomeReceiver)(input: https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/WebTriggerInput, receiver: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/WebTriggerOutput!, https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedServiceException!>)` Handles a Web Trigger event from a browser. |

## Public methods

### onDownloadCompleted

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDownloadCompleted(
    input: DownloadCompletedInput, 
    receiver: OutcomeReceiver<DownloadCompletedOutput!, IsolatedServiceException!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Handles a completed download. The platform downloads content using the parameters defined in the package manifest of the `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService`, calls this function after the download is complete, and updates the REMOTE_DATA table from `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService#getRemoteData(android.adservices.ondevicepersonalization.RequestToken)` with the result of this method.

| Parameters ||
|---|---|
| `input` | [DownloadCompletedInput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/DownloadCompletedInput): Download handler parameters. This value cannot be `null`. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [DownloadCompletedOutput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/DownloadCompletedOutput)!, [IsolatedServiceException](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedServiceException)!\>: Callback that receives the result `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/DownloadCompletedOutput` or an `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedServiceException`. If this method returns a `null` result or exception via the callback, or throws a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#`, no updates are made to the REMOTE_DATA table. |

### onEvent

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onEvent(
    input: EventInput, 
    receiver: OutcomeReceiver<EventOutput!, IsolatedServiceException!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Handles an event triggered by a request to a platform-provided tracking URL `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventUrlProvider` that was embedded in the HTML output returned by `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onRender(android.adservices.ondevicepersonalization.RenderInput,%20android.os.OutcomeReceiver)`. The platform updates the EVENTS table with `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventOutput#getEventLogRecord()`.

| Parameters ||
|---|---|
| `input` | [EventInput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventInput): The parameters needed to compute event data. This value cannot be `null`. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [EventOutput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventOutput)!, [IsolatedServiceException](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedServiceException)!\>: Callback that receives the result `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventOutput` or an `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedServiceException`. If this method returns a `null` result or exception via the callback, or throws a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#`, no data is written to the EVENTS table. |

### onExecute

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onExecute(
    input: ExecuteInput, 
    receiver: OutcomeReceiver<ExecuteOutput!, IsolatedServiceException!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Handles a request from an app. This method is called when an app calls `OnDevicePersonalizationManager#execute(ComponentName, PersistableBundle, java.util.concurrent.Executor, OutcomeReceiver)` that refers to a named `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService`.

| Parameters ||
|---|---|
| `input` | [ExecuteInput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInput): Request Parameters from the calling app. This value cannot be `null`. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [ExecuteOutput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteOutput)!, [IsolatedServiceException](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedServiceException)!\>: Callback that receives the result `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteOutput` or an `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedServiceException`. If this method throws a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` or returns either `null` or `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedServiceException`, the error is indicated to the calling app as an `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException` with error code `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_FAILED:kotlin.Int`. To avoid leaking private data to the calling app, more detailed errors are not reported to the caller. If the `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService` needs to report additional data beyond the error code to its backend servers, it should populate the logging fields in `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteOutput` with the additional error data for logging, and rely on Federated Analytics for the stats. |

### onRender

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onRender(
    input: RenderInput, 
    receiver: OutcomeReceiver<RenderOutput!, IsolatedServiceException!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Generates HTML for the results that were returned as a result of `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,%20android.os.OutcomeReceiver)`. Called when a client app calls android.adservices.ondevicepersonalization.OnDevicePersonalizationManager#requestSurfacePackage(android.adservices.ondevicepersonalization.SurfacePackageToken,IBinder,int,int,int,java.util.concurrent.Executor,android.os.OutcomeReceiver). The platform will render this HTML in an `https://developer.android.com/reference/kotlin/android/webkit/WebView.html#` inside a fenced frame.

| Parameters ||
|---|---|
| `input` | [RenderInput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderInput): Parameters for the render request. This value cannot be `null`. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [RenderOutput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderOutput)!, [IsolatedServiceException](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedServiceException)!\>: Callback that receives the result `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderOutput` or an `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedServiceException`. If this method returns a `null` result or exception via the callback, or throws a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#`, the error is also reported to calling apps as an `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException` with error code `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_FAILED:kotlin.Int`. |

### onTrainingExamples

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onTrainingExamples(
    input: TrainingExamplesInput, 
    receiver: OutcomeReceiver<TrainingExamplesOutput!, IsolatedServiceException!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Generate a list of training examples used for federated compute job. The platform will call this function when a federated compute job starts. The federated compute job is scheduled by an app through android.adservices.ondevicepersonalization.FederatedComputeScheduler#schedule.

| Parameters ||
|---|---|
| `input` | [TrainingExamplesInput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingExamplesInput): The parameters needed to generate the training example. This value cannot be `null`. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [TrainingExamplesOutput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingExamplesOutput)!, [IsolatedServiceException](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedServiceException)!\>: Callback that receives the result `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingExamplesOutput` or an `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedServiceException`. If this method returns a `null` result or exception via the callback, or throws a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#`, no training examples is produced for this training session. |

### onWebTrigger

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onWebTrigger(
    input: WebTriggerInput, 
    receiver: OutcomeReceiver<WebTriggerOutput!, IsolatedServiceException!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Handles a Web Trigger event from a browser. A Web Trigger event occurs when a browser registers a web trigger event with the OS using the [Attribution and Reporting API](https://github.com/WICG/attribution-reporting-api). If the data in the web trigger payload indicates that the event should be forwarded to an `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService`, the platform will call this function with the web trigger data.

| Parameters ||
|---|---|
| `input` | [WebTriggerInput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/WebTriggerInput): The parameters needed to process Web Trigger event. This value cannot be `null`. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [WebTriggerOutput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/WebTriggerOutput)!, [IsolatedServiceException](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedServiceException)!\>: Callback that receives the result `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/WebTriggerOutput` or an `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedServiceException`. Should be called with a `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/WebTriggerOutput` object populated with a set of records to be written to the REQUESTS or EVENTS tables. If this method returns a `null` result or exception via the callback, or throws a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#`, no data is written to the REQUESTS orEVENTS tables. |
