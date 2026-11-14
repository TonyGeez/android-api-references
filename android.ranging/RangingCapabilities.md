Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RangingCapabilities

```
class RangingCapabilities : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.ranging.RangingCapabilities](https://developer.android.com/reference/kotlin/android/ranging/RangingCapabilities#) |

Represents the capabilities and availability of various ranging technologies.

The `RangingCapabilities` class encapsulates the status of different ranging technologies. It also allows querying the availability of other ranging technologies through a mapping of technology identifiers to availability statuses.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/RangingCapabilities#DISABLED_REGULATORY:kotlin.Int` Indicates that the ranging technology is disabled due to regulatory restrictions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/RangingCapabilities#DISABLED_USER:kotlin.Int` Indicates that the ranging technology is disabled by the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/RangingCapabilities#DISABLED_USER_RESTRICTIONS:kotlin.Int` Indicates that the ranging technology is disabled due to device usage restrictions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/RangingCapabilities#ENABLED:kotlin.Int` Indicates that the ranging technology is enabled and available for use. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/RangingCapabilities#NOT_SUPPORTED:kotlin.Int` Indicates that the ranging technology is not supported on the current device. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/RangingCapabilities#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/RangingCapabilities#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [BleCsRangingCapabilities](https://developer.android.com/reference/kotlin/android/ranging/ble/cs/BleCsRangingCapabilities)? | `https://developer.android.com/reference/kotlin/android/ranging/RangingCapabilities#getCsCapabilities()()` Gets the BLE channel sounding ranging capabilities. |
| [RttRangingCapabilities](https://developer.android.com/reference/kotlin/android/ranging/wifi/rtt/RttRangingCapabilities)? | `https://developer.android.com/reference/kotlin/android/ranging/RangingCapabilities#getRttRangingCapabilities()()` Gets the WiFi NAN-RTT ranging capabilities. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/ranging/RangingCapabilities#getTechnologyAvailability()()` Gets a map containing the availability of various ranging technologies. |
| [UwbRangingCapabilities](https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingCapabilities)? | `https://developer.android.com/reference/kotlin/android/ranging/RangingCapabilities#getUwbCapabilities()()` Gets the UWB ranging capabilities. |
| [WifiPdRangingCapabilities](https://developer.android.com/reference/kotlin/android/ranging/wifi/pd/WifiPdRangingCapabilities)? | `https://developer.android.com/reference/kotlin/android/ranging/RangingCapabilities#getWifiPdRangingCapabilities()()` Gets the WiFi PD ranging capabilities. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/RangingCapabilities#hashCode()()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/RangingCapabilities#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/RangingCapabilities#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [RangingCapabilities](https://developer.android.com/reference/kotlin/android/ranging/RangingCapabilities#)!\> | `https://developer.android.com/reference/kotlin/android/ranging/RangingCapabilities#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### DISABLED_REGULATORY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISABLED_REGULATORY: Int
```

Indicates that the ranging technology is disabled due to regulatory restrictions.

 Value: 2

### DISABLED_USER

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISABLED_USER: Int
```

Indicates that the ranging technology is disabled by the user.

 Value: 1

### DISABLED_USER_RESTRICTIONS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISABLED_USER_RESTRICTIONS: Int
```

Indicates that the ranging technology is disabled due to device usage restrictions.

 Value: 4

### ENABLED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENABLED: Int
```

Indicates that the ranging technology is enabled and available for use.

 Value: 3

### NOT_SUPPORTED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NOT_SUPPORTED: Int
```

Indicates that the ranging technology is not supported on the current device.

 Value: 0

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### getCsCapabilities

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCsCapabilities(): BleCsRangingCapabilities?
```

Gets the BLE channel sounding ranging capabilities.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/ranging/ble/cs/BleCsRangingCapabilities?` | a `https://developer.android.com/reference/kotlin/android/ranging/ble/cs/BleCsRangingCapabilities` object or `null` if not available. |

### getRttRangingCapabilities

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRttRangingCapabilities(): RttRangingCapabilities?
```

Gets the WiFi NAN-RTT ranging capabilities.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/ranging/wifi/rtt/RttRangingCapabilities?` | a `https://developer.android.com/reference/kotlin/android/ranging/wifi/rtt/RttRangingCapabilities` object or `null` if not available. |

### getTechnologyAvailability

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTechnologyAvailability(): MutableMap<Int!, Int!>
```

Gets a map containing the availability of various ranging technologies.

The map uses technology identifiers as keys and their respective availability statuses as values.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | a `https://developer.android.com/reference/kotlin/java/util/Map.html#` with key android.ranging.RangingManager.RangingTechnology and value android.ranging.RangingCapabilities.RangingTechnologyAvailability. This value cannot be `null`. |

### getUwbCapabilities

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUwbCapabilities(): UwbRangingCapabilities?
```

Gets the UWB ranging capabilities.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingCapabilities?` | a `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingCapabilities` object or `null` if not available. |

### getWifiPdRangingCapabilities

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getWifiPdRangingCapabilities(): WifiPdRangingCapabilities?
```

Gets the WiFi PD ranging capabilities.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/ranging/wifi/pd/WifiPdRangingCapabilities?` | a `https://developer.android.com/reference/kotlin/android/ranging/wifi/pd/WifiPdRangingCapabilities` object or `null` if not available. |

### hashCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

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
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<RangingCapabilities!>
```
