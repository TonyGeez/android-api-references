# android.service.quickaccesswallet

# android.service.quickaccesswallet

Kotlin| [Java](https://developer.android.com/reference/android/service/quickaccesswallet/package-summary "View this page in Java")

## Interfaces

| [GetWalletCardsCallback](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsCallback) | Handles response from the [QuickAccessWalletService](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/QuickAccessWalletService) for [GetWalletCardsRequest](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsRequest) |

## Classes

| [GetWalletCardsError](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsError) | Error response for an [GetWalletCardsRequest](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsRequest). |
| [GetWalletCardsRequest](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsRequest) | Represents a request to a [QuickAccessWalletService](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/QuickAccessWalletService) for [walletCards](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard). |
| [GetWalletCardsResponse](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsResponse) | The response for an [GetWalletCardsRequest](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsRequest) contains a list of wallet cards and the index of the card that should initially be displayed in the 'selected' position. |
| [QuickAccessWalletService](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/QuickAccessWalletService) | A`QuickAccessWalletService`provides a list of`WalletCard`s shown in the Quick Access Wallet. |
| [SelectWalletCardRequest](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/SelectWalletCardRequest) | Represents a request to a [QuickAccessWalletService](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/QuickAccessWalletService) to select a particular [walletCard](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard). |
| [WalletCard](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard) | A [WalletCard](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard) can represent anything that a user might carry in their wallet -- a credit card, library card, transit pass, etc. |
| [WalletServiceEvent](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletServiceEvent) | Represents a request from the [wallet app](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/QuickAccessWalletService) to the Quick Access Wallet in System UI. |
