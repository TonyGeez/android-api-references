Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StrictHostnameVerifier

```
open class StrictHostnameVerifier : AbstractVerifier
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [org.apache.http.conn.ssl.AbstractVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier) ||
| | ↳ | [org.apache.http.conn.ssl.StrictHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/StrictHostnameVerifier#) |

| **This class was deprecated in API level 22.**
|
| Please use java.net.URL#openConnection instead. Please visit [this webpage](http://android-developers.blogspot.com/2011/09/androids-http-clients.html) for further details.

The Strict HostnameVerifier works the same way as Sun Java 1.4, Sun Java 5, Sun Java 6-rc. It's also pretty close to IE6. This implementation appears to be compliant with RFC 2818 for dealing with wildcards.

<br />

The hostname must match either the first CN, or any of the subject-alts. A wildcard can occur in the CN, and in any of the subject-alts. The one divergence from IE6 is how we only check the first CN. IE6 allows a match against any of the CNs present. We decided to follow in Sun Java 1.4's footsteps and only check the first CN. (If you need to check all the CN's, feel free to write your own implementation!).

<br />

A wildcard such as "\*.foo.com" matches only subdomains in the same level, for example "a.foo.com". It does not match deeper subdomains such as "a.b.foo.com".

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/StrictHostnameVerifier#StrictHostnameVerifier()()` <br /> |

| Public methods ||
|---|---|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/StrictHostnameVerifier#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/StrictHostnameVerifier#verify(kotlin.String,%20kotlin.Array,%20kotlin.Array)(host: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, cns: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, subjectAlts: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Checks to see if the supplied hostname matches any of the supplied CNs or "DNS" Subject-Alts. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#acceptableCountryWildcard(kotlin.String)(cn: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#countDots(kotlin.String)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Counts the number of dots "." in a string. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | `https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#getCNs(java.security.cert.X509Certificate)(cert: https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#!)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | `https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#getDNSSubjectAlts(java.security.cert.X509Certificate)(cert: https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#!)` Extracts the array of SubjectAlt DNS names from an X509Certificate. Returns null if there aren't any. <br /> Note: Java doesn't appear able to extract international characters from the SubjectAlts. It can only extract international characters from the CN field. <br /> (Or maybe the version of OpenSSL I'm using to test isn't storing the international characters correctly in the SubjectAlts?). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#verify(kotlin.String,%20kotlin.Array,%20kotlin.Array,%20kotlin.Boolean)(host: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, cns: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, subjectAlts: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, strictWithSubDomains: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#verify(kotlin.String,%20java.security.cert.X509Certificate)(host: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, cert: https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#!)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#verify(kotlin.String,%20javax.net.ssl.SSLSession)(host: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, session: https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession.html#!)` Verify that the host name is an acceptable match with the server's authentication scheme. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier#verify(kotlin.String,%20javax.net.ssl.SSLSocket)(host: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, ssl: https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket.html#!)` <br /> | ||
| From class `https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/X509HostnameVerifier` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/X509HostnameVerifier#verify(kotlin.String,%20kotlin.Array,%20kotlin.Array)(host: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, cns: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, subjectAlts: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Checks to see if the supplied hostname matches any of the supplied CNs or "DNS" Subject-Alts. Most implementations only look at the first CN, and ignore any additional CNs. Most implementations do look at all of the "DNS" Subject-Alts. The CNs or Subject-Alts may contain wildcards according to RFC 2818. <br /> | ||

## Public constructors

### StrictHostnameVerifier

```
StrictHostnameVerifier()
```

## Public methods

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

**Deprecated:** *Deprecated in Java.*

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

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

Checks to see if the supplied hostname matches any of the supplied CNs or "DNS" Subject-Alts. Most implementations only look at the first CN, and ignore any additional CNs. Most implementations do look at all of the "DNS" Subject-Alts. The CNs or Subject-Alts may contain wildcards according to RFC 2818.

| Parameters ||
|---|---|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The hostname to verify. |
| `cns` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: CN fields, in order, as extracted from the X.509 certificate. |
| `subjectAlts` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: Subject-Alt fields of type 2 ("DNS"), as extracted from the X.509 certificate. |

| Exceptions ||
|---|---|
| `javax.net.ssl.SSLException` | If verification failed. |
