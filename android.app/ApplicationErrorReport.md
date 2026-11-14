# ApplicationErrorReport

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ApplicationErrorReport

Kotlin| [Java](https://developer.android.com/reference/android/app/ApplicationErrorReport "View this page in Java") 
| --- | --- |

```
open class ApplicationErrorReport : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.ApplicationErrorReport](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#) |

Describes an application error. A report has a type, which is one of

- [TYPE_NONE](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#TYPE_NONE:kotlin.Int) uninitialized instance of [ApplicationErrorReport](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#).
- [TYPE_CRASH](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#TYPE_CRASH:kotlin.Int) application crash. Information about the crash is stored in [crashInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#crashInfo:android.app.ApplicationErrorReport.CrashInfo).
- [TYPE_ANR](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#TYPE_ANR:kotlin.Int) application not responding. Information about the ANR is stored in [anrInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#anrInfo:android.app.ApplicationErrorReport.AnrInfo).
- [TYPE_BATTERY](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#TYPE_BATTERY:kotlin.Int) user reported application is using too much battery. Information about the battery use is stored in [batteryInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#batteryInfo:android.app.ApplicationErrorReport.BatteryInfo).
- [TYPE_RUNNING_SERVICE](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#TYPE_RUNNING_SERVICE:kotlin.Int) user reported application is leaving an unneeded serive running. Information about the battery use is stored in [runningServiceInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#runningServiceInfo:android.app.ApplicationErrorReport.RunningServiceInfo).

<br />

## Summary

| Nested classes ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [AnrInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport.AnrInfo) Describes an application not responding error. |
| open | [BatteryInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport.BatteryInfo) Describes a battery usage report. |
| open | [CrashInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport.CrashInfo) Describes an application crash. |
| --- | --- |
| open | [RunningServiceInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport.RunningServiceInfo) Describes a running service report. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ANR](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#TYPE_ANR:kotlin.Int) An error report about an application that's not responding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BATTERY](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#TYPE_BATTERY:kotlin.Int) An error report about an application that's consuming too much battery. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CRASH](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#TYPE_CRASH:kotlin.Int) An error report about an application crash. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NONE](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#TYPE_NONE:kotlin.Int) Uninitialized error report. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RUNNING_SERVICE](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#TYPE_RUNNING_SERVICE:kotlin.Int) A report from a user to a developer about a running service that the user doesn't think should be running. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ApplicationErrorReport](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#ApplicationErrorReport())`()` Create an uninitialized instance of [ApplicationErrorReport](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#). |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#describeContents())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#dump(android.util.Printer,%20kotlin.String))`(`pw:` ` [Printer](https://developer.android.com/reference/kotlin/android/util/Printer.html#)!`, `prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Dump the report to a Printer. |
| openstatic [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)! | [getErrorReportReceiver](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#getErrorReportReceiver(android.content.Context,%20kotlin.String,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `appFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readFromParcel](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#readFromParcel(android.os.Parcel))`(`in:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ApplicationErrorReport](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#CREATOR:android.os.Parcelable.Creator) <br /> |
| [ApplicationErrorReport.AnrInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport.AnrInfo)! | [anrInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#anrInfo:android.app.ApplicationErrorReport.AnrInfo) If this report is of type [TYPE_ANR](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#TYPE_ANR:kotlin.Int), contains an instance of AnrInfo describing the ANR; otherwise null. |
| [ApplicationErrorReport.BatteryInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport.BatteryInfo)! | [batteryInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#batteryInfo:android.app.ApplicationErrorReport.BatteryInfo) If this report is of type [TYPE_BATTERY](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#TYPE_BATTERY:kotlin.Int), contains an instance of BatteryInfo; otherwise null. |
| --- | --- |
| [ApplicationErrorReport.CrashInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport.CrashInfo)! | [crashInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#crashInfo:android.app.ApplicationErrorReport.CrashInfo) If this report is of type [TYPE_CRASH](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#TYPE_CRASH:kotlin.Int), contains an instance of CrashInfo describing the crash; otherwise null. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [installerPackageName](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#installerPackageName:kotlin.String) Package name of the application which installed the application this report pertains to. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [packageName](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#packageName:kotlin.String) Package name of the application. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [processName](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#processName:kotlin.String) Process name of the application. |
| [ApplicationErrorReport.RunningServiceInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport.RunningServiceInfo)! | [runningServiceInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#runningServiceInfo:android.app.ApplicationErrorReport.RunningServiceInfo) If this report is of type [TYPE_RUNNING_SERVICE](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#TYPE_RUNNING_SERVICE:kotlin.Int), contains an instance of RunningServiceInfo; otherwise null. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [systemApp](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#systemApp:kotlin.Boolean) Set if the app is on the system image. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [time](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#time:kotlin.Long) Time at which the error occurred. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [type](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#type:kotlin.Int) Type of this report. |

## Constants

### TYPE_ANR

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ANR: Int
```

An error report about an application that's not responding. 

 Value: 2

### TYPE_BATTERY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_BATTERY: Int
```

An error report about an application that's consuming too much battery. 

 Value: 3

### TYPE_CRASH

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_CRASH: Int
```

An error report about an application crash. 

 Value: 1

### TYPE_NONE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_NONE: Int
```

Uninitialized error report. 

 Value: 0

### TYPE_RUNNING_SERVICE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_RUNNING_SERVICE: Int
```

A report from a user to a developer about a running service that the user doesn't think should be running. 

 Value: 5

## Public constructors

### ApplicationErrorReport

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ApplicationErrorReport()
```

Create an uninitialized instance of [ApplicationErrorReport](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#).

## Public methods

### describeContents

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### dump

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dump(
    pw: Printer!, 
    prefix: String!
): Unit
```

Dump the report to a Printer. 

### getErrorReportReceiver

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getErrorReportReceiver(
    context: Context!, 
    packageName: String!, 
    appFlags: Int
): ComponentName!
```  

### readFromParcel

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun readFromParcel(in: Parcel!): Unit
```  

### writeToParcel

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ApplicationErrorReport!>
```  

### anrInfo

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var anrInfo: ApplicationErrorReport.AnrInfo!
```

If this report is of type [TYPE_ANR](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#TYPE_ANR:kotlin.Int), contains an instance of AnrInfo describing the ANR; otherwise null. 

### batteryInfo

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var batteryInfo: ApplicationErrorReport.BatteryInfo!
```

If this report is of type [TYPE_BATTERY](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#TYPE_BATTERY:kotlin.Int), contains an instance of BatteryInfo; otherwise null. 

### crashInfo

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var crashInfo: ApplicationErrorReport.CrashInfo!
```

If this report is of type [TYPE_CRASH](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#TYPE_CRASH:kotlin.Int), contains an instance of CrashInfo describing the crash; otherwise null. 

### installerPackageName

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var installerPackageName: String!
```

Package name of the application which installed the application this report pertains to. This identifies which market the application came from. 

### packageName

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var packageName: String!
```

Package name of the application. 

### processName

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var processName: String!
```

Process name of the application. 

### runningServiceInfo

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var runningServiceInfo: ApplicationErrorReport.RunningServiceInfo!
```

If this report is of type [TYPE_RUNNING_SERVICE](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#TYPE_RUNNING_SERVICE:kotlin.Int), contains an instance of RunningServiceInfo; otherwise null. 

### systemApp

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var systemApp: Boolean
```

Set if the app is on the system image. 

### time

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var time: Long
```

Time at which the error occurred. 

### type

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var type: Int
```

Type of this report. Can be one of [TYPE_NONE](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#TYPE_NONE:kotlin.Int), [TYPE_CRASH](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#TYPE_CRASH:kotlin.Int), [TYPE_ANR](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#TYPE_ANR:kotlin.Int), [TYPE_BATTERY](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#TYPE_BATTERY:kotlin.Int), or [TYPE_RUNNING_SERVICE](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport#TYPE_RUNNING_SERVICE:kotlin.Int).
