Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AdSelectionManager

```
open class AdSelectionManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.AdSelectionManager](../android/adservices/adselection/AdSelectionManager.md) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The Rubidium (Rb) Relevance APIs, including those in android.adservices.adselection, are being deprecated. Relevance APIs have no direct replacement. Developers should stop using them, as calls will be rejected in future Android releases. Please refer to official Privacy Sandbox documentation for deprecation and roadmap details: https://privacysandbox.com/news/update-on-plans-for-privacy-sandbox-technologies/

AdSelection Manager provides APIs for app and ad-SDKs to run ad selection processes as well as report impressions.

## Summary

| Public methods ||
|---|---|
| open static [AdSelectionManager](../android/adservices/adselection/AdSelectionManager.md) | `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#get(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#)` Factory method for creating an instance of AdSelectionManager. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#getAdSelectionData(android.adservices.adselection.GetAdSelectionDataRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/adservices/adselection/GetAdSelectionDataRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, receiver: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/adservices/adselection/GetAdSelectionDataOutcome!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>)` Collects custom audience data from device. |
| open [TestAdSelectionManager](../android/adservices/adselection/TestAdSelectionManager.md) | `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#getTestAdSelectionManager()()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#persistAdSelectionResult(android.adservices.adselection.PersistAdSelectionResultRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/adservices/adselection/PersistAdSelectionResultRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, receiver: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>)` Persists the ad selection results from the server-side. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#reportEvent(android.adservices.adselection.ReportEventRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, receiver: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>)` Notifies the service that there is a new ad event to report for the ad selected by the ad-selection run identified by `adSelectionId`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#reportImpression(android.adservices.adselection.ReportImpressionRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportImpressionRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, receiver: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>)` Notifies the service that there is a new impression to report for the ad selected by the ad-selection run identified by `adSelectionId`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#selectAds(android.adservices.adselection.AdSelectionConfig,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(adSelectionConfig: https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, receiver: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>)` Runs the ad selection process on device to select a remarketing ad for the caller application. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#selectAds(android.adservices.adselection.AdSelectionFromOutcomesConfig,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(adSelectionFromOutcomesConfig: https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, receiver: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>)` Selects an ad from the results of previously ran ad selections. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#setAppInstallAdvertisers(android.adservices.adselection.SetAppInstallAdvertisersRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/adservices/adselection/SetAppInstallAdvertisersRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, receiver: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>)` Gives the provided list of adtechs the ability to do app install filtering on the calling app. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#updateAdCounterHistogram(android.adservices.adselection.UpdateAdCounterHistogramRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(updateAdCounterHistogramRequest: https://developer.android.com/reference/kotlin/android/adservices/adselection/UpdateAdCounterHistogramRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, outcomeReceiver: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>)` Updates the counter histograms for an ad which was previously selected by a call to `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#selectAds(android.adservices.adselection.AdSelectionConfig,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |

## Public methods

