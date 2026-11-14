Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Process

```
open class Process
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.os.Process](https://developer.android.com/reference/kotlin/android/os/Process#) |

Tools for managing OS processes.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#BLUETOOTH_UID:kotlin.Int` Defines the UID/GID for the Bluetooth service process. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#FIRST_APPLICATION_UID:kotlin.Int` Defines the start of a range of UIDs (and GIDs), going from this number to `https://developer.android.com/reference/kotlin/android/os/Process#LAST_APPLICATION_UID:kotlin.Int` that are reserved for assigning to applications. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#INVALID_PID:kotlin.Int` An invalid PID value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#INVALID_UID:kotlin.Int` An invalid UID value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#LAST_APPLICATION_UID:kotlin.Int` Last of application-specific UIDs starting at `https://developer.android.com/reference/kotlin/android/os/Process#FIRST_APPLICATION_UID:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#PHONE_UID:kotlin.Int` Defines the UID/GID under which the telephony code runs. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#ROOT_UID:kotlin.Int` Defines the root UID. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#SHELL_UID:kotlin.Int` Defines the UID/GID for the user shell. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#SIGNAL_KILL:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#SIGNAL_QUIT:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#SIGNAL_USR1:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#SYSTEM_UID:kotlin.Int` Defines the UID/GID under which system code runs. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#THREAD_PRIORITY_AUDIO:kotlin.Int` Standard priority of audio threads. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#THREAD_PRIORITY_BACKGROUND:kotlin.Int` Standard priority background threads. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#THREAD_PRIORITY_DEFAULT:kotlin.Int` Standard priority of application threads. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#THREAD_PRIORITY_DISPLAY:kotlin.Int` Standard priority of system display threads, involved in updating the user interface. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#THREAD_PRIORITY_FOREGROUND:kotlin.Int` Standard priority of threads that are currently running a user interface that the user is interacting with. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#THREAD_PRIORITY_LESS_FAVORABLE:kotlin.Int` Minimum increment to make a priority less favorable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#THREAD_PRIORITY_LOWEST:kotlin.Int` Lowest available thread priority. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#THREAD_PRIORITY_MORE_FAVORABLE:kotlin.Int` Minimum increment to make a priority more favorable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#THREAD_PRIORITY_URGENT_AUDIO:kotlin.Int` Standard priority of the most important audio threads. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#THREAD_PRIORITY_URGENT_DISPLAY:kotlin.Int` Standard priority of the most important display threads, for compositing the screen and retrieving input events. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#THREAD_PRIORITY_VIDEO:kotlin.Int` Standard priority of video threads. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#WIFI_UID:kotlin.Int` Defines the UID/GID for the WIFI native processes like wificond, supplicant, hostapd, vendor HAL, etc. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Process#Process()()` <br /> |

