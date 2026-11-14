# SyncStats

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SyncStats

Kotlin| [Java](https://developer.android.com/reference/android/content/SyncStats "View this page in Java") 
| --- | --- |

```
open class SyncStats : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.SyncStats](https://developer.android.com/reference/kotlin/android/content/SyncStats#) |

Used to record various statistics about the result of a sync operation. The SyncManager gets access to these via a [SyncResult](https://developer.android.com/reference/kotlin/android/content/SyncResult) and uses some of them to determine the disposition of the sync. See [SyncResult](https://developer.android.com/reference/kotlin/android/content/SyncResult) for further dicussion on how the SyncManager uses these values.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SyncStats](https://developer.android.com/reference/kotlin/android/content/SyncStats#SyncStats())`()` <br /> |
| [SyncStats](https://developer.android.com/reference/kotlin/android/content/SyncStats#SyncStats(android.os.Parcel))`(`in:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!`)` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/android/content/SyncStats#clear())`()` Reset all the counters to 0. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/content/SyncStats#describeContents())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/content/SyncStats#toString())`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/content/SyncStats#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [SyncStats](https://developer.android.com/reference/kotlin/android/content/SyncStats#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/content/SyncStats#CREATOR:android.os.Parcelable.Creator) <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [numAuthExceptions](https://developer.android.com/reference/kotlin/android/content/SyncStats#numAuthExceptions:kotlin.Long) The SyncAdapter was unable to authenticate the [android.accounts.Account](https://developer.android.com/reference/kotlin/android/accounts/Account.html#) that was specified in the request. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [numConflictDetectedExceptions](https://developer.android.com/reference/kotlin/android/content/SyncStats#numConflictDetectedExceptions:kotlin.Long) The SyncAdapter detected that there was an unrecoverable version conflict when it attempted to update or delete a version of a resource on the server. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [numDeletes](https://developer.android.com/reference/kotlin/android/content/SyncStats#numDeletes:kotlin.Long) Counter for tracking how many deletes were performed by the sync operation, as defined by the SyncAdapter. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [numEntries](https://developer.android.com/reference/kotlin/android/content/SyncStats#numEntries:kotlin.Long) Counter for tracking how many entries were affected by the sync operation, as defined by the SyncAdapter. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [numInserts](https://developer.android.com/reference/kotlin/android/content/SyncStats#numInserts:kotlin.Long) Counter for tracking how many inserts were performed by the sync operation, as defined by the SyncAdapter. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [numIoExceptions](https://developer.android.com/reference/kotlin/android/content/SyncStats#numIoExceptions:kotlin.Long) The SyncAdapter had a problem, most likely with the network connectivity or a timeout while waiting for a network response. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [numParseExceptions](https://developer.android.com/reference/kotlin/android/content/SyncStats#numParseExceptions:kotlin.Long) The SyncAdapter had a problem with the data it received from the server or the storage later. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [numSkippedEntries](https://developer.android.com/reference/kotlin/android/content/SyncStats#numSkippedEntries:kotlin.Long) Counter for tracking how many entries, either from the server or the local store, were ignored during the sync operation. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [numUpdates](https://developer.android.com/reference/kotlin/android/content/SyncStats#numUpdates:kotlin.Long) Counter for tracking how many updates were performed by the sync operation, as defined by the SyncAdapter. |

## Public constructors

### SyncStats

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SyncStats()
```  

### SyncStats

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SyncStats(in: Parcel!)
```

## Public methods

### clear

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Reset all the counters to 0. 

### describeContents

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### toString

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SyncStats!>
```  

### numAuthExceptions

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var numAuthExceptions: Long
```

The SyncAdapter was unable to authenticate the [android.accounts.Account](https://developer.android.com/reference/kotlin/android/accounts/Account.html#) that was specified in the request. The user needs to take some action to resolve before a future request can expect to succeed. This is considered a hard error. 

### numConflictDetectedExceptions

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var numConflictDetectedExceptions: Long
```

The SyncAdapter detected that there was an unrecoverable version conflict when it attempted to update or delete a version of a resource on the server. This is expected to clear itself automatically once the new state is retrieved from the server, though it may remain until the user intervenes manually, perhaps by clearing the local storage and starting over from scratch. This is considered a hard error. 

### numDeletes

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var numDeletes: Long
```

Counter for tracking how many deletes were performed by the sync operation, as defined by the SyncAdapter. 

### numEntries

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var numEntries: Long
```

Counter for tracking how many entries were affected by the sync operation, as defined by the SyncAdapter. 

### numInserts

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var numInserts: Long
```

Counter for tracking how many inserts were performed by the sync operation, as defined by the SyncAdapter. 

### numIoExceptions

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var numIoExceptions: Long
```

The SyncAdapter had a problem, most likely with the network connectivity or a timeout while waiting for a network response. The request may succeed if it is tried again later. This is considered a soft error. 

### numParseExceptions

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var numParseExceptions: Long
```

The SyncAdapter had a problem with the data it received from the server or the storage later. This problem will likely repeat if the request is tried again. The problem will need to be cleared up by either the server or the storage layer (likely with help from the user). If the SyncAdapter cleans up the data itself then it typically won't increment this value although it may still do so in order to record that it had to perform some cleanup. E.g., if the SyncAdapter received a bad entry from the server when processing a feed of entries, it may choose to drop the entry and thus make progress and still increment this value just so the SyncAdapter can record that an error occurred. This is considered a hard error. 

### numSkippedEntries

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var numSkippedEntries: Long
```

Counter for tracking how many entries, either from the server or the local store, were ignored during the sync operation. This could happen if the SyncAdapter detected some unparsable data but decided to skip it and move on rather than failing immediately. 

### numUpdates

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var numUpdates: Long
```

Counter for tracking how many updates were performed by the sync operation, as defined by the SyncAdapter.
