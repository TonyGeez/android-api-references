# NsdManager.DiscoveryListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DiscoveryListener

Kotlin| [Java](https://developer.android.com/reference/android/net/nsd/NsdManager.DiscoveryListener "View this page in Java") 

```
interface DiscoveryListener
```

| [android.net.nsd.NsdManager.DiscoveryListener](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.DiscoveryListener#) |

Interface for callback invocation for service discovery

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDiscoveryStarted](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.DiscoveryListener#onDiscoveryStarted(kotlin.String))`(`serviceType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDiscoveryStopped](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.DiscoveryListener#onDiscoveryStopped(kotlin.String))`(`serviceType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceFound](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.DiscoveryListener#onServiceFound(android.net.nsd.NsdServiceInfo))`(`serviceInfo:` ` [NsdServiceInfo](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceLost](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.DiscoveryListener#onServiceLost(android.net.nsd.NsdServiceInfo))`(`serviceInfo:` ` [NsdServiceInfo](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStartDiscoveryFailed](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.DiscoveryListener#onStartDiscoveryFailed(kotlin.String,%20kotlin.Int))`(`serviceType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStopDiscoveryFailed](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.DiscoveryListener#onStopDiscoveryFailed(kotlin.String,%20kotlin.Int))`(`serviceType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

## Public methods

### onDiscoveryStarted

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDiscoveryStarted(serviceType: String!): Unit
```  

### onDiscoveryStopped

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDiscoveryStopped(serviceType: String!): Unit
```  

### onServiceFound

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onServiceFound(serviceInfo: NsdServiceInfo!): Unit
```  

### onServiceLost

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onServiceLost(serviceInfo: NsdServiceInfo!): Unit
```  

### onStartDiscoveryFailed

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStartDiscoveryFailed(
    serviceType: String!, 
    errorCode: Int
): Unit
```  

### onStopDiscoveryFailed

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStopDiscoveryFailed(
    serviceType: String!, 
    errorCode: Int
): Unit
```
