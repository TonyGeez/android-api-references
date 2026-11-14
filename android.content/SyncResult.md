# SyncResult

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SyncResult

Kotlin| [Java](https://developer.android.com/reference/android/content/SyncResult "View this page in Java") 

```
class SyncResult : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.content.SyncResult](https://developer.android.com/reference/kotlin/android/content/SyncResult#) |

This class is used to communicate the results of a sync operation to the SyncManager. Based on the values here the SyncManager will determine the disposition of the sync and whether or not a new sync operation needs to be scheduled in the future.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------|---|
| [SyncResult](https://developer.android.com/reference/kotlin/android/content/SyncResult#SyncResult())`()` Create a "clean" SyncResult. |

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/android/content/SyncResult#clear())`()` Clears the SyncResult to a clean state. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/content/SyncResult#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasError](https://developer.android.com/reference/kotlin/android/content/SyncResult#hasError())`()` A convenience method for determining of the SyncResult indicates that an error occurred. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasHardError](https://developer.android.com/reference/kotlin/android/content/SyncResult#hasHardError())`()` Convenience method for determining if the SyncResult indicates that a hard error occurred. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasSoftError](https://developer.android.com/reference/kotlin/android/content/SyncResult#hasSoftError())`()` Convenience method for determining if the SyncResult indicates that a soft error occurred. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [madeSomeProgress](https://developer.android.com/reference/kotlin/android/content/SyncResult#madeSomeProgress())`()` Convenience method for determining if the Sync should be rescheduled after failing for some reason. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toDebugString](https://developer.android.com/reference/kotlin/android/content/SyncResult#toDebugString())`()` Generates a debugging string indicating the status. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/content/SyncResult#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/content/SyncResult#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [SyncResult](https://developer.android.com/reference/kotlin/android/content/SyncResult#)! | [ALREADY_IN_PROGRESS](https://developer.android.com/reference/kotlin/android/content/SyncResult#ALREADY_IN_PROGRESS:android.content.SyncResult) This instance of a SyncResult is returned by the SyncAdapter in response to a sync request when a sync is already underway. |
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [SyncResult](https://developer.android.com/reference/kotlin/android/content/SyncResult#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/content/SyncResult#CREATOR:android.os.Parcelable.Creator) <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [databaseError](https://developer.android.com/reference/kotlin/android/content/SyncResult#databaseError:kotlin.Boolean) Used to indicate that the SyncAdapter experienced a hard error due to an error it received from interacting with the storage layer. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [delayUntil](https://developer.android.com/reference/kotlin/android/content/SyncResult#delayUntil:kotlin.Long) Used to indicate to the SyncManager that future sync requests that match the request's Account and authority should be delayed until a time in seconds since Java epoch. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [fullSyncRequested](https://developer.android.com/reference/kotlin/android/content/SyncResult#fullSyncRequested:kotlin.Boolean) If set the SyncManager will request an immediate sync with the same Account and authority (but empty extras Bundle) as was used in the sync request. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moreRecordsToGet](https://developer.android.com/reference/kotlin/android/content/SyncResult#moreRecordsToGet:kotlin.Boolean) This field is ignored by the SyncManager. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [partialSyncUnavailable](https://developer.android.com/reference/kotlin/android/content/SyncResult#partialSyncUnavailable:kotlin.Boolean) This field is ignored by the SyncManager. |
| [SyncStats](https://developer.android.com/reference/kotlin/android/content/SyncStats)! | [stats](https://developer.android.com/reference/kotlin/android/content/SyncResult#stats:android.content.SyncStats) Used to hold extras statistics about the sync operation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [syncAlreadyInProgress](https://developer.android.com/reference/kotlin/android/content/SyncResult#syncAlreadyInProgress:kotlin.Boolean) Used to indicate that the SyncAdapter is already performing a sync operation, though not necessarily for the requested account and authority and that it wasn't able to process this request. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [tooManyDeletions](https://developer.android.com/reference/kotlin/android/content/SyncResult#tooManyDeletions:kotlin.Boolean) Used to indicate that the SyncAdapter determined that it would need to issue too many delete operations to the server in order to satisfy the request (as defined by the SyncAdapter). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [tooManyRetries](https://developer.android.com/reference/kotlin/android/content/SyncResult#tooManyRetries:kotlin.Boolean) Used to indicate that the SyncAdapter experienced a hard error due to trying the same operation too many times (as defined by the SyncAdapter). |

## Public constructors

### SyncResult

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SyncResult()
```

Create a "clean" SyncResult. If this is returned without any changes then the SyncManager will consider the sync to have completed successfully. The various fields can be set by the SyncAdapter in order to give the SyncManager more information as to the disposition of the sync.

The errors are classified into two broad categories: hard errors and soft errors. Soft errors are retried with exponential backoff. Hard errors are not retried (except when the hard error is for a [ContentResolver.SYNC_EXTRAS_UPLOAD](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_UPLOAD:kotlin.String) request, in which the request is retryed without the [ContentResolver.SYNC_EXTRAS_UPLOAD](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_UPLOAD:kotlin.String) extra set). The SyncManager checks the type of error by calling [SyncResult.hasHardError()](https://developer.android.com/reference/kotlin/android/content/SyncResult#hasHardError())and [SyncResult.hasSoftError()](https://developer.android.com/reference/kotlin/android/content/SyncResult#hasSoftError()). If both are true then the SyncManager treats it as a hard error, not a soft error.

## Public methods

### clear

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clear(): Unit
```

Clears the SyncResult to a clean state. Throws an [UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#) if this is called when [syncAlreadyInProgress](https://developer.android.com/reference/kotlin/android/content/SyncResult#syncAlreadyInProgress:kotlin.Boolean) is set. 

### describeContents

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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

Convenience method for determining if the SyncResult indicates that a hard error occurred. See [SyncResult()](https://developer.android.com/reference/kotlin/android/content/SyncResult#SyncResult())for an explanation of what the SyncManager does when it sees a hard error.

A hard error is indicated when any of the following is true:

- [SyncStats.numParseExceptions](https://developer.android.com/reference/kotlin/android/content/SyncStats#numParseExceptions:kotlin.Long)\> 0
- [SyncStats.numConflictDetectedExceptions](https://developer.android.com/reference/kotlin/android/content/SyncStats#numConflictDetectedExceptions:kotlin.Long)\> 0
- [SyncStats.numAuthExceptions](https://developer.android.com/reference/kotlin/android/content/SyncStats#numAuthExceptions:kotlin.Long)\> 0
- [tooManyDeletions](https://developer.android.com/reference/kotlin/android/content/SyncResult#tooManyDeletions:kotlin.Boolean)
- [tooManyRetries](https://developer.android.com/reference/kotlin/android/content/SyncResult#tooManyRetries:kotlin.Boolean)
- [databaseError](https://developer.android.com/reference/kotlin/android/content/SyncResult#databaseError:kotlin.Boolean)

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if a hard error is indicated |

### hasSoftError

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasSoftError(): Boolean
```

Convenience method for determining if the SyncResult indicates that a soft error occurred. See [SyncResult()](https://developer.android.com/reference/kotlin/android/content/SyncResult#SyncResult())for an explanation of what the SyncManager does when it sees a soft error.

A soft error is indicated when any of the following is true:

- [SyncStats.numIoExceptions](https://developer.android.com/reference/kotlin/android/content/SyncStats#numIoExceptions:kotlin.Long)\> 0
- [syncAlreadyInProgress](https://developer.android.com/reference/kotlin/android/content/SyncResult#syncAlreadyInProgress:kotlin.Boolean)

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

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

By default, when a sync fails, the system retries later with an exponential back-off with the system default initial delay time, which always wins over [delayUntil](https://developer.android.com/reference/kotlin/android/content/SyncResult#delayUntil:kotlin.Long)-- i.e. if the system back-off time is larger than [delayUntil](https://developer.android.com/reference/kotlin/android/content/SyncResult#delayUntil:kotlin.Long), [delayUntil](https://developer.android.com/reference/kotlin/android/content/SyncResult#delayUntil:kotlin.Long) will essentially be ignored. 

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

Used to indicate that the SyncAdapter determined that it would need to issue too many delete operations to the server in order to satisfy the request (as defined by the SyncAdapter). The SyncManager will record that the sync request failed and will cause a System Notification to be created asking the user what they want to do about this. It will give the user a chance to choose between (1) go ahead even with those deletes, (2) revert the deletes, or (3) take no action. If the user decides (1) or (2) the SyncManager will issue another sync request with either [ContentResolver.SYNC_EXTRAS_OVERRIDE_TOO_MANY_DELETIONS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_OVERRIDE_TOO_MANY_DELETIONS:kotlin.String) or [ContentResolver.SYNC_EXTRAS_DISCARD_LOCAL_DELETIONS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_DISCARD_LOCAL_DELETIONS:kotlin.String) set in the extras. It is then up to the SyncAdapter to decide how to honor that request. 

### tooManyRetries

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var tooManyRetries: Boolean
```

Used to indicate that the SyncAdapter experienced a hard error due to trying the same operation too many times (as defined by the SyncAdapter). The SyncManager will record that the sync request failed and it will not reschedule the request.
