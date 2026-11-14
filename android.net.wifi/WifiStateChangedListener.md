# WifiManager.WifiStateChangedListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiStateChangedListener

Kotlin| [Java](../android/net/wifi/WifiManager.WifiStateChangedListener.md) 
| --- | --- |

```
interface WifiStateChangedListener
```

| [android.net.wifi.WifiManager.WifiStateChangedListener](../android/net/wifi/WifiManager.WifiStateChangedListener.md) |

Listener interface for applications to be notified when the Wi-Fi enabled state changes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onWifiStateChanged](../android/net/wifi/WifiManager.WifiStateChangedListener.md))`()` Called when the Wi-Fi enabled state changes. |

## Public methods

### onWifiStateChanged

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onWifiStateChanged(): Unit
```

Called when the Wi-Fi enabled state changes. The new value can be queried via [WifiManager.getWifiState()](../android/net/wifi/WifiManager.md)).
