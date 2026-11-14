# NsdManager.DiscoveryListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DiscoveryListener

Kotlin| [Java](../android/net/nsd/NsdManager.DiscoveryListener.md) 
| --- | --- |

```
interface DiscoveryListener
```

| [android.net.nsd.NsdManager.DiscoveryListener](../android/net/nsd/NsdManager.DiscoveryListener.md) |

Interface for callback invocation for service discovery

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDiscoveryStarted](../android/net/nsd/NsdManager.DiscoveryListener.md))`(`serviceType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDiscoveryStopped](../android/net/nsd/NsdManager.DiscoveryListener.md))`(`serviceType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceFound](../android/net/nsd/NsdManager.DiscoveryListener.md))`(`serviceInfo:` ` [NsdServiceInfo](NsdServiceInfo.md)!`)` <br /> |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceLost](../android/net/nsd/NsdManager.DiscoveryListener.md))`(`serviceInfo:` ` [NsdServiceInfo](NsdServiceInfo.md)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStartDiscoveryFailed](../android/net/nsd/NsdManager.DiscoveryListener.md))`(`serviceType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStopDiscoveryFailed](../android/net/nsd/NsdManager.DiscoveryListener.md))`(`serviceType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

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
