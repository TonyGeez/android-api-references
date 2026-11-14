# AppSearchException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppSearchException

Kotlin| [Java](AppSearchException.md) 
| --- | --- |

```
open class AppSearchException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||
| | | ↳ | [android.app.appsearch.exceptions.AppSearchException](AppSearchException.md) |
| --- | --- | --- | --- |

An exception thrown by [android.app.appsearch.AppSearchSession](../android.app.appsearch/AppSearchSession.md) or a subcomponent.

These exceptions can be converted into a failed [AppSearchResult](../android.app.appsearch/AppSearchResult.md) for propagating to the client.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AppSearchException](AppSearchException.md))`(`resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Initializes an [AppSearchException](AppSearchException.md) with no message. |
| [AppSearchException](AppSearchException.md))`(`resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Initializes an [AppSearchException](AppSearchException.md) with a result code and message. |
| [AppSearchException](AppSearchException.md))`(`resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Initializes an [AppSearchException](AppSearchException.md) with a result code, message and cause. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResultCode](AppSearchException.md))`()` Returns the result code this exception was constructed with. |
| open [AppSearchResult](../android.app.appsearch/AppSearchResult.md)\<T\> | [toAppSearchResult](AppSearchException.md))`()` Converts this [java.lang.Exception](../java.lang/Exception.md) into a failed [AppSearchResult](../android.app.appsearch/AppSearchResult.md). |

## Public constructors

### AppSearchException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AppSearchException(resultCode: Int)
```

Initializes an [AppSearchException](AppSearchException.md) with no message.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resultCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of the constants documented in [AppSearchResult.getResultCode](../android.app.appsearch/AppSearchResult.md)). Value is [android.app.appsearch.AppSearchResult#RESULT_OK](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_UNKNOWN_ERROR](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_INTERNAL_ERROR](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_INVALID_ARGUMENT](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_IO_ERROR](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_OUT_OF_SPACE](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_NOT_FOUND](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_INVALID_SCHEMA](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_SECURITY_ERROR](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_DENIED](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_RATE_LIMITED](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_ALREADY_EXISTS](../android.app.appsearch/AppSearchResult.md), android.app.appsearch.AppSearchResult.RESULT_ABORTED, or android.app.appsearch.AppSearchResult.RESULT_UNAVAILABLE |

### AppSearchException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AppSearchException(
    resultCode: Int, 
    message: String?)
```

Initializes an [AppSearchException](AppSearchException.md) with a result code and message.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resultCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of the constants documented in [AppSearchResult.getResultCode](../android.app.appsearch/AppSearchResult.md)). Value is [android.app.appsearch.AppSearchResult#RESULT_OK](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_UNKNOWN_ERROR](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_INTERNAL_ERROR](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_INVALID_ARGUMENT](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_IO_ERROR](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_OUT_OF_SPACE](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_NOT_FOUND](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_INVALID_SCHEMA](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_SECURITY_ERROR](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_DENIED](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_RATE_LIMITED](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_ALREADY_EXISTS](../android.app.appsearch/AppSearchResult.md), android.app.appsearch.AppSearchResult.RESULT_ABORTED, or android.app.appsearch.AppSearchResult.RESULT_UNAVAILABLE |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The detail message (which is saved for later retrieval by the [getMessage()](../java.lang/Throwable.md))method). This value may be`null`. |

### AppSearchException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AppSearchException(
    resultCode: Int, 
    message: String?, 
    cause: Throwable?)
```

Initializes an [AppSearchException](AppSearchException.md) with a result code, message and cause.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resultCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of the constants documented in [AppSearchResult.getResultCode](../android.app.appsearch/AppSearchResult.md)). Value is [android.app.appsearch.AppSearchResult#RESULT_OK](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_UNKNOWN_ERROR](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_INTERNAL_ERROR](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_INVALID_ARGUMENT](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_IO_ERROR](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_OUT_OF_SPACE](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_NOT_FOUND](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_INVALID_SCHEMA](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_SECURITY_ERROR](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_DENIED](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_RATE_LIMITED](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_ALREADY_EXISTS](../android.app.appsearch/AppSearchResult.md), android.app.appsearch.AppSearchResult.RESULT_ABORTED, or android.app.appsearch.AppSearchResult.RESULT_UNAVAILABLE |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The detail message (which is saved for later retrieval by the [getMessage()](../java.lang/Throwable.md))method). This value may be`null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:The cause (which is saved for later retrieval by the [getCause()](../java.lang/Throwable.md))method). (A null value is permitted, and indicates that the cause is nonexistent or unknown.) |
| --- | --- |

## Public methods

### getResultCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getResultCode(): Int
```

Returns the result code this exception was constructed with.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | One of the constants documented in [AppSearchResult.getResultCode](../android.app.appsearch/AppSearchResult.md)). Value is [android.app.appsearch.AppSearchResult#RESULT_OK](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_UNKNOWN_ERROR](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_INTERNAL_ERROR](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_INVALID_ARGUMENT](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_IO_ERROR](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_OUT_OF_SPACE](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_NOT_FOUND](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_INVALID_SCHEMA](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_SECURITY_ERROR](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_DENIED](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_RATE_LIMITED](../android.app.appsearch/AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_ALREADY_EXISTS](../android.app.appsearch/AppSearchResult.md), android.app.appsearch.AppSearchResult.RESULT_ABORTED, or android.app.appsearch.AppSearchResult.RESULT_UNAVAILABLE |

### toAppSearchResult

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> toAppSearchResult(): AppSearchResult<T>
```

Converts this [java.lang.Exception](../java.lang/Exception.md) into a failed [AppSearchResult](../android.app.appsearch/AppSearchResult.md).

| Return ||
|------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [AppSearchResult](../android.app.appsearch/AppSearchResult.md)<T> | This value cannot be`null`. |
