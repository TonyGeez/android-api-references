# WifiManager.SuggestionUserApprovalStatusListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SuggestionUserApprovalStatusListener

Kotlin| [Java](../android/net/wifi/WifiManager.SuggestionUserApprovalStatusListener.md) 
| --- | --- |

```
interface SuggestionUserApprovalStatusListener
```

| [android.net.wifi.WifiManager.SuggestionUserApprovalStatusListener](../android/net/wifi/WifiManager.SuggestionUserApprovalStatusListener.md) |

Interface for network suggestion user approval status change listener. Should be implemented by applications and registered using [addSuggestionUserApprovalStatusListener(java.util.concurrent.Executor,android.net.wifi.WifiManager.SuggestionUserApprovalStatusListener)](../android/net/wifi/WifiManager.md))(

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUserApprovalStatusChange](../android/net/wifi/WifiManager.SuggestionUserApprovalStatusListener.md))`(`status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the user approval status of the App has changed. |

## Public methods

### onUserApprovalStatusChange

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onUserApprovalStatusChange(status: Int): Unit
```

Called when the user approval status of the App has changed.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current status code for the user approval. One of the`STATUS_SUGGESTION_APPROVAL_`values. Value is [android.net.wifi.WifiManager#STATUS_SUGGESTION_APPROVAL_UNKNOWN](../android/net/wifi/WifiManager.md), [android.net.wifi.WifiManager#STATUS_SUGGESTION_APPROVAL_PENDING](../android/net/wifi/WifiManager.md), [android.net.wifi.WifiManager#STATUS_SUGGESTION_APPROVAL_APPROVED_BY_USER](../android/net/wifi/WifiManager.md), [android.net.wifi.WifiManager#STATUS_SUGGESTION_APPROVAL_REJECTED_BY_USER](../android/net/wifi/WifiManager.md), or [android.net.wifi.WifiManager#STATUS_SUGGESTION_APPROVAL_APPROVED_BY_CARRIER_PRIVILEGE](../android/net/wifi/WifiManager.md) |
