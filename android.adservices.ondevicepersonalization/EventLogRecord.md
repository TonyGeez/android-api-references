# EventLogRecord

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EventLogRecord

Kotlin| [Java](https://developer.android.com/reference/android/adservices/ondevicepersonalization/EventLogRecord "View this page in Java") 

```
class EventLogRecord : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.adservices.ondevicepersonalization.EventLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord#) |

Data to be logged in the EVENTS table. Each record in the EVENTS table is associated with one row from an existing [RequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord) in the requests table [RequestLogRecord.getRows()](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord#getRows()). The purpose of the EVENTS table is to add supplemental information to logged data from a prior request, e.g., logging an event when a link in a rendered WebView is clicked`IsolatedWorker#onEvent(EventInput, android.os.OutcomeReceiver)`. The contents of the EVENTS table can be consumed by Federated Learning facilitated model training, or Federated Analytics facilitated cross-device statistical analysis.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord.Builder) A builder for [EventLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord#) |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues.html#)? | [getData](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord#getData())`()` Additional data to be logged. |
| [RequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord)? | [getRequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord#getRequestLogRecord())`()` The existing [RequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord) that this payload should be associated with. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRowIndex](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord#getRowIndex())`()` The index of the row in an existing [RequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord) that this payload should be associated with. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#) | [getTime](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord#getTime())`()` Returns the timestamp of this record. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord#getType())`()` The service-assigned identifier that identifies this payload. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord#hashCode())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [EventLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord#CREATOR:android.os.Parcelable.Creator) <br /> |

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

The existing [RequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord) that this payload should be associated with. In an implementation of [IsolatedWorker.onExecute(ExecuteInput, android.os.OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,%20android.os.OutcomeReceiver)), this should be set to a value returned by [LogReader.getRequests(Instant, Instant)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/LogReader#getRequests(java.time.Instant,%20java.time.Instant)). In an implementation of [IsolatedWorker.onEvent(EventInput, android.os.OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onEvent(android.adservices.ondevicepersonalization.EventInput,%20android.os.OutcomeReceiver)), this should be set to`null`because the payload will be automatically associated with the current [RequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord). 

### getRowIndex

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRowIndex(): Int
```

The index of the row in an existing [RequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord) that this payload should be associated with.

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
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#) | This value cannot be`null`. |

### getType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Int
```

The service-assigned identifier that identifies this payload. Each row in [RequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord) can be associated with up to one event of a specified type. The platform drops events if another event with the same type already exists for a row in [RequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord). Must be \>0 and \<128. This allows up to 127 events to be written for each row in [RequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord). If unspecified, the default is 1.

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<EventLogRecord!>
```
