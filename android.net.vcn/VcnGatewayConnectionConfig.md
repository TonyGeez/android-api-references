# VcnGatewayConnectionConfig

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VcnGatewayConnectionConfig

Kotlin| [Java](https://developer.android.com/reference/android/net/vcn/VcnGatewayConnectionConfig "View this page in Java") 
| --- | --- |

```
class VcnGatewayConnectionConfig
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.vcn.VcnGatewayConnectionConfig](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig#) |

This class represents a configuration for a connection to a Virtual Carrier Network gateway.

Each VcnGatewayConnectionConfig represents a single logical connection to a carrier gateway, and may provide one or more telephony services (as represented by network capabilities). Each gateway is expected to provide mobility for a given session as the device roams across [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#) s.

A VCN connection based on this configuration will be brought up dynamically based on device settings, and filed NetworkRequests. Underlying Networks must provide INTERNET connectivity, and must be part of the subscription group under which this configuration is registered (see [android.net.vcn.VcnManager#setVcnConfig](https://developer.android.com/reference/kotlin/android/net/vcn/VcnManager#setVcnConfig(android.os.ParcelUuid,%20android.net.vcn.VcnConfig))).

As an abstraction of a cellular network, services that can be provided by a VCN network are limited to services provided by cellular networks:

- [NetworkCapabilities.NET_CAPABILITY_MMS](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#NET_CAPABILITY_MMS:kotlin.Int)
- [NetworkCapabilities.NET_CAPABILITY_SUPL](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#NET_CAPABILITY_SUPL:kotlin.Int)
- [NetworkCapabilities.NET_CAPABILITY_DUN](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#NET_CAPABILITY_DUN:kotlin.Int)
- [NetworkCapabilities.NET_CAPABILITY_FOTA](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#NET_CAPABILITY_FOTA:kotlin.Int)
- [NetworkCapabilities.NET_CAPABILITY_IMS](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#NET_CAPABILITY_IMS:kotlin.Int)
- [NetworkCapabilities.NET_CAPABILITY_CBS](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#NET_CAPABILITY_CBS:kotlin.Int)
- [NetworkCapabilities.NET_CAPABILITY_IA](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#NET_CAPABILITY_IA:kotlin.Int)
- [NetworkCapabilities.NET_CAPABILITY_RCS](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#NET_CAPABILITY_RCS:kotlin.Int)
- [NetworkCapabilities.NET_CAPABILITY_XCAP](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#NET_CAPABILITY_XCAP:kotlin.Int)
- [NetworkCapabilities.NET_CAPABILITY_EIMS](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#NET_CAPABILITY_EIMS:kotlin.Int)
- [NetworkCapabilities.NET_CAPABILITY_INTERNET](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#NET_CAPABILITY_INTERNET:kotlin.Int)
- [NetworkCapabilities.NET_CAPABILITY_MCX](https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#NET_CAPABILITY_MCX:kotlin.Int)

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig.Builder) This class is used to incrementally build [VcnGatewayConnectionConfig](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig#) objects. |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIN_UDP_PORT_4500_NAT_TIMEOUT_UNSET](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig#MIN_UDP_PORT_4500_NAT_TIMEOUT_UNSET:kotlin.Int) Minimum NAT timeout not set. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VCN_GATEWAY_OPTION_ENABLE_DATA_STALL_RECOVERY_WITH_MOBILITY](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig#VCN_GATEWAY_OPTION_ENABLE_DATA_STALL_RECOVERY_WITH_MOBILITY:kotlin.Int) Perform mobility update to attempt recovery from suspected data stalls. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getExposedCapabilities](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig#getExposedCapabilities())`()` Returns all exposed capabilities. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getGatewayConnectionName](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig#getGatewayConnectionName())`()` Returns the configured Gateway Connection name. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxMtu](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig#getMaxMtu())`()` Retrieves the maximum MTU allowed for this Gateway Connection. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinUdpPort4500NatTimeoutSeconds](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig#getMinUdpPort4500NatTimeoutSeconds())`()` Retrieves the maximum supported IKEv2/IPsec NATT keepalive timeout. |
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html) | [getRetryIntervalsMillis](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig#getRetryIntervalsMillis())`()` Retrieves the configured retry intervals. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [VcnUnderlyingNetworkTemplate](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate)!\> | [getVcnUnderlyingNetworkPriorities](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig#getVcnUnderlyingNetworkPriorities())`()` Retrieve the VcnUnderlyingNetworkTemplate list, or a default list if it is not configured. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasGatewayOption](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig#hasGatewayOption(kotlin.Int))`(`option:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Checks if the given VCN gateway option is enabled. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig#hashCode())`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSafeModeEnabled](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig#isSafeModeEnabled())`()` Check whether safe mode is enabled |

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

- [android.net.vcn.VcnGatewayConnectionConfig.Builder#addExposedCapability(int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig.Builder#addExposedCapability(kotlin.Int))
- [android.net.vcn.VcnGatewayConnectionConfig.Builder#removeExposedCapability(int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig.Builder#removeExposedCapability(kotlin.Int)) 

### getGatewayConnectionName

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGatewayConnectionName(): String
```

Returns the configured Gateway Connection name.

This name is used by the configuring apps to distinguish between VcnGatewayConnectionConfigs configured on a single [VcnConfig](https://developer.android.com/reference/kotlin/android/net/vcn/VcnConfig). This will be used as the identifier in VcnStatusCallback invocations.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

**See Also**

- [android.net.vcn.VcnManager.VcnStatusCallback#onGatewayConnectionError](https://developer.android.com/reference/kotlin/android/net/vcn/VcnManager.VcnStatusCallback#onGatewayConnectionError(kotlin.String,%20kotlin.Int,%20kotlin.Throwable)) 

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

- [android.net.vcn.VcnGatewayConnectionConfig.Builder#setMaxMtu(int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig.Builder#setMaxMtu(kotlin.Int)) 

### getMinUdpPort4500NatTimeoutSeconds

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMinUdpPort4500NatTimeoutSeconds(): Int
```

Retrieves the maximum supported IKEv2/IPsec NATT keepalive timeout. 
**See Also**

- [android.net.vcn.VcnGatewayConnectionConfig.Builder#setMinUdpPort4500NatTimeoutSeconds(int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig.Builder#setMinUdpPort4500NatTimeoutSeconds(kotlin.Int)) 

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
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [VcnUnderlyingNetworkTemplate](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate)!> | This value cannot be`null`. |

**See Also**

- [android.net.vcn.VcnGatewayConnectionConfig.Builder#setVcnUnderlyingNetworkPriorities(List)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig.Builder#setVcnUnderlyingNetworkPriorities(kotlin.collections.MutableList)) 

### hasGatewayOption

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasGatewayOption(option: Int): Boolean
```

Checks if the given VCN gateway option is enabled.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `option` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the option to check. Value is [android.net.vcn.VcnGatewayConnectionConfig#VCN_GATEWAY_OPTION_ENABLE_DATA_STALL_RECOVERY_WITH_MOBILITY](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig#VCN_GATEWAY_OPTION_ENABLE_DATA_STALL_RECOVERY_WITH_MOBILITY:kotlin.Int) |

| Exceptions ||
|--------------------------------------|------------------------------------|
| `java.lang.IllegalArgumentException` | if the provided option is invalid. |

**See Also**

- [android.net.vcn.VcnGatewayConnectionConfig.Builder#addGatewayOption(int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig.Builder#addGatewayOption(kotlin.Int))
- [android.net.vcn.VcnGatewayConnectionConfig.Builder#removeGatewayOption(int)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig.Builder#removeGatewayOption(kotlin.Int)) 

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

- [android.net.vcn.VcnGatewayConnectionConfig.Builder#setSafeModeEnabled(boolean)](https://developer.android.com/reference/kotlin/android/net/vcn/VcnGatewayConnectionConfig.Builder#setSafeModeEnabled(kotlin.Boolean))
