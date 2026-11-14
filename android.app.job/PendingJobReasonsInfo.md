# PendingJobReasonsInfo

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PendingJobReasonsInfo

Kotlin| [Java](PendingJobReasonsInfo.md) 
| --- | --- |

```
class PendingJobReasonsInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.job.PendingJobReasonsInfo](PendingJobReasonsInfo.md) |

A simple wrapper which includes a timestamp (in millis since epoch) and an array of android.app.job.JobScheduler.PendingJobReason at that timestamp for why a particular job may be pending.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PendingJobReasonsInfo](PendingJobReasonsInfo.md))`(`timestampMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `reasons:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](PendingJobReasonsInfo.md))`()` <br /> |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getPendingJobReasons](PendingJobReasonsInfo.md))`()` Returns a set of android. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimestampMillis](PendingJobReasonsInfo.md))`()` <br /> Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](PendingJobReasonsInfo.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PendingJobReasonsInfo](PendingJobReasonsInfo.md)!\> | [CREATOR](PendingJobReasonsInfo.md) <br /> |

## Public constructors

### PendingJobReasonsInfo

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PendingJobReasonsInfo(
    timestampMillis: Long, 
    reasons: IntArray)
```

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reasons` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html):This value cannot be`null`. Value is [android.app.job.JobScheduler#PENDING_JOB_REASON_UNDEFINED](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_APP](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_APP_STANDBY](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_BACKGROUND_RESTRICTION](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_BATTERY_NOT_LOW](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CHARGING](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CONNECTIVITY](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CONTENT_TRIGGER](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_DEVICE_IDLE](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_MINIMUM_LATENCY](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_PREFETCH](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_STORAGE_NOT_LOW](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_DEVICE_STATE](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_EXECUTING](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_INVALID_JOB_ID](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_JOB_SCHEDULER_OPTIMIZATION](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_QUOTA](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_USER](JobScheduler.md), or [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_DEADLINE](JobScheduler.md) |

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getPendingJobReasons

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPendingJobReasons(): IntArray
```

Returns a set of android.app.job.JobScheduler.PendingJobReason representing why the job may not have executed at the associated timestamp.

These reasons could either be explicitly set constraints on the job or implicit constraints imposed by the system due to various reasons.

Note: if the only android.app.job.JobScheduler.PendingJobReason present is android.app.job.JobScheduler.PendingJobReason#PENDING_JOB_REASON_UNDEFINED, it could mean that the job was ready to be executed at that time.

| Return ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | This value cannot be`null`. Value is [android.app.job.JobScheduler#PENDING_JOB_REASON_UNDEFINED](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_APP](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_APP_STANDBY](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_BACKGROUND_RESTRICTION](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_BATTERY_NOT_LOW](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CHARGING](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CONNECTIVITY](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CONTENT_TRIGGER](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_DEVICE_IDLE](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_MINIMUM_LATENCY](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_PREFETCH](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_STORAGE_NOT_LOW](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_DEVICE_STATE](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_EXECUTING](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_INVALID_JOB_ID](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_JOB_SCHEDULER_OPTIMIZATION](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_QUOTA](JobScheduler.md), [android.app.job.JobScheduler#PENDING_JOB_REASON_USER](JobScheduler.md), or [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_DEADLINE](JobScheduler.md) |

### getTimestampMillis

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimestampMillis(): Long
```

<br />

Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the time (in millis since epoch) associated with the set of pending job reasons. Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z. |

### writeToParcel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<PendingJobReasonsInfo!>
```
