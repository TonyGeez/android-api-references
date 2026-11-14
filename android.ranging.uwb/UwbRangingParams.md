Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UwbRangingParams

```
class UwbRangingParams : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.ranging.uwb.UwbRangingParams](UwbRangingParams.md) |

UwbRangingParams encapsulates the parameters required for a UWB ranging session.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams.Builder` Builder class for creating instances of `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#` |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#CONFIG_MULTICAST_DS_TWR:kotlin.Int` FiRa-defined multicast `STATIC STS DS-TWR` ranging, deferred mode, ranging interval Fast (120ms), Normal (200ms), Infrequent (600ms) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#CONFIG_PROVISIONED_INDIVIDUAL_MULTICAST_DS_TWR:kotlin.Int` Same as `CONFIG_UNICAST_DS_TWR`, except P-STS individual controlee key mode is enabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#CONFIG_PROVISIONED_MULTICAST_DS_TWR:kotlin.Int` Same as `CONFIG_MULTICAST_DS_TWR`, except P-STS security mode is enabled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#CONFIG_PROVISIONED_UNICAST_DS_TWR:kotlin.Int` Same as `CONFIG_UNICAST_DS_TWR`, except P-STS security mode is enabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#CONFIG_PROVISIONED_UNICAST_DS_TWR_VERY_FAST:kotlin.Int` Same as `CONFIG_ID_3`, except fast ranging interval is 96 milliseconds. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#CONFIG_UNICAST_DS_TWR:kotlin.Int` FiRa-defined unicast `STATIC STS DS-TWR` ranging, deferred mode, ranging interval Fast (120ms), Normal (240ms), Infrequent (600ms) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#DURATION_1_MS:kotlin.Int` 1 millisecond slot duration |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#DURATION_2_MS:kotlin.Int` 2 millisecond slot duration |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#SUB_SESSION_UNDEFINED:kotlin.Int` Sub session id not applicable. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [UwbComplexChannel](UwbComplexChannel.md) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#getComplexChannel()()` Gets the complex channel information for this session. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#getConfigId()()` Gets the configuration ID associated with this session. |
| [UwbAddress](UwbAddress.md) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#getDeviceAddress()()` Gets the UWB address of the device. |
| [UwbAddress](UwbAddress.md) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#getPeerAddress()()` Returns the UwbAddress of the peer device. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#getRangingUpdateRate()()` Returns the update rate for ranging operations. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#getSessionId()()` Gets the session ID associated with this ranging session. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#getSessionKeyInfo()()` Gets session key information, if available. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#getSlotDuration()()` Returns slot duration of the session. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#getSubSessionId()()` Gets the sub-session ID if applicable for the session. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#getSubSessionKeyInfo()()` Gets sub-session key information, if available. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#hashCode()()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [UwbRangingParams](UwbRangingParams.md)!\> | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### CONFIG_MULTICAST_DS_TWR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_MULTICAST_DS_TWR: Int
```

FiRa-defined multicast `STATIC STS DS-TWR` ranging, deferred mode, ranging interval Fast (120ms), Normal (200ms), Infrequent (600ms)

 Value: 2

### CONFIG_PROVISIONED_INDIVIDUAL_MULTICAST_DS_TWR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_PROVISIONED_INDIVIDUAL_MULTICAST_DS_TWR: Int
```

Same as `CONFIG_UNICAST_DS_TWR`, except P-STS individual controlee key mode is enabled.

 Value: 5

### CONFIG_PROVISIONED_MULTICAST_DS_TWR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_PROVISIONED_MULTICAST_DS_TWR: Int
```

Same as `CONFIG_MULTICAST_DS_TWR`, except P-STS security mode is enabled.

 Value: 4

### CONFIG_PROVISIONED_UNICAST_DS_TWR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_PROVISIONED_UNICAST_DS_TWR: Int
```

Same as `CONFIG_UNICAST_DS_TWR`, except P-STS security mode is enabled.

 Value: 3

### CONFIG_PROVISIONED_UNICAST_DS_TWR_VERY_FAST

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_PROVISIONED_UNICAST_DS_TWR_VERY_FAST: Int
```

Same as `CONFIG_ID_3`, except fast ranging interval is 96 milliseconds.

 Value: 6

### CONFIG_UNICAST_DS_TWR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONFIG_UNICAST_DS_TWR: Int
```

FiRa-defined unicast `STATIC STS DS-TWR` ranging, deferred mode, ranging interval Fast (120ms), Normal (240ms), Infrequent (600ms)

 Value: 1

### DURATION_1_MS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DURATION_1_MS: Int
```

1 millisecond slot duration

 Value: 1

### DURATION_2_MS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DURATION_2_MS: Int
```

2 millisecond slot duration

 Value: 2

### SUB_SESSION_UNDEFINED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUB_SESSION_UNDEFINED: Int
```

Sub session id not applicable.

 Value: -1

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

### getComplexChannel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getComplexChannel(): UwbComplexChannel
```

Gets the complex channel information for this session.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel` | A `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel` object containing channel and preamble index. This value cannot be `null`. |

### getConfigId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConfigId(): Int
```

Gets the configuration ID associated with this session.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The configuration ID as an integer. |

### getDeviceAddress

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDeviceAddress(): UwbAddress
```

Gets the UWB address of the device.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbAddress` | The `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbAddress` of the device. This value cannot be `null`. |

### getPeerAddress

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPeerAddress(): UwbAddress
```

Returns the UwbAddress of the peer device.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbAddress` | A `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbAddress` corresponding to the peer device to range with. This value cannot be `null`. |

### getRangingUpdateRate

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRangingUpdateRate(): Int
```

Returns the update rate for ranging operations.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The ranging update rate. |

### getSessionId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSessionId(): Int
```

Gets the session ID associated with this ranging session.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The session ID as an integer. |

### getSessionKeyInfo

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSessionKeyInfo(): ByteArray?
```

Gets session key information, if available.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | A byte array containing session key info, or null if not available. |

### getSlotDuration

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSlotDuration(): Int
```

Returns slot duration of the session.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the slot duration. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#DURATION_1_MS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#DURATION_2_MS:kotlin.Int` |

### getSubSessionId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSubSessionId(): Int
```

Gets the sub-session ID if applicable for the session.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The sub-session ID as an integer or `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbRangingParams#SUB_SESSION_UNDEFINED:kotlin.Int` if not applicable. |

### getSubSessionKeyInfo

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSubSessionKeyInfo(): ByteArray?
```

Gets sub-session key information, if available.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | A byte array containing sub-session key info, or null if not available. |

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
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<UwbRangingParams!>
```
