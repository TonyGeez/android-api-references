# PartialCustomAudience

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions)

# PartialCustomAudience

Kotlin| [Java](../android/adservices/customaudience/PartialCustomAudience.md) 
| --- | --- |

```
class PartialCustomAudience : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.customaudience.PartialCustomAudience](../android/adservices/customaudience/PartialCustomAudience.md) |

Represents a partial custom audience that is passed along to the buyer ad tech, when scheduling a delayed update for Custom Audience. Any field set by the caller cannot be overridden by the custom audience fetched from the`updateUri`

Given multiple Custom Audiences could be returned by the buyer, we will match the override restriction based on the name of Custom Audience. Thus name would be a required field.

Other nullable fields will not be overridden if left null

For more information about each field refer to [CustomAudience](../android/adservices/customaudience/CustomAudience.md).

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/adservices/customaudience/PartialCustomAudience.Builder.md) Builder for [PartialCustomAudience](../android/adservices/customaudience/PartialCustomAudience.md) objects. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/adservices/customaudience/PartialCustomAudience.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/adservices/customaudience/PartialCustomAudience.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Instant](../java/time/Instant.md)? | [getActivationTime](../android/adservices/customaudience/PartialCustomAudience.md))`()` Reference [CustomAudience.getActivationTime()](../android/adservices/customaudience/CustomAudience.md))for details. |
| --- | --- |
| [Instant](../java/time/Instant.md)? | [getExpirationTime](../android/adservices/customaudience/PartialCustomAudience.md))`()` Reference [CustomAudience.getExpirationTime()](../android/adservices/customaudience/CustomAudience.md))for details. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](../android/adservices/customaudience/PartialCustomAudience.md))`()` Reference [CustomAudience.getName()](../android/adservices/customaudience/CustomAudience.md))for details. |
| [AdSelectionSignals](../android/adservices/common/AdSelectionSignals.md)? | [getUserBiddingSignals](../android/adservices/customaudience/PartialCustomAudience.md))`()` Reference [CustomAudience.getUserBiddingSignals()](../android/adservices/customaudience/CustomAudience.md))for details. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/adservices/customaudience/PartialCustomAudience.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/adservices/customaudience/PartialCustomAudience.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/adservices/customaudience/PartialCustomAudience.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PartialCustomAudience](../android/adservices/customaudience/PartialCustomAudience.md)!\> | [CREATOR](../android/adservices/customaudience/PartialCustomAudience.md) <br /> |

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`only if two [PartialCustomAudience](../android/adservices/customaudience/PartialCustomAudience.md) objects contain the same information. |

### getActivationTime

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions) 

```
fun getActivationTime(): Instant?
```

Reference [CustomAudience.getActivationTime()](../android/adservices/customaudience/CustomAudience.md))for details. Will not be overridden if left null.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [Instant](../java/time/Instant.md)? | the [Instant](../java/time/Instant.md) by which joining the custom audience will be delayed. |

### getExpirationTime

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions) 

```
fun getExpirationTime(): Instant?
```

Reference [CustomAudience.getExpirationTime()](../android/adservices/customaudience/CustomAudience.md))for details. Will not be overridden if left null.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [Instant](../java/time/Instant.md)? | the [Instant](../java/time/Instant.md) by when the membership to the custom audience will expire. |

### getName

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions) 

```
fun getName(): String
```

Reference [CustomAudience.getName()](../android/adservices/customaudience/CustomAudience.md))for details.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the [String](../java/lang/String.md) name of the custom audience to join. This value cannot be`null`. |

### getUserBiddingSignals

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions) 

```
fun getUserBiddingSignals(): AdSelectionSignals?
```

Reference [CustomAudience.getUserBiddingSignals()](../android/adservices/customaudience/CustomAudience.md))for details. Will not be overridden if left null.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [AdSelectionSignals](../android/adservices/common/AdSelectionSignals.md)? | the buyer signals to be consumed by the buyer-provided JavaScript when the custom audience participates in an ad selection. |

### hashCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hash of the [PartialCustomAudience](../android/adservices/customaudience/PartialCustomAudience.md) object's data. |

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a human-readable representation of [PartialCustomAudience](../android/adservices/customaudience/PartialCustomAudience.md). |

### writeToParcel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions) 

```
static val CREATOR: Parcelable.Creator<PartialCustomAudience!>
```
