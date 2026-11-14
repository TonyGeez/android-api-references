# WifiP2pManager.ChannelListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ChannelListener

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/p2p/WifiP2pManager.ChannelListener "View this page in Java") 

```
interface ChannelListener
```

| [android.net.wifi.p2p.WifiP2pManager.ChannelListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ChannelListener#) |

Interface for callback invocation when framework channel is lost

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onChannelDisconnected](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ChannelListener#onChannelDisconnected())`()` The channel to the framework has been disconnected. |

## Public methods

### onChannelDisconnected

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onChannelDisconnected(): Unit
```

The channel to the framework has been disconnected. Application could try re-initializing using [initialize](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#initialize(android.content.Context,%20android.os.Looper,%20android.net.wifi.p2p.WifiP2pManager.ChannelListener))
