# WifiManager.WifiStateChangedListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiStateChangedListener

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/WifiManager.WifiStateChangedListener "View this page in Java") 

```
interface WifiStateChangedListener
```

| [android.net.wifi.WifiManager.WifiStateChangedListener](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WifiStateChangedListener#) |

Listener interface for applications to be notified when the Wi-Fi enabled state changes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onWifiStateChanged](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.WifiStateChangedListener#onWifiStateChanged())`()` Called when the Wi-Fi enabled state changes. |

## Public methods

### onWifiStateChanged

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onWifiStateChanged(): Unit
```

Called when the Wi-Fi enabled state changes. The new value can be queried via [WifiManager.getWifiState()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#getWifiState()).
