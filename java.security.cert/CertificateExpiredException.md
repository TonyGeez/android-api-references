# CertificateExpiredException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertificateExpiredException

```
open class CertificateExpiredException : CertificateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.security.GeneralSecurityException](../java/security/GeneralSecurityException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.security.cert.CertificateException](../java/security/cert/CertificateException.md) ||
| | | | | ↳ | [java.security.cert.CertificateExpiredException](../java/security/cert/CertificateExpiredException.md) |

Certificate Expired Exception. This is thrown whenever the current`Date`or the specified`Date`is after the`notAfter`date/time specified in the validity period of the certificate.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertificateExpiredException](../java/security/cert/CertificateExpiredException.md))`()` Constructs a CertificateExpiredException with no detail message. |
| [CertificateExpiredException](../java/security/cert/CertificateExpiredException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a CertificateExpiredException with the specified detail message. |

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
