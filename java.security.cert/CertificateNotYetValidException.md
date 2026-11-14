# CertificateNotYetValidException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertificateNotYetValidException

```
open class CertificateNotYetValidException : CertificateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.security.GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException.html#) |||
| | | | ↳ | [java.security.cert.CertificateException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateException) ||
| | | | | ↳ | [java.security.cert.CertificateNotYetValidException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateNotYetValidException#) |

Certificate is not yet valid exception. This is thrown whenever the current`Date`or the specified`Date`is before the`notBefore`date/time in the Certificate validity period.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertificateNotYetValidException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateNotYetValidException#CertificateNotYetValidException())`()` Constructs a CertificateNotYetValidException with no detail message. |
| [CertificateNotYetValidException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateNotYetValidException#CertificateNotYetValidException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a CertificateNotYetValidException with the specified detail message. |

## Public constructors

### CertificateNotYetValidException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertificateNotYetValidException()
```

Constructs a CertificateNotYetValidException with no detail message. A detail message is a String that describes this particular exception. 

### CertificateNotYetValidException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertificateNotYetValidException(message: String!)
```

Constructs a CertificateNotYetValidException with the specified detail message. A detail message is a String that describes this particular exception.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
