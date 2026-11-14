# BootstrapMethodError

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BootstrapMethodError

```
open class BootstrapMethodError : LinkageError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Error](../java/lang/Error.md) |||
| | | ↳ | [java.lang.LinkageError](../java/lang/LinkageError.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.BootstrapMethodError](../java/lang/BootstrapMethodError.md) |

Thrown to indicate that an`invokedynamic`instruction or a dynamic constant failed to resolve its bootstrap method and arguments, or for`invokedynamic`instruction the bootstrap method has failed to provide a [call site](../java/lang/invoke/CallSite.md) with a [target](../java/lang/invoke/CallSite.md))of the correct [method type](../java/lang/invoke/MethodHandle.md)), or for a dynamic constant the bootstrap method has failed to provide a constant value of the required type.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BootstrapMethodError](../java/lang/BootstrapMethodError.md))`()` Constructs a`BootstrapMethodError`with no detail message. |
| [BootstrapMethodError](../java/lang/BootstrapMethodError.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`BootstrapMethodError`with the specified detail message. |
| [BootstrapMethodError](../java/lang/BootstrapMethodError.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`BootstrapMethodError`with the specified detail message and cause. |
| [BootstrapMethodError](../java/lang/BootstrapMethodError.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`BootstrapMethodError`with the specified cause. |

## Public constructors

### BootstrapMethodError

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BootstrapMethodError()
```

Constructs a`BootstrapMethodError`with no detail message. 

### BootstrapMethodError

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BootstrapMethodError(s: String!)
```

Constructs a`BootstrapMethodError`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |

### BootstrapMethodError

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BootstrapMethodError(
    s: String!, 
    cause: Throwable!)
```

Constructs a`BootstrapMethodError`with the specified detail message and cause.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause, may be`null`. |

### BootstrapMethodError

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BootstrapMethodError(cause: Throwable!)
```

Constructs a`BootstrapMethodError`with the specified cause.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause, may be`null`. |
