# VirtualMachineError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VirtualMachineError

```
abstract class VirtualMachineError : Error
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Error](../java/lang/Error.md) ||
| | | ↳ | [java.lang.VirtualMachineError](../java/lang/VirtualMachineError.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [InternalError](../java/lang/InternalError.md), [OutOfMemoryError](../java/lang/OutOfMemoryError.md), [StackOverflowError](../java/lang/StackOverflowError.md), [UnknownError](../java/lang/UnknownError.md) |---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InternalError](../java/lang/InternalError.md) | Thrown to indicate some unexpected internal error has occurred in the Java Virtual Machine. | | [OutOfMemoryError](../java/lang/OutOfMemoryError.md) | Thrown when the Java Virtual Machine cannot allocate an object because it is out of memory, and no more memory could be made available by the garbage collector. | | [StackOverflowError](../java/lang/StackOverflowError.md) | Thrown when a stack overflow occurs because an application recurses too deeply. | | [UnknownError](../java/lang/UnknownError.md) | Thrown when an unknown but serious exception has occurred in the Java Virtual Machine. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ZipError](../java/util/zip/ZipError.md) |-----------------------------------------------------------------------------------------|---------------------------------------------------| | [ZipError](../java/util/zip/ZipError.md) | Signals that an unrecoverable error has occurred. | |
| --- | --- | --- | --- | --- | --- | --- |

Thrown to indicate that the Java Virtual Machine is broken or has run out of resources necessary for it to continue operating.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [VirtualMachineError](../java/lang/VirtualMachineError.md))`()` Constructs a`VirtualMachineError`with no detail message. |
| [VirtualMachineError](../java/lang/VirtualMachineError.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`VirtualMachineError`with the specified detail message. |
| [VirtualMachineError](../java/lang/VirtualMachineError.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`VirtualMachineError`with the specified detail message and cause. |
| [VirtualMachineError](../java/lang/VirtualMachineError.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs an a`VirtualMachineError`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). |

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
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [getMessage()](../java/lang/Throwable.md))method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](../java/lang/Throwable.md))method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### VirtualMachineError

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
VirtualMachineError(cause: Throwable!)
```

Constructs an a`VirtualMachineError`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](../java/lang/Throwable.md))method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
