# JobServiceEngine

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JobServiceEngine

Kotlin| [Java](https://developer.android.com/reference/android/app/job/JobServiceEngine "View this page in Java") 
| --- | --- |

```
abstract class JobServiceEngine
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.job.JobServiceEngine](https://developer.android.com/reference/kotlin/android/app/job/JobServiceEngine#) |

Helper for implementing a [android.app.Service](https://developer.android.com/reference/kotlin/android/app/Service.html#) that interacts with [JobScheduler](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler). This is not intended for use by regular applications, but allows frameworks built on top of the platform to create their own [android.app.Service](https://developer.android.com/reference/kotlin/android/app/Service.html#) that interact with [JobScheduler](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler) as well as add in additional functionality. If you just want to execute jobs normally, you should instead be looking at [JobService](https://developer.android.com/reference/kotlin/android/app/job/JobService).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [JobServiceEngine](https://developer.android.com/reference/kotlin/android/app/job/JobServiceEngine#JobServiceEngine(android.app.Service))`(`service:` ` [Service](https://developer.android.com/reference/kotlin/android/app/Service.html#)!`)` Create a new engine, ready for use. |

| Public methods ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#)! | [getBinder](https://developer.android.com/reference/kotlin/android/app/job/JobServiceEngine#getBinder())`()` Retrieve the engine's IPC interface that should be returned by [Service.onBind(Intent)](https://developer.android.com/reference/kotlin/android/app/Service.html#onBind(android.content.Intent)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [jobFinished](https://developer.android.com/reference/kotlin/android/app/job/JobServiceEngine#jobFinished(android.app.job.JobParameters,%20kotlin.Boolean))`(`params:` ` [JobParameters](https://developer.android.com/reference/kotlin/android/app/job/JobParameters)!`, `needsReschedule:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Call in to engine to report that a job has finished executing. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onNetworkChanged](https://developer.android.com/reference/kotlin/android/app/job/JobServiceEngine#onNetworkChanged(android.app.job.JobParameters))`(`params:` ` [JobParameters](https://developer.android.com/reference/kotlin/android/app/job/JobParameters)`)` Engine's report that the network for the job has changed. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onStartJob](https://developer.android.com/reference/kotlin/android/app/job/JobServiceEngine#onStartJob(android.app.job.JobParameters))`(`params:` ` [JobParameters](https://developer.android.com/reference/kotlin/android/app/job/JobParameters)!`)` Engine's report that a job has started. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onStopJob](https://developer.android.com/reference/kotlin/android/app/job/JobServiceEngine#onStopJob(android.app.job.JobParameters))`(`params:` ` [JobParameters](https://developer.android.com/reference/kotlin/android/app/job/JobParameters)!`)` Engine's report that a job has stopped. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNotification](https://developer.android.com/reference/kotlin/android/app/job/JobServiceEngine#setNotification(android.app.job.JobParameters,%20kotlin.Int,%20android.app.Notification,%20kotlin.Int))`(`params:` ` [JobParameters](https://developer.android.com/reference/kotlin/android/app/job/JobParameters)`, `notificationId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `notification:` ` [Notification](https://developer.android.com/reference/kotlin/android/app/Notification.html#)`, `jobEndNotificationPolicy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Give JobScheduler a notification to tie to this job's lifecycle. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateEstimatedNetworkBytes](https://developer.android.com/reference/kotlin/android/app/job/JobServiceEngine#updateEstimatedNetworkBytes(android.app.job.JobParameters,%20android.app.job.JobWorkItem,%20kotlin.Long,%20kotlin.Long))`(`params:` ` [JobParameters](https://developer.android.com/reference/kotlin/android/app/job/JobParameters)`, `item:` ` [JobWorkItem](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem)?`, `downloadBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `uploadBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Call in to engine to report data transfer progress. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateTransferredNetworkBytes](https://developer.android.com/reference/kotlin/android/app/job/JobServiceEngine#updateTransferredNetworkBytes(android.app.job.JobParameters,%20android.app.job.JobWorkItem,%20kotlin.Long,%20kotlin.Long))`(`params:` ` [JobParameters](https://developer.android.com/reference/kotlin/android/app/job/JobParameters)`, `item:` ` [JobWorkItem](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem)?`, `downloadBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `uploadBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Call in to engine to report data transfer progress. |

## Public constructors

### JobServiceEngine

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JobServiceEngine(service: Service!)
```

Create a new engine, ready for use.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `service` | [Service](https://developer.android.com/reference/kotlin/android/app/Service.html#)!:The [Service](https://developer.android.com/reference/kotlin/android/app/Service.html#) that is creating this engine and in which it will run. |

## Public methods

### getBinder

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBinder(): IBinder!
```

Retrieve the engine's IPC interface that should be returned by [Service.onBind(Intent)](https://developer.android.com/reference/kotlin/android/app/Service.html#onBind(android.content.Intent)). 

### jobFinished

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun jobFinished(
    params: JobParameters!, 
    needsReschedule: Boolean
): Unit
```

Call in to engine to report that a job has finished executing. See [JobService.jobFinished(JobParameters, boolean)](https://developer.android.com/reference/kotlin/android/app/job/JobService#jobFinished(android.app.job.JobParameters,%20kotlin.Boolean))for more information. 

### onNetworkChanged

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onNetworkChanged(params: JobParameters): Unit
```

Engine's report that the network for the job has changed.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `params` | [JobParameters](https://developer.android.com/reference/kotlin/android/app/job/JobParameters):This value cannot be`null`. |

**See Also**

- [android.app.job.JobService#onNetworkChanged(JobParameters)](https://developer.android.com/reference/kotlin/android/app/job/JobService#onNetworkChanged(android.app.job.JobParameters)) 

### onStartJob

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStartJob(params: JobParameters!): Boolean
```

Engine's report that a job has started. See [JobService.onStartJob](https://developer.android.com/reference/kotlin/android/app/job/JobService#onStartJob(android.app.job.JobParameters))for more information. 

### onStopJob

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStopJob(params: JobParameters!): Boolean
```

Engine's report that a job has stopped. See [JobService.onStopJob](https://developer.android.com/reference/kotlin/android/app/job/JobService#onStopJob(android.app.job.JobParameters))for more information. 

### setNotification

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNotification(
    params: JobParameters, 
    notificationId: Int, 
    notification: Notification, 
    jobEndNotificationPolicy: Int
): Unit
```

Give JobScheduler a notification to tie to this job's lifecycle.

| Parameters ||
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [JobParameters](https://developer.android.com/reference/kotlin/android/app/job/JobParameters):This value cannot be`null`. |
| `notification` | [Notification](https://developer.android.com/reference/kotlin/android/app/Notification.html#):This value cannot be`null`. |
| `jobEndNotificationPolicy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.app.job.JobService#JOB_END_NOTIFICATION_POLICY_DETACH](https://developer.android.com/reference/kotlin/android/app/job/JobService#JOB_END_NOTIFICATION_POLICY_DETACH:kotlin.Int), or [android.app.job.JobService#JOB_END_NOTIFICATION_POLICY_REMOVE](https://developer.android.com/reference/kotlin/android/app/job/JobService#JOB_END_NOTIFICATION_POLICY_REMOVE:kotlin.Int) |
| --- | --- |

**See Also**

- [android.app.job.JobService#setNotification(JobParameters, int, Notification, int)](https://developer.android.com/reference/kotlin/android/app/job/JobService#setNotification(android.app.job.JobParameters,%20kotlin.Int,%20android.app.Notification,%20kotlin.Int)) 

### updateEstimatedNetworkBytes

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun updateEstimatedNetworkBytes(
    params: JobParameters, 
    item: JobWorkItem?, 
    downloadBytes: Long, 
    uploadBytes: Long
): Unit
```

Call in to engine to report data transfer progress.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------|
| `params` | [JobParameters](https://developer.android.com/reference/kotlin/android/app/job/JobParameters):This value cannot be`null`. |
| `item` | [JobWorkItem](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem)?:This value may be`null`. |
| `downloadBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Value is a non-negative number of bytes. |
| --- | --- |
| `uploadBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Value is a non-negative number of bytes. |

**See Also**

- [android.app.job.JobService#updateEstimatedNetworkBytes(JobParameters, long, long)](https://developer.android.com/reference/kotlin/android/app/job/JobService#updateEstimatedNetworkBytes(android.app.job.JobParameters,%20kotlin.Long,%20kotlin.Long))
- [android.app.job.JobService#updateEstimatedNetworkBytes(JobParameters, JobWorkItem, long, long)](https://developer.android.com/reference/kotlin/android/app/job/JobService#updateEstimatedNetworkBytes(android.app.job.JobParameters,%20android.app.job.JobWorkItem,%20kotlin.Long,%20kotlin.Long)) 

### updateTransferredNetworkBytes

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun updateTransferredNetworkBytes(
    params: JobParameters, 
    item: JobWorkItem?, 
    downloadBytes: Long, 
    uploadBytes: Long
): Unit
```

Call in to engine to report data transfer progress.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------|
| `params` | [JobParameters](https://developer.android.com/reference/kotlin/android/app/job/JobParameters):This value cannot be`null`. |
| `item` | [JobWorkItem](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem)?:This value may be`null`. |
| `downloadBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Value is a non-negative number of bytes. |
| --- | --- |
| `uploadBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Value is a non-negative number of bytes. |

**See Also**

- [android.app.job.JobService#updateTransferredNetworkBytes(JobParameters, long, long)](https://developer.android.com/reference/kotlin/android/app/job/JobService#updateTransferredNetworkBytes(android.app.job.JobParameters,%20kotlin.Long,%20kotlin.Long))
- [android.app.job.JobService#updateTransferredNetworkBytes(JobParameters, JobWorkItem, long, long)](https://developer.android.com/reference/kotlin/android/app/job/JobService#updateTransferredNetworkBytes(android.app.job.JobParameters,%20android.app.job.JobWorkItem,%20kotlin.Long,%20kotlin.Long))
