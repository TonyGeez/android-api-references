Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiP2pConnectionInfo

```
class WifiP2pConnectionInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.p2p.WifiP2pConnectionInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConnectionInfo#) |

A class representing the connection capabilities of a Wi-Fi P2P link.

This class provides information about the physical layer (PHY) of the connection, including the Wi-Fi standard in use (e.g. 802.11ax), the channel width, and the number of transmit and receive spatial streams (NSS). This data can be used to understand the performance characteristics of the P2P connection.

An instance of this class can be obtained from `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pGroup` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice`.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConnectionInfo#UNSPECIFIED:kotlin.Int` Indicates that the value of a field is not specified. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConnectionInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConnectionInfo#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConnectionInfo#getChannelWidth()()` Gets the channel width of the current P2P connection. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConnectionInfo#getRxNss()()` Gets the maximum number of receive spatial streams (NSS) for the current P2P connection. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConnectionInfo#getTxNss()()` Gets the maximum number of transmit spatial streams (NSS) for the current P2P connection. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConnectionInfo#getWifiStandard()()` Gets the Wi-Fi standard of the current P2P connection. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConnectionInfo#hashCode()()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConnectionInfo#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConnectionInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(parcel: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [WifiP2pConnectionInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConnectionInfo#)!\> | `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConnectionInfo#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### UNSPECIFIED

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNSPECIFIED: Int
```

Indicates that the value of a field is not specified.

 Value: 0

## Public methods

### describeContents

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### getChannelWidth

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChannelWidth(): Int
```

Gets the channel width of the current P2P connection.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The channel width, as defined by the `CHANNEL_WIDTH_*` constants in `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_20MHZ:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_40MHZ:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_80MHZ:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_160MHZ:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_80MHZ_PLUS_MHZ:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#CHANNEL_WIDTH_320MHZ:kotlin.Int` |

### getRxNss

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRxNss(): Int
```

Gets the maximum number of receive spatial streams (NSS) for the current P2P connection.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The maximum number of spatial streams used for receiving data, or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConnectionInfo#UNSPECIFIED:kotlin.Int` if the value is not available. Value is between 0 and 4 inclusive |

### getTxNss

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTxNss(): Int
```

Gets the maximum number of transmit spatial streams (NSS) for the current P2P connection.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The maximum number of spatial streams used for transmitting data, or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConnectionInfo#UNSPECIFIED:kotlin.Int` if the value is not available. Value is between 0 and 4 inclusive |

### getWifiStandard

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getWifiStandard(): Int
```

Gets the Wi-Fi standard of the current P2P connection.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The Wi-Fi standard, as defined by the `WIFI_STANDARD_*` constants in `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#WIFI_STANDARD_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#WIFI_STANDARD_LEGACY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#WIFI_STANDARD_11N:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#WIFI_STANDARD_11AC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#WIFI_STANDARD_11AX:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#WIFI_STANDARD_11AD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult.html#WIFI_STANDARD_11BE:kotlin.Int` |

### hashCode

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |
| `parcel` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<WifiP2pConnectionInfo!>
```
