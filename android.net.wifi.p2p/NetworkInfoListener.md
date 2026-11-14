# WifiP2pManager.NetworkInfoListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NetworkInfoListener

Kotlin| [Java](../android/net/wifi/p2p/WifiP2pManager.NetworkInfoListener.md) 
| --- | --- |

```
interface NetworkInfoListener
```

| [android.net.wifi.p2p.WifiP2pManager.NetworkInfoListener](../android/net/wifi/p2p/WifiP2pManager.NetworkInfoListener.md) |

Interface for callback invocation when [android.net.NetworkInfo](../android/net/NetworkInfo.md) is available in response to [requestNetworkInfo](../android/net/wifi/p2p/WifiP2pManager.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onNetworkInfoAvailable](../android/net/wifi/p2p/WifiP2pManager.NetworkInfoListener.md))`(`networkInfo:` ` [NetworkInfo](../android/net/NetworkInfo.md)`)` The requested [android.net.NetworkInfo](../android/net/NetworkInfo.md) is available |

## Public methods

### onNetworkInfoAvailable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onNetworkInfoAvailable(networkInfo: NetworkInfo): Unit
```

The requested [android.net.NetworkInfo](../android/net/NetworkInfo.md) is available

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `networkInfo` | [NetworkInfo](../android/net/NetworkInfo.md):Wi-Fi p2p [android.net.NetworkInfo](../android/net/NetworkInfo.md) This value cannot be`null`. |