### get

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 6](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun get(context: Context): AdSelectionManager
```

**Deprecated:** *Deprecated in Java.*

Factory method for creating an instance of AdSelectionManager.

| Parameters ||
|---|---|
| `context` | [Context](../android/content/Context.md): The `https://developer.android.com/reference/kotlin/android/content/Context.html#` to use. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#` | A `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#` instance. This value cannot be `null`. |

### getAdSelectionData

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAdSelectionData(
    request: GetAdSelectionDataRequest, 
    executor: Executor, 
    receiver: OutcomeReceiver<GetAdSelectionDataOutcome!, Exception!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Collects custom audience data from device. Returns a compressed and encrypted blob to send to auction servers for ad selection. For more details, please visit [Bidding and Auction Services Explainer](https://developer.android.com/design-for-safety/privacy-sandbox/protected-audience-bidding-and-auction-services).

Custom audience ads must have a `ad_render_id` to be eligible for to be collected.

See `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#persistAdSelectionResult(android.adservices.adselection.PersistAdSelectionResultRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` for how to process the results of the ad selection run on server-side with the blob generated by this API.

The output is passed by the receiver, which either returns an `https://developer.android.com/reference/kotlin/android/adservices/adselection/GetAdSelectionDataOutcome` for a successful run, or an `https://developer.android.com/reference/kotlin/java/lang/Exception.html#` includes the type of the exception thrown and the corresponding error message.

If the `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` is thrown, it is caused by invalid input argument the API received to run the ad selection.

If the `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` is thrown with error message "Failure of AdSelection services.", it is caused by an internal failure of the ad selection service.

If the `https://developer.android.com/reference/kotlin/java/util/concurrent/TimeoutException.html#` is thrown, it is caused when a timeout is encountered during bidding, scoring, or overall selection process to find winning Ad.

If the `https://developer.android.com/reference/kotlin/android/os/LimitExceededException.html#` is thrown, it is caused when the calling package exceeds the allowed rate limits and is throttled.

If the `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` is thrown, it is caused when the caller is not authorized or permission is not requested. 
Requires `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_CUSTOM_AUDIENCE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_PROTECTED_SIGNALS:kotlin.String` or `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_AD_SELECTION:kotlin.String`

| Parameters ||
|---|---|
| `request` | [GetAdSelectionDataRequest](../android/adservices/adselection/GetAdSelectionDataRequest.md): This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [GetAdSelectionDataOutcome](../android/adservices/adselection/GetAdSelectionDataOutcome.md)!, [Exception](../java/lang/Exception.md)!\>: This value cannot be `null`. |
| --- | --- |

### getTestAdSelectionManager

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTestAdSelectionManager(): TestAdSelectionManager
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/adservices/adselection/TestAdSelectionManager` | This value cannot be `null`. |

### persistAdSelectionResult

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun persistAdSelectionResult(
    request: PersistAdSelectionResultRequest, 
    executor: Executor, 
    receiver: OutcomeReceiver<AdSelectionOutcome!, Exception!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Persists the ad selection results from the server-side. For more details, please visit [Bidding and Auction Services Explainer](https://developer.android.com/design-for-safety/privacy-sandbox/protected-audience-bidding-and-auction-services)

See `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#getAdSelectionData(android.adservices.adselection.GetAdSelectionDataRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` for how to generate an encrypted blob to run an ad selection on the server side.

The output is passed by the receiver, which either returns an `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome` for a successful run, or an `https://developer.android.com/reference/kotlin/java/lang/Exception.html#` includes the type of the exception thrown and the corresponding error message. The `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome#getAdSelectionId()` is not guaranteed to be the same as the `https://developer.android.com/reference/kotlin/android/adservices/adselection/PersistAdSelectionResultRequest#getAdSelectionDataId()` or the deprecated `https://developer.android.com/reference/kotlin/android/adservices/adselection/PersistAdSelectionResultRequest#getAdSelectionId()`.

If the `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` is thrown, it is caused by invalid input argument the API received to run the ad selection.

If the `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` is thrown with error message "Failure of AdSelection services.", it is caused by an internal failure of the ad selection service.

If the `https://developer.android.com/reference/kotlin/java/util/concurrent/TimeoutException.html#` is thrown, it is caused when a timeout is encountered during bidding, scoring, or overall selection process to find winning Ad.

If the `https://developer.android.com/reference/kotlin/android/os/LimitExceededException.html#` is thrown, it is caused when the calling package exceeds the allowed rate limits and is throttled.

If the `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` is thrown, it is caused when the caller is not authorized or permission is not requested. 
Requires `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_CUSTOM_AUDIENCE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_PROTECTED_SIGNALS:kotlin.String` or `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_AD_SELECTION:kotlin.String`

| Parameters ||
|---|---|
| `request` | [PersistAdSelectionResultRequest](../android/adservices/adselection/PersistAdSelectionResultRequest.md): This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [AdSelectionOutcome](../android/adservices/adselection/AdSelectionOutcome.md)!, [Exception](../java/lang/Exception.md)!\>: This value cannot be `null`. |
| --- | --- |

### reportEvent

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reportEvent(
    request: ReportEventRequest, 
    executor: Executor, 
    receiver: OutcomeReceiver<Any!, Exception!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Notifies the service that there is a new ad event to report for the ad selected by the ad-selection run identified by `adSelectionId`. An ad event is any occurrence that happens to an ad associated with the given `adSelectionId`. There is no guarantee about when the ad event will be reported. The event reporting could be delayed and reports could be batched.

Using `https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest#getKey()`, the service will fetch the `reportingUri` that was registered in `registerAdBeacon`. See documentation of `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#reportImpression(android.adservices.adselection.ReportImpressionRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` for more details regarding `registerAdBeacon`. Then, the service will attach `https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest#getData()` to the request body of a POST request and send the request. The body of the POST request will have the `content-type` of `text/plain`, and the data will be transmitted in `charset=UTF-8`.

The output is passed by the receiver, which either returns an empty `https://developer.android.com/reference/kotlin/java/lang/Object.html#` for a successful run, or an `https://developer.android.com/reference/kotlin/java/lang/Exception.html#` includes the type of the exception thrown and the corresponding error message.

If the `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` is thrown, it is caused by invalid input argument the API received to report the ad event.

If the `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` is thrown with error message "Failure of AdSelection services.", it is caused by an internal failure of the ad selection service.

If the `https://developer.android.com/reference/kotlin/android/os/LimitExceededException.html#` is thrown, it is caused when the calling package exceeds the allowed rate limits and is throttled.

If the `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` is thrown, it is caused when the caller is not authorized or permission is not requested.

Events will be reported at most once as a best-effort attempt. 
Requires `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_CUSTOM_AUDIENCE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_PROTECTED_SIGNALS:kotlin.String` or `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_AD_SELECTION:kotlin.String`

| Parameters ||
|---|---|
| `request` | [ReportEventRequest](../android/adservices/adselection/ReportEventRequest.md): This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md): This value cannot be `null`. |
| `receiver` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>: This value cannot be `null`. |
| --- | --- |

### reportImpression

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reportImpression(
    request: ReportImpressionRequest, 
    executor: Executor, 
    receiver: OutcomeReceiver<Any!, Exception!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Notifies the service that there is a new impression to report for the ad selected by the ad-selection run identified by `adSelectionId`. There is no guarantee about when the impression will be reported. The impression reporting could be delayed and reports could be batched.

To calculate the winning seller reporting URL, the service fetches the seller's JavaScript logic from the `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig#getDecisionLogicUri()` found at `https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportImpressionRequest#getAdSelectionConfig()`. Then, the service executes one of the functions found in the seller JS called `reportResult`, providing on-device signals as well as `https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportImpressionRequest#getAdSelectionConfig()` as input parameters.

The function definition of `reportResult` is:

`function reportResult(ad_selection_config, render_url, bid, contextual_signals) { return { 'status': status, 'results': {'signals_for_buyer': signals_for_buyer, 'reporting_url': reporting_url } }; } `

To calculate the winning buyer reporting URL, the service fetches the winning buyer's JavaScript logic which is fetched via the buyer's `https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience.html#getBiddingLogicUri()`. Then, the service executes one of the functions found in the buyer JS called `reportWin`, providing on-device signals, `signals_for_buyer` calculated by `reportResult`, and specific fields from `https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportImpressionRequest#getAdSelectionConfig()` as input parameters.

The function definition of `reportWin` is:

`function reportWin(ad_selection_signals, per_buyer_signals, signals_for_buyer, contextual_signals, custom_audience_reporting_signals) { return {'status': 0, 'results': {'reporting_url': reporting_url } }; } `

In addition, buyers and sellers have the option to register to receive reports on specific ad events. To do so, they can invoke the platform provided `registerAdBeacon` function inside `reportWin` and `reportResult` for buyers and sellers, respectively.

The function definition of `registerBeacon` is:

`function registerAdBeacon(beacons)`, where `beacons` is a dict of string to string pairs

For each ad event a buyer/seller is interested in reports for, they would add an `event_key`: `event_reporting_uri` pair to the `beacons` dict, where `event_key` is an identifier for that specific event. This `event_key` should match `https://developer.android.com/reference/kotlin/android/adservices/adselection/ReportEventRequest#getKey()` when the SDK invokes `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#reportEvent(android.adservices.adselection.ReportEventRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. In addition, each `event_reporting_uri` should parse properly into a `https://developer.android.com/reference/kotlin/android/net/Uri.html#`. This will be the `https://developer.android.com/reference/kotlin/android/net/Uri.html#` reported to when the SDK invokes `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#reportEvent(android.adservices.adselection.ReportEventRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`.

When the buyer/seller has added all the pairings they want to receive events for, they can invoke `registerAdBeacon(beacons)`, where `beacons` is the name of the dict they added the pairs to.

`registerAdBeacon` will throw a `TypeError` in these situations:

1. `registerAdBeacon`is called more than once. If this error is caught in reportWin/reportResult, the original set of pairings will be registered
2. `registerAdBeacon` doesn't have exactly 1 dict argument.
3. The contents of the 1 dict argument are not all `String: String` pairings.

The output is passed by the `receiver`, which either returns an empty `https://developer.android.com/reference/kotlin/java/lang/Object.html#` for a successful run, or an `https://developer.android.com/reference/kotlin/java/lang/Exception.html#` includes the type of the exception thrown and the corresponding error message.

If the `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` is thrown, it is caused by invalid input argument the API received to report the impression.

If the `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` is thrown with error message "Failure of AdSelection services.", it is caused by an internal failure of the ad selection service.

If the `https://developer.android.com/reference/kotlin/android/os/LimitExceededException.html#` is thrown, it is caused when the calling package exceeds the allowed rate limits and is throttled.

If the `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` is thrown, it is caused when the caller is not authorized or permission is not requested.

Impressions will be reported at most once as a best-effort attempt. 
Requires `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_CUSTOM_AUDIENCE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_PROTECTED_SIGNALS:kotlin.String` or `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_AD_SELECTION:kotlin.String`

| Parameters ||
|---|---|
| `request` | [ReportImpressionRequest](../android/adservices/adselection/ReportImpressionRequest.md): This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md): This value cannot be `null`. |
| `receiver` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>: This value cannot be `null`. |
| --- | --- |

### selectAds

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun selectAds(
    adSelectionConfig: AdSelectionConfig, 
    executor: Executor, 
    receiver: OutcomeReceiver<AdSelectionOutcome!, Exception!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Runs the ad selection process on device to select a remarketing ad for the caller application.

The input `adSelectionConfig` is provided by the Ads SDK and the `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig` object is transferred via a Binder call. For this reason, the total size of these objects is bound to the Android IPC limitations. Failures to transfer the `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig` will throws an `https://developer.android.com/reference/kotlin/android/os/TransactionTooLargeException.html#`.

The input `adSelectionConfig` contains `Decision Logic Uri` that could follow either the HTTPS or Ad Selection Prebuilt schemas.

If the URI follows HTTPS schema then the host should match the `seller`. Otherwise, `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown.

Prebuilt URIs are a way of substituting a generic pre-built logics for the required JavaScripts for `scoreAds`. Prebuilt Uri for this endpoint should follow;

- `ad-selection-prebuilt://ad-selection/<name>?<script-generation-parameters>`

If an unsupported prebuilt URI is passed or prebuilt URI feature is disabled by the service then `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown.

See `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionConfig.Builder#setDecisionLogicUri(android.net.Uri)` for supported `<name>` and required `<script-generation-parameters>`.

The output is passed by the receiver, which either returns an `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome` for a successful run, or an `https://developer.android.com/reference/kotlin/java/lang/Exception.html#` includes the type of the exception thrown and the corresponding error message.

If the `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` is thrown, it is caused by invalid input argument the API received to run the ad selection.

If the `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` is thrown with error message "Failure of AdSelection services.", it is caused by an internal failure of the ad selection service.

If the `https://developer.android.com/reference/kotlin/java/util/concurrent/TimeoutException.html#` is thrown, it is caused when a timeout is encountered during bidding, scoring, or overall selection process to find winning Ad.

If the `https://developer.android.com/reference/kotlin/android/os/LimitExceededException.html#` is thrown, it is caused when the calling package exceeds the allowed rate limits and is throttled.

If the `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` is thrown, it is caused when the caller is not authorized or permission is not requested. 
Requires `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_CUSTOM_AUDIENCE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_PROTECTED_SIGNALS:kotlin.String` or `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_AD_SELECTION:kotlin.String`

| Parameters ||
|---|---|
| `adSelectionConfig` | [AdSelectionConfig](../android/adservices/adselection/AdSelectionConfig.md): This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [AdSelectionOutcome](../android/adservices/adselection/AdSelectionOutcome.md)!, [Exception](../java/lang/Exception.md)!\>: This value cannot be `null`. |
| --- | --- |

### selectAds

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun selectAds(
    adSelectionFromOutcomesConfig: AdSelectionFromOutcomesConfig, 
    executor: Executor, 
    receiver: OutcomeReceiver<AdSelectionOutcome!, Exception!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Selects an ad from the results of previously ran ad selections.

The input `adSelectionFromOutcomesConfig` is provided by the Ads SDK and the `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig` object is transferred via a Binder call. For this reason, the total size of these objects is bound to the Android IPC limitations. Failures to transfer the `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig` will throws an `https://developer.android.com/reference/kotlin/android/os/TransactionTooLargeException.html#`.

The output is passed by the receiver, which either returns an `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionOutcome` for a successful run, or an `https://developer.android.com/reference/kotlin/java/lang/Exception.html#` includes the type of the exception thrown and the corresponding error message.

The input `adSelectionFromOutcomesConfig` contains:

- `Seller` is required to be a registered `https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#`. Otherwise, `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` will be thrown.
- `List of ad selection ids` should exist and come from #selectAds calls originated from the same application. Otherwise, `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` for input validation will raise listing violating ad selection ids.
- `Selection logic URI` that could follow either the HTTPS or Ad Selection Prebuilt schemas.

 If the URI follows HTTPS schema then the host should match the `seller`. Otherwise, `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown.

 Prebuilt URIs are a way of substituting a generic pre-built logics for the required JavaScripts for `selectOutcome`. Prebuilt Uri for this endpoint should follow;
 - `ad-selection-prebuilt://ad-selection-from-outcomes/<name>?<script-generation-parameters>`

 If an unsupported prebuilt URI is passed or prebuilt URI feature is disabled by the service then `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown.

 See `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig.Builder#setSelectionLogicUri(android.net.Uri)` for supported `<name>` and required `<script-generation-parameters>`.

If the `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` is thrown, it is caused by invalid input argument the API received to run the ad selection.

If the `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` is thrown with error message "Failure of AdSelection services.", it is caused by an internal failure of the ad selection service.

If the `https://developer.android.com/reference/kotlin/java/util/concurrent/TimeoutException.html#` is thrown, it is caused when a timeout is encountered during bidding, scoring, or overall selection process to find winning Ad.

If the `https://developer.android.com/reference/kotlin/android/os/LimitExceededException.html#` is thrown, it is caused when the calling package exceeds the allowed rate limits and is throttled.

If the `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` is thrown, it is caused when the caller is not authorized or permission is not requested. 
Requires `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_CUSTOM_AUDIENCE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_PROTECTED_SIGNALS:kotlin.String` or `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_AD_SELECTION:kotlin.String`

| Parameters ||
|---|---|
| `adSelectionFromOutcomesConfig` | [AdSelectionFromOutcomesConfig](../android/adservices/adselection/AdSelectionFromOutcomesConfig.md): This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [AdSelectionOutcome](../android/adservices/adselection/AdSelectionOutcome.md)!, [Exception](../java/lang/Exception.md)!\>: This value cannot be `null`. |
| --- | --- |

### setAppInstallAdvertisers

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAppInstallAdvertisers(
    request: SetAppInstallAdvertisersRequest, 
    executor: Executor, 
    receiver: OutcomeReceiver<Any!, Exception!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Gives the provided list of adtechs the ability to do app install filtering on the calling app.

The input `request` is provided by the Ads SDK and the `request` object is transferred via a Binder call. For this reason, the total size of these objects is bound to the Android IPC limitations. Failures to transfer the `advertisers` will throws an `https://developer.android.com/reference/kotlin/android/os/TransactionTooLargeException.html#`.

The output is passed by the receiver, which either returns an empty `https://developer.android.com/reference/kotlin/java/lang/Object.html#` for a successful run, or an `https://developer.android.com/reference/kotlin/java/lang/Exception.html#` includes the type of the exception thrown and the corresponding error message.

If the `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` is thrown, it is caused by invalid input argument the API received.

If the `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` is thrown with error message "Failure of AdSelection services.", it is caused by an internal failure of the ad selection service.

If the `https://developer.android.com/reference/kotlin/android/os/LimitExceededException.html#` is thrown, it is caused when the calling package exceeds the allowed rate limits and is throttled.

If the `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` is thrown, it is caused when the caller is not authorized or permission is not requested. 
Requires `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_CUSTOM_AUDIENCE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_PROTECTED_SIGNALS:kotlin.String` or `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_AD_SELECTION:kotlin.String`

| Parameters ||
|---|---|
| `request` | [SetAppInstallAdvertisersRequest](../android/adservices/adselection/SetAppInstallAdvertisersRequest.md): This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md): This value cannot be `null`. |
| `receiver` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>: This value cannot be `null`. |
| --- | --- |

### updateAdCounterHistogram

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateAdCounterHistogram(
    updateAdCounterHistogramRequest: UpdateAdCounterHistogramRequest, 
    executor: Executor, 
    outcomeReceiver: OutcomeReceiver<Any!, Exception!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Updates the counter histograms for an ad which was previously selected by a call to `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#selectAds(android.adservices.adselection.AdSelectionConfig,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`.

The counter histograms are used in ad selection to inform frequency cap filtering on candidate ads, where ads whose frequency caps are met or exceeded are removed from the bidding process during ad selection.

Counter histograms can only be updated for ads specified by the given `adSelectionId` returned by a recent call to FLEDGE ad selection from the same caller app.

A `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` is returned via the `outcomeReceiver` if:

1. the app has not declared the correct permissions in its manifest, or
2. the app or entity identified by the `callerAdTechIdentifier` are not authorized to use the API.

An `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` is returned via the `outcomeReceiver` if the call does not come from an app with a foreground activity.

A `https://developer.android.com/reference/kotlin/android/os/LimitExceededException.html#` is returned via the `outcomeReceiver` if the call exceeds the calling app's API throttle.

In all other failure cases, the `outcomeReceiver` will return an empty `https://developer.android.com/reference/kotlin/java/lang/Object.html#`. Note that to protect user privacy, internal errors will not be sent back via an exception. 
Requires `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_CUSTOM_AUDIENCE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_PROTECTED_SIGNALS:kotlin.String` or `https://developer.android.com/reference/kotlin/android/adservices/common/AdServicesPermissions.html#ACCESS_ADSERVICES_AD_SELECTION:kotlin.String`

| Parameters ||
|---|---|
| `updateAdCounterHistogramRequest` | [UpdateAdCounterHistogramRequest](../android/adservices/adselection/UpdateAdCounterHistogramRequest.md): This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `outcomeReceiver` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Exception](../java/lang/Exception.md)!\>: This value cannot be `null`. |
| --- | --- |
