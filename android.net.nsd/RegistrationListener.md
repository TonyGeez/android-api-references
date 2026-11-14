# NsdManager.RegistrationListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RegistrationListener

Kotlin| [Java](../android/net/nsd/NsdManager.RegistrationListener.md) 
| --- | --- |

```
interface RegistrationListener
```

| [android.net.nsd.NsdManager.RegistrationListener](../android/net/nsd/NsdManager.RegistrationListener.md) |

Interface for callback invocation for service registration

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRegistrationFailed](../android/net/nsd/NsdManager.RegistrationListener.md))`(`serviceInfo:` ` [NsdServiceInfo](NsdServiceInfo.md)!`, `errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceRegistered](../android/net/nsd/NsdManager.RegistrationListener.md))`(`serviceInfo:` ` [NsdServiceInfo](NsdServiceInfo.md)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceUnregistered](../android/net/nsd/NsdManager.RegistrationListener.md))`(`serviceInfo:` ` [NsdServiceInfo](NsdServiceInfo.md)!`)` <br /> |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUnregistrationFailed](../android/net/nsd/NsdManager.RegistrationListener.md))`(`serviceInfo:` ` [NsdServiceInfo](NsdServiceInfo.md)!`, `errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

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
