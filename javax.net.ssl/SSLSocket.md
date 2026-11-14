Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLSocket

```
abstract class SSLSocket : Socket
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.net.Socket](../java.net/Socket.md) ||
| | ↳ | [javax.net.ssl.SSLSocket](SSLSocket.md) |

This class extends `Socket`s and provides secure socket using protocols such as the "Secure Sockets Layer" (SSL) or IETF "Transport Layer Security" (TLS) protocols.

Such sockets are normal stream sockets, but they add a layer of security protections over the underlying network transport protocol, such as TCP. Those protections include:

- *Integrity Protection*. SSL protects against modification of messages by an active wiretapper.
- *Authentication*. In most modes, SSL provides peer authentication. Servers are usually authenticated, and clients may be authenticated as requested by servers.
- *Confidentiality (Privacy Protection)*. In most modes, SSL encrypts data being sent between client and server. This protects the confidentiality of data, so that passive wiretappers won't see sensitive data such as financial information or personal information of many kinds.

These kinds of protection are specified by a "cipher suite", which is a combination of cryptographic algorithms used by a given SSL connection. During the negotiation process, the two endpoints must agree on a ciphersuite that is available in both environments. If there is no such suite in common, no SSL connection can be established, and no data can be exchanged.

The cipher suite used is established by a negotiation process called "handshaking". The goal of this process is to create or rejoin a "session", which may protect many connections over time. After handshaking has completed, you can access session attributes by using the *getSession* method. The initial handshake on this connection can be initiated in one of three ways:

- calling `startHandshake` which explicitly begins handshakes, or
- any attempt to read or write application data on this socket causes an implicit handshake, or
- a call to `getSession` tries to set up a session if there is no currently valid session, and an implicit handshake is done.

If handshaking fails for any reason, the `SSLSocket` is closed, and no further communications can be done.

There are two groups of cipher suites which you will need to know about when managing cipher suites:

- *Supported* cipher suites: all the suites which are supported by the SSL implementation. This list is reported using *getSupportedCipherSuites*.
- *Enabled* cipher suites, which may be fewer than the full set of supported suites. This group is set using the *setEnabledCipherSuites* method, and queried using the *getEnabledCipherSuites* method. Initially, a default set of cipher suites will be enabled on a new socket that represents the minimum suggested configuration.

Implementation defaults require that only cipher suites which authenticate servers and provide confidentiality be enabled by default. Only if both sides explicitly agree to unauthenticated and/or non-private (unencrypted) communications will such a ciphersuite be selected.

When `SSLSocket`s are first created, no handshaking is done so that applications may first set their communication preferences: what cipher suites to use, whether the socket should be in client or server mode, etc. However, security is always provided by the time that application data is sent over the connection.

You may register to receive event notification of handshake completion. This involves the use of two additional classes. *HandshakeCompletedEvent* objects are passed to *HandshakeCompletedListener* instances, which are registered by users of this API. `SSLSocket`s are created by `SSLSocketFactory`s, or by `accept`ing a connection from a `SSLServerSocket`.

A SSL socket must choose to operate in the client or server mode. This will determine who begins the handshaking process, as well as which messages should be sent by each party. Each connection must have one client and one server, or handshaking will not progress properly. Once the initial handshaking has started, a socket can not switch between client and server modes, even when performing renegotiations.

### Default configuration for different Android versions

`SSLSocket` instances obtained from default `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory`, `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLServerSocketFactory`, and `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext` are configured as follows:

#### Protocols

Client socket:

| Protocol | Supported (API Levels) | Enabled by default (API Levels) |
|---|---|---|
| SSLv3 | 1--25 | 1--22 |
| TLSv1 | 1+ | 1+ |
| TLSv1.1 | 16+ | 20+ |
| --- | --- | --- |
| TLSv1.2 | 16+ | 20+ |
| TLSv1.3 | 29+ | 29+ |

Server socket:

| Protocol | Supported (API Levels) | Enabled by default (API Levels) |
|---|---|---|
| SSLv3 | 1--25 | 1--22 |
| TLSv1 | 1+ | 1+ |
| TLSv1.1 | 16+ | 16+ |
| --- | --- | --- |
| TLSv1.2 | 16+ | 16+ |
| TLSv1.3 | 29+ | 29+ |

#### Cipher suites

Methods that operate with cipher suite names (for example, `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getSupportedCipherSuites()`, `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setEnabledCipherSuites(kotlin.Array)`) have used standard names for cipher suites since API Level 9, as listed in the table below. Prior to API Level 9, non-standard (OpenSSL) names had been used (see the table following this table).

| Cipher suite | Supported (API Levels) | Enabled by default (API Levels) |
|---|---|---|
| SSL_DHE_DSS_EXPORT_WITH_DES40_CBC_SHA | 9-22 | 9-19 |
| SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA | 9-22 | 9-19 |
| SSL_DHE_DSS_WITH_DES_CBC_SHA | 9-22 | 9-19 |
| --- | --- | --- |
| SSL_DHE_RSA_EXPORT_WITH_DES40_CBC_SHA | 9-22 | 9-19 |
| SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA | 9-22 | 9-19 |
| SSL_DHE_RSA_WITH_DES_CBC_SHA | 9-22 | 9-19 |
| --- | --- | --- |
| SSL_DH_anon_EXPORT_WITH_DES40_CBC_SHA | 9-22 | |
| SSL_DH_anon_EXPORT_WITH_RC4_40_MD5 | 9-22 | |
| SSL_DH_anon_WITH_3DES_EDE_CBC_SHA | 9-22 | |
| --- | --- | --- |
| SSL_DH_anon_WITH_DES_CBC_SHA | 9-22 | |
| SSL_DH_anon_WITH_RC4_128_MD5 | 9-22 | |
| SSL_RSA_EXPORT_WITH_DES40_CBC_SHA | 9-22 | 9-19 |
| --- | --- | --- |
| SSL_RSA_EXPORT_WITH_RC4_40_MD5 | 9-22 | 9-19 |
| SSL_RSA_WITH_3DES_EDE_CBC_SHA | 9+ | 9-19 |
| SSL_RSA_WITH_DES_CBC_SHA | 9-22 | 9-19 |
| --- | --- | --- |
| SSL_RSA_WITH_NULL_MD5 | 9-22 | |
| SSL_RSA_WITH_NULL_SHA | 9-22 | |
| SSL_RSA_WITH_RC4_128_MD5 | 9-25 | 9-19 |
| --- | --- | --- |
| SSL_RSA_WITH_RC4_128_SHA | 9-25 | 9-23 |
| TLS_AES_128_GCM_SHA256 | 29+ | 29+ |
| TLS_AES_256_GCM_SHA384 | 29+ | 29+ |
| --- | --- | --- |
| TLS_CHACHA20_POLY1305_SHA256 | 29+ | 29+ |
| TLS_DHE_DSS_WITH_AES_128_CBC_SHA | 9-22 | 9-22 |
| TLS_DHE_DSS_WITH_AES_128_CBC_SHA256 | 20-22 | |
| --- | --- | --- |
| TLS_DHE_DSS_WITH_AES_128_GCM_SHA256 | 20-22 | |
| TLS_DHE_DSS_WITH_AES_256_CBC_SHA | 9-22 | 11-22 |
| TLS_DHE_DSS_WITH_AES_256_CBC_SHA256 | 20-22 | |
| --- | --- | --- |
| TLS_DHE_DSS_WITH_AES_256_GCM_SHA384 | 20-22 | |
| TLS_DHE_RSA_WITH_AES_128_CBC_SHA | 9-25 | 9-25 |
| TLS_DHE_RSA_WITH_AES_128_CBC_SHA256 | 20-25 | |
| --- | --- | --- |
| TLS_DHE_RSA_WITH_AES_128_GCM_SHA256 | 20-25 | 20-25 |
| TLS_DHE_RSA_WITH_AES_256_CBC_SHA | 9-25 | 11-25 |
| TLS_DHE_RSA_WITH_AES_256_CBC_SHA256 | 20-25 | |
| --- | --- | --- |
| TLS_DHE_RSA_WITH_AES_256_GCM_SHA384 | 20-25 | 20-25 |
| TLS_DH_anon_WITH_AES_128_CBC_SHA | 9-22 | |
| TLS_DH_anon_WITH_AES_128_CBC_SHA256 | 20-22 | |
| --- | --- | --- |
| TLS_DH_anon_WITH_AES_128_GCM_SHA256 | 20-22 | |
| TLS_DH_anon_WITH_AES_256_CBC_SHA | 9-22 | |
| TLS_DH_anon_WITH_AES_256_CBC_SHA256 | 20-22 | |
| --- | --- | --- |
| TLS_DH_anon_WITH_AES_256_GCM_SHA384 | 20-22 | |
| TLS_ECDHE_ECDSA_WITH_3DES_EDE_CBC_SHA | 11-22 | 11-19 |
| TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA | 11+ | 11+ |
| --- | --- | --- |
| TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA256 | 20-28 | |
| TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256 | 20+ | 20+ |
| TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA | 11+ | 11+ |
| --- | --- | --- |
| TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA384 | 20-28 | |
| TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384 | 20+ | 20+ |
| TLS_ECDHE_ECDSA_WITH_CHACHA20_POLY1305_SHA256 | 24+ | 24+ |
| --- | --- | --- |
| TLS_ECDHE_ECDSA_WITH_NULL_SHA | 11-22 | |
| TLS_ECDHE_ECDSA_WITH_RC4_128_SHA | 11-25 | 11-23 |
| TLS_ECDHE_PSK_WITH_AES_128_CBC_SHA | 21+ | 21+ |
| --- | --- | --- |
| TLS_ECDHE_PSK_WITH_AES_256_CBC_SHA | 21+ | 21+ |
| TLS_ECDHE_PSK_WITH_CHACHA20_POLY1305_SHA256 | 24+ | 24+ |
| TLS_ECDHE_RSA_WITH_3DES_EDE_CBC_SHA | 11-22 | 11-19 |
| --- | --- | --- |
| TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA | 11+ | 11+ |
| TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256 | 20-28 | |
| TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256 | 20+ | 20+ |
| --- | --- | --- |
| TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA | 11+ | 11+ |
| TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384 | 20-28 | |
| TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384 | 20+ | 20+ |
| --- | --- | --- |
| TLS_ECDHE_RSA_WITH_CHACHA20_POLY1305_SHA256 | 24+ | 24+ |
| TLS_ECDHE_RSA_WITH_NULL_SHA | 11-22 | |
| TLS_ECDHE_RSA_WITH_RC4_128_SHA | 11-25 | 11-23 |
| --- | --- | --- |
| TLS_ECDH_ECDSA_WITH_3DES_EDE_CBC_SHA | 11-22 | 11-19 |
| TLS_ECDH_ECDSA_WITH_AES_128_CBC_SHA | 11-22 | 11-19 |
| TLS_ECDH_ECDSA_WITH_AES_128_CBC_SHA256 | 20-22 | |
| --- | --- | --- |
| TLS_ECDH_ECDSA_WITH_AES_128_GCM_SHA256 | 20-22 | |
| TLS_ECDH_ECDSA_WITH_AES_256_CBC_SHA | 11-22 | 11-19 |
| TLS_ECDH_ECDSA_WITH_AES_256_CBC_SHA384 | 20-22 | |
| --- | --- | --- |
| TLS_ECDH_ECDSA_WITH_AES_256_GCM_SHA384 | 20-22 | |
| TLS_ECDH_ECDSA_WITH_NULL_SHA | 11-22 | |
| TLS_ECDH_ECDSA_WITH_RC4_128_SHA | 11-22 | 11-19 |
| --- | --- | --- |
| TLS_ECDH_RSA_WITH_3DES_EDE_CBC_SHA | 11-22 | 11-19 |
| TLS_ECDH_RSA_WITH_AES_128_CBC_SHA | 11-22 | 11-19 |
| TLS_ECDH_RSA_WITH_AES_128_CBC_SHA256 | 20-22 | |
| --- | --- | --- |
| TLS_ECDH_RSA_WITH_AES_128_GCM_SHA256 | 20-22 | |
| TLS_ECDH_RSA_WITH_AES_256_CBC_SHA | 11-22 | 11-19 |
| TLS_ECDH_RSA_WITH_AES_256_CBC_SHA384 | 20-22 | |
| --- | --- | --- |
| TLS_ECDH_RSA_WITH_AES_256_GCM_SHA384 | 20-22 | |
| TLS_ECDH_RSA_WITH_NULL_SHA | 11-22 | |
| TLS_ECDH_RSA_WITH_RC4_128_SHA | 11-22 | 11-19 |
| --- | --- | --- |
| TLS_ECDH_anon_WITH_3DES_EDE_CBC_SHA | 11-22 | |
| TLS_ECDH_anon_WITH_AES_128_CBC_SHA | 11-22 | |
| TLS_ECDH_anon_WITH_AES_256_CBC_SHA | 11-22 | |
| --- | --- | --- |
| TLS_ECDH_anon_WITH_NULL_SHA | 11-22 | |
| TLS_ECDH_anon_WITH_RC4_128_SHA | 11-22 | |
| TLS_EMPTY_RENEGOTIATION_INFO_SCSV | 11+ | 11+ |
| --- | --- | --- |
| TLS_FALLBACK_SCSV | 21+ | |
| TLS_PSK_WITH_3DES_EDE_CBC_SHA | 21-22 | |
| TLS_PSK_WITH_AES_128_CBC_SHA | 21+ | 21+ |
| --- | --- | --- |
| TLS_PSK_WITH_AES_256_CBC_SHA | 21+ | 21+ |
| TLS_PSK_WITH_RC4_128_SHA | 21-25 | |
| TLS_RSA_WITH_AES_128_CBC_SHA | 9+ | 9+ |
| --- | --- | --- |
| TLS_RSA_WITH_AES_128_CBC_SHA256 | 20-28 | |
| TLS_RSA_WITH_AES_128_GCM_SHA256 | 20+ | 20+ |
| TLS_RSA_WITH_AES_256_CBC_SHA | 9+ | 11+ |
| --- | --- | --- |
| TLS_RSA_WITH_AES_256_CBC_SHA256 | 20-28 | |
| TLS_RSA_WITH_AES_256_GCM_SHA384 | 20+ | 20+ |
| TLS_RSA_WITH_NULL_SHA256 | 20-22 | |
| --- | --- | --- |

*NOTE* : PSK cipher suites are enabled by default only if the `SSLContext` through which the socket was created has been initialized with a `PSKKeyManager`.

API Levels 1 to 8 use OpenSSL names for cipher suites. The table below lists these OpenSSL names and their corresponding standard names used in API Levels 9 and newer.

| OpenSSL cipher suite | Standard cipher suite | Supported (API Levels) | Enabled by default (API Levels) |
|---|---|---|---|
| AES128-SHA | TLS_RSA_WITH_AES_128_CBC_SHA | 1+ | 1+ |
| AES256-SHA | TLS_RSA_WITH_AES_256_CBC_SHA | 1+ | 1--8, 11+ |
| DES-CBC-MD5 | SSL_CK_DES_64_CBC_WITH_MD5 | 1--8 | 1--8 |
| --- | --- | --- | --- |
| DES-CBC-SHA | SSL_RSA_WITH_DES_CBC_SHA | 1--22 | 1--19 |
| DES-CBC3-MD5 | SSL_CK_DES_192_EDE3_CBC_WITH_MD5 | 1--8 | 1--8 |
| DES-CBC3-SHA | SSL_RSA_WITH_3DES_EDE_CBC_SHA | 1+ | 1--19 |
| --- | --- | --- | --- |
| DHE-DSS-AES128-SHA | TLS_DHE_DSS_WITH_AES_128_CBC_SHA | 1--22 | 1--22 |
| DHE-DSS-AES256-SHA | TLS_DHE_DSS_WITH_AES_256_CBC_SHA | 1--22 | 1--8, 11--22 |
| DHE-RSA-AES128-SHA | TLS_DHE_RSA_WITH_AES_128_CBC_SHA | 1+ | 1+ |
| --- | --- | --- | --- |
| DHE-RSA-AES256-SHA | TLS_DHE_RSA_WITH_AES_256_CBC_SHA | 1+ | 1--8, 11+ |
| EDH-DSS-DES-CBC-SHA | SSL_DHE_DSS_WITH_DES_CBC_SHA | 1--22 | 1--19 |
| EDH-DSS-DES-CBC3-SHA | SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA | 1--22 | 1--19 |
| --- | --- | --- | --- |
| EDH-RSA-DES-CBC-SHA | SSL_DHE_RSA_WITH_DES_CBC_SHA | 1--22 | 1--19 |
| EDH-RSA-DES-CBC3-SHA | SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA | 1--22 | 1--19 |
| EXP-DES-CBC-SHA | SSL_RSA_EXPORT_WITH_DES40_CBC_SHA | 1--22 | 1--19 |
| --- | --- | --- | --- |
| EXP-EDH-DSS-DES-CBC-SHA | SSL_DHE_DSS_EXPORT_WITH_DES40_CBC_SHA | 1--22 | 1--19 |
| EXP-EDH-RSA-DES-CBC-SHA | SSL_DHE_RSA_EXPORT_WITH_DES40_CBC_SHA | 1--22 | 1--19 |
| EXP-RC2-CBC-MD5 | SSL_RSA_EXPORT_WITH_RC2_CBC_40_MD5 | 1--8 | 1--8 |
| --- | --- | --- | --- |
| EXP-RC4-MD5 | SSL_RSA_EXPORT_WITH_RC4_40_MD5 | 1--22 | 1--19 |
| RC2-CBC-MD5 | SSL_CK_RC2_128_CBC_WITH_MD5 | 1--8 | 1--8 |
| RC4-MD5 | SSL_RSA_WITH_RC4_128_MD5 | 1--25 | 1--19 |
| --- | --- | --- | --- |
| RC4-SHA | SSL_RSA_WITH_RC4_128_SHA | 1--25 | 1--23 |

## Summary

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#SSLSocket()()` Used only by subclasses. |
| `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#SSLSocket(kotlin.String,%20kotlin.Int)(host: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, port: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Used only by subclasses. |
| `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#SSLSocket(kotlin.String,%20kotlin.Int,%20java.net.InetAddress,%20kotlin.Int)(host: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, port: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, clientAddress: https://developer.android.com/reference/kotlin/java/net/InetAddress.html#!, clientPort: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Used only by subclasses. |
| `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#SSLSocket(java.net.InetAddress,%20kotlin.Int)(address: https://developer.android.com/reference/kotlin/java/net/InetAddress.html#!, port: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Used only by subclasses. |
| `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#SSLSocket(java.net.InetAddress,%20kotlin.Int,%20java.net.InetAddress,%20kotlin.Int)(address: https://developer.android.com/reference/kotlin/java/net/InetAddress.html#!, port: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, clientAddress: https://developer.android.com/reference/kotlin/java/net/InetAddress.html#!, clientPort: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Used only by subclasses. |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#addHandshakeCompletedListener(javax.net.ssl.HandshakeCompletedListener)(listener: https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedListener!)` Registers an event listener to receive notifications that an SSL handshake has completed on this connection. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getApplicationProtocol()()` Returns the most recent application protocol value negotiated for this connection. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getEnableSessionCreation()()` Returns true if new SSL sessions may be established by this socket. |
| --- | --- |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getEnabledCipherSuites()()` Returns the names of the SSL cipher suites which are currently enabled for use on this connection. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getEnabledProtocols()()` Returns the names of the protocol versions which are currently enabled for use on this connection. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getHandshakeApplicationProtocol()()` Returns the application protocol value negotiated on a SSL/TLS handshake currently in progress. |
| --- | --- |
| open [BiFunction](../java.util.function/BiFunction.md)\< [SSLSocket](SSLSocket.md)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getHandshakeApplicationProtocolSelector()()` Retrieves the callback function that selects an application protocol value during a SSL/TLS handshake. |
| open [SSLSession](SSLSession.md)! | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getHandshakeSession()()` Returns the `SSLSession` being constructed during a SSL/TLS handshake. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getNeedClientAuth()()` Returns true if the socket will *require* client authentication. |
| --- | --- |
| open [SSLParameters](SSLParameters.md)! | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getSSLParameters()()` Returns the SSLParameters in effect for this SSLSocket. |
| abstract [SSLSession](SSLSession.md)! | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getSession()()` Returns the SSL Session in use by this connection. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getSupportedCipherSuites()()` Returns the names of the cipher suites which could be enabled for use on this connection. |
| --- | --- |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getSupportedProtocols()()` Returns the names of the protocols which could be enabled for use on an SSL connection. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getUseClientMode()()` Returns true if the socket is set to use client mode when handshaking. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getWantClientAuth()()` Returns true if the socket will *request* client authentication. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#removeHandshakeCompletedListener(javax.net.ssl.HandshakeCompletedListener)(listener: https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedListener!)` Removes a previously registered handshake completion listener. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setEnableSessionCreation(kotlin.Boolean)(flag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Controls whether new SSL sessions may be established by this socket. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setEnabledCipherSuites(kotlin.Array)(suites: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Sets the cipher suites enabled for use on this connection. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setEnabledProtocols(kotlin.Array)(protocols: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Sets the protocol versions enabled for use on this connection. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setHandshakeApplicationProtocolSelector(java.util.function.BiFunction)(selector: https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#<https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Registers a callback function that selects an application protocol value for a SSL/TLS handshake. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setNeedClientAuth(kotlin.Boolean)(need: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Configures the socket to *require* client authentication. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setSSLParameters(javax.net.ssl.SSLParameters)(params: https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters!)` Applies SSLParameters to this socket. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setUseClientMode(kotlin.Boolean)(mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Configures the socket to use client (or server) mode when handshaking. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setWantClientAuth(kotlin.Boolean)(want: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Configures the socket to *request* client authentication. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#startHandshake()()` Starts an SSL handshake on this connection. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#toString()()` Converts this socket to a `String`. |

