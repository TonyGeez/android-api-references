# android.adservices.adselection

Kotlin | [Java](../android/adservices/adselection/_package.md)
| --- | --- |

## Classes

| [AddAdSelectionFromOutcomesOverrideRequest](../android/adservices/adselection/AddAdSelectionFromOutcomesOverrideRequest.md) | This POJO represents the `https://developer.android.com/reference/kotlin/android/adservices/adselection/TestAdSelectionManager#overrideAdSelectionFromOutcomesConfigRemoteInfo(android.adservices.adselection.AddAdSelectionFromOutcomesOverrideRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` ( AddAdSelectionOverrideRequest, Executor, OutcomeReceiver)} request |
| --- | --- |
| [AddAdSelectionOverrideRequest](../android/adservices/adselection/AddAdSelectionOverrideRequest.md) | This POJO represents the `https://developer.android.com/reference/kotlin/android/adservices/adselection/TestAdSelectionManager#overrideAdSelectionConfigRemoteInfo(android.adservices.adselection.AddAdSelectionOverrideRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` request |
| [AdSelectionConfig](../android/adservices/adselection/AdSelectionConfig.md) | Contains the configuration of the ad selection process. |
| [AdSelectionFromOutcomesConfig](../android/adservices/adselection/AdSelectionFromOutcomesConfig.md) | Contains the configuration of the ad selection process that select a winner from a given list of ad selection ids. |
| --- | --- |
| [AdSelectionManager](../android/adservices/adselection/AdSelectionManager.md) | AdSelection Manager provides APIs for app and ad-SDKs to run ad selection processes as well as report impressions. |
| [AdSelectionOutcome](../android/adservices/adselection/AdSelectionOutcome.md) | This class represents a field in the `OutcomeReceiver`, which is an input to the android. |
| [AdWithBid](../android/adservices/adselection/AdWithBid.md) | Represents an ad and its corresponding bid value after the bid generation step in the ad selection process. |
| --- | --- |
| [DecisionLogic](../android/adservices/adselection/DecisionLogic.md) | Generic Decision logic that could be provided by the buyer or seller. |
| [GetAdSelectionDataOutcome](../android/adservices/adselection/GetAdSelectionDataOutcome.md) | Represents ad selection data collected from device for ad selection. |
| [GetAdSelectionDataRequest](../android/adservices/adselection/GetAdSelectionDataRequest.md) | Represents a request containing the information to get ad selection data. |
| --- | --- |
| [PerBuyerConfiguration](../android/adservices/adselection/PerBuyerConfiguration.md) | Contains a per buyer configuration which will be used as part of a `https://developer.android.com/reference/kotlin/android/adservices/adselection/SellerConfiguration` in a `https://developer.android.com/reference/kotlin/android/adservices/adselection/GetAdSelectionDataRequest`. |
| [PerBuyerDecisionLogic](../android/adservices/adselection/PerBuyerDecisionLogic.md) | The override object for decision logic JS per buyer for `https://developer.android.com/reference/kotlin/android/adservices/adselection/SignedContextualAds`. |
| [PersistAdSelectionResultRequest](../android/adservices/adselection/PersistAdSelectionResultRequest.md) | Represents a request containing the seller, the ad selection data id and data. |
| --- | --- |
| [RemoveAdSelectionFromOutcomesOverrideRequest](../android/adservices/adselection/RemoveAdSelectionFromOutcomesOverrideRequest.md) | This POJO represents the `https://developer.android.com/reference/kotlin/android/adservices/adselection/TestAdSelectionManager` request |
| [RemoveAdSelectionOverrideRequest](../android/adservices/adselection/RemoveAdSelectionOverrideRequest.md) | This POJO represents the `https://developer.android.com/reference/kotlin/android/adservices/adselection/TestAdSelectionManager#removeAdSelectionConfigRemoteInfoOverride(android.adservices.adselection.RemoveAdSelectionOverrideRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` request |
| [ReportEventRequest](../android/adservices/adselection/ReportEventRequest.md) | Request object wrapping the required arguments needed to report an ad event. |
| --- | --- |
| [ReportImpressionRequest](../android/adservices/adselection/ReportImpressionRequest.md) | Represent input parameters to the reportImpression API. |
| [SellerConfiguration](../android/adservices/adselection/SellerConfiguration.md) | This object will be part of the `https://developer.android.com/reference/kotlin/android/adservices/adselection/GetAdSelectionDataRequest` and will be constructed and used by the SDK to influence the size of the response of `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#getAdSelectionData(android.adservices.adselection.GetAdSelectionDataRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` |
| [SetAppInstallAdvertisersRequest](../android/adservices/adselection/SetAppInstallAdvertisersRequest.md) | Represents input parameters to the setAppInstallAdvertiser API. |
| --- | --- |
| [SignedContextualAds](../android/adservices/adselection/SignedContextualAds.md) | Contains a list of buyer supplied `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdWithBid` bundle and its signature. |
| [TestAdSelectionManager](../android/adservices/adselection/TestAdSelectionManager.md) | `https://developer.android.com/reference/kotlin/android/adservices/adselection/TestAdSelectionManager` provides APIs for apps and ad SDKs to test ad selection processes. |
| [UpdateAdCounterHistogramRequest](../android/adservices/adselection/UpdateAdCounterHistogramRequest.md) | Request object wrapping the required arguments needed to update an ad counter histogram. |
| --- | --- |
