# WifiP2pManager.GroupInfoListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GroupInfoListener

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/p2p/WifiP2pManager.GroupInfoListener "View this page in Java") 

```
interface GroupInfoListener
```

| [android.net.wifi.p2p.WifiP2pManager.GroupInfoListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.GroupInfoListener#) |

Interface for callback invocation when group info is available

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupInfoAvailable](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.GroupInfoListener#onGroupInfoAvailable(android.net.wifi.p2p.WifiP2pGroup))`(`group:` ` [WifiP2pGroup](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup)!`)` The requested p2p group info is available |

## Public methods

### onGroupInfoAvailable

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGroupInfoAvailable(group: WifiP2pGroup!): Unit
```

The requested p2p group info is available

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `group` | [WifiP2pGroup](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup)!:Wi-Fi p2p group info |
