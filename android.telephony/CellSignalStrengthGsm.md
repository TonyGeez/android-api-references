# CellSignalStrengthGsm

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CellSignalStrengthGsm

Kotlin| [Java](https://developer.android.com/reference/android/telephony/CellSignalStrengthGsm "View this page in Java") 
| --- | --- |

```
class CellSignalStrengthGsm : CellSignalStrength, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.telephony.CellSignalStrength](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength) ||
| | ↳ | [android.telephony.CellSignalStrengthGsm](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthGsm#) |

GSM signal strength related information.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||
| From class [CellSignalStrength](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_GOOD](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#SIGNAL_STRENGTH_GOOD:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_GREAT](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#SIGNAL_STRENGTH_GREAT:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_MODERATE](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#SIGNAL_STRENGTH_MODERATE:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_NONE_OR_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#SIGNAL_STRENGTH_NONE_OR_UNKNOWN:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_POOR](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#SIGNAL_STRENGTH_POOR:kotlin.Int) <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthGsm#describeContents())`()` Implement the Parcelable interface |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthGsm#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAsuLevel](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthGsm#getAsuLevel())`()` Get the RSSI in ASU. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBitErrorRate](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthGsm#getBitErrorRate())`()` Return the Bit Error Rate. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDbm](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthGsm#getDbm())`()` Get the signal strength as dBm. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLevel](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthGsm#getLevel())`()` Retrieve an abstract level value for the overall signal quality. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRssi](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthGsm#getRssi())`()` Return the Received Signal Strength Indicator. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimingAdvance](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthGsm#getTimingAdvance())`()` Get the GSM timing advance between 0. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthGsm#hashCode())`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthGsm#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthGsm#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implement the Parcelable interface |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [CellSignalStrengthGsm](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthGsm#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthGsm#CREATOR:android.os.Parcelable.Creator) Implement the Parcelable interface |

## Public methods

### describeContents

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Implement the Parcelable interface

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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

Get the RSSI in ASU. Asu is calculated based on 3GPP RSSI. Refer to 3GPP 27.007 (Ver 10.3.0) Sec 8.69

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | RSSI in ASU 0..31, 99, or [UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int). |

### getBitErrorRate

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBitErrorRate(): Int
```

Return the Bit Error Rate.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the bit error rate (0-7, 99) as defined in TS 27.007 8.5 or [UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int). |

### getDbm

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDbm(): Int
```

Get the signal strength as dBm.

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the RSSI of the measured cell. |

### getLevel

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLevel(): Int
```

Retrieve an abstract level value for the overall signal quality.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is between [android.telephony.CellSignalStrength#SIGNAL_STRENGTH_NONE_OR_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#SIGNAL_STRENGTH_NONE_OR_UNKNOWN:kotlin.Int) and [android.telephony.CellSignalStrength#SIGNAL_STRENGTH_GREAT](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#SIGNAL_STRENGTH_GREAT:kotlin.Int) inclusive |

### getRssi

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRssi(): Int
```

Return the Received Signal Strength Indicator.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the RSSI in dBm (-113, -51) or [UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int). |

### getTimingAdvance

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimingAdvance(): Int
```

Get the GSM timing advance between 0..219 symbols (normally 0..63).

[UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int) is reported when there is no RR connection. Refer to 3GPP 45.010 Sec 5.8.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current GSM timing advance, if available. |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<CellSignalStrengthGsm!>
```

Implement the Parcelable interface
