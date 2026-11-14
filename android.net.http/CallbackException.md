# CallbackException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# CallbackException

Kotlin| [Java](https://developer.android.com/reference/android/net/http/CallbackException "View this page in Java") 
| --- | --- |

```
abstract class CallbackException : HttpException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.net.http.HttpException](https://developer.android.com/reference/kotlin/android/net/http/HttpException) ||
| | | | | ↳ | [android.net.http.CallbackException](https://developer.android.com/reference/kotlin/android/net/http/CallbackException#) |

Exception passed to [UrlRequest.Callback.onFailed()](https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException))when [UrlRequest.Callback](https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback) or [UploadDataProvider](https://developer.android.com/reference/kotlin/android/net/http/UploadDataProvider) method throws an exception. In this case [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())can be used to find the thrown exception.

## Summary

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CallbackException](https://developer.android.com/reference/kotlin/android/net/http/CallbackException#CallbackException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Constructs an exception that wraps`cause`thrown by a [UrlRequest.Callback](https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback). |

## Protected constructors

### CallbackException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
protected CallbackException(
    message: String?, 
    cause: Throwable?)
```

Constructs an exception that wraps`cause`thrown by a [UrlRequest.Callback](https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback).

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:explanation of failure. This value may be`null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:exception thrown by [UrlRequest.Callback](https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback) that's being wrapped. It is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause()). This value may be`null`. |
