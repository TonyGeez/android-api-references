# SSLHandshakeException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLHandshakeException

```
open class SSLHandshakeException : SSLException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.io.IOException](../java.io/IOException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [javax.net.ssl.SSLException](SSLException.md) ||
| | | | | ↳ | [javax.net.ssl.SSLHandshakeException](SSLHandshakeException.md) |

Indicates that the client and server could not negotiate the desired level of security. The connection is no longer usable.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SSLHandshakeException](SSLHandshakeException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an exception reporting an error found by an SSL subsystem during handshaking. |

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
