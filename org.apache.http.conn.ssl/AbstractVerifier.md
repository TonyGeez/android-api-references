# AbstractVerifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractVerifier

```
abstract class AbstractVerifier : X509HostnameVerifier
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.apache.http.conn.ssl.AbstractVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#) |

| Known Direct Subclasses [AllowAllHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AllowAllHostnameVerifier), [BrowserCompatHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/BrowserCompatHostnameVerifier), [StrictHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/StrictHostnameVerifier) |----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------| | [AllowAllHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AllowAllHostnameVerifier) | The ALLOW_ALL HostnameVerifier essentially turns hostname verification off. | | [BrowserCompatHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/BrowserCompatHostnameVerifier) | The HostnameVerifier that works the same way as Curl and Firefox. | | [StrictHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/StrictHostnameVerifier) | The Strict HostnameVerifier works the same way as Sun Java 1. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 22.**
|
| Please use java.net.URL#openConnection instead. Please visit [this webpage](http://android-developers.blogspot.com/2011/09/androids-http-clients.html) for further details.

Abstract base class for all standard [X509HostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/X509HostnameVerifier) implementations.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AbstractVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#AbstractVerifier())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [acceptableCountryWildcard](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#acceptableCountryWildcard(kotlin.String))`(`cn:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [countDots](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#countDots(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Counts the number of dots ". |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getCNs](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#getCNs(java.security.cert.X509Certificate))`(`cert:` ` [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!`)` <br /> |
| --- | --- |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getDNSSubjectAlts](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#getDNSSubjectAlts(java.security.cert.X509Certificate))`(`cert:` ` [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!`)` Extracts the array of SubjectAlt DNS names from an X509Certificate. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [verify](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#verify(kotlin.String,%20kotlin.Array,%20kotlin.Array,%20kotlin.Boolean))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cns:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `subjectAlts:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `strictWithSubDomains:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [verify](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#verify(kotlin.String,%20java.security.cert.X509Certificate))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cert:` ` [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!`)` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [verify](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#verify(kotlin.String,%20javax.net.ssl.SSLSession))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `session:` ` [SSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession.html#)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [verify](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#verify(kotlin.String,%20javax.net.ssl.SSLSocket))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `ssl:` ` [SSLSocket](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket.html#)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [X509HostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/X509HostnameVerifier) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [verify](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/X509HostnameVerifier#verify(kotlin.String,%20kotlin.Array,%20kotlin.Array))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cns:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `subjectAlts:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> Checks to see if the supplied hostname matches any of the supplied CNs or "DNS" Subject-Alts. Most implementations only look at the first CN, and ignore any additional CNs. Most implementations do look at all of the "DNS" Subject-Alts. The CNs or Subject-Alts may contain wildcards according to RFC 2818. <br /> | ||

## Public constructors

### AbstractVerifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AbstractVerifier()
```

## Public methods

### acceptableCountryWildcard

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun acceptableCountryWildcard(cn: String!): Boolean
```

**Deprecated:** *Deprecated in Java.* 

### countDots

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun countDots(s: String!): Int
```

**Deprecated:** *Deprecated in Java.*

Counts the number of dots "." in a string.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:string to count dots from |

| Return ||
|----------------------------------------------------------------------------|----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | number of dots |

### getCNs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getCNs(cert: X509Certificate!): Array<String!>!
```

**Deprecated:** *Deprecated in Java.* 

### getDNSSubjectAlts

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDNSSubjectAlts(cert: X509Certificate!): Array<String!>!
```

**Deprecated:** *Deprecated in Java.*

Extracts the array of SubjectAlt DNS names from an X509Certificate. Returns null if there aren't any.

<br />

Note: Java doesn't appear able to extract international characters from the SubjectAlts. It can only extract international characters from the CN field.

<br />

(Or maybe the version of OpenSSL I'm using to test isn't storing the international characters correctly in the SubjectAlts?).

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------|
| `cert` | [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!:X509Certificate |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | Array of SubjectALT DNS names stored in the certificate. |

### verify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun verify(
    host: String!, 
    cns: Array<String!>!, 
    subjectAlts: Array<String!>!, 
    strictWithSubDomains: Boolean
): Unit
```

**Deprecated:** *Deprecated in Java.* 

### verify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun verify(
    host: String!, 
    cert: X509Certificate!
): Unit
```

**Deprecated:** *Deprecated in Java.* 

### verify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun verify(
    host: String!, 
    session: SSLSession!
): Boolean
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `hostname` | the host name |
| `session` | [SSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession.html#)!:SSLSession used on the connection to host |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the host name is acceptable |

### verify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun verify(
    host: String!, 
    ssl: SSLSocket!
): Unit
```

**Deprecated:** *Deprecated in Java.*
