# WifiNetworkSpecifier

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiNetworkSpecifier

Kotlin| [Java](WifiNetworkSpecifier.md) 
| --- | --- |

```
class WifiNetworkSpecifier : NetworkSpecifier, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.net.NetworkSpecifier](../android.net/NetworkSpecifier.md) ||
| | ↳ | [android.net.wifi.WifiNetworkSpecifier](WifiNetworkSpecifier.md) |

Network specifier object used to request a Wi-Fi network. Apps should use the [WifiNetworkSpecifier.Builder](../android/net/wifi/WifiNetworkSpecifier.Builder.md) class to create an instance.

This specifier can be used to request a local-only connection on devices that support concurrent connections (indicated via [WifiManager.isStaConcurrencyForLocalOnlyConnectionsSupported()](WifiManager.md))and if the initiating app targets SDK ≥ [android.os.Build.VERSION_CODES#S](../android/os/Build.VERSION_CODES.md) or is a system app. These local-only connections may be brought up as a secondary concurrent connection (primary connection will be used for networks with internet connectivity available to the user and all apps).

This specifier can also be used to listen for connected Wi-Fi networks on a particular band. Additionally, some devices may support requesting a connection to a particular band. If the device does not support such a request, it will send [NetworkCallback.onUnavailable()](../android/net/ConnectivityManager.NetworkCallback.md))upon request to the callback passed to [ConnectivityManager.requestNetwork(NetworkRequest, NetworkCallback)](../android.net/ConnectivityManager.md))or equivalent. See [Builder.build()](../android/net/wifi/WifiNetworkSpecifier.Builder.md))for details.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/net/wifi/WifiNetworkSpecifier.Builder.md) Builder used to create [WifiNetworkSpecifier](WifiNetworkSpecifier.md) objects. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](WifiNetworkSpecifier.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](WifiNetworkSpecifier.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBand](WifiNetworkSpecifier.md))`()` The band for this Wi-Fi network specifier. |
| --- | --- |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getPreferredChannelFrequenciesMhz](WifiNetworkSpecifier.md))`()` The preferred channels fot this network specifier. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](WifiNetworkSpecifier.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](WifiNetworkSpecifier.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](WifiNetworkSpecifier.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [WifiNetworkSpecifier](WifiNetworkSpecifier.md)!\> | [CREATOR](WifiNetworkSpecifier.md) <br /> |

## Public methods

### describeContents

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### equals

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getBand

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBand(): Int
```

The band for this Wi-Fi network specifier.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.wifi.ScanResult#UNSPECIFIED](ScanResult.md), [android.net.wifi.ScanResult#WIFI_BAND_24_GHZ](ScanResult.md), [android.net.wifi.ScanResult#WIFI_BAND_5_GHZ](ScanResult.md), [android.net.wifi.ScanResult#WIFI_BAND_6_GHZ](ScanResult.md), or [android.net.wifi.ScanResult#WIFI_BAND_60_GHZ](ScanResult.md) |

### getPreferredChannelFrequenciesMhz

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPreferredChannelFrequenciesMhz(): IntArray
```

The preferred channels fot this network specifier.

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | This value cannot be`null`. |

**See Also**

- [android.net.wifi.WifiNetworkSpecifier.Builder#setPreferredChannelsFrequenciesMhz(int[])](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier.Builder#setPreferredChannelsFrequenciesMhz(kotlin.IntArray)) 

### hashCode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<WifiNetworkSpecifier!>
```
