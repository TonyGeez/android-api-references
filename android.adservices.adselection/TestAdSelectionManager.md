# TestAdSelectionManager

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# TestAdSelectionManager

Kotlin| [Java](../android/adservices/adselection/TestAdSelectionManager.md) 
| --- | --- |

```
open class TestAdSelectionManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.TestAdSelectionManager](../android/adservices/adselection/TestAdSelectionManager.md) |

[TestAdSelectionManager](../android/adservices/adselection/TestAdSelectionManager.md) provides APIs for apps and ad SDKs to test ad selection processes.

These APIs are intended to be used for end-to-end testing. They are enabled only for debuggable apps on phones running a debuggable OS build with developer options enabled.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [overrideAdSelectionConfigRemoteInfo](../android/adservices/adselection/TestAdSelectionManager.md))`(`request:` ` [AddAdSelectionOverrideRequest](../android/adservices/adselection/AddAdSelectionOverrideRequest.md)`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `receiver:` ` [OutcomeReceiver](../android/os/OutcomeReceiver.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Exception](../java/lang/Exception.md)!>`)` Overrides the AdSelection API for a given [AdSelectionConfig](../android/adservices/adselection/AdSelectionConfig.md) to avoid fetching data from remote servers and use the data provided in [AddAdSelectionOverrideRequest](../android/adservices/adselection/AddAdSelectionOverrideRequest.md) instead. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [overrideAdSelectionFromOutcomesConfigRemoteInfo](../android/adservices/adselection/TestAdSelectionManager.md))`(`request:` ` [AddAdSelectionFromOutcomesOverrideRequest](../android/adservices/adselection/AddAdSelectionFromOutcomesOverrideRequest.md)`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `receiver:` ` [OutcomeReceiver](../android/os/OutcomeReceiver.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Exception](../java/lang/Exception.md)!>`)` Overrides the AdSelection API for [AdSelectionFromOutcomesConfig](../android/adservices/adselection/AdSelectionFromOutcomesConfig.md) to avoid fetching data from remote servers and use the data provided in [AddAdSelectionFromOutcomesOverrideRequest](../android/adservices/adselection/AddAdSelectionFromOutcomesOverrideRequest.md) instead. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAdSelectionConfigRemoteInfoOverride](../android/adservices/adselection/TestAdSelectionManager.md))`(`request:` ` [RemoveAdSelectionOverrideRequest](../android/adservices/adselection/RemoveAdSelectionOverrideRequest.md)`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `receiver:` ` [OutcomeReceiver](../android/os/OutcomeReceiver.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Exception](../java/lang/Exception.md)!>`)` Removes an override for [AdSelectionConfig](../android/adservices/adselection/AdSelectionConfig.md) in the Ad Selection API with associated the data in [RemoveAdSelectionOverrideRequest](../android/adservices/adselection/RemoveAdSelectionOverrideRequest.md). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAdSelectionFromOutcomesConfigRemoteInfoOverride](../android/adservices/adselection/TestAdSelectionManager.md))`(`request:` ` [RemoveAdSelectionFromOutcomesOverrideRequest](../android/adservices/adselection/RemoveAdSelectionFromOutcomesOverrideRequest.md)`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `receiver:` ` [OutcomeReceiver](../android/os/OutcomeReceiver.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Exception](../java/lang/Exception.md)!>`)` Removes an override for [AdSelectionFromOutcomesConfig](../android/adservices/adselection/AdSelectionFromOutcomesConfig.md) in th Ad Selection API with associated the data in [RemoveAdSelectionOverrideRequest](../android/adservices/adselection/RemoveAdSelectionOverrideRequest.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetAllAdSelectionConfigRemoteOverrides](../android/adservices/adselection/TestAdSelectionManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `receiver:` ` [OutcomeReceiver](../android/os/OutcomeReceiver.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Exception](../java/lang/Exception.md)!>`)` Removes all override data for [AdSelectionConfig](../android/adservices/adselection/AdSelectionConfig.md) in the Ad Selection API. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetAllAdSelectionFromOutcomesConfigRemoteOverrides](../android/adservices/adselection/TestAdSelectionManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `receiver:` ` [OutcomeReceiver](../android/os/OutcomeReceiver.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Exception](../java/lang/Exception.md)!>`)` Removes all override data for [AdSelectionFromOutcomesConfig](../android/adservices/adselection/AdSelectionFromOutcomesConfig.md) in the Ad Selection API. |
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

Overrides the AdSelection API for a given [AdSelectionConfig](../android/adservices/adselection/AdSelectionConfig.md) to avoid fetching data from remote servers and use the data provided in [AddAdSelectionOverrideRequest](../android/adservices/adselection/AddAdSelectionOverrideRequest.md) instead. The [AddAdSelectionOverrideRequest](../android/adservices/adselection/AddAdSelectionOverrideRequest.md) is provided by the Ads SDK.

This method is intended to be used for end-to-end testing. This API is enabled only for apps in debug mode with developer options enabled. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_CUSTOM_AUDIENCE](../android/adservices/common/AdServicesPermissions.md) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_PROTECTED_SIGNALS](../android/adservices/common/AdServicesPermissions.md) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_AD_SELECTION](../android/adservices/common/AdServicesPermissions.md)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [AddAdSelectionOverrideRequest](../android/adservices/adselection/AddAdSelectionOverrideRequest.md):This value cannot be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>:This value cannot be`null`. |
| --- | --- |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this API is not enabled for the caller The receiver either returns a`void`for a successful run, or an [Exception](../java/lang/Exception.md) indicates the error. |

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

Overrides the AdSelection API for [AdSelectionFromOutcomesConfig](../android/adservices/adselection/AdSelectionFromOutcomesConfig.md) to avoid fetching data from remote servers and use the data provided in [AddAdSelectionFromOutcomesOverrideRequest](../android/adservices/adselection/AddAdSelectionFromOutcomesOverrideRequest.md) instead. The [AddAdSelectionFromOutcomesOverrideRequest](../android/adservices/adselection/AddAdSelectionFromOutcomesOverrideRequest.md) is provided by the Ads SDK.

This method is intended to be used for end-to-end testing. This API is enabled only for apps in debug mode with developer options enabled. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_CUSTOM_AUDIENCE](../android/adservices/common/AdServicesPermissions.md) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_PROTECTED_SIGNALS](../android/adservices/common/AdServicesPermissions.md) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_AD_SELECTION](../android/adservices/common/AdServicesPermissions.md)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [AddAdSelectionFromOutcomesOverrideRequest](../android/adservices/adselection/AddAdSelectionFromOutcomesOverrideRequest.md):This value cannot be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>:This value cannot be`null`. |
| --- | --- |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this API is not enabled for the caller The receiver either returns a`void`for a successful run, or an [Exception](../java/lang/Exception.md) indicates the error. |

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

Removes an override for [AdSelectionConfig](../android/adservices/adselection/AdSelectionConfig.md) in the Ad Selection API with associated the data in [RemoveAdSelectionOverrideRequest](../android/adservices/adselection/RemoveAdSelectionOverrideRequest.md). The [RemoveAdSelectionOverrideRequest](../android/adservices/adselection/RemoveAdSelectionOverrideRequest.md) is provided by the Ads SDK.

This method is intended to be used for end-to-end testing. This API is enabled only for apps in debug mode with developer options enabled. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_CUSTOM_AUDIENCE](../android/adservices/common/AdServicesPermissions.md) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_PROTECTED_SIGNALS](../android/adservices/common/AdServicesPermissions.md) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_AD_SELECTION](../android/adservices/common/AdServicesPermissions.md)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [RemoveAdSelectionOverrideRequest](../android/adservices/adselection/RemoveAdSelectionOverrideRequest.md):This value cannot be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>:This value cannot be`null`. |
| --- | --- |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this API is not enabled for the caller The receiver either returns a`void`for a successful run, or an [Exception](../java/lang/Exception.md) indicates the error. |

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

Removes an override for [AdSelectionFromOutcomesConfig](../android/adservices/adselection/AdSelectionFromOutcomesConfig.md) in th Ad Selection API with associated the data in [RemoveAdSelectionOverrideRequest](../android/adservices/adselection/RemoveAdSelectionOverrideRequest.md). The [RemoveAdSelectionOverrideRequest](../android/adservices/adselection/RemoveAdSelectionOverrideRequest.md) is provided by the Ads SDK.

This method is intended to be used for end-to-end testing. This API is enabled only for apps in debug mode with developer options enabled. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_CUSTOM_AUDIENCE](../android/adservices/common/AdServicesPermissions.md) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_PROTECTED_SIGNALS](../android/adservices/common/AdServicesPermissions.md) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_AD_SELECTION](../android/adservices/common/AdServicesPermissions.md)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [RemoveAdSelectionFromOutcomesOverrideRequest](../android/adservices/adselection/RemoveAdSelectionFromOutcomesOverrideRequest.md):This value cannot be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>:This value cannot be`null`. |
| --- | --- |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this API is not enabled for the caller The receiver either returns a`void`for a successful run, or an [Exception](../java/lang/Exception.md) indicates the error. |

### resetAllAdSelectionConfigRemoteOverrides

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
open fun resetAllAdSelectionConfigRemoteOverrides(
    executor: Executor, 
    receiver: OutcomeReceiver<Any!, Exception!>
): Unit
```

