# SSLEngine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLEngine

```
abstract class SSLEngine
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [javax.net.ssl.SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#) |

A class which enables secure communications using protocols such as the Secure Sockets Layer (SSL) or [IETF RFC 2246 "Transport Layer Security" (TLS)](http://www.ietf.org/rfc/rfc2246.txt) protocols, but is transport independent.

The secure communications modes include:

- *Integrity Protection*. SSL/TLS protects against modification of messages by an active wiretapper.
- *Authentication*. In most modes, SSL/TLS provides peer authentication. Servers are usually authenticated, and clients may be authenticated as requested by servers.
- *Confidentiality (Privacy Protection)*. In most modes, SSL/TLS encrypts data being sent between client and server. This protects the confidentiality of data, so that passive wiretappers won't see sensitive data such as financial information or personal information of many kinds.

These kinds of protection are specified by a "cipher suite", which is a combination of cryptographic algorithms used by a given SSL connection. During the negotiation process, the two endpoints must agree on a cipher suite that is available in both environments. If there is no such suite in common, no SSL connection can be established, and no data can be exchanged.

The cipher suite used is established by a negotiation process called "handshaking". The goal of this process is to create or rejoin a "session", which may protect many connections over time. After handshaking has completed, you can access session attributes by using the [getSession()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getSession())method.

The`SSLSocket`class provides much of the same security functionality, but all of the inbound and outbound data is automatically transported using the underlying , which by design uses a blocking model. While this is appropriate for many applications, this model does not provide the scalability required by large servers.

The primary distinction of an`SSLEngine`is that it operates on inbound and outbound byte streams, independent of the transport mechanism. It is the responsibility of the`SSLEngine`user to arrange for reliable I/O transport to the peer. By separating the SSL/TLS abstraction from the I/O transport mechanism, the`SSLEngine`can be used for a wide variety of I/O types, such as [non-blocking I/O (polling)](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel.html#configureBlocking(kotlin.Boolean)), [selectable non-blocking I/O](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#), [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) and the traditional Input/OutputStreams, local [ByteBuffers](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#) or byte arrays, [future asynchronous I/O models](http://www.jcp.org/en/jsr/detail?id=203), and so on.

At a high level, the`SSLEngine`appears thus: 

```kotlin
app data
 
                 |           ^
                 |     |     |
                 v     |     |
            +----+-----|-----+----+
            |          |          |
            |       SSL|Engine    |
    wrap()  |          |          |  unwrap()
            | OUTBOUND | INBOUND  |
            |          |          |
            +----+-----|-----+----+
                 |     |     ^
                 |     |     |
                 v           |
 
                    net data
  
```
Application data (also known as plaintext or cleartext) is data which is produced or consumed by an application. Its counterpart is network data, which consists of either handshaking and/or ciphertext (encrypted) data, and destined to be transported via an I/O mechanism. Inbound data is data which has been received from the peer, and outbound data is destined for the peer.

(In the context of an`SSLEngine`, the term "handshake data" is taken to mean any data exchanged to establish and control a secure connection. Handshake data includes the SSL/TLS messages "alert", "change_cipher_spec," and "handshake.")

There are five distinct phases to an`SSLEngine`.

1. Creation - The`SSLEngine`has been created and initialized, but has not yet been used. During this phase, an application may set any`SSLEngine`-specific settings (enabled cipher suites, whether the`SSLEngine`should handshake in client or server mode, and so on). Once handshaking has begun, though, any new settings (except client/server mode, see below) will be used for the next handshake.
2. Initial Handshake - The initial handshake is a procedure by which the two peers exchange communication parameters until an SSLSession is established. Application data can not be sent during this phase.
3. Application Data - Once the communication parameters have been established and the handshake is complete, application data may flow through the`SSLEngine`. Outbound application messages are encrypted and integrity protected, and inbound messages reverse the process.
4. Rehandshaking - Either side may request a renegotiation of the session at any time during the Application Data phase. New handshaking data can be intermixed among the application data. Before starting the rehandshake phase, the application may reset the SSL/TLS communication parameters such as the list of enabled ciphersuites and whether to use client authentication, but can not change between client/server modes. As before, once handshaking has begun, any new`SSLEngine`configuration settings will not be used until the next handshake.
5. Closure - When the connection is no longer needed, the application should close the`SSLEngine`and should send/receive any remaining messages to the peer before closing the underlying transport mechanism. Once an engine is closed, it is not reusable: a new`SSLEngine`must be created.

An`SSLEngine`is created by calling [javax.net.ssl.SSLContext#createSSLEngine()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#createSSLEngine())from an initialized`SSLContext`. Any configuration parameters should be set before making the first call to`wrap()`,`unwrap()`, or`beginHandshake()`. These methods all trigger the initial handshake.

Data moves through the engine by calling [wrap()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#wrap(java.nio.ByteBuffer,%20java.nio.ByteBuffer))or [unwrap()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#unwrap(java.nio.ByteBuffer,%20java.nio.ByteBuffer))on outbound or inbound data, respectively. Depending on the state of the`SSLEngine`, a`wrap()`call may consume application data from the source buffer and may produce network data in the destination buffer. The outbound data may contain application and/or handshake data. A call to`unwrap()`will examine the source buffer and may advance the handshake if the data is handshaking information, or may place application data in the destination buffer if the data is application. The state of the underlying SSL/TLS algorithm will determine when data is consumed and produced.

Calls to`wrap()`and`unwrap()`return an`SSLEngineResult`which indicates the status of the operation, and (optionally) how to interact with the engine to make progress.

The`SSLEngine`produces/consumes complete SSL/TLS packets only, and does not store application data internally between calls to`wrap()/unwrap()`. Thus input and output`ByteBuffer`s must be sized appropriately to hold the maximum record that can be produced. Calls to [javax.net.ssl.SSLSession#getPacketBufferSize()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getPacketBufferSize())and [javax.net.ssl.SSLSession#getApplicationBufferSize()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getApplicationBufferSize())should be used to determine the appropriate buffer sizes. The size of the outbound application data buffer generally does not matter. If buffer conditions do not allow for the proper consumption/production of data, the application must determine (via [SSLEngineResult](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult)) and correct the problem, and then try the call again.

For example,`unwrap()`will return a [javax.net.ssl.SSLEngineResult.Status#BUFFER_OVERFLOW](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult.Status) result if the engine determines that there is not enough destination buffer space available. Applications should call [SSLSession.getApplicationBufferSize()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getApplicationBufferSize())and compare that value with the space available in the destination buffer, enlarging the buffer if necessary. Similarly, if`unwrap()`were to return a [SSLEngineResult.Status.BUFFER_UNDERFLOW](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult.Status), the application should call [SSLSession.getPacketBufferSize()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getPacketBufferSize())to ensure that the source buffer has enough room to hold a record (enlarging if necessary), and then obtain more inbound data. 

```kotlin
<code>SSLEngineResult r = engine.unwrap(src, dst);
    switch (r.getStatus()) {
    BUFFER_OVERFLOW:
        // Could attempt to drain the dst buffer of any already obtained
        // data, but we'll just increase it to the size needed.
        int appSize = engine.getSession().getApplicationBufferSize();
        ByteBuffer b = ByteBuffer.allocate(appSize + dst.position());
        dst.flip();
        b.put(dst);
        dst = b;
        // retry the operation.
        break;
    BUFFER_UNDERFLOW:
        int netSize = engine.getSession().getPacketBufferSize();
        // Resize buffer if needed.
        if (netSize &gt; dst.capacity()) {
            ByteBuffer b = ByteBuffer.allocate(netSize);
            src.flip();
            b.put(src);
            src = b;
        }
        // Obtain more inbound network data for src,
        // then retry the operation.
        break;
    // other cases: CLOSED, OK.
    }
  </code>
