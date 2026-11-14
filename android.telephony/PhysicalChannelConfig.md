# PhysicalChannelConfig

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PhysicalChannelConfig

Kotlin| [Java](PhysicalChannelConfig.md) 
| --- | --- |

```
class PhysicalChannelConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.PhysicalChannelConfig](PhysicalChannelConfig.md) |

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BAND_UNKNOWN](PhysicalChannelConfig.md) The band is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CELL_BANDWIDTH_UNKNOWN](PhysicalChannelConfig.md) Cell bandwidth is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANNEL_NUMBER_UNKNOWN](PhysicalChannelConfig.md) Channel number is unknown. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONNECTION_PRIMARY_SERVING](PhysicalChannelConfig.md) UE has connection to cell for signalling and possibly data (3GPP 36.331, 25.331). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONNECTION_SECONDARY_SERVING](PhysicalChannelConfig.md) UE has connection to cell for data (3GPP 36.331, 25.331). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONNECTION_UNKNOWN](PhysicalChannelConfig.md) Connection status is unknown. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FREQUENCY_UNKNOWN](PhysicalChannelConfig.md) The frequency is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PHYSICAL_CELL_ID_MAXIMUM_VALUE](PhysicalChannelConfig.md) Physical Cell Id's maximum value is 1007. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PHYSICAL_CELL_ID_UNKNOWN](PhysicalChannelConfig.md) Physical Cell Id is unknown. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](PhysicalChannelConfig.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](PhysicalChannelConfig.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBand](PhysicalChannelConfig.md))`()` The valid bands are [AccessNetworkConstants.GeranBand](../android/telephony/AccessNetworkConstants.GeranBand.md), [AccessNetworkConstants.UtranBand](../android/telephony/AccessNetworkConstants.UtranBand.md), [AccessNetworkConstants.EutranBand](../android/telephony/AccessNetworkConstants.EutranBand.md) and [AccessNetworkConstants.NgranBands](../android/telephony/AccessNetworkConstants.NgranBands.md). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCellBandwidthDownlinkKhz](PhysicalChannelConfig.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCellBandwidthUplinkKhz](PhysicalChannelConfig.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConnectionStatus](PhysicalChannelConfig.md))`()` Gets the connection status of the cell. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDownlinkChannelNumber](PhysicalChannelConfig.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDownlinkFrequencyKhz](PhysicalChannelConfig.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNetworkType](PhysicalChannelConfig.md))`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPhysicalCellId](PhysicalChannelConfig.md))`()` The physical cell ID which differentiates cells using the same radio channel. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUplinkChannelNumber](PhysicalChannelConfig.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUplinkFrequencyKhz](PhysicalChannelConfig.md))`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](PhysicalChannelConfig.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](PhysicalChannelConfig.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](PhysicalChannelConfig.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PhysicalChannelConfig](PhysicalChannelConfig.md)!\> | [CREATOR](PhysicalChannelConfig.md) <br /> |

## Constants

### BAND_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BAND_UNKNOWN: Int
```

The band is unknown. 

 Value: 0

### CELL_BANDWIDTH_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CELL_BANDWIDTH_UNKNOWN: Int
```

Cell bandwidth is unknown. 

 Value: 0

### CHANNEL_NUMBER_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANNEL_NUMBER_UNKNOWN: Int
```

Channel number is unknown. 

 Value: 2147483647

### CONNECTION_PRIMARY_SERVING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONNECTION_PRIMARY_SERVING: Int
```

**Deprecated:** *Use [CellInfo.CONNECTION_PRIMARY_SERVING](CellInfo.md) instead.*

UE has connection to cell for signalling and possibly data (3GPP 36.331, 25.331). 

 Value: 1

### CONNECTION_SECONDARY_SERVING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONNECTION_SECONDARY_SERVING: Int
```

**Deprecated:** *Use [CellInfo.CONNECTION_SECONDARY_SERVING](CellInfo.md) instead.*

UE has connection to cell for data (3GPP 36.331, 25.331). 

 Value: 2

### CONNECTION_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONNECTION_UNKNOWN: Int
```

**Deprecated:** *Use [CellInfo.CONNECTION_UNKNOWN](CellInfo.md) instead.*

Connection status is unknown. 

 Value: -1

### FREQUENCY_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FREQUENCY_UNKNOWN: Int
```

The frequency is unknown. 

 Value: -1

### PHYSICAL_CELL_ID_MAXIMUM_VALUE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PHYSICAL_CELL_ID_MAXIMUM_VALUE: Int
```

Physical Cell Id's maximum value is 1007. 

 Value: 1007

### PHYSICAL_CELL_ID_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PHYSICAL_CELL_ID_UNKNOWN: Int
```

Physical Cell Id is unknown. 

 Value: -1

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

