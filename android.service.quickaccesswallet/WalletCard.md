# WalletCard

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WalletCard

Kotlin| [Java](https://developer.android.com/reference/android/service/quickaccesswallet/WalletCard "View this page in Java") 

```
class WalletCard : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.service.quickaccesswallet.WalletCard](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard#) |

A [WalletCard](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard#) can represent anything that a user might carry in their wallet -- a credit card, library card, transit pass, etc. Cards are identified by a String identifier and contain a card type, card image, card image content description, and a [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) to be used if the user clicks on the card. Cards may be displayed with an icon and label, though these are optional. Non-payment cards will also have a second image that will be displayed when the card is tapped.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard.Builder) Builder for [WalletCard](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard#) objects. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CARD_TYPE_NON_PAYMENT](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard#CARD_TYPE_NON_PAYMENT:kotlin.Int) Non-payment cards refer to any cards that are not used for cash-equivalent payment, including event tickets, flights, offers, loyalty cards, gift cards and transit tickets. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CARD_TYPE_PAYMENT](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard#CARD_TYPE_PAYMENT:kotlin.Int) Payment cards refer to credit cards, debit cards or any other cards in the wallet used to make cash-equivalent payments. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CARD_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard#CARD_TYPE_UNKNOWN:kotlin.Int) Unknown cards refer to cards whose types are unspecified. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard#describeContents())`()` <br /> |
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#)? | [getCardIcon](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard#getCardIcon())`()` An icon may be shown alongside the card image to convey information about how the card can be used, or if some other action must be taken before using the card. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getCardId](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard#getCardId())`()` The card id must be unique within the list of cards returned. |
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#) | [getCardImage](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard#getCardImage())`()` The visual representation of the card. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getCardLabel](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard#getCardLabel())`()` A card label may be shown alongside the card image to convey information about how the card can be used, or if some other action must be taken before using the card. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Location](https://developer.android.com/reference/kotlin/android/location/Location.html#)!\> | [getCardLocations](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard#getCardLocations())`()` List of locations that this card might be useful at. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCardType](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard#getCardType())`()` Returns the card type. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getContentDescription](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard#getContentDescription())`()` The content description of the card image. |
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#)? | [getNonPaymentCardSecondaryImage](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard#getNonPaymentCardSecondaryImage())`()` Visual representation of the card when it is tapped. |
| [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) | [getPendingIntent](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard#getPendingIntent())`()` If the user performs a click on the card, this PendingIntent will be sent. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [WalletCard](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard#CREATOR:android.os.Parcelable.Creator) <br /> |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getCardIcon

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCardIcon(): Icon?
```

An icon may be shown alongside the card image to convey information about how the card can be used, or if some other action must be taken before using the card. For example, an NFC logo could indicate that the card is NFC-enabled and will be provided to an NFC terminal if the phone is held in close proximity to the NFC reader.

If the supplied Icon is backed by a bitmap, it should have width and height [GetWalletCardsRequest.getIconSizePx()](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsRequest#getIconSizePx()).

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------|
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#)? | This value may be`null`. |

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

The visual representation of the card. If the card image Icon is a bitmap, it should have a width of [GetWalletCardsRequest.getCardWidthPx()](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsRequest#getCardWidthPx())and a height of [android.service.quickaccesswallet.GetWalletCardsRequest#getCardHeightPx()](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsRequest#getCardHeightPx()).

| Return ||
|---------------------------------------------------------------------------------------------|-----------------------------|
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#) | This value cannot be`null`. |

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
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Location](https://developer.android.com/reference/kotlin/android/location/Location.html#)!> | This value cannot be`null`. |

### getCardType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCardType(): Int
```

Returns the card type.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | This value cannot be`null`. Value is [android.service.quickaccesswallet.WalletCard#CARD_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard#CARD_TYPE_UNKNOWN:kotlin.Int), [android.service.quickaccesswallet.WalletCard#CARD_TYPE_PAYMENT](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard#CARD_TYPE_PAYMENT:kotlin.Int), or [android.service.quickaccesswallet.WalletCard#CARD_TYPE_NON_PAYMENT](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard#CARD_TYPE_NON_PAYMENT:kotlin.Int) |

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
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#)? | This value may be`null`. |

### getPendingIntent

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPendingIntent(): PendingIntent
```

If the user performs a click on the card, this PendingIntent will be sent. If the device is locked, the wallet will first request device unlock before sending the pending intent.

| Return ||
|-------------------------------------------------------------------------------------------------|-----------------------------|
| [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) | This value cannot be`null`. |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<WalletCard!>
```
