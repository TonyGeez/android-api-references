# NetworkSpecifier

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NetworkSpecifier

Kotlin| [Java](https://developer.android.com/reference/android/net/NetworkSpecifier "View this page in Java") 

```
abstract class NetworkSpecifier
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.NetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier#) |

| Known Direct Subclasses [EthernetNetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/EthernetNetworkSpecifier), [L2capNetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/L2capNetworkSpecifier), [TelephonyNetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/TelephonyNetworkSpecifier), [WifiAwareNetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkSpecifier), [WifiNetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier) |------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------| | [EthernetNetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/EthernetNetworkSpecifier) | A [NetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier#) used to identify ethernet interfaces. | | [L2capNetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/L2capNetworkSpecifier) | A [NetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier#) used to identify an L2CAP network over BLE. | | [TelephonyNetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/TelephonyNetworkSpecifier) | NetworkSpecifier object for cellular network request. | | [WifiAwareNetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkSpecifier) | Network specifier object used to request a Wi-Fi Aware network. | | [WifiNetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier) | Network specifier object used to request a Wi-Fi network. | |

Describes specific properties of a requested network for use in a [NetworkRequest](https://developer.android.com/reference/kotlin/android/net/NetworkRequest). This as an abstract class. Applications shouldn't instantiate this class by themselves, but can obtain instances of subclasses of this class via other APIs.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier#NetworkSpecifier())`()` Create a placeholder object. |

## Public constructors

### NetworkSpecifier

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NetworkSpecifier()
```

Create a placeholder object. Please use subclasses of this class in a [NetworkRequest](https://developer.android.com/reference/kotlin/android/net/NetworkRequest) to request a network.
