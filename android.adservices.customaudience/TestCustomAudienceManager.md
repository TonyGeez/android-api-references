# TestCustomAudienceManager

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# TestCustomAudienceManager

Kotlin| [Java](TestCustomAudienceManager.md) 
| --- | --- |

```
open class TestCustomAudienceManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.customaudience.TestCustomAudienceManager](TestCustomAudienceManager.md) |

TestCustomAudienceManager provides APIs for app and ad-SDKs to test custom audiences.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [overrideCustomAudienceRemoteInfo](TestCustomAudienceManager.md))`(`request:` ` [AddCustomAudienceOverrideRequest](AddCustomAudienceOverrideRequest.md)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `receiver:` ` [OutcomeReceiver](../android.os/OutcomeReceiver.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Exception](../java.lang/Exception.md)!>`)` Overrides the Custom Audience API to avoid fetching data from remote servers and use the data provided in [AddCustomAudienceOverrideRequest](AddCustomAudienceOverrideRequest.md) instead. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeCustomAudienceRemoteInfoOverride](TestCustomAudienceManager.md))`(`request:` ` [RemoveCustomAudienceOverrideRequest](RemoveCustomAudienceOverrideRequest.md)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `receiver:` ` [OutcomeReceiver](../android.os/OutcomeReceiver.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Exception](../java.lang/Exception.md)!>`)` Removes an override in th Custom Audience API with associated the data in [RemoveCustomAudienceOverrideRequest](RemoveCustomAudienceOverrideRequest.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetAllCustomAudienceOverrides](TestCustomAudienceManager.md))`(`executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `receiver:` ` [OutcomeReceiver](../android.os/OutcomeReceiver.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Exception](../java.lang/Exception.md)!>`)` Removes all override data in the Custom Audience API. |
| --- | --- |

## Public methods

### overrideCustomAudienceRemoteInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
open fun overrideCustomAudienceRemoteInfo(
    request: AddCustomAudienceOverrideRequest, 
    executor: Executor, 
    receiver: OutcomeReceiver<Any!, Exception!>
): Unit
```

Overrides the Custom Audience API to avoid fetching data from remote servers and use the data provided in [AddCustomAudienceOverrideRequest](AddCustomAudienceOverrideRequest.md) instead. The [AddCustomAudienceOverrideRequest](AddCustomAudienceOverrideRequest.md) is provided by the Ads SDK.

This method is intended to be used for end-to-end testing. This API is enabled only for apps in debug mode with developer options enabled.

This call will fail silently if the`owner`in the`request`is not the calling app's package name. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_CUSTOM_AUDIENCE](../android.adservices.common/AdServicesPermissions.md)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [AddCustomAudienceOverrideRequest](AddCustomAudienceOverrideRequest.md):This value cannot be`null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java.lang/Exception.md)!\>:This value cannot be`null`. |
| --- | --- |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this API is not enabled for the caller The receiver either returns a`void`for a successful run, or an [Exception](../java.lang/Exception.md) indicates the error. |

### removeCustomAudienceRemoteInfoOverride

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
open fun removeCustomAudienceRemoteInfoOverride(
    request: RemoveCustomAudienceOverrideRequest, 
    executor: Executor, 
    receiver: OutcomeReceiver<Any!, Exception!>
): Unit
```

Removes an override in th Custom Audience API with associated the data in [RemoveCustomAudienceOverrideRequest](RemoveCustomAudienceOverrideRequest.md).

This method is intended to be used for end-to-end testing. This API is enabled only for apps in debug mode with developer options enabled. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_CUSTOM_AUDIENCE](../android.adservices.common/AdServicesPermissions.md)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [RemoveCustomAudienceOverrideRequest](RemoveCustomAudienceOverrideRequest.md):This value cannot be`null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java.lang/Exception.md)!\>:This value cannot be`null`. |
| --- | --- |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this API is not enabled for the caller The [RemoveCustomAudienceOverrideRequest](RemoveCustomAudienceOverrideRequest.md) is provided by the Ads SDK. The receiver either returns a`void`for a successful run, or an [Exception](../java.lang/Exception.md) indicates the error. |

### resetAllCustomAudienceOverrides

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
open fun resetAllCustomAudienceOverrides(
    executor: Executor, 
    receiver: OutcomeReceiver<Any!, Exception!>
): Unit
```

Removes all override data in the Custom Audience API.

This method is intended to be used for end-to-end testing. This API is enabled only for apps in debug mode with developer options enabled. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_CUSTOM_AUDIENCE](../android.adservices.common/AdServicesPermissions.md)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java.util.concurrent/Executor.md):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java.lang/Exception.md)!\>:This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this API is not enabled for the caller The receiver either returns a`void`for a successful run, or an [Exception](../java.lang/Exception.md) indicates the error. |
