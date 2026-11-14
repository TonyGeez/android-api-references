# HostnameVerifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HostnameVerifier

```
interface HostnameVerifier
```

| [javax.net.ssl.HostnameVerifier](../javax/net/ssl/HostnameVerifier.md) |

| Known Direct Subclasses [X509HostnameVerifier](../org/apache/http/conn/ssl/X509HostnameVerifier.md) |----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------| | [X509HostnameVerifier](../org/apache/http/conn/ssl/X509HostnameVerifier.md) | Interface for checking if a hostname matches the names stored inside the server's X. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AbstractVerifier](../org/apache/http/conn/ssl/AbstractVerifier.md), [AllowAllHostnameVerifier](../org/apache/http/conn/ssl/AllowAllHostnameVerifier.md), [BrowserCompatHostnameVerifier](../org/apache/http/conn/ssl/BrowserCompatHostnameVerifier.md), [StrictHostnameVerifier](../org/apache/http/conn/ssl/StrictHostnameVerifier.md) |----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbstractVerifier](../org/apache/http/conn/ssl/AbstractVerifier.md) | Abstract base class for all standard [X509HostnameVerifier](../org/apache/http/conn/ssl/X509HostnameVerifier.md) implementations. | | [AllowAllHostnameVerifier](../org/apache/http/conn/ssl/AllowAllHostnameVerifier.md) | The ALLOW_ALL HostnameVerifier essentially turns hostname verification off. | | [BrowserCompatHostnameVerifier](../org/apache/http/conn/ssl/BrowserCompatHostnameVerifier.md) | The HostnameVerifier that works the same way as Curl and Firefox. | | [StrictHostnameVerifier](../org/apache/http/conn/ssl/StrictHostnameVerifier.md) | The Strict HostnameVerifier works the same way as Sun Java 1. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This class is the base interface for hostname verification.

During handshaking, the verification mechanism can call back to implementers of this interface to determine if this connection should be allowed.

For more information of the use of this interface on Android, see [HttpsURLConnection.setDefaultHostnameVerifier(HostnameVerifier)](../javax/net/ssl/HttpsURLConnection.md)).

The policies can be certificate-based or may depend on other authentication schemes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [verify](../javax/net/ssl/HostnameVerifier.md))`(`hostname:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `session:` ` [SSLSession](../javax/net/ssl/SSLSession.md)!`)` Verify that the host name is an acceptable match with the server's authentication scheme. |

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
| `session` | [SSLSession](../javax/net/ssl/SSLSession.md)!:SSLSession used on the connection to host |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the host name is acceptable |
