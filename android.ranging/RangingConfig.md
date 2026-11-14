# RangingConfig

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RangingConfig

Kotlin | [Java](../android/ranging/RangingConfig.md) 
| --- | --- |

```
abstract class RangingConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.ranging.RangingConfig](../android/ranging/RangingConfig.md) |

| Known Direct Subclasses [OobInitiatorRangingConfig](../android/ranging/oob/OobInitiatorRangingConfig.md), [OobResponderRangingConfig](../android/ranging/oob/OobResponderRangingConfig.md), [RawInitiatorRangingConfig](../android/ranging/raw/RawInitiatorRangingConfig.md), [RawResponderRangingConfig](../android/ranging/raw/RawResponderRangingConfig.md) |---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------| | [OobInitiatorRangingConfig](../android/ranging/oob/OobInitiatorRangingConfig.md) | Represents the configuration for an Out-of-Band (OOB) initiator in a ranging session. | | [OobResponderRangingConfig](../android/ranging/oob/OobResponderRangingConfig.md) | Represents the configuration for an Out-of-Band (OOB) responder in a ranging session. | | [RawInitiatorRangingConfig](../android/ranging/raw/RawInitiatorRangingConfig.md) | Represents the configuration for initiating a raw ranging session. | | [RawResponderRangingConfig](../android/ranging/raw/RawResponderRangingConfig.md) | Represents the configuration for a raw ranging session initiated by a responder device. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Abstract class to represent type of ranging configuration.

Subclasses include:

- [RawResponderRangingConfig](../android/ranging/raw/RawResponderRangingConfig.md)
- [RawInitiatorRangingConfig](../android/ranging/raw/RawInitiatorRangingConfig.md)
- [OobResponderRangingConfig](../android/ranging/oob/OobResponderRangingConfig.md)
- [OobInitiatorRangingConfig](../android/ranging/oob/OobInitiatorRangingConfig.md)

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANGING_SESSION_OOB](../android/ranging/RangingConfig.md) Ranging session with the out-of-band negotiations performed by the ranging API. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RANGING_SESSION_RAW](../android/ranging/RangingConfig.md) Ranging session with the out-of-band negotiations performed by the app. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Protected constructors ||
|--------------------------------------------------------------------------------------------------------------------------|---|
| [RangingConfig](../android/ranging/RangingConfig.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRangingSessionType](../android/ranging/RangingConfig.md))`()` Gets the ranging session type android. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/ranging/RangingConfig.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/os/Parcelable.md))`()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of [writeToParcel(android.os.Parcel,int)](../android/os/Parcelable.md)), the return value of this method must include the [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) bit. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/os/Parcelable.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. <br /> | ||

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
