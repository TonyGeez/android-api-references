# EventLogRecord

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EventLogRecord

Kotlin| [Java](EventLogRecord.md) 
| --- | --- |

```
class EventLogRecord : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.EventLogRecord](EventLogRecord.md) |

Data to be logged in the EVENTS table. Each record in the EVENTS table is associated with one row from an existing [RequestLogRecord](RequestLogRecord.md) in the requests table [RequestLogRecord.getRows()](RequestLogRecord.md)). The purpose of the EVENTS table is to add supplemental information to logged data from a prior request, e.g., logging an event when a link in a rendered WebView is clicked`IsolatedWorker#onEvent(EventInput, android.os.OutcomeReceiver)`. The contents of the EVENTS table can be consumed by Federated Learning facilitated model training, or Federated Analytics facilitated cross-device statistical analysis.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/adservices/ondevicepersonalization/EventLogRecord.Builder.md) A builder for [EventLogRecord](EventLogRecord.md) |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](EventLogRecord.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](EventLogRecord.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [ContentValues](../android.content/ContentValues.md)? | [getData](EventLogRecord.md))`()` Additional data to be logged. |
| --- | --- |
| [RequestLogRecord](RequestLogRecord.md)? | [getRequestLogRecord](EventLogRecord.md))`()` The existing [RequestLogRecord](RequestLogRecord.md) that this payload should be associated with. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRowIndex](EventLogRecord.md))`()` The index of the row in an existing [RequestLogRecord](RequestLogRecord.md) that this payload should be associated with. |
| [Instant](../java.time/Instant.md) | [getTime](EventLogRecord.md))`()` Returns the timestamp of this record. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](EventLogRecord.md))`()` The service-assigned identifier that identifies this payload. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](EventLogRecord.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](EventLogRecord.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [EventLogRecord](EventLogRecord.md)!\> | [CREATOR](EventLogRecord.md) <br /> |

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getData

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getData(): ContentValues?
```

Additional data to be logged. Can be null if no additional data needs to be written as part of the event, and only the occurrence of the event needs to be logged. 

### getRequestLogRecord

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRequestLogRecord(): RequestLogRecord?
```

The existing [RequestLogRecord](RequestLogRecord.md) that this payload should be associated with. In an implementation of [IsolatedWorker.onExecute(ExecuteInput, android.os.OutcomeReceiver)](IsolatedWorker.md)), this should be set to a value returned by [LogReader.getRequests(Instant, Instant)](LogReader.md)). In an implementation of [IsolatedWorker.onEvent(EventInput, android.os.OutcomeReceiver)](IsolatedWorker.md)), this should be set to`null`because the payload will be automatically associated with the current [RequestLogRecord](RequestLogRecord.md). 

### getRowIndex

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRowIndex(): Int
```

The index of the row in an existing [RequestLogRecord](RequestLogRecord.md) that this payload should be associated with.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 0 or greater |

### getTime

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTime(): Instant
```

Returns the timestamp of this record.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [Instant](../java.time/Instant.md) | This value cannot be`null`. |

### getType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Int
```

The service-assigned identifier that identifies this payload. Each row in [RequestLogRecord](RequestLogRecord.md) can be associated with up to one event of a specified type. The platform drops events if another event with the same type already exists for a row in [RequestLogRecord](RequestLogRecord.md). Must be \>0 and \<128. This allows up to 127 events to be written for each row in [RequestLogRecord](RequestLogRecord.md). If unspecified, the default is 1.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is between 1 and 127 inclusive |

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
| `dest` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<EventLogRecord!>
```
