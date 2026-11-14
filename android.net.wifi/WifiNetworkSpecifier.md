# WifiNetworkSpecifier

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiNetworkSpecifier

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/WifiNetworkSpecifier "View this page in Java") 

```
class WifiNetworkSpecifier : NetworkSpecifier, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.net.NetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier.html#) ||
| | ↳ | [android.net.wifi.WifiNetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier#) |

Network specifier object used to request a Wi-Fi network. Apps should use the [WifiNetworkSpecifier.Builder](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier.Builder) class to create an instance.

This specifier can be used to request a local-only connection on devices that support concurrent connections (indicated via [WifiManager.isStaConcurrencyForLocalOnlyConnectionsSupported()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager#isStaConcurrencyForLocalOnlyConnectionsSupported())and if the initiating app targets SDK ≥ [android.os.Build.VERSION_CODES#S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or is a system app. These local-only connections may be brought up as a secondary concurrent connection (primary connection will be used for networks with internet connectivity available to the user and all apps).

This specifier can also be used to listen for connected Wi-Fi networks on a particular band. Additionally, some devices may support requesting a connection to a particular band. If the device does not support such a request, it will send [NetworkCallback.onUnavailable()](https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.NetworkCallback.html#onUnavailable())upon request to the callback passed to [ConnectivityManager.requestNetwork(NetworkRequest, NetworkCallback)](https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#requestNetwork(android.net.NetworkRequest,%20android.net.ConnectivityManager.NetworkCallback))or equivalent. See [Builder.build()](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier.Builder#build())for details.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier.Builder) Builder used to create [WifiNetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier#) objects. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBand](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier#getBand())`()` The band for this Wi-Fi network specifier. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getPreferredChannelFrequenciesMhz](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier#getPreferredChannelFrequenciesMhz())`()` The preferred channels fot this network specifier. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [WifiNetworkSpecifier](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/net/wifi/WifiNetworkSpecifier#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.wifi.ScanResult#UNSPECIFIED](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#UNSPECIFIED:kotlin.Int), [android.net.wifi.ScanResult#WIFI_BAND_24_GHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_BAND_24_GHZ:kotlin.Int), [android.net.wifi.ScanResult#WIFI_BAND_5_GHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_BAND_5_GHZ:kotlin.Int), [android.net.wifi.ScanResult#WIFI_BAND_6_GHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_BAND_6_GHZ:kotlin.Int), or [android.net.wifi.ScanResult#WIFI_BAND_60_GHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_BAND_60_GHZ:kotlin.Int) |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<WifiNetworkSpecifier!>
```
