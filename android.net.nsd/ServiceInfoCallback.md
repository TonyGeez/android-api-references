# NsdManager.ServiceInfoCallback

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

# ServiceInfoCallback

Kotlin| [Java](../android/net/nsd/NsdManager.ServiceInfoCallback.md) 
| --- | --- |

```
interface ServiceInfoCallback
```

| [android.net.nsd.NsdManager.ServiceInfoCallback](../android/net/nsd/NsdManager.ServiceInfoCallback.md) |

Callback to listen to service info updates. For use with [NsdManager.registerServiceInfoCallback](../android/net/nsd/NsdManager.md))to register, and with [NsdManager.unregisterServiceInfoCallback](../android/net/nsd/NsdManager.md))to stop listening.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceInfoCallbackRegistrationFailed](../android/net/nsd/NsdManager.ServiceInfoCallback.md))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reports that registering the callback failed with an error. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceInfoCallbackUnregistered](../android/net/nsd/NsdManager.ServiceInfoCallback.md))`()` Reports that service info updates have stopped. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceLost](../android/net/nsd/NsdManager.ServiceInfoCallback.md))`()` Reports when the service that this callback listens to becomes unavailable. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceUpdated](../android/net/nsd/NsdManager.ServiceInfoCallback.md))`(`serviceInfo:` ` [NsdServiceInfo](../android/net/nsd/NsdServiceInfo.md)`)` Reports updated service info. |

## Public methods

### onServiceInfoCallbackRegistrationFailed

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onServiceInfoCallbackRegistrationFailed(errorCode: Int): Unit
```

Reports that registering the callback failed with an error. Called on the executor passed to [NsdManager.registerServiceInfoCallback](../android/net/nsd/NsdManager.md)). onServiceInfoCallbackRegistrationFailed will be called exactly once when the callback could not be registered. No other callback will be sent in that case.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.net.nsd.NsdManager#FAILURE_ALREADY_ACTIVE](../android/net/nsd/NsdManager.md), or [android.net.nsd.NsdManager#FAILURE_BAD_PARAMETERS](../android/net/nsd/NsdManager.md) |

### onServiceInfoCallbackUnregistered

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onServiceInfoCallbackUnregistered(): Unit
```

Reports that service info updates have stopped. Called on the executor passed to [NsdManager.registerServiceInfoCallback](../android/net/nsd/NsdManager.md)). A callback unregistration operation will call onServiceInfoCallbackUnregistered once. After this, the callback may be reused. 

### onServiceLost

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onServiceLost(): Unit
```

Reports when the service that this callback listens to becomes unavailable. Called on the executor passed to [NsdManager.registerServiceInfoCallback](../android/net/nsd/NsdManager.md)). The service may become available again, in which case [onServiceUpdated](../android/net/nsd/NsdManager.ServiceInfoCallback.md))will be called. 

### onServiceUpdated

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onServiceUpdated(serviceInfo: NsdServiceInfo): Unit
```

Reports updated service info. Called on the executor passed to [NsdManager.registerServiceInfoCallback](../android/net/nsd/NsdManager.md)). Any service updates will be notified via this callback until [NsdManager.unregisterServiceInfoCallback](../android/net/nsd/NsdManager.md))is called. This will only be called once the service is found, so may never be called if the service is never present.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------|
| `serviceInfo` | [NsdServiceInfo](../android/net/nsd/NsdServiceInfo.md):This value cannot be`null`. |
