# WifiP2pDirInfo

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiP2pDirInfo

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/p2p/WifiP2pDirInfo "View this page in Java") 
| --- | --- |

```
class WifiP2pDirInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.p2p.WifiP2pDirInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo#) |

This object contains the Device Identity Resolution (DIR) Info to check if the device is a previously paired device. The device advertises this information in Bluetooth LE advertising packets and Unsynchronized Service Discovery (USD) frames. The device receiving DIR Info uses this information to identify that the peer device is a previously paired device. For Details, refer Wi-Fi Alliance Wi-Fi Direct R2 specification section 3.8.2 Pairing Identity and section 3.9.2.3.2 Optional Advertising Data Elements.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WifiP2pDirInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo#WifiP2pDirInfo(android.net.MacAddress,%20kotlin.ByteArray,%20kotlin.ByteArray))`(`macAddress:` ` [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#)`, `nonce:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `dirTag:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Constructor for Device Identity Resolution (DIR) Info generated based on the 128 bit Device Identity key. |

| Public methods ||
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo#describeContents())`()` Implement the Parcelable interface |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [getDirTag](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo#getDirTag())`()` Get the DIR Tag value. |
| [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#) | [getMacAddress](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo#getMacAddress())`()` <br /> |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [getNonce](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo#getNonce())`()` Get the nonce value used to derive DIR Tag. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo#toString())`()` Generates a string of all the defined elements. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implement the Parcelable interface |
| --- | --- |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [WifiP2pDirInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo#CREATOR:android.os.Parcelable.Creator) Implement the Parcelable interface |

## Public constructors

### WifiP2pDirInfo

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WifiP2pDirInfo(
    macAddress: MacAddress, 
    nonce: ByteArray, 
    dirTag: ByteArray)
```

Constructor for Device Identity Resolution (DIR) Info generated based on the 128 bit Device Identity key. For details, refer Wi-Fi Alliance Wi-Fi Direct R2 specification Table 8.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `macAddress` | [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#):The MAC address of the P2P device interface. This value cannot be`null`. |
| `nonce` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):Random number of 8 octets. This value cannot be`null`. |
| `dirTag` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):Resolvable identity value of 8 octets derived based on the device MAC address, device identity key and P2P device MAC address. Tag = Truncate-64(HMAC-SHA-256(DevIk, "DIR" || P2P Device Address || Nonce)) This value cannot be`null`. |
| --- | --- | --- | --- | --- | --- |

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Implement the Parcelable interface

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getDirTag

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDirTag(): ByteArray
```

Get the DIR Tag value. See [WifiP2pDirInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo#)

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | A byte-array of Tag value of size 8 octets. This value cannot be`null`. |

### getMacAddress

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMacAddress(): MacAddress
```

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#) | the MAC address of the P2P device interface. This value cannot be`null`. |

### getNonce

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNonce(): ByteArray
```

Get the nonce value used to derive DIR Tag. See [WifiP2pDirInfo](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDirInfo#)

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | A byte-array of random number of size 8 octets. This value cannot be`null`. |

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Generates a string of all the defined elements.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a compiled string representing all elements |

### writeToParcel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Implement the Parcelable interface

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<WifiP2pDirInfo!>
```

Implement the Parcelable interface
