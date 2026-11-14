Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CustomAudience

```
class CustomAudience : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.customaudience.CustomAudience](CustomAudience.md) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The Rubidium (Rb) Relevance APIs, including those in android.adservices.customaudience, are being deprecated. Relevance APIs have no direct replacement. Developers should stop using them, as calls will be rejected in future Android releases. Please refer to official Privacy Sandbox documentation for deprecation and roadmap details: https://privacysandbox.com/news/update-on-plans-for-privacy-sandbox-technologies/

Represents the information necessary for a custom audience to participate in ad selection.

A custom audience is an abstract grouping of users with similar demonstrated interests. This class is a collection of some data stored on a device that is necessary to serve advertisements targeting a single custom audience.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience.Builder` Builder for CustomAudience objects. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience#FLAG_AUCTION_SERVER_REQUEST_OMIT_ADS:kotlin.Int` This auction server request flag indicates to the service that ads for this CustomAudience can be omitted in the server auction payload. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Checks whether two CustomAudience objects contain the same information. |
| [Instant](../java.time/Instant.md)? | getActivationTime On creation of the CustomAudience object, an optional activation time may be set in the future, in order to serve a delayed activation. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AdData](../android.adservices.common/AdData.md)!\> | getAds This list of `https://developer.android.com/reference/kotlin/android/adservices/common/AdData.html#` objects is a full and complete list of the ads that will be served by this CustomAudience during the ad selection process. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getAuctionServerRequestFlags Returns the bitfield of auction server request flags. |
| [Uri](../android.net/Uri.md) | getBiddingLogicUri Returns the target URI used to fetch bidding logic when a custom audience participates in the ad selection process. |
| --- | --- |
| [AdTechIdentifier](../android.adservices.common/AdTechIdentifier.md) | getBuyer A buyer is identified by a domain in the form "buyerexample. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ComponentAdData](../android.adservices.common/ComponentAdData.md)!\> | getComponentAds This list of `https://developer.android.com/reference/kotlin/android/adservices/common/ComponentAdData.html#` objects is a full and complete list of the ad components that will be served by this CustomAudience during the ad selection process. |
| [Uri](../android.net/Uri.md) | getDailyUpdateUri This URI points to a buyer-operated server that hosts updated bidding data and ads metadata to be used in the on-device ad selection process. |
| --- | --- |
| [Instant](../java.time/Instant.md)? | getExpirationTime Once the expiration time has passed, a custom audience is no longer eligible for daily ad/bidding data updates or participation in the ad selection process. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getName The custom audience's name is an arbitrary string provided by the owner and buyer on creation of the CustomAudience object. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | getPriority Returns the priority of this CustomAudience with respect to other CustomAudiences for this buyer. |
| --- | --- |
| [TrustedBiddingData](TrustedBiddingData.md)? | getTrustedBiddingData Trusted bidding data consists of a URI pointing to a trusted server for buyers' bidding data and a list of keys to query the server with. |
| [AdSelectionSignals](../android.adservices.common/AdSelectionSignals.md)? | getUserBiddingSignals User bidding signals are optionally provided by buyers to be consumed by buyer-provided JavaScript during ad selection in an isolated execution environment. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns the hash of the CustomAudience object's data. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [CustomAudience](CustomAudience.md)!\> | `https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### FLAG_AUCTION_SERVER_REQUEST_OMIT_ADS

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_AUCTION_SERVER_REQUEST_OMIT_ADS: Int
```

**Deprecated:** *Deprecated in Java.*

This auction server request flag indicates to the service that ads for this CustomAudience can be omitted in the server auction payload.

 Value: 1

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

**Deprecated:** *Deprecated in Java.*

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks whether two CustomAudience objects contain the same information.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getActivationTime

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getActivationTime(): Instant?
```

**Deprecated:** *Deprecated in Java.*

On creation of the CustomAudience object, an optional activation time may be set in the future, in order to serve a delayed activation. If the field is not set, the CustomAudience will be activated at the time of joining.

For example, a custom audience for lapsed users may not activate until a threshold of inactivity is reached, at which point the custom audience's ads will participate in the ad selection process, potentially redirecting lapsed users to the original owner application.

The maximum delay in activation is 60 days from initial creation.

If specified, the activation time must be an earlier instant than the expiration time.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#?` | the timestamp `https://developer.android.com/reference/kotlin/java/time/Instant.html#`, truncated to milliseconds, after which the custom audience is active. This value may be `null`. |

### getAds

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAds(): MutableList<AdData!>
```

**Deprecated:** *Deprecated in Java.*

This list of `https://developer.android.com/reference/kotlin/android/adservices/common/AdData.html#` objects is a full and complete list of the ads that will be served by this CustomAudience during the ad selection process.

If not specified, or if an empty list is provided, the CustomAudience will not participate in ad selection until a valid list of ads are provided via the daily update for the custom audience.

