# NotActiveException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NotActiveException

```
open class NotActiveException : ObjectStreamException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException) |||
| | | | ↳ | [java.io.ObjectStreamException](https://developer.android.com/reference/kotlin/java/io/ObjectStreamException) ||
| | | | | ↳ | [java.io.NotActiveException](https://developer.android.com/reference/kotlin/java/io/NotActiveException#) |

Thrown when serialization or deserialization is not active.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NotActiveException](https://developer.android.com/reference/kotlin/java/io/NotActiveException#NotActiveException())`()` Constructor to create a new NotActiveException without a reason. |
| [NotActiveException](https://developer.android.com/reference/kotlin/java/io/NotActiveException#NotActiveException(kotlin.String))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructor to create a new NotActiveException with the reason given. |

## Public constructors

### NotActiveException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NotActiveException()
```

Constructor to create a new NotActiveException without a reason. 

### NotActiveException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NotActiveException(reason: String!)
```

Constructor to create a new NotActiveException with the reason given.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a String describing the reason for the exception. |
