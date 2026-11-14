# X509TrustManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# X509TrustManager

```
interface X509TrustManager : TrustManager
```

| [javax.net.ssl.X509TrustManager](../javax/net/ssl/X509TrustManager.md) |

| Known Direct Subclasses [X509ExtendedTrustManager](../javax/net/ssl/X509ExtendedTrustManager.md) |-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------| | [X509ExtendedTrustManager](../javax/net/ssl/X509ExtendedTrustManager.md) | Extensions to the`X509TrustManager`interface to support SSL/TLS connection sensitive trust management. | |
| --- | --- | --- | --- | --- | --- | --- |

Instance of this interface manage which X509 certificates may be used to authenticate the remote side of a secure socket. Decisions may be based on trusted certificate authorities, certificate revocation lists, online status checking or other means.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkClientTrusted](../javax/net/ssl/X509TrustManager.md))`(`chain:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](../java/security/cert/X509Certificate.md)!>!`, `authType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Given the partial or complete certificate chain provided by the peer, build a certificate path to a trusted root and return if it can be validated and is trusted for client SSL authentication based on the authentication type. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkServerTrusted](../javax/net/ssl/X509TrustManager.md))`(`chain:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](../java/security/cert/X509Certificate.md)!>!`, `authType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Given the partial or complete certificate chain provided by the peer, build a certificate path to a trusted root and return if it can be validated and is trusted for server SSL authentication based on the authentication type. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [X509Certificate](../java/security/cert/X509Certificate.md)!\>! | [getAcceptedIssuers](../javax/net/ssl/X509TrustManager.md))`()` Return an array of certificate authority certificates which are trusted for authenticating peers. |
| --- | --- |

## Public methods

### checkClientTrusted

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun checkClientTrusted(
    chain: Array<X509Certificate!>!, 
    authType: String!
): Unit
```

Given the partial or complete certificate chain provided by the peer, build a certificate path to a trusted root and return if it can be validated and is trusted for client SSL authentication based on the authentication type.

The authentication type is determined by the actual certificate used. For instance, if RSAPublicKey is used, the authType should be "RSA". Checking is case-sensitive.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `chain` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [X509Certificate](../java/security/cert/X509Certificate.md)!\>!:the peer certificate chain |
| `authType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the authentication type based on the client certificate |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if null or zero-length chain is passed in for the chain parameter or if null or zero-length string is passed in for the authType parameter |
| `java.security.cert.CertificateException` | if the certificate chain is not trusted by this TrustManager. |

### checkServerTrusted

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun checkServerTrusted(
    chain: Array<X509Certificate!>!, 
    authType: String!
): Unit
```

Given the partial or complete certificate chain provided by the peer, build a certificate path to a trusted root and return if it can be validated and is trusted for server SSL authentication based on the authentication type.

The authentication type is the key exchange algorithm portion of the cipher suites represented as a String, such as "RSA", "DHE_DSS". Note: for some exportable cipher suites, the key exchange algorithm is determined at run time during the handshake. For instance, for TLS_RSA_EXPORT_WITH_RC4_40_MD5, the authType should be RSA_EXPORT when an ephemeral RSA key is used for the key exchange, and RSA when the key from the server certificate is used. Checking is case-sensitive.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `chain` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [X509Certificate](../java/security/cert/X509Certificate.md)!\>!:the peer certificate chain |
| `authType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the key exchange algorithm used |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if null or zero-length chain is passed in for the chain parameter or if null or zero-length string is passed in for the authType parameter |
| `java.security.cert.CertificateException` | if the certificate chain is not trusted by this TrustManager. |

### getAcceptedIssuers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAcceptedIssuers(): Array<X509Certificate!>!
```

Return an array of certificate authority certificates which are trusted for authenticating peers.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](../java/security/cert/X509Certificate.md)!>! | a non-null (possibly empty) array of acceptable CA issuer certificates. |
