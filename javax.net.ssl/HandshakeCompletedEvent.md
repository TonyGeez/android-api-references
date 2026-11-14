# HandshakeCompletedEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HandshakeCompletedEvent

```
open class HandshakeCompletedEvent : EventObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) ||
| | ↳ | [javax.net.ssl.HandshakeCompletedEvent](https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedEvent#) |

This event indicates that an SSL handshake completed on a given SSL connection. All of the core information about that handshake's result is captured through an "SSLSession" object. As a convenience, this event class provides direct access to some important session attributes.

The source of this event is the SSLSocket on which handshaking just completed.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [HandshakeCompletedEvent](https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedEvent#HandshakeCompletedEvent(javax.net.ssl.SSLSocket,%20javax.net.ssl.SSLSession))`(`sock:` ` [SSLSocket](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket)!`, `s:` ` [SSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession)!`)` Constructs a new HandshakeCompletedEvent. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCipherSuite](https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedEvent#getCipherSuite())`()` Returns the cipher suite in use by the session which was produced by the handshake. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate.html#)!\>! | [getLocalCertificates](https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedEvent#getLocalCertificates())`()` Returns the certificate(s) that were sent to the peer during handshaking. |
| open [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)! | [getLocalPrincipal](https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedEvent#getLocalPrincipal())`()` Returns the principal that was sent to the peer during handshaking. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [X509Certificate](https://developer.android.com/reference/kotlin/javax/security/cert/X509Certificate.html#)!\>! | [getPeerCertificateChain](https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedEvent#getPeerCertificateChain())`()` Returns the identity of the peer which was identified as part of defining the session. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate.html#)!\>! | [getPeerCertificates](https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedEvent#getPeerCertificates())`()` Returns the identity of the peer which was established as part of defining the session. |
| open [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)! | [getPeerPrincipal](https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedEvent#getPeerPrincipal())`()` Returns the identity of the peer which was established as part of defining the session. |
| --- | --- |
| open [SSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession)! | [getSession](https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedEvent#getSession())`()` Returns the session that triggered this event. |
| open [SSLSocket](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket)! | [getSocket](https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedEvent#getSocket())`()` Returns the socket which is the source of this event. |

| Inherited functions ||
|---|---|
| From class [EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getSource](https://developer.android.com/reference/kotlin/java/util/EventObject.html#getSource())`()` <br /> The object on which the Event initially occurred. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/EventObject.html#toString())`()` <br /> Returns a String representation of this EventObject. <br /> | ||

| Inherited properties ||
|---|---|
| From class [EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) |-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [source](https://developer.android.com/reference/kotlin/java/util/EventObject.html#source:kotlin.Any) <br /> The object on which the Event initially occurred. <br /> | ||

## Public constructors

### HandshakeCompletedEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HandshakeCompletedEvent(
    sock: SSLSocket!, 
    s: SSLSession!)
```

Constructs a new HandshakeCompletedEvent.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------|
| `sock` | [SSLSocket](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket)!:the SSLSocket acting as the source of the event |
| `s` | [SSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession)!:the SSLSession this event is associated with |

## Public methods

### getCipherSuite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCipherSuite(): String!
```

Returns the cipher suite in use by the session which was produced by the handshake. (This is a convenience method for getting the ciphersuite from the SSLsession.)

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the cipher suite negotiated during this session. |

### getLocalCertificates

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocalCertificates(): Array<Certificate!>!
```

Returns the certificate(s) that were sent to the peer during handshaking. Note: This method is useful only when using certificate-based cipher suites. When multiple certificates are available for use in a handshake, the implementation chooses what it considers the "best" certificate chain available, and transmits that to the other side. This method allows the caller to know which certificate chain was actually used.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate.html#)!>! | an ordered array of certificates, with the local certificate first followed by any certificate authorities. If no certificates were sent, then null is returned. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedEvent#getLocalPrincipal()> 

### getLocalPrincipal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocalPrincipal(): Principal!
```

Returns the principal that was sent to the peer during handshaking.

| Return ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)! | the principal sent to the peer. Returns an X500Principal of the end-entity certificate for X509-based cipher suites, and KerberosPrincipal for Kerberos cipher suites. If no principal was sent, then null is returned. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedEvent#getLocalCertificates()>
- <https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedEvent#getPeerPrincipal()> 

### getPeerCertificateChain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPeerCertificateChain(): Array<X509Certificate!>!
```

Returns the identity of the peer which was identified as part of defining the session. Note: This method can be used only when using certificate-based cipher suites; using it with non-certificate-based cipher suites, such as Kerberos, will throw an SSLPeerUnverifiedException.

*Note: this method exists for compatibility with previous releases. New applications should use [getPeerCertificates](https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedEvent#getPeerCertificates())instead.*

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](https://developer.android.com/reference/kotlin/javax/security/cert/X509Certificate.html#)!>! | an ordered array of peer X.509 certificates, with the peer's own certificate first followed by any certificate authorities. (The certificates are in the original JSSE [javax.security.cert.X509Certificate](https://developer.android.com/reference/kotlin/javax/security/cert/X509Certificate.html#) format). |

| Exceptions ||
|--------------------------------------------|------------------------------|
| `javax.net.ssl.SSLPeerUnverifiedException` | if the peer is not verified. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedEvent#getPeerPrincipal()> 

### getPeerCertificates

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPeerCertificates(): Array<Certificate!>!
```

Returns the identity of the peer which was established as part of defining the session. Note: This method can be used only when using certificate-based cipher suites; using it with non-certificate-based cipher suites, such as Kerberos, will throw an SSLPeerUnverifiedException.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate.html#)!>! | an ordered array of the peer certificates, with the peer's own certificate first followed by any certificate authorities. |

| Exceptions ||
|--------------------------------------------|------------------------------|
| `javax.net.ssl.SSLPeerUnverifiedException` | if the peer is not verified. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedEvent#getPeerPrincipal()> 

### getPeerPrincipal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPeerPrincipal(): Principal!
```

Returns the identity of the peer which was established as part of defining the session.

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)! | the peer's principal. Returns an X500Principal of the end-entity certiticate for X509-based cipher suites, and KerberosPrincipal for Kerberos cipher suites. |

| Exceptions ||
|--------------------------------------------|----------------------------------------------|
| `javax.net.ssl.SSLPeerUnverifiedException` | if the peer's identity has not been verified |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedEvent#getPeerCertificates()>
- <https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedEvent#getLocalPrincipal()> 

### getSession

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSession(): SSLSession!
```

Returns the session that triggered this event.

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------|
| [SSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession)! | the`SSLSession`for this handshake |

### getSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSocket(): SSLSocket!
```

Returns the socket which is the source of this event. (This is a convenience function, to let applications write code without type casts.)

| Return ||
|--------------------------------------------------------------------------------------|----------------------------------------------|
| [SSLSocket](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket)! | the socket on which the connection was made. |
