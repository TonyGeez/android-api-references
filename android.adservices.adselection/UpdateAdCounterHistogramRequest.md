Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UpdateAdCounterHistogramRequest

```
open class UpdateAdCounterHistogramRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.UpdateAdCounterHistogramRequest](UpdateAdCounterHistogramRequest.md) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The Rubidium (Rb) Relevance APIs, including those in android.adservices.adselection, are being deprecated. Relevance APIs have no direct replacement. Developers should stop using them, as calls will be rejected in future Android releases. Please refer to official Privacy Sandbox documentation for deprecation and roadmap details: https://privacysandbox.com/news/update-on-plans-for-privacy-sandbox-technologies/

Request object wrapping the required arguments needed to update an ad counter histogram.

The ad counter histograms, which are historical logs of events which are associated with an ad counter key and an ad event type, are used to inform frequency cap filtering when using the Protected Audience APIs.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/adservices/adselection/UpdateAdCounterHistogramRequest.Builder` Builder for `https://developer.android.com/reference/kotlin/android/adservices/adselection/UpdateAdCounterHistogramRequest#` objects. |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/adselection/UpdateAdCounterHistogramRequest#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Checks whether the `https://developer.android.com/reference/kotlin/android/adservices/adselection/UpdateAdCounterHistogramRequest#` objects contain the same information. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/adselection/UpdateAdCounterHistogramRequest#getAdEventType()()` Gets the ad event type which, along with an ad's counter keys, identifies which histogram should be updated. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/adselection/UpdateAdCounterHistogramRequest#getAdSelectionId()()` Gets the ad selection ID with which the rendered ad's events are associated. |
| --- | --- |
| open [AdTechIdentifier](../android.adservices.common/AdTechIdentifier.md) | `https://developer.android.com/reference/kotlin/android/adservices/adselection/UpdateAdCounterHistogramRequest#getCallerAdTech()()` Gets the caller adtech entity's `https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/adselection/UpdateAdCounterHistogramRequest#hashCode()()` Returns the hash of the `https://developer.android.com/reference/kotlin/android/adservices/adselection/UpdateAdCounterHistogramRequest#` object's data. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/adselection/UpdateAdCounterHistogramRequest#toString()()` Returns a string representation of the object. |
| --- | --- |

## Public methods

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks whether the `https://developer.android.com/reference/kotlin/android/adservices/adselection/UpdateAdCounterHistogramRequest#` objects contain the same information.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getAdEventType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAdEventType(): Int
```

**Deprecated:** *Deprecated in Java.*

Gets the ad event type which, along with an ad's counter keys, identifies which histogram should be updated.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters.html#AD_EVENT_TYPE_WIN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters.html#AD_EVENT_TYPE_IMPRESSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters.html#AD_EVENT_TYPE_VIEW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters.html#AD_EVENT_TYPE_CLICK:kotlin.Int` |

### getAdSelectionId

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAdSelectionId(): Long
```

**Deprecated:** *Deprecated in Java.*

Gets the ad selection ID with which the rendered ad's events are associated.

For more information about the ad selection ID, see `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome`.

The ad must have been selected from Protected Audience ad selection in the last 24 hours, and the ad selection call must have been initiated from the same app as the current calling app. Event histograms for all ad counter keys associated with the ad specified by the ad selection ID will be updated for the ad event type from `https://developer.android.com/reference/kotlin/android/adservices/adselection/UpdateAdCounterHistogramRequest#getAdEventType()`, to be used in Protected Audience frequency cap filtering.

### getCallerAdTech

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCallerAdTech(): AdTechIdentifier
```

**Deprecated:** *Deprecated in Java.*

Gets the caller adtech entity's `https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#`.

The adtech using this `https://developer.android.com/reference/kotlin/android/adservices/adselection/UpdateAdCounterHistogramRequest#` object must have enrolled with the Privacy Sandbox and be allowed to act on behalf of the calling app. The specified adtech is not required to be the same adtech as either the buyer which owns the rendered ad or the seller which initiated the ad selection associated with the ID returned by `https://developer.android.com/reference/kotlin/android/adservices/adselection/UpdateAdCounterHistogramRequest#getAdSelectionId()`.

For more information about API requirements and exceptions, see `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#updateAdCounterHistogram(android.adservices.adselection.UpdateAdCounterHistogramRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#` | This value cannot be `null`. |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the hash of the `https://developer.android.com/reference/kotlin/android/adservices/adselection/UpdateAdCounterHistogramRequest#` object's data.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### toString

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

**Deprecated:** *Deprecated in Java.*

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
