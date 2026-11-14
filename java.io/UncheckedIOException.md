# UncheckedIOException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UncheckedIOException

```
open class UncheckedIOException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.io.UncheckedIOException](../java/io/UncheckedIOException.md) |

Wraps an [IOException](../java/io/IOException.md) with an unchecked exception.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UncheckedIOException](../java/io/UncheckedIOException.md))`(`cause:` ` [IOException](../java/io/IOException.md)!`)` Constructs an instance of this class. |
| [UncheckedIOException](../java/io/UncheckedIOException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [IOException](../java/io/IOException.md)!`)` Constructs an instance of this class. |

| Properties ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| open [IOException](../java/io/IOException.md)? | [cause](../java/io/UncheckedIOException.md) Returns the cause of this exception. |

## Public constructors

### UncheckedIOException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UncheckedIOException(cause: IOException!)
```

Constructs an instance of this class.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------|
| `cause` | [IOException](../java/io/IOException.md)!:the`IOException` |

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
| `cause` | [IOException](../java/io/IOException.md)!:the`IOException` |

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
| [IOException](../java/io/IOException.md)? | the`IOException`which is the cause of this exception. |
