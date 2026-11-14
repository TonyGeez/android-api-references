Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ApplicationExitInfo

```
class ApplicationExitInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.ApplicationExitInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#) |

Describes the information of an application process's death.

Application process could die for many reasons, for example `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_LOW_MEMORY:kotlin.Int` when it was killed by the system because it was running low on memory. Reason of the death can be retrieved via `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getReason()`. Besides the reason, there are a few other auxiliary APIs like `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getStatus()` and `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getImportance()` to help the caller with additional diagnostic information.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo.AnrInfo` <br /> |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_ANOMALY:kotlin.Int` Application process violated a system resource anomaly rule and was terminated. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_ANR:kotlin.Int` Application process was killed due to being unresponsive (ANR). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_CRASH:kotlin.Int` Application process died because of an unhandled exception in Java code. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_CRASH_NATIVE:kotlin.Int` Application process died because of a native code crash. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_DEPENDENCY_DIED:kotlin.Int` Application process was killed because its dependency was going away, for example, a stable content provider connection's client will be killed if the provider is killed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_EXCESSIVE_RESOURCE_USAGE:kotlin.Int` Application process was killed by the system due to excessive resource usage. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_EXIT_SELF:kotlin.Int` Application process exit normally by itself, for example, via `https://developer.android.com/reference/kotlin/java/lang/System.html#exit(kotlin.Int)`; `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getStatus()` will specify the exit code. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_FREEZER:kotlin.Int` Application process was killed by App Freezer, for example, because it receives sync binder transactions while being frozen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_INITIALIZATION_FAILURE:kotlin.Int` Application process was killed because of initialization failure, for example, it took too long to attach to the system during the start, or there was an error during initialization. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_LOW_MEMORY:kotlin.Int` Application process was killed by the system low memory killer, meaning the system was under memory pressure at the time of kill. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_MEMORY_LIMITER:kotlin.Int` Application process was killed because it exceeded the system memory limits. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_OTHER:kotlin.Int` Application process was killed by the system for various other reasons which are not by problems in apps and not actionable by apps, for example, the system just finished updates; `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getDescription()` will specify the cause given by the system. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_PACKAGE_STATE_CHANGE:kotlin.Int` Application process was killed because the app was disabled, or any of its component states have changed without `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#DONT_KILL_APP:kotlin.Int` |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_PACKAGE_UPDATED:kotlin.Int` Application process was killed because it was updated. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_PERMISSION_CHANGE:kotlin.Int` Application process was killed due to a runtime permission change. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_SIGNALED:kotlin.Int` Application process died due to the result of an OS signal; for example, `https://developer.android.com/reference/kotlin/android/system/OsConstants.html#SIGKILL:kotlin.Int`; `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getStatus()` will specify the signal number. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_UNKNOWN:kotlin.Int` Application process died due to unknown reason. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_USER_REQUESTED:kotlin.Int` Application process was killed because of the user request, for example, user clicked the "Force stop" button of the application in the Settings, or removed the application away from Recents. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_USER_STOPPED:kotlin.Int` Application process was killed, because the user it is running as on devices with multiple users, was stopped. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [ApplicationExitInfo.AnrInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo.AnrInfo)? | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getAnrInfo()()` Populated only when the reason is `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_ANR:kotlin.Int`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getDefiningUid()()` Return the defining kernel user identifier, maybe different from `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getRealUid()` and `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getPackageUid()`, if an external service has the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestService_useAppZygote:kotlin.Int` set to `true` and was bound with the flag `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_EXTERNAL_SERVICE:kotlin.Int` - in this case, this field here will be the kernel user identifier of the external service provider. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getDescription()()` The human readable description of the process's death, given by the system; could be null. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getImportance()()` The importance of the process that it used to have before the death. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getPackageUid()()` Similar to `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getRealUid()`, it's the kernel user identifier that is assigned at the package installation time. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getPid()()` The process id of the process that died. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getProcessName()()` The actual process name it was running with. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getProcessStateSummary()()` Return the state data set by calling `https://developer.android.com/reference/kotlin/android/app/ActivityManager#setProcessStateSummary(kotlin.ByteArray)` from the process before its death. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getPss()()` Last proportional set size of the memory that the process had used in kB. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getRealUid()()` The kernel user identifier of the process, most of the time the system uses this to do access control checks. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getReason()()` The reason code of the process's death. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getRss()()` Last resident set size of the memory that the process had used in kB. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getStatus()()` The exit status argument of exit() if the application calls it, or the signal number if the application is signaled. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getTimestamp()()` The timestamp of the process's death, in milliseconds since the epoch, as returned by `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`. |
| [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)? | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getTraceInputStream()()` Return the InputStream to the traces that was taken by the system prior to the death of the process; typically it'll be available when the reason is `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_ANR:kotlin.Int`, though if the process gets an ANR but recovers, and dies for another reason later, this trace will be included in the record of `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#` still. |
| [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getUserHandle()()` Return the user id of the record on a multi-user system. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#hashCode()()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ApplicationExitInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#)!\> | `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### REASON_ANOMALY

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_ANOMALY: Int
```

Application process violated a system resource anomaly rule and was terminated.

 Value: 18

### REASON_ANR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_ANR: Int
```

Application process was killed due to being unresponsive (ANR).

 Value: 6

### REASON_CRASH

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_CRASH: Int
```

Application process died because of an unhandled exception in Java code.

 Value: 4

### REASON_CRASH_NATIVE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_CRASH_NATIVE: Int
```

Application process died because of a native code crash.

 Value: 5

### REASON_DEPENDENCY_DIED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_DEPENDENCY_DIED: Int
```

Application process was killed because its dependency was going away, for example, a stable content provider connection's client will be killed if the provider is killed.

 Value: 12

### REASON_EXCESSIVE_RESOURCE_USAGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_EXCESSIVE_RESOURCE_USAGE: Int
```

Application process was killed by the system due to excessive resource usage.

 Value: 9

### REASON_EXIT_SELF

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_EXIT_SELF: Int
```

Application process exit normally by itself, for example, via `https://developer.android.com/reference/kotlin/java/lang/System.html#exit(kotlin.Int)`; `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getStatus()` will specify the exit code.

Applications should normally not do this, as the system has a better knowledge in terms of process management.

 Value: 1

### REASON_FREEZER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_FREEZER: Int
```

Application process was killed by App Freezer, for example, because it receives sync binder transactions while being frozen.

 Value: 14

### REASON_INITIALIZATION_FAILURE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_INITIALIZATION_FAILURE: Int
```

Application process was killed because of initialization failure, for example, it took too long to attach to the system during the start, or there was an error during initialization.

 Value: 7

### REASON_LOW_MEMORY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_LOW_MEMORY: Int
```

Application process was killed by the system low memory killer, meaning the system was under memory pressure at the time of kill.

Not all devices support reporting `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_LOW_MEMORY:kotlin.Int`; on a device with no such support, when a process is killed due to memory pressure, the `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getReason()` will return `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_SIGNALED:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getStatus()` will return the value `https://developer.android.com/reference/kotlin/android/system/OsConstants.html#SIGKILL:kotlin.Int`. Application should use `https://developer.android.com/reference/kotlin/android/app/ActivityManager#isLowMemoryKillReportSupported()` to check if the device supports reporting `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_LOW_MEMORY:kotlin.Int` or not.

 Value: 3

### REASON_MEMORY_LIMITER

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_MEMORY_LIMITER: Int
```

Application process was killed because it exceeded the system memory limits.

 Value: 17

### REASON_OTHER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_OTHER: Int
```

Application process was killed by the system for various other reasons which are not by problems in apps and not actionable by apps, for example, the system just finished updates; `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getDescription()` will specify the cause given by the system.

 Value: 13

### REASON_PACKAGE_STATE_CHANGE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_PACKAGE_STATE_CHANGE: Int
```

Application process was killed because the app was disabled, or any of its component states have changed without `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#DONT_KILL_APP:kotlin.Int`

Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_USER_REQUESTED:kotlin.Int` was used to indicate that an app was updated.

 Value: 15

### REASON_PACKAGE_UPDATED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_PACKAGE_UPDATED: Int
```

Application process was killed because it was updated.

Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_USER_REQUESTED:kotlin.Int` was used to indicate that an app was updated.

 Value: 16

### REASON_PERMISSION_CHANGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_PERMISSION_CHANGE: Int
```

Application process was killed due to a runtime permission change.

 Value: 8

### REASON_SIGNALED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_SIGNALED: Int
```

Application process died due to the result of an OS signal; for example, `https://developer.android.com/reference/kotlin/android/system/OsConstants.html#SIGKILL:kotlin.Int`; `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getStatus()` will specify the signal number.

 Value: 2

### REASON_UNKNOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_UNKNOWN: Int
```

Application process died due to unknown reason.

 Value: 0

### REASON_USER_REQUESTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_USER_REQUESTED: Int
```

Application process was killed because of the user request, for example, user clicked the "Force stop" button of the application in the Settings, or removed the application away from Recents.

Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, one of the uses of this reason was to indicate that an app was killed due to it being updated or any of its component states have changed without `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#DONT_KILL_APP:kotlin.Int`

 Value: 10

### REASON_USER_STOPPED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_USER_STOPPED: Int
```

Application process was killed, because the user it is running as on devices with multiple users, was stopped.

 Value: 11

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### getAnrInfo

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAnrInfo(): ApplicationExitInfo.AnrInfo?
```

Populated only when the reason is `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_ANR:kotlin.Int`. Otherwise Null.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo.AnrInfo?` | This value may be `null`. |

### getDefiningUid

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDefiningUid(): Int
```

Return the defining kernel user identifier, maybe different from `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getRealUid()` and `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getPackageUid()`, if an external service has the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestService_useAppZygote:kotlin.Int` set to `true` and was bound with the flag `https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_EXTERNAL_SERVICE:kotlin.Int` - in this case, this field here will be the kernel user identifier of the external service provider.

### getDescription

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDescription(): String?
```

The human readable description of the process's death, given by the system; could be null.

Note: only intended to be human-readable and the system provides no guarantees that the format is stable across devices or Android releases.

### getImportance

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getImportance(): Int
```

The importance of the process that it used to have before the death.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo#IMPORTANCE_FOREGROUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo#IMPORTANCE_FOREGROUND_SERVICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo#IMPORTANCE_TOP_SLEEPING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo#IMPORTANCE_VISIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo#IMPORTANCE_PERCEPTIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo#IMPORTANCE_CANT_SAVE_STATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo#IMPORTANCE_SERVICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo#IMPORTANCE_CACHED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo#IMPORTANCE_GONE:kotlin.Int` |

### getPackageUid

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPackageUid(): Int
```

Similar to `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getRealUid()`, it's the kernel user identifier that is assigned at the package installation time.

### getPid

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPid(): Int
```

The process id of the process that died.

### getProcessName

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getProcessName(): String
```

The actual process name it was running with.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getProcessStateSummary

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getProcessStateSummary(): ByteArray?
```

Return the state data set by calling `https://developer.android.com/reference/kotlin/android/app/ActivityManager#setProcessStateSummary(kotlin.ByteArray)` from the process before its death.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | The process-customized data. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/ActivityManager#setProcessStateSummary(kotlin.ByteArray)`

### getPss

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPss(): Long
```

Last proportional set size of the memory that the process had used in kB.

Note: This is the value from last sampling on the process, it's NOT the exact memory information prior to its death; and it'll be zero if the process died before system had a chance to take the sample.

### getRealUid

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRealUid(): Int
```

The kernel user identifier of the process, most of the time the system uses this to do access control checks. It's typically the uid of the package where the component is running from, except the case of isolated process, where this field identifies the kernel user identifier that this process is actually running with, while the `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#getPackageUid()` identifies the kernel user identifier that is assigned at the package installation time.

### getReason

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getReason(): Int
```

The reason code of the process's death.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_EXIT_SELF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_SIGNALED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_LOW_MEMORY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_CRASH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_CRASH_NATIVE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_ANR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_INITIALIZATION_FAILURE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_PERMISSION_CHANGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_EXCESSIVE_RESOURCE_USAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_USER_REQUESTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_USER_STOPPED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_DEPENDENCY_DIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_OTHER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_FREEZER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_PACKAGE_STATE_CHANGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_PACKAGE_UPDATED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_MEMORY_LIMITER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_ANOMALY:kotlin.Int` |

### getRss

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRss(): Long
```

Last resident set size of the memory that the process had used in kB.

Note: This is the value from last sampling on the process, it's NOT the exact memory information prior to its death; and it'll be zero if the process died before system had a chance to take the sample.

### getStatus

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStatus(): Int
```

The exit status argument of exit() if the application calls it, or the signal number if the application is signaled.

### getTimestamp

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTimestamp(): Long
```

The timestamp of the process's death, in milliseconds since the epoch, as returned by `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`. 
Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z. |

### getTraceInputStream

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTraceInputStream(): InputStream?
```

Return the InputStream to the traces that was taken by the system prior to the death of the process; typically it'll be available when the reason is `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_ANR:kotlin.Int`, though if the process gets an ANR but recovers, and dies for another reason later, this trace will be included in the record of `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#` still. Beginning with API 31, tombstone traces will be returned for `https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo#REASON_CRASH_NATIVE:kotlin.Int`, with an InputStream containing a protobuf with [this schema](https://android.googlesource.com/platform/system/core/+/refs/heads/master/debuggerd/proto/tombstone.proto). Note that because these traces are kept in a separate global circular buffer, crashes may be overwritten by newer crashes (including from other applications), so this may still return null.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/InputStream.html#?` | The input stream to the traces that was taken by the system prior to the death of the process. |

### getUserHandle

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUserHandle(): UserHandle
```

Return the user id of the record on a multi-user system.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` | This value cannot be `null`. |

### hashCode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### toString

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<ApplicationExitInfo!>
```
