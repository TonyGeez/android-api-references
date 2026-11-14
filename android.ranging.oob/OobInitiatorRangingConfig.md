# OobInitiatorRangingConfig

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OobInitiatorRangingConfig

Kotlin| [Java](https://developer.android.com/reference/android/ranging/oob/OobInitiatorRangingConfig "View this page in Java") 

```
class OobInitiatorRangingConfig : RangingConfig, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.ranging.RangingConfig](https://developer.android.com/reference/kotlin/android/ranging/RangingConfig.html#) ||
| | ↳ | [android.ranging.oob.OobInitiatorRangingConfig](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#) |

Represents the configuration for an Out-of-Band (OOB) initiator in a ranging session. This class includes configuration options such as device handles, security level, ranging mode, and interval range for setting up an OOB initiator ranging session.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig.Builder) Builder class for creating instances of [OobInitiatorRangingConfig](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#). |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANGING_MODE_AUTO](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#RANGING_MODE_AUTO:kotlin.Int) Automatic ranging mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANGING_MODE_FUSED](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#RANGING_MODE_FUSED:kotlin.Int) Starts ranging with all the ranging technologies both devices support. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANGING_MODE_HIGH_ACCURACY](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#RANGING_MODE_HIGH_ACCURACY:kotlin.Int) High accuracy ranging mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANGING_MODE_HIGH_ACCURACY_PREFERRED](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#RANGING_MODE_HIGH_ACCURACY_PREFERRED:kotlin.Int) High accuracy ranging mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_LEVEL_BASIC](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#SECURITY_LEVEL_BASIC:kotlin.Int) Basic security level for the ranging session. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_LEVEL_SECURE](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#SECURITY_LEVEL_SECURE:kotlin.Int) Basic security level for the ranging session. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||
| From class [RangingConfig](https://developer.android.com/reference/kotlin/android/ranging/RangingConfig.html#) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANGING_SESSION_OOB](https://developer.android.com/reference/kotlin/android/ranging/RangingConfig.html#RANGING_SESSION_OOB:kotlin.Int) <br /> Ranging session with the out-of-band negotiations performed by the ranging API. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANGING_SESSION_RAW](https://developer.android.com/reference/kotlin/android/ranging/RangingConfig.html#RANGING_SESSION_RAW:kotlin.Int) <br /> Ranging session with the out-of-band negotiations performed by the app. <br /> | ||

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#describeContents())`()` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [DeviceHandle](https://developer.android.com/reference/kotlin/android/ranging/oob/DeviceHandle)!\> | [getDeviceHandles](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#getDeviceHandles())`()` Returns the list of DeviceHandles associated with the OOB initiator. |
| [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#) | [getFastestRangingInterval](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#getFastestRangingInterval())`()` Returns the fastest requested ranging interval. |
| [Range](https://developer.android.com/reference/kotlin/android/util/Range.html#)\< [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#)!\> | [getRangingIntervalRange](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#getRangingIntervalRange())`()` Returns the ranging interval range configuration. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRangingMode](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#getRangingMode())`()` Returns the ranging mode for the session. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | [getRangingTechnologyFilter](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#getRangingTechnologyFilter())`()` Returns the set of ranging technologies that can be used for the session. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSecurityLevel](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#getSecurityLevel())`()` Returns the security level set for the ranging session. |
| [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#) | [getSlowestRangingInterval](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#getSlowestRangingInterval())`()` Returns the slowest acceptable ranging. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Inherited functions ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents())`()` <br /> Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of [writeToParcel(android.os.Parcel,int)](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)), the return value of this method must include the [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) bit. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Flatten this object in to a Parcel. <br /> | ||
| From class [RangingConfig](https://developer.android.com/reference/kotlin/android/ranging/RangingConfig.html#) |----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRangingSessionType](https://developer.android.com/reference/kotlin/android/ranging/RangingConfig.html#getRangingSessionType())`()` <br /> Gets the ranging session type android.ranging.RangingConfig.RangingSessionType <br /> | ||

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [OobInitiatorRangingConfig](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### RANGING_MODE_AUTO

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RANGING_MODE_AUTO: Int
```

Automatic ranging mode. Allows the system to choose the best mode. 

 Value: 0

### RANGING_MODE_FUSED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RANGING_MODE_FUSED: Int
```

Starts ranging with all the ranging technologies both devices support. 

 Value: 3

### RANGING_MODE_HIGH_ACCURACY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RANGING_MODE_HIGH_ACCURACY: Int
```

High accuracy ranging mode. No fallback allowed. 

 Value: 1

### RANGING_MODE_HIGH_ACCURACY_PREFERRED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RANGING_MODE_HIGH_ACCURACY_PREFERRED: Int
```

High accuracy ranging mode. Fallback to lower accuracy if high accuracy ranging is not supported by all devices. 

 Value: 2

### SECURITY_LEVEL_BASIC

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_LEVEL_BASIC: Int
```

Basic security level for the ranging session.

Example usage: UWB: Static-STS BLE-CS: Security level one 

 Value: 0

### SECURITY_LEVEL_SECURE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_LEVEL_SECURE: Int
```

Basic security level for the ranging session.

Example usage: UWB: Provisioned-STS BLE-CS: Security level four 

 Value: 1

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getDeviceHandles

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeviceHandles(): MutableList<DeviceHandle!>
```

Returns the list of DeviceHandles associated with the OOB initiator.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [DeviceHandle](https://developer.android.com/reference/kotlin/android/ranging/oob/DeviceHandle)!> | A list of DeviceHandle objects. This value cannot be`null`. |

### getFastestRangingInterval

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFastestRangingInterval(): Duration
```

Returns the fastest requested ranging interval.

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------|
| [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#) | The fastest interval. This value cannot be`null`. |

### getRangingIntervalRange

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRangingIntervalRange(): Range<Duration!>
```

Returns the ranging interval range configuration.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Range](https://developer.android.com/reference/kotlin/android/util/Range.html#)< [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#)!> | The [Range](https://developer.android.com/reference/kotlin/android/util/Range.html#) associated with this OOB initiator. This value cannot be`null`. |

### getRangingMode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRangingMode(): Int
```

Returns the ranging mode for the session.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the ranging mode. Possible values: [RANGING_MODE_AUTO](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#RANGING_MODE_AUTO:kotlin.Int) [RANGING_MODE_HIGH_ACCURACY](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#RANGING_MODE_HIGH_ACCURACY:kotlin.Int) [RANGING_MODE_HIGH_ACCURACY_PREFERRED](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#RANGING_MODE_HIGH_ACCURACY_PREFERRED:kotlin.Int) [RANGING_MODE_FUSED](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#RANGING_MODE_FUSED:kotlin.Int) Value is [android.ranging.oob.OobInitiatorRangingConfig#RANGING_MODE_AUTO](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#RANGING_MODE_AUTO:kotlin.Int), [android.ranging.oob.OobInitiatorRangingConfig#RANGING_MODE_HIGH_ACCURACY](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#RANGING_MODE_HIGH_ACCURACY:kotlin.Int), [android.ranging.oob.OobInitiatorRangingConfig#RANGING_MODE_HIGH_ACCURACY_PREFERRED](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#RANGING_MODE_HIGH_ACCURACY_PREFERRED:kotlin.Int), or [android.ranging.oob.OobInitiatorRangingConfig#RANGING_MODE_FUSED](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#RANGING_MODE_FUSED:kotlin.Int) |

### getRangingTechnologyFilter

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRangingTechnologyFilter(): MutableSet<Int!>
```

Returns the set of ranging technologies that can be used for the session. If empty, the system may use any available technology.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!> | A non-null, possibly empty, [Set](https://developer.android.com/reference/kotlin/java/util/Set.html#) of Ranging Technology integers. |

### getSecurityLevel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSecurityLevel(): Int
```

Returns the security level set for the ranging session.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the security level. Possible values: [SECURITY_LEVEL_BASIC](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#SECURITY_LEVEL_BASIC:kotlin.Int) [SECURITY_LEVEL_SECURE](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#SECURITY_LEVEL_SECURE:kotlin.Int) Value is [android.ranging.oob.OobInitiatorRangingConfig#SECURITY_LEVEL_BASIC](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#SECURITY_LEVEL_BASIC:kotlin.Int), or [android.ranging.oob.OobInitiatorRangingConfig#SECURITY_LEVEL_SECURE](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig#SECURITY_LEVEL_SECURE:kotlin.Int) |

### getSlowestRangingInterval

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSlowestRangingInterval(): Duration
```

Returns the slowest acceptable ranging.

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------|
| [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#) | The slowest interval. This value cannot be`null`. |

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<OobInitiatorRangingConfig!>
```