| Public methods ||
|---|---|
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#areUidsForSameApplication(kotlin.Int,%20kotlin.Int)(uid1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns true if the two UIDs belong to the same application, taking mathematically mapped UIDs (such as Private Compute Core sandbox) into account. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#getAppUidForPrivateComputeCoreUid(kotlin.Int)(uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the app UID corresponding to a Private Compute Core UID. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#getAppUidForSdkSandboxUid(kotlin.Int)(uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the app uid corresponding to an sdk sandbox uid. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#getElapsedCpuTime()()` Returns elapsed milliseconds of the time this process has run. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Process#getExclusiveCores()()` On some devices, the foreground process may have one or more CPU cores exclusively reserved for it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#getGidForName(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the GID assigned to a particular user name, or -1 if there is none. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#getPrivateComputeCoreUidForAppUid(kotlin.Int)(uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the Private Compute Core UID corresponding to an app UID. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#getSdkSandboxUidForAppUid(kotlin.Int)(uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the sdk sandbox uid corresponding to an app uid. |
| open static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#getStartElapsedRealtime()()` Return the `https://developer.android.com/reference/kotlin/android/os/SystemClock#elapsedRealtime()` at which this process was started, but before any of the application code was executed. |
| open static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#getStartRequestedElapsedRealtime()()` Return the `https://developer.android.com/reference/kotlin/android/os/SystemClock#elapsedRealtime()` at which the system was about to start this process. |
| open static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#getStartRequestedUptimeMillis()()` Return the `https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeMillis()` at which the system was about to start this process. |
| open static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#getStartUptimeMillis()()` Return the `https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeMillis()` at which this process was started, but before any of the application code was executed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#getThreadPriority(kotlin.Int)(tid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the current priority of a thread, based on Linux priorities. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#getUidForName(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the UID assigned to a particular user name, or -1 if there is none. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#is64Bit()()` Returns true if the current process is a 64-bit runtime. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#isApplicationUid(kotlin.Int)(uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns whether the given uid belongs to an application. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#isIsolated()()` Returns whether the current process is in an isolated sandbox. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#isIsolatedUid(kotlin.Int)(uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns whether the process with the given `uid` is an isolated sandbox. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#isPrivateComputeCoreUid(kotlin.Int)(uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns whether the provided UID belongs to components running in a Private Compute Core sandbox process. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#isSdkSandbox()()` Returns whether the current process is a sdk sandbox process. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#isSdkSandboxUid(kotlin.Int)(uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns whether the provided UID belongs to an sdk sandbox process |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#killProcess(kotlin.Int)(pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Kill the process with the given PID. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#myPid()()` Returns the identifier of this process, which can be used with `https://developer.android.com/reference/kotlin/android/os/Process#killProcess(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/os/Process#sendSignal(kotlin.Int,%20kotlin.Int)`. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#myProcessName()()` Return the name of this process. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#myTid()()` Returns the identifier of the calling thread, which be used with `https://developer.android.com/reference/kotlin/android/os/Process#setThreadPriority(kotlin.Int,%20kotlin.Int)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#myUid()()` Returns the identifier of this process's uid. |
| open static [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle)! | `https://developer.android.com/reference/kotlin/android/os/Process#myUserHandle()()` Returns this process's user handle. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#sendSignal(kotlin.Int,%20kotlin.Int)(pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, signal: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Send a signal to the given process. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#setThreadPriority(kotlin.Int)(priority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the priority of the calling thread, based on Linux niceness priorities. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#setThreadPriority(kotlin.Int,%20kotlin.Int)(tid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, priority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the OS priority of a thread, using Linux niceness priorities. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/Process#supportsProcesses()()` Determine whether the current environment supports multiple processes. |

## Constants

### BLUETOOTH_UID

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BLUETOOTH_UID: Int
```

Defines the UID/GID for the Bluetooth service process.

 Value: 1002

### FIRST_APPLICATION_UID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FIRST_APPLICATION_UID: Int
```

Defines the start of a range of UIDs (and GIDs), going from this number to `https://developer.android.com/reference/kotlin/android/os/Process#LAST_APPLICATION_UID:kotlin.Int` that are reserved for assigning to applications.

 Value: 10000

### INVALID_PID

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INVALID_PID: Int
```

An invalid PID value.

 Value: -1

### INVALID_UID

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INVALID_UID: Int
```

An invalid UID value.

 Value: -1

### LAST_APPLICATION_UID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LAST_APPLICATION_UID: Int
```

Last of application-specific UIDs starting at `https://developer.android.com/reference/kotlin/android/os/Process#FIRST_APPLICATION_UID:kotlin.Int`.

 Value: 19999

### PHONE_UID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PHONE_UID: Int
```

Defines the UID/GID under which the telephony code runs.

 Value: 1001

### ROOT_UID

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROOT_UID: Int
```

Defines the root UID.

 Value: 0

### SHELL_UID

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SHELL_UID: Int
```

Defines the UID/GID for the user shell.

 Value: 2000

### SIGNAL_KILL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNAL_KILL: Int
```

 Value: 9

### SIGNAL_QUIT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNAL_QUIT: Int
```

 Value: 3

### SIGNAL_USR1

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNAL_USR1: Int
```

 Value: 10

