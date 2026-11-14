# AllowAllHostnameVerifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AllowAllHostnameVerifier

```
open class AllowAllHostnameVerifier : AbstractVerifier
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [org.apache.http.conn.ssl.AbstractVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier) ||
| | ↳ | [org.apache.http.conn.ssl.AllowAllHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AllowAllHostnameVerifier#) |

| **This class was deprecated in API level 22.**
|
| Please use java.net.URL#openConnection instead. Please visit [this webpage](http://android-developers.blogspot.com/2011/09/androids-http-clients.html) for further details.

The ALLOW_ALL HostnameVerifier essentially turns hostname verification off. This implementation is a no-op, and never throws the SSLException.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AllowAllHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AllowAllHostnameVerifier#AllowAllHostnameVerifier())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AllowAllHostnameVerifier#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [verify](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AllowAllHostnameVerifier#verify(kotlin.String,%20kotlin.Array,%20kotlin.Array))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cns:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `subjectAlts:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [AbstractVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [acceptableCountryWildcard](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#acceptableCountryWildcard(kotlin.String))`(`cn:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [countDots](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#countDots(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Counts the number of dots "." in a string. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getCNs](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#getCNs(java.security.cert.X509Certificate))`(`cert:` ` [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!`)` <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getDNSSubjectAlts](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#getDNSSubjectAlts(java.security.cert.X509Certificate))`(`cert:` ` [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!`)` <br /> Extracts the array of SubjectAlt DNS names from an X509Certificate. Returns null if there aren't any. <br /> Note: Java doesn't appear able to extract international characters from the SubjectAlts. It can only extract international characters from the CN field. <br /> (Or maybe the version of OpenSSL I'm using to test isn't storing the international characters correctly in the SubjectAlts?). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [verify](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#verify(kotlin.String,%20kotlin.Array,%20kotlin.Array,%20kotlin.Boolean))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cns:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `subjectAlts:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `strictWithSubDomains:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [verify](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#verify(kotlin.String,%20java.security.cert.X509Certificate))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cert:` ` [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [verify](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#verify(kotlin.String,%20javax.net.ssl.SSLSession))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `session:` ` [SSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession.html#)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [verify](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#verify(kotlin.String,%20javax.net.ssl.SSLSocket))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `ssl:` ` [SSLSocket](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket.html#)!`)` <br /> | ||
| From class [X509HostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/X509HostnameVerifier) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [verify](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/X509HostnameVerifier#verify(kotlin.String,%20kotlin.Array,%20kotlin.Array))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cns:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `subjectAlts:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> Checks to see if the supplied hostname matches any of the supplied CNs or "DNS" Subject-Alts. Most implementations only look at the first CN, and ignore any additional CNs. Most implementations do look at all of the "DNS" Subject-Alts. The CNs or Subject-Alts may contain wildcards according to RFC 2818. <br /> | ||

## Public constructors

### AllowAllHostnameVerifier

```
AllowAllHostnameVerifier()
```

## Public methods

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### verify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun verify(
    host: String!, 
    cns: Array<String!>!, 
    subjectAlts: Array<String!>!
): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cns` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:CN fields, in order, as extracted from the X.509 certificate. |
| `subjectAlts` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:Subject-Alt fields of type 2 ("DNS"), as extracted from the X.509 certificate. |
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The hostname to verify. |
| --- | --- |

| Exceptions ||
|------------------------------|-------------------------|
| `javax.net.ssl.SSLException` | If verification failed. |
