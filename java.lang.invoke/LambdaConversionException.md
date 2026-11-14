# LambdaConversionException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LambdaConversionException

```
open class LambdaConversionException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [java.lang.invoke.LambdaConversionException](https://developer.android.com/reference/kotlin/java/lang/invoke/LambdaConversionException#) |
| --- | --- | --- | --- |

LambdaConversionException

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LambdaConversionException](https://developer.android.com/reference/kotlin/java/lang/invoke/LambdaConversionException#LambdaConversionException())`()` Constructs a`LambdaConversionException`. |
| [LambdaConversionException](https://developer.android.com/reference/kotlin/java/lang/invoke/LambdaConversionException#LambdaConversionException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`LambdaConversionException`with a message. |
| [LambdaConversionException](https://developer.android.com/reference/kotlin/java/lang/invoke/LambdaConversionException#LambdaConversionException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`LambdaConversionException`with a message and cause. |
| [LambdaConversionException](https://developer.android.com/reference/kotlin/java/lang/invoke/LambdaConversionException#LambdaConversionException(kotlin.String,%20kotlin.Throwable,%20kotlin.Boolean,%20kotlin.Boolean))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`, `enableSuppression:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `writableStackTrace:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Constructs a`LambdaConversionException`with a message, cause, and other settings. |
| [LambdaConversionException](https://developer.android.com/reference/kotlin/java/lang/invoke/LambdaConversionException#LambdaConversionException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`LambdaConversionException`with a cause. |

## Public constructors

### LambdaConversionException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LambdaConversionException()
```

Constructs a`LambdaConversionException`. 

### LambdaConversionException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LambdaConversionException(message: String!)
```

Constructs a`LambdaConversionException`with a message.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |

### LambdaConversionException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LambdaConversionException(
    message: String!, 
    cause: Throwable!)
```

Constructs a`LambdaConversionException`with a message and cause.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause |

### LambdaConversionException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LambdaConversionException(
    message: String!, 
    cause: Throwable!, 
    enableSuppression: Boolean, 
    writableStackTrace: Boolean)
```

Constructs a`LambdaConversionException`with a message, cause, and other settings.

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause |
| `enableSuppression` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether or not suppressed exceptions are enabled |
| --- | --- |
| `writableStackTrace` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether or not the stack trace is writable |

### LambdaConversionException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LambdaConversionException(cause: Throwable!)
```

Constructs a`LambdaConversionException`with a cause.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause |
