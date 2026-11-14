# HostnameVerifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HostnameVerifier

```
interface HostnameVerifier
```

| [javax.net.ssl.HostnameVerifier](https://developer.android.com/reference/kotlin/javax/net/ssl/HostnameVerifier#) |

| Known Direct Subclasses [X509HostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/X509HostnameVerifier.html#) |----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------| | [X509HostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/X509HostnameVerifier.html#) | Interface for checking if a hostname matches the names stored inside the server's X. | |

| Known Indirect Subclasses [AbstractVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier.html#), [AllowAllHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AllowAllHostnameVerifier.html#), [BrowserCompatHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/BrowserCompatHostnameVerifier.html#), [StrictHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/StrictHostnameVerifier.html#) |----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbstractVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AbstractVerifier.html#) | Abstract base class for all standard [X509HostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/X509HostnameVerifier.html#) implementations. | | [AllowAllHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/AllowAllHostnameVerifier.html#) | The ALLOW_ALL HostnameVerifier essentially turns hostname verification off. | | [BrowserCompatHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/BrowserCompatHostnameVerifier.html#) | The HostnameVerifier that works the same way as Curl and Firefox. | | [StrictHostnameVerifier](https://developer.android.com/reference/kotlin/org/apache/http/conn/ssl/StrictHostnameVerifier.html#) | The Strict HostnameVerifier works the same way as Sun Java 1. | |

This class is the base interface for hostname verification.

During handshaking, the verification mechanism can call back to implementers of this interface to determine if this connection should be allowed.

For more information of the use of this interface on Android, see [HttpsURLConnection.setDefaultHostnameVerifier(HostnameVerifier)](https://developer.android.com/reference/kotlin/javax/net/ssl/HttpsURLConnection#setDefaultHostnameVerifier(javax.net.ssl.HostnameVerifier)).

The policies can be certificate-based or may depend on other authentication schemes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [verify](https://developer.android.com/reference/kotlin/javax/net/ssl/HostnameVerifier#verify(kotlin.String,%20javax.net.ssl.SSLSession))`(`hostname:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `session:` ` [SSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession)!`)` Verify that the host name is an acceptable match with the server's authentication scheme. |

## Public methods

### verify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun verify(
    hostname: String!, 
    session: SSLSession!
): Boolean
```

Verify that the host name is an acceptable match with the server's authentication scheme.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------|
| `hostname` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the host name |
| `session` | [SSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession)!:SSLSession used on the connection to host |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the host name is acceptable |
