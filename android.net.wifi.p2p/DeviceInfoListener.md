# WifiP2pManager.DeviceInfoListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeviceInfoListener

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/p2p/WifiP2pManager.DeviceInfoListener "View this page in Java") 
| --- | --- |

```
interface DeviceInfoListener
```

| [android.net.wifi.p2p.WifiP2pManager.DeviceInfoListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.DeviceInfoListener#) |

Interface for callback invocation when [android.net.wifi.p2p.WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice) is available in response to [requestDeviceInfo(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.wifi.p2p.WifiP2pManager.DeviceInfoListener)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestDeviceInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.DeviceInfoListener)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDeviceInfoAvailable](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.DeviceInfoListener#onDeviceInfoAvailable(android.net.wifi.p2p.WifiP2pDevice))`(`wifiP2pDevice:` ` [WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice)?`)` The requested [android.net.wifi.p2p.WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice) is available. |

## Public methods

### onDeviceInfoAvailable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDeviceInfoAvailable(wifiP2pDevice: WifiP2pDevice?): Unit
```

The requested [android.net.wifi.p2p.WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice) is available.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `wifiP2pDevice` | [WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice)?:Wi-Fi p2p [android.net.wifi.p2p.WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice) This value may be`null`. |
