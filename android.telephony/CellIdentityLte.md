# CellIdentityLte

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CellIdentityLte

Kotlin| [Java](https://developer.android.com/reference/android/telephony/CellIdentityLte "View this page in Java") 
| --- | --- |

```
class CellIdentityLte : CellIdentity
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.telephony.CellIdentity](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity) ||
| | ↳ | [android.telephony.CellIdentityLte](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte#) |

CellIdentity is to represent a unique LTE cell

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getAdditionalPlmns](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte#getAdditionalPlmns())`()` <br /> |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getBands](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte#getBands())`()` Get bands of the cell Reference: 3GPP TS 36. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBandwidth](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte#getBandwidth())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCi](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte#getCi())`()` <br /> |
| [ClosedSubscriberGroupInfo](https://developer.android.com/reference/kotlin/android/telephony/ClosedSubscriberGroupInfo)? | [getClosedSubscriberGroupInfo](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte#getClosedSubscriberGroupInfo())`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEarfcn](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte#getEarfcn())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMcc](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte#getMcc())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getMccString](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte#getMccString())`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMnc](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte#getMnc())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getMncString](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte#getMncString())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getMobileNetworkOperator](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte#getMobileNetworkOperator())`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPci](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte#getPci())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTac](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte#getTac())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte#hashCode())`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implement the Parcelable interface |

| Inherited functions ||
|---|---|
| From class [CellIdentity](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity) |------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity#describeContents())`()` <br /> Implement the Parcelable interface <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getOperatorAlphaLong](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity#getOperatorAlphaLong())`()` <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getOperatorAlphaShort](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity#getOperatorAlphaShort())`()` <br /> | ||

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [CellIdentityLte](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte#CREATOR:android.os.Parcelable.Creator) Implement the Parcelable interface |

## Public methods

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

### getAdditionalPlmns

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAdditionalPlmns(): MutableSet<String!>
```

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | a list of additional PLMN IDs supported by this cell. This value cannot be`null`. |

### getBands

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBands(): IntArray
```

Get bands of the cell Reference: 3GPP TS 36.101 section 5.5

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | Array of band number or empty array if not available. This value cannot be`null`. |

### getBandwidth

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBandwidth(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Cell bandwidth in kHz, [UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int) if unavailable. |

### getCi

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCi(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | 28-bit Cell Identity, [UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int) if unavailable. |

### getClosedSubscriberGroupInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClosedSubscriberGroupInfo(): ClosedSubscriberGroupInfo?
```

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [ClosedSubscriberGroupInfo](https://developer.android.com/reference/kotlin/android/telephony/ClosedSubscriberGroupInfo)? | closed subscriber group information about the cell if available, otherwise null. |

### getEarfcn

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEarfcn(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | 18-bit Absolute RF Channel Number, [UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int) if unavailable. |

### getMcc

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMcc(): Int
```

**Deprecated:** *Use [getMccString](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte#getMccString())instead.*

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | 3-digit Mobile Country Code, 0..999, [UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int) if unavailable. |

### getMccString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMccString(): String?
```

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | Mobile Country Code in string format, null if unavailable. |

### getMnc

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMnc(): Int
```

**Deprecated:** *Use [getMncString](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte#getMncString())instead.*

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | 2 or 3-digit Mobile Network Code, 0..999, [UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int) if unavailable. |

### getMncString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMncString(): String?
```

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | Mobile Network Code in string format, null if unavailable. |

### getMobileNetworkOperator

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMobileNetworkOperator(): String?
```

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | a 5 or 6 character string (MCC+MNC), null if any field is unknown. |

### getPci

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPci(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Physical Cell Id 0..503, [UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int) if unavailable. |

### getTac

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTac(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | 16-bit Tracking Area Code, [UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int) if unavailable. |

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
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

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
static val CREATOR: Parcelable.Creator<CellIdentityLte!>
```

Implement the Parcelable interface
