# SocketException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SocketException

```
open class SocketException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.io.IOException](../java.io/IOException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.net.SocketException](SocketException.md) |

| Known Direct Subclasses [BindException](BindException.md), [ConnectException](ConnectException.md), [NoRouteToHostException](NoRouteToHostException.md), [PortUnreachableException](PortUnreachableException.md) |--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------| | [BindException](BindException.md) | Signals that an error occurred while attempting to bind a socket to a local address and port. | | [ConnectException](ConnectException.md) | Signals that an error occurred while attempting to connect a socket to a remote address and port. | | [NoRouteToHostException](NoRouteToHostException.md) | Signals that an error occurred while attempting to connect a socket to a remote address and port. | | [PortUnreachableException](PortUnreachableException.md) | Signals that an ICMP Port Unreachable message has been received on a connected datagram. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Thrown to indicate that there is an error creating or accessing a Socket.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SocketException](SocketException.md))`()` Constructs a new`SocketException`with no detail message. |
| [SocketException](SocketException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new`SocketException`with the specified detail message. |

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
