# WifiP2pManager.ChannelListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ChannelListener

Kotlin| [Java](../android/net/wifi/p2p/WifiP2pManager.ChannelListener.md) 
| --- | --- |

```
interface ChannelListener
```

| [android.net.wifi.p2p.WifiP2pManager.ChannelListener](../android/net/wifi/p2p/WifiP2pManager.ChannelListener.md) |

Interface for callback invocation when framework channel is lost

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onChannelDisconnected](../android/net/wifi/p2p/WifiP2pManager.ChannelListener.md))`()` The channel to the framework has been disconnected. |

## Public methods

### onChannelDisconnected

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onChannelDisconnected(): Unit
```

The channel to the framework has been disconnected. Application could try re-initializing using [initialize](WifiP2pManager.md))
