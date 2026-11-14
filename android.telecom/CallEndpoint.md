Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CallEndpoint

```
class CallEndpoint : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telecom.CallEndpoint](https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#) |

Encapsulates the endpoint where call media can flow

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_BLUETOOTH:kotlin.Int` Indicates that the type of endpoint through which call media flows is a Bluetooth. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_EARPIECE:kotlin.Int` Indicates that the type of endpoint through which call media flows is an earpiece. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_SPEAKER:kotlin.Int` Indicates that the type of endpoint through which call media flows is a speakerphone. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_STREAMING:kotlin.Int` Indicates that the type of endpoint through which call media flows is an external. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_UNKNOWN:kotlin.Int` Indicates that the type of endpoint through which call media flows is unknown type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_WIRED_HEADSET:kotlin.Int` Indicates that the type of endpoint through which call media flows is a wired headset. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#CallEndpoint(kotlin.CharSequence,%20kotlin.Int,%20android.os.ParcelUuid)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, id: https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#)` Constructor for a `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#` object. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#getEndpointName()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#getEndpointType()()` <br /> |
| [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#) | `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#getIdentifier()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#hashCode()()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#writeToParcel(android.os.Parcel,%20kotlin.Int)(destination: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [CallEndpoint](https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#) | `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#BASELINE_ENDPOINT:android.telecom.CallEndpoint` Used to reset the previous request and go with the system default call endpoint. |
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [CallEndpoint](https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#)!\> | `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#CREATOR:android.os.Parcelable.Creator` Responsible for creating CallEndpoint objects for deserialized Parcels. |

## Constants

### TYPE_BLUETOOTH

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_BLUETOOTH: Int
```

Indicates that the type of endpoint through which call media flows is a Bluetooth.

 Value: 2

### TYPE_EARPIECE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_EARPIECE: Int
```

Indicates that the type of endpoint through which call media flows is an earpiece.

 Value: 1

### TYPE_SPEAKER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_SPEAKER: Int
```

Indicates that the type of endpoint through which call media flows is a speakerphone.

 Value: 4

### TYPE_STREAMING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_STREAMING: Int
```

Indicates that the type of endpoint through which call media flows is an external.

 Value: 5

### TYPE_UNKNOWN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_UNKNOWN: Int
```

Indicates that the type of endpoint through which call media flows is unknown type.

 Value: -1

### TYPE_WIRED_HEADSET

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_WIRED_HEADSET: Int
```

Indicates that the type of endpoint through which call media flows is a wired headset.

 Value: 3

## Public constructors

### CallEndpoint

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CallEndpoint(
    name: CharSequence, 
    type: Int, 
    id: ParcelUuid)
```

Constructor for a `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#` object.

| Parameters ||
|---|---|
| `name` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): Human-readable name associated with the endpoint. This value cannot be `null`. |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of endpoint through which call media being routed Allowed values: `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_EARPIECE:kotlin.Int` `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_BLUETOOTH:kotlin.Int` `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_WIRED_HEADSET:kotlin.Int` `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_SPEAKER:kotlin.Int` `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_STREAMING:kotlin.Int` `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_UNKNOWN:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_EARPIECE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_BLUETOOTH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_WIRED_HEADSET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_SPEAKER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_STREAMING:kotlin.Int` |
| `id` | [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#): A unique identifier for this endpoint on the device. This value cannot be `null`. |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### getEndpointName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEndpointName(): CharSequence
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` | Human-readable name associated with the endpoint. This value cannot be `null`. |

### getEndpointType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEndpointType(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The type of endpoint through which call media being routed. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_EARPIECE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_BLUETOOTH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_WIRED_HEADSET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_SPEAKER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint#TYPE_STREAMING:kotlin.Int` |

### getIdentifier

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIdentifier(): ParcelUuid
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#` | A unique identifier for this endpoint on the device. This value cannot be `null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    destination: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |
| `destination` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |

## Properties

### BASELINE_ENDPOINT

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BASELINE_ENDPOINT: CallEndpoint
```

Used to reset the previous request and go with the system default call endpoint.

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<CallEndpoint!>
```

Responsible for creating CallEndpoint objects for deserialized Parcels.