Inherited functions From class `https://developer.android.com/reference/kotlin/java/net/Socket.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#bind(java.net.SocketAddress)(bindpoint: https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#!)`

Binds the socket to a local address.

If the address is `null`, then the system will pick up an ephemeral port and a valid local address to bind the socket.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#close()()`

Closes this socket.

Any thread currently blocked in an I/O operation upon this socket will throw a `https://developer.android.com/reference/kotlin/java/net/SocketException.html#`.

Once a socket has been closed, it is not available for further networking use (i.e. can't be reconnected or rebound). A new socket needs to be created.

Closing this socket will also close the socket's `https://developer.android.com/reference/kotlin/java/io/InputStream.html#` and `https://developer.android.com/reference/kotlin/java/io/OutputStream.html#`.

If this socket has an associated channel then the channel is closed as well.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#connect(java.net.SocketAddress)(endpoint: https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#!)`

Connects this socket to the server.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#connect(java.net.SocketAddress,%20kotlin.Int)(endpoint: https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#!, timeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Connects this socket to the server with a specified timeout value. A timeout of zero is interpreted as an infinite timeout. The connection will then block until established or an error occurs.

<br />

`https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel.html#!` `https://developer.android.com/reference/kotlin/java/net/Socket.html#getChannel()()`

Returns the unique `https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel.html#` object associated with this socket, if any.

A socket will have a channel if, and only if, the channel itself was created via the java.nio.channels.SocketChannel#open or `https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel.html#accept()` methods.

<br />

`https://developer.android.com/reference/kotlin/java/net/InetAddress.html#!` `https://developer.android.com/reference/kotlin/java/net/Socket.html#getInetAddress()()`

Returns the address to which the socket is connected.

If the socket was connected prior to being #close, then this method will continue to return the connected address after the socket is closed.

<br />

`https://developer.android.com/reference/kotlin/java/io/InputStream.html#!` `https://developer.android.com/reference/kotlin/java/net/Socket.html#getInputStream()()`

Returns an input stream for this socket.

If this socket has an associated channel then the resulting input stream delegates all of its operations to the channel. If the channel is in non-blocking mode then the input stream's `read` operations will throw an `https://developer.android.com/reference/kotlin/java/nio/channels/IllegalBlockingModeException.html#`.

Under abnormal conditions the underlying connection may be broken by the remote host or the network software (for example a connection reset in the case of TCP connections). When a broken connection is detected by the network software the following applies to the returned input stream :-

- The network software may discard bytes that are buffered by the socket. Bytes that aren't discarded by the network software can be read using java.io.InputStream#read.
- If there are no bytes buffered on the socket, or all buffered bytes have been consumed by java.io.InputStream#read, then all subsequent calls to java.io.InputStream#read will throw an `https://developer.android.com/reference/kotlin/java/io/IOException.html#`.
- If there are no bytes buffered on the socket, and the socket has not been closed using #close, then `https://developer.android.com/reference/kotlin/java/io/InputStream.html#available()` will return `0`.

Closing the returned `https://developer.android.com/reference/kotlin/java/io/InputStream.html#` will close the associated socket.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#getKeepAlive()()`

Tests if `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_KEEPALIVE:kotlin.Int` is enabled.

<br />

`https://developer.android.com/reference/kotlin/java/net/InetAddress.html#!` `https://developer.android.com/reference/kotlin/java/net/Socket.html#getLocalAddress()()`

Gets the local address to which the socket is bound.

If there is a security manager set, its `checkConnect` method is called with the local address and `-1` as its arguments to see if the operation is allowed. If the operation is not allowed, the `https://developer.android.com/reference/kotlin/java/net/InetAddress.html#getLoopbackAddress()` address is returned.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#getLocalPort()()`

Returns the local port number to which this socket is bound.

If the socket was bound prior to being #close, then this method will continue to return the local port number after the socket is closed.

<br />

`https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#!` `https://developer.android.com/reference/kotlin/java/net/Socket.html#getLocalSocketAddress()()`

Returns the address of the endpoint this socket is bound to.

If a socket bound to an endpoint represented by an `InetSocketAddress ` is #close, then this method will continue to return an `InetSocketAddress` after the socket is closed. In that case the returned `InetSocketAddress`'s address is the `https://developer.android.com/reference/kotlin/java/net/InetAddress.html#isAnyLocalAddress()` address and its port is the local port that it was bound to.

If there is a security manager set, its `checkConnect` method is called with the local address and `-1` as its arguments to see if the operation is allowed. If the operation is not allowed, a `SocketAddress` representing the `https://developer.android.com/reference/kotlin/java/net/InetAddress.html#getLoopbackAddress()` address and the local port to which this socket is bound is returned.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#getOOBInline()()`

Tests if `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_OOBINLINE:kotlin.Int` is enabled.

<br />

`T` `https://developer.android.com/reference/kotlin/java/net/Socket.html#getOption(java.net.SocketOption)(name: https://developer.android.com/reference/kotlin/java/net/SocketOption.html#<T>!)`

Returns the value of a socket option.

<br />

`https://developer.android.com/reference/kotlin/java/io/OutputStream.html#!` `https://developer.android.com/reference/kotlin/java/net/Socket.html#getOutputStream()()`

Returns an output stream for this socket.

If this socket has an associated channel then the resulting output stream delegates all of its operations to the channel. If the channel is in non-blocking mode then the output stream's `write` operations will throw an `https://developer.android.com/reference/kotlin/java/nio/channels/IllegalBlockingModeException.html#`.

Closing the returned `https://developer.android.com/reference/kotlin/java/io/OutputStream.html#` will close the associated socket.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#getPort()()`

Returns the remote port number to which this socket is connected.

If the socket was connected prior to being #close, then this method will continue to return the connected port number after the socket is closed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#getReceiveBufferSize()()`

Gets the value of the `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_RCVBUF:kotlin.Int` option for this `Socket`, that is the buffer size used by the platform for input on this `Socket`.

<br />

`https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#!` `https://developer.android.com/reference/kotlin/java/net/Socket.html#getRemoteSocketAddress()()`

Returns the address of the endpoint this socket is connected to, or `null` if it is unconnected.

If the socket was connected prior to being #close, then this method will continue to return the connected address after the socket is closed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#getReuseAddress()()`

Tests if `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_REUSEADDR:kotlin.Int` is enabled.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#getSendBufferSize()()`

Get value of the `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_SNDBUF:kotlin.Int` option for this `Socket`, that is the buffer size used by the platform for output on this `Socket`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#getSoLinger()()`

Returns setting for `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_LINGER:kotlin.Int`. -1 returns implies that the option is disabled. The setting only affects socket close.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#getSoTimeout()()`

Returns setting for `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_TIMEOUT:kotlin.Int`. 0 returns implies that the option is disabled (i.e., timeout of infinity).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#getTcpNoDelay()()`

Tests if `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#TCP_NODELAY:kotlin.Int` is enabled.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#getTrafficClass()()`

Gets traffic class or type-of-service in the IP header for packets sent from this Socket

As the underlying network implementation may ignore the traffic class or type-of-service set using `https://developer.android.com/reference/kotlin/java/net/Socket.html#setTrafficClass(kotlin.Int)` this method may return a different value than was previously set using the `https://developer.android.com/reference/kotlin/java/net/Socket.html#setTrafficClass(kotlin.Int)` method on this Socket.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#isBound()()`

Returns the binding state of the socket.

Note: Closing a socket doesn't clear its binding state, which means this method will return `true` for a closed socket (see `https://developer.android.com/reference/kotlin/java/net/Socket.html#isClosed()`) if it was successfuly bound prior to being closed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#isClosed()()`

Returns the closed state of the socket.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#isConnected()()`

Returns the connection state of the socket.

Note: Closing a socket doesn't clear its connection state, which means this method will return `true` for a closed socket (see `https://developer.android.com/reference/kotlin/java/net/Socket.html#isClosed()`) if it was successfuly connected prior to being closed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#isInputShutdown()()`

Returns whether the read-half of the socket connection is closed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#isOutputShutdown()()`

Returns whether the write-half of the socket connection is closed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#sendUrgentData(kotlin.Int)(data: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Send one byte of urgent data on the socket. The byte to be sent is the lowest eight bits of the data parameter. The urgent byte is sent after any preceding writes to the socket OutputStream and before any future writes to the OutputStream.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#setKeepAlive(kotlin.Boolean)(on: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Enable/disable `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_KEEPALIVE:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#setOOBInline(kotlin.Boolean)(on: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Enable/disable `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_OOBINLINE:kotlin.Int` (receipt of TCP urgent data) By default, this option is disabled and TCP urgent data received on a socket is silently discarded. If the user wishes to receive urgent data, then this option must be enabled. When enabled, urgent data is received inline with normal data.

Note, only limited support is provided for handling incoming urgent data. In particular, no notification of incoming urgent data is provided and there is no capability to distinguish between normal data and urgent data unless provided by a higher level protocol.

<br />

`https://developer.android.com/reference/kotlin/java/net/Socket.html#!` `https://developer.android.com/reference/kotlin/java/net/Socket.html#setOption(java.net.SocketOption,%20java.net.Socket.setOption.T)(name: https://developer.android.com/reference/kotlin/java/net/SocketOption.html#<T>!, value: T)`

Sets the value of a socket option.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#setPerformancePreferences(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(connectionTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, latency: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bandwidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets performance preferences for this socket.

Sockets use the TCP/IP protocol by default. Some implementations may offer alternative protocols which have different performance characteristics than TCP/IP. This method allows the application to express its own preferences as to how these tradeoffs should be made when the implementation chooses from the available protocols.

Performance preferences are described by three integers whose values indicate the relative importance of short connection time, low latency, and high bandwidth. The absolute values of the integers are irrelevant; in order to choose a protocol the values are simply compared, with larger values indicating stronger preferences. Negative values represent a lower priority than positive values. If the application prefers short connection time over both low latency and high bandwidth, for example, then it could invoke this method with the values `(1, 0, 0)`. If the application prefers high bandwidth above low latency, and low latency above short connection time, then it could invoke this method with the values `(0, 1, 2)`.

Invoking this method after this socket has been connected will have no effect.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#setReceiveBufferSize(kotlin.Int)(size: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_RCVBUF:kotlin.Int` option to the specified value for this `Socket`. The `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_RCVBUF:kotlin.Int` option is used by the platform's networking code as a hint for the size to set the underlying network I/O buffers.

Increasing the receive buffer size can increase the performance of network I/O for high-volume connection, while decreasing it can help reduce the backlog of incoming data.

Because `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_RCVBUF:kotlin.Int` is a hint, applications that want to verify what size the buffers were set to should call `https://developer.android.com/reference/kotlin/java/net/Socket.html#getReceiveBufferSize()`.

The value of `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_RCVBUF:kotlin.Int` is also used to set the TCP receive window that is advertized to the remote peer. Generally, the window size can be modified at any time when a socket is connected. However, if a receive window larger than 64K is required then this must be requested **before** the socket is connected to the remote peer. There are two cases to be aware of:

1. For sockets accepted from a ServerSocket, this must be done by calling `https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#setReceiveBufferSize(kotlin.Int)` before the ServerSocket is bound to a local address.
2. For client sockets, setReceiveBufferSize() must be called before connecting the socket to its remote peer.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#setReuseAddress(kotlin.Boolean)(on: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Enable/disable the `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_REUSEADDR:kotlin.Int` socket option.

When a TCP connection is closed the connection may remain in a timeout state for a period of time after the connection is closed (typically known as the `TIME_WAIT` state or `2MSL` wait state). For applications using a well known socket address or port it may not be possible to bind a socket to the required `SocketAddress` if there is a connection in the timeout state involving the socket address or port.

Enabling `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_REUSEADDR:kotlin.Int` prior to binding the socket using `https://developer.android.com/reference/kotlin/java/net/Socket.html#bind(java.net.SocketAddress)` allows the socket to be bound even though a previous connection is in a timeout state.

When a `Socket` is created the initial setting of `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_REUSEADDR:kotlin.Int` is disabled.

The behaviour when `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_REUSEADDR:kotlin.Int` is enabled or disabled after a socket is bound (See `https://developer.android.com/reference/kotlin/java/net/Socket.html#isBound()`) is not defined.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#setSendBufferSize(kotlin.Int)(size: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets the `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_SNDBUF:kotlin.Int` option to the specified value for this `Socket`. The `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_SNDBUF:kotlin.Int` option is used by the platform's networking code as a hint for the size to set the underlying network I/O buffers.

Because `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_SNDBUF:kotlin.Int` is a hint, applications that want to verify what size the buffers were set to should call `https://developer.android.com/reference/kotlin/java/net/Socket.html#getSendBufferSize()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#setSoLinger(kotlin.Boolean,%20kotlin.Int)(on: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, linger: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Enable/disable `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_LINGER:kotlin.Int` with the specified linger time in seconds. The maximum timeout value is platform specific. The setting only affects socket close.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#setSoTimeout(kotlin.Int)(timeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Enable/disable `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_TIMEOUT:kotlin.Int` with the specified timeout, in milliseconds. With this option set to a non-zero timeout, a read() call on the InputStream associated with this Socket will block for only this amount of time. If the timeout expires, a **java.net.SocketTimeoutException** is raised, though the Socket is still valid. The option **must** be enabled prior to entering the blocking operation to have effect. The timeout must be `> 0`. A timeout of zero is interpreted as an infinite timeout.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#setSocketImplFactory(java.net.SocketImplFactory)(fac: https://developer.android.com/reference/kotlin/java/net/SocketImplFactory.html#!)`

Sets the client socket implementation factory for the application. The factory can be specified only once.

When an application creates a new client socket, the socket implementation factory's `createSocketImpl` method is called to create the actual socket implementation.

Passing `null` to the method is a no-op unless the factory was already set.

If there is a security manager, this method first calls the security manager's `checkSetFactory` method to ensure the operation is allowed. This could result in a SecurityException.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#setTcpNoDelay(kotlin.Boolean)(on: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Enable/disable `https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#TCP_NODELAY:kotlin.Int` (disable/enable Nagle's algorithm).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#setTrafficClass(kotlin.Int)(tc: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Sets traffic class or type-of-service octet in the IP header for packets sent from this Socket. As the underlying network implementation may ignore this value applications should consider it a hint.

The tc **must** be in the range `0 <= tc <= 255` or an IllegalArgumentException will be thrown.

Notes:

For Internet Protocol v4 the value consists of an `integer`, the least significant 8 bits of which represent the value of the TOS octet in IP packets sent by the socket. RFC 1349 defines the TOS values as follows:

- `IPTOS_LOWCOST (0x02)`
- `IPTOS_RELIABILITY (0x04)`
- `IPTOS_THROUGHPUT (0x08)`
- `IPTOS_LOWDELAY (0x10)`

The last low order bit is always ignored as this corresponds to the MBZ (must be zero) bit.

Setting bits in the precedence field may result in a SocketException indicating that the operation is not permitted.

As RFC 1122 section 4.2.4.2 indicates, a compliant TCP implementation should, but is not required to, let application change the TOS field during the lifetime of a connection. So whether the type-of-service field can be changed after the TCP connection has been established depends on the implementation in the underlying platform. Applications should not assume that they can change the TOS field after the connection.

For Internet Protocol v6 `tc` is the value that would be placed into the sin6_flowinfo field of the IP header.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#shutdownInput()()`

Places the input stream for this socket at "end of stream". Any data sent to the input stream side of the socket is acknowledged and then silently discarded.

If you read from a socket input stream after invoking this method on the socket, the stream's `available` method will return 0, and its `read` methods will return `-1` (end of stream).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/net/Socket.html#shutdownOutput()()`

