# JobParameters

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JobParameters

Kotlin| [Java](../android/app/job/JobParameters.md) 
| --- | --- |

```
open class JobParameters : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.job.JobParameters](../android/app/job/JobParameters.md) |

Contains the parameters used to configure/identify your job. You do not create this object yourself, instead it is handed in to your application by the System.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_APP_STANDBY](../android/app/job/JobParameters.md) The current standby bucket requires that the job stop now. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_BACKGROUND_RESTRICTION](../android/app/job/JobParameters.md) The app is restricted from running in the background. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_CANCELLED_BY_APP](../android/app/job/JobParameters.md) The job was cancelled directly by the app, either by calling [JobScheduler.cancel(int)](../android/app/job/JobScheduler.md)), [JobScheduler.cancelAll()](../android/app/job/JobScheduler.md)), or by scheduling a new job with the same job ID. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_CONSTRAINT_BATTERY_NOT_LOW](../android/app/job/JobParameters.md) The requested battery-not-low constraint is no longer satisfied. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_CONSTRAINT_CHARGING](../android/app/job/JobParameters.md) The requested charging constraint is no longer satisfied. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_CONSTRAINT_CONNECTIVITY](../android/app/job/JobParameters.md) The requested connectivity constraint is no longer satisfied. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_CONSTRAINT_DEVICE_IDLE](../android/app/job/JobParameters.md) The requested idle constraint is no longer satisfied. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_CONSTRAINT_STORAGE_NOT_LOW](../android/app/job/JobParameters.md) The requested storage-not-low constraint is no longer satisfied. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_DEVICE_STATE](../android/app/job/JobParameters.md) The device state (eg. Doze, battery saver, memory usage, etc) requires JobScheduler stop this job. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_ESTIMATED_APP_LAUNCH_TIME_CHANGED](../android/app/job/JobParameters.md) The system's estimate of when the app will be launched changed significantly enough to decide this job shouldn't be running right now. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_PREEMPT](../android/app/job/JobParameters.md) The job was stopped to run a higher priority job of the app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_QUOTA](../android/app/job/JobParameters.md) The app has consumed all of its current quota. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_SYSTEM_PROCESSING](../android/app/job/JobParameters.md) The system is doing some processing that requires stopping this job. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_TIMEOUT](../android/app/job/JobParameters.md) The job used up its maximum execution time and timed out. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_TIMEOUT_ABANDONED](../android/app/job/JobParameters.md) The job used up its maximum execution time and timed out. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_UNDEFINED](../android/app/job/JobParameters.md) There is no reason the job is stopped. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_USER](../android/app/job/JobParameters.md) The user stopped the job. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [completeWork](../android/app/job/JobParameters.md))`(`work:` ` [JobWorkItem](../android/app/job/JobWorkItem.md)`)` Report the completion of executing a [JobWorkItem](../android/app/job/JobWorkItem.md) previously returned by [dequeueWork()](../android/app/job/JobParameters.md)). |
| open [JobWorkItem](../android/app/job/JobWorkItem.md)? | [dequeueWork](../android/app/job/JobParameters.md))`()` Dequeue the next pending [JobWorkItem](../android/app/job/JobWorkItem.md) from these JobParameters associated with their currently running job. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/app/job/JobParameters.md))`()` <br /> |
| --- | --- |
| open [ClipData](../android/content/ClipData.md)? | [getClipData](../android/app/job/JobParameters.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getClipGrantFlags](../android/app/job/JobParameters.md))`()` <br /> |
| open [PersistableBundle](../android/os/PersistableBundle.md) | [getExtras](../android/app/job/JobParameters.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getJobId](../android/app/job/JobParameters.md))`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getJobNamespace](../android/app/job/JobParameters.md))`()` Get the namespace this job was placed in. |
| open [Network](../android/net/Network.md)? | [getNetwork](../android/app/job/JobParameters.md))`()` Return the network that should be used to perform any network requests for this job. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStopReason](../android/app/job/JobParameters.md))`()` Returns the reason [JobService.onStopJob(JobParameters)](../android/app/job/JobService.md))was called on this job. |
| open [Bundle](../android/os/Bundle.md) | [getTransientExtras](../android/app/job/JobParameters.md))`()` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | [getTriggeredContentAuthorities](../android/app/job/JobParameters.md))`()` For jobs with [android.app.job.JobInfo.Builder#addTriggerContentUri](../android/app/job/JobInfo.Builder.md))set, this reports which content authorities have triggered the job. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Uri](../android/net/Uri.md)!\>? | [getTriggeredContentUris](../android/app/job/JobParameters.md))`()` For jobs with [android.app.job.JobInfo.Builder#addTriggerContentUri](../android/app/job/JobInfo.Builder.md))set, this reports which URIs have triggered the job. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExpeditedJob](../android/app/job/JobParameters.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOverrideDeadlineExpired](../android/app/job/JobParameters.md))`()` For jobs with [android.app.job.JobInfo.Builder#setOverrideDeadline(long)](../android/app/job/JobInfo.Builder.md))set, this provides an easy way to tell whether the job is being executed due to the deadline expiring. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUserInitiatedJob](../android/app/job/JobParameters.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/app/job/JobParameters.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [JobParameters](../android/app/job/JobParameters.md)!\> | [CREATOR](../android/app/job/JobParameters.md) <br /> |

## Constants

### STOP_REASON_APP_STANDBY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_APP_STANDBY: Int
```

The current standby bucket requires that the job stop now. 

 Value: 12

**See Also**

- [android.app.usage.UsageStatsManager#STANDBY_BUCKET_RESTRICTED](../android/app/usage/UsageStatsManager.md) 

### STOP_REASON_BACKGROUND_RESTRICTION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_BACKGROUND_RESTRICTION: Int
```

The app is restricted from running in the background. 

 Value: 11

**See Also**

- [android.app.ActivityManager#isBackgroundRestricted()](../android/app/ActivityManager.md))
- [android.content.pm.PackageManager#isInstantApp()](../android/content/pm/PackageManager.md)) 

### STOP_REASON_CANCELLED_BY_APP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_CANCELLED_BY_APP: Int
```

The job was cancelled directly by the app, either by calling [JobScheduler.cancel(int)](../android/app/job/JobScheduler.md)), [JobScheduler.cancelAll()](../android/app/job/JobScheduler.md)), or by scheduling a new job with the same job ID. 

 Value: 1

### STOP_REASON_CONSTRAINT_BATTERY_NOT_LOW

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_CONSTRAINT_BATTERY_NOT_LOW: Int
```

The requested battery-not-low constraint is no longer satisfied. 

 Value: 5

**See Also**

- [android.app.job.JobInfo.Builder#setRequiresBatteryNotLow(boolean)](../android/app/job/JobInfo.Builder.md)) 

### STOP_REASON_CONSTRAINT_CHARGING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_CONSTRAINT_CHARGING: Int
```

The requested charging constraint is no longer satisfied. 

 Value: 6

**See Also**

- [android.app.job.JobInfo.Builder#setRequiresCharging(boolean)](../android/app/job/JobInfo.Builder.md)) 

### STOP_REASON_CONSTRAINT_CONNECTIVITY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_CONSTRAINT_CONNECTIVITY: Int
```

The requested connectivity constraint is no longer satisfied. 

 Value: 7

**See Also**

- [android.app.job.JobInfo.Builder#setRequiredNetwork(NetworkRequest)](../android/app/job/JobInfo.Builder.md))
- [android.app.job.JobInfo.Builder#setRequiredNetworkType(int)](../android/app/job/JobInfo.Builder.md)) 

### STOP_REASON_CONSTRAINT_DEVICE_IDLE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_CONSTRAINT_DEVICE_IDLE: Int
```

The requested idle constraint is no longer satisfied. 

 Value: 8

**See Also**

- [android.app.job.JobInfo.Builder#setRequiresDeviceIdle(boolean)](../android/app/job/JobInfo.Builder.md)) 

### STOP_REASON_CONSTRAINT_STORAGE_NOT_LOW

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_CONSTRAINT_STORAGE_NOT_LOW: Int
```

The requested storage-not-low constraint is no longer satisfied. 

 Value: 9

**See Also**

- [android.app.job.JobInfo.Builder#setRequiresStorageNotLow(boolean)](../android/app/job/JobInfo.Builder.md)) 

### STOP_REASON_DEVICE_STATE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_DEVICE_STATE: Int
```

The device state (eg. Doze, battery saver, memory usage, etc) requires JobScheduler stop this job. 

 Value: 4

### STOP_REASON_ESTIMATED_APP_LAUNCH_TIME_CHANGED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_ESTIMATED_APP_LAUNCH_TIME_CHANGED: Int
```

The system's estimate of when the app will be launched changed significantly enough to decide this job shouldn't be running right now. This will mostly apply to prefetch jobs. 

 Value: 15

**See Also**

- [android.app.job.JobInfo#isPrefetch()](../android/app/job/JobInfo.md))
- [android.app.job.JobInfo.Builder#setPrefetch(boolean)](../android/app/job/JobInfo.Builder.md)) 

### STOP_REASON_PREEMPT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_PREEMPT: Int
```

The job was stopped to run a higher priority job of the app. 

 Value: 2

### STOP_REASON_QUOTA

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_QUOTA: Int
```

The app has consumed all of its current quota. Each app is assigned a quota of how much it can run jobs within a certain time frame. The quota is informed, in part, by app standby buckets. Once an app has used up all of its quota, it won't be able to start jobs until quota is replenished, is changed, or is temporarily not applied. 

 Value: 10

**See Also**

- [android.app.usage.UsageStatsManager#getAppStandbyBucket()](../android/app/usage/UsageStatsManager.md)) 

### STOP_REASON_SYSTEM_PROCESSING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_SYSTEM_PROCESSING: Int
```

The system is doing some processing that requires stopping this job. 

 Value: 14

### STOP_REASON_TIMEOUT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_TIMEOUT: Int
```

The job used up its maximum execution time and timed out. Each individual job has a maximum execution time limit, regardless of how much total quota the app has. See the note on [JobScheduler](../android/app/job/JobScheduler.md) and [JobInfo](../android/app/job/JobInfo.md) for the execution time limits. 

 Value: 3

### STOP_REASON_TIMEOUT_ABANDONED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_TIMEOUT_ABANDONED: Int
```

The job used up its maximum execution time and timed out. The system also detected that the app can no longer call [JobService.jobFinished(JobParameters, boolean)](../android/app/job/JobService.md))for this job, likely because the strong reference to the job handle ([JobParameters](../android/app/job/JobParameters.md)) passed to it via [JobService.onStartJob(JobParameters)](../android/app/job/JobService.md))was lost. This can occur even if the app called [JobScheduler.cancel(int)](../android/app/job/JobScheduler.md)), [JobScheduler.cancelAll()](../android/app/job/JobScheduler.md)), or [JobScheduler.cancelInAllNamespaces()](../android/app/job/JobScheduler.md))to stop an active job while losing strong references to the job handle. In this case, the job is not necessarily abandoned. However, the system cannot distinguish such cases from truly abandoned jobs.

It is recommended that you use [JobService.jobFinished(JobParameters, boolean)](../android/app/job/JobService.md))or return false from [JobService.onStartJob(JobParameters)](../android/app/job/JobService.md))to stop an active job. This will prevent the occurrence of this stop reason and the need to handle it. The primary use case for this stop reason is to report a probable case of a job being abandoned.

<br />

 Value: 16

### STOP_REASON_UNDEFINED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_UNDEFINED: Int
```

There is no reason the job is stopped. This is the value returned from the JobParameters object passed to [JobService.onStartJob(JobParameters)](../android/app/job/JobService.md)). 

 Value: 0

### STOP_REASON_USER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_USER: Int
```

The user stopped the job. This can happen either through force-stop, adb shell commands, uninstalling, or some other UI. 

 Value: 13

## Public methods

### completeWork

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun completeWork(work: JobWorkItem): Unit
```

Report the completion of executing a [JobWorkItem](../android/app/job/JobWorkItem.md) previously returned by [dequeueWork()](../android/app/job/JobParameters.md)). This tells the system you are done with the work associated with that item, so it will not be returned again. Note that if this is the last work in the queue, completing it here will*not* finish the overall job -- for that to happen, you still need to call [dequeueWork()](../android/app/job/JobParameters.md))again.

If you are enqueueing work into a job, you must call this method for each piece of work you process. Do*not* call [JobService.jobFinished(JobParameters, boolean)](../android/app/job/JobService.md))or else you can lose work in your queue.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `work` | [JobWorkItem](../android/app/job/JobWorkItem.md):The work you have completed processing, as previously returned by [dequeueWork()](../android/app/job/JobParameters.md))This value cannot be`null`. |

### dequeueWork

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dequeueWork(): JobWorkItem?
```

Dequeue the next pending [JobWorkItem](../android/app/job/JobWorkItem.md) from these JobParameters associated with their currently running job. Calling this method when there is no more work available and all previously dequeued work has been completed will result in the system taking care of stopping the job for you -- you should not call [JobService.jobFinished(JobParameters, boolean)](../android/app/job/JobService.md))yourself (otherwise you risk losing an upcoming JobWorkItem that is being enqueued at the same time).

Once you are done with the [JobWorkItem](../android/app/job/JobWorkItem.md) returned by this method, you must call [completeWork(android.app.job.JobWorkItem)](../android/app/job/JobParameters.md))with it to inform the system that you are done executing the work. The job will not be finished until all dequeued work has been completed. You do not, however, have to complete each returned work item before deqeueing the next one -- you can use [dequeueWork()](../android/app/job/JobParameters.md))multiple times before completing previous work if you want to process work in parallel, and you can complete the work in whatever order you want.

If the job runs to the end of its available time period before all work has been completed, it will stop as normal. You should return true from [JobService.onStopJob(JobParameters)](../android/app/job/JobService.md))in order to have the job rescheduled, and by doing so any pending as well as remaining uncompleted work will be re-queued for the next time the job runs.

This example shows how to construct a JobService that will serially dequeue and process work that is available for it:

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [JobWorkItem](../android/app/job/JobWorkItem.md)? | Returns a new [JobWorkItem](../android/app/job/JobWorkItem.md) if there is one pending, otherwise null. If null is returned, the system will also stop the job if all work has also been completed. (This means that for correct operation, you must always call dequeueWork() after you have completed other work, to check either for more work or allow the system to stop the job.) |

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getClipData

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getClipData(): ClipData?
```

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ClipData](../android/content/ClipData.md)? | The clip you passed in when constructing this job with [android.app.job.JobInfo.Builder#setClipData(ClipData, int)](../android/app/job/JobInfo.Builder.md)). Will be null if it was not set. |

### getClipGrantFlags

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getClipGrantFlags(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The clip grant flags you passed in when constructing this job with [android.app.job.JobInfo.Builder#setClipData(ClipData, int)](../android/app/job/JobInfo.Builder.md)). Will be 0 if it was not set. |

### getExtras

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExtras(): PersistableBundle
```

| Return ||
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PersistableBundle](../android/os/PersistableBundle.md) | The extras you passed in when constructing this job with [android.app.job.JobInfo.Builder#setExtras(android.os.PersistableBundle)](../android/app/job/JobInfo.Builder.md)). This will never be null. If you did not set any extras this will be an empty bundle. |

### getJobId

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getJobId(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The unique id of this job, specified at creation time. |

### getJobNamespace

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getJobNamespace(): String?
```

Get the namespace this job was placed in.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The namespace this job was scheduled in. Will be`null`if there was no explicit namespace set and this job is therefore in the default namespace. |

**See Also**

- [android.app.job.JobScheduler#forNamespace(String)](../android/app/job/JobScheduler.md)) 

### getNetwork

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNetwork(): Network?
```

Return the network that should be used to perform any network requests for this job.

Devices may have multiple active network connections simultaneously, or they may not have a default network route at all. To correctly handle all situations like this, your job should always use the network returned by this method instead of implicitly using the default network route.

Note that the system may relax the constraints you originally requested, such as allowing a [JobInfo.NETWORK_TYPE_UNMETERED](../android/app/job/JobInfo.md) job to run over a metered network when there is a surplus of metered data available. Starting in Android version [android.os.Build.VERSION_CODES#UPSIDE_DOWN_CAKE](../android/os/Build.VERSION_CODES.md), this will return`null`if the app does not hold the permissions specified in [JobInfo.Builder.setRequiredNetwork(NetworkRequest)](../android/app/job/JobInfo.Builder.md)).

| Return ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Network](../android/net/Network.md)? | the network that should be used to perform any network requests for this job, or`null`if this job didn't set any required network type or if the job executed when there was no available network to use. |

**See Also**

- [android.app.job.JobInfo.Builder#setRequiredNetworkType(int)](../android/app/job/JobInfo.Builder.md))
- [android.app.job.JobInfo.Builder#setRequiredNetwork(NetworkRequest)](../android/app/job/JobInfo.Builder.md)) 

### getStopReason

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStopReason(): Int
```

Returns the reason [JobService.onStopJob(JobParameters)](../android/app/job/JobService.md))was called on this job.

Apps should not rely on the stop reason for critical decision-making, as additional stop reasons may be added in subsequent Android releases. The primary intended use of this method is for logging and diagnostic purposes to gain insights into the causes of job termination.

<br />

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The reason [JobService.onStopJob(JobParameters)](../android/app/job/JobService.md))was called on this job. Will be [STOP_REASON_UNDEFINED](../android/app/job/JobParameters.md) if [JobService.onStopJob(JobParameters)](../android/app/job/JobService.md))has not yet been called. Value is [android.app.job.JobParameters#STOP_REASON_UNDEFINED](../android/app/job/JobParameters.md), [android.app.job.JobParameters#STOP_REASON_CANCELLED_BY_APP](../android/app/job/JobParameters.md), [android.app.job.JobParameters#STOP_REASON_PREEMPT](../android/app/job/JobParameters.md), [android.app.job.JobParameters#STOP_REASON_TIMEOUT](../android/app/job/JobParameters.md), [android.app.job.JobParameters#STOP_REASON_DEVICE_STATE](../android/app/job/JobParameters.md), [android.app.job.JobParameters#STOP_REASON_CONSTRAINT_BATTERY_NOT_LOW](../android/app/job/JobParameters.md), [android.app.job.JobParameters#STOP_REASON_CONSTRAINT_CHARGING](../android/app/job/JobParameters.md), [android.app.job.JobParameters#STOP_REASON_CONSTRAINT_CONNECTIVITY](../android/app/job/JobParameters.md), [android.app.job.JobParameters#STOP_REASON_CONSTRAINT_DEVICE_IDLE](../android/app/job/JobParameters.md), [android.app.job.JobParameters#STOP_REASON_CONSTRAINT_STORAGE_NOT_LOW](../android/app/job/JobParameters.md), [android.app.job.JobParameters#STOP_REASON_QUOTA](../android/app/job/JobParameters.md), [android.app.job.JobParameters#STOP_REASON_BACKGROUND_RESTRICTION](../android/app/job/JobParameters.md), [android.app.job.JobParameters#STOP_REASON_APP_STANDBY](../android/app/job/JobParameters.md), [android.app.job.JobParameters#STOP_REASON_USER](../android/app/job/JobParameters.md), [android.app.job.JobParameters#STOP_REASON_SYSTEM_PROCESSING](../android/app/job/JobParameters.md), [android.app.job.JobParameters#STOP_REASON_ESTIMATED_APP_LAUNCH_TIME_CHANGED](../android/app/job/JobParameters.md), or [android.app.job.JobParameters#STOP_REASON_TIMEOUT_ABANDONED](../android/app/job/JobParameters.md) |

### getTransientExtras

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTransientExtras(): Bundle
```

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bundle](../android/os/Bundle.md) | The transient extras you passed in when constructing this job with [android.app.job.JobInfo.Builder#setTransientExtras(android.os.Bundle)](../android/app/job/JobInfo.Builder.md)). This will never be null. If you did not set any extras this will be an empty bundle. |

### getTriggeredContentAuthorities

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTriggeredContentAuthorities(): Array<String!>?
```

For jobs with [android.app.job.JobInfo.Builder#addTriggerContentUri](../android/app/job/JobInfo.Builder.md))set, this reports which content authorities have triggered the job. It will only be null if no authorities have triggered it -- that is, the job executed for some other reason, such as a deadline expiring. If this is non-null, you can use [getTriggeredContentUris()](../android/app/job/JobParameters.md))to retrieve the details of which URIs changed (as long as that has not exceeded the maximum number it can reported). 

### getTriggeredContentUris

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTriggeredContentUris(): Array<Uri!>?
```

For jobs with [android.app.job.JobInfo.Builder#addTriggerContentUri](../android/app/job/JobInfo.Builder.md))set, this reports which URIs have triggered the job. This will be null if either no URIs have triggered it (it went off due to a deadline or other reason), or the number of changed URIs is too large to report. Whether or not the number of URIs is too large, you can always use [getTriggeredContentAuthorities()](../android/app/job/JobParameters.md))to determine whether the job was triggered due to any content changes and the authorities they are associated with. 

### isExpeditedJob

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isExpeditedJob(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether this job is running as an expedited job or not. A job is guaranteed to have all expedited job guarantees for the duration of the job execution if this returns`true`. This will return`false`if the job that wasn't requested to run as a expedited job, or if it was requested to run as an expedited job but the app didn't have any remaining expedited job quota at the time of execution. |

**See Also**

- [android.app.job.JobInfo.Builder#setExpedited(boolean)](../android/app/job/JobInfo.Builder.md)) 

### isOverrideDeadlineExpired

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isOverrideDeadlineExpired(): Boolean
```

For jobs with [android.app.job.JobInfo.Builder#setOverrideDeadline(long)](../android/app/job/JobInfo.Builder.md))set, this provides an easy way to tell whether the job is being executed due to the deadline expiring. Note: If the job is running because its deadline expired, it implies that its constraints will not be met. However, [periodic jobs](../android/app/job/JobInfo.Builder.md))will only ever run when their constraints are satisfied, therefore, the constraints will still be satisfied for a periodic job even if the deadline has expired. 

### isUserInitiatedJob

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isUserInitiatedJob(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether this job is running as a user-initiated job or not. A job is guaranteed to have all user-initiated job guarantees for the duration of the job execution if this returns`true`. This will return`false`if the job wasn't requested to run as a user-initiated job, or if it was requested to run as a user-initiated job but the app didn't meet any of the requirements at the time of execution, such as having the [android.Manifest.permission#RUN_USER_INITIATED_JOBS](../android/Manifest.permission.md) permission. |

**See Also**

- [android.app.job.JobInfo.Builder#setUserInitiated(boolean)](../android/app/job/JobInfo.Builder.md)) 

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<JobParameters!>
```
