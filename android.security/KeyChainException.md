# KeyChainException

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyChainException

Kotlin | [Java](../android/security/KeyChainException.md) 
| --- | --- |

```
open class KeyChainException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||
| | | ↳ | [android.security.KeyChainException](../android/security/KeyChainException.md) |
| --- | --- | --- | --- |

Thrown on problems accessing the [KeyChain](../android/security/KeyChain.md).

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [KeyChainException](../android/security/KeyChainException.md))`()` Constructs a new `KeyChainException` that includes the current stack trace. |
| [KeyChainException](../android/security/KeyChainException.md))`(`detailMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new `KeyChainException` with the current stack trace and the specified detail message. |
| [KeyChainException](../android/security/KeyChainException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new `KeyChainException` with the current stack trace, the specified detail message and the specified cause. |
| [KeyChainException](../android/security/KeyChainException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new `KeyChainException` with the current stack trace and the specified cause. |

## Public constructors

### KeyChainException

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyChainException()
```

Constructs a new `KeyChainException` that includes the current stack trace. 

### KeyChainException

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyChainException(detailMessage: String!)
```

Constructs a new `KeyChainException` with the current stack trace and the specified detail message.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------|
| `detailMessage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message for this exception. |

### KeyChainException

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyChainException(
    message: String!, 
    cause: Throwable!)
```

Constructs a new `KeyChainException` with the current stack trace, the specified detail message and the specified cause.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message for this exception. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause of this exception, may be `null`. |

### KeyChainException

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyChainException(cause: Throwable!)
```

Constructs a new `KeyChainException` with the current stack trace and the specified cause.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause of this exception, may be `null`. |
