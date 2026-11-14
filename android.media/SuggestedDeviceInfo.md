Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SuggestedDeviceInfo

Kotlin | [Java](SuggestedDeviceInfo.md)
| --- | --- |

```
class SuggestedDeviceInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.SuggestedDeviceInfo](SuggestedDeviceInfo.md) |

Allows applications to suggest routes to the system UI (for example, in the System UI Output Switcher).

Suggested devices are used to transfer the current media session from one device to another.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/media/SuggestedDeviceInfo.Builder` Builder for SuggestedDeviceInfo. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Indicates whether some other object is "equal to" this one. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getDeviceDisplayName Returns the name to be displayed to the user. |
| --- | --- |
| [Bundle](../android.os/Bundle.md) | getExtras Returns the extras associated with the suggestion. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getRouteId Returns the route ID associated with the suggestion. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getType Returns the device type associated with the suggestion. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SuggestedDeviceInfo](SuggestedDeviceInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/media/SuggestedDeviceInfo#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public methods

### describeContents

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getDeviceDisplayName

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDeviceDisplayName(): String
```

Returns the name to be displayed to the user.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The device display name. This value cannot be `null`. |

### getExtras

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExtras(): Bundle
```

Returns the extras associated with the suggestion.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` | The extras. This value cannot be `null`. |

### getRouteId

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRouteId(): String
```

Returns the route ID associated with the suggestion.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The route ID. This value cannot be `null`. |

### getType

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getType(): Int
```

Returns the device type associated with the suggestion.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The device type. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_BUILTIN_SPEAKER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_WIRED_HEADSET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_WIRED_HEADPHONES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_BLUETOOTH_A2DP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_HDMI:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_HDMI_ARC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_HDMI_EARC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_LINE_DIGITAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_LINE_ANALOG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_AUX_LINE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_USB_DEVICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_USB_ACCESSORY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_DOCK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_USB_HEADSET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_HEARING_AID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_BLE_HEADSET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_MULTICHANNEL_SPEAKER_GROUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_TV:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_SPEAKER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_AUDIO_VIDEO_RECEIVER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_TABLET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_TABLET_DOCKED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_COMPUTER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_GAME_CONSOLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_CAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_SMARTWATCH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_SMARTPHONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_GROUP:kotlin.Int` |

### hashCode

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<SuggestedDeviceInfo!>
```
