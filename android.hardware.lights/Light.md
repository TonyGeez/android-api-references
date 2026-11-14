Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Light

```
class Light : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.lights.Light](Light.md) |

Represents a logical light on the device.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/lights/Light#LIGHT_CAPABILITY_ANIMATION:kotlin.Int` Capability for lights that support animations and fast transitions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/lights/Light#LIGHT_CAPABILITY_BRIGHTNESS:kotlin.Int` Capability for lights that could adjust its LED brightness. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/lights/Light#LIGHT_CAPABILITY_COLOR_RGB:kotlin.Int` Capability for lights that have red, green and blue LEDs to control the light's color. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/lights/Light#LIGHT_CAPABILITY_RGB:kotlin.Int` Capability for lights that have red, green and blue LEDs to control the light's color. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/lights/Light#LIGHT_TYPE_APPLICATION:kotlin.Int` Type for lights that indicate application driven use cases. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/lights/Light#LIGHT_TYPE_INPUT:kotlin.Int` Type for lights that indicate a monochrome color LED light. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/lights/Light#LIGHT_TYPE_KEYBOARD_BACKLIGHT:kotlin.Int` Type for lights that illuminate keyboard keys. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/lights/Light#LIGHT_TYPE_MICROPHONE:kotlin.Int` Type for lights that indicate microphone usage |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/lights/Light#LIGHT_TYPE_PLAYER_ID:kotlin.Int` Type for lights that indicate a group of LED lights representing player id. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Implement the Parcelable interface |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getId Returns the id of the light. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getMinUpdatePeriodMillis Returns the minimum update period supported by the light. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getName Returns the name of the light. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getOrdinal Returns the ordinal of the light. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getType Returns the logical type of the light. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasAnimationControl Check whether the light has animation capabilities. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasBrightnessControl Check whether the light has led brightness control. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasRgbControl Check whether the light has RGB led control. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Implement the Parcelable interface |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Light](Light.md)!\> | `https://developer.android.com/reference/kotlin/android/hardware/lights/Light#CREATOR:android.os.Parcelable.Creator` Implement the Parcelable interface |

## Constants

### LIGHT_CAPABILITY_ANIMATION

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LIGHT_CAPABILITY_ANIMATION: Int
```

Capability for lights that support animations and fast transitions.

 Value: 4

### LIGHT_CAPABILITY_BRIGHTNESS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LIGHT_CAPABILITY_BRIGHTNESS: Int
```

Capability for lights that could adjust its LED brightness. If the capability is not present the LED can only be turned either on or off.

 Value: 1

### LIGHT_CAPABILITY_COLOR_RGB

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LIGHT_CAPABILITY_COLOR_RGB: Int
```

Capability for lights that have red, green and blue LEDs to control the light's color.

 Value: 2

### LIGHT_CAPABILITY_RGB

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LIGHT_CAPABILITY_RGB: Int
```

**Deprecated:** *Wrong int based flag with value 0. Use capability flag `LIGHT_CAPABILITY_COLOR_RGB` instead.*

Capability for lights that have red, green and blue LEDs to control the light's color.

 Value: 0

### LIGHT_TYPE_APPLICATION

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LIGHT_TYPE_APPLICATION: Int
```

Type for lights that indicate application driven use cases.

 Value: 10

### LIGHT_TYPE_INPUT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LIGHT_TYPE_INPUT: Int
```

Type for lights that indicate a monochrome color LED light.

 Value: 10001

### LIGHT_TYPE_KEYBOARD_BACKLIGHT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LIGHT_TYPE_KEYBOARD_BACKLIGHT: Int
```

Type for lights that illuminate keyboard keys.

 Value: 10003

### LIGHT_TYPE_MICROPHONE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LIGHT_TYPE_MICROPHONE: Int
```

Type for lights that indicate microphone usage

 Value: 8

### LIGHT_TYPE_PLAYER_ID

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LIGHT_TYPE_PLAYER_ID: Int
```

Type for lights that indicate a group of LED lights representing player id. Player id lights normally present on game controllers are lights that consist of a row of LEDs. During multi-player game, the player id for the current game controller is represented by one of the LED that is lit according to its position in the row.

 Value: 10002

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Implement the Parcelable interface

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
| `obj` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getId(): Int
```

Returns the id of the light.

This is an opaque value used as a unique identifier for the light.

### getMinUpdatePeriodMillis

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMinUpdatePeriodMillis(): Long
```

Returns the minimum update period supported by the light. This corresponds to the inverse of the maximum supported fps for the light.

A value of 0 means that the light does not support animations and applications should not use effects on the light. 
Value is a non-negative duration in milliseconds.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the minimum period, in milliseconds, or 0 if the light does not support effects. Value is a non-negative duration in milliseconds. |

### getName

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getName(): String
```

Returns the name of the light.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getOrdinal

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOrdinal(): Int
```

Returns the ordinal of the light.

This is a sort key that represents the physical order of lights on the device with the same type. In the case of multiple lights arranged in a line, for example, the ordinals could be \[1, 2, 3, 4\], or \[0, 10, 20, 30\], or any other values that have the same sort order.

### getType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getType(): Int
```

Returns the logical type of the light.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/lights/Light#LIGHT_TYPE_MICROPHONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/lights/Light#LIGHT_TYPE_INPUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/lights/Light#LIGHT_TYPE_PLAYER_ID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/lights/Light#LIGHT_TYPE_KEYBOARD_BACKLIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/lights/Light#LIGHT_TYPE_APPLICATION:kotlin.Int` |

### hasAnimationControl

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasAnimationControl(): Boolean
```

Check whether the light has animation capabilities.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the hardware supports animations, otherwise false. |

**See Also**

- MultiLightEffect

### hasBrightnessControl

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasBrightnessControl(): Boolean
```

Check whether the light has led brightness control.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the hardware can control the led brightness, otherwise false. |

### hasRgbControl

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasRgbControl(): Boolean
```

Check whether the light has RGB led control.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the hardware can control the RGB led, otherwise false. |

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the equals method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the equals method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Implement the Parcelable interface

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<Light!>
```

Implement the Parcelable interface