### SYSTEM_UID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYSTEM_UID: Int
```

Defines the UID/GID under which system code runs.

 Value: 1000

### THREAD_PRIORITY_AUDIO

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THREAD_PRIORITY_AUDIO: Int
```

Standard priority of audio threads. Applications should not normally change to this priority. Use with `https://developer.android.com/reference/kotlin/android/os/Process#setThreadPriority(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/os/Process#setThreadPriority(kotlin.Int,%20kotlin.Int)`, **not** with the normal `https://developer.android.com/reference/kotlin/java/lang/Thread.html#` class.

 Value: -16

### THREAD_PRIORITY_BACKGROUND

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THREAD_PRIORITY_BACKGROUND: Int
```

Standard priority background threads. This gives your thread a significantly lower than normal priority, so that it will have less chance of impacting the responsiveness of the user interface. Use with `https://developer.android.com/reference/kotlin/android/os/Process#setThreadPriority(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/os/Process#setThreadPriority(kotlin.Int,%20kotlin.Int)`, **not** with the normal `https://developer.android.com/reference/kotlin/java/lang/Thread.html#` class.

 Value: 10

### THREAD_PRIORITY_DEFAULT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THREAD_PRIORITY_DEFAULT: Int
```

Standard priority of application threads. Use with `https://developer.android.com/reference/kotlin/android/os/Process#setThreadPriority(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/os/Process#setThreadPriority(kotlin.Int,%20kotlin.Int)`, **not** with the normal `https://developer.android.com/reference/kotlin/java/lang/Thread.html#` class.

 Value: 0

### THREAD_PRIORITY_DISPLAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THREAD_PRIORITY_DISPLAY: Int
```

Standard priority of system display threads, involved in updating the user interface. Use with `https://developer.android.com/reference/kotlin/android/os/Process#setThreadPriority(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/os/Process#setThreadPriority(kotlin.Int,%20kotlin.Int)`, **not** with the normal `https://developer.android.com/reference/kotlin/java/lang/Thread.html#` class.

 Value: -4

### THREAD_PRIORITY_FOREGROUND

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THREAD_PRIORITY_FOREGROUND: Int
```

Standard priority of threads that are currently running a user interface that the user is interacting with. Applications do not normally change to this priority; the system will automatically adjust your application threads as the user moves through the UI. Use with `https://developer.android.com/reference/kotlin/android/os/Process#setThreadPriority(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/os/Process#setThreadPriority(kotlin.Int,%20kotlin.Int)`, **not** with the normal `https://developer.android.com/reference/kotlin/java/lang/Thread.html#` class.

 Value: -2

### THREAD_PRIORITY_LESS_FAVORABLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THREAD_PRIORITY_LESS_FAVORABLE: Int
```

Minimum increment to make a priority less favorable.

 Value: 1

### THREAD_PRIORITY_LOWEST

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THREAD_PRIORITY_LOWEST: Int
```

Lowest available thread priority. Only for those who really, really don't want to run if anything else is happening. Use with `https://developer.android.com/reference/kotlin/android/os/Process#setThreadPriority(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/os/Process#setThreadPriority(kotlin.Int,%20kotlin.Int)`, **not** with the normal `https://developer.android.com/reference/kotlin/java/lang/Thread.html#` class.

 Value: 19

### THREAD_PRIORITY_MORE_FAVORABLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THREAD_PRIORITY_MORE_FAVORABLE: Int
```

Minimum increment to make a priority more favorable.

 Value: -1

### THREAD_PRIORITY_URGENT_AUDIO

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THREAD_PRIORITY_URGENT_AUDIO: Int
```

Standard priority of the most important audio threads. Applications should not normally change to this priority. Use with `https://developer.android.com/reference/kotlin/android/os/Process#setThreadPriority(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/os/Process#setThreadPriority(kotlin.Int,%20kotlin.Int)`, **not** with the normal `https://developer.android.com/reference/kotlin/java/lang/Thread.html#` class.

 Value: -19

