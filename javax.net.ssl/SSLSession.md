# SSLSession

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLSession

```
interface SSLSession
```

| [javax.net.ssl.SSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#) |

| Known Direct Subclasses [ExtendedSSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/ExtendedSSLSession) |-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------| | [ExtendedSSLSession](https://developer.android.com/reference/kotlin/javax/net/ssl/ExtendedSSLSession) | Extends the`SSLSession`interface to support additional session attributes. | |
| --- | --- | --- | --- | --- | --- | --- |

In SSL, sessions are used to describe an ongoing relationship between two entities. Each SSL connection involves one session at a time, but that session may be used on many connections between those entities, simultaneously or sequentially. The session used on a connection may also be replaced by a different session. Sessions are created, or rejoined, as part of the SSL handshaking protocol. Sessions may be invalidated due to policies affecting security or resource usage, or by an application explicitly calling`invalidate`. Session management policies are typically used to tune performance.

In addition to the standard session attributes, SSL sessions expose these read-only attributes:

- *Peer Identity.*Sessions are between a particular client and a particular server. The identity of the peer may have been established as part of session setup. Peers are generally identified by X.509 certificate chains.
- *Cipher Suite Name.*Cipher suites describe the kind of cryptographic protection that's used by connections in a particular session.
- *Peer Host.*All connections in a session are between the same two hosts. The address of the host on the other side of the connection is available.

Sessions may be explicitly invalidated. Invalidation may also be done implicitly, when faced with certain kinds of errors.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getApplicationBufferSize](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getApplicationBufferSize())`()` Gets the current size of the largest application data that is expected when using this session. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCipherSuite](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getCipherSuite())`()` Returns the name of the SSL cipher suite which is used for all connections in the session. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCreationTime](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getCreationTime())`()` Returns the time at which this Session representation was created, in milliseconds since midnight, January 1, 1970 UTC. |
| --- | --- |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getId](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getId())`()` Returns the identifier assigned to this Session. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLastAccessedTime](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getLastAccessedTime())`()` Returns the last time this Session representation was accessed by the session level infrastructure, in milliseconds since midnight, January 1, 1970 UTC. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate.html#)!\>! | [getLocalCertificates](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getLocalCertificates())`()` Returns the certificate(s) that were sent to the peer during handshaking. |
| --- | --- |
| abstract [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)! | [getLocalPrincipal](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getLocalPrincipal())`()` Returns the principal that was sent to the peer during handshaking. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPacketBufferSize](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getPacketBufferSize())`()` Gets the current size of the largest SSL/TLS packet that is expected when using this session. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [X509Certificate](https://developer.android.com/reference/kotlin/javax/security/cert/X509Certificate.html#)!\>! | [getPeerCertificateChain](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getPeerCertificateChain())`()` Returns the identity of the peer which was identified as part of defining the session. |
| --- | --- |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate.html#)!\>! | [getPeerCertificates](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getPeerCertificates())`()` Returns the identity of the peer which was established as part of defining the session. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPeerHost](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getPeerHost())`()` Returns the host name of the peer in this session. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPeerPort](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getPeerPort())`()` Returns the port number of the peer in this session. |
| --- | --- |
| abstract [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)! | [getPeerPrincipal](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getPeerPrincipal())`()` Returns the identity of the peer which was established as part of defining the session. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getProtocol](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getProtocol())`()` Returns the standard name of the protocol used for all connections in the session. |
| abstract [SSLSessionContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionContext)! | [getSessionContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getSessionContext())`()` Returns the context in which this session is bound. |
| --- | --- |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getValue](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getValue(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the object bound to the given name in the session's application layer data. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getValueNames](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getValueNames())`()` Returns an array of the names of all the application layer data objects bound into the Session. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [invalidate](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#invalidate())`()` Invalidates the session. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValid](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#isValid())`()` Returns whether this session is valid and available for resuming or joining. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putValue](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#putValue(kotlin.String,%20kotlin.Any))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Binds the specified`value`object into the session's application layer data with the given`name`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeValue](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#removeValue(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Removes the object bound to the given name in the session's application layer data. |
| --- | --- |

## Public methods

### getApplicationBufferSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getApplicationBufferSize(): Int
```

Gets the current size of the largest application data that is expected when using this session.

`SSLEngine`application data buffers must be large enough to hold the application data from any inbound network application data packet received. Typically, outbound application data buffers can be of any size.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current maximum expected application packet size |

**See Also**

### getCipherSuite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCipherSuite(): String!
```

Returns the name of the SSL cipher suite which is used for all connections in the session.

This defines the level of protection provided to the data sent on the connection, including the kind of encryption used and most aspects of how authentication is done.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the session's cipher suite |

### getCreationTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCreationTime(): Long
```

Returns the time at which this Session representation was created, in milliseconds since midnight, January 1, 1970 UTC.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the time this Session was created |

### getId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getId(): ByteArray!
```

Returns the identifier assigned to this Session.

| Return ||
|------------------------------------------------------------------------------------------|------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the Session identifier |

### getLastAccessedTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLastAccessedTime(): Long
```

Returns the last time this Session representation was accessed by the session level infrastructure, in milliseconds since midnight, January 1, 1970 UTC.

Access indicates a new connection being established using session data. Application level operations, such as getting or setting a value associated with the session, are not reflected in this access time.

This information is particularly useful in session management policies. For example, a session manager thread could leave all sessions in a given context which haven't been used in a long time; or, the sessions might be sorted according to age to optimize some task.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the last time this Session was accessed |

### getLocalCertificates

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLocalCertificates(): Array<Certificate!>!
```

Returns the certificate(s) that were sent to the peer during handshaking.

Note: This method is useful only when using certificate-based cipher suites.

When multiple certificates are available for use in a handshake, the implementation chooses what it considers the "best" certificate chain available, and transmits that to the other side. This method allows the caller to know which certificate chain was actually used.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate.html#)!>! | an ordered array of certificates, with the local certificate first followed by any certificate authorities. If no certificates were sent, then null is returned. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getLocalPrincipal()> 

### getLocalPrincipal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLocalPrincipal(): Principal!
```

Returns the principal that was sent to the peer during handshaking.

| Return ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)! | the principal sent to the peer. Returns an X500Principal of the end-entity certificate for X509-based cipher suites, and KerberosPrincipal for Kerberos cipher suites. If no principal was sent, then null is returned. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getLocalCertificates()>
- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getPeerPrincipal()> 

### getPacketBufferSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPacketBufferSize(): Int
```

Gets the current size of the largest SSL/TLS packet that is expected when using this session.

A`SSLEngine`using this session may generate SSL/TLS packets of any size up to and including the value returned by this method. All`SSLEngine`network buffers should be sized at least this large to avoid insufficient space problems when performing`wrap`and`unwrap`calls.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current maximum expected network packet size |

**See Also**

### getPeerCertificateChain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPeerCertificateChain(): Array<X509Certificate!>!
```

Returns the identity of the peer which was identified as part of defining the session.

Note: This method can be used only when using certificate-based cipher suites; using it with non-certificate-based cipher suites, such as Kerberos, will throw an SSLPeerUnverifiedException.

*Note: this method exists for compatibility with previous releases. New applications should use [getPeerCertificates](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getPeerCertificates())instead.*

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [X509Certificate](https://developer.android.com/reference/kotlin/javax/security/cert/X509Certificate.html#)!>! | an ordered array of peer X.509 certificates, with the peer's own certificate first followed by any certificate authorities. (The certificates are in the original JSSE certificate [javax.security.cert.X509Certificate](https://developer.android.com/reference/kotlin/javax/security/cert/X509Certificate.html#) format.) |

| Exceptions ||
|--------------------------------------------|----------------------------------------------|
| `javax.net.ssl.SSLPeerUnverifiedException` | if the peer's identity has not been verified |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getPeerPrincipal()> 

### getPeerCertificates

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPeerCertificates(): Array<Certificate!>!
```

Returns the identity of the peer which was established as part of defining the session.

Note: This method can be used only when using certificate-based cipher suites; using it with non-certificate-based cipher suites, such as Kerberos, will throw an SSLPeerUnverifiedException.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate.html#)!>! | an ordered array of peer certificates, with the peer's own certificate first followed by any certificate authorities. |

| Exceptions ||
|--------------------------------------------|----------------------------------------------|
| `javax.net.ssl.SSLPeerUnverifiedException` | if the peer's identity has not been verified |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getPeerPrincipal()> 

### getPeerHost

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPeerHost(): String!
```

Returns the host name of the peer in this session.

For the server, this is the client's host; and for the client, it is the server's host. The name may not be a fully qualified host name or even a host name at all as it may represent a string encoding of the peer's network address. If such a name is desired, it might be resolved through a name service based on the value returned by this method.

This value is not authenticated and should not be relied upon. It is mainly used as a hint for`SSLSession`caching strategies.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the host name of the peer host, or null if no information is available. |

### getPeerPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPeerPort(): Int
```

Returns the port number of the peer in this session.

For the server, this is the client's port number; and for the client, it is the server's port number.

This value is not authenticated and should not be relied upon. It is mainly used as a hint for`SSLSession`caching strategies.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the port number of the peer host, or -1 if no information is available. |

### getPeerPrincipal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPeerPrincipal(): Principal!
```

Returns the identity of the peer which was established as part of defining the session.

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)! | the peer's principal. Returns an X500Principal of the end-entity certiticate for X509-based cipher suites, and KerberosPrincipal for Kerberos cipher suites. |

| Exceptions ||
|--------------------------------------------|----------------------------------------------|
| `javax.net.ssl.SSLPeerUnverifiedException` | if the peer's identity has not been verified |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getPeerCertificates()>
- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#getLocalPrincipal()> 

### getProtocol

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getProtocol(): String!
```

Returns the standard name of the protocol used for all connections in the session.

This defines the protocol used in the connection.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the standard name of the protocol used for all connections in the session. |

### getSessionContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSessionContext(): SSLSessionContext!
```

Returns the context in which this session is bound.

This context may be unavailable in some environments, in which case this method returns null.

If the context is available and there is a security manager installed, the caller may require permission to access it or a security exception may be thrown. In a Java environment, the security manager's`checkPermission`method is called with a`SSLPermission("getSSLSessionContext")`permission.

| Return ||
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [SSLSessionContext](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSessionContext)! | the session context used for this session, or null if the context is unavailable. |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------|
| `java.lang.SecurityException` | if the calling thread does not have permission to get SSL session context. |

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getValue(name: String!): Any!
```

Returns the object bound to the given name in the session's application layer data. Returns null if there is no such binding.

For security reasons, the same named values may not be visible across different access control contexts.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the binding to find. |

| Return ||
|-----------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the value bound to that name, or null if the binding does not exist. |

| Exceptions ||
|--------------------------------------|--------------------------|
| `java.lang.IllegalArgumentException` | if the argument is null. |

### getValueNames

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getValueNames(): Array<String!>!
```

Returns an array of the names of all the application layer data objects bound into the Session.

For security reasons, the same named values may not be visible across different access control contexts.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | a non-null (possibly empty) array of names of the objects bound to this Session. |

### invalidate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun invalidate(): Unit
```

Invalidates the session.

Future connections will not be able to resume or join this session. However, any existing connection using this session can continue to use the session until the connection is closed. 
**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#isValid()> 

### isValid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isValid(): Boolean
```

Returns whether this session is valid and available for resuming or joining.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this session may be rejoined. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSession#invalidate()> 

### putValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun putValue(
    name: String!, 
    value: Any!
): Unit
```

Binds the specified`value`object into the session's application layer data with the given`name`.

Any existing binding using the same`name`is replaced. If the new (or existing)`value`implements the`SSLSessionBindingListener`interface, the object represented by`value`is notified appropriately.

For security reasons, the same named values may not be visible across different access control contexts.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name to which the data object will be bound. This may not be null. |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the data object to be bound. This may not be null. |

| Exceptions ||
|--------------------------------------|-----------------------------|
| `java.lang.IllegalArgumentException` | if either argument is null. |

### removeValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeValue(name: String!): Unit
```

Removes the object bound to the given name in the session's application layer data. Does nothing if there is no object bound to the given name. If the bound existing object implements the`SessionBindingListener`interface, it is notified appropriately.

For security reasons, the same named values may not be visible across different access control contexts.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the object to remove visible across different access control contexts |

| Exceptions ||
|--------------------------------------|--------------------------|
| `java.lang.IllegalArgumentException` | if the argument is null. |
