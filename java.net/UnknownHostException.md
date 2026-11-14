# UnknownHostException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnknownHostException

```
open class UnknownHostException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) ||
| | | | ↳ | [java.net.UnknownHostException](https://developer.android.com/reference/kotlin/java/net/UnknownHostException#) |

Thrown to indicate that the IP address of a host could not be determined.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnknownHostException](https://developer.android.com/reference/kotlin/java/net/UnknownHostException#UnknownHostException())`()` Constructs a new`UnknownHostException`with no detail message. |
| [UnknownHostException](https://developer.android.com/reference/kotlin/java/net/UnknownHostException#UnknownHostException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new`UnknownHostException`with the specified detail message. |

## Public constructors

### UnknownHostException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnknownHostException()
```

Constructs a new`UnknownHostException`with no detail message. 

### UnknownHostException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnknownHostException(message: String!)
```

Constructs a new`UnknownHostException`with the specified detail message.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
