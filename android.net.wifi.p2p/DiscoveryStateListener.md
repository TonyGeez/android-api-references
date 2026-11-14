# WifiP2pManager.DiscoveryStateListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DiscoveryStateListener

Kotlin| [Java](../android/net/wifi/p2p/WifiP2pManager.DiscoveryStateListener.md) 
| --- | --- |

```
interface DiscoveryStateListener
```

| [android.net.wifi.p2p.WifiP2pManager.DiscoveryStateListener](../android/net/wifi/p2p/WifiP2pManager.DiscoveryStateListener.md) |

Interface for callback invocation when p2p state is available in response to [requestDiscoveryState](../android/net/wifi/p2p/WifiP2pManager.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDiscoveryStateAvailable](../android/net/wifi/p2p/WifiP2pManager.DiscoveryStateListener.md))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The requested p2p discovery state is available. |

## Public methods

### onDiscoveryStateAvailable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDiscoveryStateAvailable(state: Int): Unit
```

The requested p2p discovery state is available.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Wi-Fi p2p discovery state Value is [android.net.wifi.p2p.WifiP2pManager#WIFI_P2P_DISCOVERY_STOPPED](../android/net/wifi/p2p/WifiP2pManager.md), or [android.net.wifi.p2p.WifiP2pManager#WIFI_P2P_DISCOVERY_STARTED](../android/net/wifi/p2p/WifiP2pManager.md) |

**See Also**

- [#WIFI_P2P_DISCOVERY_STARTED](../android/net/wifi/p2p/WifiP2pManager.md)
- [#WIFI_P2P_DISCOVERY_STOPPED](../android/net/wifi/p2p/WifiP2pManager.md)
