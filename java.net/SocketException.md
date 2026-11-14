# SocketException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SocketException

```
open class SocketException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) ||
| | | | ↳ | [java.net.SocketException](https://developer.android.com/reference/kotlin/java/net/SocketException#) |

| Known Direct Subclasses [BindException](https://developer.android.com/reference/kotlin/java/net/BindException), [ConnectException](https://developer.android.com/reference/kotlin/java/net/ConnectException), [NoRouteToHostException](https://developer.android.com/reference/kotlin/java/net/NoRouteToHostException), [PortUnreachableException](https://developer.android.com/reference/kotlin/java/net/PortUnreachableException) |--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------| | [BindException](https://developer.android.com/reference/kotlin/java/net/BindException) | Signals that an error occurred while attempting to bind a socket to a local address and port. | | [ConnectException](https://developer.android.com/reference/kotlin/java/net/ConnectException) | Signals that an error occurred while attempting to connect a socket to a remote address and port. | | [NoRouteToHostException](https://developer.android.com/reference/kotlin/java/net/NoRouteToHostException) | Signals that an error occurred while attempting to connect a socket to a remote address and port. | | [PortUnreachableException](https://developer.android.com/reference/kotlin/java/net/PortUnreachableException) | Signals that an ICMP Port Unreachable message has been received on a connected datagram. | |

Thrown to indicate that there is an error creating or accessing a Socket.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SocketException](https://developer.android.com/reference/kotlin/java/net/SocketException#SocketException())`()` Constructs a new`SocketException`with no detail message. |
| [SocketException](https://developer.android.com/reference/kotlin/java/net/SocketException#SocketException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new`SocketException`with the specified detail message. |

## Public constructors

### SocketException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SocketException()
```

Constructs a new`SocketException`with no detail message. 

### SocketException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SocketException(msg: String!)
```

Constructs a new`SocketException`with the specified detail message.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
