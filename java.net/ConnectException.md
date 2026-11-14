# ConnectException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConnectException

```
open class ConnectException : SocketException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) |||
| | | | ↳ | [java.net.SocketException](https://developer.android.com/reference/kotlin/java/net/SocketException) ||
| | | | | ↳ | [java.net.ConnectException](https://developer.android.com/reference/kotlin/java/net/ConnectException#) |

Signals that an error occurred while attempting to connect a socket to a remote address and port. Typically, the connection was refused remotely (e.g., no process is listening on the remote address/port).

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ConnectException](https://developer.android.com/reference/kotlin/java/net/ConnectException#ConnectException())`()` Construct a new ConnectException with no detailed message. |
| [ConnectException](https://developer.android.com/reference/kotlin/java/net/ConnectException#ConnectException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new ConnectException with the specified detail message as to why the connect error occurred. |

## Public constructors

### ConnectException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConnectException()
```

Construct a new ConnectException with no detailed message. 

### ConnectException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConnectException(msg: String!)
```

Constructs a new ConnectException with the specified detail message as to why the connect error occurred. A detail message is a String that gives a specific description of this error.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |
