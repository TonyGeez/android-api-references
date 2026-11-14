# AdSelectionOutcome

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# AdSelectionOutcome

Kotlin| [Java](https://developer.android.com/reference/android/adservices/adselection/AdSelectionOutcome "View this page in Java") 

```
open class AdSelectionOutcome
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.adservices.adselection.AdSelectionOutcome](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome#) |

This class represents a field in the`OutcomeReceiver`, which is an input to the android.adservices.adselection.AdSelectionManager#selectAds in the [AdSelectionManager](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager). This field is populated in the case of a successful android.adservices.adselection.AdSelectionManager#selectAds call.

Empty outcome may be returned from [android.adservices.adselection.AdSelectionManager#selectAds(android.adservices.adselection.AdSelectionFromOutcomesConfig,java.util.concurrent.Executor,android.os.OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#selectAds(android.adservices.adselection.AdSelectionFromOutcomesConfig,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)). Use [AdSelectionOutcome.hasOutcome()](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome#hasOutcome())to check if an instance has a valid outcome. When [android.adservices.adselection.AdSelectionOutcome#hasOutcome()](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome#hasOutcome())returns`false`, results from [getAdSelectionId()](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome#) and [AdSelectionOutcome.getRenderUri()](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome#getRenderUri())are invalid and shouldn't be used.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome.Builder) Builder for [AdSelectionOutcome](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome#) objects. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAdSelectionId](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome#getAdSelectionId())`()` Returns the adSelectionId that identifies the AdSelection. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\> | [getComponentAdUris](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome#getComponentAdUris())`()` Returns the ad component renderUris that are returned by this auction. |
| open [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | [getRenderUri](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome#getRenderUri())`()` Returns the renderUri that the AdSelection returns. |
| open [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#) | [getWinningSeller](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome#getWinningSeller())`()` Returns the willing seller that won the auction. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasOutcome](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome#hasOutcome())`()` Returns whether the outcome contains results or empty. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome#hashCode())`()` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [AdSelectionOutcome](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome#) | [NO_OUTCOME](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome#NO_OUTCOME:android.adservices.adselection.AdSelectionOutcome) Represents an AdSelectionOutcome with empty results. |

## Public methods

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAdSelectionId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
open fun getAdSelectionId(): Long
```

Returns the adSelectionId that identifies the AdSelection.

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | This value cannot be`null`. |

### getComponentAdUris

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 16](https://developer.android.com/sdkExtensions) 

```
open fun getComponentAdUris(): MutableList<Uri!>
```

Returns the ad component renderUris that are returned by this auction.

These URIs represent individual components of a multi-part ad creative. Seller ad tech SDKs are expected to fetch and render these components in their ad display logic.

This approach allows for flexible and dynamic ad creatives where different parts of the ad can be loaded and rendered independently.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!> | This value cannot be`null`. |

### getRenderUri

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
open fun getRenderUri(): Uri
```

Returns the renderUri that the AdSelection returns.

| Return ||
|-----------------------------------------------------------------------------|-----------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | This value cannot be`null`. |

### getWinningSeller

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 18](https://developer.android.com/sdkExtensions) 

```
open fun getWinningSeller(): AdTechIdentifier
```

Returns the willing seller that won the auction.

| Return ||
|---------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#) | This value cannot be`null`. |

### hasOutcome

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
open fun hasOutcome(): Boolean
```

Returns whether the outcome contains results or empty. Empty outcomes'`render uris`shouldn't be used. 

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

## Properties

### NO_OUTCOME

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
static val NO_OUTCOME: AdSelectionOutcome
```

Represents an AdSelectionOutcome with empty results.
