Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ActivityManager

```
open class ActivityManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.ActivityManager](https://developer.android.com/reference/kotlin/android/app/ActivityManager#) |

This class gives information about, and interacts with, activities, services, and the containing process.

A number of the methods in this class are for debugging or informational purposes and they should not be used to affect any runtime behavior of your app. These methods are called out as such in the method level documentation.

Most application developers should not have the need to use this class, most of whose methods are for specialized use cases. However, a few methods are more broadly applicable. For instance, `https://developer.android.com/reference/kotlin/android/app/ActivityManager#isLowRamDevice()` enables your app to detect whether it is running on a low-memory device, and behave accordingly. `https://developer.android.com/reference/kotlin/android/app/ActivityManager#clearApplicationUserData()` is for apps with reset-data functionality.

In some special use cases, where an app interacts with its Task stack, the app may use the `https://developer.android.com/reference/kotlin/android/app/ActivityManager.AppTask` and `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RecentTaskInfo` inner classes. However, in general, the methods in this class should be used for testing and debugging purposes only.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/app/ActivityManager.AppTask` The AppTask allows you to manage your own application's tasks. |
| open | `https://developer.android.com/reference/kotlin/android/app/ActivityManager.MemoryInfo` Information you can retrieve about the available memory through `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getMemoryInfo(android.app.ActivityManager.MemoryInfo)`. |
| open | `https://developer.android.com/reference/kotlin/android/app/ActivityManager.ProcessErrorStateInfo` Information you can retrieve about any processes that are in an error condition. |
| open | `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RecentTaskInfo` Information you can retrieve about tasks that the user has most recently started or visited. |
| open | `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo` Information you can retrieve about a running process. |
| open | `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningServiceInfo` Information you can retrieve about a particular Service that is currently running in the system. |
| open | `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningTaskInfo` Information you can retrieve about a particular task that is currently "running" in the system. |
| open | `https://developer.android.com/reference/kotlin/android/app/ActivityManager.TaskDescription` Information you can set and retrieve about the current activity within the recent task list. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#ACTION_REPORT_HEAP_LIMIT:kotlin.String` Action an app can implement to handle reports from `https://developer.android.com/reference/kotlin/android/app/ActivityManager#setWatchHeapLimit(kotlin.Long)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#LOCK_TASK_MODE_LOCKED:kotlin.Int` Full lock task mode is active. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#LOCK_TASK_MODE_NONE:kotlin.Int` Lock task mode is not active. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#LOCK_TASK_MODE_PINNED:kotlin.Int` App pinning mode is active. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#META_HOME_ALTERNATE:kotlin.String` [`<meta-data>`](https://developer.android.com/guide/topics/manifest/meta-data-element.html) name for a 'home' Activity that declares a package that is to be uninstalled in lieu of the declaring one. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#MOVE_TASK_NO_USER_ACTION:kotlin.Int` Flag for `https://developer.android.com/reference/kotlin/android/app/ActivityManager#moveTaskToFront(kotlin.Int,%20kotlin.Int)`: don't count this as a user-instigated action, so the current activity will not receive a hint that the user is leaving. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#MOVE_TASK_WITH_HOME:kotlin.Int` Flag for `https://developer.android.com/reference/kotlin/android/app/ActivityManager#moveTaskToFront(kotlin.Int,%20kotlin.Int)`: also move the "home" activity along with the task, so it is positioned immediately behind the task. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#RECENT_IGNORE_UNAVAILABLE:kotlin.Int` Provides a list that does not contain any recent tasks that currently are not available to the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#RECENT_WITH_EXCLUDED:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getRecentTasks(kotlin.Int,%20kotlin.Int)`: return all tasks, even those that have set their `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_EXCLUDE_FROM_RECENTS:kotlin.Int` flag. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#addAppTask(android.app.Activity,%20android.content.Intent,%20android.app.ActivityManager.TaskDescription,%20android.graphics.Bitmap)(activity: https://developer.android.com/reference/kotlin/android/app/Activity, intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, description: https://developer.android.com/reference/kotlin/android/app/ActivityManager.TaskDescription?, thumbnail: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)` Add a new `https://developer.android.com/reference/kotlin/android/app/ActivityManager.AppTask` for the calling application. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#addApplicationStartInfoCompletionListener(java.util.concurrent.Executor,%20java.util.function.Consumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo!>)` Adds a callback that is notified when the `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo` record of this startup is complete. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#addStartInfoTimestamp(kotlin.Int,%20kotlin.Long)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, timestampNs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Adds an optional developer supplied timestamp to the calling apps most recent `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#appNotResponding(kotlin.String)(reason: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Method for the app to tell system that it's wedged and would like to trigger an ANR. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#clearApplicationUserData()()` Permits an application to erase its own data from disk. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#clearWatchHeapLimit()()` Clear a heap watch limit previously set by `https://developer.android.com/reference/kotlin/android/app/ActivityManager#setWatchHeapLimit(kotlin.Long)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#dumpPackageState(java.io.FileDescriptor,%20kotlin.String)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Perform a system dump of various state associated with the given application package name. |
| open [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)! | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getAppTaskThumbnailSize()()` Return the current design dimensions for `https://developer.android.com/reference/kotlin/android/app/ActivityManager.AppTask` thumbnails, for use with `https://developer.android.com/reference/kotlin/android/app/ActivityManager#addAppTask(android.app.Activity,%20android.content.Intent,%20android.app.ActivityManager.TaskDescription,%20android.graphics.Bitmap)`. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ActivityManager.AppTask](https://developer.android.com/reference/kotlin/android/app/ActivityManager.AppTask)!\>! | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getAppTasks()()` Get the list of tasks associated with the calling application. |
| open [ConfigurationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo.html#)! | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getDeviceConfigurationInfo()()` Get the device configuration attributes. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ApplicationExitInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo)!\> | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getHistoricalProcessExitReasons(kotlin.String,%20kotlin.Int,%20kotlin.Int)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, maxNum: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return a list of `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo` records containing the reasons for the most recent app deaths. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ApplicationStartInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo)!\> | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getHistoricalProcessStartReasons(kotlin.Int)(maxNum: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return a list of `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo` records containing the information about the most recent app startups. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getLargeMemoryClass()()` Return the approximate per-application memory class of the current device when an application is running with a large heap. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getLauncherLargeIconDensity()()` Get the preferred density of icons for the launcher. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getLauncherLargeIconSize()()` Get the preferred launcher icon size. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getLockTaskModeState()()` Return the current state of task locking. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getMemoryClass()()` Return the approximate per-application memory class of the current device. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getMemoryInfo(android.app.ActivityManager.MemoryInfo)(outInfo: https://developer.android.com/reference/kotlin/android/app/ActivityManager.MemoryInfo!)` Return general information about the memory state of the system. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getMyMemoryState(android.app.ActivityManager.RunningAppProcessInfo)(outState: https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo!)` Return global memory state information for the calling process. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Debug.MemoryInfo](https://developer.android.com/reference/kotlin/android/os/Debug.MemoryInfo.html#)!\>! | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getProcessMemoryInfo(kotlin.IntArray)(pids: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!)` Return information about the memory usage of one or more processes. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ActivityManager.ProcessErrorStateInfo](https://developer.android.com/reference/kotlin/android/app/ActivityManager.ProcessErrorStateInfo)!\>! | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getProcessesInErrorState()()` Returns a list of any processes that are currently in an error condition. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ActivityManager.RecentTaskInfo](https://developer.android.com/reference/kotlin/android/app/ActivityManager.RecentTaskInfo)!\>! | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getRecentTasks(kotlin.Int,%20kotlin.Int)(maxNum: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ActivityManager.RunningAppProcessInfo](https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo)!\>! | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getRunningAppProcesses()()` Returns a list of application processes that are running on the device. |
| open [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent)! | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getRunningServiceControlPanel(android.content.ComponentName)(service: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!)` Returns a PendingIntent you can start to show a control panel for the given running service. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ActivityManager.RunningServiceInfo](https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningServiceInfo)!\>! | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getRunningServices(kotlin.Int)(maxNum: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return a list of the services that are currently running. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ActivityManager.RunningTaskInfo](https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningTaskInfo)!\>! | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getRunningTasks(kotlin.Int)(maxNum: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return a list of the tasks that are currently running, with the most recent being first and older ones after in order. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#isActivityStartAllowedOnDisplay(android.content.Context,%20kotlin.Int,%20android.content.Intent)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, displayId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#)` Check if the context is allowed to start an activity on specified display. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#isBackgroundRestricted()()` Query whether the user has enabled background restrictions for this app. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#isInLockTaskMode()()` Return whether currently in lock task mode. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#isLowMemoryKillReportSupported()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#isLowRamDevice()()` Returns true if this is a low-RAM device. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#isRunningInTestHarness()()` Returns "true" if device is running in a test harness. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#isRunningInUserTestHarness()()` Returns "true" if the device is running in Test Harness Mode. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#isUserAMonkey()()` Returns "true" if the user interface is currently being messed with by a [monkey](https://developer.android.com/studio/test/other-testing-tools/monkey). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#killBackgroundProcesses(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Have the system immediately kill all background processes associated with the given package. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#moveTaskToFront(kotlin.Int,%20kotlin.Int)(taskId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Equivalent to calling `https://developer.android.com/reference/kotlin/android/app/ActivityManager#moveTaskToFront(kotlin.Int,%20kotlin.Int,%20android.os.Bundle)` with a null options argument. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#moveTaskToFront(kotlin.Int,%20kotlin.Int,%20android.os.Bundle)(taskId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Ask that the task associated with a given task ID be moved to the front of the stack, so it is now visible to the user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#registerAnrWarningListener(java.util.concurrent.Executor,%20java.util.function.Consumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/app/AnrWarningResult!>)` Registers a listener that is called when the app is close to the ANR timeout. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#removeApplicationStartInfoCompletionListener(java.util.function.Consumer)(listener: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo!>)` Removes the provided callback set by `https://developer.android.com/reference/kotlin/android/app/ActivityManager#addApplicationStartInfoCompletionListener(java.util.concurrent.Executor,%20java.util.function.Consumer)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#restartPackage(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#setProcessStateSummary(kotlin.ByteArray)(state: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?)` Set custom state data for this process. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#setVrThread(kotlin.Int)(tid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Enable more aggressive scheduling for latency-sensitive low-runtime VR threads. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#setWatchHeapLimit(kotlin.Long)(pssSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Request that the system start watching for the calling process to exceed a pss size as given here. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ActivityManager#unregisterAnrWarningListener(java.util.function.Consumer)(listener: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<https://developer.android.com/reference/kotlin/android/app/AnrWarningResult!>)` Unregisters a previously registered ANR warning listener. |

## Constants

### ACTION_REPORT_HEAP_LIMIT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_REPORT_HEAP_LIMIT: String
```

Action an app can implement to handle reports from `https://developer.android.com/reference/kotlin/android/app/ActivityManager#setWatchHeapLimit(kotlin.Long)`. If your package has an activity handling this action, it will be launched with the heap data provided to it the same way as `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SEND:kotlin.String`. Note that to match, the activity must support this action and a MIME type of "\*/\*".

 Value: "android.app.action.REPORT_HEAP_LIMIT"

### LOCK_TASK_MODE_LOCKED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOCK_TASK_MODE_LOCKED: Int
```

Full lock task mode is active.

 Value: 1

### LOCK_TASK_MODE_NONE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOCK_TASK_MODE_NONE: Int
```

Lock task mode is not active.

 Value: 0

### LOCK_TASK_MODE_PINNED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOCK_TASK_MODE_PINNED: Int
```

App pinning mode is active.

 Value: 2

### META_HOME_ALTERNATE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_HOME_ALTERNATE: String
```

[`<meta-data>`](https://developer.android.com/guide/topics/manifest/meta-data-element.html) name for a 'home' Activity that declares a package that is to be uninstalled in lieu of the declaring one. The package named here must be signed with the same certificate as the one declaring the `<meta-data>`.

 Value: "android.app.home.alternate"

### MOVE_TASK_NO_USER_ACTION

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MOVE_TASK_NO_USER_ACTION: Int
```

Flag for `https://developer.android.com/reference/kotlin/android/app/ActivityManager#moveTaskToFront(kotlin.Int,%20kotlin.Int)`: don't count this as a user-instigated action, so the current activity will not receive a hint that the user is leaving.

 Value: 2

### MOVE_TASK_WITH_HOME

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MOVE_TASK_WITH_HOME: Int
```

Flag for `https://developer.android.com/reference/kotlin/android/app/ActivityManager#moveTaskToFront(kotlin.Int,%20kotlin.Int)`: also move the "home" activity along with the task, so it is positioned immediately behind the task. This flag is ignored if the task's windowing mode is `https://developer.android.com/reference/kotlin/android/app/ActivityManager#`.

 Value: 1

### RECENT_IGNORE_UNAVAILABLE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RECENT_IGNORE_UNAVAILABLE: Int
```

Provides a list that does not contain any recent tasks that currently are not available to the user.

 Value: 2

### RECENT_WITH_EXCLUDED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RECENT_WITH_EXCLUDED: Int
```

Flag for use with `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getRecentTasks(kotlin.Int,%20kotlin.Int)`: return all tasks, even those that have set their `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_EXCLUDE_FROM_RECENTS:kotlin.Int` flag.

 Value: 1

## Public methods

### addAppTask

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addAppTask(
    activity: Activity, 
    intent: Intent, 
    description: ActivityManager.TaskDescription?, 
    thumbnail: Bitmap
): Int
```

Add a new `https://developer.android.com/reference/kotlin/android/app/ActivityManager.AppTask` for the calling application. This will create a new recents entry that is added to the **end** of all existing recents.

| Parameters ||
|---|---|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity): The activity that is adding the entry. This is used to help determine the context that the new recents entry will be in. This value cannot be `null`. |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#): The Intent that describes the recents entry. This is the same Intent that you would have used to launch the activity for it. In generally you will want to set both `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_DOCUMENT:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_RETAIN_IN_RECENTS:kotlin.Int`; the latter is required since this recents entry will exist without an activity, so it doesn't make sense to not retain it when its activity disappears. The given Intent here also must have an explicit ComponentName set on it. This value cannot be `null`. |
| `description` | [ActivityManager.TaskDescription](https://developer.android.com/reference/kotlin/android/app/ActivityManager.TaskDescription)?: Optional additional description information. This value may be `null`. |
| `thumbnail` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#): Thumbnail to use for the recents entry. Should be the size given by `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getAppTaskThumbnailSize()`. If the bitmap is not that exact size, it will be recreated in your process, probably in a way you don't like, before the recents entry is added. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns the task id of the newly added app task, or -1 if the add failed. The most likely cause of failure is that there is no more room for more tasks for your app. |

### addApplicationStartInfoCompletionListener

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addApplicationStartInfoCompletionListener(
    executor: Executor, 
    listener: Consumer<ApplicationStartInfo!>
): Unit
```

Adds a callback that is notified when the `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo` record of this startup is complete. The startup is considered complete when the first frame is drawn. The callback doesn't wait for `https://developer.android.com/reference/kotlin/android/app/Activity#reportFullyDrawn()` to occur. Retrieve a copy of `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo` after `https://developer.android.com/reference/kotlin/android/app/Activity#reportFullyDrawn()` is called (using this callback or getHistoricalProcessStartReasons) if you need the `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TIMESTAMP_FULLY_DRAWN:kotlin.Int` timestamp. If the current start record has already been completed (that is, the process is not currently starting), the callback will be invoked immediately on the specified executor with the previously completed `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo` record. Callback will be called at most once and removed automatically after being triggered.

Note: callback is asynchronous and should be made from a background thread.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor on which the listener should be called. This value cannot be `null`. |
| `listener` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [ApplicationStartInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo)!\>: Callback to be called when collection of `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo` is complete. Will replace existing listener if one is already attached. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if executor or listener are null. |

### addStartInfoTimestamp

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addStartInfoTimestamp(
    key: Int, 
    timestampNs: Long
): Unit
```

Adds an optional developer supplied timestamp to the calling apps most recent `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo`. This is in addition to system recorded timestamps.

Note: any timestamps added after `https://developer.android.com/reference/kotlin/android/app/Activity#reportFullyDrawn()` is called are discarded.

Note: will overwrite existing timestamp if called with same key.

| Parameters ||
|---|---|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Unique key for timestamp. Must be greater than `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TIMESTAMP_RESERVED_RANGE_SYSTEM:kotlin.Int` and less than or equal to `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TIMESTAMP_RESERVED_RANGE_DEVELOPER:kotlin.Int`. Will thow `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` if not in range. Value is between `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TIMESTAMP_RESERVED_RANGE_DEVELOPER_START:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo#START_TIMESTAMP_RESERVED_RANGE_DEVELOPER:kotlin.Int` inclusive |
| `timestampNs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Clock monotonic time in nanoseconds of event to be recorded. |

### appNotResponding

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun appNotResponding(reason: String): Unit
```

Method for the app to tell system that it's wedged and would like to trigger an ANR.

| Parameters ||
|---|---|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The description of that what happened. This value cannot be `null`. |

### clearApplicationUserData

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearApplicationUserData(): Boolean
```

Permits an application to erase its own data from disk. This is equivalent to the user choosing to clear the app's data from within the device settings UI. It erases all dynamic data associated with the app -- its private data and data in its private area on external storage -- but does not remove the installed application itself, nor any OBB files. It also revokes all runtime permissions that the app has acquired, clears all notifications and removes all Uri grants related to this application.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the application successfully requested that the application's data be erased; `false` otherwise. |

### clearWatchHeapLimit

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearWatchHeapLimit(): Unit
```

Clear a heap watch limit previously set by `https://developer.android.com/reference/kotlin/android/app/ActivityManager#setWatchHeapLimit(kotlin.Long)`.

### dumpPackageState

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dumpPackageState(
    fd: FileDescriptor!, 
    packageName: String!
): Unit
```

Perform a system dump of various state associated with the given application package name. This call blocks while the dump is being performed, so should not be done on a UI thread. The data will be written to the given file descriptor as text. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#DUMP:kotlin.String`

| Parameters ||
|---|---|
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!: The file descriptor that the dump should be written to. The file descriptor is *not* closed by this function; the caller continues to own it. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the package that is to be dumped. |

### getAppTaskThumbnailSize

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAppTaskThumbnailSize(): Size!
```

Return the current design dimensions for `https://developer.android.com/reference/kotlin/android/app/ActivityManager.AppTask` thumbnails, for use with `https://developer.android.com/reference/kotlin/android/app/ActivityManager#addAppTask(android.app.Activity,%20android.content.Intent,%20android.app.ActivityManager.TaskDescription,%20android.graphics.Bitmap)`.

### getAppTasks

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAppTasks(): MutableList<ActivityManager.AppTask!>!
```

Get the list of tasks associated with the calling application.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/ActivityManager.AppTask!>!` | The list of tasks associated with the application making this call. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | |

### getDeviceConfigurationInfo

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDeviceConfigurationInfo(): ConfigurationInfo!
```

Get the device configuration attributes.

### getHistoricalProcessExitReasons

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHistoricalProcessExitReasons(
    packageName: String?, 
    pid: Int, 
    maxNum: Int
): MutableList<ApplicationExitInfo!>
```

Return a list of `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo` records containing the reasons for the most recent app deaths.

Note: System stores this historical information in a ring buffer and only the most recent records will be returned.

Note: In the case that this application was bound to an external service with flag `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_EXTERNAL_SERVICE:kotlin.Int`, the process of that external service will be included in this package's exit info.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: Optional, a null value means match all packages belonging to the caller's UID. If this package belongs to another UID, you must hold `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#DUMP:kotlin.String` in order to retrieve it. |
| `pid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A process ID that used to belong to this package but died later; a value of 0 means to ignore this parameter and return all matching records. Value is 0 or greater |
| `maxNum` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The maximum number of results to be returned; a value of 0 means to ignore this parameter and return all matching records. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo!>` | a list of `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo` records matching the criteria, sorted in the order from most recent to least recent. This value cannot be `null`. |

### getHistoricalProcessStartReasons

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHistoricalProcessStartReasons(maxNum: Int): MutableList<ApplicationStartInfo!>
```

Return a list of `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo` records containing the information about the most recent app startups. Records accessed using this path might include "incomplete" records such as in-progress app starts. Accessing in-progress starts using this method lets you access start information early to better optimize your startup path.

Note: System stores this historical information in a ring buffer and only the most recent records will be returned.

| Parameters ||
|---|---|
| `maxNum` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The maximum number of results to be returned; a value of 0 means to ignore this parameter and return all matching records. If fewer records exist, all existing records will be returned. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo!>` | a list of `https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo` records matching the criteria, sorted in the order from most recent to least recent. This value cannot be `null`. |

### getLargeMemoryClass

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLargeMemoryClass(): Int
```

Return the approximate per-application memory class of the current device when an application is running with a large heap. This is the space available for memory-intensive applications; most applications should not need this amount of memory, and should instead stay with the `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getMemoryClass()` limit. The returned value is in megabytes. This may be the same size as `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getMemoryClass()` on memory constrained devices, or it may be significantly larger on devices with a large amount of available RAM.

This is the size of the application's Dalvik heap if it has specified `android:largeHeap="true"` in its manifest.

### getLauncherLargeIconDensity

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLauncherLargeIconDensity(): Int
```

Get the preferred density of icons for the launcher. This is used when custom drawables are created (e.g., for shortcuts).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | density in terms of DPI |

### getLauncherLargeIconSize

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLauncherLargeIconSize(): Int
```

Get the preferred launcher icon size. This is used when custom drawables are created (e.g., for shortcuts).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | dimensions of square icons in terms of pixels |

### getLockTaskModeState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLockTaskModeState(): Int
```

Return the current state of task locking. The three possible outcomes are `https://developer.android.com/reference/kotlin/android/app/ActivityManager#LOCK_TASK_MODE_NONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/ActivityManager#LOCK_TASK_MODE_LOCKED:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/app/ActivityManager#LOCK_TASK_MODE_PINNED:kotlin.Int`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Activity#startLockTask()`

### getMemoryClass

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMemoryClass(): Int
```

Return the approximate per-application memory class of the current device. This gives you an idea of how hard a memory limit you should impose on your application to let the overall system work best. The returned value is in megabytes; the baseline Android memory class is 16 (which happens to be the Java heap limit of those devices); some devices with more memory may return 24 or even higher numbers.

### getMemoryInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMemoryInfo(outInfo: ActivityManager.MemoryInfo!): Unit
```

Return general information about the memory state of the system. This can be used to help decide how to manage your own memory, though note that polling is not recommended and `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)` is the preferred way to do this. Also see `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getMyMemoryState(android.app.ActivityManager.RunningAppProcessInfo)` for how to retrieve the current trim level of your process as needed, which gives a better hint for how to manage its memory.

### getMyMemoryState

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getMyMemoryState(outState: ActivityManager.RunningAppProcessInfo!): Unit
```

Return global memory state information for the calling process. This does not fill in all fields of the `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo`. The only fields that will be filled in are `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo#pid:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo#uid:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo#lastTrimLevel:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo#importance:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo#lru:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo#importanceReasonCode:kotlin.Int`.

### getProcessMemoryInfo

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getProcessMemoryInfo(pids: IntArray!): Array<Debug.MemoryInfo!>!
```

Return information about the memory usage of one or more processes.

**Note: this method is only intended for debugging or building a user-facing process management UI.**

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int`, for regular apps this method will only return information about the memory info for the processes running as the caller's uid; no other process memory info is available and will be zero. Also of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` the sample rate allowed by this API is significantly limited, if called faster the limit you will receive the same data as the previous call.

| Parameters ||
|---|---|
| `pids` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: The pids of the processes whose memory usage is to be retrieved. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/os/Debug.MemoryInfo.html#!>!` | Returns an array of memory information, one for each requested pid. |

### getProcessesInErrorState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getProcessesInErrorState(): MutableList<ActivityManager.ProcessErrorStateInfo!>!
```

Returns a list of any processes that are currently in an error condition. The result will be null if all processes are running properly at this time.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, for regular apps this method will only return `https://developer.android.com/reference/kotlin/android/app/ActivityManager.ProcessErrorStateInfo` records for the processes running as the caller's uid, unless the caller has the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#DUMP:kotlin.String`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/ActivityManager.ProcessErrorStateInfo!>!` | Returns a list of `https://developer.android.com/reference/kotlin/android/app/ActivityManager.ProcessErrorStateInfo` records, or null if there are no current error conditions (it will not return an empty list). This list ordering is not specified. |

### getRecentTasks

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRecentTasks(
    maxNum: Int, 
    flags: Int
): MutableList<ActivityManager.RecentTaskInfo!>!
```

**Deprecated:** *As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int`, this method is no longer available to third party applications: the introduction of document-centric recents means it can leak personal information to the caller. For backwards compatibility, it will still return a small subset of its data: at least the caller's own tasks (though see `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getAppTasks()` for the correct supported way to retrieve that information), and possibly some other tasks such as home that are known to not be sensitive.*

<br />

Return a list of the tasks that the user has recently launched, with the most recent being first and older ones after in order.

**Note: this method is only intended for debugging and presenting task management user interfaces** . This should never be used for core logic in an application, such as deciding between different behaviors based on the information found here. Such uses are *not* supported, and will likely break in the future. For example, if multiple applications can be actively running at the same time, assumptions made about the meaning of the data here for purposes of control flow will be incorrect.

| Parameters ||
|---|---|
| `maxNum` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The maximum number of entries to return in the list. The actual number returned may be smaller, depending on how many tasks the user has started and the maximum number the system can remember. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Information about what to return. May be any combination of `https://developer.android.com/reference/kotlin/android/app/ActivityManager#RECENT_WITH_EXCLUDED:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/app/ActivityManager#RECENT_IGNORE_UNAVAILABLE:kotlin.Int`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/ActivityManager.RecentTaskInfo!>!` | Returns a list of RecentTaskInfo records describing each of the recent tasks. |

### getRunningAppProcesses

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRunningAppProcesses(): MutableList<ActivityManager.RunningAppProcessInfo!>!
```

Returns a list of application processes that are running on the device.

**Note: this method is only intended for debugging or building a user-facing process management UI.**

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo!>!` | Returns a list of RunningAppProcessInfo records, or null if there are no running processes (it will not return an empty list). This list ordering is not specified. |

### getRunningServiceControlPanel

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRunningServiceControlPanel(service: ComponentName!): PendingIntent!
```

Returns a PendingIntent you can start to show a control panel for the given running service. If the service does not have a control panel, null is returned.

### getRunningServices

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRunningServices(maxNum: Int): MutableList<ActivityManager.RunningServiceInfo!>!
```

**Deprecated:** *As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int`, this method is no longer available to third party applications. For backwards compatibility, it will still return the caller's own services.*

Return a list of the services that are currently running.

**Note: this method is only intended for debugging or implementing service management type user interfaces.**

| Parameters ||
|---|---|
| `maxNum` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The maximum number of entries to return in the list. The actual number returned may be smaller, depending on how many services are running. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningServiceInfo!>!` | Returns a list of RunningServiceInfo records describing each of the running tasks. |

### getRunningTasks

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRunningTasks(maxNum: Int): MutableList<ActivityManager.RunningTaskInfo!>!
```

**Deprecated:** *As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int`, this method is no longer available to third party applications: the introduction of document-centric recents means it can leak person information to the caller. For backwards compatibility, it will still return a small subset of its data: at least the caller's own tasks, and possibly some other tasks such as home that are known to not be sensitive.*

Return a list of the tasks that are currently running, with the most recent being first and older ones after in order. Note that "running" does not mean any of the task's code is currently loaded or activity -- the task may have been frozen by the system, so that it can be restarted in its previous state when next brought to the foreground.

**Note: this method is only intended for debugging and presenting task management user interfaces** . This should never be used for core logic in an application, such as deciding between different behaviors based on the information found here. Such uses are *not* supported, and will likely break in the future. For example, if multiple applications can be actively running at the same time, assumptions made about the meaning of the data here for purposes of control flow will be incorrect.

| Parameters ||
|---|---|
| `maxNum` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The maximum number of entries to return in the list. The actual number returned may be smaller, depending on how many tasks the user has started. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningTaskInfo!>!` | Returns a list of RunningTaskInfo records describing each of the running tasks. |

### isActivityStartAllowedOnDisplay

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isActivityStartAllowedOnDisplay(
    context: Context, 
    displayId: Int, 
    intent: Intent
): Boolean
```

Check if the context is allowed to start an activity on specified display. Some launch restrictions may apply to secondary displays that are private, virtual, or owned by the system, in which case an activity start may throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. Call this method prior to starting an activity on a secondary display to check if the current context has access to it.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): Source context, from which an activity will be started. This value cannot be `null`. |
| `displayId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Target display id. |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#): Intent used to launch an activity. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if a call to start an activity on the target display is allowed for the provided context and no `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown, `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActivityOptions#setLaunchDisplayId(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/Display.html#FLAG_PRIVATE:kotlin.Int`

### isBackgroundRestricted

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isBackgroundRestricted(): Boolean
```

Query whether the user has enabled background restrictions for this app.

The user may chose to do this, if they see that an app is consuming an unreasonable amount of battery while in the background.

If true, any work that the app tries to do will be aggressively restricted while it is in the background. At a minimum, jobs and alarms will not execute and foreground services cannot be started unless an app activity is in the foreground.

**Note that these restrictions stay in effect even when the device is charging.**

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if user has enforced background restrictions for this app, false otherwise. |

### isInLockTaskMode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isInLockTaskMode(): Boolean
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getLockTaskModeState()` instead.*

Return whether currently in lock task mode. When in this mode no new tasks can be created or switched to.
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/Activity#startLockTask()`

### isLowMemoryKillReportSupported

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isLowMemoryKillReportSupported(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether or not the low memory kill will be reported in `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getHistoricalProcessExitReasons(kotlin.String,%20kotlin.Int,%20kotlin.Int)`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_LOW_MEMORY:kotlin.Int`

### isLowRamDevice

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isLowRamDevice(): Boolean
```

Returns true if this is a low-RAM device. Exactly whether a device is low-RAM is ultimately up to the device configuration, but currently it generally means something with 1GB or less of RAM. This is mostly intended to be used by apps to determine whether they should turn off certain features that require more RAM.

### isRunningInTestHarness

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isRunningInTestHarness(): Boolean
```

**Deprecated:** *this method is false for all user builds. Users looking to check if their device is running in a device farm should see `https://developer.android.com/reference/kotlin/android/app/ActivityManager#isRunningInUserTestHarness()`.*

Returns "true" if device is running in a test harness.

### isRunningInUserTestHarness

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isRunningInUserTestHarness(): Boolean
```

Returns "true" if the device is running in Test Harness Mode.

Test Harness Mode is a feature that allows devices to run without human interaction in a device farm/testing harness (such as Firebase Test Lab). You should check this method if you want your app to behave differently when running in a test harness to skip setup screens that would impede UI testing. e.g. a keyboard application that has a full screen setup page for the first time it is launched.

Note that you should *not* use this to determine whether or not your app is running an instrumentation test, as it is not set for a standard device running a test.

### isUserAMonkey

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isUserAMonkey(): Boolean
```

Returns "true" if the user interface is currently being messed with by a [monkey](https://developer.android.com/studio/test/other-testing-tools/monkey).

### killBackgroundProcesses

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun killBackgroundProcesses(packageName: String!): Unit
```

Have the system immediately kill all background processes associated with the given package. This is the same as the kernel killing those processes to reclaim memory; the system will take care of restarting these processes in the future as needed.

On devices that run Android 14 or higher, third party applications can only use this API to kill their own processes.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#KILL_BACKGROUND_PROCESSES:kotlin.String`

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the package whose processes are to be killed. |

### moveTaskToFront

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun moveTaskToFront(
    taskId: Int, 
    flags: Int
): Unit
```

Equivalent to calling `https://developer.android.com/reference/kotlin/android/app/ActivityManager#moveTaskToFront(kotlin.Int,%20kotlin.Int,%20android.os.Bundle)` with a null options argument. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REORDER_TASKS:kotlin.String`

| Parameters ||
|---|---|
| `taskId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The identifier of the task to be moved, as found in `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningTaskInfo` or `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RecentTaskInfo`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional operational flags. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/ActivityManager#MOVE_TASK_WITH_HOME:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityManager#MOVE_TASK_NO_USER_ACTION:kotlin.Int` |

### moveTaskToFront

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun moveTaskToFront(
    taskId: Int, 
    flags: Int, 
    options: Bundle!
): Unit
```

Ask that the task associated with a given task ID be moved to the front of the stack, so it is now visible to the user. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#REORDER_TASKS:kotlin.String`

| Parameters ||
|---|---|
| `taskId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The identifier of the task to be moved, as found in `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningTaskInfo` or `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RecentTaskInfo`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional operational flags. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/ActivityManager#MOVE_TASK_WITH_HOME:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityManager#MOVE_TASK_NO_USER_ACTION:kotlin.Int` |
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: Additional options for the operation, either null or as per `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent,%20android.os.Bundle)`. |

### registerAnrWarningListener

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerAnrWarningListener(
    executor: Executor, 
    listener: Consumer<AnrWarningResult!>
): Unit
```

Registers a listener that is called when the app is close to the ANR timeout.

This is intended to give the app a chance to collect and store any additional information they may want to gather at this time, or take any pre-ANR actions. Note that these listeners are called at best-effort, and may not be successfully called (or be provided time to execute) before the ANR occurs and the app is killed.

If the app registers multiple distinct listeners, all registered listeners will be notified on the potential ANR condition. The order in which listeners are notified is not guaranteed.

The app can unregister the listener using `https://developer.android.com/reference/kotlin/android/app/ActivityManager#unregisterAnrWarningListener(java.util.function.Consumer)`.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor on which listener will be invoked. This should not be the application's main thread. This value cannot be `null`. |
| `listener` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [AnrWarningResult](https://developer.android.com/reference/kotlin/android/app/AnrWarningResult)!\>: The listener to be triggered on the ANR warning condition. This value cannot be `null`. |

### removeApplicationStartInfoCompletionListener

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeApplicationStartInfoCompletionListener(listener: Consumer<ApplicationStartInfo!>): Unit
```

Removes the provided callback set by `https://developer.android.com/reference/kotlin/android/app/ActivityManager#addApplicationStartInfoCompletionListener(java.util.concurrent.Executor,%20java.util.function.Consumer)`.

| Parameters ||
|---|---|
| `listener` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [ApplicationStartInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo)!\>: This value cannot be `null`. |

### restartPackage

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun restartPackage(packageName: String!): Unit
```

**Deprecated:** *This is now just a wrapper for `https://developer.android.com/reference/kotlin/android/app/ActivityManager#killBackgroundProcesses(kotlin.String)`; the previous behavior here is no longer available to applications because it allows them to break other applications by removing their alarms, stopping their services, etc.*

### setProcessStateSummary

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setProcessStateSummary(state: ByteArray?): Unit
```

Set custom state data for this process. It will be included in the record of `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo` on the death of the current calling process; the new process of the app can retrieve this state data by calling `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getProcessStateSummary()` on the record returned by `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getHistoricalProcessExitReasons(kotlin.String,%20kotlin.Int,%20kotlin.Int)`.

This would be useful for the calling app to save its stateful data: if it's killed later for any reason, the new process of the app can know what the previous process of the app was doing. For instance, you could use this to encode the current level in a game, or a set of features/experiments that were enabled. Later you could analyze under what circumstances the app tends to crash or use too much memory. However, it's not suggested to rely on this to restore the applications previous UI state or so, it's only meant for analyzing application healthy status.

System might decide to throttle the calls to this API; so call this API in a reasonable manner, excessive calls to this API could result a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#`.

| Parameters ||
|---|---|
| `state` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: The state data. To be advised, **DO NOT** include sensitive information/data (PII, SPII, or other sensitive user data) here. Maximum length is 128 bytes. This value may be `null`. |

### setVrThread

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun setVrThread(tid: Int): Unit
```

Enable more aggressive scheduling for latency-sensitive low-runtime VR threads. Only one thread can be a VR thread in a process at a time, and that thread may be subject to restrictions on the amount of time it can run. If persistent VR mode is set, whatever thread has been granted aggressive scheduling via this method will return to normal operation, and calling this method will do nothing while persistent VR mode is enabled. To reset the VR thread for an application, a tid of 0 can be passed.

| Parameters ||
|---|---|
| `tid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): tid of the VR thread |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/Process.html#myTid()`

### setWatchHeapLimit

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWatchHeapLimit(pssSize: Long): Unit
```

Request that the system start watching for the calling process to exceed a pss size as given here. Once called, the system will look for any occasions where it sees the associated process with a larger pss size and, when this happens, automatically pull a heap dump from it and allow the user to share the data. Note that this request continues running even if the process is killed and restarted. To remove the watch, use `https://developer.android.com/reference/kotlin/android/app/ActivityManager#clearWatchHeapLimit()`.

This API only works if the calling process has been marked as `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#FLAG_DEBUGGABLE:kotlin.Int` or this is running on a debuggable (userdebug or eng) build.

Callers can optionally implement `https://developer.android.com/reference/kotlin/android/app/ActivityManager#ACTION_REPORT_HEAP_LIMIT:kotlin.String` to directly handle heap limit reports themselves.

| Parameters ||
|---|---|
| `pssSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The size in bytes to set the limit at. |

### unregisterAnrWarningListener

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterAnrWarningListener(listener: Consumer<AnrWarningResult!>): Unit
```

Unregisters a previously registered ANR warning listener.

| Parameters ||
|---|---|
| `listener` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [AnrWarningResult](https://developer.android.com/reference/kotlin/android/app/AnrWarningResult)!\>: The listener to unregister. This must be the same object that was previously passed to `https://developer.android.com/reference/kotlin/android/app/ActivityManager#registerAnrWarningListener(java.util.concurrent.Executor,%20java.util.function.Consumer)`. This value cannot be `null`. |
