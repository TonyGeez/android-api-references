# SettingsPreferenceServiceClient

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SettingsPreferenceServiceClient

Kotlin| [Java](https://developer.android.com/reference/android/service/settings/preferences/SettingsPreferenceServiceClient "View this page in Java") 

```
open class SettingsPreferenceServiceClient : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.service.settings.preferences.SettingsPreferenceServiceClient](https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceServiceClient#) |

Client class responsible for binding to and interacting with an instance of [SettingsPreferenceService](https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceService).

This is a convenience class to handle the lifecycle of the service connection.

This client will only interact with one instance at a time, so if the caller requires multiple instances (multiple applications that provide settings), then the caller must create multiple client classes, one for each instance required. To find all available services, a caller may query [android.content.pm.PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#) for applications that provide the intent action [SettingsPreferenceService.ACTION_PREFERENCE_SERVICE](https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceService#ACTION_PREFERENCE_SERVICE:kotlin.String) that are also system applications ([android.content.pm.ApplicationInfo#FLAG_SYSTEM](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#FLAG_SYSTEM:kotlin.Int)).

Note: Each instance of this client will open a binding to an application. This can be resource intensive and affect the health of the system. It is essential that each client instance is only used when needed and the number of calls made are minimal.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SettingsPreferenceServiceClient](https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceServiceClient#SettingsPreferenceServiceClient(android.content.Context,%20kotlin.String,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `callbackExecutor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `clientReadyCallback:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [SettingsPreferenceServiceClient](https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceServiceClient#)!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` Construct a client for binding to a [SettingsPreferenceService](https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceService) provided by the application corresponding to the provided package name. |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceServiceClient#close())`()` This client handles a resource, thus is it important to appropriately close that resource when it is no longer needed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getAllPreferenceMetadata](https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceServiceClient#getAllPreferenceMetadata(android.service.settings.preferences.MetadataRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`request:` ` [MetadataRequest](https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataRequest)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `receiver:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [MetadataResult](https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataResult)!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` Retrieve the metadata for all exposed settings preferences within the application. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getPreferenceValue](https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceServiceClient#getPreferenceValue(android.service.settings.preferences.GetValueRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`request:` ` [GetValueRequest](https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueRequest)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `receiver:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [GetValueResult](https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueResult)!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` Retrieve the current value of the requested settings preference. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreferenceValue](https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceServiceClient#setPreferenceValue(android.service.settings.preferences.SetValueRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`request:` ` [SetValueRequest](https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueRequest)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `receiver:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [SetValueResult](https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult)!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` Set the value on the target settings preference. |

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

Construct a client for binding to a [SettingsPreferenceService](https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceService) provided by the application corresponding to the provided package name.

| Parameters ||
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):Application context |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):package name for which this client will initiate a service binding |
| `callbackExecutor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):executor on which to invoke clientReadyCallback Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `clientReadyCallback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [SettingsPreferenceServiceClient](https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceServiceClient#)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>:callback invoked once the client is ready, error otherwise |

## Public methods

### close

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

This client handles a resource, thus is it important to appropriately close that resource when it is no longer needed.

This method is provided by [AutoCloseable](https://developer.android.com/reference/kotlin/java/lang/AutoCloseable.html#) and calling it will unbind any service binding.

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
| `request` | [MetadataRequest](https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataRequest):object to specify request parameters |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) on which to invoke the receiver Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [MetadataResult](https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataResult)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>:callback to receive the result or failure |

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
| `request` | [GetValueRequest](https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueRequest):object to specify request parameters |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) on which to invoke the receiver Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [GetValueResult](https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueResult)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>:callback to receive the result or failure |

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
| `request` | [SetValueRequest](https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueRequest):object to specify request parameters |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) on which to invoke the receiver Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [SetValueResult](https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>:callback to receive the result or failure |
