# TestCustomAudienceManager

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# TestCustomAudienceManager

Kotlin| [Java](https://developer.android.com/reference/android/adservices/customaudience/TestCustomAudienceManager "View this page in Java") 

```
open class TestCustomAudienceManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.adservices.customaudience.TestCustomAudienceManager](https://developer.android.com/reference/kotlin/android/adservices/customaudience/TestCustomAudienceManager#) |

TestCustomAudienceManager provides APIs for app and ad-SDKs to test custom audiences.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [overrideCustomAudienceRemoteInfo](https://developer.android.com/reference/kotlin/android/adservices/customaudience/TestCustomAudienceManager#overrideCustomAudienceRemoteInfo(android.adservices.customaudience.AddCustomAudienceOverrideRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`request:` ` [AddCustomAudienceOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/AddCustomAudienceOverrideRequest)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `receiver:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` Overrides the Custom Audience API to avoid fetching data from remote servers and use the data provided in [AddCustomAudienceOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/AddCustomAudienceOverrideRequest) instead. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeCustomAudienceRemoteInfoOverride](https://developer.android.com/reference/kotlin/android/adservices/customaudience/TestCustomAudienceManager#removeCustomAudienceRemoteInfoOverride(android.adservices.customaudience.RemoveCustomAudienceOverrideRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`request:` ` [RemoveCustomAudienceOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/RemoveCustomAudienceOverrideRequest)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `receiver:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` Removes an override in th Custom Audience API with associated the data in [RemoveCustomAudienceOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/RemoveCustomAudienceOverrideRequest). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetAllCustomAudienceOverrides](https://developer.android.com/reference/kotlin/android/adservices/customaudience/TestCustomAudienceManager#resetAllCustomAudienceOverrides(java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `receiver:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` Removes all override data in the Custom Audience API. |

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

Overrides the Custom Audience API to avoid fetching data from remote servers and use the data provided in [AddCustomAudienceOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/AddCustomAudienceOverrideRequest) instead. The [AddCustomAudienceOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/AddCustomAudienceOverrideRequest) is provided by the Ads SDK.

This method is intended to be used for end-to-end testing. This API is enabled only for apps in debug mode with developer options enabled.

This call will fail silently if the`owner`in the`request`is not the calling app's package name. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_CUSTOM_AUDIENCE](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_CUSTOM_AUDIENCE:kotlin.String)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [AddCustomAudienceOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/AddCustomAudienceOverrideRequest):This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>:This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this API is not enabled for the caller The receiver either returns a`void`for a successful run, or an [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) indicates the error. |

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

Removes an override in th Custom Audience API with associated the data in [RemoveCustomAudienceOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/RemoveCustomAudienceOverrideRequest).

This method is intended to be used for end-to-end testing. This API is enabled only for apps in debug mode with developer options enabled. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_CUSTOM_AUDIENCE](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_CUSTOM_AUDIENCE:kotlin.String)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [RemoveCustomAudienceOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/RemoveCustomAudienceOverrideRequest):This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>:This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this API is not enabled for the caller The [RemoveCustomAudienceOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/RemoveCustomAudienceOverrideRequest) is provided by the Ads SDK. The receiver either returns a`void`for a successful run, or an [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) indicates the error. |

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
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_CUSTOM_AUDIENCE](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_CUSTOM_AUDIENCE:kotlin.String)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>:This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this API is not enabled for the caller The receiver either returns a`void`for a successful run, or an [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) indicates the error. |
