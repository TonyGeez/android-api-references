# AconfigStorageReadException

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AconfigStorageReadException

Kotlin| [Java](AconfigStorageReadException.md) 
| --- | --- |

```
open class AconfigStorageReadException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.os.flagging.AconfigStorageReadException](AconfigStorageReadException.md) |

Exception thrown when an error occurs while reading from Aconfig Storage.

This exception indicates a problem accessing or retrieving configuration data from Aconfig Storage. This could be due to various reasons, such as:

- The Aconfig Storage system is not found on the device.
- The requested configuration package is not found.
- The specified container is not found.
- There was an error reading the Aconfig Storage file.
- The fingerprint of the Aconfig Storage file does not match the expected fingerprint.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CANNOT_READ_STORAGE_FILE](AconfigStorageReadException.md) Error code indicating that there was an error reading the Aconfig Storage file. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CONTAINER_NOT_FOUND](AconfigStorageReadException.md) Error code indicating that the specified container is not found. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_GENERIC](AconfigStorageReadException.md) Generic error code indicating an unspecified Aconfig Storage error. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_PACKAGE_NOT_FOUND](AconfigStorageReadException.md) Error code indicating that the requested configuration package is not found. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_STORAGE_SYSTEM_NOT_FOUND](AconfigStorageReadException.md) Error code indicating that the Aconfig Storage system is not found on the device. |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AconfigStorageReadException](AconfigStorageReadException.md))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Constructs a new`AconfigStorageReadException`with the specified error code and detail message. |
| [AconfigStorageReadException](AconfigStorageReadException.md))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`)` Constructs a new`AconfigStorageReadException`with the specified error code, detail message, and cause. |
| [AconfigStorageReadException](AconfigStorageReadException.md))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`)` Constructs a new`AconfigStorageReadException`with the specified error code and cause. |

| Public methods ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorCode](AconfigStorageReadException.md))`()` Returns the error code associated with this exception. |

| Properties ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [message](AconfigStorageReadException.md) Returns the error message for this exception, including the error code and the original message. |

## Constants

### ERROR_CANNOT_READ_STORAGE_FILE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CANNOT_READ_STORAGE_FILE: Int
```

Error code indicating that there was an error reading the Aconfig Storage file. 

 Value: 4

### ERROR_CONTAINER_NOT_FOUND

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CONTAINER_NOT_FOUND: Int
```

Error code indicating that the specified container is not found. 

 Value: 3

### ERROR_GENERIC

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_GENERIC: Int
```

Generic error code indicating an unspecified Aconfig Storage error. 

 Value: 0

### ERROR_PACKAGE_NOT_FOUND

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_PACKAGE_NOT_FOUND: Int
```

Error code indicating that the requested configuration package is not found. 

 Value: 2

### ERROR_STORAGE_SYSTEM_NOT_FOUND

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_STORAGE_SYSTEM_NOT_FOUND: Int
```

Error code indicating that the Aconfig Storage system is not found on the device. 

 Value: 1

## Public constructors

### AconfigStorageReadException

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AconfigStorageReadException(
    errorCode: Int, 
    msg: String)
```

Constructs a new`AconfigStorageReadException`with the specified error code and detail message.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The error code for this exception. Value is [android.os.flagging.AconfigStorageReadException#ERROR_GENERIC](AconfigStorageReadException.md), [android.os.flagging.AconfigStorageReadException#ERROR_STORAGE_SYSTEM_NOT_FOUND](AconfigStorageReadException.md), [android.os.flagging.AconfigStorageReadException#ERROR_PACKAGE_NOT_FOUND](AconfigStorageReadException.md), [android.os.flagging.AconfigStorageReadException#ERROR_CONTAINER_NOT_FOUND](AconfigStorageReadException.md), [android.os.flagging.AconfigStorageReadException#ERROR_CANNOT_READ_STORAGE_FILE](AconfigStorageReadException.md), or android.os.flagging.AconfigStorageReadException.ERROR_FILE_FINGERPRINT_MISMATCH |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The detail message for this exception. This value cannot be`null`. |

### AconfigStorageReadException

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AconfigStorageReadException(
    errorCode: Int, 
    msg: String, 
    cause: Throwable)
```

Constructs a new`AconfigStorageReadException`with the specified error code, detail message, and cause.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The error code for this exception. Value is [android.os.flagging.AconfigStorageReadException#ERROR_GENERIC](AconfigStorageReadException.md), [android.os.flagging.AconfigStorageReadException#ERROR_STORAGE_SYSTEM_NOT_FOUND](AconfigStorageReadException.md), [android.os.flagging.AconfigStorageReadException#ERROR_PACKAGE_NOT_FOUND](AconfigStorageReadException.md), [android.os.flagging.AconfigStorageReadException#ERROR_CONTAINER_NOT_FOUND](AconfigStorageReadException.md), [android.os.flagging.AconfigStorageReadException#ERROR_CANNOT_READ_STORAGE_FILE](AconfigStorageReadException.md), or android.os.flagging.AconfigStorageReadException.ERROR_FILE_FINGERPRINT_MISMATCH |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The detail message for this exception. This value cannot be`null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html):The cause of this exception. This value cannot be`null`. |
| --- | --- |

### AconfigStorageReadException

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AconfigStorageReadException(
    errorCode: Int, 
    cause: Throwable)
```

Constructs a new`AconfigStorageReadException`with the specified error code and cause.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The error code for this exception. Value is [android.os.flagging.AconfigStorageReadException#ERROR_GENERIC](AconfigStorageReadException.md), [android.os.flagging.AconfigStorageReadException#ERROR_STORAGE_SYSTEM_NOT_FOUND](AconfigStorageReadException.md), [android.os.flagging.AconfigStorageReadException#ERROR_PACKAGE_NOT_FOUND](AconfigStorageReadException.md), [android.os.flagging.AconfigStorageReadException#ERROR_CONTAINER_NOT_FOUND](AconfigStorageReadException.md), [android.os.flagging.AconfigStorageReadException#ERROR_CANNOT_READ_STORAGE_FILE](AconfigStorageReadException.md), or android.os.flagging.AconfigStorageReadException.ERROR_FILE_FINGERPRINT_MISMATCH |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html):The cause of this exception. This value cannot be`null`. |

## Public methods

### getErrorCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getErrorCode(): Int
```

Returns the error code associated with this exception.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The error code. Value is [android.os.flagging.AconfigStorageReadException#ERROR_GENERIC](AconfigStorageReadException.md), [android.os.flagging.AconfigStorageReadException#ERROR_STORAGE_SYSTEM_NOT_FOUND](AconfigStorageReadException.md), [android.os.flagging.AconfigStorageReadException#ERROR_PACKAGE_NOT_FOUND](AconfigStorageReadException.md), [android.os.flagging.AconfigStorageReadException#ERROR_CONTAINER_NOT_FOUND](AconfigStorageReadException.md), [android.os.flagging.AconfigStorageReadException#ERROR_CANNOT_READ_STORAGE_FILE](AconfigStorageReadException.md), or android.os.flagging.AconfigStorageReadException.ERROR_FILE_FINGERPRINT_MISMATCH |

## Properties

### message

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val message: String
```

Returns the error message for this exception, including the error code and the original message.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The error message. This value cannot be`null`. |
