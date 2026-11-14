# HttpRetryException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HttpRetryException

```
open class HttpRetryException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.net.HttpRetryException](https://developer.android.com/reference/kotlin/java/net/HttpRetryException#) |

Thrown to indicate that a HTTP request needs to be retried but cannot be retried automatically, due to streaming mode being enabled.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [HttpRetryException](https://developer.android.com/reference/kotlin/java/net/HttpRetryException#HttpRetryException(kotlin.String,%20kotlin.Int))`(`detail:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a new `HttpRetryException` from the specified response code and exception detail message |
| [HttpRetryException](https://developer.android.com/reference/kotlin/java/net/HttpRetryException#HttpRetryException(kotlin.String,%20kotlin.Int,%20kotlin.String))`(`detail:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `location:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new `HttpRetryException` with detail message responseCode and the contents of the Location response header field. |

| Public methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLocation](https://developer.android.com/reference/kotlin/java/net/HttpRetryException#getLocation())`()` Returns the value of the Location header field if the error resulted from redirection. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getReason](https://developer.android.com/reference/kotlin/java/net/HttpRetryException#getReason())`()` Returns a string explaining why the http request could not be retried. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [responseCode](https://developer.android.com/reference/kotlin/java/net/HttpRetryException#responseCode())`()` Returns the http response code |
| --- | --- |

## Public constructors

### HttpRetryException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HttpRetryException(
    detail: String!, 
    code: Int)
```

Constructs a new `HttpRetryException` from the specified response code and exception detail message

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------|
| `detail` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message. |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the HTTP response code from server. |

### HttpRetryException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HttpRetryException(
    detail: String!, 
    code: Int, 
    location: String!)
```

Constructs a new `HttpRetryException` with detail message responseCode and the contents of the Location response header field.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------|
| `detail` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message. |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the HTTP response code from server. |
| `location` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the URL to be redirected to |
| --- | --- |

## Public methods

### getLocation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocation(): String!
```

Returns the value of the Location header field if the error resulted from redirection.

| Return ||
|-----------------------------------------------------------------------------------|---------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The location string |

### getReason

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReason(): String!
```

Returns a string explaining why the http request could not be retried.

| Return ||
|-----------------------------------------------------------------------------------|-------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The reason string |

### responseCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun responseCode(): Int
```

Returns the http response code

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The http response code. |
