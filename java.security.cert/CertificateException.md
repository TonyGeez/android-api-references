# CertificateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertificateException

```
open class CertificateException : GeneralSecurityException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [java.security.GeneralSecurityException](../java/security/GeneralSecurityException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.security.cert.CertificateException](../java/security/cert/CertificateException.md) |

| Known Direct Subclasses [CertificateEncodingException](../java/security/cert/CertificateEncodingException.md), [CertificateExpiredException](../java/security/cert/CertificateExpiredException.md), [CertificateNotYetValidException](../java/security/cert/CertificateNotYetValidException.md), [CertificateParsingException](../java/security/cert/CertificateParsingException.md), [CertificateRevokedException](../java/security/cert/CertificateRevokedException.md) |--------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------| | [CertificateEncodingException](../java/security/cert/CertificateEncodingException.md) | Certificate Encoding Exception. | | [CertificateExpiredException](../java/security/cert/CertificateExpiredException.md) | Certificate Expired Exception. | | [CertificateNotYetValidException](../java/security/cert/CertificateNotYetValidException.md) | Certificate is not yet valid exception. | | [CertificateParsingException](../java/security/cert/CertificateParsingException.md) | Certificate Parsing Exception. | | [CertificateRevokedException](../java/security/cert/CertificateRevokedException.md) | An exception that indicates an X. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This exception indicates one of a variety of certificate problems.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertificateException](../java/security/cert/CertificateException.md))`()` Constructs a certificate exception with no detail message. |
| [CertificateException](../java/security/cert/CertificateException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a certificate exception with the given detail message. |
| [CertificateException](../java/security/cert/CertificateException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`CertificateException`with the specified detail message and cause. |
| [CertificateException](../java/security/cert/CertificateException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`CertificateException`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). |

## Public constructors

### CertificateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertificateException()
```

Constructs a certificate exception with no detail message. A detail message is a String that describes this particular exception. 

### CertificateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertificateException(msg: String!)
```

Constructs a certificate exception with the given detail message. A detail message is a String that describes this particular exception.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |

### CertificateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertificateException(
    message: String!, 
    cause: Throwable!)
```

Creates a`CertificateException`with the specified detail message and cause.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [getMessage()](../java/lang/Throwable.md))method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](../java/lang/Throwable.md))method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### CertificateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertificateException(cause: Throwable!)
```

Creates a`CertificateException`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`).

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](../java/lang/Throwable.md))method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
