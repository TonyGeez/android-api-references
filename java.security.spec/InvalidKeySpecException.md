# InvalidKeySpecException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InvalidKeySpecException

```
open class InvalidKeySpecException : GeneralSecurityException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.security.GeneralSecurityException](../java.security/GeneralSecurityException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.security.spec.InvalidKeySpecException](InvalidKeySpecException.md) |

This is the exception for invalid key specifications.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InvalidKeySpecException](InvalidKeySpecException.md))`()` Constructs an InvalidKeySpecException with no detail message. |
| [InvalidKeySpecException](InvalidKeySpecException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an InvalidKeySpecException with the specified detail message. |
| [InvalidKeySpecException](InvalidKeySpecException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates an`InvalidKeySpecException`with the specified detail message and cause. |
| [InvalidKeySpecException](InvalidKeySpecException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates an`InvalidKeySpecException`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). |

## Public constructors

### InvalidKeySpecException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidKeySpecException()
```

Constructs an InvalidKeySpecException with no detail message. A detail message is a String that describes this particular exception. 

### InvalidKeySpecException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidKeySpecException(msg: String!)
```

Constructs an InvalidKeySpecException with the specified detail message. A detail message is a String that describes this particular exception.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |

### InvalidKeySpecException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidKeySpecException(
    message: String!, 
    cause: Throwable!)
```

Creates an`InvalidKeySpecException`with the specified detail message and cause.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [getMessage()](../java.lang/Throwable.md))method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](../java.lang/Throwable.md))method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### InvalidKeySpecException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidKeySpecException(cause: Throwable!)
```

Creates an`InvalidKeySpecException`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`).

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](../java.lang/Throwable.md))method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
