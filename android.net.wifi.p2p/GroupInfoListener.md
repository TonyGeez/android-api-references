# WifiP2pManager.GroupInfoListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GroupInfoListener

Kotlin| [Java](../android/net/wifi/p2p/WifiP2pManager.GroupInfoListener.md) 
| --- | --- |

```
interface GroupInfoListener
```

| [android.net.wifi.p2p.WifiP2pManager.GroupInfoListener](../android/net/wifi/p2p/WifiP2pManager.GroupInfoListener.md) |

Interface for callback invocation when group info is available

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupInfoAvailable](../android/net/wifi/p2p/WifiP2pManager.GroupInfoListener.md))`(`group:` ` [WifiP2pGroup](../android/net/wifi/p2p/WifiP2pGroup.md)!`)` The requested p2p group info is available |

## Public methods

### onGroupInfoAvailable

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGroupInfoAvailable(group: WifiP2pGroup!): Unit
```

The requested p2p group info is available

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `group` | [WifiP2pGroup](../android/net/wifi/p2p/WifiP2pGroup.md)!:Wi-Fi p2p group info |
