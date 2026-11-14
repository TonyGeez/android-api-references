# javax.net.ssl

# javax.net.ssl

## Interfaces

| [HandshakeCompletedListener](https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedListener) | This interface is implemented by any class which wants to receive notifications about the completion of an SSL protocol handshake on a given SSL connection. |
| --- | --- |
| [HostnameVerifier](https://developer.android.com/reference/kotlin/javax/net/ssl/HostnameVerifier) | This class is the base interface for hostname verification. |
| [KeyManager](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManager) | This is the base interface for JSSE key managers. |
| [ManagerFactoryParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/ManagerFactoryParameters) | This class is the base interface for providing algorithm-specific information to a KeyManagerFactory or TrustManagerFactory. |
| --- | --- |
| [SSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession) | In SSL, sessions are used to describe an ongoing relationship between two entities. |
| [SSLSessionBindingListener](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionBindingListener) | This interface is implemented by objects which want to know when they are being bound or unbound from a SSLSession. |
| [SSLSessionContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionContext) | A represents a set of`SSLSession`s associated with a single entity. |
| --- | --- |
| [TrustManager](https://developer.android.com/reference/kotlin/javax/net/ssl/TrustManager) | This is the base interface for JSSE trust managers. |
| [X509KeyManager](https://developer.android.com/reference/kotlin/javax/net/ssl/X509KeyManager) | Instances of this interface manage which X509 certificate-based key pairs are used to authenticate the local side of a secure socket. |
| [X509TrustManager](https://developer.android.com/reference/kotlin/javax/net/ssl/X509TrustManager) | Instance of this interface manage which X509 certificates may be used to authenticate the remote side of a secure socket. |
| --- | --- |

## Classes

| [CertPathTrustManagerParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/CertPathTrustManagerParameters) | A wrapper for CertPathParameters. |
| --- | --- |
| [ExtendedSSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/ExtendedSSLSession) | Extends the`SSLSession`interface to support additional session attributes. |
| [HandshakeCompletedEvent](https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedEvent) | This event indicates that an SSL handshake completed on a given SSL connection. |
| [HttpsURLConnection](https://developer.android.com/reference/kotlin/javax/net/ssl/HttpsURLConnection) | `HttpsURLConnection`extends`HttpURLConnection`with support for https-specific features. |
| --- | --- |
| [KeyManagerFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManagerFactory) | This class acts as a factory for key managers based on a source of key material. |
| [KeyManagerFactorySpi](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyManagerFactorySpi) | This class defines the*Service Provider Interface* (**SPI** ) for the`KeyManagerFactory`class. |
| [KeyStoreBuilderParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/KeyStoreBuilderParameters) | A parameters object for X509KeyManagers that encapsulates a List of KeyStore. |
| --- | --- |
| [SNIHostName](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIHostName) | Instances of this class represent a server name of type [host_name](https://developer.android.com/reference/kotlin/javax/net/ssl/StandardConstants#SNI_HOST_NAME:kotlin.Int) in a Server Name Indication (SNI) extension. |
| [SNIMatcher](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIMatcher) | Instances of this class represent a matcher that performs match operations on an [SNIServerName](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName) instance. |
| [SNIServerName](https://developer.android.com/reference/kotlin/javax/net/ssl/SNIServerName) | Instances of this class represent a server name in a Server Name Indication (SNI) extension. |
| --- | --- |
| [SSLContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext) | Instances of this class represent a secure socket protocol implementation which acts as a factory for secure socket factories or`SSLEngine`s. |
| [SSLContextSpi](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContextSpi) | This class defines the*Service Provider Interface* (**SPI** ) for the`SSLContext`class. |
| [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine) | A class which enables secure communications using protocols such as the Secure Sockets Layer (SSL) or [IETF RFC 2246 "Transport Layer Security" (TLS)](http://www.ietf.org/rfc/rfc2246.txt) protocols, but is transport independent. |
| --- | --- |
| [SSLEngineResult](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult) | An encapsulation of the result state produced by`SSLEngine`I/O calls. |
| [SSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters) | Encapsulates parameters for an SSL/TLS connection. |
| [SSLPermission](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLPermission) | Legacy security code; do not use. |
| --- | --- |
| [SSLServerSocket](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocket) | This class extends`ServerSocket`s and provides secure server sockets using protocols such as the Secure Sockets Layer (SSL) or Transport Layer Security (TLS) protocols. |
| [SSLServerSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocketFactory) | `SSLServerSocketFactory`s create`SSLServerSocket`s. |
| [SSLSessionBindingEvent](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionBindingEvent) | This event is propagated to a SSLSessionBindingListener. |
| --- | --- |
| [SSLSocket](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket) | This class extends`Socket`s and provides secure socket using protocols such as the "Secure Sockets Layer" (SSL) or IETF "Transport Layer Security" (TLS) protocols. |
| [SSLSocketFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory) | `SSLSocketFactory`s create`SSLSocket`s. |
| [StandardConstants](https://developer.android.com/reference/kotlin/javax/net/ssl/StandardConstants) | Standard constants definitions |
| --- | --- |
| [TrustManagerFactory](https://developer.android.com/reference/kotlin/javax/net/ssl/TrustManagerFactory) | This class acts as a factory for trust managers based on a source of trust material. |
| [TrustManagerFactorySpi](https://developer.android.com/reference/kotlin/javax/net/ssl/TrustManagerFactorySpi) | This class defines the*Service Provider Interface* (**SPI** ) for the`TrustManagerFactory`class. |
| [X509ExtendedKeyManager](https://developer.android.com/reference/kotlin/javax/net/ssl/X509ExtendedKeyManager) | Abstract class that provides for extension of the X509KeyManager interface. |
| --- | --- |
| [X509ExtendedTrustManager](https://developer.android.com/reference/kotlin/javax/net/ssl/X509ExtendedTrustManager) | Extensions to the`X509TrustManager`interface to support SSL/TLS connection sensitive trust management. |

## Exceptions

| [SSLException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLException) | Indicates some kind of error detected by an SSL subsystem. |
| --- | --- |
| [SSLHandshakeException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLHandshakeException) | Indicates that the client and server could not negotiate the desired level of security. |
| [SSLKeyException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLKeyException) | Reports a bad SSL key. |
| [SSLPeerUnverifiedException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLPeerUnverifiedException) | Indicates that the peer's identity has not been verified. |
| --- | --- |
| [SSLProtocolException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLProtocolException) | Reports an error in the operation of the SSL protocol. |
