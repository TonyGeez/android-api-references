# RangingConfig

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RangingConfig

Kotlin | [Java](https://developer.android.com/reference/android/ranging/RangingConfig "View this page in Java") 

```
abstract class RangingConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.ranging.RangingConfig](https://developer.android.com/reference/kotlin/android/ranging/RangingConfig#) |

| Known Direct Subclasses [OobInitiatorRangingConfig](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig), [OobResponderRangingConfig](https://developer.android.com/reference/kotlin/android/ranging/oob/OobResponderRangingConfig), [RawInitiatorRangingConfig](https://developer.android.com/reference/kotlin/android/ranging/raw/RawInitiatorRangingConfig), [RawResponderRangingConfig](https://developer.android.com/reference/kotlin/android/ranging/raw/RawResponderRangingConfig) |---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------| | [OobInitiatorRangingConfig](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig) | Represents the configuration for an Out-of-Band (OOB) initiator in a ranging session. | | [OobResponderRangingConfig](https://developer.android.com/reference/kotlin/android/ranging/oob/OobResponderRangingConfig) | Represents the configuration for an Out-of-Band (OOB) responder in a ranging session. | | [RawInitiatorRangingConfig](https://developer.android.com/reference/kotlin/android/ranging/raw/RawInitiatorRangingConfig) | Represents the configuration for initiating a raw ranging session. | | [RawResponderRangingConfig](https://developer.android.com/reference/kotlin/android/ranging/raw/RawResponderRangingConfig) | Represents the configuration for a raw ranging session initiated by a responder device. | |

Abstract class to represent type of ranging configuration.

Subclasses include:

- [RawResponderRangingConfig](https://developer.android.com/reference/kotlin/android/ranging/raw/RawResponderRangingConfig)
- [RawInitiatorRangingConfig](https://developer.android.com/reference/kotlin/android/ranging/raw/RawInitiatorRangingConfig)
- [OobResponderRangingConfig](https://developer.android.com/reference/kotlin/android/ranging/oob/OobResponderRangingConfig)
- [OobInitiatorRangingConfig](https://developer.android.com/reference/kotlin/android/ranging/oob/OobInitiatorRangingConfig)

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANGING_SESSION_OOB](https://developer.android.com/reference/kotlin/android/ranging/RangingConfig#RANGING_SESSION_OOB:kotlin.Int) Ranging session with the out-of-band negotiations performed by the ranging API. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANGING_SESSION_RAW](https://developer.android.com/reference/kotlin/android/ranging/RangingConfig#RANGING_SESSION_RAW:kotlin.Int) Ranging session with the out-of-band negotiations performed by the app. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Protected constructors ||
|--------------------------------------------------------------------------------------------------------------------------|---|
| [RangingConfig](https://developer.android.com/reference/kotlin/android/ranging/RangingConfig#RangingConfig())`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRangingSessionType](https://developer.android.com/reference/kotlin/android/ranging/RangingConfig#getRangingSessionType())`()` Gets the ranging session type android. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/ranging/RangingConfig#toString())`()` <br /> |

| Inherited functions ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents())`()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of [writeToParcel(android.os.Parcel,int)](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)), the return value of this method must include the [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) bit. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. <br /> | ||

## Constants

### RANGING_SESSION_OOB

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RANGING_SESSION_OOB: Int
```

Ranging session with the out-of-band negotiations performed by the ranging API. 

 Value: 1

### RANGING_SESSION_RAW

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RANGING_SESSION_RAW: Int
```

Ranging session with the out-of-band negotiations performed by the app. 

 Value: 0

## Protected constructors

### RangingConfig

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected RangingConfig()
```

## Public methods

### getRangingSessionType

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRangingSessionType(): Int
```

Gets the ranging session type android.ranging.RangingConfig.RangingSessionType

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the type of ranging session. |

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
