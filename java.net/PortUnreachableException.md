# PortUnreachableException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PortUnreachableException

```
open class PortUnreachableException : SocketException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) |||
| | | | ↳ | [java.net.SocketException](https://developer.android.com/reference/kotlin/java/net/SocketException) ||
| | | | | ↳ | [java.net.PortUnreachableException](https://developer.android.com/reference/kotlin/java/net/PortUnreachableException#) |

Signals that an ICMP Port Unreachable message has been received on a connected datagram.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PortUnreachableException](https://developer.android.com/reference/kotlin/java/net/PortUnreachableException#PortUnreachableException())`()` Construct a new`PortUnreachableException`with no detailed message. |
| [PortUnreachableException](https://developer.android.com/reference/kotlin/java/net/PortUnreachableException#PortUnreachableException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new`PortUnreachableException`with a detail message. |

## Public constructors

### PortUnreachableException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PortUnreachableException()
```

Construct a new`PortUnreachableException`with no detailed message. 

### PortUnreachableException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PortUnreachableException(msg: String!)
```

Constructs a new`PortUnreachableException`with a detail message.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |
