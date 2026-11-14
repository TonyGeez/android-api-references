# WifiP2pManager.NetworkInfoListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NetworkInfoListener

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/p2p/WifiP2pManager.NetworkInfoListener "View this page in Java") 

```
interface NetworkInfoListener
```

| [android.net.wifi.p2p.WifiP2pManager.NetworkInfoListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.NetworkInfoListener#) |

Interface for callback invocation when [android.net.NetworkInfo](https://developer.android.com/reference/kotlin/android/net/NetworkInfo.html#) is available in response to [requestNetworkInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#requestNetworkInfo(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.WifiP2pManager.NetworkInfoListener)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onNetworkInfoAvailable](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.NetworkInfoListener#onNetworkInfoAvailable(android.net.NetworkInfo))`(`networkInfo:` ` [NetworkInfo](https://developer.android.com/reference/kotlin/android/net/NetworkInfo.html#)`)` The requested [android.net.NetworkInfo](https://developer.android.com/reference/kotlin/android/net/NetworkInfo.html#) is available |

## Public methods

### onNetworkInfoAvailable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onNetworkInfoAvailable(networkInfo: NetworkInfo): Unit
```

The requested [android.net.NetworkInfo](https://developer.android.com/reference/kotlin/android/net/NetworkInfo.html#) is available

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `networkInfo` | [NetworkInfo](https://developer.android.com/reference/kotlin/android/net/NetworkInfo.html#):Wi-Fi p2p [android.net.NetworkInfo](https://developer.android.com/reference/kotlin/android/net/NetworkInfo.html#) This value cannot be`null`. |
