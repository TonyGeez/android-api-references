# CertificateNotYetValidException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertificateNotYetValidException

```
open class CertificateNotYetValidException : CertificateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [javax.security.cert.CertificateException](../javax/security/cert/CertificateException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [javax.security.cert.CertificateNotYetValidException](../javax/security/cert/CertificateNotYetValidException.md) |

Certificate is not yet valid exception. This is thrown whenever the current`Date`or the specified`Date`is before the`notBefore`date/time in the Certificate validity period.

*Note: The classes in the package`javax.security.cert`exist for compatibility with earlier versions of the Java Secure Sockets Extension (JSSE). New applications should instead use the standard Java SE certificate classes located in`java.security.cert`.*

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertificateNotYetValidException](../javax/security/cert/CertificateNotYetValidException.md))`()` Constructs a CertificateNotYetValidException with no detail message. |
| [CertificateNotYetValidException](../javax/security/cert/CertificateNotYetValidException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a CertificateNotYetValidException with the specified detail message. |

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
