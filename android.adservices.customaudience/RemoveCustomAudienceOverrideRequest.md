Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RemoveCustomAudienceOverrideRequest

```
open class RemoveCustomAudienceOverrideRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.adservices.customaudience.RemoveCustomAudienceOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/customaudience/RemoveCustomAudienceOverrideRequest#) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The Rubidium (Rb) Relevance APIs, including those in android.adservices.customaudience, are being deprecated. Relevance APIs have no direct replacement. Developers should stop using them, as calls will be rejected in future Android releases. Please refer to official Privacy Sandbox documentation for deprecation and roadmap details: https://privacysandbox.com/news/update-on-plans-for-privacy-sandbox-technologies/

This POJO represents the `https://developer.android.com/reference/kotlin/android/adservices/customaudience/TestCustomAudienceManager#removeCustomAudienceRemoteInfoOverride(android.adservices.customaudience.RemoveCustomAudienceOverrideRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` request.

It contains fields `buyer` and `name` which will serve as the identifier for the overrides to be removed.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/adservices/customaudience/RemoveCustomAudienceOverrideRequest.Builder` Builder for `https://developer.android.com/reference/kotlin/android/adservices/customaudience/RemoveCustomAudienceOverrideRequest#` objects. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/adservices/customaudience/RemoveCustomAudienceOverrideRequest#RemoveCustomAudienceOverrideRequest(android.adservices.common.AdTechIdentifier,%20kotlin.String)(buyer: https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` <br /> |

| Public methods ||
|---|---|
| open [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#) | `https://developer.android.com/reference/kotlin/android/adservices/customaudience/RemoveCustomAudienceOverrideRequest#getBuyer()()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/customaudience/RemoveCustomAudienceOverrideRequest#getName()()` <br /> |

## Public constructors

### RemoveCustomAudienceOverrideRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

```
RemoveCustomAudienceOverrideRequest(
    buyer: AdTechIdentifier, 
    name: String)
```

| Parameters ||
|---|---|
| `buyer` | [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#): This value cannot be `null`. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

## Public methods

### getBuyer

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBuyer(): AdTechIdentifier
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#` | an `https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#` representing the buyer. This value cannot be `null`. |

### getName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getName(): String
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | name of the custom audience being overridden. This value cannot be `null`. |
