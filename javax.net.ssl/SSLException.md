# SSLException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLException

```
open class SSLException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.io.IOException](../java.io/IOException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [javax.net.ssl.SSLException](SSLException.md) |

| Known Direct Subclasses [SSLHandshakeException](SSLHandshakeException.md), [SSLKeyException](SSLKeyException.md), [SSLPeerUnverifiedException](SSLPeerUnverifiedException.md), [SSLProtocolException](SSLProtocolException.md) |-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------| | [SSLHandshakeException](SSLHandshakeException.md) | Indicates that the client and server could not negotiate the desired level of security. | | [SSLKeyException](SSLKeyException.md) | Reports a bad SSL key. | | [SSLPeerUnverifiedException](SSLPeerUnverifiedException.md) | Indicates that the peer's identity has not been verified. | | [SSLProtocolException](SSLProtocolException.md) | Reports an error in the operation of the SSL protocol. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Indicates some kind of error detected by an SSL subsystem. This class is the general class of exceptions produced by failed SSL-related operations.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SSLException](SSLException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an exception reporting an error found by an SSL subsystem. |
| [SSLException](SSLException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`SSLException`with the specified detail message and cause. |
| [SSLException](SSLException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`SSLException`with the specified cause and a detail message of (cause==null ? null : cause.toString()) (which typically contains the class and detail message of cause). |

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
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [getMessage()](../java.lang/Throwable.md))method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](../java.lang/Throwable.md))method). (A null value is permitted, and indicates that the cause is nonexistent or unknown.) |

### SSLException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SSLException(cause: Throwable!)
```

Creates a`SSLException`with the specified cause and a detail message of (cause==null ? null : cause.toString()) (which typically contains the class and detail message of cause).

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](../java.lang/Throwable.md))method). (A null value is permitted, and indicates that the cause is nonexistent or unknown.) |
