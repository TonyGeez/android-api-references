# PerBuyerDecisionLogic

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions)

# PerBuyerDecisionLogic

Kotlin | [Java](https://developer.android.com/reference/android/adservices/adselection/PerBuyerDecisionLogic "View this page in Java") 
| --- | --- |

```
class PerBuyerDecisionLogic : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.PerBuyerDecisionLogic](https://developer.android.com/reference/kotlin/android/adservices/adselection/PerBuyerDecisionLogic#) |

The override object for decision logic JS per buyer for [SignedContextualAds](https://developer.android.com/reference/kotlin/android/adservices/adselection/SignedContextualAds).

This decision logic is used for reporting when an ad wins from a buyer's bundle of [SignedContextualAds](https://developer.android.com/reference/kotlin/android/adservices/adselection/SignedContextualAds).

This JS code may be extended to updating bid values for contextual ads in the future.

See [CustomAudience.getBiddingLogicUri()](https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience.html#getBiddingLogicUri()).

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PerBuyerDecisionLogic](https://developer.android.com/reference/kotlin/android/adservices/adselection/PerBuyerDecisionLogic#PerBuyerDecisionLogic(kotlin.collections.MutableMap))`(`perBuyerLogicMap:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#)!,` ` [DecisionLogic](https://developer.android.com/reference/kotlin/android/adservices/adselection/DecisionLogic)!>`)` Builds a [PerBuyerDecisionLogic](https://developer.android.com/reference/kotlin/android/adservices/adselection/PerBuyerDecisionLogic#) instance. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/adservices/adselection/PerBuyerDecisionLogic#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/adservices/adselection/PerBuyerDecisionLogic#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#)!, [DecisionLogic](https://developer.android.com/reference/kotlin/android/adservices/adselection/DecisionLogic)!\> | [getPerBuyerLogicMap](https://developer.android.com/reference/kotlin/android/adservices/adselection/PerBuyerDecisionLogic#getPerBuyerLogicMap())`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/adservices/adselection/PerBuyerDecisionLogic#hashCode())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/adservices/adselection/PerBuyerDecisionLogic#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [PerBuyerDecisionLogic](https://developer.android.com/reference/kotlin/android/adservices/adselection/PerBuyerDecisionLogic#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/adservices/adselection/PerBuyerDecisionLogic#CREATOR:android.os.Parcelable.Creator) <br /> |
| static [PerBuyerDecisionLogic](https://developer.android.com/reference/kotlin/android/adservices/adselection/PerBuyerDecisionLogic#) | [EMPTY](https://developer.android.com/reference/kotlin/android/adservices/adselection/PerBuyerDecisionLogic#EMPTY:android.adservices.adselection.PerBuyerDecisionLogic) <br /> |

## Public constructors

### PerBuyerDecisionLogic

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions) 

```
PerBuyerDecisionLogic(perBuyerLogicMap: MutableMap<AdTechIdentifier!, DecisionLogic!>)
```

Builds a [PerBuyerDecisionLogic](https://developer.android.com/reference/kotlin/android/adservices/adselection/PerBuyerDecisionLogic#) instance.

| Parameters ||
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `perBuyerLogicMap` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#)!, [DecisionLogic](https://developer.android.com/reference/kotlin/android/adservices/adselection/DecisionLogic)!\>: map of buyers and their decision logic to be fetched during ad selection This value cannot be `null`. |

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if this object is the same as the obj argument; `false` otherwise. |

### getPerBuyerLogicMap

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions) 

```
fun getPerBuyerLogicMap(): MutableMap<AdTechIdentifier!, DecisionLogic!>
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#)!,` ` [DecisionLogic](https://developer.android.com/reference/kotlin/android/adservices/adselection/DecisionLogic)!> | This value cannot be `null`. |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### writeToParcel

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either `0` or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions) 

```
static val CREATOR: Parcelable.Creator<PerBuyerDecisionLogic!>
```  

### EMPTY

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions) 

```
static val EMPTY: PerBuyerDecisionLogic
```
