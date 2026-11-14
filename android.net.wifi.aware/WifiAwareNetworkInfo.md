Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiAwareNetworkInfo

```
class WifiAwareNetworkInfo : Parcelable, TransportInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.aware.WifiAwareNetworkInfo](../android/net/wifi/aware/WifiAwareNetworkInfo.md) |

Wi-Fi Aware-specific network information. The information can be extracted from the `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#` of the network using `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#getTransportInfo()`. The `https://developer.android.com/reference/kotlin/android/net/NetworkCapabilities.html#` is provided by the connectivity service to apps, e.g. received through the `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback.html#onCapabilitiesChanged(android.net.Network,%20android.net.NetworkCapabilities)` callback.

The Wi-Fi Aware-specific network information include the peer's scoped link-local IPv6 address for the Wi-Fi Aware link, as well as (optionally) the port and transport protocol specified by the peer. The scoped link-local IPv6, port, and transport protocol can then be used to create a `https://developer.android.com/reference/kotlin/java/net/Socket.html#` connection to the peer.

Note: these are the peer's IPv6 and port information - not the local device's!

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkInfo#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [WifiAwareChannelInfo](../android/net/wifi/aware/WifiAwareChannelInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkInfo#getChannelInfoList()()` Get a list `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareChannelInfo` which is used by this Aware data-path |
| --- | --- |
| [Inet6Address](../java/net/Inet6Address.md)? | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkInfo#getPeerIpv6Addr()()` Get the scoped link-local IPv6 address of the Wi-Fi Aware peer (not of the local device!). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkInfo#getPort()()` Get the port number to be used to create a network connection to the Wi-Fi Aware peer. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkInfo#getTransportProtocol()()` Get the transport protocol to be used to communicate over a network connection to the Wi-Fi Aware peer. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkInfo#hashCode()()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkInfo#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [WifiAwareNetworkInfo](../android/net/wifi/aware/WifiAwareNetworkInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkInfo#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public methods

### describeContents

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### getChannelInfoList

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChannelInfoList(): MutableList<WifiAwareChannelInfo!>
```

Get a list `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareChannelInfo` which is used by this Aware data-path

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareChannelInfo!>` | A list of `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareChannelInfo` This value cannot be `null`. |

### getPeerIpv6Addr

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPeerIpv6Addr(): Inet6Address?
```

Get the scoped link-local IPv6 address of the Wi-Fi Aware peer (not of the local device!).

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/Inet6Address.html#?` | An IPv6 address. This value may be `null`. |

### getPort

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPort(): Int
```

Get the port number to be used to create a network connection to the Wi-Fi Aware peer. The port information is provided by the app running on the peer which requested the connection, using the `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkSpecifier.Builder#setPort(kotlin.Int)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A port number on the peer. A value of 0 indicates that no port was specified by the peer. |

### getTransportProtocol

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTransportProtocol(): Int
```

Get the transport protocol to be used to communicate over a network connection to the Wi-Fi Aware peer. The transport protocol is provided by the app running on the peer which requested the connection, using the `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareNetworkSpecifier.Builder#setTransportProtocol(kotlin.Int)`.

The transport protocol number is assigned by the Internet Assigned Numbers Authority (IANA) https://www.iana.org/assignments/protocol-numbers/protocol-numbers.xhtml.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A transport protocol id. A value of -1 indicates that no transport protocol was specified by the peer. |

### hashCode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### toString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android/os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<WifiAwareNetworkInfo!>
```
