# InterfaceAddress

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InterfaceAddress

```
open class InterfaceAddress
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.net.InterfaceAddress](InterfaceAddress.md) |

This class represents a Network Interface address. In short it's an IP address, a subnet mask and a broadcast address when the address is an IPv4 one. An IP address and a network prefix length in the case of IPv6 address.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](InterfaceAddress.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this object against the specified object. |
| open [InetAddress](InetAddress.md)! | [getAddress](InterfaceAddress.md))`()` Returns an`InetAddress`for this address. |
| open [InetAddress](InetAddress.md)! | [getBroadcast](InterfaceAddress.md))`()` Returns an`InetAddress`for the broadcast address for this InterfaceAddress. |
| --- | --- |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getNetworkPrefixLength](InterfaceAddress.md))`()` Returns the network prefix length for this address. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](InterfaceAddress.md))`()` Returns a hashcode for this Interface address. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](InterfaceAddress.md))`()` Converts this Interface address to a`String`. |
| --- | --- |

## Public methods

### equals

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares this object against the specified object. The result is`true`if and only if the argument is not`null`and it represents the same interface address as this object.

Two instances of`InterfaceAddress`represent the same address if the InetAddress, the prefix length and the broadcast are the same for both.

| Parameters ||
|-------|--------------------------------|
| `obj` | the object to compare against. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the objects are the same;`false`otherwise. |

**See Also**

- [java.net.InterfaceAddress#hashCode()](InterfaceAddress.md)) 

### getAddress

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAddress(): InetAddress!
```

Returns an`InetAddress`for this address.

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------------|
| [InetAddress](InetAddress.md)! | the`InetAddress`for this address. |

### getBroadcast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBroadcast(): InetAddress!
```

Returns an`InetAddress`for the broadcast address for this InterfaceAddress.

Only IPv4 networks have broadcast address therefore, in the case of an IPv6 network,`null`will be returned.

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [InetAddress](InetAddress.md)! | the`InetAddress`representing the broadcast address or`null`if there is no broadcast address. |

### getNetworkPrefixLength

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNetworkPrefixLength(): Short
```

Returns the network prefix length for this address. This is also known as the subnet mask in the context of IPv4 addresses. Typical IPv4 values would be 8 (255.0.0.0), 16 (255.255.0.0) or 24 (255.255.255.0).

Typical IPv6 values would be 128 (::1/128) or 10 (fe80::203:baff:fe27:1243/10)

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | a`short`representing the prefix length for the subnet of that address. |

### hashCode

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns a hashcode for this Interface address.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this Interface address. |

### toString

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Converts this Interface address to a`String`. The string returned is of the form: InetAddress / prefix length \[ broadcast address \].

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this Interface address. |
