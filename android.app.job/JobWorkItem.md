# JobWorkItem

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JobWorkItem

Kotlin| [Java](https://developer.android.com/reference/android/app/job/JobWorkItem "View this page in Java") 
| --- | --- |

```
class JobWorkItem : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.job.JobWorkItem](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem#) |

A unit of work that can be enqueued for a job using [JobScheduler.enqueue](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#enqueue(android.app.job.JobInfo,%20android.app.job.JobWorkItem)). See [JobParameters.dequeueWork](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#dequeueWork())for more details.

**Note:** Prior to Android version [android.os.Build.VERSION_CODES#UPSIDE_DOWN_CAKE](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int), JobWorkItems could not be persisted. Apps were not allowed to enqueue JobWorkItems with persisted jobs and the system would throw an [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) if they attempted to do so. Starting with [android.os.Build.VERSION_CODES#UPSIDE_DOWN_CAKE](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int), JobWorkItems can be persisted alongside the hosting job. However, Intents cannot be persisted. Set a [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#) using [Builder.setExtras(PersistableBundle)](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem.Builder#setExtras(android.os.PersistableBundle))for any information that needs to be persisted.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem.Builder) Builder class for constructing [JobWorkItem](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem#) objects. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [JobWorkItem](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem#JobWorkItem(android.content.Intent))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` Create a new piece of work, which can be submitted to [JobScheduler.enqueue](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#enqueue(android.app.job.JobInfo,%20android.app.job.JobWorkItem)). |
| [JobWorkItem](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem#JobWorkItem(android.content.Intent,%20kotlin.Long,%20kotlin.Long))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`, `downloadBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `uploadBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Create a new piece of work, which can be submitted to [JobScheduler.enqueue](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#enqueue(android.app.job.JobInfo,%20android.app.job.JobWorkItem)). |
| [JobWorkItem](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem#JobWorkItem(android.content.Intent,%20kotlin.Long,%20kotlin.Long,%20kotlin.Long))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)?`, `downloadBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `uploadBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `minimumChunkBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Create a new piece of work, which can be submitted to [JobScheduler.enqueue](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#enqueue(android.app.job.JobInfo,%20android.app.job.JobWorkItem)). |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem#describeContents())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDeliveryCount](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem#getDeliveryCount())`()` Return the count of the number of times this work item has been delivered to the job. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getEstimatedNetworkDownloadBytes](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem#getEstimatedNetworkDownloadBytes())`()` Return the estimated size of download traffic that will be performed by this job, in bytes. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getEstimatedNetworkUploadBytes](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem#getEstimatedNetworkUploadBytes())`()` Return the estimated size of upload traffic that will be performed by this job work item, in bytes. |
| [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#) | [getExtras](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem#getExtras())`()` Return the extras associated with this work. |
| [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)! | [getIntent](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem#getIntent())`()` Return the Intent associated with this work. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMinimumNetworkChunkBytes](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem#getMinimumNetworkChunkBytes())`()` Return the smallest piece of data that cannot be easily paused and resumed, in bytes. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [JobWorkItem](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### JobWorkItem

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JobWorkItem(intent: Intent!)
```

Create a new piece of work, which can be submitted to [JobScheduler.enqueue](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#enqueue(android.app.job.JobInfo,%20android.app.job.JobWorkItem)).

Intents cannot be used for persisted JobWorkItems. Use [Builder.setExtras(PersistableBundle)](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem.Builder#setExtras(android.os.PersistableBundle))instead for persisted JobWorkItems.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:The general Intent describing this work. |

### JobWorkItem

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JobWorkItem(
    intent: Intent!, 
    downloadBytes: Long, 
    uploadBytes: Long)
```

Create a new piece of work, which can be submitted to [JobScheduler.enqueue](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#enqueue(android.app.job.JobInfo,%20android.app.job.JobWorkItem)).

See [JobInfo.Builder.setEstimatedNetworkBytes(long, long)](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setEstimatedNetworkBytes(kotlin.Long,%20kotlin.Long))for details about how to estimate network traffic.

Intents cannot be used for persisted JobWorkItems. Use [Builder.setExtras(PersistableBundle)](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem.Builder#setExtras(android.os.PersistableBundle))instead for persisted JobWorkItems.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:The general Intent describing this work. |
| `downloadBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The estimated size of network traffic that will be downloaded by this job work item, in bytes. Value is a non-negative number of bytes. |
| `uploadBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The estimated size of network traffic that will be uploaded by this job work item, in bytes. Value is a non-negative number of bytes. |
| --- | --- |

### JobWorkItem

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JobWorkItem(
    intent: Intent?, 
    downloadBytes: Long, 
    uploadBytes: Long, 
    minimumChunkBytes: Long)
```

Create a new piece of work, which can be submitted to [JobScheduler.enqueue](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#enqueue(android.app.job.JobInfo,%20android.app.job.JobWorkItem)).

See [JobInfo.Builder.setEstimatedNetworkBytes(long, long)](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setEstimatedNetworkBytes(kotlin.Long,%20kotlin.Long))for details about how to estimate network traffic.

Intents cannot be used for persisted JobWorkItems. Use [Builder.setExtras(PersistableBundle)](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem.Builder#setExtras(android.os.PersistableBundle))instead for persisted JobWorkItems.

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)?:The general Intent describing this work. This value may be`null`. |
| `downloadBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The estimated size of network traffic that will be downloaded by this job work item, in bytes. Value is a non-negative number of bytes. |
| `uploadBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The estimated size of network traffic that will be uploaded by this job work item, in bytes. Value is a non-negative number of bytes. |
| --- | --- |
| `minimumChunkBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The smallest piece of data that cannot be easily paused and resumed, in bytes. Value is a non-negative number of bytes. |

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getDeliveryCount

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeliveryCount(): Int
```

Return the count of the number of times this work item has been delivered to the job. The value will be \> 1 if it has been redelivered because the job was stopped or crashed while it had previously been delivered but before the job had called [JobParameters.completeWork](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#completeWork(android.app.job.JobWorkItem))for it. 

### getEstimatedNetworkDownloadBytes

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEstimatedNetworkDownloadBytes(): Long
```

Return the estimated size of download traffic that will be performed by this job, in bytes. 
Value is a non-negative number of bytes.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Estimated size of download traffic, or [JobInfo.NETWORK_BYTES_UNKNOWN](https://developer.android.com/reference/kotlin/android/app/job/JobInfo#NETWORK_BYTES_UNKNOWN:kotlin.Int) when unknown. Value is a non-negative number of bytes. |

### getEstimatedNetworkUploadBytes

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEstimatedNetworkUploadBytes(): Long
```

Return the estimated size of upload traffic that will be performed by this job work item, in bytes. 
Value is a non-negative number of bytes.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Estimated size of upload traffic, or [JobInfo.NETWORK_BYTES_UNKNOWN](https://developer.android.com/reference/kotlin/android/app/job/JobInfo#NETWORK_BYTES_UNKNOWN:kotlin.Int) when unknown. Value is a non-negative number of bytes. |

### getExtras

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtras(): PersistableBundle
```

Return the extras associated with this work.

| Return ||
|--------------------------------------------------------------------------------------------------------|-----------------------------|
| [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#) | This value cannot be`null`. |

**See Also**

- [android.app.job.JobWorkItem.Builder#setExtras(PersistableBundle)](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem.Builder#setExtras(android.os.PersistableBundle)) 

### getIntent

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIntent(): Intent!
```

Return the Intent associated with this work. 

### getMinimumNetworkChunkBytes

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMinimumNetworkChunkBytes(): Long
```

Return the smallest piece of data that cannot be easily paused and resumed, in bytes. 
Value is a non-negative number of bytes.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Smallest piece of data that cannot be easily paused and resumed, or [JobInfo.NETWORK_BYTES_UNKNOWN](https://developer.android.com/reference/kotlin/android/app/job/JobInfo#NETWORK_BYTES_UNKNOWN:kotlin.Int) when unknown. Value is a non-negative number of bytes. |

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
    out: Parcel, 
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
static val CREATOR: Parcelable.Creator<JobWorkItem!>
```
