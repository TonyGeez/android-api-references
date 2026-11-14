# QuicException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# QuicException

Kotlin| [Java](../android/net/http/QuicException.md) 
| --- | --- |

```
abstract class QuicException : NetworkException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||||
| | | ↳ | [java.io.IOException](../java/io/IOException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.net.http.HttpException](../android/net/http/HttpException.md) |||
| | | | | ↳ | [android.net.http.NetworkException](../android/net/http/NetworkException.md) ||
| | | | | | ↳ | [android.net.http.QuicException](../android/net/http/QuicException.md) |
| --- | --- | --- | --- | --- | --- | --- |

Subclass of [NetworkException](../android/net/http/NetworkException.md) which contains a detailed [QUIC](https://www.chromium.org/quic) error code from [QuicErrorCode](https://cs.chromium.org/search/?q=symbol:%5CbQuicErrorCode%5Cb). An instance of`QuicException`is passed to`onFailed`callbacks when the error code is [NetworkException.ERROR_QUIC_PROTOCOL_FAILED](../android/net/http/NetworkException.md).

## Summary

| Inherited constants ||
|---|---|
| From class [NetworkException](../android/net/http/NetworkException.md) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_ADDRESS_UNREACHABLE](../android/net/http/NetworkException.md) <br /> Error code indicating the IP address being contacted is unreachable, meaning there is no route to the specified host or network. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CONNECTION_CLOSED](../android/net/http/NetworkException.md) <br /> Error code indicating the connection was closed unexpectedly. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CONNECTION_REFUSED](../android/net/http/NetworkException.md) <br /> Error code indicating the connection attempt was refused. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CONNECTION_RESET](../android/net/http/NetworkException.md) <br /> Error code indicating the connection was unexpectedly reset. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CONNECTION_TIMED_OUT](../android/net/http/NetworkException.md) <br /> Error code indicating the connection attempt timed out. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_HOSTNAME_NOT_RESOLVED](../android/net/http/NetworkException.md) <br /> Error code indicating the host being sent the request could not be resolved to an IP address. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INTERNET_DISCONNECTED](../android/net/http/NetworkException.md) <br /> Error code indicating the device was not connected to any network. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NETWORK_CHANGED](../android/net/http/NetworkException.md) <br /> Error code indicating that as the request was processed the network configuration changed. When [getErrorCode](../android/net/http/NetworkException.md))returns this code, this exception may be cast to [QuicException](../android/net/http/QuicException.md) for more information if [QUIC](https://www.chromium.org/quic) protocol is used. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_OTHER](../android/net/http/NetworkException.md) <br /> Error code indicating another type of error was encountered. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_QUIC_PROTOCOL_FAILED](../android/net/http/NetworkException.md) <br /> Error code indicating an error related to the [QUIC](https://www.chromium.org/quic) protocol. When [getErrorCode](../android/net/http/NetworkException.md))returns this code, this exception can be cast to [QuicException](../android/net/http/QuicException.md) for more information. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TIMED_OUT](../android/net/http/NetworkException.md) <br /> Error code indicating a timeout expired. Timeouts expiring while attempting to connect will be reported as the more specific [ERROR_CONNECTION_TIMED_OUT](../android/net/http/NetworkException.md). <br /> | ||

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [QuicException](../android/net/http/QuicException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Constructs an exception that is caused by a QUIC protocol error. |

| Inherited functions ||
|---|---|
| From class [NetworkException](../android/net/http/NetworkException.md) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorCode](../android/net/http/NetworkException.md))`()` <br /> Returns error code, one of [ERROR_*](../android/net/http/NetworkException.md). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isImmediatelyRetryable](../android/net/http/NetworkException.md))`()` <br /> Returns`true`if retrying this request right away might succeed,`false`otherwise. For example returns`true`when [getErrorCode](../android/net/http/NetworkException.md))returns [ERROR_NETWORK_CHANGED](../android/net/http/NetworkException.md) because trying the request might succeed using the new network configuration, but`false`when`getErrorCode()`returns [ERROR_INTERNET_DISCONNECTED](../android/net/http/NetworkException.md) because retrying the request right away will encounter the same failure (instead retrying should be delayed until device regains network connectivity). <br /> | ||

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
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:the cause (which is saved for later retrieval by the [getCause()](../java/lang/Throwable.md))method). A null value is permitted, and indicates that the cause is nonexistent or unknown. |
