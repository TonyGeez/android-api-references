# ServiceDiscoveryInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceDiscoveryInfo

Kotlin| [Java](ServiceDiscoveryInfo.md) 
| --- | --- |

```
class ServiceDiscoveryInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.aware.ServiceDiscoveryInfo](ServiceDiscoveryInfo.md) |

An object providing information about a Wi-Fi Aware discovery session with a specific peer.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\> | [getMatchFilters](ServiceDiscoveryInfo.md))`()` Get the filter which resulted in this service discovery. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPairedAlias](ServiceDiscoveryInfo.md))`()` Get the paired device alias if the discovered device has already paired. |
| [AwarePairingConfig](AwarePairingConfig.md)? | [getPairingConfig](ServiceDiscoveryInfo.md))`()` Get the discovered device's pairing config. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPeerCipherSuite](ServiceDiscoveryInfo.md))`()` Get the cipher suite type specified by the publish session to be used for data-path setup. |
| [PeerHandle](PeerHandle.md) | [getPeerHandle](ServiceDiscoveryInfo.md))`()` Get the peer handle for the peer matching our discovery operation |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getScid](ServiceDiscoveryInfo.md))`()` Get the Security context identifier is associate with PMK for data path security config. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getServiceSpecificInfo](ServiceDiscoveryInfo.md))`()` The service specific information (arbitrary byte array) provided by the peer as part of its discovery configuration. |

## Public methods

### getMatchFilters

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMatchFilters(): MutableList<ByteArray!>
```

Get the filter which resulted in this service discovery. For [PublishConfig.PUBLISH_TYPE_UNSOLICITED](PublishConfig.md), [SubscribeConfig.SUBSCRIBE_TYPE_PASSIVE](SubscribeConfig.md) discovery sessions this is the publisher's match filter. For [PublishConfig.PUBLISH_TYPE_SOLICITED](PublishConfig.md), [SubscribeConfig.SUBSCRIBE_TYPE_ACTIVE](SubscribeConfig.md) discovery sessions this is the subscriber's match filter.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!> | A list of byte arrays representing the match filter. An empty list if match filter is not set. This value cannot be`null`. |

### getPairedAlias

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPairedAlias(): String?
```

Get the paired device alias if the discovered device has already paired. If not null device will automatically start the NAN pairing verification, [DiscoverySessionCallback.onPairingVerificationSucceed(PeerHandle, String)](DiscoverySessionCallback.md))will trigger when verification is finished 

### getPairingConfig

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPairingConfig(): AwarePairingConfig?
```

Get the discovered device's pairing config. Can be used for the following pairing setup or bootstrapping request.

| Return ||
|-----------------------------------------------------------------------------------------------------------------|--------------------------|
| [AwarePairingConfig](AwarePairingConfig.md)? | This value may be`null`. |

**See Also**

- [android.net.wifi.aware.AwarePairingConfig](AwarePairingConfig.md) 

### getPeerCipherSuite

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPeerCipherSuite(): Int
```

Get the cipher suite type specified by the publish session to be used for data-path setup.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | peerCipherSuite An integer represent the cipher suite used to encrypt the data-path. Value is either`0`or a combination of [android.net.wifi.aware.Characteristics#WIFI_AWARE_CIPHER_SUITE_NONE](Characteristics.md), [android.net.wifi.aware.Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_SK_128](Characteristics.md), [android.net.wifi.aware.Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_SK_256](Characteristics.md), [android.net.wifi.aware.Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_128](Characteristics.md), and [android.net.wifi.aware.Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_256](Characteristics.md) |

### getPeerHandle

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPeerHandle(): PeerHandle
```

Get the peer handle for the peer matching our discovery operation

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [PeerHandle](PeerHandle.md) | An opaque handle representing the discovered peer. This value cannot be`null`. |

### getScid

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getScid(): ByteArray?
```

Get the Security context identifier is associate with PMK for data path security config. Only use for [Characteristics.WIFI_AWARE_CIPHER_SUITE_NCS_PK_128](Characteristics.md) and [Characteristics.WIFI_AWARE_CIPHER_SUITE_NCS_PK_256](Characteristics.md) to get the PMKID set by[WifiAwareDataPathSecurityConfig.Builder.setPmkId(byte[])](https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareDataPathSecurityConfig.Builder#setPmkId(kotlin.ByteArray))from publish session. This can help the Wi-Fi Aware data-path setup to select the correct PMK/PMKID

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | An arbitrary byte array represent the security context identifier.`null`if Security context identifier is not set. |

### getServiceSpecificInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServiceSpecificInfo(): ByteArray?
```

The service specific information (arbitrary byte array) provided by the peer as part of its discovery configuration.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | An arbitrary byte array represent the service specific information.`null`if service specific information is not set. |

**See Also**

- [android.net.wifi.aware.PublishConfig.Builder#setServiceSpecificInfo(byte[])](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig.Builder#setServiceSpecificInfo(kotlin.ByteArray))
- [android.net.wifi.aware.SubscribeConfig.Builder#setServiceSpecificInfo(byte[])](https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeConfig.Builder#setServiceSpecificInfo(kotlin.ByteArray))
