# RangingPreference

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RangingPreference

Kotlin| [Java](https://developer.android.com/reference/android/ranging/RangingPreference "View this page in Java") 
| --- | --- |

```
class RangingPreference : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.ranging.RangingPreference](https://developer.android.com/reference/kotlin/android/ranging/RangingPreference#) |

Represents the configuration preferences for a ranging session.

The`RangingPreference`class allows users to specify various parameters required for a ranging session, including ranging parameters, sensor fusion settings, and data notification configurations. It provides a [Builder](https://developer.android.com/reference/kotlin/android/ranging/RangingPreference.Builder) to construct an instance with custom configurations.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/ranging/RangingPreference.Builder) Builder for creating instances of`RangingPreference`. |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_ROLE_INITIATOR](https://developer.android.com/reference/kotlin/android/ranging/RangingPreference#DEVICE_ROLE_INITIATOR:kotlin.Int) The device that initiates the session. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_ROLE_RESPONDER](https://developer.android.com/reference/kotlin/android/ranging/RangingPreference#DEVICE_ROLE_RESPONDER:kotlin.Int) The device that responds to a session. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/ranging/RangingPreference#describeContents())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDeviceRole](https://developer.android.com/reference/kotlin/android/ranging/RangingPreference#getDeviceRole())`()` Returns the device role. |
| [RangingConfig](https://developer.android.com/reference/kotlin/android/ranging/RangingConfig)? | [getRangingParams](https://developer.android.com/reference/kotlin/android/ranging/RangingPreference#getRangingParams())`()` Returns the ranging parameters associated with this preference. |
| --- | --- |
| [SessionConfig](https://developer.android.com/reference/kotlin/android/ranging/SessionConfig) | [getSessionConfig](https://developer.android.com/reference/kotlin/android/ranging/RangingPreference#getSessionConfig())`()` Returns the ranging session configuration params. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/ranging/RangingPreference#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/ranging/RangingPreference#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [RangingPreference](https://developer.android.com/reference/kotlin/android/ranging/RangingPreference#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/ranging/RangingPreference#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### DEVICE_ROLE_INITIATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_ROLE_INITIATOR: Int
```

The device that initiates the session. 

 Value: 1

### DEVICE_ROLE_RESPONDER

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_ROLE_RESPONDER: Int
```

The device that responds to a session. 

 Value: 0

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getDeviceRole

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeviceRole(): Int
```

Returns the device role.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.ranging.RangingPreference#DEVICE_ROLE_RESPONDER](https://developer.android.com/reference/kotlin/android/ranging/RangingPreference#DEVICE_ROLE_RESPONDER:kotlin.Int), or [android.ranging.RangingPreference#DEVICE_ROLE_INITIATOR](https://developer.android.com/reference/kotlin/android/ranging/RangingPreference#DEVICE_ROLE_INITIATOR:kotlin.Int) |

### getRangingParams

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRangingParams(): RangingConfig?
```

Returns the ranging parameters associated with this preference.

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [RangingConfig](https://developer.android.com/reference/kotlin/android/ranging/RangingConfig)? | the [RangingConfig](https://developer.android.com/reference/kotlin/android/ranging/RangingConfig) or`null`if not set. |

### getSessionConfig

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSessionConfig(): SessionConfig
```

Returns the ranging session configuration params.

| Return ||
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [SessionConfig](https://developer.android.com/reference/kotlin/android/ranging/SessionConfig) | a non-null [SessionConfig](https://developer.android.com/reference/kotlin/android/ranging/SessionConfig) instance. |

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
static val CREATOR: Parcelable.Creator<RangingPreference!>
```
