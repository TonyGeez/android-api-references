# InvalidPropertiesFormatException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InvalidPropertiesFormatException

```
open class InvalidPropertiesFormatException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.io.IOException](../java.io/IOException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.util.InvalidPropertiesFormatException](InvalidPropertiesFormatException.md) |

Thrown to indicate that an operation could not complete because the input did not conform to the appropriate XML document type for a collection of properties, as per the [Properties](Properties.md) specification.

Note, that although InvalidPropertiesFormatException inherits Serializable interface from Exception, it is not intended to be Serializable. Appropriate serialization methods are implemented to throw NotSerializableException.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InvalidPropertiesFormatException](InvalidPropertiesFormatException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an InvalidPropertiesFormatException with the specified detail message. |
| [InvalidPropertiesFormatException](InvalidPropertiesFormatException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs an InvalidPropertiesFormatException with the specified cause. |

## Public constructors

### InvalidPropertiesFormatException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidPropertiesFormatException(message: String!)
```

Constructs an InvalidPropertiesFormatException with the specified detail message.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. The detail message is saved for later retrieval by the [Throwable.getMessage()](../java.lang/Throwable.md))method. |

### InvalidPropertiesFormatException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidPropertiesFormatException(cause: Throwable!)
```

Constructs an InvalidPropertiesFormatException with the specified cause.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [Throwable.getCause()](../java.lang/Throwable.md))method). |
