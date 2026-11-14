# TunnelModeChildSessionParams.ConfigRequestIpv4Address

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConfigRequestIpv4Address

Kotlin| [Java](../android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv4Address.md) 
| --- | --- |

```
interface ConfigRequestIpv4Address : TunnelModeChildSessionParams.TunnelModeChildConfigRequest
```

| [android.net.ipsec.ike.TunnelModeChildSessionParams.ConfigRequestIpv4Address](../android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv4Address.md) |

Represents an IPv4 Internal Address request

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Inet4Address](../java/net/Inet4Address.md)? | [getAddress](../android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv4Address.md))`()` Retrieves the requested internal IPv4 address |

## Public methods

### getAddress

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAddress(): Inet4Address?
```

Retrieves the requested internal IPv4 address

| Return ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Inet4Address](../java/net/Inet4Address.md)? | The requested IPv4 address, or null if no specific internal address was requested |
