# AdSelectionConfig

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# AdSelectionConfig

Kotlin| [Java](../android/adservices/adselection/AdSelectionConfig.md) 
| --- | --- |

```
class AdSelectionConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.AdSelectionConfig](../android/adservices/adselection/AdSelectionConfig.md) |

Contains the configuration of the ad selection process.

Instances of this class are created by SDKs to be provided as arguments to the android.adservices.adselection.AdSelectionManager#selectAds and [AdSelectionManager.reportImpression](../android/adservices/adselection/AdSelectionManager.md))methods in [AdSelectionManager](../android/adservices/adselection/AdSelectionManager.md).

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/adservices/adselection/AdSelectionConfig.Builder.md) Builder for [AdSelectionConfig](../android/adservices/adselection/AdSelectionConfig.md) object. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/adservices/adselection/AdSelectionConfig.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/adservices/adselection/AdSelectionConfig.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [AdSelectionSignals](../android/adservices/common/AdSelectionSignals.md) | [getAdSelectionSignals](../android/adservices/adselection/AdSelectionConfig.md))`()` <br /> |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AdTechIdentifier](../android/adservices/common/AdTechIdentifier.md)!\> | [getCustomAudienceBuyers](../android/adservices/adselection/AdSelectionConfig.md))`()` <br /> |
| [Uri](../android/net/Uri.md) | [getDecisionLogicUri](../android/adservices/adselection/AdSelectionConfig.md))`()` <br /> |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [AdTechIdentifier](../android/adservices/common/AdTechIdentifier.md)!, [AdSelectionSignals](../android/adservices/common/AdSelectionSignals.md)!\> | [getPerBuyerSignals](../android/adservices/adselection/AdSelectionConfig.md))`()` <br /> |
| --- | --- |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [AdTechIdentifier](../android/adservices/common/AdTechIdentifier.md)!, [SignedContextualAds](../android/adservices/adselection/SignedContextualAds.md)!\> | [getPerBuyerSignedContextualAds](../android/adservices/adselection/AdSelectionConfig.md))`()` <br /> |
| [AdTechIdentifier](../android/adservices/common/AdTechIdentifier.md) | [getSeller](../android/adservices/adselection/AdSelectionConfig.md))`()` <br /> |
| [AdSelectionSignals](../android/adservices/common/AdSelectionSignals.md) | [getSellerSignals](../android/adservices/adselection/AdSelectionConfig.md))`()` <br /> |
| --- | --- |
| [Uri](../android/net/Uri.md) | [getTrustedScoringSignalsUri](../android/adservices/adselection/AdSelectionConfig.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/adservices/adselection/AdSelectionConfig.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/adservices/adselection/AdSelectionConfig.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AdSelectionConfig](../android/adservices/adselection/AdSelectionConfig.md)!\> | [CREATOR](../android/adservices/adselection/AdSelectionConfig.md) <br /> |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAdSelectionSignals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
fun getAdSelectionSignals(): AdSelectionSignals
```

| Return ||
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AdSelectionSignals](../android/adservices/common/AdSelectionSignals.md) | JSON in an AdSelectionSignals object, fetched from the AdSelectionConfig and consumed by the JS logic fetched from the DSP, represents signals given to the participating buyers in the ad selection and reporting processes. This value cannot be`null`. |

### getCustomAudienceBuyers

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
fun getCustomAudienceBuyers(): MutableList<AdTechIdentifier!>
```

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AdTechIdentifier](../android/adservices/common/AdTechIdentifier.md)!> | a list of custom audience buyers allowed by the SSP to participate in the ad selection process This value cannot be`null`. |

### getDecisionLogicUri

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
fun getDecisionLogicUri(): Uri
```

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Uri](../android/net/Uri.md) | the URI used to retrieve the JS code containing the seller/SSP scoreAd function used during the ad selection and reporting processes This value cannot be`null`. |

### getPerBuyerSignals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
fun getPerBuyerSignals(): MutableMap<AdTechIdentifier!, AdSelectionSignals!>
```

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [AdTechIdentifier](../android/adservices/common/AdTechIdentifier.md)!,` ` [AdSelectionSignals](../android/adservices/common/AdSelectionSignals.md)!> | a Map of buyers and AdSelectionSignals, fetched from the AdSelectionConfig and consumed by the JS logic fetched from the DSP, representing any information that each buyer would provide during ad selection to participants (such as bid floor, ad selection type, etc.) This value cannot be`null`. |

### getPerBuyerSignedContextualAds

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions) 

```
fun getPerBuyerSignedContextualAds(): MutableMap<AdTechIdentifier!, SignedContextualAds!>
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [AdTechIdentifier](../android/adservices/common/AdTechIdentifier.md)!,` ` [SignedContextualAds](../android/adservices/adselection/SignedContextualAds.md)!> | a Map of buyers and corresponding Contextual Ads, these ads are expected to be pre-downloaded from the contextual path and injected into Ad Selection. This value cannot be`null`. |

### getSeller

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
fun getSeller(): AdTechIdentifier
```

| Return ||
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [AdTechIdentifier](../android/adservices/common/AdTechIdentifier.md) | a AdTechIdentifier of the seller, for example "www.example-ssp.com" This value cannot be`null`. |

### getSellerSignals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
fun getSellerSignals(): AdSelectionSignals
```

| Return ||
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AdSelectionSignals](../android/adservices/common/AdSelectionSignals.md) | JSON in an AdSelectionSignals object, provided by the SSP and consumed by the JS logic fetched from the SSP, represents any information that the SSP used in the ad scoring process to tweak the results of the ad selection process (e.g. brand safety checks, excluded contextual ads). This value cannot be`null`. |

### getTrustedScoringSignalsUri

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
fun getTrustedScoringSignalsUri(): Uri
```

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Uri](../android/net/Uri.md) | URI endpoint of sell-side trusted signal from which creative specific realtime information can be fetched from. This value cannot be`null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
static val CREATOR: Parcelable.Creator<AdSelectionConfig!>
```
