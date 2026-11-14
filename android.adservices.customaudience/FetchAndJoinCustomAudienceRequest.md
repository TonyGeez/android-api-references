# FetchAndJoinCustomAudienceRequest

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions)

# FetchAndJoinCustomAudienceRequest

Kotlin| [Java](FetchAndJoinCustomAudienceRequest.md) 
| --- | --- |

```
class FetchAndJoinCustomAudienceRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.customaudience.FetchAndJoinCustomAudienceRequest](FetchAndJoinCustomAudienceRequest.md) |

The request object wrapping the required and optional parameters needed to fetch a [CustomAudience](CustomAudience.md).

`fetchUri`is the only required parameter. It represents the URI to fetch a custom audience from.`name`,`activationTime`,`expirationTime`and`userBiddingSignals`are optional parameters. They represent a partial custom audience which can be used by the caller to inform the choice of the custom audience the user should be added to. Any field set by the caller cannot be overridden by the custom audience fetched from the`fetchUri`. For more information about each field refer to [CustomAudience](CustomAudience.md).

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/adservices/customaudience/FetchAndJoinCustomAudienceRequest.Builder.md) Builder for [FetchAndJoinCustomAudienceRequest](FetchAndJoinCustomAudienceRequest.md) objects. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](FetchAndJoinCustomAudienceRequest.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Instant](../java.time/Instant.md)? | [getActivationTime](FetchAndJoinCustomAudienceRequest.md))`()` Reference [CustomAudience.getActivationTime()](CustomAudience.md))for details. |
| [Instant](../java.time/Instant.md)? | [getExpirationTime](FetchAndJoinCustomAudienceRequest.md))`()` Reference [CustomAudience.getExpirationTime()](CustomAudience.md))for details. |
| --- | --- |
| [Uri](../android.net/Uri.md) | [getFetchUri](FetchAndJoinCustomAudienceRequest.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getName](FetchAndJoinCustomAudienceRequest.md))`()` Reference [CustomAudience.getName()](CustomAudience.md))for details. |
| [AdSelectionSignals](../android.adservices.common/AdSelectionSignals.md)? | [getUserBiddingSignals](FetchAndJoinCustomAudienceRequest.md))`()` Reference [CustomAudience.getUserBiddingSignals()](CustomAudience.md))for details. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](FetchAndJoinCustomAudienceRequest.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](FetchAndJoinCustomAudienceRequest.md))`()` <br /> |

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
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`only if two [FetchAndJoinCustomAudienceRequest](FetchAndJoinCustomAudienceRequest.md) objects contain the same information. |

### getActivationTime

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
fun getActivationTime(): Instant?
```

Reference [CustomAudience.getActivationTime()](CustomAudience.md))for details.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Instant](../java.time/Instant.md)? | the [Instant](../java.time/Instant.md) by which joining the custom audience will be delayed. This value may be`null`. |

### getExpirationTime

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
fun getExpirationTime(): Instant?
```

Reference [CustomAudience.getExpirationTime()](CustomAudience.md))for details.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Instant](../java.time/Instant.md)? | the [Instant](../java.time/Instant.md) by when the membership to the custom audience will expire. This value may be`null`. |

### getFetchUri

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
fun getFetchUri(): Uri
```

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Uri](../android.net/Uri.md) | the [Uri](../android.net/Uri.md) from which the custom audience is to be fetched. This value cannot be`null`. |

### getName

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
fun getName(): String?
```

Reference [CustomAudience.getName()](CustomAudience.md))for details.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the [String](../java.lang/String.md) name of the custom audience to join. This value may be`null`. |

### getUserBiddingSignals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
fun getUserBiddingSignals(): AdSelectionSignals?
```

Reference [CustomAudience.getUserBiddingSignals()](CustomAudience.md))for details.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AdSelectionSignals](../android.adservices.common/AdSelectionSignals.md)? | the buyer signals to be consumed by the buyer-provided JavaScript when the custom audience participates in an ad selection. This value may be`null`. |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hash of the [FetchAndJoinCustomAudienceRequest](FetchAndJoinCustomAudienceRequest.md) object's data. |

### toString

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a human-readable representation of [FetchAndJoinCustomAudienceRequest](FetchAndJoinCustomAudienceRequest.md). |
