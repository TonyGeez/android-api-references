Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FrequencyCapFilters

```
class FrequencyCapFilters : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.common.FrequencyCapFilters](../android/adservices/common/FrequencyCapFilters.md) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The Rubidium (Rb) Relevance APIs, including those in android.adservices.common, are being deprecated. Relevance APIs have no direct replacement. Developers should stop using them, as calls will be rejected in future Android releases. Please refer to official Privacy Sandbox documentation for deprecation and roadmap details: https://privacysandbox.com/news/update-on-plans-for-privacy-sandbox-technologies/

A container for the ad filters that are based on frequency caps.

No more than 20 frequency cap filters may be associated with a single ad.

Frequency caps filters combine an event type with a list of `https://developer.android.com/reference/kotlin/android/adservices/common/KeyedFrequencyCap` objects to define a collection of ad filters. If any of these frequency caps are exceeded for a given ad, the ad will be removed from the group of ads submitted to a buyer adtech's bidding function.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters.Builder` Builder for creating `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#` objects. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#AD_EVENT_TYPE_CLICK:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#AD_EVENT_TYPE_IMPRESSION:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#AD_EVENT_TYPE_VIEW:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#AD_EVENT_TYPE_WIN:kotlin.Int` The WIN ad event type is automatically populated within the Protected Audience service for any winning ad which is returned from Protected Audience ad selection. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Checks whether the `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#` objects contain the same information. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [KeyedFrequencyCap](../android/adservices/common/KeyedFrequencyCap.md)!\> | `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#getKeyedFrequencyCapsForClickEvents()()` Gets the list of `https://developer.android.com/reference/kotlin/android/adservices/common/KeyedFrequencyCap` objects that will filter on the `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#AD_EVENT_TYPE_CLICK:kotlin.Int` event type. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [KeyedFrequencyCap](../android/adservices/common/KeyedFrequencyCap.md)!\> | `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#getKeyedFrequencyCapsForImpressionEvents()()` Gets the list of `https://developer.android.com/reference/kotlin/android/adservices/common/KeyedFrequencyCap` objects that will filter on the `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#AD_EVENT_TYPE_IMPRESSION:kotlin.Int` event type. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [KeyedFrequencyCap](../android/adservices/common/KeyedFrequencyCap.md)!\> | `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#getKeyedFrequencyCapsForViewEvents()()` Gets the list of `https://developer.android.com/reference/kotlin/android/adservices/common/KeyedFrequencyCap` objects that will filter on the `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#AD_EVENT_TYPE_VIEW:kotlin.Int` event type. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [KeyedFrequencyCap](../android/adservices/common/KeyedFrequencyCap.md)!\> | `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#getKeyedFrequencyCapsForWinEvents()()` Gets the list of `https://developer.android.com/reference/kotlin/android/adservices/common/KeyedFrequencyCap` objects that will filter on the `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#AD_EVENT_TYPE_WIN:kotlin.Int` event type. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#hashCode()()` Returns the hash of the `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#` object's data. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [FrequencyCapFilters](../android/adservices/common/FrequencyCapFilters.md)!\> | `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### AD_EVENT_TYPE_CLICK

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AD_EVENT_TYPE_CLICK: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 3

### AD_EVENT_TYPE_IMPRESSION

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AD_EVENT_TYPE_IMPRESSION: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 1

### AD_EVENT_TYPE_VIEW

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AD_EVENT_TYPE_VIEW: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 2

### AD_EVENT_TYPE_WIN

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AD_EVENT_TYPE_WIN: Int
```

**Deprecated:** *Deprecated in Java.*

The WIN ad event type is automatically populated within the Protected Audience service for any winning ad which is returned from Protected Audience ad selection.

It should not be used to manually update an ad counter histogram.

 Value: 0

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

**Deprecated:** *Deprecated in Java.*

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks whether the `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#` objects contain the same information.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getKeyedFrequencyCapsForClickEvents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKeyedFrequencyCapsForClickEvents(): MutableList<KeyedFrequencyCap!>
```

**Deprecated:** *Deprecated in Java.*

Gets the list of `https://developer.android.com/reference/kotlin/android/adservices/common/KeyedFrequencyCap` objects that will filter on the `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#AD_EVENT_TYPE_CLICK:kotlin.Int` event type.

These frequency caps apply to events which correlate to a click as interpreted by an adtech. Click events are counted when the `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager.html#updateAdCounterHistogram(android.adservices.adselection.UpdateAdCounterHistogramRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` API is invoked with the `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#AD_EVENT_TYPE_CLICK:kotlin.Int` event type.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/adservices/common/KeyedFrequencyCap!>` | This value cannot be `null`. |

### getKeyedFrequencyCapsForImpressionEvents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKeyedFrequencyCapsForImpressionEvents(): MutableList<KeyedFrequencyCap!>
```

**Deprecated:** *Deprecated in Java.*

Gets the list of `https://developer.android.com/reference/kotlin/android/adservices/common/KeyedFrequencyCap` objects that will filter on the `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#AD_EVENT_TYPE_IMPRESSION:kotlin.Int` event type.

These frequency caps apply to events which correlate to an impression as interpreted by an adtech.

Note that events are not automatically counted when calling `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager.html#reportImpression(android.adservices.adselection.ReportImpressionRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. Instead, the `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#AD_EVENT_TYPE_IMPRESSION:kotlin.Int` event type must be updated using the `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager.html#updateAdCounterHistogram(android.adservices.adselection.UpdateAdCounterHistogramRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` API.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/adservices/common/KeyedFrequencyCap!>` | This value cannot be `null`. |

### getKeyedFrequencyCapsForViewEvents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKeyedFrequencyCapsForViewEvents(): MutableList<KeyedFrequencyCap!>
```

**Deprecated:** *Deprecated in Java.*

Gets the list of `https://developer.android.com/reference/kotlin/android/adservices/common/KeyedFrequencyCap` objects that will filter on the `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#AD_EVENT_TYPE_VIEW:kotlin.Int` event type.

These frequency caps apply to events which correlate to a view as interpreted by an adtech. View events are counted when the `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager.html#updateAdCounterHistogram(android.adservices.adselection.UpdateAdCounterHistogramRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` API is invoked with the `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#AD_EVENT_TYPE_VIEW:kotlin.Int` event type.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/adservices/common/KeyedFrequencyCap!>` | This value cannot be `null`. |

### getKeyedFrequencyCapsForWinEvents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKeyedFrequencyCapsForWinEvents(): MutableList<KeyedFrequencyCap!>
```

**Deprecated:** *Deprecated in Java.*

Gets the list of `https://developer.android.com/reference/kotlin/android/adservices/common/KeyedFrequencyCap` objects that will filter on the `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#AD_EVENT_TYPE_WIN:kotlin.Int` event type.

These frequency caps apply to events for ads that were selected as winners in ad selection. Winning ads are used to automatically increment the associated counter keys on the win event type.

Note that the `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#AD_EVENT_TYPE_WIN:kotlin.Int` event type cannot be updated manually using the `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager.html#updateAdCounterHistogram(android.adservices.adselection.UpdateAdCounterHistogramRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` API.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/adservices/common/KeyedFrequencyCap!>` | This value cannot be `null`. |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the hash of the `https://developer.android.com/reference/kotlin/android/adservices/common/FrequencyCapFilters#` object's data.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### toString

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

**Deprecated:** *Deprecated in Java.*

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android/os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<FrequencyCapFilters!>
```

**Deprecated:** *Deprecated in Java.*
