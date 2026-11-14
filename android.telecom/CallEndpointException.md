# CallEndpointException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CallEndpointException

Kotlin| [Java](https://developer.android.com/reference/android/telecom/CallEndpointException "View this page in Java") 

```
class CallEndpointException : RuntimeException, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| | | | ↳ | [android.telecom.CallEndpointException](https://developer.android.com/reference/kotlin/android/telecom/CallEndpointException#) |

This class represents a set of exceptions that can occur when requesting a [CallEndpoint](https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint) change.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_ANOTHER_REQUEST](https://developer.android.com/reference/kotlin/android/telecom/CallEndpointException#ERROR_ANOTHER_REQUEST:kotlin.Int) The operation was canceled by another request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_ENDPOINT_DOES_NOT_EXIST](https://developer.android.com/reference/kotlin/android/telecom/CallEndpointException#ERROR_ENDPOINT_DOES_NOT_EXIST:kotlin.Int) The operation has failed because requested CallEndpoint does not exist. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_REQUEST_TIME_OUT](https://developer.android.com/reference/kotlin/android/telecom/CallEndpointException#ERROR_REQUEST_TIME_OUT:kotlin.Int) The operation was not completed on time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/telecom/CallEndpointException#ERROR_UNSPECIFIED:kotlin.Int) The operation has failed due to an unknown or unspecified error. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CallEndpointException](https://developer.android.com/reference/kotlin/android/telecom/CallEndpointException#CallEndpointException(kotlin.String,%20kotlin.Int))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/telecom/CallEndpointException#describeContents())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCode](https://developer.android.com/reference/kotlin/android/telecom/CallEndpointException#getCode())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/telecom/CallEndpointException#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [CallEndpointException](https://developer.android.com/reference/kotlin/android/telecom/CallEndpointException#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/telecom/CallEndpointException#CREATOR:android.os.Parcelable.Creator) Responsible for creating CallEndpointException objects for deserialized Parcels. |

## Constants

### ERROR_ANOTHER_REQUEST

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_ANOTHER_REQUEST: Int
```

The operation was canceled by another request. 

 Value: 3

### ERROR_ENDPOINT_DOES_NOT_EXIST

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_ENDPOINT_DOES_NOT_EXIST: Int
```

The operation has failed because requested CallEndpoint does not exist. 

 Value: 1

### ERROR_REQUEST_TIME_OUT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_REQUEST_TIME_OUT: Int
```

The operation was not completed on time. 

 Value: 2

### ERROR_UNSPECIFIED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_UNSPECIFIED: Int
```

The operation has failed due to an unknown or unspecified error. 

 Value: 4

## Public constructors

### CallEndpointException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CallEndpointException(
    message: String?, 
    code: Int)
```

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telecom.CallEndpointException#ERROR_ENDPOINT_DOES_NOT_EXIST](https://developer.android.com/reference/kotlin/android/telecom/CallEndpointException#ERROR_ENDPOINT_DOES_NOT_EXIST:kotlin.Int), [android.telecom.CallEndpointException#ERROR_REQUEST_TIME_OUT](https://developer.android.com/reference/kotlin/android/telecom/CallEndpointException#ERROR_REQUEST_TIME_OUT:kotlin.Int), [android.telecom.CallEndpointException#ERROR_ANOTHER_REQUEST](https://developer.android.com/reference/kotlin/android/telecom/CallEndpointException#ERROR_ANOTHER_REQUEST:kotlin.Int), or [android.telecom.CallEndpointException#ERROR_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/telecom/CallEndpointException#ERROR_UNSPECIFIED:kotlin.Int) |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.telecom.CallEndpointException#ERROR_ENDPOINT_DOES_NOT_EXIST](https://developer.android.com/reference/kotlin/android/telecom/CallEndpointException#ERROR_ENDPOINT_DOES_NOT_EXIST:kotlin.Int), [android.telecom.CallEndpointException#ERROR_REQUEST_TIME_OUT](https://developer.android.com/reference/kotlin/android/telecom/CallEndpointException#ERROR_REQUEST_TIME_OUT:kotlin.Int), [android.telecom.CallEndpointException#ERROR_ANOTHER_REQUEST](https://developer.android.com/reference/kotlin/android/telecom/CallEndpointException#ERROR_ANOTHER_REQUEST:kotlin.Int), or [android.telecom.CallEndpointException#ERROR_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/telecom/CallEndpointException#ERROR_UNSPECIFIED:kotlin.Int) |

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<CallEndpointException!>
```

Responsible for creating CallEndpointException objects for deserialized Parcels.
