# ConnectivityManager.OnNetworkActiveListener

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnNetworkActiveListener

Kotlin | [Java](../android/net/ConnectivityManager.OnNetworkActiveListener.md) 
| --- | --- |

```
interface OnNetworkActiveListener
```

| [android.net.ConnectivityManager.OnNetworkActiveListener](../android/net/ConnectivityManager.OnNetworkActiveListener.md) |

Callback for use with [ConnectivityManager.addDefaultNetworkActiveListener](../android/net/ConnectivityManager.md)) to find out when the system default network has gone in to a high power state.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onNetworkActive](../android/net/ConnectivityManager.OnNetworkActiveListener.md))`()` Called on the main thread of the process to report that the current data network has become active, and it is now a good time to perform any pending network operations. |

## Public methods

### onNetworkActive

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onNetworkActive(): Unit
```

Called on the main thread of the process to report that the current data network has become active, and it is now a good time to perform any pending network operations. Note that this listener only tells you when the network becomes active; if at any other time you want to know whether it is active (and thus okay to initiate network traffic), you can retrieve its instantaneous state with [ConnectivityManager.isDefaultNetworkActive](../android/net/ConnectivityManager.md)).
