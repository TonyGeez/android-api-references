# VirtualMachineError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VirtualMachineError

```
abstract class VirtualMachineError : Error
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error) ||
| | | ↳ | [java.lang.VirtualMachineError](https://developer.android.com/reference/kotlin/java/lang/VirtualMachineError#) |
| --- | --- | --- | --- |

| Known Direct Subclasses [InternalError](https://developer.android.com/reference/kotlin/java/lang/InternalError), [OutOfMemoryError](https://developer.android.com/reference/kotlin/java/lang/OutOfMemoryError), [StackOverflowError](https://developer.android.com/reference/kotlin/java/lang/StackOverflowError), [UnknownError](https://developer.android.com/reference/kotlin/java/lang/UnknownError) |---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InternalError](https://developer.android.com/reference/kotlin/java/lang/InternalError) | Thrown to indicate some unexpected internal error has occurred in the Java Virtual Machine. | | [OutOfMemoryError](https://developer.android.com/reference/kotlin/java/lang/OutOfMemoryError) | Thrown when the Java Virtual Machine cannot allocate an object because it is out of memory, and no more memory could be made available by the garbage collector. | | [StackOverflowError](https://developer.android.com/reference/kotlin/java/lang/StackOverflowError) | Thrown when a stack overflow occurs because an application recurses too deeply. | | [UnknownError](https://developer.android.com/reference/kotlin/java/lang/UnknownError) | Thrown when an unknown but serious exception has occurred in the Java Virtual Machine. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ZipError](https://developer.android.com/reference/kotlin/java/util/zip/ZipError.html#) |-----------------------------------------------------------------------------------------|---------------------------------------------------| | [ZipError](https://developer.android.com/reference/kotlin/java/util/zip/ZipError.html#) | Signals that an unrecoverable error has occurred. | |
| --- | --- | --- | --- | --- | --- | --- |

Thrown to indicate that the Java Virtual Machine is broken or has run out of resources necessary for it to continue operating.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [VirtualMachineError](https://developer.android.com/reference/kotlin/java/lang/VirtualMachineError#VirtualMachineError())`()` Constructs a`VirtualMachineError`with no detail message. |
| [VirtualMachineError](https://developer.android.com/reference/kotlin/java/lang/VirtualMachineError#VirtualMachineError(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`VirtualMachineError`with the specified detail message. |
| [VirtualMachineError](https://developer.android.com/reference/kotlin/java/lang/VirtualMachineError#VirtualMachineError(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`VirtualMachineError`with the specified detail message and cause. |
| [VirtualMachineError](https://developer.android.com/reference/kotlin/java/lang/VirtualMachineError#VirtualMachineError(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs an a`VirtualMachineError`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). |

## Public constructors

### VirtualMachineError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
VirtualMachineError()
```

Constructs a`VirtualMachineError`with no detail message. 

### VirtualMachineError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
VirtualMachineError(message: String!)
```

Constructs a`VirtualMachineError`with the specified detail message.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |

### VirtualMachineError

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
VirtualMachineError(
    message: String!, 
    cause: Throwable!)
```

Constructs a`VirtualMachineError`with the specified detail message and cause.

Note that the detail message associated with`cause`is*not*automatically incorporated in this error's detail message.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getMessage())method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### VirtualMachineError

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
VirtualMachineError(cause: Throwable!)
```

Constructs an a`VirtualMachineError`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
