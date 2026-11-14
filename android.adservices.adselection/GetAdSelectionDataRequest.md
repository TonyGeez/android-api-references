Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions)

# GetAdSelectionDataRequest

Kotlin | [Java](https://developer.android.com/reference/android/adservices/adselection/GetAdSelectionDataRequest "View this page in Java")
| --- | --- |

```
class GetAdSelectionDataRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.GetAdSelectionDataRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/GetAdSelectionDataRequest#) |

Represents a request containing the information to get ad selection data.

Instances of this class are created by SDKs to be provided as arguments to the `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager#getAdSelectionData(android.adservices.adselection.GetAdSelectionDataRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` methods in `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionManager`.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/adservices/adselection/GetAdSelectionDataRequest.Builder` Builder for `https://developer.android.com/reference/kotlin/android/adservices/adselection/GetAdSelectionDataRequest#` objects. |

| Public methods ||
|---|---|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | `https://developer.android.com/reference/kotlin/android/adservices/adselection/GetAdSelectionDataRequest#getCoordinatorOriginUri()()` <br /> |
| [AdTechIdentifier](https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#)? | `https://developer.android.com/reference/kotlin/android/adservices/adselection/GetAdSelectionDataRequest#getSeller()()` <br /> |
| [SellerConfiguration](https://developer.android.com/reference/kotlin/android/adservices/adselection/SellerConfiguration)? | `https://developer.android.com/reference/kotlin/android/adservices/adselection/GetAdSelectionDataRequest#getSellerConfiguration()()` Returns the seller ad tech's requested payload configuration, set by the calling SDK, to optimize the payload. |
| --- | --- |

## Public methods

### getCoordinatorOriginUri

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions)

```
fun getCoordinatorOriginUri(): Uri?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | the coordinator origin Uri where the public keys for encryption are fetched from See `https://developer.android.com/reference/kotlin/android/adservices/adselection/GetAdSelectionDataRequest.Builder#setCoordinatorOriginUri(android.net.Uri)` for more details on the coordinator origin. This value may be `null`. |

### getSeller

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions)

```
fun getSeller(): AdTechIdentifier?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#?` | a AdTechIdentifier of the seller, for example "www.example-ssp.com". This value may be `null`. |

### getSellerConfiguration

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions)

```
fun getSellerConfiguration(): SellerConfiguration?
```

Returns the seller ad tech's requested payload configuration, set by the calling SDK, to optimize the payload.

If this is `null`, the service will send all data available.
