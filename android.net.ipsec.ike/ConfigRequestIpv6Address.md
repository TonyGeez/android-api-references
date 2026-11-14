# TunnelModeChildSessionParams.ConfigRequestIpv6Address

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConfigRequestIpv6Address

Kotlin| [Java](https://developer.android.com/reference/android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv6Address "View this page in Java") 

```
interface ConfigRequestIpv6Address : TunnelModeChildSessionParams.TunnelModeChildConfigRequest
```

| [android.net.ipsec.ike.TunnelModeChildSessionParams.ConfigRequestIpv6Address](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv6Address#) |

Represents an IPv6 Internal Address request

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Inet6Address](https://developer.android.com/reference/kotlin/java/net/Inet6Address.html#)? | [getAddress](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv6Address#getAddress())`()` Retrieves the requested internal IPv6 address |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPrefixLength](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv6Address#getPrefixLength())`()` Retrieves the prefix length |

## Public methods

### getAddress

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAddress(): Inet6Address?
```

Retrieves the requested internal IPv6 address

| Return ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Inet6Address](https://developer.android.com/reference/kotlin/java/net/Inet6Address.html#)? | The requested IPv6 address, or null if no specific internal address was requested |

### getPrefixLength

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrefixLength(): Int
```

Retrieves the prefix length

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The requested prefix length, or -1 if no specific IPv6 address was requested |
