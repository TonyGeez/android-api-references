# InterruptedIOException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InterruptedIOException

```
open class InterruptedIOException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.io.IOException](IOException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.io.InterruptedIOException](InterruptedIOException.md) |

| Known Direct Subclasses [ConnectTimeoutException](../org.apache.http.conn/ConnectTimeoutException.md), [SocketTimeoutException](../java.net/SocketTimeoutException.md) |------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------| | [ConnectTimeoutException](../org.apache.http.conn/ConnectTimeoutException.md) | A timeout while connecting to an HTTP server or waiting for an available connection from an HttpConnectionManager. | | [SocketTimeoutException](../java.net/SocketTimeoutException.md) | Signals that a timeout has occurred on a socket read or accept. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Signals that an I/O operation has been interrupted. An`InterruptedIOException`is thrown to indicate that an input or output transfer has been terminated because the thread performing it was interrupted. The field [bytesTransferred](InterruptedIOException.md) indicates how many bytes were successfully transferred before the interruption occurred.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InterruptedIOException](InterruptedIOException.md))`()` Constructs an`InterruptedIOException`with`null`as its error detail message. |
| [InterruptedIOException](InterruptedIOException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`InterruptedIOException`with the specified detail message. |

| Properties ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bytesTransferred](InterruptedIOException.md) Reports how many bytes had been transferred as part of the I/O operation before it was interrupted. |

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

Constructs an`InterruptedIOException`with the specified detail message. The string`s`can be retrieved later by the [java.lang.Throwable#getMessage](../java.lang/Throwable.md))method of class`java.lang.Throwable`.

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
