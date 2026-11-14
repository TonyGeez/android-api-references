# FillEventHistory

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FillEventHistory

Kotlin| [Java](https://developer.android.com/reference/android/service/autofill/FillEventHistory "View this page in Java") 
| --- | --- |

```
class FillEventHistory : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.autofill.FillEventHistory](https://developer.android.com/reference/kotlin/android/service/autofill/FillEventHistory#) |

Describes what happened after the last [AutofillService.onFillRequest(FillRequest, android.os.CancellationSignal, FillCallback)](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onFillRequest(android.service.autofill.FillRequest,%20android.os.CancellationSignal,%20android.service.autofill.FillCallback))call.

This history is typically used to keep track of previous user actions to optimize further requests. For example, the service might return email addresses in alphabetical order by default, but change that order based on the address the user picked on previous requests.

The history is not persisted over reboots, and it's cleared every time the service replies to a [AutofillService.onFillRequest(FillRequest, android.os.CancellationSignal, FillCallback)](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onFillRequest(android.service.autofill.FillRequest,%20android.os.CancellationSignal,%20android.service.autofill.FillCallback))by calling [FillCallback.onSuccess(FillResponse)](https://developer.android.com/reference/kotlin/android/service/autofill/FillCallback#onSuccess(android.service.autofill.FillResponse))or [FillCallback.onFailure(CharSequence)](https://developer.android.com/reference/kotlin/android/service/autofill/FillCallback#onFailure(kotlin.CharSequence))(if the service doesn't call any of these methods, the history will clear out after some pre-defined time).

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Event](https://developer.android.com/reference/kotlin/android/service/autofill/FillEventHistory.Event) Description of an event that occurred after the latest call to [FillCallback.onSuccess(FillResponse)](https://developer.android.com/reference/kotlin/android/service/autofill/FillCallback#onSuccess(android.service.autofill.FillResponse)). |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/service/autofill/FillEventHistory#describeContents())`()` <br /> |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | [getClientState](https://developer.android.com/reference/kotlin/android/service/autofill/FillEventHistory#getClientState())`()` Returns the client state set in the previous [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse). |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [FillEventHistory.Event](https://developer.android.com/reference/kotlin/android/service/autofill/FillEventHistory.Event)!\>? | [getEvents](https://developer.android.com/reference/kotlin/android/service/autofill/FillEventHistory#getEvents())`()` Returns the events occurred after the latest call to [FillCallback.onSuccess(FillResponse)](https://developer.android.com/reference/kotlin/android/service/autofill/FillCallback#onSuccess(android.service.autofill.FillResponse)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSessionId](https://developer.android.com/reference/kotlin/android/service/autofill/FillEventHistory#getSessionId())`()` Returns the unique identifier of this FillEventHistory. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/service/autofill/FillEventHistory#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/service/autofill/FillEventHistory#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [FillEventHistory](https://developer.android.com/reference/kotlin/android/service/autofill/FillEventHistory#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/service/autofill/FillEventHistory#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getClientState

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClientState(): Bundle?
```

**Deprecated:** *use [getEvents()](https://developer.android.com/reference/kotlin/android/service/autofill/FillEventHistory#getEvents())then [Event.getClientState()](https://developer.android.com/reference/kotlin/android/service/autofill/FillEventHistory.Event#getClientState())instead.*

Returns the client state set in the previous [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse).

**Note:** the state is associated with the app that was autofilled in the previous [AutofillService.onFillRequest(FillRequest, android.os.CancellationSignal, FillCallback)](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onFillRequest(android.service.autofill.FillRequest,%20android.os.CancellationSignal,%20android.service.autofill.FillCallback)), which is not necessary the same app being autofilled now.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | This value may be`null`. |

### getEvents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEvents(): MutableList<FillEventHistory.Event!>?
```

Returns the events occurred after the latest call to [FillCallback.onSuccess(FillResponse)](https://developer.android.com/reference/kotlin/android/service/autofill/FillCallback#onSuccess(android.service.autofill.FillResponse)).

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [FillEventHistory.Event](https://developer.android.com/reference/kotlin/android/service/autofill/FillEventHistory.Event)!>? | The list of events or`null`if non occurred. |

### getSessionId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSessionId(): Int
```

Returns the unique identifier of this FillEventHistory.

This is used to differentiate individual FillEventHistory. 

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
static val CREATOR: Parcelable.Creator<FillEventHistory!>
```
