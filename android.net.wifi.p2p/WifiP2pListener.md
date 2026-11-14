# WifiP2pManager.WifiP2pListener

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiP2pListener

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener "View this page in Java") 
| --- | --- |

```
interface WifiP2pListener
```

| [android.net.wifi.p2p.WifiP2pManager.WifiP2pListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener#) |

Interface used to listen to Wi-Fi p2p various changes such as device state change, discovery started/stopped, connection change, etc.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDeviceConfigurationChanged](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener#onDeviceConfigurationChanged(android.net.wifi.p2p.WifiP2pDevice))`(`p2pDevice:` ` [WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice)?`)` Called when this device details have changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDiscoveryStateChanged](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener#onDiscoveryStateChanged(kotlin.Int))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when peer discovery has either started or stopped. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFrequencyChanged](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener#onFrequencyChanged(android.net.wifi.p2p.WifiP2pInfo,%20android.net.wifi.p2p.WifiP2pGroup))`(`p2pInfo:` ` [WifiP2pInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pInfo)`, `p2pGroup:` ` [WifiP2pGroup](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup)`)` Called when the frequency of a formed group has been changed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupCreated](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener#onGroupCreated(android.net.wifi.p2p.WifiP2pInfo,%20android.net.wifi.p2p.WifiP2pGroup))`(`p2pInfo:` ` [WifiP2pInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pInfo)`, `p2pGroup:` ` [WifiP2pGroup](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup)`)` Called when either group owner or group client has created p2p group successfully. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupCreating](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener#onGroupCreating())`()` Called when either group owner or group client is creating p2p group. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupCreationFailed](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener#onGroupCreationFailed(kotlin.Int))`(`reason:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when group creation has failed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupNegotiationRejectedByUser](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener#onGroupNegotiationRejectedByUser())`()` Called when group negotiation has been rejected by user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupRemoved](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener#onGroupRemoved())`()` Called when p2p group has been removed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onListenStateChanged](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener#onListenStateChanged(kotlin.Int))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when peer listen has either started or stopped. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onP2pStateChanged](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener#onP2pStateChanged(kotlin.Int))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when Wi-Fi p2p has been enabled or disabled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPeerClientDisconnected](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener#onPeerClientDisconnected(android.net.wifi.p2p.WifiP2pInfo,%20android.net.wifi.p2p.WifiP2pGroup))`(`p2pInfo:` ` [WifiP2pInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pInfo)`, `p2pGroup:` ` [WifiP2pGroup](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup)`)` Called to indicate group owner that a group client has disconnected. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPeerClientJoined](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener#onPeerClientJoined(android.net.wifi.p2p.WifiP2pInfo,%20android.net.wifi.p2p.WifiP2pGroup))`(`p2pInfo:` ` [WifiP2pInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pInfo)`, `p2pGroup:` ` [WifiP2pGroup](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup)`)` Called to indicate group owner that a group client has joined p2p group successfully. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPeerListChanged](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.WifiP2pListener#onPeerListChanged(android.net.wifi.p2p.WifiP2pDeviceList))`(`p2pDeviceList:` ` [WifiP2pDeviceList](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDeviceList)`)` Called when the available peer list has changed. |

## Public methods

### onDeviceConfigurationChanged

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDeviceConfigurationChanged(p2pDevice: WifiP2pDevice?): Unit
```

Called when this device details have changed.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `p2pDevice` | [WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice)?:provides this device details. This value may be`null`. |

**See Also**

- [#WIFI_P2P_THIS_DEVICE_CHANGED_ACTION](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_THIS_DEVICE_CHANGED_ACTION:kotlin.String)
- [#requestDeviceInfo(Channel, DeviceInfoListener)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestDeviceInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.DeviceInfoListener)) 

### onDiscoveryStateChanged

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDiscoveryStateChanged(state: Int): Unit
```

Called when peer discovery has either started or stopped.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):indicates whether discovery has started or stopped. Value is [android.net.wifi.p2p.WifiP2pManager#WIFI_P2P_DISCOVERY_STOPPED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_DISCOVERY_STOPPED:kotlin.Int), or [android.net.wifi.p2p.WifiP2pManager#WIFI_P2P_DISCOVERY_STARTED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_DISCOVERY_STARTED:kotlin.Int) |

**See Also**

- [#WIFI_P2P_DISCOVERY_CHANGED_ACTION](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_DISCOVERY_CHANGED_ACTION:kotlin.String)
- [#requestDiscoveryState(Channel, DiscoveryStateListener)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestDiscoveryState(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.DiscoveryStateListener))
- [#WIFI_P2P_DISCOVERY_STARTED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_DISCOVERY_STARTED:kotlin.Int)
- [#WIFI_P2P_DISCOVERY_STOPPED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_DISCOVERY_STOPPED:kotlin.Int) 

### onFrequencyChanged

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onFrequencyChanged(
    p2pInfo: WifiP2pInfo, 
    p2pGroup: WifiP2pGroup
): Unit
```

Called when the frequency of a formed group has been changed.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `p2pInfo` | [WifiP2pInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pInfo):provides the p2p connection info. This value cannot be`null`. |
| `p2pGroup` | [WifiP2pGroup](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup):provides the details of the group. This value cannot be`null`. |

### onGroupCreated

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onGroupCreated(
    p2pInfo: WifiP2pInfo, 
    p2pGroup: WifiP2pGroup
): Unit
```

Called when either group owner or group client has created p2p group successfully.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `p2pInfo` | [WifiP2pInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pInfo):provides the p2p connection info. This value cannot be`null`. |
| `p2pGroup` | [WifiP2pGroup](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup):provides the details of the group. This value cannot be`null`. |

### onGroupCreating

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onGroupCreating(): Unit
```

Called when either group owner or group client is creating p2p group. 

### onGroupCreationFailed

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onGroupCreationFailed(reason: Int): Unit
```

Called when group creation has failed.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):provides the group creation failure reason. Value is [android.net.wifi.p2p.WifiP2pManager#GROUP_CREATION_FAILURE_REASON_CONNECTION_CANCELLED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#GROUP_CREATION_FAILURE_REASON_CONNECTION_CANCELLED:kotlin.Int), [android.net.wifi.p2p.WifiP2pManager#GROUP_CREATION_FAILURE_REASON_TIMED_OUT](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#GROUP_CREATION_FAILURE_REASON_TIMED_OUT:kotlin.Int), [android.net.wifi.p2p.WifiP2pManager#GROUP_CREATION_FAILURE_REASON_USER_REJECTED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#GROUP_CREATION_FAILURE_REASON_USER_REJECTED:kotlin.Int), [android.net.wifi.p2p.WifiP2pManager#GROUP_CREATION_FAILURE_REASON_PROVISION_DISCOVERY_FAILED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#GROUP_CREATION_FAILURE_REASON_PROVISION_DISCOVERY_FAILED:kotlin.Int), [android.net.wifi.p2p.WifiP2pManager#GROUP_CREATION_FAILURE_REASON_GROUP_REMOVED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#GROUP_CREATION_FAILURE_REASON_GROUP_REMOVED:kotlin.Int), or [android.net.wifi.p2p.WifiP2pManager#GROUP_CREATION_FAILURE_REASON_INVITATION_FAILED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#GROUP_CREATION_FAILURE_REASON_INVITATION_FAILED:kotlin.Int) |

### onGroupNegotiationRejectedByUser

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onGroupNegotiationRejectedByUser(): Unit
```

Called when group negotiation has been rejected by user. 

### onGroupRemoved

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onGroupRemoved(): Unit
```

Called when p2p group has been removed. 

### onListenStateChanged

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onListenStateChanged(state: Int): Unit
```

Called when peer listen has either started or stopped.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):indicates whether listen has started or stopped. Value is [android.net.wifi.p2p.WifiP2pManager#WIFI_P2P_LISTEN_STOPPED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_LISTEN_STOPPED:kotlin.Int), or [android.net.wifi.p2p.WifiP2pManager#WIFI_P2P_LISTEN_STARTED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_LISTEN_STARTED:kotlin.Int) |

**See Also**

- [#ACTION_WIFI_P2P_LISTEN_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#ACTION_WIFI_P2P_LISTEN_STATE_CHANGED:kotlin.String)
- [#getListenState(Channel, Executor, Consumer)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#getListenState(android.net.wifi.p2p.WifiP2pManager.Channel,%20java.util.concurrent.Executor,%20java.util.function.Consumer))
- [#WIFI_P2P_LISTEN_STARTED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_LISTEN_STARTED:kotlin.Int)
- [#WIFI_P2P_LISTEN_STOPPED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_LISTEN_STOPPED:kotlin.Int) 

### onP2pStateChanged

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onP2pStateChanged(state: Int): Unit
```

Called when Wi-Fi p2p has been enabled or disabled.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):indicates whether Wi-Fi p2p is enabled or disabled. Value is [android.net.wifi.p2p.WifiP2pManager#WIFI_P2P_STATE_DISABLED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_STATE_DISABLED:kotlin.Int), or [android.net.wifi.p2p.WifiP2pManager#WIFI_P2P_STATE_ENABLED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_STATE_ENABLED:kotlin.Int) |

**See Also**

- [#WIFI_P2P_STATE_CHANGED_ACTION](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_STATE_CHANGED_ACTION:kotlin.String)
- [#requestP2pState(Channel, P2pStateListener)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestP2pState(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.P2pStateListener))
- [#WIFI_P2P_STATE_ENABLED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_STATE_ENABLED:kotlin.Int)
- [#WIFI_P2P_STATE_DISABLED](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_STATE_DISABLED:kotlin.Int) 

### onPeerClientDisconnected

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPeerClientDisconnected(
    p2pInfo: WifiP2pInfo, 
    p2pGroup: WifiP2pGroup
): Unit
```

Called to indicate group owner that a group client has disconnected.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `p2pInfo` | [WifiP2pInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pInfo):provides the p2p connection info. This value cannot be`null`. |
| `p2pGroup` | [WifiP2pGroup](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup):provides the details of the group. This value cannot be`null`. |

### onPeerClientJoined

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPeerClientJoined(
    p2pInfo: WifiP2pInfo, 
    p2pGroup: WifiP2pGroup
): Unit
```

Called to indicate group owner that a group client has joined p2p group successfully.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `p2pInfo` | [WifiP2pInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pInfo):provides the p2p connection info. This value cannot be`null`. |
| `p2pGroup` | [WifiP2pGroup](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup):provides the details of the group. This value cannot be`null`. |

### onPeerListChanged

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPeerListChanged(p2pDeviceList: WifiP2pDeviceList): Unit
```

Called when the available peer list has changed. This can be sent as a result of peers being found, lost or updated.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `p2pDeviceList` | [WifiP2pDeviceList](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDeviceList):provides the full list of current peers. This value cannot be`null`. |

**See Also**

- [#WIFI_P2P_PEERS_CHANGED_ACTION](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#WIFI_P2P_PEERS_CHANGED_ACTION:kotlin.String)
- [#requestPeers(Channel, PeerListListener)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestPeers(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.PeerListListener))
