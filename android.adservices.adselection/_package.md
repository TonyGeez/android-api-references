# android.adservices.adselection

Kotlin | [Java](_package.md)
| --- | --- |

## Classes

| [AddAdSelectionFromOutcomesOverrideRequest](AddAdSelectionFromOutcomesOverrideRequest.md) | This POJO represents the overrideAdSelectionFromOutcomesConfigRemoteInfo ( AddAdSelectionOverrideRequest, Executor, OutcomeReceiver)} request |
| --- | --- |
| [AddAdSelectionOverrideRequest](AddAdSelectionOverrideRequest.md) | This POJO represents the overrideAdSelectionConfigRemoteInfo request |
| [AdSelectionConfig](AdSelectionConfig.md) | Contains the configuration of the ad selection process. |
| [AdSelectionFromOutcomesConfig](AdSelectionFromOutcomesConfig.md) | Contains the configuration of the ad selection process that select a winner from a given list of ad selection ids. |
| --- | --- |
| [AdSelectionManager](AdSelectionManager.md) | AdSelection Manager provides APIs for app and ad-SDKs to run ad selection processes as well as report impressions. |
| [AdSelectionOutcome](AdSelectionOutcome.md) | This class represents a field in the `OutcomeReceiver`, which is an input to the android. |
| [AdWithBid](AdWithBid.md) | Represents an ad and its corresponding bid value after the bid generation step in the ad selection process. |
| --- | --- |
| [DecisionLogic](DecisionLogic.md) | Generic Decision logic that could be provided by the buyer or seller. |
| [GetAdSelectionDataOutcome](GetAdSelectionDataOutcome.md) | Represents ad selection data collected from device for ad selection. |
| [GetAdSelectionDataRequest](GetAdSelectionDataRequest.md) | Represents a request containing the information to get ad selection data. |
| --- | --- |
| [PerBuyerConfiguration](PerBuyerConfiguration.md) | Contains a per buyer configuration which will be used as part of a SellerConfiguration in a GetAdSelectionDataRequest. |
| [PerBuyerDecisionLogic](PerBuyerDecisionLogic.md) | The override object for decision logic JS per buyer for SignedContextualAds. |
| [PersistAdSelectionResultRequest](PersistAdSelectionResultRequest.md) | Represents a request containing the seller, the ad selection data id and data. |
| --- | --- |
| [RemoveAdSelectionFromOutcomesOverrideRequest](RemoveAdSelectionFromOutcomesOverrideRequest.md) | This POJO represents the TestAdSelectionManager request |
| [RemoveAdSelectionOverrideRequest](RemoveAdSelectionOverrideRequest.md) | This POJO represents the removeAdSelectionConfigRemoteInfoOverride request |
| [ReportEventRequest](ReportEventRequest.md) | Request object wrapping the required arguments needed to report an ad event. |
| --- | --- |
| [ReportImpressionRequest](ReportImpressionRequest.md) | Represent input parameters to the reportImpression API. |
| [SellerConfiguration](SellerConfiguration.md) | This object will be part of the GetAdSelectionDataRequest and will be constructed and used by the SDK to influence the size of the response of getAdSelectionData |
| [SetAppInstallAdvertisersRequest](SetAppInstallAdvertisersRequest.md) | Represents input parameters to the setAppInstallAdvertiser API. |
| --- | --- |
| [SignedContextualAds](SignedContextualAds.md) | Contains a list of buyer supplied AdWithBid bundle and its signature. |
| [TestAdSelectionManager](TestAdSelectionManager.md) | TestAdSelectionManager provides APIs for apps and ad SDKs to test ad selection processes. |
| [UpdateAdCounterHistogramRequest](UpdateAdCounterHistogramRequest.md) | Request object wrapping the required arguments needed to update an ad counter histogram. |
| --- | --- |
