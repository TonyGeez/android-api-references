Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MeasurementManager

```
open class MeasurementManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.measurement.MeasurementManager](../android/adservices/measurement/MeasurementManager.md) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The Rubidium (Rb) Measurement APIs, including those in android.adservices.measurement, are being deprecated. There are no direct replacement APIs for the Measurement APIs. Developers currently using these APIs should cease integration, as calls to these APIs will be rejected in upcoming Android releases as part of a soft removal process. Please refer to the official Privacy Sandbox developer documentation and announcements for more details on this deprecation and the future roadmap of Privacy Sandbox on Android: https://privacysandbox.com/news/update-on-plans-for-privacy-sandbox-technologies/

MeasurementManager provides APIs to manage source and trigger registrations.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/MeasurementManager#MEASUREMENT_API_STATE_DISABLED:kotlin.Int` This state indicates that Measurement APIs are unavailable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/MeasurementManager#MEASUREMENT_API_STATE_ENABLED:kotlin.Int` This state indicates that Measurement APIs are enabled. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/MeasurementManager#deleteRegistrations(android.adservices.measurement.DeletionRequest,%20java.util.concurrent.Executor,%20android.adservices.common.AdServicesOutcomeReceiver)(deletionRequest: https://developer.android.com/reference/kotlin/android/adservices/measurement/DeletionRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesOutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>)` Deletes previous registrations. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/MeasurementManager#deleteRegistrations(android.adservices.measurement.DeletionRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(deletionRequest: https://developer.android.com/reference/kotlin/android/adservices/measurement/DeletionRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>)` Deletes previous registrations. |
| open static [MeasurementManager](../android/adservices/measurement/MeasurementManager.md) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/MeasurementManager#get(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#)` Factory method for creating an instance of MeasurementManager. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/MeasurementManager#getMeasurementApiStatus(java.util.concurrent.Executor,%20android.adservices.common.AdServicesOutcomeReceiver)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesOutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>)` Gets Measurement API status. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/MeasurementManager#getMeasurementApiStatus(java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>)` Gets Measurement API status. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/MeasurementManager#registerSource(android.adservices.measurement.SourceRegistrationRequest,%20java.util.concurrent.Executor,%20android.adservices.common.AdServicesOutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/adservices/measurement/SourceRegistrationRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#?, callback: https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesOutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>?)` Registers attribution sources(click or view) from an app context. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/MeasurementManager#registerSource(android.adservices.measurement.SourceRegistrationRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/adservices/measurement/SourceRegistrationRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#?, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>?)` Registers attribution sources(click or view) from an app context. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/MeasurementManager#registerSource(android.net.Uri,%20android.view.InputEvent,%20java.util.concurrent.Executor,%20android.adservices.common.AdServicesOutcomeReceiver)(attributionSource: https://developer.android.com/reference/kotlin/android/net/Uri.html#, inputEvent: https://developer.android.com/reference/kotlin/android/view/InputEvent.html#?, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#?, callback: https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesOutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>?)` Registers an attribution source (click or view). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/MeasurementManager#registerSource(android.net.Uri,%20android.view.InputEvent,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(attributionSource: https://developer.android.com/reference/kotlin/android/net/Uri.html#, inputEvent: https://developer.android.com/reference/kotlin/android/view/InputEvent.html#?, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#?, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>?)` Registers an attribution source (click or view). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/MeasurementManager#registerTrigger(android.net.Uri,%20java.util.concurrent.Executor,%20android.adservices.common.AdServicesOutcomeReceiver)(trigger: https://developer.android.com/reference/kotlin/android/net/Uri.html#, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#?, callback: https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesOutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>?)` Registers a trigger (conversion). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/MeasurementManager#registerTrigger(android.net.Uri,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(trigger: https://developer.android.com/reference/kotlin/android/net/Uri.html#, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#?, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>?)` Registers a trigger (conversion). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/MeasurementManager#registerWebSource(android.adservices.measurement.WebSourceRegistrationRequest,%20java.util.concurrent.Executor,%20android.adservices.common.AdServicesOutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/adservices/measurement/WebSourceRegistrationRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#?, callback: https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesOutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>?)` Registers an attribution source(click or view) from web context. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/MeasurementManager#registerWebSource(android.adservices.measurement.WebSourceRegistrationRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/adservices/measurement/WebSourceRegistrationRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#?, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>?)` Registers an attribution source(click or view) from web context. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/MeasurementManager#registerWebTrigger(android.adservices.measurement.WebTriggerRegistrationRequest,%20java.util.concurrent.Executor,%20android.adservices.common.AdServicesOutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/adservices/measurement/WebTriggerRegistrationRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#?, callback: https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesOutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>?)` Registers an attribution trigger(click or view) from web context. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/measurement/MeasurementManager#registerWebTrigger(android.adservices.measurement.WebTriggerRegistrationRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/adservices/measurement/WebTriggerRegistrationRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#?, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>?)` Registers an attribution trigger(click or view) from web context. |
| --- | --- |

