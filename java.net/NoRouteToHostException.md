# NoRouteToHostException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NoRouteToHostException

```
open class NoRouteToHostException : SocketException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.io.IOException](../java/io/IOException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.net.SocketException](../java/net/SocketException.md) ||
| | | | | ↳ | [java.net.NoRouteToHostException](../java/net/NoRouteToHostException.md) |

Signals that an error occurred while attempting to connect a socket to a remote address and port. Typically, the remote host cannot be reached because of an intervening firewall, or if an intermediate router is down.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NoRouteToHostException](../java/net/NoRouteToHostException.md))`()` Construct a new NoRouteToHostException with no detailed message. |
| [NoRouteToHostException](../java/net/NoRouteToHostException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new NoRouteToHostException with the specified detail message as to why the remote host cannot be reached. |

## Public constructors

### NoRouteToHostException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NoRouteToHostException()
```

Construct a new NoRouteToHostException with no detailed message. 

### NoRouteToHostException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NoRouteToHostException(msg: String!)
```

Constructs a new NoRouteToHostException with the specified detail message as to why the remote host cannot be reached. A detail message is a String that gives a specific description of this error.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |
