Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# X509HostnameVerifier

```
interface X509HostnameVerifier : HostnameVerifier
```

| [org.apache.http.conn.ssl.X509HostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/X509HostnameVerifier#) |

| Known Direct Subclasses [AbstractVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier) |---|---| | [AbstractVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier) | Abstract base class for all standard `https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/X509HostnameVerifier#` implementations. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AllowAllHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AllowAllHostnameVerifier), [BrowserCompatHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/BrowserCompatHostnameVerifier), [StrictHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/StrictHostnameVerifier) |---|---| | [AllowAllHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AllowAllHostnameVerifier) | The ALLOW_ALL HostnameVerifier essentially turns hostname verification off. | | [BrowserCompatHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/BrowserCompatHostnameVerifier) | The HostnameVerifier that works the same way as Curl and Firefox. | | [StrictHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/StrictHostnameVerifier) | The Strict HostnameVerifier works the same way as Sun Java 1. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 22.**
|
| Please use java.net.URL#openConnection instead. Please visit [this webpage](http://android-developers.blogspot.com/2011/09/androids-http-clients.html) for further details.

Interface for checking if a hostname matches the names stored inside the server's X.509 certificate. Implements javax.net.ssl.HostnameVerifier, but we don't actually use that interface. Instead we added some methods that take String parameters (instead of javax.net.ssl.HostnameVerifier's SSLSession). JUnit is a lot easier this way! :-)

<br />

We provide the HostnameVerifier.DEFAULT, HostnameVerifier.STRICT, and HostnameVerifier.ALLOW_ALL implementations. But feel free to define your own implementation!

<br />

Inspired by Sebastian Hauer's original StrictSSLProtocolSocketFactory in the HttpClient "contrib" repository.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/X509HostnameVerifier#verify(kotlin.String,%20kotlin.Array,%20kotlin.Array)(host: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, cns: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, subjectAlts: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Checks to see if the supplied hostname matches any of the supplied CNs or "DNS" Subject-Alts. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/X509HostnameVerifier#verify(kotlin.String,%20java.security.cert.X509Certificate)(host: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, cert: https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#!)` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/X509HostnameVerifier#verify(kotlin.String,%20javax.net.ssl.SSLSession)(host: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, session: https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession.html#!)` Verify that the host name is an acceptable match with the server's authentication scheme. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/X509HostnameVerifier#verify(kotlin.String,%20javax.net.ssl.SSLSocket)(host: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, ssl: https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket.html#!)` <br /> |

## Public methods

### verify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun verify(
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
| --- | --- |

| Exceptions ||
|---|---|
| `javax.net.ssl.SSLException` | If verification failed. |

### verify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun verify(
    host: String!, 
    cert: X509Certificate!
): Unit
```

**Deprecated:** *Deprecated in Java.*

### verify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun verify(
    host: String!, 
    session: SSLSession!
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Verify that the host name is an acceptable match with the server's authentication scheme.

| Parameters ||
|---|---|
| `hostname` | the host name |
| `session` | [SSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession.html#)!: SSLSession used on the connection to host |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the host name is acceptable |

### verify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun verify(
    host: String!, 
    ssl: SSLSocket!
): Unit
```

**Deprecated:** *Deprecated in Java.*
