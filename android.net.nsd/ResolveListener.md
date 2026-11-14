# NsdManager.ResolveListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ResolveListener

Kotlin| [Java](https://developer.android.com/reference/android/net/nsd/NsdManager.ResolveListener "View this page in Java") 

```
interface ResolveListener
```

| [android.net.nsd.NsdManager.ResolveListener](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.ResolveListener#) |

Callback for use with android.net.nsd.NsdManager#resolveService to resolve the service info and use with [NsdManager.stopServiceResolution](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#stopServiceResolution(android.net.nsd.NsdManager.ResolveListener))to stop resolution.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResolutionStopped](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.ResolveListener#onResolutionStopped(android.net.nsd.NsdServiceInfo))`(`serviceInfo:` ` [NsdServiceInfo](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo)`)` Called on the internal thread or with an executor passed to android. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResolveFailed](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.ResolveListener#onResolveFailed(android.net.nsd.NsdServiceInfo,%20kotlin.Int))`(`serviceInfo:` ` [NsdServiceInfo](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo)!`, `errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called on the internal thread or with an executor passed to android. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceResolved](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.ResolveListener#onServiceResolved(android.net.nsd.NsdServiceInfo))`(`serviceInfo:` ` [NsdServiceInfo](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo)!`)` Called on the internal thread or with an executor passed to android. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStopResolutionFailed](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.ResolveListener#onStopResolutionFailed(android.net.nsd.NsdServiceInfo,%20kotlin.Int))`(`serviceInfo:` ` [NsdServiceInfo](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo)`, `errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called once on the internal thread or with an executor passed to android. |

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
| `serviceInfo` | [NsdServiceInfo](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo):This value cannot be`null`. |

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
| `serviceInfo` | [NsdServiceInfo](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo):This value cannot be`null`. |
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.net.nsd.NsdManager#FAILURE_OPERATION_NOT_RUNNING](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#FAILURE_OPERATION_NOT_RUNNING:kotlin.Int) |