Removes all override data for [AdSelectionConfig](../android/adservices/adselection/AdSelectionConfig.md) in the Ad Selection API.

This method is intended to be used for end-to-end testing. This API is enabled only for apps in debug mode with developer options enabled. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_CUSTOM_AUDIENCE](../android/adservices/common/AdServicesPermissions.md) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_PROTECTED_SIGNALS](../android/adservices/common/AdServicesPermissions.md) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_AD_SELECTION](../android/adservices/common/AdServicesPermissions.md)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>:This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this API is not enabled for the caller The receiver either returns a`void`for a successful run, or an [Exception](../java/lang/Exception.md) indicates the error. |

### resetAllAdSelectionFromOutcomesConfigRemoteOverrides

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
open fun resetAllAdSelectionFromOutcomesConfigRemoteOverrides(
    executor: Executor, 
    receiver: OutcomeReceiver<Any!, Exception!>
): Unit
```

Removes all override data for [AdSelectionFromOutcomesConfig](../android/adservices/adselection/AdSelectionFromOutcomesConfig.md) in the Ad Selection API.

This method is intended to be used for end-to-end testing. This API is enabled only for apps in debug mode with developer options enabled. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_CUSTOM_AUDIENCE](../android/adservices/common/AdServicesPermissions.md) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_PROTECTED_SIGNALS](../android/adservices/common/AdServicesPermissions.md) or [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_AD_SELECTION](../android/adservices/common/AdServicesPermissions.md)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md):This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>:This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this API is not enabled for the caller The receiver either returns a`void`for a successful run, or an [Exception](../java/lang/Exception.md) indicates the error. |
