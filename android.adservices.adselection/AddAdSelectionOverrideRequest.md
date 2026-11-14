Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AddAdSelectionOverrideRequest

```
open class AddAdSelectionOverrideRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.AddAdSelectionOverrideRequest](../android/adservices/adselection/AddAdSelectionOverrideRequest.md) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The Rubidium (Rb) Relevance APIs, including those in android.adservices.adselection, are being deprecated. Relevance APIs have no direct replacement. Developers should stop using them, as calls will be rejected in future Android releases. Please refer to official Privacy Sandbox documentation for deprecation and roadmap details: https://privacysandbox.com/news/update-on-plans-for-privacy-sandbox-technologies/

This POJO represents the `https://developer.android.com/reference/kotlin/android/adservices/adselection/TestAdSelectionManager#overrideAdSelectionConfigRemoteInfo(android.adservices.adselection.AddAdSelectionOverrideRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` request

It contains, a `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig` which will serve as the identifier for the specific override, a `String` decisionLogicJs and `String` trustedScoringSignals field representing the override value

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionOverrideRequest#AddAdSelectionOverrideRequest(android.adservices.adselection.AdSelectionConfig,%20kotlin.String,%20android.adservices.common.AdSelectionSignals)(adSelectionConfig: https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig, decisionLogicJs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, trustedScoringSignals: https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#)` Builds a `https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionOverrideRequest#` instance. |
| `https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionOverrideRequest#AddAdSelectionOverrideRequest(android.adservices.adselection.AdSelectionConfig,%20kotlin.String,%20android.adservices.common.AdSelectionSignals,%20android.adservices.adselection.PerBuyerDecisionLogic)(adSelectionConfig: https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig, decisionLogicJs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, trustedScoringSignals: https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#, perBuyerDecisionLogic: https://developer.android.com/reference/kotlin/android/adservices/adselection/PerBuyerDecisionLogic)` Builds a `https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionOverrideRequest#` instance. |

| Public methods ||
|---|---|
| open [AdSelectionConfig](../android/adservices/adselection/AdSelectionConfig.md) | `https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionOverrideRequest#getAdSelectionConfig()()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionOverrideRequest#getDecisionLogicJs()()` <br /> |
| open [PerBuyerDecisionLogic](../android/adservices/adselection/PerBuyerDecisionLogic.md) | `https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionOverrideRequest#getPerBuyerDecisionLogic()()` <br /> |
| --- | --- |
| open [AdSelectionSignals](../android/adservices/common/AdSelectionSignals.md) | `https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionOverrideRequest#getTrustedScoringSignals()()` <br /> |

## Public constructors

### AddAdSelectionOverrideRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions)

```
AddAdSelectionOverrideRequest(
    adSelectionConfig: AdSelectionConfig, 
    decisionLogicJs: String, 
    trustedScoringSignals: AdSelectionSignals)
```

Builds a `https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionOverrideRequest#` instance.

| Parameters ||
|---|---|
| `adSelectionConfig` | [AdSelectionConfig](../android/adservices/adselection/AdSelectionConfig.md): configuration for ad selection. See `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig` This value cannot be `null`. |
| `decisionLogicJs` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): override for scoring logic. See `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig#getDecisionLogicUri()` This value cannot be `null`. |
| `trustedScoringSignals` | [AdSelectionSignals](../android/adservices/common/AdSelectionSignals.md): override for trusted seller signals. See `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig#getTrustedScoringSignalsUri()` This value cannot be `null`. |
| --- | --- |

### AddAdSelectionOverrideRequest

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions)

```
AddAdSelectionOverrideRequest(
    adSelectionConfig: AdSelectionConfig, 
    decisionLogicJs: String, 
    trustedScoringSignals: AdSelectionSignals, 
    perBuyerDecisionLogic: PerBuyerDecisionLogic)
```

Builds a `https://developer.android.com/reference/kotlin/android/adservices/adselection/AddAdSelectionOverrideRequest#` instance.

| Parameters ||
|---|---|
| `adSelectionConfig` | [AdSelectionConfig](../android/adservices/adselection/AdSelectionConfig.md): configuration for ad selection. See `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig` This value cannot be `null`. |
| `decisionLogicJs` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): override for scoring logic. See `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig#getDecisionLogicUri()` This value cannot be `null`. |
| `trustedScoringSignals` | [AdSelectionSignals](../android/adservices/common/AdSelectionSignals.md): override for trusted seller signals. See `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig#getTrustedScoringSignalsUri()` This value cannot be `null`. |
| --- | --- |
| `perBuyerDecisionLogic` | [PerBuyerDecisionLogic](../android/adservices/adselection/PerBuyerDecisionLogic.md): override for buyer's reporting logic for contextual ads. See `https://developer.android.com/reference/kotlin/android/adservices/adselection/SignedContextualAds#getDecisionLogicUri()` This value cannot be `null`. |

## Public methods

### getAdSelectionConfig

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAdSelectionConfig(): AdSelectionConfig
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig` | an instance of `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig`, the configuration of the ad selection process. This configuration provides the data necessary to run Ad Selection flow that generates bids and scores to find a wining ad for rendering. This value cannot be `null`. |

### getDecisionLogicJs

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDecisionLogicJs(): String
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The override javascript result, should be a string that contains valid JS code. The code should contain the scoring logic that will be executed during Ad selection. This value cannot be `null`. |

### getPerBuyerDecisionLogic

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPerBuyerDecisionLogic(): PerBuyerDecisionLogic
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/adservices/adselection/PerBuyerDecisionLogic` | The override for the decision logic for each buyer that is used by contextual ads for reporting, which may be extended to updating bid values for contextual ads in the future. This value cannot be `null`. |

### getTrustedScoringSignals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTrustedScoringSignals(): AdSelectionSignals
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#` | The override trusted scoring signals, should be a valid json string. The trusted signals would be fed into the scoring logic during Ad Selection. This value cannot be `null`. |
