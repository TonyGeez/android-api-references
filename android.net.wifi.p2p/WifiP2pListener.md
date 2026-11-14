# WifiP2pManager.WifiP2pListener

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiP2pListener

Kotlin| [Java](../android/net/wifi/p2p/WifiP2pManager.WifiP2pListener.md) 
| --- | --- |

```
interface WifiP2pListener
```

| [android.net.wifi.p2p.WifiP2pManager.WifiP2pListener](../android/net/wifi/p2p/WifiP2pManager.WifiP2pListener.md) |

Interface used to listen to Wi-Fi p2p various changes such as device state change, discovery started/stopped, connection change, etc.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDeviceConfigurationChanged](../android/net/wifi/p2p/WifiP2pManager.WifiP2pListener.md))`(`p2pDevice:` ` [WifiP2pDevice](WifiP2pDevice.md)?`)` Called when this device details have changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDiscoveryStateChanged](../android/net/wifi/p2p/WifiP2pManager.WifiP2pListener.md))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when peer discovery has either started or stopped. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFrequencyChanged](../android/net/wifi/p2p/WifiP2pManager.WifiP2pListener.md))`(`p2pInfo:` ` [WifiP2pInfo](WifiP2pInfo.md)`, `p2pGroup:` ` [WifiP2pGroup](WifiP2pGroup.md)`)` Called when the frequency of a formed group has been changed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupCreated](../android/net/wifi/p2p/WifiP2pManager.WifiP2pListener.md))`(`p2pInfo:` ` [WifiP2pInfo](WifiP2pInfo.md)`, `p2pGroup:` ` [WifiP2pGroup](WifiP2pGroup.md)`)` Called when either group owner or group client has created p2p group successfully. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupCreating](../android/net/wifi/p2p/WifiP2pManager.WifiP2pListener.md))`()` Called when either group owner or group client is creating p2p group. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupCreationFailed](../android/net/wifi/p2p/WifiP2pManager.WifiP2pListener.md))`(`reason:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when group creation has failed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupNegotiationRejectedByUser](../android/net/wifi/p2p/WifiP2pManager.WifiP2pListener.md))`()` Called when group negotiation has been rejected by user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupRemoved](../android/net/wifi/p2p/WifiP2pManager.WifiP2pListener.md))`()` Called when p2p group has been removed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onListenStateChanged](../android/net/wifi/p2p/WifiP2pManager.WifiP2pListener.md))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when peer listen has either started or stopped. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onP2pStateChanged](../android/net/wifi/p2p/WifiP2pManager.WifiP2pListener.md))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when Wi-Fi p2p has been enabled or disabled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPeerClientDisconnected](../android/net/wifi/p2p/WifiP2pManager.WifiP2pListener.md))`(`p2pInfo:` ` [WifiP2pInfo](WifiP2pInfo.md)`, `p2pGroup:` ` [WifiP2pGroup](WifiP2pGroup.md)`)` Called to indicate group owner that a group client has disconnected. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPeerClientJoined](../android/net/wifi/p2p/WifiP2pManager.WifiP2pListener.md))`(`p2pInfo:` ` [WifiP2pInfo](WifiP2pInfo.md)`, `p2pGroup:` ` [WifiP2pGroup](WifiP2pGroup.md)`)` Called to indicate group owner that a group client has joined p2p group successfully. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPeerListChanged](../android/net/wifi/p2p/WifiP2pManager.WifiP2pListener.md))`(`p2pDeviceList:` ` [WifiP2pDeviceList](WifiP2pDeviceList.md)`)` Called when the available peer list has changed. |

## Public methods

### onDeviceConfigurationChanged

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDeviceConfigurationChanged(p2pDevice: WifiP2pDevice?): Unit
```

Called when this device details have changed.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `p2pDevice` | [WifiP2pDevice](WifiP2pDevice.md)?:provides this device details. This value may be`null`. |

**See Also**

- [#WIFI_P2P_THIS_DEVICE_CHANGED_ACTION](WifiP2pManager.md)
- [#requestDeviceInfo(Channel, DeviceInfoListener)](WifiP2pManager.md)) 

### onDiscoveryStateChanged

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDiscoveryStateChanged(state: Int): Unit
```

