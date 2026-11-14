# X509ExtendedTrustManager

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# X509ExtendedTrustManager

```
abstract class X509ExtendedTrustManager : X509TrustManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.net.ssl.X509ExtendedTrustManager](https://developer.android.com/reference/kotlin/javax/net/ssl/X509ExtendedTrustManager#) |

Extensions to the`X509TrustManager`interface to support SSL/TLS connection sensitive trust management.

To prevent man-in-the-middle attacks, hostname checks can be done to verify that the hostname in an end-entity certificate matches the targeted hostname. TLS does not require such checks, but some protocols over TLS (such as HTTPS) do. In earlier versions of the JDK, the certificate chain checks were done at the SSL/TLS layer, and the hostname verification checks were done at the layer over TLS. This class allows for the checking to be done during a single call to this class.

RFC 2830 defines the server identification specification for the "LDAPS" algorithm. RFC 2818 defines both the server identification and the client identification specification for the "HTTPS" algorithm.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [X509ExtendedTrustManager](https://developer.android.com/reference/kotlin/javax/net/ssl/X509ExtendedTrustManager#X509ExtendedTrustManager())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkClientTrusted](https://developer.android.com/reference/kotlin/javax/net/ssl/X509ExtendedTrustManager#checkClientTrusted(kotlin.Array,%20kotlin.String,%20java.net.Socket))`(`chain:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!>!`, `authType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `socket:` ` [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!`)` Given the partial or complete certificate chain provided by the peer, build and validate the certificate path based on the authentication type and ssl parameters. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkClientTrusted](https://developer.android.com/reference/kotlin/javax/net/ssl/X509ExtendedTrustManager#checkClientTrusted(kotlin.Array,%20kotlin.String,%20javax.net.ssl.SSLEngine))`(`chain:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!>!`, `authType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `engine:` ` [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine)!`)` Given the partial or complete certificate chain provided by the peer, build and validate the certificate path based on the authentication type and ssl parameters. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkServerTrusted](https://developer.android.com/reference/kotlin/javax/net/ssl/X509ExtendedTrustManager#checkServerTrusted(kotlin.Array,%20kotlin.String,%20java.net.Socket))`(`chain:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!>!`, `authType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `socket:` ` [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!`)` Given the partial or complete certificate chain provided by the peer, build and validate the certificate path based on the authentication type and ssl parameters. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkServerTrusted](https://developer.android.com/reference/kotlin/javax/net/ssl/X509ExtendedTrustManager#checkServerTrusted(kotlin.Array,%20kotlin.String,%20javax.net.ssl.SSLEngine))`(`chain:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!>!`, `authType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `engine:` ` [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine)!`)` Given the partial or complete certificate chain provided by the peer, build and validate the certificate path based on the authentication type and ssl parameters. |

| Inherited functions ||
|---|---|
| From class [X509TrustManager](https://developer.android.com/reference/kotlin/javax/net/ssl/X509TrustManager) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkClientTrusted](https://developer.android.com/reference/kotlin/javax/net/ssl/X509TrustManager#checkClientTrusted(kotlin.Array,%20kotlin.String))`(`chain:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!>!`, `authType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Given the partial or complete certificate chain provided by the peer, build a certificate path to a trusted root and return if it can be validated and is trusted for client SSL authentication based on the authentication type. The authentication type is determined by the actual certificate used. For instance, if RSAPublicKey is used, the authType should be "RSA". Checking is case-sensitive. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkServerTrusted](https://developer.android.com/reference/kotlin/javax/net/ssl/X509TrustManager#checkServerTrusted(kotlin.Array,%20kotlin.String))`(`chain:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!>!`, `authType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Given the partial or complete certificate chain provided by the peer, build a certificate path to a trusted root and return if it can be validated and is trusted for server SSL authentication based on the authentication type. The authentication type is the key exchange algorithm portion of the cipher suites represented as a String, such as "RSA", "DHE_DSS". Note: for some exportable cipher suites, the key exchange algorithm is determined at run time during the handshake. For instance, for TLS_RSA_EXPORT_WITH_RC4_40_MD5, the authType should be RSA_EXPORT when an ephemeral RSA key is used for the key exchange, and RSA when the key from the server certificate is used. Checking is case-sensitive. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!>! | [getAcceptedIssuers](https://developer.android.com/reference/kotlin/javax/net/ssl/X509TrustManager#getAcceptedIssuers())`()` <br /> Return an array of certificate authority certificates which are trusted for authenticating peers. <br /> | ||

## Public constructors

### X509ExtendedTrustManager

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
X509ExtendedTrustManager()
```

## Public methods

### checkClientTrusted

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun checkClientTrusted(
    chain: Array<X509Certificate!>!, 
    authType: String!, 
    socket: Socket!
): Unit
```

Given the partial or complete certificate chain provided by the peer, build and validate the certificate path based on the authentication type and ssl parameters.

The authentication type is determined by the actual certificate used. For instance, if RSAPublicKey is used, the authType should be "RSA". Checking is case-sensitive.

If the`socket`parameter is an instance of [javax.net.ssl.SSLSocket](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket), and the endpoint identification algorithm of the`SSLParameters`is non-empty, to prevent man-in-the-middle attacks, the address that the`socket`connected to should be checked against the peer's identity presented in the end-entity X509 certificate, as specified in the endpoint identification algorithm.

If the`socket`parameter is an instance of [javax.net.ssl.SSLSocket](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket), and the algorithm constraints of the`SSLParameters`is non-null, for every certificate in the certification path, fields such as subject public key, the signature algorithm, key usage, extended key usage, etc. need to conform to the algorithm constraints in place on this socket.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `chain` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!\>!:the peer certificate chain |
| `authType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the key exchange algorithm used |
| `socket` | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!:the socket used for this connection. This parameter can be null, which indicates that implementations need not check the ssl parameters |
| --- | --- |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if null or zero-length array is passed in for the`chain`parameter or if null or zero-length string is passed in for the`authType`parameter |
| `java.security.cert.CertificateException` | if the certificate chain is not trusted by this TrustManager |

**See Also**

- [javax.net.ssl.SSLParameters#getEndpointIdentificationAlgorithm](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getEndpointIdentificationAlgorithm())
- [javax.net.ssl.SSLParameters#setEndpointIdentificationAlgorithm(String)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setEndpointIdentificationAlgorithm(kotlin.String))
- [javax.net.ssl.SSLParameters#getAlgorithmConstraints](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getAlgorithmConstraints()) 

### checkClientTrusted

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun checkClientTrusted(
    chain: Array<X509Certificate!>!, 
    authType: String!, 
    engine: SSLEngine!
): Unit
```

Given the partial or complete certificate chain provided by the peer, build and validate the certificate path based on the authentication type and ssl parameters.

The authentication type is determined by the actual certificate used. For instance, if RSAPublicKey is used, the authType should be "RSA". Checking is case-sensitive.

If the`engine`parameter is available, and the endpoint identification algorithm of the`SSLParameters`is non-empty, to prevent man-in-the-middle attacks, the address that the`engine`connected to should be checked against the peer's identity presented in the end-entity X509 certificate, as specified in the endpoint identification algorithm.

If the`engine`parameter is available, and the algorithm constraints of the`SSLParameters`is non-null, for every certificate in the certification path, fields such as subject public key, the signature algorithm, key usage, extended key usage, etc. need to conform to the algorithm constraints in place on this engine.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `chain` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!\>!:the peer certificate chain |
| `authType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the key exchange algorithm used |
| `engine` | [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine)!:the engine used for this connection. This parameter can be null, which indicates that implementations need not check the ssl parameters |
| --- | --- |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if null or zero-length array is passed in for the`chain`parameter or if null or zero-length string is passed in for the`authType`parameter |
| `java.security.cert.CertificateException` | if the certificate chain is not trusted by this TrustManager |

**See Also**

- [javax.net.ssl.SSLParameters#getEndpointIdentificationAlgorithm](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getEndpointIdentificationAlgorithm())
- [javax.net.ssl.SSLParameters#setEndpointIdentificationAlgorithm(String)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setEndpointIdentificationAlgorithm(kotlin.String))
- [javax.net.ssl.SSLParameters#getAlgorithmConstraints](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getAlgorithmConstraints()) 

### checkServerTrusted

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun checkServerTrusted(
    chain: Array<X509Certificate!>!, 
    authType: String!, 
    socket: Socket!
): Unit
```

Given the partial or complete certificate chain provided by the peer, build and validate the certificate path based on the authentication type and ssl parameters.

The authentication type is the key exchange algorithm portion of the cipher suites represented as a String, such as "RSA", "DHE_DSS". Note: for some exportable cipher suites, the key exchange algorithm is determined at run time during the handshake. For instance, for TLS_RSA_EXPORT_WITH_RC4_40_MD5, the authType should be RSA_EXPORT when an ephemeral RSA key is used for the key exchange, and RSA when the key from the server certificate is used. Checking is case-sensitive.

If the`socket`parameter is an instance of [javax.net.ssl.SSLSocket](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket), and the endpoint identification algorithm of the`SSLParameters`is non-empty, to prevent man-in-the-middle attacks, the address that the`socket`connected to should be checked against the peer's identity presented in the end-entity X509 certificate, as specified in the endpoint identification algorithm.

If the`socket`parameter is an instance of [javax.net.ssl.SSLSocket](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket), and the algorithm constraints of the`SSLParameters`is non-null, for every certificate in the certification path, fields such as subject public key, the signature algorithm, key usage, extended key usage, etc. need to conform to the algorithm constraints in place on this socket.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `chain` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!\>!:the peer certificate chain |
| `authType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the key exchange algorithm used |
| `socket` | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#)!:the socket used for this connection. This parameter can be null, which indicates that implementations need not check the ssl parameters |
| --- | --- |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if null or zero-length array is passed in for the`chain`parameter or if null or zero-length string is passed in for the`authType`parameter |
| `java.security.cert.CertificateException` | if the certificate chain is not trusted by this TrustManager |

**See Also**

- [javax.net.ssl.SSLParameters#getEndpointIdentificationAlgorithm](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getEndpointIdentificationAlgorithm())
- [javax.net.ssl.SSLParameters#setEndpointIdentificationAlgorithm(String)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setEndpointIdentificationAlgorithm(kotlin.String))
- [javax.net.ssl.SSLParameters#getAlgorithmConstraints](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getAlgorithmConstraints()) 

### checkServerTrusted

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun checkServerTrusted(
    chain: Array<X509Certificate!>!, 
    authType: String!, 
    engine: SSLEngine!
): Unit
```

Given the partial or complete certificate chain provided by the peer, build and validate the certificate path based on the authentication type and ssl parameters.

The authentication type is the key exchange algorithm portion of the cipher suites represented as a String, such as "RSA", "DHE_DSS". Note: for some exportable cipher suites, the key exchange algorithm is determined at run time during the handshake. For instance, for TLS_RSA_EXPORT_WITH_RC4_40_MD5, the authType should be RSA_EXPORT when an ephemeral RSA key is used for the key exchange, and RSA when the key from the server certificate is used. Checking is case-sensitive.

If the`engine`parameter is available, and the endpoint identification algorithm of the`SSLParameters`is non-empty, to prevent man-in-the-middle attacks, the address that the`engine`connected to should be checked against the peer's identity presented in the end-entity X509 certificate, as specified in the endpoint identification algorithm.

If the`engine`parameter is available, and the algorithm constraints of the`SSLParameters`is non-null, for every certificate in the certification path, fields such as subject public key, the signature algorithm, key usage, extended key usage, etc. need to conform to the algorithm constraints in place on this engine.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `chain` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate.html#)!\>!:the peer certificate chain |
| `authType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the key exchange algorithm used |
| `engine` | [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine)!:the engine used for this connection. This parameter can be null, which indicates that implementations need not check the ssl parameters |
| --- | --- |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if null or zero-length array is passed in for the`chain`parameter or if null or zero-length string is passed in for the`authType`parameter |
| `java.security.cert.CertificateException` | if the certificate chain is not trusted by this TrustManager |

**See Also**

- [javax.net.ssl.SSLParameters#getEndpointIdentificationAlgorithm](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getEndpointIdentificationAlgorithm())
- [javax.net.ssl.SSLParameters#setEndpointIdentificationAlgorithm(String)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setEndpointIdentificationAlgorithm(kotlin.String))
- [javax.net.ssl.SSLParameters#getAlgorithmConstraints](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#getAlgorithmConstraints())
