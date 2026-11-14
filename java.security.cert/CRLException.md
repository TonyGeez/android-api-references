# CRLException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CRLException

```
open class CRLException : GeneralSecurityException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.security.GeneralSecurityException](../java.security/GeneralSecurityException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.security.cert.CRLException](CRLException.md) |

CRL (Certificate Revocation List) Exception.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CRLException](CRLException.md))`()` Constructs a CRLException with no detail message. |
| [CRLException](CRLException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a CRLException with the specified detail message. |
| [CRLException](CRLException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`CRLException`with the specified detail message and cause. |
| [CRLException](CRLException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`CRLException`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). |

## Public constructors

### CRLException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CRLException()
```

Constructs a CRLException with no detail message. A detail message is a String that describes this particular exception. 

### CRLException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CRLException(message: String!)
```

Constructs a CRLException with the specified detail message. A detail message is a String that describes this particular exception.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |

### CRLException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CRLException(
    message: String!, 
    cause: Throwable!)
```

Creates a`CRLException`with the specified detail message and cause.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [getMessage()](../java.lang/Throwable.md))method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](../java.lang/Throwable.md))method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### CRLException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CRLException(cause: Throwable!)
```

Creates a`CRLException`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`).

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](../java.lang/Throwable.md))method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