Disables the output stream for this socket. For a TCP socket, any previously written data will be sent followed by TCP's normal connection termination sequence. If you write to a socket output stream after invoking shutdownOutput() on the socket, the stream will throw an IOException.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/java/net/SocketOption.html#<*>!>!` `https://developer.android.com/reference/kotlin/java/net/Socket.html#supportedOptions()()`

Returns a set of the socket options supported by this socket. This method will continue to return the set of options even after the socket has been closed.

<br />

## Protected constructors

### SSLSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected SSLSocket()
```

Used only by subclasses. Constructs an uninitialized, unconnected TCP socket.

### SSLSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected SSLSocket(
    host: String!, 
    port: Int)
```

Used only by subclasses. Constructs a TCP connection to a named host at a specified port. This acts as the SSL client.

If there is a security manager, its `checkConnect` method is called with the host address and `port` as its arguments. This could result in a SecurityException.

| Parameters ||
|---|---|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: name of the host with which to connect, or `null` for the loopback address. |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of the server's port |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs when creating the socket |
| `java.lang.IllegalArgumentException` | if the port parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |
| `java.lang.SecurityException` | if a security manager exists and its `checkConnect` method doesn't allow the operation. |
| --- | --- |
| `java.net.UnknownHostException` | if the host is not known |

