# AdSelectionConfig

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# AdSelectionConfig

Kotlin| [Java](https://developer.android.com/reference/android/adservices/adselection/AdSelectionConfig "View this page in Java") 
| --- | --- |

```
class AdSelectionConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.AdSelectionConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig#) |

Contains the configuration of the ad selection process.

Instances of this class are created by SDKs to be provided as arguments to the android.adservices.adselection.AdSelectionManager#selectAds and [AdSelectionManager.reportImpression](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#reportImpression(android.adservices.adselection.ReportImpressionRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))methods in [AdSelectionManager](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager).

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig.Builder) Builder for [AdSelectionConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig#) object. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [AdSelectionSignals](https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#) | [getAdSelectionSignals](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig#getAdSelectionSignals())`()` <br /> |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#)!\> | [getCustomAudienceBuyers](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig#getCustomAudienceBuyers())`()` <br /> |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | [getDecisionLogicUri](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig#getDecisionLogicUri())`()` <br /> |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#)!, [AdSelectionSignals](https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#)!\> | [getPerBuyerSignals](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig#getPerBuyerSignals())`()` <br /> |
| --- | --- |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#)!, [SignedContextualAds](https://developer.android.com/reference/kotlin/android/adservices/adselection/SignedContextualAds)!\> | [getPerBuyerSignedContextualAds](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig#getPerBuyerSignedContextualAds())`()` <br /> |
| [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#) | [getSeller](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig#getSeller())`()` <br /> |
| [AdSelectionSignals](https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#) | [getSellerSignals](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig#getSellerSignals())`()` <br /> |
| --- | --- |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | [getTrustedScoringSignalsUri](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig#getTrustedScoringSignalsUri())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig#hashCode())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AdSelectionConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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
| [AdSelectionSignals](https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#) | JSON in an AdSelectionSignals object, fetched from the AdSelectionConfig and consumed by the JS logic fetched from the DSP, represents signals given to the participating buyers in the ad selection and reporting processes. This value cannot be`null`. |

### getCustomAudienceBuyers

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
fun getCustomAudienceBuyers(): MutableList<AdTechIdentifier!>
```

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#)!> | a list of custom audience buyers allowed by the SSP to participate in the ad selection process This value cannot be`null`. |

### getDecisionLogicUri

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
fun getDecisionLogicUri(): Uri
```

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | the URI used to retrieve the JS code containing the seller/SSP scoreAd function used during the ad selection and reporting processes This value cannot be`null`. |

### getPerBuyerSignals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
fun getPerBuyerSignals(): MutableMap<AdTechIdentifier!, AdSelectionSignals!>
```

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#)!,` ` [AdSelectionSignals](https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#)!> | a Map of buyers and AdSelectionSignals, fetched from the AdSelectionConfig and consumed by the JS logic fetched from the DSP, representing any information that each buyer would provide during ad selection to participants (such as bid floor, ad selection type, etc.) This value cannot be`null`. |

### getPerBuyerSignedContextualAds

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions) 

```
fun getPerBuyerSignedContextualAds(): MutableMap<AdTechIdentifier!, SignedContextualAds!>
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#)!,` ` [SignedContextualAds](https://developer.android.com/reference/kotlin/android/adservices/adselection/SignedContextualAds)!> | a Map of buyers and corresponding Contextual Ads, these ads are expected to be pre-downloaded from the contextual path and injected into Ad Selection. This value cannot be`null`. |

### getSeller

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
fun getSeller(): AdTechIdentifier
```

| Return ||
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#) | a AdTechIdentifier of the seller, for example "www.example-ssp.com" This value cannot be`null`. |

### getSellerSignals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
fun getSellerSignals(): AdSelectionSignals
```

| Return ||
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AdSelectionSignals](https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#) | JSON in an AdSelectionSignals object, provided by the SSP and consumed by the JS logic fetched from the SSP, represents any information that the SSP used in the ad scoring process to tweak the results of the ad selection process (e.g. brand safety checks, excluded contextual ads). This value cannot be`null`. |

### getTrustedScoringSignalsUri

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
fun getTrustedScoringSignalsUri(): Uri
```

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | URI endpoint of sell-side trusted signal from which creative specific realtime information can be fetched from. This value cannot be`null`. |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
static val CREATOR: Parcelable.Creator<AdSelectionConfig!>
```
