# SSLHandshakeException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLHandshakeException

```
open class SSLHandshakeException : SSLException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [javax.net.ssl.SSLException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLException) ||
| | | | | ↳ | [javax.net.ssl.SSLHandshakeException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLHandshakeException#) |

Indicates that the client and server could not negotiate the desired level of security. The connection is no longer usable.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SSLHandshakeException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLHandshakeException#SSLHandshakeException(kotlin.String))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an exception reporting an error found by an SSL subsystem during handshaking. |

## Public constructors

### SSLHandshakeException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SSLHandshakeException(reason: String!)
```

Constructs an exception reporting an error found by an SSL subsystem during handshaking.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:describes the problem. |
