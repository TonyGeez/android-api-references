# SslCertificate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SslCertificate

Kotlin| [Java](https://developer.android.com/reference/android/net/http/SslCertificate "View this page in Java") 

```
open class SslCertificate
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.http.SslCertificate](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate#) |

SSL certificate info (certificate details) class

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [DName](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate.DName) A distinguished name helper class: a 3-tuple of: - the most specific common name (CN) - the most specific organization (O) - the most specific organizational unit (OU) <br /> |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SslCertificate](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate#SslCertificate(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`issuedTo:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `issuedBy:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `validNotBefore:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `validNotAfter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new SSL certificate object |
| [SslCertificate](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate#SslCertificate(kotlin.String,%20kotlin.String,%20java.util.Date,%20java.util.Date))`(`issuedTo:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `issuedBy:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `validNotBefore:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!`, `validNotAfter:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!`)` Creates a new SSL certificate object |
| [SslCertificate](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate#SslCertificate(java.security.cert.X509Certificate))`(`certificate:` ` [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!`)` Creates a new SSL certificate object from an X509 certificate |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [SslCertificate.DName](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate.DName)! | [getIssuedBy](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate#getIssuedBy())`()` <br /> |
| open [SslCertificate.DName](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate.DName)! | [getIssuedTo](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate#getIssuedTo())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValidNotAfter](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate#getValidNotAfter())`()` <br /> |
| open [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | [getValidNotAfterDate](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate#getValidNotAfterDate())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValidNotBefore](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate#getValidNotBefore())`()` <br /> |
| open [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | [getValidNotBeforeDate](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate#getValidNotBeforeDate())`()` <br /> |
| open [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)? | [getX509Certificate](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate#getX509Certificate())`()` <br /> |
| openstatic [SslCertificate](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate#)! | [restoreState](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate#restoreState(android.os.Bundle))`(`bundle:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Restores the certificate stored in the bundle |
| openstatic [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [saveState](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate#saveState(android.net.http.SslCertificate))`(`certificate:` ` [SslCertificate](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate#)!`)` Saves the certificate state to a bundle |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate#toString())`()` <br /> |

## Public constructors

### SslCertificate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SslCertificate(
    issuedTo: String!, 
    issuedBy: String!, 
    validNotBefore: String!, 
    validNotAfter: String!)
```

**Deprecated:** *Use [SslCertificate(java.security.cert.X509Certificate)](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate#SslCertificate(java.security.cert.X509Certificate))*

Creates a new SSL certificate object

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `issuedTo` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity this certificate is issued to |
| `issuedBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity that issued this certificate |
| `validNotBefore` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The not-before date from the certificate validity period in ISO 8601 format |
| `validNotAfter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The not-after date from the certificate validity period in ISO 8601 format |

### SslCertificate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SslCertificate(
    issuedTo: String!, 
    issuedBy: String!, 
    validNotBefore: Date!, 
    validNotAfter: Date!)
```

**Deprecated:** *Use [SslCertificate(java.security.cert.X509Certificate)](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate#SslCertificate(java.security.cert.X509Certificate))*

Creates a new SSL certificate object

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `issuedTo` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity this certificate is issued to |
| `issuedBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity that issued this certificate |
| `validNotBefore` | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!:The not-before date from the certificate validity period |
| `validNotAfter` | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!:The not-after date from the certificate validity period |

### SslCertificate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SslCertificate(certificate: X509Certificate!)
```

Creates a new SSL certificate object from an X509 certificate

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------|
| `certificate` | [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!:X509 certificate |

## Public methods

### getIssuedBy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIssuedBy(): SslCertificate.DName!
```

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [SslCertificate.DName](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate.DName)! | Issued-by distinguished name or null if none has been set |

### getIssuedTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIssuedTo(): SslCertificate.DName!
```

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [SslCertificate.DName](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate.DName)! | Issued-to distinguished name or null if none has been set |

### getValidNotAfter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValidNotAfter(): String!
```

**Deprecated:** *Use [getValidNotAfterDate()](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate#getValidNotAfterDate())*

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | Not-after date from the certificate validity period in ISO 8601 format or "" if none has been set |

### getValidNotAfterDate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValidNotAfterDate(): Date!
```

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | Not-after date from the certificate validity period or "" if none has been set |

### getValidNotBefore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValidNotBefore(): String!
```

**Deprecated:** *Use [getValidNotBeforeDate()](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate#getValidNotBeforeDate())*

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | Not-before date from the certificate validity period in ISO 8601 format or "" if none has been set |

### getValidNotBeforeDate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValidNotBeforeDate(): Date!
```

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | Not-before date from the certificate validity period or "" if none has been set |

### getX509Certificate

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getX509Certificate(): X509Certificate?
```

| Return ||
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)? | The`X509Certificate`used to create this`SslCertificate`or`null`if no certificate was provided. |

### restoreState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun restoreState(bundle: Bundle!): SslCertificate!
```

Restores the certificate stored in the bundle

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `bundle` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:The bundle with the certificate state stored in it |

| Return ||
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [SslCertificate](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate#)! | The SSL certificate stored in the bundle or null if fails |

### saveState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun saveState(certificate: SslCertificate!): Bundle!
```

Saves the certificate state to a bundle

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------|
| `certificate` | [SslCertificate](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate#)!:The SSL certificate to store |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | A bundle with the certificate stored in it or null if fails |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | A string representation of this certificate for debugging |
