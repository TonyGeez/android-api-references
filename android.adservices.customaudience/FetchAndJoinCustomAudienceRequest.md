# FetchAndJoinCustomAudienceRequest

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions)

# FetchAndJoinCustomAudienceRequest

Kotlin| [Java](https://developer.android.com/reference/android/adservices/customaudience/FetchAndJoinCustomAudienceRequest "View this page in Java") 
| --- | --- |

```
class FetchAndJoinCustomAudienceRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.customaudience.FetchAndJoinCustomAudienceRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/FetchAndJoinCustomAudienceRequest#) |

The request object wrapping the required and optional parameters needed to fetch a [CustomAudience](https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience).

`fetchUri`is the only required parameter. It represents the URI to fetch a custom audience from.`name`,`activationTime`,`expirationTime`and`userBiddingSignals`are optional parameters. They represent a partial custom audience which can be used by the caller to inform the choice of the custom audience the user should be added to. Any field set by the caller cannot be overridden by the custom audience fetched from the`fetchUri`. For more information about each field refer to [CustomAudience](https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience).

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/adservices/customaudience/FetchAndJoinCustomAudienceRequest.Builder) Builder for [FetchAndJoinCustomAudienceRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/FetchAndJoinCustomAudienceRequest#) objects. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/adservices/customaudience/FetchAndJoinCustomAudienceRequest#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)? | [getActivationTime](https://developer.android.com/reference/kotlin/android/adservices/customaudience/FetchAndJoinCustomAudienceRequest#getActivationTime())`()` Reference [CustomAudience.getActivationTime()](https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience#getActivationTime())for details. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)? | [getExpirationTime](https://developer.android.com/reference/kotlin/android/adservices/customaudience/FetchAndJoinCustomAudienceRequest#getExpirationTime())`()` Reference [CustomAudience.getExpirationTime()](https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience#getExpirationTime())for details. |
| --- | --- |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | [getFetchUri](https://developer.android.com/reference/kotlin/android/adservices/customaudience/FetchAndJoinCustomAudienceRequest#getFetchUri())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getName](https://developer.android.com/reference/kotlin/android/adservices/customaudience/FetchAndJoinCustomAudienceRequest#getName())`()` Reference [CustomAudience.getName()](https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience#getName())for details. |
| [AdSelectionSignals](https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#)? | [getUserBiddingSignals](https://developer.android.com/reference/kotlin/android/adservices/customaudience/FetchAndJoinCustomAudienceRequest#getUserBiddingSignals())`()` Reference [CustomAudience.getUserBiddingSignals()](https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience#getUserBiddingSignals())for details. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/adservices/customaudience/FetchAndJoinCustomAudienceRequest#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/adservices/customaudience/FetchAndJoinCustomAudienceRequest#toString())`()` <br /> |

## Public methods

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`only if two [FetchAndJoinCustomAudienceRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/FetchAndJoinCustomAudienceRequest#) objects contain the same information. |

### getActivationTime

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
fun getActivationTime(): Instant?
```

Reference [CustomAudience.getActivationTime()](https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience#getActivationTime())for details.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)? | the [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#) by which joining the custom audience will be delayed. This value may be`null`. |

### getExpirationTime

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
fun getExpirationTime(): Instant?
```

Reference [CustomAudience.getExpirationTime()](https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience#getExpirationTime())for details.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)? | the [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#) by when the membership to the custom audience will expire. This value may be`null`. |

### getFetchUri

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
fun getFetchUri(): Uri
```

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | the [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) from which the custom audience is to be fetched. This value cannot be`null`. |

### getName

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
fun getName(): String?
```

Reference [CustomAudience.getName()](https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience#getName())for details.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) name of the custom audience to join. This value may be`null`. |

### getUserBiddingSignals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
fun getUserBiddingSignals(): AdSelectionSignals?
```

Reference [CustomAudience.getUserBiddingSignals()](https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience#getUserBiddingSignals())for details.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AdSelectionSignals](https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#)? | the buyer signals to be consumed by the buyer-provided JavaScript when the custom audience participates in an ad selection. This value may be`null`. |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hash of the [FetchAndJoinCustomAudienceRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/FetchAndJoinCustomAudienceRequest#) object's data. |

### toString

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a human-readable representation of [FetchAndJoinCustomAudienceRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/FetchAndJoinCustomAudienceRequest#). |
