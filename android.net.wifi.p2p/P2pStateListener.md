# WifiP2pManager.P2pStateListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# P2pStateListener

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/p2p/WifiP2pManager.P2pStateListener "View this page in Java") 
| --- | --- |

```
interface P2pStateListener
```

| [android.net.wifi.p2p.WifiP2pManager.P2pStateListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.P2pStateListener#) |

Interface for callback invocation when p2p state is available in response to [requestP2pState](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestP2pState(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.P2pStateListener)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onP2pStateAvailable](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.P2pStateListener#onP2pStateAvailable(kotlin.Int))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The requested p2p state is available. |

## Public methods

### onP2pStateAvailable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onP2pStateAvailable(state: Int): Unit
```

The requested p2p state is available.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Wi-Fi p2p state Value is [android.net.wifi.p2p.WifiP2pManager#WIFI_P2P_STATE_DISABLED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_STATE_DISABLED:kotlin.Int), or [android.net.wifi.p2p.WifiP2pManager#WIFI_P2P_STATE_ENABLED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_STATE_ENABLED:kotlin.Int) |

**See Also**

- [#WIFI_P2P_STATE_DISABLED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_STATE_DISABLED:kotlin.Int)
- [#WIFI_P2P_STATE_ENABLED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_STATE_ENABLED:kotlin.Int)
