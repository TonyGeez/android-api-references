# NsdManager.ServiceInfoCallback

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

# ServiceInfoCallback

Kotlin| [Java](https://developer.android.com/reference/android/net/nsd/NsdManager.ServiceInfoCallback "View this page in Java") 
| --- | --- |

```
interface ServiceInfoCallback
```

| [android.net.nsd.NsdManager.ServiceInfoCallback](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.ServiceInfoCallback#) |

Callback to listen to service info updates. For use with [NsdManager.registerServiceInfoCallback](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#registerServiceInfoCallback(android.net.nsd.NsdServiceInfo,%20java.util.concurrent.Executor,%20android.net.nsd.NsdManager.ServiceInfoCallback))to register, and with [NsdManager.unregisterServiceInfoCallback](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#unregisterServiceInfoCallback(android.net.nsd.NsdManager.ServiceInfoCallback))to stop listening.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceInfoCallbackRegistrationFailed](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.ServiceInfoCallback#onServiceInfoCallbackRegistrationFailed(kotlin.Int))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reports that registering the callback failed with an error. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceInfoCallbackUnregistered](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.ServiceInfoCallback#onServiceInfoCallbackUnregistered())`()` Reports that service info updates have stopped. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceLost](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.ServiceInfoCallback#onServiceLost())`()` Reports when the service that this callback listens to becomes unavailable. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceUpdated](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.ServiceInfoCallback#onServiceUpdated(android.net.nsd.NsdServiceInfo))`(`serviceInfo:` ` [NsdServiceInfo](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo)`)` Reports updated service info. |

## Public methods

### onServiceInfoCallbackRegistrationFailed

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onServiceInfoCallbackRegistrationFailed(errorCode: Int): Unit
```

Reports that registering the callback failed with an error. Called on the executor passed to [NsdManager.registerServiceInfoCallback](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#registerServiceInfoCallback(android.net.nsd.NsdServiceInfo,%20java.util.concurrent.Executor,%20android.net.nsd.NsdManager.ServiceInfoCallback)). onServiceInfoCallbackRegistrationFailed will be called exactly once when the callback could not be registered. No other callback will be sent in that case.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.net.nsd.NsdManager#FAILURE_ALREADY_ACTIVE](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#FAILURE_ALREADY_ACTIVE:kotlin.Int), or [android.net.nsd.NsdManager#FAILURE_BAD_PARAMETERS](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#FAILURE_BAD_PARAMETERS:kotlin.Int) |

### onServiceInfoCallbackUnregistered

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onServiceInfoCallbackUnregistered(): Unit
```

Reports that service info updates have stopped. Called on the executor passed to [NsdManager.registerServiceInfoCallback](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#registerServiceInfoCallback(android.net.nsd.NsdServiceInfo,%20java.util.concurrent.Executor,%20android.net.nsd.NsdManager.ServiceInfoCallback)). A callback unregistration operation will call onServiceInfoCallbackUnregistered once. After this, the callback may be reused. 

### onServiceLost

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onServiceLost(): Unit
```

Reports when the service that this callback listens to becomes unavailable. Called on the executor passed to [NsdManager.registerServiceInfoCallback](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#registerServiceInfoCallback(android.net.nsd.NsdServiceInfo,%20java.util.concurrent.Executor,%20android.net.nsd.NsdManager.ServiceInfoCallback)). The service may become available again, in which case [onServiceUpdated](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.ServiceInfoCallback#onServiceUpdated(android.net.nsd.NsdServiceInfo))will be called. 

### onServiceUpdated

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onServiceUpdated(serviceInfo: NsdServiceInfo): Unit
```

Reports updated service info. Called on the executor passed to [NsdManager.registerServiceInfoCallback](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#registerServiceInfoCallback(android.net.nsd.NsdServiceInfo,%20java.util.concurrent.Executor,%20android.net.nsd.NsdManager.ServiceInfoCallback)). Any service updates will be notified via this callback until [NsdManager.unregisterServiceInfoCallback](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#unregisterServiceInfoCallback(android.net.nsd.NsdManager.ServiceInfoCallback))is called. This will only be called once the service is found, so may never be called if the service is never present.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------|
| `serviceInfo` | [NsdServiceInfo](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo):This value cannot be`null`. |
