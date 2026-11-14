# QueryLocationException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# QueryLocationException

Kotlin| [Java](https://developer.android.com/reference/android/telecom/QueryLocationException "View this page in Java") 
| --- | --- |

```
class QueryLocationException : RuntimeException, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.telecom.QueryLocationException](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#) |

This class represents a set of exceptions that can occur when requesting a [Connection.queryLocationForEmergency(long, String, Executor, OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/telecom/Connection#queryLocationForEmergency(kotlin.Long,%20kotlin.String,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NOT_ALLOWED_FOR_NON_EMERGENCY_CONNECTIONS](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_NOT_ALLOWED_FOR_NON_EMERGENCY_CONNECTIONS:kotlin.Int) The operation has failed due to a location query being requested for a non-emergency connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NOT_PERMITTED](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_NOT_PERMITTED:kotlin.Int) The operation has failed because it is not permitted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_PREVIOUS_REQUEST_EXISTS](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_PREVIOUS_REQUEST_EXISTS:kotlin.Int) The operation was rejected due to an existing request. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_REQUEST_TIME_OUT](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_REQUEST_TIME_OUT:kotlin.Int) The operation was not completed on time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_SERVICE_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_SERVICE_UNAVAILABLE:kotlin.Int) The operation has failed due to the service is not available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_UNSPECIFIED:kotlin.Int) The operation has failed due to an unknown or unspecified error. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [QueryLocationException](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#QueryLocationException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> |
| [QueryLocationException](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#QueryLocationException(kotlin.String,%20kotlin.Int))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [QueryLocationException](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#QueryLocationException(kotlin.String,%20kotlin.Int,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#describeContents())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCode](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#getCode())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [QueryLocationException](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#CREATOR:android.os.Parcelable.Creator) Responsible for creating QueryLocationException objects for deserialized Parcels. |

## Constants

### ERROR_NOT_ALLOWED_FOR_NON_EMERGENCY_CONNECTIONS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_NOT_ALLOWED_FOR_NON_EMERGENCY_CONNECTIONS: Int
```

The operation has failed due to a location query being requested for a non-emergency connection. 

 Value: 4

### ERROR_NOT_PERMITTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_NOT_PERMITTED: Int
```

The operation has failed because it is not permitted. 

 Value: 3

### ERROR_PREVIOUS_REQUEST_EXISTS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_PREVIOUS_REQUEST_EXISTS: Int
```

The operation was rejected due to an existing request. 

 Value: 2

### ERROR_REQUEST_TIME_OUT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_REQUEST_TIME_OUT: Int
```

The operation was not completed on time. 

 Value: 1

### ERROR_SERVICE_UNAVAILABLE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_SERVICE_UNAVAILABLE: Int
```

The operation has failed due to the service is not available. 

 Value: 5

### ERROR_UNSPECIFIED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_UNSPECIFIED: Int
```

The operation has failed due to an unknown or unspecified error. 

 Value: 6

## Public constructors

### QueryLocationException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
QueryLocationException(message: String?)
```

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |

### QueryLocationException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
QueryLocationException(
    message: String?, 
    code: Int)
```

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telecom.QueryLocationException#ERROR_REQUEST_TIME_OUT](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_REQUEST_TIME_OUT:kotlin.Int), [android.telecom.QueryLocationException#ERROR_PREVIOUS_REQUEST_EXISTS](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_PREVIOUS_REQUEST_EXISTS:kotlin.Int), [android.telecom.QueryLocationException#ERROR_NOT_PERMITTED](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_NOT_PERMITTED:kotlin.Int), [android.telecom.QueryLocationException#ERROR_NOT_ALLOWED_FOR_NON_EMERGENCY_CONNECTIONS](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_NOT_ALLOWED_FOR_NON_EMERGENCY_CONNECTIONS:kotlin.Int), [android.telecom.QueryLocationException#ERROR_SERVICE_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_SERVICE_UNAVAILABLE:kotlin.Int), or [android.telecom.QueryLocationException#ERROR_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_UNSPECIFIED:kotlin.Int) |

### QueryLocationException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
QueryLocationException(
    message: String?, 
    code: Int, 
    cause: Throwable?)
```

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telecom.QueryLocationException#ERROR_REQUEST_TIME_OUT](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_REQUEST_TIME_OUT:kotlin.Int), [android.telecom.QueryLocationException#ERROR_PREVIOUS_REQUEST_EXISTS](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_PREVIOUS_REQUEST_EXISTS:kotlin.Int), [android.telecom.QueryLocationException#ERROR_NOT_PERMITTED](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_NOT_PERMITTED:kotlin.Int), [android.telecom.QueryLocationException#ERROR_NOT_ALLOWED_FOR_NON_EMERGENCY_CONNECTIONS](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_NOT_ALLOWED_FOR_NON_EMERGENCY_CONNECTIONS:kotlin.Int), [android.telecom.QueryLocationException#ERROR_SERVICE_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_SERVICE_UNAVAILABLE:kotlin.Int), or [android.telecom.QueryLocationException#ERROR_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_UNSPECIFIED:kotlin.Int) |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:This value may be`null`. |
| --- | --- |

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
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.telecom.QueryLocationException#ERROR_REQUEST_TIME_OUT](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_REQUEST_TIME_OUT:kotlin.Int), [android.telecom.QueryLocationException#ERROR_PREVIOUS_REQUEST_EXISTS](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_PREVIOUS_REQUEST_EXISTS:kotlin.Int), [android.telecom.QueryLocationException#ERROR_NOT_PERMITTED](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_NOT_PERMITTED:kotlin.Int), [android.telecom.QueryLocationException#ERROR_NOT_ALLOWED_FOR_NON_EMERGENCY_CONNECTIONS](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_NOT_ALLOWED_FOR_NON_EMERGENCY_CONNECTIONS:kotlin.Int), [android.telecom.QueryLocationException#ERROR_SERVICE_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_SERVICE_UNAVAILABLE:kotlin.Int), or [android.telecom.QueryLocationException#ERROR_UNSPECIFIED](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException#ERROR_UNSPECIFIED:kotlin.Int) |

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
static val CREATOR: Parcelable.Creator<QueryLocationException!>
```

Responsible for creating QueryLocationException objects for deserialized Parcels.
