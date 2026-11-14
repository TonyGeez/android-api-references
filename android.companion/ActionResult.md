# ActionResult

Kotlin | [Java](https://developer.android.com/reference/android/companion/ActionResult "View this page in Java")

```
class ActionResult : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.companion.ActionResult](https://developer.android.com/reference/kotlin/android/companion/ActionResult#) |

A result reported by a companion app in response to an `https://developer.android.com/reference/kotlin/android/companion/ActionRequest`.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/companion/ActionResult.Builder` Builder for creating an `https://developer.android.com/reference/kotlin/android/companion/ActionResult#`. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/ActionResult#RESULT_ACTIVATED:kotlin.Int` A result code indicating that the requested activation was completed successfully. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/ActionResult#RESULT_DEACTIVATED:kotlin.Int` A result code indicating that a previously active action is now inactive. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/ActionResult#RESULT_FAILED_TO_ACTIVATE:kotlin.Int` A result code indicating that the requested activation failed. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/ActionResult#describeContents()()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/companion/ActionResult#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/ActionResult#getAction()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/ActionResult#getResultCode()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/companion/ActionResult#hashCode()()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/companion/ActionResult#toString()()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/companion/ActionResult#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ActionResult](https://developer.android.com/reference/kotlin/android/companion/ActionResult#)!\> | `https://developer.android.com/reference/kotlin/android/companion/ActionResult#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### RESULT_ACTIVATED

```
static val RESULT_ACTIVATED: Int
```

A result code indicating that the requested activation was completed successfully. This is sent in response to an `https://developer.android.com/reference/kotlin/android/companion/ActionRequest#OP_ACTIVATE:kotlin.Int` request.

 Value: 0

### RESULT_DEACTIVATED

```
static val RESULT_DEACTIVATED: Int
```

A result code indicating that a previously active action is now inactive. This can be sent for two reasons: 1. As a successful response to an `https://developer.android.com/reference/kotlin/android/companion/ActionRequest#OP_DEACTIVATE:kotlin.Int` request. 2. Action was failed after initially succeed.

 Value: 2

### RESULT_FAILED_TO_ACTIVATE

```
static val RESULT_FAILED_TO_ACTIVATE: Int
```

A result code indicating that the requested activation failed. This is sent in response to an `https://developer.android.com/reference/kotlin/android/companion/ActionRequest#OP_ACTIVATE:kotlin.Int` request.

 Value: 1

## Public methods

### describeContents

```
fun describeContents(): Int
```

### equals

```
fun equals(other: Any?): Boolean
```

### getAction

```
fun getAction(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the action this result refers to, e.g. `https://developer.android.com/reference/kotlin/android/companion/ActionRequest#REQUEST_NEARBY_SCANNING:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/companion/ActionRequest#REQUEST_NEARBY_SCANNING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/companion/ActionRequest#REQUEST_NEARBY_ADVERTISING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/companion/ActionRequest#REQUEST_TRANSPORT:kotlin.Int` |

### getResultCode

```
fun getResultCode(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the result code, e.g., `https://developer.android.com/reference/kotlin/android/companion/ActionResult#RESULT_ACTIVATED:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/companion/ActionResult#RESULT_ACTIVATED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/companion/ActionResult#RESULT_FAILED_TO_ACTIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/companion/ActionResult#RESULT_DEACTIVATED:kotlin.Int` |

### hashCode

```
fun hashCode(): Int
```

### toString

```
fun toString(): String
```

### writeToParcel

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

```
static val CREATOR: Parcelable.Creator<ActionResult!>
```
