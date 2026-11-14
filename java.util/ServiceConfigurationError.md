# ServiceConfigurationError

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceConfigurationError

```
open class ServiceConfigurationError : Error
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error.html#) ||
| | | ↳ | [java.util.ServiceConfigurationError](https://developer.android.com/reference/kotlin/java/util/ServiceConfigurationError#) |

Error thrown when something goes wrong while locating, loading, or instantiating a service provider.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ServiceConfigurationError](https://developer.android.com/reference/kotlin/java/util/ServiceConfigurationError#ServiceConfigurationError(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new instance with the specified message. |
| [ServiceConfigurationError](https://developer.android.com/reference/kotlin/java/util/ServiceConfigurationError#ServiceConfigurationError(kotlin.String,%20kotlin.Throwable))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new instance with the specified message and cause. |

## Public constructors

### ServiceConfigurationError

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ServiceConfigurationError(msg: String!)
```

Constructs a new instance with the specified message.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The message, or`null`if there is no message |

### ServiceConfigurationError

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ServiceConfigurationError(
    msg: String!, 
    cause: Throwable!)
```

Constructs a new instance with the specified message and cause.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The message, or`null`if there is no message |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:The cause, or`null`if the cause is nonexistent or unknown |
