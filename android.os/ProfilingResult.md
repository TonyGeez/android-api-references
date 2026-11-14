Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProfilingResult

```
class ProfilingResult : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.ProfilingResult](ProfilingResult.md) |

Encapsulates results of a single profiling request operation.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#ERROR_FAILED_EXECUTING:kotlin.Int` The request was executed and failed for a reason not specified below. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#ERROR_FAILED_INVALID_REQUEST:kotlin.Int` The request failed due to invalid ProfilingRequest. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#ERROR_FAILED_NO_DISK_SPACE:kotlin.Int` The request was executed and failed due to a lack of disk space. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#ERROR_FAILED_POST_PROCESSING:kotlin.Int` The request was executed but post processing failed and the result was discarded. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#ERROR_FAILED_PROFILING_IN_PROGRESS:kotlin.Int` The request was denied due to profiling already in progress. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#ERROR_FAILED_RATE_LIMIT_PROCESS:kotlin.Int` The request was denied due to process level rate limiting. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#ERROR_FAILED_RATE_LIMIT_SYSTEM:kotlin.Int` The request was denied due to system level rate limiting. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#ERROR_NONE:kotlin.Int` The request was executed and succeeded. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#ERROR_UNKNOWN:kotlin.Int` The request was denied or failed for an unspecified reason. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#getErrorCode()()` The result ErrorCode for the profiling request indicating the failure reason if applicable. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#getErrorMessage()()` Additional details about failures that occurred, if applicable. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#getResultFilePath()()` The file path of the profiling result data. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#getTag()()` The tag defined by the caller at request time. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#getTriggerType()()` Trigger type that started this profiling, or `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_NONE:kotlin.Int` for profiling not started by a trigger. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#hashCode()()` Returns a hash code value for the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ProfilingResult](ProfilingResult.md)!\> | `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### ERROR_FAILED_EXECUTING

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_FAILED_EXECUTING: Int
```

The request was executed and failed for a reason not specified below.

 Value: 4

### ERROR_FAILED_INVALID_REQUEST

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_FAILED_INVALID_REQUEST: Int
```

The request failed due to invalid ProfilingRequest.

 Value: 7

### ERROR_FAILED_NO_DISK_SPACE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_FAILED_NO_DISK_SPACE: Int
```

The request was executed and failed due to a lack of disk space.

 Value: 6

### ERROR_FAILED_POST_PROCESSING

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_FAILED_POST_PROCESSING: Int
```

The request was executed but post processing failed and the result was discarded.

 Value: 5

### ERROR_FAILED_PROFILING_IN_PROGRESS

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_FAILED_PROFILING_IN_PROGRESS: Int
```

The request was denied due to profiling already in progress.

 Value: 3

### ERROR_FAILED_RATE_LIMIT_PROCESS

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_FAILED_RATE_LIMIT_PROCESS: Int
```

The request was denied due to process level rate limiting.

 Value: 2

### ERROR_FAILED_RATE_LIMIT_SYSTEM

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_FAILED_RATE_LIMIT_SYSTEM: Int
```

The request was denied due to system level rate limiting.

 Value: 1

### ERROR_NONE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_NONE: Int
```

The request was executed and succeeded.

 Value: 0

### ERROR_UNKNOWN

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_UNKNOWN: Int
```

The request was denied or failed for an unspecified reason.

 Value: 8

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getErrorCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getErrorCode(): Int
```

The result ErrorCode for the profiling request indicating the failure reason if applicable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#ERROR_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#ERROR_FAILED_RATE_LIMIT_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#ERROR_FAILED_RATE_LIMIT_PROCESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#ERROR_FAILED_PROFILING_IN_PROGRESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#ERROR_FAILED_EXECUTING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#ERROR_FAILED_POST_PROCESSING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#ERROR_FAILED_NO_DISK_SPACE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#ERROR_UNKNOWN:kotlin.Int` |

### getErrorMessage

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getErrorMessage(): String?
```

Additional details about failures that occurred, if applicable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

### getResultFilePath

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getResultFilePath(): String?
```

The file path of the profiling result data.

Will be null if `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#getErrorCode()` returns code other than `https://developer.android.com/reference/kotlin/android/os/ProfilingResult#ERROR_NONE:kotlin.Int`.

### getTag

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTag(): String?
```

The tag defined by the caller at request time.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

### getTriggerType

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTriggerType(): Int
```

Trigger type that started this profiling, or `https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger#TRIGGER_TYPE_NONE:kotlin.Int` for profiling not started by a trigger.

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<ProfilingResult!>
```
