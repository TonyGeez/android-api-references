Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JobScheduler

```
abstract class JobScheduler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.job.JobScheduler](../android/app/job/JobScheduler.md) |

This is an API for scheduling various types of jobs against the framework that will be executed in your application's own process.

See `https://developer.android.com/reference/kotlin/android/app/job/JobInfo` for more description of the types of jobs that can be run and how to construct them. You will construct these JobInfo objects and pass them to the JobScheduler with `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#schedule(android.app.job.JobInfo)`. When the criteria declared are met, the system will execute this job on your application's `https://developer.android.com/reference/kotlin/android/app/job/JobService`. You identify the service component that implements the logic for your job when you construct the JobInfo using `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#Builder(kotlin.Int,%20android.content.ComponentName)`.

The framework will be intelligent about when it executes jobs, and attempt to batch and defer them as much as possible. Typically, if you don't specify a deadline on a job, it can be run at any moment depending on the current state of the JobScheduler's internal queue.

Starting in Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, JobScheduler may try to optimize job execution by shifting execution to times with more available system resources in order to lower user impact. Factors in system health include sufficient battery, idle, charging, and access to an un-metered network. Jobs will initially be treated as if they have all these requirements, but as their deadlines approach, restrictions will become less strict. Requested requirements will not be affected by this change.

While a job is running, the system holds a wakelock on behalf of your app. For this reason, you do not need to take any action to guarantee that the device stays awake for the duration of the job.

You do not instantiate this class directly; instead, retrieve it through android.content.Context#getSystemService.

Prior to Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, jobs could only have a maximum of 100 jobs scheduled at a time. Starting with Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, that limit has been increased to 150. Expedited jobs also count towards the limit.

In Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int`, jobs had a maximum execution time of one minute. Starting with Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int` and ending with Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`, jobs had a maximum execution time of 10 minutes. Starting from Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, jobs will still be stopped after 10 minutes if the system is busy or needs the resources, but if not, jobs may continue running longer than 10 minutes.

**Note:** Beginning with API 30 (`https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`), JobScheduler will throttle runaway applications. Calling `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#schedule(android.app.job.JobInfo)` and other such methods with very high frequency can have a high cost and so, to make sure the system doesn't get overwhelmed, JobScheduler will begin to throttle apps, regardless of target SDK version.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_APP:kotlin.Int` The app is in a state that prevents the job from running (eg. the |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_APP_STANDBY:kotlin.Int` The current standby bucket prevents the job from running. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_BACKGROUND_RESTRICTION:kotlin.Int` The app is restricted from running in the background. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_BATTERY_NOT_LOW:kotlin.Int` The requested battery-not-low constraint is not satisfied. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CHARGING:kotlin.Int` The requested charging constraint is not satisfied. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CONNECTIVITY:kotlin.Int` The requested connectivity constraint is not satisfied. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CONTENT_TRIGGER:kotlin.Int` The requested content trigger constraint is not satisfied. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_DEADLINE:kotlin.Int` The override deadline has not transpired. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_DEVICE_IDLE:kotlin.Int` The requested idle constraint is not satisfied. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_MINIMUM_LATENCY:kotlin.Int` The minimum latency has not transpired. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_PREFETCH:kotlin.Int` The system's estimate of when the app will be launched is far away enough to warrant delaying this job. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_STORAGE_NOT_LOW:kotlin.Int` The requested storage-not-low constraint is not satisfied. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_DEVICE_STATE:kotlin.Int` The job is being deferred due to the device state (e.g., Doze, battery saver, memory usage, thermal status, etc.). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_EXECUTING:kotlin.Int` The job is currently running and is therefore not pending. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_INVALID_JOB_ID:kotlin.Int` The job doesn't exist. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_JOB_SCHEDULER_OPTIMIZATION:kotlin.Int` JobScheduler thinks it can defer this job to a more optimal running time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_QUOTA:kotlin.Int` The app has consumed all of its current quota. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_UNDEFINED:kotlin.Int` There is no known reason why the job is pending. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_USER:kotlin.Int` JobScheduler is respecting one of the user's actions (eg. force stop or adb shell commands) to defer this job. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#RESULT_FAILURE:kotlin.Int` Returned from `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#schedule(android.app.job.JobInfo)` if a job wasn't scheduled successfully. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#RESULT_SUCCESS:kotlin.Int` Returned from `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#schedule(android.app.job.JobInfo)` if this job has been successfully scheduled. |
| --- | --- |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#JobScheduler()()` <br /> |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#canRunUserInitiatedJobs()()` Returns `true` if the calling app currently holds the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#RUN_USER_INITIATED_JOBS:kotlin.String` permission, allowing it to run user-initiated jobs. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#cancel(kotlin.Int)(jobId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Cancel the specified job. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#cancelAll()()` Cancel all jobs that have been scheduled in the current namespace by the calling application. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#cancelInAllNamespaces()()` Cancel *all* jobs that have been scheduled by the calling application, regardless of namespace. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#enqueue(android.app.job.JobInfo,%20android.app.job.JobWorkItem)(job: https://developer.android.com/reference/kotlin/android/app/job/JobInfo, work: https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem)` Similar to `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#schedule(android.app.job.JobInfo)`, but allows you to enqueue work for a new *or existing* job. |
| open [JobScheduler](../android/app/job/JobScheduler.md) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#forNamespace(kotlin.String)(namespace: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Get a JobScheduler instance that is dedicated to a specific namespace. |
| --- | --- |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [JobInfo](../android/app/job/JobInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#getAllPendingJobs()()` Retrieve all jobs that have been scheduled by the calling application. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#getNamespace()()` Get the namespace this JobScheduler instance is operating in. |
| abstract [JobInfo](../android/app/job/JobInfo.md)? | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#getPendingJob(kotlin.Int)(jobId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Look up the description of a scheduled job. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#getPendingJobReason(kotlin.Int)(jobId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a reason why the job is pending and not currently executing. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [Duration](../java/time/Duration.md)!\> | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#getPendingJobReasonStats(kotlin.Int)(jobId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` For the given `jobId`, returns an aggregated view of why the job has been pending execution over its lifetime. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#getPendingJobReasons(kotlin.Int)(jobId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns potential reasons why the job with the given `jobId` may be pending and not currently executing. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PendingJobReasonsInfo](../android/app/job/PendingJobReasonsInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#getPendingJobReasonsHistory(kotlin.Int)(jobId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` For the given `jobId`, returns a limited historical view of why the job may have been pending execution. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [JobInfo](../android/app/job/JobInfo.md)!\>!\> | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#getPendingJobsInAllNamespaces()()` Retrieve all jobs that have been scheduled by the calling application within the current namespace. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#schedule(android.app.job.JobInfo)(job: https://developer.android.com/reference/kotlin/android/app/job/JobInfo)` Schedule a job to be executed. |
| --- | --- |

## Constants

### PENDING_JOB_REASON_APP

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PENDING_JOB_REASON_APP: Int
```

The app is in a state that prevents the job from running (eg. the `https://developer.android.com/reference/kotlin/android/app/job/JobService` component is disabled).

 Value: 1

### PENDING_JOB_REASON_APP_STANDBY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PENDING_JOB_REASON_APP_STANDBY: Int
```

The current standby bucket prevents the job from running.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager.html#STANDBY_BUCKET_RESTRICTED:kotlin.Int`

### PENDING_JOB_REASON_BACKGROUND_RESTRICTION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PENDING_JOB_REASON_BACKGROUND_RESTRICTION: Int
```

The app is restricted from running in the background.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#isBackgroundRestricted()`
- `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#isInstantApp()`

### PENDING_JOB_REASON_CONSTRAINT_BATTERY_NOT_LOW

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PENDING_JOB_REASON_CONSTRAINT_BATTERY_NOT_LOW: Int
```

The requested battery-not-low constraint is not satisfied.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setRequiresBatteryNotLow(kotlin.Boolean)`

### PENDING_JOB_REASON_CONSTRAINT_CHARGING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PENDING_JOB_REASON_CONSTRAINT_CHARGING: Int
```

The requested charging constraint is not satisfied.

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setRequiresCharging(kotlin.Boolean)`

### PENDING_JOB_REASON_CONSTRAINT_CONNECTIVITY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PENDING_JOB_REASON_CONSTRAINT_CONNECTIVITY: Int
```

The requested connectivity constraint is not satisfied.

 Value: 6

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setRequiredNetwork(android.net.NetworkRequest)`
- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setRequiredNetworkType(kotlin.Int)`

### PENDING_JOB_REASON_CONSTRAINT_CONTENT_TRIGGER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PENDING_JOB_REASON_CONSTRAINT_CONTENT_TRIGGER: Int
```

The requested content trigger constraint is not satisfied.

 Value: 7

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#addTriggerContentUri(android.app.job.JobInfo.TriggerContentUri)`

### PENDING_JOB_REASON_CONSTRAINT_DEADLINE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PENDING_JOB_REASON_CONSTRAINT_DEADLINE: Int
```

The override deadline has not transpired.

 Value: 16

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setOverrideDeadline(kotlin.Long)`

### PENDING_JOB_REASON_CONSTRAINT_DEVICE_IDLE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PENDING_JOB_REASON_CONSTRAINT_DEVICE_IDLE: Int
```

The requested idle constraint is not satisfied.

 Value: 8

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setRequiresDeviceIdle(kotlin.Boolean)`

### PENDING_JOB_REASON_CONSTRAINT_MINIMUM_LATENCY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PENDING_JOB_REASON_CONSTRAINT_MINIMUM_LATENCY: Int
```

The minimum latency has not transpired.

 Value: 9

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setMinimumLatency(kotlin.Long)`

### PENDING_JOB_REASON_CONSTRAINT_PREFETCH

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PENDING_JOB_REASON_CONSTRAINT_PREFETCH: Int
```

The system's estimate of when the app will be launched is far away enough to warrant delaying this job.

 Value: 10

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#isPrefetch()`
- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setPrefetch(kotlin.Boolean)`

### PENDING_JOB_REASON_CONSTRAINT_STORAGE_NOT_LOW

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PENDING_JOB_REASON_CONSTRAINT_STORAGE_NOT_LOW: Int
```

The requested storage-not-low constraint is not satisfied.

 Value: 11

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setRequiresStorageNotLow(kotlin.Boolean)`

### PENDING_JOB_REASON_DEVICE_STATE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PENDING_JOB_REASON_DEVICE_STATE: Int
```

The job is being deferred due to the device state (e.g., Doze, battery saver, memory usage, thermal status, etc.).

Starting in a version of Android following `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int`, the system will provide more specific pending reasons when possible, such as #PENDING_JOB_REASON_DEVICE_STATE_THERMAL or #PENDING_JOB_REASON_DEVICE_STATE_BATTERY_SAVER

 Value: 12

### PENDING_JOB_REASON_EXECUTING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PENDING_JOB_REASON_EXECUTING: Int
```

The job is currently running and is therefore not pending.

 Value: -1

### PENDING_JOB_REASON_INVALID_JOB_ID

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PENDING_JOB_REASON_INVALID_JOB_ID: Int
```

The job doesn't exist.

 Value: -2

### PENDING_JOB_REASON_JOB_SCHEDULER_OPTIMIZATION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PENDING_JOB_REASON_JOB_SCHEDULER_OPTIMIZATION: Int
```

JobScheduler thinks it can defer this job to a more optimal running time.

 Value: 13

### PENDING_JOB_REASON_QUOTA

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PENDING_JOB_REASON_QUOTA: Int
```

The app has consumed all of its current quota.

 Value: 14

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager.html#getAppStandbyBucket()`
- `https://developer.android.com/reference/kotlin/android/app/job/JobParameters#STOP_REASON_QUOTA:kotlin.Int`

### PENDING_JOB_REASON_UNDEFINED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PENDING_JOB_REASON_UNDEFINED: Int
```

There is no known reason why the job is pending. If additional reasons are added on newer Android versions, the system may return this reason to apps whose target SDK is not high enough to expect that reason.

 Value: 0

### PENDING_JOB_REASON_USER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PENDING_JOB_REASON_USER: Int
```

JobScheduler is respecting one of the user's actions (eg. force stop or adb shell commands) to defer this job.

 Value: 15

### RESULT_FAILURE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_FAILURE: Int
```

Returned from `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#schedule(android.app.job.JobInfo)` if a job wasn't scheduled successfully. Scheduling can fail for a variety of reasons, including, but not limited to:

- an invalid parameter was supplied (eg. the run-time for your job is too short, or the system can't resolve the requisite `https://developer.android.com/reference/kotlin/android/app/job/JobService` in your package)
- the app has too many jobs scheduled
- the app has tried to schedule too many jobs in a short amount of time

Attempting to schedule the job again immediately after receiving this result will not guarantee a successful schedule.

<br />

 Value: 0

### RESULT_SUCCESS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_SUCCESS: Int
```

Returned from `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#schedule(android.app.job.JobInfo)` if this job has been successfully scheduled.

 Value: 1

## Public constructors

### JobScheduler

```
JobScheduler()
```

## Public methods

### canRunUserInitiatedJobs

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canRunUserInitiatedJobs(): Boolean
```

Returns `true` if the calling app currently holds the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#RUN_USER_INITIATED_JOBS:kotlin.String` permission, allowing it to run user-initiated jobs.

### cancel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun cancel(jobId: Int): Unit
```

Cancel the specified job. If the job is currently executing, it is stopped immediately and the return value from its `https://developer.android.com/reference/kotlin/android/app/job/JobService#onStopJob(android.app.job.JobParameters)` method is ignored.

| Parameters ||
|---|---|
| `jobId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): unique identifier for the job to be canceled, as supplied to `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#Builder(kotlin.Int,%20android.content.ComponentName)`. |

### cancelAll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun cancelAll(): Unit
```

Cancel all jobs that have been scheduled in the current namespace by the calling application.

Starting with Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, this will only cancel within the current namespace. If a namespace hasn't been explicitly set with `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#forNamespace(kotlin.String)`, then this will cancel jobs in the default namespace. To cancel all jobs scheduled by the application, use `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#cancelInAllNamespaces()` instead.

### cancelInAllNamespaces

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cancelInAllNamespaces(): Unit
```

Cancel *all* jobs that have been scheduled by the calling application, regardless of namespace.

### enqueue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun enqueue(
    job: JobInfo, 
    work: JobWorkItem
): Int
```

Similar to `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#schedule(android.app.job.JobInfo)`, but allows you to enqueue work for a new *or existing* job. If a job with the same ID is already scheduled, it will be replaced with the new `https://developer.android.com/reference/kotlin/android/app/job/JobInfo`, but any previously enqueued work will remain and be dispatched the next time it runs. If a job with the same ID is already running, the new work will be enqueued for it without stopping the job.

The work you enqueue is later retrieved through `https://developer.android.com/reference/kotlin/android/app/job/JobParameters#dequeueWork()`. Be sure to see there about how to process work; the act of enqueueing work changes how you should handle the overall lifecycle of an executing job.

It is strongly encouraged that you use the same `https://developer.android.com/reference/kotlin/android/app/job/JobInfo` for all work you enqueue. This will allow the system to optimally schedule work along with any pending and/or currently running work. If the JobInfo changes from the last time the job was enqueued, the system will need to update the associated JobInfo, which can cause a disruption in execution. In particular, this can result in any currently running job that is processing previous work to be stopped and restarted with the new JobInfo.

It is recommended that you avoid using `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setExtras(android.os.PersistableBundle)` or `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setTransientExtras(android.os.Bundle)` with a JobInfo you are using to enqueue work. The system will try to compare these extras with the previous JobInfo, but there are situations where it may get this wrong and count the JobInfo as changing. (That said, you should be relatively safe with a simple set of consistent data in these fields.) You should never use `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setClipData(android.content.ClipData,%20kotlin.Int)` with work you are enqueuing, since currently this will always be treated as a different JobInfo, even if the ClipData contents are exactly the same.

**Note:** Scheduling a job can have a high cost, even if it's rescheduling the same job and the job didn't execute, especially on platform versions before version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int`. As such, the system may throttle calls to this API if calls are made too frequently in a short amount of time.

**Note:** Prior to Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, JobWorkItems could not be persisted. Apps were not allowed to enqueue JobWorkItems with persisted jobs and the system would throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` if they attempted to do so. Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, JobWorkItems can be persisted alongside the hosting job. However, Intents cannot be persisted. Set a `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#` using `https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem.Builder#setExtras(android.os.PersistableBundle)` for any information that needs to be persisted.

Note: The JobService component needs to be enabled in order to successfully schedule a job.

| Parameters ||
|---|---|
| `job` | [JobInfo](../android/app/job/JobInfo.md): The job you wish to enqueue work for. See `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder` for more detail on the sorts of jobs you can schedule. This value cannot be `null`. |
| `work` | [JobWorkItem](../android/app/job/JobWorkItem.md): New work to enqueue. This will be available later when the job starts running. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the result of the enqueue request. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#RESULT_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#RESULT_SUCCESS:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the specified `https://developer.android.com/reference/kotlin/android/app/job/JobService` doesn't exist or is disabled. |

### forNamespace

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun forNamespace(namespace: String): JobScheduler
```

Get a JobScheduler instance that is dedicated to a specific namespace. Any API calls using this instance will interact with jobs in that namespace, unless the API documentation says otherwise. Attempting to update a job scheduled in another namespace will not be possible but will instead create or update the job inside the current namespace. A JobScheduler instance dedicated to a namespace must be used to schedule or update jobs in that namespace.

Since leading and trailing whitespace can lead to hard-to-debug issues, they will be `https://developer.android.com/reference/kotlin/java/lang/String.html#trim()`. An empty String (after trimming) is not allowed.

| Parameters ||
|---|---|
| `namespace` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#getNamespace()`

### getAllPendingJobs

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getAllPendingJobs(): MutableList<JobInfo!>
```

Retrieve all jobs that have been scheduled by the calling application.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/job/JobInfo!>` | a list of all of the app's scheduled jobs. This includes jobs that are currently started as well as those that are still waiting to run. This value cannot be `null`. |

### getNamespace

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNamespace(): String?
```

Get the namespace this JobScheduler instance is operating in. A `null` value means that the app has not specified a namespace for this instance, and it is therefore using the default namespace.

### getPendingJob

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getPendingJob(jobId: Int): JobInfo?
```

Look up the description of a scheduled job.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/job/JobInfo?` | The `https://developer.android.com/reference/kotlin/android/app/job/JobInfo` description of the given scheduled job, or `null` if the supplied job ID does not correspond to any job. |

### getPendingJobReason

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPendingJobReason(jobId: Int): Int
```

Returns a reason why the job is pending and not currently executing. If there are multiple reasons why a job may be pending, this will only return one of them.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_UNDEFINED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_APP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_APP_STANDBY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_BACKGROUND_RESTRICTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_BATTERY_NOT_LOW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CHARGING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CONNECTIVITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CONTENT_TRIGGER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_DEVICE_IDLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_MINIMUM_LATENCY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_PREFETCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_STORAGE_NOT_LOW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_DEVICE_STATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_EXECUTING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_INVALID_JOB_ID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_JOB_SCHEDULER_OPTIMIZATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_QUOTA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_USER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_DEADLINE:kotlin.Int` |

### getPendingJobReasonStats

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPendingJobReasonStats(jobId: Int): MutableMap<Int!, Duration!>
```

For the given `jobId`, returns an aggregated view of why the job has been pending execution over its lifetime. The returned map is composed of `PENDING_JOB_REASON_*` constants mapped to a duration representing the total time the job has been pending for that reason.

Note that the sum of these durations will often exceed the total duration the job was waiting, since a job could be pending due to multiple reasons simultaneously.

These pending job reasons represent either explicitly set constraints on the job or implicit constraints imposed by the system due to various reasons. The results can be used to debug which constraints contribute the most to why a given job has been pending execution.

If the returned map is empty, it could indicate that the job was executed immediately and never had to wait for any constraints to be met.

To get a more detailed and historical view of why a job was pending at a certain time, use `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#getPendingJobReasonsHistory(kotlin.Int)` instead.

Note: The pending job reason stats are not persisted across device reboots. The stats are also cleared when the job successfully completes or is canceled. Apps should query this information when they observe a scheduled job is not executing as expected to understand the reasons for the delay.

<br />

| Parameters ||
|---|---|
| `jobId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The ID of the job to query. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, https://developer.android.com/reference/kotlin/java/time/Duration.html#!>` | A map of pending reasons to the total duration the job was pending for that reason. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the `jobId` does not correspond to a pending job. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#getPendingJobReasons(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#getPendingJobReasonsHistory(kotlin.Int)`

### getPendingJobReasons

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPendingJobReasons(jobId: Int): IntArray
```

Returns potential reasons why the job with the given `jobId` may be pending and not currently executing.

The returned array will include reasons composed of both explicitly set constraints on the job and implicit constraints imposed by the system. The results can be used to debug why a given job may not be currently executing.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_UNDEFINED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_APP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_APP_STANDBY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_BACKGROUND_RESTRICTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_BATTERY_NOT_LOW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CHARGING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CONNECTIVITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_CONTENT_TRIGGER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_DEVICE_IDLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_MINIMUM_LATENCY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_PREFETCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_STORAGE_NOT_LOW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_DEVICE_STATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_EXECUTING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_INVALID_JOB_ID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_JOB_SCHEDULER_OPTIMIZATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_QUOTA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_USER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#PENDING_JOB_REASON_CONSTRAINT_DEADLINE:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#getPendingJobReasonsHistory(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#getPendingJobReasonStats(kotlin.Int)`

### getPendingJobReasonsHistory

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPendingJobReasonsHistory(jobId: Int): MutableList<PendingJobReasonsInfo!>
```

For the given `jobId`, returns a limited historical view of why the job may have been pending execution. The returned list is composed of `https://developer.android.com/reference/kotlin/android/app/job/PendingJobReasonsInfo` objects, each of which include a timestamp since epoch along with an array of unsatisfied constraints represented by `PENDING_JOB_REASON_*` constants.

These constants could either be explicitly set constraints on the job or implicit constraints imposed by the system due to various reasons. The results can be used to debug why a given job may have been pending execution.

If `PENDING_JOB_REASON_UNDEFINED` is the only reason for the timestamp, it could mean that the job was ready to be executed at that point in time.

The length of the history returned is truncated so it's recommended to query this API periodically for debugging purposes. To get a holistic view of why the job has been pending, use `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#getPendingJobReasonStats(kotlin.Int)`.

Note: there is no set interval for the timestamps in the returned list since constraint changes occur based on device status and various other factors.

Note: the pending job reasons history is not persisted across device reboots.

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/job/PendingJobReasonsInfo!>` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the `jobId` is invalid. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#getPendingJobReasons(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#getPendingJobReasonStats(kotlin.Int)`

### getPendingJobsInAllNamespaces

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPendingJobsInAllNamespaces(): MutableMap<String!, MutableList<JobInfo!>!>
```

Retrieve all jobs that have been scheduled by the calling application within the current namespace.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/job/JobInfo!>!>` | a list of all of the app's scheduled jobs scheduled with the current namespace. If a namespace hasn't been explicitly set with `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#forNamespace(kotlin.String)`, then this will return jobs in the default namespace. This includes jobs that are currently started as well as those that are still waiting to run. This value cannot be `null`. |

### schedule

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun schedule(job: JobInfo): Int
```

Schedule a job to be executed. Will replace any currently scheduled job with the same ID with the new information in the `https://developer.android.com/reference/kotlin/android/app/job/JobInfo`. If a job with the given ID is currently running, it will be stopped.

**Note:** Scheduling a job can have a high cost, even if it's rescheduling the same job and the job didn't execute, especially on platform versions before version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int`. As such, the system may throttle calls to this API if calls are made too frequently in a short amount of time.

Note: The JobService component needs to be enabled in order to successfully schedule a job.

| Parameters ||
|---|---|
| `job` | [JobInfo](../android/app/job/JobInfo.md): The job you wish scheduled. See `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder` for more detail on the sorts of jobs you can schedule. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the result of the schedule request. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#RESULT_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#RESULT_SUCCESS:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the specified `https://developer.android.com/reference/kotlin/android/app/job/JobService` doesn't exist or is disabled. |
