# HealthConnectException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HealthConnectException

Kotlin| [Java](../android/health/connect/HealthConnectException.md) 
| --- | --- |

```
open class HealthConnectException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.health.connect.HealthConnectException](../android/health/connect/HealthConnectException.md) |

Class representing health connect exceptions.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DATA_SYNC_IN_PROGRESS](../android/health/connect/HealthConnectException.md) Data sync is in progress. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INTERNAL](../android/health/connect/HealthConnectException.md) An internal error occurred which the caller cannot address. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_ARGUMENT](../android/health/connect/HealthConnectException.md) The caller supplied invalid arguments to the call. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_IO](../android/health/connect/HealthConnectException.md) An issue occurred reading or writing to storage. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_RATE_LIMIT_EXCEEDED](../android/health/connect/HealthConnectException.md) The caller exhausted the allotted rate limit. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_REMOTE](../android/health/connect/HealthConnectException.md) An IPC related error occurred. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_SECURITY](../android/health/connect/HealthConnectException.md) The caller doesn't have the correct permissions for this call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNKNOWN](../android/health/connect/HealthConnectException.md) An unknown error occurred while processing the call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNSUPPORTED_OPERATION](../android/health/connect/HealthConnectException.md) This operation is currently not supported by the platform. |
| --- | --- |

| Public methods ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorCode](../android/health/connect/HealthConnectException.md))`()` <br /> |

## Constants

### ERROR_DATA_SYNC_IN_PROGRESS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_DATA_SYNC_IN_PROGRESS: Int
```

Data sync is in progress. Data read and writes are blocked.

Caller should try this api call again later. 

 Value: 8

### ERROR_INTERNAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INTERNAL: Int
```

An internal error occurred which the caller cannot address.

This error may be considered similar to [IllegalStateException](../java/lang/IllegalStateException.md) 

 Value: 2

### ERROR_INVALID_ARGUMENT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INVALID_ARGUMENT: Int
```

The caller supplied invalid arguments to the call.

This error may be considered similar to [IllegalArgumentException](../java/lang/IllegalArgumentException.md). 

 Value: 3

### ERROR_IO

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_IO: Int
```

An issue occurred reading or writing to storage. The call might succeed if repeated.

This error may be considered similar to [java.io.IOException](../java/io/IOException.md). 

 Value: 4

### ERROR_RATE_LIMIT_EXCEEDED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_RATE_LIMIT_EXCEEDED: Int
```

The caller exhausted the allotted rate limit. 

 Value: 7

### ERROR_REMOTE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_REMOTE: Int
```

An IPC related error occurred.

This error may be considered similar to [android.os.RemoteException](../android/os/RemoteException.md). 

 Value: 6

### ERROR_SECURITY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_SECURITY: Int
```

The caller doesn't have the correct permissions for this call.

This error may be considered similar to [java.lang.SecurityException](../java/lang/SecurityException.md). 

 Value: 5

### ERROR_UNKNOWN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_UNKNOWN: Int
```

An unknown error occurred while processing the call. 

 Value: 1

### ERROR_UNSUPPORTED_OPERATION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_UNSUPPORTED_OPERATION: Int
```

This operation is currently not supported by the platform.

Caller may try this api call again later. 

 Value: 9

## Public methods

### getErrorCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getErrorCode(): Int
```
