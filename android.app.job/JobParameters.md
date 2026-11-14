# JobParameters

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JobParameters

Kotlin| [Java](https://developer.android.com/reference/android/app/job/JobParameters "View this page in Java") 

```
open class JobParameters : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.job.JobParameters](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#) |

Contains the parameters used to configure/identify your job. You do not create this object yourself, instead it is handed in to your application by the System.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_APP_STANDBY](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_APP_STANDBY:kotlin.Int) The current standby bucket requires that the job stop now. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_BACKGROUND_RESTRICTION](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_BACKGROUND_RESTRICTION:kotlin.Int) The app is restricted from running in the background. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_CANCELLED_BY_APP](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_CANCELLED_BY_APP:kotlin.Int) The job was cancelled directly by the app, either by calling [JobScheduler.cancel(int)](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#cancel(kotlin.Int)), [JobScheduler.cancelAll()](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#cancelAll()), or by scheduling a new job with the same job ID. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_CONSTRAINT_BATTERY_NOT_LOW](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_CONSTRAINT_BATTERY_NOT_LOW:kotlin.Int) The requested battery-not-low constraint is no longer satisfied. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_CONSTRAINT_CHARGING](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_CONSTRAINT_CHARGING:kotlin.Int) The requested charging constraint is no longer satisfied. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_CONSTRAINT_CONNECTIVITY](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_CONSTRAINT_CONNECTIVITY:kotlin.Int) The requested connectivity constraint is no longer satisfied. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_CONSTRAINT_DEVICE_IDLE](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_CONSTRAINT_DEVICE_IDLE:kotlin.Int) The requested idle constraint is no longer satisfied. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_CONSTRAINT_STORAGE_NOT_LOW](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_CONSTRAINT_STORAGE_NOT_LOW:kotlin.Int) The requested storage-not-low constraint is no longer satisfied. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_DEVICE_STATE](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_DEVICE_STATE:kotlin.Int) The device state (eg. Doze, battery saver, memory usage, etc) requires JobScheduler stop this job. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_ESTIMATED_APP_LAUNCH_TIME_CHANGED](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_ESTIMATED_APP_LAUNCH_TIME_CHANGED:kotlin.Int) The system's estimate of when the app will be launched changed significantly enough to decide this job shouldn't be running right now. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_PREEMPT](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_PREEMPT:kotlin.Int) The job was stopped to run a higher priority job of the app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_QUOTA](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_QUOTA:kotlin.Int) The app has consumed all of its current quota. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_SYSTEM_PROCESSING](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_SYSTEM_PROCESSING:kotlin.Int) The system is doing some processing that requires stopping this job. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_TIMEOUT](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_TIMEOUT:kotlin.Int) The job used up its maximum execution time and timed out. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_TIMEOUT_ABANDONED](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_TIMEOUT_ABANDONED:kotlin.Int) The job used up its maximum execution time and timed out. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_UNDEFINED](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_UNDEFINED:kotlin.Int) There is no reason the job is stopped. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STOP_REASON_USER](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_USER:kotlin.Int) The user stopped the job. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [completeWork](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#completeWork(android.app.job.JobWorkItem))`(`work:` ` [JobWorkItem](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem)`)` Report the completion of executing a [JobWorkItem](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem) previously returned by [dequeueWork()](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#dequeueWork()). |
| open [JobWorkItem](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem)? | [dequeueWork](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#dequeueWork())`()` Dequeue the next pending [JobWorkItem](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem) from these JobParameters associated with their currently running job. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#describeContents())`()` <br /> |
| open [ClipData](https://developer.android.com/reference/kotlin/android/content/ClipData.html#)? | [getClipData](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#getClipData())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getClipGrantFlags](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#getClipGrantFlags())`()` <br /> |
| open [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#) | [getExtras](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#getExtras())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getJobId](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#getJobId())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getJobNamespace](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#getJobNamespace())`()` Get the namespace this job was placed in. |
| open [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#)? | [getNetwork](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#getNetwork())`()` Return the network that should be used to perform any network requests for this job. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStopReason](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#getStopReason())`()` Returns the reason [JobService.onStopJob(JobParameters)](https://developer.android.com/reference/kotlin/android/app/job/JobService#onStopJob(android.app.job.JobParameters))was called on this job. |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [getTransientExtras](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#getTransientExtras())`()` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | [getTriggeredContentAuthorities](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#getTriggeredContentAuthorities())`()` For jobs with [android.app.job.JobInfo.Builder#addTriggerContentUri](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#addTriggerContentUri(android.app.job.JobInfo.TriggerContentUri))set, this reports which content authorities have triggered the job. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>? | [getTriggeredContentUris](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#getTriggeredContentUris())`()` For jobs with [android.app.job.JobInfo.Builder#addTriggerContentUri](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#addTriggerContentUri(android.app.job.JobInfo.TriggerContentUri))set, this reports which URIs have triggered the job. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExpeditedJob](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#isExpeditedJob())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOverrideDeadlineExpired](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#isOverrideDeadlineExpired())`()` For jobs with [android.app.job.JobInfo.Builder#setOverrideDeadline(long)](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setOverrideDeadline(kotlin.Long))set, this provides an easy way to tell whether the job is being executed due to the deadline expiring. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUserInitiatedJob](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#isUserInitiatedJob())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [JobParameters](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### STOP_REASON_APP_STANDBY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_APP_STANDBY: Int
```

The current standby bucket requires that the job stop now. 

 Value: 12

**See Also**

- [android.app.usage.UsageStatsManager#STANDBY_BUCKET_RESTRICTED](https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager.html#STANDBY_BUCKET_RESTRICTED:kotlin.Int) 

### STOP_REASON_BACKGROUND_RESTRICTION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_BACKGROUND_RESTRICTION: Int
```

The app is restricted from running in the background. 

 Value: 11

**See Also**

- [android.app.ActivityManager#isBackgroundRestricted()](https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#isBackgroundRestricted())
- [android.content.pm.PackageManager#isInstantApp()](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#isInstantApp()) 

### STOP_REASON_CANCELLED_BY_APP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_CANCELLED_BY_APP: Int
```

The job was cancelled directly by the app, either by calling [JobScheduler.cancel(int)](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#cancel(kotlin.Int)), [JobScheduler.cancelAll()](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#cancelAll()), or by scheduling a new job with the same job ID. 

 Value: 1

### STOP_REASON_CONSTRAINT_BATTERY_NOT_LOW

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_CONSTRAINT_BATTERY_NOT_LOW: Int
```

The requested battery-not-low constraint is no longer satisfied. 

 Value: 5

**See Also**

- [android.app.job.JobInfo.Builder#setRequiresBatteryNotLow(boolean)](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setRequiresBatteryNotLow(kotlin.Boolean)) 

### STOP_REASON_CONSTRAINT_CHARGING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_CONSTRAINT_CHARGING: Int
```

The requested charging constraint is no longer satisfied. 

 Value: 6

**See Also**

- [android.app.job.JobInfo.Builder#setRequiresCharging(boolean)](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setRequiresCharging(kotlin.Boolean)) 

### STOP_REASON_CONSTRAINT_CONNECTIVITY

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_CONSTRAINT_CONNECTIVITY: Int
```

The requested connectivity constraint is no longer satisfied. 

 Value: 7

**See Also**

- [android.app.job.JobInfo.Builder#setRequiredNetwork(NetworkRequest)](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setRequiredNetwork(android.net.NetworkRequest))
- [android.app.job.JobInfo.Builder#setRequiredNetworkType(int)](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setRequiredNetworkType(kotlin.Int)) 

### STOP_REASON_CONSTRAINT_DEVICE_IDLE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_CONSTRAINT_DEVICE_IDLE: Int
```

The requested idle constraint is no longer satisfied. 

 Value: 8

**See Also**

- [android.app.job.JobInfo.Builder#setRequiresDeviceIdle(boolean)](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setRequiresDeviceIdle(kotlin.Boolean)) 

### STOP_REASON_CONSTRAINT_STORAGE_NOT_LOW

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_CONSTRAINT_STORAGE_NOT_LOW: Int
```

The requested storage-not-low constraint is no longer satisfied. 

 Value: 9

**See Also**

- [android.app.job.JobInfo.Builder#setRequiresStorageNotLow(boolean)](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setRequiresStorageNotLow(kotlin.Boolean)) 

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

- [android.app.job.JobInfo#isPrefetch()](https://developer.android.com/reference/kotlin/android/app/job/JobInfo#isPrefetch())
- [android.app.job.JobInfo.Builder#setPrefetch(boolean)](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setPrefetch(kotlin.Boolean)) 

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

- [android.app.usage.UsageStatsManager#getAppStandbyBucket()](https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager.html#getAppStandbyBucket()) 

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

The job used up its maximum execution time and timed out. Each individual job has a maximum execution time limit, regardless of how much total quota the app has. See the note on [JobScheduler](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler) and [JobInfo](https://developer.android.com/reference/kotlin/android/app/job/JobInfo) for the execution time limits. 

 Value: 3

### STOP_REASON_TIMEOUT_ABANDONED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_TIMEOUT_ABANDONED: Int
```

The job used up its maximum execution time and timed out. The system also detected that the app can no longer call [JobService.jobFinished(JobParameters, boolean)](https://developer.android.com/reference/kotlin/android/app/job/JobService#jobFinished(android.app.job.JobParameters,%20kotlin.Boolean))for this job, likely because the strong reference to the job handle ([JobParameters](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#)) passed to it via [JobService.onStartJob(JobParameters)](https://developer.android.com/reference/kotlin/android/app/job/JobService#onStartJob(android.app.job.JobParameters))was lost. This can occur even if the app called [JobScheduler.cancel(int)](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#cancel(kotlin.Int)), [JobScheduler.cancelAll()](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#cancelAll()), or [JobScheduler.cancelInAllNamespaces()](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#cancelInAllNamespaces())to stop an active job while losing strong references to the job handle. In this case, the job is not necessarily abandoned. However, the system cannot distinguish such cases from truly abandoned jobs.

It is recommended that you use [JobService.jobFinished(JobParameters, boolean)](https://developer.android.com/reference/kotlin/android/app/job/JobService#jobFinished(android.app.job.JobParameters,%20kotlin.Boolean))or return false from [JobService.onStartJob(JobParameters)](https://developer.android.com/reference/kotlin/android/app/job/JobService#onStartJob(android.app.job.JobParameters))to stop an active job. This will prevent the occurrence of this stop reason and the need to handle it. The primary use case for this stop reason is to report a probable case of a job being abandoned.

<br />

 Value: 16

### STOP_REASON_UNDEFINED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STOP_REASON_UNDEFINED: Int
```

There is no reason the job is stopped. This is the value returned from the JobParameters object passed to [JobService.onStartJob(JobParameters)](https://developer.android.com/reference/kotlin/android/app/job/JobService#onStartJob(android.app.job.JobParameters)). 

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

Report the completion of executing a [JobWorkItem](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem) previously returned by [dequeueWork()](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#dequeueWork()). This tells the system you are done with the work associated with that item, so it will not be returned again. Note that if this is the last work in the queue, completing it here will*not* finish the overall job -- for that to happen, you still need to call [dequeueWork()](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#dequeueWork())again.

If you are enqueueing work into a job, you must call this method for each piece of work you process. Do*not* call [JobService.jobFinished(JobParameters, boolean)](https://developer.android.com/reference/kotlin/android/app/job/JobService#jobFinished(android.app.job.JobParameters,%20kotlin.Boolean))or else you can lose work in your queue.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `work` | [JobWorkItem](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem):The work you have completed processing, as previously returned by [dequeueWork()](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#dequeueWork())This value cannot be`null`. |

### dequeueWork

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dequeueWork(): JobWorkItem?
```

Dequeue the next pending [JobWorkItem](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem) from these JobParameters associated with their currently running job. Calling this method when there is no more work available and all previously dequeued work has been completed will result in the system taking care of stopping the job for you -- you should not call [JobService.jobFinished(JobParameters, boolean)](https://developer.android.com/reference/kotlin/android/app/job/JobService#jobFinished(android.app.job.JobParameters,%20kotlin.Boolean))yourself (otherwise you risk losing an upcoming JobWorkItem that is being enqueued at the same time).

Once you are done with the [JobWorkItem](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem) returned by this method, you must call [completeWork(android.app.job.JobWorkItem)](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#completeWork(android.app.job.JobWorkItem))with it to inform the system that you are done executing the work. The job will not be finished until all dequeued work has been completed. You do not, however, have to complete each returned work item before deqeueing the next one -- you can use [dequeueWork()](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#dequeueWork())multiple times before completing previous work if you want to process work in parallel, and you can complete the work in whatever order you want.

If the job runs to the end of its available time period before all work has been completed, it will stop as normal. You should return true from [JobService.onStopJob(JobParameters)](https://developer.android.com/reference/kotlin/android/app/job/JobService#onStopJob(android.app.job.JobParameters))in order to have the job rescheduled, and by doing so any pending as well as remaining uncompleted work will be re-queued for the next time the job runs.

This example shows how to construct a JobService that will serially dequeue and process work that is available for it:

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [JobWorkItem](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem)? | Returns a new [JobWorkItem](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem) if there is one pending, otherwise null. If null is returned, the system will also stop the job if all work has also been completed. (This means that for correct operation, you must always call dequeueWork() after you have completed other work, to check either for more work or allow the system to stop the job.) |

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getClipData

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getClipData(): ClipData?
```

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ClipData](https://developer.android.com/reference/kotlin/android/content/ClipData.html#)? | The clip you passed in when constructing this job with [android.app.job.JobInfo.Builder#setClipData(ClipData, int)](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setClipData(android.content.ClipData,%20kotlin.Int)). Will be null if it was not set. |

### getClipGrantFlags

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getClipGrantFlags(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The clip grant flags you passed in when constructing this job with [android.app.job.JobInfo.Builder#setClipData(ClipData, int)](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setClipData(android.content.ClipData,%20kotlin.Int)). Will be 0 if it was not set. |

### getExtras

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExtras(): PersistableBundle
```

| Return ||
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#) | The extras you passed in when constructing this job with [android.app.job.JobInfo.Builder#setExtras(android.os.PersistableBundle)](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setExtras(android.os.PersistableBundle)). This will never be null. If you did not set any extras this will be an empty bundle. |

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

- [android.app.job.JobScheduler#forNamespace(String)](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#forNamespace(kotlin.String)) 

### getNetwork

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNetwork(): Network?
```

Return the network that should be used to perform any network requests for this job.

Devices may have multiple active network connections simultaneously, or they may not have a default network route at all. To correctly handle all situations like this, your job should always use the network returned by this method instead of implicitly using the default network route.

Note that the system may relax the constraints you originally requested, such as allowing a [JobInfo.NETWORK_TYPE_UNMETERED](https://developer.android.com/reference/kotlin/android/app/job/JobInfo#NETWORK_TYPE_UNMETERED:kotlin.Int) job to run over a metered network when there is a surplus of metered data available. Starting in Android version [android.os.Build.VERSION_CODES#UPSIDE_DOWN_CAKE](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int), this will return`null`if the app does not hold the permissions specified in [JobInfo.Builder.setRequiredNetwork(NetworkRequest)](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setRequiredNetwork(android.net.NetworkRequest)).

| Return ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#)? | the network that should be used to perform any network requests for this job, or`null`if this job didn't set any required network type or if the job executed when there was no available network to use. |

**See Also**

- [android.app.job.JobInfo.Builder#setRequiredNetworkType(int)](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setRequiredNetworkType(kotlin.Int))
- [android.app.job.JobInfo.Builder#setRequiredNetwork(NetworkRequest)](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setRequiredNetwork(android.net.NetworkRequest)) 

### getStopReason

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStopReason(): Int
```

Returns the reason [JobService.onStopJob(JobParameters)](https://developer.android.com/reference/kotlin/android/app/job/JobService#onStopJob(android.app.job.JobParameters))was called on this job.

Apps should not rely on the stop reason for critical decision-making, as additional stop reasons may be added in subsequent Android releases. The primary intended use of this method is for logging and diagnostic purposes to gain insights into the causes of job termination.

<br />

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The reason [JobService.onStopJob(JobParameters)](https://developer.android.com/reference/kotlin/android/app/job/JobService#onStopJob(android.app.job.JobParameters))was called on this job. Will be [STOP_REASON_UNDEFINED](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_UNDEFINED:kotlin.Int) if [JobService.onStopJob(JobParameters)](https://developer.android.com/reference/kotlin/android/app/job/JobService#onStopJob(android.app.job.JobParameters))has not yet been called. Value is [android.app.job.JobParameters#STOP_REASON_UNDEFINED](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_UNDEFINED:kotlin.Int), [android.app.job.JobParameters#STOP_REASON_CANCELLED_BY_APP](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_CANCELLED_BY_APP:kotlin.Int), [android.app.job.JobParameters#STOP_REASON_PREEMPT](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_PREEMPT:kotlin.Int), [android.app.job.JobParameters#STOP_REASON_TIMEOUT](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_TIMEOUT:kotlin.Int), [android.app.job.JobParameters#STOP_REASON_DEVICE_STATE](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_DEVICE_STATE:kotlin.Int), [android.app.job.JobParameters#STOP_REASON_CONSTRAINT_BATTERY_NOT_LOW](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_CONSTRAINT_BATTERY_NOT_LOW:kotlin.Int), [android.app.job.JobParameters#STOP_REASON_CONSTRAINT_CHARGING](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_CONSTRAINT_CHARGING:kotlin.Int), [android.app.job.JobParameters#STOP_REASON_CONSTRAINT_CONNECTIVITY](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_CONSTRAINT_CONNECTIVITY:kotlin.Int), [android.app.job.JobParameters#STOP_REASON_CONSTRAINT_DEVICE_IDLE](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_CONSTRAINT_DEVICE_IDLE:kotlin.Int), [android.app.job.JobParameters#STOP_REASON_CONSTRAINT_STORAGE_NOT_LOW](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_CONSTRAINT_STORAGE_NOT_LOW:kotlin.Int), [android.app.job.JobParameters#STOP_REASON_QUOTA](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_QUOTA:kotlin.Int), [android.app.job.JobParameters#STOP_REASON_BACKGROUND_RESTRICTION](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_BACKGROUND_RESTRICTION:kotlin.Int), [android.app.job.JobParameters#STOP_REASON_APP_STANDBY](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_APP_STANDBY:kotlin.Int), [android.app.job.JobParameters#STOP_REASON_USER](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_USER:kotlin.Int), [android.app.job.JobParameters#STOP_REASON_SYSTEM_PROCESSING](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_SYSTEM_PROCESSING:kotlin.Int), [android.app.job.JobParameters#STOP_REASON_ESTIMATED_APP_LAUNCH_TIME_CHANGED](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_ESTIMATED_APP_LAUNCH_TIME_CHANGED:kotlin.Int), or [android.app.job.JobParameters#STOP_REASON_TIMEOUT_ABANDONED](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_TIMEOUT_ABANDONED:kotlin.Int) |

### getTransientExtras

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTransientExtras(): Bundle
```

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | The transient extras you passed in when constructing this job with [android.app.job.JobInfo.Builder#setTransientExtras(android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setTransientExtras(android.os.Bundle)). This will never be null. If you did not set any extras this will be an empty bundle. |

### getTriggeredContentAuthorities

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTriggeredContentAuthorities(): Array<String!>?
```

For jobs with [android.app.job.JobInfo.Builder#addTriggerContentUri](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#addTriggerContentUri(android.app.job.JobInfo.TriggerContentUri))set, this reports which content authorities have triggered the job. It will only be null if no authorities have triggered it -- that is, the job executed for some other reason, such as a deadline expiring. If this is non-null, you can use [getTriggeredContentUris()](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#getTriggeredContentUris())to retrieve the details of which URIs changed (as long as that has not exceeded the maximum number it can reported). 

### getTriggeredContentUris

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTriggeredContentUris(): Array<Uri!>?
```

For jobs with [android.app.job.JobInfo.Builder#addTriggerContentUri](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#addTriggerContentUri(android.app.job.JobInfo.TriggerContentUri))set, this reports which URIs have triggered the job. This will be null if either no URIs have triggered it (it went off due to a deadline or other reason), or the number of changed URIs is too large to report. Whether or not the number of URIs is too large, you can always use [getTriggeredContentAuthorities()](https://developer.android.com/reference/kotlin/android/app/job/JobParameters#getTriggeredContentAuthorities())to determine whether the job was triggered due to any content changes and the authorities they are associated with. 

### isExpeditedJob

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isExpeditedJob(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether this job is running as an expedited job or not. A job is guaranteed to have all expedited job guarantees for the duration of the job execution if this returns`true`. This will return`false`if the job that wasn't requested to run as a expedited job, or if it was requested to run as an expedited job but the app didn't have any remaining expedited job quota at the time of execution. |

**See Also**

- [android.app.job.JobInfo.Builder#setExpedited(boolean)](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setExpedited(kotlin.Boolean)) 

### isOverrideDeadlineExpired

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isOverrideDeadlineExpired(): Boolean
```

For jobs with [android.app.job.JobInfo.Builder#setOverrideDeadline(long)](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setOverrideDeadline(kotlin.Long))set, this provides an easy way to tell whether the job is being executed due to the deadline expiring. Note: If the job is running because its deadline expired, it implies that its constraints will not be met. However, [periodic jobs](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setPeriodic(kotlin.Long))will only ever run when their constraints are satisfied, therefore, the constraints will still be satisfied for a periodic job even if the deadline has expired. 

### isUserInitiatedJob

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isUserInitiatedJob(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether this job is running as a user-initiated job or not. A job is guaranteed to have all user-initiated job guarantees for the duration of the job execution if this returns`true`. This will return`false`if the job wasn't requested to run as a user-initiated job, or if it was requested to run as a user-initiated job but the app didn't meet any of the requirements at the time of execution, such as having the [android.Manifest.permission#RUN_USER_INITIATED_JOBS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#RUN_USER_INITIATED_JOBS:kotlin.String) permission. |

**See Also**

- [android.app.job.JobInfo.Builder#setUserInitiated(boolean)](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setUserInitiated(kotlin.Boolean)) 

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<JobParameters!>
```
