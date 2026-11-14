Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UwbComplexChannel

```
class UwbComplexChannel : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.ranging.uwb.UwbComplexChannel](https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#) |

A Class representing the complex channel for UWB which comprises channel and preamble index negotiated between peer devices out of band before ranging.

PRF (Pulse Repetition Frequency) supported:

- BPRF - Base Pulse Repetition Frequency.
- HPRF - Higher Pulse Repetition Frequency.

See

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel.Builder` Builder for creating instances of `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#`. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#UWB_CHANNEL_10:kotlin.Int` UWB channel 10 |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#UWB_CHANNEL_12:kotlin.Int` UWB channel 12 |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#UWB_CHANNEL_13:kotlin.Int` UWB channel 13 |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#UWB_CHANNEL_14:kotlin.Int` UWB channel 14 |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#UWB_CHANNEL_5:kotlin.Int` UWB channel 5 |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#UWB_CHANNEL_6:kotlin.Int` UWB channel 6 |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#UWB_CHANNEL_8:kotlin.Int` UWB channel 8 |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#UWB_CHANNEL_9:kotlin.Int` UWB channel 9 |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#UWB_PREAMBLE_CODE_INDEX_10:kotlin.Int` UWB preamble code index 10 (PRF mode - BPRF). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#UWB_PREAMBLE_CODE_INDEX_11:kotlin.Int` UWB preamble code index 11 (PRF mode - BPRF). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#UWB_PREAMBLE_CODE_INDEX_12:kotlin.Int` UWB preamble code index 12 (PRF mode - BPRF). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#UWB_PREAMBLE_CODE_INDEX_25:kotlin.Int` UWB preamble code index 25 (PRF mode - HPRF). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#UWB_PREAMBLE_CODE_INDEX_26:kotlin.Int` UWB preamble code index 26 (PRF mode - HPRF). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#UWB_PREAMBLE_CODE_INDEX_27:kotlin.Int` UWB preamble code index 27 (PRF mode - HPRF). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#UWB_PREAMBLE_CODE_INDEX_28:kotlin.Int` UWB preamble code index 28 (PRF mode - HPRF). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#UWB_PREAMBLE_CODE_INDEX_29:kotlin.Int` UWB preamble code index 29 (PRF mode - HPRF). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#UWB_PREAMBLE_CODE_INDEX_30:kotlin.Int` UWB preamble code index 30 (PRF mode - HPRF). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#UWB_PREAMBLE_CODE_INDEX_31:kotlin.Int` UWB preamble code index 31 (PRF mode - HPRF). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#UWB_PREAMBLE_CODE_INDEX_32:kotlin.Int` UWB preamble code index 32 (PRF mode - HPRF). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#UWB_PREAMBLE_CODE_INDEX_9:kotlin.Int` UWB preamble code index 9 (PRF mode - BPRF). |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#getChannel()()` Gets the UWB channel associated with this configuration. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#getPreambleIndex()()` Gets the UWB preamble index associated with this configuration. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#hashCode()()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#toString()()` Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [UwbComplexChannel](https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#)!\> | `https://developer.android.com/reference/kotlin/android/ranging/uwb/UwbComplexChannel#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### UWB_CHANNEL_10

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UWB_CHANNEL_10: Int
```

UWB channel 10

 Value: 10

### UWB_CHANNEL_12

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UWB_CHANNEL_12: Int
```

UWB channel 12

 Value: 12

### UWB_CHANNEL_13

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UWB_CHANNEL_13: Int
```

UWB channel 13

 Value: 13

### UWB_CHANNEL_14

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UWB_CHANNEL_14: Int
```

UWB channel 14

 Value: 14

### UWB_CHANNEL_5

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UWB_CHANNEL_5: Int
```

UWB channel 5

 Value: 5

### UWB_CHANNEL_6

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UWB_CHANNEL_6: Int
```

UWB channel 6

 Value: 6

### UWB_CHANNEL_8

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UWB_CHANNEL_8: Int
```

UWB channel 8

 Value: 8

### UWB_CHANNEL_9

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UWB_CHANNEL_9: Int
```

UWB channel 9

 Value: 9

### UWB_PREAMBLE_CODE_INDEX_10

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UWB_PREAMBLE_CODE_INDEX_10: Int
```

UWB preamble code index 10 (PRF mode - BPRF).

 Value: 10

### UWB_PREAMBLE_CODE_INDEX_11

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UWB_PREAMBLE_CODE_INDEX_11: Int
```

UWB preamble code index 11 (PRF mode - BPRF).

 Value: 11

### UWB_PREAMBLE_CODE_INDEX_12

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UWB_PREAMBLE_CODE_INDEX_12: Int
```

UWB preamble code index 12 (PRF mode - BPRF).

 Value: 12

### UWB_PREAMBLE_CODE_INDEX_25

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UWB_PREAMBLE_CODE_INDEX_25: Int
```

UWB preamble code index 25 (PRF mode - HPRF).

 Value: 25

### UWB_PREAMBLE_CODE_INDEX_26

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UWB_PREAMBLE_CODE_INDEX_26: Int
```

UWB preamble code index 26 (PRF mode - HPRF).

 Value: 26

### UWB_PREAMBLE_CODE_INDEX_27

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UWB_PREAMBLE_CODE_INDEX_27: Int
```

UWB preamble code index 27 (PRF mode - HPRF).

 Value: 27

### UWB_PREAMBLE_CODE_INDEX_28

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UWB_PREAMBLE_CODE_INDEX_28: Int
```

UWB preamble code index 28 (PRF mode - HPRF).

 Value: 28

### UWB_PREAMBLE_CODE_INDEX_29

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UWB_PREAMBLE_CODE_INDEX_29: Int
```

UWB preamble code index 29 (PRF mode - HPRF).

 Value: 29

### UWB_PREAMBLE_CODE_INDEX_30

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UWB_PREAMBLE_CODE_INDEX_30: Int
```

UWB preamble code index 30 (PRF mode - HPRF).

 Value: 30

### UWB_PREAMBLE_CODE_INDEX_31

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UWB_PREAMBLE_CODE_INDEX_31: Int
```

UWB preamble code index 31 (PRF mode - HPRF).

 Value: 31

### UWB_PREAMBLE_CODE_INDEX_32

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UWB_PREAMBLE_CODE_INDEX_32: Int
```

UWB preamble code index 32 (PRF mode - HPRF).

 Value: 32

### UWB_PREAMBLE_CODE_INDEX_9

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UWB_PREAMBLE_CODE_INDEX_9: Int
```

UWB preamble code index 9 (PRF mode - BPRF).

 Value: 9

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

### getChannel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChannel(): Int
```

Gets the UWB channel associated with this configuration.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The channel number, which is one of the predefined UWB channels: |

### getPreambleIndex

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPreambleIndex(): Int
```

Gets the UWB preamble index associated with this configuration.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The preamble index, which is one of the predefined UWB preamble indices: See |

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
static val CREATOR: Parcelable.Creator<UwbComplexChannel!>
```
