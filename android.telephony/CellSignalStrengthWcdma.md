# CellSignalStrengthWcdma

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CellSignalStrengthWcdma

Kotlin| [Java](CellSignalStrengthWcdma.md) 
| --- | --- |

```
class CellSignalStrengthWcdma : CellSignalStrength, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.telephony.CellSignalStrength](CellSignalStrength.md) ||
| | ↳ | [android.telephony.CellSignalStrengthWcdma](CellSignalStrengthWcdma.md) |

Wcdma signal strength related information.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||
| From class [CellSignalStrength](CellSignalStrength.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_GOOD](CellSignalStrength.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_GREAT](CellSignalStrength.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_MODERATE](CellSignalStrength.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_NONE_OR_UNKNOWN](CellSignalStrength.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_POOR](CellSignalStrength.md) <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](CellSignalStrengthWcdma.md))`()` Implement the Parcelable interface |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](CellSignalStrengthWcdma.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAsuLevel](CellSignalStrengthWcdma.md))`()` Get the RSCP in ASU. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDbm](CellSignalStrengthWcdma.md))`()` Get the RSCP as dBm value -120. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEcNo](CellSignalStrengthWcdma.md))`()` Get the Ec/No (Energy per chip over the noise spectral density) as dB. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLevel](CellSignalStrengthWcdma.md))`()` Retrieve an abstract level value for the overall signal quality. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](CellSignalStrengthWcdma.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](CellSignalStrengthWcdma.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](CellSignalStrengthWcdma.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implement the Parcelable interface |
| --- | --- |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [CellSignalStrengthWcdma](CellSignalStrengthWcdma.md)!\> | [CREATOR](CellSignalStrengthWcdma.md) Implement the Parcelable interface |

## Public methods

### describeContents

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Implement the Parcelable interface

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### equals

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAsuLevel(): Int
```

Get the RSCP in ASU. Asu is calculated based on 3GPP RSCP. Refer to 3GPP 27.007 (Ver 10.3.0) Sec 8.69

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | RSCP in ASU 0..96, 255, or UNAVAILABLE |

### getDbm

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDbm(): Int
```

Get the RSCP as dBm value -120..-24dBm or [UNAVAILABLE](CellInfo.md). 

### getEcNo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEcNo(): Int
```

Get the Ec/No (Energy per chip over the noise spectral density) as dB. Reference: TS 25.133 Section 9.1.2.3

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the Ec/No of the measured cell in the range \[-24, 1\] or [UNAVAILABLE](CellInfo.md) if unavailable |

### getLevel

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLevel(): Int
```

Retrieve an abstract level value for the overall signal quality.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is between [android.telephony.CellSignalStrength#SIGNAL_STRENGTH_NONE_OR_UNKNOWN](CellSignalStrength.md) and [android.telephony.CellSignalStrength#SIGNAL_STRENGTH_GREAT](CellSignalStrength.md) inclusive |

### hashCode

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | string representation. |

### writeToParcel

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<CellSignalStrengthWcdma!>
```

Implement the Parcelable interface
