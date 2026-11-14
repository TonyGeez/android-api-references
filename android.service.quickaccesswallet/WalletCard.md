# WalletCard

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WalletCard

Kotlin| [Java](../android/service/quickaccesswallet/WalletCard.md) 
| --- | --- |

```
class WalletCard : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.quickaccesswallet.WalletCard](../android/service/quickaccesswallet/WalletCard.md) |

A [WalletCard](../android/service/quickaccesswallet/WalletCard.md) can represent anything that a user might carry in their wallet -- a credit card, library card, transit pass, etc. Cards are identified by a String identifier and contain a card type, card image, card image content description, and a [PendingIntent](../android/app/PendingIntent.md) to be used if the user clicks on the card. Cards may be displayed with an icon and label, though these are optional. Non-payment cards will also have a second image that will be displayed when the card is tapped.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/service/quickaccesswallet/WalletCard.Builder.md) Builder for [WalletCard](../android/service/quickaccesswallet/WalletCard.md) objects. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CARD_TYPE_NON_PAYMENT](../android/service/quickaccesswallet/WalletCard.md) Non-payment cards refer to any cards that are not used for cash-equivalent payment, including event tickets, flights, offers, loyalty cards, gift cards and transit tickets. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CARD_TYPE_PAYMENT](../android/service/quickaccesswallet/WalletCard.md) Payment cards refer to credit cards, debit cards or any other cards in the wallet used to make cash-equivalent payments. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CARD_TYPE_UNKNOWN](../android/service/quickaccesswallet/WalletCard.md) Unknown cards refer to cards whose types are unspecified. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/service/quickaccesswallet/WalletCard.md))`()` <br /> |
| [Icon](../android/graphics/drawable/Icon.md)? | [getCardIcon](../android/service/quickaccesswallet/WalletCard.md))`()` An icon may be shown alongside the card image to convey information about how the card can be used, or if some other action must be taken before using the card. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getCardId](../android/service/quickaccesswallet/WalletCard.md))`()` The card id must be unique within the list of cards returned. |
| --- | --- |
| [Icon](../android/graphics/drawable/Icon.md) | [getCardImage](../android/service/quickaccesswallet/WalletCard.md))`()` The visual representation of the card. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getCardLabel](../android/service/quickaccesswallet/WalletCard.md))`()` A card label may be shown alongside the card image to convey information about how the card can be used, or if some other action must be taken before using the card. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Location](../android/location/Location.md)!\> | [getCardLocations](../android/service/quickaccesswallet/WalletCard.md))`()` List of locations that this card might be useful at. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCardType](../android/service/quickaccesswallet/WalletCard.md))`()` Returns the card type. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getContentDescription](../android/service/quickaccesswallet/WalletCard.md))`()` The content description of the card image. |
| [Icon](../android/graphics/drawable/Icon.md)? | [getNonPaymentCardSecondaryImage](../android/service/quickaccesswallet/WalletCard.md))`()` Visual representation of the card when it is tapped. |
| --- | --- |
| [PendingIntent](../android/app/PendingIntent.md) | [getPendingIntent](../android/service/quickaccesswallet/WalletCard.md))`()` If the user performs a click on the card, this PendingIntent will be sent. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/service/quickaccesswallet/WalletCard.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [WalletCard](../android/service/quickaccesswallet/WalletCard.md)!\> | [CREATOR](../android/service/quickaccesswallet/WalletCard.md) <br /> |

## Constants

### CARD_TYPE_NON_PAYMENT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CARD_TYPE_NON_PAYMENT: Int
```

Non-payment cards refer to any cards that are not used for cash-equivalent payment, including event tickets, flights, offers, loyalty cards, gift cards and transit tickets. 

 Value: 2

### CARD_TYPE_PAYMENT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CARD_TYPE_PAYMENT: Int
```

Payment cards refer to credit cards, debit cards or any other cards in the wallet used to make cash-equivalent payments. 

 Value: 1

### CARD_TYPE_UNKNOWN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CARD_TYPE_UNKNOWN: Int
```

Unknown cards refer to cards whose types are unspecified. 

 Value: 0

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getCardIcon

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCardIcon(): Icon?
```

An icon may be shown alongside the card image to convey information about how the card can be used, or if some other action must be taken before using the card. For example, an NFC logo could indicate that the card is NFC-enabled and will be provided to an NFC terminal if the phone is held in close proximity to the NFC reader.

If the supplied Icon is backed by a bitmap, it should have width and height [GetWalletCardsRequest.getIconSizePx()](../android/service/quickaccesswallet/GetWalletCardsRequest.md)).

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------|
| [Icon](../android/graphics/drawable/Icon.md)? | This value may be`null`. |

### getCardId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCardId(): String
```

The card id must be unique within the list of cards returned.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getCardImage

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCardImage(): Icon
```

The visual representation of the card. If the card image Icon is a bitmap, it should have a width of [GetWalletCardsRequest.getCardWidthPx()](../android/service/quickaccesswallet/GetWalletCardsRequest.md))and a height of [android.service.quickaccesswallet.GetWalletCardsRequest#getCardHeightPx()](../android/service/quickaccesswallet/GetWalletCardsRequest.md)).

| Return ||
|---------------------------------------------------------------------------------------------|-----------------------------|
| [Icon](../android/graphics/drawable/Icon.md) | This value cannot be`null`. |

### getCardLabel

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCardLabel(): CharSequence?
```

A card label may be shown alongside the card image to convey information about how the card can be used, or if some other action must be taken before using the card. For example, an NFC-enabled card could be labeled "Hold near reader" to inform the user of how to use NFC cards when interacting with an NFC reader.

If the provided label is too long to fit on one line, it may be truncated and ellipsized.

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | This value may be`null`. |

### getCardLocations

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCardLocations(): MutableList<Location!>
```

List of locations that this card might be useful at.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Location](../android/location/Location.md)!> | This value cannot be`null`. |

### getCardType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCardType(): Int
```

Returns the card type.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | This value cannot be`null`. Value is [android.service.quickaccesswallet.WalletCard#CARD_TYPE_UNKNOWN](../android/service/quickaccesswallet/WalletCard.md), [android.service.quickaccesswallet.WalletCard#CARD_TYPE_PAYMENT](../android/service/quickaccesswallet/WalletCard.md), or [android.service.quickaccesswallet.WalletCard#CARD_TYPE_NON_PAYMENT](../android/service/quickaccesswallet/WalletCard.md) |

### getContentDescription

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContentDescription(): CharSequence
```

The content description of the card image.

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | This value cannot be`null`. |

### getNonPaymentCardSecondaryImage

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNonPaymentCardSecondaryImage(): Icon?
```

Visual representation of the card when it is tapped. May include additional information unique to the card, such as a barcode or number. Only valid for CARD_TYPE_NON_PAYMENT.

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------|
| [Icon](../android/graphics/drawable/Icon.md)? | This value may be`null`. |

### getPendingIntent

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPendingIntent(): PendingIntent
```

If the user performs a click on the card, this PendingIntent will be sent. If the device is locked, the wallet will first request device unlock before sending the pending intent.

| Return ||
|-------------------------------------------------------------------------------------------------|-----------------------------|
| [PendingIntent](../android/app/PendingIntent.md) | This value cannot be`null`. |

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
static val CREATOR: Parcelable.Creator<WalletCard!>
```
