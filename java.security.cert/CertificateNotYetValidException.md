# CertificateNotYetValidException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertificateNotYetValidException

```
open class CertificateNotYetValidException : CertificateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.security.GeneralSecurityException](../java.security/GeneralSecurityException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.security.cert.CertificateException](CertificateException.md) ||
| | | | | ↳ | [java.security.cert.CertificateNotYetValidException](CertificateNotYetValidException.md) |

Certificate is not yet valid exception. This is thrown whenever the current`Date`or the specified`Date`is before the`notBefore`date/time in the Certificate validity period.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertificateNotYetValidException](CertificateNotYetValidException.md))`()` Constructs a CertificateNotYetValidException with no detail message. |
| [CertificateNotYetValidException](CertificateNotYetValidException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a CertificateNotYetValidException with the specified detail message. |

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
