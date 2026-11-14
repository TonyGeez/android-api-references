# AdSelectionFromOutcomesConfig

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions)

# AdSelectionFromOutcomesConfig

Kotlin| [Java](https://developer.android.com/reference/android/adservices/adselection/AdSelectionFromOutcomesConfig "View this page in Java") 
| --- | --- |

```
class AdSelectionFromOutcomesConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.AdSelectionFromOutcomesConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig#) |

Contains the configuration of the ad selection process that select a winner from a given list of ad selection ids.

Instances of this class are created by SDKs to be provided as arguments to the android.adservices.adselection.AdSelectionManager#selectAds methods in [AdSelectionManager](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager).

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig.Builder) Builder for [AdSelectionFromOutcomesConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig#) objects. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\> | [getAdSelectionIds](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig#getAdSelectionIds())`()` <br /> |
| --- | --- |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | [getSelectionLogicUri](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig#getSelectionLogicUri())`()` <br /> |
| [AdSelectionSignals](https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#) | [getSelectionSignals](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig#getSelectionSignals())`()` <br /> |
| [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#) | [getSeller](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig#getSeller())`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig#hashCode())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AdSelectionFromOutcomesConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAdSelectionIds

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
fun getAdSelectionIds(): MutableList<Long!>
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!> | a list of ad selection ids passed by the SSP to participate in the ad selection from outcomes process This value cannot be`null`. |

### getSelectionLogicUri

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
fun getSelectionLogicUri(): Uri
```

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | the URI used to retrieve the JS code containing the seller/SSP`selectOutcome`function used during the ad selection This value cannot be`null`. |

### getSelectionSignals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
fun getSelectionSignals(): AdSelectionSignals
```

| Return ||
|-------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AdSelectionSignals](https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#) | JSON in an [AdSelectionSignals](https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#) object, fetched from the [AdSelectionFromOutcomesConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig#) and consumed by the JS logic fetched from the DSP`SelectionLogicUri`. This value cannot be`null`. |

### getSeller

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
fun getSeller(): AdTechIdentifier
```

| Return ||
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#) | a AdTechIdentifier of the seller, for example "www.example-ssp.com" This value cannot be`null`. |

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
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
static val CREATOR: Parcelable.Creator<AdSelectionFromOutcomesConfig!>
```
