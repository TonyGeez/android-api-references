# WifiP2pManager.ConnectionInfoListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConnectionInfoListener

Kotlin| [Java](../android/net/wifi/p2p/WifiP2pManager.ConnectionInfoListener.md) 
| --- | --- |

```
interface ConnectionInfoListener
```

| [android.net.wifi.p2p.WifiP2pManager.ConnectionInfoListener](../android/net/wifi/p2p/WifiP2pManager.ConnectionInfoListener.md) |

Interface for callback invocation when connection info is available

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConnectionInfoAvailable](../android/net/wifi/p2p/WifiP2pManager.ConnectionInfoListener.md))`(`info:` ` [WifiP2pInfo](WifiP2pInfo.md)!`)` The requested connection info is available |

## Public methods

### onConnectionInfoAvailable

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onConnectionInfoAvailable(info: WifiP2pInfo!): Unit
```

The requested connection info is available

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------|
| `info` | [WifiP2pInfo](WifiP2pInfo.md)!:Wi-Fi p2p connection info |
