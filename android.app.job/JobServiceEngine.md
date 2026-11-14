# JobServiceEngine

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JobServiceEngine

Kotlin| [Java](JobServiceEngine.md) 
| --- | --- |

```
abstract class JobServiceEngine
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.job.JobServiceEngine](JobServiceEngine.md) |

Helper for implementing a [android.app.Service](../android.app/Service.md) that interacts with [JobScheduler](JobScheduler.md). This is not intended for use by regular applications, but allows frameworks built on top of the platform to create their own [android.app.Service](../android.app/Service.md) that interact with [JobScheduler](JobScheduler.md) as well as add in additional functionality. If you just want to execute jobs normally, you should instead be looking at [JobService](JobService.md).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [JobServiceEngine](JobServiceEngine.md))`(`service:` ` [Service](../android.app/Service.md)!`)` Create a new engine, ready for use. |

| Public methods ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IBinder](../android.os/IBinder.md)! | [getBinder](JobServiceEngine.md))`()` Retrieve the engine's IPC interface that should be returned by [Service.onBind(Intent)](../android.app/Service.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [jobFinished](JobServiceEngine.md))`(`params:` ` [JobParameters](JobParameters.md)!`, `needsReschedule:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Call in to engine to report that a job has finished executing. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onNetworkChanged](JobServiceEngine.md))`(`params:` ` [JobParameters](JobParameters.md)`)` Engine's report that the network for the job has changed. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onStartJob](JobServiceEngine.md))`(`params:` ` [JobParameters](JobParameters.md)!`)` Engine's report that a job has started. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onStopJob](JobServiceEngine.md))`(`params:` ` [JobParameters](JobParameters.md)!`)` Engine's report that a job has stopped. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNotification](JobServiceEngine.md))`(`params:` ` [JobParameters](JobParameters.md)`, `notificationId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `notification:` ` [Notification](../android.app/Notification.md)`, `jobEndNotificationPolicy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Give JobScheduler a notification to tie to this job's lifecycle. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateEstimatedNetworkBytes](JobServiceEngine.md))`(`params:` ` [JobParameters](JobParameters.md)`, `item:` ` [JobWorkItem](JobWorkItem.md)?`, `downloadBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `uploadBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Call in to engine to report data transfer progress. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateTransferredNetworkBytes](JobServiceEngine.md))`(`params:` ` [JobParameters](JobParameters.md)`, `item:` ` [JobWorkItem](JobWorkItem.md)?`, `downloadBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `uploadBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Call in to engine to report data transfer progress. |

## Public constructors

### JobServiceEngine

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JobServiceEngine(service: Service!)
```

Create a new engine, ready for use.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `service` | [Service](../android.app/Service.md)!:The [Service](../android.app/Service.md) that is creating this engine and in which it will run. |

## Public methods

### getBinder

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBinder(): IBinder!
```

Retrieve the engine's IPC interface that should be returned by [Service.onBind(Intent)](../android.app/Service.md)). 

### jobFinished

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun jobFinished(
    params: JobParameters!, 
    needsReschedule: Boolean
): Unit
```

Call in to engine to report that a job has finished executing. See [JobService.jobFinished(JobParameters, boolean)](JobService.md))for more information. 

### onNetworkChanged

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onNetworkChanged(params: JobParameters): Unit
```

Engine's report that the network for the job has changed.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `params` | [JobParameters](JobParameters.md):This value cannot be`null`. |

**See Also**

- [android.app.job.JobService#onNetworkChanged(JobParameters)](JobService.md)) 

### onStartJob

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStartJob(params: JobParameters!): Boolean
```

Engine's report that a job has started. See [JobService.onStartJob](JobService.md))for more information. 

### onStopJob

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStopJob(params: JobParameters!): Boolean
```

Engine's report that a job has stopped. See [JobService.onStopJob](JobService.md))for more information. 

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
| `params` | [JobParameters](JobParameters.md):This value cannot be`null`. |
| `notification` | [Notification](../android.app/Notification.md):This value cannot be`null`. |
| `jobEndNotificationPolicy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.app.job.JobService#JOB_END_NOTIFICATION_POLICY_DETACH](JobService.md), or [android.app.job.JobService#JOB_END_NOTIFICATION_POLICY_REMOVE](JobService.md) |
| --- | --- |

**See Also**

- [android.app.job.JobService#setNotification(JobParameters, int, Notification, int)](JobService.md)) 

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
| `params` | [JobParameters](JobParameters.md):This value cannot be`null`. |
| `item` | [JobWorkItem](JobWorkItem.md)?:This value may be`null`. |
| `downloadBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Value is a non-negative number of bytes. |
| --- | --- |
| `uploadBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Value is a non-negative number of bytes. |

**See Also**

- [android.app.job.JobService#updateEstimatedNetworkBytes(JobParameters, long, long)](JobService.md))
- [android.app.job.JobService#updateEstimatedNetworkBytes(JobParameters, JobWorkItem, long, long)](JobService.md)) 

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
| `params` | [JobParameters](JobParameters.md):This value cannot be`null`. |
| `item` | [JobWorkItem](JobWorkItem.md)?:This value may be`null`. |
| `downloadBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Value is a non-negative number of bytes. |
| --- | --- |
| `uploadBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Value is a non-negative number of bytes. |

**See Also**

- [android.app.job.JobService#updateTransferredNetworkBytes(JobParameters, long, long)](JobService.md))
- [android.app.job.JobService#updateTransferredNetworkBytes(JobParameters, JobWorkItem, long, long)](JobService.md))
