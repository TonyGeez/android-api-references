# TransportInfo

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransportInfo

Kotlin| [Java](https://developer.android.com/reference/android/net/TransportInfo "View this page in Java") 
| --- | --- |

```
interface TransportInfo
```

| [android.net.TransportInfo](https://developer.android.com/reference/kotlin/android/net/TransportInfo#) |

| Known Direct Subclasses [WifiAwareNetworkInfo](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkInfo), [WifiInfo](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo) |--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------| | [WifiAwareNetworkInfo](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkInfo) | Wi-Fi Aware-specific network information. | | [WifiInfo](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo) | Describes the state of any Wi-Fi connection that is active or is in the process of being set up. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A container for transport-specific capabilities which is returned by [NetworkCapabilities.getTransportInfo()](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities#getTransportInfo()). Specific networks may provide concrete implementations of this interface.

## Summary
