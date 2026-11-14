Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions)

# GetAdSelectionDataRequest

Kotlin | [Java](GetAdSelectionDataRequest.md)
| --- | --- |

```
class GetAdSelectionDataRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.GetAdSelectionDataRequest](GetAdSelectionDataRequest.md) |

Represents a request containing the information to get ad selection data.

Instances of this class are created by SDKs to be provided as arguments to the getAdSelectionData methods in AdSelectionManager.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/adservices/adselection/GetAdSelectionDataRequest.Builder` Builder for GetAdSelectionDataRequest objects. |

| Public methods ||
|---|---|
| [Uri](../android.net/Uri.md)? | getCoordinatorOriginUri <br /> |
| [AdTechIdentifier](../android.adservices.common/AdTechIdentifier.md)? | getSeller <br /> |
| [SellerConfiguration](SellerConfiguration.md)? | getSellerConfiguration Returns the seller ad tech's requested payload configuration, set by the calling SDK, to optimize the payload. |
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
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | the coordinator origin Uri where the public keys for encryption are fetched from See setCoordinatorOriginUri for more details on the coordinator origin. This value may be `null`. |

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
