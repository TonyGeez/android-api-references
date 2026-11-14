# SslCertificate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SslCertificate

Kotlin| [Java](../android/net/http/SslCertificate.md) 
| --- | --- |

```
open class SslCertificate
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.http.SslCertificate](../android/net/http/SslCertificate.md) |

SSL certificate info (certificate details) class

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [DName](../android/net/http/SslCertificate.DName.md) A distinguished name helper class: a 3-tuple of: - the most specific common name (CN) - the most specific organization (O) - the most specific organizational unit (OU) <br /> |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SslCertificate](../android/net/http/SslCertificate.md))`(`issuedTo:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `issuedBy:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `validNotBefore:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `validNotAfter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new SSL certificate object |
| [SslCertificate](../android/net/http/SslCertificate.md))`(`issuedTo:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `issuedBy:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `validNotBefore:` ` [Date](../java/util/Date.md)!`, `validNotAfter:` ` [Date](../java/util/Date.md)!`)` Creates a new SSL certificate object |
| [SslCertificate](../android/net/http/SslCertificate.md))`(`certificate:` ` [X509Certificate](../java/security/cert/X509Certificate.md)!`)` Creates a new SSL certificate object from an X509 certificate |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [SslCertificate.DName](../android/net/http/SslCertificate.DName.md)! | [getIssuedBy](../android/net/http/SslCertificate.md))`()` <br /> |
| open [SslCertificate.DName](../android/net/http/SslCertificate.DName.md)! | [getIssuedTo](../android/net/http/SslCertificate.md))`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValidNotAfter](../android/net/http/SslCertificate.md))`()` <br /> |
| --- | --- |
| open [Date](../java/util/Date.md)! | [getValidNotAfterDate](../android/net/http/SslCertificate.md))`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValidNotBefore](../android/net/http/SslCertificate.md))`()` <br /> |
| open [Date](../java/util/Date.md)! | [getValidNotBeforeDate](../android/net/http/SslCertificate.md))`()` <br /> |
| --- | --- |
| open [X509Certificate](../java/security/cert/X509Certificate.md)? | [getX509Certificate](../android/net/http/SslCertificate.md))`()` <br /> |
| openstatic [SslCertificate](../android/net/http/SslCertificate.md)! | [restoreState](../android/net/http/SslCertificate.md))`(`bundle:` ` [Bundle](../android/os/Bundle.md)!`)` Restores the certificate stored in the bundle |
| openstatic [Bundle](../android/os/Bundle.md)! | [saveState](../android/net/http/SslCertificate.md))`(`certificate:` ` [SslCertificate](../android/net/http/SslCertificate.md)!`)` Saves the certificate state to a bundle |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/net/http/SslCertificate.md))`()` <br /> |

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

**Deprecated:** *Use [SslCertificate(java.security.cert.X509Certificate)](../android/net/http/SslCertificate.md))*

Creates a new SSL certificate object

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `issuedTo` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity this certificate is issued to |
| `issuedBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity that issued this certificate |
| `validNotBefore` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The not-before date from the certificate validity period in ISO 8601 format |
| --- | --- |
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

**Deprecated:** *Use [SslCertificate(java.security.cert.X509Certificate)](../android/net/http/SslCertificate.md))*

Creates a new SSL certificate object

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `issuedTo` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity this certificate is issued to |
| `issuedBy` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The entity that issued this certificate |
| `validNotBefore` | [Date](../java/util/Date.md)!:The not-before date from the certificate validity period |
| --- | --- |
| `validNotAfter` | [Date](../java/util/Date.md)!:The not-after date from the certificate validity period |

### SslCertificate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SslCertificate(certificate: X509Certificate!)
```

Creates a new SSL certificate object from an X509 certificate

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------|
| `certificate` | [X509Certificate](../java/security/cert/X509Certificate.md)!:X509 certificate |

## Public methods

### getIssuedBy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIssuedBy(): SslCertificate.DName!
```

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [SslCertificate.DName](../android/net/http/SslCertificate.DName.md)! | Issued-by distinguished name or null if none has been set |

### getIssuedTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIssuedTo(): SslCertificate.DName!
```

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [SslCertificate.DName](../android/net/http/SslCertificate.DName.md)! | Issued-to distinguished name or null if none has been set |

### getValidNotAfter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValidNotAfter(): String!
```

**Deprecated:** *Use [getValidNotAfterDate()](../android/net/http/SslCertificate.md))*

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
| [Date](../java/util/Date.md)! | Not-after date from the certificate validity period or "" if none has been set |

### getValidNotBefore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValidNotBefore(): String!
```

**Deprecated:** *Use [getValidNotBeforeDate()](../android/net/http/SslCertificate.md))*

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
| [Date](../java/util/Date.md)! | Not-before date from the certificate validity period or "" if none has been set |

### getX509Certificate

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getX509Certificate(): X509Certificate?
```

| Return ||
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [X509Certificate](../java/security/cert/X509Certificate.md)? | The`X509Certificate`used to create this`SslCertificate`or`null`if no certificate was provided. |

### restoreState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun restoreState(bundle: Bundle!): SslCertificate!
```

Restores the certificate stored in the bundle

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `bundle` | [Bundle](../android/os/Bundle.md)!:The bundle with the certificate state stored in it |

| Return ||
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [SslCertificate](../android/net/http/SslCertificate.md)! | The SSL certificate stored in the bundle or null if fails |

### saveState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun saveState(certificate: SslCertificate!): Bundle!
```

Saves the certificate state to a bundle

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------|
| `certificate` | [SslCertificate](../android/net/http/SslCertificate.md)!:The SSL certificate to store |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Bundle](../android/os/Bundle.md)! | A bundle with the certificate stored in it or null if fails |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | A string representation of this certificate for debugging |
