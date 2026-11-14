# GetWalletCardsCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GetWalletCardsCallback

Kotlin| [Java](../android/service/quickaccesswallet/GetWalletCardsCallback.md) 
| --- | --- |

```
interface GetWalletCardsCallback
```

| [android.service.quickaccesswallet.GetWalletCardsCallback](../android/service/quickaccesswallet/GetWalletCardsCallback.md) |

Handles response from the [QuickAccessWalletService](../android/service/quickaccesswallet/QuickAccessWalletService.md) for [GetWalletCardsRequest](../android/service/quickaccesswallet/GetWalletCardsRequest.md)

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFailure](../android/service/quickaccesswallet/GetWalletCardsCallback.md))`(`error:` ` [GetWalletCardsError](../android/service/quickaccesswallet/GetWalletCardsError.md)`)` Notifies the Android System that an [QuickAccessWalletService.onWalletCardsRequested](../android/service/quickaccesswallet/QuickAccessWalletService.md))could not be handled by the service. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSuccess](../android/service/quickaccesswallet/GetWalletCardsCallback.md))`(`response:` ` [GetWalletCardsResponse](../android/service/quickaccesswallet/GetWalletCardsResponse.md)`)` Notifies the Android System that an [QuickAccessWalletService.onWalletCardsRequested](../android/service/quickaccesswallet/QuickAccessWalletService.md))was successfully handled by the service. |

## Public methods

### onFailure

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFailure(error: GetWalletCardsError): Unit
```

Notifies the Android System that an [QuickAccessWalletService.onWalletCardsRequested](../android/service/quickaccesswallet/QuickAccessWalletService.md))could not be handled by the service.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `error` | [GetWalletCardsError](../android/service/quickaccesswallet/GetWalletCardsError.md):The error message.**Note:** this message should**not** contain PII (Personally Identifiable Information, such as username or email address). This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this method or [onSuccess](../android/service/quickaccesswallet/GetWalletCardsCallback.md))was already called. |

### onSuccess

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSuccess(response: GetWalletCardsResponse): Unit
```

Notifies the Android System that an [QuickAccessWalletService.onWalletCardsRequested](../android/service/quickaccesswallet/QuickAccessWalletService.md))was successfully handled by the service.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `response` | [GetWalletCardsResponse](../android/service/quickaccesswallet/GetWalletCardsResponse.md):The response contains the list of [walletCards](../android/service/quickaccesswallet/WalletCard.md) to be shown to the user as well as the index of the card that should initially be presented as the selected card. The list should not contain more than the maximum number of cards requested. This value cannot be`null`. |
