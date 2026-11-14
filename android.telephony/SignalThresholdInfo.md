# SignalThresholdInfo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SignalThresholdInfo

Kotlin| [Java](https://developer.android.com/reference/android/telephony/SignalThresholdInfo "View this page in Java") 
| --- | --- |

```
class SignalThresholdInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.SignalThresholdInfo](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#) |

Defines the threshold value of the signal strength.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo.Builder) Builder class to create [SignalThresholdInfo](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#) objects. |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_MEASUREMENT_TYPE_ECNO](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_ECNO:kotlin.Int) The ratio between the received energy from the pilot signal CPICH per chip (Ec) to the noise density (No). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_MEASUREMENT_TYPE_RSCP](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_RSCP:kotlin.Int) Received Signal Code Power. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_MEASUREMENT_TYPE_RSRP](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_RSRP:kotlin.Int) Reference Signal Received Power. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_MEASUREMENT_TYPE_RSRQ](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_RSRQ:kotlin.Int) Reference Signal Received Quality Range: -34 dB to 3 dB; Used RAN: [AccessNetworkConstants.AccessNetworkType.EUTRAN](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#EUTRAN:kotlin.Int) Reference: 3GPP TS 36. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_MEASUREMENT_TYPE_RSSI](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_RSSI:kotlin.Int) Received Signal Strength Indication. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_MEASUREMENT_TYPE_RSSNR](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_RSSNR:kotlin.Int) Reference Signal Signal to Noise Ratio Range: -20 dB to 30 dB; Used RAN: [AccessNetworkConstants.AccessNetworkType.EUTRAN](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#EUTRAN:kotlin.Int) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_MEASUREMENT_TYPE_SSRSRP](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_SSRSRP:kotlin.Int) 5G SS reference signal received power. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_MEASUREMENT_TYPE_SSRSRQ](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_SSRSRQ:kotlin.Int) 5G SS reference signal received quality. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_MEASUREMENT_TYPE_SSSINR](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_SSSINR:kotlin.Int) 5G SS signal-to-noise and interference ratio. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_MEASUREMENT_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_UNKNOWN:kotlin.Int) Unknown signal measurement type. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHysteresisDb](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#getHysteresisDb())`()` Get measurement hysteresis db. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaximumNumberOfThresholdsAllowed](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#getMaximumNumberOfThresholdsAllowed())`()` Get the maximum number of threshold allowed in each SignalThresholdInfo. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumNumberOfThresholdsAllowed](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#getMinimumNumberOfThresholdsAllowed())`()` Get the minimum number of thresholds allowed in each SignalThresholdInfo. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRadioAccessNetworkType](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#getRadioAccessNetworkType())`()` Get the radio access network type. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSignalMeasurementType](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#getSignalMeasurementType())`()` Get the signal measurement type. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getThresholds](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#getThresholds())`()` Get the signal strength thresholds. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#hashCode())`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [SignalThresholdInfo](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### SIGNAL_MEASUREMENT_TYPE_ECNO

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNAL_MEASUREMENT_TYPE_ECNO: Int
```

The ratio between the received energy from the pilot signal CPICH per chip (Ec) to the noise density (No). Range: -24 dBm to 1 dBm. Used RAN: [AccessNetworkConstants.AccessNetworkType.UTRAN](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#UTRAN:kotlin.Int) Reference: 3GPP TS 25.215 5.1.5 

 Value: 9

### SIGNAL_MEASUREMENT_TYPE_RSCP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNAL_MEASUREMENT_TYPE_RSCP: Int
```

Received Signal Code Power. Range: -120 dBm to -25 dBm; Used RAN: [AccessNetworkConstants.AccessNetworkType.UTRAN](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#UTRAN:kotlin.Int) Reference: 3GPP TS 25.123, section 9.1.1.1 

 Value: 2

### SIGNAL_MEASUREMENT_TYPE_RSRP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNAL_MEASUREMENT_TYPE_RSRP: Int
```

Reference Signal Received Power. Range: -140 dBm to -44 dBm; Used RAN: [AccessNetworkConstants.AccessNetworkType.EUTRAN](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#EUTRAN:kotlin.Int) Reference: 3GPP TS 36.133 9.1.4 

 Value: 3

### SIGNAL_MEASUREMENT_TYPE_RSRQ

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNAL_MEASUREMENT_TYPE_RSRQ: Int
```

Reference Signal Received Quality Range: -34 dB to 3 dB; Used RAN: [AccessNetworkConstants.AccessNetworkType.EUTRAN](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#EUTRAN:kotlin.Int) Reference: 3GPP TS 36.133 9.1.7 

 Value: 4

### SIGNAL_MEASUREMENT_TYPE_RSSI

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNAL_MEASUREMENT_TYPE_RSSI: Int
```

Received Signal Strength Indication. Range: -113 dBm and -51 dBm Used RAN: [AccessNetworkConstants.AccessNetworkType.GERAN](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#GERAN:kotlin.Int), [AccessNetworkConstants.AccessNetworkType.CDMA2000](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#CDMA2000:kotlin.Int) Reference: 3GPP TS 27.007 section 8.5. 

 Value: 1

### SIGNAL_MEASUREMENT_TYPE_RSSNR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNAL_MEASUREMENT_TYPE_RSSNR: Int
```

Reference Signal Signal to Noise Ratio Range: -20 dB to 30 dB; Used RAN: [AccessNetworkConstants.AccessNetworkType.EUTRAN](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#EUTRAN:kotlin.Int) 

 Value: 5

### SIGNAL_MEASUREMENT_TYPE_SSRSRP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNAL_MEASUREMENT_TYPE_SSRSRP: Int
```

5G SS reference signal received power. Range: -140 dBm to -44 dBm. Used RAN: [AccessNetworkConstants.AccessNetworkType.NGRAN](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#NGRAN:kotlin.Int) Reference: 3GPP TS 38.215. 

 Value: 6

### SIGNAL_MEASUREMENT_TYPE_SSRSRQ

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNAL_MEASUREMENT_TYPE_SSRSRQ: Int
```

5G SS reference signal received quality. Range: -43 dB to 20 dB. Used RAN: [AccessNetworkConstants.AccessNetworkType.NGRAN](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#NGRAN:kotlin.Int) Reference: 3GPP TS 38.133 section 10.1.11.1. 

 Value: 7

### SIGNAL_MEASUREMENT_TYPE_SSSINR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNAL_MEASUREMENT_TYPE_SSSINR: Int
```

5G SS signal-to-noise and interference ratio. Range: -23 dB to 40 dB Used RAN: [AccessNetworkConstants.AccessNetworkType.NGRAN](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#NGRAN:kotlin.Int) Reference: 3GPP TS 38.215 section 5.1.\*, 3GPP TS 38.133 section 10.1.16.1. 

 Value: 8

### SIGNAL_MEASUREMENT_TYPE_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNAL_MEASUREMENT_TYPE_UNKNOWN: Int
```

Unknown signal measurement type. 

 Value: 0

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

### getHysteresisDb

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHysteresisDb(): Int
```

Get measurement hysteresis db.

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hysteresis db value |

### getMaximumNumberOfThresholdsAllowed

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getMaximumNumberOfThresholdsAllowed(): Int
```

Get the maximum number of threshold allowed in each SignalThresholdInfo.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of thresholds allowed |

### getMinimumNumberOfThresholdsAllowed

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getMinimumNumberOfThresholdsAllowed(): Int
```

Get the minimum number of thresholds allowed in each SignalThresholdInfo.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the minimum number of thresholds allowed |

### getRadioAccessNetworkType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRadioAccessNetworkType(): Int
```

Get the radio access network type.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | radio access network type Value is [android.telephony.AccessNetworkConstants.AccessNetworkType#UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#UNKNOWN:kotlin.Int), [android.telephony.AccessNetworkConstants.AccessNetworkType#GERAN](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#GERAN:kotlin.Int), [android.telephony.AccessNetworkConstants.AccessNetworkType#UTRAN](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#UTRAN:kotlin.Int), [android.telephony.AccessNetworkConstants.AccessNetworkType#EUTRAN](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#EUTRAN:kotlin.Int), [android.telephony.AccessNetworkConstants.AccessNetworkType#CDMA2000](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#CDMA2000:kotlin.Int), [android.telephony.AccessNetworkConstants.AccessNetworkType#IWLAN](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#IWLAN:kotlin.Int), or [android.telephony.AccessNetworkConstants.AccessNetworkType#NGRAN](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.AccessNetworkType#NGRAN:kotlin.Int) |

### getSignalMeasurementType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSignalMeasurementType(): Int
```

Get the signal measurement type.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the SignalMeasurementType value Value is [android.telephony.SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_UNKNOWN:kotlin.Int), [android.telephony.SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_RSSI](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_RSSI:kotlin.Int), [android.telephony.SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_RSCP](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_RSCP:kotlin.Int), [android.telephony.SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_RSRP](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_RSRP:kotlin.Int), [android.telephony.SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_RSRQ](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_RSRQ:kotlin.Int), [android.telephony.SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_RSSNR](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_RSSNR:kotlin.Int), [android.telephony.SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_SSRSRP](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_SSRSRP:kotlin.Int), [android.telephony.SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_SSRSRQ](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_SSRSRQ:kotlin.Int), [android.telephony.SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_SSSINR](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_SSSINR:kotlin.Int), or [android.telephony.SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_ECNO](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_ECNO:kotlin.Int) |

### getThresholds

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getThresholds(): IntArray
```

Get the signal strength thresholds. Signal strength thresholds are a list of integer used for suggesting signal level and signal reporting criteria. The range and unit must reference specific SignalMeasurementType. Please refer to https://source.android.com/devices/tech/connect/signal-strength on how signal strength thresholds are used for signal strength reporting.

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | array of integer of the signal thresholds This value cannot be`null`. |

**See Also**

- [#SIGNAL_MEASUREMENT_TYPE_RSSI](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_RSSI:kotlin.Int)
- [#SIGNAL_MEASUREMENT_TYPE_RSCP](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_RSCP:kotlin.Int)
- [#SIGNAL_MEASUREMENT_TYPE_RSRP](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_RSRP:kotlin.Int)
- [#SIGNAL_MEASUREMENT_TYPE_RSRQ](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_RSRQ:kotlin.Int)
- [#SIGNAL_MEASUREMENT_TYPE_RSSNR](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_RSSNR:kotlin.Int)
- [#SIGNAL_MEASUREMENT_TYPE_SSRSRP](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_SSRSRP:kotlin.Int)
- [#SIGNAL_MEASUREMENT_TYPE_SSRSRQ](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_SSRSRQ:kotlin.Int)
- [#SIGNAL_MEASUREMENT_TYPE_SSSINR](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_SSSINR:kotlin.Int)
- [#SIGNAL_MEASUREMENT_TYPE_ECNO](https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo#SIGNAL_MEASUREMENT_TYPE_ECNO:kotlin.Int) 

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
    out: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
| `out` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SignalThresholdInfo!>
```
