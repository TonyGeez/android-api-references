Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PccEgressException

```
class PccEgressException : Exception, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [android.app.privatecompute.PccEgressException](https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#) |
| --- | --- | --- | --- |

Exception thrown when an egress request fails inside the PCC sandbox. Contains the android.app.privatecompute.PccEgressException.StatusCode detailing the failure.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException.SensitiveCategoryInfo` Details about the detected sensitive content that caused an egress request to be rejected. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_CONTENT_SENSITIVE:kotlin.Int` Indicates that the request failed because the content was classified as sensitive. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_NO_RESPONSE_FROM_EGRESS_SERVICE:kotlin.Int` Indicates that the request failed because the proxy service did not respond or timed out. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_UNABLE_TO_DELIVER_REQUEST:kotlin.Int` Indicates that the request failed because the system was unable to deliver the egress. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_UNKNOWN:kotlin.Int` Indicates an unspecified or unexpected failure. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#PccEgressException(kotlin.Int)(statusCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a new PccEgressException with a given android. |
| `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#PccEgressException(kotlin.Int,%20android.app.privatecompute.PccEgressException.SensitiveCategoryInfo)(statusCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, sensitiveCategoryInfo: https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException.SensitiveCategoryInfo)` Creates a new PccEgressException with a given android. |
| `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#PccEgressException(kotlin.Int,%20kotlin.String)(statusCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Creates a new PccEgressException with a given android. |
| `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#PccEgressException(kotlin.Int,%20kotlin.String,%20android.app.privatecompute.PccEgressException.SensitiveCategoryInfo)(statusCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, sensitiveCategoryInfo: https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException.SensitiveCategoryInfo)` Creates a new PccEgressException with a given android. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [PccEgressException.SensitiveCategoryInfo](https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException.SensitiveCategoryInfo)? | `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#getSensitiveCategoryInfo()()` Returns the `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException.SensitiveCategoryInfo` detailing the sensitive content detected during egress screening. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#getStatusCode()()` Returns the status code detailing the egress failure. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [PccEgressException](https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#)!\> | `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#CREATOR:android.os.Parcelable.Creator` Standard parcelable creator for `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#`. |

## Constants

### ERROR_CONTENT_SENSITIVE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_CONTENT_SENSITIVE: Int
```

Indicates that the request failed because the content was classified as sensitive.

 Value: 3

### ERROR_NO_RESPONSE_FROM_EGRESS_SERVICE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_NO_RESPONSE_FROM_EGRESS_SERVICE: Int
```

Indicates that the request failed because the proxy service did not respond or timed out.

 Value: 2

### ERROR_UNABLE_TO_DELIVER_REQUEST

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_UNABLE_TO_DELIVER_REQUEST: Int
```

Indicates that the request failed because the system was unable to deliver the egress.

 Value: 1

### ERROR_UNKNOWN

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_UNKNOWN: Int
```

Indicates an unspecified or unexpected failure.

 Value: -1

## Public constructors

### PccEgressException

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PccEgressException(statusCode: Int)
```

Creates a new PccEgressException with a given android.app.privatecompute.PccEgressException.StatusCode.

| Parameters ||
|---|---|
| `statusCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The android.app.privatecompute.PccEgressException.StatusCode of the egress failure. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_UNABLE_TO_DELIVER_REQUEST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_NO_RESPONSE_FROM_EGRESS_SERVICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_CONTENT_SENSITIVE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_UNKNOWN:kotlin.Int` |

### PccEgressException

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PccEgressException(
    statusCode: Int, 
    sensitiveCategoryInfo: PccEgressException.SensitiveCategoryInfo)
```

Creates a new PccEgressException with a given android.app.privatecompute.PccEgressException.StatusCode and `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException.SensitiveCategoryInfo`.

| Parameters ||
|---|---|
| `statusCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The android.app.privatecompute.PccEgressException.StatusCode of the egress failure. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_UNABLE_TO_DELIVER_REQUEST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_NO_RESPONSE_FROM_EGRESS_SERVICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_CONTENT_SENSITIVE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_UNKNOWN:kotlin.Int` |
| `sensitiveCategoryInfo` | [PccEgressException.SensitiveCategoryInfo](https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException.SensitiveCategoryInfo): The `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException.SensitiveCategoryInfo` detailing the sensitive content screening result. This value cannot be `null`. |

### PccEgressException

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PccEgressException(
    statusCode: Int, 
    message: String)
```

Creates a new PccEgressException with a given android.app.privatecompute.PccEgressException.StatusCode and detailed error message.

| Parameters ||
|---|---|
| `statusCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The android.app.privatecompute.PccEgressException.StatusCode of the egress failure. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_UNABLE_TO_DELIVER_REQUEST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_NO_RESPONSE_FROM_EGRESS_SERVICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_CONTENT_SENSITIVE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_UNKNOWN:kotlin.Int` |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The detailed error message description. This value cannot be `null`. |

### PccEgressException

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PccEgressException(
    statusCode: Int, 
    message: String, 
    sensitiveCategoryInfo: PccEgressException.SensitiveCategoryInfo)
```

Creates a new PccEgressException with a given android.app.privatecompute.PccEgressException.StatusCode, detailed error message, and `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException.SensitiveCategoryInfo`.

| Parameters ||
|---|---|
| `statusCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The android.app.privatecompute.PccEgressException.StatusCode of the egress failure. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_UNABLE_TO_DELIVER_REQUEST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_NO_RESPONSE_FROM_EGRESS_SERVICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_CONTENT_SENSITIVE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_UNKNOWN:kotlin.Int` |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The detailed error message description. This value cannot be `null`. |
| `sensitiveCategoryInfo` | [PccEgressException.SensitiveCategoryInfo](https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException.SensitiveCategoryInfo): The `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException.SensitiveCategoryInfo` detailing the sensitive content screening result. This value cannot be `null`. |
| --- | --- |

## Public methods

### describeContents

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getSensitiveCategoryInfo

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSensitiveCategoryInfo(): PccEgressException.SensitiveCategoryInfo?
```

Returns the `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException.SensitiveCategoryInfo` detailing the sensitive content detected during egress screening.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException.SensitiveCategoryInfo?` | The `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException.SensitiveCategoryInfo`, or `null` if not set or if the egress failure was not due to sensitive content. |

### getStatusCode

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStatusCode(): Int
```

Returns the status code detailing the egress failure.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The android.app.privatecompute.PccEgressException.StatusCode of the egress failure. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_UNABLE_TO_DELIVER_REQUEST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_NO_RESPONSE_FROM_EGRESS_SERVICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_CONTENT_SENSITIVE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_UNKNOWN:kotlin.Int` |

### writeToParcel

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<PccEgressException!>
```

Standard parcelable creator for `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#`.
