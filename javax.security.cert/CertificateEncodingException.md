# CertificateEncodingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertificateEncodingException

```
open class CertificateEncodingException : CertificateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [javax.security.cert.CertificateException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateException) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [javax.security.cert.CertificateEncodingException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateEncodingException#) |

Certificate Encoding Exception. This is thrown whenever an error occurs whilst attempting to encode a certificate.

*Note: The classes in the package`javax.security.cert`exist for compatibility with earlier versions of the Java Secure Sockets Extension (JSSE). New applications should instead use the standard Java SE certificate classes located in`java.security.cert`.*

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertificateEncodingException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateEncodingException#CertificateEncodingException())`()` Constructs a CertificateEncodingException with no detail message. |
| [CertificateEncodingException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateEncodingException#CertificateEncodingException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a CertificateEncodingException with the specified detail message. |

## Public constructors

### CertificateEncodingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertificateEncodingException()
```

Constructs a CertificateEncodingException with no detail message. A detail message is a String that describes this particular exception. 

### CertificateEncodingException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertificateEncodingException(message: String!)
```

Constructs a CertificateEncodingException with the specified detail message. A detail message is a String that describes this particular exception.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
