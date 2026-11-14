# WifiP2pManager.DeviceInfoListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeviceInfoListener

Kotlin| [Java](../android/net/wifi/p2p/WifiP2pManager.DeviceInfoListener.md) 
| --- | --- |

```
interface DeviceInfoListener
```

| [android.net.wifi.p2p.WifiP2pManager.DeviceInfoListener](../android/net/wifi/p2p/WifiP2pManager.DeviceInfoListener.md) |

Interface for callback invocation when [android.net.wifi.p2p.WifiP2pDevice](WifiP2pDevice.md) is available in response to [requestDeviceInfo(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.wifi.p2p.WifiP2pManager.DeviceInfoListener)](WifiP2pManager.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDeviceInfoAvailable](../android/net/wifi/p2p/WifiP2pManager.DeviceInfoListener.md))`(`wifiP2pDevice:` ` [WifiP2pDevice](WifiP2pDevice.md)?`)` The requested [android.net.wifi.p2p.WifiP2pDevice](WifiP2pDevice.md) is available. |

## Public methods

### onDeviceInfoAvailable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDeviceInfoAvailable(wifiP2pDevice: WifiP2pDevice?): Unit
```

The requested [android.net.wifi.p2p.WifiP2pDevice](WifiP2pDevice.md) is available.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `wifiP2pDevice` | [WifiP2pDevice](WifiP2pDevice.md)?:Wi-Fi p2p [android.net.wifi.p2p.WifiP2pDevice](WifiP2pDevice.md) This value may be`null`. |
