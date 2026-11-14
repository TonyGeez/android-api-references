# SSLException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLException

```
open class SSLException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) ||
| | | | ↳ | [javax.net.ssl.SSLException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLException#) |

| Known Direct Subclasses [SSLHandshakeException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLHandshakeException), [SSLKeyException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLKeyException), [SSLPeerUnverifiedException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLPeerUnverifiedException), [SSLProtocolException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLProtocolException) |-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------| | [SSLHandshakeException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLHandshakeException) | Indicates that the client and server could not negotiate the desired level of security. | | [SSLKeyException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLKeyException) | Reports a bad SSL key. | | [SSLPeerUnverifiedException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLPeerUnverifiedException) | Indicates that the peer's identity has not been verified. | | [SSLProtocolException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLProtocolException) | Reports an error in the operation of the SSL protocol. | |

Indicates some kind of error detected by an SSL subsystem. This class is the general class of exceptions produced by failed SSL-related operations.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SSLException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLException#SSLException(kotlin.String))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an exception reporting an error found by an SSL subsystem. |
| [SSLException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLException#SSLException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`SSLException`with the specified detail message and cause. |
| [SSLException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLException#SSLException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`SSLException`with the specified cause and a detail message of (cause==null ? null : cause.toString()) (which typically contains the class and detail message of cause). |

## Public constructors

### SSLException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SSLException(reason: String!)
```

Constructs an exception reporting an error found by an SSL subsystem.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:describes the problem. |

### SSLException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SSLException(
    message: String!, 
    cause: Throwable!)
```

Creates a`SSLException`with the specified detail message and cause.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getMessage())method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method). (A null value is permitted, and indicates that the cause is nonexistent or unknown.) |

### SSLException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SSLException(cause: Throwable!)
```

Creates a`SSLException`with the specified cause and a detail message of (cause==null ? null : cause.toString()) (which typically contains the class and detail message of cause).

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method). (A null value is permitted, and indicates that the cause is nonexistent or unknown.) |
