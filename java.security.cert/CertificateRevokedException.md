# CertificateRevokedException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertificateRevokedException

```
open class CertificateRevokedException : CertificateException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.security.GeneralSecurityException](../java/security/GeneralSecurityException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.security.cert.CertificateException](../java/security/cert/CertificateException.md) ||
| | | | | ↳ | [java.security.cert.CertificateRevokedException](../java/security/cert/CertificateRevokedException.md) |

An exception that indicates an X.509 certificate is revoked. A`CertificateRevokedException`contains additional information about the revoked certificate, such as the date on which the certificate was revoked and the reason it was revoked.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertificateRevokedException](../java/security/cert/CertificateRevokedException.md))`(`revocationDate:` ` [Date](../java/util/Date.md)!`, `reason:` ` [CRLReason](../java/security/cert/CRLReason.md)!`, `authority:` ` [X500Principal](../javax/security/auth/x500/X500Principal.md)!`, `extensions:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Extension](../java/security/cert/Extension.md)!>!`)` Constructs a`CertificateRevokedException`with the specified revocation date, reason code, authority name, and map of extensions. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [X500Principal](../javax/security/auth/x500/X500Principal.md)! | [getAuthorityName](../java/security/cert/CertificateRevokedException.md))`()` Returns the name of the authority that signed the certificate's revocation status information. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Extension](../java/security/cert/Extension.md)!\>! | [getExtensions](../java/security/cert/CertificateRevokedException.md))`()` Returns a map of X. |
| open [Date](../java/util/Date.md)! | [getInvalidityDate](../java/security/cert/CertificateRevokedException.md))`()` Returns the invalidity date, as specified in the Invalidity Date extension of this`CertificateRevokedException`. |
| --- | --- |
| open [Date](../java/util/Date.md)! | [getRevocationDate](../java/security/cert/CertificateRevokedException.md))`()` Returns the date on which the certificate was revoked. |
| open [CRLReason](../java/security/cert/CRLReason.md)! | [getRevocationReason](../java/security/cert/CertificateRevokedException.md))`()` Returns the reason the certificate was revoked. |

| Properties ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](../java/security/cert/CertificateRevokedException.md) <br /> |

## Public constructors

### CertificateRevokedException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertificateRevokedException(
    revocationDate: Date!, 
    reason: CRLReason!, 
    authority: X500Principal!, 
    extensions: MutableMap<String!, Extension!>!)
```

Constructs a`CertificateRevokedException`with the specified revocation date, reason code, authority name, and map of extensions.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `revocationDate` | [Date](../java/util/Date.md)!:the date on which the certificate was revoked. The date is copied to protect against subsequent modification. |
| `reason` | [CRLReason](../java/security/cert/CRLReason.md)!:the revocation reason |
| `extensions` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Extension](../java/security/cert/Extension.md)!\>!:a map of X.509 Extensions. Each key is an OID String that maps to the corresponding Extension. The map is copied to prevent subsequent modification. |
| --- | --- |
| `authority` | [X500Principal](../javax/security/auth/x500/X500Principal.md)!:the`X500Principal`that represents the name of the authority that signed the certificate's revocation status information |

| Exceptions ||
|----------------------------------|-----------------------------------------------------------------|
| `java.lang.NullPointerException` | if`revocationDate`,`reason`,`authority`, or`extensions`is`null` |

## Public methods

### getAuthorityName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAuthorityName(): X500Principal!
```

Returns the name of the authority that signed the certificate's revocation status information.

| Return ||
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [X500Principal](../javax/security/auth/x500/X500Principal.md)! | the`X500Principal`that represents the name of the authority that signed the certificate's revocation status information |

### getExtensions

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExtensions(): MutableMap<String!, Extension!>!
```

Returns a map of X.509 extensions containing additional information about the revoked certificate, such as the Invalidity Date Extension. Each key is an OID String that maps to the corresponding Extension.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Extension](../java/security/cert/Extension.md)!>! | an unmodifiable map of X.509 extensions, or an empty map if there are no extensions |

### getInvalidityDate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInvalidityDate(): Date!
```

Returns the invalidity date, as specified in the Invalidity Date extension of this`CertificateRevokedException`. The invalidity date is the date on which it is known or suspected that the private key was compromised or that the certificate otherwise became invalid. This implementation calls`getExtensions()`and checks the returned map for an entry for the Invalidity Date extension OID ("2.5.29.24"). If found, it returns the invalidity date in the extension; otherwise null. A new Date object is returned each time the method is invoked to protect against subsequent modification.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------|
| [Date](../java/util/Date.md)! | the invalidity date, or`null`if not specified |

### getRevocationDate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRevocationDate(): Date!
```

Returns the date on which the certificate was revoked. A new copy is returned each time the method is invoked to protect against subsequent modification.

| Return ||
|------------------------------------------------------------------------------|---------------------|
| [Date](../java/util/Date.md)! | the revocation date |

### getRevocationReason

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRevocationReason(): CRLReason!
```

Returns the reason the certificate was revoked.

| Return ||
|-------------------------------------------------------------------------------------------|-----------------------|
| [CRLReason](../java/security/cert/CRLReason.md)! | the revocation reason |

## Properties

### message

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val message: String?
```

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the detail message string of this`Throwable`instance (which may be`null`). |
