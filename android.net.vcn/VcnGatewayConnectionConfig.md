# VcnGatewayConnectionConfig

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VcnGatewayConnectionConfig

Kotlin| [Java](VcnGatewayConnectionConfig.md) 
| --- | --- |

```
class VcnGatewayConnectionConfig
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.vcn.VcnGatewayConnectionConfig](VcnGatewayConnectionConfig.md) |

This class represents a configuration for a connection to a Virtual Carrier Network gateway.

Each VcnGatewayConnectionConfig represents a single logical connection to a carrier gateway, and may provide one or more telephony services (as represented by network capabilities). Each gateway is expected to provide mobility for a given session as the device roams across [Network](../android.net/Network.md) s.

A VCN connection based on this configuration will be brought up dynamically based on device settings, and filed NetworkRequests. Underlying Networks must provide INTERNET connectivity, and must be part of the subscription group under which this configuration is registered (see [android.net.vcn.VcnManager#setVcnConfig](VcnManager.md))).

As an abstraction of a cellular network, services that can be provided by a VCN network are limited to services provided by cellular networks:

- [NetworkCapabilities.NET_CAPABILITY_MMS](../android.net/NetworkCapabilities.md)
- [NetworkCapabilities.NET_CAPABILITY_SUPL](../android.net/NetworkCapabilities.md)
- [NetworkCapabilities.NET_CAPABILITY_DUN](../android.net/NetworkCapabilities.md)
- [NetworkCapabilities.NET_CAPABILITY_FOTA](../android.net/NetworkCapabilities.md)
- [NetworkCapabilities.NET_CAPABILITY_IMS](../android.net/NetworkCapabilities.md)
- [NetworkCapabilities.NET_CAPABILITY_CBS](../android.net/NetworkCapabilities.md)
- [NetworkCapabilities.NET_CAPABILITY_IA](../android.net/NetworkCapabilities.md)
- [NetworkCapabilities.NET_CAPABILITY_RCS](../android.net/NetworkCapabilities.md)
- [NetworkCapabilities.NET_CAPABILITY_XCAP](../android.net/NetworkCapabilities.md)
- [NetworkCapabilities.NET_CAPABILITY_EIMS](../android.net/NetworkCapabilities.md)
- [NetworkCapabilities.NET_CAPABILITY_INTERNET](../android.net/NetworkCapabilities.md)
- [NetworkCapabilities.NET_CAPABILITY_MCX](../android.net/NetworkCapabilities.md)

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/net/vcn/VcnGatewayConnectionConfig.Builder.md) This class is used to incrementally build [VcnGatewayConnectionConfig](VcnGatewayConnectionConfig.md) objects. |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIN_UDP_PORT_4500_NAT_TIMEOUT_UNSET](VcnGatewayConnectionConfig.md) Minimum NAT timeout not set. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VCN_GATEWAY_OPTION_ENABLE_DATA_STALL_RECOVERY_WITH_MOBILITY](VcnGatewayConnectionConfig.md) Perform mobility update to attempt recovery from suspected data stalls. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](VcnGatewayConnectionConfig.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getExposedCapabilities](VcnGatewayConnectionConfig.md))`()` Returns all exposed capabilities. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getGatewayConnectionName](VcnGatewayConnectionConfig.md))`()` Returns the configured Gateway Connection name. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxMtu](VcnGatewayConnectionConfig.md))`()` Retrieves the maximum MTU allowed for this Gateway Connection. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinUdpPort4500NatTimeoutSeconds](VcnGatewayConnectionConfig.md))`()` Retrieves the maximum supported IKEv2/IPsec NATT keepalive timeout. |
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html) | [getRetryIntervalsMillis](VcnGatewayConnectionConfig.md))`()` Retrieves the configured retry intervals. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [VcnUnderlyingNetworkTemplate](VcnUnderlyingNetworkTemplate.md)!\> | [getVcnUnderlyingNetworkPriorities](VcnGatewayConnectionConfig.md))`()` Retrieve the VcnUnderlyingNetworkTemplate list, or a default list if it is not configured. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasGatewayOption](VcnGatewayConnectionConfig.md))`(`option:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Checks if the given VCN gateway option is enabled. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](VcnGatewayConnectionConfig.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSafeModeEnabled](VcnGatewayConnectionConfig.md))`()` Check whether safe mode is enabled |

## Constants

### MIN_UDP_PORT_4500_NAT_TIMEOUT_UNSET

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIN_UDP_PORT_4500_NAT_TIMEOUT_UNSET: Int
```

Minimum NAT timeout not set.

When the timeout is not set, the device will automatically choose a keepalive interval and may reduce the keepalive frequency for power-optimization. 

 Value: -1

### VCN_GATEWAY_OPTION_ENABLE_DATA_STALL_RECOVERY_WITH_MOBILITY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VCN_GATEWAY_OPTION_ENABLE_DATA_STALL_RECOVERY_WITH_MOBILITY: Int
```

Perform mobility update to attempt recovery from suspected data stalls.

If set, the gateway connection will monitor the data stall detection of the VCN network. When there is a suspected data stall, the gateway connection will attempt recovery by performing a mobility update on the underlying IKE session. 

 Value: 0

## Public methods

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getExposedCapabilities

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExposedCapabilities(): IntArray
```

Returns all exposed capabilities.

The returned integer-value capabilities will not contain duplicates, and will be sorted in ascending numerical order.

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | This value cannot be`null`. |

**See Also**

- [android.net.vcn.VcnGatewayConnectionConfig.Builder#addExposedCapability(int)](../android/net/vcn/VcnGatewayConnectionConfig.Builder.md))
- [android.net.vcn.VcnGatewayConnectionConfig.Builder#removeExposedCapability(int)](../android/net/vcn/VcnGatewayConnectionConfig.Builder.md)) 

### getGatewayConnectionName

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGatewayConnectionName(): String
```

Returns the configured Gateway Connection name.

This name is used by the configuring apps to distinguish between VcnGatewayConnectionConfigs configured on a single [VcnConfig](VcnConfig.md). This will be used as the identifier in VcnStatusCallback invocations.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

**See Also**

- [android.net.vcn.VcnManager.VcnStatusCallback#onGatewayConnectionError](../android/net/vcn/VcnManager.VcnStatusCallback.md)) 

### getMaxMtu

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxMtu(): Int
```

Retrieves the maximum MTU allowed for this Gateway Connection.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is android.net.vcn.VcnGatewayConnectionConfig#MIN_MTU_V6 or greater |

**See Also**

- [android.net.vcn.VcnGatewayConnectionConfig.Builder#setMaxMtu(int)](../android/net/vcn/VcnGatewayConnectionConfig.Builder.md)) 

### getMinUdpPort4500NatTimeoutSeconds

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMinUdpPort4500NatTimeoutSeconds(): Int
```

Retrieves the maximum supported IKEv2/IPsec NATT keepalive timeout. 
**See Also**

- [android.net.vcn.VcnGatewayConnectionConfig.Builder#setMinUdpPort4500NatTimeoutSeconds(int)](../android/net/vcn/VcnGatewayConnectionConfig.Builder.md)) 

### getRetryIntervalsMillis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRetryIntervalsMillis(): LongArray
```

Retrieves the configured retry intervals.

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------|
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html) | This value cannot be`null`. |

**See Also**

- [android.net.vcn.VcnGatewayConnectionConfig.Builder#setRetryIntervalsMillis(long[])](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig.Builder#setRetryIntervalsMillis(kotlin.LongArray)) 

### getVcnUnderlyingNetworkPriorities

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVcnUnderlyingNetworkPriorities(): MutableList<VcnUnderlyingNetworkTemplate!>
```

Retrieve the VcnUnderlyingNetworkTemplate list, or a default list if it is not configured.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [VcnUnderlyingNetworkTemplate](VcnUnderlyingNetworkTemplate.md)!> | This value cannot be`null`. |

**See Also**

- [android.net.vcn.VcnGatewayConnectionConfig.Builder#setVcnUnderlyingNetworkPriorities(List)](../android/net/vcn/VcnGatewayConnectionConfig.Builder.md)) 

### hasGatewayOption

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasGatewayOption(option: Int): Boolean
```

Checks if the given VCN gateway option is enabled.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `option` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the option to check. Value is [android.net.vcn.VcnGatewayConnectionConfig#VCN_GATEWAY_OPTION_ENABLE_DATA_STALL_RECOVERY_WITH_MOBILITY](VcnGatewayConnectionConfig.md) |

| Exceptions ||
|--------------------------------------|------------------------------------|
| `java.lang.IllegalArgumentException` | if the provided option is invalid. |

**See Also**

- [android.net.vcn.VcnGatewayConnectionConfig.Builder#addGatewayOption(int)](../android/net/vcn/VcnGatewayConnectionConfig.Builder.md))
- [android.net.vcn.VcnGatewayConnectionConfig.Builder#removeGatewayOption(int)](../android/net/vcn/VcnGatewayConnectionConfig.Builder.md)) 

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isSafeModeEnabled

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSafeModeEnabled(): Boolean
```

Check whether safe mode is enabled 
**See Also**

- [android.net.vcn.VcnGatewayConnectionConfig.Builder#setSafeModeEnabled(boolean)](../android/net/vcn/VcnGatewayConnectionConfig.Builder.md))
