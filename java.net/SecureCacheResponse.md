# SecureCacheResponse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SecureCacheResponse

```
abstract class SecureCacheResponse : CacheResponse
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.net.CacheResponse](https://developer.android.com/reference/kotlin/java/net/CacheResponse) ||
| | ↳ | [java.net.SecureCacheResponse](https://developer.android.com/reference/kotlin/java/net/SecureCacheResponse#) |

Represents a cache response originally retrieved through secure means, such as TLS.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------|---|
| [SecureCacheResponse](https://developer.android.com/reference/kotlin/java/net/SecureCacheResponse#SecureCacheResponse())`()` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCipherSuite](https://developer.android.com/reference/kotlin/java/net/SecureCacheResponse#getCipherSuite())`()` Returns the cipher suite in use on the original connection that retrieved the network resource. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate.html#)!\>! | [getLocalCertificateChain](https://developer.android.com/reference/kotlin/java/net/SecureCacheResponse#getLocalCertificateChain())`()` Returns the certificate chain that were sent to the server during handshaking of the original connection that retrieved the network resource. |
| abstract [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)! | [getLocalPrincipal](https://developer.android.com/reference/kotlin/java/net/SecureCacheResponse#getLocalPrincipal())`()` Returns the principal that was sent to the server during handshaking in the original connection that retrieved the network resource. |
| abstract [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)! | [getPeerPrincipal](https://developer.android.com/reference/kotlin/java/net/SecureCacheResponse#getPeerPrincipal())`()` Returns the server's principal which was established as part of defining the session during the original connection that retrieved the network resource. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate.html#)!\>! | [getServerCertificateChain](https://developer.android.com/reference/kotlin/java/net/SecureCacheResponse#getServerCertificateChain())`()` Returns the server's certificate chain, which was established as part of defining the session in the original connection that retrieved the network resource, from cache. |

| Inherited functions ||
|---|---|
| From class [CacheResponse](https://developer.android.com/reference/kotlin/java/net/CacheResponse) |------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------| | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | [getBody](https://developer.android.com/reference/kotlin/java/net/CacheResponse#getBody())`()` <br /> Returns the response body as an InputStream. <br /> | | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!>! | [getHeaders](https://developer.android.com/reference/kotlin/java/net/CacheResponse#getHeaders())`()` <br /> Returns the response headers as a Map. <br /> | ||

## Public constructors

### SecureCacheResponse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SecureCacheResponse()
```

## Public methods

### getCipherSuite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCipherSuite(): String!
```

Returns the cipher suite in use on the original connection that retrieved the network resource.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a string representing the cipher suite |

### getLocalCertificateChain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLocalCertificateChain(): MutableList<Certificate!>!
```

Returns the certificate chain that were sent to the server during handshaking of the original connection that retrieved the network resource. Note: This method is useful only when using certificate-based cipher suites.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate.html#)!>! | an immutable List of Certificate representing the certificate chain that was sent to the server. If no certificate chain was sent, null will be returned. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/SecureCacheResponse#getLocalPrincipal()> 

### getLocalPrincipal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLocalPrincipal(): Principal!
```

Returns the principal that was sent to the server during handshaking in the original connection that retrieved the network resource.

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)! | the principal sent to the server. Returns an X500Principal of the end-entity certificate for X509-based cipher suites, and KerberosPrincipal for Kerberos cipher suites. If no principal was sent, then null is returned. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/SecureCacheResponse#getLocalCertificateChain()>
- <https://developer.android.com/reference/kotlin/java/net/SecureCacheResponse#getPeerPrincipal()> 

### getPeerPrincipal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPeerPrincipal(): Principal!
```

Returns the server's principal which was established as part of defining the session during the original connection that retrieved the network resource.

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)! | the server's principal. Returns an X500Principal of the end-entity certiticate for X509-based cipher suites, and KerberosPrincipal for Kerberos cipher suites. |

| Exceptions ||
|--------------------------------------------|-------------------------------|
| `javax.net.ssl.SSLPeerUnverifiedException` | if the peer was not verified. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/SecureCacheResponse#getServerCertificateChain()>
- <https://developer.android.com/reference/kotlin/java/net/SecureCacheResponse#getLocalPrincipal()> 

### getServerCertificateChain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getServerCertificateChain(): MutableList<Certificate!>!
```

Returns the server's certificate chain, which was established as part of defining the session in the original connection that retrieved the network resource, from cache. Note: This method can be used only when using certificate-based cipher suites; using it with non-certificate-based cipher suites, such as Kerberos, will throw an SSLPeerUnverifiedException.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate.html#)!>! | an immutable List of Certificate representing the server's certificate chain. |

| Exceptions ||
|--------------------------------------------|------------------------------|
| `javax.net.ssl.SSLPeerUnverifiedException` | if the peer is not verified. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/SecureCacheResponse#getPeerPrincipal()>
