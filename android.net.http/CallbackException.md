# CallbackException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# CallbackException

Kotlin| [Java](CallbackException.md) 
| --- | --- |

```
abstract class CallbackException : HttpException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.io.IOException](../java.io/IOException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.net.http.HttpException](HttpException.md) ||
| | | | | ↳ | [android.net.http.CallbackException](CallbackException.md) |

Exception passed to [UrlRequest.Callback.onFailed()](../android/net/http/UrlRequest.Callback.md))when [UrlRequest.Callback](../android/net/http/UrlRequest.Callback.md) or [UploadDataProvider](UploadDataProvider.md) method throws an exception. In this case [getCause()](../java.lang/Throwable.md))can be used to find the thrown exception.

## Summary

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CallbackException](CallbackException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Constructs an exception that wraps`cause`thrown by a [UrlRequest.Callback](../android/net/http/UrlRequest.Callback.md). |

## Protected constructors

### CallbackException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
protected CallbackException(
    message: String?, 
    cause: Throwable?)
```

Constructs an exception that wraps`cause`thrown by a [UrlRequest.Callback](../android/net/http/UrlRequest.Callback.md).

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:explanation of failure. This value may be`null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:exception thrown by [UrlRequest.Callback](../android/net/http/UrlRequest.Callback.md) that's being wrapped. It is saved for later retrieval by the [getCause()](../java.lang/Throwable.md)). This value may be`null`. |
