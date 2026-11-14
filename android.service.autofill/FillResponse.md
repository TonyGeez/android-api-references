# FillResponse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FillResponse

Kotlin| [Java](FillResponse.md) 
| --- | --- |

```
class FillResponse : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.autofill.FillResponse](FillResponse.md) |

Response for an [android.service.autofill.AutofillService#onFillRequest(android.service.autofill.FillRequest,android.os.CancellationSignal,android.service.autofill.FillCallback)](AutofillService.md)).

See the main [AutofillService](AutofillService.md) documentation for more details and examples.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/service/autofill/FillResponse.Builder.md) Builder for [FillResponse](FillResponse.md) objects. |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_DELAY_FILL](FillResponse.md) Flag used to request to wait for a delayed fill from the remote Autofill service if it's passed to [Builder.setFlags(int)](../android/service/autofill/FillResponse.Builder.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_DISABLE_ACTIVITY_ONLY](FillResponse.md) Flag used to change the behavior of [FillResponse.Builder.disableAutofill(long)](../android/service/autofill/FillResponse.Builder.md))--- when this flag is passed to [Builder.setFlags(int)](../android/service/autofill/FillResponse.Builder.md)), autofill is disabled only for the activiy that generated the [FillRequest](FillRequest.md), not the whole app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_TRACK_CONTEXT_COMMITED](FillResponse.md) Flag used to generate [events](../android/service/autofill/FillEventHistory.Event.md) of type [FillEventHistory.Event.TYPE_CONTEXT_COMMITTED](../android/service/autofill/FillEventHistory.Event.md)---if this flag is not passed to [Builder.setFlags(int)](../android/service/autofill/FillResponse.Builder.md)), these events are not generated. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](FillResponse.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](FillResponse.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](FillResponse.md))`(`parcel:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [FillResponse](FillResponse.md)!\> | [CREATOR](FillResponse.md) <br /> |

## Constants

### FLAG_DELAY_FILL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_DELAY_FILL: Int
```

Flag used to request to wait for a delayed fill from the remote Autofill service if it's passed to [Builder.setFlags(int)](../android/service/autofill/FillResponse.Builder.md)).

Some datasets (i.e. OTP) take time to produce. This flags allows remote service to send a [FillResponse](FillResponse.md) to the latest [FillRequest](FillRequest.md) via [FillRequest.getDelayedFillIntentSender()](FillRequest.md))even if the original [FillCallback](FillCallback.md) has timed out. 

 Value: 4

### FLAG_DISABLE_ACTIVITY_ONLY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_DISABLE_ACTIVITY_ONLY: Int
```

Flag used to change the behavior of [FillResponse.Builder.disableAutofill(long)](../android/service/autofill/FillResponse.Builder.md))--- when this flag is passed to [Builder.setFlags(int)](../android/service/autofill/FillResponse.Builder.md)), autofill is disabled only for the activiy that generated the [FillRequest](FillRequest.md), not the whole app. 

 Value: 2

### FLAG_TRACK_CONTEXT_COMMITED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_TRACK_CONTEXT_COMMITED: Int
```

Flag used to generate [events](../android/service/autofill/FillEventHistory.Event.md) of type [FillEventHistory.Event.TYPE_CONTEXT_COMMITTED](../android/service/autofill/FillEventHistory.Event.md)---if this flag is not passed to [Builder.setFlags(int)](../android/service/autofill/FillResponse.Builder.md)), these events are not generated. 

 Value: 1

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<FillResponse!>
```
