# TransportInfo

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransportInfo

Kotlin| [Java](../android/net/TransportInfo.md) 
| --- | --- |

```
interface TransportInfo
```

| [android.net.TransportInfo](../android/net/TransportInfo.md) |

| Known Direct Subclasses [WifiAwareNetworkInfo](../android/net/wifi/aware/WifiAwareNetworkInfo.md), [WifiInfo](../android/net/wifi/WifiInfo.md) |--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------| | [WifiAwareNetworkInfo](../android/net/wifi/aware/WifiAwareNetworkInfo.md) | Wi-Fi Aware-specific network information. | | [WifiInfo](../android/net/wifi/WifiInfo.md) | Describes the state of any Wi-Fi connection that is active or is in the process of being set up. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A container for transport-specific capabilities which is returned by [NetworkCapabilities.getTransportInfo()](../android/net/NetworkCapabilities.md)). Specific networks may provide concrete implementations of this interface.

## Summary
