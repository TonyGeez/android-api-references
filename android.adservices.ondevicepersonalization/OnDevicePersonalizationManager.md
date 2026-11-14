# OnDevicePersonalizationManager

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDevicePersonalizationManager

Kotlin| [Java](OnDevicePersonalizationManager.md) 
| --- | --- |

```
open class OnDevicePersonalizationManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.OnDevicePersonalizationManager](OnDevicePersonalizationManager.md) |

OnDevicePersonalizationManager provides APIs for apps to load an [IsolatedService](IsolatedService.md) in an isolated process and interact with it. An app can request an [IsolatedService](IsolatedService.md) to generate content for display within an [android.view.SurfaceView](../android.view/SurfaceView.md) within the app's view hierarchy, and also write persistent results to on-device storage which can be consumed by Federated Analytics for cross-device statistical analysis or by Federated Learning for model training. The displayed content and the persistent output are both not directly accessible by the calling app.

## Summary

| Nested classes ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [ExecuteResult](../android/adservices/ondevicepersonalization/OnDevicePersonalizationManager.ExecuteResult.md) The result of a call to [OnDevicePersonalizationManager.execute(ComponentName,](OnDevicePersonalizationManager.md)) |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FEATURE_DISABLED](OnDevicePersonalizationManager.md) Indicates that a feature is present but disabled on the device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FEATURE_ENABLED](OnDevicePersonalizationManager.md) Indicates that a feature is present and enabled on the device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FEATURE_UNSUPPORTED](OnDevicePersonalizationManager.md) Indicates that a feature is not supported on the device. |
| --- | --- |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [execute](OnDevicePersonalizationManager.md))`(`service:` ` [ComponentName](../android.content/ComponentName.md)`, `params:` ` [PersistableBundle](../android.os/PersistableBundle.md)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `receiver:` ` [OutcomeReceiver](../android.os/OutcomeReceiver.md)< [OnDevicePersonalizationManager.ExecuteResult](../android/adservices/ondevicepersonalization/OnDevicePersonalizationManager.ExecuteResult.md)!,` ` [Exception](../java.lang/Exception.md)!>`)` Executes an [IsolatedService](IsolatedService.md) in the OnDevicePersonalization sandbox. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [executeInIsolatedService](OnDevicePersonalizationManager.md))`(`request:` ` [ExecuteInIsolatedServiceRequest](ExecuteInIsolatedServiceRequest.md)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `receiver:` ` [OutcomeReceiver](../android.os/OutcomeReceiver.md)< [ExecuteInIsolatedServiceResponse](ExecuteInIsolatedServiceResponse.md)!,` ` [Exception](../java.lang/Exception.md)!>`)` Executes an [IsolatedService](IsolatedService.md) in the OnDevicePersonalization sandbox. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [queryFeatureAvailability](OnDevicePersonalizationManager.md))`(`featureName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `receiver:` ` [OutcomeReceiver](../android.os/OutcomeReceiver.md)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!,` ` [Exception](../java.lang/Exception.md)!>`)` Get the status of a specific OnDevicePersonalization feature. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestSurfacePackage](OnDevicePersonalizationManager.md))`(`surfacePackageToken:` ` [SurfacePackageToken](SurfacePackageToken.md)`, `surfaceViewHostToken:` ` [IBinder](../android.os/IBinder.md)`, `displayId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `receiver:` ` [OutcomeReceiver](../android.os/OutcomeReceiver.md)< [SurfaceControlViewHost.SurfacePackage](../android/view/SurfaceControlViewHost.SurfacePackage.md)!,` ` [Exception](../java.lang/Exception.md)!>`)` Requests a [android.view.SurfaceControlViewHost.SurfacePackage](../android/view/SurfaceControlViewHost.SurfacePackage.md) to be inserted into a [android.view.SurfaceView](../android.view/SurfaceView.md) inside the calling app. |

## Constants

### FEATURE_DISABLED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_DISABLED: Int
```

Indicates that a feature is present but disabled on the device. 

 Value: 1

### FEATURE_ENABLED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_ENABLED: Int
```

Indicates that a feature is present and enabled on the device. 

 Value: 0

### FEATURE_UNSUPPORTED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_UNSUPPORTED: Int
```

Indicates that a feature is not supported on the device. 

 Value: 2

## Public methods