The valid bands are [AccessNetworkConstants.GeranBand](../android/telephony/AccessNetworkConstants.GeranBand.md), [AccessNetworkConstants.UtranBand](../android/telephony/AccessNetworkConstants.UtranBand.md), [AccessNetworkConstants.EutranBand](../android/telephony/AccessNetworkConstants.EutranBand.md) and [AccessNetworkConstants.NgranBands](../android/telephony/AccessNetworkConstants.NgranBands.md).

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the frequency band, [BAND_UNKNOWN](PhysicalChannelConfig.md) if unknown. Value is between 1 and 261 inclusive |

### getCellBandwidthDownlinkKhz

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCellBandwidthDownlinkKhz(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Downlink cell bandwidth in kHz, [CELL_BANDWIDTH_UNKNOWN](PhysicalChannelConfig.md) if unknown. Value is 1 or greater |

### getCellBandwidthUplinkKhz

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCellBandwidthUplinkKhz(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Uplink cell bandwidth in kHz, [CELL_BANDWIDTH_UNKNOWN](PhysicalChannelConfig.md) if unknown. Value is 1 or greater |

### getConnectionStatus

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnectionStatus(): Int
```

Gets the connection status of the cell.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Connection status of the cell, [CONNECTION_UNKNOWN](PhysicalChannelConfig.md) if unknown. Value is [android.telephony.PhysicalChannelConfig#CONNECTION_PRIMARY_SERVING](PhysicalChannelConfig.md), [android.telephony.PhysicalChannelConfig#CONNECTION_SECONDARY_SERVING](PhysicalChannelConfig.md), or [android.telephony.PhysicalChannelConfig#CONNECTION_UNKNOWN](PhysicalChannelConfig.md) |

**See Also**

- [#CONNECTION_PRIMARY_SERVING](PhysicalChannelConfig.md)
- [#CONNECTION_SECONDARY_SERVING](PhysicalChannelConfig.md)
- [#CONNECTION_UNKNOWN](PhysicalChannelConfig.md) 

### getDownlinkChannelNumber

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDownlinkChannelNumber(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Downlink Absolute Radio Frequency Channel Number, [CHANNEL_NUMBER_UNKNOWN](PhysicalChannelConfig.md) if unknown. Value is 0 or greater |

### getDownlinkFrequencyKhz

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDownlinkFrequencyKhz(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The downlink frequency in kHz, [FREQUENCY_UNKNOWN](PhysicalChannelConfig.md) if unknown. Value is 0 or greater |

### getNetworkType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNetworkType(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The network type for this physical channel, [TelephonyManager.NETWORK_TYPE_UNKNOWN](TelephonyManager.md) if unknown. Value is [android.telephony.TelephonyManager#NETWORK_TYPE_UNKNOWN](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_GPRS](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_EDGE](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_UMTS](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_CDMA](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_EVDO_0](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_EVDO_A](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_1xRTT](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_HSDPA](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_HSUPA](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_HSPA](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_IDEN](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_EVDO_B](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_LTE](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_EHRPD](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_HSPAP](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_GSM](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_TD_SCDMA](TelephonyManager.md), [android.telephony.TelephonyManager#NETWORK_TYPE_IWLAN](TelephonyManager.md), or [android.telephony.TelephonyManager#NETWORK_TYPE_NR](TelephonyManager.md) |

### getPhysicalCellId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPhysicalCellId(): Int
```

The physical cell ID which differentiates cells using the same radio channel. In GERAN, this value is the BSIC. The range is \[0-63\]. Reference: 3GPP TS 3.03 section 4.2.2. In UTRAN, this value is primary scrambling code. The range is \[0, 511\]. Reference: 3GPP TS 25.213 section 5.2.2. In EUTRAN, this value is physical layer cell identity. The range is \[0, 503\]. Reference: 3GPP TS 36.211 section 6.11. In 5G RAN, this value is physical layer cell identity. The range is \[0, 1007\]. Reference: 3GPP TS 38.211 section 7.4.2.1.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the physical cell identifier for this cell, [PHYSICAL_CELL_ID_UNKNOWN](PhysicalChannelConfig.md) if [android.telephony.CellInfo#UNAVAILABLE](CellInfo.md). Value is between 0 and 1007 inclusive |

### getUplinkChannelNumber

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUplinkChannelNumber(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Uplink Absolute Radio Frequency Channel Number, [CHANNEL_NUMBER_UNKNOWN](PhysicalChannelConfig.md) if unknown. Value is 0 or greater |

### getUplinkFrequencyKhz

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUplinkFrequencyKhz(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The uplink frequency in kHz, [FREQUENCY_UNKNOWN](PhysicalChannelConfig.md) if unknown. Value is 0 or greater |

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<PhysicalChannelConfig!>
```
