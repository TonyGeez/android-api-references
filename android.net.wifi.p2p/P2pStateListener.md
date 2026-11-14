# WifiP2pManager.P2pStateListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# P2pStateListener

Kotlin| [Java](../android/net/wifi/p2p/WifiP2pManager.P2pStateListener.md) 
| --- | --- |

```
interface P2pStateListener
```

| [android.net.wifi.p2p.WifiP2pManager.P2pStateListener](../android/net/wifi/p2p/WifiP2pManager.P2pStateListener.md) |

Interface for callback invocation when p2p state is available in response to [requestP2pState](../android/net/wifi/p2p/WifiP2pManager.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onP2pStateAvailable](../android/net/wifi/p2p/WifiP2pManager.P2pStateListener.md))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The requested p2p state is available. |

## Public methods

### onP2pStateAvailable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onP2pStateAvailable(state: Int): Unit
```

The requested p2p state is available.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Wi-Fi p2p state Value is [android.net.wifi.p2p.WifiP2pManager#WIFI_P2P_STATE_DISABLED](../android/net/wifi/p2p/WifiP2pManager.md), or [android.net.wifi.p2p.WifiP2pManager#WIFI_P2P_STATE_ENABLED](../android/net/wifi/p2p/WifiP2pManager.md) |

**See Also**

- [#WIFI_P2P_STATE_DISABLED](../android/net/wifi/p2p/WifiP2pManager.md)
- [#WIFI_P2P_STATE_ENABLED](../android/net/wifi/p2p/WifiP2pManager.md)
