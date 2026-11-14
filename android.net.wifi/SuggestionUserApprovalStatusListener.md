# WifiManager.SuggestionUserApprovalStatusListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SuggestionUserApprovalStatusListener

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/WifiManager.SuggestionUserApprovalStatusListener "View this page in Java") 
| --- | --- |

```
interface SuggestionUserApprovalStatusListener
```

| [android.net.wifi.WifiManager.SuggestionUserApprovalStatusListener](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SuggestionUserApprovalStatusListener#) |

Interface for network suggestion user approval status change listener. Should be implemented by applications and registered using [addSuggestionUserApprovalStatusListener(java.util.concurrent.Executor,android.net.wifi.WifiManager.SuggestionUserApprovalStatusListener)](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#addSuggestionUserApprovalStatusListener(java.util.concurrent.Executor,%20android.net.wifi.WifiManager.SuggestionUserApprovalStatusListener))(

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUserApprovalStatusChange](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.SuggestionUserApprovalStatusListener#onUserApprovalStatusChange(kotlin.Int))`(`status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the user approval status of the App has changed. |

## Public methods

### onUserApprovalStatusChange

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onUserApprovalStatusChange(status: Int): Unit
```

Called when the user approval status of the App has changed.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current status code for the user approval. One of the`STATUS_SUGGESTION_APPROVAL_`values. Value is [android.net.wifi.WifiManager#STATUS_SUGGESTION_APPROVAL_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_SUGGESTION_APPROVAL_UNKNOWN:kotlin.Int), [android.net.wifi.WifiManager#STATUS_SUGGESTION_APPROVAL_PENDING](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_SUGGESTION_APPROVAL_PENDING:kotlin.Int), [android.net.wifi.WifiManager#STATUS_SUGGESTION_APPROVAL_APPROVED_BY_USER](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_SUGGESTION_APPROVAL_APPROVED_BY_USER:kotlin.Int), [android.net.wifi.WifiManager#STATUS_SUGGESTION_APPROVAL_REJECTED_BY_USER](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_SUGGESTION_APPROVAL_REJECTED_BY_USER:kotlin.Int), or [android.net.wifi.WifiManager#STATUS_SUGGESTION_APPROVAL_APPROVED_BY_CARRIER_PRIVILEGE](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#STATUS_SUGGESTION_APPROVAL_APPROVED_BY_CARRIER_PRIVILEGE:kotlin.Int) |
