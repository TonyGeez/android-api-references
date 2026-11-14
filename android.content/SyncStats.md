# SyncStats

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SyncStats

Kotlin| [Java](SyncStats.md) 
| --- | --- |

```
open class SyncStats : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.SyncStats](SyncStats.md) |

Used to record various statistics about the result of a sync operation. The SyncManager gets access to these via a [SyncResult](SyncResult.md) and uses some of them to determine the disposition of the sync. See [SyncResult](SyncResult.md) for further dicussion on how the SyncManager uses these values.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SyncStats](SyncStats.md))`()` <br /> |
| [SyncStats](SyncStats.md))`(`in:` ` [Parcel](../android.os/Parcel.md)!`)` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](SyncStats.md))`()` Reset all the counters to 0. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](SyncStats.md))`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](SyncStats.md))`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](SyncStats.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SyncStats](SyncStats.md)!\> | [CREATOR](SyncStats.md) <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [numAuthExceptions](SyncStats.md) The SyncAdapter was unable to authenticate the [android.accounts.Account](../android.accounts/Account.md) that was specified in the request. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [numConflictDetectedExceptions](SyncStats.md) The SyncAdapter detected that there was an unrecoverable version conflict when it attempted to update or delete a version of a resource on the server. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [numDeletes](SyncStats.md) Counter for tracking how many deletes were performed by the sync operation, as defined by the SyncAdapter. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [numEntries](SyncStats.md) Counter for tracking how many entries were affected by the sync operation, as defined by the SyncAdapter. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [numInserts](SyncStats.md) Counter for tracking how many inserts were performed by the sync operation, as defined by the SyncAdapter. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [numIoExceptions](SyncStats.md) The SyncAdapter had a problem, most likely with the network connectivity or a timeout while waiting for a network response. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [numParseExceptions](SyncStats.md) The SyncAdapter had a problem with the data it received from the server or the storage later. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [numSkippedEntries](SyncStats.md) Counter for tracking how many entries, either from the server or the local store, were ignored during the sync operation. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [numUpdates](SyncStats.md) Counter for tracking how many updates were performed by the sync operation, as defined by the SyncAdapter. |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

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
| `dest` | [Parcel](../android.os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

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

The SyncAdapter was unable to authenticate the [android.accounts.Account](../android.accounts/Account.md) that was specified in the request. The user needs to take some action to resolve before a future request can expect to succeed. This is considered a hard error. 

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
