Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VibrationAttributes

Kotlin | [Java](https://developer.android.com/reference/android/os/VibrationAttributes "View this page in Java")

```
class VibrationAttributes : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.os.VibrationAttributes](https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#) |

Encapsulates a collection of attributes describing information about a vibration.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.Builder` Builder class for `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#` objects. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#FLAG_BYPASS_INTERRUPTION_POLICY:kotlin.Int` Flag requesting vibration effect to be played even under limited interruptions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_ACCESSIBILITY:kotlin.Int` Usage value to use for accessibility vibrations, such as with a screen reader. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_ALARM:kotlin.Int` Usage value to use for alarm vibrations. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_CLASS_ALARM:kotlin.Int` Vibration usage class value to use when the vibration is initiated to catch user's attention, such as alarm, ringtone, and notification vibrations. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_CLASS_FEEDBACK:kotlin.Int` Vibration usage class value to use when the vibration is initiated as a response to user's actions, such as emulation of physical effects, and texting feedback vibration. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_CLASS_MASK:kotlin.Int` Mask for vibration usage class value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_CLASS_MEDIA:kotlin.Int` Vibration usage class value to use when the vibration is part of media, such as music, movie, soundtrack, game or animations. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_CLASS_UNKNOWN:kotlin.Int` Vibration usage class value to use when the vibration usage class is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_COMMUNICATION_REQUEST:kotlin.Int` Usage value to use for vibrations which mean a request to enter/end a communication with the user, such as a voice prompt. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_GESTURE_INPUT:kotlin.Int` Usage value to use for vibrations performed as feedback for a user's gesture input. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_HARDWARE_FEEDBACK:kotlin.Int` Usage value to use for vibrations which provide a feedback for hardware component interaction, such as a fingerprint sensor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_MEDIA:kotlin.Int` Usage value to use for media vibrations, such as music, movie, soundtrack, animations, games, or any interactive media that isn't for touch feedback specifically. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_NOTIFICATION:kotlin.Int` Usage value to use for notification vibrations. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_PHYSICAL_EMULATION:kotlin.Int` Usage value to use for vibrations which emulate physical hardware reactions, such as edge squeeze. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_RINGTONE:kotlin.Int` Usage value to use for ringtone vibrations. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_TOUCH:kotlin.Int` Usage value to use for touch vibrations. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_UNKNOWN:kotlin.Int` Usage value to use when usage is unknown. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| static [VibrationAttributes](https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#createForUsage(kotlin.Int)(usage: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a new `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#` instance with given usage. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#getFlags()()` Return the flags. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#getUsage()()` Return the vibration usage. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#getUsageClass()()` Return the vibration usage class. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#hashCode()()` Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#isFlagSet(kotlin.Int)(flag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Check whether a flag is set |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator)\< [VibrationAttributes](https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#)!\> | `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### FLAG_BYPASS_INTERRUPTION_POLICY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_BYPASS_INTERRUPTION_POLICY: Int
```

Flag requesting vibration effect to be played even under limited interruptions.

Only privileged apps can ignore user settings that limit interruptions, and this flag will be ignored otherwise.

 Value: 1

### USAGE_ACCESSIBILITY

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_ACCESSIBILITY: Int
```

Usage value to use for accessibility vibrations, such as with a screen reader.

 Value: 66

### USAGE_ALARM

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_ALARM: Int
```

Usage value to use for alarm vibrations.

 Value: 17

### USAGE_CLASS_ALARM

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_CLASS_ALARM: Int
```

Vibration usage class value to use when the vibration is initiated to catch user's attention, such as alarm, ringtone, and notification vibrations.

 Value: 1

### USAGE_CLASS_FEEDBACK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_CLASS_FEEDBACK: Int
```

Vibration usage class value to use when the vibration is initiated as a response to user's actions, such as emulation of physical effects, and texting feedback vibration.

 Value: 2

### USAGE_CLASS_MASK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_CLASS_MASK: Int
```

Mask for vibration usage class value.

 Value: 15

### USAGE_CLASS_MEDIA

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_CLASS_MEDIA: Int
```

Vibration usage class value to use when the vibration is part of media, such as music, movie, soundtrack, game or animations.

 Value: 3

### USAGE_CLASS_UNKNOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_CLASS_UNKNOWN: Int
```

Vibration usage class value to use when the vibration usage class is unknown.

 Value: 0

### USAGE_COMMUNICATION_REQUEST

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_COMMUNICATION_REQUEST: Int
```

Usage value to use for vibrations which mean a request to enter/end a communication with the user, such as a voice prompt.

 Value: 65

### USAGE_GESTURE_INPUT

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_GESTURE_INPUT: Int
```

Usage value to use for vibrations performed as feedback for a user's gesture input.

A gesture input is broadly defined as a user input that falls outside the direct usage of a physical InputDevice. Note that the gesture input may involve interacting with an InputDevice, but the input itself is a user gesture that is not a direct application of the InputDevice.

The exact definition of a gesture input varies across form-factors and input modalities. For example, on Wearable devices, it could be a hand-based gesture provided by the user without touching any physical InputDevice. Another example is a pinch gesture on a touchscreen.

 Value: 98

### USAGE_HARDWARE_FEEDBACK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_HARDWARE_FEEDBACK: Int
```

Usage value to use for vibrations which provide a feedback for hardware component interaction, such as a fingerprint sensor.

 Value: 50

### USAGE_MEDIA

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_MEDIA: Int
```

Usage value to use for media vibrations, such as music, movie, soundtrack, animations, games, or any interactive media that isn't for touch feedback specifically.

 Value: 19

### USAGE_NOTIFICATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_NOTIFICATION: Int
```

Usage value to use for notification vibrations.

 Value: 49

### USAGE_PHYSICAL_EMULATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_PHYSICAL_EMULATION: Int
```

Usage value to use for vibrations which emulate physical hardware reactions, such as edge squeeze.

Note that normal screen-touch feedback "click" effects would typically be classed as `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_TOUCH:kotlin.Int`, and that on-screen "physical" animations like bouncing would be `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_MEDIA:kotlin.Int`.

 Value: 34

### USAGE_RINGTONE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_RINGTONE: Int
```

Usage value to use for ringtone vibrations.

 Value: 33

### USAGE_TOUCH

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_TOUCH: Int
```

Usage value to use for touch vibrations.

Most typical haptic feedback should be classed as *touch* feedback. Examples include vibrations for tap, long press, drag and scroll.

 Value: 18

### USAGE_UNKNOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USAGE_UNKNOWN: Int
```

Usage value to use when usage is unknown.

 Value: 0

## Public methods

### createForUsage

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createForUsage(usage: Int): VibrationAttributes
```

Creates a new `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#` instance with given usage.

| Parameters ||
|---|---|
| `usage` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_ACCESSIBILITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_ALARM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_COMMUNICATION_REQUEST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_HARDWARE_FEEDBACK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_MEDIA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_NOTIFICATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_PHYSICAL_EMULATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_RINGTONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_TOUCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_GESTURE_INPUT:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#` | This value cannot be `null`. |

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

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
| `o` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getFlags

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFlags(): Int
```

Return the flags.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a combined mask of all flags. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#FLAG_BYPASS_INTERRUPTION_POLICY:kotlin.Int` |

### getUsage

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUsage(): Int
```

Return the vibration usage.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_ACCESSIBILITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_ALARM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_COMMUNICATION_REQUEST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_HARDWARE_FEEDBACK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_MEDIA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_NOTIFICATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_PHYSICAL_EMULATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_RINGTONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_TOUCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_GESTURE_INPUT:kotlin.Int` |

### getUsageClass

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUsageClass(): Int
```

Return the vibration usage class.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_CLASS_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_CLASS_ALARM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_CLASS_FEEDBACK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#USAGE_CLASS_MEDIA:kotlin.Int` |

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

### isFlagSet

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isFlagSet(flag: Int): Boolean
```

Check whether a flag is set

| Parameters ||
|---|---|
| `flag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/VibrationAttributes#FLAG_BYPASS_INTERRUPTION_POLICY:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if a flag is set and false otherwise |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<VibrationAttributes!>
```
