# CertificateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertificateException

```
open class CertificateException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [javax.security.cert.CertificateException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateException#) |

| Known Direct Subclasses [CertificateEncodingException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateEncodingException), [CertificateExpiredException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateExpiredException), [CertificateNotYetValidException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateNotYetValidException), [CertificateParsingException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateParsingException) |---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------| | [CertificateEncodingException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateEncodingException) | Certificate Encoding Exception. | | [CertificateExpiredException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateExpiredException) | Certificate Expired Exception. | | [CertificateNotYetValidException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateNotYetValidException) | Certificate is not yet valid exception. | | [CertificateParsingException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateParsingException) | Certificate Parsing Exception. | |

This exception indicates one of a variety of certificate problems.

*Note: The classes in the package`javax.security.cert`exist for compatibility with earlier versions of the Java Secure Sockets Extension (JSSE). New applications should instead use the standard Java SE certificate classes located in`java.security.cert`.*

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertificateException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateException#CertificateException())`()` Constructs a certificate exception with no detail message. |
| [CertificateException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateException#CertificateException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a certificate exception with the given detail message. |

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
