# AdIdManager

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# AdIdManager

Kotlin| [Java](https://developer.android.com/reference/android/adservices/adid/AdIdManager "View this page in Java") 

```
open class AdIdManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.adservices.adid.AdIdManager](https://developer.android.com/reference/kotlin/android/adservices/adid/AdIdManager#) |

AdId Manager provides APIs for app and ad-SDKs to access advertising ID. The advertising ID is a unique, per-device, user-resettable ID for advertising. It gives users better controls and provides developers with a simple, standard system to continue to monetize their apps via personalized ads (formerly known as interest-based ads).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [AdIdManager](https://developer.android.com/reference/kotlin/android/adservices/adid/AdIdManager#) | [get](https://developer.android.com/reference/kotlin/android/adservices/adid/AdIdManager#get(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`)` Factory method for creating an instance of AdIdManager. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getAdId](https://developer.android.com/reference/kotlin/android/adservices/adid/AdIdManager#getAdId(java.util.concurrent.Executor,%20android.adservices.common.AdServicesOutcomeReceiver))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [AdServicesOutcomeReceiver](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesOutcomeReceiver.html#)< [AdId](https://developer.android.com/reference/kotlin/android/adservices/adid/AdId)!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` Return the AdId. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getAdId](https://developer.android.com/reference/kotlin/android/adservices/adid/AdIdManager#getAdId(java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [AdId](https://developer.android.com/reference/kotlin/android/adservices/adid/AdId)!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` Return the AdId. |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):The [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) to use This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [AdIdManager](https://developer.android.com/reference/kotlin/android/adservices/adid/AdIdManager#) | A [AdIdManager](https://developer.android.com/reference/kotlin/android/adservices/adid/AdIdManager#) instance This value cannot be`null`. |

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

**Deprecated:** *use [getAdId(java.util.concurrent.Executor,android.os.OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/adservices/adid/AdIdManager#getAdId(java.util.concurrent.Executor,%20android.os.OutcomeReceiver))instead. Android R is no longer supported.*

Return the AdId. For use on Android R or lower. 
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_AD_ID](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_AD_ID:kotlin.String)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The executor to run callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [AdServicesOutcomeReceiver](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesOutcomeReceiver.html#)\< [AdId](https://developer.android.com/reference/kotlin/android/adservices/adid/AdId)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>:The callback that's called after adid are available or an error occurs. This value cannot be`null`. |

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
Requires [android.adservices.common.AdServicesPermissions#ACCESS_ADSERVICES_AD_ID](https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_AD_ID:kotlin.String)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The executor to run callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [AdId](https://developer.android.com/reference/kotlin/android/adservices/adid/AdId)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>:The callback that's called after adid are available or an error occurs. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | This value cannot be`null`. |
