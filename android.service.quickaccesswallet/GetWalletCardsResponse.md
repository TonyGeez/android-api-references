# GetWalletCardsResponse

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GetWalletCardsResponse

Kotlin| [Java](../android/service/quickaccesswallet/GetWalletCardsResponse.md) 
| --- | --- |

```
class GetWalletCardsResponse : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.quickaccesswallet.GetWalletCardsResponse](../android/service/quickaccesswallet/GetWalletCardsResponse.md) |

The response for an [GetWalletCardsRequest](../android/service/quickaccesswallet/GetWalletCardsRequest.md) contains a list of wallet cards and the index of the card that should initially be displayed in the 'selected' position.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GetWalletCardsResponse](../android/service/quickaccesswallet/GetWalletCardsResponse.md))`(`walletCards:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [WalletCard](../android/service/quickaccesswallet/WalletCard.md)!>`, `selectedIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Construct a new response. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/service/quickaccesswallet/GetWalletCardsResponse.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSelectedIndex](../android/service/quickaccesswallet/GetWalletCardsResponse.md))`()` The`selectedIndex`represents the index of the card that should be presented in the 'selected' position when the cards are initially displayed in the quick access wallet. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [WalletCard](../android/service/quickaccesswallet/WalletCard.md)!\> | [getWalletCards](../android/service/quickaccesswallet/GetWalletCardsResponse.md))`()` The list of [WalletCard](../android/service/quickaccesswallet/WalletCard.md) s. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/service/quickaccesswallet/GetWalletCardsResponse.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [GetWalletCardsResponse](../android/service/quickaccesswallet/GetWalletCardsResponse.md)!\> | [CREATOR](../android/service/quickaccesswallet/GetWalletCardsResponse.md) <br /> |

## Public constructors

### GetWalletCardsResponse

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GetWalletCardsResponse(
    walletCards: MutableList<WalletCard!>, 
    selectedIndex: Int)
```

Construct a new response.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `walletCards` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [WalletCard](../android/service/quickaccesswallet/WalletCard.md)!\>:The list of wallet cards. The list may be empty but must NOT be larger than [GetWalletCardsRequest.getMaxCards()](../android/service/quickaccesswallet/GetWalletCardsRequest.md)). The list may not contain null values. |
| `selectedIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the card that should be presented as the initially 'selected' card. The index must be greater than or equal to zero and less than the size of the list of walletCards (unless the list is empty in which case the value may be 0). |

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getSelectedIndex

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSelectedIndex(): Int
```

The`selectedIndex`represents the index of the card that should be presented in the 'selected' position when the cards are initially displayed in the quick access wallet. The`selectedIndex`should be greater than or equal to zero and less than the size of the list of [walletCards](../android/service/quickaccesswallet/WalletCard.md), unless the list is empty in which case the`selectedIndex`can take any value. 0 is a nice round number for such cases. 

### getWalletCards

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWalletCards(): MutableList<WalletCard!>
```

The list of [WalletCard](../android/service/quickaccesswallet/WalletCard.md) s. The size of this list should not exceed [android.service.quickaccesswallet.GetWalletCardsRequest#getMaxCards()](../android/service/quickaccesswallet/GetWalletCardsRequest.md)).

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [WalletCard](../android/service/quickaccesswallet/WalletCard.md)!> | This value cannot be`null`. |

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
static val CREATOR: Parcelable.Creator<GetWalletCardsResponse!>
```
