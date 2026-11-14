# ApplicationErrorReport

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ApplicationErrorReport

Kotlin| [Java](ApplicationErrorReport.md) 
| --- | --- |

```
open class ApplicationErrorReport : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.ApplicationErrorReport](ApplicationErrorReport.md) |

Describes an application error. A report has a type, which is one of

- [TYPE_NONE](ApplicationErrorReport.md) uninitialized instance of [ApplicationErrorReport](ApplicationErrorReport.md).
- [TYPE_CRASH](ApplicationErrorReport.md) application crash. Information about the crash is stored in [crashInfo](ApplicationErrorReport.md).
- [TYPE_ANR](ApplicationErrorReport.md) application not responding. Information about the ANR is stored in [anrInfo](ApplicationErrorReport.md).
- [TYPE_BATTERY](ApplicationErrorReport.md) user reported application is using too much battery. Information about the battery use is stored in [batteryInfo](ApplicationErrorReport.md).
- [TYPE_RUNNING_SERVICE](ApplicationErrorReport.md) user reported application is leaving an unneeded serive running. Information about the battery use is stored in [runningServiceInfo](ApplicationErrorReport.md).

<br />

## Summary

| Nested classes ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [AnrInfo](../android/app/ApplicationErrorReport.AnrInfo.md) Describes an application not responding error. |
| open | [BatteryInfo](../android/app/ApplicationErrorReport.BatteryInfo.md) Describes a battery usage report. |
| open | [CrashInfo](../android/app/ApplicationErrorReport.CrashInfo.md) Describes an application crash. |
| --- | --- |
| open | [RunningServiceInfo](../android/app/ApplicationErrorReport.RunningServiceInfo.md) Describes a running service report. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ANR](ApplicationErrorReport.md) An error report about an application that's not responding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BATTERY](ApplicationErrorReport.md) An error report about an application that's consuming too much battery. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CRASH](ApplicationErrorReport.md) An error report about an application crash. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NONE](ApplicationErrorReport.md) Uninitialized error report. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RUNNING_SERVICE](ApplicationErrorReport.md) A report from a user to a developer about a running service that the user doesn't think should be running. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ApplicationErrorReport](ApplicationErrorReport.md))`()` Create an uninitialized instance of [ApplicationErrorReport](ApplicationErrorReport.md). |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](ApplicationErrorReport.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](ApplicationErrorReport.md))`(`pw:` ` [Printer](../android.util/Printer.md)!`, `prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Dump the report to a Printer. |
| openstatic [ComponentName](../android.content/ComponentName.md)! | [getErrorReportReceiver](ApplicationErrorReport.md))`(`context:` ` [Context](../android.content/Context.md)!`, `packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `appFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readFromParcel](ApplicationErrorReport.md))`(`in:` ` [Parcel](../android.os/Parcel.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](ApplicationErrorReport.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ApplicationErrorReport](ApplicationErrorReport.md)!\> | [CREATOR](ApplicationErrorReport.md) <br /> |
| [ApplicationErrorReport.AnrInfo](../android/app/ApplicationErrorReport.AnrInfo.md)! | [anrInfo](ApplicationErrorReport.md) If this report is of type [TYPE_ANR](ApplicationErrorReport.md), contains an instance of AnrInfo describing the ANR; otherwise null. |
| [ApplicationErrorReport.BatteryInfo](../android/app/ApplicationErrorReport.BatteryInfo.md)! | [batteryInfo](ApplicationErrorReport.md) If this report is of type [TYPE_BATTERY](ApplicationErrorReport.md), contains an instance of BatteryInfo; otherwise null. |
| --- | --- |
| [ApplicationErrorReport.CrashInfo](../android/app/ApplicationErrorReport.CrashInfo.md)! | [crashInfo](ApplicationErrorReport.md) If this report is of type [TYPE_CRASH](ApplicationErrorReport.md), contains an instance of CrashInfo describing the crash; otherwise null. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [installerPackageName](ApplicationErrorReport.md) Package name of the application which installed the application this report pertains to. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [packageName](ApplicationErrorReport.md) Package name of the application. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [processName](ApplicationErrorReport.md) Process name of the application. |
| [ApplicationErrorReport.RunningServiceInfo](../android/app/ApplicationErrorReport.RunningServiceInfo.md)! | [runningServiceInfo](ApplicationErrorReport.md) If this report is of type [TYPE_RUNNING_SERVICE](ApplicationErrorReport.md), contains an instance of RunningServiceInfo; otherwise null. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [systemApp](ApplicationErrorReport.md) Set if the app is on the system image. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [time](ApplicationErrorReport.md) Time at which the error occurred. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [type](ApplicationErrorReport.md) Type of this report. |

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

Create an uninitialized instance of [ApplicationErrorReport](ApplicationErrorReport.md).

## Public methods

### describeContents

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

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
| `dest` | [Parcel](../android.os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

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

If this report is of type [TYPE_ANR](ApplicationErrorReport.md), contains an instance of AnrInfo describing the ANR; otherwise null. 

### batteryInfo

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var batteryInfo: ApplicationErrorReport.BatteryInfo!
```

If this report is of type [TYPE_BATTERY](ApplicationErrorReport.md), contains an instance of BatteryInfo; otherwise null. 

### crashInfo

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var crashInfo: ApplicationErrorReport.CrashInfo!
```

If this report is of type [TYPE_CRASH](ApplicationErrorReport.md), contains an instance of CrashInfo describing the crash; otherwise null. 

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

If this report is of type [TYPE_RUNNING_SERVICE](ApplicationErrorReport.md), contains an instance of RunningServiceInfo; otherwise null. 

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

Type of this report. Can be one of [TYPE_NONE](ApplicationErrorReport.md), [TYPE_CRASH](ApplicationErrorReport.md), [TYPE_ANR](ApplicationErrorReport.md), [TYPE_BATTERY](ApplicationErrorReport.md), or [TYPE_RUNNING_SERVICE](ApplicationErrorReport.md).
