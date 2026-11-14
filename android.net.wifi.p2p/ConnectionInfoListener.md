# WifiP2pManager.ConnectionInfoListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConnectionInfoListener

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/p2p/WifiP2pManager.ConnectionInfoListener "View this page in Java") 
| --- | --- |

```
interface ConnectionInfoListener
```

| [android.net.wifi.p2p.WifiP2pManager.ConnectionInfoListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ConnectionInfoListener#) |

Interface for callback invocation when connection info is available

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConnectionInfoAvailable](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ConnectionInfoListener#onConnectionInfoAvailable(android.net.wifi.p2p.WifiP2pInfo))`(`info:` ` [WifiP2pInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pInfo)!`)` The requested connection info is available |

## Public methods

### onConnectionInfoAvailable

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onConnectionInfoAvailable(info: WifiP2pInfo!): Unit
```

The requested connection info is available

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------|
| `info` | [WifiP2pInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pInfo)!:Wi-Fi p2p connection info |
