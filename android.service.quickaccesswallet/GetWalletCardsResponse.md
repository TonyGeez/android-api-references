# GetWalletCardsResponse

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GetWalletCardsResponse

Kotlin| [Java](https://developer.android.com/reference/android/service/quickaccesswallet/GetWalletCardsResponse "View this page in Java") 

```
class GetWalletCardsResponse : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.service.quickaccesswallet.GetWalletCardsResponse](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsResponse#) |

The response for an [GetWalletCardsRequest](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsRequest) contains a list of wallet cards and the index of the card that should initially be displayed in the 'selected' position.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GetWalletCardsResponse](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsResponse#GetWalletCardsResponse(kotlin.collections.MutableList,%20kotlin.Int))`(`walletCards:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [WalletCard](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard)!>`, `selectedIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Construct a new response. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsResponse#describeContents())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSelectedIndex](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsResponse#getSelectedIndex())`()` The`selectedIndex`represents the index of the card that should be presented in the 'selected' position when the cards are initially displayed in the quick access wallet. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [WalletCard](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard)!\> | [getWalletCards](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsResponse#getWalletCards())`()` The list of [WalletCard](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard) s. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsResponse#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [GetWalletCardsResponse](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsResponse#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsResponse#CREATOR:android.os.Parcelable.Creator) <br /> |

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
| `walletCards` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [WalletCard](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard)!\>:The list of wallet cards. The list may be empty but must NOT be larger than [GetWalletCardsRequest.getMaxCards()](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsRequest#getMaxCards()). The list may not contain null values. |
| `selectedIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the card that should be presented as the initially 'selected' card. The index must be greater than or equal to zero and less than the size of the list of walletCards (unless the list is empty in which case the value may be 0). |

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getSelectedIndex

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSelectedIndex(): Int
```

The`selectedIndex`represents the index of the card that should be presented in the 'selected' position when the cards are initially displayed in the quick access wallet. The`selectedIndex`should be greater than or equal to zero and less than the size of the list of [walletCards](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard), unless the list is empty in which case the`selectedIndex`can take any value. 0 is a nice round number for such cases. 

### getWalletCards

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWalletCards(): MutableList<WalletCard!>
```

The list of [WalletCard](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard) s. The size of this list should not exceed [android.service.quickaccesswallet.GetWalletCardsRequest#getMaxCards()](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsRequest#getMaxCards()).

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [WalletCard](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard)!> | This value cannot be`null`. |

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
static val CREATOR: Parcelable.Creator<GetWalletCardsResponse!>
```
