# UiccCardInfo

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UiccCardInfo

Kotlin| [Java](https://developer.android.com/reference/android/telephony/UiccCardInfo "View this page in Java") 
| --- | --- |

```
class UiccCardInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.UiccCardInfo](https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo#) |

The UiccCardInfo represents information about a currently inserted UICC or embedded eUICC.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCardId](https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo#getCardId())`()` Get the card ID of the UICC. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getEid](https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo#getEid())`()` Get the embedded ID (EID) of the eUICC. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getIccId](https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo#getIccId())`()` Get the ICCID of the UICC. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPhysicalSlotIndex](https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo#getPhysicalSlotIndex())`()` Gets the physical slot index for the slot that the UICC is currently inserted in. |
| --- | --- |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [UiccPortInfo](https://developer.android.com/reference/kotlin/android/telephony/UiccPortInfo)!\> | [getPorts](https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo#getPorts())`()` Get information regarding port, ICCID and its active status. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSlotIndex](https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo#getSlotIndex())`()` Gets the slot index for the slot that the UICC is currently inserted in. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo#hashCode())`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEuicc](https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo#isEuicc())`()` Return whether the UICC is an eUICC. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMultipleEnabledProfilesSupported](https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo#isMultipleEnabledProfilesSupported())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRemovable](https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo#isRemovable())`()` Return whether the UICC or eUICC is removable. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [UiccCardInfo](https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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

### getCardId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCardId(): Int
```

Get the card ID of the UICC. See [TelephonyManager.getCardIdForDefaultEuicc()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#getCardIdForDefaultEuicc())for more details on card ID. 

### getEid

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEid(): String?
```

Get the embedded ID (EID) of the eUICC. If the UiccCardInfo is not an eUICC (see [isEuicc()](https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo#isEuicc())), or the EID is not available, returns null.

Note that this field may be omitted if the caller does not have the correct permissions (see [TelephonyManager.getUiccCardsInfo()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#getUiccCardsInfo())). 

### getIccId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIccId(): String?
```

**Deprecated:** *with support for MEP(multiple enabled profile) [PackageManager.FEATURE_TELEPHONY_EUICC_MEP](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC_MEP:kotlin.String), a SIM card can have more than one ICCID active at the same time. Instead use [UiccPortInfo.getIccId()](https://developer.android.com/reference/kotlin/android/telephony/UiccPortInfo#getIccId())to retrieve ICCID. To find [UiccPortInfo](https://developer.android.com/reference/kotlin/android/telephony/UiccPortInfo) use [UiccCardInfo.getPorts()](https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo#getPorts()).*

Get the ICCID of the UICC. If the ICCID is not availble, returns null.

Note that this field may be omitted if the caller does not have the correct permissions (see [TelephonyManager.getUiccCardsInfo()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#getUiccCardsInfo())).

| Exceptions ||
|-------------------------------------------|--------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the calling app's target SDK is T and beyond. |

### getPhysicalSlotIndex

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPhysicalSlotIndex(): Int
```

Gets the physical slot index for the slot that the UICC is currently inserted in. 

### getPorts

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPorts(): MutableCollection<UiccPortInfo!>
```

Get information regarding port, ICCID and its active status. For device which support [PackageManager.FEATURE_TELEPHONY_EUICC_MEP](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY_EUICC_MEP:kotlin.String), it should return more than one [UiccPortInfo](https://developer.android.com/reference/kotlin/android/telephony/UiccPortInfo) object if the card is eUICC.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [UiccPortInfo](https://developer.android.com/reference/kotlin/android/telephony/UiccPortInfo)!> | Collection of [UiccPortInfo](https://developer.android.com/reference/kotlin/android/telephony/UiccPortInfo) This value cannot be`null`. |

### getSlotIndex

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSlotIndex(): Int
```

**Deprecated:** *use [getPhysicalSlotIndex()](https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo#getPhysicalSlotIndex())*

Gets the slot index for the slot that the UICC is currently inserted in. 

### hashCode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isEuicc

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isEuicc(): Boolean
```

Return whether the UICC is an eUICC.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the UICC is an eUICC. |

### isMultipleEnabledProfilesSupported

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isMultipleEnabledProfilesSupported(): Boolean
```  

### isRemovable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isRemovable(): Boolean
```

Return whether the UICC or eUICC is removable.

UICCs are generally removable, but eUICCs may be removable or built in to the device.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the UICC or eUICC is removable |

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
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<UiccCardInfo!>
```
