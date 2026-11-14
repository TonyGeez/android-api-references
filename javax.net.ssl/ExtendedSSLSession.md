# ExtendedSSLSession

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExtendedSSLSession

```
abstract class ExtendedSSLSession : SSLSession
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.net.ssl.ExtendedSSLSession](../javax/net/ssl/ExtendedSSLSession.md) |

Extends the`SSLSession`interface to support additional session attributes.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------|---|
| [ExtendedSSLSession](../javax/net/ssl/ExtendedSSLSession.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getLocalSupportedSignatureAlgorithms](../javax/net/ssl/ExtendedSSLSession.md))`()` Obtains an array of supported signature algorithms that the local side is willing to use. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getPeerSupportedSignatureAlgorithms](../javax/net/ssl/ExtendedSSLSession.md))`()` Obtains an array of supported signature algorithms that the peer is able to use. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SNIServerName](../javax/net/ssl/SNIServerName.md)!\>! | [getRequestedServerNames](../javax/net/ssl/ExtendedSSLSession.md))`()` Obtains a [List](../java/util/List.md) containing all [SNIServerName](../javax/net/ssl/SNIServerName.md) s of the requested Server Name Indication (SNI) extension. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [SSLSession](../javax/net/ssl/SSLSession.md) |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getApplicationBufferSize](../javax/net/ssl/SSLSession.md))`()` <br /> Gets the current size of the largest application data that is expected when using this session. `SSLEngine`application data buffers must be large enough to hold the application data from any inbound network application data packet received. Typically, outbound application data buffers can be of any size. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCipherSuite](../javax/net/ssl/SSLSession.md))`()` <br /> Returns the name of the SSL cipher suite which is used for all connections in the session. This defines the level of protection provided to the data sent on the connection, including the kind of encryption used and most aspects of how authentication is done. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCreationTime](../javax/net/ssl/SSLSession.md))`()` <br /> Returns the time at which this Session representation was created, in milliseconds since midnight, January 1, 1970 UTC. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getId](../javax/net/ssl/SSLSession.md))`()` <br /> Returns the identifier assigned to this Session. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLastAccessedTime](../javax/net/ssl/SSLSession.md))`()` <br /> Returns the last time this Session representation was accessed by the session level infrastructure, in milliseconds since midnight, January 1, 1970 UTC. Access indicates a new connection being established using session data. Application level operations, such as getting or setting a value associated with the session, are not reflected in this access time. This information is particularly useful in session management policies. For example, a session manager thread could leave all sessions in a given context which haven't been used in a long time; or, the sessions might be sorted according to age to optimize some task. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Certificate](../java/security/cert/Certificate.md)!>! | [getLocalCertificates](../javax/net/ssl/SSLSession.md))`()` <br /> Returns the certificate(s) that were sent to the peer during handshaking. Note: This method is useful only when using certificate-based cipher suites. When multiple certificates are available for use in a handshake, the implementation chooses what it considers the "best" certificate chain available, and transmits that to the other side. This method allows the caller to know which certificate chain was actually used. <br /> | | [Principal](../java/security/Principal.md)! | [getLocalPrincipal](../javax/net/ssl/SSLSession.md))`()` <br /> Returns the principal that was sent to the peer during handshaking. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPacketBufferSize](../javax/net/ssl/SSLSession.md))`()` <br /> Gets the current size of the largest SSL/TLS packet that is expected when using this session. A`SSLEngine`using this session may generate SSL/TLS packets of any size up to and including the value returned by this method. All`SSLEngine`network buffers should be sized at least this large to avoid insufficient space problems when performing`wrap`and`unwrap`calls. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](../javax/security/cert/X509Certificate.md)!>! | [getPeerCertificateChain](../javax/net/ssl/SSLSession.md))`()` <br /> Returns the identity of the peer which was identified as part of defining the session. Note: This method can be used only when using certificate-based cipher suites; using it with non-certificate-based cipher suites, such as Kerberos, will throw an SSLPeerUnverifiedException. *Note: this method exists for compatibility with previous releases. New applications should use [getPeerCertificates](../javax/net/ssl/SSLSession.md))instead.* <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Certificate](../java/security/cert/Certificate.md)!>! | [getPeerCertificates](../javax/net/ssl/SSLSession.md))`()` <br /> Returns the identity of the peer which was established as part of defining the session. Note: This method can be used only when using certificate-based cipher suites; using it with non-certificate-based cipher suites, such as Kerberos, will throw an SSLPeerUnverifiedException. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPeerHost](../javax/net/ssl/SSLSession.md))`()` <br /> Returns the host name of the peer in this session. For the server, this is the client's host; and for the client, it is the server's host. The name may not be a fully qualified host name or even a host name at all as it may represent a string encoding of the peer's network address. If such a name is desired, it might be resolved through a name service based on the value returned by this method. This value is not authenticated and should not be relied upon. It is mainly used as a hint for`SSLSession`caching strategies. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPeerPort](../javax/net/ssl/SSLSession.md))`()` <br /> Returns the port number of the peer in this session. For the server, this is the client's port number; and for the client, it is the server's port number. This value is not authenticated and should not be relied upon. It is mainly used as a hint for`SSLSession`caching strategies. <br /> | | [Principal](../java/security/Principal.md)! | [getPeerPrincipal](../javax/net/ssl/SSLSession.md))`()` <br /> Returns the identity of the peer which was established as part of defining the session. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getProtocol](../javax/net/ssl/SSLSession.md))`()` <br /> Returns the standard name of the protocol used for all connections in the session. This defines the protocol used in the connection. <br /> | | [SSLSessionContext](../javax/net/ssl/SSLSessionContext.md)! | [getSessionContext](../javax/net/ssl/SSLSession.md))`()` <br /> Returns the context in which this session is bound. This context may be unavailable in some environments, in which case this method returns null. If the context is available and there is a security manager installed, the caller may require permission to access it or a security exception may be thrown. In a Java environment, the security manager's`checkPermission`method is called with a`SSLPermission("getSSLSessionContext")`permission. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getValue](../javax/net/ssl/SSLSession.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Returns the object bound to the given name in the session's application layer data. Returns null if there is no such binding. For security reasons, the same named values may not be visible across different access control contexts. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getValueNames](../javax/net/ssl/SSLSession.md))`()` <br /> Returns an array of the names of all the application layer data objects bound into the Session. For security reasons, the same named values may not be visible across different access control contexts. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidate](../javax/net/ssl/SSLSession.md))`()` <br /> Invalidates the session. Future connections will not be able to resume or join this session. However, any existing connection using this session can continue to use the session until the connection is closed. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValid](../javax/net/ssl/SSLSession.md))`()` <br /> Returns whether this session is valid and available for resuming or joining. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putValue](../javax/net/ssl/SSLSession.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Binds the specified`value`object into the session's application layer data with the given`name`. Any existing binding using the same`name`is replaced. If the new (or existing)`value`implements the`SSLSessionBindingListener`interface, the object represented by`value`is notified appropriately. For security reasons, the same named values may not be visible across different access control contexts. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeValue](../javax/net/ssl/SSLSession.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Removes the object bound to the given name in the session's application layer data. Does nothing if there is no object bound to the given name. If the bound existing object implements the`SessionBindingListener`interface, it is notified appropriately. For security reasons, the same named values may not be visible across different access control contexts. <br /> | ||

## Public constructors

### ExtendedSSLSession

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ExtendedSSLSession()
```

