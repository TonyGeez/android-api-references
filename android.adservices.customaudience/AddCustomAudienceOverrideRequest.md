# AddCustomAudienceOverrideRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# AddCustomAudienceOverrideRequest

Kotlin| [Java](https://developer.android.com/reference/android/adservices/customaudience/AddCustomAudienceOverrideRequest "View this page in Java") 

```
open class AddCustomAudienceOverrideRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.adservices.customaudience.AddCustomAudienceOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/AddCustomAudienceOverrideRequest#) |

This POJO represents the [android.adservices.customaudience.TestCustomAudienceManager#overrideCustomAudienceRemoteInfo(android.adservices.customaudience.AddCustomAudienceOverrideRequest,java.util.concurrent.Executor,android.os.OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/adservices/customaudience/TestCustomAudienceManager#overrideCustomAudienceRemoteInfo(android.adservices.customaudience.AddCustomAudienceOverrideRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))request.

It contains fields`buyer`and`name`which will serve as the identifier for the override fields,`biddingLogicJs`and`trustedBiddingSignals`, which are used during ad selection instead of querying external servers.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/adservices/customaudience/AddCustomAudienceOverrideRequest.Builder) Builder for [AddCustomAudienceOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/AddCustomAudienceOverrideRequest#) objects. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AddCustomAudienceOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/AddCustomAudienceOverrideRequest#AddCustomAudienceOverrideRequest(android.adservices.common.AdTechIdentifier,%20kotlin.String,%20kotlin.String,%20android.adservices.common.AdSelectionSignals))`(`buyer:` ` [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#)`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `biddingLogicJs:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `trustedBiddingSignals:` ` [AdSelectionSignals](https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#)`)` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getBiddingLogicJs](https://developer.android.com/reference/kotlin/android/adservices/customaudience/AddCustomAudienceOverrideRequest#getBiddingLogicJs())`()` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getBiddingLogicJsVersion](https://developer.android.com/reference/kotlin/android/adservices/customaudience/AddCustomAudienceOverrideRequest#getBiddingLogicJsVersion())`()` Returns the value to return as version for JavaScript bidding logic. |
| open [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#) | [getBuyer](https://developer.android.com/reference/kotlin/android/adservices/customaudience/AddCustomAudienceOverrideRequest#getBuyer())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](https://developer.android.com/reference/kotlin/android/adservices/customaudience/AddCustomAudienceOverrideRequest#getName())`()` <br /> |
| open [AdSelectionSignals](https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#) | [getTrustedBiddingSignals](https://developer.android.com/reference/kotlin/android/adservices/customaudience/AddCustomAudienceOverrideRequest#getTrustedBiddingSignals())`()` <br /> |

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
| `buyer` | [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#):This value cannot be`null`. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `biddingLogicJs` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `trustedBiddingSignals` | [AdSelectionSignals](https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#):This value cannot be`null`. |

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
| [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#) | an [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#) representing the buyer This value cannot be`null`. |

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
| [AdSelectionSignals](https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#) | the override trusted bidding signals that should be served during ad selection This value cannot be`null`. |
