# AdWithBid

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions)

# AdWithBid

Kotlin| [Java](https://developer.android.com/reference/android/adservices/adselection/AdWithBid "View this page in Java") 
| --- | --- |

```
class AdWithBid : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.AdWithBid](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdWithBid#) |

Represents an ad and its corresponding bid value after the bid generation step in the ad selection process.

The ads and their bids are fed into an ad scoring process which will inform the final ad selection. The currency unit for the bid is expected to be the same requested by the seller when initiating the selection process and not specified in this class. The seller can provide the currency via AdSelectionSignals. The currency is opaque to FLEDGE.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AdWithBid](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdWithBid#AdWithBid(android.adservices.common.AdData,%20kotlin.Double))`(`adData:` ` [AdData](https://developer.android.com/reference/kotlin/android/adservices/common/AdData.html#)`, `bid:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdWithBid#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdWithBid#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [AdData](https://developer.android.com/reference/kotlin/android/adservices/common/AdData.html#) | [getAdData](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdWithBid#getAdData())`()` <br /> |
| --- | --- |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getBid](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdWithBid#getBid())`()` The bid is the amount of money an advertiser has bid during the ad selection process to show an ad. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdWithBid#hashCode())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdWithBid#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AdWithBid](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdWithBid#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdWithBid#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### AdWithBid

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions) 

```
AdWithBid(
    adData: AdData, 
    bid: Double)
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `adData` | [AdData](https://developer.android.com/reference/kotlin/android/adservices/common/AdData.html#):An [AdData](https://developer.android.com/reference/kotlin/android/adservices/common/AdData.html#) object defining an ad's render URI and buyer metadata This value cannot be`null`. |
| `bid` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):The amount of money a buyer has bid to show an ad; note that while the bid is expected to be non-negative, this is only enforced during the ad selection process |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if adData is null |

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAdData

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions) 

```
fun getAdData(): AdData
```

| Return ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [AdData](https://developer.android.com/reference/kotlin/android/adservices/common/AdData.html#) | the ad that was bid on This value cannot be`null`. |

### getBid

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions) 

```
fun getBid(): Double
```

The bid is the amount of money an advertiser has bid during the ad selection process to show an ad. The bid could be any non-negative`double`, such as 0.00, 0.17, 1.10, or 1000.00.

The currency for a bid would be controlled by Seller and will remain consistent across a run of Ad selection. This could be achieved by leveraging bidding signals during "generateBid()" phase and using the same currency during the creation of contextual ads. Having currency unit as a dedicated field could be supported in future releases.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the bid value to be passed to the scoring function when scoring the ad returned by [getAdData()](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdWithBid#getAdData()) |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### writeToParcel

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions) 

```
static val CREATOR: Parcelable.Creator<AdWithBid!>
```
