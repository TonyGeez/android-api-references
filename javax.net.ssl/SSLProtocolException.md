# SSLProtocolException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLProtocolException

```
open class SSLProtocolException : SSLException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.io.IOException](../java.io/IOException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [javax.net.ssl.SSLException](SSLException.md) ||
| | | | | ↳ | [javax.net.ssl.SSLProtocolException](SSLProtocolException.md) |

Reports an error in the operation of the SSL protocol. Normally this indicates a flaw in one of the protocol implementations.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SSLProtocolException](SSLProtocolException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an exception reporting an SSL protocol error detected by an SSL subsystem. |

## Public constructors

### SSLProtocolException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SSLProtocolException(reason: String!)
```

Constructs an exception reporting an SSL protocol error detected by an SSL subsystem.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: describes the problem. |
