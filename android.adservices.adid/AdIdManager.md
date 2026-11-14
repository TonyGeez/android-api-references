# AdIdManager

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# AdIdManager

Kotlin| [Java](AdIdManager.md) 
| --- | --- |

```
open class AdIdManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adid.AdIdManager](AdIdManager.md) |

AdId Manager provides APIs for app and ad-SDKs to access advertising ID. The advertising ID is a unique, per-device, user-resettable ID for advertising. It gives users better controls and provides developers with a simple, standard system to continue to monetize their apps via personalized ads (formerly known as interest-based ads).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [AdIdManager](AdIdManager.md) | [get](AdIdManager.md))`(`context:` ` [Context](../android.content/Context.md)`)` Factory method for creating an instance of AdIdManager. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getAdId](AdIdManager.md))`(`executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [AdServicesOutcomeReceiver](../android.adservices.common/AdServicesOutcomeReceiver.md)< [AdId](AdId.md)!,` ` [Exception](../java.lang/Exception.md)!>`)` Return the AdId. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getAdId](AdIdManager.md))`(`executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `callback:` ` [OutcomeReceiver](../android.os/OutcomeReceiver.md)< [AdId](AdId.md)!,` ` [Exception](../java.lang/Exception.md)!>`)` Return the AdId. |
| --- | --- |

## Public methods

### get

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 6](https://developer.android.com/sdkExtensions) 

```
open static fun get(context: Context): AdIdManager
```

Factory method for creating an instance of AdIdManager.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md):The [Context](../android.content/Context.md) to use This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [AdIdManager](AdIdManager.md) | A [AdIdManager](AdIdManager.md) instance This value cannot be`null`. |

### getAdId

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAdId(
    executor: Executor, 
    callback: AdServicesOutcomeReceiver<AdId!, Exception!>
): Unit
```

**Deprecated:** *use [getAdId(java.util.concurrent.Executor,android.os.OutcomeReceiver)](AdIdManager.md))instead. Android R is no longer supported.*

Return the AdId. For use on Android R or lower. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_AD_ID](../android.adservices.common/AdServicesPermissions.md)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java.util.concurrent/Executor.md):The executor to run callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [AdServicesOutcomeReceiver](../android.adservices.common/AdServicesOutcomeReceiver.md)\< [AdId](AdId.md)!, [Exception](../java.lang/Exception.md)!\>:The callback that's called after adid are available or an error occurs. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | This value cannot be`null`. |

### getAdId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
open fun getAdId(
    executor: Executor, 
    callback: OutcomeReceiver<AdId!, Exception!>
): Unit
```

Return the AdId. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_AD_ID](../android.adservices.common/AdServicesPermissions.md)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java.util.concurrent/Executor.md):The executor to run callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [AdId](AdId.md)!, [Exception](../java.lang/Exception.md)!\>:The callback that's called after adid are available or an error occurs. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | This value cannot be`null`. |
