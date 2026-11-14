# SettingsPreferenceServiceClient

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SettingsPreferenceServiceClient

Kotlin| [Java](SettingsPreferenceServiceClient.md) 
| --- | --- |

```
open class SettingsPreferenceServiceClient : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.settings.preferences.SettingsPreferenceServiceClient](SettingsPreferenceServiceClient.md) |

Client class responsible for binding to and interacting with an instance of [SettingsPreferenceService](SettingsPreferenceService.md).

This is a convenience class to handle the lifecycle of the service connection.

This client will only interact with one instance at a time, so if the caller requires multiple instances (multiple applications that provide settings), then the caller must create multiple client classes, one for each instance required. To find all available services, a caller may query [android.content.pm.PackageManager](../android.content.pm/PackageManager.md) for applications that provide the intent action [SettingsPreferenceService.ACTION_PREFERENCE_SERVICE](SettingsPreferenceService.md) that are also system applications ([android.content.pm.ApplicationInfo#FLAG_SYSTEM](../android.content.pm/ApplicationInfo.md)).

Note: Each instance of this client will open a binding to an application. This can be resource intensive and affect the health of the system. It is essential that each client instance is only used when needed and the number of calls made are minimal.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SettingsPreferenceServiceClient](SettingsPreferenceServiceClient.md))`(`context:` ` [Context](../android.content/Context.md)`, `packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `callbackExecutor:` ` [Executor](../java.util.concurrent/Executor.md)`, `clientReadyCallback:` ` [OutcomeReceiver](../android.os/OutcomeReceiver.md)< [SettingsPreferenceServiceClient](SettingsPreferenceServiceClient.md)!,` ` [Exception](../java.lang/Exception.md)!>`)` Construct a client for binding to a [SettingsPreferenceService](SettingsPreferenceService.md) provided by the application corresponding to the provided package name. |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](SettingsPreferenceServiceClient.md))`()` This client handles a resource, thus is it important to appropriately close that resource when it is no longer needed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getAllPreferenceMetadata](SettingsPreferenceServiceClient.md))`(`request:` ` [MetadataRequest](MetadataRequest.md)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `receiver:` ` [OutcomeReceiver](../android.os/OutcomeReceiver.md)< [MetadataResult](MetadataResult.md)!,` ` [Exception](../java.lang/Exception.md)!>`)` Retrieve the metadata for all exposed settings preferences within the application. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getPreferenceValue](SettingsPreferenceServiceClient.md))`(`request:` ` [GetValueRequest](GetValueRequest.md)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `receiver:` ` [OutcomeReceiver](../android.os/OutcomeReceiver.md)< [GetValueResult](GetValueResult.md)!,` ` [Exception](../java.lang/Exception.md)!>`)` Retrieve the current value of the requested settings preference. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreferenceValue](SettingsPreferenceServiceClient.md))`(`request:` ` [SetValueRequest](SetValueRequest.md)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `receiver:` ` [OutcomeReceiver](../android.os/OutcomeReceiver.md)< [SetValueResult](SetValueResult.md)!,` ` [Exception](../java.lang/Exception.md)!>`)` Set the value on the target settings preference. |

## Public constructors

### SettingsPreferenceServiceClient

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SettingsPreferenceServiceClient(
    context: Context, 
    packageName: String, 
    callbackExecutor: Executor, 
    clientReadyCallback: OutcomeReceiver<SettingsPreferenceServiceClient!, Exception!>)
```

Construct a client for binding to a [SettingsPreferenceService](SettingsPreferenceService.md) provided by the application corresponding to the provided package name.

| Parameters ||
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md):Application context |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):package name for which this client will initiate a service binding |
| `callbackExecutor` | [Executor](../java.util.concurrent/Executor.md):executor on which to invoke clientReadyCallback Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| --- | --- |
| `clientReadyCallback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [SettingsPreferenceServiceClient](SettingsPreferenceServiceClient.md)!, [Exception](../java.lang/Exception.md)!\>:callback invoked once the client is ready, error otherwise |

## Public methods

### close

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

This client handles a resource, thus is it important to appropriately close that resource when it is no longer needed.

This method is provided by [AutoCloseable](../java.lang/AutoCloseable.md) and calling it will unbind any service binding.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

### getAllPreferenceMetadata

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAllPreferenceMetadata(
    request: MetadataRequest, 
    executor: Executor, 
    receiver: OutcomeReceiver<MetadataResult!, Exception!>
): Unit
```

Retrieve the metadata for all exposed settings preferences within the application.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [MetadataRequest](MetadataRequest.md):object to specify request parameters |
| `executor` | [Executor](../java.util.concurrent/Executor.md): [Executor](../java.util.concurrent/Executor.md) on which to invoke the receiver Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [MetadataResult](MetadataResult.md)!, [Exception](../java.lang/Exception.md)!\>:callback to receive the result or failure |
| --- | --- |

### getPreferenceValue

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPreferenceValue(
    request: GetValueRequest, 
    executor: Executor, 
    receiver: OutcomeReceiver<GetValueResult!, Exception!>
): Unit
```

Retrieve the current value of the requested settings preference.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [GetValueRequest](GetValueRequest.md):object to specify request parameters |
| `executor` | [Executor](../java.util.concurrent/Executor.md): [Executor](../java.util.concurrent/Executor.md) on which to invoke the receiver Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [GetValueResult](GetValueResult.md)!, [Exception](../java.lang/Exception.md)!\>:callback to receive the result or failure |
| --- | --- |

### setPreferenceValue

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPreferenceValue(
    request: SetValueRequest, 
    executor: Executor, 
    receiver: OutcomeReceiver<SetValueResult!, Exception!>
): Unit
```

Set the value on the target settings preference.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [SetValueRequest](SetValueRequest.md):object to specify request parameters |
| `executor` | [Executor](../java.util.concurrent/Executor.md): [Executor](../java.util.concurrent/Executor.md) on which to invoke the receiver Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [SetValueResult](SetValueResult.md)!, [Exception](../java.lang/Exception.md)!\>:callback to receive the result or failure |
| --- | --- |
