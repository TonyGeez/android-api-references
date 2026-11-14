# GetWalletCardsCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GetWalletCardsCallback

Kotlin| [Java](GetWalletCardsCallback.md) 
| --- | --- |

```
interface GetWalletCardsCallback
```

| [android.service.quickaccesswallet.GetWalletCardsCallback](GetWalletCardsCallback.md) |

Handles response from the [QuickAccessWalletService](QuickAccessWalletService.md) for [GetWalletCardsRequest](GetWalletCardsRequest.md)

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFailure](GetWalletCardsCallback.md))`(`error:` ` [GetWalletCardsError](GetWalletCardsError.md)`)` Notifies the Android System that an [QuickAccessWalletService.onWalletCardsRequested](QuickAccessWalletService.md))could not be handled by the service. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSuccess](GetWalletCardsCallback.md))`(`response:` ` [GetWalletCardsResponse](GetWalletCardsResponse.md)`)` Notifies the Android System that an [QuickAccessWalletService.onWalletCardsRequested](QuickAccessWalletService.md))was successfully handled by the service. |

## Public methods

### onFailure

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFailure(error: GetWalletCardsError): Unit
```

Notifies the Android System that an [QuickAccessWalletService.onWalletCardsRequested](QuickAccessWalletService.md))could not be handled by the service.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `error` | [GetWalletCardsError](GetWalletCardsError.md):The error message.**Note:** this message should**not** contain PII (Personally Identifiable Information, such as username or email address). This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this method or [onSuccess](GetWalletCardsCallback.md))was already called. |

### onSuccess

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSuccess(response: GetWalletCardsResponse): Unit
```

Notifies the Android System that an [QuickAccessWalletService.onWalletCardsRequested](QuickAccessWalletService.md))was successfully handled by the service.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `response` | [GetWalletCardsResponse](GetWalletCardsResponse.md):The response contains the list of [walletCards](WalletCard.md) to be shown to the user as well as the index of the card that should initially be presented as the selected card. The list should not contain more than the maximum number of cards requested. This value cannot be`null`. |
