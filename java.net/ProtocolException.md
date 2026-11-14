# ProtocolException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProtocolException

```
open class ProtocolException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.net.ProtocolException](https://developer.android.com/reference/kotlin/java/net/ProtocolException#) |

Thrown to indicate that there is an error in the underlying protocol, such as a TCP error.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ProtocolException](https://developer.android.com/reference/kotlin/java/net/ProtocolException#ProtocolException())`()` Constructs a new`ProtocolException`with no detail message. |
| [ProtocolException](https://developer.android.com/reference/kotlin/java/net/ProtocolException#ProtocolException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new`ProtocolException`with the specified detail message. |

## Public constructors

### ProtocolException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ProtocolException()
```

Constructs a new`ProtocolException`with no detail message. 

### ProtocolException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ProtocolException(message: String!)
```

Constructs a new`ProtocolException`with the specified detail message.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
