# OobInitiatorRangingConfig

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OobInitiatorRangingConfig

Kotlin| [Java](../android/ranging/oob/OobInitiatorRangingConfig.md) 
| --- | --- |

```
class OobInitiatorRangingConfig : RangingConfig, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.ranging.RangingConfig](../android/ranging/RangingConfig.md) ||
| | ↳ | [android.ranging.oob.OobInitiatorRangingConfig](../android/ranging/oob/OobInitiatorRangingConfig.md) |

Represents the configuration for an Out-of-Band (OOB) initiator in a ranging session. This class includes configuration options such as device handles, security level, ranging mode, and interval range for setting up an OOB initiator ranging session.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/ranging/oob/OobInitiatorRangingConfig.Builder.md) Builder class for creating instances of [OobInitiatorRangingConfig](../android/ranging/oob/OobInitiatorRangingConfig.md). |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANGING_MODE_AUTO](../android/ranging/oob/OobInitiatorRangingConfig.md) Automatic ranging mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANGING_MODE_FUSED](../android/ranging/oob/OobInitiatorRangingConfig.md) Starts ranging with all the ranging technologies both devices support. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANGING_MODE_HIGH_ACCURACY](../android/ranging/oob/OobInitiatorRangingConfig.md) High accuracy ranging mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANGING_MODE_HIGH_ACCURACY_PREFERRED](../android/ranging/oob/OobInitiatorRangingConfig.md) High accuracy ranging mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_LEVEL_BASIC](../android/ranging/oob/OobInitiatorRangingConfig.md) Basic security level for the ranging session. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_LEVEL_SECURE](../android/ranging/oob/OobInitiatorRangingConfig.md) Basic security level for the ranging session. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||
| From class [RangingConfig](../android/ranging/RangingConfig.md) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANGING_SESSION_OOB](../android/ranging/RangingConfig.md) <br /> Ranging session with the out-of-band negotiations performed by the ranging API. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANGING_SESSION_RAW](../android/ranging/RangingConfig.md) <br /> Ranging session with the out-of-band negotiations performed by the app. <br /> | ||

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/ranging/oob/OobInitiatorRangingConfig.md))`()` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [DeviceHandle](../android/ranging/oob/DeviceHandle.md)!\> | [getDeviceHandles](../android/ranging/oob/OobInitiatorRangingConfig.md))`()` Returns the list of DeviceHandles associated with the OOB initiator. |
| [Duration](../java/time/Duration.md) | [getFastestRangingInterval](../android/ranging/oob/OobInitiatorRangingConfig.md))`()` Returns the fastest requested ranging interval. |
| --- | --- |
| [Range](../android/util/Range.md)\< [Duration](../java/time/Duration.md)!\> | [getRangingIntervalRange](../android/ranging/oob/OobInitiatorRangingConfig.md))`()` Returns the ranging interval range configuration. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRangingMode](../android/ranging/oob/OobInitiatorRangingConfig.md))`()` Returns the ranging mode for the session. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | [getRangingTechnologyFilter](../android/ranging/oob/OobInitiatorRangingConfig.md))`()` Returns the set of ranging technologies that can be used for the session. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSecurityLevel](../android/ranging/oob/OobInitiatorRangingConfig.md))`()` Returns the security level set for the ranging session. |
| [Duration](../java/time/Duration.md) | [getSlowestRangingInterval](../android/ranging/oob/OobInitiatorRangingConfig.md))`()` Returns the slowest acceptable ranging. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/ranging/oob/OobInitiatorRangingConfig.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/ranging/oob/OobInitiatorRangingConfig.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Inherited functions ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/os/Parcelable.md))`()` <br /> Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of [writeToParcel(android.os.Parcel,int)](../android/os/Parcelable.md)), the return value of this method must include the [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) bit. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/os/Parcelable.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Flatten this object in to a Parcel. <br /> | ||
| From class [RangingConfig](../android/ranging/RangingConfig.md) |----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRangingSessionType](../android/ranging/RangingConfig.md))`()` <br /> Gets the ranging session type android.ranging.RangingConfig.RangingSessionType <br /> | ||

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [OobInitiatorRangingConfig](../android/ranging/oob/OobInitiatorRangingConfig.md)!\> | [CREATOR](../android/ranging/oob/OobInitiatorRangingConfig.md) <br /> |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getDeviceHandles

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeviceHandles(): MutableList<DeviceHandle!>
```

Returns the list of DeviceHandles associated with the OOB initiator.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [DeviceHandle](../android/ranging/oob/DeviceHandle.md)!> | A list of DeviceHandle objects. This value cannot be`null`. |

### getFastestRangingInterval

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFastestRangingInterval(): Duration
```

Returns the fastest requested ranging interval.

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------|
| [Duration](../java/time/Duration.md) | The fastest interval. This value cannot be`null`. |

### getRangingIntervalRange

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRangingIntervalRange(): Range<Duration!>
```

Returns the ranging interval range configuration.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Range](../android/util/Range.md)< [Duration](../java/time/Duration.md)!> | The [Range](../android/util/Range.md) associated with this OOB initiator. This value cannot be`null`. |

### getRangingMode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRangingMode(): Int
```

Returns the ranging mode for the session.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the ranging mode. Possible values: [RANGING_MODE_AUTO](../android/ranging/oob/OobInitiatorRangingConfig.md) [RANGING_MODE_HIGH_ACCURACY](../android/ranging/oob/OobInitiatorRangingConfig.md) [RANGING_MODE_HIGH_ACCURACY_PREFERRED](../android/ranging/oob/OobInitiatorRangingConfig.md) [RANGING_MODE_FUSED](../android/ranging/oob/OobInitiatorRangingConfig.md) Value is [android.ranging.oob.OobInitiatorRangingConfig#RANGING_MODE_AUTO](../android/ranging/oob/OobInitiatorRangingConfig.md), [android.ranging.oob.OobInitiatorRangingConfig#RANGING_MODE_HIGH_ACCURACY](../android/ranging/oob/OobInitiatorRangingConfig.md), [android.ranging.oob.OobInitiatorRangingConfig#RANGING_MODE_HIGH_ACCURACY_PREFERRED](../android/ranging/oob/OobInitiatorRangingConfig.md), or [android.ranging.oob.OobInitiatorRangingConfig#RANGING_MODE_FUSED](../android/ranging/oob/OobInitiatorRangingConfig.md) |

### getRangingTechnologyFilter

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRangingTechnologyFilter(): MutableSet<Int!>
```

Returns the set of ranging technologies that can be used for the session. If empty, the system may use any available technology.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!> | A non-null, possibly empty, [Set](../java/util/Set.md) of Ranging Technology integers. |

### getSecurityLevel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSecurityLevel(): Int
```

Returns the security level set for the ranging session.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the security level. Possible values: [SECURITY_LEVEL_BASIC](../android/ranging/oob/OobInitiatorRangingConfig.md) [SECURITY_LEVEL_SECURE](../android/ranging/oob/OobInitiatorRangingConfig.md) Value is [android.ranging.oob.OobInitiatorRangingConfig#SECURITY_LEVEL_BASIC](../android/ranging/oob/OobInitiatorRangingConfig.md), or [android.ranging.oob.OobInitiatorRangingConfig#SECURITY_LEVEL_SECURE](../android/ranging/oob/OobInitiatorRangingConfig.md) |

### getSlowestRangingInterval

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSlowestRangingInterval(): Duration
```

Returns the slowest acceptable ranging.

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------|
| [Duration](../java/time/Duration.md) | The slowest interval. This value cannot be`null`. |

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
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<OobInitiatorRangingConfig!>
```
