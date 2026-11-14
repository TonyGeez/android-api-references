Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CellSignalStrengthNr

```
class CellSignalStrengthNr : CellSignalStrength, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.telephony.CellSignalStrength](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength) ||
| | ↳ | [android.telephony.CellSignalStrengthNr](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr#) |

5G NR signal strength related information.

## Summary

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

From class `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#SIGNAL_STRENGTH_GOOD:kotlin.Int`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#SIGNAL_STRENGTH_GREAT:kotlin.Int`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#SIGNAL_STRENGTH_MODERATE:kotlin.Int`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#SIGNAL_STRENGTH_NONE_OR_UNKNOWN:kotlin.Int`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#SIGNAL_STRENGTH_POOR:kotlin.Int`

<br />

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr#getAsuLevel()()` Get the RSRP in ASU. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr#getCsiCqiReport()()` Return a list of CSI channel quality indicators (CQI) for all subbands. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr#getCsiCqiTableIndex()()` Return CSI channel quality indicator (CQI) table index. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr#getCsiRsrp()()` Reference: 3GPP TS 38. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr#getCsiRsrq()()` Reference: 3GPP TS 38. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr#getCsiSinr()()` Reference: 3GPP TS 38. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr#getDbm()()` Get the SS-RSRP as dBm value -140. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr#getLevel()()` Retrieve an abstract level value for the overall signal quality. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr#getSsRsrp()()` Reference: 3GPP TS 38. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr#getSsRsrq()()` Reference: 3GPP TS 38. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr#getSsSinr()()` Reference: 3GPP TS 38. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr#getTimingAdvanceMicros()()` Get the timing advance value for a one way trip from cell to device for NR. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr#hashCode()()` Returns a hash code value for the object. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [CellSignalStrengthNr](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr#)!\> | `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr#CREATOR:android.os.Parcelable.Creator` Implement the Parcelable interface |

## Public methods

### describeContents

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getAsuLevel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAsuLevel(): Int
```

Get the RSRP in ASU. Asu is calculated based on 3GPP RSRP. Refer to 3GPP 27.007 (Ver 10.3.0) Sec 8.69

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | RSRP in ASU 0..97, 255, or UNAVAILABLE |

### getCsiCqiReport

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCsiCqiReport(): MutableList<Int!>
```

Return a list of CSI channel quality indicators (CQI) for all subbands. If the CQI report is for the entire wideband, a single CQI index is provided. If the CQI report is for all subbands, one CQI index is provided for each subband, in ascending order of subband index. If CQI is not available, the CQI report is empty. Reference: 3GPP TS 138.214 section 5.2.2.1.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | the CQIs for all subbands if available or empty list if unavailable. This value cannot be `null`. Value is between 0 and 15 inclusive |

### getCsiCqiTableIndex

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCsiCqiTableIndex(): Int
```

Return CSI channel quality indicator (CQI) table index. There are multiple CQI tables. The definition of CQI in each table is different. Reference: 3GPP TS 138.214 section 5.2.2.1.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the CQI table index if available or `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int` if unavailable. Value is between 1 and 3 inclusive |

### getCsiRsrp

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCsiRsrp(): Int
```

Reference: 3GPP TS 38.133 10.1.6.1. Range: -156 dBm to -31 dBm.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | CSI reference signal received power, `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int` means unreported value. |

### getCsiRsrq

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCsiRsrq(): Int
```

Reference: 3GPP TS 38.215. Range: -20 dB to -3 dB.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | CSI reference signal received quality, `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int` means unreported value. |

### getCsiSinr

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCsiSinr(): Int
```

Reference: 3GPP TS 38.215 Sec 5.1.\*, 3GPP TS 38.133 10.1.16.1 Range: -23 dB to 23 dB

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | CSI signal-to-noise and interference ratio, `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int` means unreported value. |

### getDbm

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDbm(): Int
```

Get the SS-RSRP as dBm value -140..-44dBm or `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int`.

### getLevel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLevel(): Int
```

Retrieve an abstract level value for the overall signal quality.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is between `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#SIGNAL_STRENGTH_NONE_OR_UNKNOWN:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength#SIGNAL_STRENGTH_GREAT:kotlin.Int` inclusive |

### getSsRsrp

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSsRsrp(): Int
```

Reference: 3GPP TS 38.133 10.1.6.1. Range: -156 dBm to -31 dBm.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | SS reference signal received power, `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int` means unreported value. |

### getSsRsrq

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSsRsrq(): Int
```

Reference: 3GPP TS 38.215; 3GPP TS 38.133 section 10 Range: -43 dB to 20 dB.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | SS reference signal received quality, `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int` means unreported value. |

### getSsSinr

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSsSinr(): Int
```

Reference: 3GPP TS 38.215 Sec 5.1.\*, 3GPP TS 38.133 10.1.16.1 Range: -23 dB to 40 dB

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | SS signal-to-noise and interference ratio, `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int` means unreported value. |

### getTimingAdvanceMicros

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTimingAdvanceMicros(): Int
```

Get the timing advance value for a one way trip from cell to device for NR. Note: This value represents the raw 3GPP TS 38.213 Section 4.2 Timing Advance command index (T_A), not physical microseconds, despite the method name. `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int` is reported when there is no active RRC connection. Reference: 3GPP TS 38.213 section 4.2. Range: 0 to 3846 (raw index).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the NR timing advance if available or `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int` if unavailable. Value is between 0 and 3846 inclusive |

### hashCode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### toString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<CellSignalStrengthNr!>
```

Implement the Parcelable interface
