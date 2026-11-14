# AddAdSelectionFromOutcomesOverrideRequest

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions)

# AddAdSelectionFromOutcomesOverrideRequest

Kotlin| [Java](AddAdSelectionFromOutcomesOverrideRequest.md) 
| --- | --- |

```
open class AddAdSelectionFromOutcomesOverrideRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.AddAdSelectionFromOutcomesOverrideRequest](AddAdSelectionFromOutcomesOverrideRequest.md) |

This POJO represents the [android.adservices.adselection.TestAdSelectionManager#overrideAdSelectionFromOutcomesConfigRemoteInfo](TestAdSelectionManager.md))( AddAdSelectionOverrideRequest, Executor, OutcomeReceiver)} request

It contains, a [AdSelectionFromOutcomesConfig](AdSelectionFromOutcomesConfig.md) which will serve as the identifier for the specific override, a`String`selectionLogicJs and`String`selectionSignals field representing the override value

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AddAdSelectionFromOutcomesOverrideRequest](AddAdSelectionFromOutcomesOverrideRequest.md))`(`adSelectionFromOutcomesConfig:` ` [AdSelectionFromOutcomesConfig](AdSelectionFromOutcomesConfig.md)`, `outcomeSelectionLogicJs:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `outcomeSelectionTrustedSignals:` ` [AdSelectionSignals](../android.adservices.common/AdSelectionSignals.md)`)` Builds a [AddAdSelectionFromOutcomesOverrideRequest](AddAdSelectionFromOutcomesOverrideRequest.md) instance. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [AdSelectionFromOutcomesConfig](AdSelectionFromOutcomesConfig.md) | [getAdSelectionFromOutcomesConfig](AddAdSelectionFromOutcomesOverrideRequest.md))`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getOutcomeSelectionLogicJs](AddAdSelectionFromOutcomesOverrideRequest.md))`()` <br /> |
| open [AdSelectionSignals](../android.adservices.common/AdSelectionSignals.md) | [getOutcomeSelectionTrustedSignals](AddAdSelectionFromOutcomesOverrideRequest.md))`()` <br /> |
| --- | --- |

## Public constructors

### AddAdSelectionFromOutcomesOverrideRequest

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
AddAdSelectionFromOutcomesOverrideRequest(
    adSelectionFromOutcomesConfig: AdSelectionFromOutcomesConfig, 
    outcomeSelectionLogicJs: String, 
    outcomeSelectionTrustedSignals: AdSelectionSignals)
```

Builds a [AddAdSelectionFromOutcomesOverrideRequest](AddAdSelectionFromOutcomesOverrideRequest.md) instance.

| Parameters ||
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `adSelectionFromOutcomesConfig` | [AdSelectionFromOutcomesConfig](AdSelectionFromOutcomesConfig.md):This value cannot be`null`. |
| `outcomeSelectionLogicJs` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `outcomeSelectionTrustedSignals` | [AdSelectionSignals](../android.adservices.common/AdSelectionSignals.md):This value cannot be`null`. |
| --- | --- |

## Public methods

### getAdSelectionFromOutcomesConfig

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
open fun getAdSelectionFromOutcomesConfig(): AdSelectionFromOutcomesConfig
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AdSelectionFromOutcomesConfig](AdSelectionFromOutcomesConfig.md) | an instance of [AdSelectionFromOutcomesConfig](AdSelectionFromOutcomesConfig.md), the configuration of the ad selection process. This configuration provides the data necessary to run Ad Selection flow that generates bids and scores to find a wining ad for rendering. This value cannot be`null`. |

### getOutcomeSelectionLogicJs

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
open fun getOutcomeSelectionLogicJs(): String
```

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The override javascript result, should be a string that contains valid JS code. The code should contain the outcome selection logic that will be executed during ad outcome selection. This value cannot be`null`. |

### getOutcomeSelectionTrustedSignals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
open fun getOutcomeSelectionTrustedSignals(): AdSelectionSignals
```

| Return ||
|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AdSelectionSignals](../android.adservices.common/AdSelectionSignals.md) | The override trusted scoring signals, should be a valid json string. The trusted signals would be fed into the outcome selection logic during ad outcome selection. This value cannot be`null`. |
