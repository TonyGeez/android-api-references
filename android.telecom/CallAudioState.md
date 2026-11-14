Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CallAudioState

Kotlin | [Java](CallAudioState.md)
| --- | --- |

```
class CallAudioState : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telecom.CallAudioState](CallAudioState.md) |

Encapsulates the telecom audio state, including the current audio routing, supported audio routing and mute.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_BLUETOOTH:kotlin.Int` Direct the audio stream through Bluetooth. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_EARPIECE:kotlin.Int` Direct the audio stream through the device's earpiece. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_SPEAKER:kotlin.Int` Direct the audio stream through the device's speakerphone. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_STREAMING:kotlin.Int` Direct the audio stream through another device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_WIRED_HEADSET:kotlin.Int` Direct the audio stream through a wired headset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_WIRED_OR_EARPIECE:kotlin.Int` Direct the audio stream through the device's earpiece or wired headset if one is connected. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#CallAudioState(kotlin.Boolean,%20kotlin.Int,%20kotlin.Int)(muted: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, route: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, supportedRouteMask: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructor for a `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#` object. |

| Public methods ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#audioRouteToString(kotlin.Int)(route: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Converts the provided audio route into a human readable string representation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| --- | --- |
| [BluetoothDevice](../android.bluetooth/BluetoothDevice.md)! | `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#getActiveBluetoothDevice()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#getRoute()()` <br /> |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [BluetoothDevice](../android.bluetooth/BluetoothDevice.md)!\>! | `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#getSupportedBluetoothDevices()()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#getSupportedRouteMask()()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#isMuted()()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#toString()()` Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#writeToParcel(android.os.Parcel,%20kotlin.Int)(destination: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Writes AudioState object into a serializeable Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [CallAudioState](CallAudioState.md)!\> | `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#CREATOR:android.os.Parcelable.Creator` Responsible for creating AudioState objects for deserialized Parcels. |

## Constants

### ROUTE_BLUETOOTH

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROUTE_BLUETOOTH: Int
```

Direct the audio stream through Bluetooth.

 Value: 2

### ROUTE_EARPIECE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROUTE_EARPIECE: Int
```

Direct the audio stream through the device's earpiece.

 Value: 1

### ROUTE_SPEAKER

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROUTE_SPEAKER: Int
```

Direct the audio stream through the device's speakerphone.

 Value: 8

### ROUTE_STREAMING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROUTE_STREAMING: Int
```

Direct the audio stream through another device.

 Value: 16

### ROUTE_WIRED_HEADSET

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROUTE_WIRED_HEADSET: Int
```

Direct the audio stream through a wired headset.

 Value: 4

### ROUTE_WIRED_OR_EARPIECE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROUTE_WIRED_OR_EARPIECE: Int
```

Direct the audio stream through the device's earpiece or wired headset if one is connected.

 Value: 5

## Public constructors

### CallAudioState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CallAudioState(
    muted: Boolean, 
    route: Int, 
    supportedRouteMask: Int)
```

Constructor for a `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#` object.

| Parameters ||
|---|---|
| `muted` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the call is muted, `false` otherwise. |
| `route` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The current audio route being used. Allowed values: `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_EARPIECE:kotlin.Int` `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_BLUETOOTH:kotlin.Int` `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_WIRED_HEADSET:kotlin.Int` `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_SPEAKER:kotlin.Int` Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_EARPIECE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_BLUETOOTH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_WIRED_HEADSET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_SPEAKER:kotlin.Int` |
| `supportedRouteMask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Bit mask of all routes supported by this call. This should be a bitwise combination of the following values: `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_EARPIECE:kotlin.Int` `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_BLUETOOTH:kotlin.Int` `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_WIRED_HEADSET:kotlin.Int` `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_SPEAKER:kotlin.Int` Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_EARPIECE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_BLUETOOTH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_WIRED_HEADSET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_SPEAKER:kotlin.Int` |
| --- | --- |

## Public methods

### audioRouteToString

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun audioRouteToString(route: Int): String!
```

Converts the provided audio route into a human readable string representation.

| Parameters ||
|---|---|
| `route` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): to convert into a string. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | String representation of the provided audio route. |

### describeContents

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### getActiveBluetoothDevice

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getActiveBluetoothDevice(): BluetoothDevice!
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#!` | The `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#` through which audio is being routed. Will not be `null` if `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#getRoute()` returns `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_BLUETOOTH:kotlin.Int`. |

### getRoute

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRoute(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The current audio route being used. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_EARPIECE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_BLUETOOTH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_WIRED_HEADSET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_SPEAKER:kotlin.Int` |

### getSupportedBluetoothDevices

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSupportedBluetoothDevices(): MutableCollection<BluetoothDevice!>!
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#!>!` | `https://developer.android.com/reference/kotlin/java/util/List.html#` of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#`s that can be used for this call. |

### getSupportedRouteMask

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSupportedRouteMask(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Bit mask of all routes supported by this call. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_EARPIECE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_BLUETOOTH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_WIRED_HEADSET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallAudioState#ROUTE_SPEAKER:kotlin.Int` |

### isMuted

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isMuted(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the call is muted, `false` otherwise. |

### toString

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    destination: Parcel, 
    flags: Int
): Unit
```

Writes AudioState object into a serializeable Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<CallAudioState!>
```

Responsible for creating AudioState objects for deserialized Parcels.
