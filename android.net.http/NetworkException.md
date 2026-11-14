# NetworkException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# NetworkException

Kotlin| [Java](../android/net/http/NetworkException.md) 
| --- | --- |

```
abstract class NetworkException : HttpException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.io.IOException](../java/io/IOException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.net.http.HttpException](../android/net/http/HttpException.md) ||
| | | | | ↳ | [android.net.http.NetworkException](../android/net/http/NetworkException.md) |

| Known Direct Subclasses [QuicException](../android/net/http/QuicException.md) |------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [QuicException](../android/net/http/QuicException.md) | Subclass of [NetworkException](../android/net/http/NetworkException.md) which contains a detailed [QUIC](https://www.chromium.org/quic) error code from [QuicErrorCode](https://cs.chromium.org/search/?q=symbol:%5CbQuicErrorCode%5Cb). | |
| --- | --- | --- | --- | --- | --- | --- |

Exception passed to [UrlRequest.Callback.onFailed()](../android/net/http/UrlRequest.Callback.md))when the HTTP stack fails to process a network request. In this case [getErrorCode](../android/net/http/NetworkException.md))can be used to get more information about the specific type of failure.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_ADDRESS_UNREACHABLE](../android/net/http/NetworkException.md) Error code indicating the IP address being contacted is unreachable, meaning there is no route to the specified host or network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CONNECTION_CLOSED](../android/net/http/NetworkException.md) Error code indicating the connection was closed unexpectedly. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CONNECTION_REFUSED](../android/net/http/NetworkException.md) Error code indicating the connection attempt was refused. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CONNECTION_RESET](../android/net/http/NetworkException.md) Error code indicating the connection was unexpectedly reset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CONNECTION_TIMED_OUT](../android/net/http/NetworkException.md) Error code indicating the connection attempt timed out. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_HOSTNAME_NOT_RESOLVED](../android/net/http/NetworkException.md) Error code indicating the host being sent the request could not be resolved to an IP address. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INTERNET_DISCONNECTED](../android/net/http/NetworkException.md) Error code indicating the device was not connected to any network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NETWORK_CHANGED](../android/net/http/NetworkException.md) Error code indicating that as the request was processed the network configuration changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_OTHER](../android/net/http/NetworkException.md) Error code indicating another type of error was encountered. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_QUIC_PROTOCOL_FAILED](../android/net/http/NetworkException.md) Error code indicating an error related to the [QUIC](https://www.chromium.org/quic) protocol. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TIMED_OUT](../android/net/http/NetworkException.md) Error code indicating a timeout expired. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NetworkException](../android/net/http/NetworkException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Constructs an exception that is caused by a network error. |

| Public methods ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorCode](../android/net/http/NetworkException.md))`()` Returns error code, one of [ERROR_*](../android/net/http/NetworkException.md). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isImmediatelyRetryable](../android/net/http/NetworkException.md))`()` Returns`true`if retrying this request right away might succeed,`false`otherwise. |

## Constants

### ERROR_ADDRESS_UNREACHABLE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
static val ERROR_ADDRESS_UNREACHABLE: Int
```

Error code indicating the IP address being contacted is unreachable, meaning there is no route to the specified host or network. 

 Value: 9

### ERROR_CONNECTION_CLOSED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
static val ERROR_CONNECTION_CLOSED: Int
```

Error code indicating the connection was closed unexpectedly. 

 Value: 5

### ERROR_CONNECTION_REFUSED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
static val ERROR_CONNECTION_REFUSED: Int
```

Error code indicating the connection attempt was refused. 

 Value: 7

### ERROR_CONNECTION_RESET

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
static val ERROR_CONNECTION_RESET: Int
```

Error code indicating the connection was unexpectedly reset. 

 Value: 8

### ERROR_CONNECTION_TIMED_OUT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
static val ERROR_CONNECTION_TIMED_OUT: Int
```

Error code indicating the connection attempt timed out. 

 Value: 6

### ERROR_HOSTNAME_NOT_RESOLVED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
static val ERROR_HOSTNAME_NOT_RESOLVED: Int
```

Error code indicating the host being sent the request could not be resolved to an IP address. 

 Value: 1

### ERROR_INTERNET_DISCONNECTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
static val ERROR_INTERNET_DISCONNECTED: Int
```

Error code indicating the device was not connected to any network. 

 Value: 2

### ERROR_NETWORK_CHANGED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
static val ERROR_NETWORK_CHANGED: Int
```

Error code indicating that as the request was processed the network configuration changed. When [getErrorCode](../android/net/http/NetworkException.md))returns this code, this exception may be cast to [QuicException](../android/net/http/QuicException.md) for more information if [QUIC](https://www.chromium.org/quic) protocol is used. 

 Value: 3

### ERROR_OTHER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
static val ERROR_OTHER: Int
```

Error code indicating another type of error was encountered. 

 Value: 11

### ERROR_QUIC_PROTOCOL_FAILED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
static val ERROR_QUIC_PROTOCOL_FAILED: Int
```

Error code indicating an error related to the [QUIC](https://www.chromium.org/quic) protocol. When [getErrorCode](../android/net/http/NetworkException.md))returns this code, this exception can be cast to [QuicException](../android/net/http/QuicException.md) for more information. 

 Value: 10

### ERROR_TIMED_OUT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
static val ERROR_TIMED_OUT: Int
```

Error code indicating a timeout expired. Timeouts expiring while attempting to connect will be reported as the more specific [ERROR_CONNECTION_TIMED_OUT](../android/net/http/NetworkException.md). 

 Value: 4

## Public constructors

### NetworkException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
NetworkException(
    message: String?, 
    cause: Throwable?)
```

Constructs an exception that is caused by a network error.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:explanation of failure. This value may be`null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:the cause (which is saved for later retrieval by the [getCause()](../java/lang/Throwable.md))method). A null value is permitted, and indicates that the cause is nonexistent or unknown. |

## Public methods

### getErrorCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun getErrorCode(): Int
```

Returns error code, one of [ERROR_*](../android/net/http/NetworkException.md).

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | error code, one of [ERROR_*](../android/net/http/NetworkException.md). |

### isImmediatelyRetryable

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun isImmediatelyRetryable(): Boolean
```

Returns`true`if retrying this request right away might succeed,`false`otherwise. For example returns`true`when [getErrorCode](../android/net/http/NetworkException.md))returns [ERROR_NETWORK_CHANGED](../android/net/http/NetworkException.md) because trying the request might succeed using the new network configuration, but`false`when`getErrorCode()`returns [ERROR_INTERNET_DISCONNECTED](../android/net/http/NetworkException.md) because retrying the request right away will encounter the same failure (instead retrying should be delayed until device regains network connectivity).

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if retrying this request right away might succeed,`false`otherwise. |
