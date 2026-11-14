# CertificateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertificateException

```
open class CertificateException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||
| | | ↳ | [javax.security.cert.CertificateException](../javax/security/cert/CertificateException.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [CertificateEncodingException](../javax/security/cert/CertificateEncodingException.md), [CertificateExpiredException](../javax/security/cert/CertificateExpiredException.md), [CertificateNotYetValidException](../javax/security/cert/CertificateNotYetValidException.md), [CertificateParsingException](../javax/security/cert/CertificateParsingException.md) |---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------| | [CertificateEncodingException](../javax/security/cert/CertificateEncodingException.md) | Certificate Encoding Exception. | | [CertificateExpiredException](../javax/security/cert/CertificateExpiredException.md) | Certificate Expired Exception. | | [CertificateNotYetValidException](../javax/security/cert/CertificateNotYetValidException.md) | Certificate is not yet valid exception. | | [CertificateParsingException](../javax/security/cert/CertificateParsingException.md) | Certificate Parsing Exception. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This exception indicates one of a variety of certificate problems.

*Note: The classes in the package`javax.security.cert`exist for compatibility with earlier versions of the Java Secure Sockets Extension (JSSE). New applications should instead use the standard Java SE certificate classes located in`java.security.cert`.*

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertificateException](../javax/security/cert/CertificateException.md))`()` Constructs a certificate exception with no detail message. |
| [CertificateException](../javax/security/cert/CertificateException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a certificate exception with the given detail message. |

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
