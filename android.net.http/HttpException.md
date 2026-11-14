# HttpException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# HttpException

Kotlin| [Java](../android/net/http/HttpException.md) 
| --- | --- |

```
open class HttpException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [java.io.IOException](../java/io/IOException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.net.http.HttpException](../android/net/http/HttpException.md) |

| Known Direct Subclasses [CallbackException](../android/net/http/CallbackException.md), [NetworkException](../android/net/http/NetworkException.md) |--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CallbackException](../android/net/http/CallbackException.md) | Exception passed to [UrlRequest.Callback.onFailed()](../android/net/http/UrlRequest.Callback.md))when [UrlRequest.Callback](../android/net/http/UrlRequest.Callback.md) or [UploadDataProvider](../android/net/http/UploadDataProvider.md) method throws an exception. | | [NetworkException](../android/net/http/NetworkException.md) | Exception passed to [UrlRequest.Callback.onFailed()](../android/net/http/UrlRequest.Callback.md))when the HTTP stack fails to process a network request. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [QuicException](../android/net/http/QuicException.md) |------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [QuicException](../android/net/http/QuicException.md) | Subclass of [NetworkException](../android/net/http/NetworkException.md) which contains a detailed [QUIC](https://www.chromium.org/quic) error code from [QuicErrorCode](https://cs.chromium.org/search/?q=symbol:%5CbQuicErrorCode%5Cb). | |
| --- | --- | --- | --- | --- | --- | --- |

Base exception passed to [UrlRequest.Callback.onFailed()](../android/net/http/UrlRequest.Callback.md)).

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [HttpException](../android/net/http/HttpException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Constructs an exception that is caused by`cause`. |

## Public constructors

### HttpException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
HttpException(
    message: String?, 
    cause: Throwable?)
```

Constructs an exception that is caused by`cause`.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:explanation of failure. This value may be`null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:the cause (which is saved for later retrieval by the [getCause()](../java/lang/Throwable.md))method). A null value is permitted, and indicates that the cause is nonexistent or unknown. |
