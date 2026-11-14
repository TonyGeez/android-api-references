# CellIdentity

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CellIdentity

Kotlin| [Java](https://developer.android.com/reference/android/telephony/CellIdentity "View this page in Java") 

```
abstract class CellIdentity : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.CellIdentity](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity#) |

| Known Direct Subclasses [CellIdentityCdma](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityCdma), [CellIdentityGsm](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityGsm), [CellIdentityLte](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte), [CellIdentityNr](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityNr), [CellIdentityTdscdma](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityTdscdma), [CellIdentityWcdma](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityWcdma) |-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------| | [CellIdentityCdma](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityCdma) | CellIdentity is to represent a unique CDMA cell | | [CellIdentityGsm](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityGsm) | CellIdentity to represent a unique GSM cell | | [CellIdentityLte](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityLte) | CellIdentity is to represent a unique LTE cell | | [CellIdentityNr](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityNr) | Information to represent a unique NR(New Radio 5G) cell. | | [CellIdentityTdscdma](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityTdscdma) | CellIdentity is to represent a unique TD-SCDMA cell | | [CellIdentityWcdma](https://developer.android.com/reference/kotlin/android/telephony/CellIdentityWcdma) | CellIdentity to represent a unique UMTS cell | |

CellIdentity represents the identity of a unique cell. This is the base class for CellIdentityXxx which represents cell identity for specific network access technology.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity#describeContents())`()` Implement the Parcelable interface |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getOperatorAlphaLong](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity#getOperatorAlphaLong())`()` <br /> |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getOperatorAlphaShort](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity#getOperatorAlphaShort())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity#hashCode())`()` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [CellIdentity](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity#CREATOR:android.os.Parcelable.Creator) Implement the Parcelable interface |

## Public methods

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

Implement the Parcelable interface

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getOperatorAlphaLong

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOperatorAlphaLong(): CharSequence?
```

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | The long alpha tag associated with the current scan result (may be the operator name string or extended operator name string). May be null if unknown. |

### getOperatorAlphaShort

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOperatorAlphaShort(): CharSequence?
```

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | The short alpha tag associated with the current scan result (may be the operator name string or extended operator name string). May be null if unknown. |

### hashCode

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

## Properties

### CREATOR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<CellIdentity!>
```

Implement the Parcelable interface
