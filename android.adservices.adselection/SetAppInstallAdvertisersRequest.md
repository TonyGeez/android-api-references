Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SetAppInstallAdvertisersRequest

```
open class SetAppInstallAdvertisersRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.SetAppInstallAdvertisersRequest](SetAppInstallAdvertisersRequest.md) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The Rubidium (Rb) Relevance APIs, including those in android.adservices.adselection, are being deprecated. Relevance APIs have no direct replacement. Developers should stop using them, as calls will be rejected in future Android releases. Please refer to official Privacy Sandbox documentation for deprecation and roadmap details: https://privacysandbox.com/news/update-on-plans-for-privacy-sandbox-technologies/

Represents input parameters to the setAppInstallAdvertiser API.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/adservices/adselection/SetAppInstallAdvertisersRequest.Builder` <br /> |

| Public methods ||
|---|---|
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [AdTechIdentifier](../android.adservices.common/AdTechIdentifier.md)!\> | getAdvertisers Returns the set of advertisers that will be able to run app install filters based on this app's presence on the device after a call to SetAppInstallAdvertisers is made with this as input. |

## Public methods

### getAdvertisers

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAdvertisers(): MutableSet<AdTechIdentifier!>
```

**Deprecated:** *Deprecated in Java.*

Returns the set of advertisers that will be able to run app install filters based on this app's presence on the device after a call to SetAppInstallAdvertisers is made with this as input.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#!>` | This value cannot be `null`. |
