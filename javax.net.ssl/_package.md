# javax.net.ssl

# javax.net.ssl

## Interfaces

| [HandshakeCompletedListener](HandshakeCompletedListener.md) | This interface is implemented by any class which wants to receive notifications about the completion of an SSL protocol handshake on a given SSL connection. |
| --- | --- |
| [HostnameVerifier](HostnameVerifier.md) | This class is the base interface for hostname verification. |
| [KeyManager](KeyManager.md) | This is the base interface for JSSE key managers. |
| [ManagerFactoryParameters](ManagerFactoryParameters.md) | This class is the base interface for providing algorithm-specific information to a KeyManagerFactory or TrustManagerFactory. |
| --- | --- |
| [SSLSession](SSLSession.md) | In SSL, sessions are used to describe an ongoing relationship between two entities. |
| [SSLSessionBindingListener](SSLSessionBindingListener.md) | This interface is implemented by objects which want to know when they are being bound or unbound from a SSLSession. |
| [SSLSessionContext](SSLSessionContext.md) | A represents a set of`SSLSession`s associated with a single entity. |
| --- | --- |
| [TrustManager](TrustManager.md) | This is the base interface for JSSE trust managers. |
| [X509KeyManager](X509KeyManager.md) | Instances of this interface manage which X509 certificate-based key pairs are used to authenticate the local side of a secure socket. |
| [X509TrustManager](X509TrustManager.md) | Instance of this interface manage which X509 certificates may be used to authenticate the remote side of a secure socket. |
| --- | --- |

## Classes

| [CertPathTrustManagerParameters](CertPathTrustManagerParameters.md) | A wrapper for CertPathParameters. |
| --- | --- |
| [ExtendedSSLSession](ExtendedSSLSession.md) | Extends the`SSLSession`interface to support additional session attributes. |
| [HandshakeCompletedEvent](HandshakeCompletedEvent.md) | This event indicates that an SSL handshake completed on a given SSL connection. |
| [HttpsURLConnection](HttpsURLConnection.md) | `HttpsURLConnection`extends`HttpURLConnection`with support for https-specific features. |
| --- | --- |
| [KeyManagerFactory](KeyManagerFactory.md) | This class acts as a factory for key managers based on a source of key material. |
| [KeyManagerFactorySpi](KeyManagerFactorySpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`KeyManagerFactory`class. |
| [KeyStoreBuilderParameters](KeyStoreBuilderParameters.md) | A parameters object for X509KeyManagers that encapsulates a List of KeyStore. |
| --- | --- |
| [SNIHostName](SNIHostName.md) | Instances of this class represent a server name of type [host_name](StandardConstants.md) in a Server Name Indication (SNI) extension. |
| [SNIMatcher](SNIMatcher.md) | Instances of this class represent a matcher that performs match operations on an [SNIServerName](SNIServerName.md) instance. |
| [SNIServerName](SNIServerName.md) | Instances of this class represent a server name in a Server Name Indication (SNI) extension. |
| --- | --- |
| [SSLContext](SSLContext.md) | Instances of this class represent a secure socket protocol implementation which acts as a factory for secure socket factories or`SSLEngine`s. |
| [SSLContextSpi](SSLContextSpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`SSLContext`class. |
| [SSLEngine](SSLEngine.md) | A class which enables secure communications using protocols such as the Secure Sockets Layer (SSL) or [IETF RFC 2246 "Transport Layer Security" (TLS)](http://www.ietf.org/rfc/rfc2246.txt) protocols, but is transport independent. |
| --- | --- |
| [SSLEngineResult](SSLEngineResult.md) | An encapsulation of the result state produced by`SSLEngine`I/O calls. |
| [SSLParameters](SSLParameters.md) | Encapsulates parameters for an SSL/TLS connection. |
| [SSLPermission](SSLPermission.md) | Legacy security code; do not use. |
| --- | --- |
| [SSLServerSocket](SSLServerSocket.md) | This class extends`ServerSocket`s and provides secure server sockets using protocols such as the Secure Sockets Layer (SSL) or Transport Layer Security (TLS) protocols. |
| [SSLServerSocketFactory](SSLServerSocketFactory.md) | `SSLServerSocketFactory`s create`SSLServerSocket`s. |
| [SSLSessionBindingEvent](SSLSessionBindingEvent.md) | This event is propagated to a SSLSessionBindingListener. |
| --- | --- |
| [SSLSocket](SSLSocket.md) | This class extends`Socket`s and provides secure socket using protocols such as the "Secure Sockets Layer" (SSL) or IETF "Transport Layer Security" (TLS) protocols. |
| [SSLSocketFactory](SSLSocketFactory.md) | `SSLSocketFactory`s create`SSLSocket`s. |
| [StandardConstants](StandardConstants.md) | Standard constants definitions |
| --- | --- |
| [TrustManagerFactory](TrustManagerFactory.md) | This class acts as a factory for trust managers based on a source of trust material. |
| [TrustManagerFactorySpi](TrustManagerFactorySpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`TrustManagerFactory`class. |
| [X509ExtendedKeyManager](X509ExtendedKeyManager.md) | Abstract class that provides for extension of the X509KeyManager interface. |
| --- | --- |
| [X509ExtendedTrustManager](X509ExtendedTrustManager.md) | Extensions to the`X509TrustManager`interface to support SSL/TLS connection sensitive trust management. |

## Exceptions

| [SSLException](SSLException.md) | Indicates some kind of error detected by an SSL subsystem. |
| --- | --- |
| [SSLHandshakeException](SSLHandshakeException.md) | Indicates that the client and server could not negotiate the desired level of security. |
| [SSLKeyException](SSLKeyException.md) | Reports a bad SSL key. |
| [SSLPeerUnverifiedException](SSLPeerUnverifiedException.md) | Indicates that the peer's identity has not been verified. |
| --- | --- |
| [SSLProtocolException](SSLProtocolException.md) | Reports an error in the operation of the SSL protocol. |
