# FillResponse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FillResponse

Kotlin| [Java](https://developer.android.com/reference/android/service/autofill/FillResponse "View this page in Java") 

```
class FillResponse : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.service.autofill.FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse#) |

Response for an [android.service.autofill.AutofillService#onFillRequest(android.service.autofill.FillRequest,android.os.CancellationSignal,android.service.autofill.FillCallback)](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onFillRequest(android.service.autofill.FillRequest,%20android.os.CancellationSignal,%20android.service.autofill.FillCallback)).

See the main [AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService) documentation for more details and examples.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse.Builder) Builder for [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse#) objects. |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_DELAY_FILL](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse#FLAG_DELAY_FILL:kotlin.Int) Flag used to request to wait for a delayed fill from the remote Autofill service if it's passed to [Builder.setFlags(int)](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse.Builder#setFlags(kotlin.Int)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_DISABLE_ACTIVITY_ONLY](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse#FLAG_DISABLE_ACTIVITY_ONLY:kotlin.Int) Flag used to change the behavior of [FillResponse.Builder.disableAutofill(long)](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse.Builder#disableAutofill(kotlin.Long))--- when this flag is passed to [Builder.setFlags(int)](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse.Builder#setFlags(kotlin.Int)), autofill is disabled only for the activiy that generated the [FillRequest](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest), not the whole app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_TRACK_CONTEXT_COMMITED](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse#FLAG_TRACK_CONTEXT_COMMITED:kotlin.Int) Flag used to generate [events](https://developer.android.com/reference/kotlin/android/service/autofill/FillEventHistory.Event) of type [FillEventHistory.Event.TYPE_CONTEXT_COMMITTED](https://developer.android.com/reference/kotlin/android/service/autofill/FillEventHistory.Event#TYPE_CONTEXT_COMMITTED:kotlin.Int)---if this flag is not passed to [Builder.setFlags(int)](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse.Builder#setFlags(kotlin.Int)), these events are not generated. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse#describeContents())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### FLAG_DELAY_FILL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_DELAY_FILL: Int
```

Flag used to request to wait for a delayed fill from the remote Autofill service if it's passed to [Builder.setFlags(int)](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse.Builder#setFlags(kotlin.Int)).

Some datasets (i.e. OTP) take time to produce. This flags allows remote service to send a [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse#) to the latest [FillRequest](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest) via [FillRequest.getDelayedFillIntentSender()](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#getDelayedFillIntentSender())even if the original [FillCallback](https://developer.android.com/reference/kotlin/android/service/autofill/FillCallback) has timed out. 

 Value: 4

### FLAG_DISABLE_ACTIVITY_ONLY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_DISABLE_ACTIVITY_ONLY: Int
```

Flag used to change the behavior of [FillResponse.Builder.disableAutofill(long)](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse.Builder#disableAutofill(kotlin.Long))--- when this flag is passed to [Builder.setFlags(int)](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse.Builder#setFlags(kotlin.Int)), autofill is disabled only for the activiy that generated the [FillRequest](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest), not the whole app. 

 Value: 2

### FLAG_TRACK_CONTEXT_COMMITED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_TRACK_CONTEXT_COMMITED: Int
```

Flag used to generate [events](https://developer.android.com/reference/kotlin/android/service/autofill/FillEventHistory.Event) of type [FillEventHistory.Event.TYPE_CONTEXT_COMMITTED](https://developer.android.com/reference/kotlin/android/service/autofill/FillEventHistory.Event#TYPE_CONTEXT_COMMITTED:kotlin.Int)---if this flag is not passed to [Builder.setFlags(int)](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse.Builder#setFlags(kotlin.Int)), these events are not generated. 

 Value: 1

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<FillResponse!>
```
