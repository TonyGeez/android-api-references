# InternalError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InternalError

```
open class InternalError : VirtualMachineError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error) |||
| | | ↳ | [java.lang.VirtualMachineError](https://developer.android.com/reference/kotlin/java/lang/VirtualMachineError) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.InternalError](https://developer.android.com/reference/kotlin/java/lang/InternalError#) |

| Known Direct Subclasses [ZipError](https://developer.android.com/reference/kotlin/java/util/zip/ZipError.html#) |-----------------------------------------------------------------------------------------|---------------------------------------------------| | [ZipError](https://developer.android.com/reference/kotlin/java/util/zip/ZipError.html#) | Signals that an unrecoverable error has occurred. | |
| --- | --- | --- | --- | --- | --- | --- |

Thrown to indicate some unexpected internal error has occurred in the Java Virtual Machine.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InternalError](https://developer.android.com/reference/kotlin/java/lang/InternalError#InternalError())`()` Constructs an`InternalError`with no detail message. |
| [InternalError](https://developer.android.com/reference/kotlin/java/lang/InternalError#InternalError(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`InternalError`with the specified detail message. |
| [InternalError](https://developer.android.com/reference/kotlin/java/lang/InternalError#InternalError(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs an`InternalError`with the specified detail message and cause. |
| [InternalError](https://developer.android.com/reference/kotlin/java/lang/InternalError#InternalError(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs an`InternalError`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). |

## Public constructors

### InternalError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InternalError()
```

Constructs an`InternalError`with no detail message. 

### InternalError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InternalError(message: String!)
```

Constructs an`InternalError`with the specified detail message.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |

### InternalError

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InternalError(
    message: String!, 
    cause: Throwable!)
```

Constructs an`InternalError`with the specified detail message and cause.

Note that the detail message associated with`cause`is*not*automatically incorporated in this error's detail message.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getMessage())method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### InternalError

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InternalError(cause: Throwable!)
```

Constructs an`InternalError`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
