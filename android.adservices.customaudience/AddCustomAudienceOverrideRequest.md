# AddCustomAudienceOverrideRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# AddCustomAudienceOverrideRequest

Kotlin| [Java](AddCustomAudienceOverrideRequest.md) 
| --- | --- |

```
open class AddCustomAudienceOverrideRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.customaudience.AddCustomAudienceOverrideRequest](AddCustomAudienceOverrideRequest.md) |

This POJO represents the [android.adservices.customaudience.TestCustomAudienceManager#overrideCustomAudienceRemoteInfo(android.adservices.customaudience.AddCustomAudienceOverrideRequest,java.util.concurrent.Executor,android.os.OutcomeReceiver)](TestCustomAudienceManager.md))request.

It contains fields`buyer`and`name`which will serve as the identifier for the override fields,`biddingLogicJs`and`trustedBiddingSignals`, which are used during ad selection instead of querying external servers.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/adservices/customaudience/AddCustomAudienceOverrideRequest.Builder.md) Builder for [AddCustomAudienceOverrideRequest](AddCustomAudienceOverrideRequest.md) objects. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AddCustomAudienceOverrideRequest](AddCustomAudienceOverrideRequest.md))`(`buyer:` ` [AdTechIdentifier](../android.adservices.common/AdTechIdentifier.md)`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `biddingLogicJs:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `trustedBiddingSignals:` ` [AdSelectionSignals](../android.adservices.common/AdSelectionSignals.md)`)` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getBiddingLogicJs](AddCustomAudienceOverrideRequest.md))`()` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getBiddingLogicJsVersion](AddCustomAudienceOverrideRequest.md))`()` Returns the value to return as version for JavaScript bidding logic. |
| open [AdTechIdentifier](../android.adservices.common/AdTechIdentifier.md) | [getBuyer](AddCustomAudienceOverrideRequest.md))`()` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](AddCustomAudienceOverrideRequest.md))`()` <br /> |
| open [AdSelectionSignals](../android.adservices.common/AdSelectionSignals.md) | [getTrustedBiddingSignals](AddCustomAudienceOverrideRequest.md))`()` <br /> |

## Public constructors

### AddCustomAudienceOverrideRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
AddCustomAudienceOverrideRequest(
    buyer: AdTechIdentifier, 
    name: String, 
    biddingLogicJs: String, 
    trustedBiddingSignals: AdSelectionSignals)
```

| Parameters ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `buyer` | [AdTechIdentifier](../android.adservices.common/AdTechIdentifier.md):This value cannot be`null`. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `biddingLogicJs` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| --- | --- |
| `trustedBiddingSignals` | [AdSelectionSignals](../android.adservices.common/AdSelectionSignals.md):This value cannot be`null`. |

## Public methods

### getBiddingLogicJs

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
open fun getBiddingLogicJs(): String
```

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the override JavaScript result that should be served during ad selection This value cannot be`null`. |

### getBiddingLogicJsVersion

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions) 

```
open fun getBiddingLogicJsVersion(): Long
```

Returns the value to return as version for JavaScript bidding logic.

Default to be`0L`, which will fall back to use default version(V1 or V2). 

### getBuyer

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
open fun getBuyer(): AdTechIdentifier
```

| Return ||
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AdTechIdentifier](../android.adservices.common/AdTechIdentifier.md) | an [AdTechIdentifier](../android.adservices.common/AdTechIdentifier.md) representing the buyer This value cannot be`null`. |

### getName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
open fun getName(): String
```

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | name of the custom audience being overridden This value cannot be`null`. |

### getTrustedBiddingSignals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
open fun getTrustedBiddingSignals(): AdSelectionSignals
```

| Return ||
|-------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [AdSelectionSignals](../android.adservices.common/AdSelectionSignals.md) | the override trusted bidding signals that should be served during ad selection This value cannot be`null`. |
