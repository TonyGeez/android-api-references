# InterruptedIOException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InterruptedIOException

```
open class InterruptedIOException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException) ||
| | | | ↳ | [java.io.InterruptedIOException](https://developer.android.com/reference/kotlin/java/io/InterruptedIOException#) |

| Known Direct Subclasses [ConnectTimeoutException](https://developer.android.com/reference/kotlin/org/apache/http/conn/ConnectTimeoutException.html#), [SocketTimeoutException](https://developer.android.com/reference/kotlin/java/net/SocketTimeoutException.html#) |------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------| | [ConnectTimeoutException](https://developer.android.com/reference/kotlin/org/apache/http/conn/ConnectTimeoutException.html#) | A timeout while connecting to an HTTP server or waiting for an available connection from an HttpConnectionManager. | | [SocketTimeoutException](https://developer.android.com/reference/kotlin/java/net/SocketTimeoutException.html#) | Signals that a timeout has occurred on a socket read or accept. | |

Signals that an I/O operation has been interrupted. An`InterruptedIOException`is thrown to indicate that an input or output transfer has been terminated because the thread performing it was interrupted. The field [bytesTransferred](https://developer.android.com/reference/kotlin/java/io/InterruptedIOException#bytesTransferred:kotlin.Int) indicates how many bytes were successfully transferred before the interruption occurred.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InterruptedIOException](https://developer.android.com/reference/kotlin/java/io/InterruptedIOException#InterruptedIOException())`()` Constructs an`InterruptedIOException`with`null`as its error detail message. |
| [InterruptedIOException](https://developer.android.com/reference/kotlin/java/io/InterruptedIOException#InterruptedIOException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`InterruptedIOException`with the specified detail message. |

| Properties ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bytesTransferred](https://developer.android.com/reference/kotlin/java/io/InterruptedIOException#bytesTransferred:kotlin.Int) Reports how many bytes had been transferred as part of the I/O operation before it was interrupted. |

## Public constructors

### InterruptedIOException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InterruptedIOException()
```

Constructs an`InterruptedIOException`with`null`as its error detail message. 

### InterruptedIOException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InterruptedIOException(s: String!)
```

Constructs an`InterruptedIOException`with the specified detail message. The string`s`can be retrieved later by the [java.lang.Throwable#getMessage](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getMessage())method of class`java.lang.Throwable`.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |

## Properties

### bytesTransferred

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var bytesTransferred: Int
```

Reports how many bytes had been transferred as part of the I/O operation before it was interrupted.
