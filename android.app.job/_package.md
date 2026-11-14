# android.app.job

# android.app.job

Kotlin | [Java](https://developer.android.com/reference/android/app/job/package-summary "View this page in Java")

## Classes

| [JobInfo](https://developer.android.com/reference/kotlin/android/app/job/JobInfo) | Container of data passed to the [android.app.job.JobScheduler](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler) fully encapsulating the parameters required to schedule work against the calling application. |
| [JobParameters](https://developer.android.com/reference/kotlin/android/app/job/JobParameters) | Contains the parameters used to configure/identify your job. |
| [JobScheduler](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler) | This is an API for scheduling various types of jobs against the framework that will be executed in your application's own process. |
| [JobService](https://developer.android.com/reference/kotlin/android/app/job/JobService) | Entry point for the callback from the [android.app.job.JobScheduler](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler). |
| [JobServiceEngine](https://developer.android.com/reference/kotlin/android/app/job/JobServiceEngine) | Helper for implementing a [android.app.Service](https://developer.android.com/reference/kotlin/android/app/Service.html#) that interacts with [JobScheduler](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler). |
| [JobWorkItem](https://developer.android.com/reference/kotlin/android/app/job/JobWorkItem) | A unit of work that can be enqueued for a job using [JobScheduler.enqueue](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler#enqueue(android.app.job.JobInfo,%20android.app.job.JobWorkItem)). |
| [PendingJobReasonsInfo](https://developer.android.com/reference/kotlin/android/app/job/PendingJobReasonsInfo) | A simple wrapper which includes a timestamp (in millis since epoch) and an array of android. |
