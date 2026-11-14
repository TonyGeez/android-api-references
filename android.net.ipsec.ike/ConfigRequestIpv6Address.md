# TunnelModeChildSessionParams.ConfigRequestIpv6Address

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConfigRequestIpv6Address

Kotlin| [Java](../android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv6Address.md) 
| --- | --- |

```
interface ConfigRequestIpv6Address : TunnelModeChildSessionParams.TunnelModeChildConfigRequest
```

| [android.net.ipsec.ike.TunnelModeChildSessionParams.ConfigRequestIpv6Address](../android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv6Address.md) |

Represents an IPv6 Internal Address request

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Inet6Address](../java.net/Inet6Address.md)? | [getAddress](../android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv6Address.md))`()` Retrieves the requested internal IPv6 address |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPrefixLength](../android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv6Address.md))`()` Retrieves the prefix length |

## Public methods

### getAddress

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAddress(): Inet6Address?
```

Retrieves the requested internal IPv6 address

| Return ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Inet6Address](../java.net/Inet6Address.md)? | The requested IPv6 address, or null if no specific internal address was requested |

### getPrefixLength

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrefixLength(): Int
```

Retrieves the prefix length

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The requested prefix length, or -1 if no specific IPv6 address was requested |
