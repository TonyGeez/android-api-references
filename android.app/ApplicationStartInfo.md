Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ApplicationStartInfo

```
class ApplicationStartInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.ApplicationStartInfo](ApplicationStartInfo.md) |

Describes information related to an application process's startup.

Many aspects concerning why and how an applications process was started are valuable for apps both for logging and for potential behavior changes. Reason for process start, start type, start times, throttling, and other useful diagnostic data can be obtained from ApplicationStartInfo records.

ApplicationStartInfo objects can be retrieved via: - getHistoricalProcessStartReasons, which can be called during or after a application's startup. Using this method, an app can retrieve information about an in-progress app start. - addApplicationStartInfoCompletionListener, which returns an ApplicationStartInfo object via a callback when the startup is complete, or immediately if requested after the startup is complete.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#LAUNCH_MODE_SINGLE_INSTANCE:kotlin.Int` The system creates the activity at the root of a new task or locates the activity on an existing task with the same affinity. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#LAUNCH_MODE_SINGLE_INSTANCE_PER_TASK:kotlin.Int` The activity can only be running as the root activity of the task, the first activity that created the task, and therefore there will only be one instance of this activity in a task; but activity can be instantiated multiple times in different tasks. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#LAUNCH_MODE_SINGLE_TASK:kotlin.Int` Same as "singleTask", except that the system doesn't launch any other activities into the task holding the instance. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#LAUNCH_MODE_SINGLE_TOP:kotlin.Int` If an instance of the activity already exists at the top of the target task, the system routes the intent to that instance through a call to its onNewIntent() method, rather than creating a new instance of the activity. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#LAUNCH_MODE_STANDARD:kotlin.Int` Default. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#STARTUP_STATE_ERROR:kotlin.Int` State indicating process startup has failed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#STARTUP_STATE_FIRST_FRAME_DRAWN:kotlin.Int` State indicating process startup has made it to first frame draw. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#STARTUP_STATE_STARTED:kotlin.Int` State indicating process startup has started. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_COMPONENT_ACTIVITY:kotlin.Int` Process was started for an activity component. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_COMPONENT_BROADCAST:kotlin.Int` Process was started for a broadcast component. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_COMPONENT_CONTENT_PROVIDER:kotlin.Int` Process was started for a content provider component. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_COMPONENT_OTHER:kotlin.Int` Process was started not for one of the four standard components. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_COMPONENT_SERVICE:kotlin.Int` Process was started for a service component. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_ALARM:kotlin.Int` Process started due to alarm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_BACKUP:kotlin.Int` Process started to run backup. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_BOOT_COMPLETE:kotlin.Int` Process started due to boot complete. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_BROADCAST:kotlin.Int` Process started due to broadcast received for any reason not explicitly listed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_CONTENT_PROVIDER:kotlin.Int` Process started due to access of ContentProvider for any reason not explicitly listed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_JOB:kotlin.Int` \* Process started to run scheduled job. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_LAUNCHER:kotlin.Int` Process started due to click app icon or widget from launcher. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_LAUNCHER_RECENTS:kotlin.Int` Process started from launcher recents. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_OTHER:kotlin.Int` Process started not for any of the listed reasons. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_PUSH:kotlin.Int` Process started due to push message. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_SERVICE:kotlin.Int` Process started due to Service started for any reason not explicitly listed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_START_ACTIVITY:kotlin.Int` Process started due to Activity started for any reason not explicitly listed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TIMESTAMP_APPLICATION_ONCREATE:kotlin.Int` Clock monotonic timestamp of Application onCreate called. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TIMESTAMP_BIND_APPLICATION:kotlin.Int` Clock monotonic timestamp of bindApplication called. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TIMESTAMP_FIRST_FRAME:kotlin.Int` Clock monotonic timestamp of first frame drawn. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TIMESTAMP_FORK:kotlin.Int` Clock monotonic timestamp of process fork. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TIMESTAMP_FULLY_DRAWN:kotlin.Int` Clock monotonic timestamp of reportFullyDrawn called by application. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TIMESTAMP_INITIAL_RENDERTHREAD_FRAME:kotlin.Int` Clock monotonic timestamp of initial renderthread frame. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TIMESTAMP_LAUNCH:kotlin.Int` Clock monotonic timestamp of launch started. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TIMESTAMP_RESERVED_RANGE_DEVELOPER:kotlin.Int` The end of the range reserved for developer supplied timestamps. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TIMESTAMP_RESERVED_RANGE_DEVELOPER_START:kotlin.Int` The beginning of the range reserved for developer supplied timestamps. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TIMESTAMP_RESERVED_RANGE_SYSTEM:kotlin.Int` The end of the range, beginning with 0, reserved for system timestamps. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TIMESTAMP_SOURCE_EVENT:kotlin.Int` Clock monotonic timestamp of the source event which triggered this start. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TIMESTAMP_SURFACEFLINGER_COMPOSITION_COMPLETE:kotlin.Int` Clock monotonic timestamp of surfaceflinger composition complete. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TYPE_COLD:kotlin.Int` Process started from scratch. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TYPE_HOT:kotlin.Int` Process brought back to foreground. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TYPE_UNSET:kotlin.Int` Start type not yet set. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TYPE_WARM:kotlin.Int` Process retained minimally SavedInstanceState. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDefiningUid Return the defining kernel user identifier, maybe different from getRealUid and getPackageUid, if an external service has the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestService_useAppZygote:kotlin.Int` set to ` true` and was bound with the flag `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_EXTERNAL_SERVICE:kotlin.Int` - in this case, this field here will be the kernel user identifier of the external service provider. |
| --- | --- |
| [Intent](../android.content/Intent.md)? | getIntent The intent used to launch the application. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getLaunchMode An instruction on how the activity should be launched. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPackageUid Similar to getRealUid, it's the kernel user identifier that is assigned at the package installation time. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPid The process id. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getProcessName The actual process name it was running with. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getRealUid The kernel user identifier of the process, most of the time the system uses this to do access control checks. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getReason The reason code of what triggered the process's start. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getStartComponent The component type that was being started which triggered the start. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getStartType The state of the app at startup. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getStartupState Current state of startup. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\> | getStartupTimestamps Various clock monotonic timestamps in nanoseconds throughout the startup process. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | wasForceStopped Informs whether this is the first process launch for an app since it was `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#FLAG_STOPPED:kotlin.Int` for some reason. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ApplicationStartInfo](ApplicationStartInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### LAUNCH_MODE_SINGLE_INSTANCE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LAUNCH_MODE_SINGLE_INSTANCE: Int
```

The system creates the activity at the root of a new task or locates the activity on an existing task with the same affinity. If an instance of the activity already exists and is at the root of the task, the system routes the intent to existing instance through a call to its onNewIntent() method, rather than creating a new one.

 Value: 2

### LAUNCH_MODE_SINGLE_INSTANCE_PER_TASK

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LAUNCH_MODE_SINGLE_INSTANCE_PER_TASK: Int
```

The activity can only be running as the root activity of the task, the first activity that created the task, and therefore there will only be one instance of this activity in a task; but activity can be instantiated multiple times in different tasks.

 Value: 4

### LAUNCH_MODE_SINGLE_TASK

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LAUNCH_MODE_SINGLE_TASK: Int
```

Same as "singleTask", except that the system doesn't launch any other activities into the task holding the instance. The activity is always the single and only member of its task.

 Value: 3

### LAUNCH_MODE_SINGLE_TOP

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LAUNCH_MODE_SINGLE_TOP: Int
```

If an instance of the activity already exists at the top of the target task, the system routes the intent to that instance through a call to its onNewIntent() method, rather than creating a new instance of the activity.

 Value: 1

### LAUNCH_MODE_STANDARD

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LAUNCH_MODE_STANDARD: Int
```

Default. The system always creates a new instance of the activity in the target task and routes the intent to it.

 Value: 0

### STARTUP_STATE_ERROR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STARTUP_STATE_ERROR: Int
```

State indicating process startup has failed. Startup information in ApplicationStartInfo is incomplete, but no more will be added.

 Value: 1

### STARTUP_STATE_FIRST_FRAME_DRAWN

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STARTUP_STATE_FIRST_FRAME_DRAWN: Int
```

State indicating process startup has made it to first frame draw. Startup information in ApplicationStartInfo is complete with potential exception of fully drawn timestamp which is not guaranteed to be set.

 Value: 2

### STARTUP_STATE_STARTED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STARTUP_STATE_STARTED: Int
```

State indicating process startup has started. Some information is available in ApplicationStartInfo and more will be added.

 Value: 0

### START_COMPONENT_ACTIVITY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_COMPONENT_ACTIVITY: Int
```

Process was started for an activity component.

 Value: 1

### START_COMPONENT_BROADCAST

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_COMPONENT_BROADCAST: Int
```

Process was started for a broadcast component.

 Value: 2

### START_COMPONENT_CONTENT_PROVIDER

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_COMPONENT_CONTENT_PROVIDER: Int
```

Process was started for a content provider component.

 Value: 3

### START_COMPONENT_OTHER

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_COMPONENT_OTHER: Int
```

Process was started not for one of the four standard components.

 Value: 5

### START_COMPONENT_SERVICE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_COMPONENT_SERVICE: Int
```

Process was started for a service component.

 Value: 4

### START_REASON_ALARM

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_REASON_ALARM: Int
```

Process started due to alarm.

 Value: 0

### START_REASON_BACKUP

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_REASON_BACKUP: Int
```

Process started to run backup.

 Value: 1

### START_REASON_BOOT_COMPLETE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_REASON_BOOT_COMPLETE: Int
```

Process started due to boot complete.

 Value: 2

### START_REASON_BROADCAST

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_REASON_BROADCAST: Int
```

Process started due to broadcast received for any reason not explicitly listed.

 Value: 3

### START_REASON_CONTENT_PROVIDER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_REASON_CONTENT_PROVIDER: Int
```

Process started due to access of ContentProvider for any reason not explicitly listed.

 Value: 4

### START_REASON_JOB

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_REASON_JOB: Int
```

\* Process started to run scheduled job.

 Value: 5

### START_REASON_LAUNCHER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_REASON_LAUNCHER: Int
```

Process started due to click app icon or widget from launcher.

 Value: 6

### START_REASON_LAUNCHER_RECENTS

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_REASON_LAUNCHER_RECENTS: Int
```

Process started from launcher recents.

 Value: 7

### START_REASON_OTHER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_REASON_OTHER: Int
```

Process started not for any of the listed reasons.

 Value: 8

### START_REASON_PUSH

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_REASON_PUSH: Int
```

Process started due to push message.

 Value: 9

### START_REASON_SERVICE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_REASON_SERVICE: Int
```

Process started due to Service started for any reason not explicitly listed..

 Value: 10

### START_REASON_START_ACTIVITY

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_REASON_START_ACTIVITY: Int
```

Process started due to Activity started for any reason not explicitly listed.

 Value: 11

### START_TIMESTAMP_APPLICATION_ONCREATE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_TIMESTAMP_APPLICATION_ONCREATE: Int
```

Clock monotonic timestamp of Application onCreate called.

 Value: 2

### START_TIMESTAMP_BIND_APPLICATION

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_TIMESTAMP_BIND_APPLICATION: Int
```

Clock monotonic timestamp of bindApplication called.

 Value: 3

### START_TIMESTAMP_FIRST_FRAME

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_TIMESTAMP_FIRST_FRAME: Int
```

Clock monotonic timestamp of first frame drawn.

 Value: 4

### START_TIMESTAMP_FORK

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_TIMESTAMP_FORK: Int
```

Clock monotonic timestamp of process fork.

 Value: 1

### START_TIMESTAMP_FULLY_DRAWN

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_TIMESTAMP_FULLY_DRAWN: Int
```

Clock monotonic timestamp of reportFullyDrawn called by application.

 Value: 5

### START_TIMESTAMP_INITIAL_RENDERTHREAD_FRAME

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_TIMESTAMP_INITIAL_RENDERTHREAD_FRAME: Int
```

Clock monotonic timestamp of initial renderthread frame.

 Value: 6

### START_TIMESTAMP_LAUNCH

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_TIMESTAMP_LAUNCH: Int
```

Clock monotonic timestamp of launch started.

 Value: 0

### START_TIMESTAMP_RESERVED_RANGE_DEVELOPER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_TIMESTAMP_RESERVED_RANGE_DEVELOPER: Int
```

The end of the range reserved for developer supplied timestamps.

 Value: 30

### START_TIMESTAMP_RESERVED_RANGE_DEVELOPER_START

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_TIMESTAMP_RESERVED_RANGE_DEVELOPER_START: Int
```

The beginning of the range reserved for developer supplied timestamps.

 Value: 21

### START_TIMESTAMP_RESERVED_RANGE_SYSTEM

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_TIMESTAMP_RESERVED_RANGE_SYSTEM: Int
```

The end of the range, beginning with 0, reserved for system timestamps.

 Value: 20

### START_TIMESTAMP_SOURCE_EVENT

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_TIMESTAMP_SOURCE_EVENT: Int
```

Clock monotonic timestamp of the source event which triggered this start. The timestamp is in the uptimeNanos timebase. Timestamp will only be set when getStartComponent is equal to `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_COMPONENT_ACTIVITY:kotlin.Int`.

 Value: 8

### START_TIMESTAMP_SURFACEFLINGER_COMPOSITION_COMPLETE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_TIMESTAMP_SURFACEFLINGER_COMPOSITION_COMPLETE: Int
```

Clock monotonic timestamp of surfaceflinger composition complete.

 Value: 7

### START_TYPE_COLD

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_TYPE_COLD: Int
```

Process started from scratch.

 Value: 1

### START_TYPE_HOT

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_TYPE_HOT: Int
```

Process brought back to foreground.

 Value: 3

### START_TYPE_UNSET

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_TYPE_UNSET: Int
```

Start type not yet set.

 Value: 0

### START_TYPE_WARM

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_TYPE_WARM: Int
```

Process retained minimally SavedInstanceState.

 Value: 2

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
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
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getDefiningUid

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDefiningUid(): Int
```

Return the defining kernel user identifier, maybe different from getRealUid and getPackageUid, if an external service has the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestService_useAppZygote:kotlin.Int` set to ` true` and was bound with the flag `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_EXTERNAL_SERVICE:kotlin.Int` - in this case, this field here will be the kernel user identifier of the external service provider.

Note: field will be set for any getStartupState value.

### getIntent

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIntent(): Intent?
```

The intent used to launch the application.

Note: Intent is stripped and does not include extras.

Note: field will be set for any getStartupState value.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Intent.html#?` | This value may be `null`. |

### getLaunchMode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLaunchMode(): Int
```

An instruction on how the activity should be launched. There are five modes that work in conjunction with activity flags in Intent objects to determine what should happen when the activity is called upon to handle an intent. Modes: `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#LAUNCH_MODE_STANDARD:kotlin.Int` `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#LAUNCH_MODE_SINGLE_TOP:kotlin.Int` `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#LAUNCH_MODE_SINGLE_INSTANCE:kotlin.Int` `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#LAUNCH_MODE_SINGLE_TASK:kotlin.Int` `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#LAUNCH_MODE_SINGLE_INSTANCE_PER_TASK:kotlin.Int`

Note: field will be set for any getStartupState value.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#LAUNCH_MODE_STANDARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#LAUNCH_MODE_SINGLE_TOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#LAUNCH_MODE_SINGLE_INSTANCE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#LAUNCH_MODE_SINGLE_TASK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#LAUNCH_MODE_SINGLE_INSTANCE_PER_TASK:kotlin.Int` |

### getPackageUid

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPackageUid(): Int
```

Similar to getRealUid, it's the kernel user identifier that is assigned at the package installation time.

Note: field will be set for any getStartupState value.

### getPid

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPid(): Int
```

The process id.

Note: field will be set for any getStartupState value.

### getProcessName

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getProcessName(): String
```

The actual process name it was running with.

Note: field will be set for any getStartupState value.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getRealUid

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRealUid(): Int
```

The kernel user identifier of the process, most of the time the system uses this to do access control checks. It's typically the uid of the package where the component is running from, except the case of isolated process, where this field identifies the kernel user identifier that this process is actually running with, while the getPackageUid identifies the kernel user identifier that is assigned at the package installation time.

Note: field will be set for any getStartupState value.

### getReason

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getReason(): Int
```

The reason code of what triggered the process's start. Start reason provides granular reasoning on why the app is being started. Start reason should not be used for distinguishing between the component the app is being started for as some reasons may overlap with multiple components, see getStartComponent for this functionality instead.

Note: field will be set for any getStartupState value.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_ALARM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_BACKUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_BOOT_COMPLETE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_BROADCAST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_CONTENT_PROVIDER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_JOB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_LAUNCHER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_LAUNCHER_RECENTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_OTHER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_PUSH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_SERVICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_REASON_START_ACTIVITY:kotlin.Int` |

### getStartComponent

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStartComponent(): Int
```

The component type that was being started which triggered the start. Start component should be used to accurately distinguish between the 4 component types: activity, service, broadcast, and content provider. This can be useful for optimizing startup flow by enabling the caller to only load the necessary dependencies for a specific component type. For more granular information on why the app is being started, see getReason.

Note: field will be set for any getStartupState value.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_COMPONENT_ACTIVITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_COMPONENT_BROADCAST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_COMPONENT_CONTENT_PROVIDER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_COMPONENT_SERVICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_COMPONENT_OTHER:kotlin.Int` |

### getStartType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStartType(): Int
```

The state of the app at startup.

Note: field will be set for getStartupState value `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#STARTUP_STATE_FIRST_FRAME_DRAWN:kotlin.Int`. Not guaranteed for other states.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TYPE_UNSET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TYPE_COLD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TYPE_WARM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TYPE_HOT:kotlin.Int` |

### getStartupState

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStartupState(): Int
```

Current state of startup. Can be used to determine whether the object will have additional fields added as it may be queried before all data is collected.

Note: field will always be set and available.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#STARTUP_STATE_STARTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#STARTUP_STATE_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#STARTUP_STATE_FIRST_FRAME_DRAWN:kotlin.Int` |

### getStartupTimestamps

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStartupTimestamps(): MutableMap<Int!, Long!>
```

Various clock monotonic timestamps in nanoseconds throughout the startup process.

Note: different timestamps will be available for different values of getStartupState: (Subsequent rows contain all timestamps of proceding states.) For `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#STARTUP_STATE_STARTED:kotlin.Int`, timestamp `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TIMESTAMP_LAUNCH:kotlin.Int` will be available. For `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#STARTUP_STATE_ERROR:kotlin.Int`, no additional timestamps are guaranteed available. For `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#STARTUP_STATE_FIRST_FRAME_DRAWN:kotlin.Int`, timestamps `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TIMESTAMP_APPLICATION_ONCREATE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TIMESTAMP_BIND_APPLICATION:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TIMESTAMP_FIRST_FRAME:kotlin.Int` will additionally be available. Timestamp `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TIMESTAMP_FULLY_DRAWN:kotlin.Int` is never guaranteed to be available as it is dependant on devloper calling reportFullyDrawn.

Note: The timestamp `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TIMESTAMP_LAUNCH:kotlin.Int` for starts of type `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_COMPONENT_SERVICE:kotlin.Int` may be incorrect in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int` and below.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html!>` | This value cannot be `null`. |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the equals method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the equals method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### wasForceStopped

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun wasForceStopped(): Boolean
```

Informs whether this is the first process launch for an app since it was `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#FLAG_STOPPED:kotlin.Int` for some reason. This allows the app to know if it should re-register for any alarms, jobs and other callbacks that were cleared when the app was force-stopped.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this is the first process launch of the app after having been stopped, `false` otherwise. |

### writeToParcel

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<ApplicationStartInfo!>
```
