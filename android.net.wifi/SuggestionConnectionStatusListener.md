# WifiManager.SuggestionConnectionStatusListener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SuggestionConnectionStatusListener

Kotlin| [Java](../android/net/wifi/WifiManager.SuggestionConnectionStatusListener.md) 
| --- | --- |

```
interface SuggestionConnectionStatusListener
```

| [android.net.wifi.WifiManager.SuggestionConnectionStatusListener](../android/net/wifi/WifiManager.SuggestionConnectionStatusListener.md) |

Interface for suggestion connection status listener. Should be implemented by applications and set when calling [WifiManager.addSuggestionConnectionStatusListener(](WifiManager.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConnectionStatus](../android/net/wifi/WifiManager.SuggestionConnectionStatusListener.md))`(`wifiNetworkSuggestion:` ` [WifiNetworkSuggestion](WifiNetworkSuggestion.md)`, `failureReason:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the framework attempted to connect to a suggestion provided by the registering app, but the connection to the suggestion failed. |

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
| `wifiNetworkSuggestion` | [WifiNetworkSuggestion](WifiNetworkSuggestion.md):The suggestion which failed to connect. This value cannot be`null`. |
| `failureReason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the connection failure reason code. Value is [android.net.wifi.WifiManager#STATUS_SUGGESTION_CONNECTION_FAILURE_UNKNOWN](WifiManager.md), [android.net.wifi.WifiManager#STATUS_SUGGESTION_CONNECTION_FAILURE_ASSOCIATION](WifiManager.md), [android.net.wifi.WifiManager#STATUS_SUGGESTION_CONNECTION_FAILURE_AUTHENTICATION](WifiManager.md), or [android.net.wifi.WifiManager#STATUS_SUGGESTION_CONNECTION_FAILURE_IP_PROVISIONING](WifiManager.md) |
