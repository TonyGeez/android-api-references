Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JobInfo

```
open class JobInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.job.JobInfo](https://developer.android.com/reference/kotlin/android/app/job/JobInfo#) |

Container of data passed to the `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler` fully encapsulating the parameters required to schedule work against the calling application. These are constructed using the `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder`. The goal here is to provide the scheduler with high-level semantics about the work you want to accomplish.

Prior to Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int`, you had to specify at least one constraint on the JobInfo object that you are creating. Otherwise, the builder would throw an exception when building. From Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and onwards, it is valid to schedule jobs with no constraints.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder` Builder class for constructing `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#` objects. |
| | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.TriggerContentUri` Information about a content URI modification that a job would like to trigger on. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#BACKOFF_POLICY_EXPONENTIAL:kotlin.Int` Exponentially back-off a failed job. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#BACKOFF_POLICY_LINEAR:kotlin.Int` Linearly back-off a failed job. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#CATEGORY_APP_UPDATES:kotlin.Int` Category indicating the job is for performing app updates by a registered app store. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#CATEGORY_NONE:kotlin.Int` Default category indicating no category is assigned. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#DEFAULT_INITIAL_BACKOFF_MILLIS:kotlin.Long` Amount of backoff a job has initially by default, in milliseconds. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#MAX_BACKOFF_DELAY_MILLIS:kotlin.Long` Maximum backoff we allow for a job, in milliseconds. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#NETWORK_BYTES_UNKNOWN:kotlin.Int` Sentinel value indicating that bytes are unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#NETWORK_TYPE_ANY:kotlin.Int` This job requires network connectivity. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#NETWORK_TYPE_CELLULAR:kotlin.Int` This job requires network connectivity that is a cellular network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#NETWORK_TYPE_METERED:kotlin.Int` This job requires metered connectivity such as most cellular data networks. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#NETWORK_TYPE_NONE:kotlin.Int` Default. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#NETWORK_TYPE_NOT_ROAMING:kotlin.Int` This job requires network connectivity that is not roaming. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#NETWORK_TYPE_UNMETERED:kotlin.Int` This job requires network connectivity that is unmetered. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#PRIORITY_DEFAULT:kotlin.Int` Default value for all regular jobs. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#PRIORITY_HIGH:kotlin.Int` This task should be ordered ahead of most other tasks. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#PRIORITY_LOW:kotlin.Int` Low priority. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#PRIORITY_MAX:kotlin.Int` This task is critical to user experience or functionality and should be run ahead of all other tasks. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#PRIORITY_MIN:kotlin.Int` Job has minimal value to the user. |
| --- | --- |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getBackoffPolicy()()` Return the backoff policy of this job. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getCategory()()` <br /> |
| open [ClipData](https://developer.android.com/reference/kotlin/android/content/ClipData.html#)? | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getClipData()()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getClipGrantFlags()()` <br /> |
| --- | --- |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getDebugTags()()` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getEstimatedNetworkDownloadBytes()()` Return the estimated size of download traffic that will be performed by this job, in bytes. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getEstimatedNetworkUploadBytes()()` Return the estimated size of upload traffic that will be performed by this job, in bytes. |
| --- | --- |
| open [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getExtras()()` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getFlexMillis()()` Flex time for this job. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getId()()` Unique job id associated with this application (uid). |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getInitialBackoffMillis()()` The amount of time the JobScheduler will wait before rescheduling a failed job. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getIntervalMillis()()` Set to the interval between occurrences of this job. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getMaxExecutionDelayMillis()()` <br /> |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getMinFlexMillis()()` Query the minimum flex time allowed for periodic scheduled jobs. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getMinLatencyMillis()()` Set for a job that does not recur periodically, to specify a delay after which the job will be eligible for execution. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getMinPeriodMillis()()` Query the minimum interval allowed for periodic scheduled jobs. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getMinimumNetworkChunkBytes()()` Return the smallest piece of data that cannot be easily paused and resumed, in bytes. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getNetworkType()()` Return the basic description of the kind of network this job requires. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getPriority()()` <br /> |
| --- | --- |
| open [NetworkRequest](https://developer.android.com/reference/kotlin/android/net/NetworkRequest.html#)? | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getRequiredNetwork()()` Return the detailed description of the kind of network this job requires, or `null` if no specific kind of network is required. |
| open [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getService()()` Name of the service endpoint that will be called back into by the JobScheduler. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getTraceTag()()` <br /> |
| --- | --- |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getTransientExtras()()` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getTriggerContentMaxDelay()()` When triggering on content URI changes, this is the maximum delay we will use before scheduling the job. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getTriggerContentUpdateDelay()()` When triggering on content URI changes, this is the delay from when a change is detected until the job is scheduled. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [JobInfo.TriggerContentUri](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.TriggerContentUri)!\>? | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getTriggerContentUris()()` Which content: URIs must change for the job to be scheduled. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#hashCode()()` Returns a hash code value for the object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#isExpedited()()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#isImportantWhileForeground()()` **Note:** Beginning with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int`, this flag will be ignored and no longer function effectively, regardless of the calling app's target SDK version. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#isPeriodic()()` Track whether this job will repeat with a given period. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#isPersisted()()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#isPrefetch()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#isRequireBatteryNotLow()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#isRequireCharging()()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#isRequireDeviceIdle()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#isRequireStorageNotLow()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#isUserInitiated()()` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#toString()()` Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(out: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [JobInfo](https://developer.android.com/reference/kotlin/android/app/job/JobInfo#)!\> | `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### BACKOFF_POLICY_EXPONENTIAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BACKOFF_POLICY_EXPONENTIAL: Int
```

Exponentially back-off a failed job. See `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setBackoffCriteria(kotlin.Long,%20kotlin.Int)` retry_time(current_time, num_failures) = current_time + initial_backoff_millis \* 2 \^ (num_failures - 1), num_failures \>= 1

 Value: 1

### BACKOFF_POLICY_LINEAR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BACKOFF_POLICY_LINEAR: Int
```

Linearly back-off a failed job. See `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setBackoffCriteria(kotlin.Long,%20kotlin.Int)` retry_time(current_time, num_failures) = current_time + initial_backoff_millis \* num_failures, num_failures \>= 1

 Value: 0

### CATEGORY_APP_UPDATES

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_APP_UPDATES: Int
```

Category indicating the job is for performing app updates by a registered app store.

This category can only be used by registered app stores (apps holding the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#INSTALL_PACKAGES_AS_REGISTERED_APP_STORE:kotlin.String` permission) and will throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` otherwise.

This is a hint to the system. The system may choose relaxed throttling and quota policies for the jobs marked with this category to make sure the app updates are completed in a timely manner. This **may** include exemption from app standby buckets, but it is not guaranteed.

This category cannot be combined with #setPersisted(boolean), #setPrefetch(boolean), or #setUserInitiated(boolean) constraints. Attempting to set any of these will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` when calling #build(). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#INSTALL_PACKAGES_AS_REGISTERED_APP_STORE:kotlin.String`

 Value: 1

### CATEGORY_NONE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CATEGORY_NONE: Int
```

Default category indicating no category is assigned.

 Value: 0

### DEFAULT_INITIAL_BACKOFF_MILLIS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEFAULT_INITIAL_BACKOFF_MILLIS: Long
```

Amount of backoff a job has initially by default, in milliseconds.

 Value: 30000L

### MAX_BACKOFF_DELAY_MILLIS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX_BACKOFF_DELAY_MILLIS: Long
```

Maximum backoff we allow for a job, in milliseconds.

 Value: 18000000L

### NETWORK_BYTES_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_BYTES_UNKNOWN: Int
```

Sentinel value indicating that bytes are unknown.

 Value: -1

### NETWORK_TYPE_ANY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_ANY: Int
```

This job requires network connectivity.

 Value: 1

### NETWORK_TYPE_CELLULAR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_CELLULAR: Int
```

This job requires network connectivity that is a cellular network.

 Value: 4

### NETWORK_TYPE_METERED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_METERED: Int
```

**Deprecated:** *Cellular networks may be unmetered, or Wi-Fi networks may be metered, so this isn't a good way of selecting a specific transport. Instead, use `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#NETWORK_TYPE_CELLULAR:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/net/NetworkRequest.Builder.html#addTransportType(kotlin.Int)` if your job requires a specific network transport.*

This job requires metered connectivity such as most cellular data networks.

 Value: 4

### NETWORK_TYPE_NONE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_NONE: Int
```

Default.

 Value: 0

### NETWORK_TYPE_NOT_ROAMING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_NOT_ROAMING: Int
```

This job requires network connectivity that is not roaming.

 Value: 3

### NETWORK_TYPE_UNMETERED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NETWORK_TYPE_UNMETERED: Int
```

This job requires network connectivity that is unmetered.

 Value: 2

### PRIORITY_DEFAULT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRIORITY_DEFAULT: Int
```

Default value for all regular jobs. As noted in `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler`, these jobs have a general execution time of 10 minutes. Receives the standard job management policy.

 Value: 300

### PRIORITY_HIGH

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRIORITY_HIGH: Int
```

This task should be ordered ahead of most other tasks. It may be deferred a little, but if it doesn't run at some point, the user may think something is wrong. Assuming all constraints remain satisfied (including ideal system load conditions), these jobs can have an execution time of at least 4 minutes. Setting all of your jobs to high priority will not be beneficial to your app and in fact may hurt its performance in the long run.

 Value: 400

### PRIORITY_LOW

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRIORITY_LOW: Int
```

Low priority. The task provides some benefit to users, but is not critical and is more of a nice-to-have. This is more important than minimum priority jobs and will be prioritized ahead of them, but may still be deferred in lieu of higher priority jobs. JobScheduler *may* decide to defer these tasks while there are higher priority tasks in order to ensure there is sufficient quota available for the higher priority tasks. A sample task of low priority: prefetching data the user hasn't requested

 Value: 200

### PRIORITY_MAX

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRIORITY_MAX: Int
```

This task is critical to user experience or functionality and should be run ahead of all other tasks. Only `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setExpedited(kotlin.Boolean)` and `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setUserInitiated(kotlin.Boolean)` can have this priority.

Example tasks of max priority:

- Receiving a text message and processing it to show a notification
- Downloading or uploading some content the user requested to transfer immediately

 Value: 500

### PRIORITY_MIN

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRIORITY_MIN: Int
```

Job has minimal value to the user. The user has absolutely no expectation or knowledge of this task and it has no bearing on the user's perception of the app whatsoever. JobScheduler *may* decide to defer these tasks while there are higher priority tasks in order to ensure there is sufficient quota available for the higher priority tasks. A sample task of min priority: uploading analytics

 Value: 100

## Public methods

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getBackoffPolicy

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBackoffPolicy(): Int
```

Return the backoff policy of this job.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#BACKOFF_POLICY_LINEAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#BACKOFF_POLICY_EXPONENTIAL:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setBackoffCriteria(kotlin.Long,%20kotlin.Int)`

### getCategory

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCategory(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Return the category assigned to this job. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#CATEGORY_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#CATEGORY_APP_UPDATES:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setCategory(kotlin.Int)`

### getClipData

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getClipData(): ClipData?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/ClipData.html#?` | This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setClipData(android.content.ClipData,%20kotlin.Int)`

### getClipGrantFlags

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getClipGrantFlags(): Int
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setClipData(android.content.ClipData,%20kotlin.Int)`

### getDebugTags

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDebugTags(): MutableSet<String!>
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#addDebugTag(kotlin.String)`

### getEstimatedNetworkDownloadBytes

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEstimatedNetworkDownloadBytes(): Long
```

Return the estimated size of download traffic that will be performed by this job, in bytes. 
Value is a non-negative number of bytes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Estimated size of download traffic, or `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#NETWORK_BYTES_UNKNOWN:kotlin.Int` when unknown. Value is a non-negative number of bytes. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setEstimatedNetworkBytes(kotlin.Long,%20kotlin.Long)`

### getEstimatedNetworkUploadBytes

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEstimatedNetworkUploadBytes(): Long
```

Return the estimated size of upload traffic that will be performed by this job, in bytes. 
Value is a non-negative number of bytes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Estimated size of upload traffic, or `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#NETWORK_BYTES_UNKNOWN:kotlin.Int` when unknown. Value is a non-negative number of bytes. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setEstimatedNetworkBytes(kotlin.Long,%20kotlin.Long)`

### getExtras

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getExtras(): PersistableBundle
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setExtras(android.os.PersistableBundle)`

### getFlexMillis

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFlexMillis(): Long
```

Flex time for this job. Only valid if this is a periodic job. The job can execute at any time in a window of flex length at the end of the period.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setPeriodic(kotlin.Long)`
- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setPeriodic(kotlin.Long,%20kotlin.Long)`

### getId

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getId(): Int
```

Unique job id associated with this application (uid). This is the same job ID you supplied in the `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder` constructor.

### getInitialBackoffMillis

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInitialBackoffMillis(): Long
```

The amount of time the JobScheduler will wait before rescheduling a failed job. This value will be increased depending on the backoff policy specified at job creation time. Defaults to 30 seconds, minimum is currently 10 seconds.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setBackoffCriteria(kotlin.Long,%20kotlin.Int)`

### getIntervalMillis

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIntervalMillis(): Long
```

Set to the interval between occurrences of this job. This value is **not** set if the job does not recur periodically.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setPeriodic(kotlin.Long)`
- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setPeriodic(kotlin.Long,%20kotlin.Long)`

### getMaxExecutionDelayMillis

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMaxExecutionDelayMillis(): Long
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setOverrideDeadline(kotlin.Long)`

### getMinFlexMillis

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getMinFlexMillis(): Long
```

Query the minimum flex time allowed for periodic scheduled jobs. Attempting to declare a shorter flex time than this when scheduling such a job will result in this amount as the effective flex time for the job.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The minimum available flex time for scheduling periodic jobs, in milliseconds. |

### getMinLatencyMillis

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMinLatencyMillis(): Long
```

Set for a job that does not recur periodically, to specify a delay after which the job will be eligible for execution. This value is not set if the job recurs periodically.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setMinimumLatency(kotlin.Long)`

### getMinPeriodMillis

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getMinPeriodMillis(): Long
```

Query the minimum interval allowed for periodic scheduled jobs. Attempting to declare a smaller period than this when scheduling a job will result in a job that is still periodic, but will run with this effective period.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The minimum available interval for scheduling periodic jobs, in milliseconds. |

### getMinimumNetworkChunkBytes

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMinimumNetworkChunkBytes(): Long
```

Return the smallest piece of data that cannot be easily paused and resumed, in bytes. 
Value is a non-negative number of bytes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Smallest piece of data that cannot be easily paused and resumed, or `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#NETWORK_BYTES_UNKNOWN:kotlin.Int` when unknown. Value is a non-negative number of bytes. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setMinimumNetworkChunkBytes(kotlin.Long)`

### getNetworkType

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNetworkType(): Int
```

**Deprecated:** *This method attempts to map `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getRequiredNetwork()` into the set of simple constants, which results in a loss of fidelity. Callers should move to using `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#getRequiredNetwork()` directly.*

Return the basic description of the kind of network this job requires.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#NETWORK_TYPE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#NETWORK_TYPE_ANY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#NETWORK_TYPE_UNMETERED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#NETWORK_TYPE_NOT_ROAMING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#NETWORK_TYPE_CELLULAR:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setRequiredNetworkType(kotlin.Int)`

### getPriority

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPriority(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#PRIORITY_MIN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#PRIORITY_LOW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#PRIORITY_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#PRIORITY_HIGH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#PRIORITY_MAX:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setPriority(kotlin.Int)`

### getRequiredNetwork

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRequiredNetwork(): NetworkRequest?
```

Return the detailed description of the kind of network this job requires, or `null` if no specific kind of network is required.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setRequiredNetwork(android.net.NetworkRequest)`

### getService

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getService(): ComponentName
```

Name of the service endpoint that will be called back into by the JobScheduler.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` | This value cannot be `null`. |

### getTraceTag

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTraceTag(): String?
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setTraceTag(kotlin.String)`

### getTransientExtras

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTransientExtras(): Bundle
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setTransientExtras(android.os.Bundle)`

### getTriggerContentMaxDelay

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTriggerContentMaxDelay(): Long
```

When triggering on content URI changes, this is the maximum delay we will use before scheduling the job.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setTriggerContentMaxDelay(kotlin.Long)`

### getTriggerContentUpdateDelay

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTriggerContentUpdateDelay(): Long
```

When triggering on content URI changes, this is the delay from when a change is detected until the job is scheduled.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setTriggerContentUpdateDelay(kotlin.Long)`

### getTriggerContentUris

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTriggerContentUris(): Array<JobInfo.TriggerContentUri!>?
```

Which content: URIs must change for the job to be scheduled. Returns null if there are none required.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#addTriggerContentUri(android.app.job.JobInfo.TriggerContentUri)`

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isExpedited

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isExpedited(): Boolean
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setExpedited(kotlin.Boolean)`

### isImportantWhileForeground

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isImportantWhileForeground(): Boolean
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/app/job/JobInfo#isExpedited()` instead.*

**Note:** Beginning with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int`, this flag will be ignored and no longer function effectively, regardless of the calling app's target SDK version. Calling this method will always return `false`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setImportantWhileForeground(kotlin.Boolean)`

### isPeriodic

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isPeriodic(): Boolean
```

Track whether this job will repeat with a given period.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setPeriodic(kotlin.Long)`
- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setPeriodic(kotlin.Long,%20kotlin.Long)`

### isPersisted

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isPersisted(): Boolean
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setPersisted(kotlin.Boolean)`

### isPrefetch

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isPrefetch(): Boolean
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setPrefetch(kotlin.Boolean)`

### isRequireBatteryNotLow

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isRequireBatteryNotLow(): Boolean
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setRequiresBatteryNotLow(kotlin.Boolean)`

### isRequireCharging

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isRequireCharging(): Boolean
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setRequiresCharging(kotlin.Boolean)`

### isRequireDeviceIdle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isRequireDeviceIdle(): Boolean
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setRequiresDeviceIdle(kotlin.Boolean)`

### isRequireStorageNotLow

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isRequireStorageNotLow(): Boolean
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setRequiresStorageNotLow(kotlin.Boolean)`

### isUserInitiated

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isUserInitiated(): Boolean
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder#setUserInitiated(kotlin.Boolean)`

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<JobInfo!>
```
