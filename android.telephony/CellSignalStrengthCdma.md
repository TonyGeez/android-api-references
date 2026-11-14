# CellSignalStrengthCdma

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CellSignalStrengthCdma

Kotlin| [Java](CellSignalStrengthCdma.md) 
| --- | --- |

```
class CellSignalStrengthCdma : CellSignalStrength, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.telephony.CellSignalStrength](CellSignalStrength.md) ||
| | ↳ | [android.telephony.CellSignalStrengthCdma](CellSignalStrengthCdma.md) |

Signal strength related information.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||
| From class [CellSignalStrength](CellSignalStrength.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_GOOD](CellSignalStrength.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_GREAT](CellSignalStrength.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_MODERATE](CellSignalStrength.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_NONE_OR_UNKNOWN](CellSignalStrength.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_POOR](CellSignalStrength.md) <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](CellSignalStrengthCdma.md))`()` Implement the Parcelable interface |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](CellSignalStrengthCdma.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAsuLevel](CellSignalStrengthCdma.md))`()` Get the 1xRTT Level in (Android) ASU. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCdmaDbm](CellSignalStrengthCdma.md))`()` Get the CDMA RSSI value in dBm |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCdmaEcio](CellSignalStrengthCdma.md))`()` Get the CDMA Ec/Io value in dB\*10 |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCdmaLevel](CellSignalStrengthCdma.md))`()` Get cdma as level 0. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDbm](CellSignalStrengthCdma.md))`()` Get the signal strength as dBm |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEvdoDbm](CellSignalStrengthCdma.md))`()` Get the EVDO RSSI value in dBm |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEvdoEcio](CellSignalStrengthCdma.md))`()` Get the EVDO Ec/Io value in dB\*10 |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEvdoLevel](CellSignalStrengthCdma.md))`()` Get Evdo as level 0. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEvdoSnr](CellSignalStrengthCdma.md))`()` Get the signal to noise ratio. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLevel](CellSignalStrengthCdma.md))`()` Retrieve an abstract level value for the overall signal quality. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](CellSignalStrengthCdma.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](CellSignalStrengthCdma.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](CellSignalStrengthCdma.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implement the Parcelable interface |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [CellSignalStrengthCdma](CellSignalStrengthCdma.md)!\> | [CREATOR](CellSignalStrengthCdma.md) Implement the Parcelable interface |

## Public methods

### describeContents

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Implement the Parcelable interface

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### equals

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAsuLevel

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAsuLevel(): Int
```

Get the 1xRTT Level in (Android) ASU. There is no standard definition of ASU for CDMA; however, Android defines it as the the lesser of the following two results (for 1xRTT):

| RSSI Range (dBm) | ASU Value |
|------------------|-----------|
| -75.. | 16 |
| -82..-76 | 8 |
| -90..-83 | 4 |
| --- | --- |
| -95..-91 | 2 |
| -100..-96 | 1 |
| ..-101 | 99 |
| --- | --- |

| Ec/Io Range (dB) | ASU Value |
|------------------|-----------|
| -90.. | 16 |
| -100..-91 | 8 |
| -115..-101 | 4 |
| --- | --- |
| -130..-116 | 2 |
| --150..-131 | 1 |
| ..-151 | 99 |
| --- | --- |

<br />

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | 1xRTT Level in Android ASU {1,2,4,8,16,99} |

### getCdmaDbm

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCdmaDbm(): Int
```

Get the CDMA RSSI value in dBm 

### getCdmaEcio

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCdmaEcio(): Int
```

Get the CDMA Ec/Io value in dB\*10 

### getCdmaLevel

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCdmaLevel(): Int
```

Get cdma as level 0..4 

### getDbm

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDbm(): Int
```

Get the signal strength as dBm

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | min(CDMA RSSI, EVDO RSSI) of the measured cell. |

### getEvdoDbm

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEvdoDbm(): Int
```

Get the EVDO RSSI value in dBm 

### getEvdoEcio

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEvdoEcio(): Int
```

Get the EVDO Ec/Io value in dB\*10 

### getEvdoLevel

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEvdoLevel(): Int
```

Get Evdo as level 0..4 

### getEvdoSnr

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEvdoSnr(): Int
```

Get the signal to noise ratio. Valid values are 0-8. 8 is the highest. 

### getLevel

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLevel(): Int
```

Retrieve an abstract level value for the overall signal quality.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is between [android.telephony.CellSignalStrength#SIGNAL_STRENGTH_NONE_OR_UNKNOWN](CellSignalStrength.md) and [android.telephony.CellSignalStrength#SIGNAL_STRENGTH_GREAT](CellSignalStrength.md) inclusive |

### hashCode

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | string representation. |

### writeToParcel

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Implement the Parcelable interface

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<CellSignalStrengthCdma!>
```

Implement the Parcelable interface
