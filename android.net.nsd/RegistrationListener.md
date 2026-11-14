# NsdManager.RegistrationListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RegistrationListener

Kotlin| [Java](https://developer.android.com/reference/android/net/nsd/NsdManager.RegistrationListener "View this page in Java") 
| --- | --- |

```
interface RegistrationListener
```

| [android.net.nsd.NsdManager.RegistrationListener](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.RegistrationListener#) |

Interface for callback invocation for service registration

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRegistrationFailed](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.RegistrationListener#onRegistrationFailed(android.net.nsd.NsdServiceInfo,%20kotlin.Int))`(`serviceInfo:` ` [NsdServiceInfo](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo)!`, `errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceRegistered](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.RegistrationListener#onServiceRegistered(android.net.nsd.NsdServiceInfo))`(`serviceInfo:` ` [NsdServiceInfo](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceUnregistered](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.RegistrationListener#onServiceUnregistered(android.net.nsd.NsdServiceInfo))`(`serviceInfo:` ` [NsdServiceInfo](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo)!`)` <br /> |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUnregistrationFailed](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.RegistrationListener#onUnregistrationFailed(android.net.nsd.NsdServiceInfo,%20kotlin.Int))`(`serviceInfo:` ` [NsdServiceInfo](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo)!`, `errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

## Public methods

### onRegistrationFailed

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onRegistrationFailed(
    serviceInfo: NsdServiceInfo!, 
    errorCode: Int
): Unit
```  

### onServiceRegistered

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onServiceRegistered(serviceInfo: NsdServiceInfo!): Unit
```  

### onServiceUnregistered

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onServiceUnregistered(serviceInfo: NsdServiceInfo!): Unit
```  

### onUnregistrationFailed

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onUnregistrationFailed(
    serviceInfo: NsdServiceInfo!, 
    errorCode: Int
): Unit
```
