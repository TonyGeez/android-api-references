# GetWalletCardsRequest

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GetWalletCardsRequest

Kotlin| [Java](../android/service/quickaccesswallet/GetWalletCardsRequest.md) 
| --- | --- |

```
class GetWalletCardsRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.quickaccesswallet.GetWalletCardsRequest](../android/service/quickaccesswallet/GetWalletCardsRequest.md) |

Represents a request to a [QuickAccessWalletService](../android/service/quickaccesswallet/QuickAccessWalletService.md) for [walletCards](../android/service/quickaccesswallet/WalletCard.md). Wallet cards may represent anything that a user might carry in their wallet -- a credit card, library card, a transit pass, etc. This request contains the desired size of the card images and icons as well as the maximum number of cards that may be returned in the [GetWalletCardsResponse](../android/service/quickaccesswallet/GetWalletCardsResponse.md).

Cards may be displayed with an optional icon and label. The icon and label should communicate the same idea. For example, if a card can be used at an NFC terminal, the icon could be an NFC icon and the label could inform the user how to interact with the NFC terminal.

The maximum number of cards that may be displayed in the wallet is provided in [getMaxCards()](../android/service/quickaccesswallet/GetWalletCardsRequest.md)). The [QuickAccessWalletService](../android/service/quickaccesswallet/QuickAccessWalletService.md) may provide up to this many cards in the [GetWalletCardsResponse.getWalletCards()](../android/service/quickaccesswallet/GetWalletCardsResponse.md)). If the list of cards provided exceeds this number, some of the cards may not be shown to the user.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GetWalletCardsRequest](../android/service/quickaccesswallet/GetWalletCardsRequest.md))`(`cardWidthPx:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cardHeightPx:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `iconSizePx:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxCards:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new GetWalletCardsRequest. |

| Public methods ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/service/quickaccesswallet/GetWalletCardsRequest.md))`()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCardHeightPx](../android/service/quickaccesswallet/GetWalletCardsRequest.md))`()` The desired height of the [WalletCard.getCardImage()](../android/service/quickaccesswallet/WalletCard.md)), in pixels. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCardWidthPx](../android/service/quickaccesswallet/GetWalletCardsRequest.md))`()` The desired width of the [WalletCard.getCardImage()](../android/service/quickaccesswallet/WalletCard.md)), in pixels. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIconSizePx](../android/service/quickaccesswallet/GetWalletCardsRequest.md))`()` Wallet cards may be displayed next to an icon. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxCards](../android/service/quickaccesswallet/GetWalletCardsRequest.md))`()` The maximum size of the [GetWalletCardsResponse.getWalletCards()](../android/service/quickaccesswallet/GetWalletCardsResponse.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/service/quickaccesswallet/GetWalletCardsRequest.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [GetWalletCardsRequest](../android/service/quickaccesswallet/GetWalletCardsRequest.md)!\> | [CREATOR](../android/service/quickaccesswallet/GetWalletCardsRequest.md) <br /> |

## Public constructors

### GetWalletCardsRequest

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GetWalletCardsRequest(
    cardWidthPx: Int, 
    cardHeightPx: Int, 
    iconSizePx: Int, 
    maxCards: Int)
```

Creates a new GetWalletCardsRequest.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `cardWidthPx` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The width of the card image in pixels. |
| `cardHeightPx` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The height of the card image in pixels. |
| `iconSizePx` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The width and height of the optional card icon in pixels. |
| --- | --- |
| `maxCards` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum number of cards that may be provided in the response. |

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of [writeToParcel(android.os.Parcel,int)](../android/os/Parcelable.md)), the return value of this method must include the [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) bit.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getCardHeightPx

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCardHeightPx(): Int
```

The desired height of the [WalletCard.getCardImage()](../android/service/quickaccesswallet/WalletCard.md)), in pixels. The dimensions of the card image are requested so that it may be rendered without scaling. 

### getCardWidthPx

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCardWidthPx(): Int
```

The desired width of the [WalletCard.getCardImage()](../android/service/quickaccesswallet/WalletCard.md)), in pixels. The dimensions of the card image are requested so that it may be rendered without scaling.

The`cardWidthPx`and`cardHeightPx`should be applied to the size of the [android.service.quickaccesswallet.WalletCard#getCardImage()](../android/service/quickaccesswallet/WalletCard.md)). The size of the card image is specified so that it may be rendered accurately and without distortion caused by scaling. 

### getIconSizePx

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIconSizePx(): Int
```

Wallet cards may be displayed next to an icon. The icon can help to convey additional information about the state of the card. If the provided icon is a bitmap, its width and height should equal iconSizePx so that it is rendered without distortion caused by scaling. 

### getMaxCards

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxCards(): Int
```

The maximum size of the [GetWalletCardsResponse.getWalletCards()](../android/service/quickaccesswallet/GetWalletCardsResponse.md)). If the list of cards exceeds this number, not all cards may be displayed. 

### writeToParcel

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<GetWalletCardsRequest!>
```