### THREAD_PRIORITY_URGENT_DISPLAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THREAD_PRIORITY_URGENT_DISPLAY: Int
```

Standard priority of the most important display threads, for compositing the screen and retrieving input events. Use with `https://developer.android.com/reference/kotlin/android/os/Process#setThreadPriority(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/os/Process#setThreadPriority(kotlin.Int,%20kotlin.Int)`, **not** with the normal `https://developer.android.com/reference/kotlin/java/lang/Thread.html#` class.

 Value: -8

### THREAD_PRIORITY_VIDEO

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THREAD_PRIORITY_VIDEO: Int
```

Standard priority of video threads. Applications should not normally change to this priority. Use with `https://developer.android.com/reference/kotlin/android/os/Process#setThreadPriority(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/os/Process#setThreadPriority(kotlin.Int,%20kotlin.Int)`, **not** with the normal `https://developer.android.com/reference/kotlin/java/lang/Thread.html#` class.

 Value: -10

### WIFI_UID

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_UID: Int
```

Defines the UID/GID for the WIFI native processes like wificond, supplicant, hostapd, vendor HAL, etc.

 Value: 1010

## Public constructors

### Process

```
Process()
```

## Public methods

### areUidsForSameApplication

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun areUidsForSameApplication(
    uid1: Int, 
    uid2: Int
): Boolean
```

Returns true if the two UIDs belong to the same application, taking mathematically mapped UIDs (such as Private Compute Core sandbox) into account.

This method is user-aware. It will return false if the UIDs belong to different users, even if they map to the same base App ID.

### getAppUidForPrivateComputeCoreUid

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getAppUidForPrivateComputeCoreUid(uid: Int): Int
```

Returns the app UID corresponding to a Private Compute Core UID.

| Parameters ||
|---|---|
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the Private Compute Core UID |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the app UID for the given Private Compute Core UID |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if input is not a Private Compute Core UID |

### getAppUidForSdkSandboxUid

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getAppUidForSdkSandboxUid(uid: Int): Int
```

Returns the app uid corresponding to an sdk sandbox uid.

| Parameters ||
|---|---|
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the sdk sandbox uid |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the app uid for the given sdk sandbox uid |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if input is not an sdk sandbox uid |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager.html#`

### getElapsedCpuTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getElapsedCpuTime(): Long
```

Returns elapsed milliseconds of the time this process has run.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Returns the number of milliseconds this process has return. |

### getExclusiveCores

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getExclusiveCores(): IntArray!
```

On some devices, the foreground process may have one or more CPU cores exclusively reserved for it. This method can be used to retrieve which cores that are (if any), so the calling process can then use sched_setaffinity() to lock a thread to these cores. Note that the calling process must currently be running in the foreground for this method to return any cores. The CPU core(s) exclusively reserved for the foreground process will stay reserved for as long as the process stays in the foreground. As soon as a process leaves the foreground, those CPU cores will no longer be reserved for it, and will most likely be reserved for the new foreground process. It's not necessary to change the affinity of your process when it leaves the foreground (if you had previously set it to use a reserved core); the OS will automatically take care of resetting the affinity at that point.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` | an array of integers, indicating the CPU cores exclusively reserved for this process. The array will have length zero if no CPU cores are exclusively reserved for this process at this point in time. |

### getGidForName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getGidForName(name: String!): Int
```

Returns the GID assigned to a particular user name, or -1 if there is none. If the given string consists of only numbers, it is converted directly to a gid.

### getPrivateComputeCoreUidForAppUid

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getPrivateComputeCoreUidForAppUid(uid: Int): Int
```

Returns the Private Compute Core UID corresponding to an app UID.

| Parameters ||
|---|---|
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the app UID |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the Private Compute Core UID for the given app UID |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if input is not an app UID |

### getSdkSandboxUidForAppUid

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getSdkSandboxUidForAppUid(uid: Int): Int
```

Returns the sdk sandbox uid corresponding to an app uid.

| Parameters ||
|---|---|
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the app uid |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the sdk sandbox uid for the given app uid |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if input is not an app uid |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager.html#`

