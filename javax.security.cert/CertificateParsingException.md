# CertificateParsingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertificateParsingException

```
open class CertificateParsingException : CertificateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [javax.security.cert.CertificateException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateException) ||
| | | | ↳ | [javax.security.cert.CertificateParsingException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateParsingException#) |

Certificate Parsing Exception. This is thrown whenever invalid DER encoded certificate is parsed or unsupported DER features are found in the Certificate.

*Note: The classes in the package`javax.security.cert`exist for compatibility with earlier versions of the Java Secure Sockets Extension (JSSE). New applications should instead use the standard Java SE certificate classes located in`java.security.cert`.*

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertificateParsingException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateParsingException#CertificateParsingException())`()` Constructs a CertificateParsingException with no detail message. |
| [CertificateParsingException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateParsingException#CertificateParsingException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a CertificateParsingException with the specified detail message. |

## Public constructors

### CertificateParsingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertificateParsingException()
```

Constructs a CertificateParsingException with no detail message. A detail message is a String that describes this particular exception. 

### CertificateParsingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertificateParsingException(message: String!)
```

Constructs a CertificateParsingException with the specified detail message. A detail message is a String that describes this particular exception.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
