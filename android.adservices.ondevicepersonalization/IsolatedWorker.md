Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IsolatedWorker

```
interface IsolatedWorker
```

| [android.adservices.ondevicepersonalization.IsolatedWorker](IsolatedWorker.md) |

> [!CAUTION]
> **This interface was deprecated in API level 37.**
>
> The ODP APIs are deprecated and will not be supported in future Android releases. There is no direct replacement API available. Developers currently integrated with these APIs must cease further integration efforts. For comprehensive details regarding this deprecation and the future roadmap of Privacy Sandbox on Android, please consult the official Privacy Sandbox developer documentation and announcements: <https://privacysandbox.google.com>

Interface with methods that need to be implemented to handle requests from the OnDevicePersonalization service to an IsolatedService. The IsolatedService creates an instance of IsolatedWorker on each request and calls one of the methods below, depending the type of the request. The IsolatedService calls the method on a Binder thread and the IsolatedWorker should offload long running operations to a worker thread. The IsolatedWorker should use the `receiver` parameter of each method to return results. If any of these methods throws a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#`, the platform treats it as an unrecoverable error in the IsolatedService and ends processing the request.

## Summary

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onDownloadCompleted Handles a completed download. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onEvent Handles an event triggered by a request to a platform-provided tracking URL EventUrlProvider that was embedded in the HTML output returned by onRender. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onExecute Handles a request from an app. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onRender Generates HTML for the results that were returned as a result of onExecute. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onTrainingExamples Generate a list of training examples used for federated compute job. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onWebTrigger Handles a Web Trigger event from a browser. |
| --- | --- |

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

Handles a completed download. The platform downloads content using the parameters defined in the package manifest of the IsolatedService, calls this function after the download is complete, and updates the REMOTE_DATA table from getRemoteData with the result of this method.

| Parameters ||
|---|---|
| `input` | [DownloadCompletedInput](DownloadCompletedInput.md): Download handler parameters. This value cannot be `null`. |
| `receiver` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [DownloadCompletedOutput](DownloadCompletedOutput.md)!, [IsolatedServiceException](IsolatedServiceException.md)!\>: Callback that receives the result DownloadCompletedOutput or an IsolatedServiceException. If this method returns a `null` result or exception via the callback, or throws a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#`, no updates are made to the REMOTE_DATA table. |

### onEvent

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onEvent(
    input: EventInput, 
    receiver: OutcomeReceiver<EventOutput!, IsolatedServiceException!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Handles an event triggered by a request to a platform-provided tracking URL EventUrlProvider that was embedded in the HTML output returned by onRender. The platform updates the EVENTS table with getEventLogRecord.

| Parameters ||
|---|---|
| `input` | [EventInput](EventInput.md): The parameters needed to compute event data. This value cannot be `null`. |
| `receiver` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [EventOutput](EventOutput.md)!, [IsolatedServiceException](IsolatedServiceException.md)!\>: Callback that receives the result EventOutput or an IsolatedServiceException. If this method returns a `null` result or exception via the callback, or throws a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#`, no data is written to the EVENTS table. |

### onExecute

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onExecute(
    input: ExecuteInput, 
    receiver: OutcomeReceiver<ExecuteOutput!, IsolatedServiceException!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Handles a request from an app. This method is called when an app calls `OnDevicePersonalizationManager#execute(ComponentName, PersistableBundle, java.util.concurrent.Executor, OutcomeReceiver)` that refers to a named IsolatedService.

| Parameters ||
|---|---|
| `input` | [ExecuteInput](ExecuteInput.md): Request Parameters from the calling app. This value cannot be `null`. |
| `receiver` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [ExecuteOutput](ExecuteOutput.md)!, [IsolatedServiceException](IsolatedServiceException.md)!\>: Callback that receives the result ExecuteOutput or an IsolatedServiceException. If this method throws a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` or returns either `null` or IsolatedServiceException, the error is indicated to the calling app as an OnDevicePersonalizationException with error code `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_FAILED:kotlin.Int`. To avoid leaking private data to the calling app, more detailed errors are not reported to the caller. If the IsolatedService needs to report additional data beyond the error code to its backend servers, it should populate the logging fields in ExecuteOutput with the additional error data for logging, and rely on Federated Analytics for the stats. |

### onRender

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onRender(
    input: RenderInput, 
    receiver: OutcomeReceiver<RenderOutput!, IsolatedServiceException!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Generates HTML for the results that were returned as a result of onExecute. Called when a client app calls android.adservices.ondevicepersonalization.OnDevicePersonalizationManager#requestSurfacePackage(android.adservices.ondevicepersonalization.SurfacePackageToken,IBinder,int,int,int,java.util.concurrent.Executor,android.os.OutcomeReceiver). The platform will render this HTML in an `https://developer.android.com/reference/kotlin/android/webkit/WebView.html#` inside a fenced frame.

| Parameters ||
|---|---|
| `input` | [RenderInput](RenderInput.md): Parameters for the render request. This value cannot be `null`. |
| `receiver` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [RenderOutput](RenderOutput.md)!, [IsolatedServiceException](IsolatedServiceException.md)!\>: Callback that receives the result RenderOutput or an IsolatedServiceException. If this method returns a `null` result or exception via the callback, or throws a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#`, the error is also reported to calling apps as an OnDevicePersonalizationException with error code `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_FAILED:kotlin.Int`. |

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
| `input` | [TrainingExamplesInput](TrainingExamplesInput.md): The parameters needed to generate the training example. This value cannot be `null`. |
| `receiver` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [TrainingExamplesOutput](TrainingExamplesOutput.md)!, [IsolatedServiceException](IsolatedServiceException.md)!\>: Callback that receives the result TrainingExamplesOutput or an IsolatedServiceException. If this method returns a `null` result or exception via the callback, or throws a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#`, no training examples is produced for this training session. |

### onWebTrigger

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onWebTrigger(
    input: WebTriggerInput, 
    receiver: OutcomeReceiver<WebTriggerOutput!, IsolatedServiceException!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Handles a Web Trigger event from a browser. A Web Trigger event occurs when a browser registers a web trigger event with the OS using the [Attribution and Reporting API](https://github.com/WICG/attribution-reporting-api). If the data in the web trigger payload indicates that the event should be forwarded to an IsolatedService, the platform will call this function with the web trigger data.

| Parameters ||
|---|---|
| `input` | [WebTriggerInput](WebTriggerInput.md): The parameters needed to process Web Trigger event. This value cannot be `null`. |
| `receiver` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [WebTriggerOutput](WebTriggerOutput.md)!, [IsolatedServiceException](IsolatedServiceException.md)!\>: Callback that receives the result WebTriggerOutput or an IsolatedServiceException. Should be called with a WebTriggerOutput object populated with a set of records to be written to the REQUESTS or EVENTS tables. If this method returns a `null` result or exception via the callback, or throws a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#`, no data is written to the REQUESTS orEVENTS tables. |
