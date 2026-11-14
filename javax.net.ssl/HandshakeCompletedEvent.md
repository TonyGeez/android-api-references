# HandshakeCompletedEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HandshakeCompletedEvent

```
open class HandshakeCompletedEvent : EventObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.EventObject](../java.util/EventObject.md) ||
| | ↳ | [javax.net.ssl.HandshakeCompletedEvent](HandshakeCompletedEvent.md) |

This event indicates that an SSL handshake completed on a given SSL connection. All of the core information about that handshake's result is captured through an "SSLSession" object. As a convenience, this event class provides direct access to some important session attributes.

The source of this event is the SSLSocket on which handshaking just completed.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [HandshakeCompletedEvent](HandshakeCompletedEvent.md))`(`sock:` ` [SSLSocket](SSLSocket.md)!`, `s:` ` [SSLSession](SSLSession.md)!`)` Constructs a new HandshakeCompletedEvent. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCipherSuite](HandshakeCompletedEvent.md))`()` Returns the cipher suite in use by the session which was produced by the handshake. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Certificate](../java.security.cert/Certificate.md)!\>! | [getLocalCertificates](HandshakeCompletedEvent.md))`()` Returns the certificate(s) that were sent to the peer during handshaking. |
| open [Principal](../java.security/Principal.md)! | [getLocalPrincipal](HandshakeCompletedEvent.md))`()` Returns the principal that was sent to the peer during handshaking. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [X509Certificate](../javax.security.cert/X509Certificate.md)!\>! | [getPeerCertificateChain](HandshakeCompletedEvent.md))`()` Returns the identity of the peer which was identified as part of defining the session. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Certificate](../java.security.cert/Certificate.md)!\>! | [getPeerCertificates](HandshakeCompletedEvent.md))`()` Returns the identity of the peer which was established as part of defining the session. |
| open [Principal](../java.security/Principal.md)! | [getPeerPrincipal](HandshakeCompletedEvent.md))`()` Returns the identity of the peer which was established as part of defining the session. |
| --- | --- |
| open [SSLSession](SSLSession.md)! | [getSession](HandshakeCompletedEvent.md))`()` Returns the session that triggered this event. |
| open [SSLSocket](SSLSocket.md)! | [getSocket](HandshakeCompletedEvent.md))`()` Returns the socket which is the source of this event. |

| Inherited functions ||
|---|---|
| From class [EventObject](../java.util/EventObject.md) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getSource](../java.util/EventObject.md))`()` <br /> The object on which the Event initially occurred. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java.util/EventObject.md))`()` <br /> Returns a String representation of this EventObject. <br /> | ||

| Inherited properties ||
|---|---|
| From class [EventObject](../java.util/EventObject.md) |-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [source](../java.util/EventObject.md) <br /> The object on which the Event initially occurred. <br /> | ||

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
| `sock` | [SSLSocket](SSLSocket.md)!:the SSLSocket acting as the source of the event |
| `s` | [SSLSession](SSLSession.md)!:the SSLSession this event is associated with |

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
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Certificate](../java.security.cert/Certificate.md)!>! | an ordered array of certificates, with the local certificate first followed by any certificate authorities. If no certificates were sent, then null is returned. |

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
| [Principal](../java.security/Principal.md)! | the principal sent to the peer. Returns an X500Principal of the end-entity certificate for X509-based cipher suites, and KerberosPrincipal for Kerberos cipher suites. If no principal was sent, then null is returned. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedEvent#getLocalCertificates()>
- <https://developer.android.com/reference/kotlin/javax/net/ssl/HandshakeCompletedEvent#getPeerPrincipal()> 

### getPeerCertificateChain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPeerCertificateChain(): Array<X509Certificate!>!
```

Returns the identity of the peer which was identified as part of defining the session. Note: This method can be used only when using certificate-based cipher suites; using it with non-certificate-based cipher suites, such as Kerberos, will throw an SSLPeerUnverifiedException.

*Note: this method exists for compatibility with previous releases. New applications should use [getPeerCertificates](HandshakeCompletedEvent.md))instead.*

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](../javax.security.cert/X509Certificate.md)!>! | an ordered array of peer X.509 certificates, with the peer's own certificate first followed by any certificate authorities. (The certificates are in the original JSSE [javax.security.cert.X509Certificate](../javax.security.cert/X509Certificate.md) format). |

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
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Certificate](../java.security.cert/Certificate.md)!>! | an ordered array of the peer certificates, with the peer's own certificate first followed by any certificate authorities. |

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
| [Principal](../java.security/Principal.md)! | the peer's principal. Returns an X500Principal of the end-entity certiticate for X509-based cipher suites, and KerberosPrincipal for Kerberos cipher suites. |

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
| [SSLSession](SSLSession.md)! | the`SSLSession`for this handshake |

### getSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSocket(): SSLSocket!
```

Returns the socket which is the source of this event. (This is a convenience function, to let applications write code without type casts.)

| Return ||
|--------------------------------------------------------------------------------------|----------------------------------------------|
| [SSLSocket](SSLSocket.md)! | the socket on which the connection was made. |
