# GetWalletCardsCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GetWalletCardsCallback

Kotlin| [Java](https://developer.android.com/reference/android/service/quickaccesswallet/GetWalletCardsCallback "View this page in Java") 

```
interface GetWalletCardsCallback
```

| [android.service.quickaccesswallet.GetWalletCardsCallback](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsCallback#) |

Handles response from the [QuickAccessWalletService](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/QuickAccessWalletService) for [GetWalletCardsRequest](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsRequest)

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFailure](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsCallback#onFailure(android.service.quickaccesswallet.GetWalletCardsError))`(`error:` ` [GetWalletCardsError](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsError)`)` Notifies the Android System that an [QuickAccessWalletService.onWalletCardsRequested](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/QuickAccessWalletService#onWalletCardsRequested(android.service.quickaccesswallet.GetWalletCardsRequest,%20android.service.quickaccesswallet.GetWalletCardsCallback))could not be handled by the service. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSuccess](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsCallback#onSuccess(android.service.quickaccesswallet.GetWalletCardsResponse))`(`response:` ` [GetWalletCardsResponse](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsResponse)`)` Notifies the Android System that an [QuickAccessWalletService.onWalletCardsRequested](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/QuickAccessWalletService#onWalletCardsRequested(android.service.quickaccesswallet.GetWalletCardsRequest,%20android.service.quickaccesswallet.GetWalletCardsCallback))was successfully handled by the service. |

## Public methods

### onFailure

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFailure(error: GetWalletCardsError): Unit
```

Notifies the Android System that an [QuickAccessWalletService.onWalletCardsRequested](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/QuickAccessWalletService#onWalletCardsRequested(android.service.quickaccesswallet.GetWalletCardsRequest,%20android.service.quickaccesswallet.GetWalletCardsCallback))could not be handled by the service.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `error` | [GetWalletCardsError](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsError):The error message.**Note:** this message should**not** contain PII (Personally Identifiable Information, such as username or email address). This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this method or [onSuccess](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsCallback#onSuccess(android.service.quickaccesswallet.GetWalletCardsResponse))was already called. |

### onSuccess

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSuccess(response: GetWalletCardsResponse): Unit
```

Notifies the Android System that an [QuickAccessWalletService.onWalletCardsRequested](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/QuickAccessWalletService#onWalletCardsRequested(android.service.quickaccesswallet.GetWalletCardsRequest,%20android.service.quickaccesswallet.GetWalletCardsCallback))was successfully handled by the service.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `response` | [GetWalletCardsResponse](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsResponse):The response contains the list of [walletCards](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard) to be shown to the user as well as the index of the card that should initially be presented as the selected card. The list should not contain more than the maximum number of cards requested. This value cannot be`null`. |