Called when peer discovery has either started or stopped.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):indicates whether discovery has started or stopped. Value is [android.net.wifi.p2p.WifiP2pManager#WIFI_P2P_DISCOVERY_STOPPED](WifiP2pManager.md), or [android.net.wifi.p2p.WifiP2pManager#WIFI_P2P_DISCOVERY_STARTED](WifiP2pManager.md) |

**See Also**

- [#WIFI_P2P_DISCOVERY_CHANGED_ACTION](WifiP2pManager.md)
- [#requestDiscoveryState(Channel, DiscoveryStateListener)](WifiP2pManager.md))
- [#WIFI_P2P_DISCOVERY_STARTED](WifiP2pManager.md)
- [#WIFI_P2P_DISCOVERY_STOPPED](WifiP2pManager.md) 

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
| `p2pInfo` | [WifiP2pInfo](WifiP2pInfo.md):provides the p2p connection info. This value cannot be`null`. |
| `p2pGroup` | [WifiP2pGroup](WifiP2pGroup.md):provides the details of the group. This value cannot be`null`. |

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
| `p2pInfo` | [WifiP2pInfo](WifiP2pInfo.md):provides the p2p connection info. This value cannot be`null`. |
| `p2pGroup` | [WifiP2pGroup](WifiP2pGroup.md):provides the details of the group. This value cannot be`null`. |

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
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):provides the group creation failure reason. Value is [android.net.wifi.p2p.WifiP2pManager#GROUP_CREATION_FAILURE_REASON_CONNECTION_CANCELLED](WifiP2pManager.md), [android.net.wifi.p2p.WifiP2pManager#GROUP_CREATION_FAILURE_REASON_TIMED_OUT](WifiP2pManager.md), [android.net.wifi.p2p.WifiP2pManager#GROUP_CREATION_FAILURE_REASON_USER_REJECTED](WifiP2pManager.md), [android.net.wifi.p2p.WifiP2pManager#GROUP_CREATION_FAILURE_REASON_PROVISION_DISCOVERY_FAILED](WifiP2pManager.md), [android.net.wifi.p2p.WifiP2pManager#GROUP_CREATION_FAILURE_REASON_GROUP_REMOVED](WifiP2pManager.md), or [android.net.wifi.p2p.WifiP2pManager#GROUP_CREATION_FAILURE_REASON_INVITATION_FAILED](WifiP2pManager.md) |

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
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):indicates whether listen has started or stopped. Value is [android.net.wifi.p2p.WifiP2pManager#WIFI_P2P_LISTEN_STOPPED](WifiP2pManager.md), or [android.net.wifi.p2p.WifiP2pManager#WIFI_P2P_LISTEN_STARTED](WifiP2pManager.md) |

**See Also**

- [#ACTION_WIFI_P2P_LISTEN_STATE_CHANGED](WifiP2pManager.md)
- [#getListenState(Channel, Executor, Consumer)](WifiP2pManager.md))
- [#WIFI_P2P_LISTEN_STARTED](WifiP2pManager.md)
- [#WIFI_P2P_LISTEN_STOPPED](WifiP2pManager.md) 

### onP2pStateChanged

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onP2pStateChanged(state: Int): Unit
```

Called when Wi-Fi p2p has been enabled or disabled.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):indicates whether Wi-Fi p2p is enabled or disabled. Value is [android.net.wifi.p2p.WifiP2pManager#WIFI_P2P_STATE_DISABLED](WifiP2pManager.md), or [android.net.wifi.p2p.WifiP2pManager#WIFI_P2P_STATE_ENABLED](WifiP2pManager.md) |

**See Also**

- [#WIFI_P2P_STATE_CHANGED_ACTION](WifiP2pManager.md)
- [#requestP2pState(Channel, P2pStateListener)](WifiP2pManager.md))
- [#WIFI_P2P_STATE_ENABLED](WifiP2pManager.md)
- [#WIFI_P2P_STATE_DISABLED](WifiP2pManager.md) 

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
| `p2pInfo` | [WifiP2pInfo](WifiP2pInfo.md):provides the p2p connection info. This value cannot be`null`. |
| `p2pGroup` | [WifiP2pGroup](WifiP2pGroup.md):provides the details of the group. This value cannot be`null`. |

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
| `p2pInfo` | [WifiP2pInfo](WifiP2pInfo.md):provides the p2p connection info. This value cannot be`null`. |
| `p2pGroup` | [WifiP2pGroup](WifiP2pGroup.md):provides the details of the group. This value cannot be`null`. |

### onPeerListChanged

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPeerListChanged(p2pDeviceList: WifiP2pDeviceList): Unit
```

Called when the available peer list has changed. This can be sent as a result of peers being found, lost or updated.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `p2pDeviceList` | [WifiP2pDeviceList](WifiP2pDeviceList.md):provides the full list of current peers. This value cannot be`null`. |

**See Also**

- [#WIFI_P2P_PEERS_CHANGED_ACTION](WifiP2pManager.md)
- [#requestPeers(Channel, PeerListListener)](WifiP2pManager.md))
