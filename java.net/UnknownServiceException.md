# UnknownServiceException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnknownServiceException

```
open class UnknownServiceException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.io.IOException](../java.io/IOException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.net.UnknownServiceException](UnknownServiceException.md) |

Thrown to indicate that an unknown service exception has occurred. Either the MIME type returned by a URL connection does not make sense, or the application is attempting to write to a read-only URL connection.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnknownServiceException](UnknownServiceException.md))`()` Constructs a new`UnknownServiceException`with no detail message. |
| [UnknownServiceException](UnknownServiceException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new`UnknownServiceException`with the specified detail message. |

## Public constructors

### UnknownServiceException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnknownServiceException()
```

Constructs a new`UnknownServiceException`with no detail message. 

### UnknownServiceException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnknownServiceException(msg: String!)
```

Constructs a new`UnknownServiceException`with the specified detail message.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
