# CellIdentity

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CellIdentity

Kotlin| [Java](CellIdentity.md) 
| --- | --- |

```
abstract class CellIdentity : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.CellIdentity](CellIdentity.md) |

| Known Direct Subclasses [CellIdentityCdma](CellIdentityCdma.md), [CellIdentityGsm](CellIdentityGsm.md), [CellIdentityLte](CellIdentityLte.md), [CellIdentityNr](CellIdentityNr.md), [CellIdentityTdscdma](CellIdentityTdscdma.md), [CellIdentityWcdma](CellIdentityWcdma.md) |-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------| | [CellIdentityCdma](CellIdentityCdma.md) | CellIdentity is to represent a unique CDMA cell | | [CellIdentityGsm](CellIdentityGsm.md) | CellIdentity to represent a unique GSM cell | | [CellIdentityLte](CellIdentityLte.md) | CellIdentity is to represent a unique LTE cell | | [CellIdentityNr](CellIdentityNr.md) | Information to represent a unique NR(New Radio 5G) cell. | | [CellIdentityTdscdma](CellIdentityTdscdma.md) | CellIdentity is to represent a unique TD-SCDMA cell | | [CellIdentityWcdma](CellIdentityWcdma.md) | CellIdentity to represent a unique UMTS cell | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

CellIdentity represents the identity of a unique cell. This is the base class for CellIdentityXxx which represents cell identity for specific network access technology.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](CellIdentity.md))`()` Implement the Parcelable interface |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](CellIdentity.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getOperatorAlphaLong](CellIdentity.md))`()` <br /> |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getOperatorAlphaShort](CellIdentity.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](CellIdentity.md))`()` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [CellIdentity](CellIdentity.md)!\> | [CREATOR](CellIdentity.md) Implement the Parcelable interface |

## Public methods

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

Implement the Parcelable interface

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

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
