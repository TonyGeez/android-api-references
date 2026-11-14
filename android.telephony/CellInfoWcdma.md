# CellInfoWcdma

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CellInfoWcdma

Kotlin| [Java](https://developer.android.com/reference/android/telephony/CellInfoWcdma "View this page in Java") 
| --- | --- |

```
class CellInfoWcdma : CellInfo, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.telephony.CellInfo](https://developer.android.com/reference/kotlin/android/telephony/CellInfo) ||
| | ↳ | [android.telephony.CellInfoWcdma](https://developer.android.com/reference/kotlin/android/telephony/CellInfoWcdma#) |

A [CellInfo](https://developer.android.com/reference/kotlin/android/telephony/CellInfo) representing a WCDMA cell that provides identity and measurement info.

## Summary

| Inherited constants ||
|---|---|
| From class [CellInfo](https://developer.android.com/reference/kotlin/android/telephony/CellInfo) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONNECTION_NONE](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#CONNECTION_NONE:kotlin.Int) <br /> Cell is not a serving cell. The cell has been measured but is neither a camped nor serving cell (3GPP 36.304). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONNECTION_PRIMARY_SERVING](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#CONNECTION_PRIMARY_SERVING:kotlin.Int) <br /> UE is connected to cell for signalling and possibly data (3GPP 36.331, 25.331). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONNECTION_SECONDARY_SERVING](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#CONNECTION_SECONDARY_SERVING:kotlin.Int) <br /> UE is connected to cell for data (3GPP 36.331, 25.331). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONNECTION_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#CONNECTION_UNKNOWN:kotlin.Int) <br /> Connection status is unknown. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int) <br /> This value indicates that the integer field is unreported. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [UNAVAILABLE_LONG](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE_LONG:kotlin.Long) <br /> This value indicates that the long field is unreported. <br /> | ||
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/telephony/CellInfoWcdma#describeContents())`()` Implement the Parcelable interface |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/telephony/CellInfoWcdma#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [CellIdentityWcdma](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityWcdma) | [getCellIdentity](https://developer.android.com/reference/kotlin/android/telephony/CellInfoWcdma#getCellIdentity())`()` <br /> |
| --- | --- |
| [CellSignalStrengthWcdma](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthWcdma) | [getCellSignalStrength](https://developer.android.com/reference/kotlin/android/telephony/CellInfoWcdma#getCellSignalStrength())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/telephony/CellInfoWcdma#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/telephony/CellInfoWcdma#toString())`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/telephony/CellInfoWcdma#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implement the Parcelable interface |

| Inherited functions ||
|---|---|
| From class [CellInfo](https://developer.android.com/reference/kotlin/android/telephony/CellInfo) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCellConnectionStatus](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#getCellConnectionStatus())`()` <br /> Gets the connection status of this cell. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimeStamp](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#getTimeStamp())`()` <br /> Approximate time this cell information was received from the modem. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimestampMillis](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#getTimestampMillis())`()` <br /> Approximate time this cell information was received from the modem. Value is a non-negative timestamp in the [android.os.SystemClock#elapsedRealtime()](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtime())time base. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRegistered](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#isRegistered())`()` <br /> True if the phone is registered to a mobile network that provides service on this cell and this cell is being used or would be used for network signaling. <br /> | ||

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [CellInfoWcdma](https://developer.android.com/reference/kotlin/android/telephony/CellInfoWcdma#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/telephony/CellInfoWcdma#CREATOR:android.os.Parcelable.Creator) Implement the Parcelable interface |

## Public methods

### describeContents

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Implement the Parcelable interface

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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

### getCellIdentity

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCellIdentity(): CellIdentityWcdma
```

| Return ||
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [CellIdentityWcdma](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityWcdma) | a [CellIdentityWcdma](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityWcdma) instance. |

### getCellSignalStrength

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCellSignalStrength(): CellSignalStrengthWcdma
```

| Return ||
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [CellSignalStrengthWcdma](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthWcdma) | a [CellSignalStrengthWcdma](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthWcdma) instance. |

### hashCode

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hash code |

### toString

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<CellInfoWcdma!>
```

Implement the Parcelable interface
