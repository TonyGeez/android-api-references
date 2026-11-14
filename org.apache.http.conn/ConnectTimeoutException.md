# ConnectTimeoutException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConnectTimeoutException

```
open class ConnectTimeoutException : InterruptedIOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.io.InterruptedIOException](https://developer.android.com/reference/kotlin/java/io/InterruptedIOException.html#) ||
| | | | | ↳ | [org.apache.http.conn.ConnectTimeoutException](https://developer.android.com/reference/kotlin/org/apache/http/conn/ConnectTimeoutException#) |

| **This exception was deprecated in API level 22.**
|
| Please use java.net.URL#openConnection instead. Please visit [this webpage](http://android-developers.blogspot.com/2011/09/androids-http-clients.html) for further details.

A timeout while connecting to an HTTP server or waiting for an available connection from an HttpConnectionManager.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ConnectTimeoutException](https://developer.android.com/reference/kotlin/org/apache/http/conn/ConnectTimeoutException#ConnectTimeoutException())`()` Creates a ConnectTimeoutException with a null detail message. |
| [ConnectTimeoutException](https://developer.android.com/reference/kotlin/org/apache/http/conn/ConnectTimeoutException#ConnectTimeoutException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a ConnectTimeoutException with the specified detail message. |

| Inherited properties ||
|---|---|
| From class [InterruptedIOException](https://developer.android.com/reference/kotlin/java/io/InterruptedIOException.html#) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bytesTransferred](https://developer.android.com/reference/kotlin/java/io/InterruptedIOException.html#bytesTransferred:kotlin.Int) <br /> Reports how many bytes had been transferred as part of the I/O operation before it was interrupted. <br /> | ||

## Public constructors

### ConnectTimeoutException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConnectTimeoutException()
```

Creates a ConnectTimeoutException with a null detail message. 

### ConnectTimeoutException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConnectTimeoutException(message: String!)
```

Creates a ConnectTimeoutException with the specified detail message.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The exception detail message |
