# android.app.job

# android.app.job

Kotlin | [Java](../android/app/job/_package.md)
| --- | --- |

## Classes

| [JobInfo](../android/app/job/JobInfo.md) | Container of data passed to the [android.app.job.JobScheduler](../android/app/job/JobScheduler.md) fully encapsulating the parameters required to schedule work against the calling application. |
| --- | --- |
| [JobParameters](../android/app/job/JobParameters.md) | Contains the parameters used to configure/identify your job. |
| [JobScheduler](../android/app/job/JobScheduler.md) | This is an API for scheduling various types of jobs against the framework that will be executed in your application's own process. |
| [JobService](../android/app/job/JobService.md) | Entry point for the callback from the [android.app.job.JobScheduler](../android/app/job/JobScheduler.md). |
| --- | --- |
| [JobServiceEngine](../android/app/job/JobServiceEngine.md) | Helper for implementing a [android.app.Service](../android/app/Service.md) that interacts with [JobScheduler](../android/app/job/JobScheduler.md). |
| [JobWorkItem](../android/app/job/JobWorkItem.md) | A unit of work that can be enqueued for a job using [JobScheduler.enqueue](../android/app/job/JobScheduler.md)). |
| [PendingJobReasonsInfo](../android/app/job/PendingJobReasonsInfo.md) | A simple wrapper which includes a timestamp (in millis since epoch) and an array of android. |
| --- | --- |
