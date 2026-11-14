# WifiP2pManager.DiscoveryStateListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DiscoveryStateListener

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/p2p/WifiP2pManager.DiscoveryStateListener "View this page in Java") 

```
interface DiscoveryStateListener
```

| [android.net.wifi.p2p.WifiP2pManager.DiscoveryStateListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.DiscoveryStateListener#) |

Interface for callback invocation when p2p state is available in response to [requestDiscoveryState](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestDiscoveryState(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.DiscoveryStateListener)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDiscoveryStateAvailable](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.DiscoveryStateListener#onDiscoveryStateAvailable(kotlin.Int))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The requested p2p discovery state is available. |

## Public methods

### onDiscoveryStateAvailable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDiscoveryStateAvailable(state: Int): Unit
```

The requested p2p discovery state is available.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Wi-Fi p2p discovery state Value is [android.net.wifi.p2p.WifiP2pManager#WIFI_P2P_DISCOVERY_STOPPED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_DISCOVERY_STOPPED:kotlin.Int), or [android.net.wifi.p2p.WifiP2pManager#WIFI_P2P_DISCOVERY_STARTED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_DISCOVERY_STARTED:kotlin.Int) |

**See Also**

- [#WIFI_P2P_DISCOVERY_STARTED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_DISCOVERY_STARTED:kotlin.Int)
- [#WIFI_P2P_DISCOVERY_STOPPED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_DISCOVERY_STOPPED:kotlin.Int)