### getStartElapsedRealtime

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getStartElapsedRealtime(): Long
```

Return the `https://developer.android.com/reference/kotlin/android/os/SystemClock#elapsedRealtime()` at which this process was started, but before any of the application code was executed. 
Value is a non-negative timestamp in the `https://developer.android.com/reference/kotlin/android/os/SystemClock#elapsedRealtime()` time base.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Value is a non-negative timestamp in the `https://developer.android.com/reference/kotlin/android/os/SystemClock#elapsedRealtime()` time base. |

### getStartRequestedElapsedRealtime

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getStartRequestedElapsedRealtime(): Long
```

Return the `https://developer.android.com/reference/kotlin/android/os/SystemClock#elapsedRealtime()` at which the system was about to start this process. i.e. before a zygote fork.

More precisely, the system may start app processes before there's a start request, in order to reduce the process start up latency, in which case this is set when the system decides to "specialize" the process into a requested app. 
Value is a non-negative timestamp in the `https://developer.android.com/reference/kotlin/android/os/SystemClock#elapsedRealtime()` time base.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Value is a non-negative timestamp in the `https://developer.android.com/reference/kotlin/android/os/SystemClock#elapsedRealtime()` time base. |

### getStartRequestedUptimeMillis

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getStartRequestedUptimeMillis(): Long
```

Return the `https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeMillis()` at which the system was about to start this process. i.e. before a zygote fork.

More precisely, the system may start app processes before there's a start request, in order to reduce the process start up latency, in which case this is set when the system decides to "specialize" the process into a requested app. 
Value is a non-negative timestamp in the `https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeMillis()` time base.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Value is a non-negative timestamp in the `https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeMillis()` time base. |

### getStartUptimeMillis

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getStartUptimeMillis(): Long
```

Return the `https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeMillis()` at which this process was started, but before any of the application code was executed. 
Value is a non-negative timestamp in the `https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeMillis()` time base.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Value is a non-negative timestamp in the `https://developer.android.com/reference/kotlin/android/os/SystemClock#uptimeMillis()` time base. |

### getThreadPriority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getThreadPriority(tid: Int): Int
```

Return the current priority of a thread, based on Linux priorities. Ignores the `java.lang.Thread.getPriority()` cached priority, which is used to set the priority of newly created child Java threads.

| Parameters ||
|---|---|
| `tid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The identifier of the thread/process. If tid equals zero, the priority of the calling process/thread will be returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns the current priority, as a Linux priority level, from -20 for highest scheduling priority to 19 for lowest scheduling priority. Value is between -20 and `https://developer.android.com/reference/kotlin/android/os/Process#THREAD_PRIORITY_LOWEST:kotlin.Int` inclusive |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | Throws IllegalArgumentException if tid does not exist. |

### getUidForName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getUidForName(name: String!): Int
```

Returns the UID assigned to a particular user name, or -1 if there is none. If the given string consists of only numbers, it is converted directly to a uid.

### is64Bit

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun is64Bit(): Boolean
```

Returns true if the current process is a 64-bit runtime.

### isApplicationUid

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isApplicationUid(uid: Int): Boolean
```

Returns whether the given uid belongs to an application.

| Parameters ||
|---|---|
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A kernel uid. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the uid corresponds to an application sandbox running in a specific user. |

### isIsolated

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isIsolated(): Boolean
```

Returns whether the current process is in an isolated sandbox.

### isIsolatedUid

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isIsolatedUid(uid: Int): Boolean
```

Returns whether the process with the given `uid` is an isolated sandbox.

### isPrivateComputeCoreUid

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isPrivateComputeCoreUid(uid: Int): Boolean
```

Returns whether the provided UID belongs to components running in a Private Compute Core sandbox process.

### isSdkSandbox

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isSdkSandbox(): Boolean
```

Returns whether the current process is a sdk sandbox process.

### isSdkSandboxUid

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isSdkSandboxUid(uid: Int): Boolean
```

Returns whether the provided UID belongs to an sdk sandbox process
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager.html#`