## Constants

### MEASUREMENT_API_STATE_DISABLED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEASUREMENT_API_STATE_DISABLED: Int
```

**Deprecated:** *Deprecated in Java.*

This state indicates that Measurement APIs are unavailable. Invoking them will result in an `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

 Value: 0

### MEASUREMENT_API_STATE_ENABLED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEASUREMENT_API_STATE_ENABLED: Int
```

**Deprecated:** *Deprecated in Java.*

This state indicates that Measurement APIs are enabled.

 Value: 1

## Public methods

### deleteRegistrations

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun deleteRegistrations(
    deletionRequest: DeletionRequest, 
    executor: Executor, 
    callback: AdServicesOutcomeReceiver<Any!, Exception!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Deletes previous registrations.

If the deletion is successful, the callback's `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#onResult(android.os.OutcomeReceiver.R)` is invoked with null. In case of failure, a `https://developer.android.com/reference/kotlin/java/lang/Exception.html#` is sent through the callback's `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#onError(android.os.OutcomeReceiver.E)`. Both success and failure feedback are executed on the provided `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`.

For use on Android R or lower.

| Parameters ||
|---|---|
| `deletionRequest` | [DeletionRequest](../android/adservices/measurement/DeletionRequest.md): The request for deleting data. This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md): The executor to run callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [AdServicesOutcomeReceiver](../android/adservices/common/AdServicesOutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>: intended to notify asynchronously the API result. This value cannot be `null`. |
| --- | --- |

### deleteRegistrations

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun deleteRegistrations(
    deletionRequest: DeletionRequest, 
    executor: Executor, 
    callback: OutcomeReceiver<Any!, Exception!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Deletes previous registrations.

If the deletion is successful, the callback's `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#onResult(android.os.OutcomeReceiver.R)` is invoked with null. In case of failure, a `https://developer.android.com/reference/kotlin/java/lang/Exception.html#` is sent through the callback's `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#onError(android.os.OutcomeReceiver.E)`. Both success and failure feedback are executed on the provided `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`.

| Parameters ||
|---|---|
| `deletionRequest` | [DeletionRequest](../android/adservices/measurement/DeletionRequest.md): The request for deleting data. This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md): The executor to run callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>: intended to notify asynchronously the API result. This value cannot be `null`. |
| --- | --- |

### get

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 6](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun get(context: Context): MeasurementManager
```

**Deprecated:** *Deprecated in Java.*

Factory method for creating an instance of MeasurementManager.

| Parameters ||
|---|---|
| `context` | [Context](../android/content/Context.md): The `https://developer.android.com/reference/kotlin/android/content/Context.html#` to use. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/adservices/measurement/MeasurementManager#` | A `https://developer.android.com/reference/kotlin/android/adservices/measurement/MeasurementManager#` instance. This value cannot be `null`. |

### getMeasurementApiStatus

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMeasurementApiStatus(
    executor: Executor, 
    callback: AdServicesOutcomeReceiver<Int!, Exception!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Gets Measurement API status.

The callback's `Integer` value is one of `MeasurementApiState`.

For use on Android R or lower. 
Requires `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_ATTRIBUTION:kotlin.String`

| Parameters ||
|---|---|
| `executor` | [Executor](../java/util/concurrent/Executor.md): used by callback to dispatch results. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [AdServicesOutcomeReceiver](../android/adservices/common/AdServicesOutcomeReceiver.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [Exception](../java/lang/Exception.md)!\>: intended to notify asynchronously the API result. This value cannot be `null`. |

### getMeasurementApiStatus

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMeasurementApiStatus(
    executor: Executor, 
    callback: OutcomeReceiver<Int!, Exception!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Gets Measurement API status.

The callback's `Integer` value is one of `MeasurementApiState`. 
Requires `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_ATTRIBUTION:kotlin.String`

| Parameters ||
|---|---|
| `executor` | [Executor](../java/util/concurrent/Executor.md): used by callback to dispatch results. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [Exception](../java/lang/Exception.md)!\>: intended to notify asynchronously the API result. This value cannot be `null`. |

### registerSource

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerSource(
    request: SourceRegistrationRequest, 
    executor: Executor?, 
    callback: AdServicesOutcomeReceiver<Any!, Exception!>?
): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers attribution sources(click or view) from an app context.

This API will not process any redirects, all registration URLs should be supplied with the request. For use on Android R or lower. 
Requires `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_ATTRIBUTION:kotlin.String`

| Parameters ||
|---|---|
| `request` | [SourceRegistrationRequest](../android/adservices/measurement/SourceRegistrationRequest.md): app source registration request. This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md)?: used by callback to dispatch results. This value may be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [AdServicesOutcomeReceiver](../android/adservices/common/AdServicesOutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>?: intended to notify asynchronously the API result. This value may be `null`. |
| --- | --- |

### registerSource

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerSource(
    request: SourceRegistrationRequest, 
    executor: Executor?, 
    callback: OutcomeReceiver<Any!, Exception!>?
): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers attribution sources(click or view) from an app context.

This API will not process any redirects, all registration URLs should be supplied with the request. 
Requires `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_ATTRIBUTION:kotlin.String`

| Parameters ||
|---|---|
| `request` | [SourceRegistrationRequest](../android/adservices/measurement/SourceRegistrationRequest.md): app source registration request. This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md)?: used by callback to dispatch results. This value may be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>?: intended to notify asynchronously the API result. This value may be `null`. |
| --- | --- |

### registerSource

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerSource(
    attributionSource: Uri, 
    inputEvent: InputEvent?, 
    executor: Executor?, 
    callback: AdServicesOutcomeReceiver<Any!, Exception!>?
): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers an attribution source (click or view). For use on Android R or lower. 
Requires `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_ATTRIBUTION:kotlin.String`

| Parameters ||
|---|---|
| `attributionSource` | [Uri](../android/net/Uri.md): the platform issues a request to this URI in order to fetch metadata associated with the attribution source. The source metadata is stored on device, making it eligible to be matched to future triggers. This value cannot be `null`. |
| `inputEvent` | [InputEvent](../android/view/InputEvent.md)?: either an `https://developer.android.com/reference/kotlin/android/view/InputEvent.html#` object (for a click event) or null (for a view event). |
| `executor` | [Executor](../java/util/concurrent/Executor.md)?: used by callback to dispatch results. This value may be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| --- | --- |
| `callback` | [AdServicesOutcomeReceiver](../android/adservices/common/AdServicesOutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>?: intended to notify asynchronously the API result. This value may be `null`. |

### registerSource

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerSource(
    attributionSource: Uri, 
    inputEvent: InputEvent?, 
    executor: Executor?, 
    callback: OutcomeReceiver<Any!, Exception!>?
): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers an attribution source (click or view). 
Requires `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_ATTRIBUTION:kotlin.String`

| Parameters ||
|---|---|
| `attributionSource` | [Uri](../android/net/Uri.md): the platform issues a request to this URI in order to fetch metadata associated with the attribution source. The source metadata is stored on device, making it eligible to be matched to future triggers. This value cannot be `null`. |
| `inputEvent` | [InputEvent](../android/view/InputEvent.md)?: either an `https://developer.android.com/reference/kotlin/android/view/InputEvent.html#` object (for a click event) or null (for a view event). |
| `executor` | [Executor](../java/util/concurrent/Executor.md)?: used by callback to dispatch results. This value may be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| --- | --- |
| `callback` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>?: intended to notify asynchronously the API result. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the scheme for `attributionSource` is not HTTPS |

### registerTrigger

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerTrigger(
    trigger: Uri, 
    executor: Executor?, 
    callback: AdServicesOutcomeReceiver<Any!, Exception!>?
): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers a trigger (conversion). For use on Android R or lower. 
Requires `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_ATTRIBUTION:kotlin.String`

| Parameters ||
|---|---|
| `trigger` | [Uri](../android/net/Uri.md): the API issues a request to this URI to fetch metadata associated with the trigger. The trigger metadata is stored on-device, and is eligible to be matched with sources during the attribution process. This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md)?: used by callback to dispatch results. This value may be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [AdServicesOutcomeReceiver](../android/adservices/common/AdServicesOutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>?: intended to notify asynchronously the API result. This value may be `null`. |
| --- | --- |

### registerTrigger

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerTrigger(
    trigger: Uri, 
    executor: Executor?, 
    callback: OutcomeReceiver<Any!, Exception!>?
): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers a trigger (conversion). 
Requires `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_ATTRIBUTION:kotlin.String`

| Parameters ||
|---|---|
| `trigger` | [Uri](../android/net/Uri.md): the API issues a request to this URI to fetch metadata associated with the trigger. The trigger metadata is stored on-device, and is eligible to be matched with sources during the attribution process. This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md)?: used by callback to dispatch results. This value may be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>?: intended to notify asynchronously the API result. This value may be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the scheme for `trigger` is not HTTPS |

### registerWebSource

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerWebSource(
    request: WebSourceRegistrationRequest, 
    executor: Executor?, 
    callback: AdServicesOutcomeReceiver<Any!, Exception!>?
): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers an attribution source(click or view) from web context.

This API will not process any redirects, all registration URLs should be supplied with the request. At least one of appDestination or webDestination parameters are required to be provided. If the registration is successful, `callback`'s `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#onResult(android.os.OutcomeReceiver.R)` is invoked with null. In case of failure, a `https://developer.android.com/reference/kotlin/java/lang/Exception.html#` is sent through `callback`'s `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#onError(android.os.OutcomeReceiver.E)`. Both success and failure feedback are executed on the provided `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`.

For use on Android R or lower. 
Requires `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_ATTRIBUTION:kotlin.String`

| Parameters ||
|---|---|
| `request` | [WebSourceRegistrationRequest](../android/adservices/measurement/WebSourceRegistrationRequest.md): source registration request. This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md)?: used by callback to dispatch results. This value may be `null`. |
| `callback` | [AdServicesOutcomeReceiver](../android/adservices/common/AdServicesOutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>?: intended to notify asynchronously the API result. This value may be `null`. |
| --- | --- |

### registerWebSource

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerWebSource(
    request: WebSourceRegistrationRequest, 
    executor: Executor?, 
    callback: OutcomeReceiver<Any!, Exception!>?
): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers an attribution source(click or view) from web context.

This API will not process any redirects, all registration URLs should be supplied with the request. At least one of appDestination or webDestination parameters are required to be provided. If the registration is successful, `callback`'s `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#onResult(android.os.OutcomeReceiver.R)` is invoked with null. In case of failure, a `https://developer.android.com/reference/kotlin/java/lang/Exception.html#` is sent through `callback`'s `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#onError(android.os.OutcomeReceiver.E)`. Both success and failure feedback are executed on the provided `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`. 
Requires `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_ATTRIBUTION:kotlin.String`

| Parameters ||
|---|---|
| `request` | [WebSourceRegistrationRequest](../android/adservices/measurement/WebSourceRegistrationRequest.md): source registration request. This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md)?: used by callback to dispatch results. This value may be `null`. |
| `callback` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>?: intended to notify asynchronously the API result. This value may be `null`. |
| --- | --- |

### registerWebTrigger

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerWebTrigger(
    request: WebTriggerRegistrationRequest, 
    executor: Executor?, 
    callback: AdServicesOutcomeReceiver<Any!, Exception!>?
): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers an attribution trigger(click or view) from web context.

This API will not process any redirects, all registration URLs should be supplied with the request. If the registration is successful, `callback`'s `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#onResult(android.os.OutcomeReceiver.R)` is invoked with null. In case of failure, a `https://developer.android.com/reference/kotlin/java/lang/Exception.html#` is sent through `callback`'s `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#onError(android.os.OutcomeReceiver.E)`. Both success and failure feedback are executed on the provided `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`.

For use on Android R or lower. 
Requires `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_ATTRIBUTION:kotlin.String`

| Parameters ||
|---|---|
| `request` | [WebTriggerRegistrationRequest](../android/adservices/measurement/WebTriggerRegistrationRequest.md): trigger registration request. This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md)?: used by callback to dispatch results. This value may be `null`. |
| `callback` | [AdServicesOutcomeReceiver](../android/adservices/common/AdServicesOutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>?: intended to notify asynchronously the API result. This value may be `null`. |
| --- | --- |

### registerWebTrigger

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerWebTrigger(
    request: WebTriggerRegistrationRequest, 
    executor: Executor?, 
    callback: OutcomeReceiver<Any!, Exception!>?
): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers an attribution trigger(click or view) from web context.

This API will not process any redirects, all registration URLs should be supplied with the request. If the registration is successful, `callback`'s `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#onResult(android.os.OutcomeReceiver.R)` is invoked with null. In case of failure, a `https://developer.android.com/reference/kotlin/java/lang/Exception.html#` is sent through `callback`'s `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#onError(android.os.OutcomeReceiver.E)`. Both success and failure feedback are executed on the provided `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`. 
Requires `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_ATTRIBUTION:kotlin.String`

| Parameters ||
|---|---|
| `request` | [WebTriggerRegistrationRequest](../android/adservices/measurement/WebTriggerRegistrationRequest.md): trigger registration request. This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md)?: used by callback to dispatch results. This value may be `null`. |
| `callback` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>?: intended to notify asynchronously the API result. This value may be `null`. |
| --- | --- |
