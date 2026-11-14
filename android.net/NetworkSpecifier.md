# NetworkSpecifier

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NetworkSpecifier

Kotlin| [Java](NetworkSpecifier.md) 
| --- | --- |

```
abstract class NetworkSpecifier
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.NetworkSpecifier](NetworkSpecifier.md) |

| Known Direct Subclasses [EthernetNetworkSpecifier](EthernetNetworkSpecifier.md), [L2capNetworkSpecifier](L2capNetworkSpecifier.md), [TelephonyNetworkSpecifier](TelephonyNetworkSpecifier.md), [WifiAwareNetworkSpecifier](../android.net.wifi.aware/WifiAwareNetworkSpecifier.md), [WifiNetworkSpecifier](../android.net.wifi/WifiNetworkSpecifier.md) |------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------| | [EthernetNetworkSpecifier](EthernetNetworkSpecifier.md) | A [NetworkSpecifier](NetworkSpecifier.md) used to identify ethernet interfaces. | | [L2capNetworkSpecifier](L2capNetworkSpecifier.md) | A [NetworkSpecifier](NetworkSpecifier.md) used to identify an L2CAP network over BLE. | | [TelephonyNetworkSpecifier](TelephonyNetworkSpecifier.md) | NetworkSpecifier object for cellular network request. | | [WifiAwareNetworkSpecifier](../android.net.wifi.aware/WifiAwareNetworkSpecifier.md) | Network specifier object used to request a Wi-Fi Aware network. | | [WifiNetworkSpecifier](../android.net.wifi/WifiNetworkSpecifier.md) | Network specifier object used to request a Wi-Fi network. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Describes specific properties of a requested network for use in a [NetworkRequest](NetworkRequest.md). This as an abstract class. Applications shouldn't instantiate this class by themselves, but can obtain instances of subclasses of this class via other APIs.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NetworkSpecifier](NetworkSpecifier.md))`()` Create a placeholder object. |

## Public constructors

### NetworkSpecifier

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NetworkSpecifier()
```

Create a placeholder object. Please use subclasses of this class in a [NetworkRequest](NetworkRequest.md) to request a network.
