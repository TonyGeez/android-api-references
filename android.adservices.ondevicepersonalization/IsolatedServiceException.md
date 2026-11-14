# IsolatedServiceException

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IsolatedServiceException

Kotlin| [Java](IsolatedServiceException.md) 
| --- | --- |

```
class IsolatedServiceException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||
| | | ↳ | [android.adservices.ondevicepersonalization.IsolatedServiceException](IsolatedServiceException.md) |
| --- | --- | --- | --- |

A class that an [IsolatedService](IsolatedService.md) can use to signal a failure in handling a request and return an error to be logged and aggregated. The error is not reported to the app that invoked the [IsolatedService](IsolatedService.md) in order to prevent data leakage from the [IsolatedService](IsolatedService.md) to an app. The platform does not interpret the error code, it only logs and aggregates it.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IsolatedServiceException](IsolatedServiceException.md))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates an [IsolatedServiceException](IsolatedServiceException.md) with an error code to be logged. |
| [IsolatedServiceException](IsolatedServiceException.md))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Creates an [IsolatedServiceException](IsolatedServiceException.md) with an error code to be logged. |
| [IsolatedServiceException](IsolatedServiceException.md))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Creates an [IsolatedServiceException](IsolatedServiceException.md) with an error code to be logged. |

| Public methods ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorCode](IsolatedServiceException.md))`()` Returns the error code for this exception. |

## Public constructors

### IsolatedServiceException

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IsolatedServiceException(errorCode: Int)
```

Creates an [IsolatedServiceException](IsolatedServiceException.md) with an error code to be logged. The meaning of the error code is defined by the [IsolatedService](IsolatedService.md). The platform does not interpret the error code.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):An error code defined by the [IsolatedService](IsolatedService.md). |

### IsolatedServiceException

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IsolatedServiceException(
    errorCode: Int, 
    message: String?, 
    cause: Throwable?)
```

Creates an [IsolatedServiceException](IsolatedServiceException.md) with an error code to be logged. The meaning of the error code is defined by the [IsolatedService](IsolatedService.md). The platform does not interpret the error code.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):An error code defined by the [IsolatedService](IsolatedService.md). |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:the exception message. This value may be`null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:the cause of this exception. This value may be`null`. |
| --- | --- |

### IsolatedServiceException

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IsolatedServiceException(
    errorCode: Int, 
    cause: Throwable?)
```

Creates an [IsolatedServiceException](IsolatedServiceException.md) with an error code to be logged. The meaning of the error code is defined by the [IsolatedService](IsolatedService.md). The platform does not interpret the error code.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):An error code defined by the [IsolatedService](IsolatedService.md). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:the cause of this exception. This value may be`null`. |

## Public methods

### getErrorCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getErrorCode(): Int
```

Returns the error code for this exception.
