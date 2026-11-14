# CellIdentityNr

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CellIdentityNr

Kotlin| [Java](../android/telephony/CellIdentityNr.md) 
| --- | --- |

```
class CellIdentityNr : CellIdentity
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.telephony.CellIdentity](../android/telephony/CellIdentity.md) ||
| | ↳ | [android.telephony.CellIdentityNr](../android/telephony/CellIdentityNr.md) |

Information to represent a unique NR(New Radio 5G) cell.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/telephony/CellIdentityNr.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getAdditionalPlmns](../android/telephony/CellIdentityNr.md))`()` <br /> |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getBands](../android/telephony/CellIdentityNr.md))`()` Get bands of the cell Reference: TS 38. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getMccString](../android/telephony/CellIdentityNr.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getMncString](../android/telephony/CellIdentityNr.md))`()` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getNci](../android/telephony/CellIdentityNr.md))`()` Get the NR(New Radio 5G) Cell Identity. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNrarfcn](../android/telephony/CellIdentityNr.md))`()` Get the New Radio Absolute Radio Frequency Channel Number. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPci](../android/telephony/CellIdentityNr.md))`()` Get the physical cell id. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTac](../android/telephony/CellIdentityNr.md))`()` Get the tracking area code. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/telephony/CellIdentityNr.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/telephony/CellIdentityNr.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/telephony/CellIdentityNr.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [CellIdentity](../android/telephony/CellIdentity.md) |------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/telephony/CellIdentity.md))`()` <br /> Implement the Parcelable interface <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getOperatorAlphaLong](../android/telephony/CellIdentity.md))`()` <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getOperatorAlphaShort](../android/telephony/CellIdentity.md))`()` <br /> | ||

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [CellIdentityNr](../android/telephony/CellIdentityNr.md)!\> | [CREATOR](../android/telephony/CellIdentityNr.md) Implement the Parcelable interface |

## Public methods

### equals

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Get bands of the cell Reference: TS 38.101-1 table 5.2-1 Reference: TS 38.101-2 table 5.2-1

| Return ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | Array of band number or empty array if not available. Value is [android.telephony.AccessNetworkConstants.NgranBands#BAND_1](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_2](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_3](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_5](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_7](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_8](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_12](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_14](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_18](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_20](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_25](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_26](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_28](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_29](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_30](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_34](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_38](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_39](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_40](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_41](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_46](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_48](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_50](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_51](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_53](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_65](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_66](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_70](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_71](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_74](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_75](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_76](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_77](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_78](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_79](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_80](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_81](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_82](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_83](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_84](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_86](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_89](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_90](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_91](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_92](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_93](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_94](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_95](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_96](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_257](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_258](../android/telephony/AccessNetworkConstants.NgranBands.md), [android.telephony.AccessNetworkConstants.NgranBands#BAND_260](../android/telephony/AccessNetworkConstants.NgranBands.md), or [android.telephony.AccessNetworkConstants.NgranBands#BAND_261](../android/telephony/AccessNetworkConstants.NgranBands.md) This value cannot be`null`. |

### getMccString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMccString(): String?
```

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | Mobile Country Code in string format, or`null`if unknown. |

### getMncString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMncString(): String?
```

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | Mobile Network Code in string format, or`null`if unknown. |

### getNci

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNci(): Long
```

Get the NR(New Radio 5G) Cell Identity.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The 36-bit NR Cell Identity in range \[0, 68719476735\] or [CellInfo.UNAVAILABLE_LONG](../android/telephony/CellInfo.md) if unknown. |

### getNrarfcn

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNrarfcn(): Int
```

Get the New Radio Absolute Radio Frequency Channel Number. Reference: 3GPP TS 38.101-1 section 5.4.2.1 NR-ARFCN and channel raster. Reference: 3GPP TS 38.101-2 section 5.4.2.1 NR-ARFCN and channel raster.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Integer value in range \[0, 3279165\] or [CellInfo.UNAVAILABLE](../android/telephony/CellInfo.md) if unknown. Value is between 0 and 3279165 inclusive |

### getPci

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPci(): Int
```

Get the physical cell id.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Integer value in range \[0, 1007\] or [CellInfo.UNAVAILABLE](../android/telephony/CellInfo.md) if unknown. Value is between 0 and 1007 inclusive |

### getTac

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTac(): Int
```

Get the tracking area code.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a 24 bit integer or [CellInfo.UNAVAILABLE](../android/telephony/CellInfo.md) if unknown. Value is between 0 and 16777215 inclusive |

### hashCode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    type: Int
): Unit
```

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<CellIdentityNr!>
```

Implement the Parcelable interface
