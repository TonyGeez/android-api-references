# MloLink

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MloLink

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/MloLink "View this page in Java") 
| --- | --- |

```
class MloLink : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.MloLink](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#) |

Data structure class representing a Wi-Fi Multi-Link Operation (MLO) link This is only used by 802.11be capable devices

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVALID_MLO_LINK_ID](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#INVALID_MLO_LINK_ID:kotlin.Int) Invalid link id. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MLO_LINK_STATE_ACTIVE](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#MLO_LINK_STATE_ACTIVE:kotlin.Int) MLO link state: Link is associated to the access point and mapped to at least one traffic stream. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MLO_LINK_STATE_IDLE](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#MLO_LINK_STATE_IDLE:kotlin.Int) MLO link state: Link is associated to the access point but not mapped to any traffic stream. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MLO_LINK_STATE_INVALID](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#MLO_LINK_STATE_INVALID:kotlin.Int) MLO link state: Invalid link state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MLO_LINK_STATE_UNASSOCIATED](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#MLO_LINK_STATE_UNASSOCIATED:kotlin.Int) MLO link state: Link is not associated with the access point. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------|---|
| [MloLink](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#MloLink())`()` Constructor for a MloLInk. |

| Public methods ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#describeContents())`()` Implement the Parcelable interface |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#)? | [getApMacAddress](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#getApMacAddress())`()` Returns the AP MAC address of this link. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBand](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#getBand())`()` Returns the Wi-Fi band of this link. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChannel](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#getChannel())`()` Returns the channel number of this link. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLinkId](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#getLinkId())`()` Returns the link id of this link. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRssi](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#getRssi())`()` Returns the RSSI of the link. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRxLinkSpeedMbps](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#getRxLinkSpeedMbps())`()` Returns the current receive link speed in Mbps. |
| [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#)? | [getStaMacAddress](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#getStaMacAddress())`()` Returns the STA MAC address of this link. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getState](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#getState())`()` Returns the state of this link as one of: [MLO_LINK_STATE_INVALID](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#MLO_LINK_STATE_INVALID:kotlin.Int) [MLO_LINK_STATE_UNASSOCIATED](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#MLO_LINK_STATE_UNASSOCIATED:kotlin.Int) [MLO_LINK_STATE_IDLE](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#MLO_LINK_STATE_IDLE:kotlin.Int) [MLO_LINK_STATE_ACTIVE](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#MLO_LINK_STATE_ACTIVE:kotlin.Int) |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTxLinkSpeedMbps](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#getTxLinkSpeedMbps())`()` Returns the current transmit link speed in Mbps. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#hashCode())`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implement the Parcelable interface |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [MloLink](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#CREATOR:android.os.Parcelable.Creator) Implement the Parcelable interface |

## Constants

### INVALID_MLO_LINK_ID

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID_MLO_LINK_ID: Int
```

Invalid link id. Used in {link #getLinkId()} 

 Value: -1

### MLO_LINK_STATE_ACTIVE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MLO_LINK_STATE_ACTIVE: Int
```

MLO link state: Link is associated to the access point and mapped to at least one traffic stream. {link #getState()} Note that an MLO link could be in that state but in power save mode. 

 Value: 3

### MLO_LINK_STATE_IDLE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MLO_LINK_STATE_IDLE: Int
```

MLO link state: Link is associated to the access point but not mapped to any traffic stream. Used in {link #getState()} 

 Value: 2

### MLO_LINK_STATE_INVALID

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MLO_LINK_STATE_INVALID: Int
```

MLO link state: Invalid link state. Used in {link #getState()} 

 Value: 0

### MLO_LINK_STATE_UNASSOCIATED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MLO_LINK_STATE_UNASSOCIATED: Int
```

MLO link state: Link is not associated with the access point. Used in {link #getState()} 

 Value: 1

## Public constructors

### MloLink

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MloLink()
```

Constructor for a MloLInk.

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Implement the Parcelable interface

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getApMacAddress

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getApMacAddress(): MacAddress?
```

Returns the AP MAC address of this link.

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#)? | AP MAC address for this link or null when the caller has insufficient permissions to access the access point MAC Address. |

### getBand

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBand(): Int
```

Returns the Wi-Fi band of this link.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.wifi.ScanResult#UNSPECIFIED](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#UNSPECIFIED:kotlin.Int), [android.net.wifi.ScanResult#WIFI_BAND_24_GHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_BAND_24_GHZ:kotlin.Int), [android.net.wifi.ScanResult#WIFI_BAND_5_GHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_BAND_5_GHZ:kotlin.Int), [android.net.wifi.ScanResult#WIFI_BAND_6_GHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_BAND_6_GHZ:kotlin.Int), or [android.net.wifi.ScanResult#WIFI_BAND_60_GHZ](https://developer.android.com/reference/kotlin/android/net/wifi/ScanResult#WIFI_BAND_60_GHZ:kotlin.Int) |

### getChannel

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getChannel(): Int
```

Returns the channel number of this link. A valid value is based on the 802.11 specification in sections 19.3.15 and 27.3.23

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 1 or greater |

### getLinkId

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLinkId(): Int
```

Returns the link id of this link. Valid values are 0-15, as described in IEEE 802.11be Specification, section 9.4.2.295b.2.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVALID_MLO_LINK_ID](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#INVALID_MLO_LINK_ID:kotlin.Int) or a valid value (0-15). Value is between [android.net.wifi.MloLink#INVALID_MLO_LINK_ID](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#INVALID_MLO_LINK_ID:kotlin.Int) and android.net.wifi.MloLink#MAX_MLO_LINK_ID inclusive |

### getRssi

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRssi(): Int
```

Returns the RSSI of the link.

Use android.net.wifi.WifiManager#calculateSignalLevel to convert this number into an absolute signal level which can be displayed to a user.

| Return ||
|----------------------------------------------------------------------------|--------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | RSSI in dBM. |

### getRxLinkSpeedMbps

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRxLinkSpeedMbps(): Int
```

Returns the current receive link speed in Mbps.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the Rx link speed or [WifiInfo.LINK_SPEED_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#LINK_SPEED_UNKNOWN:kotlin.Int) if link speed is unknown. Value is -1 or greater |

**See Also**

- [android.net.wifi.WifiInfo#LINK_SPEED_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#LINK_SPEED_UNKNOWN:kotlin.Int) 

### getStaMacAddress

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStaMacAddress(): MacAddress?
```

Returns the STA MAC address of this link.

| Return ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#)? | STA MAC address assigned for this link, or null in the following cases: - The caller has insufficient permissions to access the STA MAC Address - Link is not associated, hence no MAC address is assigned to it by STA |

### getState

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getState(): Int
```

Returns the state of this link as one of: [MLO_LINK_STATE_INVALID](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#MLO_LINK_STATE_INVALID:kotlin.Int) [MLO_LINK_STATE_UNASSOCIATED](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#MLO_LINK_STATE_UNASSOCIATED:kotlin.Int) [MLO_LINK_STATE_IDLE](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#MLO_LINK_STATE_IDLE:kotlin.Int) [MLO_LINK_STATE_ACTIVE](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#MLO_LINK_STATE_ACTIVE:kotlin.Int)

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.net.wifi.MloLink#MLO_LINK_STATE_INVALID](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#MLO_LINK_STATE_INVALID:kotlin.Int), [android.net.wifi.MloLink#MLO_LINK_STATE_UNASSOCIATED](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#MLO_LINK_STATE_UNASSOCIATED:kotlin.Int), [android.net.wifi.MloLink#MLO_LINK_STATE_IDLE](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#MLO_LINK_STATE_IDLE:kotlin.Int), or [android.net.wifi.MloLink#MLO_LINK_STATE_ACTIVE](https://developer.android.com/reference/kotlin/android/net/wifi/MloLink#MLO_LINK_STATE_ACTIVE:kotlin.Int) |

### getTxLinkSpeedMbps

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTxLinkSpeedMbps(): Int
```

Returns the current transmit link speed in Mbps.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the Tx link speed or [WifiInfo.LINK_SPEED_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#LINK_SPEED_UNKNOWN:kotlin.Int) if link speed is unknown. Value is -1 or greater |

**See Also**

- [android.net.wifi.WifiInfo#LINK_SPEED_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/WifiInfo#LINK_SPEED_UNKNOWN:kotlin.Int) 

### hashCode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<MloLink!>
```

Implement the Parcelable interface
