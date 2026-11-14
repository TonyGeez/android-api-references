# ProtectedSignalsManager

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions)

# ProtectedSignalsManager

Kotlin | [Java](https://developer.android.com/reference/android/adservices/signals/ProtectedSignalsManager "View this page in Java") 
| --- | --- |

```
open class ProtectedSignalsManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.signals.ProtectedSignalsManager](https://developer.android.com/reference/kotlin/android/adservices/signals/ProtectedSignalsManager#) |

ProtectedSignalsManager provides APIs for apps and ad-SDKs to manage their protected signals.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open static [ProtectedSignalsManager](https://developer.android.com/reference/kotlin/android/adservices/signals/ProtectedSignalsManager#) | [get](https://developer.android.com/reference/kotlin/android/adservices/signals/ProtectedSignalsManager#get(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`)` Factory method for creating an instance of ProtectedSignalsManager. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateSignals](https://developer.android.com/reference/kotlin/android/adservices/signals/ProtectedSignalsManager#updateSignals(android.adservices.signals.UpdateSignalsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`updateSignalsRequest:` ` [UpdateSignalsRequest](https://developer.android.com/reference/kotlin/android/adservices/signals/UpdateSignalsRequest)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `receiver:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` The updateSignals API will retrieve a JSON from the URI that describes which signals to add or remove. |

## Public methods

### get

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions) 

```
open static fun get(context: Context): ProtectedSignalsManager
```

Factory method for creating an instance of ProtectedSignalsManager.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): The [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) to use This value cannot be `null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ProtectedSignalsManager](https://developer.android.com/reference/kotlin/android/adservices/signals/ProtectedSignalsManager#) | A [ProtectedSignalsManager](https://developer.android.com/reference/kotlin/android/adservices/signals/ProtectedSignalsManager#) instance This value cannot be `null`. |

### updateSignals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions) 

```
open fun updateSignals(
    updateSignalsRequest: UpdateSignalsRequest, 
    executor: Executor, 
    receiver: OutcomeReceiver<Any!, Exception!>
): Unit
```

The updateSignals API will retrieve a JSON from the URI that describes which signals to add or remove. This API also allows registering the encoder endpoint. The endpoint is used to download an encoding logic, which enables encoding the signals.

The top level keys for the JSON must correspond to one of 5 commands:

"put" - Adds a new signal, overwriting any existing signals with the same key. The value for this is a JSON object where the keys are base 64 strings corresponding to the key to put for and the values are base 64 string corresponding to the value to put.

"append" - Appends a new signal/signals to a time series of signals, removing the oldest signals to make room for the new ones if the size of the series exceeds the given maximum. The value for this is a JSON object where the keys are base 64 strings corresponding to the key to append to and the values are objects with two fields: "values" and "maxSignals" . "values" is a list of base 64 strings corresponding to signal values to append to the time series. "maxSignals" is the maximum number of values that are allowed in this timeseries. If the current number of signals associated with the key exceeds maxSignals the oldest signals will be removed. Note that you can append to a key added by put. Not that appending more than the maximum number of values will cause a failure.

"put_if_not_present" - Adds a new signal only if there are no existing signals with the same key. The value for this is a JSON object where the keys are base 64 strings corresponding to the key to put for and the values are base 64 string corresponding to the value to put.

"remove" - Removes the signal for a key. The value of this is a list of base 64 strings corresponding to the keys of signals that should be deleted.

"update_encoder" - Provides an action to update the endpoint, and a URI which can be used to retrieve an encoding logic. The sub-key for providing an update action is "action" and the values currently supported are:

1. "REGISTER" : Registers the encoder endpoint if provided for the first time or overwrites the existing one with the newly provided endpoint. Providing the "endpoint" is required for the "REGISTER" action.

The sub-key for providing an encoder endpoint is "endpoint" and the value is the URI string for the endpoint.

On success, the onResult method of the provided OutcomeReceiver will be called with an empty Object. This Object has no significance and is used merely as a placeholder.

Key may only be operated on by one command per JSON. If two command attempt to operate on the same key, this method will through an [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#)

This call fails with an [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) if

1. the `ownerPackageName` is not calling app's package name and/or
2. the buyer is not authorized to use the API.

This call fails with an [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) if

1. The JSON retrieved from the server is not valid.
2. The provided URI is invalid.

This call fails with [LimitExceededException](https://developer.android.com/reference/kotlin/android/os/LimitExceededException.html#) if the calling package exceeds the allowed rate limits and is throttled.

This call fails with an [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) if an internal service error is encountered. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_PROTECTED_SIGNALS](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_PROTECTED_SIGNALS:kotlin.String)

| Parameters ||
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `updateSignalsRequest` | [UpdateSignalsRequest](https://developer.android.com/reference/kotlin/android/adservices/signals/UpdateSignalsRequest): This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): This value cannot be `null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>: This value cannot be `null`. |
| --- | --- |
