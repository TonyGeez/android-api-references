# FillEventHistory

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FillEventHistory

Kotlin| [Java](../android/service/autofill/FillEventHistory.md) 
| --- | --- |

```
class FillEventHistory : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.autofill.FillEventHistory](../android/service/autofill/FillEventHistory.md) |

Describes what happened after the last [AutofillService.onFillRequest(FillRequest, android.os.CancellationSignal, FillCallback)](../android/service/autofill/AutofillService.md))call.

This history is typically used to keep track of previous user actions to optimize further requests. For example, the service might return email addresses in alphabetical order by default, but change that order based on the address the user picked on previous requests.

The history is not persisted over reboots, and it's cleared every time the service replies to a [AutofillService.onFillRequest(FillRequest, android.os.CancellationSignal, FillCallback)](../android/service/autofill/AutofillService.md))by calling [FillCallback.onSuccess(FillResponse)](../android/service/autofill/FillCallback.md))or [FillCallback.onFailure(CharSequence)](../android/service/autofill/FillCallback.md))(if the service doesn't call any of these methods, the history will clear out after some pre-defined time).

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Event](../android/service/autofill/FillEventHistory.Event.md) Description of an event that occurred after the latest call to [FillCallback.onSuccess(FillResponse)](../android/service/autofill/FillCallback.md)). |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/service/autofill/FillEventHistory.md))`()` <br /> |
| [Bundle](../android/os/Bundle.md)? | [getClientState](../android/service/autofill/FillEventHistory.md))`()` Returns the client state set in the previous [FillResponse](../android/service/autofill/FillResponse.md). |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [FillEventHistory.Event](../android/service/autofill/FillEventHistory.Event.md)!\>? | [getEvents](../android/service/autofill/FillEventHistory.md))`()` Returns the events occurred after the latest call to [FillCallback.onSuccess(FillResponse)](../android/service/autofill/FillCallback.md)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSessionId](../android/service/autofill/FillEventHistory.md))`()` Returns the unique identifier of this FillEventHistory. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/service/autofill/FillEventHistory.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/service/autofill/FillEventHistory.md))`(`parcel:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [FillEventHistory](../android/service/autofill/FillEventHistory.md)!\> | [CREATOR](../android/service/autofill/FillEventHistory.md) <br /> |

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getClientState

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClientState(): Bundle?
```

**Deprecated:** *use [getEvents()](../android/service/autofill/FillEventHistory.md))then [Event.getClientState()](../android/service/autofill/FillEventHistory.Event.md))instead.*

Returns the client state set in the previous [FillResponse](../android/service/autofill/FillResponse.md).

**Note:** the state is associated with the app that was autofilled in the previous [AutofillService.onFillRequest(FillRequest, android.os.CancellationSignal, FillCallback)](../android/service/autofill/AutofillService.md)), which is not necessary the same app being autofilled now.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [Bundle](../android/os/Bundle.md)? | This value may be`null`. |

### getEvents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEvents(): MutableList<FillEventHistory.Event!>?
```

Returns the events occurred after the latest call to [FillCallback.onSuccess(FillResponse)](../android/service/autofill/FillCallback.md)).

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [FillEventHistory.Event](../android/service/autofill/FillEventHistory.Event.md)!>? | The list of events or`null`if non occurred. |

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<FillEventHistory!>
```
