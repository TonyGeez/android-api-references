# SyncResult

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SyncResult

Kotlin| [Java](SyncResult.md) 
| --- | --- |

```
class SyncResult : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.SyncResult](SyncResult.md) |

This class is used to communicate the results of a sync operation to the SyncManager. Based on the values here the SyncManager will determine the disposition of the sync and whether or not a new sync operation needs to be scheduled in the future.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------|---|
| [SyncResult](SyncResult.md))`()` Create a "clean" SyncResult. |

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](SyncResult.md))`()` Clears the SyncResult to a clean state. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](SyncResult.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasError](SyncResult.md))`()` A convenience method for determining of the SyncResult indicates that an error occurred. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasHardError](SyncResult.md))`()` Convenience method for determining if the SyncResult indicates that a hard error occurred. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasSoftError](SyncResult.md))`()` Convenience method for determining if the SyncResult indicates that a soft error occurred. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [madeSomeProgress](SyncResult.md))`()` Convenience method for determining if the Sync should be rescheduled after failing for some reason. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toDebugString](SyncResult.md))`()` Generates a debugging string indicating the status. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](SyncResult.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](SyncResult.md))`(`parcel:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [SyncResult](SyncResult.md)! | [ALREADY_IN_PROGRESS](SyncResult.md) This instance of a SyncResult is returned by the SyncAdapter in response to a sync request when a sync is already underway. |
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SyncResult](SyncResult.md)!\> | [CREATOR](SyncResult.md) <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [databaseError](SyncResult.md) Used to indicate that the SyncAdapter experienced a hard error due to an error it received from interacting with the storage layer. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [delayUntil](SyncResult.md) Used to indicate to the SyncManager that future sync requests that match the request's Account and authority should be delayed until a time in seconds since Java epoch. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [fullSyncRequested](SyncResult.md) If set the SyncManager will request an immediate sync with the same Account and authority (but empty extras Bundle) as was used in the sync request. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moreRecordsToGet](SyncResult.md) This field is ignored by the SyncManager. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [partialSyncUnavailable](SyncResult.md) This field is ignored by the SyncManager. |
| [SyncStats](SyncStats.md)! | [stats](SyncResult.md) Used to hold extras statistics about the sync operation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [syncAlreadyInProgress](SyncResult.md) Used to indicate that the SyncAdapter is already performing a sync operation, though not necessarily for the requested account and authority and that it wasn't able to process this request. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [tooManyDeletions](SyncResult.md) Used to indicate that the SyncAdapter determined that it would need to issue too many delete operations to the server in order to satisfy the request (as defined by the SyncAdapter). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [tooManyRetries](SyncResult.md) Used to indicate that the SyncAdapter experienced a hard error due to trying the same operation too many times (as defined by the SyncAdapter). |

## Public constructors

### SyncResult

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SyncResult()
```

Create a "clean" SyncResult. If this is returned without any changes then the SyncManager will consider the sync to have completed successfully. The various fields can be set by the SyncAdapter in order to give the SyncManager more information as to the disposition of the sync.

The errors are classified into two broad categories: hard errors and soft errors. Soft errors are retried with exponential backoff. Hard errors are not retried (except when the hard error is for a [ContentResolver.SYNC_EXTRAS_UPLOAD](ContentResolver.md) request, in which the request is retryed without the [ContentResolver.SYNC_EXTRAS_UPLOAD](ContentResolver.md) extra set). The SyncManager checks the type of error by calling [SyncResult.hasHardError()](SyncResult.md))and [SyncResult.hasSoftError()](SyncResult.md)). If both are true then the SyncManager treats it as a hard error, not a soft error.

## Public methods

### clear

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clear(): Unit
```

Clears the SyncResult to a clean state. Throws an [UnsupportedOperationException](../java.lang/UnsupportedOperationException.md) if this is called when [syncAlreadyInProgress](SyncResult.md) is set. 

### describeContents

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### hasError

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasError(): Boolean
```

A convenience method for determining of the SyncResult indicates that an error occurred.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if either a soft or hard error occurred |

### hasHardError

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasHardError(): Boolean
```

Convenience method for determining if the SyncResult indicates that a hard error occurred. See [SyncResult()](SyncResult.md))for an explanation of what the SyncManager does when it sees a hard error.

A hard error is indicated when any of the following is true:

- [SyncStats.numParseExceptions](SyncStats.md)\> 0
- [SyncStats.numConflictDetectedExceptions](SyncStats.md)\> 0
- [SyncStats.numAuthExceptions](SyncStats.md)\> 0
- [tooManyDeletions](SyncResult.md)
- [tooManyRetries](SyncResult.md)
- [databaseError](SyncResult.md)

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if a hard error is indicated |

### hasSoftError

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasSoftError(): Boolean
```

