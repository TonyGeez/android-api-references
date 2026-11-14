Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VcnWifiUnderlyingNetworkTemplate

Kotlin | [Java](https://developer.android.com/reference/android/net/vcn/VcnWifiUnderlyingNetworkTemplate "View this page in Java")
| --- | --- |

```
class VcnWifiUnderlyingNetworkTemplate : VcnUnderlyingNetworkTemplate
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.net.vcn.VcnUnderlyingNetworkTemplate](https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate) ||
| | ↳ | [android.net.vcn.VcnWifiUnderlyingNetworkTemplate](https://developer.android.com/reference/kotlin/android/net/vcn/VcnWifiUnderlyingNetworkTemplate#) |

This class represents a configuration for a network template class of underlying Carrier WiFi networks.

See `https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate`

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnWifiUnderlyingNetworkTemplate.Builder` This class is used to incrementally build VcnWifiUnderlyingNetworkTemplate objects. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_ANY:kotlin.Int` Used to configure the matching criteria of a network characteristic. This may include network capabilities, or cellular subscription information. Denotes that networks with or without the characteristic are both acceptable to match this template. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_FORBIDDEN:kotlin.Int` Used to configure the matching criteria of a network characteristic. This may include network capabilities, or cellular subscription information. Denotes that a network MUST NOT have the capability in order to match this template. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#MATCH_REQUIRED:kotlin.Int` Used to configure the matching criteria of a network characteristic. This may include network capabilities, or cellular subscription information. Denotes that a network MUST have the capability in order to match this template. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnWifiUnderlyingNetworkTemplate#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnWifiUnderlyingNetworkTemplate#getSsids()()` Retrieve the matching SSIDs, or an empty set if any SSID is acceptable. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnWifiUnderlyingNetworkTemplate#hashCode()()` Returns a hash code value for the object. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#getMetered()()` Return the matching criteria for metered networks. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#getMinEntryDownstreamBandwidthKbps()()` Returns the minimum entry downstream bandwidth allowed by this template. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#getMinEntryUpstreamBandwidthKbps()()` Returns the minimum entry upstream bandwidth allowed by this template. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#getMinExitDownstreamBandwidthKbps()()` Returns the minimum exit downstream bandwidth allowed by this template. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/net/vcn/VcnUnderlyingNetworkTemplate#getMinExitUpstreamBandwidthKbps()()` Returns the minimum exit upstream bandwidth allowed by this template. <br /> | ||

## Public methods

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getSsids

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSsids(): MutableSet<String!>
```

Retrieve the matching SSIDs, or an empty set if any SSID is acceptable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/net/vcn/VcnWifiUnderlyingNetworkTemplate.Builder#setSsids(kotlin.collections.MutableSet)`

### hashCode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