**See Also**

### SSLSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected SSLSocket(
    host: String!, 
    port: Int, 
    clientAddress: InetAddress!, 
    clientPort: Int)
```

Used only by subclasses. Constructs an SSL connection to a named host at a specified port, binding the client side of the connection a given address and port. This acts as the SSL client.

If there is a security manager, its `checkConnect` method is called with the host address and `port` as its arguments. This could result in a SecurityException.

| Parameters ||
|---|---|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: name of the host with which to connect, or `null` for the loopback address. |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of the server's port |
| `clientAddress` | [InetAddress](../java.net/InetAddress.md)!: the client's address the socket is bound to, or `null` for the `anyLocal` address. |
| --- | --- |
| `clientPort` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the client's port the socket is bound to, or `zero` for a system selected free port. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs when creating the socket |
| `java.lang.IllegalArgumentException` | if the port parameter or clientPort parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |
| `java.lang.SecurityException` | if a security manager exists and its `checkConnect` method doesn't allow the operation. |
| --- | --- |
| `java.net.UnknownHostException` | if the host is not known |

**See Also**

### SSLSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected SSLSocket(
    address: InetAddress!, 
    port: Int)
```

Used only by subclasses. Constructs a TCP connection to a server at a specified address and port. This acts as the SSL client.

