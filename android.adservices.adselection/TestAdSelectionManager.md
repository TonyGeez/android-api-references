# TestAdSelectionManager

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# TestAdSelectionManager

Kotlin| [Java](https://developer.android.com/reference/android/adservices/adselection/TestAdSelectionManager "View this page in Java") 
| --- | --- |

```
open class TestAdSelectionManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.TestAdSelectionManager](https://developer.android.com/reference/kotlin/android/adservices/adselection/TestAdSelectionManager#) |

[TestAdSelectionManager](https://developer.android.com/reference/kotlin/android/adservices/adselection/TestAdSelectionManager#) provides APIs for apps and ad SDKs to test ad selection processes.

These APIs are intended to be used for end-to-end testing. They are enabled only for debuggable apps on phones running a debuggable OS build with developer options enabled.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [overrideAdSelectionConfigRemoteInfo](https://developer.android.com/reference/kotlin/android/adservices/adselection/TestAdSelectionManager#overrideAdSelectionConfigRemoteInfo(android.adservices.adselection.AddAdSelectionOverrideRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`request:` ` [AddAdSelectionOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionOverrideRequest)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `receiver:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` Overrides the AdSelection API for a given [AdSelectionConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig) to avoid fetching data from remote servers and use the data provided in [AddAdSelectionOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionOverrideRequest) instead. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [overrideAdSelectionFromOutcomesConfigRemoteInfo](https://developer.android.com/reference/kotlin/android/adservices/adselection/TestAdSelectionManager#overrideAdSelectionFromOutcomesConfigRemoteInfo(android.adservices.adselection.AddAdSelectionFromOutcomesOverrideRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`request:` ` [AddAdSelectionFromOutcomesOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionFromOutcomesOverrideRequest)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `receiver:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` Overrides the AdSelection API for [AdSelectionFromOutcomesConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig) to avoid fetching data from remote servers and use the data provided in [AddAdSelectionFromOutcomesOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionFromOutcomesOverrideRequest) instead. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAdSelectionConfigRemoteInfoOverride](https://developer.android.com/reference/kotlin/android/adservices/adselection/TestAdSelectionManager#removeAdSelectionConfigRemoteInfoOverride(android.adservices.adselection.RemoveAdSelectionOverrideRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`request:` ` [RemoveAdSelectionOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/RemoveAdSelectionOverrideRequest)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `receiver:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` Removes an override for [AdSelectionConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig) in the Ad Selection API with associated the data in [RemoveAdSelectionOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/RemoveAdSelectionOverrideRequest). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAdSelectionFromOutcomesConfigRemoteInfoOverride](https://developer.android.com/reference/kotlin/android/adservices/adselection/TestAdSelectionManager#removeAdSelectionFromOutcomesConfigRemoteInfoOverride(android.adservices.adselection.RemoveAdSelectionFromOutcomesOverrideRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`request:` ` [RemoveAdSelectionFromOutcomesOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/RemoveAdSelectionFromOutcomesOverrideRequest)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `receiver:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` Removes an override for [AdSelectionFromOutcomesConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig) in th Ad Selection API with associated the data in [RemoveAdSelectionOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/RemoveAdSelectionOverrideRequest). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetAllAdSelectionConfigRemoteOverrides](https://developer.android.com/reference/kotlin/android/adservices/adselection/TestAdSelectionManager#resetAllAdSelectionConfigRemoteOverrides(java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `receiver:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` Removes all override data for [AdSelectionConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig) in the Ad Selection API. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetAllAdSelectionFromOutcomesConfigRemoteOverrides](https://developer.android.com/reference/kotlin/android/adservices/adselection/TestAdSelectionManager#resetAllAdSelectionFromOutcomesConfigRemoteOverrides(java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `receiver:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` Removes all override data for [AdSelectionFromOutcomesConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig) in the Ad Selection API. |
| --- | --- |

## Public methods

### overrideAdSelectionConfigRemoteInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
open fun overrideAdSelectionConfigRemoteInfo(
    request: AddAdSelectionOverrideRequest, 
    executor: Executor, 
    receiver: OutcomeReceiver<Any!, Exception!>
): Unit
```

Overrides the AdSelection API for a given [AdSelectionConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig) to avoid fetching data from remote servers and use the data provided in [AddAdSelectionOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionOverrideRequest) instead. The [AddAdSelectionOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionOverrideRequest) is provided by the Ads SDK.

This method is intended to be used for end-to-end testing. This API is enabled only for apps in debug mode with developer options enabled. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_CUSTOM_AUDIENCE](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_CUSTOM_AUDIENCE:kotlin.String) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_PROTECTED_SIGNALS](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_PROTECTED_SIGNALS:kotlin.String) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_AD_SELECTION](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_AD_SELECTION:kotlin.String)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [AddAdSelectionOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionOverrideRequest):This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>:This value cannot be`null`. |
| --- | --- |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this API is not enabled for the caller The receiver either returns a`void`for a successful run, or an [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) indicates the error. |

### overrideAdSelectionFromOutcomesConfigRemoteInfo

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
open fun overrideAdSelectionFromOutcomesConfigRemoteInfo(
    request: AddAdSelectionFromOutcomesOverrideRequest, 
    executor: Executor, 
    receiver: OutcomeReceiver<Any!, Exception!>
): Unit
```

Overrides the AdSelection API for [AdSelectionFromOutcomesConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig) to avoid fetching data from remote servers and use the data provided in [AddAdSelectionFromOutcomesOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionFromOutcomesOverrideRequest) instead. The [AddAdSelectionFromOutcomesOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionFromOutcomesOverrideRequest) is provided by the Ads SDK.

This method is intended to be used for end-to-end testing. This API is enabled only for apps in debug mode with developer options enabled. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_CUSTOM_AUDIENCE](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_CUSTOM_AUDIENCE:kotlin.String) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_PROTECTED_SIGNALS](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_PROTECTED_SIGNALS:kotlin.String) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_AD_SELECTION](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_AD_SELECTION:kotlin.String)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [AddAdSelectionFromOutcomesOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionFromOutcomesOverrideRequest):This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>:This value cannot be`null`. |
| --- | --- |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this API is not enabled for the caller The receiver either returns a`void`for a successful run, or an [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) indicates the error. |

