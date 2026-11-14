# AvailableNetworkInfo

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AvailableNetworkInfo

Kotlin| [Java](AvailableNetworkInfo.md) 
| --- | --- |

```
class AvailableNetworkInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.AvailableNetworkInfo](AvailableNetworkInfo.md) |

Defines available network information which includes corresponding subscription id, network plmns and corresponding priority to be used for network selection by Opportunistic Network Service when passed through [TelephonyManager.updateAvailableNetworks](TelephonyManager.md))

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/telephony/AvailableNetworkInfo.Builder.md) Provides a convenient way to set the fields of a [AvailableNetworkInfo](AvailableNetworkInfo.md) when creating a new instance. |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PRIORITY_HIGH](AvailableNetworkInfo.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PRIORITY_LOW](AvailableNetworkInfo.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PRIORITY_MED](AvailableNetworkInfo.md) <br /> |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AvailableNetworkInfo](AvailableNetworkInfo.md))`(`subId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `priority:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mccMncs:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`, `bands:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>`)` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](AvailableNetworkInfo.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](AvailableNetworkInfo.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | [getBands](AvailableNetworkInfo.md))`()` Returns the frequency bands that need to be scanned by opportunistic network service The returned value is defined in either of [AccessNetworkConstants.GeranBand](../android/telephony/AccessNetworkConstants.GeranBand.md), [AccessNetworkConstants.UtranBand](../android/telephony/AccessNetworkConstants.UtranBand.md) and [AccessNetworkConstants.EutranBand](../android/telephony/AccessNetworkConstants.EutranBand.md) See [AccessNetworkConstants.AccessNetworkType](../android/telephony/AccessNetworkConstants.AccessNetworkType.md) for details regarding different network types. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getMccMncs](AvailableNetworkInfo.md))`()` Return List of PLMN ids (MCC-MNC) associated with the sub ID. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriority](AvailableNetworkInfo.md))`()` Return priority for the subscription id. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RadioAccessSpecifier](RadioAccessSpecifier.md)!\> | [getRadioAccessSpecifiers](AvailableNetworkInfo.md))`()` Returns a list of [RadioAccessSpecifier](RadioAccessSpecifier.md) associated with the available network. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSubId](AvailableNetworkInfo.md))`()` Return subscription Id of the available network. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](AvailableNetworkInfo.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](AvailableNetworkInfo.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](AvailableNetworkInfo.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AvailableNetworkInfo](AvailableNetworkInfo.md)!\> | [CREATOR](AvailableNetworkInfo.md) <br /> |

## Constants

### PRIORITY_HIGH

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRIORITY_HIGH: Int
```  

 Value: 1

### PRIORITY_LOW

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRIORITY_LOW: Int
```  

 Value: 3

### PRIORITY_MED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRIORITY_MED: Int
```  

 Value: 2

## Public constructors

### AvailableNetworkInfo

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AvailableNetworkInfo(
    subId: Int, 
    priority: Int, 
    mccMncs: MutableList<String!>, 
    bands: MutableList<Int!>)
```

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mccMncs` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:This value cannot be`null`. |
| `bands` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>:This value cannot be`null`. |

## Public methods

### describeContents

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

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

### getBands

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBands(): MutableList<Int!>
```

Returns the frequency bands that need to be scanned by opportunistic network service The returned value is defined in either of [AccessNetworkConstants.GeranBand](../android/telephony/AccessNetworkConstants.GeranBand.md), [AccessNetworkConstants.UtranBand](../android/telephony/AccessNetworkConstants.UtranBand.md) and [AccessNetworkConstants.EutranBand](../android/telephony/AccessNetworkConstants.EutranBand.md) See [AccessNetworkConstants.AccessNetworkType](../android/telephony/AccessNetworkConstants.AccessNetworkType.md) for details regarding different network types. When no specific bands are specified (empty array or null) CBRS band [AccessNetworkConstants.EutranBand.BAND_48](../android/telephony/AccessNetworkConstants.EutranBand.md) will be used for network scan. 

### getMccMncs

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMccMncs(): MutableList<String!>
```

Return List of PLMN ids (MCC-MNC) associated with the sub ID. Opportunistic Network Service will scan and verify specified PLMNs are available. If this entry is left empty, then the Opportunistic Network Service will not scan the network to validate the network availability.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | list of PLMN ids This value cannot be`null`. |

### getPriority

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriority(): Int
```

Return priority for the subscription id. Priorities are in the range of [AvailableNetworkInfo.PRIORITY_LOW](AvailableNetworkInfo.md) to [AvailableNetworkInfo.PRIORITY_HIGH](AvailableNetworkInfo.md) Among all networks available after network scan, subId with highest priority is chosen for network selection. If there are more than one subId with highest priority then the network with highest RSRP is chosen.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | priority level Value is [android.telephony.AvailableNetworkInfo#PRIORITY_HIGH](AvailableNetworkInfo.md), [android.telephony.AvailableNetworkInfo#PRIORITY_MED](AvailableNetworkInfo.md), or [android.telephony.AvailableNetworkInfo#PRIORITY_LOW](AvailableNetworkInfo.md) |

### getRadioAccessSpecifiers

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRadioAccessSpecifiers(): MutableList<RadioAccessSpecifier!>
```

Returns a list of [RadioAccessSpecifier](RadioAccessSpecifier.md) associated with the available network. Opportunistic network service will use this to determine which bands to scan for.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [RadioAccessSpecifier](RadioAccessSpecifier.md)!> | the access network type associated with the available network. This value cannot be`null`. |

### getSubId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSubId(): Int
```

Return subscription Id of the available network. This value must be one of the entry retrieved from [SubscriptionManager.getOpportunisticSubscriptions](SubscriptionManager.md))

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | subscription id |

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
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AvailableNetworkInfo!>
```
