Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PhoneAccountHandle

Kotlin | [Java](../android/telecom/PhoneAccountHandle.md)
| --- | --- |

```
class PhoneAccountHandle : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telecom.PhoneAccountHandle](../android/telecom/PhoneAccountHandle.md) |

The unique identifier for a `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount`. A `PhoneAccountHandle` is made of two parts:

- The component name of the associated connection service.
- A string identifier that is unique across `PhoneAccountHandle`s with the same component name. Apps registering `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#`s should ensure that the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#getId()` provided does not expose personally identifying information. A `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` should use an opaque token as the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#` identifier.

Note: This Class requires a non-null `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` and `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` to operate properly. Passing in invalid parameters will generate a log warning. See `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount`, `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager`.

<br />

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#PhoneAccountHandle(android.content.ComponentName,%20kotlin.String)(componentName: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Creates a new `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#`. |
| `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#PhoneAccountHandle(android.content.ComponentName,%20kotlin.String,%20android.os.UserHandle)(componentName: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, userHandle: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)` Creates a new `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#`. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [ComponentName](../android/content/ComponentName.md)! | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#getComponentName()()` The `ComponentName` of the connection service which is responsible for making phone calls using this `PhoneAccountHandle`. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#getId()()` A string that uniquely distinguishes this particular `PhoneAccountHandle` from all the others supported by the connection service that created it. |
| [UserHandle](../android/os/UserHandle.md)! | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#getUserHandle()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#hashCode()()` Returns a hash code value for the object. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#writeToParcel(android.os.Parcel,%20kotlin.Int)(out: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PhoneAccountHandle](../android/telecom/PhoneAccountHandle.md)!\> | `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### PhoneAccountHandle

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PhoneAccountHandle(
    componentName: ComponentName, 
    id: String)
```

Creates a new `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#`.

| Parameters ||
|---|---|
| `componentName` | [ComponentName](../android/content/ComponentName.md): The `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` of the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` which services this `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#`. This value cannot be `null`. |
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A string identifier that is unique across `PhoneAccountHandle`s with the same component name. Apps registering `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#`s should ensure that the ID provided does not expose personally identifying information. A `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` should use an opaque token as the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#` identifier. Note: Each String field is limited to 256 characters. This check is enforced when registering the PhoneAccount via `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#registerPhoneAccount(android.telecom.PhoneAccount)` and will cause an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` to be thrown if the character field limit is over 256. This value cannot be `null`. |

### PhoneAccountHandle

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PhoneAccountHandle(
    componentName: ComponentName, 
    id: String, 
    userHandle: UserHandle)
```

Creates a new `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#`.

| Parameters ||
|---|---|
| `componentName` | [ComponentName](../android/content/ComponentName.md): The `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` of the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` which services this `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#`. This value cannot be `null`. |
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A string identifier that is unique across `PhoneAccountHandle`s with the same component name. Apps registering `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#`s should ensure that the ID provided does not expose personally identifying information. A `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` should use an opaque token as the `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#` identifier. This value cannot be `null`. |
| `userHandle` | [UserHandle](../android/os/UserHandle.md): The `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` associated with this `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle#`. Note: Each String field is limited to 256 characters. This check is enforced when registering the PhoneAccount via `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#registerPhoneAccount(android.telecom.PhoneAccount)` and will cause an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` to be thrown if the character field limit is over 256. This value cannot be `null`. |
| --- | --- |

## Public methods

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

### getComponentName

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getComponentName(): ComponentName!
```

The `ComponentName` of the connection service which is responsible for making phone calls using this `PhoneAccountHandle`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!` | A suitable `ComponentName`. |

### getId

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getId(): String!
```

A string that uniquely distinguishes this particular `PhoneAccountHandle` from all the others supported by the connection service that created it.

A connection service must select identifiers that are stable for the lifetime of their users' relationship with their service, across many Android devices. The identifier should be a stable opaque token which uniquely identifies the user within the service. Depending on how a service chooses to operate, a bad set of identifiers might be an increasing series of integers (`0`, `1`, `2`, ...) that are generated locally on each phone and could collide with values generated on other phones or after a data wipe of a given phone.

Important: A non-unique identifier could cause non-deterministic call-log backup/restore behavior.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | A service-specific unique opaque identifier for this `PhoneAccountHandle`. |

### getUserHandle

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUserHandle(): UserHandle!
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!` | the `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#` to use when connecting to this PhoneAccount. |

### hashCode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
    out: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<PhoneAccountHandle!>
```
