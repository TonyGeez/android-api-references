# InvalidPreferencesFormatException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InvalidPreferencesFormatException

```
open class InvalidPreferencesFormatException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||
| | | ↳ | [java.util.prefs.InvalidPreferencesFormatException](../java/util/prefs/InvalidPreferencesFormatException.md) |
| --- | --- | --- | --- |

Thrown to indicate that an operation could not complete because the input did not conform to the appropriate XML document type for a collection of preferences, as per the [Preferences](../java/util/prefs/Preferences.md) specification.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InvalidPreferencesFormatException](../java/util/prefs/InvalidPreferencesFormatException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an InvalidPreferencesFormatException with the specified detail message. |
| [InvalidPreferencesFormatException](../java/util/prefs/InvalidPreferencesFormatException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs an InvalidPreferencesFormatException with the specified detail message and cause. |
| [InvalidPreferencesFormatException](../java/util/prefs/InvalidPreferencesFormatException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs an InvalidPreferencesFormatException with the specified cause. |

## Public constructors

### InvalidPreferencesFormatException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidPreferencesFormatException(message: String!)
```

Constructs an InvalidPreferencesFormatException with the specified detail message.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. The detail message is saved for later retrieval by the [Throwable.getMessage()](../java/lang/Throwable.md))method. |

### InvalidPreferencesFormatException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidPreferencesFormatException(
    message: String!, 
    cause: Throwable!)
```

Constructs an InvalidPreferencesFormatException with the specified detail message and cause.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. The detail message is saved for later retrieval by the [Throwable.getMessage()](../java/lang/Throwable.md))method. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [Throwable.getCause()](../java/lang/Throwable.md))method). |

### InvalidPreferencesFormatException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidPreferencesFormatException(cause: Throwable!)
```

Constructs an InvalidPreferencesFormatException with the specified cause.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [Throwable.getCause()](../java/lang/Throwable.md))method). |