### execute

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun execute(
    service: ComponentName, 
    params: PersistableBundle, 
    executor: Executor, 
    receiver: OutcomeReceiver<OnDevicePersonalizationManager.ExecuteResult!, Exception!>
): Unit
```

Executes an [IsolatedService](IsolatedService.md) in the OnDevicePersonalization sandbox. The platform binds to the specified [IsolatedService](IsolatedService.md) in an isolated process and calls [android.adservices.ondevicepersonalization.IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,android.os.OutcomeReceiver)](IsolatedWorker.md))with the caller-provided parameters. When the [IsolatedService](IsolatedService.md) finishes execution, the platform returns tokens that refer to the results from the service to the caller. These tokens can be subsequently used to display results in a [android.view.SurfaceView](../android.view/SurfaceView.md) within the calling app.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `service` | [ComponentName](../android.content/ComponentName.md):The [ComponentName](../android.content/ComponentName.md) of the [IsolatedService](IsolatedService.md). This value cannot be`null`. |
| `params` | [PersistableBundle](../android.os/PersistableBundle.md):a [PersistableBundle](../android.os/PersistableBundle.md) that is passed from the calling app to the [IsolatedService](IsolatedService.md). The expected contents of this parameter are defined by the [IsolatedService](IsolatedService.md). The platform does not interpret this parameter. This value cannot be`null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md):the [Executor](../java.util.concurrent/Executor.md) on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| --- | --- |
| `receiver` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [OnDevicePersonalizationManager.ExecuteResult](../android/adservices/ondevicepersonalization/OnDevicePersonalizationManager.ExecuteResult.md)!, [Exception](../java.lang/Exception.md)!\>:This returns a [ExecuteResult](../android/adservices/ondevicepersonalization/OnDevicePersonalizationManager.ExecuteResult.md) object on success or an [Exception](../java.lang/Exception.md) on failure. If the [IsolatedService](IsolatedService.md) returned a [RenderingConfig](RenderingConfig.md) to be displayed, [ExecuteResult.getSurfacePackageToken()](../android/adservices/ondevicepersonalization/OnDevicePersonalizationManager.ExecuteResult.md))will return a non-null [SurfacePackageToken](SurfacePackageToken.md). The [SurfacePackageToken](SurfacePackageToken.md) object can be used in a subsequent [requestSurfacePackage(android.adservices.ondevicepersonalization.SurfacePackageToken,android.os.IBinder,int,int,int,java.util.concurrent.Executor,android.os.OutcomeReceiver)](OnDevicePersonalizationManager.md))call to display the result in a view. The returned [SurfacePackageToken](SurfacePackageToken.md) may be null to indicate that no output is expected to be displayed for this request. If the [IsolatedService](IsolatedService.md) has returned any output data and the calling app is allowlisted to receive data from this service, the [android.adservices.ondevicepersonalization.OnDevicePersonalizationManager.ExecuteResult#getOutputData()](../android/adservices/ondevicepersonalization/OnDevicePersonalizationManager.ExecuteResult.md))will return a non-null byte array. In case of an error, the receiver returns one of the following exceptions: Returns a [android.content.pm.PackageManager.NameNotFoundException](../android/content/pm/PackageManager.NameNotFoundException.md) if the handler package is not installed or does not have a valid ODP manifest. Returns [ClassNotFoundException](../java.lang/ClassNotFoundException.md) if the handler class is not found. Returns an [OnDevicePersonalizationException](OnDevicePersonalizationException.md) if execution of the handler fails. |

### executeInIsolatedService

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun executeInIsolatedService(
    request: ExecuteInIsolatedServiceRequest, 
    executor: Executor, 
    receiver: OutcomeReceiver<ExecuteInIsolatedServiceResponse!, Exception!>
): Unit
```

Executes an [IsolatedService](IsolatedService.md) in the OnDevicePersonalization sandbox. The platform binds to the specified [IsolatedService](IsolatedService.md) in an isolated process and calls [android.adservices.ondevicepersonalization.IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,android.os.OutcomeReceiver)](IsolatedWorker.md))with the caller-provided parameters. When the [IsolatedService](IsolatedService.md) finishes execution, the platform returns tokens that refer to the results from the service to the caller. These tokens can be subsequently used to display results in a [android.view.SurfaceView](../android.view/SurfaceView.md) within the calling app.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [ExecuteInIsolatedServiceRequest](ExecuteInIsolatedServiceRequest.md):the [ExecuteInIsolatedServiceRequest](ExecuteInIsolatedServiceRequest.md) request This value cannot be`null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md):the [Executor](../java.util.concurrent/Executor.md) on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [ExecuteInIsolatedServiceResponse](ExecuteInIsolatedServiceResponse.md)!, [Exception](../java.lang/Exception.md)!\>:This returns a [ExecuteInIsolatedServiceResponse](ExecuteInIsolatedServiceResponse.md) object on success or an [Exception](../java.lang/Exception.md) on failure. For success case, refer to [ExecuteInIsolatedServiceResponse](ExecuteInIsolatedServiceResponse.md). For error case, the receiver returns an [OnDevicePersonalizationException](OnDevicePersonalizationException.md) if execution of the handler fails. This value cannot be`null`. |
| --- | --- |

### queryFeatureAvailability

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun queryFeatureAvailability(
    featureName: String, 
    executor: Executor, 
    receiver: OutcomeReceiver<Int!, Exception!>
): Unit
```

Get the status of a specific OnDevicePersonalization feature.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `featureName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the specific feature to check the availability of. This value cannot be`null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md):the [Executor](../java.util.concurrent/Executor.md) on which to invoke the callback This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [Exception](../java.lang/Exception.md)!\>:this either returns a value of`FeatureStatus`on success or [Exception](../java.lang/Exception.md) on failure. The exception type is [IllegalStateException](../java.lang/IllegalStateException.md) if the service is not available. This value cannot be`null`. |
| --- | --- |

### requestSurfacePackage

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestSurfacePackage(
    surfacePackageToken: SurfacePackageToken, 
    surfaceViewHostToken: IBinder, 
    displayId: Int, 
    width: Int, 
    height: Int, 
    executor: Executor, 
    receiver: OutcomeReceiver<SurfaceControlViewHost.SurfacePackage!, Exception!>
): Unit
```

Requests a [android.view.SurfaceControlViewHost.SurfacePackage](../android/view/SurfaceControlViewHost.SurfacePackage.md) to be inserted into a [android.view.SurfaceView](../android.view/SurfaceView.md) inside the calling app. The surface package will contain an [android.view.View](../android.view/View.md) with the content from a result of a prior call to`execute(ComponentName, PersistableBundle, Executor, OutcomeReceiver)`running in the OnDevicePersonalization sandbox.

| Parameters ||
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `surfacePackageToken` | [SurfacePackageToken](SurfacePackageToken.md):a reference to a [SurfacePackageToken](SurfacePackageToken.md) returned by a prior call to`execute(ComponentName, PersistableBundle, Executor, OutcomeReceiver)`. This value cannot be`null`. |
| `surfaceViewHostToken` | [IBinder](../android.os/IBinder.md):the hostToken of the [android.view.SurfaceView](../android.view/SurfaceView.md), which is returned by [android.view.SurfaceView#getHostToken()](../android.view/SurfaceView.md))after the [android.view.SurfaceView](../android.view/SurfaceView.md) has been added to the view hierarchy. This value cannot be`null`. |
| `displayId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the integer ID of the logical display on which to display the [android.view.SurfaceControlViewHost.SurfacePackage](../android/view/SurfaceControlViewHost.SurfacePackage.md), returned by`Context.getDisplay().getDisplayId()`. |
| --- | --- |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the width of the [android.view.SurfaceControlViewHost.SurfacePackage](../android/view/SurfaceControlViewHost.SurfacePackage.md) in pixels. |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the height of the [android.view.SurfaceControlViewHost.SurfacePackage](../android/view/SurfaceControlViewHost.SurfacePackage.md) in pixels. |
| `executor` | [Executor](../java.util.concurrent/Executor.md):the [Executor](../java.util.concurrent/Executor.md) on which to invoke the callback This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| --- | --- |
| `receiver` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [SurfaceControlViewHost.SurfacePackage](../android/view/SurfaceControlViewHost.SurfacePackage.md)!, [Exception](../java.lang/Exception.md)!\>:This either returns a [android.view.SurfaceControlViewHost.SurfacePackage](../android/view/SurfaceControlViewHost.SurfacePackage.md) on success, or [Exception](../java.lang/Exception.md) on failure. The exception type is [OnDevicePersonalizationException](OnDevicePersonalizationException.md) if execution of the handler fails. This value cannot be`null`. |
