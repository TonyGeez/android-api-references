# QuicException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# QuicException

Kotlin| [Java](https://developer.android.com/reference/android/net/http/QuicException "View this page in Java") 
| --- | --- |

```
abstract class QuicException : NetworkException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.net.http.HttpException](https://developer.android.com/reference/kotlin/android/net/http/HttpException) |||
| | | | | ↳ | [android.net.http.NetworkException](https://developer.android.com/reference/kotlin/android/net/http/NetworkException) ||
| | | | | | ↳ | [android.net.http.QuicException](https://developer.android.com/reference/kotlin/android/net/http/QuicException#) |
| --- | --- | --- | --- | --- | --- | --- |

Subclass of [NetworkException](https://developer.android.com/reference/kotlin/android/net/http/NetworkException) which contains a detailed [QUIC](https://www.chromium.org/quic) error code from [QuicErrorCode](https://cs.chromium.org/search/?q=symbol:%5CbQuicErrorCode%5Cb). An instance of`QuicException`is passed to`onFailed`callbacks when the error code is [NetworkException.ERROR_QUIC_PROTOCOL_FAILED](https://developer.android.com/reference/kotlin/android/net/http/NetworkException#ERROR_QUIC_PROTOCOL_FAILED:kotlin.Int).

## Summary

| Inherited constants ||
|---|---|
| From class [NetworkException](https://developer.android.com/reference/kotlin/android/net/http/NetworkException) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_ADDRESS_UNREACHABLE](https://developer.android.com/reference/kotlin/android/net/http/NetworkException#ERROR_ADDRESS_UNREACHABLE:kotlin.Int) <br /> Error code indicating the IP address being contacted is unreachable, meaning there is no route to the specified host or network. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CONNECTION_CLOSED](https://developer.android.com/reference/kotlin/android/net/http/NetworkException#ERROR_CONNECTION_CLOSED:kotlin.Int) <br /> Error code indicating the connection was closed unexpectedly. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CONNECTION_REFUSED](https://developer.android.com/reference/kotlin/android/net/http/NetworkException#ERROR_CONNECTION_REFUSED:kotlin.Int) <br /> Error code indicating the connection attempt was refused. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CONNECTION_RESET](https://developer.android.com/reference/kotlin/android/net/http/NetworkException#ERROR_CONNECTION_RESET:kotlin.Int) <br /> Error code indicating the connection was unexpectedly reset. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CONNECTION_TIMED_OUT](https://developer.android.com/reference/kotlin/android/net/http/NetworkException#ERROR_CONNECTION_TIMED_OUT:kotlin.Int) <br /> Error code indicating the connection attempt timed out. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_HOSTNAME_NOT_RESOLVED](https://developer.android.com/reference/kotlin/android/net/http/NetworkException#ERROR_HOSTNAME_NOT_RESOLVED:kotlin.Int) <br /> Error code indicating the host being sent the request could not be resolved to an IP address. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INTERNET_DISCONNECTED](https://developer.android.com/reference/kotlin/android/net/http/NetworkException#ERROR_INTERNET_DISCONNECTED:kotlin.Int) <br /> Error code indicating the device was not connected to any network. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NETWORK_CHANGED](https://developer.android.com/reference/kotlin/android/net/http/NetworkException#ERROR_NETWORK_CHANGED:kotlin.Int) <br /> Error code indicating that as the request was processed the network configuration changed. When [getErrorCode](https://developer.android.com/reference/kotlin/android/net/http/NetworkException#getErrorCode())returns this code, this exception may be cast to [QuicException](https://developer.android.com/reference/kotlin/android/net/http/QuicException#) for more information if [QUIC](https://www.chromium.org/quic) protocol is used. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_OTHER](https://developer.android.com/reference/kotlin/android/net/http/NetworkException#ERROR_OTHER:kotlin.Int) <br /> Error code indicating another type of error was encountered. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_QUIC_PROTOCOL_FAILED](https://developer.android.com/reference/kotlin/android/net/http/NetworkException#ERROR_QUIC_PROTOCOL_FAILED:kotlin.Int) <br /> Error code indicating an error related to the [QUIC](https://www.chromium.org/quic) protocol. When [getErrorCode](https://developer.android.com/reference/kotlin/android/net/http/NetworkException#getErrorCode())returns this code, this exception can be cast to [QuicException](https://developer.android.com/reference/kotlin/android/net/http/QuicException#) for more information. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TIMED_OUT](https://developer.android.com/reference/kotlin/android/net/http/NetworkException#ERROR_TIMED_OUT:kotlin.Int) <br /> Error code indicating a timeout expired. Timeouts expiring while attempting to connect will be reported as the more specific [ERROR_CONNECTION_TIMED_OUT](https://developer.android.com/reference/kotlin/android/net/http/NetworkException#ERROR_CONNECTION_TIMED_OUT:kotlin.Int). <br /> | ||

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [QuicException](https://developer.android.com/reference/kotlin/android/net/http/QuicException#QuicException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Constructs an exception that is caused by a QUIC protocol error. |

| Inherited functions ||
|---|---|
| From class [NetworkException](https://developer.android.com/reference/kotlin/android/net/http/NetworkException) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorCode](https://developer.android.com/reference/kotlin/android/net/http/NetworkException#getErrorCode())`()` <br /> Returns error code, one of [ERROR_*](https://developer.android.com/reference/kotlin/android/net/http/NetworkException#ERROR_HOSTNAME_NOT_RESOLVED:kotlin.Int). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isImmediatelyRetryable](https://developer.android.com/reference/kotlin/android/net/http/NetworkException#isImmediatelyRetryable())`()` <br /> Returns`true`if retrying this request right away might succeed,`false`otherwise. For example returns`true`when [getErrorCode](https://developer.android.com/reference/kotlin/android/net/http/NetworkException#getErrorCode())returns [ERROR_NETWORK_CHANGED](https://developer.android.com/reference/kotlin/android/net/http/NetworkException#ERROR_NETWORK_CHANGED:kotlin.Int) because trying the request might succeed using the new network configuration, but`false`when`getErrorCode()`returns [ERROR_INTERNET_DISCONNECTED](https://developer.android.com/reference/kotlin/android/net/http/NetworkException#ERROR_INTERNET_DISCONNECTED:kotlin.Int) because retrying the request right away will encounter the same failure (instead retrying should be delayed until device regains network connectivity). <br /> | ||

## Protected constructors

### QuicException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
protected QuicException(
    message: String?, 
    cause: Throwable?)
```

Constructs an exception that is caused by a QUIC protocol error.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:explanation of failure. This value may be`null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method). A null value is permitted, and indicates that the cause is nonexistent or unknown. |
