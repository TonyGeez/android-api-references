# WifiP2pManager.PeerListListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PeerListListener

Kotlin| [Java](../android/net/wifi/p2p/WifiP2pManager.PeerListListener.md) 
| --- | --- |

```
interface PeerListListener
```

| [android.net.wifi.p2p.WifiP2pManager.PeerListListener](../android/net/wifi/p2p/WifiP2pManager.PeerListListener.md) |

Interface for callback invocation when peer list is available

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPeersAvailable](../android/net/wifi/p2p/WifiP2pManager.PeerListListener.md))`(`peers:` ` [WifiP2pDeviceList](WifiP2pDeviceList.md)!`)` The requested peer list is available |

## Public methods

### onPeersAvailable

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPeersAvailable(peers: WifiP2pDeviceList!): Unit
```

The requested peer list is available

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------|
| `peers` | [WifiP2pDeviceList](WifiP2pDeviceList.md)!:List of available peers |
