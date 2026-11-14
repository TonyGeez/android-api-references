Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PollingFrame

Kotlin | [Java](PollingFrame.md)
| --- | --- |

```
class PollingFrame : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.cardemulation.PollingFrame](PollingFrame.md) |

Polling Frames represent data about individual frames of an NFC polling loop. These frames will be delivered to subclasses of HostApduService that have registered filters with registerPollingLoopFilterForService that match a given frame in a loop and will be delivered through calls to processPollingFrames.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/PollingFrame#POLLING_LOOP_TYPE_A:kotlin.Int` POLLING_LOOP_TYPE_A is the value associated with the key POLLING_LOOP_TYPE in the Bundle passed to processPollingFrames when the polling loop is for NFC-A. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/PollingFrame#POLLING_LOOP_TYPE_B:kotlin.Int` POLLING_LOOP_TYPE_B is the value associated with the key POLLING_LOOP_TYPE in the Bundle passed to processPollingFrames when the polling loop is for NFC-B. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/PollingFrame#POLLING_LOOP_TYPE_F:kotlin.Int` POLLING_LOOP_TYPE_F is the value associated with the key POLLING_LOOP_TYPE in the Bundle passed to processPollingFrames when the polling loop is for NFC-F. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/PollingFrame#POLLING_LOOP_TYPE_OFF:kotlin.Int` POLLING_LOOP_TYPE_OFF is the value associated with the key POLLING_LOOP_TYPE in the Bundle passed to processPollingFrames when the polling loop turns off. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/PollingFrame#POLLING_LOOP_TYPE_ON:kotlin.Int` POLLING_LOOP_TYPE_ON is the value associated with the key POLLING_LOOP_TYPE in the Bundle passed to processPollingFrames when the polling loop turns on. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/PollingFrame#POLLING_LOOP_TYPE_UNKNOWN:kotlin.Int` POLLING_LOOP_TYPE_UNKNOWN is the value associated with the key POLLING_LOOP_TYPE in the Bundle passed to processPollingFrames when the polling loop frame isn't recognized. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | getData Returns the raw data from the polling type frame. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getTimestamp Returns the timestamp of when the polling loop frame was observed, in microseconds. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getTriggeredAutoTransact Returns whether this frame triggered the device to automatically disable observe mode and allow one transaction. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getType Returns the type of frame for this polling loop frame. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getVendorSpecificGain Returns the gain representing the field strength of the NFC field when this polling loop frame was observed. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PollingFrame](PollingFrame.md)!\> | `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/PollingFrame#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### POLLING_LOOP_TYPE_A

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val POLLING_LOOP_TYPE_A: Int
```

POLLING_LOOP_TYPE_A is the value associated with the key POLLING_LOOP_TYPE in the Bundle passed to processPollingFrames when the polling loop is for NFC-A.

 Value: 65

### POLLING_LOOP_TYPE_B

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val POLLING_LOOP_TYPE_B: Int
```

POLLING_LOOP_TYPE_B is the value associated with the key POLLING_LOOP_TYPE in the Bundle passed to processPollingFrames when the polling loop is for NFC-B.

 Value: 66

### POLLING_LOOP_TYPE_F

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val POLLING_LOOP_TYPE_F: Int
```

POLLING_LOOP_TYPE_F is the value associated with the key POLLING_LOOP_TYPE in the Bundle passed to processPollingFrames when the polling loop is for NFC-F.

 Value: 70

### POLLING_LOOP_TYPE_OFF

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val POLLING_LOOP_TYPE_OFF: Int
```

POLLING_LOOP_TYPE_OFF is the value associated with the key POLLING_LOOP_TYPE in the Bundle passed to processPollingFrames when the polling loop turns off.

 Value: 88

### POLLING_LOOP_TYPE_ON

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val POLLING_LOOP_TYPE_ON: Int
```

POLLING_LOOP_TYPE_ON is the value associated with the key POLLING_LOOP_TYPE in the Bundle passed to processPollingFrames when the polling loop turns on.

 Value: 79

### POLLING_LOOP_TYPE_UNKNOWN

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val POLLING_LOOP_TYPE_UNKNOWN: Int
```

POLLING_LOOP_TYPE_UNKNOWN is the value associated with the key POLLING_LOOP_TYPE in the Bundle passed to processPollingFrames when the polling loop frame isn't recognized.

 Value: 85

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getData

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getData(): ByteArray
```

Returns the raw data from the polling type frame.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | This value cannot be `null`. |

### getTimestamp

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTimestamp(): Long
```

Returns the timestamp of when the polling loop frame was observed, in microseconds. These timestamps are relative and should only be used for comparing the timing of frames relative to each other.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the timestamp in microseconds |

### getTriggeredAutoTransact

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTriggeredAutoTransact(): Boolean
```

Returns whether this frame triggered the device to automatically disable observe mode and allow one transaction.

### getType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getType(): Int
```

Returns the type of frame for this polling loop frame. The possible return values are:

- `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/PollingFrame#POLLING_LOOP_TYPE_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/PollingFrame#POLLING_LOOP_TYPE_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/PollingFrame#POLLING_LOOP_TYPE_A:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/PollingFrame#POLLING_LOOP_TYPE_B:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/PollingFrame#POLLING_LOOP_TYPE_F:kotlin.Int`

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/PollingFrame#POLLING_LOOP_TYPE_A:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/PollingFrame#POLLING_LOOP_TYPE_B:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/PollingFrame#POLLING_LOOP_TYPE_F:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/PollingFrame#POLLING_LOOP_TYPE_OFF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/PollingFrame#POLLING_LOOP_TYPE_ON:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/nfc/cardemulation/PollingFrame#POLLING_LOOP_TYPE_UNKNOWN:kotlin.Int` |

### getVendorSpecificGain

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVendorSpecificGain(): Int
```

Returns the gain representing the field strength of the NFC field when this polling loop frame was observed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the gain or -1 if there is no gain measurement associated with this frame. |

### toString

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

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
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<PollingFrame!>
```
