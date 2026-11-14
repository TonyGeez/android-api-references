# CertificateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertificateException

```
open class CertificateException : GeneralSecurityException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.security.GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.security.cert.CertificateException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateException#) |

| Known Direct Subclasses [CertificateEncodingException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateEncodingException), [CertificateExpiredException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateExpiredException), [CertificateNotYetValidException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateNotYetValidException), [CertificateParsingException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateParsingException), [CertificateRevokedException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateRevokedException) |--------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------| | [CertificateEncodingException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateEncodingException) | Certificate Encoding Exception. | | [CertificateExpiredException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateExpiredException) | Certificate Expired Exception. | | [CertificateNotYetValidException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateNotYetValidException) | Certificate is not yet valid exception. | | [CertificateParsingException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateParsingException) | Certificate Parsing Exception. | | [CertificateRevokedException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateRevokedException) | An exception that indicates an X. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This exception indicates one of a variety of certificate problems.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertificateException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateException#CertificateException())`()` Constructs a certificate exception with no detail message. |
| [CertificateException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateException#CertificateException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a certificate exception with the given detail message. |
| [CertificateException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateException#CertificateException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`CertificateException`with the specified detail message and cause. |
| [CertificateException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateException#CertificateException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`CertificateException`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). |

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
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getMessage())method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### CertificateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertificateException(cause: Throwable!)
```

Creates a`CertificateException`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`).

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
