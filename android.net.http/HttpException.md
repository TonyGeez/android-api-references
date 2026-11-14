# HttpException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# HttpException

Kotlin| [Java](https://developer.android.com/reference/android/net/http/HttpException "View this page in Java") 

```
open class HttpException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) ||
| | | | ↳ | [android.net.http.HttpException](https://developer.android.com/reference/kotlin/android/net/http/HttpException#) |

| Known Direct Subclasses [CallbackException](https://developer.android.com/reference/kotlin/android/net/http/CallbackException), [NetworkException](https://developer.android.com/reference/kotlin/android/net/http/NetworkException) |--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CallbackException](https://developer.android.com/reference/kotlin/android/net/http/CallbackException) | Exception passed to [UrlRequest.Callback.onFailed()](https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException))when [UrlRequest.Callback](https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback) or [UploadDataProvider](https://developer.android.com/reference/kotlin/android/net/http/UploadDataProvider) method throws an exception. | | [NetworkException](https://developer.android.com/reference/kotlin/android/net/http/NetworkException) | Exception passed to [UrlRequest.Callback.onFailed()](https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException))when the HTTP stack fails to process a network request. | |

| Known Indirect Subclasses [QuicException](https://developer.android.com/reference/kotlin/android/net/http/QuicException) |------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [QuicException](https://developer.android.com/reference/kotlin/android/net/http/QuicException) | Subclass of [NetworkException](https://developer.android.com/reference/kotlin/android/net/http/NetworkException) which contains a detailed [QUIC](https://www.chromium.org/quic) error code from [QuicErrorCode](https://cs.chromium.org/search/?q=symbol:%5CbQuicErrorCode%5Cb). | |

Base exception passed to [UrlRequest.Callback.onFailed()](https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)).

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [HttpException](https://developer.android.com/reference/kotlin/android/net/http/HttpException#HttpException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Constructs an exception that is caused by`cause`. |

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
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method). A null value is permitted, and indicates that the cause is nonexistent or unknown. |