If there is a security manager, its `checkConnect` method is called with the host address and `port` as its arguments. This could result in a SecurityException.

| Parameters ||
|---|---|
| `address` | [InetAddress](../java.net/InetAddress.md)!: the server's host |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): its port |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs when creating the socket |
| `java.lang.IllegalArgumentException` | if the port parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |
| `java.lang.NullPointerException` | if `address` is null. |
| --- | --- |
| `java.lang.SecurityException` | if a security manager exists and its `checkConnect` method doesn't allow the operation. |

**See Also**

### SSLSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected SSLSocket(
    address: InetAddress!, 
    port: Int, 
    clientAddress: InetAddress!, 
    clientPort: Int)
```

Used only by subclasses. Constructs an SSL connection to a server at a specified address and TCP port, binding the client side of the connection a given address and port. This acts as the SSL client.

If there is a security manager, its `checkConnect` method is called with the host address and `port` as its arguments. This could result in a SecurityException.

| Parameters ||
|---|---|
| `address` | [InetAddress](../java.net/InetAddress.md)!: the server's host |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): its port |
| `clientAddress` | [InetAddress](../java.net/InetAddress.md)!: the client's address the socket is bound to, or `null` for the `anyLocal` address. |
| --- | --- |
| `clientPort` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the client's port the socket is bound to, or `zero` for a system selected free port. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs when creating the socket |
| `java.lang.IllegalArgumentException` | if the port parameter or clientPort parameter is outside the specified range of valid port values, which is between 0 and 65535, inclusive. |
| `java.lang.NullPointerException` | if `address` is null. |
| --- | --- |
| `java.lang.SecurityException` | if a security manager exists and its `checkConnect` method doesn't allow the operation. |

**See Also**

## Public methods

### addHandshakeCompletedListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun addHandshakeCompletedListener(listener: HandshakeCompletedListener!): Unit
```

Registers an event listener to receive notifications that an SSL handshake has completed on this connection.

| Parameters ||
|---|---|
| `listener` | [HandshakeCompletedListener](HandshakeCompletedListener.md)!: the HandShake Completed event listener |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the argument is null. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#startHandshake()`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#removeHandshakeCompletedListener(javax.net.ssl.HandshakeCompletedListener)`