### killProcess

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun killProcess(pid: Int): Unit
```

Kill the process with the given PID. Note that, though this API allows us to request to kill any process based on its PID, the kernel will still impose standard restrictions on which PIDs you are actually able to kill. Typically this means only the process running the caller's packages/application and any additional processes created by that app; packages sharing a common UID will also be able to kill each other's processes.

### myPid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun myPid(): Int
```

Returns the identifier of this process, which can be used with `https://developer.android.com/reference/kotlin/android/os/Process#killProcess(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/os/Process#sendSignal(kotlin.Int,%20kotlin.Int)`.

### myProcessName

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun myProcessName(): String
```

Return the name of this process. By default, the process name is the same as the app's package name, but this can be changed using `android:process`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### myTid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun myTid(): Int
```

Returns the identifier of the calling thread, which be used with `https://developer.android.com/reference/kotlin/android/os/Process#setThreadPriority(kotlin.Int,%20kotlin.Int)`.

### myUid

Added in [API level 2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun myUid(): Int
```

Returns the identifier of this process's uid. This is the kernel uid that the process is running under, which is the identity of its app-specific sandbox. It is different from `https://developer.android.com/reference/kotlin/android/os/Process#myUserHandle()` in that a uid identifies a specific app sandbox in a specific user.

### myUserHandle

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun myUserHandle(): UserHandle!
```

Returns this process's user handle. This is the user the process is running under. It is distinct from `https://developer.android.com/reference/kotlin/android/os/Process#myUid()` in that a particular user will have multiple distinct apps running under it each with their own uid.

### sendSignal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sendSignal(
    pid: Int, 
    signal: Int
): Unit
```

Send a signal to the given process.

| Parameters ||
|---|---|
| `pid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The pid of the target process. |
| `signal` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The signal to send. |

### setThreadPriority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setThreadPriority(priority: Int): Unit
```

Set the priority of the calling thread, based on Linux niceness priorities. See `https://developer.android.com/reference/kotlin/android/os/Process#setThreadPriority(kotlin.Int,%20kotlin.Int)` for more information. This is preferred over the two argument version when possible. The new priority is not inherited by Java child threads.

| Parameters ||
|---|---|
| `priority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A Linux priority level, from -20 for highest scheduling priority to 19 for lowest scheduling priority. Value is between -20 and `https://developer.android.com/reference/kotlin/android/os/Process#THREAD_PRIORITY_LOWEST:kotlin.Int` inclusive |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | Throws IllegalArgumentException if priority is out of range. |
| `java.lang.SecurityException` | Throws SecurityException if your process does not have permission to modify the given thread, or to use the given priority. |

### setThreadPriority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setThreadPriority(
    tid: Int, 
    priority: Int
): Unit
```

Set the OS priority of a thread, using Linux niceness priorities. Does not affect the value cached for use by `java.lang.Thread.getPriority()`. If this is used with a non-negative priority (Linux niceness), the priority may, on rare occasion, be reset by the runtime to its cached value, especially when setting the priority of another thread. The new priority is not inherited by Java-created child threads. It may or may not be inherited by threads created from native code. Use `java/lang/Thread.setPriority()` to allow child threads to inherit the new priority.

| Parameters ||
|---|---|
| `tid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The identifier of the thread/process to change. |
| `priority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A Linux priority a.k.a. "niceness" level, from -20 for highest scheduling priority to 19 for lowest scheduling priority. Value is between -20 and `https://developer.android.com/reference/kotlin/android/os/Process#THREAD_PRIORITY_LOWEST:kotlin.Int` inclusive |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | Throws IllegalArgumentException if tid does not exist, or priority is out of range. |
| `java.lang.SecurityException` | Throws SecurityException if your process does not have permission to modify the given thread, or to use the given priority. |

### supportsProcesses

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun supportsProcesses(): Boolean
```

**Deprecated:** *This method always returns true. Do not use.*

Determine whether the current environment supports multiple processes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the system can run in multiple processes, else false if everything is running in a single process. |