Convenience method for determining if the SyncResult indicates that a soft error occurred. See [SyncResult()](SyncResult.md))for an explanation of what the SyncManager does when it sees a soft error.

A soft error is indicated when any of the following is true:

- [SyncStats.numIoExceptions](SyncStats.md)\> 0
- [syncAlreadyInProgress](SyncResult.md)

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if a soft error is indicated |

### madeSomeProgress

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun madeSomeProgress(): Boolean
```

Convenience method for determining if the Sync should be rescheduled after failing for some reason.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the SyncManager should reschedule this sync. |

### toDebugString

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toDebugString(): String!
```

Generates a debugging string indicating the status. The string consist of a sequence of code letter followed by the count. Code letters are f - fullSyncRequested, r - partialSyncUnavailable, X - hardError, e - numParseExceptions, c - numConflictDetectedExceptions, a - numAuthExceptions, D - tooManyDeletions, R - tooManyRetries, b - databaseError, x - softError, l - syncAlreadyInProgress, I - numIoExceptions

| Return ||
|-----------------------------------------------------------------------------------|-------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | debugging string. |

### toString

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

### ALREADY_IN_PROGRESS

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALREADY_IN_PROGRESS: SyncResult!
```

This instance of a SyncResult is returned by the SyncAdapter in response to a sync request when a sync is already underway. The SyncManager will reschedule the sync request to try again later. 

### CREATOR

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SyncResult!>
```  

### databaseError

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var databaseError: Boolean
```

Used to indicate that the SyncAdapter experienced a hard error due to an error it received from interacting with the storage layer. The SyncManager will record that the sync request failed and it will not reschedule the request. 

### delayUntil

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var delayUntil: Long
```

Used to indicate to the SyncManager that future sync requests that match the request's Account and authority should be delayed until a time in seconds since Java epoch.

For example, if you want to delay the next sync for at least 5 minutes, then: 

```kotlin
result.delayUntil = (System.currentTimeMillis() / 1000) + 5 * 60;
  
```

By default, when a sync fails, the system retries later with an exponential back-off with the system default initial delay time, which always wins over [delayUntil](SyncResult.md)-- i.e. if the system back-off time is larger than [delayUntil](SyncResult.md), [delayUntil](SyncResult.md) will essentially be ignored. 

### fullSyncRequested

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var fullSyncRequested: Boolean
```

If set the SyncManager will request an immediate sync with the same Account and authority (but empty extras Bundle) as was used in the sync request. 

### moreRecordsToGet

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var moreRecordsToGet: Boolean
```

This field is ignored by the SyncManager. 

### partialSyncUnavailable

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var partialSyncUnavailable: Boolean
```

This field is ignored by the SyncManager. 

### stats

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val stats: SyncStats!
```

Used to hold extras statistics about the sync operation. Some of these indicate that the sync request resulted in a hard or soft error, others are for purely informational purposes. 

### syncAlreadyInProgress

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val syncAlreadyInProgress: Boolean
```

Used to indicate that the SyncAdapter is already performing a sync operation, though not necessarily for the requested account and authority and that it wasn't able to process this request. The SyncManager will reschedule the request to run later. 

### tooManyDeletions

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var tooManyDeletions: Boolean
```

Used to indicate that the SyncAdapter determined that it would need to issue too many delete operations to the server in order to satisfy the request (as defined by the SyncAdapter). The SyncManager will record that the sync request failed and will cause a System Notification to be created asking the user what they want to do about this. It will give the user a chance to choose between (1) go ahead even with those deletes, (2) revert the deletes, or (3) take no action. If the user decides (1) or (2) the SyncManager will issue another sync request with either [ContentResolver.SYNC_EXTRAS_OVERRIDE_TOO_MANY_DELETIONS](ContentResolver.md) or [ContentResolver.SYNC_EXTRAS_DISCARD_LOCAL_DELETIONS](ContentResolver.md) set in the extras. It is then up to the SyncAdapter to decide how to honor that request. 

### tooManyRetries

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var tooManyRetries: Boolean
```

Used to indicate that the SyncAdapter experienced a hard error due to trying the same operation too many times (as defined by the SyncAdapter). The SyncManager will record that the sync request failed and it will not reschedule the request.
