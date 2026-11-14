Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TunnelModeChildSessionParams

Kotlin | [Java](../android/net/ipsec/ike/TunnelModeChildSessionParams.md)
| --- | --- |

```
class TunnelModeChildSessionParams : ChildSessionParams
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.net.ipsec.ike.ChildSessionParams](../android/net/ipsec/ike/ChildSessionParams.md) ||
| | ↳ | [android.net.ipsec.ike.TunnelModeChildSessionParams](../android/net/ipsec/ike/TunnelModeChildSessionParams.md) |

TunnelModeChildSessionParams represents proposed configurations for negotiating a tunnel mode Child Session.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.Builder` This class can be used to incrementally construct a `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams#`. |
| abstract | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv4Address` Represents an IPv4 Internal Address request |
| abstract | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv4DhcpServer` Represents an IPv4 DHCP server request |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv4DnsServer` Represents an IPv4 DNS Server request |
| abstract | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv4Netmask` Represents an IPv4 Netmask request |
| abstract | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv6Address` Represents an IPv6 Internal Address request |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.ConfigRequestIpv6DnsServer` Represents an IPv6 DNS Server request |
| abstract | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.TunnelModeChildConfigRequest` Represents a tunnel mode child session configuration request type |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [TunnelModeChildSessionParams.TunnelModeChildConfigRequest](../android/net/ipsec/ike/TunnelModeChildSessionParams.TunnelModeChildConfigRequest.md)!\> | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams#getConfigurationRequests()()` Retrieves the list of Configuration Requests |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams#hashCode()()` Returns a hash code value for the object. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionParams` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSaProposal!>` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionParams#getChildSaProposals()()` Retrieves all ChildSaProposals configured <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionParams#getHardLifetimeSeconds()()` Retrieves hard lifetime in seconds <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeTrafficSelector!>` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionParams#getInboundTrafficSelectors()()` Retrieves configured inbound traffic selectors @see `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.Builder#addInboundTrafficSelectors(android.net.ipsec.ike.IkeTrafficSelector)` or `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TransportModeChildSessionParams.Builder#addInboundTrafficSelectors(android.net.ipsec.ike.IkeTrafficSelector)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeTrafficSelector!>` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionParams#getOutboundTrafficSelectors()()` Retrieves configured outbound traffic selectors @see `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.Builder#addOutboundTrafficSelectors(android.net.ipsec.ike.IkeTrafficSelector)` or `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TransportModeChildSessionParams.Builder#addOutboundTrafficSelectors(android.net.ipsec.ike.IkeTrafficSelector)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionParams#getSoftLifetimeSeconds()()` Retrieves soft lifetime in seconds <br /> | ||

## Public methods

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getConfigurationRequests

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConfigurationRequests(): MutableList<TunnelModeChildSessionParams.TunnelModeChildConfigRequest!>
```

Retrieves the list of Configuration Requests

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/ipsec/ike/TunnelModeChildSessionParams.TunnelModeChildConfigRequest!>` | This value cannot be `null`. |

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |
