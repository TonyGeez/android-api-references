# PowerMonitor

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PowerMonitor

Kotlin| [Java](https://developer.android.com/reference/android/os/PowerMonitor "View this page in Java") 
| --- | --- |

```
class PowerMonitor : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.PowerMonitor](https://developer.android.com/reference/kotlin/android/os/PowerMonitor#) |

A PowerMonitor represents either an ODPM rail (on-device power rail monitor) or a modeled energy consumer.

<br />

ODPM rail names are device-specific. No assumptions should be made about the names and exact purpose of ODPM rails across different device models. A rail name may be something like "S2S_VDD_G3D"; specific knowledge of the device hardware is required to interpret the corresponding power monitor data.

<br />

Energy consumer have more human-readable names, e.g. "GPU", "MODEM" etc. However, developers must be extra cautious about using energy consumers across different device models, as their exact implementations are also hardware dependent and are customized by OEMs.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POWER_MONITOR_TYPE_CONSUMER](https://developer.android.com/reference/kotlin/android/os/PowerMonitor#POWER_MONITOR_TYPE_CONSUMER:kotlin.Int) Power monitor corresponding to a subsystem. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POWER_MONITOR_TYPE_MEASUREMENT](https://developer.android.com/reference/kotlin/android/os/PowerMonitor#POWER_MONITOR_TYPE_MEASUREMENT:kotlin.Int) Power monitor corresponding to a directly measured power rail. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/os/PowerMonitor#describeContents())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](https://developer.android.com/reference/kotlin/android/os/PowerMonitor#getName())`()` Returns the name of the power monitor, either a power rail or an energy consumer. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/os/PowerMonitor#getType())`()` Returns the type of the power monitor. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/os/PowerMonitor#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator)\< [PowerMonitor](https://developer.android.com/reference/kotlin/android/os/PowerMonitor#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/os/PowerMonitor#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### POWER_MONITOR_TYPE_CONSUMER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POWER_MONITOR_TYPE_CONSUMER: Int
```

Power monitor corresponding to a subsystem. The energy value may be a direct pass-through power rail measurement, or modeled in some fashion. For example, an energy consumer may represent a combination of multiple rails or a portion of a rail shared between subsystems, e.g. WiFi and Bluetooth are often handled by the same chip, powered by a shared rail. Some consumer names are standardized, others are not. 

 Value: 0

### POWER_MONITOR_TYPE_MEASUREMENT

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POWER_MONITOR_TYPE_MEASUREMENT: Int
```

Power monitor corresponding to a directly measured power rail. Rails are device-specific: no assumptions can be made about the source of those measurements across different devices, even if they have the same name. 

 Value: 1

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getName

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String
```

Returns the name of the power monitor, either a power rail or an energy consumer.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Int
```

Returns the type of the power monitor.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.os.PowerMonitor#POWER_MONITOR_TYPE_CONSUMER](https://developer.android.com/reference/kotlin/android/os/PowerMonitor#POWER_MONITOR_TYPE_CONSUMER:kotlin.Int), and [android.os.PowerMonitor#POWER_MONITOR_TYPE_MEASUREMENT](https://developer.android.com/reference/kotlin/android/os/PowerMonitor#POWER_MONITOR_TYPE_MEASUREMENT:kotlin.Int) |

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
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<PowerMonitor!>
```
