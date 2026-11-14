Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReportImpressionRequest

```
open class ReportImpressionRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.ReportImpressionRequest](ReportImpressionRequest.md) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The Rubidium (Rb) Relevance APIs, including those in android.adservices.adselection, are being deprecated. Relevance APIs have no direct replacement. Developers should stop using them, as calls will be rejected in future Android releases. Please refer to official Privacy Sandbox documentation for deprecation and roadmap details: https://privacysandbox.com/news/update-on-plans-for-privacy-sandbox-technologies/

Represent input parameters to the reportImpression API.

## Summary

| Public constructors ||
|---|---|
| ReportImpressionRequest Ctor for auction server ad selection reporting request. |
| ReportImpressionRequest Ctor for on-device ad selection reporting request. |

| Public methods ||
|---|---|
| open [AdSelectionConfig](AdSelectionConfig.md) | getAdSelectionConfig Returns the adSelectionConfig, one of the inputs to ReportImpressionRequest |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getAdSelectionId Returns the adSelectionId, one of the inputs to ReportImpressionRequest |

## Public constructors

### ReportImpressionRequest

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

```
ReportImpressionRequest(adSelectionId: Long)
```

Ctor for auction server ad selection reporting request.

If your `adSelectionId` is for a server auction run where device info collected by getAdSelectionData then your impression reporting request should only include the ad selection id.

persistAdSelectionResult must be called with the encrypted result blob from servers before making impression reporting request.

| Parameters ||
|---|---|
| `adSelectionId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): received from getAdSelectionData |

### ReportImpressionRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

```
ReportImpressionRequest(
    adSelectionId: Long, 
    adSelectionConfig: AdSelectionConfig)
```

Ctor for on-device ad selection reporting request.

If your `adSelectionId` is for a on-device auction run using selectAds then your impression reporting request must include your AdSelectionConfig.

| Parameters ||
|---|---|
| `adSelectionId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): received from selectAds |
| `adSelectionConfig` | [AdSelectionConfig](AdSelectionConfig.md): same AdSelectionConfig used to trigger selectAds This value cannot be `null`. |

## Public methods

### getAdSelectionConfig

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAdSelectionConfig(): AdSelectionConfig
```

**Deprecated:** *Deprecated in Java.*

Returns the adSelectionConfig, one of the inputs to ReportImpressionRequest

| Return ||
|---|---|
| AdSelectionConfig | This value cannot be `null`. |

### getAdSelectionId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAdSelectionId(): Long
```

**Deprecated:** *Deprecated in Java.*

Returns the adSelectionId, one of the inputs to ReportImpressionRequest
