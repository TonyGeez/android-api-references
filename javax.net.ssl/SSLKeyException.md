# SSLKeyException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLKeyException

```
open class SSLKeyException : SSLException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [javax.net.ssl.SSLException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLException) ||
| | | | | ↳ | [javax.net.ssl.SSLKeyException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLKeyException#) |

Reports a bad SSL key. Normally, this indicates misconfiguration of the server or client SSL certificate and private key.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SSLKeyException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLKeyException#SSLKeyException(kotlin.String))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an exception reporting a key management error found by an SSL subsystem. |

## Public constructors

### SSLKeyException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SSLKeyException(reason: String!)
```

Constructs an exception reporting a key management error found by an SSL subsystem.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:describes the problem. |
