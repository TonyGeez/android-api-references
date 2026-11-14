# SslError

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SslError

Kotlin| [Java](../android/net/http/SslError.md) 
| --- | --- |

```
open class SslError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.http.SslError](../android/net/http/SslError.md) |

This class represents a set of one or more SSL errors and the associated SSL certificate.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SSL_DATE_INVALID](../android/net/http/SslError.md) The date of the certificate is invalid |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SSL_EXPIRED](../android/net/http/SslError.md) The certificate has expired |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SSL_IDMISMATCH](../android/net/http/SslError.md) Hostname mismatch |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SSL_INVALID](../android/net/http/SslError.md) A generic error occurred |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SSL_MAX_ERROR](../android/net/http/SslError.md) The number of different SSL errors. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SSL_NOTYETVALID](../android/net/http/SslError.md) The certificate is not yet valid |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SSL_UNTRUSTED](../android/net/http/SslError.md) The certificate authority is not trusted |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SslError](../android/net/http/SslError.md))`(`error:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `certificate:` ` [SslCertificate](../android/net/http/SslCertificate.md)!`)` Creates a new SslError object using the supplied error and certificate. |
| [SslError](../android/net/http/SslError.md))`(`error:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `certificate:` ` [SslCertificate](../android/net/http/SslCertificate.md)!`, `url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new SslError object using the supplied error, certificate and URL. |
| [SslError](../android/net/http/SslError.md))`(`error:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `certificate:` ` [X509Certificate](../java/security/cert/X509Certificate.md)!`)` Creates a new SslError object using the supplied error and certificate. |
| [SslError](../android/net/http/SslError.md))`(`error:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `certificate:` ` [X509Certificate](../java/security/cert/X509Certificate.md)!`, `url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new SslError object using the supplied error, certificate and URL. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addError](../android/net/http/SslError.md))`(`error:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adds the supplied SSL error to the set. |
| open [SslCertificate](../android/net/http/SslCertificate.md)! | [getCertificate](../android/net/http/SslError.md))`()` Gets the SSL certificate associated with this object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPrimaryError](../android/net/http/SslError.md))`()` Gets the most severe SSL error in this object's set of errors. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getUrl](../android/net/http/SslError.md))`()` Gets the URL associated with this object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasError](../android/net/http/SslError.md))`(`error:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines whether this object includes the supplied error. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/net/http/SslError.md))`()` Returns a string representation of this object. |
| --- | --- |

## Constants

### SSL_DATE_INVALID

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SSL_DATE_INVALID: Int
```

The date of the certificate is invalid 

 Value: 4

### SSL_EXPIRED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SSL_EXPIRED: Int
```

The certificate has expired 

 Value: 1

### SSL_IDMISMATCH

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SSL_IDMISMATCH: Int
```

Hostname mismatch 

 Value: 2

### SSL_INVALID

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SSL_INVALID: Int
```

A generic error occurred 

 Value: 5

### SSL_MAX_ERROR

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SSL_MAX_ERROR: Int
```

**Deprecated:** *This constant is not necessary for using the SslError API and can change from release to release.*

The number of different SSL errors. 

 Value: 6

### SSL_NOTYETVALID

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SSL_NOTYETVALID: Int
```

The certificate is not yet valid 

 Value: 0

### SSL_UNTRUSTED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SSL_UNTRUSTED: Int
```

The certificate authority is not trusted 

 Value: 3

## Public constructors

### SslError

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SslError(
    error: Int, 
    certificate: SslCertificate!)
```

**Deprecated:** *Use [SslError(int,android.net.http.SslCertificate,java.lang.String)](../android/net/http/SslError.md))*

Creates a new SslError object using the supplied error and certificate. The URL will be set to the empty string.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------|
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The SSL error |
| `certificate` | [SslCertificate](../android/net/http/SslCertificate.md)!:The associated SSL certificate |

### SslError

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SslError(
    error: Int, 
    certificate: SslCertificate!, 
    url: String!)
```

Creates a new SslError object using the supplied error, certificate and URL.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------|
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The SSL error |
| `certificate` | [SslCertificate](../android/net/http/SslCertificate.md)!:The associated SSL certificate |
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The associated URL |
| --- | --- |

### SslError

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SslError(
    error: Int, 
    certificate: X509Certificate!)
```

**Deprecated:** *Use [SslError(int,java.security.cert.X509Certificate,java.lang.String)](../android/net/http/SslError.md))*

Creates a new SslError object using the supplied error and certificate. The URL will be set to the empty string.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The SSL error |
| `certificate` | [X509Certificate](../java/security/cert/X509Certificate.md)!:The associated SSL certificate |

### SslError

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SslError(
    error: Int, 
    certificate: X509Certificate!, 
    url: String!)
```

Creates a new SslError object using the supplied error, certificate and URL.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The SSL error |
| `certificate` | [X509Certificate](../java/security/cert/X509Certificate.md)!:The associated SSL certificate |
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The associated URL |
| --- | --- |

## Public methods

### addError

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addError(error: Int): Boolean
```

Adds the supplied SSL error to the set.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------|
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The SSL error to add |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the error being added is a known SSL error, otherwise false. |

### getCertificate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCertificate(): SslCertificate!
```

Gets the SSL certificate associated with this object.

| Return ||
|---------------------------------------------------------------------------------------------------|--------------------------------|
| [SslCertificate](../android/net/http/SslCertificate.md)! | The SSL certificate, non-null. |

### getPrimaryError

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrimaryError(): Int
```

Gets the most severe SSL error in this object's set of errors. Returns -1 if the set is empty.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The most severe SSL error, or -1 if the set is empty. |

### getUrl

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUrl(): String!
```

Gets the URL associated with this object.

| Return ||
|-----------------------------------------------------------------------------------|--------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The URL, non-null. |

### hasError

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasError(error: Int): Boolean
```

Determines whether this object includes the supplied error.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------|
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The SSL error to check for |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this object includes the error, otherwise false. |

### toString

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of this object.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | A String representation of this object. |
