Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RemoveAdSelectionOverrideRequest

```
open class RemoveAdSelectionOverrideRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.RemoveAdSelectionOverrideRequest](RemoveAdSelectionOverrideRequest.md) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The Rubidium (Rb) Relevance APIs, including those in android.adservices.adselection, are being deprecated. Relevance APIs have no direct replacement. Developers should stop using them, as calls will be rejected in future Android releases. Please refer to official Privacy Sandbox documentation for deprecation and roadmap details: https://privacysandbox.com/news/update-on-plans-for-privacy-sandbox-technologies/

This POJO represents the `https://developer.android.com/reference/kotlin/android/adservices/adselection/TestAdSelectionManager#removeAdSelectionConfigRemoteInfoOverride(android.adservices.adselection.RemoveAdSelectionOverrideRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` request

It contains one field, a `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig` which serves as the identifier of the override to be removed

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/adservices/adselection/RemoveAdSelectionOverrideRequest#RemoveAdSelectionOverrideRequest(android.adservices.adselection.AdSelectionConfig)(adSelectionConfig: https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig)` Builds a `https://developer.android.com/reference/kotlin/android/adservices/adselection/RemoveAdSelectionOverrideRequest#` instance. |

| Public methods ||
|---|---|
| open [AdSelectionConfig](AdSelectionConfig.md) | `https://developer.android.com/reference/kotlin/android/adservices/adselection/RemoveAdSelectionOverrideRequest#getAdSelectionConfig()()` <br /> |

## Public constructors

### RemoveAdSelectionOverrideRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

```
RemoveAdSelectionOverrideRequest(adSelectionConfig: AdSelectionConfig)
```

Builds a `https://developer.android.com/reference/kotlin/android/adservices/adselection/RemoveAdSelectionOverrideRequest#` instance.

| Parameters ||
|---|---|
| `adSelectionConfig` | [AdSelectionConfig](AdSelectionConfig.md): This value cannot be `null`. |

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
| `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig` | AdSelectionConfig, the configuration of the ad selection process. This value cannot be `null`. |
