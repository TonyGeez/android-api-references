# WifiManager.LocalOnlyConnectionFailureListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocalOnlyConnectionFailureListener

Kotlin| [Java](../android/net/wifi/WifiManager.LocalOnlyConnectionFailureListener.md) 
| --- | --- |

```
interface LocalOnlyConnectionFailureListener
```

| [android.net.wifi.WifiManager.LocalOnlyConnectionFailureListener](../android/net/wifi/WifiManager.LocalOnlyConnectionFailureListener.md) |

Interface for local-only connection failure listener. Should be implemented by applications and set when calling [WifiManager.addLocalOnlyConnectionFailureListener(Executor, LocalOnlyConnectionFailureListener)](WifiManager.md))

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConnectionFailed](../android/net/wifi/WifiManager.LocalOnlyConnectionFailureListener.md))`(`wifiNetworkSpecifier:` ` [WifiNetworkSpecifier](WifiNetworkSpecifier.md)`, `failureReason:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the framework attempted to connect to a local-only network requested by the registering app, but the connection to the network failed. |

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
| `wifiNetworkSpecifier` | [WifiNetworkSpecifier](WifiNetworkSpecifier.md):The [WifiNetworkSpecifier](WifiNetworkSpecifier.md) which failed to connect. This value cannot be`null`. |
| `failureReason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the connection failure reason code. Value is [android.net.wifi.WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_UNKNOWN](WifiManager.md), [android.net.wifi.WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_ASSOCIATION](WifiManager.md), [android.net.wifi.WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_AUTHENTICATION](WifiManager.md), [android.net.wifi.WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_IP_PROVISIONING](WifiManager.md), [android.net.wifi.WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_NOT_FOUND](WifiManager.md), [android.net.wifi.WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_NO_RESPONSE](WifiManager.md), or [android.net.wifi.WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_USER_REJECT](WifiManager.md) |
