# NsdManager.ResolveListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ResolveListener

Kotlin| [Java](../android/net/nsd/NsdManager.ResolveListener.md) 
| --- | --- |

```
interface ResolveListener
```

| [android.net.nsd.NsdManager.ResolveListener](../android/net/nsd/NsdManager.ResolveListener.md) |

Callback for use with android.net.nsd.NsdManager#resolveService to resolve the service info and use with [NsdManager.stopServiceResolution](../android/net/nsd/NsdManager.md))to stop resolution.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResolutionStopped](../android/net/nsd/NsdManager.ResolveListener.md))`(`serviceInfo:` ` [NsdServiceInfo](../android/net/nsd/NsdServiceInfo.md)`)` Called on the internal thread or with an executor passed to android. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResolveFailed](../android/net/nsd/NsdManager.ResolveListener.md))`(`serviceInfo:` ` [NsdServiceInfo](../android/net/nsd/NsdServiceInfo.md)!`, `errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called on the internal thread or with an executor passed to android. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceResolved](../android/net/nsd/NsdManager.ResolveListener.md))`(`serviceInfo:` ` [NsdServiceInfo](../android/net/nsd/NsdServiceInfo.md)!`)` Called on the internal thread or with an executor passed to android. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStopResolutionFailed](../android/net/nsd/NsdManager.ResolveListener.md))`(`serviceInfo:` ` [NsdServiceInfo](../android/net/nsd/NsdServiceInfo.md)`, `errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called once on the internal thread or with an executor passed to android. |

## Public methods

### onResolutionStopped

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions) 

```
open fun onResolutionStopped(serviceInfo: NsdServiceInfo): Unit
```

Called on the internal thread or with an executor passed to android.net.nsd.NsdManager#resolveService to report the resolution was stopped. A stop resolution operation would call either onResolutionStopped or onStopResolutionFailed once based on the result.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------|
| `serviceInfo` | [NsdServiceInfo](../android/net/nsd/NsdServiceInfo.md):This value cannot be`null`. |

### onResolveFailed

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onResolveFailed(
    serviceInfo: NsdServiceInfo!, 
    errorCode: Int
): Unit
```

Called on the internal thread or with an executor passed to android.net.nsd.NsdManager#resolveService to report the resolution was failed with an error. A resolution operation would call either onServiceResolved or onResolveFailed once based on the result. 

### onServiceResolved

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onServiceResolved(serviceInfo: NsdServiceInfo!): Unit
```

Called on the internal thread or with an executor passed to android.net.nsd.NsdManager#resolveService to report the resolved service info. A resolution operation would call either onServiceResolved or onResolveFailed once based on the result. 

### onStopResolutionFailed

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions) 

```
open fun onStopResolutionFailed(
    serviceInfo: NsdServiceInfo, 
    errorCode: Int
): Unit
```

Called once on the internal thread or with an executor passed to android.net.nsd.NsdManager#resolveService to report that stopping resolution failed with an error. A stop resolution operation would call either onResolutionStopped or onStopResolutionFailed once based on the result.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `serviceInfo` | [NsdServiceInfo](../android/net/nsd/NsdServiceInfo.md):This value cannot be`null`. |
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.net.nsd.NsdManager#FAILURE_OPERATION_NOT_RUNNING](../android/net/nsd/NsdManager.md) |
