# ConnectException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConnectException

```
open class ConnectException : SocketException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.io.IOException](../java.io/IOException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.net.SocketException](SocketException.md) ||
| | | | | ↳ | [java.net.ConnectException](ConnectException.md) |

Signals that an error occurred while attempting to connect a socket to a remote address and port. Typically, the connection was refused remotely (e.g., no process is listening on the remote address/port).

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ConnectException](ConnectException.md))`()` Construct a new ConnectException with no detailed message. |
| [ConnectException](ConnectException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new ConnectException with the specified detail message as to why the connect error occurred. |

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
