Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppFunctionException

```
class AppFunctionException : Exception, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [android.app.appfunctions.AppFunctionException](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#) |

App function related error.

This exception may include a `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#getExtras()` containing additional error-specific metadata.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_APP_UNKNOWN_ERROR:kotlin.Int` An unknown error occurred while processing the call in the AppFunctionService. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_CANCELLED:kotlin.Int` The operation was cancelled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_CATEGORY_APP:kotlin.Int` The error is caused by the app providing the function. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_CATEGORY_REQUEST_ERROR:kotlin.Int` The error is caused by the app requesting a function execution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_CATEGORY_SYSTEM:kotlin.Int` The error is caused by an issue in the system. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_CATEGORY_UNKNOWN:kotlin.Int` The error category is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_DENIED:kotlin.Int` The caller does not have the permission to execute an app function. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_DISABLED:kotlin.Int` The caller tried to execute a disabled app function. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_ENTERPRISE_POLICY_DISALLOWED:kotlin.Int` The operation was disallowed by enterprise policy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_FUNCTION_NOT_FOUND:kotlin.Int` The caller tried to execute a function that does not exist. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_INVALID_ARGUMENT:kotlin.Int` The caller supplied invalid arguments to the execution request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_SYSTEM_ERROR:kotlin.Int` An internal unexpected error coming from the system. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#AppFunctionException(kotlin.Int,%20kotlin.String)(errorCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, errorMessage: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` <br /> |
| `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#AppFunctionException(kotlin.Int,%20kotlin.String,%20android.os.Bundle)(errorCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, errorMessage: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#)` <br /> |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#getErrorCategory()()` Returns the error category. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#getErrorCode()()` Returns one of the `ERROR` constants. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#getErrorMessage()()` Returns the error message. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#getExtras()()` Returns any extras associated with this error. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AppFunctionException](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#)!\> | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#CREATOR:android.os.Parcelable.Creator` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#message:kotlin.String` Returns the detail message string of this throwable. |

## Constants

### ERROR_APP_UNKNOWN_ERROR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_APP_UNKNOWN_ERROR: Int
```

An unknown error occurred while processing the call in the AppFunctionService.

This error is thrown when the service is connected in the remote application but an unexpected error is thrown from the bound application.

This error is in the `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_CATEGORY_APP:kotlin.Int` category.

 Value: 3000

### ERROR_CANCELLED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_CANCELLED: Int
```

The operation was cancelled. Use this error code to report that a cancellation is done after receiving a cancellation signal.

This error is in the `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_CATEGORY_SYSTEM:kotlin.Int` category.

 Value: 2001

### ERROR_CATEGORY_APP

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_CATEGORY_APP: Int
```

The error is caused by the app providing the function.

For example, the app crashed when the system is executing the request.

Errors in the category fall in the range 3000-3999 inclusive.

 Value: 3

### ERROR_CATEGORY_REQUEST_ERROR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_CATEGORY_REQUEST_ERROR: Int
```

The error is caused by the app requesting a function execution.

For example, the caller provided invalid parameters in the execution request e.g. an invalid function ID.

Errors in the category fall in the range 1000-1999 inclusive.

 Value: 1

### ERROR_CATEGORY_SYSTEM

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_CATEGORY_SYSTEM: Int
```

The error is caused by an issue in the system.

For example, the AppFunctionService implementation is not found by the system.

Errors in the category fall in the range 2000-2999 inclusive.

 Value: 2

### ERROR_CATEGORY_UNKNOWN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_CATEGORY_UNKNOWN: Int
```

The error category is unknown.

This is the default value for `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#getErrorCategory()`.

 Value: 0

### ERROR_DENIED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_DENIED: Int
```

The caller does not have the permission to execute an app function.

This error is returned to the caller of android.app.appfunctions.AppFunctionManager#executeAppFunction if the caller does not have the necessary permission.

This error is in the `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_CATEGORY_REQUEST_ERROR:kotlin.Int` category.

 Value: 1000

### ERROR_DISABLED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_DISABLED: Int
```

The caller tried to execute a disabled app function.

