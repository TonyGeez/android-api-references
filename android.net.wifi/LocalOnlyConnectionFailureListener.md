# WifiManager.LocalOnlyConnectionFailureListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocalOnlyConnectionFailureListener

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/WifiManager.LocalOnlyConnectionFailureListener "View this page in Java") 
| --- | --- |

```
interface LocalOnlyConnectionFailureListener
```

| [android.net.wifi.WifiManager.LocalOnlyConnectionFailureListener](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyConnectionFailureListener#) |

Interface for local-only connection failure listener. Should be implemented by applications and set when calling [WifiManager.addLocalOnlyConnectionFailureListener(Executor, LocalOnlyConnectionFailureListener)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addLocalOnlyConnectionFailureListener(java.util.concurrent.Executor,%20android.net.wifi.WifiManager.LocalOnlyConnectionFailureListener))

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConnectionFailed](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.LocalOnlyConnectionFailureListener#onConnectionFailed(android.net.wifi.WifiNetworkSpecifier,%20kotlin.Int))`(`wifiNetworkSpecifier:` ` [WifiNetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier)`, `failureReason:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the framework attempted to connect to a local-only network requested by the registering app, but the connection to the network failed. |

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
| `wifiNetworkSpecifier` | [WifiNetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier):The [WifiNetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier) which failed to connect. This value cannot be`null`. |
| `failureReason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the connection failure reason code. Value is [android.net.wifi.WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_UNKNOWN:kotlin.Int), [android.net.wifi.WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_ASSOCIATION](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_ASSOCIATION:kotlin.Int), [android.net.wifi.WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_AUTHENTICATION](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_AUTHENTICATION:kotlin.Int), [android.net.wifi.WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_IP_PROVISIONING](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_IP_PROVISIONING:kotlin.Int), [android.net.wifi.WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_NOT_FOUND](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_NOT_FOUND:kotlin.Int), [android.net.wifi.WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_NO_RESPONSE](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_NO_RESPONSE:kotlin.Int), or [android.net.wifi.WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_USER_REJECT](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_LOCAL_ONLY_CONNECTION_FAILURE_USER_REJECT:kotlin.Int) |
