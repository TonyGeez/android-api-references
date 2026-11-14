# HealthConnectException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HealthConnectException

Kotlin| [Java](https://developer.android.com/reference/android/health/connect/HealthConnectException "View this page in Java") 

```
open class HealthConnectException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| | | | ↳ | [android.health.connect.HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException#) |

Class representing health connect exceptions.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DATA_SYNC_IN_PROGRESS](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException#ERROR_DATA_SYNC_IN_PROGRESS:kotlin.Int) Data sync is in progress. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INTERNAL](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException#ERROR_INTERNAL:kotlin.Int) An internal error occurred which the caller cannot address. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_ARGUMENT](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException#ERROR_INVALID_ARGUMENT:kotlin.Int) The caller supplied invalid arguments to the call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_IO](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException#ERROR_IO:kotlin.Int) An issue occurred reading or writing to storage. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_RATE_LIMIT_EXCEEDED](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException#ERROR_RATE_LIMIT_EXCEEDED:kotlin.Int) The caller exhausted the allotted rate limit. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_REMOTE](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException#ERROR_REMOTE:kotlin.Int) An IPC related error occurred. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_SECURITY](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException#ERROR_SECURITY:kotlin.Int) The caller doesn't have the correct permissions for this call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNKNOWN](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException#ERROR_UNKNOWN:kotlin.Int) An unknown error occurred while processing the call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNSUPPORTED_OPERATION](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException#ERROR_UNSUPPORTED_OPERATION:kotlin.Int) This operation is currently not supported by the platform. |

| Public methods ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorCode](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException#getErrorCode())`()` <br /> |

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

This error may be considered similar to [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) 

 Value: 2

### ERROR_INVALID_ARGUMENT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INVALID_ARGUMENT: Int
```

The caller supplied invalid arguments to the call.

This error may be considered similar to [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#). 

 Value: 3

### ERROR_IO

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_IO: Int
```

An issue occurred reading or writing to storage. The call might succeed if repeated.

This error may be considered similar to [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#). 

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

This error may be considered similar to [android.os.RemoteException](https://developer.android.com/reference/kotlin/android/os/RemoteException.html#). 

 Value: 6

### ERROR_SECURITY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_SECURITY: Int
```

The caller doesn't have the correct permissions for this call.

This error may be considered similar to [java.lang.SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#). 

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
