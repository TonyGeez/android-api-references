Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeIpv6AddrIdentification

```
open class IkeIpv6AddrIdentification : IkeIdentification
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.net.ipsec.ike.IkeIdentification](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeIdentification) ||
| | ↳ | [android.net.ipsec.ike.IkeIpv6AddrIdentification](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeIpv6AddrIdentification#) |

IkeIpv6AddrIdentification represents an IKE entity identification based on IPv6 address.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeIpv6AddrIdentification#IkeIpv6AddrIdentification(java.net.Inet6Address)(address: https://developer.android.com/reference/kotlin/java/net/Inet6Address.html#)` Construct an instance of `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeIpv6AddrIdentification#` with an IPv6 address. |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeIpv6AddrIdentification#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeIpv6AddrIdentification#hashCode()()` Returns a hash code value for the object. |

| Properties ||
|---|---|
| [Inet6Address](https://developer.android.com/reference/kotlin/java/net/Inet6Address.html#) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeIpv6AddrIdentification#ipv6Address:java.net.Inet6Address` The IPv6 address. |

## Public constructors

### IkeIpv6AddrIdentification

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
IkeIpv6AddrIdentification(address: Inet6Address)
```

Construct an instance of `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeIpv6AddrIdentification#` with an IPv6 address.

| Parameters ||
|---|---|
| `address` | [Inet6Address](https://developer.android.com/reference/kotlin/java/net/Inet6Address.html#): the IPv6 address. This value cannot be `null`. |

## Public methods

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
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

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

## Properties

### ipv6Address

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
val ipv6Address: Inet6Address
```

The IPv6 address.
