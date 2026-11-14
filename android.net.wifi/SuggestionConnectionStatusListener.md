# WifiManager.SuggestionConnectionStatusListener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SuggestionConnectionStatusListener

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/WifiManager.SuggestionConnectionStatusListener "View this page in Java") 

```
interface SuggestionConnectionStatusListener
```

| [android.net.wifi.WifiManager.SuggestionConnectionStatusListener](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SuggestionConnectionStatusListener#) |

Interface for suggestion connection status listener. Should be implemented by applications and set when calling [WifiManager.addSuggestionConnectionStatusListener(](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addSuggestionConnectionStatusListener(java.util.concurrent.Executor,%20android.net.wifi.WifiManager.SuggestionConnectionStatusListener)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConnectionStatus](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SuggestionConnectionStatusListener#onConnectionStatus(android.net.wifi.WifiNetworkSuggestion,%20kotlin.Int))`(`wifiNetworkSuggestion:` ` [WifiNetworkSuggestion](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion)`, `failureReason:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the framework attempted to connect to a suggestion provided by the registering app, but the connection to the suggestion failed. |

## Public methods

### onConnectionStatus

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onConnectionStatus(
    wifiNetworkSuggestion: WifiNetworkSuggestion, 
    failureReason: Int
): Unit
```

Called when the framework attempted to connect to a suggestion provided by the registering app, but the connection to the suggestion failed.

| Parameters ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `wifiNetworkSuggestion` | [WifiNetworkSuggestion](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSuggestion):The suggestion which failed to connect. This value cannot be`null`. |
| `failureReason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the connection failure reason code. Value is [android.net.wifi.WifiManager#STATUS_SUGGESTION_CONNECTION_FAILURE_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_SUGGESTION_CONNECTION_FAILURE_UNKNOWN:kotlin.Int), [android.net.wifi.WifiManager#STATUS_SUGGESTION_CONNECTION_FAILURE_ASSOCIATION](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_SUGGESTION_CONNECTION_FAILURE_ASSOCIATION:kotlin.Int), [android.net.wifi.WifiManager#STATUS_SUGGESTION_CONNECTION_FAILURE_AUTHENTICATION](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_SUGGESTION_CONNECTION_FAILURE_AUTHENTICATION:kotlin.Int), or [android.net.wifi.WifiManager#STATUS_SUGGESTION_CONNECTION_FAILURE_IP_PROVISIONING](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_SUGGESTION_CONNECTION_FAILURE_IP_PROVISIONING:kotlin.Int) |
