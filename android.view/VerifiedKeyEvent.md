Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VerifiedKeyEvent

Kotlin | [Java](https://developer.android.com/reference/android/view/VerifiedKeyEvent "View this page in Java")

```
class VerifiedKeyEvent : VerifiedInputEvent, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.view.VerifiedInputEvent](https://developer.android.com/reference/kotlin/android/view/VerifiedInputEvent) ||
| | ↳ | [android.view.VerifiedKeyEvent](https://developer.android.com/reference/kotlin/android/view/VerifiedKeyEvent#) |

KeyEvent that has been verified by the system. The data contained in this class is always a subset of a `https://developer.android.com/reference/kotlin/android/view/KeyEvent`. Use this class to check which data has been confirmed by the system to be authentic. Most applications do not need to use this class.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/VerifiedKeyEvent#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/VerifiedKeyEvent#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/VerifiedKeyEvent#getAction()()` The action of this key event. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/view/VerifiedKeyEvent#getDownTimeNanos()()` Retrieve the time of the most recent key down event, in the `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()` time base, but in nanoseconds. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)? | `https://developer.android.com/reference/kotlin/android/view/VerifiedKeyEvent#getFlag(kotlin.Int)(flag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get a specific flag of this key event, if possible. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/VerifiedKeyEvent#getKeyCode()()` Retrieve the key code of the key event. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/VerifiedKeyEvent#getMetaState()()` Returns the state of the meta keys. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/VerifiedKeyEvent#getRepeatCount()()` Retrieve the repeat count of the event. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/VerifiedKeyEvent#getScanCode()()` Retrieve the hardware key id of this key event. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/VerifiedKeyEvent#hashCode()()` Returns a hash code value for the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/VerifiedKeyEvent#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/view/VerifiedInputEvent` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/view/VerifiedInputEvent#getDeviceId()()` Get the id of the device that generated this event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/view/VerifiedInputEvent#getDisplayId()()` Get the display id that is associated with this event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/android/view/VerifiedInputEvent#getEventTimeNanos()()` Get the time this event occurred, in the `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()` time base. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/view/VerifiedInputEvent#getSource()()` Get the source of the event. <br /> | ||

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [VerifiedKeyEvent](https://developer.android.com/reference/kotlin/android/view/VerifiedKeyEvent#)!\> | `https://developer.android.com/reference/kotlin/android/view/VerifiedKeyEvent#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

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

### getAction

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAction(): Int
```

The action of this key event. May be either `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_DOWN:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_UP:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_DOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/KeyEvent#ACTION_UP:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getAction()`

### getDownTimeNanos

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDownTimeNanos(): Long
```

Retrieve the time of the most recent key down event, in the `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis()` time base, but in nanoseconds. If this is a down event, this will be the same as `https://developer.android.com/reference/kotlin/android/view/VerifiedInputEvent#getEventTimeNanos()`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getDownTime()`

### getFlag

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFlag(flag: Int): Boolean?
```

Get a specific flag of this key event, if possible. Return null if the flag value could not be checked.

| Parameters ||
|---|---|
| `flag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the flag of interest |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html?` | Boolean(true) if the key event has the requested flag Boolean(false) if the key event does not have the requested flag null if the flag value could not be checked |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getFlags()`
- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#FLAG_CANCELED:kotlin.Int`

### getKeyCode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKeyCode(): Int
```

Retrieve the key code of the key event.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getKeyCode()`

### getMetaState

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMetaState(): Int
```

Returns the state of the meta keys.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | an integer in which each bit set to 1 represents a pressed meta key |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getMetaState()`

### getRepeatCount

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRepeatCount(): Int
```

Retrieve the repeat count of the event. For key down events, this is the number of times the key has repeated with the first down starting at 0 and counting up from there. For key up events, this is always equal to zero. For multiple key events, this is the number of down/up pairs that have occurred.

### getScanCode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScanCode(): Int
```

Retrieve the hardware key id of this key event. These values are not reliable and vary from device to device.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/KeyEvent#getScanCode()`

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<VerifiedKeyEvent!>
```
