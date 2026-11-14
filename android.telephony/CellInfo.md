Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CellInfo

Kotlin | [Java](https://developer.android.com/reference/android/telephony/CellInfo "View this page in Java")
| --- | --- |

```
abstract class CellInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.CellInfo](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#) |

| Known Direct Subclasses [CellInfoCdma](https://developer.android.com/reference/kotlin/android/telephony/CellInfoCdma), [CellInfoGsm](https://developer.android.com/reference/kotlin/android/telephony/CellInfoGsm), [CellInfoLte](https://developer.android.com/reference/kotlin/android/telephony/CellInfoLte), [CellInfoNr](https://developer.android.com/reference/kotlin/android/telephony/CellInfoNr), [CellInfoTdscdma](https://developer.android.com/reference/kotlin/android/telephony/CellInfoTdscdma), [CellInfoWcdma](https://developer.android.com/reference/kotlin/android/telephony/CellInfoWcdma) |---|---| | [CellInfoCdma](https://developer.android.com/reference/kotlin/android/telephony/CellInfoCdma) | A `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#` representing a CDMA cell that provides identity and measurement info. | | [CellInfoGsm](https://developer.android.com/reference/kotlin/android/telephony/CellInfoGsm) | A `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#` representing a GSM cell that provides identity and measurement info. | | [CellInfoLte](https://developer.android.com/reference/kotlin/android/telephony/CellInfoLte) | A `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#` representing an LTE cell that provides identity and measurement info. | | [CellInfoNr](https://developer.android.com/reference/kotlin/android/telephony/CellInfoNr) | A `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#` representing an 5G NR cell that provides identity and measurement info. | | [CellInfoTdscdma](https://developer.android.com/reference/kotlin/android/telephony/CellInfoTdscdma) | A `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#` representing a TD-SCDMA cell that provides identity and measurement info. | | [CellInfoWcdma](https://developer.android.com/reference/kotlin/android/telephony/CellInfoWcdma) | A `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#` representing a WCDMA cell that provides identity and measurement info. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Immutable cell information from a point in time.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#CONNECTION_NONE:kotlin.Int` Cell is not a serving cell. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#CONNECTION_PRIMARY_SERVING:kotlin.Int` UE is connected to cell for signalling and possibly data (3GPP 36.331, 25.331). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#CONNECTION_SECONDARY_SERVING:kotlin.Int` UE is connected to cell for data (3GPP 36.331, 25.331). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#CONNECTION_UNKNOWN:kotlin.Int` Connection status is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int` This value indicates that the integer field is unreported. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE_LONG:kotlin.Long` This value indicates that the long field is unreported. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#describeContents()()` Implement the Parcelable interface |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#getCellConnectionStatus()()` Gets the connection status of this cell. |
| --- | --- |
| abstract [CellIdentity](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity) | `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#getCellIdentity()()` <br /> |
| abstract [CellSignalStrength](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength) | `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#getCellSignalStrength()()` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#getTimeStamp()()` Approximate time this cell information was received from the modem. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#getTimestampMillis()()` Approximate time this cell information was received from the modem. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#hashCode()()` Returns a hash code value for the object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#isRegistered()()` True if the phone is registered to a mobile network that provides service on this cell and this cell is being used or would be used for network signaling. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#toString()()` Returns a string representation of the object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Implement the Parcelable interface |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [CellInfo](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#)!\> | `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#CREATOR:android.os.Parcelable.Creator` Implement the Parcelable interface |

## Constants

### CONNECTION_NONE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_NONE: Int
```

Cell is not a serving cell.

The cell has been measured but is neither a camped nor serving cell (3GPP 36.304).

 Value: 0

### CONNECTION_PRIMARY_SERVING

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_PRIMARY_SERVING: Int
```

UE is connected to cell for signalling and possibly data (3GPP 36.331, 25.331).

 Value: 1

### CONNECTION_SECONDARY_SERVING

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_SECONDARY_SERVING: Int
```

UE is connected to cell for data (3GPP 36.331, 25.331).

 Value: 2

### CONNECTION_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_UNKNOWN: Int
```

Connection status is unknown.

 Value: 2147483647

### UNAVAILABLE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNAVAILABLE: Int
```

This value indicates that the integer field is unreported.

 Value: 2147483647

### UNAVAILABLE_LONG

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNAVAILABLE_LONG: Long
```

This value indicates that the long field is unreported.

 Value: 9223372036854775807L

## Public methods

### describeContents

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Implement the Parcelable interface

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
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

### getCellConnectionStatus

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCellConnectionStatus(): Int
```

Gets the connection status of this cell.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The connection status of the cell. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#CONNECTION_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#CONNECTION_PRIMARY_SERVING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#CONNECTION_SECONDARY_SERVING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#CONNECTION_UNKNOWN:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#CONNECTION_NONE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#CONNECTION_PRIMARY_SERVING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#CONNECTION_SECONDARY_SERVING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#CONNECTION_UNKNOWN:kotlin.Int`

### getCellIdentity

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getCellIdentity(): CellIdentity
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telephony/CellIdentity` | a `https://developer.android.com/reference/kotlin/android/telephony/CellIdentity` instance. This value cannot be `null`. |

### getCellSignalStrength

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getCellSignalStrength(): CellSignalStrength
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength` | a `https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength` instance. This value cannot be `null`. |

### getTimeStamp

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTimeStamp(): Long
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/telephony/CellInfo#getTimestampMillis()` instead.*

Approximate time this cell information was received from the modem.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | a time stamp in nanos since boot. |

### getTimestampMillis

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTimestampMillis(): Long
```

Approximate time this cell information was received from the modem. 
Value is a non-negative timestamp in the `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtime()` time base.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | a time stamp in millis since boot. Value is a non-negative timestamp in the `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtime()` time base. |

### hashCode

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isRegistered

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isRegistered(): Boolean
```

True if the phone is registered to a mobile network that provides service on this cell and this cell is being used or would be used for network signaling.

### toString

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Implement the Parcelable interface

| Parameters ||
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<CellInfo!>
```

Implement the Parcelable interface
