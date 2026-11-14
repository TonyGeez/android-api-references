# JobWorkItem

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JobWorkItem

Kotlin| [Java](JobWorkItem.md) 
| --- | --- |

```
class JobWorkItem : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.job.JobWorkItem](JobWorkItem.md) |

A unit of work that can be enqueued for a job using [JobScheduler.enqueue](JobScheduler.md)). See [JobParameters.dequeueWork](JobParameters.md))for more details.

**Note:** Prior to Android version [android.os.Build.VERSION_CODES#UPSIDE_DOWN_CAKE](../android/os/Build.VERSION_CODES.md), JobWorkItems could not be persisted. Apps were not allowed to enqueue JobWorkItems with persisted jobs and the system would throw an [IllegalArgumentException](../java.lang/IllegalArgumentException.md) if they attempted to do so. Starting with [android.os.Build.VERSION_CODES#UPSIDE_DOWN_CAKE](../android/os/Build.VERSION_CODES.md), JobWorkItems can be persisted alongside the hosting job. However, Intents cannot be persisted. Set a [PersistableBundle](../android.os/PersistableBundle.md) using [Builder.setExtras(PersistableBundle)](../android/app/job/JobWorkItem.Builder.md))for any information that needs to be persisted.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/app/job/JobWorkItem.Builder.md) Builder class for constructing [JobWorkItem](JobWorkItem.md) objects. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [JobWorkItem](JobWorkItem.md))`(`intent:` ` [Intent](../android.content/Intent.md)!`)` Create a new piece of work, which can be submitted to [JobScheduler.enqueue](JobScheduler.md)). |
| [JobWorkItem](JobWorkItem.md))`(`intent:` ` [Intent](../android.content/Intent.md)!`, `downloadBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `uploadBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Create a new piece of work, which can be submitted to [JobScheduler.enqueue](JobScheduler.md)). |
| [JobWorkItem](JobWorkItem.md))`(`intent:` ` [Intent](../android.content/Intent.md)?`, `downloadBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `uploadBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `minimumChunkBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Create a new piece of work, which can be submitted to [JobScheduler.enqueue](JobScheduler.md)). |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](JobWorkItem.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDeliveryCount](JobWorkItem.md))`()` Return the count of the number of times this work item has been delivered to the job. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getEstimatedNetworkDownloadBytes](JobWorkItem.md))`()` Return the estimated size of download traffic that will be performed by this job, in bytes. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getEstimatedNetworkUploadBytes](JobWorkItem.md))`()` Return the estimated size of upload traffic that will be performed by this job work item, in bytes. |
| [PersistableBundle](../android.os/PersistableBundle.md) | [getExtras](JobWorkItem.md))`()` Return the extras associated with this work. |
| [Intent](../android.content/Intent.md)! | [getIntent](JobWorkItem.md))`()` Return the Intent associated with this work. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMinimumNetworkChunkBytes](JobWorkItem.md))`()` Return the smallest piece of data that cannot be easily paused and resumed, in bytes. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](JobWorkItem.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](JobWorkItem.md))`(`out:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [JobWorkItem](JobWorkItem.md)!\> | [CREATOR](JobWorkItem.md) <br /> |

## Public constructors

### JobWorkItem

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JobWorkItem(intent: Intent!)
```

Create a new piece of work, which can be submitted to [JobScheduler.enqueue](JobScheduler.md)).

Intents cannot be used for persisted JobWorkItems. Use [Builder.setExtras(PersistableBundle)](../android/app/job/JobWorkItem.Builder.md))instead for persisted JobWorkItems.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](../android.content/Intent.md)!:The general Intent describing this work. |

### JobWorkItem

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JobWorkItem(
    intent: Intent!, 
    downloadBytes: Long, 
    uploadBytes: Long)
```

Create a new piece of work, which can be submitted to [JobScheduler.enqueue](JobScheduler.md)).

See [JobInfo.Builder.setEstimatedNetworkBytes(long, long)](../android/app/job/JobInfo.Builder.md))for details about how to estimate network traffic.

Intents cannot be used for persisted JobWorkItems. Use [Builder.setExtras(PersistableBundle)](../android/app/job/JobWorkItem.Builder.md))instead for persisted JobWorkItems.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](../android.content/Intent.md)!:The general Intent describing this work. |
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

Create a new piece of work, which can be submitted to [JobScheduler.enqueue](JobScheduler.md)).

See [JobInfo.Builder.setEstimatedNetworkBytes(long, long)](../android/app/job/JobInfo.Builder.md))for details about how to estimate network traffic.

Intents cannot be used for persisted JobWorkItems. Use [Builder.setExtras(PersistableBundle)](../android/app/job/JobWorkItem.Builder.md))instead for persisted JobWorkItems.

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](../android.content/Intent.md)?:The general Intent describing this work. This value may be`null`. |
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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getDeliveryCount

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeliveryCount(): Int
```

Return the count of the number of times this work item has been delivered to the job. The value will be \> 1 if it has been redelivered because the job was stopped or crashed while it had previously been delivered but before the job had called [JobParameters.completeWork](JobParameters.md))for it. 

### getEstimatedNetworkDownloadBytes

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEstimatedNetworkDownloadBytes(): Long
```

Return the estimated size of download traffic that will be performed by this job, in bytes. 
Value is a non-negative number of bytes.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Estimated size of download traffic, or [JobInfo.NETWORK_BYTES_UNKNOWN](JobInfo.md) when unknown. Value is a non-negative number of bytes. |

### getEstimatedNetworkUploadBytes

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEstimatedNetworkUploadBytes(): Long
```

Return the estimated size of upload traffic that will be performed by this job work item, in bytes. 
Value is a non-negative number of bytes.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Estimated size of upload traffic, or [JobInfo.NETWORK_BYTES_UNKNOWN](JobInfo.md) when unknown. Value is a non-negative number of bytes. |

### getExtras

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtras(): PersistableBundle
```

Return the extras associated with this work.

| Return ||
|--------------------------------------------------------------------------------------------------------|-----------------------------|
| [PersistableBundle](../android.os/PersistableBundle.md) | This value cannot be`null`. |

**See Also**

- [android.app.job.JobWorkItem.Builder#setExtras(PersistableBundle)](../android/app/job/JobWorkItem.Builder.md)) 

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
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Smallest piece of data that cannot be easily paused and resumed, or [JobInfo.NETWORK_BYTES_UNKNOWN](JobInfo.md) when unknown. Value is a non-negative number of bytes. |

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<JobWorkItem!>
```
