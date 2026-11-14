# PartialCustomAudience

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions)

# PartialCustomAudience

Kotlin| [Java](https://developer.android.com/reference/android/adservices/customaudience/PartialCustomAudience "View this page in Java") 
| --- | --- |

```
class PartialCustomAudience : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.customaudience.PartialCustomAudience](https://developer.android.com/reference/kotlin/android/adservices/customaudience/PartialCustomAudience#) |

Represents a partial custom audience that is passed along to the buyer ad tech, when scheduling a delayed update for Custom Audience. Any field set by the caller cannot be overridden by the custom audience fetched from the`updateUri`

Given multiple Custom Audiences could be returned by the buyer, we will match the override restriction based on the name of Custom Audience. Thus name would be a required field.

Other nullable fields will not be overridden if left null

For more information about each field refer to [CustomAudience](https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience).

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/adservices/customaudience/PartialCustomAudience.Builder) Builder for [PartialCustomAudience](https://developer.android.com/reference/kotlin/android/adservices/customaudience/PartialCustomAudience#) objects. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/adservices/customaudience/PartialCustomAudience#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/adservices/customaudience/PartialCustomAudience#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)? | [getActivationTime](https://developer.android.com/reference/kotlin/android/adservices/customaudience/PartialCustomAudience#getActivationTime())`()` Reference [CustomAudience.getActivationTime()](https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience#getActivationTime())for details. |
| --- | --- |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)? | [getExpirationTime](https://developer.android.com/reference/kotlin/android/adservices/customaudience/PartialCustomAudience#getExpirationTime())`()` Reference [CustomAudience.getExpirationTime()](https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience#getExpirationTime())for details. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](https://developer.android.com/reference/kotlin/android/adservices/customaudience/PartialCustomAudience#getName())`()` Reference [CustomAudience.getName()](https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience#getName())for details. |
| [AdSelectionSignals](https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#)? | [getUserBiddingSignals](https://developer.android.com/reference/kotlin/android/adservices/customaudience/PartialCustomAudience#getUserBiddingSignals())`()` Reference [CustomAudience.getUserBiddingSignals()](https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience#getUserBiddingSignals())for details. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/adservices/customaudience/PartialCustomAudience#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/adservices/customaudience/PartialCustomAudience#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/adservices/customaudience/PartialCustomAudience#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [PartialCustomAudience](https://developer.android.com/reference/kotlin/android/adservices/customaudience/PartialCustomAudience#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/adservices/customaudience/PartialCustomAudience#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`only if two [PartialCustomAudience](https://developer.android.com/reference/kotlin/android/adservices/customaudience/PartialCustomAudience#) objects contain the same information. |

### getActivationTime

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions) 

```
fun getActivationTime(): Instant?
```

Reference [CustomAudience.getActivationTime()](https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience#getActivationTime())for details. Will not be overridden if left null.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)? | the [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#) by which joining the custom audience will be delayed. |

### getExpirationTime

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions) 

```
fun getExpirationTime(): Instant?
```

Reference [CustomAudience.getExpirationTime()](https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience#getExpirationTime())for details. Will not be overridden if left null.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)? | the [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#) by when the membership to the custom audience will expire. |

### getName

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions) 

```
fun getName(): String
```

Reference [CustomAudience.getName()](https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience#getName())for details.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) name of the custom audience to join. This value cannot be`null`. |

### getUserBiddingSignals

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions) 

```
fun getUserBiddingSignals(): AdSelectionSignals?
```

Reference [CustomAudience.getUserBiddingSignals()](https://developer.android.com/reference/kotlin/android/adservices/customaudience/CustomAudience#getUserBiddingSignals())for details. Will not be overridden if left null.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [AdSelectionSignals](https://developer.android.com/reference/kotlin/android/adservices/common/AdSelectionSignals.html#)? | the buyer signals to be consumed by the buyer-provided JavaScript when the custom audience participates in an ad selection. |

### hashCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hash of the [PartialCustomAudience](https://developer.android.com/reference/kotlin/android/adservices/customaudience/PartialCustomAudience#) object's data. |

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a human-readable representation of [PartialCustomAudience](https://developer.android.com/reference/kotlin/android/adservices/customaudience/PartialCustomAudience#). |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions) 

```
static val CREATOR: Parcelable.Creator<PartialCustomAudience!>
```
