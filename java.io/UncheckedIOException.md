# UncheckedIOException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UncheckedIOException

```
open class UncheckedIOException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| | | | ↳ | [java.io.UncheckedIOException](https://developer.android.com/reference/kotlin/java/io/UncheckedIOException#) |

Wraps an [IOException](https://developer.android.com/reference/kotlin/java/io/IOException) with an unchecked exception.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UncheckedIOException](https://developer.android.com/reference/kotlin/java/io/UncheckedIOException#UncheckedIOException(java.io.IOException))`(`cause:` ` [IOException](https://developer.android.com/reference/kotlin/java/io/IOException)!`)` Constructs an instance of this class. |
| [UncheckedIOException](https://developer.android.com/reference/kotlin/java/io/UncheckedIOException#UncheckedIOException(kotlin.String,%20java.io.IOException))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [IOException](https://developer.android.com/reference/kotlin/java/io/IOException)!`)` Constructs an instance of this class. |

| Properties ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| open [IOException](https://developer.android.com/reference/kotlin/java/io/IOException)? | [cause](https://developer.android.com/reference/kotlin/java/io/UncheckedIOException#cause:java.io.IOException) Returns the cause of this exception. |

## Public constructors

### UncheckedIOException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UncheckedIOException(cause: IOException!)
```

Constructs an instance of this class.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------|
| `cause` | [IOException](https://developer.android.com/reference/kotlin/java/io/IOException)!:the`IOException` |

| Exceptions ||
|----------------------------------|-----------------------|
| `java.lang.NullPointerException` | if the cause is`null` |

### UncheckedIOException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UncheckedIOException(
    message: String!, 
    cause: IOException!)
```

Constructs an instance of this class.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message, can be null |
| `cause` | [IOException](https://developer.android.com/reference/kotlin/java/io/IOException)!:the`IOException` |

| Exceptions ||
|----------------------------------|-----------------------|
| `java.lang.NullPointerException` | if the cause is`null` |

## Properties

### cause

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val cause: IOException?
```

Returns the cause of this exception.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [IOException](https://developer.android.com/reference/kotlin/java/io/IOException)? | the`IOException`which is the cause of this exception. |