This error is returned to the caller of android.app.appfunctions.AppFunctionManager#executeAppFunction if the app function is considered disabled according to `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionState#isEnabled()`.

This error is in the `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_CATEGORY_REQUEST_ERROR:kotlin.Int` category.

 Value: 1002

### ERROR_ENTERPRISE_POLICY_DISALLOWED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_ENTERPRISE_POLICY_DISALLOWED: Int
```

The operation was disallowed by enterprise policy.

This error is in the `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_CATEGORY_SYSTEM:kotlin.Int` category.

 Value: 2002

### ERROR_FUNCTION_NOT_FOUND

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_FUNCTION_NOT_FOUND: Int
```

The caller tried to execute a function that does not exist.

This error is returned to the caller of android.app.appfunctions.AppFunctionManager#executeAppFunction if one of the following is true:

- The function identifier specified in `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest#getFunctionIdentifier()` does not match any function identifiers in the metadata returned by `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#searchAppFunctions(android.app.appfunctions.AppFunctionSearchSpec,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`.
- The app function is `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#SCOPE_ACTIVITY:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest#getActivityId()` is not provided or does not match any activity identifiers returned by `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionState#getActivityIds()`, this error will be returned.
- The app function is `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#SCOPE_GLOBAL:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest#getActivityId()` is non-null.

This error is in the `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_CATEGORY_REQUEST_ERROR:kotlin.Int` category.

 Value: 1003

### ERROR_INVALID_ARGUMENT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_INVALID_ARGUMENT: Int
```

The caller supplied invalid arguments to the execution request.

This error may be considered similar to `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

This error is in the `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_CATEGORY_REQUEST_ERROR:kotlin.Int` category.

 Value: 1001

### ERROR_SYSTEM_ERROR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_SYSTEM_ERROR: Int
```

An internal unexpected error coming from the system.

This error is in the `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_CATEGORY_SYSTEM:kotlin.Int` category.

 Value: 2000

## Public constructors

### AppFunctionException

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AppFunctionException(
    errorCode: Int, 
    errorMessage: String?)
```

| Parameters ||
|---|---|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The error code. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_DENIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_APP_UNKNOWN_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_FUNCTION_NOT_FOUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_SYSTEM_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_INVALID_ARGUMENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_CANCELLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_ENTERPRISE_POLICY_DISALLOWED:kotlin.Int` |
| `errorMessage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The error message. This value may be `null`. |

### AppFunctionException

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AppFunctionException(
    errorCode: Int, 
    errorMessage: String?, 
    extras: Bundle)
```

| Parameters ||
|---|---|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The error code. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_DENIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_APP_UNKNOWN_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_FUNCTION_NOT_FOUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_SYSTEM_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_INVALID_ARGUMENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_CANCELLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_ENTERPRISE_POLICY_DISALLOWED:kotlin.Int` |
| `errorMessage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The error message. This value may be `null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#): The extras associated with this error. This value cannot be `null`. |

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

### getErrorCategory

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getErrorCategory(): Int
```

Returns the error category.

This method categorizes errors based on their underlying cause, allowing developers to implement targeted error handling and provide more informative error messages to users. It maps ranges of error codes to specific error categories.

This method returns `ERROR_CATEGORY_UNKNOWN` if the error code does not belong to any error category.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_CATEGORY_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_CATEGORY_REQUEST_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_CATEGORY_APP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_CATEGORY_SYSTEM:kotlin.Int` |

### getErrorCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getErrorCode(): Int
```

Returns one of the `ERROR` constants.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_DENIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_APP_UNKNOWN_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_FUNCTION_NOT_FOUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_SYSTEM_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_INVALID_ARGUMENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_CANCELLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_ENTERPRISE_POLICY_DISALLOWED:kotlin.Int` |

### getErrorMessage

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getErrorMessage(): String?
```

Returns the error message.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

### getExtras

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExtras(): Bundle
```

Returns any extras associated with this error.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` | This value cannot be `null`. |

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
static val CREATOR: Parcelable.Creator<AppFunctionException!>
```

### message

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
val message: String
```

Returns the detail message string of this throwable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |
