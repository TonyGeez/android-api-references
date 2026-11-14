# WifiP2pManager.PeerListListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PeerListListener

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/p2p/WifiP2pManager.PeerListListener "View this page in Java") 

```
interface PeerListListener
```

| [android.net.wifi.p2p.WifiP2pManager.PeerListListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.PeerListListener#) |

Interface for callback invocation when peer list is available

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPeersAvailable](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.PeerListListener#onPeersAvailable(android.net.wifi.p2p.WifiP2pDeviceList))`(`peers:` ` [WifiP2pDeviceList](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDeviceList)!`)` The requested peer list is available |

## Public methods

### onPeersAvailable

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPeersAvailable(peers: WifiP2pDeviceList!): Unit
```

The requested peer list is available

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------|
| `peers` | [WifiP2pDeviceList](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDeviceList)!:List of available peers |
