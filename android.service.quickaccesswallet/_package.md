# android.service.quickaccesswallet

# android.service.quickaccesswallet

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [GetWalletCardsCallback](GetWalletCardsCallback.md) | Handles response from the [QuickAccessWalletService](QuickAccessWalletService.md) for [GetWalletCardsRequest](GetWalletCardsRequest.md) |
| --- | --- |

## Classes

| [GetWalletCardsError](GetWalletCardsError.md) | Error response for an [GetWalletCardsRequest](GetWalletCardsRequest.md). |
| --- | --- |
| [GetWalletCardsRequest](GetWalletCardsRequest.md) | Represents a request to a [QuickAccessWalletService](QuickAccessWalletService.md) for [walletCards](WalletCard.md). |
| [GetWalletCardsResponse](GetWalletCardsResponse.md) | The response for an [GetWalletCardsRequest](GetWalletCardsRequest.md) contains a list of wallet cards and the index of the card that should initially be displayed in the 'selected' position. |
| [QuickAccessWalletService](QuickAccessWalletService.md) | A`QuickAccessWalletService`provides a list of`WalletCard`s shown in the Quick Access Wallet. |
| --- | --- |
| [SelectWalletCardRequest](SelectWalletCardRequest.md) | Represents a request to a [QuickAccessWalletService](QuickAccessWalletService.md) to select a particular [walletCard](WalletCard.md). |
| [WalletCard](WalletCard.md) | A [WalletCard](WalletCard.md) can represent anything that a user might carry in their wallet -- a credit card, library card, transit pass, etc. |
| [WalletServiceEvent](WalletServiceEvent.md) | Represents a request from the [wallet app](QuickAccessWalletService.md) to the Quick Access Wallet in System UI. |
| --- | --- |
