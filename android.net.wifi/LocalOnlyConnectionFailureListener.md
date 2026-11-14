# WifiManager.LocalOnlyConnectionFailureListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocalOnlyConnectionFailureListener

Kotlin| [Java](../android/net/wifi/WifiManager.LocalOnlyConnectionFailureListener.md) 
| --- | --- |

```
interface LocalOnlyConnectionFailureListener
```

| [android.net.wifi.WifiManager.LocalOnlyConnectionFailureListener](../android/net/wifi/WifiManager.LocalOnlyConnectionFailureListener.md) |

Interface for local-only connection failure listener. Should be implemented by applications and set when calling [WifiManager.addLocalOnlyConnectionFailureListener(Executor, LocalOnlyConnectionFailureListener)](../android/net/wifi/WifiManager.md))

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConnectionFailed](../android/net/wifi/WifiManager.LocalOnlyConnectionFailureListener.md))`(`wifiNetworkSpecifier:` ` [WifiNetworkSpecifier](../android/net/wifi/WifiNetworkSpecifier.md)`, `failureReason:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the framework attempted to connect to a local-only network requested by the registering app, but the connection to the network failed. |

## Public methods

### onConnectionFailed

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onConnectionFailed(
    wifiNetworkSpecifier: WifiNetworkSpecifier, 
    failureReason: Int
): Unit
```

Called when the framework attempted to connect to a local-only network requested by the registering app, but the connection to the network failed.

| Parameters ||
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `wifiNetworkSpecifier` | [WifiNetworkSpecifier](../android/net/wifi/WifiNetworkSpecifier.md):The [WifiNetworkSpecifier](../android/net/wifi/WifiNetworkSpecifier.md) which failed to connect. This value cannot be`null`. |
| `failureReason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the connection failure reason code. Value is [android.net.wifi.WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_UNKNOWN](../android/net/wifi/WifiManager.md), [android.net.wifi.WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_ASSOCIATION](../android/net/wifi/WifiManager.md), [android.net.wifi.WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_AUTHENTICATION](../android/net/wifi/WifiManager.md), [android.net.wifi.WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_IP_PROVISIONING](../android/net/wifi/WifiManager.md), [android.net.wifi.WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_NOT_FOUND](../android/net/wifi/WifiManager.md), [android.net.wifi.WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_NO_RESPONSE](../android/net/wifi/WifiManager.md), or [android.net.wifi.WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_USER_REJECT](../android/net/wifi/WifiManager.md) |