## Public methods

### getLocalSupportedSignatureAlgorithms

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLocalSupportedSignatureAlgorithms(): Array<String!>!
```

Obtains an array of supported signature algorithms that the local side is willing to use.

Note: this method is used to indicate to the peer which signature algorithms may be used for digital signatures in TLS 1.2. It is not meaningful for TLS versions prior to 1.2.

The signature algorithm name must be a standard Java Security name (such as "SHA1withRSA", "SHA256withECDSA", and so on). See Appendix A in the [Java Cryptography Architecture API Specification \& Reference](https://docs.oracle.com/javase/8/docs/technotes/guides/security/crypto/CryptoSpec.html#AppA) for information about standard algorithm names.

Note: the local supported signature algorithms should conform to the algorithm constraints specified by [getAlgorithmConstraints()](../javax/net/ssl/SSLParameters.md))method in`SSLParameters`.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | An array of supported signature algorithms, in descending order of preference. The return value is an empty array if no signature algorithm is supported. |

**See Also**

- [javax.net.ssl.SSLParameters#getAlgorithmConstraints](../javax/net/ssl/SSLParameters.md)) 

### getPeerSupportedSignatureAlgorithms

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPeerSupportedSignatureAlgorithms(): Array<String!>!
```

Obtains an array of supported signature algorithms that the peer is able to use.

Note: this method is used to indicate to the local side which signature algorithms may be used for digital signatures in TLS 1.2. It is not meaningful for TLS versions prior to 1.2.

The signature algorithm name must be a standard Java Security name (such as "SHA1withRSA", "SHA256withECDSA", and so on). See Appendix A in the [Java Cryptography Architecture API Specification \& Reference](https://docs.oracle.com/javase/8/docs/technotes/guides/security/crypto/CryptoSpec.html#AppA) for information about standard algorithm names.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | An array of supported signature algorithms, in descending order of preference. The return value is an empty array if the peer has not sent the supported signature algorithms. |

**See Also**

- [javax.net.ssl.X509KeyManager](../javax/net/ssl/X509KeyManager.md)
- [javax.net.ssl.X509ExtendedKeyManager](../javax/net/ssl/X509ExtendedKeyManager.md) 

### getRequestedServerNames

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRequestedServerNames(): MutableList<SNIServerName!>!
```

Obtains a [List](../java/util/List.md) containing all [SNIServerName](../javax/net/ssl/SNIServerName.md) s of the requested Server Name Indication (SNI) extension.

In server mode, unless the return [List](../java/util/List.md) is empty, the server should use the requested server names to guide its selection of an appropriate authentication certificate, and/or other aspects of security policy.

In client mode, unless the return [List](../java/util/List.md) is empty, the client should use the requested server names to guide its endpoint identification of the peer's identity, and/or other aspects of security policy.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [SNIServerName](../javax/net/ssl/SNIServerName.md)!>! | a non-null immutable list of [SNIServerName](../javax/net/ssl/SNIServerName.md) s of the requested server name indications. The returned list may be empty if no server name indications were requested. |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the underlying provider does not implement the operation |

**See Also**

- [javax.net.ssl.SNIServerName](../javax/net/ssl/SNIServerName.md)
- [javax.net.ssl.X509ExtendedTrustManager](../javax/net/ssl/X509ExtendedTrustManager.md)
- [javax.net.ssl.X509ExtendedKeyManager](../javax/net/ssl/X509ExtendedKeyManager.md)
