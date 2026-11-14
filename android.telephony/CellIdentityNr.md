# CellIdentityNr

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CellIdentityNr

Kotlin| [Java](https://developer.android.com/reference/android/telephony/CellIdentityNr "View this page in Java") 

```
class CellIdentityNr : CellIdentity
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.telephony.CellIdentity](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity) ||
| | ↳ | [android.telephony.CellIdentityNr](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityNr#) |

Information to represent a unique NR(New Radio 5G) cell.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityNr#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getAdditionalPlmns](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityNr#getAdditionalPlmns())`()` <br /> |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getBands](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityNr#getBands())`()` Get bands of the cell Reference: TS 38. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getMccString](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityNr#getMccString())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getMncString](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityNr#getMncString())`()` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getNci](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityNr#getNci())`()` Get the NR(New Radio 5G) Cell Identity. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNrarfcn](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityNr#getNrarfcn())`()` Get the New Radio Absolute Radio Frequency Channel Number. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPci](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityNr#getPci())`()` Get the physical cell id. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTac](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityNr#getTac())`()` Get the tracking area code. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityNr#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityNr#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityNr#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [CellIdentity](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity) |------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity#describeContents())`()` <br /> Implement the Parcelable interface <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getOperatorAlphaLong](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity#getOperatorAlphaLong())`()` <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getOperatorAlphaShort](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity#getOperatorAlphaShort())`()` <br /> | ||

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [CellIdentityNr](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityNr#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityNr#CREATOR:android.os.Parcelable.Creator) Implement the Parcelable interface |

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
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | Array of band number or empty array if not available. Value is [android.telephony.AccessNetworkConstants.NgranBands#BAND_1](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_1:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_2](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_2:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_3](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_3:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_5](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_5:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_7](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_7:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_8](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_8:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_12](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_12:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_14](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_14:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_18](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_18:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_20](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_20:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_25](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_25:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_26](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_26:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_28](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_28:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_29](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_29:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_30](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_30:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_34](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_34:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_38](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_38:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_39](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_39:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_40](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_40:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_41](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_41:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_46](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_46:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_48](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_48:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_50](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_50:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_51](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_51:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_53](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_53:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_65](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_65:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_66](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_66:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_70](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_70:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_71](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_71:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_74](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_74:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_75](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_75:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_76](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_76:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_77](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_77:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_78](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_78:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_79](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_79:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_80](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_80:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_81](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_81:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_82](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_82:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_83](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_83:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_84](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_84:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_86](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_86:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_89](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_89:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_90](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_90:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_91](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_91:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_92](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_92:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_93](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_93:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_94](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_94:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_95](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_95:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_96](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_96:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_257](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_257:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_258](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_258:kotlin.Int), [android.telephony.AccessNetworkConstants.NgranBands#BAND_260](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_260:kotlin.Int), or [android.telephony.AccessNetworkConstants.NgranBands#BAND_261](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.NgranBands#BAND_261:kotlin.Int) This value cannot be`null`. |

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
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The 36-bit NR Cell Identity in range \[0, 68719476735\] or [CellInfo.UNAVAILABLE_LONG](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE_LONG:kotlin.Long) if unknown. |

### getNrarfcn

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNrarfcn(): Int
```

Get the New Radio Absolute Radio Frequency Channel Number. Reference: 3GPP TS 38.101-1 section 5.4.2.1 NR-ARFCN and channel raster. Reference: 3GPP TS 38.101-2 section 5.4.2.1 NR-ARFCN and channel raster.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Integer value in range \[0, 3279165\] or [CellInfo.UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int) if unknown. Value is between 0 and 3279165 inclusive |

### getPci

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPci(): Int
```

Get the physical cell id.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Integer value in range \[0, 1007\] or [CellInfo.UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int) if unknown. Value is between 0 and 1007 inclusive |

### getTac

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTac(): Int
```

Get the tracking area code.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a 24 bit integer or [CellInfo.UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/CellInfo#UNAVAILABLE:kotlin.Int) if unknown. Value is between 0 and 16777215 inclusive |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<CellIdentityNr!>
```

Implement the Parcelable interface
