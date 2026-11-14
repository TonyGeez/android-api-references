# PendingJobReasonsInfo

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PendingJobReasonsInfo

Kotlin| [Java](https://developer.android.com/reference/android/app/job/PendingJobReasonsInfo "View this page in Java") 

```
class PendingJobReasonsInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.job.PendingJobReasonsInfo](https://developer.android.com/reference/kotlin/android/app/job/PendingJobReasonsInfo#) |

A simple wrapper which includes a timestamp (in millis since epoch) and an array of android.app.job.JobScheduler.PendingJobReason at that timestamp for why a particular job may be pending.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PendingJobReasonsInfo](https://developer.android.com/reference/kotlin/android/app/job/PendingJobReasonsInfo#PendingJobReasonsInfo(kotlin.Long,%20kotlin.IntArray))`(`timestampMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `reasons:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/job/PendingJobReasonsInfo#describeContents())`()` <br /> |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getPendingJobReasons](https://developer.android.com/reference/kotlin/android/app/job/PendingJobReasonsInfo#getPendingJobReasons())`()` Returns a set of android. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimestampMillis](https://developer.android.com/reference/kotlin/android/app/job/PendingJobReasonsInfo#getTimestampMillis())`()` <br /> Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/job/PendingJobReasonsInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [PendingJobReasonsInfo](https://developer.android.com/reference/kotlin/android/app/job/PendingJobReasonsInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/job/PendingJobReasonsInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

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
| `reasons` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html):This value cannot be`null`. Value is [android.app.job.JobScheduler#PENDING_JOB_REASON_UNDEFINED](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_UNDEFINED:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_APP](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_APP:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_APP_STANDBY](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_APP_STANDBY:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_BACKGROUND_RESTRICTION](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_BACKGROUND_RESTRICTION:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_BATTERY_NOT_LOW](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_BATTERY_NOT_LOW:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CHARGING](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CHARGING:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CONNECTIVITY](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CONNECTIVITY:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CONTENT_TRIGGER](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CONTENT_TRIGGER:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_DEVICE_IDLE](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_DEVICE_IDLE:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_MINIMUM_LATENCY](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_MINIMUM_LATENCY:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_PREFETCH](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_PREFETCH:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_STORAGE_NOT_LOW](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_STORAGE_NOT_LOW:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_DEVICE_STATE](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_DEVICE_STATE:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_EXECUTING](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_EXECUTING:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_INVALID_JOB_ID](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_INVALID_JOB_ID:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_JOB_SCHEDULER_OPTIMIZATION](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_JOB_SCHEDULER_OPTIMIZATION:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_QUOTA](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_QUOTA:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_USER](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_USER:kotlin.Int), or [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_DEADLINE](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_DEADLINE:kotlin.Int) |

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | This value cannot be`null`. Value is [android.app.job.JobScheduler#PENDING_JOB_REASON_UNDEFINED](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_UNDEFINED:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_APP](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_APP:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_APP_STANDBY](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_APP_STANDBY:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_BACKGROUND_RESTRICTION](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_BACKGROUND_RESTRICTION:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_BATTERY_NOT_LOW](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_BATTERY_NOT_LOW:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CHARGING](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CHARGING:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CONNECTIVITY](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CONNECTIVITY:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CONTENT_TRIGGER](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CONTENT_TRIGGER:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_DEVICE_IDLE](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_DEVICE_IDLE:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_MINIMUM_LATENCY](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_MINIMUM_LATENCY:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_PREFETCH](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_PREFETCH:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_STORAGE_NOT_LOW](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_STORAGE_NOT_LOW:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_DEVICE_STATE](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_DEVICE_STATE:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_EXECUTING](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_EXECUTING:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_INVALID_JOB_ID](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_INVALID_JOB_ID:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_JOB_SCHEDULER_OPTIMIZATION](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_JOB_SCHEDULER_OPTIMIZATION:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_QUOTA](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_QUOTA:kotlin.Int), [android.app.job.JobScheduler#PENDING_JOB_REASON_USER](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_USER:kotlin.Int), or [android.app.job.JobScheduler#PENDING_JOB_REASON_CONSTRAINT_DEADLINE](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_DEADLINE:kotlin.Int) |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<PendingJobReasonsInfo!>
```
