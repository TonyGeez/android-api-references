# AdSelectionFromOutcomesConfig

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions)

# AdSelectionFromOutcomesConfig

Kotlin| [Java](AdSelectionFromOutcomesConfig.md) 
| --- | --- |

```
class AdSelectionFromOutcomesConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.AdSelectionFromOutcomesConfig](AdSelectionFromOutcomesConfig.md) |

Contains the configuration of the ad selection process that select a winner from a given list of ad selection ids.

Instances of this class are created by SDKs to be provided as arguments to the android.adservices.adselection.AdSelectionManager#selectAds methods in [AdSelectionManager](AdSelectionManager.md).

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/adservices/adselection/AdSelectionFromOutcomesConfig.Builder.md) Builder for [AdSelectionFromOutcomesConfig](AdSelectionFromOutcomesConfig.md) objects. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](AdSelectionFromOutcomesConfig.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](AdSelectionFromOutcomesConfig.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\> | [getAdSelectionIds](AdSelectionFromOutcomesConfig.md))`()` <br /> |
| --- | --- |
| [Uri](../android.net/Uri.md) | [getSelectionLogicUri](AdSelectionFromOutcomesConfig.md))`()` <br /> |
| [AdSelectionSignals](../android.adservices.common/AdSelectionSignals.md) | [getSelectionSignals](AdSelectionFromOutcomesConfig.md))`()` <br /> |
| [AdTechIdentifier](../android.adservices.common/AdTechIdentifier.md) | [getSeller](AdSelectionFromOutcomesConfig.md))`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](AdSelectionFromOutcomesConfig.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](AdSelectionFromOutcomesConfig.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AdSelectionFromOutcomesConfig](AdSelectionFromOutcomesConfig.md)!\> | [CREATOR](AdSelectionFromOutcomesConfig.md) <br /> |

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

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
| [Uri](../android.net/Uri.md) | the URI used to retrieve the JS code containing the seller/SSP`selectOutcome`function used during the ad selection This value cannot be`null`. |

### getSelectionSignals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
fun getSelectionSignals(): AdSelectionSignals
```

| Return ||
|-------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AdSelectionSignals](../android.adservices.common/AdSelectionSignals.md) | JSON in an [AdSelectionSignals](../android.adservices.common/AdSelectionSignals.md) object, fetched from the [AdSelectionFromOutcomesConfig](AdSelectionFromOutcomesConfig.md) and consumed by the JS logic fetched from the DSP`SelectionLogicUri`. This value cannot be`null`. |

### getSeller

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
fun getSeller(): AdTechIdentifier
```

| Return ||
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [AdTechIdentifier](../android.adservices.common/AdTechIdentifier.md) | a AdTechIdentifier of the seller, for example "www.example-ssp.com" This value cannot be`null`. |

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
| `dest` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
static val CREATOR: Parcelable.Creator<AdSelectionFromOutcomesConfig!>
```
