# TunnelModeChildSessionParams.ConfigRequestIpv4Address

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConfigRequestIpv4Address

Kotlin| [Java](https://developer.android.com/reference/android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv4Address "View this page in Java") 
| --- | --- |

```
interface ConfigRequestIpv4Address : TunnelModeChildSessionParams.TunnelModeChildConfigRequest
```

| [android.net.ipsec.ike.TunnelModeChildSessionParams.ConfigRequestIpv4Address](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv4Address#) |

Represents an IPv4 Internal Address request

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Inet4Address](https://developer.android.com/reference/kotlin/java/net/Inet4Address.html#)? | [getAddress](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv4Address#getAddress())`()` Retrieves the requested internal IPv4 address |

## Public methods

### getAddress

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAddress(): Inet4Address?
```

Retrieves the requested internal IPv4 address

| Return ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Inet4Address](https://developer.android.com/reference/kotlin/java/net/Inet4Address.html#)? | The requested IPv4 address, or null if no specific internal address was requested |
