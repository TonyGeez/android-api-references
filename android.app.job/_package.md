# android.app.job

# android.app.job

Kotlin | [Java](_package.md)
| --- | --- |

## Classes

| [JobInfo](JobInfo.md) | Container of data passed to the [android.app.job.JobScheduler](JobScheduler.md) fully encapsulating the parameters required to schedule work against the calling application. |
| --- | --- |
| [JobParameters](JobParameters.md) | Contains the parameters used to configure/identify your job. |
| [JobScheduler](JobScheduler.md) | This is an API for scheduling various types of jobs against the framework that will be executed in your application's own process. |
| [JobService](JobService.md) | Entry point for the callback from the [android.app.job.JobScheduler](JobScheduler.md). |
| --- | --- |
| [JobServiceEngine](JobServiceEngine.md) | Helper for implementing a [android.app.Service](../android.app/Service.md) that interacts with [JobScheduler](JobScheduler.md). |
| [JobWorkItem](JobWorkItem.md) | A unit of work that can be enqueued for a job using [JobScheduler.enqueue](JobScheduler.md)). |
| [PendingJobReasonsInfo](PendingJobReasonsInfo.md) | A simple wrapper which includes a timestamp (in millis since epoch) and an array of android. |
| --- | --- |