### removeAdSelectionConfigRemoteInfoOverride

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
open fun removeAdSelectionConfigRemoteInfoOverride(
    request: RemoveAdSelectionOverrideRequest, 
    executor: Executor, 
    receiver: OutcomeReceiver<Any!, Exception!>
): Unit
```

Removes an override for [AdSelectionConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig) in the Ad Selection API with associated the data in [RemoveAdSelectionOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/RemoveAdSelectionOverrideRequest). The [RemoveAdSelectionOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/RemoveAdSelectionOverrideRequest) is provided by the Ads SDK.

This method is intended to be used for end-to-end testing. This API is enabled only for apps in debug mode with developer options enabled. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_CUSTOM_AUDIENCE](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_CUSTOM_AUDIENCE:kotlin.String) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_PROTECTED_SIGNALS](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_PROTECTED_SIGNALS:kotlin.String) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_AD_SELECTION](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_AD_SELECTION:kotlin.String)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [RemoveAdSelectionOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/RemoveAdSelectionOverrideRequest):This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>:This value cannot be`null`. |
| --- | --- |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this API is not enabled for the caller The receiver either returns a`void`for a successful run, or an [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) indicates the error. |

### removeAdSelectionFromOutcomesConfigRemoteInfoOverride

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
open fun removeAdSelectionFromOutcomesConfigRemoteInfoOverride(
    request: RemoveAdSelectionFromOutcomesOverrideRequest, 
    executor: Executor, 
    receiver: OutcomeReceiver<Any!, Exception!>
): Unit
```

Removes an override for [AdSelectionFromOutcomesConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig) in th Ad Selection API with associated the data in [RemoveAdSelectionOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/RemoveAdSelectionOverrideRequest). The [RemoveAdSelectionOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/RemoveAdSelectionOverrideRequest) is provided by the Ads SDK.

This method is intended to be used for end-to-end testing. This API is enabled only for apps in debug mode with developer options enabled. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_CUSTOM_AUDIENCE](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_CUSTOM_AUDIENCE:kotlin.String) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_PROTECTED_SIGNALS](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_PROTECTED_SIGNALS:kotlin.String) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_AD_SELECTION](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_AD_SELECTION:kotlin.String)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [RemoveAdSelectionFromOutcomesOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/RemoveAdSelectionFromOutcomesOverrideRequest):This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>:This value cannot be`null`. |
| --- | --- |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this API is not enabled for the caller The receiver either returns a`void`for a successful run, or an [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) indicates the error. |

### resetAllAdSelectionConfigRemoteOverrides

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
open fun resetAllAdSelectionConfigRemoteOverrides(
    executor: Executor, 
    receiver: OutcomeReceiver<Any!, Exception!>
): Unit
```

Removes all override data for [AdSelectionConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig) in the Ad Selection API.

This method is intended to be used for end-to-end testing. This API is enabled only for apps in debug mode with developer options enabled. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_CUSTOM_AUDIENCE](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_CUSTOM_AUDIENCE:kotlin.String) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_PROTECTED_SIGNALS](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_PROTECTED_SIGNALS:kotlin.String) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_AD_SELECTION](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_AD_SELECTION:kotlin.String)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>:This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this API is not enabled for the caller The receiver either returns a`void`for a successful run, or an [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) indicates the error. |

### resetAllAdSelectionFromOutcomesConfigRemoteOverrides

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
open fun resetAllAdSelectionFromOutcomesConfigRemoteOverrides(
    executor: Executor, 
    receiver: OutcomeReceiver<Any!, Exception!>
): Unit
```

Removes all override data for [AdSelectionFromOutcomesConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig) in the Ad Selection API.

This method is intended to be used for end-to-end testing. This API is enabled only for apps in debug mode with developer options enabled. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_CUSTOM_AUDIENCE](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_CUSTOM_AUDIENCE:kotlin.String) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_PROTECTED_SIGNALS](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_PROTECTED_SIGNALS:kotlin.String) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_AD_SELECTION](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_AD_SELECTION:kotlin.String)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>:This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this API is not enabled for the caller The receiver either returns a`void`for a successful run, or an [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) indicates the error. |