### getApplicationProtocol

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApplicationProtocol(): String!
```

Returns the most recent application protocol value negotiated for this connection.

If supported by the underlying SSL/TLS implementation, application name negotiation mechanisms such as [RFC 7301](http://www.ietf.org/rfc/rfc7301.txt), the Application-Layer Protocol Negotiation (ALPN), can negotiate application-level values between peers.

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | null if it has not yet been determined if application protocols might be used for this connection, an empty `String` if application protocols values will not be used, or a non-empty application protocol `String` if a value was successfully negotiated. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the underlying provider does not implement the operation. |

### getEnableSessionCreation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getEnableSessionCreation(): Boolean
```

Returns true if new SSL sessions may be established by this socket.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true indicates that sessions may be created; this is the default. false indicates that an existing session must be resumed |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setEnableSessionCreation(kotlin.Boolean)`

### getEnabledCipherSuites

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getEnabledCipherSuites(): Array<String!>!
```

Returns the names of the SSL cipher suites which are currently enabled for use on this connection. When an SSLSocket is first created, all enabled cipher suites support a minimum quality of service. Thus, in some environments this value might be empty.

Even if a suite has been enabled, it might never be used. (For example, the peer does not support it, the requisite certificates (and private keys) for the suite are not available, or an anonymous suite is enabled but authentication is required.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | an array of cipher suite names |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getSupportedCipherSuites()`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setEnabledCipherSuites(kotlin.Array)`

### getEnabledProtocols

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getEnabledProtocols(): Array<String!>!
```

Returns the names of the protocol versions which are currently enabled for use on this connection.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | an array of protocols |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setEnabledProtocols(kotlin.Array)`

### getHandshakeApplicationProtocol

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHandshakeApplicationProtocol(): String!
```

Returns the application protocol value negotiated on a SSL/TLS handshake currently in progress.

Like `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getHandshakeSession()`, a connection may be in the middle of a handshake. The application protocol may or may not yet be available.

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | null if it has not yet been determined if application protocols might be used for this handshake, an empty `String` if application protocols values will not be used, or a non-empty application protocol `String` if a value was successfully negotiated. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the underlying provider does not implement the operation. |

### getHandshakeApplicationProtocolSelector

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHandshakeApplicationProtocolSelector(): BiFunction<SSLSocket!, MutableList<String!>!, String!>!
```

Retrieves the callback function that selects an application protocol value during a SSL/TLS handshake. See `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setHandshakeApplicationProtocolSelector(java.util.function.BiFunction)` for the function's type parameters.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#<https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | the callback function, or null if none has been set. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the underlying provider does not implement the operation. |

### getHandshakeSession

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHandshakeSession(): SSLSession!
```

Returns the `SSLSession` being constructed during a SSL/TLS handshake.

TLS protocols may negotiate parameters that are needed when using an instance of this class, but before the `SSLSession` has been completely initialized and made available via `getSession`. For example, the list of valid signature algorithms may restrict the type of certificates that can used during TrustManager decisions, or the maximum TLS fragment packet sizes can be resized to better support the network environment.

This method provides early access to the `SSLSession` being constructed. Depending on how far the handshake has progressed, some data may not yet be available for use. For example, if a remote server will be sending a Certificate chain, but that chain has yet not been processed, the `getPeerCertificates` method of `SSLSession` will throw a SSLPeerUnverifiedException. Once that chain has been processed, `getPeerCertificates` will return the proper value.

Unlike `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getSession()`, this method does not initiate the initial handshake and does not block until handshaking is complete.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession!` | null if this instance is not currently handshaking, or if the current handshake has not progressed far enough to create a basic SSLSession. Otherwise, this method returns the `SSLSession` currently being negotiated. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the underlying provider does not implement the operation. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/ExtendedSSLSession`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/X509ExtendedKeyManager`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/X509ExtendedTrustManager`

### getNeedClientAuth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getNeedClientAuth(): Boolean
```

Returns true if the socket will *require* client authentication. This option is only useful to sockets in the server mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if client authentication is required, or false if no client authentication is desired. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setNeedClientAuth(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setWantClientAuth(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getWantClientAuth()`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setUseClientMode(kotlin.Boolean)`

### getSSLParameters

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSSLParameters(): SSLParameters!
```

Returns the SSLParameters in effect for this SSLSocket. The ciphersuites and protocols of the returned SSLParameters are always non-null.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters!` | the SSLParameters in effect for this SSLSocket. |

### getSession

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSession(): SSLSession!
```

Returns the SSL Session in use by this connection. These can be long lived, and frequently correspond to an entire login session for some user. The session specifies a particular cipher suite which is being actively used by all connections in that session, as well as the identities of the session's client and server.

This method will initiate the initial handshake if necessary and then block until the handshake has been established.

If an error occurs during the initial handshake, this method returns an invalid session object which reports an invalid cipher suite of "SSL_NULL_WITH_NULL_NULL".

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession!` | the `SSLSession` |

### getSupportedCipherSuites

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSupportedCipherSuites(): Array<String!>!
```

Returns the names of the cipher suites which could be enabled for use on this connection. Normally, only a subset of these will actually be enabled by default, since this list may include cipher suites which do not meet quality of service requirements for those defaults. Such cipher suites might be useful in specialized applications.

Applications should not blindly enable all supported cipher suites. The supported cipher suites can include signaling cipher suite values that can cause connection problems if enabled inappropriately.

The proper way to use this method is to either check if a specific cipher suite is supported via `Arrays.asList(getSupportedCipherSuites()).contains(...)` or to filter a desired list of cipher suites to only the supported ones via `desiredSuiteSet.retainAll(Arrays.asList(getSupportedCipherSuites()))`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | an array of cipher suite names |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getEnabledCipherSuites()`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setEnabledCipherSuites(kotlin.Array)`

### getSupportedProtocols

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSupportedProtocols(): Array<String!>!
```

Returns the names of the protocols which could be enabled for use on an SSL connection.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | an array of protocols supported |

### getUseClientMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getUseClientMode(): Boolean
```

Returns true if the socket is set to use client mode when handshaking.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the socket should do handshaking in "client" mode |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setUseClientMode(kotlin.Boolean)`

### getWantClientAuth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getWantClientAuth(): Boolean
```

Returns true if the socket will *request* client authentication. This option is only useful for sockets in the server mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if client authentication is requested, or false if no client authentication is desired. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setNeedClientAuth(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getNeedClientAuth()`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setWantClientAuth(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setUseClientMode(kotlin.Boolean)`

### removeHandshakeCompletedListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun removeHandshakeCompletedListener(listener: HandshakeCompletedListener!): Unit
```

Removes a previously registered handshake completion listener.

| Parameters ||
|---|---|
| `listener` | [HandshakeCompletedListener](HandshakeCompletedListener.md)!: the HandShake Completed event listener |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the listener is not registered, or the argument is null. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#addHandshakeCompletedListener(javax.net.ssl.HandshakeCompletedListener)`

### setEnableSessionCreation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setEnableSessionCreation(flag: Boolean): Unit
```

Controls whether new SSL sessions may be established by this socket. If session creations are not allowed, and there are no existing sessions to resume, there will be no successful handshaking.

| Parameters ||
|---|---|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true indicates that sessions may be created; this is the default. false indicates that an existing session must be resumed |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getEnableSessionCreation()`

### setEnabledCipherSuites

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setEnabledCipherSuites(suites: Array<String!>!): Unit
```

Sets the cipher suites enabled for use on this connection.

Each cipher suite in the `suites` parameter must have been listed by getSupportedCipherSuites(), or the method will fail. Following a successful call to this method, only suites listed in the `suites` parameter are enabled for use.

On Android 10 (API level 29) and higher, when TLS 1.3 is enabled, its supported cipher suites are always enabled and cannot be individually disabled using this method. Attempts to disable TLS 1.3 cipher suites are ignored.

See `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getEnabledCipherSuites()` for more information on why a specific ciphersuite may never be used on a connection.

| Parameters ||
|---|---|
| `suites` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: Names of all the cipher suites to enable |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | when one or more of the ciphers named by the parameter is not supported, or when the parameter is null. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getSupportedCipherSuites()`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getEnabledCipherSuites()`

### setEnabledProtocols

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setEnabledProtocols(protocols: Array<String!>!): Unit
```

Sets the protocol versions enabled for use on this connection.

The protocols must have been listed by `getSupportedProtocols()` as being supported. Following a successful call to this method, only protocols listed in the `protocols` parameter are enabled for use.

Because of the way the protocol version is negotiated, connections will only be able to use a member of the lowest set of contiguous enabled protocol versions. For example, enabling TLSv1.2 and TLSv1 will result in connections only being able to use TLSv1.

| Parameters ||
|---|---|
| `protocols` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: Names of all the protocols to enable. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | when one or more of the protocols named by the parameter is not supported or when the protocols parameter is null. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getEnabledProtocols()`

### setHandshakeApplicationProtocolSelector

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHandshakeApplicationProtocolSelector(selector: BiFunction<SSLSocket!, MutableList<String!>!, String!>!): Unit
```

Registers a callback function that selects an application protocol value for a SSL/TLS handshake. The function overrides any values supplied using `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setApplicationProtocols(kotlin.Array)` and it supports the following type parameters:

`SSLSocket`
: The function's first argument allows the current `SSLSocket` to be inspected, including the handshake session and configuration settings.

`List<String>`
: The function's second argument lists the application protocol names advertised by the TLS peer.

`String`
: The function's result is an application protocol name, or null to indicate that none of the advertised names are acceptable. If the return value is an empty `String` then application protocol indications will not be used. If the return value is null (no value chosen) or is a value that was not advertised by the peer, the underlying protocol will determine what action to take. (For example, ALPN will send a "no_application_protocol" alert and terminate the connection.)
For example, the following call registers a callback function that examines the TLS handshake parameters and selects an application protocol name:

```kotlin
<code>serverSocket.setHandshakeApplicationProtocolSelector(
          (serverSocket, clientProtocols) -&gt; {
              SSLSession session = serverSocket.getHandshakeSession();
              return chooseApplicationProtocol(
                  serverSocket,
                  clientProtocols,
                  session.getProtocol(),
                  session.getCipherSuite());
          });
  </code>
```

<br />

| Parameters ||
|---|---|
| `selector` | [BiFunction](../java.util.function/BiFunction.md)\< [SSLSocket](SSLSocket.md)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: the callback function, or null to de-register. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the underlying provider does not implement the operation. |

### setNeedClientAuth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setNeedClientAuth(need: Boolean): Unit
```

Configures the socket to *require* client authentication. This option is only useful for sockets in the server mode.

A socket's client authentication setting is one of the following:

- client authentication required
- client authentication requested
- no client authentication desired

Unlike `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setWantClientAuth(kotlin.Boolean)`, if this option is set and the client chooses not to provide authentication information about itself, *the negotiations will stop and the connection will be dropped*.

Calling this method overrides any previous setting made by this method or `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setWantClientAuth(kotlin.Boolean)`.

| Parameters ||
|---|---|
| `need` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): set to true if client authentication is required, or false if no client authentication is desired. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getNeedClientAuth()`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setWantClientAuth(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getWantClientAuth()`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setUseClientMode(kotlin.Boolean)`

### setSSLParameters

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSSLParameters(params: SSLParameters!): Unit
```

Applies SSLParameters to this socket.

This means:

- If `params.getCipherSuites()` is non-null, `setEnabledCipherSuites()` is called with that value.
- If `params.getProtocols()` is non-null, `setEnabledProtocols()` is called with that value.
- If `params.getNeedClientAuth()` or `params.getWantClientAuth()` return `true`, `setNeedClientAuth(true)` and `setWantClientAuth(true)` are called, respectively; otherwise `setWantClientAuth(false)` is called.
- If `params.getServerNames()` is non-null, the socket will configure its server names with that value.
- If `params.getSNIMatchers()` is non-null, the socket will configure its SNI matchers with that value.

| Parameters ||
|---|---|
| `params` | [SSLParameters](SSLParameters.md)!: the parameters |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the setEnabledCipherSuites() or the setEnabledProtocols() call fails |

### setUseClientMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setUseClientMode(mode: Boolean): Unit
```

Configures the socket to use client (or server) mode when handshaking.

This method must be called before any handshaking occurs. Once handshaking has begun, the mode can not be reset for the life of this socket.

Servers normally authenticate themselves, and clients are not required to do so.

| Parameters ||
|---|---|
| `mode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the socket should start its handshaking in "client" mode |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if a mode change is attempted after the initial handshake has begun. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getUseClientMode()`

### setWantClientAuth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setWantClientAuth(want: Boolean): Unit
```

Configures the socket to *request* client authentication. This option is only useful for sockets in the server mode.

A socket's client authentication setting is one of the following:

- client authentication required
- client authentication requested
- no client authentication desired

Unlike `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setNeedClientAuth(kotlin.Boolean)`, if this option is set and the client chooses not to provide authentication information about itself, *the negotiations will continue*.

Calling this method overrides any previous setting made by this method or `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setNeedClientAuth(kotlin.Boolean)`.

| Parameters ||
|---|---|
| `want` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): set to true if client authentication is requested, or false if no client authentication is desired. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getWantClientAuth()`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setNeedClientAuth(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getNeedClientAuth()`
- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#setUseClientMode(kotlin.Boolean)`

### startHandshake

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun startHandshake(): Unit
```

Starts an SSL handshake on this connection. Common reasons include a need to use new encryption keys, to change cipher suites, or to initiate a new session. To force complete reauthentication, the current session could be invalidated before starting this handshake.

If data has already been sent on the connection, it continues to flow during this handshake. When the handshake completes, this will be signaled with an event. This method is synchronous for the initial handshake on a connection and returns when the negotiated handshake is complete. Some protocols may not support multiple handshakes on an existing socket and may throw an IOException.

| Exceptions ||
|---|---|
| `java.io.IOException` | on a network level error |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#addHandshakeCompletedListener(javax.net.ssl.HandshakeCompletedListener)`

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Converts this socket to a `String`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of this socket. |
