# CertificateExpiredException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertificateExpiredException

```
open class CertificateExpiredException : CertificateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [javax.security.cert.CertificateException](CertificateException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [javax.security.cert.CertificateExpiredException](CertificateExpiredException.md) |

Certificate Expired Exception. This is thrown whenever the current`Date`or the specified`Date`is after the`notAfter`date/time specified in the validity period of the certificate.

*Note: The classes in the package`javax.security.cert`exist for compatibility with earlier versions of the Java Secure Sockets Extension (JSSE). New applications should instead use the standard Java SE certificate classes located in`java.security.cert`.*

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertificateExpiredException](CertificateExpiredException.md))`()` Constructs a CertificateExpiredException with no detail message. |
| [CertificateExpiredException](CertificateExpiredException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a CertificateExpiredException with the specified detail message. |

## Public constructors

### CertificateExpiredException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertificateExpiredException()
```

Constructs a CertificateExpiredException with no detail message. A detail message is a String that describes this particular exception. 

### CertificateExpiredException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertificateExpiredException(message: String!)
```

Constructs a CertificateExpiredException with the specified detail message. A detail message is a String that describes this particular exception.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
