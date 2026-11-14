# QueryLocationException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# QueryLocationException

Kotlin| [Java](../android/telecom/QueryLocationException.md) 
| --- | --- |

```
class QueryLocationException : RuntimeException, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.telecom.QueryLocationException](../android/telecom/QueryLocationException.md) |

This class represents a set of exceptions that can occur when requesting a [Connection.queryLocationForEmergency(long, String, Executor, OutcomeReceiver)](../android/telecom/Connection.md))

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NOT_ALLOWED_FOR_NON_EMERGENCY_CONNECTIONS](../android/telecom/QueryLocationException.md) The operation has failed due to a location query being requested for a non-emergency connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NOT_PERMITTED](../android/telecom/QueryLocationException.md) The operation has failed because it is not permitted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_PREVIOUS_REQUEST_EXISTS](../android/telecom/QueryLocationException.md) The operation was rejected due to an existing request. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_REQUEST_TIME_OUT](../android/telecom/QueryLocationException.md) The operation was not completed on time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_SERVICE_UNAVAILABLE](../android/telecom/QueryLocationException.md) The operation has failed due to the service is not available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNSPECIFIED](../android/telecom/QueryLocationException.md) The operation has failed due to an unknown or unspecified error. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [QueryLocationException](../android/telecom/QueryLocationException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> |
| [QueryLocationException](../android/telecom/QueryLocationException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [QueryLocationException](../android/telecom/QueryLocationException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/telecom/QueryLocationException.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCode](../android/telecom/QueryLocationException.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/telecom/QueryLocationException.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [QueryLocationException](../android/telecom/QueryLocationException.md)!\> | [CREATOR](../android/telecom/QueryLocationException.md) Responsible for creating QueryLocationException objects for deserialized Parcels. |

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
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telecom.QueryLocationException#ERROR_REQUEST_TIME_OUT](../android/telecom/QueryLocationException.md), [android.telecom.QueryLocationException#ERROR_PREVIOUS_REQUEST_EXISTS](../android/telecom/QueryLocationException.md), [android.telecom.QueryLocationException#ERROR_NOT_PERMITTED](../android/telecom/QueryLocationException.md), [android.telecom.QueryLocationException#ERROR_NOT_ALLOWED_FOR_NON_EMERGENCY_CONNECTIONS](../android/telecom/QueryLocationException.md), [android.telecom.QueryLocationException#ERROR_SERVICE_UNAVAILABLE](../android/telecom/QueryLocationException.md), or [android.telecom.QueryLocationException#ERROR_UNSPECIFIED](../android/telecom/QueryLocationException.md) |

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
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telecom.QueryLocationException#ERROR_REQUEST_TIME_OUT](../android/telecom/QueryLocationException.md), [android.telecom.QueryLocationException#ERROR_PREVIOUS_REQUEST_EXISTS](../android/telecom/QueryLocationException.md), [android.telecom.QueryLocationException#ERROR_NOT_PERMITTED](../android/telecom/QueryLocationException.md), [android.telecom.QueryLocationException#ERROR_NOT_ALLOWED_FOR_NON_EMERGENCY_CONNECTIONS](../android/telecom/QueryLocationException.md), [android.telecom.QueryLocationException#ERROR_SERVICE_UNAVAILABLE](../android/telecom/QueryLocationException.md), or [android.telecom.QueryLocationException#ERROR_UNSPECIFIED](../android/telecom/QueryLocationException.md) |
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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.telecom.QueryLocationException#ERROR_REQUEST_TIME_OUT](../android/telecom/QueryLocationException.md), [android.telecom.QueryLocationException#ERROR_PREVIOUS_REQUEST_EXISTS](../android/telecom/QueryLocationException.md), [android.telecom.QueryLocationException#ERROR_NOT_PERMITTED](../android/telecom/QueryLocationException.md), [android.telecom.QueryLocationException#ERROR_NOT_ALLOWED_FOR_NON_EMERGENCY_CONNECTIONS](../android/telecom/QueryLocationException.md), [android.telecom.QueryLocationException#ERROR_SERVICE_UNAVAILABLE](../android/telecom/QueryLocationException.md), or [android.telecom.QueryLocationException#ERROR_UNSPECIFIED](../android/telecom/QueryLocationException.md) |

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
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<QueryLocationException!>
```

Responsible for creating QueryLocationException objects for deserialized Parcels.
