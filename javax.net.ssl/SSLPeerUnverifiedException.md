# SSLPeerUnverifiedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLPeerUnverifiedException

```
open class SSLPeerUnverifiedException : SSLException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) |||
| | | | ↳ | [javax.net.ssl.SSLException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLException) ||
| | | | | ↳ | [javax.net.ssl.SSLPeerUnverifiedException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLPeerUnverifiedException#) |

Indicates that the peer's identity has not been verified.

When the peer was not able to identify itself (for example; no certificate, the particular cipher suite being used does not support authentication, or no peer authentication was established during SSL handshaking) this exception is thrown.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SSLPeerUnverifiedException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLPeerUnverifiedException#SSLPeerUnverifiedException(kotlin.String))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an exception reporting that the SSL peer's identity has not been verified. |

## Public constructors

### SSLPeerUnverifiedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SSLPeerUnverifiedException(reason: String!)
```

Constructs an exception reporting that the SSL peer's identity has not been verified.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:describes the problem. |
