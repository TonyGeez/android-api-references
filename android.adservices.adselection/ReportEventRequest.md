# ReportEventRequest

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions)

# ReportEventRequest

Kotlin | [Java](https://developer.android.com/reference/android/adservices/adselection/ReportEventRequest "View this page in Java") 

```
open class ReportEventRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.adservices.adselection.ReportEventRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest#) |

Request object wrapping the required arguments needed to report an ad event.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest.Builder) Builder for [ReportEventRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest#) objects. |

| Constants ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_REPORTING_DESTINATION_BUYER](https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest#FLAG_REPORTING_DESTINATION_BUYER:kotlin.Int) This is used to represent buyer as the destination for report event API. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_REPORTING_DESTINATION_COMPONENT_SELLER](https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest#FLAG_REPORTING_DESTINATION_COMPONENT_SELLER:kotlin.Int) This is used to component seller as the destination for report event API |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_REPORTING_DESTINATION_SELLER](https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest#FLAG_REPORTING_DESTINATION_SELLER:kotlin.Int) This is used to represent seller as the destination for report event API |

| Public methods ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAdSelectionId](https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest#getAdSelectionId())`()` Returns the adSelectionId, the primary identifier of an ad selection process. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getData](https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest#getData())`()` Returns the ad event data. |
| open [InputEvent](https://developer.android.com/reference/kotlin/android/view/InputEvent.html#)? | [getInputEvent](https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest#getInputEvent())`()` Returns the input event associated with the user interaction. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getKey](https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest#getKey())`()` Returns the event key, the type of ad event to be reported. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReportingDestinations](https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest#getReportingDestinations())`()` Returns the bitfield of reporting destinations to report to (buyer, seller, component seller or any of the combination of them). |

## Constants

### FLAG_REPORTING_DESTINATION_BUYER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 

```
static val FLAG_REPORTING_DESTINATION_BUYER: Int
```

This is used to represent buyer as the destination for report event API. 

 Value: 2

### FLAG_REPORTING_DESTINATION_COMPONENT_SELLER

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 18](https://developer.android.com/sdkExtensions) 

```
static val FLAG_REPORTING_DESTINATION_COMPONENT_SELLER: Int
```

This is used to component seller as the destination for report event API 

 Value: 4

### FLAG_REPORTING_DESTINATION_SELLER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 

```
static val FLAG_REPORTING_DESTINATION_SELLER: Int
```

This is used to represent seller as the destination for report event API 

 Value: 1

## Public methods

### getAdSelectionId

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 

```
open fun getAdSelectionId(): Long
```

Returns the adSelectionId, the primary identifier of an ad selection process. 

### getData

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 

```
open fun getData(): String
```

Returns the ad event data.

After ad selection, this data is generated by the caller. The caller can then call [android.adservices.adselection.AdSelectionManager#reportEvent](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#reportEvent(android.adservices.adselection.ReportEventRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)). This data will be attached in a POST request to the `reportingUri` registered in `registerAdBeacon`.

The size of [String.getBytes()](https://developer.android.com/reference/kotlin/java/lang/String.html#getBytes()) in `UTF-8` format should be below 64KB.

| Return ||
|----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be `null`. |

### getInputEvent

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
open fun getInputEvent(): InputEvent?
```

Returns the input event associated with the user interaction.

This field is either `null`, representing a *view* event, or has an [InputEvent](https://developer.android.com/reference/kotlin/android/view/InputEvent.html#) object, representing a *click* event. 

### getKey

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 

```
open fun getKey(): String
```

Returns the event key, the type of ad event to be reported.

This field will be used to fetch the `reportingUri` associated with the `eventKey` registered in `registerAdBeacon` after ad selection.

This field should be an exact match to the `eventKey` registered in `registerAdBeacon`. Specific details about `registerAdBeacon` can be found at the documentation of [AdSelectionManager.reportImpression](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#reportImpression(android.adservices.adselection.ReportImpressionRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))

The event key (when inspecting its byte array with [String.getBytes()](https://developer.android.com/reference/kotlin/java/lang/String.html#getBytes())) in `UTF-8` format should not exceed 40 bytes. Any key exceeding this limit will not be registered during the `registerAdBeacon` call.

| Return ||
|----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be `null`. |

### getReportingDestinations

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 

```
open fun getReportingDestinations(): Int
```

Returns the bitfield of reporting destinations to report to (buyer, seller, component seller or any of the combination of them).

To create this bitfield, place an `|` bitwise operator between each `reportingDestination` to be reported to. For example to only report to buyer, set the reportingDestinations field to [FLAG_REPORTING_DESTINATION_BUYER](https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest#FLAG_REPORTING_DESTINATION_BUYER:kotlin.Int) To only report to seller, set the reportingDestinations field to [FLAG_REPORTING_DESTINATION_SELLER](https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest#FLAG_REPORTING_DESTINATION_SELLER:kotlin.Int) To report to buyers and sellers, set the reportingDestinations field to [FLAG_REPORTING_DESTINATION_BUYER](https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest#FLAG_REPORTING_DESTINATION_BUYER:kotlin.Int) | [FLAG_REPORTING_DESTINATION_SELLER](https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest#FLAG_REPORTING_DESTINATION_SELLER:kotlin.Int). To report to buyer, seller and component seller, set the reportingDestinations field to [FLAG_REPORTING_DESTINATION_BUYER](https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest#FLAG_REPORTING_DESTINATION_BUYER:kotlin.Int) | [FLAG_REPORTING_DESTINATION_SELLER](https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest#FLAG_REPORTING_DESTINATION_SELLER:kotlin.Int) | [FLAG_REPORTING_DESTINATION_COMPONENT_SELLER](https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest#FLAG_REPORTING_DESTINATION_COMPONENT_SELLER:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either `0` or a combination of [android.adservices.adselection.ReportEventRequest#FLAG_REPORTING_DESTINATION_SELLER](https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest#FLAG_REPORTING_DESTINATION_SELLER:kotlin.Int), [android.adservices.adselection.ReportEventRequest#FLAG_REPORTING_DESTINATION_BUYER](https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest#FLAG_REPORTING_DESTINATION_BUYER:kotlin.Int), and [android.adservices.adselection.ReportEventRequest#FLAG_REPORTING_DESTINATION_COMPONENT_SELLER](https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest#FLAG_REPORTING_DESTINATION_COMPONENT_SELLER:kotlin.Int) |
