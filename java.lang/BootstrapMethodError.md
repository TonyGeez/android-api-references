# BootstrapMethodError

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BootstrapMethodError

```
open class BootstrapMethodError : LinkageError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error) |||
| | | ↳ | [java.lang.LinkageError](https://developer.android.com/reference/kotlin/java/lang/LinkageError) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.BootstrapMethodError](https://developer.android.com/reference/kotlin/java/lang/BootstrapMethodError#) |

Thrown to indicate that an`invokedynamic`instruction or a dynamic constant failed to resolve its bootstrap method and arguments, or for`invokedynamic`instruction the bootstrap method has failed to provide a [call site](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite) with a [target](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite#getTarget())of the correct [method type](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle#type()), or for a dynamic constant the bootstrap method has failed to provide a constant value of the required type.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BootstrapMethodError](https://developer.android.com/reference/kotlin/java/lang/BootstrapMethodError#BootstrapMethodError())`()` Constructs a`BootstrapMethodError`with no detail message. |
| [BootstrapMethodError](https://developer.android.com/reference/kotlin/java/lang/BootstrapMethodError#BootstrapMethodError(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`BootstrapMethodError`with the specified detail message. |
| [BootstrapMethodError](https://developer.android.com/reference/kotlin/java/lang/BootstrapMethodError#BootstrapMethodError(kotlin.String,%20kotlin.Throwable))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`BootstrapMethodError`with the specified detail message and cause. |
| [BootstrapMethodError](https://developer.android.com/reference/kotlin/java/lang/BootstrapMethodError#BootstrapMethodError(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`BootstrapMethodError`with the specified cause. |

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
