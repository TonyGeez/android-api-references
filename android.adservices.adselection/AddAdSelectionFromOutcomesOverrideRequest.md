# AddAdSelectionFromOutcomesOverrideRequest

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions)

# AddAdSelectionFromOutcomesOverrideRequest

Kotlin| [Java](https://developer.android.com/reference/android/adservices/adselection/AddAdSelectionFromOutcomesOverrideRequest "View this page in Java") 
| --- | --- |

```
open class AddAdSelectionFromOutcomesOverrideRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.AddAdSelectionFromOutcomesOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionFromOutcomesOverrideRequest#) |

This POJO represents the [android.adservices.adselection.TestAdSelectionManager#overrideAdSelectionFromOutcomesConfigRemoteInfo](https://developer.android.com/reference/kotlin/android/adservices/adselection/TestAdSelectionManager#overrideAdSelectionFromOutcomesConfigRemoteInfo(android.adservices.adselection.AddAdSelectionFromOutcomesOverrideRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))( AddAdSelectionOverrideRequest, Executor, OutcomeReceiver)} request

It contains, a [AdSelectionFromOutcomesConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig) which will serve as the identifier for the specific override, a`String`selectionLogicJs and`String`selectionSignals field representing the override value

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AddAdSelectionFromOutcomesOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionFromOutcomesOverrideRequest#AddAdSelectionFromOutcomesOverrideRequest(android.adservices.adselection.AdSelectionFromOutcomesConfig,%20kotlin.String,%20android.adservices.common.AdSelectionSignals))`(`adSelectionFromOutcomesConfig:` ` [AdSelectionFromOutcomesConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig)`, `outcomeSelectionLogicJs:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `outcomeSelectionTrustedSignals:` ` [AdSelectionSignals](https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#)`)` Builds a [AddAdSelectionFromOutcomesOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionFromOutcomesOverrideRequest#) instance. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [AdSelectionFromOutcomesConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig) | [getAdSelectionFromOutcomesConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionFromOutcomesOverrideRequest#getAdSelectionFromOutcomesConfig())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getOutcomeSelectionLogicJs](https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionFromOutcomesOverrideRequest#getOutcomeSelectionLogicJs())`()` <br /> |
| open [AdSelectionSignals](https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#) | [getOutcomeSelectionTrustedSignals](https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionFromOutcomesOverrideRequest#getOutcomeSelectionTrustedSignals())`()` <br /> |
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

Builds a [AddAdSelectionFromOutcomesOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionFromOutcomesOverrideRequest#) instance.

| Parameters ||
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `adSelectionFromOutcomesConfig` | [AdSelectionFromOutcomesConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig):This value cannot be`null`. |
| `outcomeSelectionLogicJs` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `outcomeSelectionTrustedSignals` | [AdSelectionSignals](https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#):This value cannot be`null`. |
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
| [AdSelectionFromOutcomesConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig) | an instance of [AdSelectionFromOutcomesConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig), the configuration of the ad selection process. This configuration provides the data necessary to run Ad Selection flow that generates bids and scores to find a wining ad for rendering. This value cannot be`null`. |

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
| [AdSelectionSignals](https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#) | The override trusted scoring signals, should be a valid json string. The trusted signals would be fed into the outcome selection logic during ad outcome selection. This value cannot be`null`. |