```

Unlike`SSLSocket`, all methods of SSLEngine are non-blocking.`SSLEngine`implementations may require the results of tasks that may take an extended period of time to complete, or may even block. For example, a TrustManager may need to connect to a remote certificate validation service, or a KeyManager might need to prompt a user to determine which certificate to use as part of client authentication. Additionally, creating cryptographic signatures and verifying them can be slow, seemingly blocking.

For any operation which may potentially block, the`SSLEngine`will create a [java.lang.Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#) delegated task. When`SSLEngineResult`indicates that a delegated task result is needed, the application must call [getDelegatedTask()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getDelegatedTask())to obtain an outstanding delegated task and call its [run()](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#run())method (possibly using a different thread depending on the compute strategy). The application should continue obtaining delegated tasks until no more exist, and try the original operation again.

At the end of a communication session, applications should properly close the SSL/TLS link. The SSL/TLS protocols have closure handshake messages, and these messages should be communicated to the peer before releasing the`SSLEngine`and closing the underlying transport mechanism. A close can be initiated by one of: an SSLException, an inbound closure handshake message, or one of the close methods. In all cases, closure handshake messages are generated by the engine, and`wrap()`should be repeatedly called until the resulting`SSLEngineResult`'s status returns "CLOSED", or [isOutboundDone()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#isOutboundDone())returns true. All data obtained from the`wrap()`method should be sent to the peer.

[closeOutbound()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#closeOutbound())is used to signal the engine that the application will not be sending any more data.

A peer will signal its intent to close by sending its own closure handshake message. After this message has been received and processed by the local`SSLEngine`'s`unwrap()`call, the application can detect the close by calling`unwrap()`and looking for a`SSLEngineResult`with status "CLOSED", or if [isInboundDone()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#isInboundDone())returns true. If for some reason the peer closes the communication link without sending the proper SSL/TLS closure message, the application can detect the end-of-stream and can signal the engine via [closeInbound()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#closeInbound())that there will no more inbound messages to process. Some applications might choose to require orderly shutdown messages from a peer, in which case they can check that the closure was generated by a handshake message and not by an end-of-stream condition.

There are two groups of cipher suites which you will need to know about when managing cipher suites:

- *Supported* cipher suites: all the suites which are supported by the SSL implementation. This list is reported using [getSupportedCipherSuites()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getSupportedCipherSuites()).
- *Enabled* cipher suites, which may be fewer than the full set of supported suites. This group is set using the[setEnabledCipherSuites(java.lang.String[])](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setEnabledCipherSuites(kotlin.Array))method, and queried using the [getEnabledCipherSuites()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getEnabledCipherSuites())method. Initially, a default set of cipher suites will be enabled on a new engine that represents the minimum suggested configuration.

Implementation defaults require that only cipher suites which authenticate servers and provide confidentiality be enabled by default. Only if both sides explicitly agree to unauthenticated and/or non-private (unencrypted) communications will such a cipher suite be selected.

Each SSL/TLS connection must have one client and one server, thus each endpoint must decide which role to assume. This choice determines who begins the handshaking process as well as which type of messages should be sent by each party. The method [setUseClientMode(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setUseClientMode(kotlin.Boolean))configures the mode. Once the initial handshaking has started, an`SSLEngine`can not switch between client and server modes, even when performing renegotiations.

Applications might choose to process delegated tasks in different threads. When an`SSLEngine`is created, the current [java.security.AccessControlContext](https://developer.android.com/reference/kotlin/java/security/AccessControlContext.html#) is saved. All future delegated tasks will be processed using this context: that is, all access control decisions will be made using the context captured at engine creation.
**Concurrency Notes** : There are two concurrency issues to be aware of:

1. The`wrap()`and`unwrap()`methods may execute concurrently of each other.
2. The SSL/TLS protocols employ ordered packets. Applications must take care to ensure that generated packets are delivered in sequence. If packets arrive out-of-order, unexpected or fatal results may occur.For example:

   ```kotlin
   synchronized (outboundLock) {
                      sslEngine.wrap(src, dst);
                      outboundQueue.put(dst);
                  }
          
   ```
 As a corollary, two threads must not attempt to call the same method (either`wrap()`or`unwrap()`) concurrently, because there is no way to guarantee the eventual packet ordering.

### Default configuration for different Android versions

`SSLEngine`instances obtained from the default [SSLContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext) are configured as follows:

#### Protocols

| Protocol | Supported (API Levels) | Enabled by default (API Levels) |
|----------|------------------------|---------------------------------|
| SSLv3 | 1--25 | 1--22 |
| TLSv1 | 1+ | 1+ |
| TLSv1.1 | 20+ | 20+ |
| TLSv1.2 | 20+ | 20+ |
| TLSv1.3 | 29+ | 29+ |

#### Cipher suites

| Cipher suite | Supported (API Levels) | Enabled by default (API Levels) |
|-----------------------------------------------|------------------------|---------------------------------|
| SSL_DHE_DSS_EXPORT_WITH_DES40_CBC_SHA | 9-22 | 9-19 |
| SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA | 9-22 | 9-19 |
| SSL_DHE_DSS_WITH_DES_CBC_SHA | 9-22 | 9-19 |
| SSL_DHE_RSA_EXPORT_WITH_DES40_CBC_SHA | 9-22 | 9-19 |
| SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA | 9-22 | 9-19 |
| SSL_DHE_RSA_WITH_DES_CBC_SHA | 9-22 | 9-19 |
| SSL_DH_anon_EXPORT_WITH_DES40_CBC_SHA | 9-22 | |
| SSL_DH_anon_EXPORT_WITH_RC4_40_MD5 | 9-22 | |
| SSL_DH_anon_WITH_3DES_EDE_CBC_SHA | 9-22 | |
| SSL_DH_anon_WITH_DES_CBC_SHA | 9-22 | |
| SSL_DH_anon_WITH_RC4_128_MD5 | 9-22 | |
| SSL_RSA_EXPORT_WITH_DES40_CBC_SHA | 9-22 | 9-19 |
| SSL_RSA_EXPORT_WITH_RC4_40_MD5 | 9-22 | 9-19 |
| SSL_RSA_WITH_3DES_EDE_CBC_SHA | 9+ | 9-19 |
| SSL_RSA_WITH_DES_CBC_SHA | 9-22 | 9-19 |
| SSL_RSA_WITH_NULL_MD5 | 9-22 | |
| SSL_RSA_WITH_NULL_SHA | 9-22 | |
| SSL_RSA_WITH_RC4_128_MD5 | 9-25 | 9-19 |
| SSL_RSA_WITH_RC4_128_SHA | 9-25 | 9-23 |
| TLS_AES_128_GCM_SHA256 | 29+ | 29+ |
| TLS_AES_256_GCM_SHA384 | 29+ | 29+ |
| TLS_CHACHA20_POLY1305_SHA256 | 29+ | 29+ |
| TLS_DHE_DSS_EXPORT_WITH_DES40_CBC_SHA | 1-8 | 1-8 |
| TLS_DHE_DSS_WITH_3DES_EDE_CBC_SHA | 1-8 | 1-8 |
| TLS_DHE_DSS_WITH_AES_128_CBC_SHA | 9-22 | 9-22 |
| TLS_DHE_DSS_WITH_AES_128_CBC_SHA256 | 20-22 | |
| TLS_DHE_DSS_WITH_AES_128_GCM_SHA256 | 20-22 | |
| TLS_DHE_DSS_WITH_AES_256_CBC_SHA | 9-22 | 20-22 |
| TLS_DHE_DSS_WITH_AES_256_CBC_SHA256 | 20-22 | |
| TLS_DHE_DSS_WITH_AES_256_GCM_SHA384 | 20-22 | |
| TLS_DHE_DSS_WITH_DES_CBC_SHA | 1-8 | 1-8 |
| TLS_DHE_RSA_EXPORT_WITH_DES40_CBC_SHA | 1-8 | 1-8 |
| TLS_DHE_RSA_WITH_3DES_EDE_CBC_SHA | 1-8 | 1-8 |
| TLS_DHE_RSA_WITH_AES_128_CBC_SHA | 9-25 | 9-25 |
| TLS_DHE_RSA_WITH_AES_128_CBC_SHA256 | 20-25 | |
| TLS_DHE_RSA_WITH_AES_128_GCM_SHA256 | 20-25 | 20-25 |
| TLS_DHE_RSA_WITH_AES_256_CBC_SHA | 9-25 | 20-25 |
| TLS_DHE_RSA_WITH_AES_256_CBC_SHA256 | 20-25 | |
| TLS_DHE_RSA_WITH_AES_256_GCM_SHA384 | 20-25 | 20-25 |
| TLS_DHE_RSA_WITH_DES_CBC_SHA | 1-8 | 1-8 |
| TLS_DH_DSS_EXPORT_WITH_DES40_CBC_SHA | 1-8 | |
| TLS_DH_DSS_WITH_3DES_EDE_CBC_SHA | 1-8 | |
| TLS_DH_DSS_WITH_DES_CBC_SHA | 1-8 | |
| TLS_DH_RSA_EXPORT_WITH_DES40_CBC_SHA | 1-8 | |
| TLS_DH_RSA_WITH_3DES_EDE_CBC_SHA | 1-8 | |
| TLS_DH_RSA_WITH_DES_CBC_SHA | 1-8 | |
| TLS_DH_anon_EXPORT_WITH_DES40_CBC_SHA | 1-8 | |
| TLS_DH_anon_WITH_3DES_EDE_CBC_SHA | 1-8 | |
| TLS_DH_anon_WITH_AES_128_CBC_SHA | 9-22 | |
| TLS_DH_anon_WITH_AES_128_CBC_SHA256 | 20-22 | |
| TLS_DH_anon_WITH_AES_128_GCM_SHA256 | 20-22 | |
| TLS_DH_anon_WITH_AES_256_CBC_SHA | 9-22 | |
| TLS_DH_anon_WITH_AES_256_CBC_SHA256 | 20-22 | |
| TLS_DH_anon_WITH_AES_256_GCM_SHA384 | 20-22 | |
| TLS_DH_anon_WITH_DES_CBC_SHA | 1-8 | |
| TLS_ECDHE_ECDSA_WITH_3DES_EDE_CBC_SHA | 20-22 | |
| TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA | 20+ | 20+ |
| TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA256 | 20-28 | |
| TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256 | 20+ | 20+ |
| TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA | 20+ | 20+ |
| TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA384 | 20-28 | |
| TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384 | 20+ | 20+ |
| TLS_ECDHE_ECDSA_WITH_CHACHA20_POLY1305_SHA256 | 24+ | 24+ |
| TLS_ECDHE_ECDSA_WITH_NULL_SHA | 20-22 | |
| TLS_ECDHE_ECDSA_WITH_RC4_128_SHA | 20-25 | 20-23 |
| TLS_ECDHE_PSK_WITH_AES_128_CBC_SHA | 21+ | 21+ |
| TLS_ECDHE_PSK_WITH_AES_256_CBC_SHA | 21+ | 21+ |
| TLS_ECDHE_PSK_WITH_CHACHA20_POLY1305_SHA256 | 24+ | 24+ |
| TLS_ECDHE_RSA_WITH_3DES_EDE_CBC_SHA | 20-22 | |
| TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA | 20+ | 20+ |
| TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256 | 20-28 | |
| TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256 | 20+ | 20+ |
| TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA | 20+ | 20+ |
| TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384 | 20-28 | |
| TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384 | 20+ | 20+ |
| TLS_ECDHE_RSA_WITH_CHACHA20_POLY1305_SHA256 | 24+ | 24+ |
| TLS_ECDHE_RSA_WITH_NULL_SHA | 20-22 | |
| TLS_ECDHE_RSA_WITH_RC4_128_SHA | 20-25 | 20-23 |
| TLS_ECDH_ECDSA_WITH_3DES_EDE_CBC_SHA | 20-22 | |
| TLS_ECDH_ECDSA_WITH_AES_128_CBC_SHA | 20-22 | |
| TLS_ECDH_ECDSA_WITH_AES_128_CBC_SHA256 | 20-22 | |
| TLS_ECDH_ECDSA_WITH_AES_128_GCM_SHA256 | 20-22 | |
| TLS_ECDH_ECDSA_WITH_AES_256_CBC_SHA | 20-22 | |
| TLS_ECDH_ECDSA_WITH_AES_256_CBC_SHA384 | 20-22 | |
| TLS_ECDH_ECDSA_WITH_AES_256_GCM_SHA384 | 20-22 | |
| TLS_ECDH_ECDSA_WITH_NULL_SHA | 20-22 | |
| TLS_ECDH_ECDSA_WITH_RC4_128_SHA | 20-22 | |
| TLS_ECDH_RSA_WITH_3DES_EDE_CBC_SHA | 20-22 | |
| TLS_ECDH_RSA_WITH_AES_128_CBC_SHA | 20-22 | |
| TLS_ECDH_RSA_WITH_AES_128_CBC_SHA256 | 20-22 | |
| TLS_ECDH_RSA_WITH_AES_128_GCM_SHA256 | 20-22 | |
| TLS_ECDH_RSA_WITH_AES_256_CBC_SHA | 20-22 | |
| TLS_ECDH_RSA_WITH_AES_256_CBC_SHA384 | 20-22 | |
| TLS_ECDH_RSA_WITH_AES_256_GCM_SHA384 | 20-22 | |
| TLS_ECDH_RSA_WITH_NULL_SHA | 20-22 | |
| TLS_ECDH_RSA_WITH_RC4_128_SHA | 20-22 | |
| TLS_ECDH_anon_WITH_3DES_EDE_CBC_SHA | 20-22 | |
| TLS_ECDH_anon_WITH_AES_128_CBC_SHA | 20-22 | |
| TLS_ECDH_anon_WITH_AES_256_CBC_SHA | 20-22 | |
| TLS_ECDH_anon_WITH_NULL_SHA | 20-22 | |
| TLS_ECDH_anon_WITH_RC4_128_SHA | 20-22 | |
| TLS_EMPTY_RENEGOTIATION_INFO_SCSV | 20+ | 20+ |
| TLS_FALLBACK_SCSV | 21+ | |
| TLS_NULL_WITH_NULL_NULL | 1-8 | |
| TLS_PSK_WITH_3DES_EDE_CBC_SHA | 21-22 | |
| TLS_PSK_WITH_AES_128_CBC_SHA | 21+ | 21+ |
| TLS_PSK_WITH_AES_256_CBC_SHA | 21+ | 21+ |
| TLS_PSK_WITH_RC4_128_SHA | 21-25 | |
| TLS_RSA_EXPORT_WITH_DES40_CBC_SHA | 1-8 | 1-8 |
| TLS_RSA_WITH_3DES_EDE_CBC_SHA | 1-8 | 1-8 |
| TLS_RSA_WITH_AES_128_CBC_SHA | 9+ | 9+ |
| TLS_RSA_WITH_AES_128_CBC_SHA256 | 20-28 | |
| TLS_RSA_WITH_AES_128_GCM_SHA256 | 20+ | 20+ |
| TLS_RSA_WITH_AES_256_CBC_SHA | 9+ | 20+ |
| TLS_RSA_WITH_AES_256_CBC_SHA256 | 20-28 | |
| TLS_RSA_WITH_AES_256_GCM_SHA384 | 20+ | 20+ |
| TLS_RSA_WITH_DES_CBC_SHA | 1-8 | 1-8 |
| TLS_RSA_WITH_NULL_MD5 | 1-8 | |
| TLS_RSA_WITH_NULL_SHA | 1-8 | |
| TLS_RSA_WITH_NULL_SHA256 | 20-22 | |

*NOTE* : PSK cipher suites are enabled by default only if the`SSLContext`through which the engine was created has been initialized with a`PSKKeyManager`.

## Summary

| Protected constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#SSLEngine())`()` Constructor for an`SSLEngine`providing no hints for an internal session reuse strategy. |
| [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#SSLEngine(kotlin.String,%20kotlin.Int))`(`peerHost:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `peerPort:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor for an`SSLEngine`. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [beginHandshake](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#beginHandshake())`()` Initiates handshaking (initial or renegotiation) on this SSLEngine. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [closeInbound](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#closeInbound())`()` Signals that no more inbound network data will be sent to this`SSLEngine`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [closeOutbound](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#closeOutbound())`()` Signals that no more outbound application data will be sent on this`SSLEngine`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getApplicationProtocol](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getApplicationProtocol())`()` Returns the most recent application protocol value negotiated for this connection. |
| abstract [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)! | [getDelegatedTask](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getDelegatedTask())`()` Returns a delegated`Runnable`task for this`SSLEngine`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getEnableSessionCreation](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getEnableSessionCreation())`()` Returns true if new SSL sessions may be established by this engine. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getEnabledCipherSuites](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getEnabledCipherSuites())`()` Returns the names of the SSL cipher suites which are currently enabled for use on this engine. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getEnabledProtocols](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getEnabledProtocols())`()` Returns the names of the protocol versions which are currently enabled for use with this`SSLEngine`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getHandshakeApplicationProtocol](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getHandshakeApplicationProtocol())`()` Returns the application protocol value negotiated on a SSL/TLS handshake currently in progress. |
| open [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\< [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getHandshakeApplicationProtocolSelector](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getHandshakeApplicationProtocolSelector())`()` Retrieves the callback function that selects an application protocol value during a SSL/TLS handshake. |
| open [SSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession)! | [getHandshakeSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getHandshakeSession())`()` Returns the`SSLSession`being constructed during a SSL/TLS handshake. |
| abstract [SSLEngineResult.HandshakeStatus](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult.HandshakeStatus)! | [getHandshakeStatus](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getHandshakeStatus())`()` Returns the current handshake status for this`SSLEngine`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getNeedClientAuth](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getNeedClientAuth())`()` Returns true if the engine will*require*client authentication. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPeerHost](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getPeerHost())`()` Returns the host name of the peer. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPeerPort](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getPeerPort())`()` Returns the port number of the peer. |
| open [SSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters)! | [getSSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getSSLParameters())`()` Returns the SSLParameters in effect for this SSLEngine. |
| abstract [SSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession)! | [getSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getSession())`()` Returns the`SSLSession`in use in this`SSLEngine`. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getSupportedCipherSuites](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getSupportedCipherSuites())`()` Returns the names of the cipher suites which could be enabled for use on this engine. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getSupportedProtocols](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getSupportedProtocols())`()` Returns the names of the protocols which could be enabled for use with this`SSLEngine`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getUseClientMode](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getUseClientMode())`()` Returns true if the engine is set to use client mode when handshaking. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getWantClientAuth](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getWantClientAuth())`()` Returns true if the engine will*request*client authentication. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInboundDone](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#isInboundDone())`()` Returns whether [unwrap(java.nio.ByteBuffer,java.nio.ByteBuffer)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#unwrap(java.nio.ByteBuffer,%20java.nio.ByteBuffer))will accept any more inbound data messages. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOutboundDone](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#isOutboundDone())`()` Returns whether [wrap(java.nio.ByteBuffer,java.nio.ByteBuffer)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#wrap(java.nio.ByteBuffer,%20java.nio.ByteBuffer))will produce any more outbound data messages. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnableSessionCreation](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setEnableSessionCreation(kotlin.Boolean))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Controls whether new SSL sessions may be established by this engine. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnabledCipherSuites](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setEnabledCipherSuites(kotlin.Array))`(`suites:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Sets the cipher suites enabled for use on this engine. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnabledProtocols](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setEnabledProtocols(kotlin.Array))`(`protocols:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Set the protocol versions enabled for use on this engine. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHandshakeApplicationProtocolSelector](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setHandshakeApplicationProtocolSelector(java.util.function.BiFunction))`(`selector:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)< [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#)!,` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Registers a callback function that selects an application protocol value for a SSL/TLS handshake. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNeedClientAuth](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setNeedClientAuth(kotlin.Boolean))`(`need:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Configures the engine to*require*client authentication. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setSSLParameters(javax.net.ssl.SSLParameters))`(`params:` ` [SSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters)!`)` Applies SSLParameters to this engine. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUseClientMode](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setUseClientMode(kotlin.Boolean))`(`mode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Configures the engine to use client (or server) mode when handshaking. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWantClientAuth](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setWantClientAuth(kotlin.Boolean))`(`want:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Configures the engine to*request*client authentication. |
| open [SSLEngineResult](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult)! | [unwrap](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#unwrap(java.nio.ByteBuffer,%20java.nio.ByteBuffer))`(`src:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`, `dst:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`)` Attempts to decode SSL/TLS network data into a plaintext application data buffer. |
| open [SSLEngineResult](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult)! | [unwrap](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#unwrap(java.nio.ByteBuffer,%20kotlin.Array))`(`src:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`, `dsts:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!>!`)` Attempts to decode SSL/TLS network data into a sequence of plaintext application data buffers. |
| abstract [SSLEngineResult](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult)! | [unwrap](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#unwrap(java.nio.ByteBuffer,%20kotlin.Array,%20kotlin.Int,%20kotlin.Int))`(`src:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`, `dsts:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!>!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Attempts to decode SSL/TLS network data into a subsequence of plaintext application data buffers. |
| open [SSLEngineResult](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult)! | [wrap](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#wrap(java.nio.ByteBuffer,%20java.nio.ByteBuffer))`(`src:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`, `dst:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`)` Attempts to encode a buffer of plaintext application data into SSL/TLS network data. |
| abstract [SSLEngineResult](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult)! | [wrap](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#wrap(kotlin.Array,%20kotlin.Int,%20kotlin.Int,%20java.nio.ByteBuffer))`(`srcs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!>!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dst:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`)` Attempts to encode plaintext bytes from a subsequence of data buffers into SSL/TLS network data. |
| open [SSLEngineResult](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult)! | [wrap](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#wrap(kotlin.Array,%20java.nio.ByteBuffer))`(`srcs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!>!`, `dst:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`)` Attempts to encode plaintext bytes from a sequence of data buffers into SSL/TLS network data. |

## Protected constructors

### SSLEngine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected SSLEngine()
```

Constructor for an`SSLEngine`providing no hints for an internal session reuse strategy. 
**See Also**

- [javax.net.ssl.SSLContext#createSSLEngine()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#createSSLEngine())
- [javax.net.ssl.SSLSessionContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionContext) 

### SSLEngine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected SSLEngine(
    peerHost: String!, 
    peerPort: Int)
```

Constructor for an`SSLEngine`.

`SSLEngine`implementations may use the`peerHost`and`peerPort`parameters as hints for their internal session reuse strategy.

Some cipher suites (such as Kerberos) require remote hostname information. Implementations of this class should use this constructor to use Kerberos.

The parameters are not authenticated by the`SSLEngine`.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `peerHost` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the peer host |
| `peerPort` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the port number of the peer |

**See Also**

- [javax.net.ssl.SSLContext#createSSLEngine(String, int)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext#createSSLEngine(kotlin.String,%20kotlin.Int))
- [javax.net.ssl.SSLSessionContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionContext)

## Public methods

### beginHandshake

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun beginHandshake(): Unit
```

Initiates handshaking (initial or renegotiation) on this SSLEngine.

This method is not needed for the initial handshake, as the`wrap()`and`unwrap()`methods will implicitly call this method if handshaking has not already begun.

Note that the peer may also request a session renegotiation with this`SSLEngine`by sending the appropriate session renegotiate handshake message.

Unlike the [SSLSocket#startHandshake()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#startHandshake())method, this method does not block until handshaking is completed.

To force a complete SSL/TLS session renegotiation, the current session should be invalidated prior to calling this method.

Some protocols may not support multiple handshakes on an existing engine and may throw an`SSLException`.

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `javax.net.ssl.SSLException` | if a problem was encountered while signaling the`SSLEngine`to begin a new handshake. See the class description for more information on engine closure. |
| `java.lang.IllegalStateException` | if the client/server mode has not yet been set. |

**See Also**

- [javax.net.ssl.SSLSession#invalidate()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#invalidate()) 

### closeInbound

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun closeInbound(): Unit
```

Signals that no more inbound network data will be sent to this`SSLEngine`.

If the application initiated the closing process by calling [closeOutbound()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#closeOutbound()), under some circumstances it is not required that the initiator wait for the peer's corresponding close message. (See section 7.2.1 of the TLS specification ([RFC 2246](http://www.ietf.org/rfc/rfc2246.txt)) for more information on waiting for closure alerts.) In such cases, this method need not be called.

But if the application did not initiate the closure process, or if the circumstances above do not apply, this method should be called whenever the end of the SSL/TLS data stream is reached. This ensures closure of the inbound side, and checks that the peer followed the SSL/TLS close procedure properly, thus detecting possible truncation attacks.

This method is idempotent: if the inbound side has already been closed, this method does not do anything.

[wrap()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#wrap(java.nio.ByteBuffer,%20java.nio.ByteBuffer))should be called to flush any remaining handshake data.

| Exceptions ||
|------------------------------|----------------------------------------------------------------------------------------------|
| `javax.net.ssl.SSLException` | if this engine has not received the proper SSL/TLS close notification message from the peer. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#isInboundDone()>
- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#isOutboundDone()> 

### closeOutbound

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun closeOutbound(): Unit
```

Signals that no more outbound application data will be sent on this`SSLEngine`.

This method is idempotent: if the outbound side has already been closed, this method does not do anything.

[wrap(java.nio.ByteBuffer,java.nio.ByteBuffer)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#wrap(java.nio.ByteBuffer,%20java.nio.ByteBuffer))should be called to flush any remaining handshake data. 
**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#isOutboundDone()> 

### getApplicationProtocol

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getApplicationProtocol(): String!
```

Returns the most recent application protocol value negotiated for this connection.

If supported by the underlying SSL/TLS implementation, application name negotiation mechanisms such as [RFC 7301](http://www.ietf.org/rfc/rfc7301.txt), the Application-Layer Protocol Negotiation (ALPN), can negotiate application-level values between peers.

<br />

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | null if it has not yet been determined if application protocols might be used for this connection, an empty`String`if application protocols values will not be used, or a non-empty application protocol`String`if a value was successfully negotiated. |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the underlying provider does not implement the operation. |

### getDelegatedTask

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDelegatedTask(): Runnable!
```

Returns a delegated`Runnable`task for this`SSLEngine`.

`SSLEngine`operations may require the results of operations that block, or may take an extended period of time to complete. This method is used to obtain an outstanding operation (task). Each task must be assigned a thread (possibly the current) to perform the [run](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#run())operation. Once the`run`method returns, the`Runnable`object is no longer needed and may be discarded.

Delegated tasks run in the`AccessControlContext`in place when this object was created.

A call to this method will return each outstanding task exactly once.

Multiple delegated tasks can be run in parallel.

| Return ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)! | a delegated`Runnable`task, or null if none are available. |

### getEnableSessionCreation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEnableSessionCreation(): Boolean
```

Returns true if new SSL sessions may be established by this engine.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true indicates that sessions may be created; this is the default. false indicates that an existing session must be resumed |

**See Also**

- [#setEnableSessionCreation(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setEnableSessionCreation(kotlin.Boolean)) 

### getEnabledCipherSuites

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEnabledCipherSuites(): Array<String!>!
```

Returns the names of the SSL cipher suites which are currently enabled for use on this engine. When an SSLEngine is first created, all enabled cipher suites support a minimum quality of service. Thus, in some environments this value might be empty.

Even if a suite has been enabled, it might never be used. (For example, the peer does not support it, the requisite certificates/private keys for the suite are not available, or an anonymous suite is enabled but authentication is required.)

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array of cipher suite names |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getSupportedCipherSuites()> 

### getEnabledProtocols

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEnabledProtocols(): Array<String!>!
```

Returns the names of the protocol versions which are currently enabled for use with this`SSLEngine`.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array of protocols |

**See Also**

### getHandshakeApplicationProtocol

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHandshakeApplicationProtocol(): String!
```

Returns the application protocol value negotiated on a SSL/TLS handshake currently in progress.

Like [getHandshakeSession()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getHandshakeSession()), a connection may be in the middle of a handshake. The application protocol may or may not yet be available.

<br />

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | null if it has not yet been determined if application protocols might be used for this handshake, an empty`String`if application protocols values will not be used, or a non-empty application protocol`String`if a value was successfully negotiated. |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the underlying provider does not implement the operation. |

### getHandshakeApplicationProtocolSelector

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHandshakeApplicationProtocolSelector(): BiFunction<SSLEngine!, MutableList<String!>!, String!>!
```

Retrieves the callback function that selects an application protocol value during a SSL/TLS handshake. See [setHandshakeApplicationProtocolSelector](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setHandshakeApplicationProtocolSelector(java.util.function.BiFunction))for the function's type parameters.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)< [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#)!,` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the callback function, or null if none has been set. |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the underlying provider does not implement the operation. |

### getHandshakeSession

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHandshakeSession(): SSLSession!
```

Returns the`SSLSession`being constructed during a SSL/TLS handshake.

TLS protocols may negotiate parameters that are needed when using an instance of this class, but before the`SSLSession`has been completely initialized and made available via`getSession`. For example, the list of valid signature algorithms may restrict the type of certificates that can used during TrustManager decisions, or the maximum TLS fragment packet sizes can be resized to better support the network environment.

This method provides early access to the`SSLSession`being constructed. Depending on how far the handshake has progressed, some data may not yet be available for use. For example, if a remote server will be sending a Certificate chain, but that chain has yet not been processed, the`getPeerCertificates`method of`SSLSession`will throw a SSLPeerUnverifiedException. Once that chain has been processed,`getPeerCertificates`will return the proper value.

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession)! | null if this instance is not currently handshaking, or if the current handshake has not progressed far enough to create a basic SSLSession. Otherwise, this method returns the`SSLSession`currently being negotiated. |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the underlying provider does not implement the operation. |

**See Also**

- [javax.net.ssl.SSLSocket](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket)
- [javax.net.ssl.SSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession)
- [javax.net.ssl.ExtendedSSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/ExtendedSSLSession)
- [javax.net.ssl.X509ExtendedKeyManager](https://developer.android.com/reference/kotlin/javax/net/ssl/X509ExtendedKeyManager)
- [javax.net.ssl.X509ExtendedTrustManager](https://developer.android.com/reference/kotlin/javax/net/ssl/X509ExtendedTrustManager) 

### getHandshakeStatus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getHandshakeStatus(): SSLEngineResult.HandshakeStatus!
```

Returns the current handshake status for this`SSLEngine`.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [SSLEngineResult.HandshakeStatus](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult.HandshakeStatus)! | the current`SSLEngineResult.HandshakeStatus`. |

### getNeedClientAuth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNeedClientAuth(): Boolean
```

Returns true if the engine will*require*client authentication. This option is only useful to engines in the server mode.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if client authentication is required, or false if no client authentication is desired. |

**See Also**

- [#setNeedClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setNeedClientAuth(kotlin.Boolean))
- [#setWantClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setWantClientAuth(kotlin.Boolean))
- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getWantClientAuth()>
- [#setUseClientMode(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setUseClientMode(kotlin.Boolean)) 

### getPeerHost

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPeerHost(): String!
```

Returns the host name of the peer.

Note that the value is not authenticated, and should not be relied upon.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the host name of the peer, or null if nothing is available. |

### getPeerPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPeerPort(): Int
```

Returns the port number of the peer.

Note that the value is not authenticated, and should not be relied upon.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the port number of the peer, or -1 if nothing is available. |

### getSSLParameters

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSSLParameters(): SSLParameters!
```

Returns the SSLParameters in effect for this SSLEngine. The ciphersuites and protocols of the returned SSLParameters are always non-null.

| Return ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| [SSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters)! | the SSLParameters in effect for this SSLEngine. |

### getSession

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSession(): SSLSession!
```

Returns the`SSLSession`in use in this`SSLEngine`.

These can be long lived, and frequently correspond to an entire login session for some user. The session specifies a particular cipher suite which is being actively used by all connections in that session, as well as the identities of the session's client and server.

Unlike [SSLSocket.getSession()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket#getSession())this method does not block until handshaking is complete.

Until the initial handshake has completed, this method returns a session object which reports an invalid cipher suite of "SSL_NULL_WITH_NULL_NULL".

| Return ||
|----------------------------------------------------------------------------------------|------------------------------------|
| [SSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession)! | the`SSLSession`for this`SSLEngine` |

**See Also**

- [javax.net.ssl.SSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession) 

### getSupportedCipherSuites

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSupportedCipherSuites(): Array<String!>!
```

Returns the names of the cipher suites which could be enabled for use on this engine. Normally, only a subset of these will actually be enabled by default, since this list may include cipher suites which do not meet quality of service requirements for those defaults. Such cipher suites might be useful in specialized applications.

Applications should not blindly enable all supported cipher suites. The supported cipher suites can include signaling cipher suite values that can cause connection problems if enabled inappropriately.

The proper way to use this method is to either check if a specific cipher suite is supported via`Arrays.asList(getSupportedCipherSuites()).contains(...)`or to filter a desired list of cipher suites to only the supported ones via`desiredSuiteSet.retainAll(Arrays.asList(getSupportedCipherSuites()))`.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array of cipher suite names |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getEnabledCipherSuites()> 

### getSupportedProtocols

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSupportedProtocols(): Array<String!>!
```

Returns the names of the protocols which could be enabled for use with this`SSLEngine`.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array of protocols supported |

### getUseClientMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getUseClientMode(): Boolean
```

Returns true if the engine is set to use client mode when handshaking.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the engine should do handshaking in "client" mode |

**See Also**

- [#setUseClientMode(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setUseClientMode(kotlin.Boolean)) 

### getWantClientAuth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getWantClientAuth(): Boolean
```

Returns true if the engine will*request*client authentication. This option is only useful for engines in the server mode.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if client authentication is requested, or false if no client authentication is desired. |

**See Also**

- [#setNeedClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setNeedClientAuth(kotlin.Boolean))
- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getNeedClientAuth()>
- [#setWantClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setWantClientAuth(kotlin.Boolean))
- [#setUseClientMode(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setUseClientMode(kotlin.Boolean)) 

### isInboundDone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isInboundDone(): Boolean
```

Returns whether [unwrap(java.nio.ByteBuffer,java.nio.ByteBuffer)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#unwrap(java.nio.ByteBuffer,%20java.nio.ByteBuffer))will accept any more inbound data messages.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the`SSLEngine`will not consume anymore network data (and by implication, will not produce any more application data.) |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#closeInbound()> 

### isOutboundDone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isOutboundDone(): Boolean
```

Returns whether [wrap(java.nio.ByteBuffer,java.nio.ByteBuffer)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#wrap(java.nio.ByteBuffer,%20java.nio.ByteBuffer))will produce any more outbound data messages.

Note that during the closure phase, a`SSLEngine`may generate handshake closure data that must be sent to the peer.`wrap()`must be called to generate this data. When this method returns true, no more outbound data will be created.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the`SSLEngine`will not produce any more network data |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#closeOutbound()>
- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#closeInbound()> 

### setEnableSessionCreation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setEnableSessionCreation(flag: Boolean): Unit
```

Controls whether new SSL sessions may be established by this engine. If session creations are not allowed, and there are no existing sessions to resume, there will be no successful handshaking.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true indicates that sessions may be created; this is the default. false indicates that an existing session must be resumed |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getEnableSessionCreation()> 

### setEnabledCipherSuites

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setEnabledCipherSuites(suites: Array<String!>!): Unit
```

Sets the cipher suites enabled for use on this engine.

Each cipher suite in the`suites`parameter must have been listed by getSupportedCipherSuites(), or the method will fail. Following a successful call to this method, only suites listed in the`suites`parameter are enabled for use.

See [getEnabledCipherSuites()](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getEnabledCipherSuites())for more information on why a specific cipher suite may never be used on a engine.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `suites` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:Names of all the cipher suites to enable |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | when one or more of the ciphers named by the parameter is not supported, or when the parameter is null. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getSupportedCipherSuites()>
- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getEnabledCipherSuites()> 

### setEnabledProtocols

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setEnabledProtocols(protocols: Array<String!>!): Unit
```

Set the protocol versions enabled for use on this engine.

The protocols must have been listed by getSupportedProtocols() as being supported. Following a successful call to this method, only protocols listed in the`protocols`parameter are enabled for use.

Because of the way the protocol version is negotiated, connections will only be able to use a member of the lowest set of contiguous enabled protocol versions. For example, enabling TLSv1.2 and TLSv1 will result in connections only being able to use TLSv1.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `protocols` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:Names of all the protocols to enable. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | when one or more of the protocols named by the parameter is not supported or when the protocols parameter is null. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getEnabledProtocols()> 

### setHandshakeApplicationProtocolSelector

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setHandshakeApplicationProtocolSelector(selector: BiFunction<SSLEngine!, MutableList<String!>!, String!>!): Unit
```

Registers a callback function that selects an application protocol value for a SSL/TLS handshake. The function overrides any values supplied using [SSLParameters.setApplicationProtocols](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters#setApplicationProtocols(kotlin.Array))and it supports the following type parameters:

`SSLEngine`
: The function's first argument allows the current`SSLEngine`to be inspected, including the handshake session and configuration settings.

`List<String>`
: The function's second argument lists the application protocol names advertised by the TLS peer.

`String`
: The function's result is an application protocol name, or null to indicate that none of the advertised names are acceptable. If the return value is an empty`String`then application protocol indications will not be used. If the return value is null (no value chosen) or is a value that was not advertised by the peer, the underlying protocol will determine what action to take. (For example, ALPN will send a "no_application_protocol" alert and terminate the connection.)
For example, the following call registers a callback function that examines the TLS handshake parameters and selects an application protocol name: 

```kotlin
<code>serverEngine.setHandshakeApplicationProtocolSelector(
          (serverEngine, clientProtocols) -&gt; {
              SSLSession session = serverEngine.getHandshakeSession();
              return chooseApplicationProtocol(
                  serverEngine,
                  clientProtocols,
                  session.getProtocol(),
                  session.getCipherSuite());
          });
  </code>
```

<br />

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `selector` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\< [SSLEngine](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the callback function, or null to disable the callback functionality. |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the underlying provider does not implement the operation. |

### setNeedClientAuth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNeedClientAuth(need: Boolean): Unit
```

Configures the engine to*require*client authentication. This option is only useful for engines in the server mode.

An engine's client authentication setting is one of the following:

- client authentication required
- client authentication requested
- no client authentication desired

Unlike [setWantClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setWantClientAuth(kotlin.Boolean)), if this option is set and the client chooses not to provide authentication information about itself,*the negotiations will stop and the engine will begin its closure procedure*.

Calling this method overrides any previous setting made by this method or [setWantClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setWantClientAuth(kotlin.Boolean)).

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `need` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):set to true if client authentication is required, or false if no client authentication is desired. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getNeedClientAuth()>
- [#setWantClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setWantClientAuth(kotlin.Boolean))
- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getWantClientAuth()>
- [#setUseClientMode(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setUseClientMode(kotlin.Boolean)) 

### setSSLParameters

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSSLParameters(params: SSLParameters!): Unit
```

Applies SSLParameters to this engine.

This means:

- If`params.getCipherSuites()`is non-null,`setEnabledCipherSuites()`is called with that value.
- If`params.getProtocols()`is non-null,`setEnabledProtocols()`is called with that value.
- If`params.getNeedClientAuth()`or`params.getWantClientAuth()`return`true`,`setNeedClientAuth(true)`and`setWantClientAuth(true)`are called, respectively; otherwise`setWantClientAuth(false)`is called.
- If`params.getServerNames()`is non-null, the engine will configure its server names with that value.
- If`params.getSNIMatchers()`is non-null, the engine will configure its SNI matchers with that value.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------|
| `params` | [SSLParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLParameters)!:the parameters |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the setEnabledCipherSuites() or the setEnabledProtocols() call fails |

### setUseClientMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setUseClientMode(mode: Boolean): Unit
```

Configures the engine to use client (or server) mode when handshaking.

This method must be called before any handshaking occurs. Once handshaking has begun, the mode can not be reset for the life of this engine.

Servers normally authenticate themselves, and clients are not required to do so.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the engine should start its handshaking in "client" mode |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if a mode change is attempted after the initial handshake has begun. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getUseClientMode()> 

### setWantClientAuth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setWantClientAuth(want: Boolean): Unit
```

Configures the engine to*request*client authentication. This option is only useful for engines in the server mode.

An engine's client authentication setting is one of the following:

- client authentication required
- client authentication requested
- no client authentication desired

Unlike [setNeedClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setNeedClientAuth(kotlin.Boolean)), if this option is set and the client chooses not to provide authentication information about itself,*the negotiations will continue*.

Calling this method overrides any previous setting made by this method or [setNeedClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setNeedClientAuth(kotlin.Boolean)).

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `want` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):set to true if client authentication is requested, or false if no client authentication is desired. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getWantClientAuth()>
- [#setNeedClientAuth(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setNeedClientAuth(kotlin.Boolean))
- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#getNeedClientAuth()>
- [#setUseClientMode(boolean)](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngine#setUseClientMode(kotlin.Boolean)) 

### unwrap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unwrap(
    src: ByteBuffer!, 
    dst: ByteBuffer!
): SSLEngineResult!
```

Attempts to decode SSL/TLS network data into a plaintext application data buffer.

An invocation of this method behaves in exactly the same manner as the invocation: 

```kotlin
<code><a docref="javax.net.ssl.SSLEngine$unwrap(java.nio.ByteBuffer, kotlin.Array((java.nio.ByteBuffer)), kotlin.Int, kotlin.Int)"> engine.unwrap(src, new ByteBuffer [] </a></code>
```

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:a`ByteBuffer`containing inbound network data. |
| `dst` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:a`ByteBuffer`to hold inbound application data. |

| Return ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [SSLEngineResult](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult)! | an`SSLEngineResult`describing the result of this operation. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `javax.net.ssl.SSLException` | A problem was encountered while processing the data that caused the`SSLEngine`to abort. See the class description for more information on engine closure. |
| `java.nio.ReadOnlyBufferException` | if the`dst`buffer is read-only. |
| `java.lang.IllegalArgumentException` | if either`src`or`dst`is null. |
| `java.lang.IllegalStateException` | if the client/server mode has not yet been set. |

**See Also**

### unwrap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unwrap(
    src: ByteBuffer!, 
    dsts: Array<ByteBuffer!>!
): SSLEngineResult!
```

Attempts to decode SSL/TLS network data into a sequence of plaintext application data buffers.

An invocation of this method behaves in exactly the same manner as the invocation: 

```kotlin
<code><a docref="javax.net.ssl.SSLEngine$unwrap(java.nio.ByteBuffer, kotlin.Array((java.nio.ByteBuffer)), kotlin.Int, kotlin.Int)"> engine.unwrap(src, dsts, 0, dsts.length);</a></code>
```

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:a`ByteBuffer`containing inbound network data. |
| `dsts` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!\>!:an array of`ByteBuffer`s to hold inbound application data. |

| Return ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [SSLEngineResult](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult)! | an`SSLEngineResult`describing the result of this operation. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `javax.net.ssl.SSLException` | A problem was encountered while processing the data that caused the`SSLEngine`to abort. See the class description for more information on engine closure. |
| `java.nio.ReadOnlyBufferException` | if any of the`dst`buffers are read-only. |
| `java.lang.IllegalArgumentException` | if either`src`or`dsts`is null, or if any element in`dsts`is null. |
| `java.lang.IllegalStateException` | if the client/server mode has not yet been set. |

**See Also**

### unwrap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun unwrap(
    src: ByteBuffer!, 
    dsts: Array<ByteBuffer!>!, 
    offset: Int, 
    length: Int
): SSLEngineResult!
```

Attempts to decode SSL/TLS network data into a subsequence of plaintext application data buffers. This*"scattering"* operation decodes, in a single invocation, a sequence of bytes into one or more of a given sequence of buffers. Scattering unwraps are often useful when implementing network protocols or file formats that, for example, group data into segments consisting of one or more fixed-length headers followed by a variable-length body. See [java.nio.channels.ScatteringByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ScatteringByteChannel.html#) for more information on scattering, and[java.nio.channels.ScatteringByteChannel#read(ByteBuffer[], * int, int)](https://developer.android.com/reference/kotlin/java/nio/channels/ScatteringByteChannel.html#read(kotlin.Array,%20kotlin.Int,%20kotlin.Int))for more information on the subsequence behavior.

Depending on the state of the SSLEngine, this method may consume network data without producing any application data (for example, it may consume handshake data.)

The application is responsible for reliably obtaining the network data from the peer, and for invoking unwrap() on the data in the order it was received. The application must properly synchronize multiple calls to this method.

If this`SSLEngine`has not yet started its initial handshake, this method will automatically start the handshake.

This method will attempt to consume one complete SSL/TLS network packet, but will never consume more than the sum of the bytes remaining in the buffers. Each`ByteBuffer`'s position is updated to reflect the amount of data consumed or produced. The limits remain the same.

The underlying memory used by the`src`and`dsts ByteBuffer`s must not be the same.

The inbound network buffer may be modified as a result of this call: therefore if the network data packet is required for some secondary purpose, the data should be duplicated before calling this method. Note: the network data will not be useful to a second SSLEngine, as each SSLEngine contains unique random state which influences the SSL/TLS messages.

See the class description for more information on engine closure.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:a`ByteBuffer`containing inbound network data. |
| `dsts` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!\>!:an array of`ByteBuffer`s to hold inbound application data. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset within the buffer array of the first buffer from which bytes are to be transferred; it must be non-negative and no larger than`dsts.length`. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum number of buffers to be accessed; it must be non-negative and no larger than`dsts.length`-`offset`. |

| Return ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [SSLEngineResult](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult)! | an`SSLEngineResult`describing the result of this operation. |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `javax.net.ssl.SSLException` | A problem was encountered while processing the data that caused the`SSLEngine`to abort. See the class description for more information on engine closure. |
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`offset`and`length`parameters do not hold. |
| `java.nio.ReadOnlyBufferException` | if any of the`dst`buffers are read-only. |
| `java.lang.IllegalArgumentException` | if either`src`or`dsts`is null, or if any element in the`dsts`subsequence specified is null. |
| `java.lang.IllegalStateException` | if the client/server mode has not yet been set. |

**See Also**

- [java.nio.channels.ScatteringByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ScatteringByteChannel.html#)
- [java.nio.channels.ScatteringByteChannel#read(
* ByteBuffer[], int, int)](https://developer.android.com/reference/kotlin/java/nio/channels/ScatteringByteChannel.html#read(kotlin.Array,%20kotlin.Int,%20kotlin.Int)) 

### wrap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun wrap(
    src: ByteBuffer!, 
    dst: ByteBuffer!
): SSLEngineResult!
```

Attempts to encode a buffer of plaintext application data into SSL/TLS network data.

An invocation of this method behaves in exactly the same manner as the invocation: 

```kotlin
<code><a docref="javax.net.ssl.SSLEngine$wrap(kotlin.Array((java.nio.ByteBuffer)), kotlin.Int, kotlin.Int, java.nio.ByteBuffer)"> engine.wrap(new ByteBuffer [] </a></code>
```

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:a`ByteBuffer`containing outbound application data |
| `dst` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:a`ByteBuffer`to hold outbound network data |

| Return ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [SSLEngineResult](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult)! | an`SSLEngineResult`describing the result of this operation. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `javax.net.ssl.SSLException` | A problem was encountered while processing the data that caused the`SSLEngine`to abort. See the class description for more information on engine closure. |
| `java.nio.ReadOnlyBufferException` | if the`dst`buffer is read-only. |
| `java.lang.IllegalArgumentException` | if either`src`or`dst`is null. |
| `java.lang.IllegalStateException` | if the client/server mode has not yet been set. |

**See Also**

### wrap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun wrap(
    srcs: Array<ByteBuffer!>!, 
    offset: Int, 
    length: Int, 
    dst: ByteBuffer!
): SSLEngineResult!
```

Attempts to encode plaintext bytes from a subsequence of data buffers into SSL/TLS network data. This*"gathering"* operation encodes, in a single invocation, a sequence of bytes from one or more of a given sequence of buffers. Gathering wraps are often useful when implementing network protocols or file formats that, for example, group data into segments consisting of one or more fixed-length headers followed by a variable-length body. See [java.nio.channels.GatheringByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/GatheringByteChannel.html#) for more information on gathering, and[java.nio.channels.GatheringByteChannel#write(ByteBuffer[], * int, int)](https://developer.android.com/reference/kotlin/java/nio/channels/GatheringByteChannel.html#write(kotlin.Array,%20kotlin.Int,%20kotlin.Int))for more information on the subsequence behavior.

Depending on the state of the SSLEngine, this method may produce network data without consuming any application data (for example, it may generate handshake data.)

The application is responsible for reliably transporting the network data to the peer, and for ensuring that data created by multiple calls to wrap() is transported in the same order in which it was generated. The application must properly synchronize multiple calls to this method.

If this`SSLEngine`has not yet started its initial handshake, this method will automatically start the handshake.

This method will attempt to produce SSL/TLS records, and will consume as much source data as possible, but will never consume more than the sum of the bytes remaining in each buffer. Each`ByteBuffer`'s position is updated to reflect the amount of data consumed or produced. The limits remain the same.

The underlying memory used by the`srcs`and`dst ByteBuffer`s must not be the same.

See the class description for more information on engine closure.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `srcs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!\>!:an array of`ByteBuffers`containing the outbound application data |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset within the buffer array of the first buffer from which bytes are to be retrieved; it must be non-negative and no larger than`srcs.length` |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum number of buffers to be accessed; it must be non-negative and no larger than`srcs.length`-`offset` |
| `dst` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:a`ByteBuffer`to hold outbound network data |

| Return ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [SSLEngineResult](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult)! | an`SSLEngineResult`describing the result of this operation. |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `javax.net.ssl.SSLException` | A problem was encountered while processing the data that caused the`SSLEngine`to abort. See the class description for more information on engine closure. |
| `java.lang.IndexOutOfBoundsException` | if the preconditions on the`offset`and`length`parameters do not hold. |
| `java.nio.ReadOnlyBufferException` | if the`dst`buffer is read-only. |
| `java.lang.IllegalArgumentException` | if either`srcs`or`dst`is null, or if any element in the`srcs`subsequence specified is null. |
| `java.lang.IllegalStateException` | if the client/server mode has not yet been set. |

**See Also**

- [java.nio.channels.GatheringByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/GatheringByteChannel.html#)
- [java.nio.channels.GatheringByteChannel#write(
* ByteBuffer[], int, int)](https://developer.android.com/reference/kotlin/java/nio/channels/GatheringByteChannel.html#write(kotlin.Array,%20kotlin.Int,%20kotlin.Int)) 

### wrap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun wrap(
    srcs: Array<ByteBuffer!>!, 
    dst: ByteBuffer!
): SSLEngineResult!
```

Attempts to encode plaintext bytes from a sequence of data buffers into SSL/TLS network data.

An invocation of this method behaves in exactly the same manner as the invocation: 

```kotlin
<code><a docref="javax.net.ssl.SSLEngine$wrap(kotlin.Array((java.nio.ByteBuffer)), kotlin.Int, kotlin.Int, java.nio.ByteBuffer)"> engine.wrap(srcs, 0, srcs.length, dst);</a></code>
```

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `srcs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!\>!:an array of`ByteBuffers`containing the outbound application data |
| `dst` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:a`ByteBuffer`to hold outbound network data |

| Return ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [SSLEngineResult](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult)! | an`SSLEngineResult`describing the result of this operation. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `javax.net.ssl.SSLException` | A problem was encountered while processing the data that caused the`SSLEngine`to abort. See the class description for more information on engine closure. |
| `java.nio.ReadOnlyBufferException` | if the`dst`buffer is read-only. |
| `java.lang.IllegalArgumentException` | if either`srcs`or`dst`is null, or if any element in`srcs`is null. |
| `java.lang.IllegalStateException` | if the client/server mode has not yet been set. |

**See Also**
