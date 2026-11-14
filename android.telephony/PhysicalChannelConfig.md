# PhysicalChannelConfig

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PhysicalChannelConfig

Kotlin| [Java](https://developer.android.com/reference/android/telephony/PhysicalChannelConfig "View this page in Java") 

```
class PhysicalChannelConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.PhysicalChannelConfig](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#) |

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BAND_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#BAND_UNKNOWN:kotlin.Int) The band is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CELL_BANDWIDTH_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#CELL_BANDWIDTH_UNKNOWN:kotlin.Int) Cell bandwidth is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANNEL_NUMBER_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#CHANNEL_NUMBER_UNKNOWN:kotlin.Int) Channel number is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONNECTION_PRIMARY_SERVING](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#CONNECTION_PRIMARY_SERVING:kotlin.Int) UE has connection to cell for signalling and possibly data (3GPP 36.331, 25.331). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONNECTION_SECONDARY_SERVING](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#CONNECTION_SECONDARY_SERVING:kotlin.Int) UE has connection to cell for data (3GPP 36.331, 25.331). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONNECTION_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#CONNECTION_UNKNOWN:kotlin.Int) Connection status is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FREQUENCY_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#FREQUENCY_UNKNOWN:kotlin.Int) The frequency is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PHYSICAL_CELL_ID_MAXIMUM_VALUE](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#PHYSICAL_CELL_ID_MAXIMUM_VALUE:kotlin.Int) Physical Cell Id's maximum value is 1007. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PHYSICAL_CELL_ID_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#PHYSICAL_CELL_ID_UNKNOWN:kotlin.Int) Physical Cell Id is unknown. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBand](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#getBand())`()` The valid bands are [AccessNetworkConstants.GeranBand](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.GeranBand), [AccessNetworkConstants.UtranBand](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.UtranBand), [AccessNetworkConstants.EutranBand](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.EutranBand) and [AccessNetworkConstants.NgranBands](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCellBandwidthDownlinkKhz](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#getCellBandwidthDownlinkKhz())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCellBandwidthUplinkKhz](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#getCellBandwidthUplinkKhz())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConnectionStatus](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#getConnectionStatus())`()` Gets the connection status of the cell. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDownlinkChannelNumber](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#getDownlinkChannelNumber())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDownlinkFrequencyKhz](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#getDownlinkFrequencyKhz())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNetworkType](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#getNetworkType())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPhysicalCellId](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#getPhysicalCellId())`()` The physical cell ID which differentiates cells using the same radio channel. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUplinkChannelNumber](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#getUplinkChannelNumber())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUplinkFrequencyKhz](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#getUplinkFrequencyKhz())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [PhysicalChannelConfig](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#CREATOR:android.os.Parcelable.Creator) <br /> |

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

**Deprecated:** *Use [CellInfo.CONNECTION_PRIMARY_SERVING](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#CONNECTION_PRIMARY_SERVING:kotlin.Int) instead.*

UE has connection to cell for signalling and possibly data (3GPP 36.331, 25.331). 

 Value: 1

### CONNECTION_SECONDARY_SERVING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONNECTION_SECONDARY_SERVING: Int
```

**Deprecated:** *Use [CellInfo.CONNECTION_SECONDARY_SERVING](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#CONNECTION_SECONDARY_SERVING:kotlin.Int) instead.*

UE has connection to cell for data (3GPP 36.331, 25.331). 

 Value: 2

### CONNECTION_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONNECTION_UNKNOWN: Int
```

**Deprecated:** *Use [CellInfo.CONNECTION_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#CONNECTION_UNKNOWN:kotlin.Int) instead.*

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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

The valid bands are [AccessNetworkConstants.GeranBand](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.GeranBand), [AccessNetworkConstants.UtranBand](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.UtranBand), [AccessNetworkConstants.EutranBand](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.EutranBand) and [AccessNetworkConstants.NgranBands](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands).

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the frequency band, [BAND_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#BAND_UNKNOWN:kotlin.Int) if unknown. Value is between 1 and 261 inclusive |

### getCellBandwidthDownlinkKhz

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCellBandwidthDownlinkKhz(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Downlink cell bandwidth in kHz, [CELL_BANDWIDTH_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#CELL_BANDWIDTH_UNKNOWN:kotlin.Int) if unknown. Value is 1 or greater |

### getCellBandwidthUplinkKhz

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCellBandwidthUplinkKhz(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Uplink cell bandwidth in kHz, [CELL_BANDWIDTH_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#CELL_BANDWIDTH_UNKNOWN:kotlin.Int) if unknown. Value is 1 or greater |

### getConnectionStatus

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnectionStatus(): Int
```

Gets the connection status of the cell.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Connection status of the cell, [CONNECTION_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#CONNECTION_UNKNOWN:kotlin.Int) if unknown. Value is [android.telephony.PhysicalChannelConfig#CONNECTION_PRIMARY_SERVING](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#CONNECTION_PRIMARY_SERVING:kotlin.Int), [android.telephony.PhysicalChannelConfig#CONNECTION_SECONDARY_SERVING](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#CONNECTION_SECONDARY_SERVING:kotlin.Int), or [android.telephony.PhysicalChannelConfig#CONNECTION_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#CONNECTION_UNKNOWN:kotlin.Int) |

**See Also**

- [#CONNECTION_PRIMARY_SERVING](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#CONNECTION_PRIMARY_SERVING:kotlin.Int)
- [#CONNECTION_SECONDARY_SERVING](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#CONNECTION_SECONDARY_SERVING:kotlin.Int)
- [#CONNECTION_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#CONNECTION_UNKNOWN:kotlin.Int) 

### getDownlinkChannelNumber

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDownlinkChannelNumber(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Downlink Absolute Radio Frequency Channel Number, [CHANNEL_NUMBER_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#CHANNEL_NUMBER_UNKNOWN:kotlin.Int) if unknown. Value is 0 or greater |

### getDownlinkFrequencyKhz

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDownlinkFrequencyKhz(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The downlink frequency in kHz, [FREQUENCY_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#FREQUENCY_UNKNOWN:kotlin.Int) if unknown. Value is 0 or greater |

### getNetworkType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNetworkType(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The network type for this physical channel, [TelephonyManager.NETWORK_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UNKNOWN:kotlin.Int) if unknown. Value is [android.telephony.TelephonyManager#NETWORK_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UNKNOWN:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_GPRS](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GPRS:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_EDGE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EDGE:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_UMTS](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UMTS:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_CDMA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_CDMA:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_EVDO_0](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_0:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_EVDO_A](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_A:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_1xRTT](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_1xRTT:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_HSDPA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSDPA:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_HSUPA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSUPA:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_HSPA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPA:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_IDEN](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_IDEN:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_EVDO_B](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_B:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_LTE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_LTE:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_EHRPD](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EHRPD:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_HSPAP](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPAP:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_GSM](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GSM:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_TD_SCDMA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_TD_SCDMA:kotlin.Int), [android.telephony.TelephonyManager#NETWORK_TYPE_IWLAN](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_IWLAN:kotlin.Int), or [android.telephony.TelephonyManager#NETWORK_TYPE_NR](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_NR:kotlin.Int) |

### getPhysicalCellId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPhysicalCellId(): Int
```

The physical cell ID which differentiates cells using the same radio channel. In GERAN, this value is the BSIC. The range is \[0-63\]. Reference: 3GPP TS 3.03 section 4.2.2. In UTRAN, this value is primary scrambling code. The range is \[0, 511\]. Reference: 3GPP TS 25.213 section 5.2.2. In EUTRAN, this value is physical layer cell identity. The range is \[0, 503\]. Reference: 3GPP TS 36.211 section 6.11. In 5G RAN, this value is physical layer cell identity. The range is \[0, 1007\]. Reference: 3GPP TS 38.211 section 7.4.2.1.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the physical cell identifier for this cell, [PHYSICAL_CELL_ID_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#PHYSICAL_CELL_ID_UNKNOWN:kotlin.Int) if [android.telephony.CellInfo#UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int). Value is between 0 and 1007 inclusive |

### getUplinkChannelNumber

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUplinkChannelNumber(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Uplink Absolute Radio Frequency Channel Number, [CHANNEL_NUMBER_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#CHANNEL_NUMBER_UNKNOWN:kotlin.Int) if unknown. Value is 0 or greater |

### getUplinkFrequencyKhz

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUplinkFrequencyKhz(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The uplink frequency in kHz, [FREQUENCY_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/PhysicalChannelConfig#FREQUENCY_UNKNOWN:kotlin.Int) if unknown. Value is 0 or greater |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<PhysicalChannelConfig!>
```