The combined ads size of the CA is limited and the sizes of each ad's string fields are considered using getBytes in `UTF-8` encoding.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/adservices/common/AdData.html#!>` | a `https://developer.android.com/reference/kotlin/java/util/List.html#` of `https://developer.android.com/reference/kotlin/android/adservices/common/AdData.html#` objects representing ads currently served by the custom audience. This value cannot be `null`. |

### getAuctionServerRequestFlags

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAuctionServerRequestFlags(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the bitfield of auction server request flags. These are flags that influence the creation of the payload generated by the getAdSelectionData API.

To create this bitfield, place an `|` bitwise operator between each android.adservices.customaudience.CustomAudience.AuctionServerRequestFlag to be enabled.
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience#FLAG_AUCTION_SERVER_REQUEST_OMIT_ADS:kotlin.Int` |

### getBiddingLogicUri

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBiddingLogicUri(): Uri
```

**Deprecated:** *Deprecated in Java.*

Returns the target URI used to fetch bidding logic when a custom audience participates in the ad selection process. The URI must use HTTPS.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#` | the URI for fetching buyer bidding logic. This value cannot be `null`. |

### getBuyer

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBuyer(): AdTechIdentifier
```

**Deprecated:** *Deprecated in Java.*

A buyer is identified by a domain in the form "buyerexample.com".

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#` | an `https://developer.android.com/reference/kotlin/android/adservices/common/AdTechIdentifier.html#` containing the custom audience's buyer's domain. This value cannot be `null`. |

### getComponentAds

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 16](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getComponentAds(): MutableList<ComponentAdData!>
```

**Deprecated:** *Deprecated in Java.*

This list of `https://developer.android.com/reference/kotlin/android/adservices/common/ComponentAdData.html#` objects is a full and complete list of the ad components that will be served by this CustomAudience during the ad selection process.

The combined ads size of the CA is limited and the sizes of each ad's string fields are considered using getBytes in `UTF-8` encoding.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/adservices/common/ComponentAdData.html#!>` | a `https://developer.android.com/reference/kotlin/java/util/List.html#` of `https://developer.android.com/reference/kotlin/android/adservices/common/ComponentAdData.html#` objects representing component ads currently served by the custom audience. This value cannot be `null`. |

### getDailyUpdateUri

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDailyUpdateUri(): Uri
```

**Deprecated:** *Deprecated in Java.*

This URI points to a buyer-operated server that hosts updated bidding data and ads metadata to be used in the on-device ad selection process. The URI must use HTTPS.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#` | the custom audience's daily update URI. This value cannot be `null`. |

### getExpirationTime

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExpirationTime(): Instant?
```

**Deprecated:** *Deprecated in Java.*

Once the expiration time has passed, a custom audience is no longer eligible for daily ad/bidding data updates or participation in the ad selection process. The custom audience will then be deleted from memory by the next daily update.

If no expiration time is provided on creation of the CustomAudience, expiry will default to 60 days from activation.

The maximum expiry is 60 days from initial activation.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#?` | the timestamp `https://developer.android.com/reference/kotlin/java/time/Instant.html#`, truncated to milliseconds, after which the custom audience should be removed. This value may be `null`. |

### getName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getName(): String
```

**Deprecated:** *Deprecated in Java.*

The custom audience's name is an arbitrary string provided by the owner and buyer on creation of the CustomAudience object.

The overall size of the CA is limited and the size of this field is considered using getBytes in `UTF-8` encoding.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the String name of the custom audience. This value cannot be `null`. |

### getPriority

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPriority(): Double
```

**Deprecated:** *Deprecated in Java.*

Returns the priority of this CustomAudience with respect to other CustomAudiences for this buyer.

This means if there is insufficient space during buyer input generation in the getAdSelectionData call, the service will attempt to include the highest priority custom audiences first.

The default value if this field is not set is 0.0.

### getTrustedBiddingData

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTrustedBiddingData(): TrustedBiddingData?
```

**Deprecated:** *Deprecated in Java.*

Trusted bidding data consists of a URI pointing to a trusted server for buyers' bidding data and a list of keys to query the server with. Note that the keys are arbitrary identifiers that will only be used to query the trusted server for a buyer's bidding logic during ad selection.

If not specified, the CustomAudience will not participate in ad selection until trusted bidding data are provided via the daily update for the custom audience.

| Return ||
|---|---|
| TrustedBiddingData | a TrustedBiddingData object containing the custom audience's trusted bidding data. This value may be `null`. |

### getUserBiddingSignals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUserBiddingSignals(): AdSelectionSignals?
```

**Deprecated:** *Deprecated in Java.*

User bidding signals are optionally provided by buyers to be consumed by buyer-provided JavaScript during ad selection in an isolated execution environment.

If the user bidding signals are not a valid JSON object that can be consumed by the buyer's JS, the custom audience will not be eligible for ad selection.

If not specified, the CustomAudience will not participate in ad selection until user bidding signals are provided via the daily update for the custom audience.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#?` | an `https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#` object representing the user bidding signals for the custom audience. This value may be `null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the hash of the CustomAudience object's data.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### toString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

**Deprecated:** *Deprecated in Java.*

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<CustomAudience!>
```

**Deprecated:** *Deprecated in Java.*
